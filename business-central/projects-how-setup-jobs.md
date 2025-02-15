---
title: 'Jobs, Preise und Buchungsgruppen festlegen'
description: 'Beschreibt, wie allgemeine Informationen zu Projekten eingerichtet werden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 04/25/2023
ms.custom: bap-template
ms.search.keywords: project management
ms.search.form: '211, 463, 1012'
---
# <a name="set-up-jobs-prices-and-job-posting-groups" />Jobs, Preise und Buchungsgruppen festlegen

Als Projekt-Manager können Sie Projekte einrichten, die jedes der Projekte definieren, das Sie in [!INCLUDE[prod_short](includes/prod_short.md)] verwalten. Verwenden Sie die Seite **Projekt Einrichtung**, um festzulegen, wie Sie Projektfeatures verwenden.

Geben Sie für jedes Projekt verschiedene Informationen an:

* Preise für Projektartikel
* Projektressourcen
* Projektfibukonten
* Projektbuchungsgruppen (falls erforderlich)

## <a name="to-set-general-information-for-jobs" />Um allgemeine Informationen für Projekte einzurichten:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Projekt Einrichtung** ein und wählen Sie den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Der Umschalter **Verbrauchslink standardmässig anwenden** auf der Seite **Projekt Einrichtung** zeigt an, ob Projektsachkontoeinträge standardmässig mit Projektplanungszeilen verknüpft werden. Aktivieren Sie den Umschalter, um diese Einstellung auf alle neuen Projekte anzuwenden. Sie können das Tracking des Projektverbrauchs für ein bestimmtes Projekt aktivieren oder deaktivieren, indem Sie den Umschalter **Verbrauchslink anwenden** auf der Seite **Projektkarte** ein- oder ausschalten.

### <a name="to-set-up-job-usage-tracking" />Projektverbrauch-Tracking einrichten

Wenn Sie an einem Projekt arbeiten, möchten Sie vielleicht wissen, wie sich Ihr Verbrauch im Vergleich zu Ihrem Plan verhält. Um den Verbrauch herauszufinden, können Sie einen Link zwischen Ihren Projektplanungszeilen und dem tatsächlichen Verbrauch erstellen. Über den Link können Sie Ihre Kosten verfolgen und nachvollziehen, wie viel Arbeit noch übrig ist. Standardmässig ist de Projektplanungszeilentyp **Plan**, aber die Verwendung der Zeilenart **Plan und fakturierbar** hat ähnliche Effekte.

Nachdem Sie das Verbrauchstracking über den Umschalter **Verbrauchsverknüpfung standardmässig anwenden** aktiviert haben, können Sie die Informationen der Projektplanungszeile überprüfen. Beispielsweise können Sie die Menge der Ressource, des Artikels oder des Fibukontos festlegen. Sie können auch die Menge festlegen, die Sie an das Projekt Erf.-Journal übertragen möchten. Das Feld **Restmenge** auf der Projektplanungszeile zeigt Ihnen an, was noch übertragen und im Projekt Erf.-Journal gebucht werden muss.

>[!NOTE]
> Wenn die **Verbrauchsverknüpfung anwenden** auf dem einzelnen Projekt gewählt wird und das Feld **Zeilentyp** auf der Projekt Erf.-Journal oder Einkaufszeile **Fakturierbar** ist, dann werden neue Projektplanungszeilen des Zeilentyps **Sowohl Budget als auch fakturierbar** erstellt, wenn Sie das Projekt Erf.-Journal oder den Einkaufsbeleg buchen.  
>
> Weitere Informationen finden Sie unter [Datensätze für Aufträge](projects-how-record-job-usage.md) und [Auftragsvorräte verwalten](projects-how-manage-project-supplies.md)

> [!IMPORTANT]
> Wenn Sie im Feld **Zeilentyp** auf der Zeile für die Projekt Erfassungsjournalzeile oder den Kauf keinen Wert angeben, werden keine Projektplanungszeilen erstellt, wenn Sie das Projekt Erf.-Journal oder den Einkaufsbeleg buchen.

