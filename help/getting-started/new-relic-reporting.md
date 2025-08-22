---
title: Generazione rapporti di [!DNL New Relic]
description: Scopri il  [!DNL New Relic] reporting disponibile per gli account di Adobe Commerce sull'infrastruttura cloud, che include il software per il servizio New Relic APM.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: c406add80981387305755221f21624dad475e63f
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# Generazione rapporti di [!DNL New Relic]

[New Relic][1] è un servizio di analisi del software che consente di analizzare e migliorare le interazioni delle applicazioni. Gli account per Adobe Commerce sull&#39;infrastruttura cloud includono il software per il servizio [!DNL New Relic APM]. Per ulteriori informazioni, vedere [Servizi New Relic][4] nella _Guida all&#39;infrastruttura cloud di Commerce_.

## Passaggio 1: registrarsi a un account [!DNL New Relic]

1. Vai al sito Web [[!DNL New Relic]][1] e registrati per un account.

   Puoi anche iscriverti a un account di prova gratuito.

1. Seguire le istruzioni sul sito. Quando richiesto, scegliere il prodotto da installare per primo.

1. Mentre ti trovi nel tuo account, individua le seguenti credenziali necessarie per completare la configurazione di Commerce:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | ID account | Dal dashboard account [!DNL New Relic], l&#39;ID account è il numero nell&#39;URL dopo: `/accounts` |
   | ID applicazione | Dal dashboard dell&#39;account [!DNL New Relic], fai clic su **[!UICONTROL New Relic APM]**. Nel menu, scegliere **[!UICONTROL Applications]**. Quindi, scegli l’applicazione. ID applicazione è il numero nell&#39;URL dopo: `/applications/` |
   | Chiave API New Relic | Dal dashboard dell&#39;account [!DNL New Relic], fai clic su **[!UICONTROL Account Settings]**. Nel menu a sinistra in Integrazioni, scegli **[!UICONTROL Data Sharing]**. Puoi creare, rigenerare o eliminare la chiave API da questa pagina. |
   | Chiave API approfondimenti | Dal dashboard dell&#39;account [!DNL New Relic], fai clic su **[!UICONTROL Insights]**. Nel menu a sinistra di Amministrazione, scegliere **[!UICONTROL API Keys]**. Le chiavi API di Insights vengono visualizzate in questa pagina. Se necessario, fare clic sul segno più (**+**) accanto a Inserisci chiavi per generare una chiave. |

   {style="table-layout:auto"}

## Passaggio 2: installare l&#39;agente [!DNL New Relic] sul server

Per utilizzare [!DNL New Relic APM Pro] per raccogliere e trasmettere dati, è necessario che l&#39;agente PHP sia installato nel server.

1. Quando viene richiesto di scegliere un agente Web, fare clic su **PHP**.

1. Per configurare l&#39;agente PHP sul server, seguire le istruzioni.

   Se hai bisogno di aiuto, consulta [New Relic per PHP][3].

1. Verificare che cron sia in esecuzione sul server.

   Per ulteriori informazioni, consulta [Configurare ed eseguire cron][5] nella documentazione per gli sviluppatori.

## Passaggio 3: configurare lo store

