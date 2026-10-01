---
title: Menu [!UICONTROL Stores]
description: L'amministratore di Commerce include il menu [!UICONTROL Stores], che fornisce l'accesso agli strumenti per l'impostazione della gerarchia del punto vendita, la configurazione, l'inventario, le imposte e gli attributi.
exl-id: b9d8ea6b-5b4b-42af-b74d-7afa48ccf2ff
TQID: https://experienceleague.adobe.com/LEoQUYqvin2UfF55kCMUiEUh8YungghN-VuEwUOu7gY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%
---
# Menu [!UICONTROL Stores]

Il menu _[!UICONTROL Stores]_consente di accedere alle impostazioni utilizzate meno frequentemente, ma a cui si fa riferimento durante l&#39;installazione di Adobe Commerce o Magento Open Source. Queste funzioni includono l’impostazione della gerarchia del negozio, la configurazione, le impostazioni di vendita e ordine, le imposte e la valuta, gli attributi del prodotto, le valutazioni di recensione del prodotto e i gruppi di clienti.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

![Amministratore - Menu Archivi](./assets/stores-menu.png){width="500" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce as a Cloud Service e Adobe Commerce Optimizer (infrastruttura SaaS gestita da Adobe)."}

![Amministratore - Menu Archivi](./assets/stores-menu-accs.png){width="500" zoomable="yes"}

>[!ENDTABS]

## Visualizza il menu [!UICONTROL Stores]

Nella barra laterale _Admin_, fai clic su **[!UICONTROL Stores]**.

## Sezioni principali

### [!UICONTROL Settings]

Gestisci la gerarchia di [siti Web, archivi e visualizzazioni dello store](stores.md#store-and-site-structure) nell&#39;installazione di Adobe Commerce o Magento Open Source e tutte le [impostazioni di configurazione](../configuration-reference/guide-overview.md). Inoltre, puoi impostare i [Termini e condizioni](terms-and-conditions.md) di una vendita e gestire le [impostazioni dello stato dell&#39;ordine](order-status.md#custom-order-status).

### [!UICONTROL Inventory]

[Gestisci e crea scorte](../inventory-management/introduction.md) per collegare i tuoi canali di vendita o siti Web a [sorgenti](../inventory-management/sources-manage.md). Le scorte forniscono una quantità aggregata di prodotti vendibili. I commercianti single Source utilizzano il titolo predefinito, mentre i commercianti multi-Source utilizzano titoli personalizzati aggiuntivi.

### [!UICONTROL Taxes]

Gestisci tutti i tipi di [funzioni fiscali](taxes.md) nel tuo store, imposta le regole fiscali per il tuo store, definisci le classi fiscali per clienti e prodotti e gestisci le aree e le aliquote fiscali. Puoi anche importare i dati dell’aliquota fiscale nel tuo store.

### [!UICONTROL Currency]

Gestisci i tassi per le [valute](currency.md) accettate come pagamento nel tuo Negozio e personalizza i simboli di valuta visualizzati nei prezzi dei prodotti e nei documenti di vendita.

### [!UICONTROL Attributes]

Gestisci gli attributi utilizzati per [informazioni sul cliente](../customers/attribute-properties.md) o [informazioni sul prodotto](../catalog/attribute-product-create.md), resi e valutazioni del prodotto. È possibile creare attributi, modificare attributi esistenti e gestire [set di attributi](../catalog/attribute-sets.md).

### [!UICONTROL Other Settings]

Gestisci impostazioni aggiuntive per [premi tassi di cambio](../merchandising-promotions/reward-exchange-rates.md), [confezione regalo](cart-configuration.md#gift-wrap) e [registri regali](../merchandising-promotions/gift-registries.md).

## Integrazione di [!DNL Adobe Commerce Optimizer]

Una volta installato [!DNL Adobe Commerce Optimizer Connector], è possibile sincronizzare il sito Web e archiviare i dati di visualizzazione in [!DNL Adobe Commerce Optimizer]. L&#39;ambito del sito Web controlla [sincronizzazione prezzi](stores.md#step-1-create-a-website) (listini prezzi e listini prezzi). Controlli dell&#39;ambito di visualizzazione dell&#39;archivio [sincronizzazione prodotti](store-views.md#add-a-store-view) (prodotti e attributi prodotto).

Per gli indicatori dello stato di sincronizzazione visualizzati nella griglia [!UICONTROL All Stores], vedere [Stato di sincronizzazione di Adobe Commerce Optimizer](store-views.md#optimizer-sync-status). Per informazioni sul comportamento di configurazione e configurazione del connettore, vedere [Personalizzare la configurazione di esportazione degli ambiti di Commerce](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/get-started#customize-the-commerce-scopes-export-configuration) nella *Guida al connettore di Adobe Commerce Optimizer*.

Se [!DNL Adobe Commerce Optimizer Connector for B2B] è installato, i dati vengono sincronizzati anche per i cataloghi condivisi B2B disponibili. Vedi [Gestire le visualizzazioni del catalogo](../b2b/catalog-views-manage.md).