## <a name="to-set-up-prices-for-resources-items-and-general-ledger-accounts-for-jobs" />Erstellen von Preisen für Ressourcen, Artikel und Fibukonten für Projekte

> [!NOTE]
> In der 2020er Release-Welle 2 haben wir neue Prozesse zum Einrichten und Verwalten von Preisen und Rabatten freigegeben. Wenn Sie ein neuer Kunde sind, nutzen Sie die neue Erfahrung. Wenn Sie bereits Kunde sind, hängt es davon ab, ob Sie die neue Erfahrung verwenden, ob Ihr Administrator die Funktionsaktualisierung **Neues Verkaufspreiserlebnis** in **Funktionsverwaltung** akualisiert hat. Weitere Informationen finden Sie unter [Bevorstehende Funktionen im Voraus aktivieren](/dynamics365/business-central/dev-itpro/administration/feature-management).

Sie können Preise für die Artikel, Ressourcen und Fibukonten für Projekte einrichten. 

#### [Aktuelle Erfahrung](#tab/current-experience)

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das entsprechende Projekt und dann die Aktion **Ressource**, **Artikel** oder **Fibukonto** aus.
3. Füllen Sie auf den Seiten **Res.-VK-Preise Projekt**, **Projektartikelpreise**, oder **Projekt-Fibukontopreise** die Felder nach Bedarf aus.

Wenn Sie ein Ressourcen-, Artikel- oder Fibukonto für ein Projekt auswählen, verwendet [!INCLUDE [prod_short](includes/prod_short.md)] Informationen in den optionalen Feldern in Projektplanungszeilen und Projekt Erf.-Journal. Die folgende Tabelle erläutert, wie.

|Spalte1  |Spalte2  |
|---------|---------|
|**Projektressourcen**|Die Felder **Projektaufgabennr.**, **Arbeitstyp**, **Währungscode**, **Zeilenrabatt %** und **Einstandspreis**. Der Wert im Feld **Einzelpreis** für die Ressource wird in den Projektplanungszeilen und Projekt Erfassungsjournale verwendet, wenn Sie eine Ressource oder eine der Ressourcengruppe zugeordnete Ressource eingeben. Dieser Preis überschreibt immer die auf der Seite **Ressourcen-VK-Preis/Ressourcengruppen-VK-Preise** angegebenen Preise.|
|**Projektartikel**|Die Felder **Projektaufgabennr.**, **Währungscode** und **Zeilenrabatt %**. Dies ist der Wert im Feld **Einheitspreis** der in den Projektplanungszeilen und Projektbuchungsblättern verwendet wird, wenn dieser Artikel eingegeben wird. Dieser Preis hat Vorrang vor dem regulären Debitorenpreis (Mechanismus für „bester Preis“) für Artikel. Um den regulären Debitorenpreis zu verwenden, geben Sie keine Projektartikelpreise für den Projekt an.|
|**Fibukonten**|Die Informationen in den Feldern **Projektaufgabennr.**, **Währungscode**, **Zeilenrabatt %**, **Einheitskostenfaktor** und **Einheitskosten** werden auf den Projektplanungszeilen und Projekt-Erfassungsjournalen verwendet, wenn dieses Fibukonto eingegeben und einem Projekt hinzugefügt wird. Wenn Sie ein Fibukonto auswählen, verwenden Projektplanungszeilen und Projekt Erfassungsjournale den Wert im Feld **Einzelpreis** für das Aufwandssachkonto.|

#### [Neue Erfahrung](#tab/new-experience)

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Markieren Sie den entsprechenden Job und wählen Sie dann die Aktion **Verkaufspreislisten**.

---

## <a name="to-set-up-job-posting-groups" />Projektbuchungsgruppen einrichten

Ein Aspekt der Projektenplanung besteht darin, zu entscheiden, welche Buchungskonten für die Projektkalkulation verwendet werden. Damit Projekte gebucht werden können, müssen Sie Konten für die Buchung für jede Projektbuchungsgruppe einrichten. Eine Buchungsgruppe stellt eine Verknüpfung zwischen dem Projekt und der Art dar, wie es im Fibuposten zu behandeln ist. Wenn Sie ein Projekt erstellen, geben Sie eine Buchungsgruppe an, und standardmässig wird jede Aufgabe, die Sie erstellen, dieser Buchungsgruppe zugeordnet. Wenn Sie Aufgaben erstellen, können Sie jedoch die Voreinstellung überschreiben und eine Buchungsgruppe auswählen, die geeigneter ist.  

