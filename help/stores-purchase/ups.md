---
title: United Parcel Service (UPS)
description: Scopri come impostare UPS come corriere per il tuo negozio.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: a925827f2d939eeb9e6b3e57c023792ae358cbfc
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) offre servizi di spedizione nazionali e internazionali via terra e via aria a più di 220 paesi.

{{ups-api}}

>[!NOTE]
>
>UPS può utilizzare [peso dimensionale](carriers.md#dimensional-weight) per determinare alcune tariffe di spedizione. Tuttavia, Adobe Commerce supporta solo il calcolo delle spese di spedizione in base al peso.

## Passaggio 1: aprire un conto di spedizione UPS

Per offrire questo metodo di spedizione ai clienti, è necessario prima aprire un account UPS e completare l&#39;applicazione per ottenere un numero di conto Corriere. Vedere [Aprire un account UPS gratuito](https://www.ups.com/us/en/business-solutions/open-an-account).

## Passaggio 2: ottenere le credenziali OAUTH UPS

Segui i passaggi descritti nella [Guida introduttiva alle API UPS](https://developer.ups.com/get-started) per ottenere le credenziali API (ID client e segreto client) necessarie per abilitare l&#39;integrazione UPS. Per ottenere le credenziali è necessario creare un&#39;applicazione UPS.

Quando si configurano le impostazioni del gruppo di continuità nell&#39;amministratore, utilizzare i valori delle credenziali per `username` e `password`.

## Passaggio 3: abilitare UPS per il tuo store

1. Nella barra laterale _Admin_, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, in **[!UICONTROL Sales]**, scegli **[!UICONTROL Delivery Methods]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL UPS]**.

1. Imposta **[!UICONTROL Enabled for Checkout]** su `Yes`.

1. Per un account REST UPS (impostazione predefinita), effettuare le seguenti operazioni:

   - Immettere le credenziali del gruppo di continuità: ID client gruppo di continuità come **[!UICONTROL User ID]**, segreto client gruppo di continuità come **[!UICONTROL Password]**.

   - Impostare **[!UICONTROL Mode]** su `Live` per inviare dati al sistema di spedizione UPS tramite una connessione protetta. La modalità di sviluppo non invia dati tramite una connessione protetta.

   - Verificare **[!UICONTROL Gateway URL]** necessario per inviare le richieste. Utilizza un URL sandbox (`https://wwwcie.ups.com/api/rating/`) per la modalità di test e un URL di produzione per le richieste live (`https://onlinetools.ups.com/api/rating/`). Assicurati di utilizzare i rispettivi endpoint per ogni richiesta con l’host specificato.

   - Verificare **[!UICONTROL Tracking URL]** necessario per ottenere le informazioni di tracciamento. Utilizza un URL sandbox (`https://wwwcie.ups.com/api/track/`) per la modalità di test e un URL di produzione per le richieste live (`https://onlinetools.ups.com/api/track/`). Assicurati di utilizzare i rispettivi endpoint per ogni richiesta con l’host specificato.

   - Impostare **[!UICONTROL Origin of the Shipment]** sull&#39;area di origine della spedizione.

   - Se si dispone di tariffe speciali con UPS, impostare **[!UICONTROL Enable Negotiated Rates]** su `Yes` e immettere le sei cifre **[!UICONTROL Shipper Number]** assegnate da UPS.

   - Imposta **[!UICONTROL Live Account]** su uno dei seguenti:

      - `Yes` - Esegue UPS in modalità di produzione e offre UPS come metodo di spedizione ai tuoi clienti. Assicurati di utilizzare gli endpoint corretti in URL gateway e URL di tracciamento.
      - `No` - Esegue UPS in modalità di test. Assicurati di utilizzare gli endpoint corretti in URL gateway e URL di tracciamento.

   >[!NOTE]
   >
   >Il tipo di servizio United Parcel Service standard è impostato come obsoleto. Per le nuove configurazioni, utilizzare il tipo predefinito `United Parcel Service REST`. È inoltre necessario il tipo REST per generare [etichette di spedizione](shipping-labels.md).<br/>
   >Per la versione 2.4.7, **[!UICONTROL UPS Type]** è stato rimosso perché i tipi `UPS` e `UPS XML` sono pianificati per l&#39;obsolescenza e `UPS REST` è l&#39;impostazione predefinita. Le API di United Parcel Service (UPS) utilizzate dall’integrazione nativa di Adobe Commerce sono temporaneamente obsolete perché non supportano attualmente il modello di sicurezza OAuth 2.0.

   >[!IMPORTANT]
   >
   >UPS sta interrompendo il supporto di HTTP, utilizzato nell’impostazione predefinita corrente (valore di sistema). Deselezionare la casella di controllo **[!UICONTROL Use system value]** e modificare l&#39;URL per utilizzare HTTPS. Esempio: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Per **[!UICONTROL Title]**, immettere il nome dell&#39;opzione di spedizione che si desidera venga visualizzata durante l&#39;estrazione.

   Per impostazione predefinita, questo campo è impostato su `United Parcel Service`.

   ![Abilita UPS](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Passaggio 3: completare la descrizione del contenitore

1. Imposta **[!UICONTROL Packages Request Type]** su uno dei seguenti:

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

1. Impostare **[!UICONTROL Weight Unit]** sul sistema utilizzato per misurare il peso del prodotto.

   Il sistema di peso supportato da UPS varia in base al paese. In caso di dubbi, chiedere a UPS quale sistema di peso deve utilizzare. Le opzioni includono:

   - `LBS`
   - `KGS`

1. Imposta **[!UICONTROL Destination Type]** su uno dei seguenti:

   - `Residential` - La maggior parte delle spedizioni è da business a consumer (B2C).
   - `Commercial` - La maggior parte delle spedizioni sono business to business (B2B).

1. Immetti il **[!UICONTROL Maximum Package Weight]** consentito dal gestore.

1. Imposta **[!UICONTROL Pickup Method]** su uno dei seguenti:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Immetti il **[!UICONTROL Minimum Package Weight]** consentito dal gestore.

   ![Descrizione contenitore](./assets/ups2.png){width="600" zoomable="yes"}

## Passaggio 5: impostare le commissioni di gestione

La tariffa di imballaggio è facoltativa e viene visualizzata come un costo aggiuntivo che viene aggiunto al costo di spedizione UPS. Se si desidera includere una tariffa di imballaggio, eseguire le operazioni seguenti:

1. Impostare **[!UICONTROL Calculate Handling Fee]** su uno dei metodi seguenti:

   - `Fixed`
   - `Percent`

1. Per determinare la modalità di applicazione della tariffa di gestione, impostare **[!UICONTROL Handling Applied]** su uno dei seguenti valori:

   - `Per Order`
   - `Per Package`

1. Immettere l&#39;importo di **[!UICONTROL Handling Fee]** da addebitare.

   Per immettere una percentuale, utilizzare il formato decimale. Ad esempio, immettere `0.25` per il 25%.

   ![Spese di gestione](./assets/ups3.png){width="600" zoomable="yes"}

## Passaggio 6: specificare i metodi consentiti e i paesi applicabili

1. Per **[!UICONTROL Allowed Methods]**, scegliere ogni metodo di spedizione UPS per renderlo disponibile ai clienti.

   I metodi vengono visualizzati in UPS durante il check-out. Per selezionare più metodi, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

1. Se desideri fornire un&#39;opzione [Spedizione gratuita](shipping-free.md) tramite UPS, imposta le opzioni di spedizione gratuita:

   - Impostare **[!UICONTROL Free Method]** sul metodo da utilizzare per la spedizione gratuita. Se non si desidera offrire la spedizione gratuita tramite UPS, scegliere `None`.

   - Per richiedere un importo minimo dell&#39;ordine che qualifichi un ordine per la spedizione gratuita con UPS, impostare **[!UICONTROL Enable Free Shipping Threshold]** su `Enable`. Immettere quindi il valore minimo in **[!UICONTROL Free Shipping Amount Threshold]**.

1. Se necessario, modificare **[!UICONTROL Displayed Error Message]**.

   Questa casella di testo è preimpostata con un messaggio predefinito, ma è possibile immettere un messaggio diverso da visualizzare se UPS non è più disponibile.

   ![Metodi consentiti](./assets/ups4.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Ship to Applicable Countries]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione dell&#39;archivio possono utilizzare questo metodo di consegna.
   - `Specific Countries` - Quando si sceglie questa opzione, viene visualizzato l&#39;elenco _Spedisci a paesi specifici_. Seleziona ogni paese nell’elenco in cui può essere utilizzato questo metodo di consegna.

1. Imposta **[!UICONTROL Show Method if Not Applicable]** su uno dei seguenti:

   - `Yes` - Elenca tutti i metodi di spedizione UPS disponibili durante il pagamento, inclusi i metodi non applicabili alla spedizione.
   - `No` - Elenca solo i metodi di spedizione UPS applicabili alla spedizione.

   ![Paesi applicabili](./assets/ups5.png){width="600" zoomable="yes"}

1. Per creare un file di registro con i dettagli delle spedizioni UPS effettuate dal tuo archivio, imposta **[!UICONTROL Debug]** su `Yes`.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza di visualizzazione del gruppo di continuità quando viene elencato con altri metodi di consegna durante l&#39;estrazione.

   `0` = primo, `1` = secondo, `2` = terzo e così via.

1. Fare clic su **[!UICONTROL Save Config]**.

## Passaggio 7: imposta l&#39;indirizzo di origine della spedizione

1. Assicurati che le [Informazioni sullo store](../getting-started/store-details.md#store-information) siano state completate.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e seleziona **[!UICONTROL Shipping Settings]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Origin]** nella pagina e configurare l&#39;indirizzo di origine della spedizione.

   ![Configurazione vendite - opzioni indirizzo origine spedizione](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Commerce non dichiara il prezzo dell&#39;ordine completo a UPS durante il calcolo delle spese di spedizione. Questo comportamento non può essere modificato.
