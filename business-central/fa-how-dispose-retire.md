---
title: FA entsorgen oder ausmustern
description: 'Wenn Sie eine Anlage verkaufen oder anderweitig entfernen, muss der Verkaufswert gebucht werden, um den Gewinn oder Verlust zu berechnen und zu erfassen.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: scrap
ms.search.form: '5628, 5610, 5611, 5629, 5633'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="dispose-of-or-retire-fixed-assets" />Anlagen entsorgen oder ausser Dienst stellen

Wenn Sie eine Anlage verkaufen oder anderweitig entfernen, muss der Verkaufswert gebucht werden, um den Gewinn oder Verlust zu berechnen und zu erfassen. Ein Verkaufsposten muss der letzte gebuchte Posten einer Anlage sein. Für teilweise verkaufte Anlagen können Sie mehr als einen Verkaufsposten buchen. Die Summe aller gebuchten Verkaufsbeträge muss ein Habenposten sein.  

> [!NOTE]  
> Falls Sie für den Verkauf einer Anlage eine andere Anlage in Zahlung nehmen, müssen Sie sowohl den Verkauf der alten Anlage als auch die Anschaffung der neuen Anlage buchen. Weitere Informationen finden Sie unter [Anschaffen von Anlagen](fa-how-acquire.md).  

Bei den folgenden Schritten wird davon ausgegangen, dass Sie die entsprechenden Buchungsgruppen auf der Seite **Anlagen-Buchungsgruppen** bereits eingerichtet haben. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  

## <a name="to-post-a-disposal-from-the-fixed-asset-gl-journal" />So buchen Sie einen Verkauf aus dem Anlagen Fibu Erf.-Journal

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen-Fibu Erfassungsjournale** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine ursprüngliche Erf.-Journalzeile und füllen Sie die notwendigen Felder aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Wählen Sie im Feld **Anlagenbuchungsart** den **Verkauf**.  
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Erf.-Journalzeile wird für das Gegenkonto erstellt, das für die Buchung eines Verkaufs eingerichtet wird.  

    > [!NOTE]  
    >  Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Auf der Seite **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Kto. Verkauf** das Sollkonto im Fibukonto und das Feld **Gegenkonto Verkauf** enthält das Fibukonto, auf das die Gegenposten für Zuschreibungen gebucht werden sollen. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Wählen Sie die Aktion **Buchen** aus.  

Wenn Sie eine Anlage zum Teil verkaufen, müssen Sie die Anlage aufteilen, bevor Sie die Verkaufstransaktion buchen können. Weitere Informationen finden Sie unter [Übertragen, Teilen oder Kombinieren von Anlagen](fa-how-trans-split-combine.md).  

## <a name="to-view-disposal-ledger-entries" />So zeigen Sie Verkaufsposten an

Wenn Sie eine Anlage verkaufen, wird der Verkaufswert in den Fibuposten gebucht, wo Sie die Ergebnisse anzeigen können.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Anlage aus, für die Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **AfA-Bücher** aus.  
3. Wählen Sie das AfA-Buch aus, für das Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **Posten** aus.  
4. Wählen Sie im Feld **Anlagebuchungskategorie** eine Zeile mit **Abgang** aus, und wählen Sie dann die Aktion **Posten finden** aus.  
5. Wählen Sie auf der Seite **Posten finden** die Fibupostenzeile aus, und wählen Sie dann die Aktion **Zugehörige Posten anzeigen** aus.  

Die Seite **Fibuposten** wird geöffnet, auf der Sie die Posten sehen können, die aus der Verkaufsbuchung resultieren.  

## <a name="see-related-microsoft-trainingtrainingmodulesdispose-fixed-assets" />Siehe verwandte [Microsoft Schulungen](/training/modules/dispose-fixed-assets/)

## <a name="see-also" />Siehe auch

[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[So richten Sie Anlagen-Buchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
[Finanzen](finance.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Posten finden](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
