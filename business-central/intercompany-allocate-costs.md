---
title: Kosten den Intercompanypartnern zuordnen | Microsoft Docs
description: 'Erfahren Sie, wie die Mehrwertsteuereinstellungen für Kunden und Lieferanten steuern, ob und wie die Mehrwertsteuer berechnet wird.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocate-costs-to-intercompany-partners" />Kosten den Intercompanypartnern zuordnen
Wenn Sie konzerninterne Buchungen verwenden, um Belege zwischen Partnerunternehmen zu übertragen, steuern die den Kunden- oder Lieferantenkonten (dem konzerninternen Partner zugeordneten) zugewiesenen umsatzsteuerlichen Einstellungen (hauptsächlich die Umsatzsteuer-Geschäftsbuchungsgruppe), ob und wie die Mehrwertsteuer berechnet und registriert wird. Sie können Kostenverteilungen auch direkt von einer Bestellung an Partnerunternehmen durchführen. Wenn Sie beispielsweise eine Kaufrechnung von einem externen Anbieter registrieren und einen Teil oder die gesamten Kosten an einen oder mehrere konzerninterne Partner verteilen möchten.

Sie können Kosten einem oder mehreren konzerninternen Partnern wie folgt zuordnen:

* **Intercompany Fibu Erf.-Journalzeile** – Diese Fibu Erfassungsjournale sind nützlich, wenn ein Dienst gekauft wird. Zum Beispiel, wenn eine Muttergesellschaft einen Dienst kauft, um Computersysteme in zwei Tochtergesellschaften einzurichten. Die Rechnung wird an die Muttergesellschaft gesendet, die Kosten werden jedoch den Intercompanypartnern zugewiesen. Weitere Informationen finden Sie unter [Arbeiten mit Intercompanybelegen und Fibu Erfassungsjournalen](intercompany-how-work-documents-journals.md).
* Bestellungen und Rechnungen – Die Verwendung von Einkaufsbelegen ist nützlich, wenn die Einkaufsfunktionen von beispielsweise Betriebskosten in einem Unternehmen zentralisiert und dann den konzerninternen Partnern zugeordnet werden.

## <a name="to-allocate-costs-using-an-intercompany-general-journal" />Zuordnung der Kosten mithilfe eines Intercompany Fibu Erf.-Journals
Führen Sie die folgenden Schritte aus, um eine Zeile in ein Intercompany Fibu Erf.-Journal einzugeben. 

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Intercompany-Fibu Erf.-Journal** ein, und wählen Sie dann den entsprechenden Link.
2. Bei Bedarf im Feld **Externes Dokument Nr.** die Belegnummer des Lieferanten auf der Rechnung eingeben.
3. Wählen Sie in dem Feld **Belegart** **Rechnung** ein.
4. Wählen Sie im Feld **Kontoart** die Option **Kreditor** aus.
5. Wählen Sie im Feld **Kontonummer** die Option Kreditor aus.
6. In dem Feld **Betrag** geben Sie einen negativen Betrag ein, der dem Betrag auf der Rechnung entspricht.
7. Geben Sie im Feld **Gegenkonto** **Fibukonto** ein.
8. Wählen Sie im Feld **Gegenkontonr.** die Nummer des Gegenkontos aus.
9. Gehen Sie folgendermassen vor, um die Kosten der Intercompanypartern ein:
   1. Erstellen Sie eine neue Zeile.
   2. Lassen Sie die **Art des Dokuments**, wählen Sie im Feld die Option aus, bei der das Feld leer bleibt.
   3. In dem Feld **Dokument Nr.** geben Sie eine andere Nummer als die im Feld **Externe Dokument Nr.** angegebene Nummer ein. Die Kostenverteilung wird als eine andere Transaktion betrachtet.
   4. Wählen Sie im Feld **Kontoart** die Option **IC Partner** aus.
   5. In dem Feld **Konto Nr.** wählen Sie den Intercompany-Partner aus, dem die Kosten zugeordnet werden sollen.
   6. Geben Sie im Feld **Gegenkontoart** **Fibukonto** ein.
   7. In dem Feld **Gegenkontonummer** wählen Sie das Fibukonto aus, auf das der vom Intercompany-Partner erhaltene Betrag gebucht werden soll.
   1. In dem Feld **Menge** geben Sie den Rechnungsbetrag ein, der dem Intercompany-Partner zugeordnet werden soll.
   1. In dem Feld **Fibukonto IC Partner** wählen Sie das Fibukonto aus, auf das der vom Intercompany-Partner erhaltene Betrag gebucht werden soll. 
   1. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Wiederholen Sie diese Schritte für jeden Intercompany-Partner, der sich an den Kosten beteiligen soll.
