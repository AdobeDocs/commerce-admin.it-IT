---
title: Pagamenti PayPal avanzati
description: Scopri come impostare PayPal Payments Advanced come soluzione di pagamento online sul tuo store.
exl-id: 018dd999-2f17-4650-8f61-624809ae76c6
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2155'
ht-degree: 0%

---

# Pagamenti PayPal avanzati

[Pagamenti PayPal avanzati][4] è un [conforme allo standard PCI](../getting-started/compliance-pci.md) soluzione che consente ai clienti di pagare con carta di debito o di credito senza lasciare il sito. Include una pagina di pagamento incorporata che può essere personalizzata per creare un’esperienza di pagamento fluida e sicura.

Anche i clienti senza un conto PayPal possono effettuare acquisti tramite il gateway di pagamento sicuro PayPal. Le carte accettate includono le carte di credito Visa, MasterCard, Switch/Maestro e Solo negli Stati Uniti e nel Regno Unito. Per maggiore comodità, PayPal Express Checkout è incluso con PayPal Payments Advanced.

>[!IMPORTANT]
>
>**Requisiti PSD2:** <br/>
>A partire dal 14 settembre 2019, le banche europee potrebbero rifiutare i pagamenti che non soddisfano [PSD2](../getting-started/compliance-payment-services-directive.md) requisiti. Per rispettare PSD2, PayPal Payments Advanced deve essere integrato con un plug-in di terze parti. Per ulteriori informazioni, consulta [Protezione 3D per il flusso di pagamento](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

>[!NOTE]
>
>PayPal Payments Advanced non può essere utilizzato per gli ordini creati dall&#39;amministratore del tuo negozio.

## Requisiti

- [Account aziendale PayPal][1]
- Se gestisci più siti web Adobe Commerce e Magento Open Source, devi avere un account esercente PayPal separato per ogni sito web.

## Flusso di lavoro di cassa

1. **Il cliente sceglie il metodo di pagamento** - Durante il pagamento, il cliente sceglie di pagare con PayPal Payments Advanced. Viene visualizzato il pulsante Paga ora invece del pulsante Inserisci ordine.

1. **Paga ora** - Il cliente fa clic/tocca _Paga ora_ e viene visualizzato un modulo ospitato da PayPal. Il cliente immette le informazioni sulla scheda e la scheda viene verificata. In caso di esito positivo, viene visualizzata la pagina di conferma dell’ordine.

   **Paga con PayPal** - Il modulo comprende anche: _Paga con PayPal_ che reindirizza il cliente al sito PayPal, dove il pagamento può essere effettuato con PayPal Express Checkout.

1. **Risoluzione dei problemi** - Se per qualsiasi motivo la transazione non riesce, nella pagina di pagamento viene visualizzato un messaggio di errore e al cliente viene richiesto di riprovare. Tutti i problemi sono gestiti da PayPal.

## Flusso di lavoro di elaborazione degli ordini

L&#39;elaborazione degli ordini con PayPal Payments Advanced è la stessa di qualsiasi ordine PayPal normale. Gli ordini vengono fatturati e spediti e vengono generate le note di credito per i rimborsi online e offline. Tuttavia, non sono disponibili più rimborsi online per gli ordini pagati con PayPal Payments Advanced.

1. **Il cliente effettua l&#39;ordine** - Nella fase finale del pagamento, il cliente tocca il pulsante Inserisci ordine.

1. **PayPal risponde** - PayPal valuta la richiesta. Se risulta valida, PayPal elabora la transazione.

1. **Stato ordine per set Commerce** - Commerce riceve una risposta da PayPal e imposta lo stato dell&#39;ordine su uno dei seguenti:

   - **Elaborazione** - La transazione è stata completata.
   - **Pagamento in sospeso** - Il sistema non ha ricevuto alcuna risposta da PayPal.
   - **Annullato** - Transazione non riuscita per qualche motivo
   - **Sospetta frode** - La transazione non ha superato alcuni dei [Filtri di frode PayPal](paypal.md#paypal-fraud-management-filters). Il sistema riceve la risposta da PayPal che la transazione è sotto esame da Fraud Service.

1. **Ordine di evasione esercente** - Il commerciante fattura e spedisce l&#39;ordine.

## Configura il tuo conto PayPal

Prima di configurare PayPal Payments Advanced in Commerce, devi configurare il tuo account sul sito Web PayPal.

1. Accedi al tuo [Account aziendale PayPal][2].

1. Vai a **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up Menu]** e completare le impostazioni seguenti:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. **[!UICONTROL Save]** le impostazioni.

   >[!NOTE]
   >
   >Se hai più siti Web Commerce, devi creare un account PayPal Payments Advanced separato per ciascuno di essi.

1. Quando viene richiesto di creare un layout, effettuare le seguenti operazioni:

   - Nella parte superiore della pagina, fai clic su **[!UICONTROL Customize]**.

   - Scegli **[!UICONTROL Layout C]**.

   - Clic **[!UICONTROL Save and Publish]**.

1. Configura un altro utente (consigliato da PayPal):

   - Accedi al tuo [Account aziendale PayPal][2].

   - Per impostare un altro utente, seguire le istruzioni.

   - **[!UICONTROL Save]** le modifiche.

## Imposta pagamenti PayPal avanzati in Commerce

>[!NOTE]
>
>Puoi avere due soluzioni PayPal attive contemporaneamente: Pagamento rapido, più qualsiasi soluzione All-In-One o Gateway di pagamento. Se modifichi le soluzioni di pagamento, quella utilizzata in precedenza viene disabilitata.

>[!TIP]
>
>Clic **[!UICONTROL Save Config]** in qualsiasi momento per salvare i tuoi progressi.

### Passaggio 1: avviare la configurazione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. Se nell’installazione di Commerce sono presenti più siti web, store o visualizzazioni, imposta **[!UICONTROL Store View]** nella vista Store in cui desideri applicare questa configurazione.

1. In _[!UICONTROL Merchant Location]_, seleziona la sezione **[!UICONTROL Merchant Country]**dove si trova la tua azienda.

   Questa impostazione determina la selezione delle soluzioni PayPal visualizzate nella configurazione.

   ![Paese esercente](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Espandi **[!UICONTROL PayPal All-in-One Payment Solution]** e fai clic su **[!UICONTROL Configure]** per **[!UICONTROL Payments Advanced]**.

   ![Pagamenti PayPal avanzati](./assets/paypal-payments-advanced.png){width="600" zoomable="yes"}

### Passaggio 2: completare le impostazioni richieste

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Required PayPal Settings]** sezione, se necessario.

   ![Impostazioni avanzate richieste - Pagamenti PayPal avanzati](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-required.png){width="600" zoomable="yes"}

1. (Facoltativo) Inserisci il **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Gli indirizzi e-mail fanno distinzione tra maiuscole e minuscole. Per ricevere il pagamento, l&#39;indirizzo email deve corrispondere a quello specificato nel tuo conto PayPal.

   Se non hai un conto PayPal, fai clic su **[!UICONTROL Start accepting payments via PayPal]**.

1. Immetti una delle seguenti credenziali che utilizzi per accedere al tuo conto PayPal per esercenti:

   - **[!UICONTROL Partner]** - Il tuo PayPal Partner ID.
   - **[!UICONTROL Vendor]** - Nome di accesso dell&#39;utente PayPal.
   - **[!UICONTROL User]** - L&#39;ID di un altro utente che è configurato sul tuo conto PayPal.

1. Inserisci il **[!UICONTROL Password]** associato al tuo conto PayPal.

1. Per eseguire transazioni di test, impostare **[!UICONTROL Test Mode]** a `Yes`.

   Quando esegui il test della configurazione in una sandbox, utilizza solo [numeri di carta di credito][3] che sono consigliati da PayPal. Quando sei pronto per passare alla produzione, torna alla configurazione e imposta Modalità di test su `No`.

1. Se il sistema utilizza un server proxy per stabilire la connessione al sistema PayPal, impostare **[!UICONTROL Use Proxy]** a `Yes` ed effettuare le seguenti operazioni:

   - Inserisci l’indirizzo IP del **[!UICONTROL Proxy Host]**.

   - Immettere il numero di porta del **[!UICONTROL Proxy Port]**.

     Un proxy viene utilizzato quando il firewall del server impedisce l&#39;accesso diretto al server PayPal. In questo caso, per inoltrare il traffico viene utilizzato un server di terze parti.

1. Imposta **[!UICONTROL Enable this Solution]** a `Yes`.

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

   ![Pubblicizza le impostazioni della home page del credito PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) nelle sezioni rimanenti e ripetere i passaggi precedenti:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Pubblicizza PayPal PayLater

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Advertise PayPal PayLater]** sezione.

