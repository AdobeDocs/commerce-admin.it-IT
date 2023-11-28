---
title: United Parcel Service (UPS)
description: Scopri come impostare UPS come corriere per il tuo negozio.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) offre servizi di spedizione nazionali e internazionali via terra e via aria a più di 220 paesi.

{{ups-api}}

>[!NOTE]
>
>UPS può utilizzare [peso dimensionale](carriers.md#dimensional-weight) per determinare alcune tariffe di spedizione. Tuttavia, Adobe Commerce supporta solo il calcolo delle spese di spedizione in base al peso.

## Passaggio 1: aprire un conto di spedizione UPS

Per offrire questo metodo di spedizione ai tuoi clienti, devi prima aprire un account con UPS.

## Passaggio 2: abilitare UPS per il tuo store

{{beta2-updates}}

1. Il giorno _Barra laterale di amministrazione_, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, sotto **[!UICONTROL Sales]**, scegli **[!UICONTROL Delivery Methods]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL UPS]** sezione.

1. Imposta **[!UICONTROL Enabled for Checkout]** a `Yes`.

1. Per un account UPS XML (impostazione predefinita), impostare **[!UICONTROL UPS Type]** a `United Parcel Service XML` ed effettuare le seguenti operazioni:

   - Immettere le credenziali del gruppo di continuità: **[!UICONTROL User ID]**, **[!UICONTROL Access License Number]** (account UPS a 16 cifre) `Access Key`), e **[!UICONTROL Password]**

   - Imposta **[!UICONTROL Mode]** a `Live` per inviare i dati al sistema di spedizione UPS tramite una connessione sicura. La modalità di sviluppo non invia dati tramite una connessione protetta.

   - Verificare la **[!UICONTROL Gateway XML URL]** necessario per inviare richieste tramite file XML.

   - Imposta **[!UICONTROL Origin of the Shipment]** alla regione di origine della spedizione.

   - Se si dispone di tariffe speciali con UPS, impostare **[!UICONTROL Enable Negotiated Rates]** a `Yes` e immettere le sei cifre **[!UICONTROL Shipper Number]** assegnati da UPS.

