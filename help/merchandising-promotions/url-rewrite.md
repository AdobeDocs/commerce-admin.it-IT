---
title: Riscritture URL
description: Scopri come riscrivere gli URL e come utilizzare lo strumento di riscrittura URL di Commerce per modificare gli URL associati a una pagina di prodotto, categoria o CMS.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 2f2db4926ff92adfa27692eeca872c1765fd31d6
workflow-type: tm+mt
source-wordcount: '905'
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

Se disponi di una singola pagina accessibile da più URL o da pagine diverse con contenuto simile, Google le considera come versioni duplicate della stessa pagina. Google sceglie un URL come versione canonica e esegue la ricerca per indicizzazione di tale URL e di tutti gli altri URL, considerati duplicati, vengono eseguiti con minore frequenza.

Se non dici esplicitamente a Google quale URL è canonico, effettua la scelta o potrebbe considerarli entrambi di peso uguale. Ciò potrebbe causare un comportamento indesiderato, con il rischio di un budget di ricerca per indicizzazione inefficace e di collegamenti retroversi distribuiti ridotti.

A seconda di come configuri il sito web, nell’indice possono essere presenti più versioni del sito, ad esempio:

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Per specificare una pagina canonica, vedere [Documentazione di Google Search Central](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).
