---
title: Artikelposten entfernen und erneut ausgleichen
description: 'Sie können bestimmte Artikelausgleichsposten, die bei Lagertransaktionen automatisch erstellt werden, anzeigen und manuell ändern.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '506, 521, 9125'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="remove-and-reapply-item-ledger-entries" />Entfernen und erneutes Ausgleichen von Lagerposten
Sie können auf der Seite **Ausgleichsarbeitsblatt** bestimmte Artikelausgleichsposten, die bei Lagertransaktionen automatisch erstellt werden, anzeigen und manuell ändern.  

Wenn Sie eine Transaktion buchen, in der Artikel in den oder aus dem Lagerbestand verschoben werden, wird ein Artikelausgleich zwischen jedem Lagerzugang und Lagerabgang erstellt. Diese Ausgleiche bestimmen die Richtung für die Kosten von den Waren, die in den Lagerbestand übernommen wurden, zu den Kosten der Waren, die aus dem Lagerbestand herausgenommen wurden. Wegen der Art, in der Einstandspreise berechnet werden, könnte ein fehlerhafter Artikelausgleich zu falschen Durchschnittskosten und zu falschen Einstandspreisen führen. Weitere Informationen finden Sie unter "Designdetails: Artikelverfolgung".

Der folgende Szenarios erfordern möglicherweise, dass Sie einen Ausgleich rückgängig machen oder Lagerposten erneut ausgleichen:

- Sie haben vergessen, einen festen Ausgleich vorzunehmen.
- Sie haben einen fehlerhaften festen Ausgleich vorgenommen.
- Sie müssen einen Artikel zurücknehmen, für den bereits ein Verkauf ausgeglichen wurde.

Wenn möglich, verwenden Sie einen Beleg, um einen Lagerposten erneut auszugleichen. Wenn Sie beispielsweise eine Einkaufsreklamation für einen Artikel vornehmen müssen, für den bereits ein Verkauf ausgeglichen wurde, können Sie den erneuten Ausgleich vornehmen, indem Sie einfach den Einkaufsreklamationsbeleg in der Einkaufsreklamationszeile im Feld **Ausgleich mit Artikelposten** mit dem richtigen Ausgleich erstellen und buchen. Sie können die Funktion **Gebuchte Belegzeilen zum Stornieren holen** oder die Funktion **Aus Beleg kopieren** im Rückkaufsbeleg verwenden, um dies zu erleichtern. Wenn Sie den Beleg buchen, wird automatisch der Lagerposten erneut ausgeglichen. Weitere Informationen finden Sie unter [Einkaufsretouren verarbeiten oder Stornieren](purchasing-how-process-purchase-returns-cancellations.md).

Wenn Sie keinen Beleg verwenden können, um erneut auszugleichen, zum Beispiel wenn Sie einen festen Ausgleich korrigieren müssen, verwenden Sie die Seite **Ausgleichsarbeitsblatt**, um einen Ausgleich zu korrigieren.

> [!Warning]  
> Im Folgenden einige wichtige Überlegungen zur Arbeit mit dem Ausgleichsarbeitsblatt:
    - Sie sollten Ausgleichsposten nicht über einen längeren Zeitraum ohne Ausgleich lassen, da andere Benutzer die Artikel erst bearbeiten können, wenn Sie die Ausgleichsposten erneut ausgeglichen oder die Seite **Ausgleichsarbeitsblatt** geschlossen haben. Benutzer, die versuchen, Aktionen auszuführen, die einen manuell nicht ausgeglichenen Ausgleichsposten betreffen, erhalten die folgende Fehlermeldung: "Sie können diese Aktion nicht ausführen, da Posten für Artikel XXX im Ausgleichsarbeitsblatt vom Benutzer XXX aufgehoben wird. "
    - Sie sollten Lagerposten nur ausserhalb der Kernarbeitszeiten erneut ausgleichen, um Konflikte mit anderen Benutzern zu vermeiden, die Transaktionen zu den gleichen Artikeln buchen.
    - Wenn Sie den Ausgleichsarbeitsblatt schliessen, führt [!INCLUDE[prod_short](includes/prod_short.md)] eine Prüfung durch, um sicherzustellen, dass alle Posten ausgeglichen wurden. Wenn Sie beispielsweise einen Mengenausgleich entfernt, jedoch keinen neuen Ausgleich erstellt haben und den Ausgleichsarbeitsblatt dann schliessen, wird ein neuer Ausgleich erzeugt. Dies trägt dazu bei, die Kosten intakt zu halten. Beim Entfernen eines festen Ausgleichs wird jedoch nicht automatisch ein neuer fester Ausgleich erstellt, wenn Sie den Ausgleichsarbeitsblatt schliessen. Dies muss manuell erfolgen, indem Sie im Arbeitsblatt einen neuen Ausgleich erstellen.
    - Es ist möglich, einen oder mehrere Ausgleiche gleichzeitig für einen Posten im Ausgleichsarbeitsblatt zu entfernen. Da der Ausgleich von Posten jedoch den Satz der zum Ausgleich verfügbaren Posten beeinflusst, ist es nicht möglich, einen Ausgleich für mehr als einen Posten gleichzeitig zu erstellen.
    - In der folgenden Situation kann über den Ausgleichsarbeitsblatt kein Ausgleich erfolgen: Wenn im Lager nicht genügend Menge zum Ausgleich vorhanden ist, kann über den Ausgleichsarbeitsblatt kein Ausgleich vorgenommen werden, wenn Sie versuchen, einen Lagerabgangsposten ohne Artikeltrackinginformationen mit einem Lagerzugangsposten mit Artikeltrackinginformationen auszugleichen.

