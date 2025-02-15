---
title: Exemplarische Vorgehensweise – Verwalten von Projekten mit Aufträgen
description: 'Diese exemplarische Vorgehensweise führt Sie in die Funktionen der Projektverwaltung in Aufträgen ein, die es Ihnen erlauben, die Nutzung der Ressourcen Ihrer Firma zu planen und mehr.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-managing-projects-with-jobs" />Exemplarische Vorgehensweise: Verwalten von Projekten

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

In dieser exemplarischen Vorgehensweise erhalten Sie eine Einführung in die Projektmanagementfunktionen in "Projekte". Mit Projekten können Sie den Verbrauch der Ressourcen Ihres Unternehmens planen und die verschiedenen Kosten im Zusammenhang mit dem Einsatz von Ressourcen für ein bestimmtes Projekt verfolgen. Projekte beinhalten den Verbrauch von Mitarbeiterstunden, Maschinenstunden, Bestandsposten und andere Verbrauchsarten, die während des Projekts verfolgt werden können.  

 In dieser exemplarischen Vorgehensweise werden die Einrichtung eines neuen Projekts sowie einige allgemeine Aufgaben wie das Verwenden von Festpreisen, Anwenden von Teilzahlungen, Buchen von Projektrechnungen und Kopieren von Projekten erläutert.  

## <a name="about-this-walkthrough" />Informationen zu dieser exemplarischen Vorgehensweise

 In dieser exemplarischen Vorgehensweise werden folgende Aufgaben erläutert:  

### <a name="setting-up-a-job" />Einrichten eines Projekts

 Wenn die Budgetstruktur für Projekte eingerichtet ist, ist ein Projekt einfach zu erstellen. Diese exemplarische Vorgehensweise umfasst folgende Verfahren:  

- Einrichten von Projektaufgabenzeilen und Planungszeilen  
- Erstellen projektspezifischer Preise für Artikel, Ressourcen und Sachkonten  
- Fakturieren eines Projekts  

### <a name="handling-fixed-prices" />Verwenden von Festpreisen

 In Projekten können Festpreise und die vorab mit Kunden vereinbarten Preise für Services oder Waren verwendet werden. In dieser exemplarischen Vorgehensweise können Sie Folgendes durchführen:  

- Erfahren Sie, wie Vertrags- und Rechnungswerte ermittelt werden.  
- Einplanen zusätzlicher, nicht fakturierter Arbeit im Plan  

### <a name="copying-a-job" />Kopieren eines Projekts

 In diesem Teil der exemplarischen Vorgehensweise wird gezeigt, wie Sie ein Projekt ganz oder teilweise kopieren, um den manuellen Dateneingabeaufwand zu reduzieren und die Genauigkeit zu verbessern. Dazu zählen folgende Aufgaben:  

- Kopieren eines Projektteils in ein neues Projekt  
- Kopieren projektspezifischer Preise  
- Kopieren von Planungszeilen  

### <a name="making-payment-by-installment" />Anwenden von Teilzahlungen

 Wenn ein grosses, kostspieliges Projekt über einen langen Zeitraum läuft, schliesst der Kunde häufig mit dem Unternehmen eine Teilzahlungsvereinbarung ab. In diesem Szenario wird gezeigt, wie Sie Teilzahlungen und Versicherungen einrichten:  

- Erstellen von Teilzahlungen für ein Projekt  
- Fakturieren von Teilzahlungen  
- Abrechnen des Verbrauchs in einem Projekt, das für Teilzahlungen eingerichtet ist.  

## <a name="roles" />Rollen

 Diese exemplarische Vorgehensweise umfasst Aufgaben für folgende Rollen:  

- Projekt-Manager  
- Projektteammitglied  

## <a name="prerequisites" />Voraussetzungen

 Für diese exemplarische Vorgehensweise gelten folgende Voraussetzungen:  

- Installiere die CRONUS-Demonstrationsdatenbank.
- Erstellen Sie wie im folgenden Abschnitt beschrieben einige Beispieldaten.  

## <a name="story" />Hintergrund

