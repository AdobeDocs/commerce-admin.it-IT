---
title: Collegamento flusso di pagamento PayPal
description: Scopri come impostare PayPal Payflow Link come soluzione di pagamento online sul tuo store.
exl-id: dba4057e-1fea-4a23-8594-cc85f619d664
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2172'
ht-degree: 0%

---

# Collegamento flusso di pagamento PayPal

PayPal Payflow Link è disponibile solo per gli esercenti negli Stati Uniti e in Canada. I clienti non devono avere un conto PayPal personale e inserire le informazioni sulla carta di credito in un modulo ospitato da PayPal. Le informazioni non vengono mai memorizzate sul server Adobe Commerce o di Magento Open Source. Il collegamento del flusso di pagamento non può essere utilizzato per gli ordini creati dall’amministratore.

Le note di credito sono supportate per i rimborsi online e offline. Tuttavia, non sono supportati più rimborsi online.

>[!IMPORTANT]
>
>**Requisiti PSD2:** <br/>
>A partire dal 14 settembre 2019, le banche europee potrebbero rifiutare i pagamenti che non soddisfano [PSD2](../getting-started/compliance-payment-services-directive.md) requisiti. Per rispettare PSD2, PayPal Payflow Link deve essere integrato con Cardinal Commerce. Per ulteriori informazioni, consulta [Protezione 3D per il flusso di pagamento](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

## Requisiti

- [Account aziendale PayPal][1] Il gateway PayPal Payflow Pro collega l&#39;account esercente di PayPal con il sito Web esercente, fungendo sia da gateway che da account esercente.

- Se gestisci più siti web di Commerce, devi disporre di un account esercente PayPal separato per ogni sito web.

## Flusso di lavoro cliente

1. **Il cliente accede al pagamento** - Durante il pagamento, il cliente sceglie di pagare con PayPal Payflow link e inserisce le informazioni sulla carta di credito. Il cliente non deve avere un conto PayPal personale.
1. **Il cliente sceglie Paga ora** - Il cliente tocca il pulsante Paga ora per inviare l&#39;ordine.
1. **Il cliente immette le informazioni sulla carta di credito** - Il cliente inserisce le informazioni sulla carta di credito in un modulo ospitato da PayPal. Se il cliente fa clic su _Annulla pagamento_ , il cliente ritorna alla fase Informazioni pagamento del pagamento del pagamento e lo stato dell&#39;ordine cambia in _Annullato_.
1. **Il cliente invia l&#39;ordine** - Le informazioni sulla carta di credito vengono inviate direttamente a PayPal e non vengono conservate in nessun punto del sito Commerce.

## Flusso di lavoro ordini

1. **PayPal riceve una richiesta** - PayPal riceve dal cliente la richiesta di pagamento immediato.
1. **PayPal verifica le informazioni per il pagamento** - PayPal verifica le informazioni sulla carta di credito e assegna lo stato appropriato:
   - **Pagamento verificato:** Se verificata, la _Pagamento in sospeso_ Lo stato viene inizialmente assegnato all&#39;ordine fino al regolamento della transazione.
   - **Elaborazione** - La transazione è stata completata.
   - **Pagamento in sospeso** - Il sistema non ha ricevuto risposta da PayPal.
   - **Annullato** - La transazione non è riuscita per qualche motivo.
   - **Sospetta frode** - La transazione non ha superato alcuni dei [Filtri di frode PayPal](paypal.md#paypal-fraud-management-filters). Il sistema riceve la risposta da PayPal che la transazione è sotto esame da Fraud Service.
   - **Annulla pagamento:** Se il cliente fa clic su _Annulla pagamento_ , il cliente ritorna alla fase Informazioni pagamento del pagamento del pagamento e lo stato dell&#39;ordine cambia in _Annullato_.
1. **Il cliente viene reindirizzato alla pagina di conferma**  - Se la transazione è stata completata correttamente, il cliente viene reindirizzato alla pagina di conferma dell&#39;ordine nel tuo negozio. Se la transazione non riesce per qualsiasi motivo, nella pagina di pagamento viene visualizzato un messaggio di errore e il cliente viene invitato a ripetere il processo di pagamento. Queste situazioni sono gestite da PayPal.
1. **Ordine di evasione esercente** - Il commerciante fattura e spedisce l&#39;ordine come di consueto.

## Configura il tuo conto PayPal

1. Accedi al tuo [Account aziendale PayPal][2].

1. Configurare [Pagine di estrazione ospitate][4] utilizzando PayPal Manager con le seguenti impostazioni:

   - Sotto **[!UICONTROL Security Options]**, completa le impostazioni seguenti:

     **[!UICONTROL AVS]**: `No`

     **[!UICONTROL CSC]**: `No`

     **[!UICONTROL Enable Secure Token]**: `Yes`

   - Scegli **[!UICONTROL Customize]** e quindi scegliere **[!UICONTROL Layout C]**.

     Il layout C mostra solo i campi della carta di credito e di debito e può essere incorniciato sul sito o utilizzato come finestra a comparsa autonoma. La dimensione è fissa a 490 x 565 pixel, con spazio aggiuntivo per i messaggi di errore. Su alcuni sistemi, questa impostazione corregge un problema di reindirizzamento trasparente.

1. Al termine delle impostazioni di configurazione, fai clic su **[!UICONTROL Save and Publish]**.

1. Imposta un utente aggiuntivo (consigliato da PayPal):

   - Nella seconda riga del menu principale, fai clic su **[!UICONTROL Manage Users]**.

   - Per aggiungere un altro utente all&#39;account, fare clic su **[!UICONTROL Add User]**.

   - Compila i campi obbligatori nelle sezioni seguenti della _Aggiungi utente_ forma:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Clic **[!UICONTROL Update]**.

## Imposta collegamento flusso di pagamento PayPal

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

1. Espandi **[!UICONTROL PayPal Payment Gateways]** (se necessario) e fai clic su **[!UICONTROL Configure]** per **[!UICONTROL Payflow Link]**.

   ![Collegamento payflow - Configura](./assets/payflow-link.png){width="600" zoomable="yes"}

### Passaggio 2: completa le impostazioni PayPal richieste

![Impostazioni PayPal richieste - Collegamento flusso di pagamento PayPal](./assets/payflow-required-link.png){width="600" zoomable="yes"}

1. (Facoltativo) Inserisci il **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Gli indirizzi e-mail fanno distinzione tra maiuscole e minuscole. Per ricevere il pagamento, l&#39;indirizzo email deve corrispondere a quello specificato nel tuo conto PayPal.

1. Immetti una delle seguenti credenziali che utilizzi per accedere al tuo conto PayPal per esercenti:

   - **[!UICONTROL Partner]** - Il tuo PayPal Partner ID.
   - **[!UICONTROL User]** - L&#39;ID di un altro utente che è configurato sul tuo conto PayPal.
   - **[!UICONTROL Vendor]** - Nome di accesso dell&#39;utente PayPal.

1. Inserisci il **[!UICONTROL Password]** associato al tuo conto PayPal.

1. Per eseguire transazioni di test, impostare **[!UICONTROL Test Mode]** a `Yes`.

   Quando esegui il test della configurazione in una sandbox, utilizza solo [numeri di carta di credito][3] che sono consigliati da PayPal. Quando sei pronto per passare alla produzione, torna alla configurazione e imposta Modalità di test su `No`.

1. Se il sistema utilizza un server proxy per stabilire la connessione al sistema PayPal, impostare **[!UICONTROL Test Mode]** a `Yes` ed effettuare le seguenti operazioni:

   - Inserisci l’indirizzo IP del **[!UICONTROL Proxy Host]**.

   - Immettere il numero di porta del **[!UICONTROL Proxy Port]**.

     Un proxy viene utilizzato quando il firewall del server impedisce l&#39;accesso diretto al server PayPal. In questo caso, per inoltrare il traffico viene utilizzato un server di terze parti.

1. Imposta **[!UICONTROL Enable Payflow Link]** a `Yes`.

1. Se desideri abilitare [Pagamento PayPal Express](paypal-express-checkout.md) opzioni per i clienti, imposta **[!UICONTROL Enable Express Checkout]** a `Yes`.

1. Se desideri offrire [Credito PayPal](paypal.md#paypal-credit-and-pay-later) ai clienti, imposta **[!UICONTROL Enable PayPal Credit]** a `Yes`.

### Passaggio 3: Impostare Advertise PayPal Credit / Advertise PayPal PayLater (facoltativo)

A partire dalla versione 2.4.3, PayPal PayLater è supportato nelle implementazioni che includono PayPal. Questa funzione consente ai clienti di pagare un ordine in rate bi-settimanali invece di pagare l’intero importo al momento dell’acquisto. L&#39;esperienza di credito PayPal è obsoleta.

Imposta **[!UICONTROL Enable PayPal PayLater Experience]** a uno dei seguenti elementi:

- `Yes` - Per impostare Advertise PayPal PayLater
- `No` - Per impostare il credito PayPal di Advertising

#### Pubblicizza credito PayPal

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Advertise PayPal Credit]** sezione.

   ![Pubblicizza credito PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Per ottenere le informazioni sull&#39;account, fare clic su **[!UICONTROL Get Publisher ID from PayPal]** e seguire le istruzioni.

1. Immetti il **[!UICONTROL Publisher ID]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Home Page]** sezione.

   ![Pubblicizza le impostazioni della home page del credito PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) nelle sezioni rimanenti e ripetere i passaggi precedenti per la configurazione della home page:

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
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Passaggio 4: completare le impostazioni di base

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Basic Settings - PayPal Payflow Link]** sezione.

   ![Impostazioni di base - PayPal Payflow Link](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-basic-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Title]**, inserisci un titolo che identifichi PayPal Payflow Link durante il pagamento.

   Si consiglia di utilizzare il titolo _Carta di debito o di credito_.

1. Se vengono offerti più metodi di pagamento, immettere un numero per **[!UICONTROL Sort Order]** per determinare la sequenza in cui viene visualizzato il collegamento del flusso di pagamento quando elencato con gli altri metodi di pagamento.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = innanzitutto, `1` = secondo, `2` = terzo e così via.)

