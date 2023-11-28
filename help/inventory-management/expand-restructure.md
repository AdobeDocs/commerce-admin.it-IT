---
title: Espandere e ristrutturare l'inventario
description: Scopri come espanderlo a un commerciante multi-sorgente o ridurlo a un commerciante single-source.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Espandere e ristrutturare l&#39;inventario

Man mano che l&#39;azienda cresce e cambia, [!DNL Inventory Management] supporta le tue esigenze. Puoi espanderlo a un commerciante multi-sorgente o ridurlo a un commerciante single-source con facilità.

## Espandi a multi-source

I commercianti single-source possono aggiungere nuovi negozi, magazzini, corrieri diretti e altro ancora. L’espansione richiede solo alcune aggiunte e alcuni aggiornamenti delle scorte per essere estesa al multi-sourcing:

1. Aggiungi [origini personalizzate](sources-add.md) per ogni nuova posizione.

   Per i prodotti Bundle viene utilizzata solo l&#39;origine predefinita.

1. Aggiungi [scorte personalizzate](stocks-add.md) in base alle esigenze per le nuove sorgenti.

   Ad esempio, è possibile creare scorte per sito Web, paese, lingua o altro metodo. Puoi assegnare le origini alle tue scorte personalizzate. Per i prodotti in bundle si utilizza solo il magazzino predefinito.

1. Aggiorna [assegnazioni di origine e quantità](quantities-manage.md) per i tuoi prodotti.

   È inoltre possibile utilizzare [Strumento Azioni di massa](bulk-assignment.md) e [Import-Export](inventory-import-export.md) per aggiungere rapidamente origini e dati di prodotto.

## Ristrutturazione su fonte singola

Per i commercianti che desiderano ridurre le vendite online a un&#39;unica sede per la spedizione, modifica le origini, le scorte e le quantità per aggiornare:

1. Disattiva [origini personalizzate](sources-disable.md).

1. Trasferisci l’inventario dei prodotti all’origine predefinita.

   Si consiglia di utilizzare azioni di massa. Consulta [Trasferimento del magazzino all&#39;origine](inventory-transfer.md).

1. Assegna tutti i siti Web a [Magazzino predefinito](stocks-manage.md).
