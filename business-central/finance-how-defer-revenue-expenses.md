---
title: Einnahmen und Ausgaben abgrenzen
description: 'Um Umsätze und Aufwendungen in Perioden zu erfassen, in denen die Transaktion nicht gebucht wurde, können Sie diese automatisch über einen festgelegten Zeitplan abgrenzen oder verschieben.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: postpone
ms.search.form: '1700, 1701, 1702, 1703, 1704, 1705, 1706, 1707'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="defer-revenues-and-expenses" />Einnahmen und Ausgaben abgrenzen

Um Einnahmen und Ausgaben in einer anderen Periode als in jener, in der die Transaktion gebucht wurde, zu erkennen, können Sie die Funktionen verwenden, um Einnahmen und Ausgaben über einen bestimmten Zeitplan automatisch abzugrenzen.

Um Einnahmen oder Ausgaben in den betroffenen Buchhaltungsperioden einzubeziehen, können Sie eine Abgrenzungsvorlage für die Ressource, den Artikel oder ein Fibukonto anlegen, für das die Einnahmen oder Ausgaben gebucht werden. Wenn Sie den zugehörigen Kauf- oder Verkaufsbeleg buchen, werden die Einnahmen oder Ausgaben zu den entsprechenden Buchhaltungsperioden zurückgestellt, entsprechend einem Abgrenzungsplan, der durch Einstellungen in der Abgrenzungsvorlage und das Buchungsdatum bestimmt wird.

## <a name="to-set-up-a-gl-account-for-deferral" />So richten Sie ein Fibukonto für Abgrenzungen ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder wie notwendig aus, um ein Fibukonto für abgegrenzte Einnahmen zu erstellen. Weitere Informationen finden Sie unter [Die Finanzbuchhaltung und der Kontenplan](finance-general-ledger.md).
4. Wiederholen Sie die Schritte 2 und 3, um ein neues Fibukonto für abgegrenzte Ausgaben zu erstellen.

Für beide Arten Abgrenzung wählen Sie im Feld **Art** **Bilanz** aus und benennen Sie die Konten entsprechend, wie "Nicht verdiente Erträge" für zurückgestellte Einnahmen und "nicht bezahlte Ausgaben" für abgegrenzte Ausgaben.

## <a name="to-set-up-a-deferral-template" />So richten Sie eine Abgrenzungsvorlage ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Abgrenzungsvorlagen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie die Felder je nach Bedarf aus.
4. Geben Sie auf der Seite **Berechnungsmethode** an, wie das Feld **Betrag** für jede Periode auf der Seite **Abgrenzungsplan** berechnet wird. Sie haben die Wahl zwischen den folgenden Optionen:

   * **Linear**: Die regelmässigen Abgrenzungsbeträge werden entsprechend der Anzahl der Perioden berechnet, verteilt entsprechend der Periodenlänge.
   * **Gleich pro Periode**: Die regelmässigen Abgrenzungsbeträge werden entsprechend der Anzahl der Perioden berechnet, gleichmässig nach Perioden verteilt.
   * **Tage pro Periode**: Die regelmässigen Abgrenzungsbeträge werden entsprechend der Anzahl der Tage in der Periode berechnet.
   * **Benutzerdefiniert**: Die regelmässig Abgrenzungsbeträge werden nicht berechnet. Sie müssen das Feld **Betrag** für jede Periode auf der Abgrenzungsplanseite manuell ausfüllen. Weitere Informationen finden Sie im Abschnitt „So ändern Sie einen Aufschubzeitplan aus einer Verkaufsrechnung”.
5. In der **Periodenbeschr.** Feld geben Sie eine Beschreibung an, die bei Einträgen für die Abgrenzungsbuchung angezeigt wird. Sie können die folgenden Platzhaltercodes für typische Werte eingeben, die automatisch eingefügt werden, wenn die Periodenbeschreibung angezeigt wird.

   * %1 = Die Tagesnummer des Periodenbuchungsdatums
   * %2 = Die Wochennummer des Periodenbuchungsdatums
   * %3 = Die Monatsnummer des Periodenbuchungsdatums
   * %4 = Der Monatsname des Periodenbuchungsdatums
   * %5 = Der Buchhaltungsperiodenname des Periodenbuchungsdatums
   * %6 = Das Geschäftsjahr des Periodenbuchungsdatums

Beispiel: Das Buchungsdatum ist 02.06.2016. Wenn Sie „Abgrenzungsausgabe für %4 %6“ eingeben, ist die angezeigte Beschreibung „Abgrenzungsausgaben für Februar 2016“.

## <a name="to-assign-a-deferral-template-to-an-item" />So weisen Sie einem Artikel eine Abgrenzungsvorlage zu

