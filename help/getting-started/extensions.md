---
title: Estensioni da Adobe
description: Rivedi le informazioni sulle estensioni per Adobe Commerce e Magento Open Source rilasciate da Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/-QGqm0VMRlCNuKqHGdGVKjs8ZgNcjYZjFaeIFsOLWCA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: da3860b0-d637-47df-bef0-273751180266
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f5c2a4bb-71ca-4d7e-8efd-442250e6ba48
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1434
ht-degree: 0%

---

# Estensioni da Adobe

Questo argomento fornisce informazioni sulle estensioni PHP per Adobe Commerce e Magento Open Source rilasciate da Adobe.

Le estensioni aggiungono funzioni, funzionalità, servizi e integrazioni all’amministratore e alla vetrina. Alcune di queste estensioni sono sviluppate tramite contributi della community di Magento Open Source. Alcune estensioni sono installate per impostazione predefinita, altre richiedono un’installazione separata.

+++Ulteriori informazioni sull’estensione di Adobe Commerce

Adobe offre due approcci principali per estendere o personalizzare i progetti Adobe Commerce:

- Estensibilità in-process: utilizza codice personalizzato ed estensioni eseguite all’interno del processo dell’applicazione Adobe Commerce, come le estensioni PHP. Questo approccio tradizionale consente una profonda integrazione ma richiede un&#39;attenta gestione durante gli aggiornamenti.

- Estensibilità out-of-process: utilizza codice personalizzato e applicazioni che operano in modo indipendente dal software di base. Questo approccio moderno consente di ridurre il costo totale di proprietà:

   - Semplificazione degli aggiornamenti, dal momento che le estensioni sono scollegate dal core
   - Offrire agli sviluppatori maggiore controllo sui tempi e i metodi di implementazione
   - Abilitazione della scalabilità e della manutenzione indipendenti dei componenti dell’estensione

Adobe Commerce offre strategie e strumenti per supportare entrambi i tipi di estensibilità. Per ulteriori informazioni, consulta [Estensibilità Adobe Commerce](https://developer.adobe.com/commerce/extensibility/).

+++

## Estensioni Adobe installate per impostazione predefinita

Le seguenti estensioni Adobe sono incluse in Adobe Commerce e installate automaticamente con l’applicazione Adobe Commerce. Alcune estensioni richiedono un’ulteriore configurazione o abilitazione in Admin, come indicato nella descrizione dell’estensione.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) offre una gestione avanzata delle scorte e delle spedizioni in una o più sedi e canali di vendita con algoritmi di protezione dell&#39;estrazione simultanea e di corrispondenza delle spedizioni. Tenere traccia delle quantità di magazzino, fornire ai clienti quantità precise di scorte vendibili e spedirle in base a raccomandazioni o selezioni manuali per controllare l&#39;intero magazzino. Configurare le impostazioni di gestione a livello globale, per origine e per prodotto.

