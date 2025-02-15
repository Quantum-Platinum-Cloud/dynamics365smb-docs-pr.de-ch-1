---
title: Übersicht der Aufgaben zur Verwaltung von Debitoren
description: In diesem Thema werden Aufgaben zur Verwaltung von Debitoren und zur Anwendung von Zahlungen auf Debitoren- oder Kreditor-Sachkonto-Einträge beschrieben.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customer payment, debtor, balance due, AR'
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="managing-receivables" />Debitoren verwalten

Ein regelmässiger Schritt in jedem Finanzrhythmus ist, Bankkonten abzustimmen, die es erfordern, dass Sie Zahlungen mit Debitoren- oder Kreditorenposten ausgleichen, um Verkaufsrechnungen und - gutschriften zu schliessen.

Da die meisten Debitoren in B2B-Umgebung einige Zeit nach der Lieferung bezahlen, lassen Sie die gebuchten Verkaufsrechnungen geöffnet für die Debitorenabteilung, um sie zu beenden, wenn die Zahlung erfolgt. Einige Verkaufsrechnungen können zum Beispiel mit Paypal sofort bezahlt werden. Solche Rechnungen werden sofort folgendermassen als bezahlt angewendet, wenn sie gebucht werden und werden nicht als Zahlung in der Verarbeitung in AR angezeigt. Weitere Informationen finden Sie unter [Fakturieren eines Verkaufs](sales-how-invoice-sales.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)] ist einer der schnellsten Arten, Zahlungen auf der Seite **Zahlungsabstimmungserf.-Journal** zu erfassen, indem Sie eine Bankauszugsdatei oder einen Feed erfassen. Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten basierend auf Übereinstimmungen zwischen Zahlungstext und Zahlungsinformationen verknüpft werden. Sie können die Suchergebnisse überprüfen und ändern, bevor Sie das Erf.-Journal buchen, und schliessen Bankposten für Posten, wenn Sie das Erf.-Journal buchen. Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.

Andere Seiten gibt es, wo Sie entweder Zahlungen anwenden oder Bankkonten abstimmen können:

* Die Seite **Bankkontoabstimmung**, in dem Sie Bankkonten abstimmen, indem Sie Bankkontoauszugszeilen importierten mit Ihren Systembankposten. Hier können Sie auch Scheckzahlungen ausgleichen. Weitere Informationen finden Sie unter [Abstimmen von Bankkonten](bank-how-reconcile-bank-accounts-separately.md). Hier können Sie Zahlungen nicht übernehmen.
* Die Seite **Zahlungs-Registrierung**, wo Sie manuell Zahlungseingänge wie Kasse, Scheck oder Bankbuchung für eine generierte Liste der unbezahlten Verkaufsbelege überprüfen können. Beachten Sie, dass diese Funktionen nur für Verkaufsbelege verfügbar sind. Hier können Sie ausgehende Zahlungen nicht übernehmen, und Sie können keine Bankkonten abstimmen.
* Die Seite **Zahlungseingangserf.-Journal**, in der Sie manuell Belege der relevanten Fibukonten, Debitoren oder anderer Konten durch Eingabe einer Zahlungsposition buchen können. In diesem Fall können Sie entweder den Wareneingang oder die Rückerstattung mit einem oder mehreren offenen Posten anwenden, bevor Sie das Zahlungseingangs Erf.-Journal buchen, oder Sie können sie aus den erstellten Debitorenposten erstellen. Hier können Sie Bankkonten nicht ausgeglichen.

Die Seite **Zahlungsabstimmungserf.-Journal** verwendet eine automatische Abgleichslogik, die Sie auf der Seite **Zahlungsausgleichsvorschriften** einrichten können. Weitere Informationen finden Sie unter [Einrichten von Regeln für die automatische Anwendung von Zahlungen](receivables-how-set-up-payment-application-rules.md).  

Andere Aspekte der Verwaltung von Forderungen umfassen die Erfassung offener Salden, einschliesslich Zinsrechnungen und Mahnungen und die Einrichtung von Bankkonten, damit Zahlungen von Debitoren automatisch von ihren Konten abgehoben werden können.

In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.  

| Aktion | Informationen |
| --- | --- |
| Zahlungen verwenden, um Debitoren- oder Kreditorenposten zu öffnen, indem Sie einen Bankkontoauszug importieren und das Bankkonto abstimmen, wenn alle Zahlungen ausgeglichen werden. |[Zahlungen automatisch vornehmen und Bankkonten abstimmen](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| Wenden Sie Zahlungen auf offene Debitorenposten basierend auf einer Liste der unbezahlten Verkaufsbelege auf der Seite**Zahlungs-Registrierung** an. |[Debitoren-Zahlungen aus einer Liste mit unbezahlten Verkaufsbelegen abstimmen](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| Buchen Sie Zahlungseingänge oder Erstattungen für Debitoren im Zahlungseingangs Erfassungsjournal für Debitorenposten, entweder aus dem Erfassungsjournal oder von gebuchten Posten. |[Abstimmen von Debitoren-Zahlungen mit dem Zahlungseingangs Erf.-Journal oder von Debitorenposten](receivables-how-apply-sales-transactions-manually.md) |
| Erinnern von Debitoren an überfällige Beträge, Berechnen von Zinsen und Gebühren sowie Verwalten von Debitoren |[Einziehen von Restbeträgen](receivables-collect-outstanding-balances.md) |
|Mit Zustimmung Ihres Kunden können Sie Zahlungen direkt vom Bankkonto des Kunden nur in Schweizer Frankenpäischen Währung einziehen.|[Erfassen von Zahlungen per Lastschriftverfahren SEPA](finance-collect-payments-with-sepa-direct-debit.md)|
|Sperren Sie einen Debitor, so dass er nicht in Belege oder für das Buchen eingegeben werden kann, zum Beispiel aufgrund von Zahlungsunfähigkeit.|[Debitoren sperren](receivables-how-block-customers.md)|
|Einrichtung einer Toleranz, mit der das System eine Rechnung schliesst, selbst wenn die Zahlung einschliesslich aller Rabatte nicht vollständig den Betrag der Rechnung abdeckt.|[Arbeiten mit Zahlungstoleranzen und Skontotoleranzen](finance-payment-tolerance-and-payment-discount-tolerance.md)|
| Sagen Sie voraus, wenn Zahlungen für Verkaufsbelege zu spät geleistet werden. | [Die Erweiterung zur Vorhersage verspäteter Zahlungen](ui-extensions-late-payment-prediction.md) |

## <a name="see-related-microsoft-trainingtrainingpathsprocess-customer-vendor-payments-dynamics-365-business-central" />Siehe verwandte [Microsoft Schulungen](/training/paths/process-customer-vendor-payments-dynamics-365-business-central/)

## <a name="see-also" />Siehe auch
[Verkauf](sales-manage-sales.md)  
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
