---
title: Guida [!DNL Inventory Management]
description: Guida di amministrazione e CLI per  [!DNL Inventory Management]  scorte, origini, quantità, configurazione, ordini e spedizioni in Adobe Commerce e Magento Open Source.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: a3817847081e56272e3677dede02d992e760a2d4
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 1%

---

# Panoramica di [!DNL Inventory Management]

Questa guida è destinata agli amministratori che gestiscono azioni in più posizioni in Adobe Commerce e Magento Open Source. Fornisce procedure di configurazione e gestione per il modulo [!DNL Inventory Management] e presuppone una conoscenza di base della funzionalità di base di [!DNL Commerce].

Utilizza **Admin** per le attività di configurazione, reporting e inventario giornaliere. Utilizza l&#39;**interfaccia della riga di comando** per l&#39;installazione, gli aggiornamenti e la configurazione back-end.

Questa guida tratta i seguenti argomenti:

| Oggetto | Descrizione |
| ------- | ----------- |
| [Introduzione](introduction.md) | Funzionalità, terminologia e adattamento di [!DNL Inventory Management] al tuo archivio. |
| [Note sulla versione](release-notes.md) | Cronologia delle versioni del modulo e problemi noti. |
| [Nozioni di base sull&#39;inventario](sources-stocks.md) | Concetti per [scorte e origini](sources-stocks.md), [selezione origine e prenotazioni](selection-reservations.md), [stato ordine e prenotazione](order-status.md) e [tipi di prodotto](product-types.md). |
| Introduzione | [Aggiornamenti di Commerce](migrate.md), [installazione e aggiornamenti](install-update.md), [tipi di origini esercente](merchant-sourcing.md) e [ristrutturazione inventario](expand-restructure.md). |
| [Configurazione](configuration.md) | Impostazioni globali, del prodotto e dell&#39;algoritmo per la visualizzazione e la spedizione della vetrina. |
| [Gestisci origini](sources-manage.md) | Creare e gestire le ubicazioni di evasione. |
| [Gestisci scorte](stocks-manage.md) | Mappare le origini ai canali di vendita. |
| [Gestione quantità](quantities-manage.md) | Assegnare e aggiornare le quantità di prodotti per origine. |
| [Gestione di ordini e spedizioni](shipments.md) | Esegue gli ordini e gestisce le spedizioni dal magazzino. |
| [Riferimento CLI](cli.md) | Attività di inventario e configurazione della riga di comando. |

{style="table-layout:auto"}

## Informazioni per sviluppatori

Accedi a risorse avanzate per API, personalizzazione e architettura dei moduli. Per informazioni tecniche sulle API e sulla personalizzazione dell&#39;algoritmo, vedere [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) nella documentazione per gli sviluppatori REST API.

## Documentazione di Commerce

Trova guide per esercenti, cloud e sviluppatori per aiutarti con ogni parte di Adobe Commerce. Utilizza queste risorse per qualsiasi esigenza di configurazione o gestione.

{{docs-links}}

## Risoluzione dei problemi e supporto

Utilizza articoli di supporto e sistemi di ticket per risolvere rapidamente i problemi di inventario. Ottieni ulteriore assistenza per lo stato delle scorte o la gestione del prodotto.

Se hai bisogno di informazioni o hai domande che non sono trattate in questa guida, utilizza le risorse seguenti:

- [Lo stato delle scorte non è corretto dopo l&#39;installazione del magazzino](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-29910)
- [Ticket di supporto](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#support-case) - Invia un ticket per ricevere ulteriore assistenza.
