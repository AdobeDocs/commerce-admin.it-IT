---
title: Servizio postale degli Stati Uniti (USPS)
description: Scopri come impostare USPS come vettore di spedizione per il tuo negozio.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Servizio postale degli Stati Uniti (USPS)

Lo United States Postal Service è il servizio postale indipendente del governo degli Stati Uniti, che offre servizi di spedizione nazionali e internazionali via terra e via aria.

## Passaggio 1: aprire un account di spedizione USPS

Apri un [Strumenti Web USPS][1] account. Dopo aver completato il processo di registrazione, riceverai il tuo ID utente e un URL al server di test USPS.

Puoi anche aprire una [Strumenti Web USPS][1] account. Dopo aver completato il processo di registrazione, riceverai il tuo ID utente e un URL al server di test USPS. Per ulteriori informazioni sugli strumenti Web USPS, vedere [Documentazione tecnica][2].

## Passaggio 2: abilitare USPS per il tuo store

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Delivery Methods]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL USPS]** sezione.

   >[!NOTE]
   >
   >Se necessario, deselezionare **[!UICONTROL Use system value]** per modificare le seguenti impostazioni come descritto.

1. Imposta **[!UICONTROL Enabled for Checkout]** a `Yes`.

1. Se necessario, immettere **[!UICONTROL Gateway URL]** per accedere alle tariffe USPS.

   >[!IMPORTANT]
   >
   >A partire dal 24 giugno 2021, gli strumenti web USPS rimuoveranno il supporto per tutti gli endpoint HTTP non sicuri. Dopo questa modifica, tutte le richieste API di Strumenti Web inviate a un endpoint HTTP non sicuro avranno esito negativo. Assicurati che il tuo **[!UICONTROL Gateway URL]** utilizza l’endpoint HTTPS sicuro.

   Il campo è preimpostato per impostazione predefinita e normalmente non deve essere modificato.

1. Immetti un **[!UICONTROL Title]** per questo metodo di spedizione visualizzato durante il pagamento.

1. Inserisci il **[!UICONTROL User ID]** e **[!UICONTROL Password]** per il tuo account USPS.

1. Imposta **[!UICONTROL Mode]** a uno dei seguenti elementi:

   - `Development` : esegue USPS in un ambiente di test. Dopo aver eseguito USPS in un ambiente di sviluppo, assicurati di tornare più tardi e imposta la modalità su `Live`.
   - `Live` : esegue USPS in un ambiente di produzione live.

## Passaggio 3: completare la descrizione dell&#39;imballaggio

1. Per determinare la modalità di gestione dell&#39;ordine se inviato come più pacchetti, impostare **[!UICONTROL Packages Request Type]** a uno dei seguenti elementi:

   - `Divide to Equal Weight` - (Una richiesta) La spedizione di più colli può essere presentata come una richiesta se i colli sono divisi per peso uguale.
   - `Use Origin Weight` - (Richieste multiple) È necessario inviare più pacchetti come richieste separate se si utilizza il peso dell&#39;origine come base per il calcolo delle spese di spedizione.

1. Imposta **[!UICONTROL Container]** al tipo di imballaggio normalmente utilizzato per spedire i prodotti ordinati per il tuo negozio.

1. Imposta il **[!UICONTROL Size]** della confezione tipica spedita dal tuo negozio.

1. Imposta **[!UICONTROL Machinable]** a uno dei seguenti elementi:

   - `Yes` - Se il pacchetto tipico può essere elaborato da una macchina.
   - `No` - Se il pacchetto tipico deve essere elaborato manualmente.

1. Inserisci il **[!UICONTROL Maximum Package Weight]** in base alle esigenze del vettore.

   ![Impostazioni pacchetto USPS](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Passaggio 4: impostare le commissioni di gestione

La tariffa di movimentazione è facoltativa e viene visualizzata come un supplemento che viene aggiunto al costo di spedizione DHL. Se si desidera includere una tariffa di imballaggio, eseguire le operazioni seguenti:

1. Imposta **[!UICONTROL Calculate Handling Fee]** a uno dei seguenti metodi:

   - `Fixed`
   - `Percent`

1. Per determinare la modalità di applicazione della tariffa di imballaggio, impostare **[!UICONTROL Handling Applied]** a uno dei seguenti elementi:

   - `Per Order`
   - `Per Package`

1. Immetti l&#39;importo del **[!UICONTROL Handling Fee]** a carico.

   Per immettere una percentuale, utilizzare il formato decimale. Ad esempio, immetti `0.25` al 25%.

   ![Commissione di gestione USPS](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Passaggio 5: specificare i metodi consentiti e i paesi applicabili

1. Per **[!UICONTROL Allowed Methods]**, scegli ogni metodo di spedizione USPS per essere disponibile ai tuoi clienti.

   I metodi vengono visualizzati in USPS durante l&#39;estrazione. Per selezionare più metodi, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

1. Se desideri fornire un [Spedizione gratuita](shipping-free.md) tramite USPS, impostare le opzioni di spedizione gratuita:

   - Imposta **[!UICONTROL Free Method]** al metodo che si desidera utilizzare per la spedizione gratuita. Se non vuoi offrire la spedizione gratuita tramite USPS, scegli `None`.

   - Per richiedere un importo minimo dell&#39;ordine che qualifichi un ordine per la spedizione gratuita con USPS, impostare **[!UICONTROL Enable Free Shipping Threshold]** a `Enable`. Quindi, inserisci il valore minimo in **[!UICONTROL Free Shipping Amount Threshold]**.

1. Se necessario, modificare il **[!UICONTROL Displayed Error Message]**.

   Questa casella di testo è preimpostata con un messaggio predefinito, ma è possibile immettere un messaggio diverso da visualizzare se USPS non è più disponibile.

   ![Metodi consentiti USPS](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Ship to Applicable Countries]** a uno dei seguenti elementi:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione dell’archivio può utilizzare questo metodo di consegna.
   - `Specific Countries` - Quando si sceglie questa opzione, il _Spedisci a paesi specifici_ viene visualizzato. Seleziona ogni paese nell’elenco in cui può essere utilizzato questo metodo di consegna.

   ![Paesi USPS applicabili](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Show Method if Not Applicable]** a uno dei seguenti elementi:

   - `Yes` - Elenca tutti i metodi di spedizione USPS disponibili durante il pagamento, inclusi i metodi non applicabili alla spedizione.
   - `No` - Elenca solo i metodi di spedizione USPS applicabili alla spedizione.

1. Per creare un file di registro con i dettagli delle spedizioni USPS effettuate dal tuo archivio, imposta **[!UICONTROL Debug]** a `Yes`.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza in cui viene visualizzato USPS quando viene elencato con altri metodi di consegna durante il check-out.

   `0` = innanzitutto, `1` = secondo, `2` = terzo e così via.

1. Clic **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
