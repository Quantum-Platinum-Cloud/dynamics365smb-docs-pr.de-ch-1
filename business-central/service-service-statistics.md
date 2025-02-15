---
title: Service-Statistik
description: 'Verschaffen Sie sich einen schnellen Überblick über die Inhalte und Statistiken von Service-Belegen wie Bestellungen, Offerten, Rechnungen, Gutschriften, Service-Zeilen und mehr.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---

# <a name="viewing-service-statistics" />So zeigen Sie die Servicestatistik an
Sie können Statistiken nutzen, um Belege zu analysieren und zu bestimmen, wie Sie Ihre Dienstvorgänge verwalten sollen. Sie können Serviceverträge, Artikel, Offerten, Bestellungen, Rechnungen und Gutschriften analysieren, indem Sie die **Statistik** Aktion auswählen. Für Serviceartikel und Verträge können Sie **Serviceartikel-Trendscape** oder **Servicevertrag-Trendscape** verwenden, um eine Zusammenfassung der Serviceposten für einen bestimmten Serviceartikel angezeigt.   

## <a name="viewing-statistics-for-service-orders" />So zeigen Sie die Serviceauftragsstatistik an
Die Funktion "Serviceauftragsstatistik" bietet Ihnen einen schnellen Überblick über den Inhalt des gesamten Serviceauftrags, über die Details zu bestimmten Servicezeilen und über Informationen zur Fakturierung, Lieferung und dem Verbrauch sowie über den Saldo des Debitors.  

Die statistischen Daten eines Serviceauftrags werden auf der Seite **Serviceauftragsstatistik** des jeweiligen Auftrags angezeigt. Sie können die entsprechende Statistikseite aus einem Serviceauftrag öffnen. Die Seite **Serviceauftrag** wählen Sie **Statisitk**. Auf den Inforegistern auf dieser Seite werden u. a. die Menge, der Betrag, der MWST-Betrag, der Einstandspreis, der Deckungsbeitrag und das Kreditlimit des Debitors angezeigt. Die Beträge auf der Seite werden – sofern nichts anderes angegeben wird – in der Währung des Serviceauftrags angezeigt.  

### <a name="view-totals-for-a-service-order" />Anzeigen von Summen für einen Auftrag
Die Daten umfassen den Gesamtbetrag der Servicezeilen (mit und ohne MWST), MWST-Anteil, Einstandspreis sowie DB der Servicezeilen. Die Seite zeigt auch die artikelspezifischen Informationen, wie Gewicht, Volumen und Menge an Paketen.  

### <a name="view-shipping-information" />Ansichtsversandinformationen
Auf diesem Inforegister werden die Informationen über die zu liefernden Artikel, Ressourcen und/oder Kosten angezeigt. Die Anwendung verwendet die im Feld **Zu liefernde Menge** für die einzelnen Servicezeilen angegebenen Werte, um die Informationen bereitzustellen.  

### <a name="view-order-details" />Auftragsdetails anzeigen
Auf diesem Inforegister werden Informationen zu den Artikeln, Ressourcenstunden und Kosten angezeigt, die fakturiert und verbraucht werden sollen. Die Berechnungen sind in der folgenden Tabelle beschrieben.  

|Spalte | Beschreibung|  
|------------|---------------------------------------|  
|**Fakturierung**|Enthält Beträge, die vom Serviceauftrag aus als fakturiert gebucht werden müssen.|  
|**Verbrauch**|Zeigt die Menge und die Kosten von Artikeln oder Ressourcen an, die als verbraucht gebucht wurden.|  
|**Summe**|Zeigt die Gesamtbeträge des Serviceauftrags an, die sich durch Addieren der Beträge für die Fakturierung mit den Beträgen für den Verbrauch ergeben.|  

### <a name="analyze-service-order-lines" />Serviceauftragspositionen analysieren
Sie können die Informationen nach den Arten von Servicezeilen analysieren, die sich im Serviceauftrag befinden. Die Beträge werden einzeln für Folgendes angezeigt:  

