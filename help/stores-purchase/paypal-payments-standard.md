---
title: Pagamenti PayPal Standard
description: Scopri come impostare PayPal Payments Standard come soluzione di pagamento online sul tuo store.
exl-id: b4024dac-34d7-4f1a-ad9d-0fc406194609
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2073'
ht-degree: 0%

---

# Pagamenti PayPal Standard

[Pagamenti PayPal Standard][4] è il modo più semplice per accettare i pagamenti online. Puoi offrire ai tuoi clienti la comodità del pagamento sia con carta di credito che con PayPal semplicemente aggiungendo un pulsante di pagamento al tuo negozio.

>[!NOTE]
>
>Per i commercianti al di fuori degli Stati Uniti, si chiama _Pagamenti sito Web PayPal Standard_.

Con PayPal Payments Standard puoi scorrere le carte di credito sui dispositivi mobili. Non esiste alcun costo mensile e puoi ricevere il pagamento tramite eBay. Le carte di credito supportate sono Visa, MasterCard, Discover e American Express. Inoltre, i clienti possono pagare direttamente dai loro account PayPal personali. PayPal Payments Standard è disponibile in tutti i paesi dell&#39;elenco di riferimento di PayPal a livello mondiale.

>[!IMPORTANT]
>
>**Requisiti PSD2:** <br/>
>A partire dal 14 settembre 2019, le banche europee potrebbero rifiutare i pagamenti che non soddisfano [PSD2](../getting-started/compliance-payment-services-directive.md) requisiti. Non è necessaria alcuna azione affinché PayPal Payments Standard si conformi a PSD2 perché tutti i requisiti sono gestiti da PayPal.

## Esigenze degli esercenti

- [Account aziendale PayPal][1]

## Flusso di lavoro di cassa

Per i clienti, PayPal Payments Standard è un processo in un&#39;unica fase se le informazioni sulla carta di credito sui loro conti PayPal personali sono aggiornate.

1. **Ordine di Customer Places** - Il cliente fa clic/tocca il _Paga ora_ per completare l’acquisto.

1. **PayPal elabora la transazione** - Il cliente viene reindirizzato al sito PayPal per completare la transazione.

## Imposta Pagamenti PayPal Standard

>[!NOTE]
>
>PayPal Payments Standard non può essere utilizzato contemporaneamente a qualsiasi altro metodo PayPal, incluso Express Checkout. Se modifichi le soluzioni di pagamento, quella utilizzata in precedenza è disabilitata.

>[!TIP]
>
>Clic **[!UICONTROL Save Config]** in qualsiasi momento per salvare i tuoi progressi.

### Passaggio 1: avviare la configurazione

Questo metodo di impostazione presuppone che sia presente un conto PayPal.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. Se nell’installazione di Commerce sono presenti più siti web, store o visualizzazioni, imposta **[!UICONTROL Store View]** nella vista Store in cui desideri applicare questa configurazione.

