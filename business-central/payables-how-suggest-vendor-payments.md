---
title: Stapelverarbeitung „Zahlungsvorschlag“ vorschlagen
description: 'Sie können Kreditorenzahlungseinstellungen festlegen, um Vorschläge für Zahlungen zu erhalten, die in Kürze fällig sind oder für die ein Rabatt verfügbar ist.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: 256
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="suggest-vendor-payments" />Zahlungsvorschlag

Auf der Seite **Zahlungsjournal** können Sie die Stapelverarbeitung **Zahlungsvorschlag** verwenden, um Zahlungspositionen vorzuschlagen. Zeilen für Elemente wie Zahlungen, die in Kürze fällig sind oder Zahlungen, bei denen ein Skonto verfügbar ist, werden entsprechend Ihren Einstellungen vorgeschlagen.

Um aus vorgeschlagenen Zeilen voll zu profitieren, müssen Sie zuerst die Kreditoren priorisieren. Weitere Informationen finden Sie unter [Priorisieren von Kreditoren](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> In die Stapelverarbeitung werden nur die Kreditorenposten einbezogen, bei denen das Feld **Abwarten** nicht markiert ist.  

> [!IMPORTANT]  
>   Wenn Sie Skonti nutzen möchten und einen verfügbaren Betrag eingegeben haben, wird der Rechnungsrabatt verwendet für:  
    * Priorisierte überfällige Kreditorenposten nach der Priorität.   
    * Überfällige Kreditorenposten, die nicht berücksichtigt werden.  
    * Öffnen Sie die Kreditorenposten, die sich für Skonti qualifizieren, angeordnet nach Kreditorennummer.  

## <a name="to-use-the-suggest-vendor-payments-function" />Die Zahlungsvorschlagfunktion verwenden

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Zahlungsausgangs Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie das relevante Erfassungsjournal, und klicken Sie dann auf die Aktion **Zahlungsvorschlag**.  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Wählen Sie die Schaltfläche **OK** aus.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines" />Einfügen des Fälligkeitsdatum als Buchungsdatum auf Zahlungsausgangs-Erfassungsjournalzeilen

Wenn Sie die Stapelverarbeitung **Zahlungsvorschlag** verwenden, um Zahlungszeilen für Ihre Kreditoren zu erstellen, können Sie zwei Felder ausfüllen, um sicherzustellen, dass die erzeugten Zeilen das Fälligkeitsdatum verwenden, um das Buchungsdatum zu berechnen. Diese Felder sind **Buchungsdatum von Fälligkeitsdatum für Ausgleich mit Beleg berechnen** und **Offset für Fälligkeitsdatum für Ausgleich mit Beleg**.  

> [!IMPORTANT]  
>   Sie können das Feld **Buchungsdatum von Fälligkeitsdatum für Ausgleich mit Beleg berechnen** nicht zusammen mit den Feldern **Skonto finden** oder **Pro Kreditor summieren** verwenden. Der Grund besteht darin, dass, wenn das Buchungsdatum auf dem Fälligkeitsdatum liegt, einige Zahlungsrabatte nicht korrekt berechnet werden, da das Buchungsdatum nach dem Zahlungsrabattdatum liegen kann.  

Wenn das berechnete Buchungsdatum also in der Vergangenheit liegt, wird das Buchungsdatum auf das Arbeitsdatum verschoben, und eine Warnung wird angezeigt.  

Alternativ können Sie Zahlungspositionen mithilfe des Fälligkeitsdatums manuell generieren, um das Buchungsdatum zu berechnen Nachdem Sie Kreditorenposten ausgleichen, können Sie die Aktion **Buchungsdatum berechnen**  verwenden, um das Buchungsdatum der Buch.-Blattzeile mit dem Fälligkeitsdatum der zugehörigen Einkaufsrechnung zu aktualisieren. Weitere Informationen finden Sie unter [Einkaufstransaktionen manuell ausgleichen](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Wenn die Einkaufsrechnung überfällig ist, wird das Buchungsdatum auf das Arbeitsdatum festgelegt, und die Schrift auf der Zeile wird in roter Farbe angezeigt.  

## <a name="see-related-microsoft-trainingtrainingmodulessuggest-vendor-payments-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/suggest-vendor-payments-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Zahlungen vornehmen](payables-make-payments.md)  
[Arbeiten mit Fibu Erfassungsjournalen](ui-work-general-journals.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
