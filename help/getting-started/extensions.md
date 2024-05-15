---
title: Estensioni da Adobe
description: Rivedi le informazioni sulle estensioni per Adobe Commerce e Magento Open Source rilasciate da Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 6414a7aea7dcbe0f2379ed74455518220a1fbd64
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Estensioni da Adobe

Questo argomento fornisce informazioni sulle estensioni per Adobe Commerce e Magento Open Source rilasciate da Adobe. Le estensioni aggiungono funzioni, funzionalità, servizi e integrazioni all’amministratore e alla vetrina. Alcune di queste estensioni sono sviluppate attraverso contributi Magenti Open Source della Comunità. Alcune estensioni richiedono un’installazione separata, altre sono installate per impostazione predefinita.

## Estensioni installate

Alcune estensioni vengono installate automaticamente con Adobe Commerce o Magento Open Source.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) offre una migliore gestione delle scorte e delle spedizioni in una o più sedi e canali di vendita con algoritmi di protezione del pagamento e di corrispondenza delle spedizioni simultanei. Tenere traccia delle quantità di magazzino, fornire ai clienti quantità precise di scorte vendibili e spedirle in base a raccomandazioni o selezioni manuali per controllare l&#39;intero magazzino. Configurare le impostazioni di gestione a livello globale, per origine e per prodotto.

>[!NOTE]
>
>Questa estensione è stata sviluppata nell&#39;ambito del [[!DNL Inventory Management]](https://github.com/magento/inventory) (precedentemente MSI) tramite il programma di progettazione della community.

[!DNL Inventory Management] viene installato con tutte le funzionalità abilitate per impostazione predefinita. Non sono necessari ulteriori passaggi per abilitare queste funzioni di inventario. Per ulteriori informazioni su [!DNL Inventory Management] , consulta la sezione [[!DNL Inventory Management] Guida utente](../inventory-management/guide-overview.md).

### Braintree

PayPal e Gene Commerce hanno sviluppato insieme l&#39;estensione ufficiale di Braintree per i negozi Commerce 2.4.x. Grazie a una migliore esperienza di pagamento progettata per favorire la conversione, gli aggiornamenti includono opzioni PayLater che mostrano automaticamente messaggi e pulsanti PayLater rilevanti ai consumatori durante gli acquisti e durante il pagamento.