>[!NOTE]
>
>Questa estensione è stata sviluppata come parte del progetto [[!DNL Inventory Management]](https://github.com/magento/inventory) (precedentemente MSI) tramite il programma di progettazione della community.

[!DNL Inventory Management] viene installato con tutte le funzionalità abilitate per impostazione predefinita. Non sono necessari ulteriori passaggi per abilitare queste funzioni di inventario. Per informazioni dettagliate sulle funzionalità di [!DNL Inventory Management], vedere la [[!DNL Inventory Management] Guida utente](../inventory-management/guide-overview.md).

### Braintree

PayPal e Gene Commerce hanno sviluppato insieme l&#39;estensione ufficiale Braintree per i negozi Commerce 2.4.x. Grazie a una migliore esperienza di pagamento progettata per favorire la conversione, gli aggiornamenti includono opzioni PayLater che mostrano automaticamente messaggi e pulsanti PayLater rilevanti ai consumatori durante gli acquisti e durante il pagamento.

Questa estensione è installata per impostazione predefinita, ma richiede un account [Braintree](https://www.braintreepayments.com/) e la configurazione nell&#39;amministratore per essere abilitata per l&#39;archivio. Per determinare le tariffe da applicare quando si utilizza Braintree per elaborare le transazioni, controllare la [determinazione prezzi Braintree](https://www.braintreepayments.com/braintree-pricing).

Per informazioni sulla configurazione di Braintree in Amministrazione, consulta l&#39;argomento [Braintree](../stores-purchase/braintree.md) nella _Guida alle vendite e all&#39;esperienza di acquisto_.

### Google reCAPTCHA

Google reCAPTCHA offre un livello di sicurezza maggiore sia per la vetrina che per l’interfaccia utente amministratore rispetto a quello disponibile con il CAPTCHA standard e consente di:

- Verifica quando i clienti creano account, recuperano le password, accedono ai loro account o contattano la tua azienda.
- Migliora la sicurezza quando gli utenti amministratori accedono.

Riduce il potenziale errore dell’utente durante l’immissione di un codice Captcha e incoraggia la conversione del carrello senza aggiungere ostacoli durante il pagamento. [Abilitare e configurare reCAPTCHA](../systems/security-google-recaptcha.md) utilizzando controlli invisibili o interattivi per migliorare l&#39;accesso sicuro all&#39;amministratore e alla vetrina di [!DNL Commerce].

### Autenticazione a due fattori

L&#39;amministratore [!DNL Commerce] fornisce tutti gli accessi al tuo store, agli ordini e ai dati dei clienti. [L&#39;autenticazione a due fattori](../systems/security-two-factor-authentication.md) (2FA o TFA) migliora la sicurezza richiedendo un&#39;autenticazione aggiuntiva, oltre al nome di accesso e alla password standard, per accedere all&#39;amministratore [!DNL Commerce] da tutti i dispositivi. L&#39;estensione supporta più autenticatori tra cui Google Authenticator, Authy, [!DNL Duo] e le chiavi U2F. Questa autenticazione si applica solo agli utenti amministratori. Non è disponibile per gli account cliente di vetrina.

Queste funzioni sono attivate per impostazione predefinita. Ogni utente amministratore deve installare e configurare uno degli autenticatori supportati.

>[!NOTE]
>
>Gli archivi Adobe Commerce che hanno abilitato l’autenticazione Adobe Identity Management Services (IMS) per l’amministratore hanno Commerce 2FA nativo disabilitato. Gli utenti che hanno effettuato l’accesso all’Amministratore con le proprie credenziali Adobe non devono ripetere l’autenticazione per molte attività di Amministratore. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Consulta [Panoramica dell&#39;integrazione del servizio Adobe Identity Management (IMS)](./adobe-ims-integration-overview.md).

## Estensioni Adobe che richiedono l’installazione

Adobe offre estensioni aggiuntive che devono essere installate separatamente utilizzando Composer. Queste estensioni sono disponibili tramite diversi canali:

- Accesso all’archivio (repo.magento.com)

  Le seguenti estensioni richiedono il provisioning dell’account e le credenziali per essere installate. Per assistenza, contatta il rappresentante commerciale Adobe.

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [Integrazione di AEM Assets per Commerce](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  Le seguenti estensioni di Adobe sono accessibili al pubblico all&#39;indirizzo [marketplace.magento.com](https://marketplace.magento.com). Queste estensioni sono disponibili senza costi aggiuntivi.

   - [Live Search](#live-search)
   - [Consigli di prodotto](#product-recommendations)
   - [Servizio catalogo](#catalog-service)
   - [Servizi di pagamento](#payment-services)

### [!DNL Adobe Commerce B2B]

![Solo Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce, richiede una licenza separata.

[!DNL Adobe Commerce B2B] è un&#39;estensione integrata che trasforma gli store standard di Commerce in piattaforme complete business-to-business. Consente alle aziende di gestire strutture organizzative complesse con più acquirenti, ruoli personalizzati e autorizzazioni di acquisto in account aziendali unificati. Le funzionalità chiave includono cataloghi e prezzi specifici della società, offerte negoziabili, gestione degli ordini di acquisto, elenchi di richieste di acquisto e funzionalità di ordinamento rapido. La soluzione supporta sia i modelli B2B che B2C in un’unica istanza, rendendola flessibile per le diverse esigenze aziendali. L’estensione richiede una licenza separata e si integra perfettamente con le funzioni principali di Adobe Commerce per fornire una soluzione di e-commerce B2B completa.

Per il provisioning, contatta il rappresentante del tuo account Adobe. Per informazioni dettagliate sull&#39;implementazione e sui passaggi di configurazione, vedere la [[!DNL B2B for Adobe Commerce] Guida utente](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

### [!DNL AEM Assets Integration for Commerce]

![Solo Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce, richiede anche licenze per Adobe Experience Manager (AEM) Assets e AEM Dynamic Media.

[!DNL AEM Assets Integration for Commerce] collega Adobe Commerce con il sistema DAM (Digital Asset Management) di Adobe Experience Manager per fornire il controllo centralizzato su tutte le risorse digitali. Questa integrazione consente la sincronizzazione automatizzata delle risorse, aggiornamenti in tempo reale ed un riutilizzo efficiente dei contenuti tra gli store commerce. Combinando le solide funzionalità di gestione delle risorse di AEM con Commerce, le aziende possono trarre vantaggio da flussi di lavoro semplificati, esperienze di marchio coerenti e distribuzione ottimizzata dei contenuti multimediali tramite infrastrutture basate su cloud.

Per il provisioning, contatta il rappresentante del tuo account Adobe. Per informazioni dettagliate sull&#39;implementazione e sui passaggi di configurazione, vedere la [[!DNL Assets Integration] Guida utente](../content-design/aem-assets-integration.md).

### [!DNL Live Search]

![Solo Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

Live Search è una funzione esclusiva di Adobe Commerce che fornisce una soluzione di ricerca basata sull’intelligenza artificiale con funzionalità di ricerca in tempo reale basata sulla tipologia di utente. Offre risultati rapidi e significativi grazie alle miniature dei prodotti mentre gli acquirenti digitano, insieme a faceting intelligente che regola automaticamente i filtri in base al comportamento di acquisto. La soluzione include funzionalità di merchandising per il potenziamento e la sottrazione dei prodotti, la gestione dei sinonimi e l’analisi delle ricerche. Incluso in Adobe Commerce senza costi aggiuntivi, [!DNL Live Search] sostituisce la funzionalità di ricerca predefinita con un&#39;esperienza di ricerca più sofisticata basata su SaaS. Per iniziare, è necessaria una configurazione minima.

Per informazioni dettagliate sull&#39;implementazione e requisiti tecnici, consulta la [Guida utente di Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html).

### [!DNL Product Recommendations]

![Solo Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

[!DNL Product Recommendations] è una funzionalità esclusiva di Adobe Commerce basata sulla tecnologia Adobe AI che offre suggerimenti di prodotto personalizzati in tutto il percorso di acquisto del cliente. La soluzione analizza in tempo reale il comportamento degli acquirenti e le relazioni tra i prodotti per generare automaticamente consigli pertinenti, senza richiedere regole manuali per il merchandising. Questo approccio basato sull’intelligenza artificiale consente di aumentare i tassi di conversione e il potenziale di profitto, creando al contempo esperienze di rilevamento dei prodotti più coinvolgenti per gli acquirenti.

Per i dettagli sull&#39;implementazione e le best practice, consulta la [[!DNL Product Recommendations] Guida utente](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html).

### [!DNL Catalog Service]

[!BADGE Installazioni supportate]{type=Informative tooltip="Supportato"} di Adobe Commerce e Magento Open Source

[!DNL Catalog Service] è una soluzione ad alte prestazioni per Adobe Commerce e Magento Open Source che fornisce accesso ottimizzato ai dati del catalogo tramite endpoint GraphQL. Gestisce un database separato sincronizzato per i dettagli dei prodotti e le informazioni correlate, evitando la comunicazione diretta tra le applicazioni per velocizzare i tempi di caricamento delle pagine. Il servizio è particolarmente utile per le pagine di dettaglio dei prodotti, gli elenchi di categorie e le pagine dei risultati di ricerca, rendendolo ideale sia per le implementazioni commerciali tradizionali che headless.

Per istruzioni di installazione e dettagli tecnici, vedere la [[!DNL Catalog Service] Guida utente](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html).

>[!NOTE]
>
>Catalog Services viene installato automaticamente quando sono abilitati Live Search o Product Recommendations. Non è richiesta l&#39;installazione manuale.

### [!DNL Payment Services]

[!BADGE Installazioni supportate]{type=Informative tooltip="Supportato"} di Adobe Commerce e Magento Open Source

[!DNL Payment Services] è una soluzione di pagamento chiavi in mano per i negozi Adobe Commerce e Magento Open Source che offre funzionalità complete di elaborazione dei pagamenti. Il servizio integra funzionalità di gateway di pagamento sicure con protezione antifrode integrata, offrendo al contempo più opzioni di pagamento tra cui carte di credito/debito, PayPal, Venmo (Stati Uniti) e piani PayLater. Offre funzioni di reporting unificato delle transazioni e gestione degli ordini tramite l&#39;interfaccia di amministrazione di Commerce, semplificando agli esercenti il tracciamento dei pagamenti, la gestione del flusso di cassa e la riconciliazione dei dati finanziari in un&#39;unica posizione.

Per i passaggi di configurazione dettagliati e le opzioni di pagamento, consulta la [[!DNL Payment Services] Guida utente](https://experienceleague.adobe.com/en/docs/commerce/payment-services/overview).
