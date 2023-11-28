---
title: Impostazioni visualizzazione prezzo
description: Scopri la visualizzazione delle imposte nel catalogo, nel carrello, negli ordini, nelle fatture e nelle note di credito che supportano l’esperienza di acquisto del cliente.
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Impostazioni visualizzazione prezzo

Le impostazioni di visualizzazione del prezzo determinano se i prezzi di prodotto e spedizione includono o escludono l&#39;imposta o mostrano due versioni del prezzo: una con e l&#39;altra senza imposta.

Se il prezzo del prodotto include l&#39;imposta, questa viene visualizzata solo se esiste una regola fiscale che corrisponde all&#39;origine dell&#39;imposta o se l&#39;indirizzo di un cliente corrisponde alla regola fiscale. Gli eventi che possono attivare una corrispondenza includono la creazione di un account, l’accesso o la generazione di una stima di imposta e spedizione dal carrello.

>[!IMPORTANT]
>
>Mostrare i prezzi che includono ed escludono le imposte può confondere il cliente. Per evitare che venga attivato un messaggio di avviso, vedere [linee guida](international-tax-guidelines.md) per il tuo paese e [impostazioni consigliate](taxes.md#warning-messages) per evitare messaggi di avviso.

![Impostazioni visualizzazione prezzo](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedi [Impostazioni visualizzazione prezzo](../configuration-reference/sales/tax.md#price-display-settings) nel _Guida di riferimento alla configurazione_.

## Configurare le impostazioni di visualizzazione del prezzo

Al termine della configurazione del calcolo per imposte, tassi e classi, le imposte vengono calcolate in base a tali impostazioni. Tuttavia, anche la visualizzazione delle imposte nel catalogo, nel carrello, negli ordini, nelle fatture e nelle note di accredito deve essere configurata per supportare l&#39;esperienza del cliente nella vetrina.

È consigliabile visualizzare i prezzi con le imposte associate (incluse le imposte o entrambe incluse le imposte e escluse le imposte) in modo che i clienti possano sapere come vengono applicati questi calcoli prima di effettuare un ordine.

### Passaggio 1: configurare le impostazioni di visualizzazione dei prezzi del catalogo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Tax]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Price Display Settings]** sezione.

1. Per **[!UICONTROL Display Product Prices in Catalog]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >Se si imposta questa opzione su `Including Tax`, l&#39;imposta viene visualizzata solo se esiste una regola fiscale che corrisponde all&#39;origine dell&#39;imposta o se è presente un indirizzo del cliente che corrisponde alla regola fiscale. Gli eventi che possono attivare una corrispondenza includono la creazione di un account cliente, l’accesso o l’utilizzo dello strumento di stima delle imposte e della spedizione nel carrello.

1. Per **[!UICONTROL Display Shipping Prices]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

Se scegli di visualizzare entrambi i prezzi (con e senza imposte), la vetrina sarà simile alla seguente:

![Esempio di visualizzazione del prezzo, comprese le imposte sul negozio](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### Passaggio 2: configurare le impostazioni di visualizzazione del carrello

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Shopping Cart Display Settings]** sezione.

   ![Impostazioni di visualizzazione carrello](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Display Prices]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per **[!UICONTROL Display Subtotal]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per **[!UICONTROL Display Shipping Amount]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) per **[!UICONTROL Display Gift Wrapping Prices]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) per **[!UICONTROL Display Printed Card Prices]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per ciascuna di queste opzioni rimanenti, imposta su `Yes` o `No` in base alle tue preferenze:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### Passaggio 3: configurare le impostazioni di visualizzazione di ordini, fatture e note di accredito

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** sezione.

   ![Impostazioni visualizzazione ordini, fatture e note di accredito](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Display Prices]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per **[!UICONTROL Display Subtotal]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per **[!UICONTROL Display Shipping Amount]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) per **[!UICONTROL Display Gift Wrapping Prices]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) per **[!UICONTROL Display Printed Card Prices]**, scegli una delle seguenti opzioni:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Per ciascuna di queste opzioni rimanenti, imposta su `Yes` o `No` in base alle tue preferenze:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
