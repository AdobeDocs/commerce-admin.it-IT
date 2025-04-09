---
title: FedEx
description: Scopri come configurare FedEx come corriere per il vostro store.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: ad5da1d77b63bf6bcc0227a5c467e369b7bb8d89
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# FedEx

FedEx è una delle più grandi società di servizi di spedizione al mondo, che fornisce servizi di spedizione aerea, merci e via terra con diversi livelli di priorità.

![FedEx Shipping Opzioni al momento del pagamento](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx può utilizzare [il peso](carriers.md#dimensional-weight) dimensionale per determinare alcune tariffe di spedizione. Tuttavia, Adobe Systems Commerce e Magento Open Source supportano solo il calcolo dei costi di spedizione basato sul peso.

## Fase 1: Registrazione alla produzione di servizi Web FedEx

È necessario un commerciante FedEx account e registrazione per FedEx Web Services Production Access. Dopo aver creato un account FedEx, leggere la pagina delle informazioni sulla account di produzione, quindi fare clic sulla _collegare Ottieni chiave_ di produzione nella parte inferiore della pagina per registrarsi e ottenere una chiave.

>[!NOTE]
>
>Assicurati di copiare o annotare la chiave di autenticazione. È necessario impostare FedEx nelle impostazioni di spedizione di Commerce.

## Passaggio 2: attiva FedEx per il tuo negozio

1. _Nella barra laterale Amministratore_, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Delivery Methods]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL FedEx]**.

1. Imposta **[!UICONTROL Enabled for Checkout]** su `Yes`.

1. Per **[!UICONTROL Title]**, inserisci un titolo che identifichi il metodo di spedizione FedEx durante il checkout.

1. Inserite le seguenti informazioni dal vostro account FedEx:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. Se disponi di credenziali API di tracciamento separate, abilita la configurazione seguente:

   - **[!UICONTROL Enable Tracking API credentials]**

1. Inserite le seguenti informazioni dal vostro account FedEx:

   - **[!UICONTROL Tracking API Key]**
   - **[!UICONTROL Tracking API Secret Key]**

