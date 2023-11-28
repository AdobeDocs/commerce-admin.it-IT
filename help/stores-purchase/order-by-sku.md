---
title: Ordina per SKU
description: Scopri come configurare il tuo negozio per supportare l’ordinazione per SKU (Stock Keeping Unit), per facilitare l’accesso dei clienti.
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Ordina per SKU

{{ee-feature}}

Una &#39;SKU&#39; è una &#39;Stock Keeping Unit&#39;. Le SKU generalmente aiutano i venditori online a identificare le caratteristiche più importanti del prodotto come: dimensioni, colore, prezzo e materiale. Gli ID prodotto sono diversi dagli SKU:

- Il `Product ID` è una serie sequenziale di numeri utilizzata internamente per identificare i prodotti e non disponibile per i clienti.
- Il `SKU` è generato dal venditore, di solito in base al nome del prodotto e agli attributi per il marketing o il tracciamento interno. Ad esempio: T-shirt blu, cotone, taglia media: T-COT-MED-BL. Se necessario, il venditore può modificare la SKU.

Normalmente, una SKU comprende una serie di abbreviazioni che indicano le caratteristiche distintive del prodotto. La lunghezza massima dello SKU è di 64 caratteri. Le SKU sono importanti per tenere traccia e gestire in modo efficace l’inventario, pertanto la loro corretta configurazione è fondamentale per l’e-commerce.

_Ordina per SKU_ è un [widget](../content-design/widgets.md) che possono essere esposti in negozio per comodità di tutti gli acquirenti o messi a disposizione solo degli acquirenti appartenenti a specifiche categorie di clienti. Gli acquirenti possono inserire le informazioni relative allo SKU e alla quantità direttamente nel blocco Ordina per SKU oppure caricare un file CSV dal proprio account cliente. Indipendentemente dalla configurazione, l’ordine in base allo SKU è sempre disponibile per gli amministratori di store.

![Ordina per SKU in vetrina](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## Configurare l’ordine per SKU

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegliere **[!UICONTROL Sales]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Order by SKU Settings]** sezione.

1. Imposta **[!UICONTROL Enable Order by SKU on my Account in Storefront]** a uno dei seguenti elementi:

   - `Yes, for Everyone` - Il blocco Order by SKU è disponibile nel negozio per ogni cliente.
   - `Yes, for Specified Customer Groups` - Ordina per SKU è disponibile solo per i membri di un gruppo di clienti specifico, ad esempio `Wholesale`.
   - `No` - Il blocco Ordina per SKU non viene visualizzato nella vetrina e la pagina Ordina per SKU non è disponibile nel conto cliente.

   ![Impostazioni Ordina per SKU](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.

![B2B per Adobe Commerce](../assets/b2b.svg) (B2B solo per Adobe Commerce) _**Per attivare la funzione Ordina per SKU, disattivare la funzione Ordine rapido:**_

1. Vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL B2B Features]**

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL B2B Features]** sezione.

1. Imposta **[!UICONTROL Enable Quick Order]** a `No`.

   Il [Funzione ordine rapido](../b2b/quick-order.md) consente ai clienti e agli ospiti di effettuare rapidamente gli ordini in base allo SKU (Stock Keeping Unit) o al nome del prodotto.

## Esperienza vetrina

Quando la funzionalità è configurata per lo store, i clienti possono ordinare per SKU da qualsiasi pagina che include _Ordina per SKU_ widget o dal dashboard dell’account.

### Ordina per SKU dal blocco della pagina

1. In _Ordina per SKU_ blocco, il cliente immette il **[!UICONTROL SKU]** e **[!UICONTROL Qty]** dell&#39;articolo da ordinare.

1. Per aggiungere un altro elemento, fai clic su **[!UICONTROL Add Row]** e ripetere il processo.

1. Clic **[!UICONTROL Add to Cart]**.

### Ordina per SKU da un account cliente

1. Dalla vetrina, il cliente accede al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Order by SKU]**.

1. Aggiunge singoli elementi in base alle preferenze:

   _**Aggiunge ogni elemento in base allo SKU:**_

   - Entra nel **[!UICONTROL SKU]** e **[!UICONTROL Qty]** dell&#39;articolo da ordinare.

   - Per aggiungere altri elementi in base alle esigenze, fai clic su _Aggiungi riga_ ![Pulsante segno più](../assets/button-add-item.png) e si ripete per tutti gli elementi necessari.

   - Clic **[!UICONTROL Add to Cart]**.

   _**Carica un file CSV con più elementi:**_

   - Prepara un [importare dati CSV](../systems/data-csv.md) (Valore separato da virgole) che include colonne per `SKU` e `Qty`.

   ![SKU da importare](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - Per caricare il file CSV, fai clic su **[!UICONTROL Choose File]** e seleziona il file da caricare.

   - Clic **[!UICONTROL Add to Cart]**.

   Se uno dei prodotti dispone di opzioni aggiuntive, al cliente viene richiesto dal carrello che il prodotto richiede attenzione.

   ![Il prodotto richiede attenzione](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se sono presenti SKU duplicate, le quantità vengono combinate in una riga nel carrello. Il cliente può modificare la quantità di qualsiasi articolo e fare clic su **[!UICONTROL Update Shopping Cart]** per ricalcolare i totali.

