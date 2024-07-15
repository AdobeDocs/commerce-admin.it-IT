---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Tax]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Sales] &gt; [!UICONTROL Tax] dell'amministratore di Commerce.
exl-id: eb929a6c-adb2-45ac-b6ec-6239938355bf
feature: Configuration, Taxes
source-git-commit: f95e6d22f83b518c64b254f0d98147e3c6ebaf42
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Tax]

>[!NOTE]
>
>Le versioni da 2.4.0 a 2.4.3 di Adobe Commerce e Magento Open Source includono l&#39;estensione sviluppata dal fornitore Vertex utilizzata per l&#39;integrazione con [!UICONTROL Vertex Cloud]. A partire dalla versione 2.4.4, questa estensione non è più inclusa nella versione core e deve essere installata e aggiornata dalla versione Commerce Marketplace. Il Marketplace fornisce anche accesso alla documentazione corrente fornita dallo sviluppatore dell’estensione.
><br><br>
>Se l’estensione in bundle è abilitata e configurata, devi aggiornare il file compositore.json come parte del processo di aggiornamento 2.4.4 e gestire gli aggiornamenti delle estensioni in futuro. Per ulteriori informazioni, vedere [Moduli di aggiornamento ed estensioni](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) nella _Guida all&#39;aggiornamento_.

{{config}}

## [!UICONTROL Tax Classes]

![Classi imposta](./assets/tax-tax-classes.png)<!-- zoom -->

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Classi imposta](../../stores-purchase/tax-class.md) nella _Guida agli store e all&#39;esperienza di acquisto_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Tax Class for Shipping] | Sito Web | Identifica la classe fiscale utilizzata per la spedizione. Le opzioni includono tutte le classi di imposta sul prodotto disponibili: `None` / `Taxable Goods` / `Shipping` / `Tax Exempt` |
| [!UICONTROL Tax Class for Gift Options] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) identifica la classe di imposta predefinita utilizzata per le opzioni regalo. |
| [!UICONTROL Default Tax Class for Product] | Globale | Identifica la classe fiscale predefinita utilizzata per i prodotti. |
| [!UICONTROL Default Tax Class for Customer] | Globale | Identifica la classe fiscale predefinita utilizzata per i clienti. |

{style="table-layout:auto"}

## [!UICONTROL Calculation Settings]

![Impostazioni di calcolo](./assets/tax-calculation-settings.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | Sito Web | Determina il metodo utilizzato per calcolare l&#39;imposta per un ordine. Opzioni:<br/>**`Unit Price`**- I calcoli delle imposte si basano sul prezzo unitario di ciascun prodotto.<br/>**`Row Total`** - I calcoli delle imposte si basano sul totale delle voci. <br/>**`Total`**- I calcoli delle imposte si basano sul totale dell&#39;ordine.<br/><br/>_** Nota:**_se dal Marketplace è installata un&#39;estensione per il calcolo delle imposte, ad esempio _Vertex Cloud_, il servizio di estensione è elencato come opzione. |
| [!UICONTROL Tax Calculation Based On] | Sito Web | Determina se il calcolo dell&#39;imposta si basa sull&#39;indirizzo di spedizione, sull&#39;indirizzo di fatturazione o sull&#39;origine di spedizione. Opzioni: `Shipping Address` / `Billing Address` / `Shipping Origin` |
| [!UICONTROL Catalog Prices] | Sito Web | Determina se i prezzi del catalogo includono o escludono le imposte. Opzioni: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Shipping Prices] | Sito Web | Determina i prezzi di spedizione che includono o escludono le imposte. Opzioni: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Customer Tax] | Sito Web | Determina se l&#39;imposta viene applicata prima o dopo uno sconto. Opzioni: `Before Discount` / `After Discount` |
| [!UICONTROL Apply Discount on Prices] | Sito Web | Determina se i prezzi scontati includono o escludono le imposte. Opzioni: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Tax On] | Sito Web | Determina se l&#39;imposta viene applicata al prezzo originale o a un prezzo personalizzato, se disponibile. Opzioni: `Custom price if available` / `Original price only` |
| [!UICONTROL Enable Cross Border Trade] | Sito Web | Quando questa opzione è abilitata, applica prezzi coerenti oltre i confini delle aree con aliquote diverse. Opzioni: `Yes` / `No` <br/><br/>**_Nota:_**L&#39;utilizzo del commercio transfrontaliero consente di adeguare il margine di profitto in base all&#39;aliquota fiscale. |

{style="table-layout:auto"}

## [!UICONTROL Default Tax Destination Calculation]

