---
title: Mit Fertigungsfamilien in der Produktion arbeiten
description: 'Die Hauptaufgabe beim Anpassen eines Basiskalenders für Ihre Firma oder einen Ihrer Geschäftspartner ist, alle Änderungen am Status der Daten als freie Tage oder Arbeitstage einzugeben.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000790, 99000791, 99000792, 99000793'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="work-with-production-families" />Arbeiten mit Fertigungsfamilien

Eine Fertigungsfamilie ist eine Gruppe einzelner Artikel, deren Zusammenhang in der Ähnlichkeit ihres Fertigungsprozesses liegt. Wenn Sie Fertigungsfamilien zusammenstellen, können einzelne Artikel mehrfach, in einem Arbeitsschritt, gefertigt werden, womit Sie den Materialverbrauch optimieren können.

Geben Sie auf der **Menge**-Seite im **Familien**-Fenster die Menge ein, die gefertigt werden soll, wenn die gesamte Fertigungsfamilie einmal gefertigt wird.

## <a name="example" />Beispiel

Beim Stanzen können vier Teile eines Artikels und 10 Teile eines anderen Artikels aus einem Blech zur gleichen Zeit gestanzt werden. Die Stanzmaschine stanzt die kompletten 14 Teile in einem Arbeitsschritt.

Fertigungsfamilien verringern die Ausschussmenge, da der normalerweise bei der Fertigung grosser Teile entstehende Ausschuss zur Fertigung kleiner Teile verwendet wird.

## <a name="to-set-up-a-production-family" />Fertigungsfamilien einrichten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Fertigungsfamilien** ein, und wählen Sie dann den entsprechenden Link.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-produce-based-on-a-production-family" />Um auf Grundlage eine Produktionsfamilie erzeugen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Geplante Prod. Aufträge** ein und wählen Sie dann den zugehörigen Link.
2. Dient zum Erstellen eines neuen Produktionsauftrags. Weitere Informationen finden Sie unter [Erstellen von Montageaufträgen](production-how-to-create-production-orders.md).
3. Wählen Sie im Feld **Quelltyp** **Familie** aus.  
4. Wählen Sie im Feld **Quelle** die entsprechende Produktionsfamilien aus.

## <a name="see-also" />Siehe auch

[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)  
[Produktion einrichten](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)
[Planung](production-planning.md)   
[Bestand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
