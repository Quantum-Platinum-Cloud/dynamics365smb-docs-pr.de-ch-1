---
title: Anlagen neu bewerten
description: 'Erfahren Sie, wie der Wert von Anlagen reguliert wird und neue Beträge als erhöhte AfA oder Zuschreibungen erfasst werden, und buchen Sie zusätzliche Anschaffungskosten.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5628, 5629, 5633'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="revalue-fixed-assets" />Anlagen neu bewerten

Eine Neubewertung von Anlagen kann aus Abschreibungen, erhöhter AfA oder allgemeinen Wertanpassungen bestehen.

Wenn sich der Wert einer Anlage erhöht hat, buchen Sie eine Erf.-Journalzeile mit einem höheren Betrag, einer Abschreibung, auf das Abschreibungsbuch. Der neue Betrag wird als Abschreibung gemäss der Anlagebuchung eingerichtet.

Wenn sich der Wert einer Anlage verringert hat, buchen Sie eine Erf.-Journalzeile mit einem niedrigen Betrag, einer erhöhten Abschreibung, auf das Abschreibungsbuch. Der neue Betrag wird als erhöhte AfA gemäss der Anlagebuchung eingerichtet.

Die Indexierung wird verwendet, um mehrere zu versichernde Summen, wie beispielsweise allgemeinen Preisänderungen, anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um verschiedene Beträge (wie erhöhte AfA und Zuschreibungen) zu ändern.

## <a name="to-post-an-appreciation-from-the-fixed-asset-gl-journal" />So buchen Sie Zuschreibungen aus dem Anlagen Fibu Erf.-Journal

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen Fibu Erfassungsjournale** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine ursprüngliche Erf.-Journalzeile und füllen Sie die notwendigen Felder aus.
3. Wählen Sie im Feld **Anlagenbuchungsart** die **Neubewertung**.
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Erf.-Journalzeile wird für das Gegenkonto erstellt, das für die Buchung von Zuschreibungen eingerichtet wird.

    > [!NOTE]  
    >   Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Auf der Seite **Zuschreibungskonto** der Buchungsgruppe der Anlage enthält das Feld **Kto. Wartung** das Sollkonto im Fibukonto und das Feld **Gegenkto. Wartung** enthält das Fibukonto, auf das die Gegenposten für Zuschreibungen gebucht werden sollen. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).  
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-post-a-write-down-from-the-fixed-asset-gl-journal" />So buchen Sie eine erhöhte Abschreibung aus dem Anlagen Fibu Erf.-Journal

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen Fibu Erfassungsjournale** ein, und wählen Sie dann den zugehörigen Link.  
2. Erstellen Sie eine ursprüngliche Erf.-Journalzeile und füllen Sie die notwendigen Felder aus.
3. Wählen Sie im Feld **Anlagenbuchungsart** die **Erhöhte AfA**.
4. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Erf.-Journalzeile wird für das Gegenkonto erstellt, das für die Buchung einer erhöhten Abschreibung eingerichtet wird.

    > [!NOTE]  
    >   Schritt 4 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Auf der Seite **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Abschreibungskonto** das Habenkonto im Fibukonto und das Feld **Ausgaben-Abschreibungskonto** das Sollkonto im Fibukonto, auf das die Gegenposten für erhöhte Abschreibungen gebucht werden sollen. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
5. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-perform-general-revaluation-of-fixed-assets" />So führen Sie allgemeine Neubewertungen von Anlagen aus

Die Indexierung wird verwendet, um mehrere zu versichernde Summen, wie beispielsweise allgemeinen Preisänderungen, anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um verschiedene Beträge (wie erhöhte AfA und Zuschreibungen) zu ändern. Das Kontrollkästchen **Indexierung zulassen** auf der Seite **Abschreibungsbuch** muss aktiviert sein.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlage indexieren** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder je nach Bedarf aus.
3. Wählen Sie die Schaltfläche **OK** aus.

    Neubewertungszeilen werden in Schritt 2 gemäss Ihrer Einstellungen erstellt. Die Zeilen werden entweder im Anlagen Erf.-Journal oder im Anlagen Fibu Erf.-Journal, abhängig von Ihren Vorlagen und Stapeln, die auf der Seite **Anlagen Erf.-Journal Einr.** installiert sind, erstellt. Weitere Informationen finden Sie unter [Allgemeine Anlageninformationen einrichten](fa-how-setup-general.md).
4. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagen Fibu Erfassungsjournale** ein, und wählen Sie dann den zugehörigen Link.  
5. Wählen Sie das Buch.-Blatt mit den Anlagen, die Sie neu bewerten möchten und wählen die Aktion **Posten** aus.  
6. Prüfen Sie die erstellten Posten und wählen Sie dann die Aktion **Buchen** aus, um das Buch.-Blatt zu buchen.

    > [!TIP]  
    >   Falls die Indexzahlen nur für die Simulation verwendet werden, können Sie ein spezielles Abschreibungsbuch dafür erstellen. Dann haben diese Posten keinen Einfluss auf andere Abschreibungsbücher.