Questa estensione è installata per impostazione predefinita, ma richiede [Braintree account](https://www.braintreepayments.com/) e la configurazione nell’Amministratore da abilitare per il tuo archivio. Per determinare le commissioni applicabili quando si utilizza Braintree per elaborare le transazioni, selezionare [Braintree prezzi](https://www.braintreepayments.com/braintree-pricing).

Per informazioni sulla configurazione delle Braintree in Admin, vedi [Braintree](../stores-purchase/braintree.md) argomento in _Guida all’esperienza di vendita e acquisto_.

### Google reCAPTCHA

Google reCAPTCHA offre un livello di sicurezza maggiore sia per la vetrina che per l’interfaccia utente amministratore rispetto a quello disponibile con il CAPTCHA standard e consente di:

- Verifica quando i clienti creano account, recuperano le password, accedono ai loro account o contattano la tua azienda.
- Migliora la sicurezza quando gli utenti amministratori accedono.

Riduce il potenziale errore dell’utente durante l’immissione di un codice Captcha e incoraggia la conversione del carrello senza aggiungere ostacoli durante il pagamento. [Abilitare e configurare reCAPTCHA](../systems/security-google-recaptcha.md) utilizzo di controlli invisibili o interattivi per migliorare l’accesso sicuro al [!DNL Commerce] Amministratore e vetrina.

### Autenticazione a due fattori

Il [!DNL Commerce] L’amministratore fornisce tutti gli accessi al tuo Negozio, agli ordini e ai dati dei clienti. [Autenticazione a due fattori](../systems/security-two-factor-authentication.md) (2FA o TFA) migliora la sicurezza richiedendo un’autenticazione aggiuntiva, oltre al nome di accesso e alla password standard, per accedere al [!DNL Commerce] Amministratore da tutti i dispositivi. L’estensione supporta più autenticatori, tra cui Google Authenticator, Authy, [!DNL Duo]e U2F. Questa autenticazione si applica solo agli utenti amministratori. Non è disponibile per gli account cliente di vetrina.

Queste funzioni sono attivate per impostazione predefinita. Ogni utente amministratore deve installare e configurare uno degli autenticatori supportati.

>[!NOTE]
>
>Per gli archivi Adobe Commerce che hanno abilitato l’autenticazione Adobe Identity Management Services (IMS) per l’amministratore, Commerce 2FA nativo è disabilitato. Gli utenti che hanno effettuato l’accesso all’amministratore con le proprie credenziali di Adobe non devono ripetere l’autenticazione per molte attività dell’amministratore. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Consulta [Panoramica dell’integrazione di Adobe Identity Management Service (IMS)](./adobe-ims-integration-overview.md).

## Estensioni da aggiungere

Il [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) è la risorsa eCommerce globale per applicazioni e servizi che si espandono [!DNL Commerce] con nuove funzioni e funzionalità. Adobe rilascia diverse estensioni tramite [!DNL Marketplace] che possono essere installati e configurati nell’Adobe Commerce o nell’archivio di Magento Open Source per fornire integrazioni e funzionalità avanzate.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Solo Adobe Commerce

Il [!DNL Live Search] L’estensione collega il negozio al servizio Live Search, una piattaforma di ricerca gratuita di Adobe Commerce che consente ai venditori di offrire ai clienti un’esperienza di ricerca avanzata con l’intelligenza artificiale. Costruito con l&#39;intelligenza artificiale di Adobe, Adobe Sensei, Intelligent Faceting aiuta i commercianti a fare di più con meno, rimuovendo il lavoro manuale sul faceting/filtraggio.

Consulta la [Guida utente di Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) per ulteriori informazioni.

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Solo Adobe Commerce

Il [!DNL Product Recommendations] L’estensione collega il tuo store al servizio Product Recommendations, un potente strumento di marketing che puoi utilizzare per aumentare le conversioni, i ricavi e il coinvolgimento. [!DNL Product Recommendations] è stato costruito da Adobe Commerce ed è guidato dalla sua intelligenza artificiale testata in battaglia, Adobe Sensei, in modo da poter stimolare il coinvolgimento e la conversione. Questa funzione elimina il lavoro manuale necessario per fornire consigli di prodotto pertinenti a ogni cliente.

Consulta la [[!DNL Product Recommendations] Guida utente](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) per ulteriori informazioni.

### [!DNL Catalog Service]

Il [!DNL Catalog Service] consente di offrire ai clienti un’esperienza di prodotto ottimizzata aumentando al contempo le prestazioni, migliorando la scalabilità e aumentando le conversioni. Consulta la [[!DNL Catalog Service] Guida utente](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) per ulteriori informazioni.

### [!DNL Payment Services]

[!DNL Payment services] per Adobe Commerce e Magento Open Source è una soluzione di pagamento completamente integrata che semplifica la gestione dei pagamenti e offre ai clienti l&#39;opportunità di pagare. Esegui la riconciliazione sicura di tutti i dati relativi a pagamenti e transazioni all’interno dell’amministratore di Adobe Commerce, consentendoti di gestire gli ordini e i pagamenti in un’unica posizione e di effettuare un pagamento senza soluzione di continuità. Consulta la [[!DNL Payment Services] Guida utente](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) per ulteriori informazioni.

### [!DNL Store Fulfillment]

Il servizio di consegna del negozio per Adobe Commerce e il Magento Open Source consente un acquisto online di qualità superiore, la customer experience del ritiro in negozio (BOPIS) e massimizza la produttività dei dipendenti grazie a un flusso di lavoro di distribuzione completo abilitato tramite un dispositivo mobile. Consulta la [[!DNL Store Fulfillment] Guida utente](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) per ulteriori informazioni.

### [!DNL Amazon Sales Channel]

Il [!DNL Amazon Sales Channel] per Adobe Commerce consente di integrare il database delle inserzioni di Amazon Seller Central con il [!DNL Commerce] catalogo dei prodotti e gestisci le inserzioni e le vendite Amazon nell’amministratore Commerce. Consulta la [[!DNL Amazon Sales] Guida utente](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) per ulteriori informazioni.

### [!DNL Channel Manager]

[!DNL Channel Manager] consente di aumentare le vendite, raggiungere nuovi clienti, semplificare le operazioni e risparmiare tempo integrando un catalogo di prodotti Adobe Commerce o di Magento Open Source con Walmart Marketplace. Dopo l&#39;installazione e la configurazione dell&#39;estensione, il personale dell&#39;azienda può gestire in modo semplice elenchi, inventario, ordini, restituzioni e rimborsi di Walmart Marketplace dal [!DNL Commerce Admin]. Consulta la [[!DNL Channel Manager] Guida utente](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) per ulteriori informazioni.
