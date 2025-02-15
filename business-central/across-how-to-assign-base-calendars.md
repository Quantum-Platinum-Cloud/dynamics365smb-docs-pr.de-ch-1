---
title: Basiskalender einrichten
description: 'Sie können Ihrer Firma und ihren Geschäftspartnern einen Basiskalender zuweisen, um Liefer- und Empfangsdaten gemäss den angegebenen Arbeitstagen zu berechnen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '7600, 7601, 7602, 5703'
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="set-up-base-calendars" />Basiskalender einrichten

Sie können Ihrer Firma sowie Ihren Geschäftspartnern, wie z. B. Debitoren, Kreditoren und Lagerorten oder Standorte zuordnen. Die Liefer- und Wareneingangsdaten auf zukünftigen Verkaufsaufträgen, Einkaufsbestellungen, Umlagerungsaufträgen und in Fertigungsauftragszeilen werden, entsprechend den Arbeitstagen, die im Kalender festgelegt sind, errechnet. Die Hauptaufgabe beim Einrichten eines neuen Basiskalenders ist, die freien Tage festzulegen.  

## <a name="to-set-up-a-base-calendar" />einen Basiskalender einrichten

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Basiskalender** ein, und wählen Sie dann den entsprechenden Link.  
2.  Wählen Sie die Aktion **Neu** aus.  
3.  Füllen Sie das Feld **Code** aus.  
4. Wählen Sie die **Basiskalender pflegen** Aktion aus.
5. Sie können auf der Seite **Basiskalender ändern** das Feld **Wiederkehrendes System** verwenden, um ein bestimmtes Datum als einen wiederkehrenden freien Tag zu kennzeichnen. Sie können das Wiederholungsmuster **Jährlich** oder **Wöchentlich** wählen.  

    Wenn Sie **Jährlich** wählen, müssen Sie auch das relevante Datum im Feld **Datum** eingeben.  

    Wenn Sie **Wöchentlich** wählen, müssen Sie auch im Feld **Tag** den relevanten Wochentag wählen. Wenn Sie das Feld leer lassen, müssen Sie das Feld **Datum** ausfüllen. Das Feld **Tag** wird automatisch ausgefüllt.  

Wenn Sie einen Eintrag vornehmen, wird das Feld **Frei** ausgewählt. Sie können festlegen, das Häkchen zu löschen, um einen Arbeitstag zu erstellen.  
 Wenn Sie zur Basiskalenderkarte zurückkehren, werden Sie feststellen, dass die freien Tage automatisch Ihren Einträgen entsprechend aktualisiert wurden. Diese Daten erscheinen jetzt in Rot, und das Feld **Frei** ist aktiviert.  

> [!NOTE]  
>  Wenn Sie einen neuen Basiskalender einrichten, können Sie in einem bestehenden Kalender Zeilen auswählen und kopieren. Dieser Schritt wird auf der jeweiligen Seite **Basiskalenderänderungen** durchgeführt.  

