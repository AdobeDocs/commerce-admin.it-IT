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

Il tuo store può essere connesso ai social network installando un [Estensione Marketplace](../getting-started/commerce-marketplace.md). Inoltre, puoi aggiungere facilmente plug-in per social network come _Mi piace_ ai blocchi CMS che possono essere incorporati nelle pagine di tutto il negozio.

I siti di social networking dispongono di numerosi plug-in che possono essere facilmente aggiunti al tuo store. Inoltre, sulla Commerce Marketplace sono presenti molte estensioni che possono essere utilizzate per integrare il negozio con i social media. Nell&#39;esempio seguente viene illustrato come aggiungere un Facebook _Mi piace_ al negozio.

>[!NOTE]
>
>Adobe Commerce ha rimosso il file nativo _Social Magento_ Integrazione di facebook e non supporta più l’estensione. Vai a [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} per individuare estensioni alternative per l’integrazione con Facebook.

### Passaggio 1: Ottieni il codice del pulsante

1. Sul sito web Meta developers, vai al [impostazione pulsante](https://developers.facebook.com/docs/plugins/like-button) pagina.

1. Per **[!UICONTROL URL to Like]**, immetti l&#39;URL della pagina del Negozio che desideri che gli utenti _Mi piace_.

   Ad esempio, puoi immettere l’URL della home page del tuo negozio.

1. Scegli la **[!UICONTROL Layout]** per il pulsante.

1. Inserisci il **[!UICONTROL Width]** in pixel disponibile sul sito per il pulsante ed eventuali messaggi di testo associati.

1. Imposta **[!UICONTROL Action Type]** a uno dei seguenti elementi:

   - `Like`
   - `Recommend`

1. Clic **[!UICONTROL Get Code]** per copiare il codice generato negli Appunti.

### Passaggio 2: Creare un blocco di contenuto

1. Torna all’amministratore del tuo negozio.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add New Block]**.

1. Inserisci un valore descrittivo **[!UICONTROL Block Title]** per riferimento interno.

   Ad esempio: `Facebook Like Button`.

1. Assegna un univoco **[!UICONTROL Identifier]** al blocco, utilizzando tutti i caratteri minuscoli e i caratteri di sottolineatura anziché gli spazi.

   Ad esempio: `facebook_like_button`.

1. Se la tua istanza di Commerce dispone di più visualizzazioni dello store, scegli ciascuna **[!UICONTROL Store View]** dove il blocco deve essere disponibile.

1. Aggiungi lo snippet di codice al contenuto del blocco, a seconda dello strumento di contenuto:

   - Quando si utilizza [!DNL Page Builder], aggiungi un [Codice HTML](../page-builder/html-code.md) blocca nell’area di visualizzazione e incolla lo snippet di codice copiato dal sito Facebook. In caso contrario, incolla lo snippet di codice nel **[!UICONTROL Content]** casella.

   - Con l’editor, incolla lo snippet di codice copiato dal sito Facebook in **[!UICONTROL Content]** casella.

1. Se il blocco non è pronto per essere pubblicato, imposta **[!UICONTROL Enable Block]** a `No`.

1. Al termine, fai clic su **[!UICONTROL Save Block]**.

### Passaggio 3: Posizionare il blocco

1. Aggiungi il blocco, a seconda dello strumento di contenuto:

   - Quando si utilizza [!UICONTROL Page Builder], seguire le istruzioni per [aggiungi il blocco](../page-builder/block.md) sul palco.

   - Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Widget]** ed effettuare le seguenti operazioni:

   - ![Adobe Commerce B2B](../assets/b2b.svg) (Disponibile solo con Adobe Commerce B2B) Nella _Impostazioni_ sezione, set **[!UICONTROL Type]** a `CMS Static Block` e fai clic su **[!UICONTROL Continue]**.

   - Verifica che **[!UICONTROL Design Theme]** è impostato sul tema corrente.

   - Clic **[!UICONTROL Continue]**.

1. In **[!UICONTROL Storefront Properties]** eseguire le operazioni seguenti:

   - Per **[!UICONTROL Widget Title]**, immetti un titolo per riferimento interno.

   - Imposta **[!UICONTROL Assign to Store Views]** a `All Store Views`, o alla visualizzazione in cui desideri che l&#39;app sia disponibile. Per selezionare più viste, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   - Immettere un numero in **[!UICONTROL Sort Order]** per determinare l’ordine del blocco, se assegnato per essere visualizzato nella stessa posizione sulla pagina come altri elementi di contenuto. La posizione superiore è zero.

1. In _[!UICONTROL Layout Updates]_, fare clic su **[!UICONTROL Add Layout Update]**e imposta **[!UICONTROL Display On]**alla categoria, al prodotto o alla pagina in cui si desidera visualizzare il blocco.

   Ad esempio, se scegli `All Pages` e posiziona il blocco nell’intestazione o nel piè di pagina, il blocco viene visualizzato nello stesso punto su ogni pagina del negozio.

   Per posizionare il blocco su una pagina specifica, eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Display On]** a `Specified Page` e seleziona la **[!UICONTROL Page]** dove si desidera visualizzare il blocco.

   - Scegli la **[!UICONTROL Block Reference]** per identificare il punto della pagina in cui deve essere posizionato il blocco.

   - Accetta l&#39;impostazione predefinita per **[!UICONTROL Template]**, impostato su `CMS Static Block Default Template`.

   - Clic **[!UICONTROL Save and Continue Edit]**.

1. Nel pannello a sinistra, scegli **[!UICONTROL Widget Options]**.

1. Clic **[!UICONTROL Select Block…]** e scegliere il blocco che si desidera posizionare.

1. Al termine, fai clic su **[!UICONTROL Save]**.

1. Quando richiesto, segui le istruzioni nella parte superiore dell’area di lavoro per aggiornare l’indice e la cache delle pagine.

   Il widget ora viene visualizzato nel _[!UICONTROL Widgets]_elenco.

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

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nell&#39;angolo in alto a destra, imposta **[!UICONTROL Store View]** alle visualizzazioni in cui i feed devono essere disponibili.

   Se viene richiesto di confermare, fare clic su **[!UICONTROL OK]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL RSS Feeds]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Rss Config]** sezione e set **[!UICONTROL Enable RSS]** a `Enable`.

   ![Configurazione catalogo - Feed RSS](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Se necessario, cancellare il **[!UICONTROL Use Default]** per modificare il valore predefinito.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Wish List]** sezione e set **[!UICONTROL Enable RSS]** a `Enable`.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Catalog]** e impostare altri feed su `Enable` secondo necessità.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Catalogo - Impostazioni feed RSS](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Order]** sezione e set **[!UICONTROL Customer Order Status Notification]** a `Enable`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Vedi il risultato nella vetrina con `/rss` alla fine dell’URL della pagina.

