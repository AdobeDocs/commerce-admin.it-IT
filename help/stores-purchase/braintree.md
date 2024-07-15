---
title: Braintree
description: Scopri come impostare Braintree come soluzione di pagamento online nel tuo negozio.
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: fcd08ea5d8c3bd498eb4beae41bdf2f078a89f55
workflow-type: tm+mt
source-wordcount: '2625'
ht-degree: 0%

---

# Braintree

Braintree offre un’esperienza di pagamento completamente personalizzabile con rilevamento di frodi e integrazione PayPal. Supporta [!DNL Apple Pay], [!DNL Google Pay], ACH, Venmo e metodi di pagamento locali. Braintree riduce il carico di conformità PCI per gli esercenti perché la transazione avviene sul sistema Braintree. L&#39;integrazione Braintree Payments è stata sviluppata da [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/).

>[!NOTE]
>
>Se stai eseguendo l&#39;aggiornamento a 2.4.x da una versione precedente di Adobe Commerce o di un Magento Open Source con l&#39;estensione Braintree di Commerce Marketplace installata, consulta le [2.4 note sull&#39;aggiornamento](#24-upgrade-notes) alla fine di questa pagina.


## Passaggio 1: ottieni le credenziali Braintree

Vai a [Braintree pagamenti][1] e registrati per un account.

## Passaggio 2: completare le impostazioni di base

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

   - Se nell&#39;installazione di Commerce sono presenti più siti Web, store o visualizzazioni, nell&#39;angolo superiore sinistro scegliere **[!UICONTROL Store View]** in cui applicare la configurazione.

   - Nella sezione _[!UICONTROL Merchant Location]_verificare che **[!UICONTROL Merchant Country]**sia impostato sul percorso dell&#39;azienda.

