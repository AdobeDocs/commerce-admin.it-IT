---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods] dell'amministratore di Commerce.
exl-id: 159b76a8-3676-4692-9cd6-18947bda4666
feature: Configuration, Shipping/Delivery
source-git-commit: d1e919d9025c3609e0512f26d563cebae325ca0b
workflow-type: tm+mt
source-wordcount: '4160'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Delivery Methods]

{{config}}

## [!UICONTROL Basic Delivery Methods]

### [!UICONTROL Flat Rate]

![Tariffa fissa](./assets/delivery-methods-flat-rate.png)<!-- zoom -->

<!-- [Flat Rate](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-flat-rate) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sito Web | Se attivato, l&#39;opzione Tariffa fissa viene visualizzata nella sezione _Stima spese di spedizione e imposte_ del carrello e nella sezione _Spedizione_ durante il pagamento. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Nome utilizzato per questo metodo di spedizione durante il pagamento. |
| [!UICONTROL Method Name] | Visualizzazione store | Nome che descrive il metodo di calcolo utilizzato per produrre una stima di spedizione. Il nome del metodo viene visualizzato accanto alla tariffa stimata calcolata nel carrello. Il valore predefinito è `Fixed`. |
| [!UICONTROL Type] | Sito Web | Descrive il tipo di calcolo utilizzato per determinare la tariffa fissa. Opzioni: <br/>**`None`**- Nessun calcolo utilizzato. Imposta la tariffa fissa su zero, che equivale alla spedizione gratuita.<br/>**`Per Order`** - Addebita una singola tariffa fissa per l&#39;intero ordine. <br/>**`Per Item`**- Addebita una tariffa forfettaria separata per ogni elemento del carrello. Il tasso viene moltiplicato per il numero di articoli nel carrello, anche se la quantità totale include una combinazione di articoli diversi. |
| [!UICONTROL Price] | Sito Web | Il prezzo applicato al cliente per la spedizione a tariffa fissa. |
| [!UICONTROL Calculate Handling Fee] | Sito Web | Determina la modalità di calcolo della commissione di gestione, se inclusa. Opzioni: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Sito Web | Immettere l&#39;importo da addebitare per una commissione di gestione, in base al metodo scelto per calcolare l&#39;importo. Ad esempio, se l&#39;addebito è basato su un addebito fisso, immettere l&#39;importo come decimale, ad esempio 4,90. Tuttavia, se la commissione di gestione si basa su una percentuale dell&#39;ordine, immettere l&#39;importo come percentuale. Ad esempio, se si sta addebitando il 6% dell&#39;ordine, immettere il valore come `.06`. |
| [!UICONTROL Displayed Error Message] | Visualizzazione store | Messaggio visualizzato se un cliente sceglie il metodo Tasso fisso, ma per qualche motivo il metodo non è disponibile. |
| [!UICONTROL Ship to Applicable Countries] | Sito Web | Identifica i paesi in cui offri la spedizione a tariffa fissa. Opzioni: <br/>**`All Allowed Countries`**- I clienti di qualsiasi paese specificato nella configurazione del punto vendita possono utilizzare la spedizione a tariffa fissa.<br/>**`Specific Countries`** - Solo i clienti di determinati paesi possono utilizzare la spedizione a tariffa fissa. |
| [!UICONTROL Ship to Specific Countries] | Sito Web | Identifica ogni paese in cui i clienti possono utilizzare la spedizione a tariffa fissa. |
| [!UICONTROL Show Method if Not Applicable] | Sito Web | Determina se la tariffa fissa viene visualizzata come opzione durante il pagamento se il metodo non è applicabile all&#39;acquisto. Opzioni: `Yes` / `No` |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione della tariffa fissa quando viene elencata con altri metodi di consegna durante il pagamento. |

{style="table-layout:auto"}

### [!UICONTROL Free Shipping]

![Spedizione gratuita](./assets/delivery-methods-free-shipping.png)<!-- zoom -->

<!-- [Free Shipping](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-free) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sito Web | Quando questa opzione è abilitata, la Spedizione gratuita viene visualizzata come opzione nella sezione Spedizione durante il pagamento. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Nome utilizzato per questo metodo di spedizione durante il pagamento. |
| Nome metodo | Visualizzazione store | Nome che descrive il metodo di calcolo utilizzato per produrre una stima di spedizione. Il nome del metodo viene visualizzato accanto alla tariffa stimata calcolata nel carrello. Il valore predefinito è `Free`. |
| Importo minimo ordine | Sito Web | L&#39;acquisto minimo necessario per applicare la Spedizione gratuita a un ordine. |
| Includi imposta in importo | Sito Web | Determina se l&#39;imposta è inclusa nel calcolo dell&#39;importo ordine minimo. Opzioni: <br/>**Sì** - L&#39;imposta è inclusa nel calcolo dell&#39;importo minimo dell&#39;ordine (Subtotale + Imposta - Sconto).<br/>**No** - L&#39;imposta non è inclusa nel calcolo dell&#39;importo minimo dell&#39;ordine (Subtotale - Sconto). |
| Messaggio di errore visualizzato | Visualizzazione store | Messaggio visualizzato se un cliente sceglie la spedizione gratuita, ma per qualche motivo il metodo non è disponibile. |
| Spedisci a paesi applicabili | Sito Web | Identifica i paesi in cui offri la spedizione gratuita. Opzioni: <br/>**Tutti i paesi consentiti** - I clienti di qualsiasi paese specificato nella configurazione del negozio possono utilizzare la spedizione gratuita. <br/>**Paesi specifici** - Solo i clienti di paesi specifici possono utilizzare la Spedizione gratuita. |
| Spedisci a paesi specifici | Sito Web | Identifica ogni paese in cui i clienti possono utilizzare la Spedizione gratuita. |
| Mostra metodo se non applicabile | Sito Web | Determina se la Spedizione gratuita viene visualizzata come opzione durante il pagamento se il metodo non è applicabile all&#39;acquisto. Opzioni: `Yes` / `No` |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione di Spedizione gratuita quando viene elencato con altri metodi di consegna durante il pagamento. |

