---
title: Einem Lieferanten eine Prioritätsstufe zuweisen (enthält ein Video)
description: 'Sie können sowohl Zahlen Ihren Kreditoren oder Lieferanten zuweisen, um sie zu priorisieren und Zahlungsvorschläge in  Business Central zu erleichtern.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'supplier, payment priority'
ms.search.form: '26, 27'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="prioritize-vendors" />Kreditoren priorisieren

[!INCLUDE[prod_short](includes/prod_short.md)] kann verschiedene Zahlungen an Kreditoren vorschlagen. Dies können z. B. Zahlungen sein, die in Kürze fällig sind, oder Zahlungen, bei denen Sie einen Rabatt erhalten können. Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).

Zuerst müssen Sie den Kreditoren priorisieren, indem Sie ihm Nummern zuweisen.
<br><br>
> [!Video https://www.microsoft.com/videoplayer/embed/RE3PRGa?rel=0]

## <a name="to-prioritize-vendors" />So priorisieren Sie Kreditoren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") Symbol. Geben Sie **Kreditoren** ein und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die entsprechende Kreditor, und klicken Sie dann auf **Bearbeiten**.
3. Geben Sie im Feld **Priorität** eine Zahl ein.

[!INCLUDE[prod_short](includes/prod_short.md)] geht davon aus, dass die niedrigsten Nummern (ausser 0) die höchste Priorität haben. Wenn Sie also z. B. 1, 2 und 3 verwenden, erhält 1 die höchste Priorität.

Falls Sie einem Kreditor keine Priorität zuweisen wollen, lassen Sie das Feld **Priorität** leer. Wenn Sie dann die Funktion "Zahlungsvorschlag" verwenden, wird dieser Kreditor nach den Kreditoren aufgeführt, die eine Priorität haben. Sie können so viele Prioritäten einrichten wie Sie benötigen.

## <a name="see-also" />Siehe auch

[Registriert einen neuen Kreditor](purchasing-how-register-new-vendors.md)  
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