Im Mittelpunkt dieser exemplarischen Vorgehensweise steht CRONUS, ein Entwicklungs- und Beratungsunternehmen, von dem neue Infrastrukturen (beispielsweise Sitzungssäle oder Büros) entwickelt und angepasst werden – komplett mit Einrichtungsgegenständen, Zubehör und Speichereinheiten. Der Grossteil der Arbeiten ist projektorientierter Natur. Prakash, ein Projektmanager bei CRONUS verwendet Aufträge, da er sich damit einen Überblick über die einzelnen laufenden Aufträge bei CRONUS verschaffen kann, die gestartet haben, wie auch über die abgeschlossenen Projekte. In der Regel ist es Prakash, der die Geschäfte mit Debitoren einrichtet und die Kerndaten des Projekts, d.h. Aufgaben- und Planungszeilen sowie Preise, in [!INCLUDE[prod_short](includes/prod_short.md)] erfasst. Prakash findet, dass erstellen, verwalten, und Informationen prüfen einfach ist. Auch ist Bernhard schätzt die Art, wie [!INCLUDE[prod_short](includes/prod_short.md)] das Kopieren von Projekten sowie von Teilzahlungen ausführt.

 Katrin, ein Projektteammitglied, das Bernard unterstellt ist, ist für die tägliche Überwachung des Projekts zuständig. Tricia trägt ihre eigene Arbeit zusätzlich zu der Arbeit der Techniker bei jeder Aufgabe ein, erfasst die von ihnen verwendeten Artikel und die ihnen entstandenen Kosten.  

## <a name="preparing-sample-data" />Vorbereiten der Beispieldaten

 Um sich für diese exemplarische Vorgehensweise vorzubereiten, müssen Sie Katrin als neue Ressource hinzufügen.  

### <a name="to-prepare-the-sample-data" />So bereiten Sie die Beispieldaten vor

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Ressourcen** ein und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die **Neu** Aktion aus, um eine neue Ressourcenkarte zu erstellen.  
3.  Geben Sie auf dem Inforegister **Allgemein** die folgenden Informationen ein:  

    - **Nr.**: **Katrin**  
    - **Name**: **Katrin**  
    - **Art**: **Person**  

4.  Wählen Sie im Feld **Basiseinheit** die Option **Neu**, um die Seite **Ressourceneinheit** zu öffnen. Wählen Sie im Feld **Code** die Option **Stunde** aus.  
5.  Geben Sie auf dem Inforegister **Fakturierung** die folgenden Informationen ein:  

    - **EK-Preis**: **5**  
    - **Kosten %**: **4**  
    - **Einstandspreis**: **10**  
    - **Produktbuchungsgruppe**: **Services**  
    - **MWST.-Produktbuchungsgruppe**: **MWST25**  

6. Schliessen Sie die Seite.

Im folgenden Verfahren erstellen Sie eine Projekt Erf.-Journal für Tricia, um deren Verbrauch zu buchen.  

### <a name="to-create-a-job-journal-batch" />So erstellen Sie einen Projekt Erfassungsjournalnamen

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Projekt Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie auf der Seite **Projekt Erf.-Journal** das Feld **Erf.-Journalname** aus. Die Seite **Projekt Erf.-Journalnamen** wird geöffnet.  
3.  Wählen Sie auf der Registerkarte Start die Option **Neu** aus, um eine neue Zeile mit folgender Information zu erstellen.  

    - **Name**: **Katrin**  
    - **Beschreibung**: **Katrin**  
    - **Nummernserie**: **PRJ-BCHBL**  

4.  Klicken Sie auf die Schaltfläche **OK**, um die Änderungen zu speichern.

## <a name="setting-up-a-job" />Einrichten eines Projekts

 In diesem Szenario hat CRONUS einen Vertrag mit einem Kunden, Progressive Home Furnishings, für den Entwurf eines Konferenz- und Speisesaals abgeschlossen. Der Kunde hat seinen Sitz in den USA, und für das Projekt ist spezielle Software erforderlich. Der Projektmanager trifft eine Vereinbarung mit dem Debitoren und erstellt ein Projekt für den Vertrag.  

### <a name="to-set-up-a-job" />So richten Sie ein Projekt ein

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die **Neu** Aktion aus, um eine neue Ressourcenkarte zu erstellen.  
3.  Geben Sie auf dem Inforegister **Allgemein** die folgenden Informationen ein:  

    - **Beschreibung**: **Beratung zur Einrichtung des Konferenzraums**  
    - **Rech. an Deb.-Nr.**: **01445544**  

4.  Geben Sie auf dem Inforegister **Buchung** die folgenden Informationen ein:  

    - **Status**: **Planung**  
    - **Projektbuchungsgruppe**: **Einrichten**  
    - **WIP-Methode**: **Einstandswert**  

