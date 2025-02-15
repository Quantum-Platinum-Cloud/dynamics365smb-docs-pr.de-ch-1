---
title: Buchungsdatum auf Wertposten
description: 'Erfahren Sie wie die Stapelverarbeitung Lagerreg gekennzeichnet wird und ein Buchungsdatum auf Wertposten zugewiesen wird, der die Stapelverarbeitung erstellt.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---
# <a name="design-details-posting-date-on-adjustment-value-entry" />Designdetails: Buchungsdatum auf Ausgleichs-Wertposten

Dieser Artikel enthält Anleitungen für Benutzer der Funktionalität der Bestandskalkulation in [!INCLUDE[prod_short](includes/prod_short.md)] und insbesondere für die Art und Weise, wie der Batchauftrag **Kosten kalkulieren – Element-Einträge** die Wert-Einträge, die der Batchauftrag erstellen soll, identifiziert und ihnen ein Buchungsdatum zuweist.

## <a name="how-posting-dates-are-assigned" />Wie Buchungsdaten zugewiesen werden

Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** weist ein Buchungsdatum dem Wertposten zu, den sie im Begriffe ist, in den nachfolgenden Schritten zu erstellen:  

1. Das Buchungsdatum des Postens hat das gleiche Datum, wie der angepasste Posten.  

2. Das Buchungsdatum wird mit den Lagerbuchungsperioden und/oder Fibuposteneinrichtung überprüft.  

3. Zuweisung des Buchungsdatums; wenn das ursprüngliche Buchungsdatum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums liegt, wird die Stapelverarbeitung ein zulässiges Buchungsdatum aus entweder Fibuposteneinrichtung oder Lagerbuchungsperiode zuweisen. Wenn die Lagerbuchungsperioden und die zugelassenen Buchungszeiträume in der Fibuposteneinrichtung festgelegt wurden, wird das Datum der beiden dem Ausgleichs-Wertposten zugeordnet.  

Lassen Sie uns dieses Verfahren in der Praxis überprüfen. Angenommen, wir haben einen Lagerposten zum Verkauf. Der Artikel wurde am 5. September 2020 geliefert und er wurde am darauffolgenden Tag fakturiert.  

#### <a name="item-ledger-entry" />Lagerposten

|Laufnr.  |Artikelnr.  |Buch. Datum  |Postenart   | Belegnummer |Lagerortcode   |Menge  |Einstandsbetrag (tatsächl.)  |Fakturierte Menge  |Restmenge  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Verkauf       |102033     |  Blau       | -1    |    -11     |-1     |    0     |

Nachfolgend finden Sie die zugehörigen Werteinträge:

- **Eintrag Nr. 379** stellt die Sendung dar und trägt dasselbe Buchungsdatum wie der übergeordnete Lagerposten.  
- **Eintrag Nr. 381** steht für die Rechnung.  
- **Eintrag Nr. 391** ist eine Anpassung des Rechnungswerts (Eintrag Nr. 381 oben).  

|Laufnr.  |Artikelnr.  |Buch. Datum  |Lagerpostenart  |Postenart   |Belegnummer  |Lagerposten Laufnr.  |Lagerortcode   |Lagerpostenmenge  |Fakturierte Menge  |Einstandsbetrag (tatsächl.)  |Einstandsbetrag (erwartet)  |Ausgleich  |Ausgleich mit Laufnr.  |Buchungsspurcode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Verkauf     | EK-Preis   | 102033        |319     | Blau        | -1       |0         |  0       |     -10   |Nein   |0    |Verkauf          |
|381     |  A       |    2020-09-06     |    Verkauf     | EK-Preis   | 103022        |319     | Blau        |  0       |-1        |-10       |    10     | Nein  |0      |       Verkauf   |
|391     |  A       |    2020-09-10     |    Verkauf     | EK-Preis   | 103022        |319     | Blau        |  0       |0         |-1        |    0     |Ja   |    181   | LAGERREGUL   |

Um das Buchungsdatum für **Eintrag Nr. 391** zuzuweisen, wurden die folgenden Schritte durchgeführt:

1. Dem zu erstellenden **Anpassungswert-Eintrag** (**Eintrag Nr. 391**) wird dasselbe **Buchungsdatum** zugewiesen wie dem Eintrag, den er anpasst.

2. Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** bestimmt, ob das ursprüngliche Buchungsdatum des Ausgleichs-Wertpostens innerhalb des Bereichs des zugelassenen Buchungszeitraums ist, der auf Lagerbuchungsperioden und/oder Fibuposteneinrichtung basiert.  

