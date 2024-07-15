---
title: Tipi di prodotto
description: Scopri come [!DNL Inventory Management] supporta la gestione degli inventari e degli ordini per tutti i tipi di prodotti Adobe Commerce e Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Tipi di prodotto

[!DNL Inventory Management] supporta la gestione dell&#39;inventario e degli ordini per tutti i tipi di prodotto in Adobe Commerce e Magento Open Source: semplice, configurabile, virtuale, scaricabile, bundle e raggruppato. Le opzioni e i requisiti possono variare in base al tipo di prodotto per origini, scorte e spedizioni.

- [I commercianti con una sola origine](merchant-sourcing.md#single-source-merchants) creano e aggiornano le impostazioni e le quantità dei prodotti senza richiedere ulteriori aggiornamenti. Tutti i prodotti creati e importati di recente vengono assegnati automaticamente al Source predefinito e al magazzino predefinito, immediatamente disponibili per i clienti se abilitati e in magazzino.

- [I commercianti multi-sorgente](merchant-sourcing.md#multi-source-merchants) assegnano origini, quantità per origine e impostazioni durante o dopo la creazione del prodotto. [!DNL Commerce] assegna tutti i nuovi prodotti importati al Source predefinito, richiedendo ulteriori modifiche per assegnare origini e quantità.

| Tipo di prodotto | Algoritmo di selezione spedizione e Source |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | Supporta i consigli e le sostituzioni SSA durante la spedizione. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | Supporta i consigli e le sostituzioni SSA durante la spedizione. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | Utilizza sempre il consiglio SSA. Il sistema esegue l&#39;algoritmo implicitamente quando crea le fatture e utilizza sempre i risultati suggeriti.<br/>Impossibile modificare questi risultati. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | Utilizza sempre il consiglio SSA. Il sistema esegue l&#39;algoritmo implicitamente quando crea le fatture e utilizza sempre i risultati suggeriti. <br/>Impossibile modificare questi risultati. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | Supporta i consigli e le sostituzioni SSA durante la spedizione. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | Supporta i consigli e le sostituzioni SSA durante la spedizione. |