* Arti&amp;kel  
* Ressourcen  
* Kosten und Fibukonten  

### <a name="view-customer-information" />So zeigen Sie Debitoreninformationen an
Dieses Inforegister enthält den Saldo des Debitorenkontos sowie das maximale Kreditlimit, das dem Debitor gewährt werden kann, für den Sie den Servicebeleg erstellt haben.

## <a name="viewing-service-item-statistics" />So zeigen Sie die Servicestatistik an
Auf dieser Seite **Serviceartikelstatistik** sind aktuelle Informationen über den Verbrauch, fakturierte Beträge und Deckungsbetrag eines bestimmten Artikels ersichtlich.  

* Ressourcen  
* Arti&amp;kel  
* Servicekosten  
* Serviceverträge  
* Total  

Für jede Postenart sind der fakturierte Betrag, der Verbrauchsbetrag, der Einstandsbetrag, die Menge, die fakturierte und die verbrauchte Menge, der Deckungsbeitrag und der Deckungsbeitrag in Prozent angegeben. Der Deckungsbeitrag in Prozent wird gemäss der folgenden Formel berechnet:  

* (Fakturierter Betrag - Verbrauch (Kosten)) x 100 / Fakturierter Betrag  

## <a name="use-trendscapes" />Trendscapes nutzen
Um Serviceartikel und Serviceverträgen stellen die Seiten **Serviceartikel-Trendscape** oder **Servicevertrags-Trendscape** eine Zusammenfassung der Serviceposten in einem Zeitraum für einen bestimmten Serviceartikel oder einen Vertrag. Um das Trendscape anzuzeigen, öffnen Sie den Serviceartikel oder den Servicevertrag, wählen Sie die **Statistik** Aktion aus, und wählen Sie dann **Trendscape** aus.

Wenn Sie mit den Bildlaufleisten den sichtbaren Fensterausschnitt verschieben, werden automatisch die Beträge für das gewählte Intervall berechnet. Alle Beträge aus den Serviceposten werden berechnet. Dabei handelt es sich um Posten, die beim Buchen von Serviceaufträgen oder Servicerechnungen erzeugt wurden.

Sie können die Liste filtern, indem Sie die Serviceartikel festlegen, die berücksichtigt werden sollen.  

> [!Tip]  
>  Wenn Sie die Periodenlänge auf **Tag** gesetzt haben und die Suche mit den Bildlaufleisten sehr lange dauert, können Sie auch ein grösseres Intervall (z. B. **Quartal**) verwenden. Wenn Sie die gewünschte Periode gefunden haben, können Sie wieder auf das ursprüngliche Intervall umschalten, so dass detailliertere Daten angezeigt werden.   

## <a name="viewing-gains-and-losses-on-contracts" />Gewinne und Verluste auf Verträgen anzeigen
Die Anwendung erstellt automatisch einen Gewinn- oder Verlustposten, wenn Vertragsofferten in Serviceverträge umgewandelt werden, wenn Vertragszeilen zum Servicevertrag hinzugefügt oder aus ihm entfernt werden und wenn Verträge gekündigt werden. Sie können Vertragsgewinne oder -verluste auf den folgenden Seiten anzeigen.  