1. Per un account UPS standard, impostare **[!UICONTROL UPS Type]** a `United Parcel Service` ed effettuare le seguenti operazioni:

   >[!NOTE]
   >
   >Il tipo di servizio United Parcel Service standard è impostato come obsoleto. Per le nuove configurazioni, utilizza il valore predefinito  `United Parcel Service XML` tipo. Per generare è necessario anche il tipo XML [etichette di spedizione](shipping-labels.md).

   - Imposta **[!UICONTROL Live Account]** a uno dei seguenti elementi:

      - `Yes` - Esegue UPS in modalità di produzione e offre UPS come metodo di spedizione ai clienti.
      - `No` - Esegue il gruppo di continuità in modalità di test.

   - In **[!UICONTROL Gateway URL]** , immettere l&#39;URL utilizzato per calcolare le tariffe di spedizione UPS.

     >[!IMPORTANT]
     >
     >UPS sta interrompendo il supporto di HTTP, utilizzato nell’impostazione predefinita corrente (valore di sistema). Cancella **[!UICONTROL Use system value]** e modificare l’URL per utilizzare HTTPS. Esempio: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Per **[!UICONTROL Title]**, immettere il nome dell&#39;opzione di spedizione che si desidera venga visualizzata durante il pagamento.

   Per impostazione predefinita, questo campo è impostato su `United Parcel Service`.

   ![Abilita UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Passaggio 3: completare la descrizione del contenitore

1. Imposta **[!UICONTROL Packages Request Type]** a uno dei seguenti elementi:

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Per **[!UICONTROL Container]**, specificare il tipo di imballaggio tipico utilizzato per la spedizione:

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. Imposta **[!UICONTROL Weight Unit]** al sistema utilizzato per misurare il peso del prodotto.

   Il sistema di peso supportato da UPS varia in base al paese. In caso di dubbi, chiedere a UPS quale sistema di peso deve utilizzare. Le opzioni includono:

   - `LBS`
   - `KGS`

1. Imposta **[!UICONTROL Destination Type]** a uno dei seguenti elementi:

   - `Residential` - La maggior parte delle spedizioni è B2C (business to consumer).
   - `Commercial` - La maggior parte delle spedizioni riguarda business to business (B2B).

1. Inserisci il **[!UICONTROL Maximum Package Weight]** consentito dal vettore.

1. Imposta **[!UICONTROL Pickup Method]** a uno dei seguenti elementi:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Inserisci il **[!UICONTROL Minimum Package Weight]** consentito dal vettore.

   ![Descrizione contenitore](./assets/ups2.png){width="600" zoomable="yes"}

## Passaggio 4: impostare le commissioni di gestione

La tariffa di imballaggio è facoltativa e viene visualizzata come un costo aggiuntivo che viene aggiunto al costo di spedizione UPS. Se si desidera includere una tariffa di imballaggio, eseguire le operazioni seguenti:

1. Imposta **[!UICONTROL Calculate Handling Fee]** a uno dei seguenti metodi:

   - `Fixed`
   - `Percent`

1. Per determinare la modalità di applicazione della tariffa di imballaggio, impostare **[!UICONTROL Handling Applied]** a uno dei seguenti elementi:

   - `Per Order`
   - `Per Package`

1. Immetti l&#39;importo del **[!UICONTROL Handling Fee]** a carico.

   Per immettere una percentuale, utilizzare il formato decimale. Ad esempio, immetti `0.25` al 25%.

   ![Spese di imballaggio](./assets/ups3.png){width="600" zoomable="yes"}

## Passaggio 5: specificare i metodi consentiti e i paesi applicabili

1. Per **[!UICONTROL Allowed Methods]**, scegliere ogni metodo di spedizione UPS per essere disponibile ai clienti.

   I metodi vengono visualizzati in UPS durante il check-out. Per selezionare più metodi, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

1. Se desideri fornire un [Spedizione gratuita](shipping-free.md) tramite UPS, impostare le opzioni di spedizione gratuita:

   - Imposta **[!UICONTROL Free Method]** al metodo che si desidera utilizzare per la spedizione gratuita. Se non si desidera offrire la spedizione gratuita tramite UPS, scegliere `None`.

   - Per richiedere un importo minimo dell&#39;ordine che qualifichi un ordine per la spedizione gratuita con UPS, impostare **[!UICONTROL Enable Free Shipping Threshold]** a `Enable`. Quindi, inserisci il valore minimo in **[!UICONTROL Free Shipping Amount Threshold]**.

1. Se necessario, modificare il **[!UICONTROL Displayed Error Message]**.

   Questa casella di testo è preimpostata con un messaggio predefinito, ma è possibile immettere un messaggio diverso da visualizzare se UPS non è più disponibile.

   ![Metodi consentiti](./assets/ups4.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Ship to Applicable Countries]** a uno dei seguenti elementi:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione dell’archivio può utilizzare questo metodo di consegna.
   - `Specific Countries` - Quando si sceglie questa opzione, il _Spedisci a paesi specifici_ viene visualizzato. Seleziona ogni paese nell’elenco in cui può essere utilizzato questo metodo di consegna.

1. Imposta **[!UICONTROL Show Method if Not Applicable]** a uno dei seguenti elementi:

   - `Yes` - Elenca tutti i metodi di spedizione UPS disponibili durante il pagamento, inclusi i metodi non applicabili alla spedizione.
   - `No` - Elenca solo i metodi di spedizione UPS applicabili alla spedizione.

   ![Paesi applicabili](./assets/ups5.png){width="600" zoomable="yes"}

1. Per creare un file di registro con i dettagli delle spedizioni UPS effettuate dal tuo archivio, imposta **[!UICONTROL Debug]** a `Yes`.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui viene visualizzato il gruppo di continuità quando viene elencato con altri metodi di consegna durante il check-out.

   `0` = innanzitutto, `1` = secondo, `2` = terzo e così via.

1. Clic **[!UICONTROL Save Config]**.

## Passaggio 6: imposta l&#39;indirizzo di origine della spedizione

1. Assicurati che il tuo [Informazioni sul negozio](../getting-started/store-details.md#store-information) è stato completato.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e seleziona **[!UICONTROL Shipping Settings]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Origin]** sulla pagina e configura l’indirizzo dell’origine di spedizione.

   ![Configurazione vendite - opzioni indirizzo origine spedizione](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Commerce non dichiara il prezzo dell’ordine completo a UPS durante il calcolo delle spese di spedizione. Questo comportamento non può essere modificato.
