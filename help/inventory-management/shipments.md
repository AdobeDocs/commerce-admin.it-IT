---
title: Gestisci ordini e spedizioni dal magazzino
description: Scopri le funzioni e le opzioni aggiuntive [!DNL Inventory Management]  per la gestione delle quantità di magazzino tramite il processo di spedizione.
exl-id: cc4ca518-d98c-48f3-9051-6fb3c6fae9fe
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---

# Gestione di ordini e spedizioni

[!DNL Inventory Management] include funzionalità e opzioni aggiuntive per la gestione delle quantità di magazzino tramite il processo di spedizione. Durante la revisione e l&#39;evasione delle spedizioni, l&#39;annullamento degli ordini e l&#39;emissione delle note di accredito, le quantità dei prodotti commerciabili e disponibili vengono aggiornate automaticamente.

Queste informazioni includono specifiche per [!DNL Inventory Management]. Per ulteriori informazioni, vedere l&#39;argomento [Ordini](../stores-purchase/orders.md){target="_blank"} nella _Guida alle vendite e all&#39;esperienza di acquisto_.

## Ordini

[!DNL Commerce] supporta ordini singoli e ordini con più indirizzi preconfigurati senza configurazioni aggiuntive. Quando i clienti o il personale inseriscono gli ordini, [!DNL Inventory Management] tiene traccia delle scorte utilizzando gli impegni rispetto alla quantità vendibile, detraendo dalla quantità di magazzino i prodotti fatturati e spediti.

### Ordini con più indirizzi

Per gli ordini con più indirizzi, viene generata una serie di ordini singoli, uno per ciascun indirizzo di destinazione inserito. Durante il pagamento, i clienti selezionano ogni set di prodotti associati per indirizzo durante il pagamento generato come ordini singoli in base all&#39;indirizzo di destinazione. Ogni ordine include i prodotti associati per indirizzo.

[!DNL Commerce] gestisce le scorte per questi ordini con più indirizzi esattamente come per i singoli ordini. Consente di utilizzare l&#39;algoritmo di selezione Source per le raccomandazioni o le sostituzioni durante la spedizione, le spedizioni parziali, l&#39;annullamento degli ordini e il rimborso con aggiornamenti delle scorte.

![Indirizzo multiplo al momento dell&#39;estrazione](assets/inventory-multi-ship.png){width="350" zoomable="yes"}

### Rimborsi

Quando si immette una [nota di credito](../stores-purchase/credit-memo-create.md){target="_blank"} per emettere un rimborso, è possibile restituire la quantità di prodotto all&#39;origine detratta. Le informazioni sull&#39;ordine includono l&#39;origine di magazzino che ha spedito il prodotto. Si consiglia di aggiudicare la quantità di prodotto restituita tramite una nota di credito quando si riceve il prodotto restituito.

![Elementi da rimborsare con restituzione al magazzino selezionato](assets/credit-memo-items-to-refund.png)
{width="350" zoomable="yes"}

### Annulla ordini non spediti

Se un ordine non è stato spedito e viene annullato (in tutto o in parte), [!DNL Inventory Management] restituisce automaticamente le scorte del prodotto alla quantità vendibile. Fino alla fatturazione e alla spedizione, i prodotti acquistati vengono prenotati a fronte della quantità vendibile, non dedotta dalla quantità effettiva. Al momento della fatturazione e della spedizione dell&#39;ordine, il sistema converte l&#39;impegno in una detrazione di magazzino.

Dietro le quinte, [!DNL Inventory Management] inserisce automaticamente una prenotazione retribuzione rimuovendo il blocco sulla quantità di prodotto. La quantità torna alla quantità vendibile virtuale aggregata.

## Spedizioni

Se [!DNL Inventory Management] è abilitato, è possibile inviare spedizioni parziali o complete da una o più origini per evadere gli ordini. È possibile controllare le scorte in uscita per ogni ordine, impostando gli importi da detrarre, inviando una o più spedizioni e consegnando scorte e ordini inevasi quando le scorte sono disponibili. Per ogni voce dell&#39;ordine, inserire un importo da detrarre dalla quantità di origine. Generare una spedizione per origine quando si dispone di scorte di magazzino, fino all&#39;evasione dell&#39;intero ordine.

### Spedizioni parziali

Per i commercianti con più origini, [!DNL Commerce] genera una spedizione per ogni origine selezionata. Il flusso di lavoro generale consente di selezionare un&#39;origine, impostare la quantità di prodotti da detrarre per evadere l&#39;ordine e procedere alla spedizione. Una volta completato, creare ulteriori spedizioni per ciascuna origine fino a quando non si è evaso l&#39;ordine.

I commercianti con una sola origine possono anche inviare spedizioni parziali per supportare ordini inevasi o bilanciare le scorte quando arrivano gli ordini per gli articoli più popolari.

### Algoritmo di selezione Recommendations e Source

L&#39;[algoritmo di selezione Source](selection-reservations.md) (SSA) fornisce raccomandazioni per spedizioni parziali e complete. È possibile accedere agli algoritmi di selezione di Source durante la creazione delle fatture di spedizione per un ordine. Nella pagina Spedizione eseguire l&#39;algoritmo Priorità Source o Priorità distanza in qualsiasi momento per determinare le opzioni migliori per la corrispondenza delle quantità ordinate e delle origini disponibili. Il sistema supporta la spedizione di un ordine completo da un&#39;unica origine e la suddivisione dell&#39;ordine in più spedizioni parziali da più origini. Puoi accedere a queste opzioni per l&#39;evasione immediata e le spedizioni scaglionate per inviare quantità minori nel tempo.

Per completare e spedire un ordine, è necessario che sia stato completato il pagamento e che sia stato fatturato. Attualmente, è possibile eseguire nuovamente la valutazione della sicurezza della nave per i consigli e la spedizione da una o più origini oppure sostituire i consigli della valutazione della sicurezza della nave con l&#39;impostazione manuale delle origini e delle quantità per evadere la spedizione.

- Si consiglia di eseguire nuovamente la valutazione della sicurezza della nave per esaminare le raccomandazioni per ogni spedizione.

- Se si desidera modificare le selezioni, è possibile eseguire l&#39;override con detrazioni di origine manuali.

### Spedizioni e prenotazioni

Man mano che vengono generate le spedizioni, le prenotazioni per i prodotti vengono cancellate e la quantità di prodotto viene dedotta. La quantità esistente per magazzino viene aggiornata in base ai dettagli della spedizione. Ad esempio, se si inviano spedizioni per dieci prodotti da due origini, le quantità per tali origini vengono detratte 10 ciascuna. La Quantità vendibile viene aggiornata automaticamente per le scorte associate, fornendo ai clienti e al personale le quantità di prodotti più recenti. E le prenotazioni sono state cancellate completamente, senza contare più la Quantità vendibile.
