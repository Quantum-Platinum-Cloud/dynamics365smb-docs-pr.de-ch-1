---
title: Anlagen verwalten
description: 'Sie führen einen Wartungs-Datensatz über alle Reparaturen und Wartungen an einer Anlage, um den Wert dieser Anlage zu erhalten.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'repair, service'
ms.search.form: '5642, 5625'
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="maintain-fixed-assets" />Anlagen verwalten

Wartungsausgaben sind periodische Kosten, die dem Werterhalt von Anlagen dienen. Im Gegensatz zu Kapitalerhöhungen wird der Wert dabei nicht erhöht.

Sie können den Service und die Wartung ihrer Anlagen erfassen, damit Ihnen jederzeit aktuelle Daten über die Wartung Ihrer Anlagen zur Verfügung stehen. Die wichtigen Daten, wie z. B. Kreditorennummer und Tel.-Nr. der Wartungsfirma und Datum, können Sie bei jedem Service einer Anlage erfassen. Die Registrierung der Wartung erfolgt für jede Anlage aus der Anlagenkarte.

Die Indexierung wird verwendet, um die Werte allgemeinen Preisänderungen anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um Wartungskosten neu zu berechnen.

## <a name="to-record-maintenance-work-on-a-fixed-asset" />So erfassen Sie Wartungsarbeiten in einer Anlage

Jedes Mal, wenn eine Wartung ausgeführt wurde, wie z.B. ein Servicebesuch, können Sie diese für die entsprechende Anlage auf der Seite **Wartungsregistrierung** erfassen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Anlage aus, für die Sie die Wartung übernehmen möchten und wählen Sie dann die Aktion **Wartungsregistrierung** aus.
3. Füllen Sie auf der Seite **Wartungsregistrierung** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-post-maintenance-costs-from-a-fixed-asset-gl-journal" />So buchen Sie Wartungskosten aus einem Anlagen Fibu Erf.-Journal

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Abschreibungsbuch Liste** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie das AfA-Buch aus, das der Anlage zugewiesen ist, und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Stellen Sie auf der Seite **Abschreibungsbuch - Karte** sicher, dass das Kontrollkästchen **Wartung** nicht aktiviert ist. Dadurch ist sichergestellt, dass keine Wartungskosten im Fibuposten gebucht werden.
4. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen Fibu Erfassungsjournale** ein, und wählen Sie dann den zugehörigen Link.  
5. Erstellen Sie eine ursprüngliche Erf.-Journalzeile und füllen Sie die notwendigen Felder aus.
6. Wählen Sie im Feld **Anlagenbuchungsart** die **Wartung**.
7. Wählen Sie die Aktion **Anlagengegenkonto einfügen**. Eine zweite Erf.-Journalzeile wird für das Gegenkonto erstellt, das für die Buchung einer Wartung eingerichtet wird.

    > [!NOTE]  
    >   Schritt 7 funktioniert nur, wenn Sie Folgendes eingerichtet haben: Auf der Seite **Anlagenbuchungsgruppenkarte** der Buchungsgruppe der Anlage enthält das Feld **Kto. Wartung** das Sollkonto im Fibukonto und das Feld **Gegenkto. Wartung** enthält das Fibukonto, auf das die Gegenposten für Zuschreibungen gebucht werden sollen. Weitere Informationen finden Sie unter [So richten Sie Anlagenbuchungsgruppen ein](fa-how-setup-general.md#to-set-up-fixed-asset-posting-groups).
8. Wählen Sie die Aktion **Buchen** aus.

## <a name="to-follow-up-on-fixed-assets-service-visits" />So führen Sie Folgeaktionen nach Servicebesuchen für Anlagen aus

Sie können den Bericht **Wartung - Nächster Service** drucken, um anzuzeigen, für welche Anlagen ein Servicebesuch geplant ist. Sie können diesen Bericht auch verwenden, wenn Sie das Feld **Nächstes Servicedatum** auf den Anlagenkarten aktualisieren.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Wartung Nächste Wartung** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder **Startdatum** und **Enddatum** aus.  
3. Klicken Sie auf die Schaltfläche **Drucken** oder **Vorschau**.

## <a name="to-monitor-maintenance-costs" />So prüfen Sie Wartungskosten

Sie können die Wartungskosten einsehen, wenn Sie sich die Statistik einer Anlage anzeigen lassen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage aus, für die Sie die Wartungskosten anzeigen möchten und wählen Sie dann die Aktion **AfA-Bücher** aus.
3. Wählen Sie auf der Seite **Anlagen-Abschreibungsbücher** das relevante Anlagen-Abschreibungsbuch aus, und dann die Aktion **Statistik**.
4. Klicken Sie zum Öffnen auf der Seite **Anlagenstatistik** auf das Feld **Wartung**.

Die Seite**Wartungsposten** wird geöffnet und zeigt die Posten an, aus denen sich der Betrag im Feld **Wartung** zusammensetzt.

## <a name="to-view-or-print-maintenance-costs-for-multiple-fixed-assets" />So werden Wartungskosten für mehrere Anlagen angezeigt oder gedruckt

In dem Bericht **Wartungsanalyse** können Sie auswählen, ob Sie sich Wartungen basierend auf ein, zwei oder drei Wartungscodes für ein bestimmtes Datum oder ein Datumsintervall anzeigen lassen wollen. Sie können sich eine Gesamtsumme für alle ausgewählten Anlagen oder eine Summe für jede einzelne Anlage anzeigen lassen.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Wartungsanalyse** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus.
3. Klicken Sie auf die Schaltfläche **Drucken** oder **Vorschau**.

## <a name="to-view-maintenance-ledger-entries" />So zeigen Sie Wartungsposten an

Sie können sich ausserdem die Wartungskosten ansehen, wenn Sie sich die Wartungsposten anzeigen lassen.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage aus, für die Sie die Posten anzeigen möchten und wählen Sie dann die Aktion **AfA-Bücher** aus.
3. Wählen Sie auf der Seite **Anlagen-Abschreibungsbücher** das relevante Anlagen-Abschreibungsbuch aus, und dann die Aktion **Wartungsposten**.

## <a name="to-view-or-print-maintenance-ledger-entries-for-multiple-fixed-assets" />So werden Wartungsposten für mehrere Anlagen angezeigt oder gedruckt

Sie können im Bericht **Wartungsdetails** Wartungsposten für eine oder mehrere Anlagen anzeigen oder drucken.  

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Wartungsdetails** ein und wählen Sie dann den zugehörigen Link.
2. Füllen Sie die Felder je nach Bedarf aus.
3. Klicken Sie auf die Schaltfläche **Drucken** oder **Vorschau**.

## <a name="see-related-microsoft-trainingtrainingpathsmanage-fixed-assets-maintenance-insurances" />Siehe verwandte [Microsoft Schulungen](/training/paths/manage-fixed-assets-maintenance-insurances/)

## <a name="see-also" />Siehe auch

[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
