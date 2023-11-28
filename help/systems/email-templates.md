---
title: Modelli e-mail
description: Scopri i modelli e-mail e come utilizzarli per supportare le comunicazioni con i clienti e rafforzare il tuo marchio.
exl-id: dfe28c77-607e-41e4-b872-3a07bcd67962
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# Modelli e-mail

I modelli e-mail definiscono il layout, il contenuto e la formattazione dei messaggi automatizzati inviati dal tuo archivio. Sono denominate e-mail transazionali perché ciascuna di esse è associata a un tipo specifico di transazione o evento.

Commerce include un set di modelli e-mail dinamici attivati da vari eventi che si verificano durante il funzionamento dell’archivio. Ogni modello è ottimizzato per qualsiasi dimensione di schermo e può essere visualizzato dal desktop, nonché su tablet e dispositivi mobili. Sono disponibili vari modelli e-mail preparati relativi ad attività cliente, vendite, avvisi sui prodotti, azioni di amministrazione e messaggi di sistema [personalizzare](email-template-custom.md) per rispecchiare il tuo marchio.

Le e-mail Commerce possono essere visualizzate da client e-mail HTML e di testo normale. Potrebbero esserci alcune varianti tra i client nel modo in cui vengono riprodotte le e-mail.

## Prepara il logo e-mail

I logo possono essere salvati in uno dei seguenti tipi di file. I logo con sfondi trasparenti possono essere salvati come file .GIF o .PNG.

- JPG/JPEG
- GIF
- PNG

Sono presenti dimensioni specificate nel modello di intestazione. Tuttavia, per garantire che il logo venga riprodotto correttamente su dispositivi ad alta risoluzione, l’immagine caricata dovrebbe avere dimensioni tre volte superiori. In genere, la grafica originale del logo viene creata come immagine vettoriale, in modo da poter essere ridimensionata senza perdere la risoluzione. L&#39;immagine può quindi essere salvata in uno dei formati di immagine bitmap supportati.

<!-- ![Logo 3X display size](./assets/email-logo-third-size.png)-->

Per sfruttare lo spazio verticale limitato nell’intestazione, assicurati di ritagliare l’immagine per eliminare lo spazio sprecato nella parte superiore o inferiore. Durante la modifica dell&#39;immagine, prestare attenzione a mantenere le proporzioni del logo, in modo che l&#39;altezza e la larghezza vengano ridimensionate in modo proporzionale.

Di regola, potete rendere un&#39;immagine più piccola dell&#39;originale, ma non più grande senza perdere la risoluzione. Scattare una piccola immagine e ridimensionarla in un editor fotografico riduce la risoluzione dell&#39;immagine. Ad esempio, se le dimensioni di visualizzazione del logo sono di 168 pixel di larghezza per 48 pixel di altezza nel modello di intestazione, l’immagine caricata deve avere una larghezza di 504 pixel per 144 pixel di altezza.

| Dimension logo | 1 x (dimensioni del display) | 3 x (dimensioni immagine) |
|----------|----|----|
| Larghezza: | 168 px | 504 px |
| Altezza: | 48 px | 144 px |

{style="table-layout:auto"}

## Configurare i modelli e-mail

