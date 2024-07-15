---
title: Social media e feed RSS
description: Scopri come aggiungere i social media e altre integrazioni di feed RSS per creare consapevolezza del marchio e del prodotto.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# Social media e feed RSS

Molti commercianti utilizzano i social media e altri strumenti digitali per creare brand awareness e product awareness. Puoi integrare il tuo store con i social network installando un’estensione Marketplace o aggiungendo un plug-in alle pagine di contenuto. Utilizzare i feed RSS per pubblicare le informazioni sui prodotti sui siti di aggregazione degli acquisti e persino includerli nelle newsletter. I clienti possono abbonarsi ai feed RSS per conoscere i nuovi prodotti e le promozioni.

## Social network

Il tuo archivio può essere connesso ai social network installando una [estensione Marketplace](../getting-started/commerce-marketplace.md). Inoltre, puoi aggiungere facilmente plug-in per social network come il pulsante _Mi piace_ ai blocchi CMS che possono essere incorporati nelle pagine di tutto lo store.

I siti di social networking dispongono di numerosi plug-in che possono essere facilmente aggiunti al tuo store. Inoltre, sulla Commerce Marketplace sono presenti molte estensioni che possono essere utilizzate per integrare il negozio con i social media. Nell&#39;esempio seguente viene illustrato come aggiungere un pulsante _Like_ di Facebook all&#39;archivio.

>[!NOTE]
>
>Adobe Commerce ha rimosso l&#39;integrazione nativa di _Magento Social_ Facebook e non supporta più l&#39;estensione. Vai alla [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} per individuare estensioni alternative per l’integrazione con Facebook.

### Passaggio 1: Ottieni il codice del pulsante

1. Nel sito Web Meta developers, vai alla pagina [installazione del pulsante](https://developers.facebook.com/docs/plugins/like-button).

1. Per **[!UICONTROL URL to Like]**, immetti l&#39;URL della pagina nello store che desideri che le persone _Mi piace_.

   Ad esempio, puoi immettere l’URL della home page del tuo negozio.

1. Scegliere **[!UICONTROL Layout]** per il pulsante.

1. Immetti **[!UICONTROL Width]** in pixel disponibile sul sito per il pulsante ed eventuali messaggi di testo associati.

1. Imposta **[!UICONTROL Action Type]** su uno dei seguenti:

   - `Like`
   - `Recommend`

1. Fare clic su **[!UICONTROL Get Code]** per copiare il codice generato negli Appunti.

### Passaggio 2: Creare un blocco di contenuto

1. Torna all’amministratore del tuo negozio.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add New Block]**.

1. Immettere un **[!UICONTROL Block Title]** descrittivo come riferimento interno.

   Esempio: `Facebook Like Button`.

1. Assegna un **[!UICONTROL Identifier]** univoco al blocco, utilizzando tutti i caratteri minuscoli e i caratteri di sottolineatura invece degli spazi.

   Esempio: `facebook_like_button`.

1. Se l&#39;istanza di Commerce dispone di più visualizzazioni dello store, scegliere ogni **[!UICONTROL Store View]** in cui il blocco sarà disponibile.

1. Aggiungi lo snippet di codice al contenuto del blocco, a seconda dello strumento di contenuto:

   - Quando utilizzi [!DNL Page Builder], aggiungi un blocco [HTML Code](../page-builder/html-code.md) nell&#39;area di visualizzazione e incolla lo snippet di codice copiato dal sito Facebook. In caso contrario, incollare il frammento di codice nella casella **[!UICONTROL Content]**.

   - Con l&#39;editor, incollare il frammento di codice copiato dal sito Facebook nella casella **[!UICONTROL Content]**.

1. Se il blocco non è pronto per essere attivato, impostare **[!UICONTROL Enable Block]** su `No`.

1. Al termine, fare clic su **[!UICONTROL Save Block]**.

### Passaggio 3: Posizionare il blocco

1. Aggiungi il blocco, a seconda dello strumento di contenuto:

   - Quando utilizzi [!UICONTROL Page Builder], segui le istruzioni per [aggiungere il blocco](../page-builder/block.md) all&#39;area di visualizzazione.

   - Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add Widget]** ed eseguire le operazioni seguenti:

   - ![Adobe Commerce B2B](../assets/b2b.svg) (disponibile solo con Adobe Commerce B2B) Nella sezione _Settings_, impostare **[!UICONTROL Type]** su `CMS Static Block` e fare clic su **[!UICONTROL Continue]**.

   - Verificare che **[!UICONTROL Design Theme]** sia impostato sul tema corrente.

   - Fare clic su **[!UICONTROL Continue]**.

1. Nella sezione **[!UICONTROL Storefront Properties]** eseguire le operazioni seguenti:

   - Per **[!UICONTROL Widget Title]**, immettere un titolo per riferimento interno.

   - Impostare **[!UICONTROL Assign to Store Views]** su `All Store Views` o sulla visualizzazione in cui si desidera rendere disponibile l&#39;app. Per selezionare più viste, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   - Immettere un numero nel campo **[!UICONTROL Sort Order]** per determinare l&#39;ordine del blocco, se assegnato per essere visualizzato nella stessa posizione sulla pagina degli altri elementi di contenuto. La posizione superiore è zero.