5.  Geben Sie auf dem Inforegister **Dauer** das heutige Datum in die Felder **Startdatum** und **Enddatum** ein. Diese Datumsangaben werden bei der Fakturierung des Projekts zur Währungsumrechnung verwendet.  
6.  Stellen Sie auf dem Inforegister **Aussenhandel** sicher, dass der Währungscode auf **USD** festgelegt ist. Wenn Sie im Feld **Währungscode Rechnung** die Option "USD" auswählen, wird der Auftrag in US-Dollar fakturiert und nur in der lokalen Währung von CRONUS geplant.  

 Sie können die Preise für Debitoren auf Pro-Projekt-Basis je nach den getroffenen Vereinbarungen anpassen. Im folgenden Verfahren gibt der Projekt-Manager Kosten für Katrins Zeit an, setzt den Preis für die benötigte Software fest und fügt in den Reisekosten hinzu, dass der Debitor zugestimmt hat, zu zahlen.  

### <a name="to-customize-pricing" />Preise anpassen

1.  Von der Projektkarte wählen Sie die **Ressource** Aktion aus.  
2.  Geben Sie auf der Seite **Res.-VK-Preise Projekt** die folgenden Informationen ein:  

    - **Code**: **Katrin**  
    - **VK-Preis**: **20**  

3.  Schliessen Sie die Seite.  
4.  Wählen Sie die Aktion **Artikel** aus.  
5.  Geben Sie auf der Seite **Projektartikelpreise** die folgenden Informationen und den folgenden angepassten Preis ein:  

    1.  **Artikelnr.**: **80201 (Grafikprogramm)**  
    2.  **VK-Preis**: **200**  

6.  Schliessen Sie die Seite.  
7.  Wählen Sie die **Fibukonto** Aktion aus.  
8.  Geben Sie auf der Seite **Projekt-Fibukontopreise** die folgenden Werte sowie die Reisekosten ein, für die Sie mit dem Debitor vereinbart haben, dass er sie zuzüglich 25 Prozent übernimmt.  

    1.  **Fibukonto**: **8430 (Reisekosten)**  
    2.  **Einstandspreis**: **1,25**  

9. Schliessen Sie die Seite.  

 Die letzten Schritte beim Einrichten eines Projekts bestehen darin, die Projektaufgaben und die Planungszeilen hinzufügen, die Teil jedes Projekts sind. Die Planungszeilen bestimmen, welche Posten dem Debitoren in Rechnung gestellt werden.  

### <a name="to-add-job-tasks" />So fügen Sie Projektaufgaben hinzu

1.  Auf der Karte **Projekt** für das neue Projekt, wählen Sie die **Projektaufgabenzeilen** Aktion aus.  
2.  In der folgenden Tabelle werden die Informationen beschrieben, die Sie in die Felder eingeben müssen.  

    |Projektaufgabennr.|Description|Projektaufgabenart|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Beratung zur Einrichtung des Raums|Von-Summe|  
    |1010|Beratungsgespräch mit dem Kunden|Buchen|  
    |1020|Entwicklung|Buchen|  
    |1090|Beratung insgesamt|Bis-Summe|  

3.  Um anzuzeigen, dass einige Aufgaben Unterkategorien anderer Aufgaben sind, wählen Sie die Aktion **Projektaufgaben einrücken**.  

 Eine Planungszeile kann von einer der folgenden Arten sein:  

- **Budget**: Dem Plan hinzugefügt, aber noch nicht fakturiert.  
- **Fakturierbar**: Fakturiert, aber noch nicht dem Plan hinzugefügt.  
- **Budgetiert und verrechenbar**: Fakturiert und dem Plan hinzugefügt.  

 In dieser exemplarischen Vorgehensweise verwendet der Projektmanager **Budgetiert und verrechenbar**. Sie erstellen drei Planungszeilen für die Aufgabe 1010 und zwei Planungszeilen für die Aufgabe 1020.  

### <a name="to-create-planning-lines" />So erstellen Sie Planungszeilen

1. Wählen Sie die Zeile 1010 und wählen Sie dann die Aktion **Projektplanzeilen** aus.  

2. Erstellen Sie Planungszeilen mit den folgenden Informationen:  

    | Zeile | Zeilenart | Planungsdatum  | Art        | Nr.   | Menge | VK-Preis |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Sowohl budgetiert und verrechenbar | (heutiges Datum) | Ressource | Katrin | 40        |     |
    | 2    | Sowohl budgetiert und verrechenbar | (heutiges Datum) | Ressource | Thorsten | 40        |     |
    | 3    | Sowohl budgetiert und verrechenbar | (heutiges Datum) | Fibukonto | 8430 (Reise) | 2 | 400    |

     Schliessen Sie die Seite. Die Summen werden auf der Seite **Projektaufgabenzeilen** aktualisiert.  
