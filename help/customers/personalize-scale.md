---
title: Personalizzazione su larga scala
description: Scopri quali funzioni di Adobe Commerce ti consentono di creare un’esperienza personalizzata per i tuoi acquirenti.
feature: Customers, Storefront, Personalization
source-git-commit: a4eeda918adcb74ad5e7008b80eff703fa15e878
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# Personalizzazione su larga scala

&#x200B;La personalizzazione su larga scala consente alle aziende di personalizzare l’esperienza di acquisto per ogni punto di contatto del cliente in base al contesto immediato e al comportamento osservato in precedenza. L’obiettivo è quello di presentare ogni volta l’esperienza più rilevante e personalizzata possibile.

Per comprendere i vantaggi di offrire un’esperienza di acquisto personalizzata, scarica il [_Guida introduttiva alla personalizzazione su scala_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) rapporto.

Per creare un’esperienza di acquisto personalizzata è necessario conoscere il tipo di dati necessari per comprendere il contesto del cliente. Da lì, scopri le funzioni di Adobe Commerce che utilizzano quei dati per sbloccare le informazioni sui clienti necessarie per creare l’esperienza di acquisto personalizzata.

L’immagine seguente illustra i concetti coinvolti nella personalizzazione dell’esperienza di acquisto:

![Creazione di una pipeline di personalizzazione](assets/personalization-journey.png){width="700" zoomable="yes"}

In questo articolo vengono descritti in modo più dettagliato ciascuno dei concetti descritti in precedenza.

## Come personalizzare l’esperienza di acquisto

La personalizzazione di successo inizia con il contesto del cliente. In questa sezione scopri i tipi di dati disponibili per aiutarti a creare il contesto del cliente.

### Dati vetrina

I dati della vetrina, o dati comportamentali o del browser, possono rivelare informazioni su come gli acquirenti interagiscono con il sito. Ad esempio:

- Quali sono i prodotti e le categorie a cui i miei acquirenti sono più interessati?
- In che tipo di ricerca sono più coinvolti i miei acquirenti?
- I miei acquirenti stanno aggiungendo prodotti al carrello e poi abbandonandolo?
- I miei acquirenti utilizzano un browser desktop o mobile?

