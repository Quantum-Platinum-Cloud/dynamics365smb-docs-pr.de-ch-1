---
title: Drucken einer Liste zur Lagerkommissionierung aus einem Verkaufsauftrag
description: 'Sie können eine Lager-Kommissionierliste direkt aus einem Verkaufsauftrag, Verkaufsbeleg, Rechnungsbeleg und anderen ausgehenden Verkaufsauftragsbelegen drucken.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="print-the-picking-list" />Kommissionierliste drucken

Sie können eine Lager-Kommissionierliste direkt aus einem Verkaufsauftrag und anderen Belegen drucken, die den Versand von Artikeln einleiten.

Dieser Bericht wird normalerweise in Unternehmen ohne dedizierte Funktionen für die Lagerverwaltung verwendet, sodass ein Lagerarbeiter die Kommissionierliste über den zugehörigen Verkaufsbeleg aufrufen oder drucken kann. In Unternehmen mit höherem Volumen oder komplexeren Prozessen werden die Lieferung und die Kommissionierung in dedizierten Lagerbelegen geplant und durchgeführt. Weitere Informationen finden Sie unter [Ausgehender Lagerfluss](design-details-outbound-warehouse-flow.md).

## <a name="to-print-a-picking-list-from-a-sales-order" />So drucken Sie eine Kommissionierliste aus einem Verkaufsauftrag

Das folgende Verfahren basiert auf einer Auftragsabwicklung. Die Schritte sind für alle anderen Belege ähnlich, mit denen der Versand von Artikeln eingeleitet werden kann, z. B. ein Umlagerungsauftrag.

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Symbol 'Nach Seite oder Bericht suchen'") Symbol. Geben Sie **Verkaufsaufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Öffnen Sie den Verkaufsauftrag, für den Sie Artikel auswählen möchten.  
3. Wählen Sie die Aktion **Bericht** und dann die Aktion **Kommissionierliste nach Bestellung** aus.  
4. Wählen Sie die Schaltfläche **Drucken** aus, um die Auswahlliste zu drucken oder wählen Sie die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.

Sie können die Kommissionierliste auch als Dokument speichern, um sie beispielsweise an jemanden zu senden oder dem Verkaufsauftrag als Anhang hinzuzufügen. Weitere Informationen finden Sie unter [Verwalten von Anhängen, Links und Notizen zu Karten und Belegen](ui-how-add-link-to-record.md).

> [!NOTE]
> Wenn Sie die Funktion **Stückliste explodieren** auf dem Verkaufsauftrag verwendet haben, werden im Bericht nur die Komponenten des zugehörigen Montageartikels angezeigt. Weitere Informationen finden Sie unter [Mit Stücklisten arbeiten](inventory-how-work-BOMs.md).

## <a name="see-also" />Weitere Informationen

[Bestand](inventory-manage-inventory.md)  
[Ausgehende Lagerflüsse](design-details-outbound-warehouse-flow.md)
[Arbeiten Sie mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
