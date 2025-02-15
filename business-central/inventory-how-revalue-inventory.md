---
title: Erstellen Sie Neuwert-Posten für Artikel im Lagerbestand| Microsoft Docs
description: 'Beschreibt, wie Sie die Werteinträge eines oder mehrerer Artikel im Bestand aufwerten oder abschreiben, indem Sie deren aktuellen, berechneten Wert buchen.'
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'costing, inventory cost, value entries'
ms.search.forms: '5803,'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="revalue-inventory" />Neubewerten von Lagerbestand
Wenn Sie den Lagerwert eines Artikels oder den eines bestimmten Lagerpostens nach oben oder unten verändern möchten, müssen Sie das Neubewertungs Erf.-Journal verwenden.

## <a name="to-revalue-inventory" />Neubewerten von Lagerbestand
1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Neubewertungs Erf.-Journal** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Aktion **Lagerwert berechnen** aus.
3. Füllen Sie auf der Seite **Lagerwert berechnen** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wählen Sie die Schaltfläche **OK** aus.
5. In jeder Zeile auf der Seite **Neubewertungs-Erf.-Journal** im Feld **Einheitskosten (neu bewertet)** geben Sie den neuen Einstandspreis ein. Oder geben Sie den Gesamtbetrag im Feld **Lagerwert (neu bewertet)** ein.

    Die entsprechenden Felder werden automatisch aktualisiert. Beachten Sie, dass das Feld **Betrag** die tatsächliche Änderung des Lagerwertes für den ausgewählten Lagerposten zeigt. Es berechnet die Differenz zwischen den Feldern **Lagerwert (berechnet)** und **Lagerwert (neu bewertet)**.
6. Wenn Sie das Einlagern der Artikel abgeschlossen haben, wählen Sie die Aktion **Buchen** aus.

Neue Wertposten werden nun erstellt, um die Neubewertungen abzubilden, die Sie gebucht haben. Sie können die neuen Werte in der entsprechenden Artikelkarten sehen.

## <a name="see-also" />Siehe auch
[Designdetails: Neubewertung](design-details-revaluation.md)  
[Bestand](inventory-manage-inventory.md)  
[Verkauf](sales-manage-sales.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