3. Wählen Sie die Zeile 1020 und wählen Sie dann die Aktion **Projektplanzeilen** aus. Geben Sie die folgenden Informationen ein:  

    | Zeile | Zeilenart | Planungsdatum  | Art        | Nr.   | Menge | VK-Preis |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Sowohl budgetiert und verrechenbar | (heutiges Datum) | Ressource | Katrin | 80        |     |
    | 2    | Sowohl budgetiert und verrechenbar | (heutiges Datum) | Artikel | 80201 (Grafikprogramm) | 1 |     |

4. Schliessen Sie die Seite. Die Summen werden auf der Seite **Projektaufgabenzeilen** aktualisiert.  

## <a name="calculating-remaining-usage" />Berechnen des Restverbrauchs

 Tricia, das Teamprojektmitglied, arbeitet seit einiger Zeit an dem Projekt und möchte ihre Stunden und ihren Verbrauch für das Projekt erfassen. Tricia hat nicht mehr gearbeitet, als vorab mit dem Debitoren vereinbart wurde. Tricia verwendet den Batchauftrag **Restverbrauch berechnen**, um den Restverbrauch für das Projekt in einem Projekt Erf.-Journal zu berechnen. Mithilfe der Stapelverarbeitung wird für jede Projektaufgabe die Differenz zwischen dem geplanten Verbrauch von Artikeln, Ressourcen und Aufwandssachposten und dem in Projektposten gebuchten tatsächlichen Verbrauch berechnet. Der Restverbrauch wird dann im Projektbuchungsblatt angezeigt, von dem aus sie eine Buchung vornehmen kann.  

### <a name="to-calculate-remaining-usage" />So berechnen Sie den Restverbrauch

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Projekt Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.  
2.  Öffnen Sie auf der Seite **Projekt Erf.-Journal** im Feld **Erf.-Journalname** die Liste **Projekt Erf.-Journalnamen**. Wählen Sie den Projekt-Erfassungsjournalnamen **Katrin** aus.  
3.  Wächlen Sie im Aktionsbereich **Restverbrauch**.  
4.  Wählen Sie auf der Seite **Restverbrauch für Projekt berechnen** im Inforegister **Projektaufgabe** das Feld **Projektnr.** aus, und wählen die Jobnummer des entsprechenden Projekts, üblicherweise Projekt J00010.  
5.  Geben Sie auf dem Inforegister **Optionen** die Nummer **PW00001** in das Feld **Belegnr.** ein. Dadurch wird das zukünftige Tracking der Buchung vereinfacht.  
6.  Geben Sie als Buchungsdatum das heutige Datum ein.  
7.  Wählen Sie die Schaltfläche **OK**. Dadurch werden alle Projekt-Buchungsblattzeilen generiert, die von den von Bernard erstellten Planungszeilen für das Projektbuchhaltungsblatt abgeleitet wurden.  
8.  Wählen Sie die Schaltfläche **OK** aus auf der Bestätigungsseite. Die generierten Zeilen werden dem Projekt-Erfassungsjournal hinzugefügt.  
9. Stellen Sie sicher, dass für alle Belegnummern J00001 angezeigt wird. Klicken Sie auf Aktionen, zeigen Sie auf **Buchen**, und klicken Sie dann auf Buchen. Wählen Sie **Ja**, um die Buchung zu bestätigen.  

Die Zeilen werden gebucht.  

## <a name="creating-and-posting-a-job-sales-invoice" />Erstellen und Buchen einer Projektverkaufsrechnung

 Als Nächstes kann Katrin eine neue Rechnung für das gesamte Projekt oder für Teil eines Projekts erstellen. Tricia kann die Rechnung auch an eine andere Rechnung für denselben Debitoren und dasselbe Projekt anfügen. In diesem Fall fakturiert Tricia das gesamte Projekt, da es jetzt abgeschlossen ist.  

### <a name="to-create-a-job-sales-invoice" />So erstellen Sie eine Projektverkaufsrechnung

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie das Projekt aus, das Sie zuvor erstellt haben, und wählen die **Projektverkaufsrechnung erstellen** Aktion aus.  
3.  Löschen Sie im Inforegister **Projektaufgabe** in **Projektaufgabennr.** alle Filter, um das Projekt zu fakturieren. Wählen Sie im Feld **Projektnr.** das entsprechende Projekt aus.  
4.  Geben Sie im Inforegister **Optionen** das Buchungsdatum ein, und definieren Sie, ob eine Rechnung pro Aufgabe oder eine einzige Rechnung für alle Aufgaben erstellt werden soll.  
5.  Wählen Sie die Schaltfläche **OK** aus, um die Rechnung zu erstellen, und wählen Sie dann die Schaltfläche **OK** auf der Bestätigungsseite.  

 Nachdem Tricia die Rechnung erstellt hat, kann sie diese z.B. aus dem **Kundenauftragsabwickler** Rollencenter aufrufen. 

