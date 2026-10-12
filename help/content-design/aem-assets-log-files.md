---
title: Configurare la rotazione del registro
description: Configurare la rotazione dei registri per l’integrazione di AEM Assets per Commerce.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: 'https://experienceleague.adobe.com/I6iWurcyEbPi3fJmBZAnvbPlZfOJiSS4yGR6j5xFsp4'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: ddbd0f6e-b569-5a04-8a70-55058777c373
    internal-label: CMS
  - id: 4ca54350-01cb-5b22-8966-5f2873dc6d90
    internal-label: Media
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%
---
# Configurare Experience Manager Assets

L’integrazione di AEM Assets per Commerce fornisce i seguenti file di registro nell’istanza di Commerce:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Chiedere all&#39;amministratore di sistema di controllare la pianificazione della rotazione dei file di registro per questi registri per evitare che diventino troppo grandi. In alcuni ambienti, i file di registro vengono ruotati automaticamente, ma in altri è necessario impostare manualmente la rotazione del registro. Per ulteriori informazioni, vedere i seguenti argomenti:

- Per le installazioni locali di Adobe Commerce, chiedi all&#39;amministratore di sistema di impostare [la rotazione del registro](https://experienceleague.adobe.com/it/docs/commerce-operations/installation-guide/next-steps/configuration#server-settings).
- Per i progetti Adobe Commerce su infrastrutture cloud, consulta [Visualizzare e gestire i registri](https://experienceleague.adobe.com/it/docs/commerce-on-cloud/user-guide/develop/test/log-locations).

