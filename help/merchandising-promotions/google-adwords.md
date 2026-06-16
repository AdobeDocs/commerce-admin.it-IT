---
title: Google AdWords
description: Scopri come configurare il tuo store di Commerce per il tracciamento delle conversioni di Google AdWords per misurare i clic sugli annunci che portano a una vendita o ad altre azioni di valore.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
TQID: https://experienceleague.adobe.com/QleYYt3Qc17JJjdUimL1iWfu-PYsx0OGWwfchMN3VVs
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 659
ht-degree: 0%

---

# Google AdWords

[Google AdWords](https://www.google.com/adwords/) è un servizio che è possibile utilizzare per inserire annunci nei risultati di Google Search e nelle pagine delle aziende della Google Display Network. Il dashboard di AdWords include strumenti per gestire le campagne, tracciare le risposte e misurare i risultati.

Il tracciamento delle conversioni mostra il numero di clic dell’annuncio che hanno portato a una vendita o ad altre azioni di valore. La pagina _Operazione riuscita_ visualizzata dal cliente dopo l&#39;invio di un ordine viene utilizzata per tenere traccia delle conversioni, in quanto viene visualizzata solo dopo una vendita. Dopo aver completato la configurazione di Google AdWords per il tuo archivio, non è necessario copiare lo script di tracciamento della conversione nella pagina di successo, perché Commerce dispone già delle informazioni necessarie. Per ulteriori informazioni, consulta la [Guida di Google AdWords](https://support.google.com/adwords/answer/6095821).

![Annuncio Adobe nei risultati di ricerca di Google](./assets/google-adwords-adobe-ad.png){width="500"}

## Passaggio 1: Creare una campagna Google AdWords

1. Visita [Google AdWords](https://ads.google.com/) e registrati per un account.

1. Segui le istruzioni per creare una campagna.

1. Per impostare il tracciamento delle conversioni per la campagna, effettua le seguenti operazioni:

   - Nella scheda **[!UICONTROL Tools]** del dashboard AdWords, scegli **[!UICONTROL Conversions]** e fai clic su **[!UICONTROL Conversion]**.

   - Quando viene richiesto l&#39;origine di conversione, scegliere **[!UICONTROL Website]**.

   - Immettere un nome per l&#39;azione di conversione da monitorare e fare clic su **[!UICONTROL Done]**.

   - Fare clic su **[!UICONTROL Value]** e, se applicabile, assegnare un valore alla conversione. Ad esempio:

      - Se si effettuano $5 per ogni vendita, scegliere `Each time it happens` e assegnare un valore di `$5`.
      - Se il valore di ciascuna vendita varia, lasciare vuoto il valore.

     Per completare, fare clic su **[!UICONTROL Done]**.

   - Fare clic su **[!UICONTROL Conversion windows]** e completare le impostazioni per determinare la durata del tracciamento delle conversioni, la categoria di reporting e il modello di attribuzione.

1. Al termine, fare clic su **[!UICONTROL Save and Continue]**.

## Passaggio 2: Ottieni il tag di conversione

1. In **[!UICONTROL Install your tag]** scegliere di contare le conversioni su **[!UICONTROL Page load]**.

1. In alternativa, è possibile aggiungere la notifica **[!UICONTROL Google Site Stats]** alla pagina di conversione.

   La notifica viene visualizzata nell’angolo inferiore con un collegamento agli standard di sicurezza e all’utilizzo dei cookie di Google.

1. Per scegliere la modalità di gestione del tag AdWords, eseguire una delle operazioni seguenti:

   - Se prevedi di aggiungere lo script al tuo store, scegli **[!UICONTROL Save instructions and tag]**.
   - Se si prevede che un altro utente aggiunga lo script al proprio archivio, scegliere **[!UICONTROL Email instructions and tag]**.

1. Al termine, fare clic su **[!UICONTROL Done]**.

## Passaggio 3: Configurare lo store

{{gtag-api-note}}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Se si configura Google AdWords per una visualizzazione archivio specifica, effettuare le seguenti operazioni:

   - Nell&#39;angolo in alto a sinistra, scegliere **[!UICONTROL Store View]** da configurare.

   - Quando viene richiesto di confermare il cambio di ambito, fare clic su **[!UICONTROL OK]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Google API]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Google AdWords]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Enable]** su `Yes`.

   - Immetti **[!UICONTROL Conversion ID]** dallo script Google AdWords.

   ![Configurazione vendite - API Google Ads](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Per formattare la notifica Google Sites Stat, effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Conversion Language]** sulla lingua identificata nello script Google AdWords.

   - Immettere **[!UICONTROL Conversion Format]** da utilizzare per la notifica di Google Sites Stat nella pagina di conversione.

      - `1` - Visualizza una notifica su una riga con un collegamento a ulteriori informazioni sul tracciamento di Google.
      - `2` - Visualizza una notifica su due righe con un collegamento a ulteriori informazioni sul tracciamento di Google.
      - `3` - Nessuna notifica del cliente.

   - Immettere il [codice esadecimale](https://www.w3schools.com/colors/colors_picker.asp){:target="_blank"} per **[!UICONTROL Conversion Color]** che si desidera utilizzare per l&#39;etichetta di notifica Statistiche sito Google.

   - Immettere il testo crittografato per **[!UICONTROL Conversion Label]** visualizzato nella notifica Google Sites Stat.

     Esempio: `MlEYCOKBnGoQz6CZoAM`

     **Codice tag Google AdWords di esempio**

     ```html
     <!-- Google Code for Back to School Sale Conversion Page -->
     <script type="text/javascript">
     /* <![CDATA[ */
     var google_conversion_id = 999999999;
     var google_conversion_language = "en";
     var google_conversion_format = "3";
     var google_conversion_color = "ffffff";
     var google_conversion_label = "MlEYCOKBnGoQz6CZoAM";
     var google_remarketing_only = false;
     /* ]]> */
     </script>
     
     <script type="text/javascript" src="//www.googleadservices.com/pagead/conversion.js">
     </script>
     <noscript>
     <div style="display:inline;">
     <img height="1" width="1" style="border-style:none;" alt="" src="//www.googleadservices.com/pagead/conversion/872829007/?label=MlEYCOKBnGoQz6CZoAM&amp;guid=ON&amp;script=0"/>
     
     </noscript>
     ```

1. Imposta **[!UICONTROL Conversion Value Type]** su uno dei seguenti:

   - `Dynamic` - Determina che si è verificata una conversione in base al valore dinamico dell&#39;importo dell&#39;ordine.
   - `Constant` - Determina che si è verificata una conversione in base a un valore specifico immesso.

   Per un tipo di valore di conversione _Constant_, immettere un valore di conversione **[!UICONTROL Value]** specifico per _[!UICONTROL Order Amount]_.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Passaggio 4: Verifica la configurazione

In poche ore lo stato di tracciamento nel dashboard di Google AdWords cambia da `Unverified` a `No recent conversions` o `Recording conversions`. Quando un utente fa clic sull’annuncio e effettua un acquisto, la conversione viene visualizzata nella pagina Azioni di conversione del dashboard e del rapporto della campagna.
