---
title: Creare esperienze coinvolgenti e personalizzate su larga scala
description: Scopri le funzioni di Adobe [!DNL Commerce] ti consente di creare un’esperienza personalizzata per i tuoi acquirenti.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 728a1fdb413009a00377cd8205dde93cd4feadc8
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# Creare esperienze coinvolgenti e personalizzate su larga scala

Adobe [!DNL Commerce] offre un potente toolkit per personalizzare ogni punto di contatto del cliente, aumentando il coinvolgimento degli acquirenti, la conversione e i ricavi.

In questo articolo imparerai:

- Cos’è la personalizzazione?
- Di quali dati ho bisogno per ottenere la personalizzazione?
- Come funziona Adobe [!DNL Commerce] sbloccare la personalizzazione?
- Casi d’uso di personalizzazione disponibili

## Cos’è la personalizzazione?

Personalizzazione significa personalizzare gli aspetti dell’esperienza di acquisto di ogni cliente in base alle sue esigenze, al suo contesto e alle sue preferenze. La personalizzazione non si limita ai contenuti sul sito o alla raccomandazione di prodotti best-fit, ma include tutti i punti di contatto nel percorso di clienti, tra cui:

- **Campagne e comunicazioni** - Distribuzione di messaggi pertinenti e coerenti tramite campagne e comunicazioni
- **Individuazione prodotto** - Mostrare i prodotti giusti ai clienti giusti nei momenti giusti
- **Promozioni e offerte** - Targeting di promozioni e offerte per spingere ogni cliente a convertire
- **Esperienze di contenuto** - Personalizzazione dei contenuti del sito per garantire un&#39;esperienza di iperrilevanza ai singoli clienti e percorsi

![Tipi di personalizzazione](assets/types-personalization.png){width="700" zoomable="yes"}

Anche se questo tipo di esperienze personalizzate può sembrare realizzabile per un piccolo sottoinsieme di clienti, personalizzando su larga scala per migliaia o milioni di clienti in ogni punto di contatto e canale, il tutto in tempo reale può sembrare impossibile. Nelle sezioni seguenti, scopri come Adobe [!DNL Commerce] e Adobe Experience Cloud può essere d&#39;aiuto.

## Di quali dati ho bisogno per ottenere la personalizzazione?

Una personalizzazione efficace richiede contesto o segnali che forniscano informazioni sui clienti e che possano quindi essere utilizzati per modificare la loro esperienza. La tabella seguente fornisce i vari tipi di dati e il ruolo Adobe [!DNL Commerce] svolge un ruolo di supporto nella raccolta e attivazione di tali dati.

| Tipi di dati | Dati storefront (eventi comportamentali) | Dati di back office (eventi lato server) | Profilo cliente e dati dei segmenti |
|---|---|---|---|
| **Definizione** | Clic o azioni eseguite dai clienti sul sito. | Informazioni sul ciclo di vita e dettagli di ciascun ordine (passato e corrente). | Chi sono i tuoi acquirenti e a quali segmenti si qualificano. |
| **Eventi acquisiti da Adobe Commerce** | [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[disconnetti](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRichiesteList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRichiesteList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRichiesteList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist) | **Stato ordine**:<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Cronologia ordini**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, nome, quantità prezzo, sconto<br>- Categoria di prodotto<br>- Importo, tipo, divisa del pagamento<br>- Metodo di spedizione e importo<br>- ID rimborso, importo, valuta<br>- Motivo restituzione, condizione, risoluzione<br>- Indirizzo<br>- E-mail | [**Record profilo**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord): (Nome, Genere, Indirizzo, Stato fedeltà, Numero di telefono, Indirizzo e-mail)<br>**Stato dell’account**:<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Con tutto questo ricco, primo partito [!DNL Commerce] dati, sei pronto per eseguire il targeting e personalizzare l’esperienza di ogni acquirente. Nella sezione successiva verrà illustrato come [!DNL Commerce] e Adobe Experience Cloud ti aiutano a creare esperienze personalizzate e i casi d’uso che puoi attivare.

## Come funziona Adobe [!DNL Commerce] abilitare la personalizzazione?

Adobe [!DNL Commerce] La condivisione dei dati consente di raccogliere e condividere i tipi di dati della tabella precedente con altri prodotti Adobe Experience Cloud per abilitare profili cliente e tipi di pubblico unificati, campagne personalizzate, analisi e informazioni approfondite.

![Flusso dei dati verso il server Edge di Experienci Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] La condivisione dei dati include due componenti chiave:

1. [Connessione dati](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview): condividi i dati della vetrina, del back office e del profilo cliente da Adobe [!DNL Commerce] alla rete edge di Adobe Experience Platform per l&#39;utilizzo in applicazioni Adobe Experience Cloud, tra cui:

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): unisci i dati del cliente da più origini (ERP, CRM, POS) in profili unificati e crea segmenti basati su regole o su intelligenza artificiale.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started): avvia percorsi omni-channel personalizzati, tra cui campagne e-mail, SMS, notifiche push e altro ancora.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) e [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview): ottenere informazioni sul cliente e sull’azienda.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro): testa e ottimizza contenuti, prodotti consigliati, offerte, navigazione e altro ancora.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation): Utilizzare [!DNL Real-Time CDP] tipi di pubblico per personalizzare sul tuo Adobe blocchi di contenuti dinamici, promozioni e regole di prodotto correlate [!DNL Commerce] sito.

