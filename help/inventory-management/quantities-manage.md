---
title: Gestire le quantità di magazzino
description: Scopri come assegnare origini e quantità per nuovi prodotti o modificare prodotti esistenti.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/ykiHTLnzZGtJrRdp2wZvlL7YLbEb7iAiYlcbY8K7IX8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 325
ht-degree: 0%

---

# Gestire le quantità di magazzino

Le informazioni seguenti spiegano come assegnare le origini e le quantità per i nuovi prodotti o modificare quelli esistenti.

Durante la creazione dei prodotti, assegna origini e quantità. Per istruzioni complete, consulta [Creare un prodotto](../catalog/product-create.md). Queste pagine includono informazioni provenienti da una o più origini per le origini e le quantità per origine.

Quando si accede per la prima volta a un [!DNL Commerce] aggiornato con [!DNL Inventory Management], tutti i prodotti e le quantità vengono assegnati al Source predefinito. Quando si importano nuovi prodotti tramite il file .csv, questi vengono assegnati anche al Source predefinito.

I commercianti con una sola e più origini possono aggiornare le origini, le quantità di magazzino e le soglie per prodotto o in blocco.

- I commercianti con una sola origine possono aggiornare le quantità di prodotti per il Source predefinito. La quantità è il numero totale di prodotti disponibili per la vendita.

- I commercianti con più origini possono assegnare più origini e quantità per prodotto per ogni ubicazione (magazzini, magazzini, corrieri diretti e così via). Si consiglia di aggiungere le origini prima di impostare le quantità di scorte dei prodotti.

Quando si aggiungono origini e quantità ai prodotti, è possibile visualizzare le quantità tramite la griglia prodotti. Se il numero di origini è elevato, passare il cursore su _[!UICONTROL Quantity per Source]_&#x200B;per visualizzare l&#39;elenco completo e scorrevole delle origini con le quantità correnti.

![Quantità di prodotti per origine](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

Per assegnare le scorte ai prodotti, sono disponibili le seguenti opzioni:

- [Assegnazione di origini per prodotto](sources-assign-per-product.md) - Assegnazione manuale di origini per prodotto nel catalogo.

- [Assegnazione di quantità per prodotto](quantities-assign-per-product.md) - Aggiungere le scorte disponibili ai prodotti per origine. Queste informazioni sono specifiche per i venditori di più sorgenti.

- [Assegnazione in blocco e annullamento dell&#39;assegnazione di origini](bulk-assignment.md) - Assegnazione di origini ai prodotti selezionati come azione di massa. Utilizzare l&#39;opzione [Trasferisci inventario a Source](inventory-transfer.md) se si desidera trasferire le scorte e rimuovere l&#39;origine.

- [Trasferimento delle scorte in Source](inventory-transfer.md) - Trasferimento di massa di tutte le scorte da un&#39;origine a un&#39;origine di destinazione.

- [Importazione ed esportazione di quantità](inventory-import-export.md) - Utilizzare le funzioni di importazione ed esportazione per aggiornare più SKU di prodotto con le origini e le quantità di magazzino.
