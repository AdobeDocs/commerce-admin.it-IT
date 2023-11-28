---
title: Gestire l’integrazione Experience Cloud
description: Scopri come gestire l’integrazione di Experience Cloud e risolvere i problemi
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---

# Gestire l’integrazione Experience Cloud

{{$include /help/_includes/admin-unified-experience-beta-note.md}}

Dopo l’abilitazione iniziale, gestisci lo stato dell’integrazione Experience Cloud abilitando o disabilitando l’estensione Commerce Admin Unified Experience.

- Se l’estensione Commerce Admin Unified Experience è abilitata e gli account amministratore sono [predisposto correttamente](#manage-admin-user-accounts), gli amministratori Commerce possono visualizzare e accedere ai progetti Commerce disponibili da Adobe Experience Cloud. Gli amministratori possono comunque accedere ai singoli progetti utilizzando l’URL amministratore per l’ambiente del progetto Commerce.

- Se l’estensione Commerce Admin Unified Experience è disabilitata, l’accesso tramite Experience Cloud è disabilitato. Gli amministratori devono accedere ai singoli progetti utilizzando l’URL amministratore per l’ambiente del progetto Commerce.

>[!WARNING]
>
>Se l’integrazione Adobe Identity Management Service (IMS) è disabilitata, l’integrazione Experience Cloud viene disabilitata automaticamente.

## Gestire l’integrazione dall’Amministratore

1. Dall’amministratore di Commerce, apri il menu Configurazione archivio selezionando **[!UICONTROL Stores]** dal menu di navigazione sinistro, quindi selezionare **[!UICONTROL Configuration]**.

1. Dal menu Configuration, seleziona **[!UICONTROL Advanced > Admin]**, quindi espandere **[!UICONTROL Unified Experience option]**.

   ![Configurazione dell’archivio di amministrazione per l’integrazione di Experience Cloud](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. Abilita o disabilita l’integrazione selezionando la **[!UICONTROL Enable]** valore.

1. Modifica il nome del progetto visualizzato nell’area di lavoro Progetti Commerce aggiungendo o aggiornando la sezione **[!UICONTROL Project Name]** valore.

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

   - **Abilita**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **Disattiva**—`bin/magento config:set admin/unified_experience/enabled 0`

## Gestire gli account utente amministratore

Per accedere ai prodotti e ai servizi Adobe, tutti gli utenti Commerce Admin devono disporre sia di un account Amministratore nell’istanza Commerce che di un account utente Adobe (Adobe ID). Entrambi gli account devono essere associati allo stesso indirizzo e-mail.

- **Account amministratore Commerce**—[Gestire gli utenti amministratori di Commerce](../systems/permissions-users-all.md) dall’amministratore per l’istanza Commerce. Agli account utente per amministratori Commerce deve essere assegnato il ruolo Amministratore.

  Gli amministratori di sistema nel progetto Commerce possono utilizzare [SSH per la connessione all&#39;ambiente remoto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment), e utilizzare Commerce CLI `admin:user:create` e `admin:user:unlock` comandi per aggiungere o sbloccare account utente amministratore.

- **account utente Adobe**- Un amministratore dell’organizzazione Adobe associata all’istanza Commerce deve accedere a Adobe Admin Console e aggiungere all’organizzazione l’Adobe ID di ogni amministratore Commerce. Quindi, devono assegnare le autorizzazioni e i diritti del prodotto per accedere all’applicazione Commerce. Consulta [Configurare gli utenti di Adobe Commerce in Adobe Admin Console](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console).

Gli amministratori che gestiscono la configurazione per l’integrazione Experience Cloud dalla console Adobe Developer devono disporre di un account utente Adobe con accesso Amministratore di sistema o Sviluppatore.

>[!NOTE]
>
>Un Adobe ID è un account creato tramite Adobe che è necessario per accedere a prodotti e servizi tramite Experience Cloud. Gli amministratori Commerce che non dispongono di un Adobe ID possono [creare un account gratuito](https://helpx.adobe.com/manage-account/using/create-update-adobe-id.html) che utilizzano lo stesso indirizzo e-mail per accedere all’amministratore di Commerce.
