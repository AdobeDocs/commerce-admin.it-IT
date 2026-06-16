---
title: Riscritture URL
description: Scopri come riscrivere gli URL e come utilizzare lo strumento di riscrittura URL di Commerce per modificare gli URL associati a una pagina di prodotto, categoria o CMS.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/fuILlBHCevV6rfQT-PUiuBPBgWkFXDbFofgde8O5BCM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 940
ht-degree: 0%

---

# Riscritture URL

>[!TIP]
>
>Per Adobe Commerce as a Cloud Service, consulta le [linee guida SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=it) nella documentazione di Commerce Storefront

Lo strumento di riscrittura URL consente di modificare qualsiasi URL associato a un prodotto, una categoria o una pagina CMS. Quando crei una riscrittura URL, Commerce crea automaticamente un reindirizzamento permanente (301) in modo che tutti i collegamenti che puntano al vecchio URL vengano reindirizzati al nuovo indirizzo.

>[!NOTE]
>
>Per aggiornare le riscritture URL per più o tutti i prodotti contemporaneamente, fare riferimento a [Più riscritture URL](url-rewrite-product.md#multiple-url-rewrites).

>[!BEGINSHADEBOX &quot;Informazioni su riscritture e reindirizzamenti&quot;]

I termini _rewrite_ e _redirect_ vengono spesso utilizzati in modo intercambiabile, ma si tratta di operazioni diverse:

* **Riscrittura URL**: processo lato server che esegue il mapping interno di un URL a un altro senza modificare gli elementi visualizzati nella barra degli indirizzi del browser. Quando un visitatore richiede un URL, il server lo elabora come un URL diverso dietro le quinte, ma il browser continua a visualizzare l’URL originale.

* **URL Redirect** - Invia una risposta HTTP al browser per indicare di passare a un URL diverso. La barra degli indirizzi del browser si aggiorna e mostra il nuovo URL. I reindirizzamenti possono essere temporanei (302) o permanenti (301).

>[!ENDSHADEBOX]

## Funzionamento dello strumento Riscritture

In Adobe Commerce, per impostazione predefinita, lo strumento di riscrittura URL crea reindirizzamenti permanenti (301) per mantenere il valore SEO (Search Engine Optimization) quando si modifica il codice URL di un prodotto, di una categoria o di una pagina. Questo comportamento assicura che i collegamenti esistenti continuino a funzionare e che le classificazioni dei motori di ricerca siano mantenute.

Per impostazione predefinita, [i reindirizzamenti URL automatici](url-redirect-product-automatic.md) sono abilitati per l&#39;archivio e la casella di controllo **Crea reindirizzamento permanente per il vecchio URL** è selezionata nel campo chiave URL di ciascun prodotto.

{{url-rewrite-skip}}

![Ottimizzazione motore di ricerca - crea reindirizzamento URL permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

{{url-rewrite-params}}

## URL riscrive demo

Guarda il video seguente per scoprire come gestire le riscritture URL:

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)

## Crea riscritture URL

Utilizza lo strumento URL rewrites per creare reindirizzamenti di prodotti e categorie e reindirizzamenti personalizzati per qualsiasi pagina del tuo archivio. Quando si applica la configurazione di riscrittura dell’URL, tutti i collegamenti esistenti che puntano all’URL precedente vengono reindirizzati direttamente al nuovo indirizzo.

Puoi creare riscritture URL in:

* Aggiungi parole chiave di alto valore per migliorare il modo in cui il prodotto viene indicizzato dai motori di ricerca.

* Aggiungi ulteriori URL per una modifica stagionale temporanea o permanente.

* Aggiungi un percorso valido per una pagina, incluse le pagine di contenuto CMS. Ad esempio, puoi creare un URL per creare un URL più semplice da usare o SEO (Search Engine Optimization) su un sistema che fa sempre riferimento a prodotti e categorie in base al loro ID interno.

Le riscritture URL create possono essere reindirizzate a categorie esistenti o pagine personalizzate senza modificare la struttura del sito, semplificando così la creazione di URL memorabili per le campagne di marketing.

![URL riscrive griglia](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce offre i seguenti tipi di riscrittura URL:

* [Riscritture prodotto](url-rewrite-product.md)
* [Riscritture categoria](url-rewrite-category.md)
* [Riscrittura della pagina CMS](url-rewrite-cms-page.md)
* [Riscritture personalizzate](url-rewrite-custom.md)

### Casi d’uso ed esempi

Le riscritture URL sono comunemente utilizzate in questi scenari:

#### Modificare un URL di sistema interno in un URL compatibile con SEO

Commerce utilizza internamente gli URL basati su ID, ma puoi creare URL compatibili con SEO per i clienti:

**URL di sistema (interno):**

    http://www.example.com/catalog/category/id/6

**URL rivolto al cliente:**

    http://www.example.com/peripherals/keyboard.html

#### Rinnovo del prodotto o ottimizzazione URL

Quando rinomini un prodotto o desideri migliorarne l’URL per SEO (Search Engine Optimization), crea un reindirizzamento per mantenere i collegamenti esistenti:

**URL originale:**

    http://www.example.com/peripherals/keyboard.html

**Nuovo URL ottimizzato:**

    http://www.example.com/ergonomic-keyboard.html

Lo strumento Riscritture crea automaticamente un reindirizzamento 301 dal vecchio URL a quello nuovo, in modo che i clienti e i motori di ricerca vengano indirizzati direttamente alla pagina corretta.

#### Pagine di destinazione promozionali

Creare URL personalizzati temporanei o permanenti per le campagne di marketing:

**URL promozionali:**

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

## Configurazione aggiuntiva di gestione URL

Nelle sezioni seguenti viene descritto come configurare le riscritture dei server web e gli URL canonici per Commerce.

### Configura riscritture server Web

>[!NOTE]
>
>Questa sezione descrive la riscrittura degli URL a livello di server web, diversa dalla funzionalità dello strumento URL Rewrite. Il server Web riscrive la gestione della formattazione degli URL tecnici (ad esempio rimuovendo `index.php`), mentre lo strumento di riscrittura URL gestisce i reindirizzamenti per le modifiche al contenuto.

L&#39;abilitazione delle riscritture del server web fa parte della configurazione iniziale di Commerce ed è in genere configurata durante l&#39;installazione. Quando è abilitato, il server Web (Apache o Nginx) rimuove automaticamente il nome file `index.php` dagli URL, creando indirizzi più puliti e compatibili con SEO.
L’esempio seguente mostra come vengono visualizzati gli URL con e senza le riscritture del server web abilitate:

**URL senza riscrittura server Web**

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

**URL con riscrittura server Web**

    http://www.yourdomain.com/magento/storeview/url-identifier

#### Attiva o disattiva riscritture server Web:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in cui è espanso **[!UICONTROL General]**, scegli **[!UICONTROL Web]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]**.

   ![Configurazione generale - ottimizzazione motore di ricerca Web](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Use Web Server Rewrites]** sulla tua preferenza.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

### Specificare gli URL canonici

Ai fini SEO, ogni pagina web deve avere un solo URL distinto.

Se disponi di una singola pagina accessibile da più URL o da pagine diverse con contenuto simile, Google le considera come versioni duplicate della stessa pagina. Google sceglie un URL come versione canonica e scansiona che, e tutti gli altri URL, sono considerati URL duplicati e vengono scansionati meno spesso.

Se non dici esplicitamente a Google quale URL è canonico, effettua la scelta o potrebbe considerarli entrambi di peso uguale. Questo potrebbe portare a comportamenti indesiderati e rischia di compromettere l’efficacia del budget di scansiono e la presenza di collegamenti di backlink distribuiti.

A seconda di come configuri il sito web, nell’indice possono essere presenti più versioni del sito, ad esempio:

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Per specificare una pagina canonica, vedere [Documentazione di Google Search Central](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).