1. Wählen Sie **buchen**, um das Dokument zu buchen und die Kosten zuzuordnen.  

## <a name="to-allocate-costs-using-a-purchase-document" />Kosten anhand eines Kaufbelegs zuordnen
Das folgende Verfahren beschreibt die Zuordnung von Kosten mithilfe einer Einkaufsrechnung. Die Schritte sind für eine Einkaufsbestellung gleich.

> [!NOTE]
> Um diese Schritte auszuführen, müssen Sie die Seite **Einkaufsrechnung** durch Hinzufügen der **IC-Partnercode**, **IC Partner Ref. Art**, und **IC-Partner** Felder personalisieren. Weitere Informationen finden Sie unter [So starten Sie die Personalisierung einer Seite über das Banner Personalisierung](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Einkaufsrechnungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie im Feld **Art** die Option **Fibukonto** aus.
   
   Das Fibukonto ist die einzige Option, mit der Sie Kosten zuordnen können.  
1. Geben Sie im Feld **Nr.** Wählen Sie im Feld das Fibukonto zum Buchen aus.
1. In dem Feld **IC Partnercode** wählen Sie den Intercompany-Partner aus, dem die Kosten zugeordnet werden sollen.
1. Unter **IC Partner Ref. Art** wählen Sie das Fibukonto aus, das für die Zuordnung verwendet werden soll. Dieses Konto ordnet die Ausgaben einem Konto im Kontenplan des Intercomany-Partners zu.
1. In dem Feld **Menge** geben die Anzahl der Einheiten an, die dem Intercompany-Partner in Rechnung gestellt werden sollen.
1. In dem Feld **Direkte Stückkosten exkl. Mehrwertsteuer (oder inkl. Mehrwertsteuer)** geben Sie die Kosten pro Artikel ein, die dem Intercompany-Partner in Rechnung gestellt werden sollen.
1. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
1. Um die Bestellung zu buchen, wählen Sie **Buchen**.

## <a name="to-send-the-allocated-costs-to-intercompany-partners" />Um die zugeordneten Kosten an die Intercompanypartner zu senden
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **IC-Ausgangstransaktionen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die zu sendenden Zeilen aus und wählen Sie dann die **An IC-Partner senden** Aktion aus. 
3. Um die Kosten zuzuordnen, wählen Sie die Aktion **Komplette Linienaktionen** aus.

## <a name="calculating-vat-for-cost-distributions" />Berechnung der Mehrwertsteuer für Kostenverteilungen
Wenn Sie einen Beleg verwenden, um die Kosten an konzerninterne Partner zu verteilen, müssen Sie zwei Mehrwertsteuereinstellungen beachten: 
* Die Einstellungen im Fibukonto für Ausgaben:
   * Wenn die allgemeinen Geschäfts- oder Umsatzsteuerbuchungsgruppen auf dem Fibukonto eingerichtet sind, hängt die Berechnung von den Gruppen und Produktgruppen aus der Belegzeile ab.
   * Wenn auf dem Fibukonto keine allgemeinen Geschäfts- oder Mehrwertsteuer-Buchungsgruppen angegeben sind, hängt die Berechnung von folgenden Faktoren ab:
* Die Buchungsgruppeneinstellungen auf dem Intercompany-Partner
   * Gibt an, ob der Intercompanypartner einer Kundennummer zugeordnet ist, für die keine allgemeinen Geschäfts- oder Mehrwertsteuer-Buchungsgruppen angegeben sind.
   * Dem Intercompanypartner ist keine Kundennummer zugeordnet. Dann sind die allgemeinen Geschäfts- oder Mehrwertsteuergeschäftsbuchungsgruppen leer, und die Zeile in der Mehrwertsteuerbuchungskonfiguration wird verwendet. Dies ist normalerweise eine Gruppe, in der 0% Mehrwertsteuer angegeben ist.

> [!NOTE]
> Es ist wichtig, sowohl die Einrichtung des Intercompanypartners als auch die Einrichtung des Fibukontos (für das für die Kostenverteilung verwendete Kostenkonto) zu überprüfen, bevor Sie den Intercompanypartnern Kosten zuweisen.

## <a name="see-also" />Siehe auch
[Intercompany einrichten](intercompany-how-setup.md)  
[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finanzen einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Erfassungsjournalen](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
