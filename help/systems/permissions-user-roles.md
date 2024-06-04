---
title: Ruoli utente
description: Scopri come creare ruoli utente e le autorizzazioni associate per gestire l’accesso alle funzioni di amministrazione.
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# Ruoli utente

Per concedere a un utente un accesso limitato all’amministratore, il primo passaggio consiste nel creare un ruolo con il livello di autorizzazioni appropriato. Dopo il salvataggio del ruolo, puoi aggiungere nuovi utenti e assegnare il ruolo con restrizioni per concedere loro l’accesso limitato all’amministratore.

![Amministratore - Ruoli utente](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## Definisci un ruolo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add New Role]**.

1. Completa i passaggi per definire il ruolo:

### Passaggio 1: aggiungere il nome del ruolo

1. Sotto _[!UICONTROL Role Information]_, inserisci un valore descrittivo **[!UICONTROL Role Name]**.

1. Sotto _[!UICONTROL Current User Identity Verification]_, immettere la password.

   ![Autorizzazioni di sistema - Informazioni sul ruolo](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### Passaggio 2: assegnare le risorse

>[!IMPORTANT]
>
>Quando assegni le risorse, accertati di disabilitare l’accesso allo strumento Autorizzazioni se stai limitando l’accesso per un determinato ruolo. In caso contrario, gli utenti possono modificare le proprie autorizzazioni.

1. Imposta **[!UICONTROL Role Scopes]** a uno dei seguenti elementi:

   - `All`
   - `Custom`

   Se impostato su `Custom` per un&#39;installazione multisito, selezionare la casella di controllo del sito Web e archiviare il ruolo da utilizzare.

   ![Risorse per i ruoli utente - Ambito personalizzato](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Utenti con un `Custom` gli ambiti del ruolo non sono in grado di creare siti web e categorie, assegnare prodotti alle categorie o modificare prodotti in _[!UICONTROL All Store Views]_ambito quando vengono assegnati a archivi con restrizioni. Questi utenti non possono eseguire altre operazioni_ globale _azioni che interessano ambiti a cui non hanno accesso.

1. Sotto _[!UICONTROL Roles Resources]_, impostato **[!UICONTROL Resource Access]**a `Custom`.

1. In **[!UICONTROL Resource]** struttura ad albero, seleziona la casella di controllo di ogni funzionalità amministratore a cui il ruolo può accedere.

   Per creare un ruolo amministratore con accesso alle impostazioni relative alle imposte, scegliere le risorse Vendite/Imposta e Sistema/Imposta. Se si configura un sito Web per un&#39;area diversa da quella predefinita [punto di origine di spedizione](../stores-purchase/shipping-settings.md#point-of-origin), è necessario consentire l&#39;accesso alle risorse di sistema/spedizione per il ruolo. Le impostazioni di spedizione determinano l&#39;aliquota dell&#39;imposta del negozio utilizzata per i prezzi del catalogo.

   ![Risorse del ruolo utente assegnate](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   L’elenco delle autorizzazioni disponibili può includere opzioni aggiuntive per le estensioni in bundle e installate. Selezionando l’autorizzazione più in alto per ogni funzione, assegni tutte le autorizzazioni disponibili per l’utente.

   >[!NOTE]
   >
   >Un utente amministratore deve avere **[!UICONTROL Sales / Archive]** autorizzazioni per il loro ambito di ruolo per visualizzare _[!UICONTROL Invoices]_,_[!UICONTROL Credit Memos]_, e _[!UICONTROL Shipments]_ordine [schede](../stores-purchase/order-processing.md).

1. Al termine, fai clic su **[!UICONTROL Save Role]**.

   Il ruolo viene ora visualizzato nella griglia e può essere assegnato agli account utente.

## Assegnare un ruolo agli utenti

1. Dalla sezione _[!UICONTROL Roles]_nella griglia, aprire il record in modalità di modifica.

1. Sotto _[!UICONTROL Current User Identity Verification]_, immettere la password dell&#39;account utente.

1. Nel pannello a sinistra, scegli **[!UICONTROL Role Users]**.

   Il _[!UICONTROL Role Users]_L&#39;opzione viene visualizzata solo dopo il salvataggio di un nuovo ruolo.

   ![Account utente assegnati al ruolo](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. Per cercare un record utente specifico, effettuare le seguenti operazioni:

   - Immetti il valore nel filtro di ricerca nella parte superiore di una colonna e premi **Invio**.

   - Quando sei pronto a tornare all’elenco completo, fai clic su **[!UICONTROL Reset Filter]**.

1. Selezionare la casella di controllo degli utenti da assegnare al ruolo.

1. Clic **[!UICONTROL Save Role]**.

## Modificare un ruolo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Individuare il ruolo utilizzando i filtri sopra la griglia e fare clic sul nome del ruolo.

1. Apporta le modifiche necessarie.

   Per informazioni sulle impostazioni del ruolo, esaminare i passaggi per la creazione di un ruolo utente.

1. Quando richiesto, immettere la password per confermare l&#39;identità.

1. Fai clic su **[!UICONTROL Save Role]**.

## Eliminare una mansione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Individua il ruolo utilizzando i filtri sopra la griglia e apri in modalità di modifica.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Delete Role]**.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.

## Demo sui ruoli utente

Guarda questo video per scoprire come gestire i ruoli utente:

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12)

## Risorse per il ruolo

L’accesso alle seguenti risorse può essere assegnato a un ruolo personalizzato. Per ulteriori informazioni sulle funzionalità associate a ciascuna risorsa, consulta la pagina collegata.

![Adobe Commerce](../assets/adobe-logo.svg) - Solo Adobe Commerce

![Adobe Commerce B2B](../assets/b2b.svg) - Disponibile solo con Adobe Commerce B2B

| Risorsa |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![Adobe Commerce B2B](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
| [`Carts`](../stores-purchase/shopping-assisted-cart-manage.md) | [`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md) |  |
| [`My Account`](../customers/account-dashboard-my-account.md) |  |  |
| [`Marketing`](../merchandising-promotions/marketing-menu.md) | [`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions) | [`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) | [`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
|  | `Communications` | [`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
|  | `Sales Channel` | [`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html) |
|  | [`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search) | [`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md) |
|  | [`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> |  |
| [`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)) | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md) |  |
|  | [`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md) |  |
|  | [Staging dei contenuti](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
| [`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md) | `Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports` |  |
|  | [`Reviews`](../getting-started/review-reports.md)<br /> |  |
|  | [`Sales`](../getting-started/sales-reports.md) |  |
|  | `System Insights` ![Adobe Commerce](../assets/adobe-logo.svg) | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) |
|  | [`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md) |  |
| [`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md) |  |
|  | [`Inventory`](../inventory-management/sources-stocks.md) | [`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md) |  |
|  | [`Taxes`](../stores-purchase/taxes.md) |  |  |
|  | [`Currency`](../stores-purchase/currency.md) | [`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |  |
|  | [`Attributes`](../catalog/product-attributes.md) | [`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|  | [`Other Settings`](../stores-purchase/stores-menu.md) | [`Customer Groups`](../customers/customer-groups.md) |
| [`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history) |  |
|  | [`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions` |  |
|  | [`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) |  |
|  | [`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md) |
| [`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) | [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md) |
|  | [`Other Settings`](system-menu.md) | [`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md) |  |
| [`Global Search`](../getting-started/admin-workspace.md#workspace-search) |  |  |

{style="table-layout:auto"}
