---
title: Informationen zur Berechnung von festen Einstandspreisen
description: Ein Standard-Kostensystem bestimmt die Kosten der Einheit des Bestandes auf der Grundlage angemessener historischer oder erwarteter Kosten.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.author: edupont
---
# <a name="about-calculating-standard-cost" />Informationen zur Berechnung von festen Einstandspreisen

Viele Produktionsbetriebe verwenden feste Einstandspreise als Bewertungsbasis. Dies gilt auch für Unternehmen, die Leichtproduktion ausführen, wie Montage und Kitting. Ein Einstandspreissystem bestimmt die Kosten einer Lagerbestandseinheit anhand fundierter früherer oder erwarteter Kosten. Untersuchungen der früheren oder der erwarteten zukünftigen Kosten können dann die Basis für feste Einstandspreise bereitstellen. Es ist kaum zu vermeiden, dass sich die Ist-Produktionskosten eines Produkts von den erwarteten festen Einstandspreisen unterscheiden. Die Ist-Produktionskosten eines Produkts können von den erwarteten festen Einstandspreisen abweichen. Damit das Management steuernd eingreifen kann, werden die Ist-Kosten eines bestimmten Artikels mit dessen festem Einstandspreis verglichen. Dabei entdeckte Unterschiede oder *Abweichungen* werden gekennzeichnet und analysiert.  

Feste Einstandspreise können für Artikel verwaltet werden, die durch Einkauf, Montage und Produktion beschafft werden. Für jede Beschaffungsmethode können feste Einstandspreise aus den folgenden Elementen bestehen.  

|Beschaffungsmethode|Standardkostenelemente|  
|--------------------------|----------------------------|  
|**Einkauf**|Direkte Materialkosten und indirekte Materialkosten, falls erforderlich.|  
|**Montage**|Direkte Materialkosten, direkte oder feste Arbeitskosten und Gemeinkosten.|  
|**Fertigungsauftrag**|Direkte Materialkosten, Arbeitskosten, Subunternehmerkosten und Gemeinkosten.|  

## <a name="setting-up-standard-costs" />Festlegen von Standardkalkulationen

Da der Einstandspreis eines produzierten oder montierten Artikels aus mehreren Kostenelementen - Material-, Kapzitäts- und Fremdarbeitskosten (EK-Preise und Gemeinkosten) - besteht, muss der Einstandspreis für jedes dieser Elemente festgelegt werden.  

Die Kalkulationsaufgabe für einen Artikelproduktionsbetrieb, in dem Einstandspreise verwendet werden, besteht aus:  

- Kalkulieren Sie einen Einstandspreis für einen fertigen Artikel und richten sie ihn auf der Artikelkarte ein.  
- Erfassen und Zuordnen der Ist-Kosten der Produktionskostenelemente und genaues Feststellen von Abweichungen.  

Zum Bestimmen der direkten Kosten eines fertigen Artikels müssen alle Komponentenkosten summiert werden. Ein montierter oder hergestellter Artikel kann Unterbaugruppen umfassen, die auch aus mehreren Komponenten bestehen.  

Die folgenden wesentlichen Kostenelemente bilden die direkten Kosten eines fertig bearbeiteten Artikels:  

- Materialkosten.  
- Kapazitätskosten.  
- Fremdarbeitskosten nur für gefertigte Artikel.  

### <a name="material-costs" />Stoffkosten

Materialkosten sind Kosten, die Halbfabrikaten und gekauftem Rohmaterial zugeordnet sind. Materialeinstandspreise können aus direkten und indirekten Kostenelementen bestehen.  

- Direkte Materialkosten entsprechen dem in Rechnung gestellten Betrag für gekauftes Rohmaterial oder den Produktionskosten bei Halbfabrikaten.  
- Indirekte Materialkosten (oder *Gemeinkosten*) entsprechen beispielsweise den Logistikkosten für den produzierten fertigen Artikel.  