La configurazione determina il logo visualizzato nel modello di intestazione predefinito ed eventuali [intestazione](email-template-custom.md#header-template) e [footer](email-template-custom.md#footer-template) modelli che desideri utilizzare per i messaggi e-mail transazionali inviati dai tuoi store.

![Progettazione delle e-mail transazionali](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

Per un elenco dettagliato delle impostazioni di configurazione, vedi [_E-mail transazionali_](../content-design/configuration.md) nel _Guida ai contenuti e alla progettazione_.

## Passaggio 1: Carica il logo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Individuare la visualizzazione dello store che si desidera configurare e fare clic su **[!UICONTROL Edit]** nel _[!UICONTROL Action]_colonna.

1. Sotto _[!UICONTROL Other Settings]_, espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Transactional Emails]**sezione.

1. Per caricare il file preparato **[!UICONTROL Logo Image]**, fai clic su **[!UICONTROL Upload]** e selezionare il file dal sistema.

1. Per **[!UICONTROL Logo Image Alt]**, immettere un testo alternativo per identificare l&#39;immagine.

1. Inserisci il **[!UICONTROL Logo Width]** e **[!UICONTROL Logo Height]** in pixel.

   Inserisci ciascun valore come numero, senza `px` abbreviazione. Questi valori si riferiscono alle dimensioni di visualizzazione del logo nell’intestazione e non alle dimensioni effettive dell’immagine.

## Passaggio 2: Scegliere i modelli di intestazione e piè di pagina

Se disponi di modelli di intestazione e piè di pagina personalizzati per il tuo Negozio o per negozi diversi, puoi specificare quali modelli vengono utilizzati per ciascuno, in base al [ambito](../getting-started/websites-stores-views.md#scope-settings) della configurazione. In caso contrario, vengono utilizzati i modelli predefiniti. Per ulteriori informazioni, consulta [Personalizzazione dei modelli e-mail](email-template-custom.md).

1. Scegli la **[!UICONTROL Header Template]** da utilizzare per tutti i messaggi e-mail transazionali.

1. Scegli la **[!UICONTROL Footer Template]** da utilizzare per tutti i messaggi e-mail transazionali.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Elenco modelli e-mail

L’elenco dei modelli e-mail è organizzato alfabeticamente per modulo.

### [!DNL Amazon_Payment]

| Modello | Percorso di configurazione |
|--- |--- |
| `Hard-declined Authorization` | n/d |
| `Soft-declined Authorization` | n/d |

{style="table-layout:auto"}

### [!DNL Magento_Checkout]

| Modello | Percorso di configurazione |
|--- |--- |
| `Payment Failed` | **Pagina:** [!UICONTROL Sales] > [[!UICONTROL Checkout]](../configuration-reference/sales/checkout.md)<br/>**Sezione:** [!UICONTROL Payment Failed Emails]<br/>**Campo:** [!UICONTROL Payment Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_Company]

![B2B per Adobe Commerce](../assets/b2b.svg) (Disponibile solo con B2B per Adobe Commerce)

| Modello | Percorso di configurazione |
|--- |--- |
| `Assign Company Admin` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Assign Company Admin' Email] |
| `Assign Company to Customer` | **Pagina:** [!UICONTROL Customers] > [Configurazione società&#x200B;](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Customer-Related Emails] <br/>**Campo:** [!UICONTROL Default 'Assign Company to Customer' Email] |
| `Company Admin Changed to Member` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Company Admin Changed To Member' Email] |
| `Company Admin Set Inactive` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Customer Status Inactive' Email] |
| `Company Invite` | n/d |
| `Company Registration Request` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Email Options - Company Registration]<br/>**Campo:** [!UICONTROL Default Company Registration Email] |
| `Company Status Active1` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Company Status Change]<br/>**Campo:** [!UICONTROL Default 'Company Status Change To Active 1" Email] |
| `Company Status Active2` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Company Status Change]<br/>**Campo:** [!UICONTROL Default 'Company Status Change To Active 2" Email] |
| `Company Status Blocked` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Company Status Change]<br/>**Campo:** [!UICONTROL Default 'Company Status Change To Blocked" Email] |
| `Company Status Pending Approval` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Company Status Change]<br/>**Campo:** [!UICONTROL Default 'Company Status Change To Pending Approval" Email] |
| `Company Status Rejected` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Company Status Change]<br/>**Campo:** [!UICONTROL Default 'Company Status Change To Rejected" Email] |
| `Customer Status Active` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Customer Status Active' Email] |
| `Customer Status Inactive` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Company Admin Inactive' Email] |
| `Sales Representative Assigned to Company` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Customer-Related Emails]<br/>**Campo:** [!UICONTROL Default 'Sales Rep Assigned' Email] |

{style="table-layout:auto"}

### [!DNL Magento_CompanyCredit]

![B2B per Adobe Commerce](../assets/b2b.svg) (Disponibile solo con B2B per Adobe Commerce)

| Modello | Percorso di configurazione |
|--- |--- |
| `Credit Limit Allocated` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Company Credit]<br/>**Campo:** [!UICONTROL Allocated Email Template] |
| `Credit Limit Updated` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Company Credit]<br/>**Campo:** [!UICONTROL Updated Email Template] |
| `Credit Reimbursed` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Company Credit]<br/>**Campo:** [!UICONTROL Reimbursed Email Template] |
| `Order Refunded to Company Credit` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Company Credit]<br/>**Campo:** [!UICONTROL Refunded Email Template] |
| `Order Reverted to Company Credit` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Sezione:** [!UICONTROL Company Credit]<br/>**Campo:** [!UICONTROL Reverted Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Contact]

| Modello | Percorso di configurazione |
|--- |--- |
| `Contact Form` | **Pagina:** [!UICONTROL General] > [[!UICONTROL Contacts]](../configuration-reference/general/contacts.md)<br/>**Sezione:** [!UICONTROL Email Options]<br/>**Campo:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Customer]

