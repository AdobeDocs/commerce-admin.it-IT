---
title: FedEx
description: Scopri come impostare FedEx come vettore di spedizione per il tuo negozio.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# FedEx

FedEx è una delle più grandi società di servizi di trasporto marittimo al mondo, che fornisce servizi di trasporto aereo, merci e di terra con diversi livelli di priorità.

![Opzioni di spedizione FedEx al momento del pagamento](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx può utilizzare [peso dimensionale](carriers.md#dimensional-weight) per determinare alcune tariffe di spedizione. Tuttavia, Adobe Commerce e il Magento Open Source supportano solo il calcolo delle spese di spedizione basato sul peso.

## Fase 1: Registrati per la produzione di servizi Web FedEx

A [Account commerciante FedEx][1] e la registrazione per FedEx Web Services Production Access è obbligatoria. Dopo aver creato un account FedEx, leggi la pagina delle informazioni dell’account di produzione, quindi fai clic su _Ottieni chiave di produzione_ nella parte inferiore della pagina per registrarsi e ottenere una chiave.

>[!NOTE]
>
>Assicurati di copiare o annotare la chiave di autenticazione. È necessario impostare FedEx nelle impostazioni di spedizione di Commerce.

## Passaggio 2: abilitare FedEx per il tuo Negozio

{{beta2-updates}}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Delivery Methods]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL FedEx]** sezione.

1. Imposta **[!UICONTROL Enabled for Checkout]** a `Yes`.

1. Per **[!UICONTROL Title]**, inserisci un titolo che identifichi il metodo di spedizione FedEx durante il pagamento.

1. Immetti le seguenti informazioni dal tuo account FedEx:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Meter Number]**
   - **[!UICONTROL Key]**
   - **[!UICONTROL Password]**

