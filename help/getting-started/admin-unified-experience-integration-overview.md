---
title: Integrazione di Adobe Experience Cloud per l’amministratore di Commerce
description: Scopri l’estensione Admin Unified Experience, che integra Commerce con Experience Cloud in modo che i clienti possano accedere ai progetti Commerce dalla pagina Home di Experience Cloud.
feature: Integration
exl-id: e3fb6337-c7d5-4b6f-8f4a-583697a1f2d2
source-git-commit: 61874f3dac4f574ad393e8ae258f3d6c56c8f37e
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Integrazione di Adobe Experience Cloud per Commerce

<table style="border:1px solid red">
<tr><td><img alt="Funzione di Adobe Commerce" src="../assets/adobe-logo.svg" width="20" height="20" /> Funzionalità esclusiva solo in Adobe Commerce (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">Ulteriori informazioni</a>)</td></tr>
</table>

Integra i progetti Adobe Commerce con Experience Cloud abilitando l’estensione Admin Unified Experience. Quando l’integrazione è attiva, gli amministratori possono accedere ai progetti Commerce da Adobe Experience Cloud.

![Accedi a Commerce dalla home page di Experience Cloud](./assets/admin-uex-home-page.png){width="700" zoomable="yes"}

## Visualizza progetti Commerce disponibili

Gli amministratori possono visualizzare i progetti Commerce per i quali dispongono dell&#39;autorizzazione di accesso selezionando **[!UICONTROL Commerce]** dalla home page dell&#39;Experience Cloud.

![Area di lavoro Progetti Commerce in Experience Cloud](./assets/admin-uex-commerce-projects-home.png){width="700" zoomable="yes"}

Gli amministratori possono aprire Admin e Storefront per ciascun progetto dall&#39;area di lavoro [!DNL Commerce Projects] e visualizzare ulteriori informazioni.

- **Istantanea della home page della vetrina di Commerce**: istantanea della home page della vetrina. Se un progetto ha più siti Web, lo snapshot mostra la home page del sito predefinito.

- **[Nome progetto](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**—Identifica l&#39;ambiente del progetto cloud per l&#39;istanza. Il nome predefinito del progetto è [Nome ramo Git](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/console-branches.html) nel progetto cloud. Modifica o aggiorna il nome del progetto nelle [impostazioni di configurazione di Unified Experience Store](admin-unified-experience-integration-manage.md#manage-the-integration-from-the-admin).

- **[URL vetrina](../stores-purchase/store-urls.md)** - Mostra l&#39;URL di base del sito Web predefinito.

- **[Tipo di ambiente](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-develop-deploy-workflow.html)**: le istanze di Commerce distribuite in un ambiente di sviluppo o di gestione temporanea sono identificate con un&#39;etichetta [!UICONTROL Development] o [!UICONTROL Staging]. Le istanze prive di etichetta vengono distribuite in un ambiente di produzione.

- **Accesso amministratore Commerce**. Aprire l&#39;amministratore facendo clic su **[!UICONTROL Open]**.

- **Accesso storefront**—Aprire la vetrina selezionando **[!UICONTROL Open storefront]** dal menu delle opzioni.

- **Accesso rapido a progetti selezionati**—Seleziona **[!UICONTROL Add to Favorites]** dal menu delle opzioni per aggiungere un progetto alla scheda [!UICONTROL Favorites].

## Flusso di autenticazione

Quando l’integrazione Experience Cloud è abilitata, gli amministratori utilizzano il seguente flusso di lavoro per autenticare e accedere ai progetti Commerce.

1. Accedi tramite la pagina di accesso di Experience Cloud.

   ![Pagina di accesso Experience Cloud](./assets/admin-uex-experience-cloud-login.png){width="600" zoomable="yes"}

   Gli amministratori devono effettuare l’accesso a Experience Cloud con il profilo aziendale Adobe per l’organizzazione associata all’istanza Commerce. Consulta [Gestire i profili di Adobe](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html).

1. Nella home page di Experience Cloud, aprire [!UICONTROL Commerce Projects workspace] selezionando **[!UICONTROL Open]**.

1. Accedere all&#39;amministratore per un progetto selezionando **[!UICONTROL Open]**.

1. Nella pagina di accesso di Adobe Commerce, seleziona **[!UICONTROL Sign in with Adobe ID]** per completare l&#39;autenticazione e aprire l&#39;amministratore.

   ![Pagina di accesso di Adobe Commerce](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Consulta [Gestire l&#39;integrazione Experience Cloud](admin-unified-experience-integration-manage.md) per informazioni dettagliate su come viene influenzato il flusso di lavoro di autenticazione quando l&#39;integrazione Experience Cloud è abilitata o disabilitata.

## Requisiti

- Adobe Commerce 2.4.5 o versione successiva
- Adobe Commerce sull’infrastruttura cloud
- Estensioni Adobe Commerce

   - Estensione Unified Experience per l&#39;amministrazione di Commerce (`magento/module-unified-experience`)

     Se il modulo non è disponibile nell’istanza di Commerce, può essere installato utilizzando Composer.

   - [Servizio eventi di Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/) - Necessario per inviare i dati dell&#39;evento da Experience Cloud per gestire l&#39;accesso amministratore ai progetti Commerce.

     L&#39;integrazione Adobe I/O Events con Commerce è abilitata dall&#39;estensione Commerce Event (`magento/commerce-eventing`) disponibile con Adobe Commerce 2.4.4 e versioni successive.

## Abilitare l’integrazione

Abilita l&#39;integrazione seguendo le istruzioni per [configurare l&#39;integrazione Experience Cloud con l&#39;amministratore Commerce](admin-unified-experience-integration-configure.md).

>[!TIP]
>
>Se l&#39;integrazione Experience Cloud è già abilitata nell&#39;istanza Commerce, vedere [Gestire l&#39;integrazione Experience Cloud](admin-unified-experience-integration-manage.md) per informazioni dettagliate sulla modifica o l&#39;aggiornamento della configurazione, sulla gestione dell&#39;accesso amministratore e sulla risoluzione dei problemi.