| Modello | Percorso di configurazione |
|--- |--- |
| `Change Email` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Account Information Options]<br/>**Campo:** [!UICONTROL Change Email Template] |
| Modifica e-mail e password | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Account Information Options]<br/>**Campo:** [!UICONTROL Change Email and Password Template] |
| `Forgot Password` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Password Options]<br/>**Campo:** Modello e-mail dimenticato |
| `New Account` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Create New Account Options]<br/>**Campo:** E-mail di benvenuto predefinita |
| `New Account (Magento/luma)` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Create New Account Options]<br/>**Campo:** E-mail di benvenuto predefinita |
| `New Account Confirmation Key` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Create New Account Options]<br/>**Campo:** E-mail collegamento conferma |
| `New Account Confirmed` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Create New Account Options]<br/>**Campo:** E-mail di benvenuto |
| `New Account Without Password` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Create New Account Options]<br/>**Campo:** E-mail di benvenuto predefinita senza password |
| `Remind Password` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Password Options]<br/>**Campo:** Ricorda modello e-mail |
| `Reset Password` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Password Options] <br/>**Campo:** Ripristina modello password |

{style="table-layout:auto"}

### [!DNL Magento_CustomerBalance]

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

| Modello | Percorso di configurazione |
|--- |--- |
| `Store Credit Update` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Sezione:** [!UICONTROL Store Credit Options]<br/>**Campo:** [!UICONTROL Store Credit Update Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Directory]

| Modello | Percorso di configurazione |
|--- |--- |
| `Currency Update Warnings` | **Pagina:** [!UICONTROL General] > [[!UICONTROL Currency Setup]](../configuration-reference/general/currency-setup.md)<br/>**Sezione:** [!UICONTROL Scheduled Import Settings]<br/>**Campo:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Email]

| Modello | Percorso di configurazione |
|--- |--- |
| `Footer` | n/d |
| `Footer (Magento/luma)` | n/d |
| `Header` | n/d |

{style="table-layout:auto"}

### [!UICONTROL Magento_GiftCard]

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

| Modello | Percorso di configurazione |
|--- |--- |
| `Gift Card(s) Purchase` | **Pagina:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Sezione:** [!UICONTROL Gift Card Email Settings]<br/>**Campo:** [!UICONTROL Gift Card Notification Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftCardAccount]

| Modello | Percorso di configurazione |
|--- |--- |
| `Gift Card Code/Balance` | **Pagina:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Sezione:** [!UICONTROL Email Sent from Gift Card Account Management]<br/>**Campo:** [!UICONTROL Gift Card Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftRegistry]

| Modello | Percorso di configurazione |
|--- |--- |
| `New Registry` | **Pagina:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Sezione:** [!UICONTROL Owner Notification]<br/>**Campo:** [!UICONTROL Email Template] |
| `Registry Sharing` | **Pagina:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Sezione:** [!UICONTROL Gift Registry Sharing]<br/>**Campo:** [!UICONTROL Email Template] |
| `Registry Update` | **Pagina:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Sezione:** [!UICONTROL Gift Registry Update]<br/>**Campo:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_InventoryInStorePickupSales]

| Modello | Percorso di configurazione |
|--- |--- |
| `Order is Ready for Pickup` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Campo:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Order is Ready for Pickup For Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Campo:** [!UICONTROL Order Ready For Pickup Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_Invitation]

| Modello | Percorso di configurazione |
|--- |--- |
| `Customer Invitation` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Invitation]](../configuration-reference/customers/invitations.md)<br/>**Sezione:** [!UICONTROL Email]<br/>**Campo:** [!UICONTROL Customer Invitation Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_NegotiableQuote]

![B2B per Adobe Commerce](../assets/b2b.svg) (Disponibile solo con B2B per Adobe Commerce)