1. Imposta **[!UICONTROL Payment Action]** a uno dei seguenti elementi:

   - `Authorization` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato fino a quando non viene catturato dal mercante.
   - `Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente prelevato dal conto del cliente.

### Passaggio 5: completare le impostazioni avanzate

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Advanced Settings]** sezione.

   ![Impostazioni avanzate - PayPal Payflow Link](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-advanced-settings.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Payment Applicable From]** a uno dei seguenti elementi:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione del negozio può utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, il _[!UICONTROL Payment from Specific Countries]_viene visualizzato. Tenere premuto il tasto Ctrl e selezionare ogni paese nell&#39;elenco in cui i clienti possono effettuare acquisti dal negozio.

1. Per scrivere le comunicazioni con il sistema di pagamento nel file di registro, impostare **[!UICONTROL Debug Mode]** a `Yes`.

   >[!NOTE]
   >
   >In conformità agli standard di sicurezza dei dati PCI, le informazioni sulla carta di credito non vengono registrate nel file di registro.

1. Per abilitare la verifica dell’autenticità dell’host, imposta **[!UICONTROL Enable SSL Verification]** a `Yes`.

1. Se si desidera che il cliente sia in grado di correggere l&#39;immissione del codice di sicurezza CVV a tre cifre dal retro di una carta di credito, impostare **[!UICONTROL CVV Entry is Editable]** a `Yes`.

1. Per richiedere ai clienti di inserire un codice CVV, imposta **[!UICONTROL Require CVV Entry]** a `Yes`.

1. Per inviare una conferma del pagamento al cliente, impostare **[!UICONTROL Send Email Confirmation]** a `Yes`.

1. Per determinare il metodo utilizzato per scambiare informazioni con il server PayPal durante una transazione, impostare **[!UICONTROL URL method for Cancel URL and Return URL]** a uno dei seguenti elementi:

   - `GET` - Recupera le informazioni risultanti da un processo (metodo predefinito).
   - `POST` : fornisce un blocco di dati, ad esempio i dati immessi in un modulo, a un processo di gestione dei dati.

   Il _Annulla URL_ e _URL restituito_ fare riferimento alla pagina in cui il cliente restituisce dopo aver completato o annullato la parte di pagamento del processo di pagamento sul server PayPal

1. Completa le seguenti sezioni, in base alle esigenze del tuo negozio:

   - [Impostazioni rapporto liquidazione](#settlement-report-settings)
   - [Impostazioni esperienza front-end](#frontend-experience-settings)

#### Impostazioni rapporto liquidazione

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Settlement Report Settings]** sezione.

   ![Impostazioni report liquidazione - Payflow PayPal Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

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

   ![Impostazioni esperienza front-end - Payflow PayPal Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### Passo 6: Completare le impostazioni di base per PayPal Express Checkout

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Basic Settings - PayPal Express Checkout]** sezione.

   ![Impostazioni di base](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi questo metodo di pagamento durante il pagamento.

   Impostazione del titolo su _PayPal_ per ogni visualizzazione store.

1. Se vengono offerti più metodi di pagamento, immettere un numero per **[!UICONTROL Sort Order]** per determinare la sequenza in cui appare PayPal Express Checkout quando elencato con gli altri metodi di pagamento.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = innanzitutto, `1` = secondo, `2` = terzo e così via.)

1. Imposta **[!UICONTROL Payment Action]** a uno dei seguenti elementi:

   - `Authorization` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato fino al _acquisito_ dal mercante.
   - `Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente prelevato dal conto del cliente.

