---
title: Estensioni da Adobe
description: Rivedi le informazioni sulle estensioni per Adobe Commerce e Magento Open Source rilasciate da Adobe.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Estensioni da Adobe

Questo argomento fornisce informazioni sulle estensioni per Adobe Commerce e Magento Open Source rilasciate da Adobe. Le estensioni aggiungono funzioni, funzionalità, servizi e integrazioni all’amministratore e alla vetrina. Alcune di queste estensioni sono sviluppate tramite contributi della community di Magento Open Source. Alcune estensioni richiedono un’installazione separata, altre sono installate per impostazione predefinita.

## Estensioni installate

Alcune estensioni vengono installate automaticamente con Adobe Commerce o Magento Open Source.

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

## Estensioni da aggiungere

[[!DNL Commerce Marketplace]](https://marketplace.magento.com/) è la risorsa eCommerce globale per le applicazioni e i servizi che espandono le soluzioni [!DNL Commerce] con nuove potenti funzionalità. Adobe rilascia diverse estensioni tramite [!DNL Marketplace] che possono essere installate e configurate nell&#39;archivio Adobe Commerce o Magento Open Source per fornire integrazioni e funzionalità avanzate.

### [!DNL Live Search]

![Solo Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

L&#39;estensione [!DNL Live Search] collega il tuo store al servizio Live Search, una piattaforma di ricerca gratuita di Adobe Commerce che consente ai venditori di offrire ai clienti un&#39;esperienza di ricerca avanzata dall&#39;intelligenza artificiale. Costruito con l&#39;intelligenza artificiale di Adobe, Adobe Sensei, Intelligent Faceting aiuta i commercianti a fare di più con meno, rimuovendo il lavoro manuale sul faceting/filtraggio.

Per ulteriori informazioni, consulta la [Guida utente di Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/guide-overview.html).

### [!DNL Product Recommendations]

![Solo Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

L&#39;estensione [!DNL Product Recommendations] collega lo store al servizio Product Recommendations, un potente strumento di marketing che puoi utilizzare per aumentare conversioni, ricavi e coinvolgimento. [!DNL Product Recommendations] è stato creato da Adobe Commerce ed è guidato dall&#39;intelligenza artificiale testata in battaglia, Adobe Sensei, in modo da poter stimolare il coinvolgimento e la conversione. Questa funzione elimina il lavoro manuale necessario per fornire consigli di prodotto pertinenti a ogni cliente.

Per ulteriori informazioni, consultare la [[!DNL Product Recommendations] Guida utente](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=en).

### [!DNL Catalog Service]

[!DNL Catalog Service] consente di offrire ai clienti un&#39;esperienza di prodotto ottimizzata migliorando le prestazioni, migliorando la scalabilità e aumentando le conversioni. Per ulteriori informazioni, consultare la [[!DNL Catalog Service] Guida utente](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html).

### [!DNL Payment Services]

[!DNL Payment services] per Adobe Commerce e Magento Open Source è una soluzione di pagamento completamente integrata che semplifica la gestione dei pagamenti e offre ai clienti l&#39;opportunità di pagare. Esegui la riconciliazione sicura di tutti i dati relativi a pagamenti e transazioni all’interno dell’amministratore di Adobe Commerce, consentendoti di gestire gli ordini e i pagamenti in un’unica posizione e di effettuare un pagamento senza soluzione di continuità. Per ulteriori informazioni, consultare la [[!DNL Payment Services] Guida utente](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html).

### [!DNL Store Fulfillment]

Il servizio Store Fulfillment per Adobe Commerce e Magento Open Source consente un acquisto online di qualità superiore, la customer experience del ritiro in negozio (BOPIS) e massimizza la produttività dei dipendenti grazie a un flusso di lavoro completo di esecuzione abilitato tramite un dispositivo mobile. Per ulteriori informazioni, consultare la [[!DNL Store Fulfillment] Guida utente](https://experienceleague.adobe.com/docs/commerce/store-fulfillment/guide-overview.html).

### [!DNL Amazon Sales Channel]

[!DNL Amazon Sales Channel] per Adobe Commerce consente di integrare il database delle inserzioni di Amazon Seller Central con il catalogo prodotti [!DNL Commerce] e di gestire le inserzioni e le vendite di Amazon nell&#39;amministratore Commerce. Per ulteriori informazioni, consultare la [[!DNL Amazon Sales] Guida utente](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html).

### [!DNL Channel Manager]

[!DNL Channel Manager] consente di aumentare le vendite, raggiungere nuovi clienti, semplificare le operazioni e risparmiare tempo integrando un catalogo di prodotti Adobe Commerce o Magento Open Source con Walmart Marketplace. Dopo l&#39;installazione e la configurazione dell&#39;estensione, il personale dell&#39;azienda potrà gestire in modo semplice le inserzioni, le scorte, gli ordini, le restituzioni e i rimborsi di Walmart Marketplace da [!DNL Commerce Admin]. Per ulteriori informazioni, consultare la [[!DNL Channel Manager] Guida utente](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html).
