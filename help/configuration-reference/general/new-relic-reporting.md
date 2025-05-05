---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] dell'amministratore di Commerce.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>Queste opzioni di configurazione non si applicano ad Adobe Commerce su infrastruttura cloud.
>
>Se ti trovi nel piano Pro, New Relic è già [preconfigurato e abilitato per impostazione predefinita](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html?lang=it). Se si utilizza il piano Starter, è necessario completare i [passaggi di configurazione di New Relic](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html?lang=it#configure-new-relic-for-starter-environment) che fanno parte del processo di installazione.

## [!UICONTROL General]

![Generale](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/it/docs/commerce-admin/start/reporting/new-relic-reporting) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Visualizzazione store | Determina se il tuo archivio può essere utilizzato con il reporting di [!DNL New Relic]. Opzioni: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Visualizzazione store | L’URL in cui vengono distribuite le API di New Relic. Esempio: `https://api.newrelic.com/deployments.xml` |
| URL API approfondimenti | Visualizzazione store | L’URL in cui vengono distribuite le API di Insights. Utilizza il simbolo di percentuale (%) per rappresentare l’ID account. Esempio: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Visualizzazione store | L&#39;ID account assegnato al tuo account [!DNL New Relic]. |
| [!UICONTROL New Relic Application ID] | Visualizzazione store | L&#39;ID applicazione assegnato al tuo account [!DNL New Relic] per l&#39;integrazione di Commerce. |
| [!UICONTROL New Relic API Key] | Visualizzazione store | Chiave assegnata per l&#39;accesso all&#39;API [!DNL New Relic]. |
| [!UICONTROL Insights API Key] | Visualizzazione store | Chiave assegnata all&#39;utente per accedere a Insights. |
| [!UICONTROL New Relic Application Name] | Visualizzazione store | Nome assegnato all&#39;integrazione [!DNL New Relic]. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Visualizzazione store | Opzione per inviare i dati dei rapporti raccolti per la vetrina e per l’amministratore come app separate a New Relic. Questa opzione richiede un nome immesso per [!UICONTROL New Relic Application Name]. La funzione aggiunge il nome dell’applicazione con un carattere di sottolineatura ai dati dell’app raccolti. Esempio: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://experienceleague.adobe.com/it/docs/commerce-admin/systems/tools/cron) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Visualizzazione store | Determina se è possibile eseguire [!DNL New Relic] report secondo la pianificazione con [Cron](../../systems/cron.md). Opzioni: `Yes` / `No` |

{style="table-layout:auto"}
