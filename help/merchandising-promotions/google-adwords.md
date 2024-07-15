---
title: Google AdWords
description: Scopri come configurare il tuo store di Commerce per il tracciamento delle conversioni di Google AdWords per misurare i clic sugli annunci che portano a una vendita o ad altre azioni di valore.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Google AdWords

[Google AdWords][1] è un servizio che è possibile utilizzare per inserire annunci nei risultati di Google Search e nelle pagine delle aziende della Google Display Network. Il dashboard di AdWords include strumenti per gestire le campagne, tracciare le risposte e misurare i risultati.

Il tracciamento delle conversioni mostra il numero di clic dell’annuncio che hanno portato a una vendita o ad altre azioni di valore. La pagina _Operazione riuscita_ visualizzata dal cliente dopo l&#39;invio di un ordine viene utilizzata per tenere traccia delle conversioni, in quanto viene visualizzata solo dopo una vendita. Dopo aver completato la configurazione di Google AdWords per il tuo archivio, non è necessario copiare lo script di tracciamento della conversione nella pagina di successo, perché Commerce dispone già delle informazioni necessarie. Per ulteriori informazioni, consulta la [Guida di Google AdWords][2].

![Annuncio di Adobe nei risultati di ricerca di Google](./assets/google-adwords-adobe-ad.png){width="500"}

## Passaggio 1: Creare una campagna Google AdWords

1. Visita [Google AdWords][3] e registrati per un account.

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

   - Immettere il [codice esadecimale][4]{:target=&quot;_blank&quot;} per **[!UICONTROL Conversion Color]** che si desidera utilizzare per l&#39;etichetta di notifica Statistiche sito Google.

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

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
