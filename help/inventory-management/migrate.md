---
title: '[!DNL Commerce] aggiornamenti'
description: Scopri in che modo gli aggiornamenti di Adobe Commerce e Magento Open Source influiscono sulle configurazioni del catalogo e  [!DNL Inventory Management] .
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# [!DNL Commerce] aggiornamenti

Se in una versione precedente è stato utilizzato un inventario a origine singola, queste informazioni forniscono dettagli sulle nuove funzioni e sulle modifiche apportate alle configurazioni di catalogo e inventario esistenti.

[!DNL Inventory Management] per Adobe Commerce e Magento Open Source include funzionalità, miglioramenti e supporto per sviluppatori che migliorano e aggiornano la gestione di tutto il materiale di prodotto e aggiungono nuove funzionalità. Sono disponibili tutte le funzioni pronte all’uso, inclusi l’algoritmo di selezione di Source e l’estrazione concorrente, per abbinare le quantità degli ordini alle origini e all’evasione degli ordini. A seconda dei siti Web, dei negozi e del tipo di commerciante, è possibile creare scorte e origini aggiuntive, assegnare quantità di scorte e altro ancora. Per informazioni complete, vedere [Inventory management](introduction.md).

Quando installi Magento Open Source 2.4.x o Adobe Commerce 2.4.x, si verificano le seguenti modifiche iniziali:

- [Inventory management](enable.md) abilita a livello di archivio globale o di prodotto. L&#39;opzione Gestisci scorte consente o disabilita la registrazione delle quantità di magazzino, i calcoli delle quantità vendibili aggregate e la gestione delle prenotazioni per tenere traccia degli acquisti fino alla fattura e alla spedizione. È possibile disattivare questa opzione per utilizzare un ERP e altri servizi di terze parti per la gestione di scorte, ordini e spedizioni. Per ulteriori informazioni, vedere [!DNL Inventory Management] moduli di seguito.

- Aggiunta al sistema di [Source predefinito](sources-manage.md) e [Stock predefinito](stocks-manage.md). Non disattivare o rimuovere queste impostazioni predefinite. [!DNL Commerce] assegna i prodotti esistenti e quelli appena importati a questi valori predefiniti.

  >[!IMPORTANT]
  >
  >L&#39;utilizzo delle azioni predefinite e del Source predefinito è sconsigliato perché fanno parte del modulo `CatalogInventory`, che è ora obsoleto. Al suo posto, si consiglia di creare e utilizzare scorte e origini personalizzate.

   - Le scorte forniscono una quantità di vendita virtuale aggregata con prenotazioni per tenere traccia di carrelli e ordini, garantendo il pagamento simultaneo.

   - Tutti i prodotti esistenti nel catalogo vengono assegnati al Source predefinito. Fino a quando non aggiungi nuove sorgenti, l’interfaccia del prodotto non cambia. Se i prodotti vengono spediti da una sola ubicazione, non vi sono altre differenze per le origini. È possibile creare [origini](sources-add.md) e [assegnare quantità](quantities-manage.md) personalizzate per ubicazione di spedizione.

   - È possibile configurare un&#39;origine come ubicazione di prelievo e [assegnare quantità](quantities-manage.md) per tale origine.

   - Il tuo sito web assegna al titolo predefinito. Puoi creare [scorte](stocks-add.md) personalizzate per collegare i canali di vendita (siti Web) e le origini (località).

- [opzioni di configurazione](configuration.md) aggiuntive aggiunte ai prodotti e all&#39;archivio globale. Alcune opzioni di configurazione esistenti ricevono opzioni e comportamenti aggiornati:

   - Notify for Quantity Below invia notifiche e deduce dalla Quantità vendibile.

   - La soglia esaurita supporta gli importi positivi, zero e negativi. Con gli ordini inevasi abilitati, gli importi positivi vengono ignorati, considerati zero (o infinito).

   - Gli ordini in inevaso supportano gli importi zero (infinito) e negativi. Se l&#39;opzione è abilitata, la notifica per la quantità seguente non viene dedotta dalla quantità di vendita.

- Le nuove prenotazioni tengono traccia delle vendite potenziali, convertendo in detrazioni di quantità quando l&#39;ordine viene spedito. Non puoi mai accedere o creare prenotazioni direttamente. [!DNL Commerce] crea e gestisce le prenotazioni dietro le quinte tramite ordini, spedizioni e note di credito.

- [Ordini e spedizioni](shipments.md) includono nuove funzionalità per consigliare le spedizioni utilizzando l&#39;algoritmo di selezione Source e supportare le spedizioni parziali da più origini per evadere un ordine.

- Le nuove [funzioni di importazione/esportazione](inventory-import-export.md) consentono di aggiungere in massa sorgenti, aggiornare le quantità di magazzino e impostare lo stato delle scorte (in/out stock) per tutti gli SKU del catalogo. Queste funzioni consentono di modificare una, una o tutte le origini.

- Le nuove opzioni di massa nella pagina della griglia di prodotto supportano [l&#39;assegnazione e l&#39;annullamento dell&#39;assegnazione delle origini](bulk-assignment.md) e [il trasferimento dell&#39;inventario all&#39;origine](inventory-transfer.md).

- [!DNL Inventory Management] supporta i cataloghi B2B. Attualmente, tutti i prodotti B2B devono essere assegnati al Source predefinito e al Stock predefinito.

## [!DNL Commerce Order Management] e [!DNL Inventory Management]

[Commerce Order Management (MCOM)](https://commerce-docs.github.io/oms-documentation-archive/) non è compatibile con [!DNL Inventory Management]. Una volta installati, i moduli MCOM forniscono a [!DNL Commerce] tutte le funzionalità di gestione dell&#39;inventario, tra cui gestione di origini singole e multiple, scorte, prenotazioni e altro ancora. I moduli [!DNL Inventory Management] sono disabilitati per impostazione predefinita.

MCOM offre funzioni e servizi completi per la gestione degli ordini omnicanale avanzata, l&#39;inventario globale e il multi-sourcing, l&#39;evasione da magazzino a magazzino e l&#39;assistenza clienti centralizzata. Per un elenco completo delle funzionalità, vedere [Elenco delle funzionalità MCOM](https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/).

[!DNL Inventory Management] estende le funzionalità esistenti di [!DNL Commerce] con opzioni aggiuntive per tenere traccia degli ordini in-process, delle scorte disponibili, delle scorte disponibili per un magazzino e delle API per lo sviluppo di estensioni.

## [!DNL Inventory Management] moduli

Disabilitare [!DNL Inventory Management] moduli per:

- Velocizza l’aggiornamento dei commercianti che utilizzano Adobe Commerce o Magento Open Source 2.0/2.1/2.2/2.3 e la migrazione a 2.4.x.

- Utilizza moduli personalizzati o di terze parti per la gestione degli inventari e degli ordini.

- Utilizza [!DNL Order Management System] per la gestione dell&#39;inventario. Il connettore corrente non supporta [!DNL Inventory Management] interfacce. I commercianti OMS che eseguono l’aggiornamento ad Adobe Commerce 2.4.0 devono disattivare questi moduli.

Per informazioni dettagliate, vedere [Installa e aggiorna](install-update.md).
