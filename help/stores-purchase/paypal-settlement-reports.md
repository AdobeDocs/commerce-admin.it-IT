---
title: Rapporto liquidazione PayPal
description: Scopri il rapporto Pagamento PayPal come strumento per gestire le transazioni PayPal.
exl-id: cd087e15-e6ad-4472-9038-8c64fde316f9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---

# Rapporto liquidazione PayPal

Il rapporto PayPal Settlement fornisce agli esercenti le informazioni su ogni transazione che influisce sulla liquidazione dei fondi.

>[!NOTE]
>
>Prima di generare rapporti di liquidazione, l&#39;amministratore del negozio deve richiedere a PayPal Merchant Technical Services di creare un account utente SFTP, abilitare la generazione di rapporti di liquidazione e abilitare SFTP nel proprio account aziendale PayPal.

Dopo aver configurato e abilitato i rapporti di liquidazione nel conto dell&#39;esercente PayPal, Adobe Commerce e Magento Open Source inizieranno a generare rapporti nelle 24 ore successive. L&#39;elenco dei rapporti di liquidazione disponibili può essere visualizzato dall&#39;amministratore.

**_Per visualizzare i rapporti di liquidazione:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

   ![Rapporti di liquidazione PayPal](../getting-started/assets/reports-sales-paypal-settlement.png){width="600" zoomable="yes"}

1. Per gli aggiornamenti più recenti, fai clic su **[!UICONTROL Fetch Updates]** nell’angolo superiore destro.

   Il sistema si connette al server SFTP PayPal per recuperare i rapporti. Al termine del processo, viene visualizzato un messaggio con il numero di rapporti recuperati. Il rapporto include le seguenti informazioni per ciascuna transazione:

   | Colonna report | Descrizione |
   | ------------ | ----------- |
   | [!UICONTROL PayPal Reference ID Type] | Uno dei seguenti codici di riferimento:<br/>- Ordine IDT<br/>- ID transazione<br/>- ID abbonamento |
   | [!UICONTROL Preapproved Payment ID] | **[!UICONTROL Custom]** - Il testo immesso dall&#39;esercente sulla transazione in PayPal.<br/>**[!UICONTROL Transaction Debit or Credit]**- La direzione del movimento di denaro di importo lordo.<br/>**[!UICONTROL Fee Debit or Credit]** - La direzione del movimento di denaro a pagamento. |

   {style="table-layout:auto"}
