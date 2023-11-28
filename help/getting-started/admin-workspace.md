---
title: Strumenti di amministrazione e area di lavoro
description: Scopri Admin Workspace, che consente di accedere a tutti gli strumenti, i dati e i contenuti utilizzati per eseguire lo store.
exl-id: 61cc53ab-e1c5-4349-b306-a15eb7c5ab57
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '530'
ht-degree: 0%

---

# Strumenti di amministrazione e area di lavoro

L’area di lavoro di amministrazione consente di accedere a tutti gli strumenti, i dati e il contenuto utilizzati per eseguire lo store. La pagina di avvio predefinita può essere impostata nella configurazione. Molte pagine Amministratore dispongono di una griglia che elenca i dati della sezione, con un set di strumenti per cercare, ordinare, filtrare, selezionare e applicare azioni. Per impostazione predefinita, il [Dashboard](admin-dashboard.md) è la pagina di avvio per l’Amministratore. Tuttavia, è possibile scegliere qualsiasi altra pagina da visualizzare come pagina di avvio al momento dell&#39;accesso. Puoi fare clic sul logo nella barra laterale Amministratore per tornare alla pagina di avvio dell’Amministratore.

![Amministratore - area di lavoro](./assets/admin-workspace.png){zoomable=&quot;yes&quot;}

## Controlli di Workspace

| Controllo | Descrizione |
|--- |--- |
| [!UICONTROL Global Search] | L’icona di ricerca in alto a destra può essere utilizzata per trovare qualsiasi valore nel database, inclusi i record di prodotti, clienti e ordini. |
| [!UICONTROL Grid Search] | La casella di ricerca sopra la griglia può essere utilizzata per filtrare rapidamente la visualizzazione della griglia in base alle parole chiave presenti nei record. |
| [!UICONTROL Sort] | L’intestazione di ciascuna colonna può essere utilizzata per ordinare l’elenco in ordine crescente o decrescente. |
| [!UICONTROL Filters] | Definisce un insieme di parametri di ricerca che determina i record visualizzati nella griglia. Inoltre, i filtri nell’intestazione di alcune colonne possono essere utilizzati per limitare l’elenco a valori specifici. Alcuni filtri dispongono di opzioni aggiuntive selezionabili da una casella di riepilogo. |
| [!UICONTROL Default View] | Determina il layout di colonna predefinito della griglia. |
| [!UICONTROL Columns] | Determina la selezione di [colonne](admin-grid-controls.md) e il loro ordine nella griglia. Il layout delle colonne può essere modificato e salvato come _visualizza_. Per impostazione predefinita, nella griglia sono incluse solo alcune colonne. |
| [!UICONTROL Paginate] | I controlli di impaginazione vengono utilizzati per visualizzare le pagine aggiuntive dei risultati. |
| [!UICONTROL Actions] | Il controllo Azioni applica un&#39;operazione a tutti i record selezionati. |
| [!UICONTROL Select] | Il controllo Seleziona viene utilizzato per selezionare più record che devono essere oggetto dell&#39;azione. Opzioni: `Select All` / `Deselect All` |

{style="table-layout:auto"}

## Ricerca in Workspace

Per trovare un record nel database, utilizzare l&#39;icona della lente di ingrandimento nell&#39;intestazione del _Amministratore_. I risultati possono includere clienti, prodotti, ordini o qualsiasi attributo correlato. Ad esempio, se si inserisce il nome di un cliente, i risultati potrebbero includere il record del cliente ed eventuali ordini associati al nome.

![Strumento di ricerca amministrazione](./assets/admin-search.png){width="700" zoomable="yes"}

1. Nell’intestazione, fai clic su _Ricerca_ (![lente di ingrandimento](../assets/icon-magnify-search.png)) per aprire la casella di ricerca.

1. Effettuare una delle seguenti operazioni:

   - Per trovare una corrispondenza di chiusura, immettere le prime lettere di ciò che si desidera trovare.
   - Per trovare una corrispondenza esatta, immettere la parola o più parole che si desidera trovare.

1. Nei risultati di ricerca visualizzati fare clic su un elemento qualsiasi per aprire il record.

## Modificare la pagina di avvio dell&#39;amministratore

Il [dashboard](admin-workspace.md#the-dashboard) è la pagina di avvio predefinita per l’amministratore, anche se è possibile configurare una pagina di avvio diversa.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello di navigazione a sinistra in **[!UICONTROL Advanced]**, scegli **[!UICONTROL Admin]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Startup Page]** sezione.

   ![Configurazione avanzata - Impostazione della pagina di avvio amministratore](./assets/admin-startup-page.png){width="600"}

1. Imposta **[!UICONTROL Startup Page]** alla pagina che desideri visualizzare per prima dopo aver effettuato l’accesso all’amministratore.

   Per un elenco dettagliato di tutte le opzioni di amministrazione, consulta [Amministratore](../configuration-reference/advanced/admin.md) nel _Riferimento configurazione_.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
