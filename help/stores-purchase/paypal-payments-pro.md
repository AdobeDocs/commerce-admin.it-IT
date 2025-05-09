---
title: Pagamenti PayPal Pro
description: Scopri come impostare PayPal Payments Pro come soluzione di pagamento online sul tuo store.
exl-id: 9cc5c3a6-d471-4198-85a2-c4cf9dfd378b
feature: Payments
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '2257'
ht-degree: 0%

---

# Pagamenti PayPal Pro

[PayPal Payments Pro][3] ti offre tutti i vantaggi di un account esercente e di un gateway di pagamento in uno, oltre alla possibilità di creare un&#39;esperienza di pagamento personalizzata. PayPal Express Checkout è abilitato automaticamente con PayPal Payments Pro, in modo da poter accedere a più di 110 milioni di utenti PayPal attivi.

![Pagamenti PayPal Pro visualizzati nel mini carrello](./assets/storefront-mini-cart-payments-pro-racer-tank.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**Requisiti di PSD2:** <br/>
>A partire dal 14 settembre 2019, le banche europee potrebbero rifiutare i pagamenti che non soddisfano i requisiti di [PSD2](../getting-started/compliance-payment-services-directive.md). Per rispettare PSD2, PayPal Payments Pro deve essere integrato con un plug-in di terze parti.

>[!NOTE]
>
>Attualmente, PayPal Payments Pro è disponibile negli Stati Uniti, nel Regno Unito e in Canada.

## Requisiti

- [Account commerciante PayPal][1] (con pagamenti diretti attivati)

## Flusso di lavoro di cassa

1. **Il cliente accede al carrello**. Il cliente aggiunge prodotti al carrello e fa clic/tocca _Procedi al pagamento_.|
1. **Il cliente sceglie il metodo di pagamento**. Durante il pagamento, il cliente sceglie l&#39;opzione _Pagamento diretto PayPal_ e immette le informazioni sulla carta di credito.
   - Se paghi con PayPal Payments Pro, il cliente rimane sul tuo sito durante il processo di pagamento.
   - Se il pagamento viene effettuato tramite PayPal Express Checkout, il cliente viene reindirizzato al sito PayPal per completare la transazione.

Su richiesta del cliente, l&#39;amministratore del negozio può anche creare un ordine dall&#39;amministratore ed elaborare la transazione con PayPal Payments Pro.

## Flusso di lavoro di elaborazione degli ordini

1. **Ordine effettuato** - L&#39;ordine può essere elaborato dall&#39;amministratore del tuo Negozio o dal tuo conto PayPal.

1. **[!UICONTROL Payment Action]** - L&#39;azione di pagamento specificata nella configurazione viene applicata all&#39;ordine. Le opzioni includono:

   - **Autorizza** - Commerce crea un ordine cliente con stato _Elaborazione_. In questo caso, l&#39;importo di denaro da autorizzare è in attesa di approvazione.
   - **Vendita** - Commerce crea sia un ordine cliente che una fattura.
   - **Acquisizione** - PayPal trasferisce l&#39;importo dell&#39;ordine dal saldo del cliente, dal conto bancario o dalla carta di credito al conto dell&#39;esercente.

1. **Fatturazione** - Viene creata una fattura in Commerce dopo che PayPal invia un messaggio di notifica di pagamento immediato a Commerce.

   Assicurati che le notifiche di pagamento istantaneo siano abilitate nel tuo conto PayPal per esercenti.

   >[!NOTE]
   >
   >Se necessario, un ordine può essere parzialmente fatturato per una determinata quantità di prodotti. Per ogni fattura parziale sottomessa, diventa disponibile una transazione di acquisizione separata con un ID univoco e viene generata una fattura separata.

   Le transazioni di pagamento per sola autorizzazione vengono chiuse solo dopo l&#39;acquisizione dell&#39;intero importo dell&#39;ordine.

   Un ordine può essere annullato online in qualsiasi momento fino a quando l&#39;importo dell&#39;ordine non viene completamente fatturato.

1. **Restituzioni** - Se il cliente restituisce i prodotti acquistati e richiede un rimborso, come per l&#39;acquisizione dell&#39;importo dell&#39;ordine e la creazione della fattura, è possibile creare un rimborso online dall&#39;amministratore o dal proprio conto commerciale PayPal.

## Configura il tuo conto PayPal

Prima di configurare PayPal Payments Pro in Commerce, devi configurare il tuo account esercente sul sito Web PayPal.

1. Accedi al tuo account aziendale [PayPal](https://manager.paypal.com/).

1. Scegliere **[!UICONTROL Service Settings]** dal menu PayPal Manager.

1. In **[!UICONTROL Hosted Checkout Pages]**, fare clic su **[!UICONTROL Set Up]**.

1. In **[!UICONTROL Choose your settings]**, impostare **[!UICONTROL Transaction Process Mode]** su `Live`.

1. In **[!UICONTROL Display options on payment page]**, impostare **[!UICONTROL Cancel URL Method]** su `POST`.

1. In **[!UICONTROL Billing Information]**, selezionare le caselle di controllo del codice di sicurezza della scheda **[!UICONTROL CSC]** per i campi obbligatori e modificabili.

1. In **[!UICONTROL Payment Confirmation]**, impostare **[!UICONTROL Return URL Method]** su `POST`.

1. In **[!UICONTROL Security Options]**, configura quanto segue:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. Fare clic su **[!UICONTROL Save Changes]**.

1. Nel menu _PayPal Manager_, scegli **[!UICONTROL Service Settings]** e in _Pagine di pagamento ospitate_ scegli **[!UICONTROL Customize]**.

1. Scegli **[!UICONTROL Layout C]**.

   Il layout C mostra solo i campi della carta di credito e di debito e può essere incorniciato sul sito o utilizzato come finestra a comparsa autonoma. La dimensione è fissa a 490 x 565 pixel, con spazio aggiuntivo per i messaggi di errore. Su alcuni sistemi, questa impostazione corregge un problema di reindirizzamento trasparente.

1. Fare clic su **[!UICONTROL Save and Publish]**.

1. Scegliere **[!UICONTROL Account Administration]** dal menu PayPal Manager. In **[!UICONTROL Manage Security]**, fare clic su **[!UICONTROL Transaction Settings]**.

1. Imposta **[!UICONTROL Allow reference transactions]** su `Yes`.

1. Fare clic su **[!UICONTROL Confirm]**.

   >[!NOTE]
   >
   >Se hai più siti Web Commerce, devi creare un account PayPal Payments Pro separato per ciascuno di essi.

1. Configura un altro utente (consigliato da PayPal):

   - Nella seconda riga del menu principale fare clic su **[!UICONTROL Manage Users]**.

   - Per aggiungere un altro utente all&#39;account, scegliere **[!UICONTROL Add User]**. Il collegamento si trova appena sopra il titolo Gestisci utenti.

   - Compila i campi obbligatori nelle sezioni seguenti del modulo _[!UICONTROL Add User]_:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Fare clic su **[!UICONTROL Update]**.

1. Assicurati di disconnetterti dal tuo conto PayPal.

## Imposta PayPal Payments Pro in Commerce

>[!NOTE]
>
>Puoi avere due soluzioni PayPal attive contemporaneamente: [Pagamento PayPal Express](paypal-express-checkout.md), più una qualsiasi delle [soluzioni all-in-one](paypal.md#paypal-all-in-one-payment-solutions). Se modifichi le soluzioni di pagamento, quella utilizzata in precedenza viene disabilitata automaticamente.

>[!TIP]
>
>Fai clic su **[!UICONTROL Save Config]** in qualsiasi momento per salvare l&#39;avanzamento.

### Passaggio 1: avviare la configurazione

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. Se nell&#39;installazione di Commerce sono presenti più siti Web, store o visualizzazioni, impostare **[!UICONTROL Store View]** sulla visualizzazione dello store in cui si desidera applicare questa configurazione.

1. Nella sezione _[!UICONTROL Merchant Location]_, seleziona **[!UICONTROL Merchant Country]**in cui si trova la tua azienda.

   Questa impostazione determina la selezione delle soluzioni PayPal visualizzate nella configurazione.

   ![Paese esercente](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Espandere **[!UICONTROL PayPal All-in-One Payment Solution]** e fare clic su **[!UICONTROL Configure]** per **[!UICONTROL Payments Pro]**.

   ![Pagamenti PayPal Pro](./assets/paypal-payments-pro.png){width="600" zoomable="yes"}

### Passaggio 2: completa le impostazioni PayPal richieste

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Payments Pro and Express Checkout]**.

   ![Impostazioni richieste di PayPal Payments Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-required.png){width="600" zoomable="yes"}

1. (Facoltativo) Immetti **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Gli indirizzi e-mail fanno distinzione tra maiuscole e minuscole. Per ricevere il pagamento, l&#39;indirizzo email deve corrispondere a quello specificato nel tuo conto PayPal.

   Se non hai un conto PayPal, fai clic su **[!UICONTROL Start accepting payments via PayPal]**.

1. Immetti una delle seguenti credenziali che utilizzi per accedere al tuo conto PayPal per esercenti:

   - **[!UICONTROL Partner]** - ID partner PayPal.
   - **[!UICONTROL Vendor]** - Nome di accesso utente PayPal.
   - **[!UICONTROL User]** - L&#39;ID di un altro utente configurato sul tuo conto PayPal.

1. Immetti **[!UICONTROL Password]** associato al tuo conto PayPal.

1. Per eseguire le transazioni di test, impostare **[!UICONTROL Test Mode]** su `Yes`.

   Durante il test della configurazione in una sandbox, utilizza solo [numeri di carta di credito][2] consigliati da PayPal. Quando si è pronti per passare alla produzione, tornare alla configurazione e impostare la modalità di test su `No`.

1. Se il sistema utilizza un server proxy per stabilire la connessione al sistema PayPal, impostare **[!UICONTROL Use Proxy]** su `Yes` e procedere come segue:

   - Immettere l&#39;indirizzo IP di **[!UICONTROL Proxy Host]**.

   - Immettere il numero di porta di **[!UICONTROL Proxy Port]**.

   Un proxy viene utilizzato quando il firewall del server impedisce l&#39;accesso diretto al server PayPal. In questo caso, per inoltrare il traffico viene utilizzato un server di terze parti.

1. Imposta **[!UICONTROL Enable this Solution]** su `Yes`.

1. Se vuoi offrire [il credito PayPal](paypal.md#paypal-credit-and-pay-later) ai tuoi clienti, imposta **[!UICONTROL Enable PayPal Credit]** su `Yes`.

1. Se si desidera memorizzare in modo sicuro i dettagli relativi al pagamento o alla carta di credito del cliente, in modo che i clienti non debbano immettere nuovamente le informazioni sul pagamento ogni volta, impostare **[!UICONTROL Vault Enabled]** su `Yes`.

### Passaggio 3: Impostare Advertise PayPal Credit / Advertise PayPal PayLater (facoltativo)

A partire dalla versione 2.4.3, PayPal PayLater è supportato nelle implementazioni che includono PayPal. Questa funzione consente ai clienti di pagare un ordine in rate bi-settimanali invece di pagare l’intero importo al momento dell’acquisto. L&#39;esperienza di credito PayPal è obsoleta.

Imposta **[!UICONTROL Enable PayPal PayLater Experience]** su uno dei seguenti:

- `Yes` - Per impostare PayPal PayLater come annuncio
- `No` - Per impostare il credito PayPal per la pubblicità

#### Pubblicizza credito PayPal

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Advertise PayPal Credit]**.

   ![Pubblicizza credito PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Per ottenere le informazioni sul tuo account, fai clic su **[!UICONTROL Get Publisher ID from PayPal]** e segui le istruzioni.

1. Immetti **[!UICONTROL Publisher ID]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Home Page]**.

   ![Pubblicizza impostazioni home page credito PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Per inserire un banner nella pagina, impostare **[!UICONTROL Display]** su `Yes`.

1. Imposta **[!UICONTROL Position]** su uno dei seguenti:

   - `Header (center)`
   - `Sidebar (right)`

1. Imposta **[!UICONTROL Size]** su uno dei seguenti:

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) le sezioni rimanenti e ripetere i passaggi precedenti:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Pubblicizza PayPal PayLater

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Advertise PayPal PayLater]**.

1. Imposta **[!UICONTROL Enable PayPal PayLater]** su `Yes`.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Home Page]**.

   ![Pubblicizza impostazioni home page credito PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Per inserire un banner nella pagina, impostare **[!UICONTROL Display]** su `Yes`.

1. Imposta **[!UICONTROL Position]** su uno dei seguenti:

   - `Header (center)`
   - `Sidebar`

1. Imposta **[!UICONTROL Style Layout]** su uno dei seguenti:

   - `Text`
   - `Flex`

1. Solo per [!UICONTROL Style Layout] **[!UICONTROL Text]**, impostare **[!UICONTROL Logo Type]** su uno dei seguenti:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Solo per [!UICONTROL Style Layout] **[!UICONTROL Text]**, impostare **[!UICONTROL Logo Position]** su uno dei seguenti:

   - `Left`
   - `Right`
   - `Top`

1. Solo per [!UICONTROL Style Layout] **[!UICONTROL Text]**, impostare **[!UICONTROL Text Color]** su uno dei seguenti:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Solo per [!UICONTROL Style Layout] **[!UICONTROL Text]**, impostare **[!UICONTROL Text Size]** su uno dei seguenti:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Solo per [!UICONTROL Style Layout] **[!UICONTROL Flex]**, impostare **[!UICONTROL Ratio]** su uno dei seguenti:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Solo per [!UICONTROL Style Layout] **[!UICONTROL Flex]**, impostare **[!UICONTROL Color]** su uno dei seguenti:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) le sezioni rimanenti e ripetere i passaggi precedenti:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Passaggio 4: completare le impostazioni di base

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Basic Settings - PayPal Payments Pro]**.

   ![Impostazioni di base di PayPal Payment Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-basic-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi PayPal Payments Pro durante l&#39;estrazione.

   È consigliabile utilizzare il titolo _Carta di debito o carta di credito_.

1. Se si offrono più metodi di pagamento, immettere un numero per **[!UICONTROL Sort Order]** per determinare la sequenza di visualizzazione di PayPal Payments Pro quando viene elencato con altri metodi di pagamento durante l&#39;estrazione.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = primo, `1` = secondo, `2` = terzo e così via).

1. Imposta **[!UICONTROL Payment Action]** su uno dei seguenti:

   - `Authorization` - Approva l&#39;acquisto, ma blocca i fondi. L&#39;importo non viene prelevato finché non viene _acquisito_ dal commerciante.
   - `Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente ritirato dal conto cliente.

1. Per **[!UICONTROL Credit Card Settings]**, seleziona le carte di credito accettate per il pagamento nel tuo store.

   Per selezionare più schede, tenete premuto il tasto Ctrl (PC) o Comando (Mac) e fate clic su ciascuna scheda.

   >[!NOTE]
   >
   >American Express richiede un accordo aggiuntivo.

### Passaggio 5: completare le impostazioni avanzate

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Advanced Settings]**.

   ![Impostazioni avanzate di PayPal Payments Pro](./assets/paypal-payments-pro-advanced-settings.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Payment Applicable From]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del tuo negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco _[!UICONTROL Payment from Specific Countries]_. Tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e selezionare ogni paese nell&#39;elenco in cui i clienti possono effettuare acquisti dal negozio.

1. Per scrivere le comunicazioni con il sistema di pagamento nel file di registro, impostare **[!UICONTROL Debug Mode]** su `Yes`.

   >[!NOTE]
   >
   >In conformità agli standard di sicurezza dei dati PCI, le informazioni sulla carta di credito non vengono registrate nel file di registro.

1. Per abilitare la verifica dell&#39;autenticità host, impostare **[!UICONTROL Enable SSL Verification]** su `Yes`.

1. Per richiedere ai clienti di immettere un codice CVV, impostare **[!UICONTROL Require CVV Entry]** su `Yes`.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL CVV and AVS Settings]**.

1. Per determinare quando una transazione deve essere rifiutata quando il sistema di verifica degli indirizzi identifica una mancata corrispondenza, specificare come gestire ciascuno dei seguenti scenari:

   - Per rifiutare una transazione in base a una mancata corrispondenza delle strade, impostare **[!UICONTROL AVS Street Does Not Match]** su `Yes`.

   - Per rifiutare una transazione basata su un CAP non corrispondente, impostare **[!UICONTROL AVS Zip Does Not Match]** su `Yes`.

   - Per rifiutare una transazione basata su un identificatore di paese non corrispondente, impostare **[!UICONTROL International AVS Indicator Does Not Match]** su `Yes`.

   - Per rifiutare una transazione basata su un codice CVV non corrispondente, impostare **[!UICONTROL International Card Security Code Does Not Match]** su `Yes`.

   ![Impostazioni richieste di PayPal Payments Pro- CVV e AVS](./assets/paypal-payments-pro-cvv-avs-settings.png){width="600" zoomable="yes"}

1. Completa le seguenti sezioni, in base alle esigenze del tuo negozio:

   - [Impostazioni rapporto liquidazione](#settlement-report-settings)
   - [Impostazioni esperienza front-end](#frontend-experience-settings)

#### Impostazioni rapporto liquidazione

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Settlement Report Settings]**.

   ![Impostazioni report liquidazione PayPal](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL SFTP Credentials]**, eseguire le operazioni seguenti:

   - Se ti sei iscritto al server FTP protetto di PayPal, immetti le seguenti credenziali di accesso SFTP:

      - Login
      - Password

   - Per eseguire i rapporti sui test prima di iniziare a utilizzare Payments Pro sul sito, impostare **[!UICONTROL Sandbox Mode]** su `Yes`.

   - Immettere **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     Il valore predefinito è `reports.paypal.com`.

   - Immettere **[!UICONTROL Custom Path]** in cui salvare i report.

     Il valore predefinito è `/ppreports/outgoing`.

1. Per generare i report in base a una pianificazione, completare le impostazioni di **[!UICONTROL Scheduled Fetching]**:

   - Imposta **[!UICONTROL Enable Automatic Fetching]** su `Yes`.

   - Imposta **[!UICONTROL Schedule]** su uno dei seguenti:

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal conserva ogni rapporto per 45 giorni.

   - Impostare **[!UICONTROL Time of Day]** sull&#39;ora, il minuto e il secondo in cui si desidera generare i report.

#### Impostazioni esperienza front-end

Utilizza _[!UICONTROL Frontend Experience Settings]_per scegliere quali logo PayPal visualizzare sul tuo sito e per personalizzare l&#39;aspetto delle tue pagine di esercenti PayPal.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Frontend Experience Settings]**.

   ![Impostazioni esperienza front-end](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Seleziona **[!UICONTROL PayPal Product Logo]** che vuoi visualizzare nel blocco PayPal del tuo Negozio.

   I logo PayPal sono disponibili in quattro stili e due dimensioni:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Per personalizzare l&#39;aspetto delle pagine di PayPal per esercenti, eseguire le operazioni seguenti:

   - Immetti il nome di **[!UICONTROL Page Style]** che desideri applicare alle pagine dell&#39;esercente PayPal:

      - `paypal` - Utilizza lo stile di pagina PayPal.
      - `primary` - Utilizza lo stile di pagina identificato come _primario_ nel profilo dell&#39;account.
      - `your_custom_value` - Utilizza uno stile di pagina di pagamento personalizzato, specificato nel profilo del tuo account.

   - Per **[!UICONTROL Header Image URL]**, immettere l&#39;URL dell&#39;immagine che si desidera visualizzare nell&#39;angolo superiore sinistro della pagina di pagamento. La dimensione massima del file è di 750 pixel di larghezza per 90 pixel di altezza.

     >[!NOTE]
     >
     >PayPal consiglia che l&#39;immagine risieda su un server protetto (https). In caso contrario, un browser potrebbe segnalare che _la pagina contiene elementi protetti e non protetti_.

   - Per impostare il colore delle pagine, immettere il codice esadecimale a sei caratteri, senza il simbolo `#`, per ognuno dei seguenti elementi:

      - **[!UICONTROL Header Background Color]** - Colore di sfondo per l&#39;intestazione della pagina di pagamento.
      - **[!UICONTROL Header Border Color]** - Colore per il bordo di due pixel attorno all&#39;intestazione.
      - **[!UICONTROL Page Background Color]** - Colore di sfondo per la pagina di pagamento e attorno all&#39;intestazione e al modulo di pagamento.

### Passo 6: Completare le impostazioni di base per PayPal Express Checkout

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Basic Settings - PayPal Express Checkout]**.

   ![Impostazioni di base estrazione rapida](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi questo metodo di pagamento durante l&#39;estrazione.

   Si consiglia di impostare il titolo su _PayPal_ per ogni visualizzazione dello store.

1. Se si offrono più metodi di pagamento, immettere un numero per **[!UICONTROL Sort Order]** per determinare la sequenza di visualizzazione del Checkpoint PayPal Express elencato con gli altri metodi di pagamento.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = primo, `1` = secondo, `2` = terzo e così via).