### <a name="to-post-a-new-sales-invoice" />So buchen Sie eine neue Verkaufsrechnung

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Verkaufsrechnungen** ein und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Rechnung für die Debitorennummer 01445544. Die aus den Planungszeilen erfassten Informationen werden angezeigt.  
3.  Wählen Sie die Aktion **Buchen** aus. Wählen Sie **Ja**, um die Buchung zu bestätigen.  

### <a name="to-view-the-posted-invoice" />So zeigen Sie die gebuchte Rechnung an

1.  Öffnen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Projektplanzeilen** aus.  
2.  Wählen Sie eine der fakturierten Planungszeilen aus, und wählen Sie auf der Registerkarte Start in der Gruppe Prozess die Option **Verkaufsrechnung/Gutschrift** aus.
3. Auf der Seite **Projektrechnungen** wählen Sie die Aktion **Verkaufsrechnungen/Gutschrift** aus.  

 Tricia hat eine Frage zu den Preisen, Kosten und Gewinnen für dieses spezielle Projekt, daher greift sie über die Seite **Statistik** auf die Informationen zu.  

### <a name="to-open-the-statistics-page" />So öffnen Sie die Seite "Statistik"

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2.  Wählen Sie die Aktion **Statistik** aus. Sie können detaillierte Informationen über die Projektverkaufspreise, Kosten und Gewinne in lokalen und fremden Währungen anzeigen.  
3.  Wählen Sie die Schaltfläche **Schliessen**, um die Seite **Projektstatistik** zu schliessen.  

## <a name="handling-fixed-prices" />Verwenden von Festpreisen

 CRONUS wurde abgeschlossen, um Konferenzräume einrichten. Als Projekt-Manager benötigt Bernard einen umfassenden Überblick über die erforderlichen Aufgaben für das Projekt sowie die zugehörigen budgetierten und angefallenen Kosten für jede Aufgabe. Zudem möchte Prakash den vertraglich vereinbarten Verkaufsbetrag für das Projekt und den bisher fakturierten Betrag ermitteln. Sie haben mit dem Debitoren Festpreise für das Projekt vereinbart.  

### <a name="to-manage-fixed-pricing-in-jobs" />So verwalten Sie Festpreise in Projekten

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Projektnummer **Guildford**, und wählen Sie die **Projektaufgabenzeilen** Aktion aus.  
3. Wählen Sie die Zeile 1120 aus, klicken Sie im Feld **Budget (Einstandsbetrag)** mit der rechten Maustaste auf den Betrag, und wählen Sie **DrillDown** aus.  

     Beim Überprüfen der Projektplanungszeilen stellt Prakash fest, dass er Tricia in dieser Phase des Projekts für 30 Stunden benötigt. Prakash vereinbart einen Festpreis mit dem Debitoren.  

4. Auf der Seite **Projekt Buch,-Blatt** wählen Sie die Zeile 1120 und wählen die Aktion **Buchen** aus. Erstellen Sie eine Planungszeile mit den folgenden Informationen:  

    | Zeile | Zeilenart | Art        | Nr.   | Menge |
    |------|-----------|-------------|-------|----------|
    | 1    | Sowohl budgetiert und verrechenbar  | Ressource | Katrin | 30 |

     Schliessen Sie die Seite.  
5. Klicken Sie mit der rechten Maustaste im Feld **Budget (Einstandsbetrag)**, und wählen Sie erneut **Drilldown** auf der Seite **Projektaufgabenzeilen** aus. Zeigen Sie die Änderungen am Plan an. Die 30 Stunden wurden dem Plan hinzugefügt.  
6. Schliessen Sie die Seiten.  

Nachdem Tricia den Plan für diese Aufgabenzeile hinzugefügt wurde, arbeitet sie 25 Stunden an dem Projekt. Diese Stunden können im Projekt Erf.-Journal erfasst werden.  

### <a name="to-enter-hours-in-the-job-journal" />So erfassen Sie Stunden im Projekt Erf.-Journal

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Projekt Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.  
2. Geben Sie in einer neuen Zeile die folgenden Informationen ein:  

    - **Zeilenart**: **(leer)**  
    - **Buchungsdatum**: **(heutiges Datum)**  
    - **Belegnr.**: **J00002**  
    - **Projektnr.**: **Bäderwelt**  
    - **Projektaufgabennr.**: **1120**  
    - **Art**: **Ressource**  
    - **Nr.**: **Katrin**  
    - **Menge**: **25**  

