---
title: Nuove opzioni account cliente
description: Scopri le opzioni di configurazione per i nuovi account cliente nel tuo store.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Nuove opzioni account cliente

Nella sezione _[!UICONTROL Create New Account Options]_&#x200B;della configurazione, le opzioni account di base sono combinate con opzioni più avanzate relative alla convalida dell&#39;ID IVA e alle integrazioni personalizzate. Le istruzioni seguenti descrivono solo le opzioni utilizzate più di frequente. Per informazioni sulle assegnazioni automatiche dei gruppi di clienti, vedere [Convalida IVA](../stores-purchase/vat.md).

![Crea nuove opzioni account](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## Impostare le opzioni di account cliente di base

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Customer Configuration]**.

1. Espandere la sezione **[!UICONTROL Create New Account Options]**:

   ![Impostazioni predefinite per la creazione di nuove opzioni account](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. Imposta ciascuna delle opzioni in base all’esperienza del cliente che devi supportare sulla vetrina:

   - Impostare **[!UICONTROL Default Group]** sul gruppo di clienti assegnato ai nuovi clienti al momento della creazione di un account.

   - Se si dispone di un numero _Imposta sul valore aggiunto_ e si desidera che sia visibile ai clienti, impostare **[!UICONTROL Show VAT Number on Storefront]** su `Yes`.

   - Per richiedere l&#39;e-mail di un cliente durante la creazione dell&#39;ordine di amministrazione, impostare **[!UICONTROL Email is required field for Admin order creation]** su `Yes`.

   - Immettere **[!UICONTROL Default Email Domain]** per l&#39;archivio, ad esempio `mystore.com`

   - Imposta **[!UICONTROL Default Welcome Email]** sul modello utilizzato per l&#39;e-mail di benvenuto inviata ai nuovi clienti.

   - Per richiedere ai clienti di confermare la richiesta di apertura di un account con il tuo store, imposta **[!UICONTROL Require Emails Confirmation]** su `Yes`. Quindi, impostare **[!UICONTROL Confirmation Link Email]** sul modello utilizzato per l&#39;e-mail di conferma.

     >[!NOTE]
     >
     >A partire dalla versione 2.4.7, i clienti devono reinserire l’e-mail e la password per accedere al proprio account dopo la conferma e-mail, indipendentemente dal browser.

   - Impostare **[!UICONTROL Welcome Email]** sul modello utilizzato per il messaggio di benvenuto inviato dopo la conferma dell&#39;account.

   - Impostare **[!UICONTROL Default Welcome Email without Password]** sul modello utilizzato al momento della creazione di un account cliente che non dispone ancora di una password. Ad esempio, a un account cliente creato dall’amministratore non è ancora stata assegnata una password.

   - Impostare **[!UICONTROL Email Sender]** sul contatto dello store che viene visualizzato come mittente dell&#39;e-mail di benvenuto.

   - Per richiedere ai clienti di confermare la richiesta di apertura di un account con il tuo store, imposta **[!UICONTROL Require Emails Confirmation]** su `Yes`. Quindi, impostare **[!UICONTROL Confirmation Link Email]** sul modello utilizzato per l&#39;e-mail di conferma.

   ![Crea nuove opzioni account con IVA abilitata](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   Per informazioni dettagliate su ciascuna delle opzioni disponibili in questo set di opzioni di configurazione, vedere _Crea nuove opzioni account_ [riferimento alla configurazione](../configuration-reference/customers/customer-configuration.md).

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
