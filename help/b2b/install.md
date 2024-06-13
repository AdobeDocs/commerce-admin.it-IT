---
title: Installare [!DNL Adobe Commerce B2B] estensione
description: Scopri come installare [!DNL Adobe Commerce B2B] metapacchetto.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: be36742aa1214e7e8e7f343051336cd3635099f4
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# Installare [!DNL Adobe Commerce B2B] estensione

L’estensione Adobe Commerce B2B, `magento/extension-b2b` è disponibile per tutte le versioni supportate di Adobe Commerce. Viene installato dopo l’installazione di Adobe Commerce.


## Requisiti

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html), tutte le versioni supportate
- PHP 8,1 / 8,2 / 8,3
- [!DNL Composer]

## Piattaforme supportate

- Adobe Commerce sull’infrastruttura cloud (ECE)
- Adobe Commerce on-premise (EE)

## Passaggi per l’installazione

>[!BEGINSHADEBOX]

**Prerequisiti**

- Accesso a [repo.magento.com](https://repo.magento.com/) per scaricare l&#39;estensione. Per generare le chiavi e ottenere i diritti necessari, consulta [Ottieni le chiavi di autenticazione](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Salva le chiavi di autenticazione per l&#39;installazione definendole globalmente nel tuo [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) directory. Oppure, salvali in un [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) nella directory principale dell’applicazione Adobe Commerce.

- [Versione supportata dell’estensione B2B](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability): determina la versione più recente dell’estensione B2B supportata nella versione di Adobe Commerce implementata.

- Consulta le note sulla versione per informazioni aggiornate sulla compatibilità delle versioni, sugli aggiornamenti o sulle modifiche che possono influenzare i requisiti di installazione o aggiornamento.

   - [Note sulla versione B2B](release-notes.md)
   - [Note sulla versione di Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Installare l’estensione B2B (`magento/b2b-extension`) utilizzando Composer. L’estensione è un metapacchetto di compositore che include la raccolta di moduli che abilitano le funzionalità B2B per un’istanza di Adobe Commerce. Per un elenco dei moduli inclusi, consulta [Pacchetti B2B](packages.md).

>[!BEGINTABS]

>[!TAB Infrastruttura cloud]

>[!TIP]
>
>Durante l’installazione di Adobe Commerce B2B su un’infrastruttura cloud, Adobe consiglia di implementare l’applicazione Adobe Commerce in un ambiente di integrazione o staging prima di iniziare.

L’Adobe consiglia di lavorare in un ramo di sviluppo quando aggiungi l’estensione B2B al progetto. Se non hai un ramo, consulta [Creare un ramo per lo sviluppo](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). Durante l’installazione dell’estensione B2B, il `Magento_B2b` il nome dell&#39;estensione viene inserito automaticamente nel `app/etc/config.php` file. Non è necessario modificare direttamente il file.

**Per installare l’estensione B2B**:

1. Sulla workstation locale, passa alla directory del progetto.

1. Creare o estrarre un ramo di sviluppo.

1. Aggiungere l’estensione B2B alla `require` sezione del `composer.json` file.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. Aggiornare le dipendenze del progetto.

   ```bash
   composer update
   ```

1. Aggiungi, conferma e invia modifiche al codice.

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >Inviando gli aggiornamenti all’ambiente cloud si avvia il processo di distribuzione cloud di Commerce per applicare le modifiche. Controlla lo stato della distribuzione da [registro di distribuzione](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). Se riscontri errori di distribuzione, consulta [Ripristino da guasto componente](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Al termine della build e della distribuzione, utilizza SSH per accedere all’ambiente remoto e verificare che l’estensione B2B sia installata e abilitata.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Il nome di un’estensione utilizza il formato: `<VendorName>_<ComponentName>`.

   Risposta di esempio:

   ```terminal
   Magento_B2b : Module is enabled
   ```

>[!TAB On-premise]

1. Dalla directory principale dell’applicazione Adobe Commerce, aggiorna la `composer.json` per aggiungere le dipendenze per l’estensione B2B:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Se si verifica un errore, ad esempio:

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Controlla l’ortografia del pacchetto, il vincolo di versione e che il pacchetto sia disponibile e corrisponda al requisito di stabilità minima (stabile).

1. Se richiesto, immetti [chiavi di autenticazione](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

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

>[!ENDTABS]

Al termine dell’installazione, configura e avvia gli utenti dei messaggi.

## Consumatori di messaggi

L’estensione Adobe Commerce B2B utilizza MySQL per la gestione della coda dei messaggi. Nella tabella seguente sono elencati i consumer di messaggi che supportano le funzionalità B2B. Dopo aver installato l’estensione, avvia il messaggio consumer per le funzionalità B2B necessarie per la vetrina Commerce.

| Consumatore | Descrizione |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Aggiorna il prezzo di ogni prodotto in un catalogo condiviso. Obbligatorio quando [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `sharedCatalogUpdateCategoryPermissions` | Aggiorna le categorie assegnate a una categoria di catalogo condiviso. Obbligatorio quando [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `negotiableQuotePriceUpdate` | Aggiorna i prezzi per i preventivi negoziabili. Obbligatorio quando [**[!UICONTROL Quotes]**](quotes.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `purchaseorder.toorder` | Converte l&#39;ordine fornitore in ordine. Obbligatorio quando [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `purchaseorder.transactional.email` | Invia e-mail ordine fornitore. Obbligatorio quando [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `purchaseorder.validation` | Convalida l&#39;ordine fornitore a fronte dei relativi [regole di approvazione](account-dashboard-approval-rules.md). Obbligatorio quando [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `quoteItemCleaner` | Elimina i preventivi di prezzo non validi o inattivi quando un prodotto viene eliminato dal catalogo o rimosso dal carrello. Obbligatorio quando [**[!UICONTROL Quotes]**](quotes.md) nelle impostazioni di configurazione del sistema di amministrazione. |
| `inventoryQtyCounter` | Corregge in modo asincrono l&#39;indice azionario dopo aver effettuato un ordine o rimosso un prodotto. Obbligatorio quando [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) è abilitata per Inventory management nelle impostazioni di configurazione dell’amministratore. Consulta [Best practice per le prestazioni](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Crea messaggi per ogni singola attività di un [operazione in blocco](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/) ad esempio l&#39;importazione o l&#39;esportazione di articoli, la modifica dei prezzi su scala di massa e l&#39;assegnazione di prodotti a un magazzino. Obbligatorio quando [**Operazioni di amministrazione in blocco**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) opzione per [!DNL Inventory Management] è impostato su **Esegui in modo asincrono** nelle impostazioni di configurazione del sistema di amministrazione. |

{style="table-layout:auto"}

>[!NOTE]
>
>Per un elenco di tutti i consumer di messaggi di Adobe Commerce, consulta [Consumatori coda messaggi](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) nel _Guida alla configurazione_.

### Configurare i consumer di messaggi

Per evitare possibili problemi di elaborazione o ritardi, aggiungi i seguenti parametri quando [avvia il messaggio consumer](#start-message-consumers) funzionalità B2B.

- `--max-messages <value>`— Specifica il numero massimo di messaggi che ogni consumatore deve elaborare prima di terminare (impostazione predefinita = 10000). Anche se Adobe non lo consiglia, è possibile utilizzare 0 per impedire al consumatore di terminare. La best practice per un&#39;applicazione PHP consiste nel riavviare i processi a esecuzione prolungata per evitare possibili perdite di memoria.

- `--batch-size <value>`— Consente di limitare le risorse di sistema utilizzate dai consumatori (CPU, memoria). L’utilizzo di batch più piccoli riduce l’utilizzo delle risorse e, pertanto, rallenta l’elaborazione.  Se specificato, i messaggi in una coda vengono utilizzati in batch di `<value>` ciascuno. Questa opzione è applicabile solo al consumatore batch. Se `--batch-size` non è definito, il consumatore batch riceve tutti i messaggi disponibili in una coda.

Per informazioni sulle opzioni di configurazione aggiuntive, vedi [Configurazione specifica](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

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

Per ulteriori informazioni, consulta [Gestire le code dei messaggi](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) nel _Guida alla configurazione_.

### Aggiungi consumer di messaggi a cron

Puoi automatizzare la pianificazione dell’esecuzione per `SharedCatalogUpdateCategoryPermissions` e `SharedCatalogUpdatePrice` inviare messaggi ai consumatori aggiungendo la pianificazione al file di configurazione cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Puoi anche configurare le pianificazioni per i consumatori di messaggi da [Impostazioni configurazione archivio](../systems/cron.md) in Admin.

## Abilitare le funzioni B2B in Amministrazione

Dopo aver installato l’estensione Adobe Commerce B2B e aver avviato i consumer di messaggi, devi anche: [abilitare le funzioni B2B in Admin](enable-basic-features.md).

