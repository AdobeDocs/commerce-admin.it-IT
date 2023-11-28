---
title: Strumenti di supporto
description: Scopri gli strumenti di supporto forniti che puoi utilizzare per identificare i problemi nel sistema.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
source-git-commit: 97eeb733836f0336401664c5cfb3df2b9f2f2ccf
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Strumenti di supporto

{{ee-feature}}

Gli strumenti di supporto sono progettati per identificare i problemi noti nel sistema. Possono essere utilizzati come risorsa durante i processi di sviluppo e ottimizzazione e come strumento diagnostico per aiutare il nostro team di supporto a identificare e risolvere i problemi.

## Agente di raccolta dati

L’agente di raccolta dati raccoglie le informazioni sul sistema necessarie al nostro team di supporto per risolvere i problemi relativi all’installazione di Adobe Commerce. Il backup creato richiede diversi minuti e include sia un&#39;immagine del codice che un&#39;immagine del database. I dati possono essere esportati in un file CSV o Excel XML.

![Sistema - Agente di raccolta dati](./assets/data-collector.png){width="600" zoomable="yes"}

### Eseguire l&#39;agente di raccolta dati

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL New Backup]**.

   La generazione del backup richiede alcuni minuti. Puoi monitorare i risultati dell’elaborazione facendo clic su **[!UICONTROL Refresh Status]**. Una volta completato, il backup viene visualizzato nel _[!UICONTROL Data Collector]_griglia.

1. Per visualizzare un registro con i dettagli del backup, effettuare le seguenti operazioni:

   - In _[!UICONTROL Action]_colonna, seleziona **[!UICONTROL Show Log]**.

   - Clic **[!UICONTROL Back]** per tornare alla griglia.

   ![registro agenti di raccolta dati](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Esportare i dati di backup

1. Nella prima colonna selezionare la casella di controllo del backup da esportare.

1. Utilizza il **[!UICONTROL Export]** per scegliere il formato dei dati di esportazione.

   ![Formato di esportazione](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Accedere al file dal percorso di download del browser Web e **[!UICONTROL Save]** ...

### Scarica dati di backup

Una volta generato il backup, puoi scaricare la copia di Code e DB data.

1. Individuare l&#39;entità di backup necessaria nella griglia.

1. Assicurati che abbia `Complete` stato.

1. Fai clic sul nome dell’entità in _[!UICONTROL Code Dump]_o_[!UICONTROL DB Dump]_ colonne.

Il processo di download deve iniziare automaticamente.

## Elimina dati di backup

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Individuare e selezionare i dati di backup da eliminare.

1. In _[!UICONTROL Action]_, fare clic su **[!UICONTROL Delete]**.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.

## Rapporti di sistema

Lo strumento di reporting di sistema consente di acquisire istantanee periodiche complete o parziali del sistema e di salvarle per riferimento futuro. Puoi confrontare le impostazioni delle prestazioni prima e dopo i cicli di sviluppo del codice o le modifiche alle impostazioni del server. Lo strumento di reporting di sistema può ridurre notevolmente il tempo impiegato per preparare e inviare le informazioni richieste dal Supporto per avviare un&#39;indagine.

Dalla griglia Rapporti di sistema è possibile visualizzare e scaricare i rapporti esistenti, eliminarli e crearli.

### Accedere ai report di sistema

Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Amministratore - Rapporti di sistema](./assets/reports.png){width="600" zoomable="yes"}

### Generare un rapporto

1. Clic **[!UICONTROL New Report]**.

1. In **[!UICONTROL Groups]** selezionare ogni insieme di informazioni che si desidera includere nel report. Per impostazione predefinita, sono selezionati tutti i gruppi.

   ![Rapporto di sistema - seleziona gruppi](./assets/report-create.png){width="600" zoomable="yes"}

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Create]**.

   La generazione del rapporto potrebbe richiedere alcuni minuti, a seconda del numero di tipi di rapporto selezionati. Quando il report è pronto, viene visualizzato nella parte superiore della griglia con la data e l’ora generate.

### Visualizza informazioni modulo

Sono disponibili informazioni utili sui moduli installati.

**_Per visualizzare le informazioni di report per ciascun modulo installato:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Clic **[!UICONTROL New Report]**.
1. Seleziona `Modules` dal **[!UICONTROL Groups]** elenco.
1. Clic **[!UICONTROL Create]**.
1. Dopo la generazione del rapporto, fai clic su **[!UICONTROL Select]** e poi **[!UICONTROL View]** per visualizzare tutte le versioni dei moduli.
1. Clic **[!UICONTROL Download]** per scaricare il rapporto.

