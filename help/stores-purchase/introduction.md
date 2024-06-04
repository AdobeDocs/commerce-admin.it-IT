---
title: Introduzione ai negozi ed esperienza di acquisto
description: Scopri le funzioni utilizzate per creare e gestire i negozi online e l’esperienza di acquisto per i clienti.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Introduzione ai negozi ed esperienza di acquisto

Adobe Commerce e Magento Open Source forniscono un set completo di funzioni per creare e gestire i negozi online e l’esperienza di acquisto per i clienti. All’interno dell’istanza di Commerce, puoi gestire la gerarchia di store di siti web, store e visualizzazioni. È inoltre possibile configurare le imposte e i tassi di valuta necessari per eseguire i negozi per più impostazioni internazionali, incluse le classi di imposta per i prodotti e i gruppi di clienti.

## Struttura del Negozio

Una singola istanza di Adobe Commerce o Magento Open Source può supportare più siti, store o visualizzazioni di store che utilizzano attributi e contenuti diversi. Uno scenario tipico consiste nell’impostare archivi con opzioni diverse in domini diversi. Ad esempio, potresti desiderare un set di categorie e prodotti in un dominio e un altro set di categorie e prodotti in un dominio diverso in un’altra lingua. I commercianti possono configurare i siti web, gli store e le visualizzazioni dello store nell’amministratore.

Quando [gerarchia](stores.md) è definito, è possibile applicare le impostazioni di configurazione in base a [ambito](../getting-started/websites-stores-views.md#scope-settings) in modo che ogni visualizzazione sito, store e store fornisca l&#39;esperienza di catalogo prodotti e vetrina desiderata.

## Punto vendita

Adobe Commerce e Magento Open Source riducono gli errori di ordinazione verificando automaticamente lo SKU e la disponibilità di tutti gli articoli prima dell&#39;invio di un ordine. È possibile configurare [carrello](cart.md) e [opzioni di pagamento](checkout-process.md) per fornire un’esperienza di acquisto ottimale, dalla transazione alla consegna. I clienti che hanno effettuato l&#39;accesso ai loro account possono completare rapidamente l&#39;estrazione, poiché molte delle informazioni sono già presenti nei loro account. Il _Pagamento_ pagina guida il cliente attraverso ogni fase del processo per il completamento della transazione dell&#39;ordine. Se attivi [Acquisto immediato](checkout-instant-purchase.md), i clienti possono velocizzare il processo di pagamento utilizzando le informazioni salvate nel loro account.

>[!TIP]
>
>![Adobe Commerce B2B](../assets/b2b.svg) Con l’installazione e l’abilitazione di Adobe Commerce B2B, puoi configurare _Ordine rapido_ per i clienti associati a un account aziendale. Questa funzione riduce il processo di ordinazione a diversi clic quando conoscono il nome o lo SKU dei prodotti che desiderano ordinare. È inoltre possibile configurare il supporto per i preventivi negoziabili per gli account aziendali. Per ulteriori informazioni sulle funzioni B2B, vedi [Guida utente di Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## Assistenza agli acquisti

I clienti a volte hanno bisogno di assistenza per completare un acquisto. Ad alcuni clienti piace fare acquisti online, ma preferiscono ordinare per telefono. Puoi offrire assistenza immediata sia agli ospiti che ai clienti che si sono registrati per un account presso il tuo negozio.

- [Gestire il carrello](shopping-assisted-cart-manage.md)
- [Crea ordini](customer-account-create-order.md) per clienti registrati
- [Aggiorna ordini](order-update.md)

![Carrello](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

Guarda questo video per scoprire cosa sono gli acquisti assistiti dal venditore:

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12)

## Gestione degli ordini e operazioni

Nell’amministratore, gli esercenti possono accedere alle informazioni in ogni fase del flusso di lavoro dell’ordine ed elaborare gli ordini:

- Il [Ordini](orders.md) La pagina fornisce ai commercianti un elenco di facile accesso di tutti gli ordini correnti e include strumenti per modificare ed elaborare gli ordini esistenti e creare gli ordini per conto dei clienti.

- Il [Fatture](invoices.md) elenchi di pagine Una fattura è basata su un ordine di vendita temporaneo e fornisce un record permanente dell&#39;ordine.

- Il [Spedizioni](shipments.md) pagina elenca il record di spedizione di ogni fattura pronta per la spedizione.

- Il [Note di credito](credit-memos.md) Questa pagina consente ai commercianti di elaborare e gestire una nota di credito, ovvero un documento che mostra l&#39;importo dovuto al cliente. L’importo può essere applicato a un acquisto o rimborsato al cliente.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Solo per Adobe Commerce) Il [Restituisce](returns.md) Questa pagina elenca le richieste di materiale promozionale (RMA) restituite correnti e viene utilizzata per immettere nuove richieste di reso.

- Il [Transazioni](transactions.md) pagina elenca tutte le attività di pagamento che hanno avuto luogo tra il tuo negozio e un sistema di pagamento e fornisce l&#39;accesso a informazioni più dettagliate.

## Spedizione e consegna

Alcuni studi dimostrano che i negozi offrono ai clienti una scelta di [metodi di consegna](delivery.md) hanno tassi di conversione più elevati rispetto agli archivi che utilizzano un singolo metodo. L’amministratore fornisce vari strumenti che i commercianti possono utilizzare per impostare più metodi di consegna e [vettori di spedizione](carriers.md), e per stampare [etichette di spedizione](shipping-labels.md).
