---
title: Verarbeiten von Verkaufschancen in Verkaufsprozessen
description: 'Dieses Thema beschreibt die verschiedenen Möglichkeiten, wie Sie Verkaufschancen in Verkaufszyklen verarbeiten und eine Verkaufschance durch die Phasen eines Verkaufszyklus bewegen können.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect'
ms.date: 06/22/2021
ms.author: jswymer
---
# <a name="process-sales-opportunities" />Verarbeiten von Verkaufschancen
Nachdem Sie eine Verkaufschance erstellen haben, gibt es einige Funktionen für die Verwaltung der Verkaufschance und deren Abschluss.

## <a name="to-view-opportunities" />Anzeigen von Verkaufschancen
Vorhandene Verkaufsverkaufschancen sind auf der Seite **Verkaufschancenliste** verfügbar. Es gibt unterschiedliche Arten, um auf diese Seite für die Verarbeitung von Verkaufschancen zuzugreifen:

| Verkaufschancen anzeigen für | Dann |
| --- | --- |
| Alle Verkäufer und Kontakte |Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Verkaufschancenliste** ein und wählen Sie dann den zugehörigen Link. |
| Ein bestimmter Verkäufer |Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Verkäufer** ein und wählen Sie dann den zugehörigen Link. Wählen Sie den Verkäufer, wählen sie die Aktion **Verkaufschancen** und dann die Aktion **Liste**. |
| Ein bestimmter Kontakt |Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Kontakte** ein, und wählen Sie dann den zugehörigen Link. Wählen Sie den Kontakt aus der Liste, und wählen sie die Aktion **Verkaufschancen**. |

Jede dieser Aufgaben öffnet die Seite **Verkaufschancenliste**.

## <a name="to-close-opportunities" />Um Verkaufschancen abzuschliessen
Sie können Verkaufschancen abschliessen, wenn die Verhandlungen abgeschlossen sind. Wenn Sie eine Verkaufschance schliessen, können Sie angeben, ob sie gewonnen oder verloren wurde und dafür die Gründe festlegen. Um einen Grund anzugeben, müssen Sie Verkaufschancenabschlusscodes einrichten.

1. Auf der Seite **Verkaufschancenliste** wählen Sie die Verkaufschance und die **Abschluss**-Aktion aus. Die Seite **Verkaufschance abschliessen** wird geöffnet.
2. Füllen Sie die relevanten Felder aus, und wählen Sie dann die Schaltfläche **OK** aus.

   Die Felder **Verkaufschancenabschlusscode** und **Abschlussdatum** sind erforderlich und müssen ausgefüllt werden, bevor Sie auf die Schaltfläche **Ok** klicken können.

   Geben Sie im **Verkaufschancenabschlusscode**-Feld einen der vorhandenen Verkaufschancenabschlusscodes aus oder fügen Sie einen neuen Code hinzu. Um einen neuen Code hinzuzufügen, wählen Sie in der Dropdownliste **Aus vollständiger Liste auswählen** aus in wählen Sie dann **Neu**. Füllen Sie in der neuen leeren Zeile die Felder **Code**, **Art** und **Beschreibung** aus, und wählen Sie dann die **OK**-Schaltfläche.

## <a name="to-create-quotes-for-opportunities" />Um Angebote für Verkaufschancen zu erstellen
> [!NOTE]
> Sie können nur Verkaufsofferten aus Verkaufschancen erstellen, bei denen der Kontakttyp Firma ist.

1. Auf der Seite **Verkaufschancenliste** wählen Sie die Verkaufschance und dann die **Verkaufsofferte zuweisen**-Aktion aus. Die Seite **Verkaufsofferte** wird geöffnet.
2. Füllen Sie die entsprechenden Felder aus.

## <a name="to-create-sales-orders-for-opportunities" />Verkaufsaufträge für Verkaufschancen erstellen
Sie können Verkaufsaufträge aus Verkaufsofferten erstellen, die Sie für Ihre Verkaufschancen erfasst haben. Bevor Sie Verkaufsaufträge für Ihre Kontakte erstellen können, müssen Sie den Kontakt als Debitor erstellen. Weitere Informationen finden Sie unter [Kontakte erstellen](marketing-create-contact-companies.md).

