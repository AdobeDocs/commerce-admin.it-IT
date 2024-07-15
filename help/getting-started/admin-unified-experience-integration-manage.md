---
title: Gestire l’integrazione Experience Cloud
description: Scopri come gestire l’integrazione di Experience Cloud e risolvere i problemi
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: 15569794c1e66ba5a93e46206244e2951522923e
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Gestire l’integrazione Experience Cloud

Dopo l’abilitazione iniziale, gestisci lo stato dell’integrazione Experience Cloud abilitando o disabilitando l’estensione Commerce Admin Unified Experience.

- Se l&#39;estensione Commerce Admin Unified Experience è abilitata e gli account dell&#39;amministratore dispongono del provisioning [corretto](#manage-admin-user-accounts), gli amministratori di Commerce possono visualizzare e accedere ai progetti Commerce disponibili da Adobe Experience Cloud. Gli amministratori possono comunque accedere ai singoli progetti utilizzando l’URL amministratore per l’ambiente del progetto Commerce.

- Se l’estensione Commerce Admin Unified Experience è disabilitata, l’accesso tramite Experience Cloud è disabilitato. Gli amministratori devono accedere ai singoli progetti utilizzando l’URL amministratore per l’ambiente del progetto Commerce.

>[!WARNING]
>
>Se l’integrazione Adobe Identity Management Service (IMS) è disabilitata, l’integrazione Experience Cloud viene disabilitata automaticamente.

## Gestire l’integrazione dall’Amministratore

1. Dall&#39;amministratore di Commerce, aprire il menu Configurazione archivio selezionando **[!UICONTROL Stores]** dal menu di navigazione sinistro, quindi selezionare **[!UICONTROL Configuration]**.

1. Dal menu Configuration, selezionare **[!UICONTROL Advanced > Admin]**, quindi espandere **[!UICONTROL Unified Experience option]**.

   ![Configurazione dell&#39;archivio di amministrazione per l&#39;integrazione Experience Cloud](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Abilitare o disabilitare l&#39;integrazione selezionando il valore **[!UICONTROL Enable]**.

1. Modificare il nome del progetto visualizzato nell&#39;area di lavoro Progetti Commerce aggiungendo o aggiornando il valore **[!UICONTROL Project Name]**.

1. Salva la configurazione.

1. Cancella la cache.

## Gestire l’integrazione tramite Adobe Commerce CLI

Gli amministratori di sistema di Commerce con accesso amministratore al progetto cloud Commerce possono utilizzare i comandi CLI di Adobe Commerce per gestire l’integrazione Experience Cloud.

1. Dall’ambiente di sviluppo locale, accedi al progetto cloud.

   ```bash
   magento-cloud login
   ```

1. Dalla directory principale dell’ambiente di progetto Cloud, connettiti al server applicazioni Commerce.

   ```bash
   ssh magento-cloud
   ```

1. Controlla lo stato dell’estensione Admin Unified Experience:

   ```bash
   bin/magento admin:uex:status
   ```

1. Modifica lo stato dell’estensione per disabilitare l’integrazione

   - **Attiva**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Disabilita**—`bin/magento config:set admin/unified_experience/enabled 0`

## Gestire gli account utente amministratore

Per accedere ai prodotti e ai servizi Commerce, tutti gli utenti amministratore di Commerce devono disporre sia di un account amministratore nell’istanza Adobe che di un account utente Adobe (Adobe ID). Entrambi gli account devono essere associati allo stesso indirizzo e-mail.

- **Account amministratore Commerce**—[Gestisci utenti amministratore Commerce](../systems/permissions-users-all.md) dall&#39;amministratore per l&#39;istanza Commerce. Agli account utente per amministratori di Commerce deve essere assegnato il ruolo Amministratore.

  Gli amministratori di sistema nel progetto Commerce possono utilizzare [SSH per connettersi all&#39;ambiente remoto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment) e utilizzare i comandi Commerce CLI `admin:user:create` e `admin:user:unlock` per aggiungere o sbloccare gli account utente Admin.

- **Account utente Adobe** - Un amministratore per l&#39;organizzazione Adobe associata all&#39;istanza Commerce deve accedere a Adobe Admin Console e aggiungere l&#39;Adobe ID per ogni amministratore Commerce all&#39;organizzazione. Quindi, devono assegnare le autorizzazioni e i diritti del prodotto per accedere all’applicazione Commerce. Vedi [Configurare gli utenti Adobe Commerce in Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Gli amministratori che gestiscono la configurazione dell’integrazione Experience Cloud da Adobe Developer Console devono disporre di un account utente Adobe con accesso Amministratore di sistema o Sviluppatore.

>[!NOTE]
>
>Un Adobe ID è un account creato tramite Adobe che è necessario per accedere a prodotti e servizi tramite Experience Cloud. Gli amministratori di Commerce che non dispongono di un Adobe ID possono [creare un account gratuito](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) utilizzando lo stesso indirizzo e-mail utilizzato per accedere all&#39;amministratore di Commerce.