> [!NOTE]  
> Sie müssen die Konten in den Kontenplan eingegeben, bevor Sie Buchungsgruppen einrichten können. Weitere Informationen finden Sie unter [Einrichten oder ändern des Kontenplans](finance-setup-chart-accounts.md).  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Projektbuchungsgruppen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

| Das Feld "Konto" | Description |
| --- | --- |
| **Code** |Eine Kennung für die Buchungsgruppe. Sie können bis zu 10 Zeichen, einschliesslich Leerzeichen, eingeben. |
| **Konto f. Kosten n. abgs. Arb.** |Das WIP-Konto für die berechneten Kosten der Projekt-WIP, bei dem es sich um ein Bilanz-Aktivkonto für Kapital handelt. |
| **Konto f. aufgel. Kosten n. abgs. Arb.** |Ein Konto für die Einstandswert- oder Vertriebskostenmethode der WIP-Berechnung. Dieses Konto ist für die aufgelaufene Kosten in Ihrer Bilanz. Wenn die WIP-Regulierung erfordert, dass Sie die Verbrauchsosten, die Sie in Ihrer Erfolgsrechnung buchen, erhöhen, buchen Sie dies auf dieses Konto. |
| **Projektkostenausgleich-Konto** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Konto für ausgeglichene Artikelpreise** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Konto für ausgeglichene Ressourcenpreise** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Kostenausgleich-Konto** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Projektkostenregulierung-Konto** |Das Gegenkonto zum WIP-Konto für aufgelaufene Kosten, bei dem es sich um ein Aufwandskonto handelt. |
| **Aufwandssachkonto (Budget)** |Das Verkaufskonto, das für Aufwandsfibuposten in Projektaufgaben mit dieser Buchungsgruppe verwendet werden soll. Wenn dieses Feld leer gelassen wird, wird das für die Projektplanungszeile eingegebene Fibukonto verwendet. |
| **Konto f. aufgel. Verkäufe n. abgs. Arb.** |Das WIP-Konto für den berechneten Verkaufswert der WIP, bei dem es sich um ein Konto für aufgelaufene Umsätze für Ihre Bilanz handelt. Wenn eine WIP-Regulierung erfordert, dass Sie die anerkannten Umsätze erhöhen, buchen Sie dies auf dieses Konto. |
| **Konto f. fakt. Verkäufe n. abgs. Arb.** |Das Konto für den fakturierten WIP-Verkaufswert, der nicht deklariert werden kann. Es handelt sich dabei um ein Bilanzblatt für nicht realisierte Einnahmen. |
| **Projektverkaufsausgleich-Konto** |Das Gegenkonto zum WIP-Konto für fakturierte Verkäufe, bei dem es sich um ein Ertragsgegenkonto handelt. |
| **Projektverkaufsregulierungs-** Konto |Das Gegenkonto zum WIP-Konto für den Umsatz, bei dem es sich um ein Ertragskonto handelt. |
| **Konto deklarierte Kosten** |Das Aufwandskonto, das die deklarierten Kosten für das Projekt enthält. Dabei handelt es sich normalerweise um ein Soll-Aufwandskonto. |
| **Konto deklarierte Verkäufe** |Das Ertragskonto, das den deklarierten Umsatz für das Projekt enthält. Dabei handelt es sich normalerweise um ein Haben-Ertragskonto. |

## <a name="see-related-microsoft-trainingtrainingpathsset-up-jobs-resources" />Siehe verwandte [Microsoft Schulungen](/training/paths/set-up-jobs-resources/)

## <a name="see-also" />Siehe auch

[Projektmanagement einrichten](projects-setup-projects.md)  
[Video: So erstellen Sie ein Projekt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projekte verwalten](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
