---
title: Servizio postale degli Stati Uniti (USPS)
description: Scopri come impostare USPS come vettore di spedizione per il tuo negozio.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: be8a4e9d7cbcf34452724f8055980007794f525f
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---

# Servizio postale degli Stati Uniti (USPS)

Lo United States Postal Service è il servizio postale indipendente del governo degli Stati Uniti, che offre servizi di spedizione nazionali e internazionali via terra e via aria.

## Passaggio 1: aprire un account di spedizione USPS

Apri un account [Strumenti Web USPS][1]. Dopo aver completato il processo di registrazione, riceverai il tuo ID utente e un URL al server di test USPS.

È inoltre possibile aprire un account [Strumenti Web USPS][1]. Dopo aver completato il processo di registrazione, riceverai il tuo ID utente e un URL al server di test USPS. Per ulteriori informazioni sugli strumenti Web USPS, vedere la relativa [documentazione tecnica][2].

## Passaggio 2: abilitare USPS per il tuo store

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Delivery Methods]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL USPS]**.

   >[!NOTE]
   >
   >Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare le impostazioni seguenti come descritto.

1. Imposta **[!UICONTROL Enabled for Checkout]** su `Yes`.

1. Impostare **[!UICONTROL USPS Type]** su `USPS Rest APIs` se si utilizza l&#39;API REST USPS.

   Se si utilizza l&#39;API degli strumenti Web USPS, impostare **[!UICONTROL USPS Type]** su `USPS Web Tools API`.

1. Se necessario, immettere **[!UICONTROL Gateway URL]** per accedere alle tariffe di spedizione USPS.

   Il campo è preimpostato per impostazione predefinita e normalmente non deve essere modificato.

1. Immettere un **[!UICONTROL Title]** per questo metodo di spedizione visualizzato durante l&#39;estrazione.

1. Utilizza le credenziali fornite da USPS per completare i campi seguenti:

   Se utilizzi le API REST USPS, devi fornire le seguenti credenziali:

   - **[!UICONTROL Consumer Key]**
   - **[!UICONTROL Consumer Secret]**
   - **[!UICONTROL Pricing Options]**

   Se si utilizza l&#39;API degli strumenti Web USPS, è necessario fornire le credenziali seguenti:

   - **[!UICONTROL User ID]**
   - **[!UICONTROL Password]**

1. Imposta **[!UICONTROL Mode]** su uno dei seguenti:

   - `Development` - Esegue USPS in un ambiente di test. Dopo aver eseguito USPS in un ambiente di sviluppo, assicurarsi di tornare più tardi e impostare la modalità su `Live`.
   - `Live` - Esegue USPS in un ambiente di produzione live.

## Passaggio 3: completare la descrizione dell&#39;imballaggio

1. Per determinare la modalità di gestione dell&#39;ordine se inviato come più pacchetti, impostare **[!UICONTROL Packages Request Type]** su uno dei seguenti:

   - `Divide to Equal Weight` - (Una richiesta) La spedizione di più pacchetti può essere inviata come un&#39;unica richiesta se i pacchetti sono divisi per lo stesso peso.
   - `Use Origin Weight` - (Richieste multiple) È necessario inviare più pacchetti come richieste separate se si utilizza il peso dell&#39;origine come base per il calcolo delle spese di spedizione.

1. Impostare **[!UICONTROL Container]** sul tipo di imballaggio normalmente utilizzato per la spedizione dei prodotti ordinati per il tuo Negozio.

1. Imposta **[!UICONTROL Size]** del pacchetto tipico spedito dal tuo archivio.

1. Imposta **[!UICONTROL Machinable]** su uno dei seguenti:

   - `Yes` - Se il pacchetto tipico può essere elaborato da un computer.
   - `No` - Se il pacchetto tipico deve essere elaborato manualmente.

1. Immettere **[!UICONTROL Maximum Package Weight]** in base ai requisiti del vettore.

   ![Impostazioni pacchetto USPS](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Passaggio 4: impostare le commissioni di gestione

La tariffa di movimentazione è facoltativa e viene visualizzata come un supplemento che viene aggiunto al costo di spedizione DHL. Se si desidera includere una tariffa di imballaggio, eseguire le operazioni seguenti:

1. Impostare **[!UICONTROL Calculate Handling Fee]** su uno dei metodi seguenti:

   - `Fixed`
   - `Percent`

1. Per determinare la modalità di applicazione della tariffa di gestione, impostare **[!UICONTROL Handling Applied]** su uno dei seguenti valori:

   - `Per Order`
   - `Per Package`

1. Immettere l&#39;importo di **[!UICONTROL Handling Fee]** da addebitare.

   Per immettere una percentuale, utilizzare il formato decimale. Ad esempio, immettere `0.25` per il 25%.

   ![Spese di gestione USPS](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Passaggio 5: specificare i metodi consentiti e i paesi applicabili

1. Per **[!UICONTROL Allowed Methods]**, scegli ogni metodo di spedizione USPS da rendere disponibile ai tuoi clienti.

   I metodi vengono visualizzati in USPS durante l&#39;estrazione. Per selezionare più metodi, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

1. Se desideri fornire un&#39;opzione [Spedizione gratuita](shipping-free.md) tramite USPS, imposta le opzioni di spedizione gratuita:

   - Impostare **[!UICONTROL Free Method]** sul metodo da utilizzare per la spedizione gratuita. Se non desideri offrire la spedizione gratuita tramite USPS, scegli `None`.

   - Per richiedere un importo minimo dell&#39;ordine che qualifichi un ordine per la spedizione gratuita con USPS, impostare **[!UICONTROL Enable Free Shipping Threshold]** su `Enable`. Immettere quindi il valore minimo in **[!UICONTROL Free Shipping Amount Threshold]**.

1. Se necessario, modificare **[!UICONTROL Displayed Error Message]**.

   Questa casella di testo è preimpostata con un messaggio predefinito, ma è possibile immettere un messaggio diverso da visualizzare se USPS non è più disponibile.

   ![Metodi consentiti USPS](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Ship to Applicable Countries]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione dell&#39;archivio possono utilizzare questo metodo di consegna.
   - `Specific Countries` - Quando si sceglie questa opzione, viene visualizzato l&#39;elenco _Spedisci a paesi specifici_. Seleziona ogni paese nell’elenco in cui può essere utilizzato questo metodo di consegna.

   ![Paesi USPS applicabili](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Show Method if Not Applicable]** su uno dei seguenti:

   - `Yes` - Elenca tutti i metodi di spedizione USPS disponibili durante il pagamento, inclusi i metodi non applicabili alla spedizione.
   - `No` - Elenca solo i metodi di spedizione USPS applicabili alla spedizione.

1. Per creare un file di registro con i dettagli delle spedizioni USPS effettuate dal tuo archivio, imposta **[!UICONTROL Debug]** su `Yes`.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui verrà visualizzato USPS quando elencato con altri metodi di consegna durante l&#39;estrazione.

   `0` = primo, `1` = secondo, `2` = terzo e così via.

1. Fare clic su **[!UICONTROL Save Config]**.

[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm

<!-- Last updated from includes: 2025-10-29 05:34:15 -->