| Modello | Percorso di configurazione |
|--- |--- |
| `Declined Quote` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Declined Quote Template (to Buyer)] |
| `Expiration Date Reset` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Expiration Date Reset] | **Pagina:** [!UICONTROL Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Expiration Warning` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Quote Expiration (in 48 hrs)] |
| `Expiration Warning1` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Quote Expiration (in 24 hrs)] |
| `New Quote` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL New Quote Template (to Seller)] |
| `Updated Quote` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Quote]<br/>**Campo:** [!UICONTROL Updated Quote Template (to Seller)] |

{style="table-layout:auto"}

### [!DNL Magento_Newsletter]

| Modello | Percorso di configurazione |
|--- |--- |
| `Subscription Confirmation` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Sezione:** [!UICONTROL  Subscription Options]<br/>**Campo:** [!UICONTROL Confirmation Email Template] |
| `Subscription Success` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Sezione:** [!UICONTROL  Subscription Options]<br/>**Campo:** [!UICONTROL Success Email Template] |
| `Unsubscription Success` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Sezione:** [!UICONTROL  Subscription Options]<br/>**Campo:** [!UICONTROL Unsubscription Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_ProductAlert]

| Modello | Percorso di configurazione |
|--- |--- |
| `Cron Error Warning` | **Pagina:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Sezione:** [!UICONTROL Product Alerts Run Settings]<br/>**Campo:** [!UICONTROL Error Email Template] |
| `Price Alert` | **Pagina:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Sezione:** [!UICONTROL Product Alerts]<br/>**Campo:** [!UICONTROL Price Alert Email Template] |
| `Stock Alert` | **Pagina:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Sezione:** [!UICONTROL Product Alerts]<br/>**Campo:** [!UICONTROL Stock Alert Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_PurchaseOrder]

| Modello | Percorso di configurazione |
|--- |--- |
| `Approved Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Approved Purchase Order] |
| `Approved, requires payment` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Approved, requires payment details (to Buyer)] |
| `Comment added to Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Comment added to Purchase Order] |
| `Created and Auto-approved Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] |
| `Created and automatically approved, requires payment details` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Created and automatically approved, requires payment details (to Buyer)] |
| `Created and requires Approval Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] |
| `Error creating Order from Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Error creating Order from Purchase Order (to Buyer)] |
| `Purchase Order requires Approval` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Purchase Order requires Approval (to Approver)] |
| `Rejected Purchase Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL Purchase Order Approval]<br/>**Campo:** [!UICONTROL Rejected Purchase Order (to Buyer)] |

{style="table-layout:auto"}

### [!DNL Magento_Reminder]

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

| Modello | Percorso di configurazione |
|--- |--- |
| `Promotion Notification/Reminder` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Promotions]](../configuration-reference/customers/promotions.md)<br/>**Sezione:** [!UICONTROL Automated Email Reminder Rules]<br/>**Campo:** [!UICONTROL Reminder Email Sender] |

{style="table-layout:auto"}

### [!DNL Magento_Reward]

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

| Modello | Percorso di configurazione |
|--- |--- |
| `Balance Update` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Sezione:** [!UICONTROL Email Notification Settings]<br/>**Campo:** [!UICONTROL Balance Update Email] |
| `Points Expiry Warning` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Sezione:** [!UICONTROL Email Notification Settings]<br/>**Campo:** [!UICONTROL Reward Points Expiry Warning Email] |

{style="table-layout:auto"}

### [!DNL Magento_Rma]

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

| Modello | Percorso di configurazione |
|--- |--- |
| `New RMA` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL  RMA]<br/>**Campo:** [!UICONTROL RMA Email Template] |
| `New RMA for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL  RMA]<br/>**Campo:** [!UICONTROL RMA Email Template for Guest] |
| `RMA Admin Comments` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL  RMA Admin Comments]<br/>**Campo:** [!UICONTROL RMA Comment Email Template] |
| `RMA Admin Comments for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL  RMA Admin Comments]<br/>**Campo:** [!UICONTROL RMA Comment Email Template for Guest] |
| `RMA Authorization` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL  RMA Authorization]<br/>**Campo:** [!UICONTROL RMA Authorization Email Template] |
| `RMA Authorization for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL  RMA Authorization]<br/>**Campo:** [!UICONTROL RMA Authorization Email Template for Guest] |
| `RMA Customer Comments` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Sezione:** [!UICONTROL RMA Customer Comments]<br/>**Campo:** [!DNL RMA Comment Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sales]

