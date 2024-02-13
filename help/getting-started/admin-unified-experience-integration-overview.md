---
title: Integrazione di Adobe Experience Cloud per l’amministratore di Commerce
description: Scopri l’estensione Admin Unified Experience che integra Commerce con Experience Cloud in modo che i clienti possano accedere ai progetti Commerce dalla home page di Experience Cloud.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: a07c91bc2f01cd110f3e0ccd6d27fe5d37eb2fc9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Integrazione di Adobe Experience Cloud per Commerce

{{ee-feature}}

Integra i progetti Adobe Commerce con Experience Cloud abilitando l’estensione Admin Unified Experience. Quando l’integrazione è attiva, gli amministratori possono accedere ai progetti Commerce da Adobe Experience Cloud.

![Accedere a Commerce dalla home page di Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Visualizza progetti Commerce disponibili

Gli amministratori possono visualizzare i progetti Commerce a cui dispongono dell’autorizzazione di accesso selezionando **[!UICONTROL Commerce]** dalla home page dell’Experience Cloud.

![Area di lavoro Progetti Commerce su Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Gli amministratori possono aprire l’Amministratore e la vetrina di ciascun progetto dall’ [!DNL Commerce Projects] e visualizzare ulteriori informazioni.

- **Snapshot della pagina Home della vetrina Commerce**- Snapshot della home page della vetrina. Se un progetto ha più siti Web, lo snapshot mostra la home page del sito predefinito.

- **[Nome progetto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**- Identifica l&#39;ambiente del progetto cloud per l&#39;istanza. Il nome predefinito del progetto è [Nome del ramo Git](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) nel progetto cloud. Modificare o aggiornare il nome del progetto in [Impostazioni di configurazione di Unified Experience Store](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[URL vetrina](../stores-purchase/store-urls.md)**- Visualizza l&#39;URL di base del sito Web predefinito.

- **[Tipo di ambiente](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**: le istanze Commerce distribuite in un ambiente di sviluppo o di staging sono identificate con un [!UICONTROL Development] o [!UICONTROL Staging] etichetta. Le istanze prive di etichetta vengono distribuite in un ambiente di produzione.

- **Accesso amministratore Commerce**- Apri l&#39;amministratore facendo clic su **[!UICONTROL Open]**.

- **Accesso a Storefront**- Aprire la vetrina selezionando **[!UICONTROL Open storefront]** dal menu delle opzioni.

- **Accesso rapido a progetti selezionati**- Seleziona **[!UICONTROL Add to Favorites]** dal menu delle opzioni per aggiungere un progetto al [!UICONTROL Favorites] scheda.

## Flusso di autenticazione

Quando l’integrazione Experience Cloud è abilitata, gli amministratori utilizzano il seguente flusso di lavoro per autenticare e accedere ai progetti Commerce.

1. Accedi tramite la pagina di accesso di Experience Cloud.

   ![Pagina di accesso Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Gli amministratori devono effettuare l’accesso a Experience Cloud con il profilo aziendale Adobe per l’organizzazione associata all’istanza Commerce. Consulta [Gestire i profili Adobi](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. Nella home page di Experience Cloud, apri [!UICONTROL Commerce Projects workspace] selezionando **[!UICONTROL Open]**.

1. Accedi all’amministratore per un progetto selezionando **[!UICONTROL Open]**.

1. Nella pagina di accesso di Adobe Commerce, seleziona **[!UICONTROL Sign in with Adobe ID]** per completare l’autenticazione e aprire Admin.

   ![Pagina di accesso di Adobe Commerce](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Consulta [Gestire l’integrazione Experience Cloud](admin-unified-experience-integration-manage.md) per informazioni dettagliate su come viene influenzato il flusso di lavoro di autenticazione quando l’integrazione Experience Cloud è abilitata o disabilitata.

## Requisiti

- Adobe Commerce 2.4.5 o versione successiva
- Adobe Commerce sull’infrastruttura cloud
- Estensioni Adobe Commerce

   - Estensione Unified Experience per l’amministrazione di Commerce (`magento/module-unified-experience`)

     Se il modulo non è disponibile nell’istanza Commerce, può essere installato utilizzando Composer.

   - [Servizio eventi di Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/): necessario per inviare i dati dell’evento da Experience Cloud per gestire l’accesso degli amministratori ai progetti Commerce.

     L’integrazione di Adobe I/O Events con Commerce è abilitata dall’estensione Commerce Event (`magento/commerce-eventing`) disponibile con Adobe Commerce 2.4.4 e versioni successive.

## Abilitare l’integrazione

Abilita l’integrazione seguendo le istruzioni per: [Configurare l’integrazione di Experience Cloud con l’amministratore di Commerce](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Se l’integrazione Experience Cloud è già abilitata nell’istanza Commerce, consulta [Gestire l’integrazione Experience Cloud](admin-unified-experience-integration-manage.md) per informazioni dettagliate sulla modifica o l&#39;aggiornamento della configurazione, sulla gestione dell&#39;accesso amministratore e sulla risoluzione dei problemi.
