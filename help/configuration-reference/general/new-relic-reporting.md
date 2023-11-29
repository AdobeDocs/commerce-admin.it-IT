---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] pagina dell’amministratore di Commerce.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 4%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

## [!UICONTROL General]

![Generale](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Visualizzazione store | Determina se il tuo archivio può essere utilizzato con [!DNL New Relic] Generazione rapporti. Opzioni: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Visualizzazione store | L’URL in cui vengono distribuite le API di New Relic. Ad esempio: `https://api.newrelic.com/deployments.xml` |
| URL API approfondimenti | Visualizzazione store | L’URL in cui vengono distribuite le API di Insights. Utilizza il simbolo di percentuale (%) per rappresentare l’ID account. Ad esempio: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Visualizzazione store | L&#39;ID account assegnato al tuo [!DNL New Relic] account. |
| [!UICONTROL New Relic Application ID] | Visualizzazione store | L&#39;ID applicazione assegnato al tuo [!DNL New Relic] account per l’integrazione con Commerce. |
| [!UICONTROL New Relic API Key] | Visualizzazione store | Chiave assegnata all&#39;utente per l&#39;accesso al [!DNL New Relic] API. |
| [!UICONTROL Insights API Key] | Visualizzazione store | Chiave assegnata all&#39;utente per accedere a Insights. |
| [!UICONTROL New Relic Application Name] | Visualizzazione store | Nome assegnato al tuo [!DNL New Relic] integrazione. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Visualizzazione store | Opzione per inviare i dati dei rapporti raccolti per la vetrina e per l’amministratore come app separate a New Relic. Questa opzione richiede un nome immesso per [!UICONTROL New Relic Application Name]. La funzione aggiunge il nome dell’applicazione con un carattere di sottolineatura ai dati dell’app raccolti. Ad esempio: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Visualizzazione store | Determina se [!DNL New Relic] i rapporti possono essere eseguiti secondo programma con [Cron](../../systems/cron.md). Opzioni: `Yes` / `No` |

{style="table-layout:auto"}
