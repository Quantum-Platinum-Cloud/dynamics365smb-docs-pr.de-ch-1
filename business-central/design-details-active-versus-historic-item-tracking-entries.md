---
title: Design-Details – Aktive versus historische Elemente zur Tracking von Einträgen
description: 'Wenn Teile einer Beleg-Zeilen-Menge gebucht werden, wird nur diese Menge in die Artikel-Ledger-Einträge und ihre Artikeltrackingsnummern übertragen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-active-versus-historic-item-tracking-entries" />Designdetails: Aktive vs. historische Artikeltrackingposten
Wenn Teile einer Belegzeilenmenge gebucht werden, wird nur diese bestimmte Menge in Lagerposten und deren Artikeltrackingnummern übertragen. Jedoch möchten Sie sicher auf alle relevanten Trackinginformationen des Artikels direkt aus der aktiven Belegzeile heraus zugreifen. Anders ausgedrückt, Sie möchten nicht nur die Posten, die mit der Restmenge verbunden sind, sondern Sie wünschen auch Informationen über die gebuchten Einheiten. Wenn Sie die Seite **Artikeltrackingzeilen** anzeigen oder ändern, werden die Kollektivinhalte der Tabelle **Trackingspezifikation** (T336) und der Tabelle **Reservierungsposten** (T337) in einer temporären Version von T336 dargestellt. Dadurch ist sichergestellt, dass auf historische und aktive Artikeltrackingdaten als Einheit zugegriffen wird.  

 Die nachstehende Tabelle zeigt, wie T336 und T337 in einem Einkaufsszenario verwendet werden. Die fettgedruckten Zahlen stellen Werte dar, die der Benutzer manuell auf der **Artikeltrackingzeilen**-Seite eingibt.  

 Schritt 1: Erstellen Sie eine Einkaufszeile von sieben Stück mit Artikeltrackingnummern.  

||**Menge (Basis)**|**Bewegungsmge.**|**Zu fakturieren Menge (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Fakturierte Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Schritt 2: Empfangen Sie vier Teile.  

||**Menge (Basis)**|**Bewegungsmge.**|**Zu fakturieren Menge (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Fakturierte Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Logistik Artikeltrackingzeilen** Seite|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Schritt 3: Empfangen Sie zwei Teile, und fakturieren Sie zwei Teile.  

||**Menge (Basis)**|**Bewegungsmge.**|**Zu fakturieren Menge (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Fakturierte Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Logistik Artikeltrackingzeilen** Seite|7|**2**|**2**|4|0|  
|**T337**|1|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Schritt 4: Empfangen Sie ein Stück.  

||**Menge (Basis)**|**Bewegungsmge.**|**Zu fakturieren Menge (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Fakturierte Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Logistik Artikeltrackingzeilen** Seite|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Fakturieren von 5 Stück.  

||**Menge (Basis)**|**Bewegungsmge.**|**Zu fakturieren Menge (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Fakturierte Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**Logistik Artikeltrackingzeilen** Seite|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also" />Siehe auch
 [Designdetails: Artikeltracking](design-details-item-tracking.md)   
 [Designdetails – Artikeltrackingzeilenfenster-Seite](design-details-item-tracking-lines-window.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
