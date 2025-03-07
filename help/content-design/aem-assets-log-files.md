---
title: Configurare la rotazione del registro
description: Configurare la rotazione dei registri per l’integrazione di AEM Assets per Commerce.
feature: CMS, Media, Integration
source-git-commit: 9e1f80d24eed078b5b28ae2d102c3f3df457081d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Configurare Experience Manager Assets

L’integrazione di AEM Assets per Commerce fornisce i seguenti file di registro:

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

Chiedere all&#39;amministratore di sistema di controllare la pianificazione della rotazione dei file di registro per questi registri per evitare che diventino troppo grandi. In alcuni ambienti, i file di registro vengono ruotati automaticamente, ma in altri è necessario impostare manualmente la rotazione del registro. Per ulteriori informazioni, vedere i seguenti argomenti:

- Per le installazioni locali di Adobe Commerce, chiedi all&#39;amministratore di sistema di impostare [la rotazione del registro](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings).
- Per i progetti Adobe Commerce su infrastrutture cloud, consulta [Visualizzare e gestire i registri](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html).