3. Wählen Sie die Aktion **Buchen** aus.  

     Ein paar Tage später arbeitet Tricia weitere 10 Stunden im Job und hat jetzt insgesamt 35 Stunden gearbeitet. Da Sie nur 30 Stunden mit dem Kunden vereinbart haben, werden dem Kunden nur fünf dieser Stunden in Rechnung gestellt. Tricia fügt manuell die fünf zusätzlichen Stunden hinzu, in denen sie den Plan bearbeitete.  

4. Wählen Sie auf der Seite **Projekt Erf.-Journal**auf der Registerkarte Start die Option **Restverbrauch berechnen**.  
5. Geben auf der Seite **Restverbrauch für Projekt berechnen** im Inforegister**Optionen** die folgenden Informationen ein:  

    - **Belegnr.**: **J00003**  
    - **Buchungsdatum**: **(heutiges Datum)**  

6. Geben Sie auf dem Inforegister **Projektaufgabe** die folgenden Informationen ein:  

    - **Projektnr.**: **Bäderwelt**  
    - **Projektaufgabennr.**: **1120**  

7. Klicken Sie auf die Schaltfläche **OK**, um die Berechnung auszuführen.

    Es gibt fünf Arbeitsstunden, die für Katrin bleiben. Das Feld **Zeilenart** ist leer; dies gibt an, dass nur der Verbrauch gebucht werden muss, da die Arbeit bereits geplant wurde.  

8. Erstellen Sie im **Projekt Erfassungsjournal** eine neue Zeile mit den folgenden Informationen. Prüfen Sie, ob beide Projektnummern Folgenummern derer, die Sie bereits verwendet haben:  

    - **Zeilenart**: **Budget**  
    - **Projektnr.**: **Bäderwelt**  
    - **Projektaufgabennr.**: **1120**  
    - **Art**: **Ressource**  
    - **Nr.**: **Katrin**  
    - **Menge**: **5**  

     Durch die Verwendung der Zeilenart **Budget** werden die geplanten Kosten und der Preis aktualisiert, ohne die dem Debitoren in Rechnung gestellten Einstandsbeträge und Preise aus dem Vertrag zu aktualisieren.  

9. Wählen Sie die Aktion **Buchen** aus. Wählen Sie die Schaltfläche **OK**, um die Seite zu schliessen.  
10. Öffnen Sie die Liste **Projekte**.  
11. Wählen Sie das Projekt GUILDFORD und dann im Abschnitt **Projektaufgabenzeilen** Sie Zeile 1120 aus, und klicken Sie im Feld **Budget (Gesamtkosten)** mit der rechten Maustaste auf den Betrag. Wählen Sie **DrillDown** aus, um die Informationen anzuzeigen.  

     Sie können sehen, dass die Änderungen automatisch in der Zeile für die Projektaufgabennummer 1120 eingegeben wurden. Im Einstandsbetrag der geplanten Arbeit sind fünf zusätzliche Arbeitsstunden von Katrin dem Plan hinzugefügt worden.  

12. Klicken Sie auf die Schaltfläche **Schliessen**, um die Seite zu schliessen.  
13. Klicken Sie mit der rechten Maustaste auf den Betrag im Feld **Vertrag (Einstandsbetrag)**, und wählen Sie dann **DrillDown** aus, um die Informationen anzuzeigen.  

Im Einstandsbetrag des Vertrags werden nur die ursprünglich im Vertrag festgesetzten 30 Stunden angezeigt, da dies mit dem Kunden vereinbart wurde.  

## <a name="copying-jobs" />Kopieren von Projekten

Bernard hat mit einem Kunden, Blütenhaus GmbH, einen Vertrag über die Einrichtung von zehn Konferenzräumen abgeschlossen. Da die Vereinbarung ähnelt einem früheren Projekt. Daher spart es Zeit, dieses frühere Projekt zu kopieren.  

Auf der Seite **Projekt kopieren** können Sie das zu kopierende Projekt und die gewünschten Aufgabenzeilen auswählen. Sie können auch festlegen, ob die Projektposten aus dem Quellprojekt (dabei werden Planungszeilen basierend auf dem tatsächlichen Verbrauch erstellt) oder die Planungszeilen des Quellprojekts (dabei werden die ursprünglichen Planungszeilen in das neue Projekt kopiert) kopiert werden sollen. Danach können Sie die für das neue Projekt relevanten Planungszeilen- oder Projektpostenarten auswählen und in den Kopiervorgang einschliessen. Zum Schluss wählen Sie das Zielprojekt aus, und Sie legen fest, ob Preise und Mengen ebenfalls kopiert werden sollen.  

