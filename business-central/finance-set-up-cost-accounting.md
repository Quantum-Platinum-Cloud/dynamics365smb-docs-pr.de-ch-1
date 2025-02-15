---
title: Einrichten der Kostenrechnung
description: 'Bevor Sie mit der Kostenrechnung arbeiten, müssen Sie eine Einrichtung vornehmen. Jedem Kosteneintrag muss eine Kostenart und ein Kostenstellencode oder ein Kostenobjekt zugewiesen werden.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1112, 1113, 1122'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="setting-up-cost-accounting" />Einrichten der Kostenrechnung

Bevor Sie die Arbeit mit der Kostenrechnung beginnen können, müssen Sie Einrichtungsaufgaben ausführen.

## <a name="balances-between-cost-type-cost-center-and-cost-object" />Salden zwischen Kostenart, Kostenstelle und Kostenträger

Wenn Sie die Kostenrechnung einrichten, müssen Sie sicherstellen, dass alle Daten einer Kostenart sowie einer Kostenstelle oder einem Kostenträger zugeordnet sind. Das bedeutet, dass jedem Kostenposten eine Kostenart und eine Kostenstelle oder ein Kostenträger zugewiesen sein muss. Diese Regel stellt sicher, dass jeder Kostenposten entweder in Kostenstellen oder in den Kostenträgern erscheint, jedoch nicht an beiden Stellen.  

Auf diese Weise erstellen Sie die folgende Buchhaltungsgleichung:  

*Kostenart-Saldo*  = *Kostenstellen-Saldo*  + *Kostenträger-Saldo*  

Wenn Sie den Kostenartenplan, den Kostenstellenplan und den Kostenträgerplan drucken, können Sie diese Beziehung analysieren.

## <a name="setting-up-cost-types" />Einrichten von Kostenarten

Kostenartenpläne ähneln Kontenplänen im Fibukonto. Sie können den Kostenartenplan auf die folgenden Weisen einrichten:  

- Strukturieren Sie den Kostenartenplan ähnlich wie Erfolgsrechnungskonten im Fibukontenplan. Dann können Sie den Fibukontenplan in den Kostenartenplan übertragen. Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.  
- Erstellen Sie einen neuen Kostenartenplan, oder fügen Sie einem vorhandenen Kostenartenplan neue Kostenarten hinzu. Sie müssen jede neue Kostenart einzeln erstellen.  

### <a name="to-transfer-the-general-ledger-chart-of-accounts-to-the-chart-of-cost-types" />So übertragen Sie den Fibukontenplan in den Kostenartenplan.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Tell me-Funktion"). Symbol. Geben Sie **Kostenartenplan** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Kostenarten aus K&amp;ontenplan abrufen**. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**, um die Übertragung zu bestätigen. Die Funktion verwendet den Kontenplan, um einen Kostenartenplan zu erstellen.  

    Der Kostenartenplan enthält jetzt alle Erfolgsrechnungskonten im Fibukonto und umfasst Überschriften und Zwischensummen. Sie können den Kostenartenplan ändern, falls erforderlich. Beispielsweise können Sie doppelt vorhandene Kostenarten löschen.  

    > [!IMPORTANT]  
    >  Die **Kostenarten in Kontenplan registrieren**-Funktion aktualisiert das Verhältnis zwischen dem Kontenplan und dem Kostenartenplan. Das **Nr.** Das Feld wird ausgefüllt und geprüft, um sicherzustellen, dass jedes Fibukonto mit nur einer Kostenart verknüpft ist. Die Funktion wird automatisch ausgeführt, bevor Sie Fibuposten in die Kostenrechnung übertragen.  

### <a name="to-set-up-new-cost-types-in-the-chart-of-cost-types-page" />So richten Sie auf der Seite "Liquiditätskontenplan" neue Liquiditätskonten ein