1. Se avete configurato una sandbox FedEx e desiderate lavorare nell&#39;ambiente di test, impostate **[!UICONTROL Sandbox Mode]** su `Yes`.

   >[!NOTE]
   >
   >Ricordati di impostare la modalità Sandbox su `No` quando sei pronto per offrire FedEx come metodo di spedizione ai tuoi clienti.

   ![FedEx Impostazioni account](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Passaggio 3: descrizione del pacchetto e spese di gestione

1. Imposta **[!UICONTROL Pickup Type]** il metodo di ritiro utilizzato per le spedizioni.

   - `DropOff at Fedex Location` - (Impostazione predefinita) Indica che tasso di caduta le spedizioni presso la stazione FedEx locale.
   - `Contact Fedex to Schedule` - Indica che si contatta FedEx per richiesta un ritiro.
   - `Use Scheduled Pickup` - Indica che la spedizione viene ritirata come parte di un normale ritiro programmato.
   - `On Call` - Indica che il ritiro è programmato chiamando FedEx.
   - `Package Return Program` - Indica che la spedizione viene ritirata dal FedEx Ground Package Returns Program.
   - `Regular Stop` - Indica che la spedizione viene ritirata presso il normale programmare di ritiro.
   - `Tag` - Indica che il ritiro della spedizione è specifico per una chiamata Express tag o Ground tag richiesta di ritiro. Questo è applicabile solo per un&#39;etichetta di spedizione per la restituzione.

1. Per **[!UICONTROL Packages Request Type]**, seleziona il tipo di richiesta che meglio descrive la tua preferenza quando dividi un ordine in più spedizioni:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Per **[!UICONTROL Packaging]**, selezionate il tipo di imballaggio FedEx che utilizzate solitamente per spedire i prodotti dal vostro store.

1. Impostare **[!UICONTROL Weight Unit]** sull&#39;unità di misura utilizzata nelle impostazioni locali.

   - `Pounds`
   - `Kilograms`

1. Immetti il **[!UICONTROL Maximum Package Weight]** consentito per le spedizioni FedEx.

   Il peso massimo predefinito di FedEx è di 150 libbre. Per ulteriori informazioni, rivolgiti al tuo corriere. Il valore predefinito è consigliato, a meno che tu non abbia stipulato accordi speciali con FedEx. Per ulteriori informazioni, vedere [Peso dimensionale](carriers.md#dimensional-weight) .

   ![FedEx Package Impostazioni](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Configura le opzioni delle spese di gestione in base alle tue esigenze.

   La tassa di gestione è facoltativa e non è visibile durante il checkout. Se desideri includere una commissione di gestione, procedi come segue:

   - Imposta **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - Per **[!UICONTROL Handling Applied]**, scegliere uno dei seguenti metodi per gestire le spese di gestione:

      - `Per Order`
      - `Per Package`

   - Immettete l&#39;importo **[!UICONTROL Handling Fee]** come o `fixed` `percentage`, a seconda del metodo di calcolo.

1. Imposta **[!UICONTROL Residential Delivery]** su una delle opzioni seguenti, a seconda che vendi Aziende-to-Consumer (B2C) o Aziende-to-Aziende (B2B).

   - `Yes` - Per B2C consegne residenziali.
   - `No` - Per B2B consegne residenziali.

   ![Spese di gestione FedEx Impostazioni](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Passaggio 4: metodi consentiti e paesi applicabili

1. Imposta **[!UICONTROL Allowed Methods]** su ogni metodo di spedizione che desideri offrire.

   Quando scegliete i metodi, considerate il vostro account FedEx, la frequenza e le dimensioni delle vostre spedizioni e se consentite le spedizioni internazionali. Puoi offrire tutti i metodi desiderati, ad esempio:

   - Priorità Europa
   - Opzioni per il giorno di consegna: 1 giorno di trasporto, 2 giorni di trasporto, 2 giorni, 2 giorni AM, 3 giorni di trasporto
   - Opzioni nazionali: Express Saver, Ground, First, Overnight, consegna a domicilio, Standard Overnight
   - Opzioni internazionali: economia internazionale, trasporto merci in economia internazionale, prima internazionale, terra internazionale, internazionale, priorità internazionale
   - Opzioni prioritarie: trasporto, priorità durante la notte
   - Smart Post: se si offre il metodo Smart Post (immettere l&#39;ID **** Hub)
   - Opzioni di trasporto–Freight, National Freight

1. Se si desidera fornire un&#39;opzione [di spedizione](shipping-free.md) gratuita tramite FedEx, impostare le opzioni di spedizione gratuito.

   - Imposta **[!UICONTROL Free Method]** il metodo che desideri utilizzare per la spedizione gratuito. Se non vuoi offrire gratuito la spedizione tramite FedEx, scegli `None`.

   - Per richiedere un importo minimo dell&#39;ordine che qualifichi un ordine per la spedizione gratuito con FedEx, impostare **[!UICONTROL Enable Free Shipping Threshold]** su `Enable`. Quindi, immettete il valore minimo in **[!UICONTROL Free Shipping Amount Threshold]**.

   Questa impostazione è simile a quella per il metodo di spedizione gratuita standard, ma appare nella sezione FedEx durante il checkout, in modo che i clienti sappiano quale metodo viene utilizzato per il loro ordine.

1. Se necessario, modificare .**[!UICONTROL Displayed Error Message]**

   Questa casella di testo è preimpostata con un messaggio predefinito, ma è possibile immettere un messaggio diverso che si desidera visualizzare se FedEx diventa non disponibile.

   ![Metodi di consegna consentiti da FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del store possono utilizzare questo metodo di consegna.

   - `Specific Countries` - Quando si sceglie questa opzione, viene visualizzato l&#39;elenco _Spedisci in paesi_ specifici. Seleziona ogni paese nell&#39;elenco in cui può essere utilizzato questo metodo di consegna.

1. Se desiderate tenere un registro di tutte le comunicazioni tra il vostro store e il sistema FedEx, impostate **[!UICONTROL Debug]** su `Yes`.

1. Imposta **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Mostra tutti i metodi di spedizione FedEx ai clienti, indipendentemente dalla loro disponibilità.
   - `No` - Mostra solo i metodi di spedizione FedEx applicabili all&#39;ordine.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui viene visualizzato FedEx quando elencato con altri metodi di consegna durante l&#39;estrazione.

   `0` = primo, `1` = secondo, `2` = terzo e così via.

1. Fare clic su **[!UICONTROL Save Config]**.

   ![Paesi interessati FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Commerce dichiara sempre l&#39;intero prezzo dell&#39;ordine a FedEx quando calcola le spese di spedizione. Questo comportamento non può essere modificato.