Das Konfigurieren der Materialkosten für Einkaufsartikel hinsichtlich der direkten und der indirekten Kosten hängt von der Lagerabgangsmethode ab, die für den fraglichen Artikel ausgewählt ist. Die Kosteninformationen für jede Lagerabgangsmethode auf der Artikelkarte. Weitere Informationen finden Sie unter [Neue Artikel registrieren](inventory-how-register-new-items.md).

Ausschusskosten (nur Fertigung) sind ein zusätzlicher Faktor, der bei der Berechnung der Gesamtmaterialkosten zu berücksichtigen ist. Wenn bei der Montage oder Herstellung eines Artikels eine bestimmte Menge Rohmaterial als Ausschuss anfällt, hat dies zur Folge, dass mehr Komponenten benötigt werden, um den Artikel zu produzieren. Dadurch erhöhen sich auch dadurch die Materialkosten für die Komponenten, die beim Produzieren eines übergeordneten Artikels verbraucht werden. Ausschusskosten für Materialien können entweder auf der Fertigungsstückliste oder auf dem Arbeitsplan eingerichtet werden.  

Die Materialkosten eines Produktionsartikels können auf zwei Arten dargestellt werden, die den folgenden Berechnungsgrundlagen für feste Einstandspreise entsprechen.  

|Kostenberechnungsgrundlage|Materialkostenberechnung|  
|----------------------------|-------------------------------|  
|Einstufig|Der gefertigte Artikel entspricht den Gesamtkosten aller gekauften oder als Unterbaugruppen verbauten Artikel in der Fertigungsstückliste dieses Artikels.|  
|Mehrstufige Ebene oder mehrstufig|"Gefertigter Artikel" ist die Summe der Materialkosten aller Halbfabrikate in der Stückliste dieses Artikels und der Kosten aller Einkaufsartikel in der Fertigungsstückliste dieses Artikels.|  

### <a name="capacity-costs" />Kalkulation von Kapazitäten

Kapazitätskosten entsprechen den internen Bearbeitungs- und den Maschinenkosten. Sie müssen diese Kosten für jede Ressource (in der Montageverwaltung) und jeden Arbeitsplatz bzw. jede Arbeitsplatzgruppe im Arbeitsgang (in der Fertigung) einrichten. Wie bei den Materialien können Sie sowohl direkte als auch indirekte Elemente für die Kapazitätskosten angeben. Beispielsweise können die direkten Kosten für eine Arbeitsplatzgruppe gleich dem "Werkstattsatz" sein, der für das Ausführen einer bestimmten Funktion anfällt. Die indirekten Kosten für eine Arbeitsplatzgruppe entsprechen üblicherweise allgemeinen Unternehmensausgaben wie Beleuchtung, Heizung usw. Analog zu Materialkosten können Kapazitätsgemeinkosten als Prozentsatz indirekter Kosten und/oder als feststehender Gemeinkostenbetrag ausgedrückt werden.  

Die Einrichtung der Kapazitätskosten für montierte Artikel besteht aus den folgenden Elementen:  

- Direkter und indirekter Einstandspreis der Ressource.  
- Feste oder direkte Ressourcenverbrauchsart.  

Die Einrichtung der Kapazitätskosten für produzierte Artikel besteht aus den folgenden Elementen:  

- Direkter und indirekter Einstandspreis des Arbeitsplatzes bzw. der Arbeitsplatzgruppe.  
- Zeit und Losgrösse einrichten.  

Zum Berechnen der Standardkapazitätskosten müssen Sie die Standardzeitlöhne festlegen, die zum Ausführen von Arbeitsgängen an Arbeitsplätzen oder Arbeitsplatzgruppen erforderlich sind. Die Gesamtzeit, die für einen Arbeitsgang erforderlich ist, besteht üblicherweise aus der Rüst- und der Bearbeitungszeit sowie der Warte- und der Transportzeit.  

Sie können die Sätze für diese Zeitarten für jeden Arbeitsplatz bzw. jede Arbeitsplatzgruppe in einem eigenen Arbeitsplan einrichten.  