1. Öffnen Sie die Seite **Kontenplan-Arten** im Bearbeitungsmodus.  
2. Füllen Sie je nach Bedarf die Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >  Sie können Kostenarten auf der Seite **Kostenartkarte** oder auf der Seite **Kostenartenplan** einrichten und verwalten. So richten Sie auf der Seite **Liquiditätskontenplan** neue Liquiditätskonten ein.

3. Nachdem Sie alle Kostenarten erstellt haben, wählen Sie die Aktion **Kostenarten einrücken** aus. Klicken Sie im Dialogfeld auf die Schaltfläche **Ja**.  
4. Verknüpfen Sie die neue Kostenart mit dem entsprechenden Fibukonto.  

    > [!IMPORTANT]  
    >  Wenn Sie in den Feldern **Zusammenzählung** Definitionen für die Zeilenart **Bis-Summe** eingetragen haben, bevor Sie die Funktion **Kostenarten einrücken** ausgeführt haben, müssen Sie diese Eintragungen wiederholen, da die Funktion die Werte in allen **Bis-Summe**-Feldern überschreibt.  

### <a name="to-update-cost-types" />So aktualisieren Sie Kostenarten

1. Auf der Seite **Kostenrechnung einrichten**  wählen Sie aus, ob der Kostenartenplan automatisch aktualisiert werden soll, wenn der Kontenplan geändert wird.  
2. Die folgenden Optionen stehen im Feld **Fibukonto ausrichten** zur Auswahl.  

- **Keine Ausrichtung** - Es gibt keine entsprechende Änderung im Kostenartenplan, wenn Sie den Kontenplan ändern.  
- **Automatisch** - Es gibt eine entsprechende Änderung im Kostenartenplan, wenn Sie den Kontenplan ändern.  
- **Eingabeaufforderung** - Eine Meldung wird mit der Frage angezeigt, ob Sie die entsprechende Änderung auch im Kostenartenplan vornehmen möchten, wenn Sie den Kontenplan ändern.

## <a name="defining-the-relationship-between-cost-types-and-general-ledger-accounts" />Definieren der Beziehung zwischen Kostenarten und Fibukonten

Das Verbindung zwischen der Kostenart und dem Fibukonto wird in der Kostenart und im Fibukonto erstellt.  

- Das Feld **Fibukontenbereich** in der Tabelle **Kostenart** bestimmt, welche Fibukonten zu einer Kostenart gehören.  
- Das **Kostenartennummer** Feld im Kontenplan bestimmt, zu welcher Kostenart ein Fibukonto gehört.  

Diese beiden Felder werden automatisch ausgefüllt, wenn Sie die **Kostenarten aus Kontenplan abrufen**-Funktion verwenden.  

### <a name="relationship-between-general-ledger-accounts-and-cost-types" />Beziehung zwischen Fibukonten und Kostenarten

Zwischen Fibukonten und Kostenarten besteht eine n:1-Beziehung. Mehrere Fibukonten können zu einer Kostenart gehören, aber jedes Fibukonto gehört nur zu einer Kostenart. In der folgenden Tabelle werden die Details der Beziehung beschrieben.  

|Verbindungen|**Fibukontobereich**|**Kostenartnr.**|  
|------------------|------------------------------------------------|-------------------------------------------|  
|Ein Fibukonto für jede Kostenart|Ein Fibukonto|Eine Kostenart|  
|Mehrere Fibukonten für eine Kostenart|Fibukontobereich, z. B. 7110 ... 7193 für jedes Fibukonto|Für jedes Fibukonto im Bereich gibt es nur eine Kostenart|  
|Kostenarten ohne entsprechende Fibukonten|\<Empty\>||  
|Fibukonten, deren Posten nicht übertragen werden||\<Empty\>|  

### <a name="cost-types-without-a-relationship-to-the-general-ledger" />Kostenarten ohne Beziehung zum Fibukonto

Eine Kostenart hat möglicherweise keine Beziehung zu Fibukonten, wenn eine der folgenden Bedingungen zutrifft:  

