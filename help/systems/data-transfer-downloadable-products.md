---
title: Importare prodotti scaricabili
description: Rivedi un esempio di importazione di dati di prodotto per un prodotto scaricabile.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/a62y8GDLpN0PHxlm8EYHHMsHfzzkjB4mSNa-BV78Ra8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Importare prodotti scaricabili

Il flusso per l&#39;importazione dei prodotti scaricabili è lo stesso di [Prodotti in bundle](data-transfer-bundle-products.md) o [Prodotti configurabili](data-transfer-configurable-products.md). La differenza sta nel fatto che un prodotto scaricabile ha [collegamenti scaricabili](../catalog/product-create-downloadable.md) e [esempi scaricabili](../catalog/product-create-downloadable.md) con le relative immagini.

La directory principale predefinita per i collegamenti e gli esempi scaricabili è `<Magento-root-folder>/pub/media/import`. Se il modulo di archiviazione remota è abilitato, la directory principale predefinita per i collegamenti e gli esempi scaricabili è la directory `<remote-storage-root-folder>/media/import`.

Il file CSV contiene colonne separate per `downloadable_links` e `downloadable_samples`.

- **Immagini di collegamento scaricabili**. Nell&#39;esempio seguente, le immagini di collegamento scaricabili (`red.jpg` e `black.jpg`) si trovano nella cartella `<Magento-root-folder>/pub/media/import/test`. Se l&#39;archiviazione remota è abilitata, queste immagini si trovano nella cartella `<remote-storage-root-folder>/media/import/test`.

  ![Dati di esempio - prodotto scaricabile con collegamenti scaricabili](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Immagini di esempio scaricabili**. Nell&#39;esempio seguente, l&#39;immagine di esempio scaricabile (`white.jpg`) si trova nella cartella `<Magento-root-folder>/pub/media/import/test`. Se l&#39;archiviazione remota è abilitata, l&#39;immagine si trova nella cartella `<remote-storage-root-folder>/media/import/test`.

  ![Dati di esempio - prodotto scaricabile con esempi scaricabili](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Per ulteriori informazioni sull&#39;attivazione e la gestione del modulo di archiviazione remota, vedere [Configurare l&#39;archiviazione remota](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) nella _Guida alla configurazione_.
