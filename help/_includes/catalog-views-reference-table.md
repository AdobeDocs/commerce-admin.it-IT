---
title: Tabella di riferimento delle viste catalogo
description: Tabella di riferimento riutilizzata per la griglia delle visualizzazioni del catalogo
source-git-commit: bc4baccc4b40fb7ecdc7f489bfaf3c797881db88
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%
---
# Tabella di riferimento delle viste catalogo

La griglia elenca una riga per ogni visualizzazione catalogo creata quando un catalogo condiviso viene sincronizzato con [!DNL Adobe Commerce Optimizer]. La griglia è di sola lettura a parte l&#39;azione di assegnazione della chiave. Le viste catalogo vengono create e rimosse automaticamente quando il connettore sincronizza i cataloghi condivisi configurati in Adobe Commerce. Se un catalogo viene rimosso, è necessario un [periodo di tolleranza](/help/systems/catalog-view-sync-status.md#configure-the-deletion-grace-period) prima che la visualizzazione del catalogo e i dati corrispondenti vengano eliminati.

Per assegnare o annullare l&#39;assegnazione delle chiavi con restrizioni di accesso, vedere [Assegnare le chiavi a una visualizzazione catalogo](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view).

| Campo | Descrizione |
| --- | --- |
| [!UICONTROL ACO Catalog View ID] | Identificatore della visualizzazione catalogo corrispondente in [!DNL Adobe Commerce Optimizer]. Consulta [Riepilogo stato sincronizzazione visualizzazione catalogo](/help/systems/catalog-view-sync-status.md#catalog-view-sync-status-summary) per verificarne lo stato di sincronizzazione. |
| [!UICONTROL Store View] | La visualizzazione store rappresentata dalla visualizzazione catalogo. Vedi [Visualizzazioni store](/help/stores-purchase/store-views.md). |
| [!UICONTROL Access Keys] | Titoli dei tasti di accesso limitato attualmente assegnati alla vista catalogo. Consulta [Gestione chiavi di accesso con restrizioni](/help/systems/restricted-access-keys.md). |
| [!UICONTROL Actions] | Selezionare **[!UICONTROL Edit Restricted Access Keys]** per assegnare o annullare l&#39;assegnazione delle chiavi per la visualizzazione del catalogo. Vedi [Assegnare le chiavi a una visualizzazione catalogo](/help/systems/restricted-access-keys.md#assign-keys-to-a-catalog-view). |

{style="table-layout:auto"}
