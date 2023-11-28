---
title: '''[!DNL Commerce] aggiornamenti"'
description: Scopri in che modo gli aggiornamenti di Adobe Commerce e Magento Open Source influiscono su cataloghi e [!DNL Inventory Management] configurazioni.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# [!DNL Commerce] aggiornamenti

Se in una versione precedente è stato utilizzato un inventario a origine singola, queste informazioni forniscono dettagli sulle nuove funzioni e sulle modifiche apportate alle configurazioni di catalogo e inventario esistenti.

[!DNL Inventory Management] per Adobe Commerce e Magento Open Source include funzioni, miglioramenti e supporto per sviluppatori che migliorano e aggiornano la gestione di tutto il stock di prodotto e aggiungono nuove funzioni. Sono disponibili tutte le funzioni pronte all’uso, inclusi l’algoritmo di selezione dell’origine e l’estrazione concorrente, per abbinare le quantità degli ordini alle origini e all’evasione degli ordini. A seconda dei siti Web, dei negozi e del tipo di commerciante, è possibile creare scorte e origini aggiuntive, assegnare quantità di scorte e altro ancora. Per informazioni complete vedi [Inventory management](introduction.md).

Quando si installa Magento Open Source 2.4.x o Adobe Commerce 2.4.x, si verificano le seguenti modifiche iniziali:

- [Inventory management](enable.md) abilita a livello di store globale o prodotto. L&#39;opzione Gestisci scorte consente o disabilita la registrazione delle quantità di magazzino, i calcoli delle quantità vendibili aggregate e la gestione delle prenotazioni per tenere traccia degli acquisti fino alla fattura e alla spedizione. È possibile disattivare questa opzione per utilizzare un ERP e altri servizi di terze parti per la gestione di scorte, ordini e spedizioni. Per ulteriori informazioni, consulta [!DNL Inventory Management] Moduli di seguito.

- A [Origine predefinita](sources-manage.md) e [Magazzino predefinito](stocks-manage.md) aggiungi al sistema. Non disattivare o rimuovere queste impostazioni predefinite. [!DNL Commerce] assegna i prodotti esistenti e quelli appena importati a questi valori predefiniti.

  >[!IMPORTANT]
  >
  >L&#39;utilizzo delle scorte di default e dell&#39;origine di default è fortemente sconsigliato perché fanno parte del `CatalogInventory` , che ora è diventato obsoleto. Al suo posto, si consiglia di creare e utilizzare scorte e origini personalizzate.

   - Le scorte forniscono una quantità di vendita virtuale aggregata con prenotazioni per tenere traccia di carrelli e ordini, garantendo il pagamento simultaneo.

   - Tutti i prodotti esistenti nel catalogo vengono assegnati all&#39;origine predefinita. Fino a quando non aggiungi nuove sorgenti, l’interfaccia del prodotto non cambia. Se i prodotti vengono spediti da una sola ubicazione, non vi sono altre differenze per le origini. Puoi creare personalizzati [sorgenti](sources-add.md) e [assegna quantità](quantities-manage.md) per ubicazione di spedizione.

   - È possibile configurare un’origine come Posizione di prelievo e [assegna quantità](quantities-manage.md) per quella sorgente.

   - Il tuo sito web assegna al titolo predefinito. Puoi creare personalizzati [scorte](stocks-add.md) per collegare i canali di vendita (siti web) e le fonti (ubicazioni).

- Aggiuntivo [opzioni di configurazione](configuration.md) aggiungi ai tuoi prodotti e al negozio globale. Alcune opzioni di configurazione esistenti ricevono opzioni e comportamenti aggiornati:

   - Notify for Quantity Below invia notifiche e deduce dalla Quantità vendibile.

   - La soglia esaurita supporta gli importi positivi, zero e negativi. Con gli ordini inevasi abilitati, gli importi positivi vengono ignorati, considerati zero (o infinito).

   - Gli ordini in inevaso supportano gli importi zero (infinito) e negativi. Se l&#39;opzione è abilitata, la notifica per la quantità seguente non viene dedotta dalla quantità di vendita.

- Le nuove prenotazioni tengono traccia delle vendite potenziali, convertendo in detrazioni di quantità quando l&#39;ordine viene spedito. Non puoi mai accedere o creare prenotazioni direttamente. [!DNL Commerce] crea e gestisce le prenotazioni dietro le quinte tramite ordini, spedizioni e note di credito.

- [Ordini e spedizioni](shipments.md) includere nuove funzioni per consigliare le spedizioni utilizzando l&#39;algoritmo di selezione origine e supportare le spedizioni parziali da più origini per evadere un ordine.

- Nuovo [funzioni di importazione/esportazione](inventory-import-export.md) consente di aggiungere in massa le origini, aggiornare le quantità di magazzino e impostare lo stato delle scorte (in/out stock) per tutti gli SKU del catalogo. Queste funzioni consentono di modificare una, una o tutte le origini.

- Le nuove opzioni per la modifica in serie nella pagina della griglia di prodotto supportano la modifica in serie [assegnazione e annullamento dell&#39;assegnazione delle origini](bulk-assignment.md), e [trasferimento del magazzino all&#39;origine](inventory-transfer.md).

- [!DNL Inventory Management] supporta i cataloghi B2B. Attualmente, tutti i prodotti B2B devono essere assegnati all&#39;origine predefinita e alle scorte predefinite.

## [!DNL Commerce Order Management] e [!DNL Inventory Management]

[Gestione ordini Commerce (MCOM)][1] non è compatibile con [!DNL Inventory Management]. Una volta installati, i moduli MCOM forniscono tutte le funzioni di gestione dell&#39;inventario a [!DNL Commerce], compresa la gestione da una fonte e da più fonti, gli stock, le riserve e altro ancora. Il [!DNL Inventory Management] I moduli sono disabilitati per impostazione predefinita.

MCOM offre funzioni e servizi completi per la gestione degli ordini omnicanale avanzata, l&#39;inventario globale e il multi-sourcing, l&#39;evasione da magazzino a magazzino e l&#39;assistenza clienti centralizzata. Per un elenco completo delle funzioni, vedere [Elenco delle funzioni MCOM][2].

[!DNL Inventory Management] estende esistente [!DNL Commerce] funzioni con opzioni aggiuntive per tenere traccia degli ordini in-process, delle scorte disponibili, delle scorte disponibili per un magazzino e delle API per lo sviluppo di estensioni.

## [!DNL Inventory Management] moduli

Potrebbe essere necessario disattivare [!DNL Inventory Management] moduli per:

- Velocizza l’aggiornamento dei commercianti attualmente in Adobe Commerce o nel Magento Open Source 2.0/2.1/2.2/2.3 e la migrazione a 2.4.x.

- Utilizza moduli personalizzati o di terze parti per la gestione degli inventari e degli ordini.

- Utilizzare [!DNL Order Management System] per la gestione dell’inventario. Il connettore corrente non supporta [!DNL Inventory Management] interfacce. I commercianti OMS che eseguono l’aggiornamento ad Adobe Commerce 2.4.0 devono disattivare questi moduli.

Per informazioni dettagliate, consulta [Installazione e aggiornamento](install-update.md).

[1]: https://omsdocs.magento.com/
[2]: https://omsdocs.magento.com/en/getting-started/feature-list/
