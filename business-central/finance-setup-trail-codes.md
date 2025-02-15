---
title: Codes für Audit-Trails festlegen
description: 'Erfahren Sie mehr über die Aufgaben zum Einrichten von Buchungsspurcodes und Ursachencodes, mit denen Sie Audit-Trails verfolgen können.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accounting, auditing, bookkeeping'
ms.search.form: '257, 259, 279'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="setting-up-source-codes-and-reason-codes-for-audit-trails" />Buchungsspurcodes und Ursachencodes für Audit Trails einrichten

Allen gebuchten Posten wird automatisch ein Buchungsspurcode zugewiesen, sodass Transaktionen bis zu ihrem Ursprung nachverfolgt werden können. Wenn Sie Posten einen zusätzlichen Buchungsspurcode zuordnen möchten, können Sie Ursachencodes verwenden. Ursachencodes werden verwendet, um den Grund für eine Buchung anzugeben. Ursachencodes können gesamten Erf.-Journalvorlagen und Erf.-Journalnamen oder auch einzelnen Erfassungsjournalzeilen und Belegen zugeordnet werden.  

Verwenden Sie als Buchungsspurcodes und Ursachencodes aussagekräftige Codes, an die Sie sich leicht erinnern können. Der Code muss eindeutig sein, und Sie können beliebig viele Codes einrichten.

## <a name="define-source-codes" />Buchungsspurcodes definieren

Gelegentlich möchten Sie nachvollziehen, wie ein bestimmter Posten entstanden ist, ob er z. B. beim Buchen eines Erf.-Journales oder einer Einkaufsrechnung erzeugt wurde. Ein Buchungsspurcode gibt an, wo ein Posten erstellt wurde. Posten werden erstellt, wenn Erfassungsjournale und Rechnungen gebucht und bestimmte Stapelverarbeitungen ausgeführt werden. Jede Buchungsart hat einen bestimmten Buchungsspurcode, der zugewiesen wird, wenn Posten erstellt werden.  

Beim Buchen von Erfassungsjournalen, Aufträgen, Rechnungen oder Gutschriften sowie beim Ausführen bestimmter Stapelverarbeitungen werden Posten in den Finanzaufstellungen erstellt. Die Seite **Buchungsspurcode Einrichtung** enthält für jede Anwendungsregion mehrere Inforegister. Jedes Inforegister enthält die Buchungsspurcodes, die für diese Anwendungsregion anwendbar sind.

Beim Buchen oder Ausführen einer Stapelverarbeitung wird dem Posten automatisch der richtige Buchungsspurcode zugeordnet. Wenn Sie z. B. von einem Fibu Erf.-Journal aus buchen, erhält der Posten den Code *FIBUBUCHBL*. Sie können dann die Seite **Fibuposten** filtern, um anzuzeigen, welche Einträge beispielsweise aus dem Fibu Erf.-Journal oder aus Verkaufsbelegen gebucht wurden.

### <a name="to-define-source-codes" />So definieren Sie Buchungsspurcodes

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Symbol 'Nach Seite oder Bericht suchen'") Symbol. Geben Sie **Buchungsspurcode Einrichtung** ein, und wählen Sie dann den entsprechenden Link.  

2. Geben Sie im Fenster **Buchungsspurcode Einrichtung** für jede Buchungsart und jede Stapelverarbeitung den entsprechenden Buchungsspurcode ein.  

Sie können den Inhalt eines Felds später ändern. Diese Änderung wirkt sich dann auf zukünftige Buchungen aus.

## <a name="change-source-codes" />Buchungsspurcodes ändern

Sie können einen Buchungsspurcode ändern. Sie können den Buchungsspurcode *FIBUBUCHBL* beispielsweise in *FIBUBL* ändern.

### <a name="to-change-source-codes" />So ändern Sie Buchungsspurcodes

1. Wählen Sie die ![Suche nach Seite oder Bericht.](media/ui-search/search_small.png "Symbol 'Nach Seite oder Bericht suchen'") Symbol. Geben Sie **Buchungsspurcodes** ein und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Zeile mit dem zu ändernden den Code im Feld **Code** aus.