{style="table-layout:auto"}

### [!UICONTROL Table Rates]

![Tariffe tabella](./assets/delivery-methods-table-rates.png)<!-- zoom -->

<!-- [Table Rates](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-table-rate) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sito Web | Quando questa opzione è abilitata, l&#39;opzione Tassi tabella viene visualizzata nella sezione Stima spedizione e imposte del carrello e nella sezione Spedizione durante il pagamento. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Nome utilizzato per questo metodo di spedizione durante il pagamento. |
| Nome metodo | Visualizzazione store | Nome che descrive il metodo di calcolo utilizzato per produrre una stima di spedizione. Il nome del metodo viene visualizzato accanto alla tariffa stimata calcolata nel carrello. Il valore predefinito è `Table Rate`. |
| [!UICONTROL Condition] | Sito Web | Determina la condizione su cui si basa il calcolo. Il formato del file CSV caricato è specifico per ogni condizione. Opzioni: `Weight vs. Destination` / `Price vs. Destination` / `# of Items vs. Destination` |
| [!UICONTROL Include Virtual Products in Price Calculation] | Sito Web | Determina se i prodotti virtuali, che non richiedono la spedizione, sono inclusi nei calcoli del prezzo Tasso tabella. |
| [!UICONTROL Calculate Handling Fee] | Sito Web | Determina la modalità di calcolo della commissione di gestione, se inclusa. Opzioni: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Sito Web | L&#39;importo di qualsiasi tariffa aggiunta alle spese di spedizione per coprire le spese di gestione della spedizione. Immetti il valore come decimale. Ad esempio, se la tariffa è basata su una percentuale, immettere 0,06 anziché 6 %. Per un importo fisso, immettere `6.00`. |
| [!UICONTROL Displayed Error Message] | Visualizzazione store | Messaggio visualizzato se un cliente sceglie Tassi tabella, ma per qualche motivo il metodo non è disponibile. |
| [!UICONTROL Ship to Applicable Countries] | Sito Web | Identifica i paesi in cui offri la spedizione tramite Tasso tabella. Opzioni: <br/>**`All Allowed Countries`**- I clienti di qualsiasi paese specificato nella configurazione del punto vendita possono utilizzare la spedizione basata su tariffa tabella.<br/>**`Specific Countries`** - Solo i clienti di paesi specifici possono utilizzare la spedizione basata su tariffa tabella. |
| [!UICONTROL Ship to Specific Countries] | Sito Web | Identifica ogni paese in cui i clienti possono utilizzare la spedizione basata su tariffa tabella. |
| [!UICONTROL Show Method if Not Applicable] | Sito Web | Determina se i tassi tabella vengono visualizzati come opzione durante il pagamento se il metodo non è applicabile all&#39;acquisto. Opzioni: `Yes` / `No` |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione dei tassi tabella quando vengono elencati con altri metodi di consegna durante il pagamento. |

{style="table-layout:auto"}

### [!UICONTROL In-Store Delivery]

![Consegna in-store](./assets/delivery-methods-in-store-delivery.png)<!-- zoom -->

<!-- [In-Store Delivery](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/basic-methods/shipping-in-store-delivery) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sito Web | Se abilitata, la consegna in negozio può essere visualizzata come opzione nella sezione _Stima spedizione e imposte_ del carrello e nella sezione _Spedizione_ durante il pagamento. Opzioni: `Yes` / `No` |
| [!UICONTROL Method Name] | Visualizzazione store | Nome che identifica la funzione di prelievo in negozio come metodo di spedizione. Questo valore viene visualizzato come etichetta di una scheda nella parte superiore della pagina Pagamento spedizione e nella tabella dei metodi di spedizione disponibili nella parte inferiore della stessa pagina. Il valore predefinito è `In-store Delivery`. |
| [!UICONTROL Title] | Visualizzazione store | Nome utilizzato per questo metodo di spedizione durante il pagamento. |
| [!UICONTROL Price] | Sito Web | Il prezzo addebitato al cliente per un prelievo in negozio. |
| [!UICONTROL Search Radius] | Sito Web | Raggio, in km, da utilizzare per la ricerca delle posizioni di prelievo. |
| [!UICONTROL Displayed Error Message] | Visualizzazione store | Messaggio visualizzato quando un cliente seleziona un prelievo in-store, ma il metodo di consegna non è disponibile. |

{style="table-layout:auto"}

## [!UICONTROL Carriers]

### [!UICONTROL UPS]

{{ups-api}}

![Impostazioni account REST UPS](./assets/delivery-methods-ups1.png)<!-- zoom -->

![Impostazioni account XML UPS](./assets/delivery-methods-ups1.png)<!-- zoom -->