Wir überprüfen den oben erwähnten Verkauf, indem wir die zugelassenen Buchungszeiträume hinzufügen.  
  
#### <a name="inventory-periods" />Lagerbuchungsperioden

|Enddatum  |Name  |Geschlossen  |
|---------|---------|---------|
|2020-01-31     |2020. Januar      |  Ja    |
|2020-02-28     |Februar 2020     |  Ja    |
|2020-03-31     |März 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Mai   2020        |  Ja    |
|2020-06-30     |Juni   2020       |  Ja    |
|2020-07-31     |Juli  2020        |  Ja    |
|2020-08-31     |August 2020     |  Ja    |
|2020-09-30     |September 2020  |         |
|2020-10-31     |Oktober 2020    |         |
|2020-11-30     |November 2020   |         |
|2020-12-31     |Dezember   2020   |         |

Das erste zugelassene Buchungsdatum ist der erste Tag der ersten offenen Periode, also der 1. September 2020.  

#### <a name="general-ledger-setup" />Finanzbuchhaltung Einrichtung

|Feld|Wert  |
|---------|---------|
|Buchungen zugel. ab:  |  2020-09-10      |
|Buchungen zugel. bis:    |  2020-09-30      |
|Protokollzeit:       |         |
|Lokales Adressformat:|   PLZ      |  

Das erste zulässige Buchungsdatum ist das in Feld **Buchungen zugel. ab** angegebene Datum: 10. September 2020. Wenn sowohl Lagerbuchungsperioden als auch erlaubte Buchungsdaten in **Fibuposten Einrichtung** definiert sind, definiert das spätere Datum von beiden den erlaubten Buchungsdatumsbereich.  

**Zuweisung eines erlaubten Buchungsdatums**  

Das zugewiesene Buchungsdatum war 6. September, wie in Schritt 1 veranschaulicht. Im zweiten Schritt stellt der Batchauftrag Lagerreg. fakt. Artikel-Einträge zugel. jedoch fest, dass das früheste zulässige Buchungsdatum der 10. September ist und ordnet somit den 10. September dem unten aufgeführten Eintrag für den Korrekturwert (**Eintrag Nr. 391**) zu.  


|Laufnr.  |Artikelnr.  |Buch. Datum  |Lagerpostenart  |Postenart   |Belegnummer  |Lagerposten Laufnr.  |Lagerortcode   |Lagerpostenmenge  |Fakturierte Menge  |Einstandsbetrag (tatsächl.)  |Einstandsbetrag (erwartet)  |Ausgleich  |Ausgleich mit Laufnr.  |Buchungsspurcode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Verkauf     | EK-Preis   | 102033        |319     | Blau        | -1       |0         |  0       |     -10   |Nein   |0    |Verkauf          |
|381     |  A       |    2020-09-06     |    Verkauf     | EK-Preis   | 103022        |319     | Blau        |  0       |-1        |-10       |    10     | Nein  |0      |       Verkauf   |
|391     |  A       |    **2020-09-10**     |    Verkauf     | EK-Preis   | 103022        |319     | Blau        |  0       |0         |-1        |    0     |Ja   |    181   | LAGERREGUL   |

## <a name="common-problems-with-the-adjust-cost---item-entries-batch-job" />Allgemeine Probleme mit dem „Lagerreg. fakt. Einst. Preise“-Batchauftrag

Es gibt zwei Szenarien, die dem Support-Team so häufig begegnen, dass sie einen eigenen Artikel zur Problemlösung rechtfertigen.

### <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates" />Fehlermeldung: „Das Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten...“

Wenn Sie auf diesen Fehler stossen, müssen Sie die Daten anpassen, für die der Benutzer Buchungen zulassen darf. Weitere Informationen finden Sie unter [Fehlermeldung „Das Buchungsdatum liegt nicht in Ihrem Bereich der zulässigen Buchungsdaten“](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md).

### <a name="posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge" />Buchungsdatum der Korrekturwerteingabe gegenüber dem Buchungsdatum der Buchung, die die Korrektur verursacht, wie z.B. Neubewertung oder Artikel Zu-/Abschlag

Weitere Informationen finden Sie unter [Buchungsdatum der Korrekturwerteingabe im Vergleich zur Quellbuchung](design-details-inventory-adjustment-value-entry-source-entry.md).

## <a name="see-also" />Weitere Informationen

[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)  
[Designdetails: Artikelausgleich](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
