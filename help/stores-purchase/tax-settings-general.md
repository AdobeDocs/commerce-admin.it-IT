---
title: Impostazioni di configurazione imposte
description: Scopri come configurare le impostazioni delle imposte di base, incluse le classi fiscali, il calcolo e la destinazione delle imposte predefinita.
exl-id: e32747f9-20d0-4717-9cee-aa1bcffebb65
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 0%

---

# Impostazioni di configurazione imposte

Le istruzioni seguenti descrivono la configurazione delle imposte di base per l’istanza Commerce. Prima di impostare le imposte, accertati di conoscere i requisiti fiscali del tuo [lingua](store-localize.md#step-3-change-the-locale-of-the-store-view). Quindi, completare la configurazione dell&#39;imposta in base alle proprie esigenze.

Amministratore [autorizzazioni](../systems/permissions.md) può essere impostato per limitare [accesso](../systems/permissions-user-roles.md) per tassare le risorse, in base all&#39;azienda _ha bisogno di sapere_. Per creare un ruolo amministratore con accesso alle impostazioni relative alle imposte, scegliere le risorse Vendite/Imposta e Sistema/Imposta. Se si imposta un sito Web per un&#39;area diversa dal punto di origine di spedizione predefinito, è necessario consentire anche l&#39;accesso alle risorse di sistema/spedizione per il ruolo. Le impostazioni di spedizione determinano l&#39;aliquota dell&#39;imposta del negozio utilizzata per i prezzi del catalogo.

## Configurare le impostazioni fiscali generali

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Per una configurazione multisito, imposta **[!UICONTROL Store View]** al sito web e al negozio di destinazione della configurazione.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Tax]**.

1. Completa le seguenti impostazioni di configurazione.

   Se necessario, cancellare il **[!UICONTROL Use system value]** casella di controllo di tutte le impostazioni disattivate.

