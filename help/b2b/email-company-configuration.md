---
title: Configurare l’e-mail aziendale
description: Scopri le opzioni e i modelli e-mail utilizzati per inviare comunicazioni per gli account aziendali.
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# Configurare le opzioni e-mail aziendali

Il [rappresentante commerciale](account-company-manage.md) che viene assegnato come contatto principale per una società è configurato per impostazione predefinita come mittente di molti messaggi e-mail automatizzati inviati alla società.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Company Configuration]**.

1. Se necessario, impostare **[!UICONTROL Store View]** nella vista store per definire [ambito](../getting-started/websites-stores-views.md#scope-settings) della configurazione.

1. Completa il **[!UICONTROL Company Registration]** sezione:

   >[!NOTE]
   >
   >Cancella **[!UICONTROL Use system value]** per rendere il campo modificabile.

   - Imposta **[!UICONTROL Company Registration Email Recipient]** al [contatto store](../getting-started/store-details.md#store-email-addresses) chi deve essere informato quando viene ricevuta una nuova richiesta di registrazione dell’azienda.

   - In **[!UICONTROL Send Company Registration Email Copy To]** immettere l&#39;indirizzo di posta elettronica di ogni persona che deve ricevere una copia della notifica di registrazione. Separa più indirizzi e-mail con una virgola.

   - Per determinare la modalità di invio della copia della notifica, impostare **[!UICONTROL Send Email Copy Method]** a uno dei seguenti elementi:

      - `Bcc` - Invia una _copia per cortesia cieca_ includendo il destinatario nell’intestazione della stessa e-mail inviata al cliente. Il destinatario Ccn non è visibile al cliente.
      - `Separate Email` - Invia la copia come e-mail separata.

   - Se hai preparato un modello e-mail da utilizzare al posto del predefinito, imposta **[!UICONTROL Default Company Registration Email]** al nome del modello. Per impostazione predefinita, il `Company Registration Request` viene utilizzato il modello.

     ![Configurazione clienti - Registrazione società](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. Completa il **[!UICONTROL Customer-Related Emails]** sezione:

   Se hai preparato modelli e-mail alternativi da utilizzare al posto dei predefiniti, scegli il modello da utilizzare per ciascuno dei seguenti elementi:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configurazione clienti: e-mail relative al cliente](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. Completa il **[!UICONTROL Company Status Change]** sezione:

   - Imposta **[!UICONTROL Company Status Change for Email Recipient]** al [contatto store](../getting-started/store-details.md#store-email-addresses) chi deve ricevere una notifica quando lo stato di un’azienda cambia.

   - In **[!UICONTROL Send Company Status Change Email Copy To]** immettere l&#39;indirizzo di posta elettronica di ogni persona che deve ricevere una copia della notifica di modifica dello stato. Separa più indirizzi e-mail con una virgola.

   - Per determinare la modalità di invio della copia della notifica, impostare **[!UICONTROL Send Email Copy Method]** a uno dei seguenti elementi:

      - `Bcc` - Invia una _copia per cortesia cieca_ includendo il destinatario nell’intestazione della stessa e-mail inviata al cliente. Il destinatario Ccn non è visibile al cliente.
      - `Separate Email` - Invia la copia come e-mail separata.

   - Se disponi di un modello e-mail preparato da utilizzare al posto del modello predefinito quando lo stato dell’azienda cambia da `Pending Approval` a `Active`, impostato **[!UICONTROL Default 'Company Status Change to Active 1' Email]** a tale modello. Per impostazione predefinita, il `Company Status Active 1` viene utilizzato il modello.

   - Se disponi di un modello e-mail preparato da utilizzare al posto del modello predefinito quando lo stato dell’azienda cambia da `Rejected` o `Blocked` a `Active`, impostato **[!UICONTROL Default 'Company Status Change to Active 2' Email]** a tale modello. Per impostazione predefinita, il `Company Status Active 2` viene utilizzato il modello.

   - Se disponi di un modello e-mail preparato da utilizzare al posto di quello predefinito quando lo stato dell’azienda cambia in `Rejected`, impostato **[!UICONTROL Default 'Company Status Change to Rejected' Email]** a tale modello. Per impostazione predefinita, il `Company Status Rejected` viene utilizzato il modello.

   - Se disponi di un modello e-mail preparato da utilizzare al posto di quello predefinito quando lo stato dell’azienda cambia in `Blocked`, impostato **[!UICONTROL Default 'Company Status Change to Blocked' Email]** a tale modello. Per impostazione predefinita, il `Company Status Blocked` viene utilizzato il modello.

   - Se disponi di un modello e-mail preparato da utilizzare al posto di quello predefinito quando lo stato dell’azienda cambia in `Pending Approval`, impostato **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** a tale modello. Per impostazione predefinita, il `Company Status Pending Approval` viene utilizzato il modello.

     ![Configurazione clienti: modifica dello stato della società](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. Completa il **[!UICONTROL Company Credit Emails]** sezione:

   - Imposta **[!UICONTROL Company Credit Change Email Sender]** al [contatto store](../getting-started/store-details.md#store-email-addresses) chi deve essere informato quando viene apportata una modifica al limite di credito assegnato a una società. Per impostazione predefinita, la notifica viene inviata a _Rappresentante commerciale_.

   - In **[!UICONTROL Send Company Credit Change Email Copy To]** immettere l&#39;indirizzo di posta elettronica di ogni persona che deve ricevere una copia della notifica di modifica del credito. Separa più indirizzi e-mail con una virgola.

   - Per determinare la modalità di invio della copia della notifica, impostare **[!UICONTROL Send Email Copy Method]** a uno dei seguenti elementi:

      - `Bcc` - Invia una _copia per cortesia cieca_ includendo il destinatario nell’intestazione della stessa e-mail inviata al cliente. Il destinatario Ccn non è visibile al cliente.
      - `Separate Email` - Invia la copia come e-mail separata.

   - Se hai preparato dei modelli e-mail da utilizzare al posto dei predefiniti, scegli il modello per ciascuna delle seguenti notifiche inviate all’amministratore della società.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configurazione clienti - e-mail di accredito aziendale](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