![Calcolo destinazione imposta predefinita](./assets/tax-default-tax-destination-calculation.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Default Country] | Visualizzazione store | Determina il paese su cui si basano i calcoli delle imposte. |
| [!UICONTROL Default State] | Visualizzazione store | Determina lo stato su cui si basano i calcoli delle imposte. Un asterisco (*) può fungere da carattere jolly per indicare tutti gli stati all&#39;interno del paese selezionato. |
| [!UICONTROL Default Post Code] | Visualizzazione store | Identifica il CAP su cui si basano i calcoli delle imposte. Un asterisco (*) può fungere da carattere jolly per indicare tutti i codici postali all’interno dello stato selezionato. |

{style="table-layout:auto"}

## [!UICONTROL Price Display Settings]

![Impostazioni visualizzazione prezzo](./assets/tax-price-display-settings.png)<!-- zoom -->

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Configurare le impostazioni di visualizzazione dei prezzi](../../stores-purchase/display-settings.md#configure-price-display-settings) nella _Guida agli store e all&#39;esperienza di acquisto_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | Visualizzazione store | Determina se i prezzi dei prodotti pubblicati nel catalogo includono o escludono le imposte o visualizzano due versioni del prezzo, una con e l&#39;altra senza imposte. Opzioni: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` <br/><br/>**_Nota:_**Se si imposta il campo Visualizza prezzi prodotto su `Including Tax`, l&#39;imposta viene visualizzata solo se esiste una regola fiscale che corrisponde all&#39;origine dell&#39;imposta o se esiste un indirizzo cliente che corrisponde alla regola fiscale. Gli eventi che possono attivare una corrispondenza includono la creazione di un account cliente, l’accesso o l’utilizzo dello strumento di stima delle imposte e della spedizione nel carrello. |
| [!UICONTROL Display Shipping Prices] | Visualizzazione store | Determina se i prezzi di spedizione includono o escludono l&#39;imposta oppure se visualizzano due versioni del prezzo di spedizione, una con e l&#39;altra senza imposta. Opzioni: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart Display Settings]

![Impostazioni visualizzazione carrello](./assets/tax-shopping-cart-display-settings.png)<!-- zoom -->

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Configurare le impostazioni di visualizzazione del carrello acquisti](../../stores-purchase/display-settings.md#step-2-configure-shopping-cart-display-settings) nella _Guida agli store e all&#39;esperienza di acquisto_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Visualizzazione store | Determina se i prezzi del carrello includono o escludono le imposte o se visualizzano due versioni del prezzo: una con e l&#39;altra senza imposte. Opzioni: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal|Store View] | Determina se il subtotale del carrello acquisti include o esclude le imposte oppure mostra due versioni del subtotale, una con e l&#39;altra senza imposte. Opzioni: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Visualizzazione store | Determina se l&#39;importo della spedizione del carrello acquisti include o esclude le imposte o mostra due versioni dell&#39;importo della spedizione, una con e l&#39;altra senza imposte. Opzioni: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Visualizzazione store | Determina se nel carrello viene visualizzata una riga aggiuntiva con l&#39;importo totale complessivo senza imposte. Opzioni: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Visualizzazione store | Determina se il carrello include un riepilogo fiscale completo. Opzioni: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Visualizzazione store | Determina se il carrello acquisti include un subtotale dell&#39;imposta quando l&#39;imposta è zero. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

![Impostazioni visualizzazione ordini, fatture e note di accredito](./assets/tax-orders-invoices-credit-memos-display-settings.png)<!-- zoom -->

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Configurare le impostazioni di visualizzazione di ordini, fatture e note di accredito](../../stores-purchase/display-settings.md#step-3-configure-order-invoice-and-credit-memo-display-settings) nella _Guida agli archivi e all&#39;esperienza di acquisto_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Visualizzazione store | Determina se i prezzi nei documenti di vendita includono o escludono le imposte o se in ogni documento vengono visualizzate due versioni del prezzo, una con e l&#39;altra senza imposte. Opzioni: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal] | Visualizzazione store | Determina se il subtotale nei documenti di vendita include o esclude le imposte o se in ogni documento vengono visualizzate due versioni del subtotale, una con e l&#39;altra senza imposte. Opzioni: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Visualizzazione store | Determina se l&#39;importo di spedizione nei documenti di vendita include o esclude le imposte o se in ogni documento vengono visualizzate due versioni del subtotale, una con e l&#39;altra senza imposte. Opzioni: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Visualizzazione store | Determina se nei documenti di vendita viene visualizzata una riga aggiuntiva con l&#39;importo totale complessivo senza imposte. Opzioni: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Visualizzazione store | Determina se il riepilogo fiscale completo viene visualizzato nei documenti di vendita. Opzioni: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Visualizzazione store | Determina la sezione del subtotale nei documenti di vendita quando non viene addebitata alcuna imposta. Opzioni: `Yes` / `No` |
| [!UICONTROL Display Gift Wrapping Prices] | Visualizzazione store | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) determina se i prezzi per confezioni regalo sono inclusi nel subtotale. Opzioni: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | Visualizzazione store | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) determina se i prezzi delle schede stampate sono inclusi nel subtotale. Opzioni: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Fixed Product Taxes]

