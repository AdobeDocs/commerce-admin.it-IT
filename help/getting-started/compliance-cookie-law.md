---
title: Conformità alle normative sui cookie
description: Per mantenere il passo con la legislazione in molti paesi per quanto riguarda l’utilizzo dei cookie, Adobe Commerce e Magento Open Source offrono ai commercianti una scelta di metodi per ottenere il consenso dei clienti.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: b90164030569f18bfd10fd52f12e3bbd22626b63
workflow-type: tm+mt
source-wordcount: '2138'
ht-degree: 0%

---

# Conformità alle normative sui cookie

I cookie sono file di piccole dimensioni che vengono salvati nel computer di ogni visitatore del sito e utilizzati come luoghi di memorizzazione temporanea per informazioni. Le informazioni salvate nei cookie vengono utilizzate per personalizzare l’esperienza di acquisto, collegare i visitatori ai loro carrelli, misurare i pattern di traffico e migliorare l’efficacia delle promozioni. Per mantenere il passo con la legislazione in molti paesi per quanto riguarda l’utilizzo dei cookie, Adobe Commerce e Magento Open Source offrono ai commercianti una scelta di metodi per ottenere il consenso dei clienti. Per un elenco dei cookie predefiniti in Adobe Commerce e Magento Open Source, [Riferimento cookie](#default-cookies).

>[!NOTE]
>
>Se modifichi le [impostazioni predefinite per la privacy di Google](../merchandising-promotions/google-tools.md#google-privacy-settings) in modo da rispettare il [Regolamento generale sulla protezione dei dati](compliance-gdpr.md), non è necessario ottenere il consenso degli utenti per l&#39;utilizzo dei cookie di Google Analytics.

## Modalità di restrizione dei cookie

Quando la modalità di restrizione dei cookie è abilitata, i visitatori del tuo store ricevono una notifica che indica che i cookie sono necessari per le operazioni complete delle funzioni. A seconda del tema, il messaggio potrebbe essere visualizzato sopra l’intestazione, sotto il piè di pagina o in un altro punto della pagina. Il messaggio rimanda all’informativa sulla privacy per ulteriori informazioni e incoraggia i visitatori a fare clic sul pulsante Consenti per concedere il consenso. Una volta concesso il consenso, il messaggio scompare.

L&#39;[informativa sulla privacy](privacy-policy.md)) deve includere il nome dell&#39;archivio e le informazioni di contatto e spiegare lo scopo di ogni cookie utilizzato dall&#39;archivio. Per ulteriori informazioni, consulta [Riferimento cookie](#default-cookies).

>[!NOTE]
>
>Se modifichi la chiave URL dell’informativa sulla privacy, devi anche creare un URL personalizzato da riscrivere per reindirizzare il traffico alla nuova chiave URL. In caso contrario, il collegamento nel messaggio Modalità di restrizione cookie restituisce `404 Page Not Found`.

![Esempio di vetrina - Avviso di restrizione cookie](./assets/storefront-cookie-restriction-message.png){width="600"}

### Passaggio 1: abilitare la modalità di restrizione dei cookie

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra in **[!UICONTROL General]**, scegli **[!UICONTROL Web]**.

1. Espandere la sezione **[!UICONTROL Default Cookie Settings]** ed eseguire le operazioni seguenti:

   ![Configurazione Web - impostazioni cookie predefinite](./assets/web-default-cookie-settings.png){width="600"}

   - Immetti **[!UICONTROL Cookie Lifetime]** in secondi.

   - Se si desidera rendere i cookie disponibili per altre cartelle, immettere **[!UICONTROL Cookie Path]**. Per rendere i cookie disponibili in qualsiasi punto del sito, immettere una barra (`/`). Questo valore può contenere solo il percorso del cookie e **_non può_** contenere altri parametri del cookie.

   - Per rendere i cookie disponibili per un sottodominio, immettere il nome del sottodominio nel campo **[!UICONTROL Cookie Domain]** (`subdomain.yourdomain.com`). Per rendere i cookie disponibili per tutti i sottodomini, immettere il nome di dominio preceduto da un punto (`.yourdomain.com`). Questo valore può contenere solo il dominio del cookie e **_non può_** contenere altri parametri del cookie.

   - Per impedire ai linguaggi di script, come JavaScript, di accedere ai cookie, assicurarsi che **Usa solo HTTP** sia impostato su `Yes`.

   - Imposta **[!UICONTROL Cookie Restriction Mode]** su `Yes`.

     Se necessario, deselezionare la casella di controllo e fare clic su **[!UICONTROL OK]** per confermare il cambio di ambito.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Quando viene richiesto di aggiornare la cache, fare clic sul collegamento **[!UICONTROL Cache Management]** nel messaggio di sistema e aggiornare ogni cache non valida.

### Passaggio 2: aggiornare l’informativa sulla privacy

Aggiorna l&#39;[informativa sulla privacy](privacy-policy.md) in modo che rifletta le informazioni raccolte dalla tua azienda e il modo in cui vengono utilizzate.

## Cookie predefiniti

I cookie predefiniti in Adobe Commerce e Magento Open Source sono classificati come Esenti/Non esenti per aiutare i commercianti a soddisfare i requisiti delle normative sulla privacy come il [RGPD](compliance-gdpr.md). I commercianti devono utilizzare queste informazioni come guida e consultare i consulenti legali per aggiornare le Politiche sulla privacy e sui cookie nell’ambito di una strategia completa di conformità alla normativa sulla privacy.

I seguenti cookie sono utilizzati da [!DNL Commerce] &quot;preconfigurati&quot; per le installazioni on-premise e cloud. Questi cookie possono essere richiesti da funzionalità esplicitamente richieste dal cliente. Per ulteriori informazioni sulla durata dei cookie di sessione, vedere [Durata sessione](../customers/customer-online-options.md).

Alcuni di questi cookie possono fornire opzioni di configurazione, inclusa l’abilitazione/disabilitazione, in base alle esigenze.

### Cookie di funzionalità richiesti (esenti)

#### `add_to_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) acquisisce lo SKU del prodotto, il nome, il prezzo e la quantità rimossi dal carrello. Consente a Google Analytics di sapere quando un prodotto è stato aggiunto a un carrello.

#### `guest-view`

Collega un ordine ospite a un ospite (perché non esiste un account per l&#39;ospite). Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `login_redirect`

Salva l&#39;URL di reindirizzamento per indirizzare l&#39;utente in caso di accesso e registrazione dell&#39;utente completati. Salva la pagina in cui si trovava un utente prima dell&#39;accesso (per determinare la posizione in cui tornerà dopo l&#39;accesso).

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Archiviazione locale per funzionalità banner. Memorizza localmente il contenuto del banner per migliorarne le prestazioni. Il contenuto del banner include risorse generali del sito web che visualizzano le informazioni per un acquirente. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `mage-messages`

Tiene traccia dei messaggi di errore e di altre notifiche mostrate all’utente, come il messaggio di consenso ai cookie e vari messaggi di errore. Il messaggio viene eliminato dal cookie dopo che è stato mostrato all’acquirente. Non esiste un’opzione per disabilitare questo cookie. Questo è il modo in cui le informazioni una tantum vengono comunicate all’utente, ad esempio i messaggi di errore. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `product_data_storage` (archiviazione locale)

Memorizza la configurazione dei dati di prodotto utilizzati per utilizzare le funzioni &quot;Visualizzato di recente&quot; e &quot;Confronta prodotti&quot;. Memorizza le impostazioni specifiche di un utente (ad esempio, se ha recentemente visualizzato un prodotto o confrontato prodotti). Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `recently_compared_product` (archiviazione locale)

Memorizza gli ID prodotto dei prodotti confrontati di recente. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `recently_compared_product_previous` (archiviazione locale)

Memorizza gli ID prodotto dei prodotti confrontati in precedenza per facilitarne la navigazione. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `recently_viewed_product` (archiviazione locale)

Memorizza gli ID prodotto dei prodotti visualizzati di recente per facilitarne la navigazione. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `recently_viewed_product_previous` (archiviazione locale)

Memorizza gli ID prodotto dei prodotti visualizzati di recente per facilitarne la navigazione. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `remove_from_cart`

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) consente a Google Analytics di sapere quando un prodotto è stato rimosso da un carrello.

#### `stf`

Registra l&#39;ora in cui i messaggi vengono inviati dal modulo SendFriend ([Invia un messaggio e-mail a un amico](../stores-purchase/email-a-friend.md)). Quando un acquirente invia un collegamento a un prodotto, questo cookie registra una marca temporale e mantiene un conteggio.

#### `X-Magento-Vary`

Indica quando è necessario distribuire una nuova versione di una pagina dalla cache. Supporta le prestazioni del sito web. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `form_key`

Un meccanismo di sicurezza che contiene un valore generato in modo casuale per impedire attacchi CSRF (Cross Site Request Forgery), aiutando a determinare se una richiesta proviene da una sorgente autentica o da un attore non valido. Si tratta di una procedura standard del settore per prevenire gli attacchi CSRF. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `mage-cache-sessid`

Utile per determinare quando pulire l’archiviazione locale nel browser dopo la scadenza della sessione. Viene utilizzato per determinare se l’archiviazione locale deve essere pulita. L’assenza di questo cookie attiva la pulizia dell’archiviazione locale. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `mage-cache-storage`

Archiviazione locale di contenuti specifici per i visitatori che abilita le funzioni di e-commerce. Inutilizzato per impostazione predefinita, ma quando viene utilizzato, viene utilizzato per accelerare il pagamento in modo che le informazioni utente di base siano disponibili quando qualcuno esce e ritorna. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `mage-cache-storage-section-invalidation`

Memorizza le informazioni relative alle sezioni della pagina che devono essere invalidate e rimosse. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `persistent_shopping_cart`

Memorizza l’ID chiave di un carrello persistente per consentire il ripristino del carrello per un acquirente anonimo. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `private_content_version`

Aggiunge un numero e un orario casuali e univoci alle pagine con contenuto del cliente per impedire che vengano memorizzate nella cache del server. È impostato in più posizioni: in PHP, in JavaScript come cookie e in JavaScript nell’archiviazione locale. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `section_data_ids`

Memorizza informazioni specifiche del cliente relative alle azioni avviate dall&#39;acquirente, ad esempio la visualizzazione della lista dei desideri e le informazioni di pagamento. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `store`

Tiene traccia della visualizzazione o delle impostazioni locali specifiche del negozio selezionate dall’acquirente. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `PHPSESSID`

Tiene traccia delle sessioni utente nella vetrina. Questi sono gli acquirenti che usano i prodotti finali. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `admin`

Tiene traccia delle sessioni utente sul lato Amministratore. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `loggedOutReasonCode`

Impostato quando un utente amministratore viene bloccato dopo un certo numero di tentativi di password non riusciti.

#### `section_data_clean`

Impostato quando un utente passa alla visualizzazione archivio. La presenza di questo cookie attiva JavaScript per ricaricare determinate sezioni sulla pagina in modo da riflettere la corretta visualizzazione dello store. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `lang`

Impostato indirettamente dal modulo Admin Analytics. Utilizzato solo in un&#39;area amministrativa di un negozio. Non applicabile agli acquirenti. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `s_fid`

Impostato indirettamente dal modulo Admin Analytics. ID visitatore univoco/timestamp di fallback. Viene utilizzato per identificare un visitatore univoco se il cookie standard `s_vi` non è disponibile a causa di restrizioni relative ai cookie di terze parti. Utilizzato solo in un&#39;area amministrativa di un negozio. Non applicabile agli acquirenti. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `s_cc`

Impostato indirettamente dal modulo Admin Analytics. Viene impostato e letto dal codice JavaScript per determinare se i cookie sono abilitati. Utilizzato solo in un&#39;area amministrativa di un negozio. Non applicabile agli acquirenti. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `apt.sid`

Impostato dalla libreria PX Gainsight utilizzata indirettamente dal modulo Admin Analytics. Questo cookie ha lo scopo di consentire il tracciamento degli ID di sessione persistenti nel dominio di primo livello del prodotto e viene utilizzato come ID di riferimento per la sessione attiva. Utilizzato solo in un&#39;area amministrativa di un negozio. Non applicabile agli acquirenti. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `apt.uid`

Impostato dalla libreria PX Gainsight utilizzata indirettamente dal modulo Admin Analytics. Lo scopo di questo cookie è quello di consentire il tracciamento degli ID persistenti sotto il dominio di primo livello del prodotto e viene utilizzato come ID di riferimento per l’entità utente. Utilizzato solo in un&#39;area amministrativa di un negozio. Non applicabile agli acquirenti. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `s_sq`

Impostato indirettamente dal modulo Admin Analytics. Utilizzato dalla funzione ClickMap che raccoglie dati su dove i visitatori fanno clic e su ciò che fanno clic. Memorizza le informazioni di ogni clic. Utilizzato solo in un&#39;area amministrativa di un negozio. Non applicabile agli acquirenti. Per mantenere la stabilità del sistema, non disabilitare questo cookie.

#### `pagebuilder_modal_dismissed`

Impostato dal modulo Page Builder. Contiene un flag che impedisce ai prompt successivi che richiedono a un amministratore di confermare l’apertura di una determinata azione se l’amministratore li ha esplicitamente ignorati in precedenza. Utilizzato solo in un&#39;area amministrativa di un negozio. Non applicabile agli acquirenti.

#### `pagebuilder_template_apply_confirm`

Impostato dal modulo Page Builder. Contiene un flag che impedisce ai prompt successivi che richiedono a un amministratore di confermare l’apertura di una determinata azione se l’amministratore li ha esplicitamente ignorati in precedenza. Utilizzato solo in un&#39;area amministrativa di un negozio. Non applicabile agli acquirenti.

#### `accordion-&lbrace;VARIABLE&rbrace;-&lbrace;VARIABLE&rbrace;`

Utilizzato come parte dell’implementazione della funzionalità schede solo in un’area amministrativa di un archivio. Non applicabile agli acquirenti.

## Cookie di Product Recommendations

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) I seguenti cookie sono utilizzati dai consigli di prodotto per i clienti Adobe Commerce. Questi cookie sono installati con il modulo [DataServices](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure).

- `mg_dnt`: ti consente di [limitare la raccolta dati di Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/developer/setting-cookie) se disponi di codice personalizzato per gestire il consenso dei cookie sul tuo sito.
- `user_allowed_save_cookie`: utilizzato per la [modalità di restrizione cookie](#cookie-restriction-mode).
- `authentication_flag`: indica se un acquirente ha effettuato l&#39;accesso o la disconnessione. Questo cookie viene aggiornato contemporaneamente al cookie `dataservices_customer_id`.
- `dataservices_customer_id`: indica se un acquirente ha effettuato l&#39;accesso o la disconnessione. Questo cookie contiene l’ID univoco del cliente nel sistema.
- `dataservices_customer_group`: indica il gruppo di un cliente. Questo cookie viene memorizzato come checksum [sha1](https://en.wikipedia.org/wiki/SHA-1) dell&#39;ID gruppo del cliente.
- `dataservices_cart_id`: identifica le azioni del carrello di un acquirente. Questo cookie contiene l’ID carrello univoco del cliente nel sistema.
- `dataservices_product_context`: identifica le interazioni prodotto di un acquirente. Questo cookie contiene l’ID univoco del preventivo del cliente nel sistema.

### Dati di archiviazione locale per Product Recommendations

I seguenti dati vengono salvati nell’archiviazione locale per i negozi che utilizzano il tema Luma quando è installato Live Search o Product Recommendations:

- `ds-cart`: memorizza le informazioni del carrello per la funzionalità specifica di Luma
- `ds-cart-order`: memorizza le informazioni sull&#39;ordine per la funzionalità del carrello
- `ds-purchase-history`: tiene traccia della cronologia acquisti del cliente
- `ds-view-history-time-decay`: memorizza la cronologia di visualizzazione del prodotto con il decadimento basato sul tempo
- `ds-logged-in`: indica lo stato di accesso del cliente. Questi dati esistono solo quando il cliente ha effettuato l’accesso e vengono memorizzati anche quando è abilitata la modalità di restrizione dei cookie. Questi sono gli unici dati che Commerce memorizza nell’archiviazione locale quando è abilitata la modalità di restrizione dei cookie, indipendentemente dallo stato di consenso dell’utente.

## Cookie aggiuntivi

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) I seguenti cookie sono impostati per i clienti Adobe Commerce. Questi cookie sono installati con il modulo [DataServices](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure).

- `mg`: impostato da Snowplow JavaScript tracker. Ulteriori informazioni sono disponibili nella [documentazione Snowplow](https://docs.snowplow.io/docs/sources/trackers/javascript-trackers/web-tracker/tracker-setup/initialization-options/).
- `com.adobe.alloy.getTld`: dato il nome host della pagina Web corrente, questo è il dominio più in alto che non è un &quot;suffisso pubblico&quot; come descritto in https://publicsuffix.org. In sostanza, questo è il dominio di primo livello che può accettare i cookie. Questo cookie fa parte di [Alloy Web SDK](https://github.com/adobe/alloy).

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
