---
title: Design-Details – Planungszuordnungstabelle
description: 'Dieses Thema bietet einen Einblick in das, was passiert, wenn eine Änderung des Bedarfs oder der Vorräte erfordert, dass Sie berechnen, wie Sie für ein Element planen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-planning-assignment-table" />Designdetails: Planungs-Zuordnungstabelle
Alle Artikel sollten eingeplant werden, es gibt jedoch keinen Grund, einen Plan für einen Artikel zu berechnen, es sei denn, es gab eine Änderung im Bedarfs- oder Vorratsmuster seit der letzten Berechnung des Plans.  

Wenn der Benutzer einen neuen Verkaufsauftrag eingegeben oder einen vorhandenen geändert hat, gibt es Gründe zur Neuberechnung des Plans. Andere Ursachen beinhalten eine Änderung in der Planung oder im gewünschten Sicherheitsbestand. Das Ändern einer Stückliste durch Hinzufügen oder Entfernen einer Komponente führt wahrscheinlich zur Anzeige einer Änderung, jedoch nur für den Komponentenartikel.  

Für mehrere Lagerorte findet die Zuweisung auf Artikelebene pro Lagerortkombination statt. Wenn beispielsweise ein Auftrag an nur einem Lagerplatz erstellt wurde, ordnet die Anwendung den Artikel an diesem bestimmten Lagerort der Planung zu.  

Der Grund für die Auswahl von Artikeln für die Planung hat mit der Systemleistung zu tun. Wenn keine Änderung des Bedarf-Vorrat-Musters eines Artikels eingetreten ist, schlägt das Planungssystem keine Aktionen vor. Ohne die Planungs-Zuweisung müsste das System die Berechnungen für alle Artikel ausführen, um herauszufinden, was zu planen ist, wodurch die Systemressourcen belastet würden.  

Die Tabelle **Planungszuweisung** überwacht Bedarf und Vorrat und ordnet die entsprechenden Artikel für die Planung zu. Die folgenden Ereignisse werden überwacht:  

* Ein neuer Verkaufsauftrag, eine Planung, eine Komponente, eine Bestellung, ein Fertigungsauftrag, ein Montageauftrag oder ein Umlagerungsauftrag.  
* Änderung von Artikel, Menge, Lagerort, Variante oder Datum auf einem Verkaufsauftrag, Plan, einer Komponente, einem Einkaufsauftrag, einem Produktionsauftrag, einem Montageauftrag oder einem Umlagerungsauftrag.  
* Stornierung eines Verkaufsauftrags, einer Planung, einer Komponente, einer Bestellung, eines Fertigungsauftrags, eines Montageauftrags oder eines Umlagerungsauftrags.  
* Verbrauch von Artikeln ausserhalb der Planung.  
* Istmeldungen von Artikeln ausserhalb der Planung.  
* Ungeplante Bestandänderungen.  

Für diese direkten Vorrat-Bedarf-Verschiebungen wahrt das Auftragstracking- und Aktionsmeldungssystem die Planungs-Zuordnungstabelle und gibt einen Planungsgrund als Aktionsmeldung aus.  

Die folgenden Änderungen in den Stammdaten können ebenfalls eine Planungsunausgeglichenheit verursachen:  

* Änderung des Status zu Zertifiziert im Fertigungsstücklistenkopf (für alle Artikel mit diesem Kopf).  
* Gelöschte Zeile (untergeordneter Artikel).  
* Änderung des Status zu Zertifiziert im Arbeitsplankopf (für alle Artikel mit diesem Arbeitsplan).  
* Änderungen in den folgenden Artikelkartenfeldern.  
* Sicherheitsbestand oder Sicherh.-Zuschl. Beschaff.-Zt.  
* Beschaffungszeit.  
* Minimalbestand.  
* Fert.-Stücklistennr (und alle untergeordneten Elemente der alten Stücklistenreferenz).  
* Arbeitsplannr.  
* Wiederbeschaffungsverfahren.  

In diesen Fällen verwaltet eine neue Funktion, Planungszuweisungs-Verwaltung, die Tabelle und zeigt den Planungsgrund als Nettoänderung an.  

Die folgenden Änderungen verursachen keine Planungszuweisung:  

* Kalender  
* Andere Planungsparameter auf einer Artikelkarte sind:  

Wenn sie eine Prod.-Programmplanung oder einen Nettobedarf berechnen, gelten die folgenden Einschränkungen:  

* Prod.-Programmplanung: Die Planungssystemprüfungen prüft, ob der Artikel eine Absatzplanung oder einen Verkaufsauftrag führt. Wenn nicht, ist der Artikel nicht im Plan enthalten.  
* Nettobedarf: Wenn das Planungssystem erkennt, dass der Artikel durch eine Prod.-Programmplanungs-Planungszeile oder einen Prod.-Programmplanungs-Beschaffungsauftrag aufgefüllt wird, wird der Artikel aus der Planung genommen. Jedoch ist jeder Bedarf aus den entsprechenden Komponenten enthalten.  

## <a name="see-also" />Siehe auch
[Designdetails: Ausgleich von Bedarf und Vorrat](design-details-balancing-demand-and-supply.md)   
[Designdetails: Umgang mit Wiederbeschaffungsverfahren](design-details-handling-reordering-policies.md)   
[Designdetails: Umlagerungen in Planung](design-details-transfers-in-planning.md)   
[Designdetails: Planungsparameter](design-details-planning-parameters.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
