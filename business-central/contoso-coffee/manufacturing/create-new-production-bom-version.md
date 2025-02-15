---
title: Eine neue Produktionsstücklisten- und Stücklistenversion erstellen
description: 'Exemplarische Vorgehensweise, um zu erfahren, wie Sie der Produktlinie von Contoso Coffee in Business Central eine weitere Kaffeemaschine hinzufügen.'
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---
# <a name="walkthrough-create-a-new-production-bom-and-bom-version" />Exemplarische Vorgehensweise: Eine neue Produktionsstücklisten- und Stücklistenversion erstellen

In diesem Artikel führen wir Sie durch die Schritte zur Verwendung der Demodaten von Contoso Coffee für die Arbeit mit Stücklisten (BOM) in Produktionsprozessen.  

## <a name="scenario" />Szenario

Contoso Coffee hat beschlossen, seiner Produktlinie eine weitere Kaffeemaschine hinzuzufügen: **SP-SCM1008 Airpot Lite**. Diese Kaffeemaschine ist baugleich mit dem vorhandenen Artikel **SP-SCM1009 Airpot**, ausser dass die Warmhalteplatte **SP-BOM1104** nicht enthalten ist. In einem separaten Schritt wird das Ein/Aus-Licht **SP-BOM1106** für eine Version des Airpot Lite BOM entfernt.

Oscar, Verfahrenstechniker bei Contoso Coffee, muss eine neue Produktionsstückliste erstellen, um die anfänglichen Komponentenanforderungen für den Airpot Lite zu definieren. Oscar muss dann eine neue BOM-Version mit einem Startdatum am 1. Juli einrichten, um sie mit weiteren Plänen zur Veröffentlichung einer weiteren Edition in Einklang zu bringen.

## <a name="steps" />Schritte

1. Erstellen Sie eine neue Produktionsstückliste für den Airpot Lite.

    1. Wählen Sie das Symbol ![Glühbirne, die die Funktion „Wie möchten Sie weiter verfahren“ öffnet.](../../media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Produktionsstückliste** ein und wählen Sie dann den zugehörigen Link.  

    2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld  |Wert  |
        |---------|---------|
        |**Nr.** |SP-SCM1008|
        |**Description** |Airpot Lite|
        |**Einheitencode**|STÜCK  |

2. Kopieren Sie die Stücklistenkomponenten aus der Produktionsstückliste **SP-SCM1009**.

    1. Wählen Sie im Fenster **Kopiere Stückliste**.

    2. Wählen Sie auf der Seite **Produktionsstücklisten** die Zeile für **SP-SCM1009, Airpot**, und klicken Sie dann auf die Schaltfläche **OK**.

3. Ändern Sie die Komponenten für die neue Fertigungsstückliste wie im Szenario beschrieben.

    1. Wählen Sie auf dem Inforegister **Positionen** die Zeile für die Position **SP-BOM1104** aus, und wählen Sie dann die Aktion **Position löschen**.  

4. Überprüfen Sie die neue Fertigungsstückliste.  

    1. Wählen Sie im Feld **Status** *Zertifiziert* aus.  

5. Erstellen Sie eine Produktionsstücklistenversion für den Airpot Lite.

    1. Wählen Sie die Aktion **Versionen** aus.

    2. Wählen Sie auf der Seite **Fert.-Stückl.-Versionsliste** die Aktion **Neu**, und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld  |Wert  |
        |---------|---------|
        |**Versionscode** |02|
        |**Description** |Airpot Lite, v2|
        |**Einheitencode**|STÜCK  |  
        |**Startdatum**|Juli 01  |  

6. Kopieren Sie die Komponentenzeilen aus der Produktionsstückliste in die neue Stücklistenversion.

    1. Wählen Sie die **Stückliste kopieren**-Aktion, und wählen Sie dann die **Ja**-Schaltfläche zum Kopieren der Komponenten aus der ursprünglichen Produktionsstückliste.

7. Entfernen Sie das Element **SP-BOM1106, Ein/Aus-Licht** aus den Versionskomponenten.

8. Überprüfen Sie die neue Stücklistenversion.

    1. Wählen Sie im Feld **Status** *Zertifiziert* aus.  

    2. Schliessen Sie die Stücklistenversion

Die neue Kaffeemaschine ist nun als Produktionsstückliste mit einer Version angelegt.  

## <a name="see-also" />Siehe auch

[Einführung in Contoso Coffee Demo Data](../contoso-coffee-intro.md)  
