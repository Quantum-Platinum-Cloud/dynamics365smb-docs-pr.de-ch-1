---
title: So sperren Sie Artikel vom Verkauf oder Einkauf
description: 'Sie können verhindern, dass Artikel in Zeilen von Verkaufs- oder Kaufbelegen eingegeben oder in einer Transaktion gebucht werden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 11/03/2022
ms.author: bholtorf
---
# <a name="block-items-from-sales-or-purchasing" />Artikel vom Verkauf oder Einkauf sperren

Sie können einen Artikel sperren, damit er nicht in Zeilen von Verkaufs- oder Einkaufsbelegen eingegeben und nicht in Transaktionen gebucht werden kann. Dies ist beispielsweise nützlich, wenn ein Artikel einen bekannten Fehler aufweist. Wenn jemand in einem Verkaufs- oder Einkaufsbeleg einen gesperrten Artikel auswählt, wird er durch eine Nachricht darüber informiert, dass der Artikel gesperrt ist.

In der folgenden Tabelle wird beschrieben, was geschieht, wenn Artikel gesperrt sind.  

|Option|Description|  
|--------------------|------------|  
|**Vertrieb gesperrt**|Sie können den Artikel nicht in einen Verkaufsbeleg oder in einem Verkaufsartikel-Erfassungsjournal eingeben.|  
|**Einkauf gesperrt**|Sie können den Artikel nicht in einen Einkaufsbeleg, in einem Einkaufsartikel-Erfassungsjournal oder in Einkaufsplanungsvorgänge eingeben.|  
|**Gesperrt**|Sie können den Artikel nicht in Transaktionen einbeziehen.|  

> [!NOTE]
> Blockierte Artikel können zurückgesendet werden. Das bedeutet, dass keine der obigen Einstellungen für Retouren und Gutschriften gilt.

Wenn Sie die Aktion **Aus Dokument kopieren** verwenden, um neue Belege auf der Grundlage vorhandener Belege zu erstellen, werden Sie benachrichtigt, wenn Artikel in den Zeilen des Quellbelegs blockiert sind. Die gesperrten Belegzeilen werden vom neuen Beleg ausgeschlossen, und eine Benachrichtigung zeigt eine Übersicht aller Belegzeilen, die im Quellbeleg gesperrt sind.

## <a name="to-block-an-item-from-being-entered-on-sales-lines" />So sperren Sie einen Artikel vom Eintrag auf Verkaufszeilen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Verkauf gesperrt** aus.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines" />So sperren Sie einen Artikel vom Eintrag auf Einkaufszeilen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Einkauf gesperrt** aus.  

## <a name="to-block-an-item-from-being-posted" />So sperren Sie einen Artikel vor der Buchung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Elemente** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Artikel aus, den Sie sperren möchten, und wählen Sie dann das Kontrollkästchen **Gesperrt** aus.

## <a name="see-also" />Siehe auch

[Neue Artikel registrieren](inventory-how-register-new-items.md)  
[Lagerbestand](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