- Konten für die betriebliche Buchhaltung, wie Berech. Zinsen und Abschreibungen, entnehmen nur Kosten aus der betrieblichen Buchhaltung.  
- Helfende Kostenarten, wie Kostenarten 9901, 9902 und 9903 in der [!INCLUDE[prod_short](includes/prod_short.md)]-Datenbank, werden als Haben- und Sollbeträge für Zuordnungen verwendet.  
- Das helfende Konto, 9920 in der [!INCLUDE[prod_short](includes/prod_short.md)]-Datenbank, enthält tatsächliche Zugänge, die die Differenz zwischen Kosten und Ausgaben des Fibukontos anzeigen.

## <a name="setting-up-cost-centers" />Einrichten von Kostenstellen

Kostenstellen sind Abteilungen, die für die Kosten und die Einnahmen zuständig sind. Der Kostenstellenplan ähnelt den Dimensionsinformationen für das Sachkonto. Sie können den Kostenstellenplan auf die folgenden Weisen einrichten:  

- Transferieren Sie Dimensionswerte im Sachkonto zum Kostenstellenplan. Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.  
- Erstellen Sie einen neuen Kostenstellenplan, der unabhängig vom Sachkonto ist, oder fügen Sie einem vorhandenen Kostenstellenplan eine neue Kostenstelle hinzu. Sie müssen jede Kostenstelle einzeln erstellen.  

### <a name="to-transfer-dimension-values-in-the-general-ledger-to-the-chart-of-cost-centers" />So transferieren Sie Dimensionswerte im Fibukonto zum Kostenstellenplan

1. Richten Sie eine Dimension als Kostenstellendimension auf der Seite **Kostenstellendimension aktualisieren** ein. Nur die Werte aus dieser Dimension werden übertragen.  
2. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 2.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Kostenstellenplan** ein, und wählen Sie dann den entsprechenden Link.  
3. Klicken Sie auf der Registerkarte **Aktionen** in der Gruppe **Funktion** auf **Kostenstellen aus Dimension abrufen**, um Dimensionswerte zum Kostenstellenplan zu übertragen. Die Funktion überträgt die Dimensionswerte, die Sie in Schritt 1 definiert haben.  

    > [!NOTE]  
    >  Sie können das Feld **Kostenstellendimension ausrichten** so einrichten, dass eine unidirektionale Synchronisierung von Dimensionswerten aus dem Fibukonto zum Kostenstellenplan definiert wird. Sie können keine Synchronisierung des Kostenstellenplans mit Dimensionswerten aus dem Sachkonto definieren.  

Der Kostenstellenplan enthält jetzt alle angegebenen Dimensionswerte aus dem Fibukonto und umfasst Titel und Zwischensummen.  

### <a name="to-create-new-cost-centers-in-the-chart-of-cost-centers-page" />So richten Sie auf der Seite Kostenstellenplan neue Kostenstellen ein

Sie können Kostenkarten auf der Seite **Kostenstellen** oder auf der Seite **Kostenstellenkarte** einrichten und verwalten. So richten Sie auf der Seite **Kostenstellenplan** neue Kostenstellen ein.  

