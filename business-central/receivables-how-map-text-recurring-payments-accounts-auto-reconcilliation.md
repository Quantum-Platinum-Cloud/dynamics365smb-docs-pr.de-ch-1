---
title: Text-zu-Kontenzuordnung für wiederkehrende Zahlungen einrichten
description: 'Verknüpfen Sie Text für Zahlungen mit bestimmten Konten, so dass Zahlungen auf die Konten gebucht werden, wenn Sie das ZahlungsabstimmungsErf.-Journal buchen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation" />Zuordnen von Text auf sich wiederholenden Zahlungen an Konten für automatische Abstimmung

Im Fenster **Zuordnung Text zu Konto**, das Sie auf der Seite **Zahlungsabstimmungserf.-Journal** öffnen, können Sie schnell Zuordnungen zwischen Text in Zahlungen und bestimmten Soll-, Haben- und Gegenkonten eingeben, sodass solche Zahlungen auf die angegebenen Konten gebucht werden, wenn Sie Zahlungen im Zahlungsabstimmungserf.-Journal buchen.

Ähnliche Funktionen sind vorhanden, um Mehrbeträge auf Zahlungsabstimmungserf.-Journalzeilen fallweise abzustimmen. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Zuordnung](receivables-how-reconcile-payments-cannot-apply-auto.md).

Die Zahlungen, die anhand der Text-zu-Kontenzuordnung gebucht wurden, werden nicht auf offene Einträge angewendet, sondern sie werden nur für die angegebenen Konten sowie das Erstellen von Bankposten gebucht. Entsprechend eignet sich die Text-zu-Konto-Zuordnung für wiederkehrende Zahlungseingänge oder Ausgaben wie häufig auftretende Einkäufe von Autokraftstoff, Bankgebühren und Zinsen, die regelmässig im Bankkontoauszug auftreten und keinen zugehörigen Geschäftsbeleg benötigen. Weitere Informationen finden Sie im Abschnitt „Beispiel – Zuordnung Text zu Konto für Kraftstoffausgaben“ in diesem Thema.

> [!NOTE]  
>   Zahlungen auf Abstimmungsbuch.-Blattzeilen werden nur dann für das Buchen entsprechend der Text-zu-Kontenzuordnung festgelegt, wenn die automatische Anwendungsfunktion lediglich ein Abgleichungsvertrauen zwischen **Niedrig**und **Normal** zurückgibt. Wenn die automatische Anwendungsfunktion eine Übereinstimmungsgenauigkeit von "Hoch" liefert, wird die Zahlung eines oder mehrerer offener Posten automatisch angewendet, und die Zahlung wird nicht auf die Konten gebucht, die auf der Seite **Zuordnung Text zu Konto** angegeben wurde. Anders ausgedrückt, ein Abgleichungsvertrauen **Hoch** überschreibt eine Text-zu-Konto-Zuordnung.

In einer Zahlungsabstimmungs-Erf.-Journalzeile, in der die Zahlung entsprechend der Text-zu-Kontenzuordnung zur Buchung festgelegt wurde, enthält das Feld **Übereinstimmungsgenauigkeit** **Hoch - Text-Kontozuordnung** und den **Kontenart** und die **Kontennummer**.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation" />Zuordnen von text auf sich wiederholenden Zahlungen an Konten für automatische Abstimmung

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Zahlungsausgangs Erfassungsjournale** ein und wählen Sie dann den zugehörigen Link.
2. Öffnen Sie ein Zahlungsabstimmungserf.-Journal. Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).
3. Wählen Sie die Aktion **Text zu Konto zuordnen**. Die Seite **Text zu Konto zuordnen** öffnet sich.
4. Geben Sie im Feld **Text zuordnen** einen beliebigen Text ein, der in Zahlungen auftritt, die Sie an die angegebenen Konten ohne Anwendung auf einen offenen Posten buchen möchten. Sie können bis zu 50 Zeichen eingeben.

    > [!NOTE]  
    >   Wenn keine anderen Zahlungsbelege mit dem jeweiligen Zuordnungstext vorhanden sind, dann erfolgt die Text-Konto-Zuordnung auch, wenn nur ein Teil des Texts auf den Zahlungsbeleg als Zuordnungstext vorhanden ist.
5. In dem Feld **Kreditorennr.** geben Sie den Kreditor ein, bei dem die Zahlungen gebucht werden.
6. Geben Sie im Feld **Herkunftsart Saldo** an, ob die Zahlung auf ein Sachkonto oder auf ein Debitoren- oder Kreditorenkonto gebucht wird.
7. Im Feld **Saldoquellen-Nr.** definieren Sie das Konto, auf das die Zahlung gebucht wird, abhängig von Ihrer Wahl im Feld **Herkunftsart Saldo**.

    > [!NOTE]
    > Verwenden Sie nicht die Felder **Sollkontonr.** und **Habenkontonr.** in Verbindung mit Zahlungsabstimmung. Sie werden nur für eingehende Belege verwendet. Weitere Informationen finden Sie unter [Verwenden von OCR, um PDF und Bilddateien in elektronische Belege umzuwandeln](across-how-use-ocr-pdf-images-files.md).

8. Wiederholen Sie die Schritte 3 bis 7 für alle Texte auf Zahlungen, die Sie zuordnen möchten, um die entsprechenden Posten direkt, ohne Anwendung, zu buchen.

Beim nächsten Mal, wenn Sie eine Bankkontoauszugsdatei importieren oder die Funktion **Automatisch anwenden** auf der Seite **Zahlungsabstimmungserf.-Journal** wählen, enthalten die Erfassungsjournalzeilen für die Zahlungen, die den angegebenen Zuordnungstext enthalten, die zugehörigen Konten im Feld **Kontoart** und **Kontonummer**. Das Feld **Übereinstimmungsgenauigkeit** enthält **Hoch - Text zu Konto Zuordnung**. Dies ist unter der Bedingung der Fall, dass die automatische Anwendungsfunktion nur ein Abgleichungsvertrauen von **Niedrig** oder **Normal** zur Verfügung stellen kann.

## <a name="example-text-to-account-mapping-for-bank-fees" />Beispiel: Zuordnung Text zu Konto für Bankgebühren

Um Ausgaben, die sich auf Gebühren einer bestimmten Bank, MyBank, beziehen, immer auf das Fibukonto für Bankgebühren und Gebühren (Konto 60400) zu buchen, füllen Sie eine Zeile auf der Seite **Zuordnung Text zu Konto** wie folgt aus.

| Abbildungstext | Sollkontonr. | Habenkontonr. | Herkunftsart Saldo | Herkunftsnr. Saldo |
| --- | --- | --- | --- | --- |
| MyBank |LEER |60400|Fibukonto |LEER |

## <a name="see-related-microsoft-trainingtrainingmodulesuse-journals-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/modules/use-journals-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch

[Verwalten von Forderungen](receivables-manage-receivables.md)  
[Verkauf](sales-manage-sales.md)  
[Den Envestnet Yodlee Bank Feeds Service einrichten](bank-how-setup-bank-statement-service.md)  
[Anpassen [!INCLUDE[prod_short](includes/prod_short.md)] Erweiterungen nutzen](ui-extensions.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