### <a name="to-copy-a-job" />So kopieren Sie ein Projekt

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Aufträge** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die **Neu** Aktion aus, um eine neue Ressourcenkarte zu erstellen. Geben Sie die folgenden Informationen ein:  

    - **Beschreibung**: **Zehn Konferenzräume einrichten**  
    - **Rech. an Deb.-Nr.**: **20000**  

3. Wählen Sie die Aktion **Von Workflowvorlage kopieren** aus.  
4. Geben Sie auf der Seite **Projektaufgaben kopieren** Folgendes ein:  

    - **Projektnr.**: **Bäderwelt**  
    - **Projektaufgabennr. von**: **1000**  
    - **Herkunft**: **Projektplanzeilen**  
    - **Inkl. Planzeilenart**: **Budget + Fakturierbar**  
    - **Zu Projekt-Nr.** **Guildford-Einstellung bis zu 10 Konferenzräume**  
    - Aktivieren Sie die Felder **Dimensionen kopieren** und **Menge kopieren**.  

5. Wählen Sie die Schaltfläche **OK**, um das Projekt zu kopieren und wählen Sie dann die Schaltfläche **OK**, um die Bestätigungsseite zu schliessen.  

Indem Sie Preise, Projektaufgabenzeilen und Projektplanungszeilen für die beiden Projekte vergleichen, können Sie sehen, dass die Informationen erfolgreich kopiert wurden.  

## <a name="making-payments-by-installments" />Anwenden von Teilzahlungen

CRONUS hat gerade ein grosses Projekt an Land gezogen, das über ein Jahr laufen wird. Da viele Ressourcen erforderlich sind, richtet der Projektmanager den Vertrag so ein, dass der Debitor eine Teilzahlung im Voraus, eine Teilzahlung nach der Hälfte des Projekts und schliesslich die endgültige Zahlung nach Abschluss des Projekts leistet.  

### <a name="to-set-up-a-new-account" />So richten Sie ein neues Konto ein

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie auf der Seite **Kontenplan** auf der Registerkarte Start die Option **Neu**, um eine neue Karte zu erstellen.  
3. Geben Sie auf der Karte **Neues Fibukonto** die folgenden Informationen ein:  

    - **Nr.**: **40255**  
    - **Name**: **Projektbezahlung**  

4. Wählen Sie auf dem Inforegister **Buchung** im Feld **Produktbuchungsgruppe** die Option **Services** aus. Schliessen Sie die Seite.  
5. Wählen sie auf der Seite **Kontenplan** die Option **Nr. - 40255 Projektbezahlung** und auf der Registerkarte Start in der Gruppe Vorgang die Option **Einrückung des Kontenplans**aus. Wählen Sie **Ja** aus, um den Vorgang zu bestätigen.  

In den folgenden Verfahren wird gezeigt, wie Sie ein neues Projekt erstellen, die Preisgestaltung festlegen und dann Teilzahlungen einrichten. In den Projektaufgabenzeilen können Sie spezifische Zeilen für die Teilzahlungen erstellen. Alle für das Projekt ausgeführten Arbeiten werden dem Plan hinzugefügt und in den Verbrauchszeilen erfasst. Für jede Zahlungsaufgabenzeile der Planungszeilen kann die Zeilenart auf **Fakturierbar** festgelegt werden, wodurch die Fakturierung für den Debitor erfolgt. Geben Sie für die Anzahlung eine neue Zeile ein. In der Verbrauchsaufgabenzeile können Sie die Informationen für die in diesem Projekt verwendeten Artikel und Ressourcen eingeben, z. B. Mitarbeiterstunden und für das Projekt verbrauchte Artikel. Der Plan wird dadurch entsprechend erhöht.  

### <a name="to-make-a-payment-by-installment" />So wenden Sie eine Teilzahlung an

1. Erstellen Sie ein neues Projekt.  
2. Geben Sie auf der neuen Karte **Projekt** die folgenden Informationen ein:  

    - **Beschreibung**: **Neugestaltung des Empfangsbereichs**  
    - **Rech. an Deb.-Nr.**: **30000**  
    - **Projektbuchungsgruppe**: **Einrichten**  
    - **WIP-Methode**: **Einstandswert**  

3. Wählen Sie auf der Projektkarte die Aktion **Preise** und dann die Aktion **Ressource** aus. Geben Sie die folgenden Informationen ein:  

    - **Code**: **Katrin**  
    - **VK-Preis**: **10**  

     Schliessen Sie die Seite.  

