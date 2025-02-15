---
title: Verkaufsrechnungen einrichten und fakturieren Vorauszahlungen
description: 'Vorauszahlungen sind Zahlungen, die vor der finalen Fakturierung fakturiert und auf einen Vorauszahlungsauftrag (Einkauf oder Verkauf) gebucht werden.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/03/2021
ms.author: edupont
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments" />Exemplarische Vorgehensweise: Einrichten und Fakturieren von Verkaufsvorauszahlungen

Diese exemplarische Vorgehensweise führt Sie durch den Prozess der Einrichtung und die Verwendung von Vorauszahlungen in [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

Sie haben zum Beispiel auch die Möglichkeit zum Senden mehrerer Vorauszahlungsrechnungen, für den Fall, dass dem Auftrag weitere Artikel hinzugefügt wurden.  

## <a name="about-this-walkthrough" />Informationen zu dieser exemplarischen Vorgehensweise

In dieser exemplarischen Vorgehensweise werden folgende Szenarios behandelt:  

- Einrichten von Vorauszahlungen  
- Erstellen eines Auftrags, der eine Vorauszahlung erfordert  
- Erstellen einer Vorauszahlungsrechnung  
- Korrigieren der Vorauszahlungsanforderungen für einen Auftrag  
- Ausgleichen von Vorauszahlungen für einen Auftrag  
- Fakturieren des Endbetrags für einen Auftrag mit Vorauszahlung  

### <a name="roles" />Rollen

Diese exemplarische Vorgehensweise umfasst Aufgaben für folgende Rollen:  

- Kundenbetreuerin (Heike)  
- Auftragsbearbeiterin (Martha)  
- Debitorenadministrator (Peter)  

## <a name="story" />Hintergrund

 Phyllis ist ein Buchhaltungsmanager und entschweidet, welche Debitoren eine Anzahlung leisten müssen, bevor Artikel hergestellt oder geliefert werden. Heike hat [!INCLUDE[prod_short](includes/prod_short.md)] eingerichtet, um Vorauszahlungen automatisch zu berechnen.  

 Marta ist eine Verkaufsauftragsbearbeiterin. Wenn ein Debitor eine telefonische Bestellung tätigt, gibt Susan die Auftragsdaten in das System ein, während sie mit dem Debitoren telefoniert. Auf diese Weise kann Susan Preise und Zahlungsbedingungen sofort absprechen, und sie hat die Möglichkeit, den Auftrag noch während des Gesprächs mit dem Debitoren anzupassen.  

 Arnie arbeitet in der Debitorenabteilung, wo er Rechnungen und Zahlungen bucht.  

 In diesem Szenario richtet Heike basierend auf der Kreditgeschichte Vorauszahlungsanforderungen für den Debitoren Blütenhaus GmbH ein. Sie informiert Martha, wie Aufträge dieses Debitoren gehandhabt werden sollen.  

 Wenn der Kunde anruft, verhandelt Susan mit ihm, bis sie zu einer Einigung kommen. Im System stehen ihr unterschiedliche Methoden zur Verfügung, um die Vorauszahlung zu berechnen.  

 Nachdem Martha die Vorauszahlungsrechnung gesendet hat, bestellt der Kunde einen weiteren Artikel. Martha aktualisiert den Auftrag und erstellt eine zweite Vorauszahlungsrechnung.  

 Peter erfasst die Zahlung des Kunden und gleicht sie mit den Rechnungen aus. Anschliessend sendet er die endgültige Rechnung.  

## <a name="set-up-prepayments" />Vorauszahlungen einrichten

Die Kundenbetreuerin Heike richtet das System zur Verarbeitung von Vorauszahlungen für Kunden ein.  

- Heike entscheidet sich, für Vorauszahlungen die gleichen Nummernserien zu verwenden wie für die Fakturierung von Verkaufsaufträgen.  
- Heike richtet die Anwendung so ein, dass die Notwendigkeit von Vorauszahlungen vor der endgültigen Fakturierung eines Auftrags überprüft wird.  
- Heike legt Standardwerte für den erforderlichen Vorauszahlungsprozentsatz für bestimmte Artikel und Kunden fest.  

In den folgenden Verfahren wird beschrieben, wie Sie Heikes Aufgaben ausführen:  

### <a name="to-set-up-number-series-for-prepayments" />So richten Sie Nummernserien für Vorauszahlungen ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Einrichtung Debitoren & Verkauf** ein und wählen Sie dann den entsprechenden Link.  
2. Erweitern Sie auf der Seite **Debitoren Verkauf Einr.** das Inforegister **Nummernserie**.  
3. Vergewissern Sie sich, dass die Nummernserien für gebuchte Vorauszahlungsrechnungen im Feld **Geb. Vorauszahlungs-Rechnungsnr.** und gebuchte Verkaufsrechnungen (**Gebuchte Rechnungsnummern**) sowie die Nummernserien für gebuchte Vorauszahlungsgutschriften (**Geb. Vorauszahlungs-Gutschriftennr.**) und gebuchte Gutschriften (**Gebuchte Gutschriftennr.**) übereinstimmen.  

### <a name="to-block-shipments-for-unpaid-prepayment" />Lieferungen für nicht geleistete Vorauszahlung sperren

1. Aktivieren Sie auf der Seite **Debitoren & Verkauf Einr.** auf dem Inforegister **Allgemein** die Option **Vorauszahlung beim Buchen prüfen**.

Jetzt können Sie einen Auftrag mit nicht bezahltem Vorauszahlungsbetrag nicht liefern oder in Rechnung stellen.  

Heike legt standardmässig fest, dass für den Kunden 20000 eine Anzahlung in Höhe von 30 % für alle Aufträge fakturiert werden muss. Daher gibt Phyllis einen Standardvorauszahlungsprozentsatz in der Debitorenkarte ein.  

Heike legt fest, dass für alle Debitoren eine Anzahlung in Höhe von 20 % für den Artikel 1896-S fakturiert werden muss. Aufgrund der schlechten Zahlungshistorie des Kunden 20000 verlangt Phyllis vom Kunden 20000 eine Vorauszahlung in Höhe von 40 % für Artikel 1896-S. Im folgenden Beispiel wird gezeigt, wie Sie standardmässige Vorauszahlungsprozentsätze einrichten.  

### <a name="to-assign-default-prepayment-percentages-to-customers-and-items" />So weisen Sie Debitoren und Artikeln Standardvorauszahlungsprozentsätze zu

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Geben Sie **Debitoren** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Öffnen Sie das Kartenfenster für Debitor 20000 (Trey Research).
3. Geben Sie im Inforegister **Zahlungen** im Feld **Vorauszahlung %** **30** ein.  
4. Wählen Sie die Aktion **Zugehörig** den Menüpunkt **Verkauf** und dann den Menüpunkt **Vorauszahlungsprozentsätze** aus.  
5. Füllen Sie auf der Seite **Verkaufsvorauszahlungs-Prozentsätze** zwei Zeilen wie folgt aus:  

    |**Verkaufsart**|**Verkaufscode**|**Artikelnr.**|**Vorauszahlung %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Debitor**|**20000**|**1896-S**|**40**|
    |**Debitor**|**20000**|**1900-S**|**30**|  
    
    > [!TIP]
    > Je nach Land/Region müssen Sie im Inforegister **Einstandspreise und Buchung** für den Artikel 1896-S auch einen Salestax Gruppencode angeben. Wenn Sie das Demounternehmen verwenden, ist dieses Feld bereits festgelegt.

6. Schliessen Sie alle Seiten.  

### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup" />Ein Konto für Verkaufsvorauszahlung in der allgemeinen Buchungsmatrix angeben

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Allgemeine Buchungsmatrixeinrichtung** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Zeile aus, in der das Feld **Geschäftsbuchungsgruppe** auf **INLAND** und das Feld **Produktbuchungsgruppe** auf **EINZELHANDEL** festgelegt wurde.  
3. Geben Sie das entsprechende Konto im Feld **Verkaufsvorauszahlungs-Konto** an. Ihre Auswahl wird automatisch gespeichert.  

> [!TIP]
> Wenn das Feld auf der Seite **Buchungsmatrix einrichten** nicht angezeigt wird, verwenden Sie die horizontale Bildlaufleiste am unteren Rand der Seite, um nach rechts zu scrollen.  

## <a name="create-an-order-that-requires-a-prepayment" />Erstellen eines Auftrags, der eine Vorauszahlung erfordert

 Im folgenden Szenario erstellt Susan aus der Auftragsabwicklung einen Auftrag, während sie mit einem Kunden spricht. Die Artikel, die der Debitor bestellt, erfordern eine Vorauszahlung. Ausserdem hat der Debitor in der Vergangenheit einige verspätete Zahlungen geleistet. Daher wurde Martha angewiesen, einen festen Betrag von **800** als Vorauszahlung auf dem Auftrag zu benötigen.  

Der Debitor bittet, nur 35 % anzahlen zu müssen. Da Susan dem zustimmen kann, ändert sie den Auftrag entsprechend.  

Martha erstellt die Vorauszahlungsrechnung und sendet sie an den Kunden.  

### <a name="to-create-a-sales-order-with-a-prepayment" />So erstellen Sie einen Verkaufsauftrag mit einer Vorauszahlung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie im Feld **Debitorenname** **Trey Research** aus.  
4. Schliessen Sie die angezeigte Warnung zum fälligen Saldo.  
5. Füllen Sie zwei Verkaufszeilen mit den folgenden Informationen aus.  

    |**Typ**|**Nr.**|**Menge**|  
    |--------------|-------------|------------------|  
    |**Artikel**|**1896-S**|**1**|  
    |**Artikel**|**1900-S**|**1**|

    Die Vorauszahlungsfelder in der Verkaufszeile sind standardmässig ausgeblendet. Um die Felder anzuzeigen, müssen Sie die Seite personalisieren. Weitere Informationen finden Sie unter [So starten Sie die Personalisierung einer Seite über das Banner Personalisierung](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6. Vergewissern Sie sich, dass das Feld **Vorauszahlung %** in der Zeile mit dem Artikel **1900-S** den Wert **30** enthält. Der Standardwert wurde aus dem Verkaufskopf von der Kundenkarte übernommen.  

    Das Feld **Vorauszahlung %** in der Zeile mit dem Artikel **1896-S** enthält **40**. 40 ist der Prozentsatz, den Sie auf der Seite **Verkaufsvorauszahlungs-Prozentsätze** für den Artikel **1896-S** und den Kunden **20000** eingegeben haben.  

    Weitere Informationen finden Sie unter [Einrichten von Vorauszahlungen](finance-set-up-prepayments.md).  
7. Wählen Sie in der Aktion **Bestellung** die Option **Statistik** aus.  
8. Im Inforegister **Vorauszahlung** enthält das Feld **Vorauszahlungszeilenbetrag ohne MWST** den Wert **458,16**. Wenn Sie jetzt eine Vorauszahlungsrechnung für den Auftrag erstellen, wird 458,16 in der Rechnung angezeigt.  

    In diesem Szenario wurde Martha angewiesen, eine Gesamtvorauszahlung in Höhe von **800** für den Auftrag vorzuschlagen.  

    > [!IMPORTANT]  
    >  Abhängig von Ihrem Land/Ihrer Region trifft der nächste Schritt möglicherweise nicht zu.  
9. Ändern Sie den Betrag im Feld **Vorauszahlungsbetrag ohne Salestax** in **800**, und schliessen Sie dann die Seite.  
10. Überprüfen Sie das Feld **Vorauszahlung %** in den Verkaufszeilen. Der Wert wurde neu berechnet und lautet nun **67.02438** und **67.02282**.  

     Die erneute Berechnung beinhaltet alle Zeilen mit einem Vorauszahlungsprozentsatz grösser 0.  

     Jetzt fragt der Kunde, ob der Vorauszahlungsprozentsatz auf 35 % festgelegt werden kann. Da Marthas Vorgesetzter genehmigt die Änderung.
11. Erweitern Sie auf der Seite **Verkaufsauftrag** im Inforegister **Vorauszahlung** das Feld **Vorauszahlung %**, und geben Sie **35** ein.  
12. In der Warnung, die erscheint, wählen Sie die Schaltfläche **Ja**. Eine Rate von 35 % wird als Vorauszahlungsprozentsatz für den gesamten Auftrag angewendet.  
13. Überprüfen Sie dann, ob die Zeilen korrekt aktualisiert wurden.  

## <a name="create-a-prepayment-invoice" />Erstellen einer Vorauszahlungsrechnung

Nachdem sie die korrekten Vorauszahlungswerte im Auftrag eingegeben hat, erstellt Martha die Vorauszahlungsrechnung und sendet sie an den Kunden.  

### <a name="to-create-a-prepayment-invoice" />So erstellen Sie eine Vorauszahlungsrechnung

1. Wählen Sie auf der Seite **Verkaufsauftrag** nacheinander die Optionen **Aktionen**, **Buchung**, **Vorauszahlung** und dann **Vorauszahlungsrechnung buchen und drucken** aus.
2. Klicken Sie auf die Schaltfläche **Ja**, um die Rechnung zu buchen.  

> [!NOTE]  
> Susan würde nun die Rechnung an den Kunden senden.  

## <a name="create-an-additional-prepayment-invoice" />Erstellen einer weitere Vorauszahlungsrechnung

Am folgenden Tag, ruft der Kunde Martha an, und nimmt Änderungen am Auftrag vor. Der Debitor möchte zwei Exemplare des Artikels 1896-S. Susan öffnet und aktualisiert den auftrag, und dann erstellt sie eine zweite Vorauszahlungsrechnung auf dem Auftrag und sendet sie an den Debitoren.  

### <a name="to-create-an-additional-prepayment-invoice" />So erstellen Sie eine weitere Vorauszahlungsrechnung

1. Wählen Sie auf der Seite **Verkaufsauftrag** die Aktion **Freigeben** und dann **Erneut öffnen** aus.  
2. Geben Sie in der Zeile für den Artikel **1896-S** im Feld **Menge** den Wert **2** ein.  

    Wählen Sie in der Aktion **Bestellung** die Option **Statistik** aus. Das Feld **Vorauszahlungsbetrag ohne. MWST** enthält jetzt **768,04**, und das Feld **Fakt. Vorauszahlungsbetrag ohne MWST** enthält **417,76**. Diese Werte bedeuten, dass ein zusätzlicher Vorauszahlungsbetrag vorhanden ist, der noch nicht fakturiert wurde.  
3. Wählen Sie nacheinander die Optionen **Aktionen**, **Buchen**, **Vorauszahlung** und dann **Vorauszahlungsrechnung buchen und drucken** aus, um eine Rechnung für den zusätzlichen Vorauszahlungsbetrag zu buchen.
4. Klicken Sie auf die Schaltfläche **Ja**, um die Rechnung zu buchen.  

## <a name="apply-the-prepayments" />Ausgleichen der Vorauszahlungen

Der Debitor zahlt den Vorauszahlungsbetrag. Peter aus der Buchhaltung registriert die Zahlung und wendet sie auf die Vorauszahlungsrechnungen an.  

### <a name="to-apply-a-payment-to-the-prepayment-invoices" />So gleichen Sie eine Zahlung mit den Vorauszahlungsrechnungen aus

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Zahlungseingangs Erfassungsjournale** ein und wählen Sie dann den entsprechenden Link.  
2. Füllen Sie ein Buchhaltungsprotokoll mit den folgenden Informationen aus.  

    |Name des Felds|Enter|  
    |----------------|-----------|  
    |**Belegart**|**Zahlung**|  
    |**Kontoart**|**Debitor**|  
    |**Kontonummer**|**20000**|  
3. Wählen Sie die Aktion **Prozess** und dann **Posten ausgleichen** aus.  
4. Wählen Sie auf der Seite **Debitorenpostenausgleich** die erste Vorauszahlungsrechnung, dann die Aktion **Prozess** und anschliessend Aktion **Ausgleichs-ID setzen** aus.  
5. Wiederholen Sie den vorherigen Schritt für die zweite Vorauszahlung.  
6. Wählen Sie die Schaltfläche **OK**.  

    Die Felder **Betrag** enthalten jetzt die Summe der beiden Vorauszahlungsrechnungen.  

7. Wählen Sie zum Veröffentlichen des Journals die Aktion **Buchen/Drucken** und dann **Buchen** aus.
8. Wählen Sie die Schaltfläche **Ja** aus.

## <a name="invoice-the-remaining-amount" />Fakturieren des Restbetrags

Peter wurde darüber informiert, dass die Artikel im Auftrag geliefert wurden und der Auftrag fakturiert werden kann. Peter erstellt die Rechnung für den Auftrag.  

### <a name="to-invoice-the-remaining-amount" />So fakturieren Sie den Restbetrag

1. Öffnen Sie den Verkaufsauftrag.
2. Wählen Sie die Aktion **Buchung** und dann **Buchen** aus.
3. Wählen Sie **Lieferung und Rechnung** und dann die Schaltfläche **OK** aus.
4. Wenn Sie eine Vorschau der Rechnung anzeigen möchten, wählen Sie die Schaltfläche **Ja** aus.

    > [!NOTE]  
    > Normalerweise wurde die Lieferung bereits von der Versandabteilung gebucht.  

    Peter kann die Historie anzeigen, um sicherzustellen, dass die Verkaufsrechnung wie beabsichtigt erstellt wurde.

5. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Gebuchte Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically" />Aktualisieren Sie den Status von vorausbezahlten Bestellungen und Rechnungen automatisch

Sie können die Auftrags- und Rechnungsverarbeitung beschleunigen, indem Sie Auftragswarteschlangeneinträge einrichten, die den Status dieser Belege automatisch aktualisieren. Wenn eine Vorauszahlungsrechnung bezahlt wird, können die Auftragswarteschlangeneinträge den Dokumentstatus automatisch von **Ausstehende Vorauszahlung** zu **Freigegeben** ändern. Wenn Sie die Jobwarteschlangeneinträge einrichten, müssen Sie folgende Codeunits verwenden: **383 Ausstehende Vorauszahlungsverkäufe aktualisieren** und **383 Ausstehende Vorauszahlungsbestellungen aktualisieren**. Wir empfehlen, die Einträge häufig auszuführen, z. B. jede Minute. Weitere Informationen finden Sie unter [Projektwarteschlangen nutzen, um Aufgaben zu planen](admin-job-queues-schedule-tasks.md)

## <a name="next-steps" />Nächste Schritte

In dieser Demonstration wurde beschrieben, wie Sie [!INCLUDE[prod_short](includes/prod_short.md)] zur Verarbeitung von Vorauszahlungen einrichten. 

- So richten Sie für Debitoren und Artikel Standardvorauszahlungsprozentsätze zu.
- Verwenden Sie verschiedene Methoden, um die Vorauszahlungen für eine Bestellung zu berechnen.  
- Berechnen Sie den Vorauszahlungsbetrag als Prozentsatz des Gesamtbetrags der Bestellung.
- Weisen Sie der Bestellung einen Gesamtvorauszahlungsbetrag zu.  

Zudem wurden das Buchen einer Vorauszahlungsrechnung, Erstellen einer zweiten Vorauszahlungsrechnung bei einer Änderung des Auftrags und das Buchen der endgültigen Rechnung für den Restbetrag erläutert.  

Die Vorauszahlungsfunktionen erleichtern die Einrichtung und Durchsetzung von Vorauszahlungsregeln für Kunden und Artikel. Ausserdem können Sie jede Zahlung gegen eine Rechnung buchen.  

## <a name="see-related-microsoft-trainingtrainingmodulesprepayment-invoices-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Fakturieren von Vorauszahlungen](finance-invoice-prepayments.md)  
[Finanzen](finance.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
