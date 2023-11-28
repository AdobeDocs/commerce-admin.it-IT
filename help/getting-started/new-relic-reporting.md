---
title: '[!DNL New Relic]'' reporting'''
description: Scopri informazioni sui [!DNL New Relic] report disponibili per gli account per Adobe Systems Commerce su infrastruttura cloud, che include il software per il servizio Nuovo Relic APM.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: e9a7645aed0e3b48bf565b04cdb6a31ce5d39ca0
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 0%

---

# [!DNL New Relic] reportistica

[New Relic][1] è un servizio di analisi del software che consente di analizzare e migliorare le interazioni tra le applicazioni. Gli account per Adobe Commerce sull’infrastruttura cloud includono il software per [!DNL New Relic APM] servizio. Per ulteriori informazioni, consulta [Servizi New Relic][4] nel _Guida di Commerce su infrastruttura cloud_.

## Passaggio 1: registrarsi a [!DNL New Relic] account

1. Vai al [[!DNL New Relic]][1] sito Web e registrati per un account.

   Puoi anche iscriverti per una versione di prova gratuito account.

1. Segui le istruzioni sul sito. Quando richiesto, scegliere per primo il prodotto che si desidera installare.

1. Durante il account, individuare le seguenti credenziali necessarie per completare la configurazione di Commerce:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | ID account | Dal tuo [!DNL New Relic] account, l’ID account è il numero nell’URL dopo: `/accounts` |
   | ID applicazione | Dal tuo [!DNL New Relic] dashboard account, fai clic su **[!UICONTROL New Relic APM]**. Nel menu, scegli **[!UICONTROL Applications]**. Quindi, scegli l’applicazione. L’ID applicazione è il numero nell’URL dopo: `/applications/` |
   | Chiave API New Relic | Dal tuo [!DNL New Relic] dashboard account, fai clic su **[!UICONTROL Account Settings]**. Nel menu a sinistra in Integrazioni, scegli **[!UICONTROL Data Sharing]**. Puoi creare, rigenerare o eliminare la chiave API da questa pagina. |
   | Chiave API approfondimenti | Dal tuo [!DNL New Relic] dashboard account, fai clic su **[!UICONTROL Insights]**. Nel menu a sinistra in Amministrazione, scegli **[!UICONTROL API Keys]**. Le chiavi API di Insights vengono visualizzate in questa pagina. Se necessario, fare clic sul segno più (**+**) accanto a Inserisci chiavi per generare una chiave. |

   {style="table-layout:auto"}

## Passaggio 2: installare [!DNL New Relic] agente sul server

Da utilizzare [!DNL New Relic APM Pro] per raccogliere e trasmettere i dati, l&#39;agente PHP deve essere installato sul server.

1. Quando viene richiesto di scegliere un agente Web, fai clic su **PHP**.

1. Per configurare l&#39;agente PHP sul server, seguire le istruzioni.

   Se hai bisogno di aiuto, consulta [New Relic per PHP][3].

1. Verificare che cron sia in esecuzione sul server.

   Per ulteriori informazioni, consulta [Configurare ed eseguire cron][5] nella documentazione per gli sviluppatori.

## Passaggio 3: configurare lo store

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra, dove **[!UICONTROL General]** è espanso, scegli **[!UICONTROL New Relic Reporting]** ed effettuare le seguenti operazioni:

   ![Configurazione del reporting di New Relic](./assets/new-relic-reporting-general.png){width="600"}

   * Imposta **[!UICONTROL Enable New Relic Integration]** a `Yes`.

   * In **[!UICONTROL Insights API URL]**, sostituisci la percentuale (`%`) con il tuo ID account New Relic.

   * Immetti il **[!UICONTROL New Relic Account ID]**.

   * Immetti il **[!UICONTROL New Relic Application ID]**.

   * Immetti il **[!UICONTROL New Relic API Key]**.

   * Immetti **[!UICONTROL Insights API Key]**.

1. Per **[!UICONTROL New Relic Application Name]**, immetti un nome per identificare la configurazione per un riferimento interno.

1. (Facoltativo) Per **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, seleziona `Yes` per inviare i dati raccolti per la vetrina e per l&#39;amministratore come app separate a New Relic.

   Questa opzione richiede l&#39;immissione di un nome per .**[!UICONTROL New Relic Application Name]**

   >[!NOTE]
   >
   >L’abilitazione di questa funzione riduce il numero di falsi positivi [!DNL New Relic] avvisi e consente di configurare il monitoraggio e gli avvisi in modo rigoroso per le prestazioni front-end. New Relic riceve file di dati dell’app separati con i nomi dell’applicazione aggiunti alla `Adminhtml` e front-end. Ad esempio: `MyStore_Adminhtml`

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Passaggio 4: abilitare Cron per [!DNL New Relic] reportistica

