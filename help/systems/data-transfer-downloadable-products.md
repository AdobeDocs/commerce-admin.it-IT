---
title: Importare prodotti scaricabili
description: Rivedi un esempio di importazione di dati di prodotto per un prodotto scaricabile.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '172'
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

Per ulteriori informazioni sull&#39;attivazione e la gestione del modulo di archiviazione remota, vedere [Configurare l&#39;archiviazione remota](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html?lang=it) nella _Guida alla configurazione_.