1. Per visualizzare _[!UICONTROL Check out with PayPal]_sulla pagina del prodotto, impostare **[!UICONTROL Display on Product Details Page]**a `Yes`.

### Passo 7: Completare le impostazioni avanzate per PayPal Express Checkout

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Advanced Settings]** sezione.

   ![Impostazioni avanzate](../configuration-reference/sales/assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Display on Shopping Cart]** a `Yes`.

1. Imposta **[!UICONTROL Payment Applicable From]** a uno dei seguenti elementi:

   - `All Allowed Countries` - I clienti di tutti i paesi specificati nella configurazione del negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, il _[!UICONTROL Payment from Specific Countries]_viene visualizzato. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ogni elemento.

1. Per scrivere le comunicazioni con il sistema di pagamento nel file di registro, impostare **[!UICONTROL Debug Mode]** a `Yes`.

   >[!NOTE]
   >
   >In conformità agli standard di sicurezza dei dati PCI, le informazioni sulla carta di credito non vengono registrate nel file di registro.

1. Per abilitare la verifica dell’autenticità dell’host, imposta **[!UICONTROL Enable SSL Verification]** a `Yes`.

1. Per visualizzare un riepilogo completo dell&#39;ordine cliente per voce dalla sede PayPal, impostare **[!UICONTROL Transfer Cart Line Items]** a `Yes`.

1. Per consentire al cliente di completare la transazione dal sito PayPal senza tornare al negozio per la revisione dell&#39;ordine, impostare **[!UICONTROL Skip Order Review Step]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