4. Fügen Sie auf der Karte **Projekt** im Abschnitt **Aufgaben** Projektaufgabenzeilen hinzu, wie in der folgenden Tabelle beschrieben:  

    | Zeile | Projektaufgabennr. | Beschreibung          | Projektaufgabenart |
    |------|--------------|----------------------|---------------|
    | 1    | 1000         | Zahlung - Anzahlung | Buchen       |
    | 2    | 2000         | Verbrauch                | Buchen       |
    | 3    | 3000         | Zahlung - Hälfte     | Buchen       |
    | 4    | 4000         | Zahlung - Abschluss | Buchen       |

5. Wählen Sie die Aufgabe 1000 und wählen Sie dann die Aktion **Projektplanzeilen** aus.  

6. Erstellen Sie eine Planungszeile mit den folgenden Informationen:  

    | Zeile | Zeilenart | Planungsdatum  | Art        | Nr.   | Menge | VK-Preis |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Fakturierbar  | (heutiges Datum) | Fibukonto | 40255 | 1        | 5000       |

     Schliessen Sie die Seite.  

7. Wählen Sie die Aufgabe 2000 und wählen Sie dann die Aktion **Projektplanzeilen** aus.  

8. Erstellen Sie eine Planungszeile mit den folgenden Informationen:

    | Zeile | Zeilenart | Planungsdatum  | Art     | Nr.    | Menge |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Budget    | (heutiges Datum) | Ressource | Katrin | 120      |
    | 2    | Budget    | (heutiges Datum) | Artikel     | 70104  | 10       |

     Schliessen Sie die Seite. Auf der Seite **Projektaufgabenzeilen** können Sie sehen, dass die Planbeträge aktualisiert wurden.  

9. Wählen Sie die Aufgabe 32000 und wählen Sie dann die Aktion **Projektplanzeilen** aus.  

10. Erstellen Sie eine Planungszeile mit den folgenden Informationen:

    | Zeile | Zeilenart | Planungsdatum   | Art        | Nr.   | Menge | VK-Preis |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Fakturierbar  | (ein zukünftiges Datum) | Fibukonto | 40255 | 1        | 5000       |

     Schliessen Sie die Seite.  

11. Erstellen Sie eine ähnliche Planungszeile für Projektaufgabe 4000.  

 Nachdem die Aufgaben- und Planungszeilen erfasst wurden, erstellt Bernard eine Rechnung für die erste Zahlung. Prakash verwendet dazu die Projektaufgabenzeilen, um sicherzustellen, dass die Rechnung nur die Zeilen für die erste Zahlung enthält. Der Verkaufsauftrag kann über die Planungszeilen oder die Aufgabenzeilen geöffnet werden.  

### <a name="to-create-an-invoice" />So erstellen Sie eine Rechnung

1.  Auf der Seite **Projekt Buch,-Blatt** wählen Sie die Zeile 1000 und wählen die Aktion **Verkaufsrechung erstellen** aus.  
2.  Legen Sie auf der Seite **Verkaufsrechnung erstellen** das heutige Datum als Buchungsdatum fest, geben Sie **" Nach Aufgabe** an, und wählen Sie die Schaltfläche **OK**, um eine Rechnung mit den Standardinformationen zu erstellen. Klicken Sie auf **OK**, um die Bestätigungsseite zu schliessen.  
3.  Wählen Sie die Aktion **Verkaufsrechnung/Gutschrift**. Auf der Verkaufsrechnung können Sie sehen, dass die Rechnung nur die Anzahlung enthält. Diese Rechnung kann jetzt wie vereinbart an den Kunden gesendet werden.  

## <a name="next-steps" />Nächste Schritte

 In dieser exemplarischen Vorgehensweise wurden Sie durch mehrere der grundlegenden Schritte für die Arbeit mit Projekten in [!INCLUDE[prod_short](includes/prod_short.md)] geführt. Sie haben gelernt, wie ein neues Projekt erstellt, ein Projekt kopiert und Zahlungen verarbeitet werden. Sie haben auch eine Demonstration gesehen, wie Stunden verfolgt und Rechnungen erstellt werden.  

## <a name="see-related-microsoft-trainingtrainingpathscreate-jobs" />Siehe verwandte [Microsoft Schulungen](/training/paths/create-jobs/)

## <a name="see-also" />Siehe auch

 [Exemplarische Vorgehensweisen für Geschäftsprozesse](walkthrough-business-process-walkthroughs.md)  
 [Richten Sie Ihr Projektmanagement ein.](projects-setup-projects.md)  
 [Ressourcen verwenden](projects-how-use-resources.md)  
 [Überwachen von Status und Leistung](projects-how-monitor-progress-performance.md)  
 [Fakturieren von Projekten](projects-how-invoice-jobs.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
