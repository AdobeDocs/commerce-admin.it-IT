---
title: Segmenti cliente
description: I segmenti di clienti consentono di visualizzare in modo dinamico contenuti e promozioni a clienti specifici.
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
source-git-commit: 0b9f394a792171e93ee72f3b4ebb904b96ea1051
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Segmenti clienti

I segmenti dei clienti consentono di visualizzare in modo dinamico contenuti e promozioni a clienti specifici, in base a varie proprietà. Alcuni esempi sono l’indirizzo del cliente, la cronologia degli ordini e i contenuti del carrello acquisti. Puoi ottimizzare le iniziative di marketing in base a segmenti mirati con regole di prezzo del carrello. Puoi anche generare rapporti ed esportare l’elenco dei clienti target. Poiché le informazioni sui segmenti dei clienti vengono costantemente aggiornate, i clienti possono associarsi e dissociarsi da un segmento mentre fanno acquisti nel negozio.

Per comprendere meglio la differenza tra [gruppi di clienti](../customers/customer-groups.md) e segmenti di clienti, tieni presente dove vengono utilizzati:

|  | Segmento cliente | Gruppo di clienti |
|--- |--- |--- |
| Regola prezzo catalogo |  | ✔️ |
| Regola prezzo carrello | ✔️ | ✔️ |
| Prezzo livello |  | ✔️ |
| Regola prodotto correlata | ✔️ |  |
| Blocco dinamico | ✔️ |  |
| Tassi di cambio premi |  | ✔️ |
| Autorizzazioni categoria |  | ✔️ |
| Inviti |  | ✔️ |

{style="table-layout:auto"}

## Attributi del segmento clienti

Gli attributi del segmento clienti sono definiti in modo simile alle regole del carrello e del prezzo di catalogo. Affinché un attributo possa essere utilizzato in una condizione di segmento del cliente, la _[!UICONTROL Use in Customer Segment]_[proprietà](attribute-properties.md#) deve essere impostata su `Yes`. Le condizioni del segmento del cliente possono incorporare i seguenti tipi di attributi:

| Attributo | Descrizione |
|---|---|
| `Customer Address Fields` | Puoi definire qualsiasi campo dell’indirizzo, ad esempio città o paese. Qualsiasi indirizzo nella rubrica di un cliente può soddisfare queste condizioni per il cliente. Oppure puoi specificare di utilizzare solo gli indirizzi predefiniti di fatturazione o spedizione per trovare un cliente. Gli attributi dell’indirizzo del cliente sono disponibili solo per i clienti che hanno effettuato l’accesso ai loro account. |
| `Customer Information Fields` | È possibile definire varie informazioni sul cliente, tra cui Gruppo clienti, nome, e-mail, stato di iscrizione alla newsletter e saldo del credito del Negozio. Le informazioni sui clienti sono disponibili solo per i clienti che hanno effettuato l&#39;accesso ai loro account. |
| `Cart Fields` | Le proprietà del carrello possono essere basate sulla quantità (articoli riga o quantità totale) o sul valore (come totale complessivo, imposte e gift card) del contenuto del carrello. |
| `Products` | Puoi fare riferimento a prodotti attualmente nel carrello, nella lista dei desideri o che sono stati precedentemente visualizzati o ordinati. Puoi anche impostare un intervallo di date in cui si è verificato. I prodotti vengono definiti utilizzando gli attributi del prodotto. |
| `Order Fields` | Le caratteristiche dell&#39;ordine per gli ordini passati possono essere definite in base all&#39;indirizzo di fatturazione/spedizione nell&#39;ordine, all&#39;importo totale (o medio) o alla quantità degli ordini oppure al numero totale di ordini. È inoltre possibile impostare un intervallo di date per il momento in cui si è verificato e lo stato dell&#39;ordine degli ordini che soddisfano queste condizioni. Disponibile solo per i clienti che hanno effettuato l’accesso. Le condizioni impostate per gli acquirenti che non hanno effettuato l’accesso cessano di funzionare al momento dell’accesso. |

{style="table-layout:auto"}

Consulta [Creare ed eliminare segmenti cliente](../customers/customer-segment-create.md) per ulteriori informazioni sulla definizione dei segmenti cliente.

## eBooks

- **Segmentazione del cliente**: ottieni il [eBook](https://business.adobe.com/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html) per scoprire come aumentare i profitti e la soddisfazione complessiva del cliente.
- **Tattiche di segmentazione**: ottieni il [eBook](https://business.adobe.com/resources/3-segmentation-tactics-ignite-conversion.html) per migliorare il targeting dei messaggi e delle promozioni e creare conversazioni significative con i tuoi clienti.
