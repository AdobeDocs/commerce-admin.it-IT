---
title: Stato dell’ordine e prenotazioni
description: Scopri l’inserimento automatico della prenotazione o le modifiche che aggiornano la quantità vendibile per un magazzino (o canale di vendita) e la quantità di scorte disponibili per origine.
exl-id: d264cb49-5aa8-4949-ae87-5efcd463d38c
feature: Inventory, Orders, Shipping/Delivery
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 0%

---

# Stato dell’ordine e prenotazioni

[!DNL Inventory Management] supporta fatturazione, pagamenti, spedizione e annullamenti parziali e completi per ordine. Quando si gestisce un ordine tramite l&#39;elaborazione, la fatturazione, la spedizione e potenzialmente i rimborsi, [!DNL Commerce] inserisce o modifica automaticamente gli impegni per aggiornare la quantità vendibile per un magazzino (o canale di vendita) e la quantità esistente per origine. Non è necessario accedere o inserire prenotazioni attivamente. Il completamento delle azioni per evadere, annullare o rimborsare un ordine lo fa per te.

Queste prenotazioni consentono di regolare sempre la quantità vendibile, con importi positivi o negativi per aumentare o diminuire le quantità. Il risultato è un aggiornamento delle scorte disponibili e delle quantità vendibili per la disponibilità aggiornata dei prodotti.

Per informazioni specifiche su ordini e spedizioni, vedere [Gestione di ordini e spedizioni](shipments.md).

## Opzioni di gestione degli ordini

A seconda dello stato del magazzino e delle richieste dei clienti, è possibile aggiornare gli ordini con pagamenti e annullamenti parziali, spedizioni parziali da più origini o per ordini arretrati o note di accredito per rimborsare i prodotti restituiti.

### Spedizioni

Dopo aver fatturato gli ordini, inviare spedizioni parziali o complete fino a quando non si evade l&#39;intero ordine. Ogni spedizione converte la prenotazione, detraendo l&#39;importo dalla quantità di prodotto per origine. Risarcimenti per impegni inserire per aggiornare la quantità vendibile per le scorte. Se invii spedizioni parziali, ogni spedizione detrae tale importo dalla quantità del prodotto e dalle prenotazioni. Eventuali prenotazioni di prodotti non spediti rimangono in vigore fino a quando non vengono spediti, in modo che l&#39;importo vendibile sia corrente e per dare controllo sull&#39;inventario dei prodotti e supportare più spedizioni di origine e ordini inevasi.

### Ordini annullati

Se un cliente annulla l&#39;ordine prima della spedizione (parziale o totale), viene inserito un nuovo impegno per restituire l&#39;importo di magazzino alla quantità vendibile. Le prenotazioni si annullano a vicenda, senza detrarre la quantità da alcuna origine. Altri clienti possono acquistare attivamente tali quantità di prodotti attraverso le scorte e i canali di vendita associati.

### Ordini rimborsati

Se un cliente richiede un rimborso, emettere la nota di credito per gli importi parziali o completi dei prodotti. Quando si ricevono i prodotti restituiti, inserire una nota di credito per fornire i fondi e aggiornare gli importi dei prodotti. Quando si seleziona l&#39;opzione Restituisci a magazzino, [!DNL Commerce] aggiunge nuovamente le quantità ai prodotti e alle origini che hanno spedito gli ordini e le compensazioni per impegni per aggiornare le quantità vendibili per le scorte associate.

## Tipi di ordine

Gli ordini semplici iniziano con un carrello, continuano a pagare e terminano con una consegna soddisfatta. In questi ordini, [!DNL Inventory Management] elabora facilmente gli impegni in base alla disponibilità (o alla quantità vendibile) nel carrello e al pagamento e detrae dalle scorte disponibili alla spedizione.

![Elaborazione per un ordine semplice](assets/diagram-simple-order-flow.png){width="600" zoomable="yes"}

Un ordine più complicato può comportare annullamenti parziali, spedizioni parziali e rimborsi. In queste situazioni, le prenotazioni influiscono sulle scorte disponibili per aggiungere quantità per annullamenti e rimborsi e ridurre le quantità quando ordinate e spedite.

![Processo per un ordine complicato](assets/diagram-complicated-order-flow.png){width="600" zoomable="yes"}

Gli impegni di disponibilità e le variazioni di magazzino si verificano in base allo stato dell&#39;ordine.

## Stato e prenotazioni

Nelle tabelle seguenti vengono descritti dettagliatamente lo stato degli ordini e delle note di accredito con le modifiche degli impegni inserite da [!DNL Commerce] per gestire l&#39;inventario.

