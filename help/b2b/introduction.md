---
title: Introduzione a [!DNL B2B for Adobe Commerce]
description: Scopri come utilizzare le funzionalità B2B integrate per soddisfare le tue esigenze di clienti che sono aziende.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# Introduzione a [!DNL B2B for Adobe Commerce]

A differenza del modello standard business-to-consumer, le funzioni integrate B2B (Business to Business) sono progettate per soddisfare le esigenze dei venditori (commercianti Adobe Commerce) che hanno clienti che sono aziende. Offre alle aziende con strutture organizzative complesse e a più utenti vari ruoli e livelli di autorizzazione all’acquisto. Un cliente B2B tipico può essere il manager di un negozio al dettaglio, o un acquirente che effettua acquisti per conto di un&#39;azienda. In entrambi i casi, la transazione ha luogo tra la tua azienda e la loro. Puoi anche vendere prodotti direttamente al consumatore. [!DNL B2B for Adobe Commerce] è una soluzione integrata che supporta sia i modelli B2B che B2C.

Con il [installazione](install.md) e [abilitazione](enable-basic-features.md) dell’estensione B2B nel tuo store Adobe Commerce, l’esperienza di acquisto può essere personalizzata con cataloghi e prezzi specifici per il cliente, contenuti mirati e promozioni.

## Account società

Il componente Conto aziendale è un’entità chiave all’interno del B2B da cui dipendono in qualche modo tutte le altre funzioni. Consente di unire più acquirenti che appartengono a una singola azienda in un singolo account aziendale (o account aziendale). L’amministratore della società può creare una struttura aziendale (divisioni, suddivisioni e utenti) che rifletta il modello operativo della società e fornire diversi ruoli utente e autorizzazioni ai membri della società. Questa struttura consente all&#39;amministratore della società di controllare l&#39;attività dell&#39;utente per l&#39;account della società: ordine, preventivo, acquisto, accesso alle informazioni sul credito o al profilo della società e così via.

Dall’amministratore, l’amministratore del sito Commerce può configurare il funzionamento della società sul sito web. La configurazione determina le funzionalità B2B disponibili per gli utenti aziendali, tra cui i metodi di pagamento, i livelli di prezzo, la possibilità di negoziare i prezzi utilizzando i preventivi, la possibilità di creare elenchi di richieste di acquisto e altro ancora.

Per ulteriori informazioni, consulta [Account società](account-companies.md).

>[!NOTE]
>
>Quando è abilitato, il tuo store può dare alle aziende l’opzione di _Pagamento in acconto_, il che significa effettuare acquisti su una linea di credito aziendale. In qualità di esercente, puoi allocare il credito per un conto aziendale e gestire le impostazioni del credito per una società e il rimborso del credito.

## Gestione società

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponibile solo per i partecipanti ai programmi beta"}

La gestione aziendale aiuta gli amministratori di esercenti a semplificare l’amministrazione e la gestione delle organizzazioni B2B con modelli operativi complessi.

L’amministratore può creare una **[!UICONTROL Company Hierarchy]** che rispecchia la struttura organizzativa di un&#39;impresa commerciale composta da più imprese. Questa gerarchia consente loro di visualizzare e gestire le società come un gruppo. Ad esempio, l&#39;amministratore può designare una società padre e assegnare tutte le società che operano come filiali della società madre. L&#39;amministratore della società madre può quindi visualizzare e gestire gli account della società per tutte le società assegnate.

Per ulteriori informazioni, consulta [Gestione società](manage-companies.md).

## Servizi per Adobe Commerce

I servizi per Adobe Commerce sono servizi in hosting che forniscono funzionalità estese ad Adobe Commerce e Magento Open Source. I servizi che supportano i flussi di lavoro B2B sono:

* [Servizio catalogo](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)
* [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)
* [Recommendations del prodotto](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)

## Cataloghi condivisi

I cataloghi condivisi sono i livelli di prezzo che consentono di impostare prezzi personalizzati per prodotto per diverse aziende su uno o più siti Web. Utilizzando i cataloghi condivisi, puoi vendere i prodotti applicando livelli di prezzo diversi per gruppi di clienti diversi. Il supporto per i cataloghi condivisi è disponibile solo per i negozi Commerce configurati per supportare gli account aziendali.

Per ulteriori informazioni, consulta [Utilizzo dei cataloghi condivisi](catalog-shared.md).

## Ordine rapido

Configura Ordine rapido per ridurre il processo di ordine a diversi clic per i clienti connessi che conoscono il nome del prodotto o lo SKU dei prodotti che desiderano ordinare.

Per ulteriori informazioni, consulta [Ordini rapidi](quick-order.md).

## Offerte negoziabili

Utilizzare la funzione Preventivi per avviare la negoziazione dei prezzi tra un acquirente e un venditore della società.

* Un acquirente autorizzato può avviare un preventivo dal carrello.

* Un venditore può richiedere un preventivo per un acquirente all&#39;Amministratore.

Acquirenti e venditori utilizzano il preventivo per gestire il processo di negoziazione, ad esempio l&#39;aggiunta di articoli, l&#39;aggiornamento delle quantità, la richiesta e l&#39;applicazione di sconti, fino al raggiungimento di un accordo. Il _Virgolette_ Nella griglia dell&#39;amministratore sono elencati tutti i preventivi ricevuti e viene conservata una cronologia delle comunicazioni tra l&#39;acquirente e il venditore.

Il supporto per i preventivi negoziabili è disponibile solo per i negozi Commerce configurati per supportare gli account aziendali.

Per ulteriori informazioni, consulta [Offerte negoziabili](quotes.md).

## Approvazioni ordini fornitore

Quando si attivano gli ordini di acquisto per un conto della società, tutti gli ordini vengono creati automaticamente come ordini di acquisto (OA). Gli utenti aziendali con le autorizzazioni necessarie possono creare, modificare ed eliminare gli OA creati e quelli creati da utenti subordinati. A seconda del ruolo e dell’ordine, gli utenti aziendali possono essere soggetti a diverse regole di approvazione.

Per ulteriori informazioni, consulta [Ordini di acquisto per società](purchase-order-flow.md).

## Elenchi richieste

I clienti possono utilizzare l&#39;elenco delle richieste di acquisto per risparmiare tempo quando acquistano prodotti ordinati di frequente, in quanto possono aggiungere articoli al carrello direttamente dall&#39;elenco. Possono gestire più elenchi che si concentrano su prodotti di fornitori, acquirenti, team, campagne o qualsiasi altra cosa che semplifichi il loro flusso di lavoro.

Per ulteriori informazioni, consulta [Elenchi richieste](requisition-lists.md).
