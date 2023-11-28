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

_Tariffa fissa_ è un addebito fisso predefinito che può essere applicato per articolo o per spedizione. Tariffa fissa è una soluzione di spedizione semplice, soprattutto se utilizzata con l&#39;imballaggio forfettario disponibile presso alcuni vettori. Quando è attivata, _Tariffa fissa_ viene visualizzato come opzione durante l&#39;estrazione. Poiché non è specificato alcun gestore specifico, è possibile utilizzare un gestore scelto.

## Imposta spedizione a tariffa fissa

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Delivery Methods]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **Tariffa fissa** sezione.

   ![Tariffa fissa](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedi [Tariffa fissa](../configuration-reference/sales/delivery-methods.md#flat-rate) nel _Guida di riferimento alla configurazione_.

1. Imposta **[!UICONTROL Enabled]** a `Yes`.

   Tariffa fissa viene visualizzata come opzione nella sezione Stima spedizione e imposte del carrello e anche nella sezione Spedizione durante il pagamento.

1. Inserisci un valore descrittivo **[!UICONTROL Title]** per il metodo Tariffa fissa.

1. Immetti un **Nome metodo** accanto alla tariffa calcolata nel carrello.

   Il nome del metodo predefinito è `Fixed`. Se si addebita una tariffa di imballaggio, è possibile modificare questo testo in `Plus Handling`o qualcos’altro che sia adatto.

1. Per descrivere il modo in cui è possibile utilizzare la spedizione a tariffa fissa, impostare **Tipo** a uno dei seguenti elementi:

   - `None` - Disattiva il tipo di pagamento. L&#39;opzione Tariffa fissa è elencata nel carrello, ma con un tasso pari a zero, che equivale alla spedizione gratuita.
   - `Per Order` - Addebita una singola tariffa fissa per l&#39;intero ordine.
   - `Per Item` - Addebita una singola tariffa forfettaria per ogni articolo. La tariffa viene moltiplicata per il numero di articoli nel carrello, indipendentemente dal fatto che vi siano più quantità dello stesso articolo o di articoli diversi.

1. Inserisci il **Prezzo** che si desidera addebitare per la spedizione a tariffa fissa.

1. Configura le opzioni relative alle commissioni di gestione in base alle tue esigenze.

   La tariffa di imballaggio è facoltativa e viene visualizzata come un costo aggiuntivo che viene aggiunto alle spese di spedizione. Se si desidera includere una tariffa di imballaggio, eseguire le operazioni seguenti:

   - Per **Calcola commissione di imballaggio**, selezionare il metodo che si desidera utilizzare per calcolare le tariffe di imballaggio:

      - `Fixed`
      - `Percent`

   - Per **Spese di imballaggio**, immettere l&#39;importo da addebitare, in base al metodo scelto per calcolare l&#39;importo.

     Ad esempio, se l&#39;addebito è basato su un addebito fisso, immettere l&#39;importo come decimale, ad esempio `4.90`. Tuttavia, se la tariffa di imballaggio si basa su una percentuale delle spese di spedizione, immettere l&#39;importo come percentuale. Ad esempio, se si sta addebitando il 6% delle spese di spedizione, immettere il valore come `6`.

1. Se necessario, modificare il **Messaggio di errore visualizzato**.

   Questa casella di testo è preimpostata con un messaggio predefinito, ma è possibile immettere un messaggio diverso da visualizzare se la spedizione a tariffa fissa non è più disponibile.

1. Imposta **Spedisci a paesi applicabili**:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione dell’archivio può utilizzare questo metodo di consegna.
   - `Specific Countries` - Quando si sceglie questa opzione, il _Spedisci a paesi specifici_ viene visualizzato. Seleziona ogni paese nell’elenco in cui può essere utilizzato questo metodo di consegna.

1. Imposta **Mostra metodo se non applicabile**:

   - `Yes` - Mostra sempre il metodo Tasso forfettario, anche quando non applicabile.
   - `No` - Mostra il metodo Tasso forfettario solo se applicabile.

1. Per **[!UICONTROL Sort Order]** Inserire un numero per determinare la sequenza di visualizzazione della spedizione a tariffa fissa quando viene elencata con altri metodi di consegna durante il pagamento.

   `0` = innanzitutto, `1` = secondo, `2` = terzo e così via.

1. Clic **[!UICONTROL Save Config]**.