| Modello | Percorso di configurazione |
|--- |--- |
| `Credit Memo Update` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Credit Memo Contents]<br/>**Campo:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Credit Memo Comments]<br/>**Campo:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Credit Memo Comments]<br/>**Campo:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Credit Memo Update for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Credit Memo Comments]<br/>**Campo:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Invoice Update` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Invoice Comments]<br/>**Campo:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Invoice Comments]<br/>**Campo:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Invoice Comments]<br/>**Campo:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `Invoice Update for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Invoice Comments]<br/>**Campo:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `New Credit Memo` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Credit Memo]<br/>**Campo:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]]../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Credit Memo]<br/>**Campo:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Credit Memo]<br/>**Campo:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Credit Memo for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Credit Memo]<br/>**Campo:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Invoice` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Invoice]<br/>**Campo:** [!UICONTROL Invoice Email Template] |
| `New Invoice (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Invoice]<br/>**Campo:** [!UICONTROL Invoice Email Template] |
| `New Invoice for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Invoice]<br/>**Campo:** [!UICONTROL Invoice Email Template for Guest] |
| `New Invoice for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Invoice]<br/>**Campo:** [!UICONTROL Invoice Email Template for Guest] |
| `New Order` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Order]<br/>**Campo:** [!UICONTROL New Order Confirmation Template] |
| `New Order (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Order]<br/>**Campo:** [!UICONTROL New Order Confirmation Template] |
| `New Order for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Order]<br/>**Campo:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Order for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Order]<br/>**Campo:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Shipment` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Shipment]<br/>**Campo:** [!UICONTROL Shipment Email Template] |
| `New Shipment (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Shipment]<br/>**Campo:** [!UICONTROL Shipment Email Template] |
| `New Shipment for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Shipment]<br/>**Campo:** [!UICONTROL Shipment Email Template for Guest] |
| `New Shipment for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Shipment]<br/>**Campo:** [!UICONTROL Shipment Email Template for Guest] |
| `Order Update` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Order Comments]<br/>**Campo:** [!UICONTROL Order Comment Email Template] |
| `Order Update (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Order Comments]<br/>**Campo:** [!UICONTROL Order Comment Email Template] |
| `Order Update for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Order Comments]<br/>**Campo:** [!UICONTROL Order Comment Email Template for Guest] |
| `Order Update for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Order Comments]<br/>**Campo:** [!UICONTROL Order Comment Email Template for Guest] |
| `Shipment Update` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Shipment Comments]<br/>**Campo:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Shipment Comments]<br/>**Campo:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update for Guest` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Shipment Comments]<br/>**Campo:** [!UICONTROL Shipment Comment Email Template for Guest] |
| `Shipment Update for Guest (Magento/luma)` | **Pagina:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Sezione:** [!UICONTROL Shipment Comments]<br/>**Campo:** [!UICONTROL Shipment Comment Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_ScheduledImportExport]

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

| Modello | Percorso di configurazione |
|--- |--- |
| `Export Failed` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Sezione:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Campo:** [!UICONTROL Export Failed Template] |
| `File History Clean Failed` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Sezione:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Campo:** [!UICONTROL Error Email Template] |
| `Import Failed` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Sezione:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Campo:** [!UICONTROL Import Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_SendFriend]

| Modello | Percorso di configurazione |
|--- |--- |
| `Send Product Link to Friend` | **Pagina:** [!UICONTROL Catalog] > [[!UICONTROL Email to a Friend]](../configuration-reference/catalog/email-to-a-friend.md)<br/>**Sezione:** [!UICONTROL Email Templates]<br/>**Campo:** [!UICONTROL Select Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sitemap]

| Modello | Percorso di configurazione |
|--- |--- |
| `Sitemap Generation Settings` | **Pagina:** [!UICONTROL Catalog] > [[!UICONTROL XML Sitemap]](../configuration-reference/catalog/xml-sitemap.md)<br/>**Sezione:** [!UICONTROL Generation Settings]<br/>**Campo:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_TwoFactorAuth]

| Modello | Percorso di configurazione |
|--- |--- |
| `2FA Configuration Required by User` | n/d |
| `2FA Configuration Required for the Application` | n/d |

{style="table-layout:auto"}

### [!DNL Magento_User]

| Modello | Percorso di configurazione |
|--- |--- |
| `Forgot Admin Password` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Sezione:** [!UICONTROL Admin User Emails]<br/>**Campo:** Modello e-mail per password dimenticata |
| `User Notification` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Sezione:** [!UICONTROL Admin User Emails]<br/>**Campo:** Modello di notifica utente |
| `New User Notification` | **Pagina:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Sezione:** [!UICONTROL Admin User Emails]<br/>**Campo:** [!UICONTROL New User Notification Template] |

{style="table-layout:auto"}

### [!DNL Magento_Wishlist]

| Modello | Percorso di configurazione |
|--- |--- |
| `Magento Wish List Sharing` | **Pagina:** [!UICONTROL Customers] > [[!UICONTROL Wish List]](../configuration-reference/customers/wishlist.md)<br/>**Sezione:** [!UICONTROL Share Options]<br/>**Campo:** [!UICONTROL Email Template] |

{style="table-layout:auto"}