1. In _[!UICONTROL Merchant Location]_, seleziona la sezione **[!UICONTROL Merchant Country]**dove si trova la tua azienda.

   Questa impostazione determina la selezione delle soluzioni PayPal visualizzate nella configurazione.

   ![Paese esercente](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Espandi **[!UICONTROL PayPal All-in-One Payment Solutions]** e fai clic su **[!UICONTROL Configure]** per **[!UICONTROL Payments Standard]**.

   ![Pagamenti PayPal Standard](./assets/paypal-payments-standard.png){width="700" zoomable="yes"}

### Passaggio 2: abilita e collega il tuo conto PayPal

![Configurazione standard pagamenti PayPal](./assets/paypal-payments-display.png){width="600" zoomable="yes"}

1. Connetti il tuo account per test o produzione:

   - Per verificare la modalità di sviluppo, fai clic su **[!UICONTROL Sandbox Credentials]** e inserisci il [Sandbox PayPal][3] credenziali.
   - Per la modalità di produzione, fai clic su **[!UICONTROL Connect with PayPal]** e inserisci le credenziali dell’account di produzione.

   Una volta convalidata la connessione, puoi procedere.

1. Imposta **[!UICONTROL Enable this Solution]** a `Yes`.

1. Se desideri offrire [Credito PayPal](paypal.md#paypal-credit-and-pay-later) ai clienti, imposta **[!UICONTROL Enable PayPal Credit]** a `Yes`.

### Passaggio 3: completare le impostazioni di Payments Standard

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Payments Standard]** sezione.

   ![Impostazioni richieste](../configuration-reference/sales/assets/payment-methods-paypal-payments-standard-required.png){width="600" zoomable="yes"}

1. Inserisci il **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Gli indirizzi e-mail fanno distinzione tra maiuscole e minuscole. Per ricevere il pagamento, l&#39;indirizzo email che immetti deve corrispondere a quello specificato nel tuo conto PayPal dell&#39;esercente.

   Se non hai un conto PayPal, fai clic su **[!UICONTROL Start accepting payments via PayPal]**.

1. Imposta **[!UICONTROL API Authentication Methods]** a uno dei seguenti elementi:

   - `API Signature` - Questo metodo di autenticazione PayPal è il più semplice da implementare ed è basato sul nome utente, la password e una stringa univoca di caratteri e numeri che identifica il tuo account. Le credenziali della firma API non scadono.
   - `API Certificate` - Questo metodo di autenticazione PayPal è più sicuro, si basa sul tuo nome utente, password e un certificato scaricabile. Le credenziali API scadono dopo tre anni e devono essere rinnovate.

   Se necessario, completare quanto segue:

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. Se utilizzi le credenziali dell’account sandbox, imposta **[!UICONTROL Sandbox Mode]** a `Yes`.

   Quando esegui il test della configurazione in una sandbox, utilizza solo [numeri di carta di credito][2] che sono consigliati da PayPal. Quando sei pronto per passare alla produzione, torna alla configurazione e imposta la modalità sandbox su `No` e collegati al tuo conto PayPal di produzione.

1. Se il sistema utilizza un server proxy per stabilire la connessione tra Adobe Commerce o Magento Open Source e il sistema di pagamento PayPal, impostare **[!UICONTROL API Uses Proxy]** a `Yes` e completano quanto segue:

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

### Passaggio 4: Impostare Advertise PayPal Credit / Advertise PayPal PayLater (facoltativo)

A partire dalla versione 2.4.3, PayPal PayLater è supportato nelle implementazioni che includono PayPal. Questa funzione consente ai clienti di pagare un ordine in rate bi-settimanali invece di pagare l’intero importo al momento dell’acquisto. L&#39;esperienza di credito PayPal è obsoleta.

Imposta **[!UICONTROL Enable PayPal PayLater Experience]** a uno dei seguenti elementi:

- `Yes` - Per impostare Advertise PayPal PayLater
- `No` - Per impostare il credito PayPal di Advertising

#### Pubblicizza credito PayPal

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Advertise PayPal Credit]** sezione.

   ![Pubblicizza le impostazioni della home page del credito PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Per ottenere le informazioni sull&#39;account, fare clic su **[!UICONTROL Get Publisher ID from PayPal]** e seguire le istruzioni.

1. Immetti il **[!UICONTROL Publisher ID]**.

   ![Pubblicizza credito PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Home Page]** sezione.

1. Per inserire un banner nella pagina, imposta **[!UICONTROL Display]** a `Yes`.

1. Imposta **[!UICONTROL Position]** a uno dei seguenti elementi:

   - `Header (center)`
   - `Sidebar (right)`

1. Imposta **[!UICONTROL Size]** a uno dei seguenti elementi:

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) nelle sezioni rimanenti e ripetere i passaggi precedenti:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Pubblicizza PayPal PayLater

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Advertise PayPal PayLater]** sezione.

