---
title: Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen
description: Die fertig gestellte Menge repräsentiert den Arbeitsfortschritt in Form der fertigen Menge und der genutzten Kapazität der Arbeit oder des Arbeitsplatzes.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '99000773, 99000778, 99000823, 99000827'
ms.date: 03/08/2023
ms.author: edupont
---
# <a name="batch-post-output-and-run-times" />Ausgabe über Stapelverarbeitung buchen und Bearbeitungszeiten prüfen

Die fertig gestellte Menge repräsentiert den Arbeitsfortschritt in Form der fertigen Menge und der genutzten Kapazität der Arbeit oder des Arbeitsplatzes.

Sie können das Ausgabejournal für Folgendes verwenden:

* Regulieren Sie Lagerbestand in Verbindung mit der Ausgabe fertiger Artikel aus der Produktion.
* Registrieren Sie Mengen und Ausschuss für jeden Vorgang im Fertigungsarbeitsgang.
* Registrieren Sie Setup und Laufzeit für Arbeit und Arbeitsplätze.

> [!NOTE]
> Wenn der Fertigungsarbeitsgang verwendet wird, aktualisiert die Anwendung automatisch den Lagerbestand nur wenn Sie die fertig gestellte Menge für den letzten Arbeitsgang buchen.

Auf der Seite **Produktionsjournal** können Sie die gleichen Aufgaben ausführen wie auf der Seite **Ausgangsjournal** und auch Verbrauchsbuchungs-Aufgaben vornehmen. Weitere Informationen finden Sie unter [Gemeinsames Erfassen und Buchen von Verbrauch und Istmeldungen für eine einzelne freigegebene Fertigungsauftragszeile](production-how-to-register-consumption-and-output.md).

## <a name="to-post-output-quantities-andor-register-run-times-for-one-or-more-production-order-lines" />Die fertig gestellte Mengen und/oder Erfassungslaufzeiten für eine oder mehrere Fertigungsauftragszeilen buchen

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Erfassung Erf.-Journal** ein und wählen Sie dann den zugehörigen Link.  
2. Füllen Sie die Felder mit den Daten des Fertigungsauftrags und den Ausgabedaten und/oder der Laufzeit aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
  
    Sie können die Funktion **Arbeitsplan auflösen** Generieren von Journalzeilen aus Fertigungsaufträgen verwenden.
  
3. Wenn der Arbeitsgang beendet ist, wählen Sie das Feld **Beendet** aus.  
4. Um die Vorgänge zu buchen, wählen Sie die Aktion **Buchen** aus.

    Kapazitätsposten werden für die verwendeten Arbeitsplätze mit Informationen zu Zeit und Menge der Ausgabe und des Ausschusses aktualisiert. Wenn Sie den letzten Vorgang gebucht haben, wird der Artikel dem Lager hinzugefügt.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## <a name="see-also" />Siehe auch

[Ausschuss manuell buchen](production-how-to-post-scrap.md)
[Gebuchte fertig gestellte Menge stornieren](production-how-to-reverse-output-posting.md)
[Produktion](production-manage-manufacturing.md)
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)  
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