> [!NOTE]  
>  Während Bearbeitungszeitsätze pro produziertem Artikel gelten, gelten Rüstzeitsätze pro Los. Daher muss die Arbeitsplanrüstzeit für jeden Arbeitsgang entsprechend der Losgrösse umgelegt werden. Die Losgrösse wird im entsprechenden Feld im Inforegister **Beschaffung** der Seite **Artikelkarte** angegeben.  

Um Rüstzeiten im Arbeitsgang für die Planung anzugeben, jedoch nicht bei der Einstandspreisberechnung zu berücksichtigen, leeren Sie das Feld **Kosten inkl. Rüsten**  auf der Seite **Produktion Einrichtung**.  

Auf einer einstufigen Grundlage sind dies die Bearbeitungskosten, die erforderlich sind, um den fertigen Produktionsartikel herzustellen, und die im Arbeitsplan des Produktionsartikels angegeben werden. Auf einer mehrstufigen Grundlage, sind dies die Kapazitätskosten, die für jeden einzeln gefertigten Artikel, der in der Stückliste des übergeordneten Artikels enthalten ist, angegeben werden.  

### <a name="subcontractor-costs" />Kosten für Subunternehmer

Fremdarbeitskosten sind die Kosten, die Serviceleistungen zugeordnet sind, die von externen Kreditoren oder von Subunternehmern bereitgestellt werden. Ähnlich wie Material- und Kapazitätskosten können Fremdarbeitskosten sowohl aus direkten Kosten (Einstandspreise) als auch aus Gemeinkosten bestehen. Direkte Subunternehmerkosten entsprechen den tatsächlichen Kosten, pro bereitgestellter Serviceeinheit anfallen. Subunternehmergemeinkosten können z. B. den Fracht- und/oder Transportkosten entsprechen, die das Unternehmen im Zusammenhang mit einem Auftrag übernimmt, der einem Subunternehmer erteilt wurde.  

Da Fremdarbeit im Wesentlichen eine ausgelagerte Kapazität ist, werden die Kosten der Fremdarbeitsservices (sowohl direkte als auch indirekte Kosten) auf der Subunternehmer-Arbeitsplatzkarte eingerichtet.  

## <a name="updating-standard-costs" />Aktualisieren von Standardkalkulationen

Um den festen Einstandspreis von Montageartikeln zu aktualisieren oder zu berechnen, verwenden Sie die Funktion auf der Artikelkarte.  

Die Aktualisierung oder Berechnung von festen Einstandspreisen umfasst üblicherweise die folgenden Aufgaben:  

1.  Aktualisieren der Kosten auf der Komponenten- und der Kapazitätsebene. Weitere Informationen finden Sie unter Stapelverarbeitungen **Artikel Einst.-Preis vorschlagen** und **Einstandspreis für Kapazität vorschlagen**.  
2.  Konsolidieren und mehrstufiges Berechnen der Komponenten- und Kapazitätskosten, um die Gesamtproduktionskosten der Artikel zu berechnen. Weitere Informationen finden Sie unter Weitere Informationen finden Sie unter [So berechnen Sie die Standardkosten für ein Montage-Element](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Implementieren der festen Einstandspreise, die bei der Ausführung der vorherigen Batchaufträge eingegeben werden. Die festen Einstandspreise treten erst in Kraft, wenn Sie implementiert werden. Verwenden Sie den Stapelverarbeitungsauftrag **Einst.-Preis (fest) Vorschlag übernehmen**, der die Änderungen der Standardkosten für Artikel mit denen aus der Tabelle „Einst.-Preis (fest) Arbeitsblatt“ aktualisiert.  
4.  Implementieren der Änderungen, um das Feld **Einstandspreis** auf der Artikelkarte zu aktualisieren und eine Lagerneubewertung durchzuführen. Weitere Informationen finden Sie unter [Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md).

## <a name="see-also" />Siehe auch

[Designdetails: Kostenberechnungsmethoden](design-details-costing-methods.md)  
[Standardkosten aktualisieren](finance-how-to-update-standard-costs.md)  
[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)  
[Arbeiten mit Stücklisten für die Montage](assembly-how-work-assembly-boms.md)  
[Fertigungsauftrag erstellen](production-how-to-create-production-boms.md)  
[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
