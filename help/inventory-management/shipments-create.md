---
title: Creazione di spedizioni multi-source
description: Scopri in che modo i commercianti multi-source possono creare e inviare spedizioni.
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Creazione di spedizioni multi-source

Con [!DNL Inventory Management], invia una o più spedizioni con l&#39;inventario. Per generare ulteriori spedizioni in base alle necessità, ripetere queste istruzioni utilizzando le quantità e le origini consigliate o inserite manualmente. Queste istruzioni descrivono in dettaglio il modo in cui i commercianti multi-sorgente inviano le spedizioni. I commercianti con una sola origine inviano le spedizioni senza questi passaggi aggiuntivi (consulta [Creare una spedizione](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} nella guida utente di base).

Durante la creazione delle spedizioni, utilizza l&#39;algoritmo di selezione origine per i consigli calcolati. Segui e utilizza questi consigli o imposta gli importi per origine, generando spedizioni personalizzate. È possibile controllare le scorte in uscita per ogni ordine, impostando gli importi da detrarre, inviando una o più spedizioni e consegnando scorte e ordini inevasi quando le scorte sono disponibili. Per ogni voce dell&#39;ordine, inserire un importo da detrarre dalla quantità di origine.

È possibile inviare spedizioni parziali a:

- Esegui ordini inevasi all&#39;arrivo del magazzino

- Saldo detrazioni magazzino tra origini

Quando si inseriscono le spedizioni, le quantità di scorte disponibili detraggono gli importi inseriti. In effetti, le prenotazioni vengono convertite in detrazioni quantità effettive.

## Creare una spedizione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Individuare l&#39;ordine e aprirlo in modalità di visualizzazione.

1. Se l&#39;ordine è stato pagato e fatturato ed è pronto per la spedizione, fare clic su **[!UICONTROL Ship]**.

1. Completa la selezione origine per l’invio di prodotti per origine:

   - Per visualizzare i consigli di spedizione, fai clic su **[!UICONTROL Source Selection Algorithm]** e seleziona un algoritmo.

     | Algoritmo | Descrizione |
     |--|--|
     | [Priorità origine](source-priority-algorithm.md) | Consiglia le spedizioni dalle origini in base agli ordini delle origini assegnate alle scorte. |
     | [Priorità distanza](distance-priority-algorithm.md) | Consiglia le spedizioni dalle origini più vicine all&#39;indirizzo di spedizione in base alla distanza fisica o al tempo di consegna più breve. |

     >[!IMPORTANT]
     >
     >Quando si utilizza l’algoritmo di priorità distanza per la spedizione e le route e i dati non vengono restituiti per la selezionata [Modalità di calcolo](distance-priority-algorithm.md) (guida di veicoli, bicicletta o camminata) per una spedizione, il valore predefinito di SSA è Source Priority (Priorità origine). Si consiglia inoltre di impostare [priorità per le fonti per stock](stocks-prioritize-sources.md).


   - Per  **[!UICONTROL Select a Source to Ship from]**, selezionare un&#39;origine per inviare una spedizione.

   - Per ogni voce, mantenere l&#39;importo consigliato o inserire un importo specifico nella **[!UICONTROL Qty to Deduct]**. Questo valore specifica l&#39;importo dedotto dal magazzino dell&#39;origine selezionata.

   - Clic **[!UICONTROL Proceed to Shipment]**.

     ![Selezionare un&#39;origine e inserire una quantità](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. Rivedi _[!UICONTROL New Shipment]_e inserisci eventuali modifiche aggiuntive, se necessario.

   Il _[!UICONTROL Inventory]_Questa sezione mostra l&#39;origine, la spedizione dei prodotti, la quantità ordinata totale e la quantità da spedire.

   ![Dettagli di magazzino per la spedizione, ad esempio spedizione parziale](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. Clic **[!UICONTROL Submit Shipment]** per completare.
