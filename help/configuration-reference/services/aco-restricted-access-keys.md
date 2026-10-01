---
title: '[!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys] dell'amministratore di Commerce.
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
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%
---
# [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]

Utilizzare questa impostazione per controllare il periodo di scadenza predefinito applicato da [!DNL Adobe Commerce Optimizer Connector for B2B] alle chiavi ad accesso limitato per le visualizzazioni di catalogo condivise B2B. Per creare, assegnare ed eliminare queste chiavi, vedere [Gestione chiavi di accesso con restrizioni](../../systems/restricted-access-keys.md).

{{config}}

## [!UICONTROL Provisioning]

![Provisioning](./assets/optimizer-restricted-access-key-config.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| --- | --- | --- |
| [!UICONTROL Default key expiry (days)] | Globale | Periodo di validità per le chiavi di accesso con restrizioni di cui è stato appena eseguito il provisioning. [!DNL Adobe Commerce Optimizer] richiede una data di scadenza di almeno un minuto nel futuro per ogni chiave ed esclude le chiavi scadute dalle letture del gateway, pertanto viene sempre applicato un valore di almeno un giorno. Valore predefinito: `36500` |

{style="table-layout:auto"}

>[!NOTE]
>
>La scadenza predefinita è impostata su un periodo di scadenza lungo perché la rotazione automatica dei tasti non è ancora disponibile. Vedi [Selezione chiave e rotazione](../../systems/restricted-access-keys.md#key-selection-and-rotation).

>[!MORELIKETHIS]
>
> - [Visualizzazione catalogo ACO](./aco-catalog-view.md) — Configura i token di accesso della vetrina per le visualizzazioni catalogo
> - [Gestione chiavi di accesso con restrizioni](../../systems/restricted-access-keys.md): creazione, assegnazione ed eliminazione di chiavi di accesso con restrizioni
> - [Monitoraggio dello stato di sincronizzazione della visualizzazione del catalogo](../../systems/catalog-view-sync-status.md) — Monitoraggio delle chiavi in scadenza