> [!NOTE]  
> Die Schritte in diesem Verfahren sind die gleichen wie bei der Zuordnung einer Stundungsvorlage zu einem Fibukonto oder einer Ressource.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Element** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie die Karte für den Artikel, für den Ausgaben oder Einnahmen zu den Buchhaltungsperioden abgegrenzt werden müssen, wenn der Artikel gekauft oder verkauft wurde.
3. Im Feld **Standard-Abgrenzungsvorlage** wählen Sie die entsprechende Abgrenzungsvorlage aus.

## <a name="to-change-a-deferral-schedule-from-a-sales-invoice" />So ändern Sie einen Aufschubzeitplan von einer Verkaufsrechnung aus

> [!NOTE]  
> Die Schritte in diesem Ablauf sind identisch, wie wenn Sie einen Abgrenzungsplan für Ausgaben aus einer Kaufrechnung ändern.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.
2. Erstellen Sie eine Verkaufsrechnung für einen Artikel, der einer Abgrenzungsvorlage zugewiesen ist. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).

    Beachten Sie Folgendes: Sobald Sie den Artikel (oder Ressource oder Sachkonto) in der Rechnungszeile eingeben, wird das Feld **Abgrenzungscode** mit dem Code der zugewiesenen Abgrenzungsvorlage ausgefüllt.
3. Wählen Sie die Aktion **Abgrenzungsplan** aus.
4. Ändern Sie auf der Seite **Abgrenzungsplan** die Einstellungen im Kopf oder die Werte in den Zeilen, zum Beispiel, um den Betrag bis zu einer zusätzlichen Buchhaltungsperiode zurückzustellen.
5. Wählen Sie die Aktion **Berechnungsplan** aus.
6. Wählen Sie die Schaltfläche **OK** aus. Der Aufschubzeitplan wird für die Verkaufsrechnung aktualisiert. Die zugehörige Aufschubvorlage ist unverändert.

## <a name="to-preview-how-deferred-revenues-or-expenses-will-be-posted-to-the-general-ledger" />Um anzuzeigen, wie die Abgrenzungsausgaben oder -einnahmen im Fibuposten gebucht werden

> [!NOTE]  
> Die Schritte in diesem Ablauf sind die selben, wie Sie in der Vorschau sehen, wie Abgrenzungsausgaben gebucht werden.

1. Auf der Seite **Gebuchte Verkaufsrechnung** wählen Sie die Aktion **Buchung ansehen** aus.
2. Wählen Sie auf der Seite **Buchungsvorschau** die Option **Fibukonteneintrag** aus und wählen Sie dann **Zugehörige Einträge anzeigen** aus.

Fibukonteneinträge, die im entsprechenden Abgrenzungskonto gebucht werden müssen, wie beispielsweise "Nicht verdiente Erträge" werden durch die Beschreibung bezeichnet, die Sie unter **Perioden Beschr.** eingegeben haben. Feld in der Abgrenzungsvorlage beispielsweise "Ausgaben abgegrenzt für Februar 2016".

## <a name="to-review-posted-deferrals-in-the-sales-deferral-summary-report" />So überprüfen Sie gebuchte Aufschübe im Bericht „Verkaufsaufschubzusammenfassung” .

> [!NOTE]  
> Die Schritte in diesem Ablauf sind die selben, wie Sie sie sehen, wenn Sie die Zusammenfassung des Einkaufsabgrenzungsberichts ansehen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Verkaufsverzögerung – Zusammenfassung** ein und wählen Sie dann den zugehörigen Link.
2. Geben Sie auf der Seite **Verkaufsabgrenzungszusammenfassung** im Feld **Saldo ab** das Datum ein, bis zu welchem Sie abgegrenzte Einnahmen anzeigen möchten.
3. Klicken Sie auf die Schaltfläche **Vorschau**.

## <a name="to-specify-a-period-in-which-to-allow-deferral-posting" />So legen Sie einen Zeitraum fest, in dem die Abgrenzungsbuchung zugelassen werden soll

Sie können einen Zeitraum festlegen, in dem Transaktionen gebucht werden können, indem Sie in den Feldern **Buchung zulassen von** und **Buchung zulassen bis** wie folgt Daten eingeben:

* Für alle Benutzer, auf der Seite **Fibuposten Einrichtung**
* Für bestimmte Benutzer, auf der Seite **Benutzereinrichtung**

Wenn Sie das getan haben, müssen Sie eine Ausnahme für Abgrenzungen machen, damit diese auch ausserhalb des Zeitraums gebucht werden dürfen. Um den Zeitraum zu definieren, gehen Sie folgendermassen vor.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol, geben Sie **Fibuposten Einrichtung** oder **Benutzereinrichtung** ein, und wählen Sie dann den entsprechenden Link.
2. Geben Sie in die Felder **Abgrenzungsbuchung zulassen von** und **Abgrenzungsbuchung zulassen bis** ein Anfangs- und Enddatum für den Zeitraum ein.

## <a name="see-related-microsoft-trainingtrainingmodulesprocessing-invoices-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/processing-invoices-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Erfassungsjournalen](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
