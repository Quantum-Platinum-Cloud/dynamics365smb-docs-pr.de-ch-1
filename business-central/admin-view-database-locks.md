---
title: Datenbank-Sperren anzeigen
description: 'Erfahren Sie, wie Sie Informationen über Debitoren-Datenbanksperren direkt über die Client-Oberfläche in Business Central anzeigen können.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 9511
ms.date: 06/14/2021
ms.author: jswymer
---
# <a name="viewing-database-locks" />Anzeigen von Datenbank-Sperren

Die Datenbanksperre steuert den gleichzeitigen Zugriff mehrerer Benutzer auf dieselben Daten. Um eine Transaktion gegen andere Transaktionen zu schützen, die dieselben Daten ändern, sperrt die erste Transaktion die Daten. Die Sperre bleibt bestehen, bis die Transaktion abgeschlossen ist.

Benutzer können für den Abschluss von Transaktionen mit den gesperrten Daten gesperrt werden. Sie erhalten in der Regel eine Meldung, die den Sperrzustand anzeigt.

## <a name="to-view-database-locks" />So zeigen Sie Datenbanksperren an

Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Suche nach Seiten- oder Berichtssymbolen") Symbol. Geben Sie **Datenbanksperren** ein und wählen Sie dann den zugehörigen Link.

Die Seite **Datenbanksperren** zeigt eine Momentaufnahme aller aktuellen Datenbanksperren.

Weitere Informationen über Datenbanksperren finden Sie unter [Überwachung von Datenbanksperren](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in der Hilfe für Business Central Entwickler und IT Pro.

## <a name="see-also" />Siehe auch

[Datenbanksperren überwachen](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]