> [!IMPORTANT]  
>  Alle Basiskalender, die für den Kreditor oder Lagerort definiert wurden, wirken sich darauf aus, wie die Daten in Arbeitstage berechnet und gerundet werden.
Gibt eine Datumsformel für die Beschaffungszeit des Artikels an. Es wird verwendet, um das Feld **Geplantes Empfangsdatum** vorwärts zu berechnen und um das Feld **Aufrtragsdatum** rückwärts zu berechnen. Sehen Sie [Beschaffungszeit](across-how-to-assign-base-calendars.md#lead-time-calculation).

## <a name="lead-time-calculation" />Beschaffungszeit

Alle Basiskalender, die für den Kreditor oder Lagerort definiert wurden, wirken sich darauf aus, wie die Daten in Arbeitstage berechnet und gerundet werden. Die beiden Schlüsseldatumsfelder in Einkaufszeilen werden daher wie folgt mit unterschiedlichen Bedingungen berechnet.

|Berechnungsrichtung|Kreditorenkalender definiert|Kreditorenkalender nicht definiert|
|---------------------|-----------------------|---------------------------|
|Vorwärts|geplantes Wareneingangsdatum = Bestelldatum + Kreditorenbeschaffungszeit (pro Kreditorenkalender und auf den nächsten Arbeitstag im ersten Kreditorenkalender und dann im Lagerplatz-Arbeitsplatzgruppenkalender gerundet)|geplantes Wareneingangsdatum = Bestelldatum + Kreditorenbeschaffungszeit (pro Lagerort-Arbeitsplatzgruppenkalender)|
|"Rückwärts"|Bestelldatum = geplantes Wareneingangsdatum - Kreditorenbeschaffungszeit (pro Kreditorenkalender und auf den vorherigen Arbeitstag im ersten Kreditorenkalender und dann im Lagerplatz-Arbeitsplatzgruppenkalender gerundet)|Bestelldatum = geplantes Wareneingangsdatum - Kreditorenbeschaffungszeit (pro Lagerort-Arbeitsplatzgruppenkalender)|

> [!NOTE]
> Zusätzlich zur Beschaffungszeitberechnung, die das geplante Wareneingangsdatum beeinflusst, wird hinzugefügt und Auftragsdatum werden, wie in der obigen Tabelle angezeigt, Lagerdurchlaufzeit und Sicherheitsbeschaffungszeit zu den Formeln, um den Wert im Feld **Erwartetes Wareneingangsdatum** Feld zu schaffen, wie folgt: Geplantes Wareneingangsdatum + Sicherheitszuschlag Beschaffungszeit + Eingehende Lagerdurchlaufzeit = Erwartetes Wareneingangsdatum.

> [!Important]
> Wenn Ihr Lagerort einen erheblich anderen Kalender als Ihre Kreditoren verwendet, ist es wichtig, dass Sie bestimmte Kalender für die einzelnen Kreditoren einrichten, um optimale Kreditorbeschaffungszeiten zu berechnen. Weitere Informationen darüber, wie Kreditorenkalender eingerichtet werden, finden Sie unter [Zuweisen eines Basiskalenders](across-how-to-assign-base-calendars.md#to-assign-a-base-calendar).

Der Inhalt des Felds **Berechung Beschaffungszeit** wird von der Artikelkarte oder der Lagerhaltungsdatenkarte kopiert, wenn die Beschaffungszeit für den Artikel definiert wird, oder auf der Seite **Artikel/Debitoren Katalog**, wenn die Beschaffungszeit für den Kreditor definiert wird.

## <a name="to-customize-a-calendar" />Einen Kalender individuell anpassen
Die Hauptaufgabe beim Anpassen eines Basiskalenders für Ihre Firma oder einen Ihrer Geschäftspartner ist, alle Änderungen am Status der Daten als freie Tage oder Arbeitstage einzugeben.

Während ein Basiskalender z. B. alle Samstage als freie Tage auflistet, kann der spezifische Kalender für einen bestimmten Lagerort alle Samstage in den Monaten November und Dezember als arbeitsfreie Tage führen.

Die folgende Vorgehensweise verwendet den Fall eines Lagerortes als Beispiel. Beachten Sie, dass Sie dem Lagerort zu diesem Zeitpunkt bereits einen Basiskalender zugeordnet haben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Lagerorte** ein, und wählen Sie dann den entsprechenden Link.
2. Öffnen Sie den Lagerort, den Sie aktualisieren möchten, und wählen Sie das Feld **Spezifischer Kalender** aus. Beachten Sie, dass ein Kalender im Feld **Basiskalendercode** ausgewählt werden muss.
3. Auf der Seite **Spezifische Kalenderposten** wählen Sie **Spezifische Kalenderänderungen verwalten** Aktion aus.
4. In **Spezifische Kalenderänderungen** fügen Sie Zeilen für spezifische Kalenderposten hinzu.

    Wenn Sie eine Zeile eingeben, wird das Feld **Frei** ausgewählt. Sie können das Häkchen entfernen, wenn Sie den Status auf den eines Arbeitstags setzen möchten.

    Sie können das Feld **Wiederholungsmuster** verwenden, um ein bestimmtes Datum als einen wiederkehrenden freien Tag einzurichten. Sie können das Wiederholungsmuster **Jährlich** oder **Wöchentlich** wählen.

    Wenn Sie **Jährlich** wählen, müssen Sie auch das relevante Datum im Feld **Datum** eingeben. Wenn Sie **Wöchentlich** wählen, müssen Sie auch im Feld **Tag** den relevanten Wochentag wählen. Wenn Sie das Feld leer lassen, müssen Sie das Feld **Datum** ausfüllen. Das Feld **Tag** wird dann automatisch ausgefüllt. Dies kann hilfreich sein, wenn Sie ein individuelles Datum als einen freien Tag (oder einen Arbeitstag) kennzeichnen möchten.

5. Wählen Sie die Schaltfläche **OK** aus.

Auf der Seite **Spezifische Kalenderposten** werden Sie feststellen, dass die Datumsangaben Ihren Einträgen entsprechend aktualisiert wurden.

Auf der Lagerortkarte werden Sie sehen, dass das Feld **Spezifischer Kalender** das Wort **Ja** enthält, wodurch angezeigt wird, dass ein spezifischer Kalender eingerichtet worden ist.

> [!Important]
> Wenn Sie das Feld **Lagerortcode** in einer Auftragszeile nicht ausfüllen, wird der Kalender Ihrer Firma verwendet.


Wenn Sie das Feld **Spediteurcode** in einer Auftragszeile nicht ausfüllen, wird der Kalender Ihrer Firma verwendet.

> [!NOTE]  
> Wenn Sie an einem Basiskalender Änderungen vornehmen, für den ein spezifischer Kalender existiert, werden automatisch auch alle bestehenden spezifischen Kalender aktualisiert.

## <a name="to-assign-a-base-calendar" />Einen Basiskalender zuordnen
Das folgende Vorgehen plant Lieferdaten in Verkaufsauftragszeilen für einen Debitoren als Beispiel.

Basiskalender werden Ihrer eigenen Firma, Debitoren, Kreditoren, Lagerorten und Spediteurn zugeordnet, wie folgt:  

-   Auf den Karten **Firmendaten** und **Debitor** wird der Basiskalender im Inforegister **Lieferung** zugewiesen.  
-   Klicken Sie auf der Karte **Kreditor** wird der Basiskalender im Inforegister **Lieferung** zugewiesen.  
-   Klicken Sie auf der Karte **Lagerort** wird der Basiskalender im Inforegister **Logistik** zugewiesen.  
-   Auf der Seite **Spediteur** wird der Basiskalender im Fenster **Spediteurtransportarten** zugeordnet.  

1.  Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Debitor** ein und wählen Sie dann den entsprechenden Link.  
2.  Öffnen Sie die **Debitorenkarte**, für der Sie einen Basiskalender zuordnen möchten.  
3.  Wählen Sie im Inforegister **Lieferung** im Feld **Basiskalendercode** den Basiskalender aus, den Sie zuordnen möchten.  

> [!IMPORTANT]  
>  -   Wenn Sie einem Unternehmen keinen Basiskalender zuordnen, werden alle Tage als Arbeitstage berechnet.  
> -   Wenn Sie den Lagerort "Leer" in einer Auftragszeile eingeben, werden alle Tage als Arbeitstage berechnet.  
> -   Alle Basiskalender, die für den Kreditor oder Lagerort definiert wurden, wirken sich darauf aus, wie die Daten in Arbeitstage berechnet und gerundet werden.

> [!NOTE]  
>  Bevor Sie einen spezifischen Kalender anlegen können, müssen Sie zuerst der Firma einen Basiskalender zuordnen.  

## <a name="see-also" />Weitere Informationen
[Einkauf](purchasing-manage-purchasing.md)  
[Bearbeitungen](production-manage-manufacturing.md)    
[Bestand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
