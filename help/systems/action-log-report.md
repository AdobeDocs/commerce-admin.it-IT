---
title: Rapporto Registri azioni
description: Scopri come visualizzare, filtrare ed esportare il rapporto Registro azioni, che fornisce un record dettagliato di tutte le azioni amministratore abilitate per il registro.
exl-id: f2be5852-9185-4f14-b0bb-44d779b40819
feature: Logs, Data Import/Export
TQID: https://experienceleague.adobe.com/b6LYoDmgU-uDdTLCjtDKd1TS4f7krj4fs9Qz4ClAJr4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 441
ht-degree: 0%

---

# Rapporto Registri azioni

{{ee-feature}}

Il report _Registri azioni_ visualizza un record dettagliato di tutte le azioni di amministrazione abilitate per la registrazione. Ogni record è contrassegnato con marca temporale e registra l’indirizzo IP e il nome dell’utente. I dettagli del registro includono i dati utente amministratore e le relative modifiche apportate durante l’azione.

Le azioni che si desidera visualizzare nel report devono essere abilitate nella schermata [Registrazione azioni amministratore](action-log.md) nelle impostazioni dell&#39;archivio. Se il tipo di azione è selezionato (abilitato), questi tipi di azioni amministratore vengono visualizzati nel rapporto Registri azioni.

Il rapporto può essere filtrato utilizzando le opzioni in ogni colonna. È possibile impostare un&#39;unica opzione di filtro o impostare opzioni di filtro per più colonne per limitare il report ad elencare azioni specifiche. Puoi anche esportare i dati dei rapporti in formato CSV o XML Excel.

Il rapporto Action Logs (Registri azioni azioni) include le seguenti informazioni:

- **[!UICONTROL Time]** - Data e ora in cui si è verificata l&#39;azione
- **[!UICONTROL Action Group]** - Visualizza il tipo di azione, correlato alle azioni abilitate nella schermata _Registrazione azioni amministratore_ nelle impostazioni dell&#39;archivio
- **[!UICONTROL Action]** - Visualizza l&#39;azione registrata
- **[!UICONTROL IP Address]** - Visualizza l&#39;indirizzo IP del computer in cui è stata eseguita l&#39;azione
- **[!UICONTROL Username]** - Visualizza l&#39;ID di accesso per l&#39;utente che ha eseguito l&#39;azione
- **[!UICONTROL Result]** - Visualizza l&#39;esito positivo o negativo dell&#39;azione dell&#39;utente
- **[!UICONTROL Full Action Name]** - Visualizza il nome dell&#39;azione di backend
- **[!UICONTROL Details]** - Visualizza la categoria di azioni back-end
- **[!UICONTROL Full Details]** - Visualizza tutti i dettagli registrati dell&#39;azione di amministrazione

## Visualizzare il rapporto Action Logs

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Report]**.

   ![Registri azioni](./assets/action-log-report.png){width="600" zoomable="yes"}

1. Per visualizzare tutti i dettagli di un&#39;azione di amministrazione elencata, fare clic su **[!UICONTROL View]**.

   ![Dettagli voce registro azioni](./assets/action-log-report-view.png){width="600" zoomable="yes"}

## Filtrare il rapporto Registri azioni

È possibile definire i campi delle opzioni di filtro e quindi fare clic su **[!UICONTROL Search]** per limitare le azioni visualizzate.

Per cancellare le opzioni di filtro e tornare al report completo, fare clic su **[!UICONTROL Reset Filter]**.

![Filtri report log azioni](./assets/action-log-report-filters.png){width="600" zoomable="yes"}

| Campo | descrizione |
|--- |--- |
| [!UICONTROL Time] | In **[!UICONTROL From]**, fare clic per selezionare una data dal calendario dinamico per definire la data di inizio per il filtro. In **[!UICONTROL To]**, fare clic per selezionare una data per definire la data di fine per il filtro. |
| [!UICONTROL Action Group] | Scegli un gruppo di azioni. |
| [!UICONTROL Action] | Scegli un&#39;azione. |
| [!UICONTROL IP Address] | Immettere l&#39;indirizzo IP del computer utilizzato per un&#39;azione. |
| [!UICONTROL Username] | Scegli un nome utente. Il valore predefinito è `All Users`. |
| [!UICONTROL Result] | Scegliere Operazione completata o Operazione non riuscita. |
| [!UICONTROL Full Action Name] | Immetti il testo da cercare nel campo. |
| [!UICONTROL Details] | Immetti il testo da cercare nel campo. |

{style="table-layout:auto"}

## Esportare il rapporto Action Logs

1. Per **[!UICONTROL Export to]**, scegliere un formato di esportazione:

   - `CSV` - File di valori separati da virgole contenente dati di testo normale
   - `Excel XML` - Formato dati foglio di calcolo basato su XML

1. Fare clic su **[!UICONTROL Export]**.

   Il file generato viene salvato automaticamente nella cartella specificata per i download.

   ![Esportazione report log azioni](./assets/action-log-report-export.png){width="200"}
