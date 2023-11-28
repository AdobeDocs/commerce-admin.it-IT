---
title: Assegnare la priorità alle origini di magazzino per un magazzino
description: Scopri come disporre le origini dall’alto verso il basso in ordine di priorità, utilizzato per determinare le detrazioni per spedizione e scorte.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Assegnazione di priorità alle origini per un magazzino

Dopo l’aggiunta [sorgenti](sources-manage.md) al [stock](stocks-manage.md), disponi tali origini dall’alto verso il basso in ordine di priorità per l’esecuzione degli ordini. L&#39;algoritmo SSA (Source Selection Algorithm) fornisce un algoritmo Priority che utilizza questo ordine per determinare le detrazioni di spedizione e di magazzino.

La priorità di origine sulle scorte non influenza le origini assegnate durante la modifica degli inventari dei prodotti.

In questo esempio, le origini di UK Stock vengono assegnate fuori servizio a un negozio, a due magazzini a Londra e a un magazzino a Berlino.

![Ordine di origine prima della definizione delle priorità](assets/inventory-priority-before.png){width="350" zoomable="yes"}

Il mercante preferisce avere spedizioni prioritarie dal più grande magazzino di Berlino, poi il magazzino di Londra, la posizione di traboccamento di Londra e infine la vetrina a Londra. Per modificare l&#39;ordine, le voci vengono trascinate nell&#39;ordine desiderato.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. Aprite il materiale grezzo in _Modifica_ modalità.

1. Espandi _[!UICONTROL Sources]_, se necessario.

1. Utilizzare ![Icona Ordina](assets/icon-sort.png) per trascinare e rilasciare le origini in una priorità dall&#39;alto (primo) al basso (ultimo).

   Questo ordine è importante per gli ordini di spedizione. SSA consiglia spedizioni in base all&#39;ordine delle origini

1. Clic **[!UICONTROL Save & Continue]** per salvare le modifiche.

![Ordine di origine dopo la definizione delle priorità](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
