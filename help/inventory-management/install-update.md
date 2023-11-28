---
title: "Installare, aggiornare e rimuovere [!DNL Inventory Management]"
description: Scopri come gestire [!DNL Inventory Management] metapacchetto.
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
source-git-commit: d6c81da4b4e0674d6699e9781921ccb2160b9983
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Installare, aggiornare e rimuovere [!DNL Inventory Management]

[!DNL Inventory Management] I moduli forniscono tutte le funzioni e le opzioni di inventario per i commercianti di origini singole e multiple per gestire le quantità di prodotti e le scorte per i canali di vendita. Queste funzioni sono disponibili nelle versioni 2.4.x di Adobe Commerce e Magento Open Source.

Queste funzioni ed estensioni sono state sviluppate come parte della [Progetto di magazzino](https://github.com/magento/inventory) tramite il programma di ingegneria della community di Magento Open Source.

[!DNL Inventory Management] installa nelle versioni 2.3.x e 2.4.x di Adobe Commerce e Magento Open Source, con tutte le funzioni abilitate per impostazione predefinita. Non sono necessari passaggi aggiuntivi per abilitare queste funzioni di inventario. Gli aggiornamenti da v2.1.x o 2.2.x possono richiedere passaggi aggiuntivi. Consulta [Aggiornare Inventory management](#upgrade-inventory-management).

Installazione secondo [Installazione rapida on-premise](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"} è consigliato. Installa con un metapacchetto per ricevere tutti [!DNL Inventory Management] moduli.

La riga seguente nella `composer.json` installazioni di metapackage [!DNL Inventory Management]:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Per un elenco di [!DNL Inventory Management] versioni di metapackage, vedi [note sulla versione](release-notes.md).

Il [!DNL Inventory Management] Il processo di installazione aggiunge tutti i moduli al `<Magento_installation_directory>/app/etc/config.php` file. A `1` Il valore indica che il modulo corrispondente è abilitato. È aggiunto il seguente elenco di moduli:

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## Abilita [!DNL Inventory Management] funzioni

Una volta installato, aggiornato o aggiornato, _[!UICONTROL Manage Stock]_in Admin è attivata per impostazione predefinita. Questa opzione consente la registrazione e la gestione dell&#39;inventario, ma non influisce sullo stato del modulo. Per disattivare i moduli, consulta la sezione successiva.

Per ulteriori informazioni sulle configurazioni, consulta [Configurare Inventory management](configuration.md).

## Disabilita Inventory management

>[!IMPORTANT]
>
>Utilizzo del valore predefinito [!DNL Inventory Management] è vivamente consigliato. L&#39;alternativa [!DNL CatalogInventory] che viene utilizzato per i sistemi con disabilitato [!DNL Inventory Management] moduli, è ora obsoleto. Disattivazione di [!DNL Inventory Management] I moduli possono causare un sistema instabile e causare vari problemi.

Potrebbe essere necessario disattivare [!DNL Inventory Management] moduli per:

* Accelera il processo di aggiornamento per i commercianti che eseguono la migrazione da 2.0.x, 2.1.x, 2.2.x o da 2.3.x a 2.4.x.
* Utilizza moduli personalizzati o di terze parti per il sistema di gestione degli ordini e delle scorte.

Consulta la [Abilitare o disabilitare i moduli](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) pagina in _Guida all’installazione_ per informazioni su come disattivare i moduli applicabili.

Una volta completato, il sistema fornisce un elenco di moduli e valori in `<Magento_installation_directory>/app/etc/config.php`, a partire da:

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>Se sono installati i moduli Connettore OMS, assicurarsi di non disattivare `Magento_InventoryMessageBus` modulo, che è un modulo Connector. È necessario utilizzare il connettore con OMS.

## Rimuovi Inventory management

>[!IMPORTANT]
>
>Utilizzo del valore predefinito [!DNL Inventory Management] è vivamente consigliato. L&#39;alternativa [!DNL CatalogInventory] modulo, utilizzato per sistemi con rimossi [!DNL Inventory Management] moduli, è ora obsoleto. Rimozione di [!DNL Inventory Management] I moduli possono causare un sistema instabile e causare vari problemi.

Se scegli di non utilizzare il [!DNL Inventory Management] , è possibile rimuovere (disinstallare) questi moduli. Per rimuovere tutti i moduli tramite il file del compositore, aggiungi quanto segue a `composer.json`:

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

Una volta completata la modifica, esegui l’installazione del compositore e rimuove automaticamente questi moduli di Inventory management.

## Aggiornare Inventory management

### Precedente [!DNL Commerce] versioni

Durante l’aggiornamento o l’aggiornamento di un’installazione esistente 2.1.x, 2.2.x o 2.3.x in Adobe Commerce o Magento Open Source 2.4.x, [!DNL Inventory Management] I moduli sono disabilitati per impostazione predefinita. Questa impostazione predefinita è una precauzione per evitare aggiornamenti incompatibili con le versioni precedenti e per supportare meglio Order Management (OMS).

>[!NOTE]
>
>Order Management non supporta [!DNL Inventory Management]. Durante l&#39;upgrade, [!DNL Inventory Management] I moduli sono disattivati per consentire OMS e [!DNL Commerce] 2.3.x per funzionare senza problemi.


Per abilitare [!DNL Inventory Management] moduli:

1. Modifica il `<Commerce_installation_directory>/app/etc/config.php` file.
1. Modifica tutti i moduli Inventory da `0` a `1` per attivare.
1. Aggiornare il database:

   ```bash
   bin/magento setup:upgrade
   ```

1. Pulisci la cache:

   ```bash
   bin/magento cache:clean
   ```

Si consiglia di utilizzare il [comandi di prenotazione incoerenze](cli.md) dopo l&#39;upgrade. Durante l&#39;aggiornamento, tutti i prodotti vengono aggiunti al magazzino predefinito. Se sono presenti ordini in sospeso, i comandi aggiornano correttamente la quantità e gli impegni di vendita per l&#39;evasione degli ordini e delle vendite.

### Precedente [!DNL Inventory Management] versioni

Durante l’aggiornamento da versioni precedenti di [!DNL Inventory Management] alla versione più recente, segui i normali passaggi per l’aggiornamento dell’estensione.

Al più tardi, aggiorna la versione del metapackage:

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Per ulteriori informazioni sugli aggiornamenti di Commerce, consulta le seguenti guide:

* [Guida all’aggiornamento di Commerce](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [Abilitare o disabilitare i moduli](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