<!-- [UPS REST Account Settings]https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled for Checkout] | Sito Web | Determina se UPS è disponibile per i clienti come metodo di spedizione durante il pagamento. Opzioni: `Yes` / `No` |
| [!UICONTROL Enabled for RMA] | Sito Web | Determina se UPS è disponibile per i clienti come metodo di spedizione per un RMA. Opzioni: `Yes` / `No` |
| _[!UICONTROL UPS Account Settings]_ |  |  |
| [!UICONTROL Live Account] | Visualizzazione store | Specifica che l&#39;account United Parcel Service è attivo. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Nome utilizzato per questo metodo di spedizione durante il pagamento. |
| _[!UICONTROL UPS REST Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Sito Web | Per il servizio REST UPS, visualizza i seguenti URL necessari per la trasmissione dei dati JSON: URL gateway, URL di tracciamento, URL di spedizione. Utilizza endpoint sandbox o di produzione in base all’impostazione dell’account live. |
| [!UICONTROL Mode] | Sito Web | Determina la modalità di trasmissione utilizzata per i dati inviati al sistema UPS. Opzioni: <br/>**`Development`**- UPS non verifica che i dati ricevuti dal server Commerce vengano inviati tramite SSL.<br/>**`Live`** - UPS verifica che i dati ricevuti dal server Commerce vengano inviati tramite un livello di socket sicuro (SSL). |
| ID utente | Sito Web | ID client dell&#39;account di spedizione UPS. |
| [!UICONTROL Origin of the Shipment] | Sito Web | (Solo REST UPS) Il paese o l&#39;area geografica di origine della spedizione del prodotto. |
| [!UICONTROL Password] | Visualizzazione store | Segreto client dell&#39;account di spedizione UPS. |

{style="table-layout:auto"}

![Informazioni sul pacchetto UPS](./assets/delivery-methods-ups-packaging-settings.png)<!-- zoom -->

<!-- [UPS Package Information]https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL UPS Negotiated Rate Settings]_ |  |  |
| [!UICONTROL Enable Negotiated Rates] | Sito Web | (Solo UPS REST) Attiva/disattiva tariffe speciali, in base al contratto con UPS. Opzioni: `Yes` / `No` |
| [!UICONTROL Packages Request Type] | Sito Web | Determina la modalità di calcolo del peso per le spedizioni con più colli. Opzioni: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Shipper Number] | Sito Web | (Solo UPS REST) Il numero di spedizione UPS di sei caratteri è necessario per il riferimento per utilizzare le tariffe negoziate. |
| [!UICONTROL Container] | Sito Web | Imposta il tipo di contenitore utilizzato per imballare le spedizioni. Opzioni: `Customer Packaging` / `UPS Letter Envelope` / `Customer Packaging` / `UPS Letter Envelope` / `UPS Tube` / `UPS Express Box` / `UPS Worldwide 25 kilo` / `UPS Worldwide 10 kilo` |
| [!UICONTROL Weight Unit] | Sito Web | Imposta l&#39;unità di misura predefinita per il peso del prodotto nel punto vendita. Per ulteriori informazioni, vedere [Peso dimensionale](../../stores-purchase/carriers.md#dimensional-weight). |
| [!UICONTROL Tracking URL] | Sito Web | (Solo REST UPS) URL del gruppo di continuità utilizzato per tenere traccia dei pacchetti. Utilizza `https://onlinetools.ups.com/api/track` per la produzione OPPURE `https://wwwcie.ups.com/api/track` per la configurazione della sandbox. |
| [!UICONTROL Destination Type] | Sito Web | Imposta il tipo di destinazione di spedizione predefinito. Opzioni: `Business` / `Residential` |
| [!UICONTROL Maximum Package Weight] | Sito Web | Imposta il peso massimo che un pacchetto può avere come specificato da UPS. Se i prodotti ordinati superano il peso massimo del pacchetto, questa opzione di spedizione non è disponibile. In base a [UPS.com](https://www.ups.com/us/en/global.page), i pacchetti non possono superare i 70 kg (150 lb). Per verificare il peso massimo, rivolgiti al tuo corriere. |
| [!UICONTROL Pickup Method] | Sito Web | Imposta il metodo di prelievo del gruppo di continuità. Opzioni: `Regular Daily Pickup` / `On Call Air` / `One Time Pickup` / `Letter Center` / `Customer Counter` |
| [!UICONTROL Minimum Package Weight] | Sito Web | Imposta il peso minimo che un pacchetto può avere in base a quanto specificato da UPS. Se i prodotti ordinati pesano meno del peso minimo del pacchetto, questa opzione di spedizione non è disponibile. Per verificare il peso minimo, contattare il vettore di spedizione. |
| [!UICONTROL Calculate Handling Fee] | Sito Web | Imposta il metodo di calcolo della tariffa di movimentazione per la spedizione delle tariffe della tabella. Opzioni: <br>**`Fixed`**- La tariffa di imballaggio è fissa.<br>**`Percent`** - La tariffa di imballaggio viene applicata come percentuale dell&#39;importo dell&#39;ordine. |
| [!UICONTROL Handling Applied] | Sito Web | Specifica se le spese di imballaggio vengono applicate a ogni ordine o pacchetto all&#39;interno di un ordine. |
| [!UICONTROL Handling Fee] | Sito Web | Imposta la gestione inclusa nel prezzo della tariffa di spedizione. La tariffa di imballaggio può essere impostata come importo fisso o percentuale. <br/><br/>**_Nota:_** Se si digita un importo percentuale, utilizzare il formato decimale `0.25` per il 25%. |

{style="table-layout:auto"}

![Metodi consentiti UPS](./assets/delivery-methods-ups-allowed-methods.png)<!-- zoom -->

<!-- [UPS Allowed Methods]https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL UPS allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Sito Web | Specifica i metodi consentiti di spedizione UPS offerti ai clienti. Le tariffe di spedizione vengono calcolate in base al metodo di spedizione selezionato. |
| [!UICONTROL Free Method] | Sito Web | Identifica il metodo utilizzato per il metodo di spedizione gratuita tramite UPS. Per disattivare la spedizione gratuita, scegliere &quot;Nessuno&quot;. <br/><br/>**_Note:_** Questo metodo è simile al [Spedizione gratuita](../../stores-purchase/shipping-free.md) di base, tuttavia viene visualizzato come opzione di spedizione UPS durante il pagamento. |
| [!UICONTROL Free Shipping Amount Threshold] | Sito Web | Determina se la spedizione gratuita viene applicata quando l&#39;importo dell&#39;ordine soddisfa la soglia di spedizione gratuita. Opzioni: `Enable` / `Disable` |
| [!UICONTROL Free Shipping Amount Threshold] | Sito Web | Imposta l&#39;importo totale minimo che un ordine deve raggiungere per qualificarsi per la spedizione gratuita. |
| [!UICONTROL Displayed Error Message] | Visualizzazione store | Messaggio di errore visualizzato quando il metodo di spedizione non è disponibile per alcun motivo. |

{style="table-layout:auto"}

![Paesi UPS applicabili e altre impostazioni](./assets/delivery-methods-ups-ship-to.png)<!-- zoom -->

<!-- [UPS Applicable Countries and Other Settings]https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/ups) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL UPS Applicable countries and other Settings]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Sito Web | Specifica il paese in cui i clienti possono utilizzare questo metodo di spedizione. Opzioni: <br/>**`All Allowed Countries`**- I clienti di tutti i [paesi](../../getting-started/store-details.md#country-options) specificati nella configurazione dell&#39;archivio possono utilizzare questo metodo di spedizione.<br/>**`Specific Countries`** - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco [!UICONTROL Ship to Specific Countries]. Selezionare ogni paese nell&#39;elenco in cui è possibile utilizzare questo metodo di spedizione. |
| [!UICONTROL Show Method if Not Applicable] | Sito Web | Determina se UPS viene sempre visualizzato come opzione di spedizione durante il pagamento. Opzioni: <br/>**`Yes`**- UPS viene sempre visualizzato come opzione di spedizione durante il pagamento, anche se non applicabile all&#39;ordine.<br/>**`No`** - UPS viene visualizzato come opzione di spedizione durante il pagamento solo se applicabile all&#39;ordine. (ad esempio, se il peso dell&#39;ordine supera l&#39;importo del peso massimo). |
| [!UICONTROL Debug] | Sito Web | Specifica se le trasmissioni di dati tra l&#39;archivio e UPS vengono registrate nel sistema per il debug. A meno che non sia necessario tenere traccia e registrare un problema, questa opzione deve essere impostata su `No`. |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione del gruppo di continuità quando viene elencato con altri metodi di consegna durante il pagamento. Immetti `0` come primo elemento dell&#39;elenco. |

{style="table-layout:auto"}

### [!UICONTROL USPS]

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| Abilitato per l&#39;estrazione | Sito Web | Determina se USPS è disponibile per i clienti come metodo di spedizione durante il pagamento. Opzioni: `Yes` / `No` |
| _[!UICONTROL USPS Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Sito Web | URL utilizzato per connettersi al sistema USPS per recuperare dinamicamente le tariffe di spedizione. |
| [!UICONTROL Secure Gateway URL] | Sito Web | L’URL sicuro utilizzato per connettersi al sistema USPS su un livello di socket sicuro (SSL) per recuperare dinamicamente le tariffe di spedizione. |
| [!UICONTROL Title] | Visualizzazione store | Il titolo di questa opzione di spedizione visualizzato nel carrello acquisti. |
| [!UICONTROL User ID] | Sito Web | ID utente dell&#39;account speditore USPS. |
| [!UICONTROL Password] | Sito Web | Password dell&#39;account speditore USPS. |
| [!UICONTROL Mode] | Sito Web | Determina la modalità di trasmissione dei dati inviati al sistema USPS. Le opzioni includono: <br/>**`Development`**- USPS non verifica che i dati ricevuti dal server Commerce vengano inviati tramite SSL.<br/>**`Live`** - USPS verifica che i dati ricevuti dal server Commerce vengano inviati tramite un livello di socket protetto (SSL). |

{style="table-layout:auto"}

I campi seguenti sono disponibili solo se è stata applicata la patch di qualità [USPS REST API Migration](https://experienceleague.adobe.com/it/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/v1-1-70/ac-15210). Questa patch abilita il supporto per le API USPS, una piattaforma basata su REST che sostituisce le API degli strumenti web. Per informazioni dettagliate, vedere [API degli strumenti Web USPS obsoleta](../../stores-purchase/carriers.md).

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL USPS Type] | Sito Web | Scegli **API REST USPS** o **API degli strumenti Web USPS** in base alla quale utilizzerai. |
| [!UICONTROL Consumer Key] | Sito Web | ID client dell&#39;account corriere USPS per API REST. |
| [!UICONTROL Consumer Secret] | Sito Web | Chiave segreto client per API REST dell’account corriere USPS. |
| [!UICONTROL Account Type] | Sito Web | Tipo di conto di pagamento USPS. Opzioni: `"EPS"` (Enterprise Payment System) o `"PERMIT"` (Consenti stampa) per API REST. <br/><br/>**_Note:_** Questo campo è facoltativo, ma è necessario per abilitare la creazione delle etichette di spedizione. |
| [!UICONTROL Pricing Options] | Sito Web | Opzioni di determinazione prezzi USPS: **Vendita al dettaglio** o **Commerciale**. Influisce sulla tariffa di spedizione applicata. Il valore predefinito è **Commercial** per API REST. |
| [!UICONTROL Account Number] | Sito Web | Il numero di account **USPS**, utilizzato per il pagamento dell&#39;API REST.  <br/><br/>**_Note:_** Questo campo è facoltativo, ma è necessario per abilitare la creazione delle etichette di spedizione. |
| [!UICONTROL Customer Registration Identifier(CRID)] | Sito Web | Un codice CRID (Customer Registration Identification Number) è un codice numerico generato da USPS che identifica in modo univoco un’azienda in una posizione per l’API REST.  <br/><br/>**_Note:_** Questo campo è facoltativo, ma è necessario per abilitare la creazione delle etichette di spedizione. |
| [!UICONTROL Mailer Identifier(MID)] | Sito Web | Il Mailer Identifier (MID) è un campo all&#39;interno del codice a barre di Intelligent Mail utilizzato per identificare i mailer. Gli identificatori MID vengono assegnati dall’USPS a un Proprietario della posta, a un agente di posta o a un altro provider di servizi che richiede loro l’API REST.  <br/><br/>**_Note:_** Questo campo è facoltativo, ma è necessario per abilitare la creazione delle etichette di spedizione. |
| [!UICONTROL Manifest MID] | Sito Web | L’identificatore univoco del mailer designato per il manifesto per l’API REST.  <br/><br/>**_Note:_** Questo campo è facoltativo, ma è necessario per abilitare la creazione delle etichette di spedizione. Per Magento 2.4.7-p8 con la patch [AC-15210](https://experienceleague.adobe.com/it/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/v1-1-70/ac-15210) applicata, [!UICONTROL Manifest MID] è un campo obbligatorio. |
| [!UICONTROL AES/ITN] | Sito Web | USPS AES - Automated Export System/ITN - Numero di transazione interno per API REST. <br/><br/>**_Note:_** Questo campo è generalmente facoltativo, ma è necessario per abilitare la creazione di etichette di spedizione se: <ul><li>Ogni tipo di merce presente nella spedizione (come definito dai codici di esportazione di cui alla tabella B al <a href="https://www.census.gov/foreign-trade/schedules/b" target="_blank">www.census.gov/foreign-trade/schedules/b</a>) ha un valore pari o inferiore a 2.500 $ e non richiede una licenza di esportazione; oppure</li><li>La spedizione, indipendentemente dal valore, viene inviata in Canada e non richiede una licenza per l&#39;esportazione.</li></ul> |

{style="table-layout:auto"}

![Impostazioni pacchetto USPS](./assets/delivery-methods-usps-packaging.png)<!-- zoom -->

<!-- [USPS Packaging Settings](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL USPS packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | Sito Web | Determina la modalità di calcolo del peso per le spedizioni con più colli. Opzioni: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Container] | Sito Web | Imposta il tipo di contenitore utilizzato per imballare le spedizioni. Opzioni: `Variable` / `Flat Rate Box` / `Flat Rate Envelope` / `Rectangular` / Non rettangolare |
| [!UICONTROL Size] | Sito Web | Imposta l&#39;opzione Dimensione sulle dimensioni tipiche del pacchetto di spedizione. Questa opzione influisce sul calcolo della tariffa di spedizione. Opzioni: `Regular` / `Large` / `Oversize` |
| [!UICONTROL Machinable] | Sito Web | Specifica se il pacchetto può essere elaborato dalla macchina. Questa opzione influisce sul calcolo della tariffa di spedizione. |
| [!UICONTROL Maximum Package Weight] | Sito Web | Imposta il peso massimo che un pacchetto può avere come specificato da USPS. Se i prodotti ordinati superano il peso massimo del pacchetto, questa opzione di spedizione non è disponibile. |

{style="table-layout:auto"}

![Impostazioni tariffe di gestione USPS](./assets/delivery-methods-usps-handling-fee.png)<!-- zoom -->

<!-- [USPS Handling Fee Settings](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL USPS Handling Fee settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Sito Web | Imposta il metodo di calcolo della tariffa di movimentazione per la spedizione delle tariffe della tabella. Opzioni: <br/>**`Fixed`**- La tariffa di imballaggio è fissa.<br/>**`Percent`** - La tariffa di imballaggio viene applicata come percentuale dell&#39;importo dell&#39;ordine. |
| [!UICONTROL Handling Applied] | Sito Web | Specifica se le spese di imballaggio vengono applicate a ogni ordine o pacchetto all&#39;interno di un ordine. |
| [!UICONTROL Handling Fee] | Sito Web | Imposta la gestione inclusa nel prezzo della tariffa di spedizione. La tariffa di imballaggio può essere impostata come importo fisso o percentuale. <br/><br/>**_Nota:_** Quando si digita un importo percentuale, utilizzare il formato decimale `0.25` per il 25%. |

{style="table-layout:auto"}

![Metodi consentiti USPS](./assets/delivery-methods-usps-allowed-methods.png)<!-- zoom -->

<!-- [USPS Allowed Methods](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL USPS Allowed Methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Sito Web | Specifica i metodi di spedizione USPS consentiti offerti ai clienti. Le tariffe di spedizione vengono calcolate in base al metodo di spedizione selezionato. |
| [!UICONTROL Free Method] | Sito Web | Imposta il metodo di spedizione gratuita tramite USPS o può essere disabilitato selezionando `None`. <br/><br/>**_Note:_** Questo metodo di spedizione è simile al metodo di spedizione gratuita del tuo Negozio, tuttavia è elencato come opzione di spedizione USPS e identificato come spedizione USPS. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Sito Web | Imposta l&#39;importo minimo dell&#39;ordine che deve essere raggiunto per qualificarsi per la spedizione gratuita. |
| [!UICONTROL Displayed Error Message] | Visualizzazione store | Messaggio di errore visualizzato quando USPS non è disponibile per alcun motivo. |

{style="table-layout:auto"}

![Paesi USPS applicabili](./assets/delivery-methods-usps-countries.png)<!-- zoom -->

<!-- [USPS Applicable Countries](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/usps) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL USPS Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Sito Web | Specifica i paesi in cui possono essere spediti gli ordini. Opzioni: <br/>**`All Allowed Countries`**- I clienti di tutti i [paesi](../../getting-started/store-details.md#country-options) specificati nella configurazione dell&#39;archivio possono utilizzare questo metodo di spedizione.<br/>**`Specific Countries`** - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco [!UICONTROL Ship to Specific Countries]. Selezionare ogni paese nell&#39;elenco in cui è possibile utilizzare questo metodo di spedizione. |
| [!UICONTROL Show Method if Not Applicable] | Sito Web | Controlla la visualizzazione della spedizione USPS durante il pagamento. Opzioni: <br/>**`Yes`**- USPS viene sempre visualizzato come opzione di spedizione durante il pagamento, anche se non applicabile all&#39;ordine.<br/>**`No`** - USPS viene visualizzato come opzione di spedizione durante il pagamento solo se applicabile all&#39;ordine (ovvero se il peso dell&#39;ordine supera il peso massimo). |
| [!UICONTROL Debug] | Sito Web | Determina se il sistema gestisce un registro delle trasmissioni di dati tra l&#39;archivio e USPS per il debug. A meno che non sia necessario tenere traccia e registrare un problema, questa opzione deve essere impostata su `No`. |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione di USPS quando viene elencato con altri metodi di consegna durante il pagamento. Immetti `0` come primo elemento dell&#39;elenco. |

{style="table-layout:auto"}

### [!UICONTROL FedEx]

<!-- [FedEx Account Settings](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/fedex) -->

#### Impostazioni account FedEx

![Impostazioni account FedEx](./assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|-------|------ |-----------------------------------------------------------------------------|
| [!UICONTROL Enabled for Checkout] | Sito Web | Determina se FedEx è disponibile per i clienti come metodo di spedizione durante il pagamento. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Il titolo di questa opzione di spedizione visualizzato nel carrello acquisti. |
| [!UICONTROL Account ID] | Sito Web | ID del tuo account FedEx. |
| [!UICONTROL Api Key] | Sito Web | Chiave API dell&#39;account FedEx. |
| [!UICONTROL Secret Key] | Sito Web | Chiave segreta API del tuo account FedEx. |
| [!UICONTROL Sandbox Mode] | Sito Web | Per eseguire transazioni FedEx in un ambiente di test, impostare la modalità sandbox su `Yes`. Opzioni: `Yes` / `No`. |
| [!UICONTROL Web-Services URL] | Sito Web | L’URL richiesto dipende dall’impostazione della modalità sandbox. Opzioni: <br/>**`Production`**- URL per accedere ai servizi Web FedEx quando il negozio è attivo.<br/>**`Sandbox`** - URL di accesso all&#39;ambiente di test per i servizi Web FedEx. |

{style="table-layout:auto"}

#### Impostazioni imballaggio FedEx

![Packaging FedEx](./assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Pickup Type] | Sito Web | Dall&#39;elenco, selezionare il metodo di prelievo: <br/>**`DropOff at Fedex Location`**- (impostazione predefinita) Indica che si desidera eliminare le spedizioni dalla stazione FedEx locale.<br/>**`Contact Fedex to Schedule`** - Indica che hai contattato FedEx per richiedere un prelievo. <br/>**`Use Scheduled Pickup`**- Indica che la spedizione viene prelevata come parte di un prelievo pianificato regolare.<br/>**`On Call`** - Indica che il prelievo è pianificato chiamando FedEx. <br/>**`Package Return Program`**- Indica che la spedizione viene prelevata dal programma di restituzione dei pacchetti terrestri FedEx.<br/>**`Regular Stop`** - Indica che la spedizione viene prelevata al normale programma di prelievo. <br/>**`Tag`**- Indica che il prelievo della spedizione è specifico per una richiesta di prelievo di tag di chiamata rapida o di chiamata di terra. Questo è applicabile solo per un&#39;etichetta di spedizione di ritorno. |
| [!UICONTROL Packages Request Type] | Sito Web | Determina la modalità di calcolo del peso per le spedizioni con più colli. Opzioni: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Packaging] | Sito Web | Dall’elenco, seleziona il tipo di contenitore che in genere utilizzi per imballare i prodotti ordinati dal tuo store. |
| [!UICONTROL Weight Unit] | Sito Web | Unità utilizzata per il peso del pacchetto. Opzioni: `Pounds` (predefinito) / `Kilograms` |
| [!UICONTROL Maximum Package Weight] | Sito Web | Il valore predefinito per FedEx è 150 libbre. Rivolgersi al vettore di spedizione per conoscere il peso massimo supportato. Si consiglia di utilizzare il valore predefinito, a meno che non si disponga di accordi speciali con FedEx. |

{style="table-layout:auto"}

#### FedEx gestione delle tariffe

![Tariffa di gestione FedEx](./assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Calculate Handling Fee] | Sito Web | Determina il metodo utilizzato per calcolare le commissioni di gestione. Opzioni: `Fixed Fee` / `Percentage` <br/><br/>**_Note:_** La tariffa di imballaggio è facoltativa e viene visualizzata come un costo aggiuntivo aggiunto alle spese di spedizione FedEx. |
| [!UICONTROL Handling Applied] | Sito Web | Determina la modalità di applicazione delle commissioni di gestione. Opzioni: `Per Order` / `Per Package` |
| [!UICONTROL Handling Fee] | Sito Web | Specifica l&#39;importo addebitato come commissione di imballaggio, in base al metodo utilizzato per calcolare l&#39;importo. Se l&#39;addebito è basato su una tariffa fissa, immettere l&#39;importo come decimale, ad esempio `4.90`. Se la commissione di gestione è basata su una percentuale dell&#39;ordine, immettere l&#39;importo come percentuale. Ad esempio, per addebitare il 6% dell&#39;ordine, immettere il valore come `.06`. |

{style="table-layout:auto"}

#### Metodi di consegna FedEx

![Metodi di consegna FedEx](./assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Residential Delivery] | Sito Web | Impostato su uno dei seguenti, a seconda che si venda business-to-consumer (B2C) o business-to-business (B2B): <br/>**`Yes`**- Per consegne B2C<br/>**`No`** - Per consegne B2B |
| [!UICONTROL Allowed Methods] | Sito Web | Selezionare dall&#39;elenco i metodi di spedizione supportati. I metodi dipendono dal tuo account FedEx, dalla frequenza e dalle dimensioni delle tue spedizioni e dall’autorizzazione o meno delle spedizioni internazionali. In qualità di commerciante, potresti decidere di offrire solo la spedizione a terra. |
| [!UICONTROL Hub ID] | Sito Web | ID fornito da FedEx utilizzato con il metodo [!DNL Smart Post]. |
| [!UICONTROL Free Method] | Sito Web | Dall’elenco, seleziona il metodo di spedizione che preferisci utilizzare per le offerte di spedizione gratuita. <br/><br/>**_Note:_** Questo metodo di spedizione è simile al normale metodo di spedizione gratuita, tuttavia è elencato tra le opzioni di spedizione FedEx ed è identificato come spedizione FedEx. |
| [!UICONTROL Free Shipping Amount Threshold] | Sito Web | Determina se è necessario un importo minimo per la spedizione gratuita. Opzioni: <br/>**`Enable`**- Consente la spedizione gratuita FedEx per gli ordini che soddisfano l&#39;importo minimo.<br/>**`Disable`** - Disabilita la spedizione gratuita FedEx con un ordine minimo. |
| [!UICONTROL Free Shipping Amount Threshold] | Sito Web | Specifica l&#39;importo minimo dell&#39;ordine necessario per la spedizione gratuita. |
| [!UICONTROL Displayed Error Message] | Visualizzazione store | Messaggio visualizzato quando FedEx non è disponibile per qualsiasi motivo. Puoi utilizzare il messaggio predefinito o immetterne un altro. |

{style="table-layout:auto"}

#### Impostazioni paese applicabili FedEx

![Paesi applicabili FedEx](./assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Ship to Applicable Countries] | Sito Web | Indica i paesi in cui i clienti possono effettuare le spedizioni tramite FedEx. Opzioni: <br/>**`All Allowed Countries`**- I clienti di tutti i [paesi](../../getting-started/store-details.md#country-options) specificati nella configurazione dell&#39;archivio possono utilizzare questo metodo di spedizione.<br/>**`Specific Countries`** - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco [!UICONTROL Ship to Specific Countries]. Selezionare ogni paese nell&#39;elenco in cui è possibile utilizzare questo metodo di spedizione. |
| [!UICONTROL Ship to Specific Countries] | Sito Web | Indica i paesi specifici in cui i clienti possono effettuare le spedizioni tramite FedEx. |
| [!UICONTROL Debug] | Sito Web | Determina se il sistema gestisce un registro delle trasmissioni di dati tra il tuo archivio e FedEx per il debug. A meno che non sia necessario tenere traccia e registrare un problema, questa opzione deve essere impostata su `No`. |
| [!UICONTROL Show Method if Not Applicable] | Sito Web | Determina quando FedEx viene visualizzato come metodo di spedizione durante il pagamento. Opzioni: <br/>**`Yes`**- L&#39;opzione di spedizione FedEx viene visualizzata nell&#39;elenco dei metodi di consegna, indipendentemente dal fatto che l&#39;ordine sia idoneo per utilizzarlo.<br/>**`No`** - L&#39;opzione di spedizione FedEx non viene visualizzata nell&#39;elenco dei metodi di consegna se non è applicabile all&#39;ordine (ad esempio, se il peso dell&#39;ordine supera l&#39;importo del peso massimo). |
| [!UICONTROL Sort Order] | Sito Web | Un numero che determina l’ordine di visualizzazione di FedEx quando viene elencato con altri metodi di consegna durante il pagamento. Immetti `0` come primo elemento dell&#39;elenco. |

{style="table-layout:auto"}

### [!UICONTROL DHL]

![Impostazioni account DHL](./assets/delivery-methods-dhl-account-settings.png)<!-- zoom -->

<!-- [DHL Account Settings](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL DHL Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | Sito Web | Determina se DHL è disponibile per i clienti come metodo di spedizione durante il pagamento. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Titolo del metodo di spedizione visualizzato durante il pagamento. |
| [!UICONTROL Gateway URL] | Sito Web | In genere, è possibile accettare l&#39;URL del gateway predefinito. Se invece DHL ha fornito un URL alternativo, immettere il valore in questo campo. |
| [!UICONTROL Access ID] | Sito Web | ID di accesso dell&#39;account spedizioniere DHL. |
| [!UICONTROL Password] | Sito Web | Password dell&#39;account spedizioniere DHL. |
| [!UICONTROL Account Number] | Sito Web | Il numero del conto di spedizione DHL. |

{style="table-layout:auto"}

![Impostazioni pacchetto DHL](./assets/delivery-methods-dhl-package-settings.png)<!-- zoom -->

<!-- [DHL Package Settings](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL DHL Package Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Sito Web | La tariffa di movimentazione è facoltativa e appare come un supplemento aggiunto al costo di spedizione DHL. Selezionare dall&#39;elenco il metodo che si desidera utilizzare per calcolare le commissioni di gestione. Opzioni: Tariffa Fissa / Percentuale. |
| [!UICONTROL Handling Applied] | Sito Web | Dall’elenco, seleziona la modalità di applicazione delle tariffe di gestione. Opzioni: `Per Order` / `Per Package` |
| Spese di imballaggio | Sito Web | Immettere l&#39;importo da addebitare per una commissione di gestione, in base al metodo scelto per calcolare l&#39;importo. Ad esempio, se l&#39;addebito è basato su una tariffa fissa, immettere l&#39;importo come decimale, ad esempio `4.90`. Tuttavia, se la commissione di gestione si basa su una percentuale dell&#39;ordine, immettere l&#39;importo come percentuale. Ad esempio, se si sta addebitando il 6% dell&#39;ordine, immettere il valore come `.06`. |
| [!UICONTROL Divide Order Weight] | Visualizzazione store | Determina se il peso di un ordine superiore a 70 kg può essere diviso in unità più piccole per garantire una spesa di spedizione accurata. Opzioni: `Yes` / `No` |
| [!UICONTROL Weight Unit] | Visualizzazione store | Determina l&#39;unità di misura per il peso utilizzata nei calcoli di spedizione. Opzioni: `Pounds` / `Kilograms` |
| [!UICONTROL Size] | Visualizzazione store | Determina la dimensione del pacchetto. Opzioni: <br/>**`Regular`**- I pacchetti spediti sono conformi ai metodi di imballaggio standard DHL. Nell&#39;elenco [!UICONTROL Allowed Methods], selezionare ogni metodo di imballaggio utilizzato per spedire i prodotti dal tuo negozio.<br/>**`Specific`** - Se i pacchetti spediti hanno dimensioni personalizzate, completare le operazioni seguenti: [!UICONTROL Height (cm)] / [!UICONTROL Depth (cm)] / [!UICONTROL Width (cm)] |

{style="table-layout:auto"}

![Metodi consentiti DHL](./assets/delivery-methods-dhl-allowed-methods.png)<!-- zoom -->

<!-- DHL Allowed Methods](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL DHL allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Sito Web | Nell&#39;elenco selezionare tutti i metodi di spedizione supportati. |
| [!UICONTROL Ready Time] | Sito Web | Specifica quando il pacchetto sarà pronto per il ritiro (in ore) dopo l’invio di un ordine. |
| [!UICONTROL Displayed Error Message] | Visualizzazione store | Questo messaggio viene visualizzato quando DHL non è più disponibile per qualsiasi motivo. Puoi utilizzare il messaggio predefinito o immetterne uno tuo. |
| [!UICONTROL Free Method] |  | Questo metodo di spedizione è simile al normale metodo di spedizione gratuita, tuttavia è elencato all&#39;interno delle opzioni di spedizione DHL ed è identificato come spedizione DHL. Nell&#39;elenco selezionare il metodo di spedizione che si preferisce utilizzare per le offerte di spedizione gratuita. |
| [!UICONTROL Free Shipping with Minimum Order Amount] | Sito Web | Impostare uno dei seguenti valori: <br/>**`Enable`**- Per consentire la spedizione gratuita di DHL per gli ordini che soddisfano l&#39;importo minimo.<br/>**`Disable`** - Per non offrire spedizione DHL gratuita con ordine minimo. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Sito Web | Se abiliti [!UICONTROL Free Shipping with Minimum Order], immetti il valore dell&#39;importo minimo dell&#39;ordine nel campo. |

{style="table-layout:auto"}

![Paesi applicabili DHL](./assets/delivery-methods-dhl-applicable-countries.png)<!-- zoom -->

<!-- [DHL Applicable Countries](https://experienceleague.adobe.com/it/docs/commerce-admin/stores-sales/delivery/shipping-carriers/dhl) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| _[!UICONTROL DHL applicable countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Sito Web | Specifica il paese in cui i clienti possono utilizzare questo metodo di spedizione. Opzioni: <br/>**Tutti i paesi consentiti** - Tutti i paesi consentiti possono utilizzare il metodo di spedizione gratuita. I paesi consentiti sono specificati nella pagina di configurazione [!UICONTROL General]. <br/>**Paesi specifici** - Limita questa opzione di spedizione ai paesi specificati nell&#39;elenco Spedisci a paesi specifici. |
| [!UICONTROL Ship to Specific Countries] | Sito Web | Specifica i paesi in cui possono essere inviate le spedizioni DHL. Questo elenco di paesi selezionati viene utilizzato se `Specific Countries` è selezionato nell&#39;opzione [!UICONTROL Ship to Applicable Countries]. |
| [!UICONTROL Show Method if Not Applicable] | Sito Web | Determina quando DHL viene visualizzato come metodo di spedizione durante il pagamento. Opzioni: <br/>**`Yes`**- DHL viene sempre visualizzato come opzione di spedizione durante il pagamento, anche se non applicabile all&#39;ordine.<br/>**`No`** - DHL viene visualizzato come opzione di spedizione durante il pagamento solo se applicabile all&#39;ordine (ovvero se il peso dell&#39;ordine supera il peso massimo). |
| [!UICONTROL Debug] | Sito Web | Crea un file di registro con informazioni sull&#39;errore. |
| [!UICONTROL Sort Order] | Sito Web | Numero che determina l&#39;ordine di visualizzazione di DHL quando viene elencato con altri metodi di consegna durante il pagamento. Per collocarla all&#39;inizio dell&#39;elenco, immettere `0`. |

{style="table-layout:auto"}