1. Imposta **[!UICONTROL Enable PayPal PayLater]** a `Yes`.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Home Page]** sezione.

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

   ![Pubblicizza le impostazioni della home page del credito PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) nelle sezioni rimanenti e ripetere i passaggi precedenti:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Passaggio 4: completare le impostazioni di base

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Basic Settings - PayPal Payments Advanced]** sezione, se necessario.

   ![Impostazioni di base avanzate pagamenti PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-basic-settings.png){width="600" zoomable="yes"}

1. Per identificare PayPal Payments Advanced durante il pagamento, immettere un valore **[!UICONTROL Title]**.

   Si consiglia di utilizzare il titolo _Carta di debito o di credito_.

1. Se vengono offerti più metodi di pagamento, immettere un numero per **[!UICONTROL Sort Order]** per determinare la sequenza di visualizzazione di PayPal Payments Advanced quando viene elencato con altri metodi di pagamento durante l&#39;estrazione.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = innanzitutto, `1` = secondo, `2` = terzo e così via.)

1. Imposta **[!UICONTROL Payment Action]** a uno dei seguenti elementi:

   - `Authorization` - Approva l&#39;acquisto, ma blocca i fondi. L&#39;importo non viene prelevato fino al _acquisito_ dal mercante.
   - `Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente prelevato dal conto del cliente.

### Passaggio 5: completare le impostazioni avanzate

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Advanced Settings]** sezione.

   ![Impostazioni avanzate - Pagamenti PayPal avanzati](./assets/paypal-payments-advanced2.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Payment Applicable From]** a uno dei seguenti elementi:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione del negozio può utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, il _[!UICONTROL Payment from Specific Countries]_viene visualizzato. Tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e selezionare ogni paese nell&#39;elenco in cui i clienti possono effettuare acquisti dal negozio.

1. Per scrivere le comunicazioni con il sistema di pagamento nel file di registro, impostare **[!UICONTROL Debug Mode]** a `Yes`.

   Il file di registro per PayPal Payments Advanced è `payments_payflow_advanced.log`.

   >[!NOTE]
   >
   >In conformità agli standard di sicurezza dei dati PCI, le informazioni sulla carta di credito non vengono registrate nel file di registro.

1. Per abilitare la verifica dell’autenticità dell’host, imposta **[!UICONTROL Enable SSL Verification]** a `Yes`.

1. Per consentire al cliente di correggere il codice di sicurezza CVV a tre cifre dal retro di una carta di credito, impostare **[!UICONTROL CVV Entry is Editable]** a `Yes`.

1. Per richiedere ai clienti di inserire un codice CVV, imposta **[!UICONTROL Require CVV Entry]** a `Yes`.

1. Per inviare una conferma del pagamento al cliente, impostare **[!UICONTROL Send Email Confirmation]** a `Yes`.

1. Per determinare il metodo utilizzato per scambiare informazioni con il server PayPal durante una transazione, impostare **[!UICONTROL URL method for Cancel URL and Return URL]** a uno dei seguenti elementi:

   - `GET` - (Impostazione predefinita) Recupera le informazioni risultanti da un processo.
   - `POST` : fornisce un blocco di dati, ad esempio i dati immessi in un modulo, a un processo di gestione dei dati.

   Il _Annulla URL_ e _URL restituito_ fare riferimento alla pagina in cui il cliente ritorna dopo aver completato o annullato la parte di pagamento del processo di pagamento sul server PayPal.

1. Completa le seguenti sezioni, in base alle esigenze del tuo negozio:

   - [Impostazioni rapporto liquidazione](#settlement-report-settings)
   - [Impostazioni esperienza front-end](#frontend-experience-settings)

#### Impostazioni rapporto liquidazione

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Settlement Report Settings]** sezione.

   ![Impostazioni report liquidazione PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL SFTP Credentials]**, eseguire le operazioni seguenti:

   - Se ti sei iscritto al server FTP protetto di PayPal, immetti le seguenti credenziali di accesso SFTP:

      - Login
      - Password

   - Per eseguire i rapporti sui test prima della pubblicazione, impostare **[!UICONTROL Sandbox Mode]** a `Yes`.

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

   ![Impostazioni esperienza front-end PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png){width="600" zoomable="yes"}

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

   ![Impostazioni di base cassa PayPal Express](../configuration-reference/sales/assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi questo metodo di pagamento durante il pagamento.

   Impostazione del titolo su _PayPal_ per ogni visualizzazione store.

1. Se vengono offerti più metodi di pagamento, immettere un numero per **[!UICONTROL Sort Order]** per determinare la sequenza in cui appare PayPal Express Checkout quando elencato con gli altri metodi di pagamento.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = innanzitutto, `1` = secondo, `2` = terzo e così via.)

1. Imposta **[!UICONTROL Payment Action]** a uno dei seguenti elementi:

   - `Authorization` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato fino al _acquisito_ dal mercante.
   - `Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente prelevato dal conto del cliente.

