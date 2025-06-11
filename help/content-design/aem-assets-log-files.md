---
title: Configurare la rotazione del registro
description: Configurare la rotazione dei registri per l’integrazione di AEM Assets per Commerce.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Configurare Experience Manager Assets

L’integrazione di AEM Assets per Commerce fornisce i seguenti file di registro nell’istanza di Commerce:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Chiedere all&#39;amministratore di sistema di controllare la pianificazione della rotazione dei file di registro per questi registri per evitare che diventino troppo grandi. In alcuni ambienti, i file di registro vengono ruotati automaticamente, ma in altri è necessario impostare manualmente la rotazione del registro. Per ulteriori informazioni, vedere i seguenti argomenti:

- Per le installazioni locali di Adobe Commerce, chiedi all&#39;amministratore di sistema di impostare [la rotazione del registro](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html?lang=it#server-settings).
- Per i progetti Adobe Commerce su infrastrutture cloud, consulta [Visualizzare e gestire i registri](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html?lang=it).
