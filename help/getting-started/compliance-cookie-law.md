---
title: Conformità alle normative sui cookie
description: Per tenere il passo con la legislazione in molti paesi per quanto riguarda l’utilizzo dei cookie, Adobe Commerce e Magento Open Source offrono ai commercianti una scelta di metodi per ottenere il consenso dei clienti.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2145'
ht-degree: 0%

---

# Conformità alle normative sui cookie

I cookie sono file di piccole dimensioni che vengono salvati nel computer di ogni visitatore del sito e utilizzati come luoghi di memorizzazione temporanea per informazioni. Le informazioni salvate nei cookie vengono utilizzate per personalizzare l’esperienza di acquisto, collegare i visitatori ai loro carrelli, misurare i pattern di traffico e migliorare l’efficacia delle promozioni. Per tenere il passo con la legislazione in molti paesi per quanto riguarda l’utilizzo dei cookie, Adobe Commerce e Magento Open Source offrono ai commercianti una scelta di metodi per ottenere il consenso dei clienti. Per un elenco dei cookie predefiniti in Adobe Commerce e Magento Open Source, [Riferimento cookie](#default-cookies).

>[!NOTE]
>
>Se modificate il valore predefinito [Impostazioni privacy Google](../merchandising-promotions/google-tools.md#google-privacy-settings) per rispettare [Regolamento generale sulla protezione dei dati](compliance-gdpr.md), non è necessario ottenere il consenso degli utenti per l’utilizzo dei cookie Google Analytics.

## Metodo 1: consenso implicito

Il consenso implicito significa che i visitatori del tuo archivio hanno una chiara comprensione del fatto che i cookie sono una parte necessaria delle operazioni e, utilizzando il tuo sito, hanno indirettamente concesso l’autorizzazione per utilizzarli. La chiave per ottenere il consenso implicito è fornire informazioni sufficienti a consentire al visitatore di prendere una decisione informata. Molti negozi visualizzano un messaggio nella parte superiore di tutte le pagine standard che fornisce una breve panoramica sull’utilizzo dei cookie, con un collegamento all’informativa sulla privacy dello store. L&#39;informativa sulla privacy deve descrivere il tipo di informazioni raccolte dal tuo negozio e come vengono utilizzate.

## Metodo 2: consenso espresso

Gestione dello store in _modalità di restrizione dei cookie_ richiede ai visitatori di esprimere il proprio consenso prima che i cookie possano essere salvati nei loro computer. A meno che non venga concesso il consenso, molte funzioni del tuo archivio non sono disponibili. Ad esempio, se per il tuo archivio sono disponibili Google Analytics, queste possono essere richiamate solo dopo che il visitatore ha concesso l’autorizzazione all’uso dei cookie.

## Modalità di restrizione dei cookie

Quando la modalità di restrizione dei cookie è abilitata, i visitatori del tuo store ricevono una notifica che indica che i cookie sono necessari per le operazioni complete delle funzioni. A seconda del tema, il messaggio potrebbe essere visualizzato sopra l’intestazione, sotto il piè di pagina o in un altro punto della pagina. Il messaggio rimanda all’informativa sulla privacy per ulteriori informazioni e incoraggia i visitatori a fare clic sul pulsante Consenti per concedere il consenso. Una volta concesso il consenso, il messaggio scompare.

Il tuo [informativa sulla privacy](privacy-policy.md)) deve includere il nome del tuo Negozio e le informazioni di contatto, e spiegare lo scopo di ogni cookie utilizzato dal tuo Negozio. Per ulteriori informazioni, consulta [Riferimento cookie](#default-cookies).

>[!NOTE]
>
>Se modifichi la chiave URL dell’informativa sulla privacy, devi anche creare un URL personalizzato da riscrivere per reindirizzare il traffico alla nuova chiave URL. In caso contrario, il collegamento nel messaggio Modalità di restrizione cookie restituisce `404 Page Not Found`.

![Esempio di vetrina: avviso di restrizione dei cookie](./assets/storefront-cookie-restriction-message.png){width="600"}

### Passaggio 1: abilitare la modalità di restrizione dei cookie

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra in **[!UICONTROL General]**, scegli **[!UICONTROL Web]**.

1. Espandi **[!UICONTROL Default Cookie Settings]** ed effettuare le seguenti operazioni:

   ![Configurazione web: impostazioni cookie predefinite](./assets/web-default-cookie-settings.png){width="600"}

   - Inserisci il **[!UICONTROL Cookie Lifetime]** in secondi.

   - Se desideri rendere i cookie disponibili per altre cartelle, immetti **[!UICONTROL Cookie Path]**. Per rendere i cookie disponibili in qualsiasi punto del sito, immetti una barra (`/`). Questo valore può contenere solo il percorso del cookie e **_non può_** contiene altri parametri dei cookie.

   - Per rendere i cookie disponibili per un sottodominio, inserisci il nome del sottodominio nel **[!UICONTROL Cookie Domain]** campo (`subdomain.yourdomain.com`). Per rendere i cookie disponibili per tutti i sottodomini, inserisci il nome di dominio preceduto da un punto (`.yourdomain.com`). Questo valore può contenere solo il dominio del cookie e **_non può_** contiene altri parametri dei cookie.

   - Per impedire ai linguaggi di script, come JavaScript, di accedere ai cookie, assicurati che **Usa solo HTTP** è impostato su `Yes`.

   - Imposta **[!UICONTROL Cookie Restriction Mode]** a `Yes`.

     Se necessario, deseleziona la casella di controllo e fai clic su **[!UICONTROL OK]** per confermare il cambio di ambito.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando viene richiesto di aggiornare la cache, fare clic su **[!UICONTROL Cache Management]** nel messaggio di sistema. Quindi, aggiorna ogni cache non valida.

### Passaggio 2: aggiornare l’informativa sulla privacy

Aggiorna il tuo [informativa sulla privacy](privacy-policy.md) in modo da riflettere le informazioni raccolte dalla tua azienda e il modo in cui vengono utilizzate.

## Cookie predefiniti

I cookie predefiniti in Adobe Commerce e Magento Open Source sono classificati come Esenti/Non esenti per aiutare i commercianti a soddisfare i requisiti delle normative sulla privacy come [RGPD](compliance-gdpr.md). I commercianti devono utilizzare queste informazioni come guida e consultare i consulenti legali per aggiornare le Politiche sulla privacy e sui cookie nell’ambito di una strategia completa di conformità alla normativa sulla privacy.

I seguenti cookie vengono utilizzati da [!DNL Commerce] &quot;preconfigurato&quot; per le installazioni on-premise e cloud. Questi cookie possono essere richiesti da funzionalità esplicitamente richieste dal cliente. Per informazioni sulla durata dei cookie di sessione, consulta [Durata sessione](../customers/customer-online-options.md).

Alcuni di questi cookie possono fornire opzioni di configurazione, inclusa l’abilitazione/disabilitazione, in base alle esigenze.

### Cookie di funzionalità richiesti (esenti)


#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Solo per Adobe Commerce) Utilizzato da Google Tag Manager. Acquisisce lo SKU del prodotto, il nome, il prezzo e la quantità rimossi dal carrello e rende le informazioni disponibili per l’integrazione futura tramite script di terze parti.

#### `guest-view`

Memorizza l&#39;ID ordine utilizzato dagli acquirenti per recuperare lo stato dell&#39;ordine. Visualizzazione ordini guest. Utilizzato in _[!DNL Orders and Returns]_widget.

- È sicuro? No
- Solo HTTP: sì
- Criterio di scadenza: sessione
- Modulo: `Magento_Sales`

#### `login_redirect`

Mantiene la pagina di destinazione che veniva caricata prima che il cliente venisse indirizzato all’accesso. Un reindirizzamento di accesso viene utilizzato con il mini carrello per i clienti connessi se [Visualizza Mini Carrello](../stores-purchase/cart-configuration.md#mini-cart) l&#39;opzione di configurazione è impostata su `Yes`.

- È sicuro? No
- Solo HTTP: No
- Criterio di scadenza: sessione
- Modulo: `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (Solo per Adobe Commerce) Memorizza localmente il contenuto del banner per migliorare le prestazioni.

#### `mage-messages`

Tiene traccia dei messaggi di errore e di altre notifiche mostrate all’utente, come il messaggio di consenso ai cookie e vari messaggi di errore. Il messaggio viene eliminato dal cookie dopo che è stato mostrato all’acquirente.

Non esiste un’opzione per disabilitare questo cookie.

- È sicuro? No
- Solo HTTP: No
- Criteri di scadenza: durata 1 anno. Cancellato in front-end quando il messaggio viene visualizzato all’utente.
- Modulo: `Magento_Theme`

#### `mage-translation-storage` (archiviazione locale)

Memorizza il contenuto tradotto quando richiesto dall’acquirente. Utilizzato quando [Strategia di traduzione](../configuration-reference/advanced/developer.md) è configurato come &quot;Dictionary (Translation on Storefront side)&quot;.

- È sicuro? No
- Solo HTTP: No
- Criteri di scadenza: per regole di archiviazione locale
- Modulo: `Magento_Translation`

#### `mage-translation-file-version` (archiviazione locale)

Tiene traccia della versione delle traduzioni nell’archiviazione locale. Utilizzato quando [Strategia di traduzione](../configuration-reference/advanced/developer.md) è configurato come `Dictionary (Translation on Storefront side)`.

- È sicuro? No
- Solo HTTP: No
- Criteri di scadenza: per regole di archiviazione locale
- Modulo: `Magento_Translation`

#### `product_data_storage` (archiviazione locale)

Memorizza la configurazione per i dati di prodotto relativi a Prodotti visualizzati/confrontati di recente.

- È sicuro? No
- Solo HTTP: No
- Criteri di scadenza: per regole di archiviazione locale
- Modulo: `Magento_Catalog`

#### `recently_compared_product` (archiviazione locale)

Memorizza gli ID prodotto dei prodotti confrontati di recente.

- È sicuro? No
- Solo HTTP: No
- Criteri di scadenza: per regole di archiviazione locale
- Modulo: `Magento_Catalog`

#### `recently_compared_product_previous` (archiviazione locale)

Memorizza gli ID prodotto dei prodotti confrontati in precedenza per facilitarne la navigazione.

- È sicuro? No
- Solo HTTP: No
- Criteri di scadenza: per regole di archiviazione locale
- Modulo: `Magento_Catalog`

#### `recently_viewed_product` (archiviazione locale)

Memorizza gli ID prodotto dei prodotti visualizzati di recente per facilitarne la navigazione.

- È sicuro? No
- Solo HTTP: No
- Criteri di scadenza: per regole di archiviazione locale
- Modulo: `Magento_Catalog`

#### `recently_viewed_product_previous` (archiviazione locale)

Memorizza gli ID prodotto dei prodotti visualizzati di recente per facilitarne la navigazione.

- È sicuro? No
- Solo HTTP: No
- Criteri di scadenza: per regole di archiviazione locale
- Modulo: `Magento_Catalog`

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Utilizzato da [Gestione tag Google](../merchandising-promotions/google-tag-manager.md). Acquisisce lo SKU del prodotto, il nome, il prezzo e la quantità aggiunti al carrello e rende le informazioni disponibili per l’integrazione futura tramite script di terze parti.

#### `stf`

Registra l&#39;ora in cui i messaggi vengono inviati dall&#39;oggetto SendFriend ([Invia un&#39;e-mail a un amico](../stores-purchase/email-a-friend.md)).

- È sicuro? Sì
- Solo HTTP: sì
- Criterio di scadenza: sessione
- Modulo: `Magento_SendFriend`

#### `X-Magento-Vary`

Impostazione di configurazione che migliora le prestazioni quando si utilizza il caching dei contenuti statici di Vernice.

- È sicuro? Sì
- Solo HTTP: sì
- Criterio di scadenza: basato sull’impostazione PHP session.cookie_lifetime
- Modulo: `Magento_PageCache`

#### `form_key`

Misura di sicurezza che aggiunge una stringa casuale a tutti gli invii di moduli per proteggere i dati da CSRF (Cross-Site Request Forgery).

- È sicuro? No
- Solo HTTP: No
- Criteri di scadenza:
   - PHP: Basato sull&#39;impostazione PHP session.cookie_lifetime
   - JS: Session
- Modulo: Cache pagine

#### `mage-cache-sessid`

Il valore di questo cookie attiva la pulizia dell’archiviazione della cache locale. Quando il cookie viene rimosso dall’applicazione back-end, l’amministratore ripulisce l’archiviazione locale e imposta il valore del cookie su `true`.

- È sicuro? No
- Solo HTTP: No
- Criterio di scadenza: sessione
- Modulo: `Magento_Customer`

#### `mage-cache-storage`

Archiviazione locale di contenuti specifici per i visitatori che abilita le funzioni di e-commerce.

- È sicuro? No
- Solo HTTP: No
- Criterio di scadenza: sessione
- Modulo: `Magento_Customer`, `Magento_Persistent`

#### `mage-cache-storage` (archiviazione locale)

Archiviazione locale di contenuti specifici per i visitatori che abilita le funzioni di e-commerce.

- È sicuro? No
- Solo HTTP: No
- Criterio di scadenza: sessione
- Modulo: `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation` (archiviazione locale)

Forza l’archiviazione locale di sezioni di contenuto specifiche che devono essere invalidate.

- È sicuro? No
- Solo HTTP: No
- Criteri di scadenza: per archiviazione locale
- Modulo: `Magento_Customer`

#### `persistent_shopping_cart`

Memorizza la chiave (ID) del carrello persistente per consentire il ripristino del carrello per un acquirente anonimo.

- È sicuro? Sì
- Solo HTTP: sì
- Criterio di scadenza: basato su [Carrello acquisti persistente](../stores-purchase/cart-persistent.md) - Configurazione della durata della persistenza (secondi)
- Modulo: `Magento_Persistent`

#### `private_content_version`

Aggiunge un numero e un orario casuali e univoci alle pagine con contenuto del cliente per impedire che vengano memorizzate nella cache del server.

È impostato in più posizioni: in PHP, in JavaScript come cookie e in JavaScript per l’archiviazione locale.

For HTTP Only= Solo HTTP`Yes` (in base alla richiesta), significa che il cookie è sicuro se impostato durante la richiesta HTTPS e non sicuro se impostato durante la richiesta HTTP.

- È sicuro? `Yes` (su richiesta), `No`
- Solo HTTP: `No`
- Criterio di scadenza: basato su [Carrello acquisti persistente](../stores-purchase/cart-persistent.md) - Configurazione della durata della persistenza (secondi)
   - PHP: `1` anno / `315360000s` (dieci anni)
   - JS: `1` giorno
   - Archiviazione locale JS: per regole di archiviazione locale (per sempre)
- Modulo: `Magento_PageCache`, `Magento_Customer`

#### `section_data_ids`

Memorizza informazioni specifiche del cliente relative alle azioni avviate dall&#39;acquirente, ad esempio la visualizzazione della lista dei desideri e le informazioni di pagamento.

- È sicuro? `No`
- Solo HTTP: `No`
- Criteri di scadenza: `Session`
- Modulo: `Magento_Customer`

#### `store`

Tiene traccia della visualizzazione o delle impostazioni locali specifiche del negozio selezionate dall’acquirente.

- È sicuro? `No`
- Solo HTTP: `Yes`
- Criteri di scadenza: `1` anno
- Modulo: `Magento_Store`

#### `mage-banners-cache-storage` - stoccaggio locale

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Archiviazione locale per la funzionalità banner.

- È sicuro? `No`
- Solo HTTP: `No`
- Criteri di scadenza: per regole di archiviazione locale
- Modulo: `Magento_Banner`

## Google Analytics i cookie

I seguenti cookie vengono utilizzati quando [Google Analytics](../merchandising-promotions/google-analytics.md) o Google Universal Analytics è completamente abilitato per l&#39;installazione. Per disabilitare questi cookie per la conformità alle normative sulla privacy, consulta [Impostazioni privacy Google](../merchandising-promotions/google-tools.md#google-privacy-settings). Per ulteriori informazioni, consulta [Google Analytics l’utilizzo dei cookie sui siti web][1].

### Cookie di Google Universal Analytics - non esenti

![Adobe Commerce](../assets/adobe-logo.svg) Librerie JavaScript di (solo Adobe Commerce): `gtag.js` e `analytics.js`

- `_ga`: distingue i visitatori dal sito.
- `_gid`: distingue i visitatori dal sito.
- `gat`: utilizzato per limitare la frequenza delle richieste.
- `dc_gtm_<property-id>`: limita la frequenza delle richieste quando le Google Analytics vengono distribuite con [Gestione tag Google](../merchandising-promotions/google-tag-manager.md).
- `AMP_TOKEN`: contiene un token che può essere utilizzato per recuperare un ID client dal servizio ID client AMP. Altri valori possibili includono rinuncia, richiesta di informazioni o errore durante il recupero di un ID client dal servizio ID client AMP.
- `_gac_<property-id>`: contiene informazioni relative alla campagna per l’utente. I tag di conversione di Google AdWords leggono questo cookie se la Google Analytics è collegata al tuo [AdWords][2] account.

### Cookie Google Analytics - non esenti

![Adobe Commerce](../assets/adobe-logo.svg) Libreria JavaScript (solo Adobe Commerce): `ga.js`

- `__utma`: distingue acquirenti e sessioni. Questo cookie viene creato quando viene eseguita la libreria JavaScript e non esiste `__utma` cookie. Il cookie viene aggiornato ogni volta che i dati vengono inviati alle Google Analytics.
- `__utmt`: utilizzato per limitare la frequenza delle richieste.
- `__utmb`: determina nuove sessioni/visite. Questo cookie viene creato quando viene eseguita la libreria JavaScript e non esiste `__utmb` cookie. Il cookie viene aggiornato ogni volta che i dati vengono inviati alle Google Analytics.
- `_utmz`: salva l’origine del traffico o la campagna che spiega come l’acquirente ha raggiunto il sito. Il cookie viene creato al momento dell’esecuzione della libreria JavaScript e viene aggiornato ogni volta che i dati vengono inviati alle Google Analytics.
- `__utmv`: memorizza i dati delle variabili personalizzate a livello di visitatore. Questo cookie viene creato quando uno sviluppatore utilizza `_setCustomVar` con una variabile personalizzata a livello di visitatore. Questo cookie viene aggiornato ogni volta che i dati vengono inviati alle Google Analytics.

## Cookie di Recommendations del prodotto

![Adobe Commerce](../assets/adobe-logo.svg) (Solo per Adobe Commerce) I seguenti cookie vengono utilizzati da Product Recommendations per i clienti Adobe Commerce. Questi cookie vengono installati con [Modulo DataServices](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg_dnt`: ti consente di: [limitare la raccolta dati di Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html) se disponi di un codice personalizzato per gestire il consenso dei cookie sul sito.
- `user_allowed_save_cookie`: utilizzato per [modalità di restrizione dei cookie](#cookie-restriction-mode).
- `authentication_flag`: indica se un acquirente ha effettuato l’accesso o la disconnessione. Questo cookie viene aggiornato contemporaneamente al `dataservices_customer_id` cookie.
- `dataservices_customer_id`: indica se un acquirente ha effettuato l’accesso o la disconnessione. Questo cookie contiene l’ID univoco del cliente nel sistema.
- `dataservices_customer_group`: indica il gruppo di un cliente. Questo cookie viene memorizzato come [sha1](https://en.wikipedia.org/wiki/SHA-1) checksum dell’ID gruppo del cliente.
- `dataservices_cart_id`: identifica le azioni del carrello di un acquirente. Questo cookie contiene l’ID carrello univoco del cliente nel sistema.
- `dataservices_product_context`: identifica le interazioni di prodotto di un acquirente. Questo cookie contiene l’ID univoco del preventivo del cliente nel sistema.

## Cookie aggiuntivi

![Adobe Commerce](../assets/adobe-logo.svg) (Solo per Adobe Commerce) I seguenti cookie sono impostati per i clienti Adobe Commerce. Questi cookie vengono installati con [Modulo DataServices](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html).

- `mg`: impostato da Snowplow JavaScript tracker. Ulteriori informazioni sono disponibili nella sezione [Documentazione di Snowplow](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options).
- `com.adobe.alloy.getTld`: dato il nome host della pagina web corrente, questo è il dominio più in alto che non è un &quot;suffisso pubblico&quot; come descritto in https://publicsuffix.org. In sostanza, questo è il dominio di primo livello che può accettare i cookie. Questo cookie fa parte del [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