1. Per visualizzare _[!UICONTROL Check out with PayPal]_sulla pagina del prodotto, impostare **[!UICONTROL Display on Product Details Page]**a `Yes`.

### Passo 7: Completa impostazioni avanzate - PayPal Express Checkout

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Advanced Settings]** sezione.

   ![Impostazioni avanzate cassa PayPal Express](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png){width="600" zoomable="yes"}

1. Per rendere PayPal Express Checkout disponibile sia dal carrello che dal mini carrello, impostare **[!UICONTROL Display on Shopping Cart]** a `Yes`.

1. Imposta **[!UICONTROL Payment Applicable From]** a uno dei seguenti elementi:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione del negozio può utilizzare questo metodo di pagamento.
   - `Specific Countries` |Dopo aver scelto questa opzione, il _Pagamento da elenco paesi specifici_ viene visualizzato. Tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ogni paese nell&#39;elenco in cui i clienti possono effettuare acquisti dal negozio.

1. Per scrivere le comunicazioni con il sistema di pagamento nel file di registro, impostare **[!UICONTROL Debug Mode]** a `Yes`.

   >[!NOTE]
   >
   >In conformità con [Standard di sicurezza dei dati PCI](../getting-started/compliance-pci.md), le informazioni sulla carta di credito non vengono registrate nel file di registro.

1. Per abilitare la verifica dell’autenticità dell’host, imposta **[!UICONTROL Enable SSL Verification]** a `Yes`.

1. Per visualizzare un riepilogo completo dell&#39;ordine del cliente per voce dalla sede PayPal, impostare **[!UICONTROL Transfer Cart Line Items]** a `Yes`.

1. Per consentire al cliente di completare la transazione dal sito PayPal senza tornare al negozio per la revisione dell&#39;ordine, impostare **[!UICONTROL Skip Order Review Step]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/gs-ppa-hosted-pages/
