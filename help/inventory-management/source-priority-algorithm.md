---
title: Configurare l’algoritmo di priorità sorgente
description: Scopri come configurare la priorità di origine utilizzata per l’ordine delle origini assegnate nell’inventario per creare consigli.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Configurare l’algoritmo di priorità sorgente

Le scorte personalizzate includono un elenco assegnato di origini per la vendita e la spedizione dell&#39;inventario dei prodotti disponibile tramite il punto vendita. Questo algoritmo utilizza l’ordine delle origini assegnate nel tuo stock per creare consigli.

Quando viene eseguito, l’algoritmo:

- Funziona in base all&#39;ordine configurato delle origini a livello di magazzino a partire dalla parte superiore

- Consiglia una quantità da spedire e di origine per prodotto in base all&#39;ordine nell&#39;elenco, alla quantità disponibile e alla quantità ordinata

- Continua verso il basso nell&#39;elenco fino al completamento della spedizione dell&#39;ordine

- Ignora le origini disabilitate se presenti nell&#39;elenco

Per configurare, disponi tali origini dall’alto verso il basso in priorità per l’esecuzione degli ordini. L&#39;algoritmo SSA (Source Selection Algorithm) fornisce un algoritmo Priority che utilizza questo ordine per determinare le detrazioni di spedizione e di magazzino. Consulta [Assegnazione di priorità alle origini per un Stock](stocks-prioritize-sources.md).

## Configurare la priorità delle origini

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Aprire un magazzino in modalità di modifica e passare alla _[!UICONTROL Sources]_area.

1. Clic **[!UICONTROL Assign Sources]**.

1. In _[!UICONTROL Assign Sources]_, selezionare la casella di controllo relativa all&#39;origine desiderata e quindi fare clic su **[!UICONTROL Done]**per assegnare un&#39;origine al materiale.

>[!NOTE]
>
>Quando si utilizza [Priorità distanza](distance-priority-algorithm.md) algoritmo per la spedizione, se route e dati non vengono restituiti per il [Modalità di calcolo](distance-priority-algorithm.md) (guida di veicoli, bicicletta o camminata) per una spedizione, la SSA utilizza per impostazione predefinita la Priorità origine.

![Ordine di origine dopo la definizione delle priorità](assets/inventory-stock-priority-after.png)

| Icone | Descrizione |
|----------------------------------------------|----------------------------------------------------------------|
| ![trascina l’icona per impostare la priorità](assets/icon-drag-and-drop-action.png) | Utilizza per trascinare e rilasciare le sorgenti in base alla priorità. |
| ![fai clic su icona per annullare l’assegnazione di un’origine](assets/icon-delete-action.png) | Annullamento dell&#39;assegnazione di un&#39;origine a un magazzino. |