1. Suchen Sie auf der Seite **Verkaufschancenliste** die Verkaufschance, für die Sie eine Verkaufsofferte erstellt haben.
2. Wählen Sie die Aktion **Verkaufsangebot zuweisen** aus. Die Seite **Verkaufsofferte** wird geöffnet. Es enthält die Verkaufsofferte, die der Verkaufschance zugewiesen wurde.
3. Füllen Sie die weiteren Felder aus, und wählen Sie dann die Aktion **Auftrag erstellen** aus.

Bei der Bearbeitung von Verkaufschancen können Sie eine Offerte für den Kontakt erstellen, mit dem die Verkaufschance verknüpft ist.

## <a name="to-delete-opportunities" />Um Verkaufchancen zu löschen
Sie können Verkaufschancen z. B. löschen, wenn Sie ein Geschäft abgeschlossen haben. Es können jedoch nur abgeschlossene Verkaufschancen gelöscht werden. Es gibt zwei Möglichkeiten, um abgeschlossene Verkaufschancen zu löschen. Sie können einzelnen abgeschlossene Verkaufschancen über die Seite **Verkaufschancenliste** löschen, oder Sie können die Stapelverarbeitung **Geschlossene Verkaufschancen löschen...** ausführen, um mehrere Verkaufschancen auf Grundlage von Kriterien zu löschen.

Um abgeschlossene Verkaufschancen aus der Seite **Verkaufschancenliste** zu löschen, wählen Sie die Verkaufschance, und wählen Sie dann die Aktion **Löschen** aus.

Um abgeschlossene Verkaufschancen über die Stapelverarbeitung **Geschlossene Verkaufschancen löschen...** zu löschen verwenden, gehen Sie folgendermassen vor:

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Verkaufschancen löschen** ein und wählen Sie dann den zugehörigen Link.
2. Im **Verkaufschance**-Abschnitt richten Sie die Filter ein, die die zu löschenden abgeschlossenen Verkaufschancen definieren.
3. Wählen Sie die Schaltfläche **OK** aus.

Nachdem Sie eine Verkaufschance gelöscht haben, wird sie aus der Seite **Verkaufschancenliste** entfernt.

## <a name="to-move-an-opportunity-through-sales-cycle-stages" />Verschieben einer Verkaufschance über Verkaufsprozessstufen
Wenn eine Verkaufschance einem Verkaufsprozess folgt, können Sie sie vorwärts oder rückwärts durch die verschiedenen Stufen verschieben oder eine Stufe überspringen.

1. Wählen Sie auf der Seite **Verkaufschancenliste** die Aktion **Aktualisieren**. Der Assistent **Verkaufschance aktualisieren** wird geöffnet.
2. Verwenden Sie das **Aktionsart**-Feld, um die Verkaufschance durch die Verkaufsprozessstufen zu verschieben:
   * **Nächste** verschiebt die Verkaufschance eine Stufe weiter.
   * **Überspringen** verschiebt die Verkaufschance eine oder mehrere Stufen im Verkaufsprozess weiter, die Sie im Feld **Präsentation** angeben. Sie können nur Stufen überspringen, die eingerichtet wurden, um das Überspringen zu ermöglichen.
   * **Vorherige** verschiebt die Verkaufschance eine Stufe zurück.
   * **Überspringen** verschiebt die Verkaufschance eine oder mehrere Stufen im Verkaufsprozess zurück, die Sie im Feld **Präsentation** angeben.
   * **Aktualisieren** ermöglicht das Ändern von Informationen (z. B. Ihre Einschätzung zu den Erfolgschancen und den erwarteten Zahlen), ohne die Verkaufschance auf eine andere anderen Stufe zu verschieben.
3. Füllen Sie die anderen relevanten Felder wie erforderlich aus, und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="see-also" />Weitere Informationen
[Verkauf](sales-manage-sales.md)  
[Erstellen und Verwalten von Kontakten](marketing-contacts.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