### Gestire i report di sistema

In **[!UICONTROL Action]** nella griglia, selezionare una delle seguenti opzioni:

- `View` : utilizza questa funzione per visualizzare i dettagli del rapporto.
- `Delete` : utilizza questa funzione per eliminare il rapporto generato dall’elenco.
- `Download` : utilizza questa funzione per salvare il rapporto come file HTML.

### Visualizza dettagli report di sistema

1. Per il rapporto necessario, seleziona **[!UICONTROL View]** nel _[!UICONTROL Actions]_colonna.

1. Nel pannello a sinistra, espandi ![Selettore di espansione](../assets/icon-display-expand.png) ogni sezione del rapporto per visualizzare i dettagli.

   ![Informazioni generali sui report di sistema](./assets/report-information.png){width="600" zoomable="yes"}

### Report di sistema disponibili

| Gruppo di rapporti | Informazioni incluse |
| ------------ | -------------------- |
| [!UICONTROL General] | Versione Adobe Commerce<br>Conteggio dei dati<br>Stato cache<br>Stato indice |
| [!UICONTROL Environment] | Informazioni sull&#39;ambiente<br>Stato MySQL |
| [!UICONTROL Data] | Duplica categorie per chiave URL<br>Duplica prodotti per chiave URL<br>Duplica prodotti per SKU<br>Duplica Ordini Per Id Incremento<br>Duplica utenti per e-mail<br>Dati Categorie Danneggiate |
| [!UICONTROL Modules] | Elenco moduli personalizzati<br>Elenco moduli disattivati<br>Elenco tutti i moduli |
| [!UICONTROL Configuration] | Configurazione<br>Dati da `app/etc/env.php`<br>Metodi di spedizione<br>Metodi di pagamento<br>Matrice funzionalità pagamenti |
| [!UICONTROL Logs] | File di registro<br>Messaggi di sistema principali<br>Messaggi di sistema principali di oggi<br>Messaggi di debug principali<br>Messaggi di debug principali di oggi<br>Primi messaggi eccezione<br>Messaggi eccezione principali di oggi |
| [!UICONTROL Attributes] | Attributi EAV definiti dall&#39;utente<br>Nuovi attributi EAV<br>Tipi di entità<br>Tutti gli attributi EAV<br>Attributi EAV della categoria<br>Attributi EAV del prodotto<br>Attributi EAV del cliente<br>Attributo EAV indirizzo cliente<br>Attributi EAV articolo RMA |
| [!UICONTROL Events] | Eventi globali personalizzati<br>Eventi di amministrazione personalizzati<br>Eventi front-end personalizzati<br>Eventi documento personalizzati<br>Eventi Crontab Personalizzati<br>Eventi REST personalizzati<br>Eventi SOAP personalizzati<br>Eventi globali principali<br>Eventi di amministrazione core<br>Eventi front-end di base<br>Eventi documento core<br>Eventi Crontab Core<br>Eventi REST core<br>Eventi SOAP di base<br>Tutti gli eventi globali<br>Tutti gli eventi di amministrazione<br>Tutti gli eventi front-end<br>Tutti gli eventi documento<br>Tutti gli eventi REST<br>Tutti gli eventi SOAP<br>Tutti gli eventi Crontab |
| [!UICONTROL Cron] | Pianificazioni Cron per codice di stato<br>Pianificazioni Cron per codice processo<br>Errori nella coda degli Schedules Cron<br>Elenco Schedules Cron<br>Processi Cron Globali Personalizzati<br>Processi di replica configurabili personalizzati<br>Processi core Global Cron<br>Processi core configurabili Cron<br>Tutti i processi Cron globali<br>Tutti i processi di replica configurabili |
| [!UICONTROL Design] | Elenco Temi Amministratore<br>Elenco temi front-end |
| [!UICONTROL Stores] | Albero sito Web<br>Elenco siti Web<br>Elenco Negozi<br>Elenco visualizzazioni store |
| Connettore OMS <br>_(visibile con l&#39;integrazione OMS)_ | Versione connettore<br>Monitoraggio del connettore<br>Risultati elaborazione messaggi |

{style="table-layout:auto"}