## <a name="to-remove-an-item-application-by-using-the-application-worksheet" />Artikelausgleich mit dem Ausgleichsarbeitsblatt entfernen

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet](media/ui-search/search_small.png "Tell me-Funktion"). Symbol. Geben Sie **Ausgleichsarbeitsblatt** ein und wählen Sie dann den zugehörigen Link.  
2.  Die Seite **Ausgleichsarbeitsblatt** wird geöffnet und zeigt bestehende Lagerposten für alle Artikel an.  
3.  Geben Sie im Inforegister **Allgemein** Filter ein, um die Suche nach dem Lagerposten, für den Sie den Ausgleich ändern möchten, zu erleichtern.  
4.  Wählen Sie den Lagerposten aus, und wählen Sie die Aktionen **Ausgeglichene Posten**. Die Seite **Ausgeglichene Posten anzeigen – Ausgeglichene Posten** wird geöffnet und zeigt den/die Lagerposten für den Ausgleich mit dem ausgewählten Posten an.  
5.  Wählen Sie den Lagerposten aus, für den Sie den Ausgleich entfernen möchten.  
6.  Wählen Sie die Aktion **Ausgleich entfernen** aus. Dadurch wird der Artikelausgleichsposten, der die beiden Lagerposten verknüpft, entfernt und auf der Seite **Ausgleichsposten anzeigen - nicht ausgeglichene Posten** verschoben.  
7.  Schliessen Sie die Seite **Ausgeglichene Posten anzeigen – Ausgeglichene Posten**.  

 Für beide Lagerposten wird das jeweilige Feld **Restmenge** um die Menge erhöht, deren Ausgleich aufgehoben wurde. Der entfernte Lagerposten ist jetzt für den erneuten Ausgleich auf der Seite **Ausgeglichene Posten anzeigen – Nicht ausgeglichene Posten** verfügbar.  

> [!IMPORTANT]  
>  Sie sollten Ausgleichsposten nicht über einen längeren Zeitraum ohne Ausgleich lassen, da andere Benutzer die Artikel erst bearbeiten können, wenn Sie die Ausgleichsposten erneut ausgeglichen oder die Seite **Ausgleichsarbeitsblatt** geschlossen haben. Die folgende Fehlermeldung wird angezeigt, wenn Sie versuchen, Aktionen auszuführen, die einen manuell nicht ausgeglichenen Ausgleichsposten betreffen:  
>   
>  **Diese Aktion kann nicht ausgeführt werden, da der Artikel \<item\> vom Benutzer \<user\> im Ausgleichsarbeitsblatt aufgehoben wurde.**  

## <a name="to-reapply-an-item-application-by-using-the-application-worksheet" />Artikelausgleich mit dem Ausgleichsarbeitsblatt erneut ausgleichen

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet 2.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Ausgleichsarbeitsblatt** ein und wählen Sie dann den zugehörigen Link.  
2.  Die Seite **Ausgleichsarbeitsblatt** wird geöffnet und zeigt bestehende Lagerposten für alle Artikel an.  
3.  Um Einträge, die seit dem Öffnen des Arbeitsblattes entfernt wurden, erneut zu übernehmen, markieren Sie den Lagerposten, den Sie erneut übernehmen möchten, und wählen Sie dann die Aktion **Erneut anwenden**.  

    > [!NOTE]  
    >  Der erneute Ausgleich mit dem ursprünglichen Saldo erfolgt auch automatisch, wenn Sie die Seite **Anwendungsarbeitsblatt** schliessen.  
4.  Wählen Sie zum Ausgleich eines verfügbaren offenen Lagerpostens mit einem anderen Posten den entsprechenden Lagerposten aus. Wählen Sie die Aktion **Nicht ausgeglichene Posten** aus. Die Seite **Ausgleichsposten anzeigen - nicht ausgeglichene Posten** wird geöffnet.  
5.  Wählen Sie einen oder mehrere Lagerposten aus, die Sie für den Posten auf der Seite **Ausgleichsarbeitsblatt.** ausgewählten Posten auswählen, und wählen Sie die Schaltfläche **OK**.  

     Es wird ein Artikelausgleichsposten zwischen den beiden Lagerposten erstellt. Das Feld **Restmenge** der beiden Post wird jeweils um die für den Ausgleich verwendete Menge verringert.  

    > [!NOTE]  
    >  Wenn Sie einen Ausgleich ausgewählt haben, mit dem eine Endlosschleife in der Lagerregulierung erzeugt wird, wird der von Ihnen gewünschte Ausgleich nicht vorgenommen. Dies kommt in Fällen vor, in denen mit den ursprünglichen Posten ein negativer Lagerbestand erzeugt wurde. Der Ausgleich wird nicht vorgenommen. Daher müssen Sie einen anderen Posten für den Ausgleich auswählen.  
6.  Wenn in **Lager Einrichtung** das Feld **Automatische Lagerregulierung** auf **Immer** festgelegt ist, wird die Stapelverarbeitung für Kostenregulierung automatisch ausgeführt, nachdem Sie einen erneuten Ausgleich vorgenommen haben. Führen Sie andernfalls den Batchauftrag **Lagerreg. fakt. Einst. Preise** aus, um sicherzustellen, dass alle Kosten auf dem neuesten Stand sind.  

## <a name="see-also" />Siehe auch

[Schliessen von offenen Lagerposten aus einem festen Ausgleich im Artikel Erf.-Journal](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
 [Verarbeiten einer Einkaufsrücklieferung oder von Stornierungen](purchasing-how-process-purchase-returns-cancellations.md)  
 [Verwalten der Lagerregulierung](finance-manage-inventory-costs.md)   
 [Designdetails: Artikelausgleich](design-details-item-application.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
