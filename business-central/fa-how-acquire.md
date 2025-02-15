---
title: Erworbene Anlagen
description: 'Sie können Anlagen einrichten, ein Abschreibungsbuch zuweisen und Anlagen-Anschaffungskosten aufzeichnen.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 12/03/2021
ms.author: edupont
---
# <a name="acquire-fixed-assets" />Erworbene Anlagen

Sie müssen für jede Anlage eine Karte mit den entsprechenden Informationen über die Anlage einrichten. Sie können Gebäude oder Produktionseinrichtungen als Hauptanlage mit einer Komponentenliste einrichten und sie unterschiedlich gruppieren, z. B. nach Klasse, Abteilung oder Standort. Vor der Anschaffung muss für jede Anlage ein Abschreibungsbuch eingerichtet und zugewiesen werden.

Wenn eine Anlage eingerichtet und ein Abschreibungsbuch zugewiesen ist, müssen Sie die Anlage erwerben. Um eine Anlage zu erwerben, erfassen Sie ihre Anschaffungskosten im entsprechenden Fibukonto, Bankkonto oder Kreditor, indem Sie eine Anschaffungstransaktion auf der Seite **Anlagen Fibu Erf.-Journal** buchen. Sie können die Seite **Unterstützte Anlagenanschaffung** verwenden, um die erforderlichen Fibu Erfassungsjournalzeilen automatisch zu erstellen und zu buchen.

Der Restwert ist der verbleibende Wert einer Anlage, die nicht mehr verwendet werden kann. Sie können den Restbetrag zusammen mit den Anschaffungskosten buchen. Weitere Informationen finden Sie unter [Anlagen abschreiben oder amortisieren](fa-how-depreciate-amortize.md).

Die Indexierung wird verwendet, um die Werte allgemeinen Preisänderungen anzupassen. Die Stapelverarbeitung **Anlagen indexieren** kann verwendet werden, um die Anschaffungskosten zu Wiederbeschaffungskosten zu ermitteln.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically" />So erstellen Sie eine Anlage und erwerben diese automatisch

