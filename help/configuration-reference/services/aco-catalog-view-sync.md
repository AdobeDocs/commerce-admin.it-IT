---
title: '[!UICONTROL Services] > Sincronizzazione visualizzazione catalogo ACO'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync] dell'amministratore di Commerce.
feature: Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync]

Utilizzare queste impostazioni per controllare il modo in cui [!DNL Adobe Commerce Optimizer Connector for B2B] sincronizza in [!DNL Adobe Commerce Optimizer] le configurazioni del catalogo condiviso B2B, ovvero la vista del catalogo, i criteri, il listino prezzi e la chiave, e come risolve le differenze di configurazione tra i due sistemi. Per controllare i risultati di queste impostazioni, vedere [Monitoraggio dello stato di sincronizzazione della visualizzazione del catalogo](../../systems/catalog-view-sync-status.md).

{{config}}

## [!UICONTROL Deletion]

![Eliminazione](./assets/aco-catalog-view-sync-configuration.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| --- | --- | --- |
| [!UICONTROL Deletion Grace Period (days)] | Globale | Periodo di conservazione per i dati di catalogo condivisi. Specifica il numero di giorni in cui le visualizzazioni di catalogo condiviso, i criteri e i metadati di un catalogo eliminato vengono conservati prima di essere eliminati definitivamente. Il valore predefinito è 7 giorni. Imposta su `0` per l&#39;eliminazione immediata. |

{style="table-layout:auto"}

## [!UICONTROL Creation]

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| --- | --- | --- |
| [!UICONTROL Creation Grace Period (days)] | Globale | Numero di giorni in cui una visualizzazione catalogo appena registrata può attendere che [!DNL Adobe Commerce Optimizer Connector for B2B] completi la prima sincronizzazione delle configurazioni di visualizzazione catalogo, criterio, listino prezzi e chiave, mentre il relativo stato è [!UICONTROL Pending]. Se il periodo di tolleranza scade senza una sincronizzazione riuscita, lo stato cambia in [!UICONTROL Failed]. Valore predefinito: `1` |

{style="table-layout:auto"}

## [!UICONTROL Drift Reconciler]

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| --- | --- | --- |
| [!UICONTROL Enabled] | Globale | Esegue il riconciliatore della deriva pianificato per rilevare e segnalare le differenze tra la visualizzazione del catalogo proiettata da [!DNL Adobe Commerce] e la configurazione della visualizzazione del catalogo in [!DNL Adobe Commerce Optimizer]. Se `automatically repair drift` è abilitato, tenterà anche di correggere eventuali discrepanze riparabili. |
| [!UICONTROL Automatically Repair Drift] | Globale | Se impostato su `Yes`, il riconciliatore della deriva pianificato aggiorna la configurazione [!DNL Adobe Commerce Optimizer] in modo che corrisponda a [!DNL Adobe Commerce] e risincronizza la configurazione. Se è impostato su `No`, l&#39;esecuzione rileva e segnala solo la deriva. Le entità [!DNL Adobe Commerce Optimizer] orfane vengono sempre segnalate, mai rimosse automaticamente. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [Visualizzazione catalogo ACO](./aco-catalog-view.md) — Configura i token di accesso per le letture in vetrina di una visualizzazione catalogo
> - [Monitoraggio dello stato di sincronizzazione della visualizzazione del catalogo](../../systems/catalog-view-sync-status.md) — Monitora lo stato di sincronizzazione e correggi la deriva utilizzando queste impostazioni
> - [Gestione chiavi di accesso limitate](../../systems/restricted-access-keys.md): gestire le chiavi di accesso assegnate alle visualizzazioni del catalogo sincronizzate
