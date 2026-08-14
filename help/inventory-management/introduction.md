---
title: Introduzione a  [!DNL Inventory Management]
description: Scopri come utilizzare  [!DNL Inventory Management] for [!DNL Commerce] per gestire le scorte tra origini e scorte, calcolare le quantità vendibili, tenere traccia delle prenotazioni e supportare l'evasione degli ordini. Utilizza l’amministratore per configurare le impostazioni e generare rapporti, nonché l’interfaccia della riga di comando per le modifiche di configurazione e in background.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
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
source-git-commit: 125a49f740639bce0ced8063074ca43d627c0eac
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 0%

---

# Introduzione a [!DNL Inventory Management]

[!DNL Inventory Management] per [!DNL Commerce] consente ai commercianti di gestire l&#39;inventario in uno o più siti Web e posizioni di prodotti fisici o virtuali. Fornisce strumenti nell&#39;interfaccia di amministrazione e nella riga di comando per configurare le scorte, tenere traccia delle quantità disponibili e aggregare le quantità vendibili, proteggere le scorte durante il pagamento e supportare l&#39;evasione degli ordini. È possibile utilizzare [!DNL Inventory Management] per una singola origine o una rete multi-origine che include magazzini, ubicazioni di prelievo, corrieri e altre ubicazioni di evasione.

## Modalità di utilizzo di [!DNL Inventory Management]

- **Amministratore:** Imposta le opzioni di inventario e genera i rapporti di inventario.
- **Interfaccia della riga di comando:** Eseguire i comandi di installazione e applicare le modifiche di inventario in background.
- **Ambito di configurazione:** Configurare le impostazioni di inventario a livello globale, per origine o per prodotto.

## Funzioni principali

Le funzionalità di [!DNL Inventory Management] includono:

- Configurazioni diverse per i commercianti il cui inventario proviene da un’unica origine o da più origini
- Scorte per la registrazione delle quantità vendibili aggregate tra le origini assegnate
- Protezione da estrazione simultanea
- Algoritmi di abbinamento delle spedizioni che supportano i consigli di evasione in base alla distanza o alla priorità

>[!NOTE]
>
>Queste funzionalità sono state sviluppate come parte del progetto [Inventory management](https://github.com/magento/inventory) (precedentemente MSI) tramite il programma di progettazione della community.<br/>
>
>Il modulo [!DNL Inventory Management] è installato con Magento Open Source e Adobe Commerce, con tutte le funzionalità abilitate per impostazione predefinita. Per informazioni sulle modifiche incluse nelle versioni dei moduli, consulta le [Note sulla versione](release-notes.md).

## Terminologia di base

È importante comprendere i seguenti termini mentre si lavora con [!DNL Inventory Management]:

[!UICONTROL Sources] rappresentano le posizioni fisiche che archiviano e spediscono i prodotti disponibili. Vedere [Scorte e origini](sources-stocks.md) per esempi e diagrammi. Qualsiasi posizione può essere designata come origine per i prodotti virtuali.

[!UICONTROL Stocks] mappa un canale di vendita (attualmente limitato a siti Web) alle posizioni di origine e alle scorte disponibili. Un titolo può essere associato a più canali di vendita, ma un canale di vendita può essere assegnato a un solo titolo.

[!UICONTROL Aggregate Salable Quantity] è l&#39;inventario virtuale totale che può essere venduto tramite un canale di vendita. L&#39;importo viene calcolato in tutte le origini assegnate a una scorta.

[!UICONTROL Reservations] traccia le detrazioni dalla quantità vendibile quando i clienti aggiungono prodotti ai carrelli e completano il pagamento. Quando un ordine viene spedito, la prenotazione cancella e deduce gli importi spediti dalle quantità di magazzino di origine specifiche.