1. Öffnen Sie die Seite **Kontenplan-Kostenstellen** im Bearbeitungsmodus.  
2. Geben Sie im Feld **Code** den Kostenstellencode ein. Alle Kostenstellen müssen einen Code aufweisen.  
3. Geben Sie im Feld **Namen** den Kostenstellennamen ein.  
4. Wählen Sie den Dropdownpfeil im Feld **Positionstyp** aus, um den Zweck der Kostenstelle anzugeben.  

    - Für Kostenstellen der Art **Summe** müssen Sie das Feld **Zusammenzählung** ausfüllen. Verwenden Sie den **Oder**-Operator, der eine vertikale Zeile (**&#124;**) ist, um Bereiche von Kostenstellen festzulegen.  
    - Für Kostenstellen der **Bis-Summe**-Zeilenart wird dieses Feld automatisch ausgefüllt, wenn Sie die Einzugsfunktion verwenden.  
5. Füllen Sie die Felder **Sortierreihenfolge** und **Kostenunterart** aus.  
6. Wählen Sie die nächste leere Zeile aus, um eine neue Kostenstelle zu erstellen. Wiederholen Sie dann die Schritte 2 bis 5.  
7. Nachdem Sie alle Kostenstellen eingerichtet haben, wählen Sie die Aktion **Kostenstellen einrücken** aus. Wählen Sie die Schaltfläche **Ja** aus.  

> [!IMPORTANT]  
> Wenn Sie Definitionen in den **Zusammenzählung**-Feldern für **Bis-Summe**-Kostenstellen eingegeben haben, bevor Sie die Einzugsfunktion ausführen, müssen Sie sie noch einmal eingeben. Die Funktion überschreibt die Werte in allen **Bis-Summe**-Feldern.

## <a name="setting-up-cost-objects" />Einrichten von Kostenträgern

Kostenträger sind Projekte, Produkte oder Services eines Unternehmens. Der Kostenträgerplan ähnelt den Dimensionsinformationen für das Sachkonto. Sie können den Kostenträgerplan auf die folgenden Weisen einrichten:  

* Transferieren Sie Dimensionswerte im Sachkonto zum Kostenträgerplan. Sie können alle notwendigen Änderungen nach der Übertragung vornehmen.  
* Erstellen Sie einen neuen Kostenträgerplan, der unabhängig vom Sachkonto ist, oder fügen Sie einem vorhandenen Kostenträgerplan einen neuen Kostenträger hinzu. Sie müssen jeden Kostenträger einzeln erstellen.  

### <a name="to-transfer-dimension-values-from-the-general-ledger-to-the-chart-of-cost-objects" />So transferieren Sie Dimensionswerte aus dem Fibukonto zum Kostenträgerplan

1.  Legen Sie eine Dimension als Kostenträgerdimension auf der Seite **Kostenträger-Dimensionen aktualisieren** fest. Nur die Werte aus dieser Dimension werden übertragen.  
2.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 3.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Diagramm der Kostenträgerpläne** ein und wählen Sie dann den zugehörigen Link.  
3.  Wählen Sie die Aktion **Kostenträger aus Dimension abrufen**, um Dimensionswerte zum Kostenträgerplan zu übertragen. Die Funktion überträgt die Dimensionswerte, die Sie in Schritt 1 definiert haben.  

    > [!NOTE]  
    >  Sie können das Feld **Kostenträgerdimension ausrichten** so einrichten, dass eine unidirektionale Synchronisierung von Dimensionswerten aus dem Fibukonto zum Kostenträgerplan definiert wird. Sie können keine Synchronisierung des Kostenträgerplans mit Dimensionswerten aus dem Sachkonto definieren.  

Der Kostenträgerplan enthält jetzt alle angegebenen Dimensionswerte aus dem Fibukonto und umfasst Titel und Zwischensummen.  

### <a name="to-create-new-cost-objects-in-the-chart-of-cost-objects-page" />So richten Sie auf der Seite Kostenstellenträger neue Kostenträger ein

Sie können Kostenkarten auf der Seite **Kostenträger** oder im Fenster **Kostenträgerkarte** einrichten und verwalten. So richten Sie auf der Seite **Kostenträger** neue Kostenstellenträger ein.  

1.  Öffnen Sie die Seite **Kontenplan-Objekte** im Bearbeitungsmodus.  
2.  Geben Sie im Feld **Code** den Kostenträgercode ein. Alle Kostenträger müssen einen Code aufweisen.  
3.  Geben Sie im Feld **Namen** den Kostenträgernamen ein.  
4.  Wählen Sie den Dropdownpfeil im Feld **Positionstyp** aus, um den Zweck des Kostenträgers anzugeben.  

    * Für Kostenträger der **Summe**-Zeilenart müssen Sie das Feld **Summe Von/Bis** ausfüllen. Verwenden Sie den **Oder**-Operator, der eine vertikale Zeile (**&#124;**) ist, um Bereiche von Kostenträgern festzulegen.  
    * Für Kostenträger der **Bis-Summe**-Zeilenart wird dieses Feld automatisch ausgefüllt, wenn Sie die Einzugsfunktion verwenden.  
5.  Füllen Sie das Feld **Sortierungsauftrag** aus.  
6.  Wählen Sie die nächste leere Zeile aus, um einen neuen Kostenträger zu erstellen. Wiederholen Sie dann die Schritte 2 bis 5.  
7.  Nachdem Sie alle Kostenträger eingerichtet haben, wählen Sie die Aktion **Kostenträger einrücken** aus. Wählen Sie die Schaltfläche **Ja** aus.  

> [!IMPORTANT]  
>  Wenn Sie Definitionen in den **Summe Von/Bis**-Feldern für **Bis-Summe**-Kostenträger eingegeben haben, bevor Sie die Einzugsfunktion ausführen, müssen Sie sie noch einmal eingeben. Die Funktion überschreibt die Werte in allen **Bis-Summe**-Feldern.

## <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts" />Definieren von Kostenstellen und Kostenträgern für Kontenpläne

Sie können die Ausgaben- und Einnahmenposten aus dem Sachkonto in die Kostenrechnung entweder für jede Sachkontobuchung oder mit einem Batchauftrag übertragen. Wenn Sie die Übertragung ausführen, überträgt [!INCLUDE[prod_short](includes/prod_short.md)] nur die Posten, die bereits mit einer Kostenstelle oder einem Kostenträger verknüpft sind. Um eine sinnvolle Übertragung herzustellen, müssen Sie sicherstellen, dass die Kostenstellen und die Kostenträger korrekt definiert sind.  

### <a name="defining-default-dimension-values-for-general-ledger-accounts" />Definieren von Standarddimensionswerten für Sachkonten

Für jedes Fibukonto können Sie Standarddimensionswerte in der Tabelle **Standarddimensionen** definieren. Das folgende Beispiel zeigt, wie Sie definieren, dass es immer eine Kostenstelle ABTEILUNG, aber nie einen Kostenträger PROJEKT geben soll, wenn Sie auf ein Sachkonto buchen.  

|**Dimensionscode**|**Dimensionswertbuchung**|  
|------------------------------------------|-----------------------------------------|  
|Abteilung|Code notwendig|  
|Kostenträger|Kein Code|  

### <a name="defining-dimension-values-for-overhead-costs-and-direct-costs" />Definieren von Dimensionswerten für Gemeinkosten und direkte Kosten

 Sie können Gemeinkosten an eine Kostenstelle und direkte Kosten an einen Kostenträger übertragen. In der folgenden Tabelle wird die optimale Kombination aus Dimensionseinrichtungswerten angezeigt.  

|Übertragen in|Kostenstellenbuchung|Kostenträgerbuchung|  
|-----------------|-------------------------|-------------------------|  
|Kostenstelle|Code notwendig|Kein Code|  
|Kostenträger|Kein Code|Code notwendig|  

> [!NOTE]  
>  Um sicherzustellen, dass die vordefinierte Kostenstelle und der vordefinierte Kostenträger, die bzw. den Sie im Fibukonto eingerichtet haben, automatisch in die Kostenrechnung übertragen werden, aktivieren Sie das Kontrollkästchen **Fibu-Buchung prüfen** auf der Seite Kostenbuchungseinrichtung.

## <a name="see-related-microsoft-trainingtrainingmodulescost-accounting-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/cost-accounting-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Kostenrechnung](finance-manage-cost-accounting.md)  
[Übertragung und Buchung von Kostenzuteilungen](finance-transfer-and-post-cost-entries.md)  
[Definieren und Zuweisen von Kosten](finance-define-and-allocate-costs.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