![Imposta sul prodotto fissa](./assets/tax-fixed-product-taxes.png)<!-- zoom -->

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [FPT (Fixed product tax)](../../stores-purchase/fixed-product-tax.md) nella _Guida agli store e all&#39;esperienza di acquisto_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable FPT] | Sito Web | Determina se FPT è disponibile. Opzioni: `Yes` / `No` |
| [!UICONTROL Display Prices in Product Lists] | Sito Web | Controlla la visualizzazione di FPT negli elenchi di prodotti. Opzioni:<br/> **`Including FPT Only`** - I prezzi visualizzati includono le imposte sui prodotti fisse. L&#39;importo FPT non viene visualizzato separatamente.<br/>**`Including FPT and FPT description`**- I prezzi visualizzati includono le imposte sui prodotti fisse. L&#39;importo FPT viene visualizzato separatamente.<br/>**`Excluding FPT. Including FPT description and final price`** - I prezzi visualizzati non includono le imposte sui prodotti fisse. L&#39;importo FPT viene visualizzato separatamente.<br/>**`Excluding FPT`**- I prezzi visualizzati non includono le imposte sui prodotti fisse. L&#39;importo FPT non viene visualizzato separatamente. |
| [!UICONTROL Display Prices On Product View Page] | Sito Web | Controlla la visualizzazione di FPT nella pagina del prodotto. Opzioni:<br/> **`Including FPT Only`** - I prezzi visualizzati includono le imposte sui prodotti fisse. L&#39;importo FPT non viene visualizzato separatamente.<br/>**`Including FPT and FPT description`**- I prezzi visualizzati includono le imposte sui prodotti fisse. L&#39;importo FPT viene visualizzato separatamente.<br/>**`Excluding FPT. Including FPT description and final price`** - I prezzi visualizzati non includono le imposte sui prodotti fisse. L&#39;importo FPT viene visualizzato separatamente.<br/>**`Excluding FPT`**- I prezzi visualizzati non includono le imposte sui prodotti fisse. L&#39;importo FPT non viene visualizzato separatamente. |
| [!UICONTROL Display Prices in Sales Modules] | Sito Web | Controlla la visualizzazione di FPT nel carrello e durante il pagamento. Opzioni:<br/> **`Including FPT Only`** - I prezzi visualizzati includono le imposte sui prodotti fisse. L&#39;importo FPT non viene visualizzato separatamente.<br/>**`Including FPT and FPT description`**- I prezzi visualizzati includono le imposte sui prodotti fisse. L&#39;importo FPT viene visualizzato separatamente.<br/>**`Excluding FPT. Including FPT description and final price`** - I prezzi visualizzati non includono le imposte sui prodotti fisse. L&#39;importo FPT viene visualizzato separatamente.<br/>**`Excluding FPT`**- I prezzi visualizzati non includono le imposte sui prodotti fisse. L&#39;importo FPT non viene visualizzato separatamente. |
| [!UICONTROL Display Prices in Emails] | Sito Web | Controlla la visualizzazione di FPT nelle e-mail. Opzioni:<br/> **`Including FPT Only`** - I prezzi visualizzati includono le imposte sui prodotti fisse. L&#39;importo FPT non viene visualizzato separatamente.<br/>**`Including FPT and FPT description`**- I prezzi visualizzati includono le imposte sui prodotti fisse. L&#39;importo FPT viene visualizzato separatamente.<br/>** Esclusione di FPT. Inclusi descrizione FPT e prezzo finale **- I prezzi visualizzati non includono le imposte sui prodotti fisse. L&#39;importo FPT viene visualizzato separatamente.<br/>**`Excluding FPT`** - I prezzi visualizzati non includono le imposte sui prodotti fisse. L&#39;importo FPT non viene visualizzato separatamente. |
| [!UICONTROL Apply Tax to FPT] | Sito Web | Determina se l&#39;imposta viene applicata all&#39;importo FPT. Opzioni: `Yes` / `No` |
| [!UICONTROL Include FPT in Subtotal] | Sito Web | Determina se FPT è incluso nel subtotale del carrello acquisti. Opzioni: <br/>**`Yes`**- Include FPT nel subtotale del carrello acquisti.<br/>**`No`** - FPT non è incluso nel subtotale e viene inserito dopo il subtotale nel carrello. |

{style="table-layout:auto"}