I seguenti eventi storefront acquisiscono dati che possono aiutarti a rispondere a queste domande:

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [disconnetti](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRichiesteList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRichiesteList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRichiesteList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### Dati di back office

I dati di back office, detti anche dati lato server, possono rivelare informazioni sul ciclo di vita dell’ordine. Ad esempio:

- Esistono prodotti acquistati più frequentemente in base alla stagione?
- I miei acquirenti stanno restituendo prodotti?
- Come posso calcolare il valore del cliente per tutto il ciclo di vita?

I seguenti eventi di back office consentono di acquisire dati utili per rispondere alle seguenti domande:

- [orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### Dati di profilo cliente e segmento

I dati del profilo del cliente possono rivelare informazioni approfondite su chi sono i tuoi acquirenti e per quali segmenti si qualificano. Ad esempio:

- Nome
- Genere
- Indirizzo
- Stato fedeltà
- Numero di telefono
- Indirizzo e-mail
- Stato fedeltà
- Numero di telefono
- Indirizzo e-mail
- Idoneità agli aggiornamenti
- Acquirenti cross-channel
- Prospettive di nuovi prodotti
- Membri fedeltà oro, argento o bronzo

I seguenti eventi di profilo acquisiscono dati che possono aiutarti a rispondere a queste domande:

- [Record profilo](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

I dati di vetrina, back office e profilo costituiscono la base del contesto del cliente e dell’ordine di Commerce, che consente di conoscere i prodotti che i clienti visualizzano e acquistano. Puoi quindi indirizzare i loro interessi e personalizzare la loro esperienza. Nella sezione successiva, scopri i tipi di esperienze personalizzate con cui puoi coinvolgere i tuoi acquirenti.

## Tipi di esperienze personalizzate

I dati contestuali relativi a clienti e ordini in Commerce alimentano i seguenti tipi di esperienze personalizzate:

| Esperienza | Descrizione |
|---|---|
| **Individuazione prodotto** | Contiene i servizi di merchandising che sono [distribuito come SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). Si tratta di funzioni che consentono di utilizzare dati comportamentali, attributi di prodotto e livelli di inventario per personalizzare automaticamente l’individuazione del prodotto in base a risultati di ricerca, consigli di prodotto e pagine esplorative. Queste funzioni utilizzano tutte [IA per Adobe Sensei](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **Contenuto del sito** | Si riferisce alla possibilità di distribuire blocchi di contenuto dinamici personalizzati in base al cliente corrente che esplora il sito. |
| **Offerte e campagne** | Consente di distribuire contenuti promozionali personalizzati in base ai dati dei segmenti. |
| **Misurazione** | Utilizza l&#39;intelligenza dei dati per comprendere meglio la tua attività, inclusi i ricavi, le prestazioni di canale e del materiale promozionale, le promozioni e così via. |

Nelle due sezioni successive scopri come utilizzare questi dati per creare esperienze personalizzate in [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) e in [funzioni native di Commerce](#using-commerce-data-in-native-commerce-features).

## Utilizzo dei dati di Commerce in Adobe Experience Platform

Per creare un’esperienza personalizzata per gli acquirenti su tutti i canali, invia i dati di Commerce alla rete Edge di Experienci Platform utilizzando [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) estensione.

![Flusso dei dati verso il server Edge di Experienci Platform](assets/commerce-edge.png){width="700" zoomable="yes"}

Nell’immagine precedente, i dati della vetrina, del back office e del profilo cliente vengono inviati al server Edge di Experienci Platform utilizzando un SDK, un’API e un connettore di origine. Non è necessario comprendere appieno il funzionamento di tali parti, in quanto l’estensione gestisce automaticamente la complessità della condivisione dei dati. Quando i dati dell’evento si trovano al limite, puoi richiamarli in altre applicazioni Experienci Platform.

La tabella seguente evidenzia alcune delle applicazioni di Experience Platform disponibili e il modo in cui tali applicazioni utilizzano i dati di Commerce.

| Esperienza | Applicazione | Utilizzo dei dati Commerce |
|---|---|---|
| **Contenuto del sito** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | I dati di Adobe Commerce alimentano i profili cliente unificati, con Real-Time CDP che unisce i dati provenienti da più origini (ERP, CRM, CMS, POS) in singoli profili. Real-Time CDP può anche creare segmenti basati su regole e su intelligenza artificiale da utilizzare poi nel set di soluzioni di marketing. Puoi inoltre utilizzare i tipi di pubblico di Real-Time CDP per personalizzare blocchi di contenuto, promozioni e regole di prodotto correlate. Consulta [[!DNL Audience Activation]](../customers/audience-activation.md) per ulteriori informazioni.&#x200B; |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | I dati di Adobe Commerce possono essere attivati in Adobe [!DNL Target] per testare, ottimizzare e creare pagine di destinazione dinamiche. Puoi personalizzare l’ordine in cui il contenuto viene visualizzato in una pagina, ad esempio descrizioni, specifiche, revisioni e prodotti consigliati in base ai dati di Commerce inviati. |
| **Offerte e campagne** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | I dati comportamentali e di back office di Adobe Commerce possono fungere da trigger per percorsi omni-channel personalizzati, tra cui campagne e-mail, SMS, notifiche push e altro ancora&#x200B; |
| **Misurazione** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) e [Cliente [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | Commerce invia dati sia di vetrina che di back-office al cliente [!DNL Journey Analytics] (e solo i dati della vetrina per Adobe [!DNL Analytics]) per consentire un’analisi più ricca oltre le metriche di base in Adobe Commerce Intelligence, come ricavi, merci e promozioni&#x200B;. |

Per ulteriori informazioni su come inviare i dati di Commerce all’Experience Platform, consulta [Connessione dati](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## Utilizzo dei dati di Commerce nelle funzioni native di Commerce

Nella sezione seguente, scopri come utilizzare le funzioni native di Commerce, come Product Recommendations e Live Search per creare un’esperienza di acquisto personalizzata. Scoprirai anche una funzione denominata [!DNL Audience Activation], che utilizza i dati di un prodotto disponibile nell’Experience Platform denominato Real-Time CDP, come indicato [in precedenza](#using-commerce-data-in-adobe-experience-platform). Anche se Real-Time CDP non è nativo di Commerce, le sue informazioni possono essere acquisite in Commerce tramite [[!DNL Audience Activation]](../customers/audience-activation.md) estensione.

La tabella seguente evidenzia le funzioni di Commerce disponibili per trasformare i dati contestuali di ordini e clienti Commerce in informazioni fruibili.

| Esperienza | Funzionalità | Descrizione |
|---|---|---|
| **Individuazione prodotto** | [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | Utilizza algoritmi di classificazione basati su IA per personalizzare e ottimizzare i risultati della ricerca in base alle azioni comportamentali di un acquirente sul sito, aumentando la rilevanza della ricerca e la conversione. |
|  | [Recommendations del prodotto](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | Visualizza i consigli sui prodotti basati sull’intelligenza artificiale in base al comportamento degli acquirenti, alle tendenze, alla somiglianza dei prodotti e altro ancora. In combinazione con il tuo catalogo Adobe Commerce, i consigli di prodotto forniscono un’esperienza altamente coinvolgente, rilevante e personalizzata. |
|  | [Merchandising categorie](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | Accessibile dall’amministratore di Live Search, il merchandising per categorie utilizza l’intelligenza artificiale per classificare automaticamente la sequenza di prodotti su ogni pagina delle categorie, in modo da aumentare la rilevanza e la conversione per ogni acquirente. Puoi creare e gestire regole basate sull’intelligenza artificiale per eseguire automaticamente una classificazione della sequenza di prodotti nelle pagine delle categorie in base alle azioni e alle affinità dell’acquirente. |
| **Contenuto del sito** | [Blocchi dinamici basati sulle funzioni native di Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Ti consente di fornire contenuti del sito personalizzati in base alla logica configurata nelle regole di prezzo e nei segmenti di clienti. |
|  | [Blocchi dinamici informati dal pubblico di Real-Time CDP](../customers/audience-activation.md) | Consente ai commercianti di fornire contenuti del sito personalizzati in base ai tipi di pubblico configurati in Real-Time CDP. |
| **Offerte e campagne** | [Regole prezzi carrello](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | Consente di applicare sconti agli articoli nel carrello in base a una serie di condizioni. |
|  | [Blocchi dinamici basati sulle funzioni native di Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Consente di visualizzare promozioni di banner personalizzate in base ai segmenti di clienti configurati in modo nativo in Commerce. |
|  | [Blocchi dinamici informati dal pubblico di Real-Time CDP](../customers/audience-activation.md) | Consente di visualizzare promozioni personalizzate in base al pubblico configurato in Real-Time CDP. |
| **Misurazione** | [Adobe Commerce Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | (precedentemente nota come Magenti Business Intelligence) è una piattaforma cloud che fornisce informazioni sulle best practice per aiutarti a prendere decisioni basate sui dati e ad intraprendere azioni chiare e informate. Adobe Commerce Intelligence è in grado di analizzare i dati per rispondere a domande sulla crescita degli ordini, sul comportamento dei clienti e sull&#39;efficacia delle strategie promozionali. |
