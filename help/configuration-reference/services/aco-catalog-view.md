---
title: '[!UICONTROL Services] > Visualizzazione catalogo ACO'
description: Rivedi e aggiorna le impostazioni di configurazione di Adobe Commerce Optimizer nella pagina [!UICONTROL Services] > [!UICONTROL ACO Catalog View] dell'amministratore di Commerce.
feature: Configuration, Security
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
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
source-git-commit: b32c28afffe75b3f684f0fef81bd61e9cdcb485a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View]

Utilizzare queste impostazioni per controllare i token di accesso emessi da [!DNL Adobe Commerce Optimizer Connector for B2B]. Gli storefront utilizzano questi token per l’autenticazione nelle viste di catalogo privato di Commerce Optimizer compilate con dati sincronizzati da cataloghi condivisi personalizzati configurati nell’amministratore.

{{config}}

![L&#39;amministratore Adobe Commerce visualizza le impostazioni dei token di accesso per la visualizzazione del catalogo ACO, con un TTL di 3.600 secondi e un rilascio di token abilitato.](./assets/aco-catalog-view-access-token-config.png)<!-- zoom -->

## [!UICONTROL Access Token Configuration]

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| --- | --- | --- |
| [!UICONTROL Token TTL (seconds)] | Globale | Numero di secondi in cui un token di accesso rimane valido dopo la generazione. Questa impostazione è di sola lettura nell&#39;ambito predefinito. I valori configurati nel sito Web o nell&#39;ambito della visualizzazione archivio vengono ignorati. Impostazione predefinita: 3600 secondi. |
| [!UICONTROL Issue Access Tokens] | Visualizzazione store | Controlla se la vetrina può ottenere un token di accesso per una vista catalogo. Se è impostato su `No`, `Company.catalogViewContext` restituisce l&#39;ID della vista catalogo ma non un token di accesso, pertanto gli storefront non possono eseguire l&#39;autenticazione per la lettura da [!DNL Adobe Commerce Optimizer] viste di catalogo private sincronizzate da Adobe Commerce. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [Sincronizzazione visualizzazione catalogo ACO](./aco-catalog-view-sync.md) — Configura la modalità di sincronizzazione delle visualizzazioni catalogo in [!DNL Adobe Commerce Optimizer]
> - [Monitoraggio dello stato di sincronizzazione della visualizzazione del catalogo](../../systems/catalog-view-sync-status.md) — Monitora l&#39;integrità della sincronizzazione e riconcilia la deriva
