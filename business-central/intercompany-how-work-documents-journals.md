---
title: Intercompany Belege und Erfassungen posten
description: 'Dieses Thema erklärt, wie Sie Intercompany-Belege oder Erfassungen verwenden, um Transaktionen mit Ihren Intercompany-Partnern zu buchen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '600, 610'
---
# <a name="work-with-intercompany-documents-and-journals" />Mit Intercompany-Belegen und -Erfassungsjournalen arbeiten

Intercompanybelege bzw. -Erf.-Journale werden zum Buchen der Transaktionen zwischen Intercompanypartnern verwenden. Wenn Sie einen Intercompanybeleg oder eine Erf.-Journalzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Sie übertragen die Leitung von Ihrem Postausgang zu Ihrem Partner. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

Für Verkaufsaufträge und Einkaufsbelege stellt der Intercompanypartner auf den entsprechenden Debitor oder Kreditor sicher, dass alle Aufträge und Rechnungen für Transaktionen zwischen den Partnern entsprechende Belege in den Partnerunternehmen erstellen. Die Firmenkonten saldieren korrekt.

Dasselbe gilt für Intercompany-Erfassungsjournalzeilen. Sie müssen keine Konten angeben, Sie wählen einfach das Partnerunternehmen aus. In der Partnerfirma werden dann entsprechende Intercompany-Fbu Erfassungsjournalzeilen erstellt.

## <a name="fill-in-and-send-an-intercompany-sales-order" />Einen Intercompanyauftrag ausfüllen und senden

Aufträge, Bestellungen und Rücksendungen können vor der Buchung gesendet werden. Rechnungen und Gutschriften können jedoch erst gesendet werden, nachdem sie gebucht sind.

Im Folgenden wird beschrieben, wie ein Intercompanyauftrag ausgefüllt und gesendet wird. Die gleichen Schritte gelten auch für Intercompanybestellungen und Reklamationen und Intercompanyrechnungen auf Rechnungen und Gutschriften.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Um neue Verkaufsaufträge zu erstellen, wählen Sie **Neu**. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Stellt sicher, dass der Debitor ein Intercompany-Partner ist.
5. Um den Verkaufsauftrag zu senden, bevor Sie ihn buchen, wählen Sie die **IC Verkaufsauftrag senden** Aktion aus.

> [!NOTE]
> Wenn Sie Schritt 5 ausführen, wird der Verkaufsauftrag auf den Intercompany-Ausgang verschoben, wo er später dann gebucht werden kann. Um mehr über den Intercompany-Eingang und -Ausgang zu erfahren, gehen Sie zu [ Verwalten Sie den Intercompany-Eingang und -Ausgang](intercompany-how-manage-intercompany-inbox.md).

## <a name="fill-in-and-post-an-intercompany-journal" />Intercompany-Erfassungsjournal ausfüllen und buchen

Wenn Sie einen Intercompany-Fibu-Erf.-Journalzeile im Unternehmen buchen, wird durch das Programm im IC-Ausgang ein entsprechender Beleg erstellt, der an den Partner übertragen werden kann. Seit dem 1. Veröffentlichungszyklus 2022 können Sie das Unternehmen für die automatische Erstellung empfangener Intercompany-Transaktionen von Intercompany-Partnern einrichten, die über das Intercompany-Erfassungsjournal gebucht werden. Der Partner kann dieses Buch.-Blatt dann im eigenen Unternehmen buchen, ohne die Daten dazu noch einmal eingeben zu müssen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Intercompany-Fibu Erfassungsjournale** ein, und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie das Erf.-Journal. Weitere Informationen finden Sie unter [Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md).
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. Geben Sie im Feld **IC Partner-Fibukontonr.** das IC-Fibukonto ein, auf das der Betrag beim Partnerunternehmen gebucht wird.

    > [!NOTE]
    > Das Feld muss auf einer Zeile mit einem Bank- bzw. Fibukonto im Feld **Kontonr.** oder **Gegenkontonr.** ausgefüllt werden.  
5. Wählen Sie die Aktion **Buchen** aus.

Die entsprechenden Posten werden im Unternehmen gebucht und ein Erf.-Journal mit den entsprechenden Posten wird im Intercompanyausgang erstellt, den Sie dann an das Partnerunternehmen senden können.

## <a name="see-also" />Siehe auch

[Intercompanytransaktionen verwalten](intercompany-manage.md)  
[Finanzen](finance.md)  
[Finance einrichten](finance-setup-finance.md)  
[Arbeiten mit Fibu Erfassungsjournalen](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
