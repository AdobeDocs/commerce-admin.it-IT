---
title: Scorte e fonti
description: Scopri le relazioni tra prodotti, origini e stock.
exl-id: 01bbbd82-898b-4757-ab40-0d8b89ec59bc
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Scorte e fonti

Gestione dell&#39;inventario indipendentemente dall&#39;ubicazione del magazzino, dal tipo di prodotto o servizio o dal canale di vendita. evadere ordini e spedire prodotti da più magazzini, magazzini fisici, centri di distribuzione e spedizione diretta per completare gli ordini con particolare attenzione a scorte equilibrate, costi di spedizione e altro ancora.

Queste descrizioni includono prodotti, fonti e scorte per una società di biciclette con più sedi di spedizione e siti web negli Stati Uniti e in Europa.

## Sorgenti

[Le origini](sources-manage.md) sono le ubicazioni fisiche in cui l&#39;inventario dei prodotti viene gestito e spedito per l&#39;evasione degli ordini o in cui sono disponibili i servizi. Queste sedi possono includere magazzini, negozi fisici, centri di distribuzione e corrieri diretti. [!DNL Commerce] utilizza le quantità e le quantità vendibili per magazzino e gestisce automaticamente le quantità di magazzino per i prodotti e gli ordini gestiti. Se hai una sola origine, sei considerato in modalità _single-source_. Se hai più sorgenti, sei considerato in modalità _multi-source_.

Un&#39;origine può avere la priorità nell&#39;ambito delle scorte in un magazzino, ma non necessariamente in tutti i magazzini, poiché l&#39;origine può essere riutilizzata in scorte diverse. Il numero di scorte e di origini aumenta la complessità per determinare il magazzino o il negozio migliore per evadere un ordine. È possibile, ad esempio, che un numero limitato di prodotti sia disponibile presso le sedi principali con un ampio inventario nei magazzini e nei servizi in sedi chiave con disponibilità limitata.

In questo esempio, il commerciante ha una mountain bike disponibile per la spedizione da negozi, magazzini e un corriere espresso.

![Esempio di diagramma delle origini](assets/diagram-sources.png){width="600" zoomable="yes"}

## Scorte

[Le scorte](stocks-manage.md) rappresentano un inventario virtuale e aggregato dei prodotti disponibili per la vendita ai canali di vendita (siti Web). Ogni azione mappa i canali di vendita con le origini delle scorte disponibili e delle quantità vendibili. A seconda della configurazione del sito, le scorte possono essere assegnate a uno o più canali e fonti di vendita.

I Sales Channel rappresentano le entità che vendono il proprio inventario, inclusi i siti web, le visualizzazioni dei negozi, i gruppi di clienti B2B e così via. I canali di vendita possono essere associati a un solo magazzino. A ciascun canale di vendita può essere assegnato un solo magazzino e un singolo magazzino può essere assegnato a più siti web. Attraverso le scorte, puoi modificare la priorità delle origini utilizzate per la spedizione degli ordini e dall&#39;[Algoritmo di selezione Source](selection-reservations.md).

Inizia con un Titolo predefinito assegnato con il Source predefinito e il tuo sito web, meglio utilizzato dai commercianti single-source. Solo il Source di default può essere assegnato a questo stock. Se necessario, i commercianti multi-sorgente creano scorte personalizzate per origini e siti web personalizzati.

![Diagramma ad esempio scorte per uno store](assets/diagram-stock.png){width="600" zoomable="yes"}

## Quantità di prodotti

Quantità è il numero di prodotti nel magazzino attivo disponibili per l&#39;acquisto. La quantità di prodotti aumenta e diminuisce quando si completano le spedizioni o si adegua il magazzino. L’aggiunta di prodotti a un carrello non influisce su questa quantità. La Quantità vendibile tiene traccia della disponibilità del prodotto per un canale di vendita e utilizza questo valore anche per determinare le scorte disponibili per l&#39;acquisto. A seconda del numero di origini, è possibile visualizzare e gestire la quantità di prodotto per uno dei seguenti elementi:

- **Quantità** - Per i commercianti con una sola origine, la colonna e il valore _[!UICONTROL Quantity]_&#x200B;tengono traccia della quantità di scorte disponibili.
- **Quantità per Source** - Per i commercianti con più origini, la colonna e i valori _[!UICONTROL Quantity per Source]_&#x200B;tengono traccia delle scorte disponibili in base all&#39;ubicazione. Se si aggiungono più origini, questo valore sostituisce la Quantità ed elenca tutte le origini e le quantità assegnate.

Le prenotazioni tengono traccia delle richieste di scorte per l&#39;intero processo di acquisto, aggiungendo prodotti al carrello, completando il pagamento e gestendo i rimborsi. Per le scorte e le scorte disponibili, gli impegni riservano gli importi delle scorte per ordine tramite il processo di pagamento, sottratti dalla quantità vendibile. Gli impegni vengono convertiti in detrazioni quantità durante la fatturazione e la spedizione dei prodotti.

Quantità vendibile calcola l&#39;inventario virtuale dei prodotti (o della disponibilità), utilizzando soglie configurate, importi prenotati o venduti e quantità per origine. Per ogni scorta, [!DNL Commerce] accede a tutte le origini assegnate e aggrega le quantità di prodotto associate. Con questo valore di base, vengono quindi sottratti tutti gli importi di prenotazione e la soglia _[!UICONTROL Notify for Quantity Below]_.

![Calcolo della quantità vendibile per un magazzino](assets/diagram-salable-quantity.png){width="600" zoomable="yes"}

## Configurazioni inventario

Ogni prodotto, origine e magazzino include diverse opzioni da configurare per il negozio a livello globale, di origine, di magazzino e di prodotto. Per un elenco completo di queste opzioni, consultare [Configurazione di Inventory management](configuration.md).

Di seguito sono riportate alcune opzioni importanti da comprendere per [!DNL Inventory Management]:

- **[!UICONTROL Out-of-Stock Threshold]** - Imposta un importo da sottrarre dalla quantità di vendita. Se si abilita Ordini inevasi, questo valore non viene detratto dalla quantità vendibile.
- **[!UICONTROL Backorders]** - Determina se i prodotti possono essere venduti oltre lo zero scorte, salvando gli ordini fino alla ricostituzione delle scorte. Quando gli ordini arretrati sono abilitati, si consiglia di configurare [!UICONTROL Out-of-Stock Threshold].

>[!NOTE]
>
>Il valore Soglia scorte esaurite supporta gli importi negativi e positivi. Se abiliti gli ordini in inevaso, imposta questo valore su un importo negativo per il numero massimo di prodotti che possono essere messi in inevaso prima che il prodotto sia considerato esaurito.

## Demo di Inventory management

Guarda questo video per scoprire le origini e le scorte di Inventory management:

>[!VIDEO](https://video.tv.adobe.com/v/3410197?quality=12&learn=on&captions=ita)