1. Espandi ![Espansione selettore](../assets/icon-display-expand.png) sezione **[!UICONTROL Cron]** .

   ![Configurazione New Relic Cron](./assets/new-relic-reporting-cron.png){width="600"}

1. Imposta **[!UICONTROL Enable Cron]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## [!DNL New Relic] query

[!DNL New Relic Insights] i dati si basano su istruzioni scritte in [!DNL New Relic Query Language] (NRQL) ed eventuali parametri personalizzati che potrebbero essere inclusi. I dati possono essere restituiti da query ad hoc o da query salvate nel dashboard. Per ulteriori informazioni, consulta [Riferimento NRQL][6] nel [!DNL New Relic] documentazione.

### Eventi di amministrazione

#### Utenti amministratori attivi

Restituisce il numero di utenti amministratori attivi.

    SELECT uniqueCount(AdminId)
    Transazione FROM
    WHERE appName=&#39;&lt;your_app_name>&#39; DA 15 minuti fa

#### Utenti Admin attualmente attivi

Restituisce i nomi degli utenti Admin attivi.

    SELECT uniques(AdminName)
    FROM Transazione
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 minuti fa
&lt;/your_app_name>
#### Attività amministratore recente

Restituisce il numero di azioni Amministratore recenti.

    SELECT count(AdminId)
    Transazione FROM
    DOVE appName =&#39;&lt;your_app_name>&#39; FACET AdminName DA 1 giorno fa

#### Ultima attività amministratore

Restituisce informazioni dettagliate sulle azioni recenti dell&#39;amministratore, inclusi il nome utente, la durata e il nome applicazione dell&#39;amministratore.

    SELEZIONA AdminName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; And AdminName NON È NULL
    E AdminName !&lt;/your_app_name>= LIMITE &#39;N/D&#39; 50

### Eventi cron

#### Categoria conteggio

Restituisce il numero di eventi applicazione per categoria durante il periodo di tempo specificato.

    SELECT average(CatalogCategoryCount)
    DA Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND nomeApplicazione = &#39;&lt;your_app_name>&#39; SERIE TEMPORALI 2 minuti

#### Conteggio catalogo corrente

Restituisce il numero medio di eventi applicazione nel catalogo per categoria durante il periodo di tempo specificato.

    SELECT average(CatalogCategoryCount)
    DA Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND ConteggioCategorieCatalogo > 0
    AND nomeApplicazione = &#39;&lt;your_app_name>&#39; DA 2 minuti fa LIMITE 1

#### Prodotti attivi

Restituisce il numero di eventi di applicazione per prodotto durante il periodo di tempo specificato.

    SELECT average(CatalogProductActiveCount)
    DA Cron
    WHERE CatalogProductActiveCount NON È NULL
    AND nomeApplicazione = &#39;&lt;your_app_name>&#39; SERIE TEMPORALI 2 minuti

#### Conteggio prodotti attivi

Restituisce il numero medio di eventi di applicazione attivi per prodotto durante il periodo di tempo specificato.

    SELECT average(CatalogProductActiveCount)
    DA Cron
    WHERE CatalogProductActiveCount NON È NULL
    AND CatalogProductActiveCount > 0
    AND nomeApplicazione = &#39;&lt;your_app_name>&#39; DA 2 minuti fa LIMITE 1

#### Prodotti configurabili

Restituisce il numero medio di eventi dell&#39;applicazione per i prodotti configurabili durante il periodo di tempo specificato.

    SELECT average(CatalogProductConfigurableCount)
    DA Cron
    WHERE CatalogProductConfigurableCount NON È NULL
    AND nomeApplicazione = &#39;&lt;your_app_name>&#39; SERIE TEMPORALI 2 minuti

#### Numero di prodotti configurabili

Restituisce il numero medio di eventi dell&#39;applicazione per prodotto configurabile durante il periodo di tempo specificato.

    SELECT average(CatalogProductConfigurableCount)
    DA Cron
    WHERE CatalogProductConfigurableCount NON È NULL
    AND CatalogProductConfigurableCount > 0
    AND nomeApplicazione = &#39;&lt;your_app_name>&#39; DA 2 minuti fa LIMITE 1

#### Numero di prodotti (tutti)

Restituisce il numero totale di eventi di applicazione per tutti i prodotti.

    SELECT average(CatalogProductCount)
    DA Cron
    WHERE CatalogProductCount NON È NULL
    AND nomeApplicazione = &#39;&lt;your_app_name>&#39; SERIE TEMPORALI 2 minuti

