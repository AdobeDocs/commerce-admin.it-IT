---
title: Installa l'estensione  [!DNL Adobe Commerce B2B]
description: Scopri come installare il metapackage  [!DNL Adobe Commerce B2B] .
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---


# Installa l&#39;estensione [!DNL Adobe Commerce B2B]

L&#39;estensione Adobe Commerce B2B `magento/extension-b2b` è disponibile per tutte le versioni supportate di Adobe Commerce. Viene installato dopo l’installazione di Adobe Commerce.


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

- Accedi a [repo.magento.com](https://repo.magento.com/) per scaricare l&#39;estensione. Per generare le chiavi e ottenere i diritti necessari, vedere [Ottenere le chiavi di autenticazione](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

  Salva le chiavi di autenticazione per l&#39;installazione definendole globalmente nella directory [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home). In alternativa, salvarli in un file [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) nella directory principale dell&#39;applicazione Adobe Commerce.

- [Versione supportata dell&#39;estensione B2B](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability)-Determinare la versione più recente dell&#39;estensione B2B supportata nella versione distribuita di Adobe Commerce.

- Consulta le note sulla versione per informazioni aggiornate sulla compatibilità delle versioni, sugli aggiornamenti o sulle modifiche che possono influenzare i requisiti di installazione o aggiornamento.

   - [Note sulla versione B2B](release-notes.md)
   - [Note sulla versione di Adobe Commerce](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Installare l&#39;estensione B2B (`magento/b2b-extension`) tramite Composer. L’estensione è un metapacchetto di compositore che include la raccolta di moduli che abilitano le funzionalità B2B per un’istanza di Adobe Commerce. Per un elenco dei moduli inclusi, vedere [Pacchetti B2B](packages.md).

>[!BEGINTABS]

>[!TAB Infrastruttura cloud]

>[!TIP]
>
>Durante l’installazione di Adobe Commerce B2B su un’infrastruttura cloud, Adobe consiglia di implementare l’applicazione Adobe Commerce in un ambiente di integrazione o staging prima di iniziare.

L’Adobe consiglia di lavorare in un ramo di sviluppo quando aggiungi l’estensione B2B al progetto. Se non hai un ramo, vedi [Crea un ramo per lo sviluppo](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches). Durante l&#39;installazione dell&#39;estensione B2B, il nome dell&#39;estensione `Magento_B2b` viene inserito automaticamente nel file `app/etc/config.php`. Non è necessario modificare direttamente il file.

**Per installare l&#39;estensione B2B**:

1. Sulla workstation locale, passa alla directory del progetto.

1. Creare o estrarre un ramo di sviluppo.

1. Aggiungere l&#39;estensione B2B alla sezione `require` del file `composer.json`.

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
   >Inviando gli aggiornamenti all’ambiente cloud si avvia il processo di distribuzione cloud di Commerce per applicare le modifiche. Controllare lo stato della distribuzione dal [registro distribuzione](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process). Se si verificano errori di distribuzione, vedere [Ripristino da errore del componente](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment).

1. Al termine della build e della distribuzione, utilizza SSH per accedere all’ambiente remoto e verificare che l’estensione B2B sia installata e abilitata.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   Un nome di estensione utilizza il formato: `<VendorName>_<ComponentName>`.

   Risposta di esempio:

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB Locale]

1. Dalla directory radice dell&#39;applicazione Adobe Commerce, aggiornare `composer.json` per aggiungere le dipendenze per l&#39;estensione B2B:

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   Se si verifica un errore, ad esempio:

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   Controlla l’ortografia del pacchetto, il vincolo di versione e che il pacchetto sia disponibile e corrisponda al requisito di stabilità minima (stabile).

1. Se richiesto, immettere le [chiavi di autenticazione](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys).

   La _chiave pubblica_ è il tuo nome utente; la tua _chiave privata_ è la tua password. Se le chiavi pubbliche e private sono state archiviate in `auth.json`, non verrà richiesto di eseguire l&#39;autenticazione.

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
   >In modalità di produzione, è possibile che si riceva un messaggio a `Please rerun Magento compile command`. Immettere i comandi per completare l&#39;installazione. Adobe Commerce non richiede di eseguire il comando di compilazione in modalità Sviluppatore.

>[!ENDTABS]

Al termine dell’installazione, configura e avvia gli utenti dei messaggi.

## Consumatori di messaggi

L’estensione Adobe Commerce B2B utilizza MySQL per la gestione della coda dei messaggi. Nella tabella seguente sono elencati i consumer di messaggi che supportano le funzionalità B2B. Dopo aver installato l’estensione, avvia il messaggio consumer per le funzionalità B2B necessarie per la vetrina Commerce.

| Consumatore | Descrizione |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | Aggiorna il prezzo di ogni prodotto in un catalogo condiviso. Obbligatorio se l&#39;opzione [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) è abilitata nelle impostazioni di configurazione di Admin System. |
| `sharedCatalogUpdateCategoryPermissions` | Aggiorna le categorie assegnate a una categoria di catalogo condiviso. Obbligatorio se l&#39;opzione [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) è abilitata nelle impostazioni di configurazione di Admin System. |
| `negotiableQuotePriceUpdate` | Aggiorna i prezzi per i preventivi negoziabili. Obbligatorio se l&#39;opzione [**[!UICONTROL Quotes]**](quotes.md) è abilitata nelle impostazioni di configurazione di Admin System. |
| `purchaseorder.toorder` | Converte l&#39;ordine fornitore in ordine. Obbligatorio se l&#39;opzione [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) è abilitata nelle impostazioni di configurazione di Admin System. |
| `purchaseorder.transactional.email` | Invia e-mail ordine fornitore. Obbligatorio se l&#39;opzione [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) è abilitata nelle impostazioni di configurazione di Admin System. |
| `purchaseorder.validation` | Convalida l&#39;ordine fornitore in base alle [regole di approvazione](account-dashboard-approval-rules.md) pertinenti. Obbligatorio se l&#39;opzione [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) è abilitata nelle impostazioni di configurazione di Admin System. |
| `quoteItemCleaner` | Elimina i preventivi di prezzo non validi o inattivi quando un prodotto viene eliminato dal catalogo o rimosso dal carrello. Obbligatorio se l&#39;opzione [**[!UICONTROL Quotes]**](quotes.md) è abilitata nelle impostazioni di configurazione di Admin System. |
| `inventoryQtyCounter` | Corregge in modo asincrono l&#39;indice azionario dopo aver effettuato un ordine o rimosso un prodotto. Obbligatorio se l&#39;opzione [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) è abilitata per Inventory management nelle impostazioni di configurazione dell&#39;amministratore. Consulta [Best practice per le prestazioni](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update). |
| `async.operations.all` | Crea messaggi per ogni singola attività di una [operazione in blocco](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/), ad esempio l&#39;importazione o l&#39;esportazione di articoli, la modifica dei prezzi su scala di massa e l&#39;assegnazione di prodotti a un magazzino. Obbligatorio se l&#39;opzione [**Operazioni collettive di amministrazione**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) per [!DNL Inventory Management] è impostata su **Esegui in modo asincrono** nelle impostazioni di configurazione di Admin System. |

{style="table-layout:auto"}

>[!NOTE]
>
>Per un elenco di tutti i consumer di messaggi di Adobe Commerce, vedere [Consumer di code di messaggi](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers) nella _Guida alla configurazione_.

### Configurare i consumer di messaggi

Per evitare possibili problemi di elaborazione o ritardi, aggiungi i seguenti parametri quando [avvii il messaggio consumer](#start-message-consumers) per le funzionalità B2B.

- `--max-messages <value>`— Specifica il numero massimo di messaggi che ogni consumer deve elaborare prima di terminare (impostazione predefinita = 10000). Anche se Adobe non lo consiglia, è possibile utilizzare 0 per impedire al consumatore di terminare. La best practice per un&#39;applicazione PHP consiste nel riavviare i processi a esecuzione prolungata per evitare possibili perdite di memoria.

- `--batch-size <value>`: consente di limitare le risorse di sistema utilizzate dai consumatori (CPU, memoria). L’utilizzo di batch più piccoli riduce l’utilizzo delle risorse e, pertanto, rallenta l’elaborazione.  Se specificato, i messaggi in una coda vengono utilizzati in batch di `<value>` ciascuno. Questa opzione è applicabile solo al consumatore batch. Se `--batch-size` non è definito, il consumer batch riceve tutti i messaggi disponibili in una coda.

Per informazioni sulle opzioni di configurazione aggiuntive, vedere [Specific-configuration](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration).

### Avvia consumer di messaggi

Per abilitare le operazioni asincrone per le funzionalità B2B, devi avviare più consumer di messaggi.

1. Elencare i consumatori di messaggi disponibili:

   ```bash
   bin/magento queue:consumers:list
   ```

   Il comando restituisce i consumer di messaggi disponibili, inclusi tutti i [consumer di messaggi B2B](#message-consumers).

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
>Per eseguirlo in background, aggiungere `&` al comando, tornare a un prompt e continuare a eseguire i comandi. Esempio: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

Per ulteriori informazioni, vedere [Gestione delle code di messaggi](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues) nella _Guida alla configurazione_.

### Aggiungi consumer di messaggi a cron

È possibile automatizzare la pianificazione dell&#39;esecuzione per i consumer di messaggi `SharedCatalogUpdateCategoryPermissions` e `SharedCatalogUpdatePrice` aggiungendo la pianificazione al file di configurazione cron [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management).

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

Puoi anche configurare le pianificazioni per i consumer di messaggi dalle [Impostazioni configurazione archivio](../systems/cron.md) nell&#39;amministratore.

## Abilitare le funzioni B2B in Amministrazione

Dopo aver installato l&#39;estensione Adobe Commerce B2B e aver avviato i consumer di messaggi, devi anche [abilitare le funzionalità B2B in Amministrazione](enable-basic-features.md).