1. Imposta **[!UICONTROL Enable PayPal PayLater]** a `Yes`.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Home Page]** sezione.

   ![Pubblicizza le impostazioni della home page del credito PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Per inserire un banner nella pagina, imposta **[!UICONTROL Display]** a `Yes`.

1. Imposta **[!UICONTROL Position]** a uno dei seguenti elementi:

   - `Header (center)`
   - `Sidebar`

1. Imposta **[!UICONTROL Style Layout]** a uno dei seguenti elementi:

   - `Text`
   - `Flex`

1. Per [!UICONTROL Style Layout] **[!UICONTROL Text]** solo, imposta **[!UICONTROL Logo Type]** a uno dei seguenti elementi:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Per [!UICONTROL Style Layout] **[!UICONTROL Text]** solo, imposta **[!UICONTROL Logo Position]** a uno dei seguenti elementi:

   - `Left`
   - `Right`
   - `Top`

1. Per [!UICONTROL Style Layout] **[!UICONTROL Text]** solo, imposta **[!UICONTROL Text Color]** a uno dei seguenti elementi:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Per [!UICONTROL Style Layout] **[!UICONTROL Text]** solo, imposta **[!UICONTROL Text Size]** a uno dei seguenti elementi:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Per [!UICONTROL Style Layout] **[!UICONTROL Flex]** solo, imposta **[!UICONTROL Ratio]** a uno dei seguenti elementi:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Per [!UICONTROL Style Layout] **[!UICONTROL Flex]** solo, imposta **[!UICONTROL Color]** a uno dei seguenti elementi:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) nelle sezioni rimanenti e ripetere i passaggi precedenti:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **Passaggio pagamento cassa**
   - **[!UICONTROL Catalog Category Page]**

### Passaggio 5: completare le impostazioni di base

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Basic Settings - PayPal Website Payments Standard]** sezione.

   ![Impostazioni di base](./assets/paypal-payments-basic.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi questo metodo di pagamento durante il pagamento.

   Si consiglia di utilizzare il titolo _PayPal_ per tutte le visualizzazioni dello store.

1. Se vengono offerti più metodi di pagamento, immettere un numero per **[!UICONTROL Sort Order]** per determinare la sequenza in cui PayPal Payments Standard viene visualizzato quando elencato con gli altri metodi di pagamento.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = innanzitutto, `1` = secondo, `2` = terzo e così via.)

