---
title: Gestione degli indici
description: Scopri la gestione dell’indice, incluse le azioni che attivano la reindicizzazione e le best practice.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 422fce6c2676f7c760c1a97b67fbd0f45d65e19c
workflow-type: tm+mt
source-wordcount: '1296'
ht-degree: 0%

---

# Gestione degli indici

Adobe Commerce e Magento Open Source si reindicizzano automaticamente ogni volta che uno o più elementi cambiano. Le azioni che attivano la reindicizzazione includono le modifiche dei prezzi, la creazione di regole dei prezzi per il catalogo o il carrello, l’aggiunta di nuove categorie e così via. Per ottimizzare le prestazioni, Commerce accumula i dati in tabelle speciali utilizzando gli indici. Man mano che i dati cambiano, le tabelle indicizzate devono essere aggiornate o reindicizzate. Commerce reindicizza come processo in background e il tuo archivio rimane accessibile durante i processi.

La reindicizzazione dei dati velocizza l’elaborazione e riduce il tempo di attesa del cliente. Se ad esempio si modifica il prezzo di un articolo da 4,99 a 3,99 dollari, Commerce reindicizza i dati per mostrare la modifica del prezzo nel negozio. Senza l&#39;indicizzazione, Commerce dovrebbe calcolare il prezzo di ogni prodotto al volo, gestendo le regole di prezzo del carrello, i prezzi dei bundle, gli sconti, i prezzi dei livelli e così via. Il caricamento del prezzo di un prodotto potrebbe richiedere più tempo di quanto il cliente sia disposto ad aspettare.

Gli indicizzatori possono essere impostati per l&#39;aggiornamento al momento del salvataggio o in base alla pianificazione. Tutti gli indici possono utilizzare entrambe le opzioni, ad eccezione di Customer Grid che supporta solo al salvataggio. Durante l’indicizzazione al momento del salvataggio, Commerce avvia una reindicizzazione delle azioni di salvataggio. La pagina Gestione dell’indice completa l’aggiornamento e svuota la cache, con il messaggio di reindicizzazione visualizzato entro un minuto o due. Quando si reindicizza in base a una pianificazione, la reindicizzazione viene eseguita in base a una pianificazione come processo cron. Se non è disponibile un processo [cron](cron.md) per aggiornare gli indicizzatori che non sono più validi, verrà visualizzato un messaggio di sistema. L’archivio rimane accessibile durante i processi di reindicizzazione.

