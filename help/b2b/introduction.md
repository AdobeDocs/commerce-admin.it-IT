---
title: Introduzione a  [!DNL Adobe Commerce B2B]
description: Scopri come utilizzare le funzioni B2B integrate per soddisfare le tue esigenze con i clienti che sono aziende.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
TQID: https://experienceleague.adobe.com/dt7QZnXH9yO6vMFJBIgt4g43XVfk6Da1gyXEMqqvJlo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 829
ht-degree: 2%

---

# Introduzione a [!DNL Adobe Commerce B2B]

A differenza del modello standard business-to-consumer, le funzioni integrate B2B (Business to Business) sono progettate per soddisfare le esigenze dei venditori (commercianti Adobe Commerce) che hanno clienti che sono aziende. Offre alle aziende con strutture organizzative complesse e a più utenti vari ruoli e livelli di autorizzazione all’acquisto. Un cliente B2B tipico può essere il manager di un negozio al dettaglio, o un acquirente che effettua acquisti per conto di un&#39;azienda. In entrambi i casi, la transazione ha luogo tra la tua azienda e la loro. Puoi anche vendere prodotti direttamente al consumatore. [!DNL Adobe Commerce B2B] è una soluzione integrata che supporta sia i modelli B2B che B2C.

Con l&#39;[installazione](install.md) e l&#39;[abilitazione](enable-basic-features.md) dell&#39;estensione B2B nel tuo store Adobe Commerce, l&#39;esperienza di acquisto può essere personalizzata con cataloghi e prezzi specifici per il cliente, nonché con contenuti e promozioni mirati.

## Account società

Il componente Conto aziendale è un’entità chiave all’interno del B2B da cui dipendono in qualche modo tutte le altre funzioni. Consente di unire più acquirenti che appartengono a una singola azienda in un singolo account aziendale (o account aziendale). L’amministratore della società può creare una struttura aziendale (divisioni, suddivisioni e utenti) che rifletta il modello operativo della società e fornire diversi ruoli utente e autorizzazioni ai membri della società. Questa struttura consente all&#39;amministratore della società di controllare l&#39;attività dell&#39;utente per l&#39;account della società: ordine, preventivo, acquisto, accesso alle informazioni sul credito o al profilo della società e così via.

Dall’amministratore, l’amministratore del sito Commerce può configurare il funzionamento della società sul sito web. La configurazione determina le funzionalità B2B disponibili per gli utenti aziendali, tra cui i metodi di pagamento, i livelli di prezzo, la possibilità di negoziare i prezzi utilizzando i preventivi, la possibilità di creare elenchi di richieste di acquisto e altro ancora.

Per ulteriori informazioni, vedere [Account società](account-companies.md).

>[!NOTE]
>
>Quando è abilitato, il tuo store può dare alle aziende l&#39;opzione di _Pagare sul conto_, il che significa effettuare acquisti su una linea di credito aziendale. In qualità di esercente, puoi allocare il credito per un conto aziendale e gestire le impostazioni del credito per una società e il rimborso del credito.

## Gestione società

La gestione aziendale aiuta gli amministratori di esercenti a semplificare l’amministrazione e la gestione delle organizzazioni B2B con modelli operativi complessi.

Dall&#39;amministratore, gli utenti con le autorizzazioni appropriate possono creare un **[!UICONTROL Company Hierarchy]** che riflette la struttura organizzativa di un&#39;azienda aziendale composta da più aziende. Questa gerarchia consente loro di visualizzare e gestire le società come un gruppo. Ad esempio, l&#39;amministratore può designare una società padre e assegnare tutte le società che operano come filiali della società madre. L&#39;amministratore della società madre può quindi visualizzare e gestire gli account della società per tutte le società assegnate.

Per ulteriori informazioni, vedere [Gestione società](manage-companies.md).

## Servizi per Adobe Commerce

I servizi per Adobe Commerce sono servizi in hosting che forniscono funzionalità estese ad Adobe Commerce e Magento Open Source. I servizi che supportano i flussi di lavoro B2B sono:

* [Servizio catalogo](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html?lang=it)
* [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/guide-overview.html?lang=it)
* [Consigli di prodotto](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=it)

## Cataloghi condivisi

I cataloghi condivisi sono i livelli di prezzo che consentono di impostare prezzi personalizzati per prodotto per diverse aziende su uno o più siti Web. Utilizzando i cataloghi condivisi, puoi vendere i prodotti applicando livelli di prezzo diversi per gruppi di clienti diversi. Il supporto per i cataloghi condivisi è disponibile solo per i negozi Commerce configurati per supportare gli account aziendali.

Per ulteriori informazioni, vedere [Utilizzo dei cataloghi condivisi](catalog-shared.md).

## Ordine rapido

Configura Ordine rapido per ridurre il processo di ordine a diversi clic per i clienti connessi che conoscono il nome del prodotto o lo SKU dei prodotti che desiderano ordinare.

Per ulteriori informazioni, vedere [Ordini rapidi](quick-order.md).

## Offerte negoziabili

Utilizzare la funzione Preventivi per avviare la negoziazione dei prezzi tra un acquirente e un venditore della società.

* Un acquirente autorizzato può avviare un preventivo dal carrello.

* Un venditore può richiedere un preventivo per un acquirente all&#39;Amministratore.

Acquirenti e venditori utilizzano il preventivo per gestire il processo di negoziazione, ad esempio l&#39;aggiunta di articoli, l&#39;aggiornamento delle quantità, la richiesta e l&#39;applicazione di sconti, fino al raggiungimento di un accordo. La griglia _Offerte_ dell&#39;amministratore elenca ogni preventivo ricevuto e mantiene una cronologia della comunicazione tra l&#39;acquirente e il venditore.

Il supporto per i preventivi negoziabili è disponibile solo per i negozi Commerce configurati per supportare gli account aziendali.

Per ulteriori informazioni, vedere [Offerte negoziabili](quotes.md).

## Approvazioni ordini fornitore

Quando si attivano gli ordini di acquisto per un conto della società, tutti gli ordini vengono creati automaticamente come ordini di acquisto (OA). Gli utenti aziendali con le autorizzazioni necessarie possono creare, modificare ed eliminare gli OA creati e quelli creati da utenti subordinati. A seconda del ruolo e dell’ordine, gli utenti aziendali possono essere soggetti a diverse regole di approvazione.

Per ulteriori informazioni, vedere [Ordini di acquisto per società](purchase-order-flow.md).

## Elenchi richieste

I clienti possono utilizzare l&#39;elenco delle richieste di acquisto per risparmiare tempo quando acquistano prodotti ordinati di frequente, in quanto possono aggiungere articoli al carrello direttamente dall&#39;elenco. Possono gestire più elenchi che si concentrano su prodotti di fornitori, acquirenti, team, campagne o qualsiasi altra cosa che semplifichi il loro flusso di lavoro.

Per ulteriori informazioni, vedere [Elenchi richieste](requisition-lists.md).
