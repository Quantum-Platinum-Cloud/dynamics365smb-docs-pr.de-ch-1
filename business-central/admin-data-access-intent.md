---
title: Datenbank-Zugriffsabsicht in Business Central verwalten
description: 'Ändern Sie die Datenbank-Zugriffsabsicht für Berichte, API-Seiten und Abfragen.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9880
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="managing-database-access-intent" />Verwaltung der Datenbank-Zugriffsabsicht

Als Superuser oder Administrator können Sie die Datenbankzugriffsabsicht auf Berichte, Seiten vom Typ API und Abfragen ändern, um die Leistung des Dienstes zu verbessern.

## <a name="overview" />Matrix

[!INCLUDE[prod_short](includes/prod_short.md)] kann so eingerichtet werden, dass schreibgeschützte Replikate der primären Datenbank (Lesen und Schreiben) verwendet werden. Die Verwendung der Datenbankreplik reduziert die Belastung der primären Datenbank. In einigen Fällen wird dadurch auch die Leistung beim Anzeigen von Daten im Client verbessert. Replikate sind vorteilhaft für Objekte wie Berichte, Abfragen und API-Seiten, die nur zur Anzeige von Daten, nicht zur Änderung von Daten verwendet werden.

Wenn Objekte ausgeführt werden, bestimmt die Datenbank-Zugriffsabsicht, ob eine schreibgeschützte Replik, falls vorhanden, oder die primäre Datenbank verwendet werden soll. Berichte, API-Seiten und Abfragen werden mit einer vordefinierten Datenbank-Zugriffsabsicht entwickelt (siehe [DatabaseAccessIntent-Eigenschaft](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

Auf der Seite **Datenbank-Zugriffsabsichtsliste** können Sie die vordefinierte Datenbank-Zugriffsabsicht für Objekte ausser Kraft setzen, wenn sie ausgeführt werden.

In Bezug auf die Datenbank wird diese Funktion allgemein als *Lesen Scale-out* bezeichnet. Weitere Informationen über die Ausleseskalierung und die Datenzugriffsabsicht in [!INCLUDE[prod_short](includes/prod_short.md)] finden Sie unter [Ausnutzung der Ausleseskalierung für eine bessere Leistung](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) in der Hilfe für Entwickler und die Verwaltung unter [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-change-the-database-access-intent" />So ändern Sie die Datenbank-Zugriffsabsicht

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Liste Datenbankzugriffsabsicht** ein, und wählen Sie den zugehörigen Link.

    Die Seite listet alle Berichte, Seiten und Abfragen auf. Die Spalte **Zugriffsabsicht** enthält einen der folgenden Werte:

    |**Einstellung**|**Description**|  
    |------------|-------------|  
    |**Standard**|Zeigt an, dass das Objekt die vordefinierte Datenbankzugriffsabsicht verwendet.|
    |**Schreiben erlauben**|Legt das Objekt so fest, dass es die primäre Datenbank verwendet, was bedeutet, dass der Benutzer Daten ändern kann.|
    |**Nur lesen**|Legen Sie das Objekt so fest, dass die Datenbankreplik verwendet wird, d.h. der Benutzer kann die Daten nur anzeigen und nicht ändern.|

2. Wählen Sie die Aktion **Liste bearbeiten** aus.

3. Ändern Sie auf der Seite **Bearbeiten - Datenbank-Zugriffsabsichtsliste** das Feld **Zugriffsabsicht** für die Objekte.

    > [!NOTE]
    > Wenn ein editierbares Objekt, wie die Debitorenkarte, auf **Nur lesen** gesetzt ist, wird die primäre Datenbank unabhängig von der Zugriffsabsicht weiterhin verwendet, so dass die Benutzer wie gewohnt Änderungen vornehmen können.

## <a name="see-related-microsoft-trainingtrainingpathsdeploy-configure-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch
[Geschäftsfunktionen](across-business-functionality.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)    

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