### Esperienze personalizzate in vetrina su qualsiasi canale, su larga scala

Adobe [!DNL Commerce] può trarre vantaggio da una vetrina ad alte prestazioni, denominata [Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/), per fornire esperienze personalizzate su tutti i canali, con le funzionalità di intelligenza artificiale al centro e la velocità come base.

Con i Edge Delivery Services è possibile:

- **Contenuti personalizzati per l’artigianato**: utilizza l’authoring basato su documenti e la sperimentazione nativa con varianti di testo e immagine di IA generativa per personalizzare l’esperienza su larga scala. Utilizza la creazione di contenuti di Assets e di IA generativa per produrre immagini di prodotti e marketing su larga scala.

- **Genera varianti**: consente agli autori di contenuti di utilizzare l’intelligenza artificiale generativa per creare grandi volumi di IA personalizzata [contenuto di testo e varianti di immagine](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/generative-ai/generate-variations) con Adobe Firefly.

- **Distribuisci tramite Edge Delivery Services Storefront**: contenuto su Edge e funzionalità di Commerce basate su componenti di rilascio, per creare esperienze personalizzate acquistabili per il pubblico.

- **COMMERCE e ADOBE EXPERIENCE MANAGER ASSETS**: creazione e varianti di risorse di prodotti di intelligenza artificiale generativa su larga scala. Creare, distribuire e monitorare la distribuzione dei contenuti su qualsiasi canale.

![Pagina Drop-ins: Dettagli prodotto](assets/drop-in.png){width="700" zoomable="yes"}

### Personalizzazione preconfigurata: guida introduttiva all’Adobe nativo [!DNL Commerce] funzioni

Adobe [!DNL Commerce] offre una potente personalizzazione con le sue funzionalità native pronte all’uso. La tabella seguente descrive [!DNL Commerce] funzionalità che puoi attivare immediatamente per iniziare a utilizzare il percorso di personalizzazione.

| Categoria | Funzioni |
|---|---|
| Individuazione personalizzata del prodotto | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview): personalizza e ottimizza i risultati della ricerca in base alle azioni comportamentali in loco di un acquirente e alle affinità con la ricerca basata sull’intelligenza artificiale.<br>[Merchandising intelligente per categorie](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch): classificazione dei prodotti basata sull’intelligenza artificiale sulle pagine di categorie in base alle azioni comportamentali e alle affinità in loco di un acquirente.<br>[Recommendations del prodotto](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview): consigli di prodotti basati sull’intelligenza artificiale basati sul comportamento, le tendenze e le affinità degli acquirenti.<br>[Regole prodotto correlate](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): definisci regole personalizzate per visualizzare i prodotti dal catalogo e promuovere vendite incrociate e upselling. |
| Contenuto del sito personalizzato | [Blocchi di contenuto dinamici](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): visualizza blocchi di contenuto personalizzati, ad esempio banner, in base ai segmenti dei clienti in Adobe Commerce. |
| Offerte e promozioni personalizzate | [Regole prezzo carrello](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): applica sconti agli articoli nel carrello in base a una serie di condizioni, inclusi i segmenti cliente in Adobe [!DNL Commerce]. |
| Approfondimenti e misurazione | [Adobe [!DNL Commerce] Intelligenza](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started): scopri come funzionano le strategie di personalizzazione e come migliorarle nel tempo. |