1. Nella sezione _[!UICONTROL Layout Updates]_, fare clic su **[!UICONTROL Add Layout Update]**e impostare **[!UICONTROL Display On]**sulla categoria, il prodotto o la pagina in cui si desidera visualizzare il blocco.

   Se ad esempio si sceglie `All Pages` e si posiziona il blocco nell&#39;intestazione o nel piè di pagina, il blocco verrà visualizzato nello stesso punto in ogni pagina dell&#39;archivio.

   Per posizionare il blocco su una pagina specifica, eseguire le operazioni seguenti:

   - Impostare **[!UICONTROL Display On]** su `Specified Page` e selezionare **[!UICONTROL Page]** dove si desidera visualizzare il blocco.

   - Scegli **[!UICONTROL Block Reference]** per identificare il punto nella pagina in cui deve essere inserito il blocco.

   - Accettare l&#39;impostazione predefinita per **[!UICONTROL Template]**, impostata su `CMS Static Block Default Template`.

   - Fare clic su **[!UICONTROL Save and Continue Edit]**.

1. Nel pannello a sinistra, scegli **[!UICONTROL Widget Options]**.

1. Fare clic su **[!UICONTROL Select Block…]** e scegliere il blocco che si desidera inserire.

1. Al termine, fare clic su **[!UICONTROL Save]**.

1. Quando richiesto, segui le istruzioni nella parte superiore dell’area di lavoro per aggiornare l’indice e la cache delle pagine.

   Il widget viene ora visualizzato nell&#39;elenco _[!UICONTROL Widgets]_.

### Passaggio 4: Verifica la posizione nell’archivio

Torna alla vetrina per verificare che il blocco si trovi nella posizione corretta. Per spostare il blocco, potete riaprire il widget e provare con un riferimento a una pagina o a un blocco diverso.

## Feed RSS

RSS (Really Simple Syndication) è un formato di dati basato su XML utilizzato per distribuire informazioni online. I clienti possono abbonarsi ai feed RSS per conoscere i nuovi prodotti e le nuove promozioni. I feed RSS possono essere utilizzati anche per pubblicare le informazioni sui prodotti sui siti di aggregazione degli acquisti e possono essere inclusi nelle newsletter.

Quando i feed RSS sono attivati, tutte le aggiunte a prodotti, speciali, categorie e coupon vengono inviate automaticamente agli abbonati di ciascun feed. Un collegamento a tutti i feed RSS pubblicati si trova nel piè di pagina del negozio.

![Icona feed RSS](./assets/icon-rss.png){width="100"}<br/>

Il software necessario per leggere un feed RSS è denominato lettore di feed e consente alle persone di iscriversi a titoli, blog, podcast e molto altro. Google Reader è uno dei numerosi lettori di feed disponibili online gratuitamente.

![Esempio di vetrina - feed RSS](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### Vantaggi della configurazione di un feed RSS

- Scarica l’ultimo aggiornamento dal tuo store o blog
- Annunci leggeri
- Azioni ordinarie
- Aumenta SEO
- Aumenta le vendite

### Tipi di feed RSS

| Feed RSS | Descrizione |
|--- |--- |
| [!UICONTROL Wish List] | Quando è attivata, nella parte superiore delle pagine della lista dei desideri del cliente viene visualizzato un collegamento al feed RSS. Inoltre, la pagina di condivisione della lista dei desideri include una casella di controllo che consente di includere un collegamento al feed dalla lista dei desideri condivisi. |
| [!UICONTROL New Products] | Pubblica la notifica dei nuovi prodotti aggiunti al catalogo. |
| [!UICONTROL Special Products] | Pubblica le notifiche di qualsiasi prodotto con prezzi speciali. |
| [!UICONTROL Coupons / Discounts] | Pubblica la notifica di eventuali coupon o sconti speciali disponibili nel negozio. |
| [!UICONTROL Top Level Category] | Pubblica la notifica di qualsiasi modifica alla struttura di categorie di livello superiore del catalogo, che si riflette nel menu principale. |
| [!UICONTROL Customer Order Status] | Consente ai clienti di tenere traccia dello stato dell&#39;ordine tramite il feed RSS. Quando questa opzione è attivata, nell&#39;ordine viene visualizzato un collegamento del feed RSS. |

{style="table-layout:auto"}

### Configurare i feed RSS per il punto vendita

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nell&#39;angolo superiore destro, impostare **[!UICONTROL Store View]** sulle visualizzazioni in cui i feed saranno disponibili.

   Se viene richiesto di confermare, fare clic su **[!UICONTROL OK]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL RSS Feeds]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) della sezione **[!UICONTROL Rss Config]** e impostare **[!UICONTROL Enable RSS]** su `Enable`.

   ![Configurazione catalogo - Feed RSS](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Se necessario, deselezionare la casella di controllo **[!UICONTROL Use Default]** per modificare il valore predefinito.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) della sezione **[!UICONTROL Wish List]** e impostare **[!UICONTROL Enable RSS]** su `Enable`.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Catalog]** e impostare altri feed su `Enable` in base alle esigenze.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Catalogo - Impostazioni feed RSS](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) della sezione **[!UICONTROL Order]** e impostare **[!UICONTROL Customer Order Status Notification]** su `Enable`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Vedi il risultato nella vetrina con `/rss` alla fine dell&#39;URL della pagina.

