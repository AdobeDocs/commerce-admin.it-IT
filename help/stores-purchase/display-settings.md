---
title: Impostazioni visualizzazione prezzo
description: Scopri la visualizzazione delle imposte nel catalogo, nel carrello, negli ordini, nelle fatture e nelle note di credito che supportano l’esperienza di acquisto del cliente.
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
TQID: https://experienceleague.adobe.com/XIcN-vl8owiToGhM3Et2euyNWgnJdsgSl6urwJcRdLE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# Impostazioni visualizzazione prezzo

Le impostazioni di visualizzazione del prezzo determinano se i prezzi di prodotto e spedizione includono o escludono l&#39;imposta o mostrano due versioni del prezzo: una con e l&#39;altra senza imposta.

Se il prezzo del prodotto include l&#39;imposta, questa viene visualizzata solo se esiste una regola fiscale che corrisponde all&#39;origine dell&#39;imposta o se l&#39;indirizzo di un cliente corrisponde alla regola fiscale. Gli eventi che possono attivare una corrispondenza includono la creazione di un account, l’accesso o la generazione di una stima di imposta e spedizione dal carrello.

>[!IMPORTANT]
>
>Mostrare i prezzi che includono ed escludono le imposte può confondere il cliente. Per evitare di attivare un messaggio di avviso, consulta le [linee guida](international-tax-guidelines.md) per il tuo paese e le [impostazioni consigliate](taxes.md#warning-messages) per evitare messaggi di avviso.

![Impostazioni visualizzazione prezzo](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedere [Impostazioni visualizzazione prezzo](../configuration-reference/sales/tax.md#price-display-settings) nella _Guida di riferimento configurazione_.

## Configurare le impostazioni di visualizzazione del prezzo

Al termine della configurazione del calcolo per imposte, tassi e classi, le imposte vengono calcolate in base a tali impostazioni. Tuttavia, anche la visualizzazione delle imposte nel catalogo, nel carrello, negli ordini, nelle fatture e nelle note di accredito deve essere configurata per supportare l&#39;esperienza del cliente nella vetrina.

È consigliabile visualizzare i prezzi con le imposte associate (incluse le imposte o entrambe incluse le imposte e escluse le imposte) in modo che i clienti possano sapere come vengono applicati questi calcoli prima di effettuare un ordine.

### Passaggio 1: configurare le impostazioni di visualizzazione dei prezzi del catalogo

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Tax]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Price Display Settings]**.

1. Per **[!UICONTROL Display Product Prices in Catalog]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >Se si imposta questa opzione su `Including Tax`, l&#39;imposta verrà visualizzata solo se esiste una regola fiscale che corrisponde all&#39;origine dell&#39;imposta o se esiste un indirizzo cliente che corrisponde alla regola fiscale. Gli eventi che possono attivare una corrispondenza includono la creazione di un account cliente, l’accesso o l’utilizzo dello strumento di stima delle imposte e della spedizione nel carrello.

1. Per **[!UICONTROL Display Shipping Prices]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

Se scegli di visualizzare entrambi i prezzi (con e senza imposte), la vetrina sarà simile alla seguente:

![Esempio di visualizzazione del prezzo, incluse le imposte sulla vetrina](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### Passaggio 2: configurare le impostazioni di visualizzazione del carrello

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Shopping Cart Display Settings]**.

   ![Impostazioni visualizzazione carrello](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Display Prices]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per **[!UICONTROL Display Subtotal]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per **[!UICONTROL Display Shipping Amount]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Per **[!UICONTROL Display Gift Wrapping Prices]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Per **[!UICONTROL Display Printed Card Prices]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per ognuna di queste opzioni rimanenti, passa a `Yes` o `No` in base alle tue preferenze:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### Passaggio 3: configurare le impostazioni di visualizzazione di ordini, fatture e note di accredito

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]**.

   ![Impostazioni visualizzazione ordini, fatture e note di accredito](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Display Prices]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per **[!UICONTROL Display Subtotal]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per **[!UICONTROL Display Shipping Amount]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Per **[!UICONTROL Display Gift Wrapping Prices]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Per **[!UICONTROL Display Printed Card Prices]**, scegliere una delle opzioni seguenti:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per ognuna di queste opzioni rimanenti, passa a `Yes` o `No` in base alle tue preferenze:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