## Casi d’uso principali per la personalizzazione

Adobe [!DNL Commerce] I clienti di utilizzano funzionalità predefinite e condividono dati con Adobe Experience Cloud per una serie di casi d’uso. Le sezioni seguenti evidenziano i casi d’uso principali e descrivono come vengono implementati utilizzando Adobe [!DNL Commerce] Solo o [!DNL Commerce] più app di Experience Cloud.

### Campagne e comunicazioni personalizzate

| Caso d’uso | Soluzione |
|---|---|
| **Carrello abbandonato e navigazione** - Inviare un’e-mail o una notifica di ricoinvolgimento personalizzata quando un cliente abbandona il carrello o la sessione di navigazione dopo aver dimostrato un elevato coinvolgimento | **Adobe [!DNL Commerce] Solo**:<br>[Promemoria e-mail](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] con Adobe Journey Optimizer**:<br>[!DNL Commerce] I dati fungono da attivatore per un percorso di abbandono omni-channel. Personalizza il percorso in base agli attributi del cliente, a cosa hanno abbandonato, ad altri comportamenti di acquisto e agli acquisti precedenti.<br>Commerce con Adobe Journey Optimizer e Real-Time CDP: campagne di abbandono personalizzate basate su profili cliente unificati e tipi di pubblico gestiti a livello centrale, ad esempio la creazione di un pubblico con un tasso di abbandono elevato. |
| **Creazione centralizzata del pubblico** : crea tipi di pubblico basati su regole o su intelligenza artificiale in base al comportamento nel sito, agli acquisti precedenti, agli attributi del profilo, alle affinità tra categorie, allo stato di fedeltà, al valore del cliente e altro ancora | **Adobe [!DNL Commerce] Solo**:<br>Raccogliere informazioni sul profilo cliente quando [!DNL Commerce] i clienti creano account. Crea basato su regole [segmenti cliente](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) e gruppi di clienti per personalizzare contenuti e promozioni.<br>**Adobe [!DNL Commerce] con Adobe Real-Time CDP**:<br> [Profili unificati](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) da origini dati e canali diversi; tipi di pubblico basati su regole o basati su intelligenza artificiale. |
| **Offerta e-mail/SMS personalizzata in base al comportamento dell’acquirente** - Inviare offerte personalizzate ai clienti tramite e-mail mirate in base agli acquisti precedenti e al comportamento dell’acquirente, ad esempio inviare offerte per prodotti o categorie con cui i clienti hanno visualizzato o contattato. | **Adobe [!DNL Commerce] Solo**:<br>Esporta dati da utilizzare con soluzioni di automazione marketing.<br>**Adobe [!DNL Commerce] con Adobe Journey Optimizer e Real-Time CDP**:<br>[!DNL Commerce] I dati fungono da trigger per le offerte e-mail o SMS e forniscono segnali (comportamenti degli acquirenti) su cui personalizzare in base a. Real-Time CDP non è richiesto, ma in genere queste offerte e campagne vengono create intorno ai tipi di pubblico, che verrebbero creati e gestiti all’interno di Real-Time CDP. |
| **Prodotti/marchi compatibili cross-selling o upselling** - Se un cliente acquista un prodotto o un marchio compatibile o che indica un’elevata affinità verso un altro prodotto o un altro marchio, invia una campagna (e-mail/SMS) per promuovere la conversione cross-selling. | **Adobe [!DNL Commerce] Solo**:<br>Utilizza Adobe [!DNL Commerce] [Recommendations del prodotto](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) per consigliare prodotti specifici sul sito. Puoi anche utilizzare [Regole prodotto correlate](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) per suggerire altri prodotti.<br>**[!DNL Commerce] con [!DNL Target]**:<br>Adobe [!DNL Target] dispone anche di un motore integrato di consigli sui prodotti con funzionalità avanzate come l’affinità tra categorie. Può essere utilizzato per effettuare cross-selling o upselling.<br>**[!DNL Commerce] con Adobe Journey Optimizer**:<br>Utilizzare [!DNL Target] o [!DNL Commerce] per determinare i prodotti da consigliare, quindi consegnarli tramite Adobe Journey Optimizer. |

### Esperienze del sito personalizzate