### [!UICONTROL Tax Classes]

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Tax Classes]** sezione.

   ![Classi imposta](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

   - **Classe imposta per la spedizione** — Impostare sulla classe appropriata. Le classi predefinite sono: `None` e `Taxable Goods`
   - **Classe imposta per le opzioni regalo** — ![Adobe Commerce](../assets/adobe-logo.svg) (Solo per Adobe Commerce) Imposta sulla classe appropriata. Le classi predefinite sono: `None` e `Taxable Goods`
   - **Classe imposta predefinita per prodotto** — Impostare sulla classe appropriata. Le classi predefinite sono: `None` e `Taxable Goods`
   - **Classe imposta predefinita per il cliente** — Impostare sulla classe appropriata. La classe predefinita è: `Retail Customer` e `Wholesale Customer`

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### [!UICONTROL Calculation Settings]

1. Espandi **[!UICONTROL Calculation Settings]** sezione.

   ![Impostazioni di calcolo](../configuration-reference/sales/assets/tax-calculation-settings.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Tax Calculation Method Based On]** a uno dei seguenti elementi:

   - `Unit Price` - Il prezzo di ciascun prodotto
   - `Row Total` - Il totale della riga nell&#39;ordine, meno gli sconti
   - `Total` - Il totale dell’ordine

1. Imposta **[!UICONTROL Tax Calculation Based On]** a uno dei seguenti elementi:

   - `Shipping Address` - Indirizzo dove deve essere spedito l&#39;ordine
   - `Billing Address` - L&#39;indirizzo di fatturazione del cliente o dell&#39;azienda
   - `Shipping Origin` : l’indirizzo specificato come [punto di origine](shipping-settings.md#point-of-origin) per il tuo store

1. Imposta **[!UICONTROL Catalog Prices]** a `Excluding Tax` o `Including Tax`.

1. Imposta **[!UICONTROL Shipping Prices]** a `Excluding Tax` o `Including Tax`.

1. Imposta **[!UICONTROL Apply Customer Tax]** per determinare se l&#39;imposta viene applicata al prezzo originale o al prezzo scontato, eseguire una delle operazioni seguenti: `After Discount` o `Before Discount`

1. Imposta **[!UICONTROL Apply Discount on Prices]** per determinare se gli sconti includono o escludono l&#39;imposta, eseguire una delle operazioni seguenti: `Excluding Tax` o `Including Tax`

1. Imposta **[!UICONTROL Apply Tax On]** a `Custom price if available` o `Original price only`.

1. Imposta **[!UICONTROL Enable Cross-Border Trade]** a uno dei seguenti elementi:

   - `Yes` - Utilizzare prezzi coerenti tra diverse aliquote fiscali. Se il prezzo di catalogo include l&#39;imposta, scegliere questa impostazione per correggere il prezzo indipendentemente dall&#39;aliquota fiscale del cliente.
   - `No` - Variare il prezzo in base all&#39;aliquota fiscale.

   >[!IMPORTANT]
   >
   >Se [commercio transfrontaliero](#cross-border-price-consistency) è attivato, il margine di profitto cambia in base all&#39;aliquota fiscale. Il profitto è determinato dalla formula (`Revenue - CustomerVAT - CostOfGoodsSold`). Per consentire il commercio transfrontaliero, i prezzi devono essere fissati in modo da includere l&#39;imposta.

### [!UICONTROL Default Tax Destination Calculation]

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Default Tax Destination Calculation]** sezione.

   ![Calcolo destinazione imposta predefinita](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Specifica la **[!UICONTROL Default Country]** per i calcoli delle imposte.

1. Se del caso, specificare **[!UICONTROL Default State]** per i calcoli delle imposte.

1. Se del caso, specificare **[!UICONTROL Default Post Code]** per i calcoli delle imposte.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### [!UICONTROL Price Display Settings]

>[!IMPORTANT]
>
>Alcune combinazioni di impostazioni relative a una visualizzazione del prezzo che includono ed escludono l’imposta possono confondere il cliente. Per evitare che venga attivato un messaggio di avviso, vedere [impostazioni consigliate](taxes.md#warning-messages).

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Price Display Settings]** sezione.

   ![Impostazioni visualizzazione prezzo](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Display Product Prices in Catalog]** a uno dei seguenti elementi:

   - `Excluding Tax` - I prezzi del catalogo visualizzati nella vetrina non includono le imposte.
   - `Including Tax` - I prezzi del catalogo nella vetrina includono l&#39;imposta solo se una regola fiscale corrisponde all&#39;origine dell&#39;imposta o se l&#39;indirizzo del cliente corrisponde alla regola fiscale. Ciò può verificarsi dopo che un cliente ha creato un account, ha effettuato l’accesso o ha utilizzato lo strumento Stima imposte e spedizione nel carrello.
   - `Including and Excluding Tax` - I prezzi del catalogo visualizzati nella vetrina vengono visualizzati sia con che senza imposte.

1. Imposta **[!UICONTROL Display Shipping Prices]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### [!UICONTROL Shopping Cart Display Settings]

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Shopping Cart Display Settings]** sezione.

   ![Impostazioni di visualizzazione carrello](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. Per ciascuna delle impostazioni seguenti, scegliere come visualizzare le imposte e i prezzi nel carrello, in base alle esigenze del negozio e alle impostazioni internazionali:

   - Imposta **[!UICONTROL Display Prices]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

   - Imposta **[!UICONTROL Display Subtotal]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

   - Imposta **[!UICONTROL Display Shipping Amount]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Imposta **[!UICONTROL Display Gift Wrapping Prices]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Imposta **[!UICONTROL Display Printed Card Prices]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

1. Impostate le seguenti opzioni di visualizzazione su `Yes` o `No`, in base alle tue esigenze:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

1. Espandi ![Espansione](../assets/icon-display-expand.png) il **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** sezione.

   ![Impostazioni visualizzazione ordini, fatture e note di accredito](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Specificare la modalità di visualizzazione di prezzi e imposte in ordini, fatture e note di accredito:

   - Imposta **[!UICONTROL Display Prices]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

   - Imposta **[!UICONTROL Display Subtotal]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

   - Imposta **[!UICONTROL Display Shipping Amount]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Imposta **[!UICONTROL Display Gift Wrapping Prices]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Imposta **[!UICONTROL Display Printed Card Prices]** a `Excluding Tax`, `Including Tax`, o `Including and Excluding Tax`.

1. Impostate le seguenti opzioni di visualizzazione su `Yes` o `No`, in base alle tue esigenze:

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### [!UICONTROL Fixed Product Taxes]

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Fixed Product Taxes]** sezione.

   ![Imposte fisse sui prodotti](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enable FPT]** a uno dei due `Yes` o `No`, in base alle tue esigenze.

1. Se FPT è abilitato, specificate le opzioni di visualizzazione FPT:

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Price On Product view Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   - `Including FPT Only` - I prezzi visualizzati includono le imposte sui prodotti fisse. L&#39;importo FPT non viene visualizzato separatamente.
   - `Including FPT and FPT description` - I prezzi visualizzati includono le imposte sui prodotti fisse. L&#39;importo FPT viene visualizzato separatamente.
   - `Excluding FPT. Including FPT description and final price` - I prezzi visualizzati non includono le imposte sui prodotti fisse. L&#39;importo FPT viene visualizzato separatamente.
   - `Excluding FPT` - I prezzi visualizzati non includono le imposte sui prodotti fisse. L&#39;importo FPT non viene visualizzato separatamente.

1. Imposta **[!UICONTROL Apply Discounts to FPT]** a `Yes` o `No`, in base alle tue esigenze.

1. Imposta **[!UICONTROL FPT Tax Configuration]** per determinare come viene calcolato il valore FPT.

   - `Not Taxed` - Selezionare questa opzione se la giurisdizione di imposta non applica l&#39;FPT. Ad esempio, California.
   - `Taxed` - Selezionare questa opzione se la giurisdizione fiscale imposta l&#39;FPT. Ad esempio, Canada.
   - `Loaded and Displayed with Tax` - Fare clic su questa opzione se FPT viene aggiunto al totale dell&#39;ordine prima dell&#39;applicazione delle imposte. Ad esempio, i paesi dell&#39;UE.

1. Imposta **[!UICONTROL Include FPT in Subtotal]** a `Yes` o `No`, in base alle tue esigenze.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Coerenza transfrontaliera dei prezzi

Il commercio transfrontaliero (detto anche coerenza dei prezzi) sostiene gli esercenti dell&#39;Unione europea (UE) e di altri paesi che desiderano mantenere prezzi coerenti per i clienti le cui aliquote fiscali sono diverse dall&#39;aliquota dell&#39;imposta sui depositi.

I commercianti che operano in aree geografiche e aree geografiche possono visualizzare un unico prezzo includendo l&#39;imposta nel prezzo del prodotto. I prezzi sono puliti e ordinati indipendentemente dalle strutture fiscali e dalle aliquote che variano da paese a paese. Queste impostazioni richiedono l&#39;installazione di un&#39;estensione per il calcolo delle imposte dal [Marketplace](../getting-started/commerce-marketplace.md), ad esempio _Vertex Cloud_.

>[!NOTE]
>
>Quando il commercio transfrontaliero è abilitato, il margine di profitto cambia in base all’aliquota fiscale. Il profitto è determinato dalla formula:<br>
>`Revenue - CustomerVAT - CostOfGoodsSold`

**_Per garantire la coerenza transfrontaliera dei prezzi:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Per una configurazione multisito, imposta **[!UICONTROL Store View]** al sito web e al negozio di destinazione della configurazione.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Tax]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Calculation Settings]** sezione.

1. Imposta **[!UICONTROL Catalog Prices]** a `Including Tax`.

1. Per garantire la coerenza dei prezzi a livello transfrontaliero, impostare **[!UICONTROL Enable Cross Border Trade]** a `Yes`.

   ![Abilita impostazioni commercio transfrontaliero](./assets/cross-border-calculations-settings.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