>[!NOTE]
>Queste opzioni di configurazione non si applicano ad Adobe Commerce su infrastruttura cloud.
>
>Se ti trovi nel piano Pro, New Relic è già [preconfigurato e abilitato per impostazione predefinita](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Se si utilizza il piano Starter, è necessario completare i [passaggi di configurazione di New Relic](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) che fanno parte del processo di installazione.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra in cui è espanso **[!UICONTROL General]**, scegliere **[!UICONTROL New Relic Reporting]** ed effettuare le seguenti operazioni:

   ![Configurazione report New Relic](./assets/new-relic-reporting-general.png){width="600"}

   * Imposta **[!UICONTROL Enable New Relic Integration]** su `Yes`.

   * In **[!UICONTROL Insights API URL]**, sostituisci il simbolo di percentuale (`%`) con l&#39;ID account New Relic.

   * Immetti **[!UICONTROL New Relic Account ID]**.

   * Immetti **[!UICONTROL New Relic Application ID]**.

   * Immetti **[!UICONTROL New Relic API Key]**.

   * Immetti **[!UICONTROL Insights API Key]**.

1. Per **[!UICONTROL New Relic Application Name]**, immettere un nome per identificare la configurazione per il riferimento interno.

1. (Facoltativo) Per **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, selezionare `Yes` per inviare i dati raccolti per la vetrina e Admin come app separate a New Relic.

   Questa opzione richiede un nome immesso per **[!UICONTROL New Relic Application Name]**.

   >[!NOTE]
   >
   >L&#39;abilitazione di questa funzione riduce il numero di falsi positivi [!DNL New Relic] avvisi e consente di configurare il monitoraggio e gli avvisi in modo rigoroso per le prestazioni front-end. New Relic riceve file di dati app separati con nomi di applicazione aggiunti a `Adminhtml` e front-end. Esempio: `MyStore_Adminhtml`

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Passaggio 4: abilitare Cron per il reporting di [!DNL New Relic]

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Cron]**.

   ![Configurazione New Relic Cron](./assets/new-relic-reporting-cron.png){width="600"}

1. Imposta **[!UICONTROL Enable Cron]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## [!DNL New Relic] query

I dati di [!DNL New Relic Insights] si basano su istruzioni scritte in [!DNL New Relic Query Language] (NRQL) e su eventuali parametri personalizzati che è possibile includere. I dati possono essere restituiti da query ad hoc o da query salvate nel dashboard. Per ulteriori informazioni, consulta il [Riferimento NRQL][6] nella documentazione di [!DNL New Relic].

### Eventi di amministrazione

#### Utenti amministratori attivi

Restituisce il numero di utenti amministratori attivi.

    SELECT uniqueCount(AdminId)
    FROM Transaction
    WHERE appName=&#39;&lt;nome_app>&#39; DA 15 minuti fa

#### Utenti amministratori attualmente attivi

Restituisce i nomi degli utenti amministratori attivi.

    SELECT uniques(AdminName)
    FROM Transaction
    WHERE appName=&#39;&lt;nome_app>&#39; DA 15 minuti fa

#### Attività amministratore recente

Restituisce il numero di azioni Amministratore recenti.

    SELECT count(AdminId)
    FROM Transaction
    WHERE appName =&#39;&lt;nome_app>&#39; FACET AdminName FROM 1 giorno fa

#### Ultima attività amministratore

Restituisce informazioni dettagliate sulle azioni di amministrazione recenti, inclusi il nome utente, la durata e il nome dell&#39;applicazione Admin.

    SELECT AdminName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;nome_app>&#39; AND AdminName IS NOT NULL
    AND AdminName != LIMITE &#39;N/D&#39; 50

### Eventi Cron

#### Conteggio categorie

Restituisce il numero di eventi applicazione per categoria durante il periodo di tempo specificato.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    E appName = &#39;&lt;nome_app>&#39; TIMESERIES 2 minuti

#### Conteggio catalogo corrente

Restituisce il numero medio di eventi applicazione nel catalogo per categoria durante il periodo di tempo specificato.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND CatalogCategoryCount > 0
    AND nomeApp = &#39;&lt;nome_app>&#39; DA 2 minuti fa LIMIT 1

#### Prodotti attivi

Restituisce il numero di eventi di applicazione per prodotto durante il periodo di tempo specificato.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    E appName = &#39;&lt;nome_app>&#39; TIMESERIES 2 minuti

#### Conteggio prodotti attivi

Restituisce il numero medio di eventi di applicazione attivi per prodotto durante il periodo di tempo specificato.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount NON È NULL
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;nome_app>&#39; da 2 minuti fa LIMIT 1

#### Prodotti configurabili

Restituisce il numero medio di eventi dell&#39;applicazione per i prodotti configurabili durante il periodo di tempo specificato.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount NON È NULL
    E appName = &#39;&lt;nome_app>&#39; TIMESERIES 2 minuti

#### Numero di prodotti configurabili