| Stato ordine | Descrizione | Impegno per quantità vendibile |
|--|--|--|
| [!UICONTROL Open] | Nuovo e inviato di recente, nessuna elaborazione | L&#39;impegno viene salvato quando l&#39;ordine viene sottomesso per le scorte. |
| [!UICONTROL Canceled] | Annullato parzialmente o interamente prima del pagamento | La compensazione della prenotazione viene inserita per restituire la quantità parziale o totale alla quantità di vendita delle scorte. |
| [!UICONTROL On Hold] | Pagamento e spedizione non elaborati o fatturati | La prenotazione rimane attiva. |
| [!UICONTROL Suspected Fraud] | Non elaborato a causa di frode | Se approvata o in revisione, la prenotazione rimane in vigore.<br/>Se rifiutata, la prenotazione rimane in vigore finché il commerciante non decide di approvare o annullare.<br/>Se annullata, la compensazione della prenotazione viene inserita per restituire l&#39;intera quantità alla quantità di merce venduta. |
| [!UICONTROL Pending] | In attesa di pagamento | La prenotazione rimane al suo posto. |
| [!UICONTROL Processing] | Elaborazione del pagamento, non ricevuto | La prenotazione rimane al suo posto. |
| [!UICONTROL Pending Payment] | Pagamento non ricevuto | La prenotazione rimane al suo posto. |
| [!UICONTROL Payment Review] | Pagamento in fase di revisione per l&#39;elaborazione e il completamento | La prenotazione rimane al suo posto. |
| [!UICONTROL Complete] | Pagato e spedito per intero | L&#39;importo dell&#39;impegno viene detratto dalla quantità del prodotto per l&#39;origine selezionata quando viene fatturato parzialmente o completamente. La retribuzione della prenotazione viene inserita per aggiornare la quantità totale vendibile. |
| [!UICONTROL Closed] | Rimborso o archiviazione | Se archiviato, non vi è alcuna modifica nelle quantità. Se rimborsata in modo parziale o completo, la compensazione della prenotazione viene inserita e convertita per aggiungere quantità di prodotto per origine e quantità vendibile per magazzino. |

| Stato nota di credito | Descrizione | Impegno per quantità vendibile |
|--|--|--|
| [!UICONTROL Open] | Il rimborso è dovuto, non completato | Le prenotazioni non cambiano. |
| [!UICONTROL Refunded] | Completato, fondi restituiti | Se rimborsata in parte o interamente, la compensazione della prenotazione viene inserita e convertita per aggiungere quantità di prodotto per origine e quantità vendibile per magazzino. |

## Esempio di ordine complesso

Blake Sanders ordina biciclette e vestiti per le loro vacanze in famiglia e divertimento. Vedono alcune grandi vendite sul tuo negozio di Biking Adventures con scorte e fonti che si estendono su Stati Uniti, Canada ed Europa.

Comprano due fantastiche bici da parco per i loro bambini piccoli, una BMX per i loro adolescenti, una bella mountain bike per loro stessi e una moderna bici da fondo tedesca per il loro coniuge. Il negozio aveva una vendita di camicie carine, così hanno comprato un po &#39;per tutta la famiglia di abbinare. Consulta l’elenco degli acquisti per le vacanze riportato di seguito, gli SKU corrispondenti e gli impegni inseriti a fronte delle quantità di merce venduta.

![Ordine complesso](assets/diagram-order-complex.png){width="600" zoomable="yes"}

Mostrano alla loro famiglia cosa hanno trovato, ma apporta qualche cambiamento. Prima del completamento del pagamento, annullano due dei 33 SKU BikeFun (ai bambini non piacevano). Si tratta di una cancellazione parziale a causa di un pagamento in sospeso, quindi non è necessaria alcuna nota di credito. Per aggiornare, [!DNL Commerce] viene aggiunto nuovamente alla quantità vendibile per il Canada. L&#39;ordine viene pagato e tutti i prodotti vengono spediti, arrivando in tempo per le vacanze. [!DNL Commerce] aggiorna la quantità vendibile e le quantità di origine per i magazzini di spedizione per i prodotti spediti.

Ma la maglietta non andava bene per il coniuge. Blake chiede un rimborso e rispedisce indietro la sua maglietta. La creazione della nota di credito aggiunge una camicia 54-BikeLife al magazzino di spedizione e di magazzino del Canada.

- **Prodotti spediti** - Con i prodotti acquistati e spediti, [!DNL Commerce] aggiorna l&#39;inventario. Le compensazioni per impegni vengono convertite in detrazioni quantità scorte disponibili dall&#39;origine spedita. Aggiornamenti della quantità vendibile disponibile per il magazzino.

- **Prodotti annullati** - Annullando le scorte, [!DNL Commerce] rimuove la prenotazione per quel prodotto. La compensazione della prenotazione viene inserita a livello di magazzino per aggiungere quantità di vendita arretrata per l&#39;annullamento parziale di due camicie. Ciò non influisce sulla quantità di magazzino a livello di origine.

- **Nota di credito/Prodotto rimborsato** - Per restituire le scorte, è necessario aggiungerle nuovamente alle quantità. Quando si emette la nota di credito, è possibile scegliere di tornare alle scorte. [!DNL Commerce] aggiunge nuovamente la quantità di magazzino all&#39;origine spedita per il prodotto. Per liquidare gli impegni rimanenti, inserire le compensazioni per gli impegni. La quantità vendibile viene ricalcolata in base alla quantità aggiornata.

![Aggiornamenti quantità rimborso ordini](assets/diagram-order-refund.png){width="600" zoomable="yes"}
