---
title: Configurare l’algoritmo Source Priority
description: Scopri come configurare la priorità di origine utilizzata per l’ordine delle origini assegnate nell’inventario per creare consigli.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
TQID: https://experienceleague.adobe.com/TB4THYjkzbNvEbsjNzOewNtYS6JoRvLDiQQCovSMkbI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# Configurare l’algoritmo Source Priority

Le scorte personalizzate includono un elenco assegnato di origini per la vendita e la spedizione dell&#39;inventario dei prodotti disponibile tramite il punto vendita. Questo algoritmo utilizza l’ordine delle origini assegnate nel tuo stock per creare consigli.

Quando viene eseguito, l’algoritmo:

- Funziona in base all&#39;ordine configurato delle origini a livello di magazzino a partire dalla parte superiore

- Consiglia una quantità da spedire e di origine per prodotto in base all&#39;ordine nell&#39;elenco, alla quantità disponibile e alla quantità ordinata

- Continua verso il basso nell&#39;elenco fino al completamento della spedizione dell&#39;ordine

- Ignora le origini disabilitate se presenti nell&#39;elenco

Per configurare, disponi tali origini dall’alto verso il basso in priorità per l’esecuzione degli ordini. L&#39;algoritmo di selezione Source (SSA) fornisce un algoritmo Priorità che utilizza questo ordine per determinare le detrazioni di spedizione e di magazzino. Vedi [Assegnazione di priorità alle origini per un Stock](stocks-prioritize-sources.md).

## Configurare la priorità delle origini

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Aprire un magazzino in modalità di modifica e passare all&#39;area _[!UICONTROL Sources]_.

1. Fare clic su **[!UICONTROL Assign Sources]**.

1. Nella visualizzazione _[!UICONTROL Assign Sources]_, selezionare la casella di controllo per l&#39;origine richiesta, quindi fare clic su **[!UICONTROL Done]**&#x200B;per assegnare un&#39;origine al titolo.

>[!NOTE]
>
>Quando si utilizza l&#39;algoritmo [Distance Priority](distance-priority-algorithm.md) per la spedizione, se le route e i dati non vengono restituiti per la [Modalità di calcolo](distance-priority-algorithm.md) selezionata (guida, bicicletta o camminata) per una spedizione, il valore predefinito di SSA è Source Priority.

![Ordine Source dopo la definizione delle priorità](assets/inventory-stock-priority-after.png)

| Icone | Descrizione |
|----------------------------------------------|----------------------------------------------------------------|
| ![trascina l&#39;icona per impostare la priorità](assets/icon-drag-and-drop-action.png) | Utilizza per trascinare e rilasciare le sorgenti in base alla priorità. |
| ![fai clic sull&#39;icona per annullare l&#39;assegnazione di un&#39;origine](assets/icon-delete-action.png) | Annullamento dell&#39;assegnazione di un&#39;origine a un magazzino. |
