---
title: Installare [!DNL B2B for Adobe Commerce] estensione
description: Scopri come installare [!DNL B2B for Adobe Commerce] metapacchetto.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: e57aa4e8919c2de5341c4b8363197d6380bbb0f6
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 0%

---


# Installare [!DNL B2B for Adobe Commerce] estensione

L’estensione B2B per Adobe Commerce è disponibile solo per Adobe Commerce v2.2.0 o versione successiva. Viene installato dopo l’installazione di Adobe Commerce.

Installa la versione più recente dell’estensione B2B supportata nella versione distribuita di Adobe Commerce.

>[!NOTE]
>
>Queste istruzioni di installazione si applicano ad Adobe Commerce implementato in locale. Per installare l’estensione B2B per i progetti Commerce implementati nell’infrastruttura cloud, consulta [Guida all’infrastruttura Commerce Cloud](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## Requisiti

- Adobe Commerce versione 2.3.x o successiva
- [Versione supportata dell’estensione B2B](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- Valido [chiavi di autenticazione](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) per scaricare le estensioni Adobe Commerce.

  Salva le chiavi di autenticazione per l&#39;installazione definendole globalmente nel tuo [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) directory. Oppure, salvali in un [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) nella directory principale dell’applicazione Adobe Commerce.

Prima di installare o aggiornare l’estensione B2B, consulta le note sulla versione per informazioni aggiornate sulla compatibilità della versione, sugli aggiornamenti o sulle modifiche che possono influenzare i requisiti di installazione o aggiornamento.

- [Note sulla versione B2B](release-notes.md)
- [Note sulla versione di Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## Passaggi per l’installazione

1. Dalla directory principale dell’applicazione Adobe Commerce, aggiorna la `composer.json` per aggiungere le dipendenze per l’estensione B2B:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Se si verifica un errore, ad esempio:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Controlla l’ortografia del pacchetto, il vincolo di versione e che il pacchetto sia disponibile e corrisponda al requisito di stabilità minima (stabile).

1. Se richiesto, immetti [chiavi di autenticazione](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

   Il tuo _chiave pubblica_ è il tuo nome utente; il tuo _chiave privata_ è la password. Se hai memorizzato le chiavi pubbliche e private in `auth.json`, l&#39;autenticazione non viene richiesta.

1. Dopo aver completato l&#39;aggiornamento dei moduli, esegui i seguenti comandi:

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >In modalità di produzione, potresti ricevere un messaggio a `Please rerun Magento compile command`. Immettere i comandi per completare l&#39;installazione. Adobe Commerce non richiede di eseguire il comando di compilazione in modalità Sviluppatore.

Dopo aver completato l’installazione, configura e avvia gli utenti dei messaggi, tra cui [specifica dei parametri per i consumer di messaggi](#configure-message-consumers).

## Consumatori di messaggi

L’estensione B2B per Adobe Commerce utilizza MySQL per la gestione della coda dei messaggi. Nella tabella seguente sono elencati i consumer di messaggi che supportano le funzionalità B2B. Dopo aver installato l’estensione, avvia il messaggio consumer per le funzionalità B2B necessarie per la vetrina Commerce.

| Consumatore | Descrizione |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Aggiorna il prezzo per ogni prodotto in un catalogo condiviso. Obbligatorio quando [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `sharedCatalogUpdateCategoryPermissions` | Aggiorna le categorie assegnate a una categoria di catalogo condiviso. Obbligatorio quando [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `negotiableQuotePriceUpdate` | Aggiorna i prezzi per i preventivi negoziabili. Obbligatorio quando [**[!UICONTROL Quotes]**](quotes.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `purchaseorder.toorder` | Converte l&#39;ordine fornitore in ordine. Obbligatorio quando [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `purchaseorder.transactional.email` | Invia e-mail ordine fornitore. Obbligatorio quando [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `purchaseorder.validation` | Convalida l&#39;ordine fornitore a fronte dei relativi [regole di approvazione](account-dashboard-approval-rules.md). Obbligatorio quando [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `quoteItemCleaner` | Elimina i preventivi di prezzo non validi o inattivi quando un prodotto viene eliminato dal catalogo o rimosso dal carrello. Obbligatorio quando [**[!UICONTROL Quotes]**](quotes.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `inventoryQtyCounter` | Corregge in modo asincrono l&#39;indice azionario dopo aver effettuato un ordine o rimosso un prodotto. Obbligatorio quando [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) è abilitata per Inventory management nelle impostazioni di configurazione dell’amministratore. Consulta [Best practice per le prestazioni](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | Crea messaggi per ogni singola attività di un [operazione in blocco](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/)ad esempio l&#39;importazione o l&#39;esportazione di articoli, la modifica dei prezzi su scala di massa e l&#39;assegnazione di prodotti a un magazzino. Obbligatorio quando [**Operazioni di amministrazione in blocco**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) opzione per [!DNL Inventory Management] è impostato su **Esegui in modo asincrono** nelle impostazioni di configurazione del sistema di amministrazione. |

{style="table-layout:auto"}

>[!NOTE]
>
>Per un elenco di tutti i consumer di messaggi di Adobe Commerce, consulta [Consumatori coda messaggi](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) nel _Guida alla configurazione_.

### Configurare i consumer di messaggi

Per evitare possibili problemi di elaborazione o ritardi, aggiungi i seguenti parametri quando [avvia il messaggio consumer](#start-message-consumers) funzionalità B2B.

- `--max-messages <value>`— Specifica il numero massimo di messaggi che ogni consumatore deve elaborare prima di terminare (impostazione predefinita = 10000). Sebbene non sia consigliato, è possibile utilizzare 0 per impedire al consumatore di terminare l’operazione. La best practice per un&#39;applicazione PHP consiste nel riavviare i processi a esecuzione prolungata per evitare possibili perdite di memoria.

- `--batch-size <value>`— Consente di limitare le risorse di sistema utilizzate dai consumatori (CPU, memoria). L’utilizzo di batch più piccoli riduce l’utilizzo delle risorse e, pertanto, rallenta l’elaborazione.  Se specificato, i messaggi in una coda vengono utilizzati in batch di `<value>` ciascuno. Questa opzione è applicabile solo al consumatore batch. Se `--batch-size` non è definito, il consumatore batch riceve tutti i messaggi disponibili in una coda.

Per informazioni sulle opzioni di configurazione aggiuntive, vedi [Configurazione specifica](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

### Avvia consumer di messaggi

Per abilitare le operazioni asincrone per le funzionalità B2B, devi avviare più consumer di messaggi.

1. Elencare i consumatori di messaggi disponibili:

   ```bash
   bin/magento queue:consumers:list
   ```

   Il comando restituisce i consumer di messaggi disponibili, inclusi tutti [Consumatori di messaggi B2B](#message-consumers).

1. Avvia ogni consumatore separatamente:

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   Ad esempio:

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>Per eseguirlo in background, aggiungi `&` al comando, tornare a un prompt e continuare a eseguire i comandi. Ad esempio: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Per ulteriori informazioni, consulta [Gestire le code dei messaggi](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) nel _Guida alla configurazione_.

### Aggiungi consumer di messaggi a cron

È possibile automatizzare la pianificazione di esecuzione per `SharedCatalogUpdateCategoryPermissions` e `SharedCatalogUpdatePrice` inviare messaggi ai consumatori aggiungendo la pianificazione al file di configurazione cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Puoi anche configurare le pianificazioni per i consumatori di messaggi da [Impostazioni configurazione archivio](../systems/cron.md) in Admin.

## Abilitare le funzioni B2B in Amministrazione

Dopo aver installato l’estensione B2B per Adobe Commerce e aver avviato i consumer di messaggi, devi anche: [abilitare le funzioni B2B in Admin](enable-basic-features.md).