1. Se hai impostato una sandbox FedEx e vuoi lavorare nell’ambiente di test, imposta **[!UICONTROL Sandbox Mode]** a `Yes`.

   >[!NOTE]
   >
   >Ricordati di impostare la modalità sandbox su `No` quando sei pronto a offrire FedEx come metodo di spedizione ai tuoi clienti.

   ![Impostazioni account FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Passaggio 3: Descrizione del pacchetto e spese di imballaggio

1. Seleziona la **[!UICONTROL Packages Request Type]** all&#39;opzione che meglio descrive la preferenza quando si suddivide un ordine in più spedizioni:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Seleziona il tipo di **[!UICONTROL Packaging]** in genere utilizzato per spedire prodotti dal tuo negozio.

1. Imposta **[!UICONTROL Dropoff]** al metodo di prelievo utilizzato per la consegna.

   - `Regular Pickup` - Se si dispone di un elevato volume di spedizioni, può essere conveniente prendere accordi con FedEx per i prelievi regolari.

   - `Request Courier` - È necessario chiamare e richiedere un corriere FedEx per ritirare le spedizioni.

   - `Drop Box` - Devi consegnare le consegne presso la tua vicina confezione FedEx.

   - `Business Service Center` - Le spedizioni devono essere effettuate presso il centro di assistenza locale FedEx.

   - `Station` - Le consegne devono essere effettuate presso la stazione FedEx locale.

1. Imposta **[!UICONTROL Weight Unit]** all&#39;unità di misura utilizzata nelle impostazioni internazionali.

   - `Pounds`
   - `Kilograms`

1. Inserisci il **[!UICONTROL Maximum Package Weight]** consentito per spedizioni FedEx.

   Il peso massimo predefinito di FedEx è di 150 libbre. Per ulteriori informazioni, rivolgiti al tuo corriere. Il valore predefinito è consigliato, a meno che tu non abbia stipulato accordi speciali con FedEx. Consulta [Peso dimensionale](carriers.md#dimensional-weight) per ulteriori informazioni.

   ![Impostazioni pacchetto FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Configura le opzioni relative alle commissioni di gestione in base alle tue esigenze.

   La tariffa di imballaggio è facoltativa e non è visibile durante il pagamento. Se si desidera includere una tariffa di imballaggio, eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - Per **[!UICONTROL Handling Applied]**, scegliere uno dei metodi seguenti per la gestione delle commissioni:

      - `Per Order`
      - `Per Package`

   - Inserisci il **[!UICONTROL Handling Fee]** come `fixed` importo o `percentage`, a seconda del metodo di calcolo.

1. Imposta **[!UICONTROL Residential Delivery]** a una delle seguenti opzioni, a seconda che si venda Business-to-Consumer (B2C) o Business-to-Business (B2B).

   - `Yes` - per consegne residenziali B2C.
   - `No` - per consegne residenziali B2B.

   ![Impostazioni delle tariffe di gestione FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Fase 4: Metodi consentiti e paesi applicabili

1. Imposta **[!UICONTROL Allowed Methods]** a ogni metodo di spedizione che si desidera offrire.

   Quando si scelgono i metodi, considerare il proprio account FedEx, la frequenza e le dimensioni delle spedizioni e se si consentono spedizioni internazionali. Puoi offrire tutti i metodi desiderati, ad esempio:

   - Priorità Europa
   - Opzioni per il giorno di consegna: 1 giorno di trasporto, 2 giorni di trasporto, 2 giorni, 2 giorni AM, 3 giorni di trasporto
   - Opzioni nazionali-Express Saver, Terra, Primo, Pernottamento, Consegna a domicilio, Standard Overnight
   - Opzioni internazionali-International Economy, Intl Economy Freight, International First, International Ground, International, Priority Intl
   - Opzioni di priorità-Trasporto, Priorità notte
   - Smart Post-If che offre il metodo Smart Post (immettere il valore **ID hub**)
   - Opzioni di trasporto-Trasporto, trasporto nazionale

1. Se desideri fornire un [Spedizione gratuita](shipping-free.md) tramite FedEx, impostare le opzioni di spedizione gratuita.

   - Imposta **[!UICONTROL Free Method]** al metodo che si desidera utilizzare per la spedizione gratuita. Se non si desidera offrire la spedizione gratuita tramite FedEx, scegliere `None`.

   - Per richiedere un importo minimo per un ordine per la spedizione gratuita con FedEx, impostare **[!UICONTROL Enable Free Shipping Threshold]** a `Enable`. Quindi, inserisci il valore minimo in **[!UICONTROL Free Shipping Amount Threshold]**.

   Questa impostazione è simile a quella del metodo di spedizione gratuita standard, ma viene visualizzata nella sezione FedEx durante il pagamento, in modo che i clienti sappiano quale metodo viene utilizzato per il loro ordine.

1. Se necessario, modificare il **[!UICONTROL Displayed Error Message]**.

   Questa casella di testo è preimpostata con un messaggio predefinito, ma è possibile immettere un messaggio diverso da visualizzare se FedEx non è più disponibile.

   ![Metodi di consegna consentiti FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione dell’archivio può utilizzare questo metodo di consegna.

   - `Specific Countries` - Quando si sceglie questa opzione, il _Spedisci a paesi specifici_ viene visualizzato. Seleziona ogni paese nell’elenco in cui può essere utilizzato questo metodo di consegna.

1. Per conservare un registro di tutte le comunicazioni tra il negozio e il sistema FedEx, impostare **[!UICONTROL Debug]** a `Yes`.

1. Imposta **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Mostra tutti i metodi di spedizione FedEx ai clienti, indipendentemente dalla loro disponibilità.
   - `No` - Mostra solo i metodi di spedizione FedEx applicabili all&#39;ordine.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui viene visualizzato FedEx quando viene elencato con altri metodi di consegna durante il pagamento.

   `0` = innanzitutto, `1` = secondo, `2` = terzo e così via.

1. Clic **[!UICONTROL Save Config]**.

   ![Paesi applicabili FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Durante il calcolo delle spese di spedizione, Commerce dichiara sempre a FedEx il prezzo dell’ordine completo. Questo comportamento non può essere modificato.

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
