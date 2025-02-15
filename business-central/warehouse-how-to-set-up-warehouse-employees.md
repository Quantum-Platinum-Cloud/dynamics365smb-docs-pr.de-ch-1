---
title: Lagermitarbeiter einrichten
description: 'Jeder Benutzer, von dem Lageraktivitäten ausgeführt werden, muss als Lagermitarbeiter eingerichtet und einem Standardlagerort und ggf. mehreren nicht standardmässigen Lagerorten zugeordnet werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/09/2023
ms.custom: bap-template
ms.search.form: '7328, 7348'
---
# <a name="set-up-warehouse-employees" />Lagermitarbeiter einrichten

Jeder Benutzer, von dem Lageraktivitäten ausgeführt werden, muss als Lagermitarbeiter eingerichtet und einem Standardlagerort und ggf. mehreren nicht standardmässigen Lagerorten zugeordnet werden. [!INCLUDE [prod_short](includes/prod_short.md)] filtert Lageraktivitäten zum Standardstandort des Mitarbeiters. Sie können nur die Lagertätigkeiten am Standort ausführen. Sie können einem Benutzer anderen Standorten zuweisen. Sie können auf diese Standorte zugreifen, aber keine Aktivitäten dort ausführen.

## <a name="to-set-up-warehouse-employees" />So richten Sie die Lagermitarbeiter ein:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Lagermitarbeiter** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Wählen Sie das Feld **Benutzer-ID** und dann den Benutzer aus, der als Lagermitarbeiter hinzugefügt werden soll. Wählen Sie die Schaltfläche **OK** aus.  
4. Geben Sie im Feld **Lagerortcode** den Code des Lagerorts ein, an dem der Lagermitarbeiter arbeitet.  
5. Aktivieren Sie die Umschaltung **Standard**, um den Lagerort als einzigen Lagerort zu definieren, an dem der Mitarbeiter Lageraktivitäten ausführen kann.  
6. Wiederholen Sie diese Schritte, um Lagerorten weitere Mitarbeiter zuzuordnen oder um andere Lagerorte bestehenden Lagermitarbeitern zuzuordnen.  

## <a name="see-related-microsoft-trainingtrainingmodulesget-started-warehouse-management" />Siehe verwandte [Microsoft Schulungen](/training/modules/get-started-warehouse-management/)

## <a name="see-also" />Siehe auch

[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Bestand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)  
[Montageverwaltung](assembly-assemble-items.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definieren Sie eine Rechnungsbuchungsrichtlinie für Benutzer](admin-setup-invoice-posting-policy.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