1. Imposta **[!UICONTROL Payment Action]** a uno dei seguenti elementi:

   - `Authorization` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato fino a quando non viene catturato dal mercante.
   - `Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente prelevato dal conto del cliente.

1. Per visualizzare _[!UICONTROL Check out with PayPal]_sulla pagina del prodotto, impostare **[!UICONTROL Display on Product Details Page]**a `Yes`.

### Passaggio 6: completare le impostazioni avanzate

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Advanced Settings]** sezione.

   ![Impostazioni avanzate](../configuration-reference/sales/assets/payment-methods-paypal-payment-standard-advanced.png){width="600" zoomable="yes"}

1. Per rendere PayPal Payments Standard disponibile sia nel carrello che nel mini-carrello, impostare **[!UICONTROL Display on Shopping Cart]** a `Yes`.

1. Imposta **[!UICONTROL Payment from Applicable Countries]** a uno dei seguenti elementi:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione del negozio può utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, il _[!UICONTROL Payment from Specific Countries]_viene visualizzato. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Per registrare le comunicazioni con il sistema di pagamento nel file di registro, impostare **[!UICONTROL Debug Mode]** a `Yes`.

   >[!NOTE]
   >
   >Il file di registro viene archiviato sul server ed è accessibile solo agli sviluppatori. In conformità agli standard di sicurezza dei dati PCI, le informazioni sulla carta di credito non vengono registrate nel file di registro.

1. Per abilitare la verifica SSL, imposta **[!UICONTROL Enable SSL Verification]** a `Yes`.

1. Per visualizzare un riepilogo di ogni voce dell&#39;ordine nella pagina dei pagamenti PayPal, impostare **[!UICONTROL Transfer Cart Line Items]** a `Yes`.

   Per includere nel riepilogo fino a dieci opzioni di spedizione, impostare **[!UICONTROL Transfer Shipping Options]** a `Yes`. Questa opzione viene visualizzata solo se gli elementi riga sono impostati per il trasferimento.

1. Per determinare il tipo di immagine utilizzata per il pulsante di accettazione PayPal, imposta **[!UICONTROL Shortcut Buttons Flavor]** a uno dei seguenti elementi:

   - `Dynamic` - (Consigliato) Visualizza un&#39;immagine che può essere modificata dinamicamente dal server PayPal.
   - `Static` - Visualizza un&#39;immagine specifica che non può essere modificata dinamicamente.

1. Per consentire ai clienti che non hanno un conto PayPal di effettuare un acquisto con questo metodo, imposta **[!UICONTROL Enable PayPal Guest Checkout]** a `Yes`.

1. Imposta **[!UICONTROL Require Customer's Billing Address]** a uno dei seguenti elementi:

   - `Yes` - Richiede l&#39;indirizzo di fatturazione del cliente per tutti gli acquisti.
   - `No` - Non richiede l&#39;indirizzo di fatturazione del cliente per nessun acquisto.
   - `For Virtual Quotes Only` - Richiede l&#39;indirizzo di fatturazione del cliente solo per i preventivi virtuali.

1. Per consentire a un cliente di accedere a un [Contratto di fatturazione PayPal](paypal-billing-agreements.md) con il tuo Negozio quando non sono disponibili contratti di fatturazione attivi nell&#39;account cliente, imposta **[!UICONTROL Billing Agreement Signup]** a uno dei seguenti elementi:

   - `Auto` - Il cliente può stipulare un contratto di fatturazione durante il Checkout rapido o utilizzare un altro metodo di pagamento.
   - `Ask Customer` - Il cliente può decidere se stipulare un contratto di fatturazione durante il flusso di lavoro Pagamento rapido.
   - `Never` - Il cliente non può stipulare un contratto di fatturazione durante il flusso di lavoro Pagamento rapido.

   >[!NOTE]
   >
   >I commercianti devono richiedere l&#39;assistenza tecnica PayPal per abilitare gli accordi di fatturazione nei loro account. Il _Iscrizione al contratto di fatturazione_ Il parametro può essere abilitato solo dopo che PayPal conferma che gli accordi di fatturazione sono abilitati per il tuo account esercente.

1. Per consentire al cliente di completare la transazione dal sito PayPal senza tornare al negozio per la revisione dell&#39;ordine, impostare **[!UICONTROL Skip Order Review Step]** a `Yes`.

### Passaggio 7: completare e salvare le impostazioni di configurazione

1. Completa le seguenti sezioni, in base alle esigenze del tuo negozio:

   - [Impostazioni contratto di fatturazione PayPal](#paypal-billing-agreement-settings)
   - [Impostazioni rapporto liquidazione](#settlement-report-settings)
   - [Impostazioni esperienza front-end](#frontend-experience-settings)

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

#### Impostazioni contratto di fatturazione PayPal

A [contratto di fatturazione](paypal-billing-agreements.md) è un contratto di vendita tra l&#39;esercente e il cliente che è stato autorizzato da PayPal per l&#39;utilizzo con più ordini. Durante il processo di pagamento, l&#39;opzione di pagamento del contratto di fatturazione viene visualizzata solo per i clienti che hanno già stipulato un contratto di fatturazione con la società. Dopo che PayPal ha autorizzato il contratto, il sistema di pagamento emette un ID di riferimento univoco per identificare ogni ordine associato al contratto. Analogamente a un ordine di acquisto, non esiste alcun limite al numero di accordi di fatturazione che un cliente può impostare con la società.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL PayPal Billing Agreement Settings]** sezione.

   ![Impostazioni contratto di fatturazione](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enabled]** a `Yes`.

1. Per **[!UICONTROL Title]**, inserisci un titolo che identifichi il metodo PayPal Billing Agreement durante il pagamento.

1. Se vengono offerti più metodi di pagamento, immettere un numero in **[!UICONTROL Sort Order]** per determinare la sequenza in cui viene visualizzato il contratto di fatturazione quando viene elencato con altri metodi di pagamento durante il pagamento.

1. Imposta **[!UICONTROL Payment Action]** a uno dei seguenti elementi:

   - `Authorization` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato fino a quando non viene &quot;catturato&quot; dal mercante.
   - `Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente prelevato dal conto del cliente.

1. Imposta **[!UICONTROL Payment Applicable From]** a uno dei seguenti elementi:

   - `All Allowed Countries` - I clienti di tutti i paesi specificati nella configurazione del negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, il _[!UICONTROL Payment from Specific Countries]_viene visualizzato. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuno di essi.

