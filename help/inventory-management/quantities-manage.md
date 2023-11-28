---
title: Gestire le quantità di magazzino
description: Scopri come assegnare origini e quantità per nuovi prodotti o modificare prodotti esistenti.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Gestire le quantità di magazzino

Le informazioni seguenti spiegano come assegnare le origini e le quantità per i nuovi prodotti o modificare quelli esistenti.

Durante la creazione dei prodotti, assegna origini e quantità. Consulta [Creare un prodotto](../catalog/product-create.md) per istruzioni complete. Queste pagine includono informazioni provenienti da una o più origini per le origini e le quantità per origine.

Quando si accede per la prima volta a un [!DNL Commerce] con [!DNL Inventory Management], tutti i prodotti e le quantità vengono assegnati all&#39;origine predefinita. Quando si importano nuovi prodotti tramite il file .csv, questi vengono assegnati anche all&#39;origine predefinita.

I commercianti con una sola e più origini possono aggiornare le origini, le quantità di magazzino e le soglie per prodotto o in blocco.

- I commercianti con una sola origine possono aggiornare le quantità di prodotti per l’origine predefinita. La quantità è il numero totale di prodotti disponibili per la vendita.

- I commercianti con più origini possono assegnare più origini e quantità per prodotto per ogni ubicazione (magazzini, magazzini, corrieri diretti e così via). Si consiglia di aggiungere le origini prima di impostare le quantità di scorte dei prodotti.

Quando si aggiungono origini e quantità ai prodotti, è possibile visualizzare le quantità tramite la griglia prodotti. Se il numero di sorgenti è elevato, passa il puntatore del mouse sull&#39;icona _[!UICONTROL Quantity per Source]_per visualizzare l&#39;elenco completo e scorrevole delle origini con le quantità correnti.

![Quantità di prodotti per origine](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

Per assegnare le scorte ai prodotti, sono disponibili le seguenti opzioni:

- [Assegnazione di origini per prodotto](sources-assign-per-product.md) : assegna manualmente le origini per prodotto nel catalogo.

- [Assegnazione di quantità per prodotto](quantities-assign-per-product.md) - Aggiungere le scorte disponibili ai prodotti per origine. Queste informazioni sono specifiche per i venditori di più sorgenti.

- [Assegnazione in blocco e annullamento dell&#39;assegnazione delle origini](bulk-assignment.md) - Assegna origini ai prodotti selezionati come azione di massa. Utilizza il [Trasferisci magazzino all&#39;origine](inventory-transfer.md) opzione se si desidera trasferire le scorte e rimuovere l&#39;origine.

- [Trasferimento del magazzino all&#39;origine](inventory-transfer.md) - Trasferire in massa tutto il magazzino da un&#39;origine a un&#39;origine di destinazione.

- [Importazione ed esportazione di quantità](inventory-import-export.md) : utilizza le funzioni di importazione ed esportazione per aggiornare più SKU di prodotto con origini e quantità di magazzino.