1. In _[!UICONTROL Recommended Solutions]_, nella sezione_[!UICONTROL Braintree Payments] (di [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/) v4.6.1 - [Note sulla versione](https://support.gene.co.uk/support/solutions/articles/35000228529)_, fare clic su **[!UICONTROL Configure]**.

   ![Configura Braintree](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi Braintree come opzione di pagamento durante l&#39;estrazione.

1. Imposta **[!UICONTROL Environment]** operativo corrente per le transazioni Braintree su `Sandbox` o `Production`

   Durante il test della configurazione in una sandbox, utilizza solo [numeri di carta di credito][2] consigliati per Braintree. Quando si è pronti per passare alla produzione con Braintree, impostare **[!UICONTROL Environment]** su `Production`.

   ![Impostazioni credenziali di base](./assets/braintree-settings1.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Payment Action]** su uno dei seguenti:

   - `Authorize Only` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato dal conto bancario del cliente fino a quando la vendita non viene _acquisita_ dall&#39;esercente.|
   - `Intent Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente ritirato dal conto del cliente. **_Nota:_** questo valore era _Autorizza e acquisisci_ nelle versioni 2.3.x e precedenti.|

1. Immetti **[!UICONTROL Sandbox Merchant ID / Merchant ID]** dal tuo account di Braintree.

1. Immetti le seguenti credenziali dal tuo account di Braintree:

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >Sono presenti campi separati per gli ambienti **(Sandbox e Produzione)** e per gli altri campi il rendering dipende dall&#39;ambiente selezionato.

1. Prima di salvare la configurazione, fare clic su **[!UICONTROL Validate Credentials]** per convalidare le credenziali.

1. Imposta **[!UICONTROL Enable Card Payments]** su `Yes`.

   ![Impostazioni di base](./assets/braintree-settings2.png){width="600" zoomable="yes"}

   Se si desidera poter archiviare le informazioni dei clienti in modo sicuro, in modo che i clienti non debbano reinserirle ogni volta che effettuano un acquisto, impostare **[!UICONTROL Enable Vault for Card Payments]** su `Yes`.

## Passaggio 3: completare le impostazioni avanzate

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Advanced Braintree Settings]**.

   ![Impostazioni avanzate](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. Per **[!UICONTROL Vault Title]**, immettere un titolo descrittivo per il riferimento che identifichi l&#39;insieme di credenziali in cui sono memorizzate le informazioni della scheda cliente.

1. Immetti **[!UICONTROL Merchant Account ID]** dal tuo account di Braintree.

   Se non si specifica il conto esercente da utilizzare, Braintree elabora la transazione utilizzando il proprio conto esercente predefinito.

1. Per fornire un&#39;esperienza di pagamento più rapida con le opzioni di pagamento rapido all&#39;inizio del processo di pagamento, inclusi PayPal, PayLater, Apple Pay e Google Pay, impostare **[!UICONTROL Enable Checkout Express Payments]** su `Yes`.

1. Se si desidera impedire l&#39;invio della transazione per la valutazione come parte dei controlli degli strumenti fraudolenti avanzati, negli ordini inoltrati tramite l&#39;amministratore, impostare **[!UICONTROL Skip Fraud Checks on Admin Orders]** su `Yes`.

1. Impostare **[!UICONTROL Bypass Fraud Protection Threshold]** in modo che i controlli `Advanced Fraud Protection` vengano ignorati quando la soglia viene raggiunta o superata.

   Se si lascia vuoto questo campo, questa opzione viene disabilitata.

1. Se si desidera che venga salvato un file di registro delle interazioni tra l&#39;archivio e Braintree, impostare **[!UICONTROL Debug]** su `Yes`.

1. Per richiedere ai clienti di fornire il codice di sicurezza a tre cifre dal retro di una carta di credito, impostare **[!UICONTROL CVV Verification]** su `Yes`.

   Se utilizzi la verifica CVV, assicurati di abilitare AVS e/o CVV nella sezione _Impostazioni/Elaborazione_ del tuo account di Braintree.

1. Per inviare gli elementi riga carrello per tutti i metodi di pagamento, impostare **[!UICONTROL Send Card Line Items]** su `Yes`.

1. Per **[!UICONTROL Credit Card Types]**, selezionare ogni carta di credito accettata dal tuo Negozio come pagamento tramite Braintree.

   Per selezionare più tipi di schede, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza di visualizzazione della Braintree quando questa viene elencata con altri metodi di pagamento durante l&#39;estrazione.

## Passaggio 4: completare le impostazioni del webhook di Braintree

![Braintree impostazioni webhook](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. Impostare **[!UICONTROL Enable Webhook]** su `Yes` per abilitare la funzionalità webhook per la protezione dalle frodi, i pagamenti ACH e i metodi di pagamento locali.

1. Copia l&#39;URL nel campo **[!UICONTROL Fraud Protection URL]** e aggiungilo al tuo account di Braintree come _[!UICONTROL Webhook Destination URL]_.

   >[!IMPORTANT]
   >
   >Questo URL deve essere sicuro e accessibile al pubblico.

1. Impostare il campo **[!UICONTROL Fraud Protection Approve Order Status]** per determinare quando la protezione antifrode viene approvata dalla Braintree.

   Lo stato dell&#39;ordine selezionato viene assegnato all&#39;ordine Commerce.

1. Impostare il campo **[!UICONTROL Fraud Protection Reject Order Status]** per determinare quando la protezione contro le frodi viene rifiutata dalla Braintree.

   Lo stato dell&#39;ordine selezionato viene assegnato all&#39;ordine Commerce.

## Passaggio 5: completare le impostazioni specifiche del paese

1. Imposta **[!UICONTROL Payment from Applicable Countries]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del tuo negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco _[!UICONTROL Payment from Specific Countries]_. Tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e selezionare ogni paese nell&#39;elenco in cui i clienti possono effettuare acquisti dal negozio.

   ![Impostazioni specifiche per paese](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. Per impostare **[!UICONTROL Country Specific Credit Card Types]**:

   - Fare clic su **[!UICONTROL Add]**.

   - Imposta **[!UICONTROL Country]** e scegli ogni **[!UICONTROL Allowed Credit Card Type]**.

   - Ripetere l&#39;operazione per identificare le carte di credito accettate da ciascun paese.

## Passaggio 6: completare l&#39;ACH tramite le impostazioni delle Braintree

![ACH tramite Braintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. Per includere ACH come opzione di pagamento con Braintree, impostare **[!UICONTROL Enable ACH Direct Debit]** su `Yes`.

1. I clienti possono archiviare il metodo di pagamento con Addebito automatico sul conto bancario (ACH Direct Debit) monouso e memorizzarlo per utilizzarlo in futuro. Una volta eseguito il vaulting, i clienti possono riutilizzare l&#39;Addebito automatico sul conto bancario senza dover reimmettere o autenticare le informazioni di pagamento se impostato su `Yes`.**[!UICONTROL Enable Vault for ACH Direct Debit]**

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui viene visualizzata l&#39;opzione di pagamento Braintree ACH quando elencata con altre opzioni di pagamento durante l&#39;estrazione.

## Passaggio 7: completare [!UICONTROL Apple Pay] tramite le impostazioni di Braintree

![ApplePay tramite impostazioni Braintree](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. Per includere [!DNL Apple Pay] come opzione di pagamento con Braintree, impostare **[!UICONTROL Enable ApplePay through Braintree]** su `Yes`.

   Assicurati di [verificare prima il nome di dominio](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) nell&#39;account di Braintree.

1. Se desideri poter archiviare le informazioni dei clienti in modo sicuro, in modo che i clienti non debbano reinserirle ogni volta che effettuano un acquisto con Apple Pay, imposta **[!UICONTROL Enable Vault for ApplePay]** su `Yes`.

1. Imposta **[!UICONTROL Payment Action]** su uno dei seguenti:

   - `Authorize Only` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato dal conto bancario del cliente finché la vendita non viene _acquisita_ dal commerciante.
   - `Intent Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente ritirato dal conto del cliente.

1. Per **[!UICONTROL Merchant Name]**, immettere il testo che specifica l&#39;etichetta visualizzata ai clienti nella finestra di dialogo Apple Pay.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui viene visualizzata l&#39;opzione di pagamento [!DNL Apple Pay] quando elencata con altre opzioni di pagamento durante l&#39;estrazione.

## Passo 8: Completare le impostazioni per i metodi di pagamento locali

1. Per includere i metodi di pagamento locali come opzione di pagamento con Braintree, impostare **[!UICONTROL Enable Local Payment Methods]** su `Yes`.

1. Per **[!UICONTROL Title]**, immettere il testo da utilizzare per l&#39;etichetta visualizzata nella sezione relativa al metodo di pagamento dell&#39;estrazione (valore predefinito: `Local Payments`).

1. Per **[!UICONTROL Fallback Button Text]**, immettere il testo da utilizzare per il pulsante visualizzato nella pagina Braintree di fallback per riportare il cliente al sito Web (ad esempio, `Complete Checkout`).

1. Per **[!UICONTROL Redirect on Fail]**, immettere l&#39;URL in cui i clienti devono essere reindirizzati quando le transazioni del metodo di pagamento locale vengono annullate, non riuscite o rilevano errori. Deve essere la pagina di pagamento per l&#39;estrazione, ad esempio `https://www.domain.com/checkout#payment`.

1. Per **[!UICONTROL Allowed Payment Methods]**, selezionare il metodo di pagamento locale da abilitare.

   Opzioni: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (non ancora supportato)

   ![Impostazioni dei metodi di pagamento locali](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >L&#39;estensione Braintree nel pacchetto non supporta tutti i metodi di pagamento locali elencati nella [documentazione per gli sviluppatori Braintree](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Sono in fase di sviluppo altri metodi di pagamento locali, che saranno supportati nelle prossime versioni.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui viene visualizzato il metodo di pagamento locale quando viene elencato con altre opzioni di pagamento durante l&#39;estrazione.

## Passaggio 9: completare [!DNL Google Pay] tramite le impostazioni di Braintree

![Pagamento Google tramite Braintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. Per includere [!DNL Google Pay] come opzione di pagamento con Braintree, impostare **[!UICONTROL Enable GooglePay Through Braintree]** su `Yes`.

1. Se desideri poter archiviare le informazioni dei clienti in modo sicuro, in modo che i clienti non debbano reinserirle ogni volta che effettuano un acquisto con Google Pay, imposta **[!UICONTROL Enable Vault for GooglePay]** su `Yes`.

1. Imposta **[!UICONTROL Payment Action]** su uno dei seguenti:

   - `Authorize Only` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato dal conto bancario del cliente finché la vendita non viene _acquisita_ dal commerciante.
   - `Intent Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente ritirato dal conto del cliente.

1. Impostare **[!UICONTROL Button Color]** per determinare il colore del pulsante [!DNL Google Pay]: `White` o `Black`

1. Per **[!UICONTROL Merchant ID]**, immetti il tuo ID commerciante (fornito da Google).

1. Per **[!UICONTROL Accepted Cards]**, selezionare il tipo di schede che un cliente può utilizzare per effettuare un ordine utilizzando [!DNL Google Pay].

   Opzioni: `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui [!DNL Google Pay] viene visualizzato quando elencato con altre opzioni di pagamento durante l&#39;estrazione.

## Passaggio 10: Completare le impostazioni di Braintree di Venmo through

1. Per includere Venmo come opzione di pagamento con Braintree, impostare **[!UICONTROL Enable Venmo through Braintree]** su `Yes`.

1. Impostare **[!UICONTROL Enable Vault for Venmo]** su `Yes` per consentire l&#39;utilizzo di un archivio protetto per archiviare l&#39;account Venmo dei clienti in modo che non sia necessario accedere nuovamente al proprio account Venmo per le transazioni future.

   ![Venmo attraverso Braintree](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Payment Action]** su uno dei seguenti:

   - `Authorize Only` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato dal conto bancario del cliente finché la vendita non viene _acquisita_ dal commerciante.
   - `Intent Sale` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente ritirato dal conto del cliente.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui viene visualizzato Venmo quando viene elencato con altre opzioni di pagamento durante l&#39;estrazione.

## Passo 11: Completare PayPal attraverso le impostazioni di Braintree

![PayPal tramite impostazioni Braintree](./assets/braintree-paypal.png){width="550" zoomable="yes"}

1. Per includere PayPal come opzione di pagamento con Braintree, impostare **[!UICONTROL Enable PayPal through Braintree]** su `Yes`.

1. Specifica il metodo di pagamento PayPal tramite Braintree:

   >[!NOTE]
   >
   >È possibile abilitare **[!DNL PayPal Credit]** o **[!DNL PayPal PayLater]**. Entrambi i metodi non possono essere attivati contemporaneamente.

   - Per includere [!DNL PayPal Credit] come opzione di pagamento con Braintree, impostare **[!UICONTROL Enable PayPal Credit through Braintree]** su `Yes`.

     Quando **Abilita PayPal tramite Braintree** è impostato su `Yes`, viene visualizzato solo questo campo.

     >[!NOTE]
     >
     >PayPal Credit è disponibile solo negli Stati Uniti e nel Regno Unito. Il credito PayPal è disabilitato se il valore selezionato per il campo _[!UICONTROL Merchant Country]_non è `US` o `UK`.

   - Per includere [!DNL PayPal PayLater] come opzione di pagamento con Braintree, impostare **[!UICONTROL Enable PayPal PayLater through Braintree]** su `Yes`.

     Quando **[!UICONTROL Enable PayPal PayLater through Braintree]** è impostato su `Yes`, viene visualizzato solo questo campo.

     Puoi visualizzare sul tuo sito i messaggi PayLater per le offerte, ad esempio _Paga in 3_, che consente ai clienti di pagare con tre pagamenti mensili senza interessi. L’integrazione Braintree può visualizzare messaggi sul sito per promuovere questa funzione. Non puoi promuovere le offerte PayLater con altri contenuti, materiale di marketing o materiale.

1. Per **[!UICONTROL Title]**, inserisci un titolo che identifichi il pagamento Braintree tramite PayPal durante l&#39;acquisto.

1. Imposta **[!UICONTROL Vault Enabled]** su `Yes` per abilitare l&#39;utilizzo di un insieme di credenziali protetto per archiviare il conto PayPal dei clienti. Il conto PayPal archiviato può essere utilizzato per transazioni future, riducendo il numero di passaggi per i clienti.

1. Imposta **[!UICONTROL Send Cart Line Items for PayPal]** su `Yes` per inviare gli articoli della linea (articoli dell&#39;ordine) a PayPal insieme a Biglietti regalo, Confezione regalo per gli articoli, Confezione regalo per l&#39;ordine, Credito del Negozio, Spedizione e Imposta come articoli della linea.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui viene visualizzata l&#39;opzione di pagamento Braintree PayPal quando elencata con altre opzioni di pagamento durante l&#39;estrazione.

1. Per visualizzare il nome dell&#39;esercente in modo diverso da quello definito nella [configurazione archivio](../getting-started/store-details.md#store-information), immettere il nome nel campo **[!UICONTROL Override Merchant Name]** come si desidera visualizzarlo.

1. Imposta **[!UICONTROL Payment Action]** su uno dei seguenti:

   - `Authorize Only` - Approva l&#39;acquisto e blocca i fondi. L&#39;importo non viene prelevato dal conto bancario del cliente finché la vendita non viene _acquisita_ dal commerciante.
   - `Authorize and Capture` - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente ritirato dal conto del cliente.

1. Imposta **[!UICONTROL Payment from Applicable Countries]** su uno dei seguenti per le transazioni Braintree elaborate da PayPal:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del tuo negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco _[!UICONTROL Payment from Specific Countries]_. Tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e selezionare ogni paese nell&#39;elenco in cui i clienti possono effettuare acquisti dal negozio.

1. Per richiedere ai clienti di fornire un indirizzo di fatturazione, impostare **[!UICONTROL Require Customer's Billing Address]** su `Yes`.

   >[!NOTE]
   >
   >Questa funzione deve essere abilitata per il tuo account dal Supporto tecnico PayPal.

1. Per salvare un file di registro delle interazioni tra il tuo store e PayPal tramite Braintree, imposta **[!UICONTROL Debug]** su `Yes`.

1. Per visualizzare il pulsante PayPal sia sul mini carrello che sulla pagina del carrello, impostare **[!UICONTROL Display on Shopping Cart]** su `Yes`.

## Passaggio 12: impostazione degli stili

1. Per **[!UICONTROL Location]**, scegli dove vengono visualizzati i pulsanti e i messaggi PayPal: `Mini-Cart and Cart Page`, `Checkout Page` o `Product Page`

   ![Impostazioni stile PayPal](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

Le opzioni e le impostazioni di questa sezione variano a seconda dell&#39;impostazione nel campo _[!UICONTROL Location]_.

1. Imposta **[!UICONTROL PayPal Button Type]** su uno dei tre tipi di pulsanti: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

Le opzioni e le impostazioni di questa sezione variano a seconda del tipo di pulsante selezionato nel campo _[!UICONTROL PayPal Button Type]_.

1. Per visualizzare il pulsante PayPal sulla vetrina nella posizione selezionata, impostare **[!UICONTROL Show PayPal Button]** su `Yes`.

1. Per **[!UICONTROL Button Label]**, seleziona l&#39;etichetta del pulsante PayPal: `Paypal`, `Checkout`, `Buynow` o `Pay`

1. Per **[!UICONTROL Color]**, selezionare il colore del pulsante PayPal: `Blue`, `Black`, `Gold` o `Silver`

1. Per **[!UICONTROL Shape]**, selezionare la forma pulsante PayPal: `Pill` o `Rectangle`

1. Per **[!UICONTROL Size (Deprecated)]**, selezionare la dimensione del pulsante PayPal: `Medium`, `Large` o `Responsive`

>[!NOTE]
>
>Il campo di configurazione **[!DNL Size(Deprecated)]** è obsoleto e non viene utilizzato per assegnare uno stile ai pulsanti PayPal.

**[!UICONTROL PayLater Messaging]**

1. Per visualizzare i messaggi di [!DNL PayLater] nella vetrina nel percorso selezionato, impostare **[!UICONTROL Show PayLater Messaging]** su `Yes`.

   Questo messaggio include la visualizzazione di [!DNL PayLater] messaggi per le offerte disponibili ([restrizioni applicate](https://developer.paypal.com/docs/checkout/pay-later/us/)).

1. Per **[!UICONTROL Message Layout]**, selezionare il layout del messaggio [!DNL PayLater]: `Text` o `Flex`

1. Per **[!UICONTROL Logo]**, seleziona il tipo di logo PayPal: `Inline`, `Primary`, `Alternative` o `None`

1. Per **[!UICONTROL Logo Position]**, seleziona la posizione del logo PayPal: `Left`, `Right` o `Top`

1. Per **[!UICONTROL Text Color]**, selezionare il colore del testo del messaggio [!DNL PayLater]: `Black`, `White`, `Monochrome` o `Grayscale`

Quando queste opzioni sono impostate, puoi visualizzare l&#39;anteprima dei pulsanti PayPal e dei messaggi PayLater. Esistono controlli che è possibile utilizzare per applicare le impostazioni o reimpostare i valori:

- Per memorizzare le impostazioni di stile selezionate per i pulsanti e i messaggi PayLater e applicarle alla posizione corrente e al tipo di pulsante corrente, fare clic su **[!UICONTROL Apply]**.

- per memorizzare le impostazioni di stile selezionate per i pulsanti e i valori di messaggistica PayLater e applicarle a tutti i tipi di pulsanti e le posizioni, fare clic su **[!UICONTROL Apply to All Buttons]**.

- Per ripristinare i valori predefiniti consigliati per i pulsanti e i messaggi PayLater e applicarli a tutti i tipi di pulsanti e le posizioni, fare clic su **[!UICONTROL Reset to Recommended Defaults]**.

## Passaggio 13: completare le impostazioni di verifica 3D

1. Se si desidera aggiungere un passaggio di verifica per i clienti che utilizzano carte di credito registrate in un programma di verifica, ad esempio _Verified by VISA_, impostare **[!UICONTROL 3D Secure Verification]** su `Yes`.

   Durante il processo, l&#39;importo della transazione sottomesso per la verifica viene confrontato con l&#39;importo inviato per l&#39;autorizzazione.

2. Per soddisfare sempre la richiesta 3D Secure per tutte le transazioni, impostare **[!UICONTROL Always request 3DS]** su `Yes`.

3. Per **[!UICONTROL Threshold Amount]**, immettere l&#39;importo minimo dell&#39;ordine necessario per attivare la verifica 3D.

4. Imposta **[!UICONTROL Verify for Applicable Countries]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del tuo negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco _[!UICONTROL Verify for Specific Countries]_. Tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e selezionare ogni paese nell&#39;elenco in cui i clienti possono effettuare acquisti dal negozio.

   ![Impostazioni di verifica 3D](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## Passaggio 14: configurare i descrittori dinamici Braintree

I seguenti descrittori vengono utilizzati per identificare gli acquisti sugli estratti conto della carta di credito del cliente. Puoi ridurre il numero di chargeback identificando chiaramente l’azienda associata a ogni acquisto. Se i descrittori dinamici non sono abilitati per il tuo account, contatta il supporto Braintree.

![Descrittori dinamici](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. Immettere il descrittore dinamico per **[!UICONTROL Name]**, **[!UICONTROL Phone]** e **[!UICONTROL URL]** in base alle seguenti linee guida:

   - **[!UICONTROL Name]** - Il descrittore del nome è composto da due parti separate da un asterisco (*). Ad esempio:

     `company*myproduct`

     La prima parte del descrittore identifica l’azienda o il DBA e la seconda parte identifica il prodotto. La lunghezza delle parti `company` e `product` del descrittore può essere allocata nei modi seguenti, per una lunghezza combinata fino a 22 caratteri.

     **_Caratteri nel descrittore del nome_**

     _Opzione 1:_ `Company` deve essere di tre caratteri, `Product` può contenere fino a 18 caratteri

     _Opzione 2:_ `Company` deve essere composto da sette caratteri, `Product` da un massimo di 14 caratteri

     _Opzione 3_: `Company` deve essere di 12 caratteri, `Product` può contenere fino a nove caratteri

   - **[!UICONTROL Phone]** - La lunghezza del descrittore telefonico deve essere compresa tra 10 e 14 caratteri e può includere solo numeri, trattini, parentesi e punti. Ad esempio:

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - Il descrittore URL rappresenta il nome di dominio e può contenere fino a 13 caratteri. Ad esempio:

     `company.com`

1. Al termine della configurazione di Braintree, fare clic su **[!UICONTROL Save Config]**.

## Note sull’aggiornamento 2.4

A partire da Adobe Commerce e dal Magento Open Source 2.4.0, l’estensione Braintree è inclusa nella versione. Se si esegue la migrazione a Commerce 2.4.x da una versione precedente alla 2.4.0 in cui è installata l&#39;estensione Marketplace Braintree, è necessario disinstallare tale estensione (`paypal/module-braintree` o `gene/module-braintree`) e aggiornare le personalizzazioni del codice per utilizzare lo spazio dei nomi `PayPal_Braintree` anziché `Magento_Braintree`. Le impostazioni di configurazione dell&#39;estensione del bundle Commerce Braintree Payments di base e dell&#39;estensione distribuita su Commerce Marketplace persistono e i pagamenti effettuati con le versioni precedenti possono ancora essere acquisiti, annullati o rimborsati come di consueto.

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