|Seite | Beschreibung|  
|----------------|---------------------------------------|  
|**Vertrag Gew./Verl. (Verträge)**|Um den Vertragsgewinn/-verlust nach Servicevertrag anzuzeigen.|  
|**Vertrag Gew./Verl. (Gruppen)**|Um den Vertragsgewinn/-verlust nach Servicevertragsgruppe anzuzeigen.|  
|**Vertrag Gew./Verl. (Debitoren)**|Um den Vertragsgewinn/-verlust nach Debitor anzuzeigen.|  
|**Vertrag Gew./Verl. (Ursachen)**|Um den Vertragsgewinn/-verlust nach Ursachencode anzuzeigen.|  
|**Vertrag Gew./Verl. (Zust.Ein.)**|Um den Vertragsgewinn/-verlust nach Zuständigkeitseinheit anzuzeigen.|  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie den Namen der Seite ein, die angezeigt werden soll, und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie die Filterkriterien aus, die Sie anwenden möchten. Wählen Sie beispielsweise auf der Seite **Vertrag Gew./Verl. (Ursachen)** einen Wert für **Ursachencodefilter** aus.  
3. Wählen Sie die Aktion **Matrix anzeigen** aus.

## <a name="viewing-statistics-for-posted-service-documents" />Servicestatistik für gebuchte Service-Belege anzeigen
Mit der Funktion "Servicestatistik" erhalten Sie eine statistische Übersicht über den Inhalt von gebuchten Servicebelegen, wie gebuchte Lieferungen, Rechnungen und Gutschriften.  

Die statistischen Daten werden auf der Seite "Servicestatistik" für den gebuchten Service angezeigt. Sie können die entsprechende Statistikseite aus der gebuchten Servicelieferung, aus der gebuchten Servicerechnung oder den gebuchten Servicegutschriftbelegen öffnen. Wählen Sie für jede dieser Dokumentarten die Aktion **Statistik**. Wählen Sie beispielsweise auf der Seite **Gebuchte Dienstleistungsrechnungen** die Aktion **Statistik**.  

### <a name="posted-service-shipment-statistics" />Geb. Servicelieferungsstatistik
Die Seite **Servicelieferungsstatistik** bietet Ihnen eine Übersicht über die gebuchte Servicelieferung. Das Fenster umfasst das Inforegister "Allgemein", auf dem Informationen zum physischen Inhalt der Lieferung angezeigt werden, z. B. die Menge der gelieferten Artikel, die Ressourcenstunden oder die Einstandspreise und das Gewicht sowie das Volumen der gelieferten Artikel.  

### <a name="posted-service-invoice-statistics" />Geb. Servicerechnungsstatistik
Auf der Seite **Servicerechnungsstatistik** wird eine statistische Zusammenfassung der gebuchten Servicerechnung angezeigt. Sie können die Summen der gebuchten Servicerechnung angezeigt. Die Daten umfassen den Gesamtbetrag der Servicezeilen (mit und ohne MWST), die als fakturiert gebucht wurden, MWST-Anteil, Einstandspreis sowie DB der gebuchten Rechnung. Die Spalten auf der Seite zeigen darüber hinaus die folgenden Informationen an:  

* Die Artikel in den Servicerechnungszeilen, wie Gewicht, Volumen und Menge an Paketen.  
* Der Saldo des Debitorenkontos und der maximale Kredit, den Sie für den Debitor erweitern können.  

### <a name="posted-service-credit-memo-statistics" />Statistik zu gebuchten Servicegutschriften
Auf der Seite **Servicegutschriftstatistik** erhalten Sie eine Übersicht über die Zeilen in einer gebuchten Servicegutschrift. Die Übersicht kann gehören:

* Auf dem Inforegister "Allgemein" werden die Gesamtbeträge der gebuchten Gutschrift sowie Informationen wie Menge, Betrag, MWST, Einstandspreis und DB angezeigt. Das Inforegister enthält zudem spezifische Informationen über die Artikel in den Servicezeilen der gebuchten Gutschrift wie Menge, Gewicht und Volumen.  
* Das Inforegister "Debitor" enthält allgemeine Informationen zum Debitor, z. B. Kreditlimit und Kontosaldo.  

## <a name="see-also" />Siehe auch
[Erstellen von Serviceaufträgen](service-how-to-create-service-orders.md)   
[Serviceartikel erstellen](service-how-to-create-service-items.md)   
[Planungsservice](service-plan-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