Nachfolgend wird beschrieben, wie eine Anlage erstellt und erhalten wird, indem Sie die Seite **Unterstützte Anlagenanschaffung** verwenden, um die entsprechenden Fibu Erfassungsjournalzeilen zu erstellen und zu buchen. Sie können die Erfassungsjournalzeilen auch manuell erstellen und buchen. Weitere Informationen finden Sie unter [Wie Anlagenanschaffungen mit dem Anlagen Fibu Erf.-Journal manuell gebucht werden](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.  
2. Wählen Sie die Aktion **Neu** aus, und füllen Sie dann bei Bedarf die Felder im Inforegister **Allgemein** aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Füllen Sie im Inforegister **AfA-Buch** die Felder nach Bedarf aus. Dieser Schritt weist eine Anlage einem Abschreibungsbuch zu.  
4. Wenn Sie mehrere Abschreibungsbücher der Anlage zuweisen müssen, wählen Sie die Aktion **Weitere Abschreibungsbücher hinzufügen** aus. Weitere Informationen finden Sie unter [So weisen Sie ein Abschreibungsbuch einer Anlage zu](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Wenn alle Felder, die benötigt werden, um eine Anlage zu erwerben, ausgefüllt sind, erscheint oben auf der Seite die Benachrichtigung **Sie sind bereit, die Anlage zu erwerben**.
5. Wählen Sie Aktion **Erwerben** in der Benachrichtigung aus.
6. Befolgen Sie die Schritte auf der Seite **Unterstützte Anlagenanschaffung** Fenster, um die automatische Beschaffung der Anlage abzuschliessen.

> [!NOTE]  
>   Sie können Anchaffungskosten auch als auch Habenbeträge buchen. In diesem Fall sollten Sie daran denken, dass der Wert im Feld **Anschaffungskosten inklusive MwSt** mit einem Minuszeichen eingegeben werden muss, um eine Gutschrift anzugeben.

Wenn Sie **Fertigstellen** auswählen, wird das Feld **Buchwert** im Fenster **Anlagenkarte** ausgefüllt und gibt an, dass die Anlage zu den angegebenen Anschaffungskosten erworben wurde.  

## <a name="to-set-up-a-component-list-for-a-main-asset" />So richten Sie Komponentenlisten für Hauptanlagen ein

Sie können Ihre Anlagen in Hauptanlagen und deren Komponenten gliedern. Sie können dies z. B. für eine Produktionsanlage verwenden, die aus vielen Teilen besteht, die auf diese Weise gruppiert werden sollen.  

Sowohl für die Hauptanlage als auch für die Unteranlagen müssen Anlagenkarten eingerichtet werden. Nachdem Sie eine Komponentenübersicht eingerichtet haben, füllt [!INCLUDE[prod_short](includes/prod_short.md)] automatisch die Felder **Hauptanlage/Komponente** und **Komponente/Hauptanlage** auf den Anlagenkarten aus.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlagen** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Anlage, die die Hauptanlage ist, und wählen die Aktion **Hauptanl. Unteranlagen** aus.
3. auf der Seite **Unteranlagen** wählen Sie **Anlagennr.** aus und wählen Sie die Anlage aus, die Sie als Komponente der Hauptanlage hinzufügen möchten.
4. Schliessen Sie die Seite.
5. Wiederholen Sie die Schritte 3 und 4 für jede Unteranlage, die Sie hinzufügen möchten.
6. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Anlageneinrichtung** ein und wählen Sie dann den entsprechenden Link.
7. Aktivieren Sie das Kontrollkästchen **Buchen auf Hauptanl. erlaubt**.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal" />So buchen Sie eine Anlagenanschaffungen mit dem Anlagen Fibu Erf.-Journal manuell

Nachfolgend wird beschrieben, wie eine Anlage manuell erworben wird, indem Zeilen auf der Seite **Anlagen Fibu Erf.-Journal** erstellt und gebucht werden. Sie können eine Anlage auch automatisch erwerben, indem Sie die Seite **Unterstützte Anlagenanschaffung** verwenden. Weitere Informationen finden Sie unter Schritt 5 in [So erstellen Sie eine Anlage und erwerben diese automatisch](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically).

> [!NOTE]  
>   Sie können Anchaffungskosten auch als auch Habenbeträge buchen. In diesem Fall sollten Sie daran denken, dass der Wert im Feld **Betrag** mit einem Minuszeichen eingegeben werden muss, um eine Gutschrift anzugeben.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagen Fibu Erfassungsjournale** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Anlagen Fibu Erf.-Journal** wählen Sie im Feld **Anlagenbuchungsart** die **Anschaffungskosten** aus.
3. Füllen Sie die verbleibenden Felder je nach Bedarf aus.
4. Wählen Sie die Aktion **Buchen** aus.  

> [!TIP]  
>   Wenn Sie bei der Buchung von Anschaffungskosten im Anlagen Fibu Erf.-Journal das Feld **Versicherungsnr.** ausfüllen, bucht [!INCLUDE[prod_short](includes/prod_short.md)] die Anwendung die Anschaffungskosten der Anlage auch für die Versicherungsposten. Weitere Informationen finden Sie unter [Versichern von Anlagen](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset" />So stornieren Sie eine Anschaffungskostenbuchung für eine Anlage

Wenn Ihnen beim Buchen von Anschaffungskosten ein Fehler unterläuft, können Sie den Posten mithilfe der Stapelverarbeitung **Anlagenposten storn.** entfernen und anschliessend den korrekten Anschaffungsposten buchen. Die fehlerhaften Posten werden in die Seite **Anlagenstornoposten** übertragen.

Wenn Sie also beispielsweise eine Anschaffung mit dem falschen Datum gebucht haben, müssen Sie sie so schnell wie möglich korrigieren, da das Anlagenbuchungsdatum für viele Berechnungen verwendet wird.

> [!IMPORTANT]  
> Sie können die Funktion **Transaktion stornieren** nicht für Anlagenposten verwenden.

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") aus, geben Sie **Anlagenposten** ein, und wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie auf der Seite **Anlagenposten** den/die zu stornierenden Einträge aus.  
3. Wählen Sie das Menü **Aktionen** und dann die Aktion **Posten stornieren** aus.
4. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Wählen Sie die Schaltfläche **OK**, um den Batchauftrag zu starten.
6. Wenn der falsche Posten oder die falschen Posten storniert wurden, können Sie mit dem Buchen der korrekten Anschaffungskosten fortfahren.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost" />So buchen Sie den Restbetrag zusammen mit den Anschaffungskosten

Sie können den Restwert zusammen mit den Anschaffungskosten aus einem Anlagen Erf.-Journal buchen.

> [!NOTE]
> Dieser Prozess erfordert möglicherweise, dass Sie die Seite Anlagenbuchhaltung personalisieren, indem Sie das Feld Restwert hinzufügen. Das Feld An wird auf der Seite standardmässig nicht angezeigt. Weitere Informationen finden Sie unter [Personalisieren Sie Ihren Arbeitsbereich](ui-personalization-user.md).

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell Me-Funktion") Symbol. Geben Sie **Anlagen-Erfassungsjournale** ein, und wählen Sie dann den zugehörigen Link.
2. Auf der Seite **Anlagen Erfassungsjournale** erstellen Sie die Anschaffungszeile. Weitere Informationen finden Sie unter [Wie Anlagenanschaffungen mit dem Anlagen Fibu Erf.-Journal manuell gebucht werden](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).
3. Geben Sie im Feld **Restwert** in der Rechnungszeile den Restwertbetrag als Haben (Betrag mit einem Minuszeichen, z. B. **-** 100) ein.
4. Wählen Sie die Aktion **Buchen** aus.

> [!NOTE]
> Wenn für eine Anlage ein Restwert vorhanden ist, wird dieser Wert bei der Abschreibungsbuchung anstelle des Wertes im Feld **Erinnerungswert** auf der Seite **Anlagenabschreibungsbücher** verwendet. Weitere Informationen finden Sie unter [Wie der Erinnerungswert verwaltet wird](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-related-microsoft-trainingtrainingmodulespurchase-fixed-assets" />Siehe verwandte [Microsoft Schulungen](/training/modules/purchase-fixed-assets/)

## <a name="see-also" />Siehe auch

[Anlagen](fa-manage.md)  
[Anlagen einrichten](fa-setup.md)  
[Finanzen](finance.md)  
[Vorbereitungen zum Tätigen von Geschäften](ui-get-ready-business.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
