---
title: Rapporto liquidazione PayPal
description: Scopri il rapporto Pagamento PayPal come strumento per gestire le transazioni PayPal.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Rapporto liquidazione PayPal

Il rapporto PayPal Settlement fornisce agli esercenti le informazioni su ogni transazione che influisce sulla liquidazione dei fondi.

>[!NOTE]
>
>Prima di generare rapporti di liquidazione, l&#39;amministratore del negozio deve richiedere a PayPal Merchant Technical Services di creare un account utente SFTP, abilitare la generazione di rapporti di liquidazione e abilitare SFTP nel proprio account aziendale PayPal.

Dopo aver configurato e abilitato i rapporti di liquidazione nel conto dell&#39;esercente PayPal, Adobe Commerce e Magento Open Source inizieranno a generare rapporti nelle 24 ore successive. L&#39;elenco dei rapporti di liquidazione disponibili può essere visualizzato dall&#39;amministratore.

**_Per visualizzare i report di liquidazione:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

   ![Report liquidazioni PayPal](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. Per gli aggiornamenti più recenti, fare clic su **[!UICONTROL Fetch Updates]** nell&#39;angolo superiore destro.

   Il sistema si connette al server SFTP PayPal per recuperare i rapporti. Al termine del processo, viene visualizzato un messaggio con il numero di rapporti recuperati. Il rapporto include le seguenti informazioni per ciascuna transazione:

   | Colonna report | Descrizione |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | Uno dei seguenti codici di riferimento:<br/>- Order IDT<br/>- Transaction ID<br/>- Subscription ID |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - Testo immesso dal commerciante nella transazione su PayPal.<br/>**[!UICONTROL Transaction Debit or Credit]**- Direzione del movimento di denaro dell&#39;importo lordo.<br/>**[!UICONTROL Fee Debit or Credit]** - Direzione del movimento di denaro a pagamento. |

   {style="table-layout:auto"}
