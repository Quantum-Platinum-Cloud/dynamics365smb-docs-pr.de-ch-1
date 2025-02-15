---
title: Wie Sie mit Zuständigkeitseinheiten arbeiten
description: 'Zuständigkeitseinheiten als Verwaltungszentren helfen Unternehmen, benutzerspezifische Ansichten von Einkaufs- und Kaufbelegen festzulegen, die sich ausschliesslich auf das jeweilige Zentrum beziehen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '5714, 5715'
ms.date: 03/09/2023
ms.author: bholtorf
---
# <a name="work-with-responsibility-centers" />Arbeiten mit Zuständigkeitseinheiten

Zuständigkeitseinheiten ermöglichen die Verwaltung von Verwaltungscentern. Eine Zuständigkeitseinheit kann ein Cost Center, ein Profit Center, ein Investment Center oder ein anderes unternehmensdefiniertes Verwaltungscenter sein. Beispiele von Zuständigkeitseinheiten können ein Verkaufsbüro, eine Einkaufsabteilung für mehrere Lagerorte und ein Fabrikplanungsbüro sein. Mithilfe dieser Funktionalität können Unternehmen beispielsweise benutzerspezifische Ansichten von Verkaufs- und Einkaufsbelegen einrichten, die ausschliesslich mit einem bestimmten Verwaltungscenter zusammenhängen.  

Die Verwendung mehrerer Lagerorte und Zuständigkeitseinheiten bietet Unternehmen mit mehreren Lagerorten die Möglichkeit, ihre Unternehmensabläufe äusserst flexibel und zugleich so optimal wie möglich zu verwalten.

Die Funktionalität "Mehrere Lagerorte" ermöglicht Unternehmen die Verwaltung ihres Lagers an mehreren Lagerorten mithilfe einer Datenbank. Zwei Konzepte, Lagerorte und Lagerhaltungsdaten, bilden die Eckpfeiler dieses Elements. Ein Lagerort ist definiert als ein Ort, der die physische Platzierung von Artikeln sowie Artikelmengen verwaltet. Das begriffliche Konzept erstreckt sich auch auf Anlagen oder Produktionsstätten sowie Vertriebsstellen, Lager, Verkaufsräume und Dienstfahrzeuge. Lagerhaltungsdaten sind definiert als ein Artikel an einem bestimmten Lagerort und/oder als Variante. Mithilfe von Lagerhaltungsdaten können Unternehmen mit mehreren Standorten Beschaffungsdaten, Adressen sowie einige Finanzbuchungsdaten auf Standortebene hinzuzufügen. Dadurch können Sie Varianten desselben Artikels für einen einzelnen Lagerort beschaffen und Artikel für die einzelnen Standorte auf der Grundlage standortspezifischer Beschaffungsdaten bestellen.  

## <a name="to-set-up-a-responsibility-center" />Zuständigkeitseinheiten einrichten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Zuständigkeitseinheiten** ein, und wählen Sie dann den entsprechenden Link.  
2. Wählen Sie die Aktion **Neu** aus.  
3. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Wenn Sie den Mandanten mithilfe von Zuständigkeitseinheiten verwalten, empfiehlt es sich möglicherweise, eine standardmässige Zuständigkeitseinheit für den Mandanten einzurichten.
4. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Unternehmensdaten** ein, und wählen Sie dann den zugehörigen Link.
5. In dem Feld **Zuständigkeitseinheiten** können Sie einen Zuständigkeitseinheitencode eingeben.

Dieser Code wird auf Einkaufs- und Verkaufsbelegen oder Servicebelegen verwendet werden, wenn der Anwender, Debitor oder Kreditor keine standardmässige Zuständigkeitseinheit hat. Auf allen möglichen Verkaufs- oder Einkaufs-Belegen können Sie eine andere Zuständigkeitseinheit als die standardmässige eingeben.

> [!NOTE]  
> Wenn Sie einen Zuständigkeitseinheitencode in einem Beleg angeben, beeinflusst er die Adresse, Dimensionen und Preise im Beleg.  

## <a name="to-assign-responsibility-centers-to-users" />Zuständigkeitseinheiten für Benutzer zuweisen:

Sie können die Benutzer so einrichten, dass [!INCLUDE [prod_short](includes/prod_short.md)] nur die entsprechenden Belege für ihre speziellen Arbeitsbereiche anzeigt. Benutzer werden normalerweise mit einer Zuständigkeitseinheit verknüpft und arbeiten nur mit Belegen, die mit speziellen Anwendungsbereichen in dieser Zuständigkeitseinheit verbunden sind.  

Um dies einzurichten, weisen Sie Benutzern Zuständigkeitseinheiten in drei Basisfunktionsbereichen zu: Kreditoren, Einkauf und Servicemanagement.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Benutzereinrichtung** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie im Fenster **Benutzer einrichten** den Benutzer, dem Sie eine Zuständigkeitseinheit zuweisen wollen. Wenn sich der Benutzer nicht in der Liste befindet, müssen Sie eine Benutzer-ID im Feld **Benutzer-ID** eingeben.  
3. Im Feld **Verk.-Zuständigk.-Einh. Filter** geben Sie die Zuständigkeitseinheit ein, in der der Benutzer Aufgaben haben wird, die mit "Debitoren &amp; Verkauf" verbunden sind.  
4. Im Feld  **Eink.-Zuständigk.-Einh. Filter** geben Sie die Zuständigkeitseinheit ein, in der der Benutzer Aufgaben haben wird, die mit "Kreditoren &amp;amp; Einkauf" verknüpft sind.  
5. Im Feld **Serv.-Zuständigk.-Einh. Filter** geben Sie die Zuständigkeitseinheit ein, in der der Benutzer Aufgaben haben wird, die mit Serviceverwaltung verknüpft sind.  

> [!NOTE]  
> Benutzer können nur die gebuchten Belege anzeigen, die sich auf ihr eigenes Verantwortungszentrum beziehen. Sie können jedoch alle Ledger-Einträge anzeigen und aus den Ledger-Einträgen zu anderen gebuchten Belegen navigieren.

## <a name="see-related-microsoft-trainingtrainingmodulesset-up-responsibility-centers" />Siehe verwandte [Microsoft Schulungen](/training/modules/set-up-responsibility-centers/)

## <a name="see-also" />Siehe auch

[Bestand einrichten](inventory-setup-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Lagerverwaltung – Übersicht](design-details-warehouse-management.md)
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Definieren Sie eine Rechnungsbuchungsrichtlinie für Benutzer](admin-setup-invoice-posting-policy.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