#### Numero di prodotti corrente (tutti)

Restituisce il numero medio di eventi dell&#39;applicazione per tutti i prodotti durante il periodo di tempo specificato.

    SELECT average(CatalogProductCount)
    DA Cron
    WHERE CatalogProductCount NON È NULL
    E CatalogProductCount > 0
    AND nomeApplicazione = &#39;&lt;your_app_name>&#39; DA 2 minuti fa LIMITE 1

#### Conteggio clienti

Restituisce il numero medio di eventi applicazione per cliente.

    SELECT average(CustomerCount)
    DA Cron
    WHERE ConteggioClienti NON È NULLO
    E Conteggio clienti > 0&lt;
    AND nomeApplicazione = &#39;&lt;your_app_name>&#39; SERIE TEMPORALI 2 minuti

#### Conteggio clienti corrente

Restituisce il numero medio di clienti durante il periodo di tempo specificato.

    SELECT average(CustomerCount)
    DA Cron
    WHERE ConteggioClienti NON È NULLO
    E Conteggio clienti > 0
    AND nomeApplicazione = &#39;&lt;your_app_name>&#39; DA 2 minuti fa LIMITE 1

#### Stato del modulo

Restituisce il numero medio di volte in cui i moduli applicativi vengono attivati, disattivati o installati durante il periodo di tempo specificato.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average(ModulesEnabled)
    (ModuliInstallati)
    DA Cron&lt;
    DOVE appName = &#39;&lt;your_app_name>&#39; SERIE TEMPORALI 2 minuti

#### Stato del modulo corrente

Restituisce il numero medio di volte in cui i moduli sono stati attivati, disattivati o installati durante il periodo di tempo specificato.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average(ModulesEnabled)
    (ModuliInstallati)
    DA Cron
    DOVE appName = &#39;&lt;your_app_name>&#39; DA 2 minuti fa LIMITE 1

#### Conteggi di siti web e store

Restituisce il numero medio di eventi dell&#39;applicazione per sito Web e archivio durante il periodo di tempo specificato.

    SELECT average(StoreViewCount), average(WebsiteCount)
    DA Cron
    WHERE nomeApp = &#39;&amp;lt;nome_app&amp;gt;&#39; SERIE TEMPORALI 2 minuti

#### Conteggi correnti per siti Web e store

Restituisce il numero medio di eventi dell&#39;applicazione correnti durante il periodo di tempo specificato.

    SELECT average(StoreViewCount), average(WebsiteCount)
    DA Cron
    DOVE appName = &#39;&lt;your_app_name>&#39; DA 2 minuti fa LIMITE 1

#### Cron: tutti i dati dell’evento

Restituisce tutti i dati evento applicazione.

    SELEZIONA *
    DA Cron
    DOVE appName = &#39;&lt;your_app_name>&#39;

### Clienti

#### Conteggio clienti attivi

Restituisce il numero di clienti attivi durante il periodo di tempo specificato.

    SELECT uniqueCount(CustomerId)
    Transazione FROM
    DOVE appName = &#39;&lt;your_app_name>&#39; DA 15 minuti fa

#### Clienti attivi

Restituisce i nomi dei clienti attivi durante il periodo di tempo specificato.

    SELECT uniques(CustomerName)
    FROM Transazione
    WHERE appName=&#39;&lt;your_app_name>&#39; SINCE 15 minuti fa
&lt;/your_app_name>
#### Clienti principali

Restituisce i clienti principali durante il periodo di tempo specificato.

    SELECT count(CustomerId)
    Transazione FROM
    DOVE appName = &#39;&lt;your_app_name>&#39; FACET NomeCliente DA 1 giorno fa

#### Attività amministratore recente

Restituisce un numero definito di record di attività recenti, inclusi il nome del cliente e la durata del visita.

    SELEZIONA CustomerName, duration, name
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39;
    AND CustomerName NON È NULL
    E CustomerName !&lt;/your_app_name>= LIMITE &#39;N/D&#39; 50

### Ordini

#### Numero di ordini effettuati

Restituisce il numero di ordini effettuati durante il periodo di tempo specificato.

    SELECT count(Order)
    DA transazione DA 1 giorno fa

#### Valore totale dell’ordine

Restituisce il numero totale di righe ordinate durante il periodo di tempo specificato.

    SELECT sum(orderValue)
    DA transazione DA 1 giorno fa

#### Totale elementi riga ordinati

Restituisce il numero totale di righe ordinate durante il periodo di tempo specificato.

    SELECT sum(lineItemCount)
    DA transazione DA 1 giorno fa


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