>[!NOTE]
> I commercianti di Adobe Commerce che utilizzano Live Search, Catalog Service o Product Recommendations possono utilizzare un indicizzatore prezzi basato su [SaaS](https://experienceleague.adobe.com//en/docs/commerce/price-indexer/price-indexing?lang=it).

Quando è necessaria una reindicizzazione, nella parte superiore della pagina viene visualizzata una notifica. L’indice e il messaggio vengono cancellati in base alla modalità di reindicizzazione e alle potenziali azioni eseguite. Per informazioni più dettagliate sull&#39;indicizzazione, vedere [Come l&#39;applicazione implementa l&#39;indicizzazione](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) nella _Guida per gli sviluppatori PHP_.

![Gestione indice - azioni](./assets/index-management.png){width="700" zoomable="yes"}

- La gestione degli indici presenta una presentazione leggermente diversa per i cataloghi di prodotti piatti.
- Per evitare problemi quando più utenti Admin aggiornano oggetti che attivano la reindicizzazione automatica, è consigliabile impostare tutti gli indicizzatori in modo che vengano eseguiti secondo la pianificazione come [processi cron](cron.md). In caso contrario, ogni volta che un oggetto viene salvato, qualsiasi oggetto con interdipendenze potrebbe causare un deadlock. I sintomi di un deadlock includono un elevato utilizzo di CPU ed errori MySQL. Come best practice, si consiglia di utilizzare l’indicizzazione pianificata.
- ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Per impostazione predefinita, le azioni dell&#39;amministratore, ad esempio la reindicizzazione, vengono registrate dal sistema e possono essere visualizzate nel [report dei log delle azioni](action-log-report.md). La registrazione delle azioni può essere configurata in [Registrazione azioni amministratore](action-log.md) nelle impostazioni di amministrazione avanzate dell&#39;archivio.

## Best practice per la reindicizzazione

La reindicizzazione e il caching hanno scopi diversi in Commerce. Gli indici tengono traccia delle informazioni del database per migliorare le prestazioni di ricerca, velocizzare il recupero dei dati per le vetrine e altro ancora. [Le cache](cache-management.md) consentono di salvare i dati caricati, le immagini, i formati e così via per migliorare le prestazioni di caricamento e accesso alla vetrina.

- In genere, si desidera reindicizzare quando si aggiornano i dati in Commerce.
- Se si dispone di uno o più store di grandi dimensioni, può essere utile impostare gli indicizzatori come categoria e prodotti sui processi cron pianificati, in quanto è possibile reindicizzare i cicli. È possibile impostare la reindicizzazione in base a una pianificazione nelle ore non di picco.
- Durante la reindicizzazione, non è necessario eseguire anche una cache di scaricamento.
- Per le nuove installazioni di Commerce, è necessario svuotare la cache e reindicizzare.
- Lo svuotamento delle cache e la reindicizzazione non svuota la cache del browser del computer. Cancella la cache del browser dopo aver completato gli aggiornamenti alla vetrina.

## Modificare la modalità indice

>[!IMPORTANT]
>
>Per gli archivi che utilizzano [Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=it) e hanno impostato Elasticsearch come indicizzatore full-text (`catalogsearch_fulltext`): è necessario eseguire nuovamente l&#39;indice full-text dopo eventuali modifiche delle autorizzazioni in blocco o quando l&#39;indicizzatore &#39;permissions&#39; è in modalità &#39;Pianificato&#39;.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. Selezionare la casella di controllo per ogni indicizzatore che si desidera modificare.

1. Imposta **[!UICONTROL Actions]** su uno dei seguenti:

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >La griglia clienti può essere reindicizzata solo utilizzando `Update on Save`. Questo indice **_non_** supporta `Update by Schedule`.

1. Fare clic su **[!UICONTROL Submit]** per applicare la modifica a ogni indicizzatore selezionato.

   **Colonne gestione indice**

   | Colonna | Descrizione |
   | ------ |---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | [!UICONTROL Indexer] | Nome dell&#39;indicizzatore. |
   | [!UICONTROL Description] | Descrizione dell&#39;indicizzatore. |
   | [!UICONTROL Mode] | Indica la modalità di aggiornamento corrente per ogni indicizzatore. Opzioni: <br/>**[!UICONTROL Update on Save]**- L&#39;indice viene impostato per l&#39;aggiornamento ogni volta che viene salvata una modifica di entità. Tali entità includono prodotti, categorie e clienti. Al termine dell’azione di salvataggio, una serie di passaggi inizia a rilevare le modifiche e aggiornare l’indice. La pagina Gestione indice aggiorna e scarica il messaggio di reindicizzazione entro uno o due minuti.<br/>**[!UICONTROL Update on Schedule]** - L&#39;indice è impostato per l&#39;aggiornamento pianificato in base a un [processo cron](cron.md). Il processo cron include l&#39;intervallo di pianificazione per la reindicizzazione, la scrittura degli aggiornamenti all&#39;indice durante l&#39;esecuzione. |
   | [!UICONTROL Schedule Status] | Visualizza gli aggiornamenti dello stato della pianificazione. |
   | [!UICONTROL Status] | Visualizza uno dei seguenti elementi: <br/>**[!UICONTROL Ready]**— L&#39;indice è aggiornato.<br/>**[!UICONTROL Suspended]** - Reindicizzazione sospesa. <br/>**[!UICONTROL Processing]**- La reindicizzazione è attualmente in esecuzione.<br/>**[!UICONTROL Reindex Required]** - È stata apportata una modifica che richiede la reindicizzazione, ma gli indicizzatori non possono essere aggiornati automaticamente. Verifica se [cron](cron.md) è disponibile e configurato correttamente. |
   | [!UICONTROL Updated] | Indica la data e l’ora dell’ultimo aggiornamento di un indice. |

   {style="table-layout:auto"}

## Reindicizzare utilizzando la riga di comando

Commerce fornisce opzioni di reindicizzazione aggiuntive utilizzando la riga di comando. Per informazioni dettagliate e opzioni di comando, vedere [Reindex](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html?lang=it#reindex){:target="blank"} nella _Guida alla configurazione_.

## Indice eventi trigger

## Reindicizzazione dei trigger

| Tipo di indice | Evento di reindicizzazione |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | Aggiungi gruppo di clienti<br/>Modifica impostazioni di configurazione |
| [!UICONTROL Flat catalog product data] | Aggiungi store<br/>Aggiungi gruppo di store<br/>Aggiungi, modifica o elimina attributo (per ricerca e filtro) |
| [!UICONTROL Flat catalog category data] | Aggiungi store<br/>Aggiungi gruppo di store<br/>Aggiungi, modifica o elimina attributo (per ricerca e filtro) |
| [!UICONTROL Catalog category/product index] | Aggiungere, modificare o eliminare prodotti (singoli, di massa e di importazione)<br/>Modificare le relazioni tra prodotti e categorie<br/>Aggiungere, modificare o eliminare categorie<br/>Aggiungere o eliminare archivi<br/>Eliminare gruppi di archivi<br/>Eliminare siti Web |
| [!UICONTROL Catalog search index] | Aggiungi, modifica o elimina prodotti (singoli, di massa e di importazione)<br/>Aggiungi o elimina archivi<br/>Elimina gruppi di archivi<br/>Elimina siti Web |
| [!UICONTROL Stock status index] | Modificare le impostazioni di configurazione dell&#39;inventario. |
| [!UICONTROL Category permissions index] | Aggiungi store<br/>Aggiungi gruppo di store<br/>Aggiungi, elimina o aggiorna attributo (per ricerca e filtro) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>L’utilizzo di un catalogo semplice non è più consigliato come best practice. L’utilizzo continuo di questa funzione può causare il deterioramento delle prestazioni e altri problemi di indicizzazione. Per ulteriori informazioni, vedere [Utilizza prodotto catalogo flat](../catalog/catalog-flat.md).

## Azioni e controlli indice

| Azione | Risultato | Controlli |
| ------ | ------ | -------- |
| Creazione di uno store, di un nuovo gruppo di clienti o di qualsiasi azione elencata in `Actions that Cause a Full Reindex` | Reindicizzazione completa | La reindicizzazione completa viene eseguita secondo la pianificazione determinata dal processo Adobe Commerce o Magento Open Source cron. |
| Caricamento in blocco di elementi (importazione/esportazione Commerce, query SQL diretta e qualsiasi altro metodo che aggiunge, modifica o elimina direttamente i dati) | Reindicizzazione parziale (solo gli elementi modificati vengono reindicizzati) | Alla frequenza determinata dal processo Commerce cron. |
| Modifica dell’ambito (ad esempio, da globale a sito web) | Reindicizzazione parziale (solo gli elementi modificati vengono reindicizzati) | Alla frequenza determinata dal processo Commerce cron. |

{style="table-layout:auto"}

## Eventi che attivano la reindicizzazione completa

| Indicizzatore | Evento |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | Crea un archivio Web<br/>Crea una visualizzazione dell&#39;archivio Web<br/>Crea o elimina uno degli attributi seguenti:<br/>- Ricercabile o visibile nella ricerca avanzata<br/>- Filterabile<br/>- Filterabile nella ricerca<br/>- Utilizzato per l&#39;ordinamento<br/>Modifica un attributo esistente in modo che sia uno degli attributi precedenti.<br/>Abilita opzioni di vetrina per categoria semplice |
| [!UICONTROL Catalog Product Flat Indexer] | Creare un archivio Web<br>Creare una visualizzazione dell&#39;archivio Web<br/>Creare o eliminare un attributo che sia:<br/>- Ricercabile o visibile nella ricerca avanzata<br>- Filterabile<br>- Filterabile nella ricerca<br/>- Utilizzato per ordinare <br/>Modificare un attributo esistente in modo che sia uno dei precedenti.<br/>Abilita opzioni di vetrina per categoria semplice |
| [!UICONTROL Stock status indexer] | Quando le seguenti _opzioni di inventario del catalogo_ cambiano nella configurazione di sistema:<br/>`Stock Options` - Visualizza prodotti esauriti<br/>`Product Stock Options` - Gestisci scorte |
| [!UICONTROL Price Indexer] | Aggiunta di un gruppo di clienti.<br/>Quando una delle seguenti opzioni di Inventario catalogo cambia nella configurazione di sistema:<br/>`Stock Options` - Visualizza prodotti esauriti<br/>`Product Stock Options` - Gestisci scorte<br/>`Price` - Ambito prezzo catalogo |
| [!UICONTROL Category or Product Indexer] | Creare o eliminare una visualizzazione archivio<br/>Eliminare un archivio<br/>Eliminare un sito Web |

{style="table-layout:auto"}