Restituisce il numero medio di eventi dell&#39;applicazione per prodotto configurabile durante il periodo di tempo specificato.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount NON È NULL
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;nome_app>&#39; DA 2 minuti fa LIMIT 1

#### Numero di prodotti (tutti)

Restituisce il numero totale di eventi di applicazione per tutti i prodotti.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    E appName = &#39;&lt;nome_app>&#39; TIMESERIES 2 minuti

#### Numero di prodotti corrente (tutti)

Restituisce il numero medio di eventi dell&#39;applicazione per tutti i prodotti durante il periodo di tempo specificato.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount NON È NULL
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;nome_app>&#39; da 2 minuti fa LIMIT 1

#### Conteggio clienti

Restituisce il numero medio di eventi applicazione per cliente.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0&lt;
    AND nomeApp = &#39;&lt;nome_app>&#39; TIMESERIES 2 minutes

#### Conteggio clienti corrente

Restituisce il numero medio di clienti durante il periodo di tempo specificato.

    SELECT average(CustomerCount)
    FROM Cron
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0
    AND nomeApp = &#39;&lt;nome_app>&#39; FROM 2 minuti ago LIMIT 1

#### Stato del modulo

Restituisce il numero medio di volte in cui i moduli applicativi vengono attivati, disattivati o installati durante il periodo di tempo specificato.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron&lt;
    WHERE nomeApp = &#39;&lt;nome_app>&#39; TIMESERIES 2 minuti

#### Stato del modulo corrente

Restituisce il numero medio di volte in cui i moduli sono stati attivati, disattivati o installati durante il periodo di tempo specificato.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron
    WHERE nomeApp = &#39;&lt;nome_app>&#39; DA 2 minuti fa LIMIT 1

#### Conteggi di siti web e store

Restituisce il numero medio di eventi dell&#39;applicazione per sito Web e archivio durante il periodo di tempo specificato.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE nomeApp = &#39;&lt;your_app_name&gt;&#39; TIMESERIES 2 minuti

#### Conteggi correnti per siti Web e store

Restituisce il numero medio di eventi dell&#39;applicazione correnti durante il periodo di tempo specificato.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE nomeApp = &#39;&lt;nome_app_utente>&#39; DA 2 minuti fa LIMIT 1

#### Cron: tutti i dati dell’evento

Restituisce tutti i dati evento applicazione.

    SELEZIONA *
    DA Cron
    WHERE nomeApp = &#39;&lt;nome_app>&#39;

### Clienti

#### Conteggio clienti attivi

Restituisce il numero di clienti attivi durante il periodo di tempo specificato.

    SELECT uniqueCount(CustomerId)
    FROM Transaction
    WHERE nomeApp = &#39;&lt;nome_app>&#39; DA 15 minuti fa

#### Clienti attivi

Restituisce i nomi dei clienti attivi durante il periodo di tempo specificato.

    SELECT uniques(CustomerName)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; FROM 15 minuti fa

#### Clienti principali

Restituisce i clienti principali durante il periodo di tempo specificato.

    SELECT count(CustomerId)
    FROM Transaction
    WHERE nomeApp = &#39;&lt;nome_app>&#39; FACET NomeCliente DA 1 giorno fa

#### Attività amministratore recente

Restituisce un numero definito di record di attività recenti, che includono il nome del cliente e la durata della visita.

    SELECT NomeCliente, durata, nome
    FROM Transazione
    WHERE NomeApp=&#39;&lt;nome_app>&#39;
    AND NomeCliente IS NOT NULL
    AND NomeCliente != LIMITE &#39;N/D&#39; 50

### Ordini

#### Numero di ordini effettuati

Restituisce il numero di ordini effettuati durante il periodo di tempo specificato.

    SELECT count(Order)
    FROM Transazione FROM 1 giorno fa

#### Valore totale dell’ordine

Restituisce il numero totale di righe ordinate durante il periodo di tempo specificato.

    SELECT sum(orderValue)
    FROM Transazione DA 1 giorno fa

#### Totale elementi riga ordinati

Restituisce il numero totale di righe ordinate durante il periodo di tempo specificato.

    SELECT sum(lineItemCount)
    FROM Transazione DA 1 giorno fa


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
