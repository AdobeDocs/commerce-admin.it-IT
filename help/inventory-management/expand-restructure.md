---
title: Espandere e ristrutturare l'inventario
description: Scopri come espanderlo a un commerciante multi-sorgente o ridurlo a un commerciante single-source.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/w4TV-BQrg0RzlHn4DVSdHFPD2M5CF11wA7I5OyA7jsY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# Espandere e ristrutturare l&#39;inventario

Con la crescita e il cambiamento dell&#39;azienda, [!DNL Inventory Management] supporta le tue esigenze. Puoi espanderlo a un commerciante multi-sorgente o ridurlo a un commerciante single-source con facilità.

## Espandi a multi-source

I commercianti single-source possono aggiungere nuovi negozi, magazzini, corrieri diretti e altro ancora. L’espansione richiede solo alcune aggiunte e alcuni aggiornamenti delle scorte per essere estesa al multi-sourcing:

1. Aggiungi [origini personalizzate](sources-add.md) per ogni nuova posizione.

   Per i prodotti Bundle si utilizza solo il Source predefinito.

1. Aggiungi [scorte personalizzate](stocks-add.md) in base alle esigenze per le nuove origini.

   Ad esempio, è possibile creare scorte per sito Web, paese, lingua o altro metodo. Puoi assegnare le origini alle tue scorte personalizzate. Per i prodotti in bundle si utilizza solo il magazzino predefinito.

1. Aggiorna [assegnazioni di origine e quantità](quantities-manage.md) per i prodotti.

   È inoltre possibile utilizzare lo strumento [Azioni di massa](bulk-assignment.md) e la funzionalità [Importa-Esporta](inventory-import-export.md) per aggiungere rapidamente origini e dati di prodotto.

## Ristrutturazione su fonte singola

Per i commercianti che desiderano ridurre le vendite online a un&#39;unica sede per la spedizione, modifica le origini, le scorte e le quantità per aggiornare:

1. Disabilita [origini personalizzate](sources-disable.md).

1. Trasferisci l’inventario dei prodotti al Source predefinito.

   Si consiglia di utilizzare azioni di massa. Vedere [Trasferimento dell&#39;inventario a Source](inventory-transfer.md).

1. Assegna tutti i siti Web a [Stock predefinito](stocks-manage.md).
