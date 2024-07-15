---
title: Tipi di origini esercente
description: Scopri i due tipi di origini in base al numero di posizioni o origini nella tua azienda.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Tipi di origini esercente

[!DNL Commerce] supporta [!DNL Inventory Management] per tutte le dimensioni di aziende, incluso un singolo negozio con un sito Web a una rete internazionale di siti Web, negozi, magazzini e corrieri diretti. Tutti i commercianti che utilizzano Adobe Commerce o Magento Open Source rientrano in due tipi in base al numero di posizioni, o origini, nella tua azienda.

- I commercianti single-source spediscono i prodotti da un&#39;unica posizione. Sei considerato un commerciante/modalità a fonte singola fino a quando non inizi ad aggiungere sorgenti e scorte personalizzate all’installazione.

- I mercanti multi-sorgente spediscono i prodotti da più di una località, ad esempio negozi, magazzini, corrieri e centri di distribuzione. Dopo aver aggiunto sorgenti personalizzate per posizione, diventi automaticamente un commerciante multi-sorgente.

## Mercanti single-source

I commercianti con una sola origine dispongono di un&#39;unica ubicazione che gestisce le scorte disponibili ed evade gli ordini. In genere, si dispone di più siti Web (o canali di vendita) che vendono prodotti dallo stesso catalogo, inventario e ubicazione.

Ad esempio, disponi di un sito web o di un’implementazione multisito con siti per Stati Uniti, Germania, Francia e Brasile che richiamano tutti i prodotti da un unico grande magazzino. Questa singola origine gestisce tutte le quantità di magazzino, le spedizioni e le restituzioni indipendentemente dal canale di vendita che riceve l&#39;ordine.

Per iniziare:

- Configura le [impostazioni globali e di prodotto](configuration.md) per l&#39;inventario del tuo Negozio in base alle esigenze.

- Aggiorna [Source predefinito](sources-manage.md) con le informazioni per la posizione di inventario singola. La creazione di origini aggiuntive non è obbligatoria.

- Aggiorna [Stock predefinito](stocks-manage.md). Assicurati che tutti i tuoi siti web siano selezionati come canali di vendita. Quando si aggiungono nuovi siti Web, [!DNL Commerce] li aggiunge automaticamente allo Stock predefinito. Non è necessario creare scorte aggiuntive.

>[!NOTE]
>
>Con l&#39;espansione dell&#39;azienda, aggiungi altre origini e scorte e aggiorna la configurazione di [!DNL Inventory Management] per diventare un commerciante multi-source. Per tutti i dettagli, vedere [Espandi e ripristina inventario](expand-restructure.md).

## Mercanti multi-source

I commercianti multi-sorgente dispongono di un sito web o di un’implementazione multi-sito e gestiscono le scorte disponibili ed evadono gli ordini tramite più ubicazioni.

Ad esempio, disponi di un’implementazione multisito con siti web per Stati Uniti, Germania, Francia e Brasile. La tua azienda include più magazzini e negozi in questi paesi e servizi di spedizione diretta che gestiscono tutte le scorte di magazzino e evadono gli ordini. Queste posizioni e questi siti Web diventano origini e scorte in [!DNL Commerce]. Puoi creare un magazzino per le Americhe e un altro per l&#39;Europa, assegnando siti web e sorgenti in base alle località e alle posizioni. I clienti che acquistano ogni sito web hanno accesso solo agli inventari vendibili dalle fonti assegnate.

Per iniziare:

- Configura le impostazioni globali per l&#39;inventario del tuo Negozio in base alle esigenze.

- Aggiungi [origini personalizzate](sources-add.md) per le ubicazioni di magazzino: magazzini, magazzini, centri di distribuzione e corrieri diretti.

- Aggiungi [scorte personalizzate](stocks-add.md) per ogni area geografica per mappare i siti Web con più origini. Riordinare le origini di ogni magazzino in base alla priorità dell&#39;ubicazione, utile quando si eseguono gli ordini.

- Assegna origini ai prodotti, aggiungendo quantità per ubicazione.

- Completa eventuali altre configurazioni per prodotto per soglie di quantità, ordini inevasi e così via.