1. Imposta **[!UICONTROL Payment Action]** su uno dei seguenti:

   - `Authorization` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato finché non viene _acquisito_ dal commerciante.
   - `Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente ritirato dal conto del cliente.

1. Per visualizzare il pulsante _[!UICONTROL Check out with PayPal]_nella pagina del prodotto, impostare **[!UICONTROL Display on Product Details Page]**su `Yes`.

### Passo 7: Completare le impostazioni avanzate per PayPal Express Checkout

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Advanced Settings]**.

   ![Impostazione avanzata estrazione rapida](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Display on Shopping Cart]** su `Yes`.

1. Imposta **[!UICONTROL Payment Applicable From]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del tuo negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco _[!UICONTROL Payment from Specific Countries]_. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ogni elemento.

1. Per scrivere le comunicazioni con il sistema di pagamento nel file di registro, impostare **[!UICONTROL Debug Mode]** su `Yes`.

   >[!NOTE]
   >
   >In conformità agli standard di sicurezza dei dati PCI, le informazioni sulla carta di credito non vengono registrate nel file di registro.

1. Per abilitare la verifica dell&#39;autenticità host, impostare **[!UICONTROL Enable SSL Verification]** su `Yes`.

1. Per visualizzare un riepilogo completo dell&#39;ordine cliente per voce dal sito PayPal, impostare **[!UICONTROL Transfer Cart Line Items]** su `Yes`.

1. Per consentire al cliente di completare la transazione dal sito PayPal senza tornare allo store per la revisione dell&#39;ordine, impostare **[!UICONTROL Skip Order Review Step]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/paypal-payments-pro/
