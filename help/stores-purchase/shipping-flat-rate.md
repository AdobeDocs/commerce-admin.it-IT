---
title: Spedizione a tariffa fissa
description: Scopri come impostare un’opzione di spedizione forfettaria per il tuo negozio.
exl-id: a6874509-a79b-42ab-aa93-d70d18fc33f6
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Spedizione a tariffa fissa

_Tariffa fissa_ è un addebito predefinito che può essere applicato per articolo o per spedizione. Tariffa fissa è una soluzione di spedizione semplice, soprattutto se utilizzata con l&#39;imballaggio forfettario disponibile presso alcuni vettori. Se attivato, _Tariffa fissa_ viene visualizzato come opzione durante l&#39;estrazione. Poiché non è specificato alcun gestore specifico, è possibile utilizzare un gestore scelto.

## Imposta spedizione a tariffa fissa

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Delivery Methods]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **Tariffa fissa**.

   ![Tariffa fissa](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedere [Tariffa fissa](../configuration-reference/sales/delivery-methods.md#flat-rate) nella _Guida di riferimento alla configurazione_.

1. Imposta **[!UICONTROL Enabled]** su `Yes`.

   Tariffa fissa viene visualizzata come opzione nella sezione Stima spedizione e imposte del carrello e anche nella sezione Spedizione durante il pagamento.

1. Immettere un **[!UICONTROL Title]** descrittivo per il metodo Tasso uniforme.

1. Immetti un **Nome metodo** da visualizzare accanto alla tariffa calcolata nel carrello.

   Il nome del metodo predefinito è `Fixed`. Se si addebita una tariffa di gestione, è possibile modificare il testo in `Plus Handling` o in un altro formato appropriato.

1. Per descrivere il modo in cui è possibile utilizzare la spedizione a tariffa fissa, impostare **Type** su uno dei seguenti valori:

   - `None` - Disabilita il tipo di pagamento. L&#39;opzione Tariffa fissa è elencata nel carrello, ma con un tasso pari a zero, che equivale alla spedizione gratuita.
   - `Per Order` - Addebita una singola tariffa fissa per l&#39;intero ordine.
   - `Per Item` - Addebita un singolo tasso forfettario per ogni elemento. La tariffa viene moltiplicata per il numero di articoli nel carrello, indipendentemente dal fatto che vi siano più quantità dello stesso articolo o di articoli diversi.

1. Immetti il **Prezzo** che desideri addebitare per la spedizione a tariffa fissa.

1. Configura le opzioni relative alle commissioni di gestione in base alle tue esigenze.

   La tariffa di imballaggio è facoltativa e viene visualizzata come un costo aggiuntivo che viene aggiunto alle spese di spedizione. Se si desidera includere una tariffa di imballaggio, eseguire le operazioni seguenti:

   - Per **Calcola commissione di gestione**, selezionare il metodo che si desidera utilizzare per calcolare le commissioni di gestione:

      - `Fixed`
      - `Percent`

   - Per **Spese di imballaggio**, immettere l&#39;importo da addebitare, in base al metodo scelto per calcolare l&#39;importo.

     Ad esempio, se l&#39;addebito è basato su una tariffa fissa, immettere l&#39;importo come decimale, ad esempio `4.90`. Tuttavia, se la tariffa di imballaggio si basa su una percentuale delle spese di spedizione, immettere l&#39;importo come percentuale. Ad esempio, se si sta addebitando il 6% delle spese di spedizione, immettere il valore come `6`.

1. Se necessario, modificare il **Messaggio di errore visualizzato**.

   Questa casella di testo è preimpostata con un messaggio predefinito, ma è possibile immettere un messaggio diverso da visualizzare se la spedizione a tariffa fissa non è più disponibile.

1. Imposta **Spedisci nei paesi applicabili**:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione dell&#39;archivio possono utilizzare questo metodo di consegna.
   - `Specific Countries` - Quando si sceglie questa opzione, viene visualizzato l&#39;elenco _Spedisci a paesi specifici_. Seleziona ogni paese nell’elenco in cui può essere utilizzato questo metodo di consegna.

1. Imposta **Mostra metodo se non applicabile**:

   - `Yes` - Mostra sempre il metodo Tasso uniforme, anche quando non applicabile.
   - `No` - Mostra il metodo Tasso forfettario solo se applicabile.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la sequenza di visualizzazione della spedizione a tariffa fissa quando viene elencata con altri metodi di consegna durante il pagamento.

   `0` = primo, `1` = secondo, `2` = terzo e così via.

1. Fare clic su **[!UICONTROL Save Config]**.