## <a name="to-post-additional-acquisition-costs" />So buchen Sie zusätzliche Anschaffungskosten

Sie können zusätzliche Anschaffungskosten einer Anlage auf die gleiche Art buchen, auf die Sie die ursprünglichen Anschaffungskosten gebucht haben: aus einer Einkaufsrechnung oder aus einem Anlagen Erf.-Journal. Weitere Informationen finden Sie unter [Anschaffen von Anlagen](fa-how-acquire.md).  

Falls bereits AfA für die Anlage berechnet wurde, aktivieren Sie das Kontrollkästchen **Rückw. AfA-Korr. b. Anschaff.**, damit die zusätzlichen Anschaffungskosten abzüglich des Restwertes proportional zu dem Betrag abgeschrieben werden, der für angeschaffte Anlage bereits abgeschrieben worden ist. Dies stellt sicher, dass die Abschreibungsperiode nicht geändert wird.  

Die Berechnung des Abschreibungsprozentsatzes erfolgt in dieser Weise:  

*P = (Gesamt AfA x 100) / AfA Basis*

*AfA Betrag = (P/100) x (zusätzliche Anschaffungskosten - Restwert)*  

Beachten Sie, dass Sie das Kontrollkästchen **AfA bis Anlagedatum** auf der Rechnung, dem Anlagen Fibu Buch.-Blatt oder den Anlagen Buch.-Blattzeilen aktivieren müssen, um sicherzustellen, dass die AfA vom letzten Anlagenbuchungsdatum bis zum Buchungsdatum der zusätzlichen Anschaffungskosten berechnet wird.

### <a name="example---posting-additional-acquisition-costs" />Beispiel – Buchen von zusätzlichen Anschaffungskosten

Eine Maschine wurde am 1. August 2000 erworben. Die Anschaffungskosten betragen 4.800. Die Abschreibungsmethode ist linear über vier Jahre.

Am 31. August 2000 wird die Stapelverarbeitung **AfA berechnen** ausgeführt. Die Abschreibung wird berechnet als:

*Buchwert x AfA-Tage / Gesamtzahl der AfA-Tage = 4800 x 30 / 1440 = 100*  

Am 15. September 2000 wird eine Rechnung für die Lackierung der Maschine gebucht. Der Rechnungsbetrag ist 480.

Falls Sie das Kontrollkästchen **AfA bis Anlagedatum** auf der Rechnung aktiviert haben, bevor diese gebucht wurde, würde die folgende Berechnung erfolgen:  

15 Tage Abschreibung Date (vom 01.09.00 bis zum 15.09.00) werden berechnet als:

*Buchwert x AfA-Tage / verbleibende Anzahl der AfA-Tage = (4800 - 100) x 15 / 1410 = 50*

Falls Sie das Kontrollkästchen **Rückw. AfA-Korr. b. Anschaff.** auf der Rechnung aktiviert haben, bevor diese gebucht wurde, würde die folgende Berechnung erfolgen:  

*Die zusätzlichen Anschaffungskosten werden abgeschrieben als ((150 x 100) / 4800) / 100 x 480 = 15*

Die Grundlage für AfA ist jetzt *5280 = (4800 + 480)*, und die kumulierte AfA ist *165 = (100 + 50 + 15)*. Dies entspricht 45 AfA-Tagen der gesamten Anschaffungskosten. Das bedeutet, dass die Anlage innerhalb der geschätzten Lebensdauer von vier Jahren vollständig abgeschrieben wird.  

Wenn die Stapelverarbeitung **AfA berechnen** am 30.09.00 ausgeführt wird, wird die folgende Berechnung verwendet:  

*Verbleibende Restlebensdauer ist 3 Jahre, 10 Monate und 15 Tage = 1395 Tage*  

*Der Buchwert ist (5280 - 165) = 5115*  

*AfA-Betrag für September 2000: 5115 x 15 / 1395 = 55,00*  

*Gesamtsumme AfA = 165 + 55 = 220*  

Falls Sie das Kontrollkästchen **AfA bis Anlagedatum** aktiviert haben, würde die Anlage 15 AfA-Tage verlieren, weil die Stapelverarbeitung **AfA berechnen**, die am 30.09.00 ausgeführt wurde, die AfA vom 15.09.00 bis zum 30.09.00 berechnen würde. D. h., wenn die Stapelverarbeitung **AfA berechnen** am 30.09.00 ausgeführt würde, würde die folgende Berechnung erfolgen:  

*Verbleibende Restlebensdauer ist 3 Jahre, 10 Monate und 15 Tage = 1395 Tage*  

*Der Buchwert ist (4800 + 480 - 100 - 15) = 5165*

*Der AfA-Betrag für September 2000: 5165 x 15 / 1395 = 55,54*  

*Gesamtsumme AfA = 100 + 15 + 55.54 = 170.54*

## <a name="see-related-microsoft-trainingtrainingpathsmanage-advanced-fixed-assets-transactions" />Siehe verwandte [Microsoft Schulungen](/training/paths/manage-advanced-fixed-assets-transactions/)

## <a name="see-also" />Siehe auch

[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
