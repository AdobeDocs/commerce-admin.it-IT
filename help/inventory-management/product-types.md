---
title: Tipi di prodotto
description: Scopri come [!DNL Inventory Management] supporta la gestione degli inventari e degli ordini per tutti i tipi di prodotti Adobe Commerce e Magento Open Source.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 213
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