3. Geben Sie den neuen Code ein, und klicken Sie dann auf die Schaltfläche **Ja**. Sie können auch den Inhalt des Feldes **Beschreibung** ändern.

Alle neuen Posten, die über das Fibu Erf.-Journal gebucht werden, weisen den neuen Buchungsspurcode auf.

## <a name="define-reason-codes" />Ursachencodes definieren

Ursachencodes ergänzen die Buchungsspurcodes und geben an, warum ein Eintrag erstellt wurde. Sie können Ursachencodes für einzelne Posten und permanente Codes bestimmten Erf.-Journalvorlagen und Erf.-Journalnamen zuweisen. Wenn ein Ursachencodes mit einer Erf.-Journalzeile bzw. einem Einkaufs- oder Verkaufskopf verknüpft ist, werden beim Buchen alle Posten mit dem entsprechenden Ursachencode markiert.  

### <a name="to-set-up-reason-codes" />So richten Sie Ursachencodes ein

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Symbol 'Nach Seite oder Bericht suchen'")  Symbol. Geben Sie **Ursachencodes** ein und wählen Sie dann den zugehörigen Link.

2. Geben Sie im Fenster **Ursachencodes** den ersten Code im Feld **Code** ein. Geben Sie im Feld **Beschreibung** einen erklärenden Text ein.

Wiederholen Sie den Ablauf für jeden Code, den Sie verwenden möchten. Sie können eine beliebige Anzahl von Codes einrichten.

Nachfolgend wird beschrieben, wie Sie einer Erf.-Journalvorlage einen Ursachencodes hinzufügen. Ähnliche Schritte gelten jedoch für das Hinzufügen eines Ursachencodes zu einer Erf.-Journalzeile oder einer Stapelverarbeitung.  

### <a name="to-assign-reason-codes-to-journal-templates" />So weisen Sie Erf.-Journalvorlagen Ursachencodes zu

1. Wählen Sie das ![Suchen Sie nach Seite oder Bericht.](media/ui-search/search_small.png "Suche nach Seiten- oder Berichtssymbolen")  Symbol. Geben Sie **Allgemeine Fibu Erf.-Journalvorlagen** ein, und wählen Sie dann den zugehörigen Link.

2. Geben Sie in der Zeile mit der ausgewählten Erf.-Journalvorlage den entsprechenden Code in das Feld **Ursachencode** ein.

3. Schliessen Sie die Erf.-Journalvorlage.

Der ausgewählte Ursachencode wird in neue Erf.-Journale eingefügt, die unter dieser Erf.-Journalvorlage erstellt werden. In anderen Anwendungsbereichen weisen Sie auf dieselbe Art und Weise Erf.-Journalvorlagen Ursachencodes zu.

### <a name="to-use-reason-codes-on-sales-and-purchase-documents" />So verwenden Sie Ursachencodes in Verkaufs- und Einkaufsbelegen

1. Öffnen Sie den gewünschten Verkaufs- oder Einkaufsbeleg.

2. Geben Sie im Einkaufskopf im Feld **Ursachencode** den Code ein.

Wenn die Rechnung gebucht wird, wird der Ursachencode in jeden Sach-, Debitor- und Kreditorposten kopiert. Sie können einzelnen Einkaufs- oder Verkaufszeilen nicht unterschiedliche Ursachencodes zuordnen, da alle Zeilen als ein Posten gebucht werden.

## <a name="see-related-microsoft-trainingtrainingpathsset-up-financial-management-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/paths/set-up-financial-management-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Finanzen](finance.md)  
[Abstimmen von Bankkonten](bank-manage-bank-accounts.md)  
[Arbeiten mit Dimensionen](finance-dimensions.md)  
[Geschäftsdaten aus anderen Finanzsystemen importieren](across-import-data-configuration-packages.md)  
[Analysieren von Cashflow in Ihren Mandanten](finance-analyze-cash-flow.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
