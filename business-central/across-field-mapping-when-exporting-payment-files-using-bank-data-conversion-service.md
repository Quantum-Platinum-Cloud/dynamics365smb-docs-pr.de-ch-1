---
title: Feldzuordnung für den Export von Bankzahlungsdateien | Microsoft Docs
description: 'Wenn Sie Zahlungsdateien mit der AMC Banking 365 Fundamentals-Erweiterung exportieren, werden die von Ihnen exportierten Daten dem Dienstanbieter zugänglich gemacht.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="field-mapping-when-exporting-payment-files-using-the-amc-banking-365-fundamentals-extension" />Feldzuordnung beim Export von Zahlungsdateien mit der AMC Banking 365 Fundamentals-Erweiterung
Wenn Sie Zahlungsdateien mit der AMC Banking 365 Fundamentals-Erweiterung exportieren, werden die von Ihnen exportierten Daten dem Dienstanbieter zugänglich gemacht. Der Dienstanbieter ist für den Schutz dieser Daten verantwortlich. Weitere Informationen zur AMC Banking 365 Fundamentals-Erweiterung finden Sie unter [Die AMC Banking 365 Fundamentals-Erweiterung verwenden](ui-extensions-amc-banking.md).  

> [!CAUTION]  
>  Wenn Sie Zahlungsdateien mit der AMC Banking 365 Fundamentals-Erweiterung exportieren, werden einige Ihrer Geschäftsdaten dem Anbieter des Dienstes zugänglich gemacht. Der Dienstanbieter, AMC Consult A/S, ist für den Schutz dieser Daten verantwortlich. Weitere Informationen finden Sie unter [AMC-Datenschutzrichtlinie](https://go.microsoft.com/fwlink/?LinkId=510158).  

> [!NOTE]
> In der generischen Version von [!INCLUDE[prod_short](includes/prod_short.md)]  wird ein globaler Diensteanbieter eingerichtet und verbunden, der Bankdaten in das Dateiformat konvertiert, das Ihre Bank verlangt. In den nordamerikanischen Versionen kann derselbe Dienst verwendet werden, um Zahlungsdateien als Electronic Funds Transfer (EFT) zu senden, z.B. über das allgemein verwendete Automated Clearing House (ACH) Netzwerk, allerdings mit einem etwas anderen Verfahren.

Die folgende Tabelle listet die Felder in [!INCLUDE[prod_short](includes/prod_short.md)] auf, aus denen Sie Daten exportieren können.  

|Zugeordnetes Feld|Feld in Tabelle|Tabelle|Beschreibung|  
|------------------|--------------------|-----------|---------------------------------------|  
|Gläubiger-Identifikationsnummer|Gläubiger-Identifikationsnummer|Bankkonto|Die Identifikationsnummer, die Ihrem Unternehmen von Ihrer Bank zugeordnet wurde, um Zahlungen zu erfassen|  
|Bankkontonr. des Absenders|Bankkontonummer/IBAN|Bankkonto|Die Kontonummer (IBAN oder sonstige) Ihres Unternehmens, die auf der Bankkontokarte angegeben ist|  
|Absenderbank-Clearing-Standard|Bank-Clearing-Standard|Bankkonto|Das Nationale Register der Banknamen für das Bankkonto des Absenders|  
|Clearing-Code Absenderbank|Bank-Clearing-Code|Bankkonto|Die Identifikationsnummer Bank des Absenders in Bezug auf das Bankadressenregister, das verwendet wird|  
|BIC Absenderbank|SWIFT-Code|Bankkonto|Die SWIFT-Kennung des Absenderbankkontos.|  
|Kontowährung der Absenderbank|Währungscode|Bankkonto|Der Währungscode der Absenderbank|  
|Belegnr.|Belegnr.|Fibu Erf.-Journalzeile|Die Belegnummer der Zahlungszeile|  
|Ausgleich ext. Belegnr.|Ausgleich ext. Belegnr.|Fibu Erf.-Journalzeile|Die Nummer des externen Belegs, der Rechnung oder Gutschrift, mit der die Zahlungszeile ausgeglichen werden soll.|  
|Empfänger-ID|Kontonummer|Fibu Erf.-Journalzeile|Die Nummer des Debitors oder Kreditors, die auf der Zahlungszeile angegeben ist|  
|Zahlungsart|Zahlungstyp Bankdatenkonvertierung|Zahlungsform|Die Art des Banktransfers, wie Inland oder International|  
|Zahlungsreferenz|Zahlungsreferenz|Fibu Erf.-Journalzeile|Die Zahlungsreferenz der Zahlungszeile|  
|Adresse des Empfängers|Adresse|Debitor/Kreditor|Die Empfängeradresse, die auf der Debitoren- oder Kreditorenkarte angegeben ist|  
|Ort des Empfängers|Ort|Debitor/Kreditor|Die Stadt, die auf der Debitoren- oder Kreditorenkarte angegeben ist|  
|Name des Empfängers|Name|Debitor/Kreditor|Die Empfängername, der auf der Debitoren- oder Kreditorenkarte angegeben ist|  
|Landes-/Regionscode Empfänger|Länder-/Regionscode|Debitor/Kreditor|Der Länder-/Regionencode des Bankkontos des Empfängers, der auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|PLZ-Code Empfänger|PLZ|Debitor/Kreditor|Die Postleitzahl des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Bankkontonr. Empfänger|Bankkontonummer/IBAN|Debitorenbankkonto/Kreditorenbankkonto|Die Nummer (IBAN oder sonstige) des Bankkontos des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Clearing-Code Empfängerbank|Bank-Clearing-Standard|Debitorenbankkonto/Kreditorenbankkonto|Das Nationale Register der Banknamen für das Bankkonto des Empfängers|  
|Clearing-Standard Empfängerbank|Bank-Clearing-Code|Debitorenbankkonto/Kreditorenbankkonto|Die Identifikationsnummer des Empfänger-Bankkontos in Bezug auf das Bankadressenregister, das verwendet wird|  
|E-Mail-Adresse Empfänger|E-Mail|Debitor/Kreditor|Die E-Mail-Adresse des Empfängers.|  
|Nachricht an Empfänger 1|Nachricht an Empfänger|Fibu Erf.-Journalzeile|Die Meldung an den Empfänger, die in der Zahlungszeile angegeben ist|  
|Betrag|Betrag|Fibu Erf.-Journalzeile|Der Betrag auf der Zahlungszeile|  
|Währungscode|Währungscode|Fibu Erf.-Journalzeile|Der Währungscode auf der Zahlungszeile.|  
|Lastschriftdatum|Buchungsdatum|Fibu Erf.-Journalzeile|Das Buchungsdatum der Zahlungsposition.|  
|Fakturierter Betrag|Ursprungsbetrag|Debitoren-/Kreditorenposten|Der Betrag in dem Eintrag, auf den die Zahlung angewendet wird.|  
|Rechnungsdatum|Belegdatum|Debitoren-/Kreditorenposten|Der Rechnungsbetrag in dem Eintrag, auf den die Zahlung angewendet wird.|  
|Adresse Empfängerbank|Adresse|Debitorenbankkonto/Kreditorenbankkonto|Die Bankkontoadresse des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Die Bankkontoadresse des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|Ort|Debitorenbankkonto/Kreditorenbankkonto|Die Stadt des Bankkontos des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Name Empfängerbank|Name|Debitorenbankkonto/Kreditorenbankkonto|Der Name des Bankkontos des Empfängers, der auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Land/Region Empfängerbank|Länder-/Regionscode|Debitorenbankkonto/Kreditorenbankkonto|Das Land/Die Region des Bankkontos des Empfängers, das auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|PLZ-Code Empfängerbank|PLZ|Debitorenbankkonto/Kreditorenbankkonto|Die Postleitzahl des Bankkontos des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist|  
|Adresse Absenderbank|Adresse|Bankkonto|Die Absenderbankkontoadresse, die auf der Bankkontokarte angegeben ist|  
|Ort Absenderbank|Ort|Bankkonto|Die Absenderbankkontostadt, die auf der Bankkontokarte angegeben ist|  
|Name der Absenderbank|Name|Bankkonto|Der Absenderbankkontoname, der auf der Bankkontokarte angegeben ist|  
|Land/Region Absenderbank|Länder-/Regionscode|Bankkonto|Das Land/Die Region des Absenderbankkontos, das/die auf der Bankkontokarte angegeben ist|  
|PLZ-Code Absenderbank|PLZ|Bankkonto|Der Absenderbankkonto-PLZ-Code, der auf der Bankkontokarte angegeben ist|  
|Fibu Erf.-Journalvorlage|Erf.-Journalvorlagenname|Fibu Erf.-Journalzeile|Die Fibu Erf.-Journalvorlage, die für die Zahlungszeile verwendet wird|  
|Fibu Erf.-Journalname|Erf.-Journalname|Fibu Erf.-Journalzeile|Der Fibu Erf.-Journal-Erf.-Journal, das für die Zahlungszeile verwendet wird|  
|Name der Absenderbank – Datenkonvertierung|Bankname – Datenkonv.|Bankkonto|Der Name des Absenderbankkontos, der von der AMC Banking 365 Fundamentals-Erweiterung angefordert und auf der Bankkarte angegeben wird.|  

## <a name="see-also" />Siehe auch
[Einrichten eines Datenaustauschs](across-set-up-data-exchange.md)  
[Daten elektronisch austauschen](across-data-exchange.md)
[Die AMC Banking 365 Fundamentals-Erweiterung verwenden](ui-extensions-amc-banking.md)   
[Zahlungen mit der AMC Banking 365 Fundamentals-Erweiterung oder per SEPA-Überweisung vornehmen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