| Caso d’uso | Soluzione |
|---|---|
| **Contenuto del sito personalizzato** : personalizza i banner del sito e altri contenuti della pagina in base alle azioni dell’acquirente, come la navigazione dei prodotti e le affinità tra categorie. Distribuisci contenuti ottimali in base ai risultati dei test A/B o agli obiettivi aziendali. | **Adobe [!DNL Commerce] Solo**:<br>Distribuisci per segmenti specifici [blocchi di contenuto dinamici](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] con Real-Time CDP **:<br>Utilizzare [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) distribuire blocchi di contenuti dinamici specifici per il pubblico che rispondano alle azioni in tempo reale e ai dati unificati del profilo cliente, gestendo al contempo profili e tipi di pubblico a livello centrale in Real-Time CDP;<br>**[!DNL Commerce] con[!DNL Target]**:<br>Personalizza ogni parte dell’esperienza del sito, inclusi contenuti, elementi di navigazione, layout di pagina completi e altro ancora utilizzando Adobe [!DNL Commerce] dati in Adobe [!DNL Target]. Test A/B dei contenuti, selezione e distribuzione automatica dei contenuti vincenti per ogni cliente.<br>**[!DNL Commerce] con AEM Assets **:<br>Archivia tutti i contenuti in Adobe Experience Manager Assets. Accedi in modo nativo a tale contenuto da Adobe Commerce. Utilizza l’intelligenza artificiale generativa per creare varianti di contenuto da personalizzare per diversi segmenti o tipi di pubblico. |
| **Offerta personalizzata nel sito in base al comportamento** - Personalizzare le promozioni in base alle azioni dei clienti, ad esempio la navigazione dei prodotti e le affinità tra categorie. Distribuisci la migliore offerta successiva in base ai risultati dei test A/B o agli obiettivi aziendali. | **Adobe [!DNL Commerce] Solo**:<br>Distribuire il catalogo specifico per il segmento e [regole prezzi carrello](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] con Real-Time CDP**:<br>Utilizzare [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) distribuire offerte specifiche per il pubblico, gestendo al tempo stesso in modo centralizzato profili/tipi di pubblico in Real-Time CDP.<br>**Commerce con[!DNL Target]**: utilizza l’offer decisioning per determinare quale offerta distribuire, test A/B o impostare obiettivi aziendali per guidare le offerte implementate in Adobe Commerce. |

### Analytics e approfondimenti

| Caso d’uso | Soluzione |
|---|---|
| **Comportamento del cliente per canale** : scopri le sfumature del modo in cui i clienti si impegnano in ogni canale (web, di persona, app, altro) per influire sulle strategie di marketing per ogni canale; scopri il funnel cliente e le sue debolezze. | **Adobe [!DNL Commerce] Solo**:<br>[Adobe [!DNL Commerce] Intelligenza](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) fornisce analisi avanzate sul digitale [!DNL Commerce] ma non su canali diversi o su parti più ampie del percorso di clienti.<br>**Adobe [!DNL Commerce] con Customer Journey Analytics**:<br>[!DNL Commerce] feed di dati dashboard di dati per informazioni complete su tutte le fasi dell’esperienza del cliente (nei diversi canali). Comprendi ogni punto di contatto e il funnel più ampio per identificare i punti deboli nel percorso di clienti in cui i clienti potrebbero cadere. |
| **Tendenze di acquisto** - Comprendi i comportamenti di acquisto in un arco di tempo specifico (ad esempio, analisi del carrello acquisti e dei prodotti) per identificare tendenze e stagionalità e ottimizzare il marketing in base a modelli di acquisto storici. | **Adobe [!DNL Commerce] Solo**:<br>[Adobe [!DNL Commerce] Intelligenza](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) fornisce analisi avanzate sul digitale [!DNL Commerce] ma non su canali diversi o su parti più ampie del percorso di clienti.<br>**Adobe [!DNL Commerce] con Customer Journey Analytics**:<br>[!DNL Commerce] feed di dati dashboard di dati per informazioni complete su tutte le fasi dell’esperienza del cliente (nei diversi canali). Comprendi ogni punto di contatto e il funnel più ampio per identificare i punti deboli nel percorso di clienti in cui i clienti potrebbero cadere. |

## Casi d’uso di esempio

- Scopri come utilizzare Adobe Journey Optimizer per [invia un’e-mail carrello abbandonata](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
- Scopri come [creare un pubblico in Real-Time CDP](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience) per informare una regola di prezzo del carrello in Adobe [!DNL Commerce].
