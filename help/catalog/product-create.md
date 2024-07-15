---
title: Creare un prodotto
description: Scopri i tipi di prodotti che puoi creare per il catalogo.
exl-id: ff90bf8a-a64d-403f-bd09-5c8167a36f0b
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 0%

---

# Creare un prodotto

La scelta di un tipo di prodotto è una delle prime operazioni da eseguire per creare un prodotto. Se stai iniziando a costruire il catalogo dei prodotti, puoi creare alcuni prodotti di esempio per sperimentare con ciascun tipo di prodotto. Oltre ai tipi di prodotto di base, il termine _prodotto complesso_ viene talvolta utilizzato per fare riferimento a prodotti con più opzioni, ad esempio un prodotto configurabile disponibile in vari colori e dimensioni.

>[!NOTE]
>
>Per maggiori informazioni, consulta il catalogo [navigazione](navigation.md), come impostare [categorie](categories.md) e [attributi](product-attributes.md) e le [opzioni URL](catalog-urls.md) disponibili per il catalogo. Dopo aver compreso questi concetti, il modo più efficiente per aggiungere molti prodotti al catalogo è [importarli](../systems/data-import.md) da un file CSV.

![Pagina di prodotto nella vetrina](./assets/storefront-product-page.png){width="700" zoomable="yes"}

## Tipi di prodotto

**[Prodotto semplice](product-create-simple.md)**: un prodotto semplice è un elemento fisico con un solo SKU. I prodotti semplici hanno vari prezzi e controlli dei fattori di produzione che consentono di vendere varianti del prodotto. I prodotti semplici possono essere utilizzati in associazione a prodotti raggruppati, in bundle e configurabili.

**[Prodotto configurabile](product-create-configurable.md)** - Un prodotto configurabile sembra essere un singolo prodotto con elenchi di opzioni per ogni variante. Tuttavia, ogni opzione rappresenta un prodotto semplice e separato con una SKU distinta, che consente di tenere traccia dell’inventario per ogni variante.

**[Prodotto raggruppato](product-create-grouped.md)** - Un prodotto raggruppato presenta più prodotti autonomi come gruppo. Puoi offrire varianti di un singolo prodotto o raggrupparle per una promozione. I prodotti possono essere acquistati separatamente o come gruppo.

**[Prodotti virtuali](product-create-virtual.md)**: un prodotto virtuale non è un prodotto tangibile e viene in genere utilizzato per prodotti quali servizi, appartenenze, garanzie e abbonamenti. I prodotti virtuali possono essere utilizzati in associazione con prodotti raggruppati e in bundle.

**[Prodotto in bundle](product-create-bundle.md)**: un prodotto in bundle consente ai clienti di &quot;creare il proprio&quot; da una serie di opzioni. Il pacchetto potrebbe essere un cestino regalo, un computer o qualsiasi altra cosa che possa essere personalizzata. Ogni elemento nel bundle è un prodotto separato e autonomo.

**[Prodotto scaricabile](product-create-downloadable.md)**: un prodotto scaricabile digitalmente è costituito da uno o più file scaricati. I file possono risiedere sul server o essere forniti come URL a qualsiasi altro server.

**[gift card](product-gift-card-create.md)** - ([solo Adobe Commerce](../landing/home.md#product-editions)) Esistono tre tipi di gift card. Le _gift card virtuali_ vengono inviate tramite e-mail. Le _gift card fisiche_ vengono spedite al destinatario. _gift card combinate_ che sono una combinazione di virtual e physical. Ciascuno ha un codice univoco, che viene riscattato durante il pagamento. Le gift card possono essere incluse anche in un prodotto raggruppato.

## Impostazioni prodotto

Le impostazioni e gli attributi del prodotto utilizzati più di frequente vengono visualizzati nella parte superiore della pagina, seguiti dagli attributi personalizzati. Tutte le altre impostazioni di prodotto sono disponibili in sezioni espandibili nella parte inferiore della pagina.

![Impostazioni prodotto](./assets/product-settings.png){width="600" zoomable="yes"}

| Impostazione | Descrizione |
|--- |--- |
| [[!UICONTROL Sources]](../inventory-management/sources-assign-per-product.md) | (Quando [[!DNL Inventory Management]](../inventory-management/introduction.md) è abilitato) Elenca le origini da cui è possibile distribuire il prodotto. |
| [[!UICONTROL Content]](product-content.md) | Utilizzato per inserire e modificare la descrizione del prodotto principale che viene visualizzata nella pagina del prodotto vetrina. |
| [[!UICONTROL Configurations]](product-configurations.md) | Elenca tutte le varianti esistenti del prodotto e può essere utilizzato per generare varianti da utilizzare con il tipo di prodotto Configurabile. |
| [[!UICONTROL Product Reviews]](settings-advanced-product-reviews.md) | Elenca tutte le recensioni inviate dai clienti per il prodotto. |
| [[!UICONTROL Search Engine Optimization]](product-search-engine-optimization.md) | Specifica i campi Chiave URL e metadati utilizzati dai motori di ricerca per indicizzare il prodotto. |
| [[!UICONTROL Related Products, Up-Sells, and Cross-Sells]](related-products-up-sells-cross-sells.md) | Utilizzato per impostare semplici blocchi promozionali sulla vetrina che presentano una selezione di prodotti aggiuntivi che potrebbero essere di interesse per il cliente. |
| [[!UICONTROL Customizable Options]](settings-advanced-custom-options.md) | Aggiunge opzioni personalizzabili a un prodotto. |
| [[!UICONTROL Product in Websites]](settings-basic-websites.md) | Identifica ogni sito web in cui il prodotto è disponibile, in base alla gerarchia del negozio. |
| [[!UICONTROL Design]](settings-advanced-design.md) | Utilizzato per applicare un tema diverso alla pagina del prodotto, modificare il layout delle colonne, determinare dove vengono visualizzate le opzioni del prodotto e immettere un codice XML personalizzato. |
| [[!UICONTROL Gift options]](product-gift-options.md) | Utilizzato per abilitare o disabilitare un&#39;opzione di messaggio regalo durante il pagamento a livello di prodotto. |
| [[!UICONTROL Product In Shared Catalogs]](../b2b/catalog-shared.md) | ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile solo con [Adobe Commerce B2B](../b2b/introduction.md)) consente di gestire cataloghi condivisi con prezzi personalizzati per diverse società. |
| [[!UICONTROL Downloadable Information]](product-create-downloadable.md#step-5-complete-the-downloadable-information) | Utilizzato per definire i parametri per il download del prodotto. |

{style="table-layout:auto"}

## Prezzi e scorte avanzati

Per accedere alle impostazioni avanzate di inventario e prezzi, fare clic sul collegamento seguente **[!UICONTROL Price]** e **[!UICONTROL Quantity]**. Per ulteriori informazioni, vedere [Gestione dei prezzi](pricing-advanced.md) e [Inventory management](../inventory-management/introduction.md).