1. Per registrare le comunicazioni con il sistema di pagamento nel file di registro, impostare **[!UICONTROL Debug Mode]** a `Yes`.

   >[!NOTE]
   >
   >Il file di registro viene archiviato sul server ed è accessibile solo agli sviluppatori. In conformità agli standard di sicurezza dei dati PCI, le informazioni sulla carta di credito non vengono registrate nel file di registro.

1. Per abilitare la verifica SSL, imposta **[!UICONTROL Enable SSL Verification]** a `Yes`.

1. Per visualizzare un riepilogo di ogni voce nell&#39;ordine del cliente nella pagina dei pagamenti PayPal, impostare **[!UICONTROL Transfer Cart Line Items]** a `Yes`.

1. Per consentire ai clienti di avviare un contratto di fatturazione dal dashboard del proprio account cliente, impostare **[!UICONTROL Allow in Billing Agreement Wizard]** a `Yes`.

#### Impostazioni rapporto liquidazione

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Settlement Report Settings]** sezione.

   ![Impostazioni rapporto liquidazione](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL SFTP Credentials]**, eseguire le operazioni seguenti:

   - Se ti sei iscritto al server FTP protetto PayPal, immetti le seguenti credenziali di accesso SFTP:

      - Login
      - Password

   - Per eseguire i rapporti sui test prima di andare in diretta con Express Checkout sul sito, imposta **[!UICONTROL Sandbox Mode]** a `Yes`.

   - Inserisci il **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     Per impostazione predefinita, il valore è `reports.paypal.com`.

   - Inserisci il **[!UICONTROL Custom Path]** in cui vengono salvati i rapporti.

     Per impostazione predefinita, il valore è `/ppreports/outgoing`.

1. Per generare i rapporti in base a una pianificazione, completa la **[!UICONTROL Scheduled Fetching]** impostazioni:

   - Imposta **[!UICONTROL Enable Automatic Fetching]** a `Yes`.

   - Imposta **[!UICONTROL Schedule]** a uno dei seguenti elementi:

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal conserva ogni rapporto per 45 giorni.

   - Imposta **[!UICONTROL Time of Day]** all’ora, al minuto e al secondo quando desideri generare i rapporti.

#### Impostazioni esperienza front-end

Utilizza il _[!UICONTROL Frontend Experience Settings]_per scegliere i logo PayPal da visualizzare sul sito e per personalizzare l&#39;aspetto delle pagine di PayPal.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Frontend Experience Settings]** sezione.

   ![Impostazioni esperienza front-end](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Seleziona la **[!UICONTROL PayPal Product Logo]** che desideri visualizzare nel blocco PayPal del tuo negozio.

   I logo PayPal sono disponibili in quattro stili e due dimensioni:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Per personalizzare l&#39;aspetto delle pagine di PayPal:

   - Inserisci il nome del **[!UICONTROL Page Style]** che desideri applicare alle tue pagine PayPal per esercenti:

      - `paypal` - Utilizza lo stile di pagina PayPal.
      - `primary` - Utilizza lo stile di pagina identificato come _primario_ nel profilo del tuo account.
      - `your_custom_value` - Utilizza uno stile di pagina di pagamento personalizzato, specificato nel profilo del tuo account.

   - Per **[!UICONTROL Header Image URL]**, immetti l&#39;URL dell&#39;immagine da visualizzare nell&#39;angolo superiore sinistro della pagina di pagamento. La dimensione massima del file è di 750 pixel di larghezza per 90 pixel di altezza.

     >[!NOTE]
     >
     >PayPal consiglia che l&#39;immagine risieda su un server protetto (https). In caso contrario, un browser potrebbe avvertire che _la pagina contiene elementi protetti e non protetti_.

   - Per impostare il colore delle pagine, immettere il codice esadecimale a sei caratteri, senza `#` simbolo, per ciascuno dei seguenti elementi:

      - **[!UICONTROL Header Background Color]** - Colore di sfondo per l&#39;intestazione della pagina di pagamento.
      - **[!UICONTROL Header Border Color]** - Colore per il bordo di due pixel attorno all&#39;intestazione.
      - **[!UICONTROL Page Background Color]** - Colore di sfondo per la pagina di pagamento e intorno all&#39;intestazione e al modulo di pagamento.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/api-basics/sandbox/
[4]: https://developer.paypal.com/docs/paypal-payments-standard/mobile-paypal-payments-standard/
