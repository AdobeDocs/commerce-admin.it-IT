---
title: Integrazione di Adobe Stock
description: Integra Adobe Stock con il tuo [!DNL Commerce] per accedere a innumerevoli risorse multimediali da utilizzare nel tuo store.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 6666073a48741cb494f408a61401f46fc20cedc4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Integrazione di Adobe Stock

Per accedere a innumerevoli risorse multimediali da utilizzare nel tuo negozio, integra [Adobe Stock][adobe-stock] con [!UICONTROL Commerce].

![Risultati di ricerca Adobe Stock](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Il servizio Adobe Stock offre alle aziende l’accesso a milioni di foto, vettori, illustrazioni, video, modelli e risorse 3D di alta qualità e curate, senza royalty, per tutti i loro progetti creativi. [!DNL Commerce] Gli utenti possono trovare, visualizzare in anteprima e concedere in licenza le risorse Adobe Stock in modo rapido. Gli utenti possono anche salvarli in [archiviazione dei supporti][media-storage], il tutto senza uscire dall’area di lavoro di amministrazione.

## Prerequisiti

Questa integrazione richiede:

- Un [Adobe Developer][dev-console] account
- Adobe Commerce o Magento Open Source, versione 2.3.4 o successiva

La concessione di licenze per le immagini Adobe Stock richiede:

- Un [account Adobe][adobe-signin]
- A a pagamento [Adobe Stock][adobe-stock] piano associato all’account

## Integrare [!DNL Commerce] e ADOBE STOCK

La configurazione dell’integrazione di Adobe Stock per Adobe Commerce prevede due fasi:

1. [Creare un’integrazione adobe.developer](#create-an-adobe-developer-integration) per generare una chiave API
1. [Configurare l’integrazione di Adobe Stock nell’amministrazione di Commerce](#configure-the-adobe-stock-integration)

### Creare un’integrazione Adobe Developer

1. Accedi a [Console Adobe Developer][dev-console].

1. Sotto _[!UICONTROL Quick Start]_, fai clic su **[!UICONTROL Create new project]**.

1. In _[!UICONTROL Project overview]_blocco, fai clic su **[!UICONTROL Add API]**.

1. Seleziona **[!UICONTROL Adobe Stock]** dall’elenco delle integrazioni e fai clic su **[!UICONTROL Next]**.

1. Seleziona OAuth 2.0 **[!UICONTROL Web App]**.

1. Specifica la **[!UICONTROL redirect URI]**.

   L&#39;URI di reindirizzamento predefinito è nel modulo `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, ad esempio `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, dove:

   - `${HOST}` è il tuo [!DNL Commerce] nome di dominio completo (ad esempio, `https://store.myshop.com`).
   - `${ADMIN_URI}` è il tuo [!DNL Commerce] URI amministratore (ad esempio `admin_hgkq1l`), recuperabile eseguendo il comando `magento info:adminuri`.

1. Specifica la **[!UICONTROL Redirect URI pattern]**, che è lo stesso dell’URI di reindirizzamento con due differenze:

   - Qualsiasi periodo (`.`) con due barre rovesciate (`\\`).
   - Aggiungi `.*` alla fine del pattern.

   Utilizzando l’esempio dell’URI di reindirizzamento predefinito precedente, `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Clic **[!UICONTROL Next]**.

1. Rivedi gli ambiti disponibili e fai clic su **[!UICONTROL Save configured API]**.

1. Nella pagina successiva, copia il **[!UICONTROL Client ID]** (chiave API) e **[!UICONTROL Client secret]**.

   Queste informazioni vengono utilizzate nei passaggi della sezione successiva.

### Configurare l’integrazione di Adobe Stock

Per impostare la configurazione di sistema in [!DNL Commerce] Amministratore, utilizza _Chiave API_ e _Segreto client_ generato in [sezione precedente][create-integration].

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Enabled Adobe Stock]** a `Yes`.

   - Immetti il **[!UICONTROL API Key (Client ID)]**.

   - Immetti il **[!UICONTROL Client Secret]**.

   - Clic **[!UICONTROL Test Connection]** per convalidare le chiavi.

   ![Configurazione avanzata - Integrazione con Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Assegna alla convalida alcuni secondi. Se le credenziali sono valide, verrà visualizzato un segno verde _Connessione riuscita_ messaggio.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
