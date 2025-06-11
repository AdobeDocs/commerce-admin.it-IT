---
title: Integrazione di Adobe Stock
description: Integra Adobe Stock con la tua istanza  [!DNL Commerce]  per accedere a innumerevoli risorse multimediali da utilizzare nello store.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Integrazione di Adobe Stock

Per accedere a innumerevoli risorse multimediali da utilizzare nel tuo archivio, integra [Adobe Stock][adobe-stock] con [!UICONTROL Commerce].

![Risultati ricerca Adobe Stock](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Il servizio Adobe Stock offre alle aziende l’accesso a milioni di foto, vettori, illustrazioni, video, modelli e risorse 3D di alta qualità e curate, senza royalty, per tutti i loro progetti creativi. [!DNL Commerce] utenti sono in grado di trovare rapidamente, visualizzare in anteprima e concedere in licenza le risorse Adobe Stock. Gli utenti possono anche salvarli nello spazio di archiviazione [multimediale](./media-storage.md), il tutto senza uscire dall&#39;area di lavoro di amministrazione.

## Prerequisiti

Questa integrazione richiede:

- Un account [Adobe Developer][dev-console]
- Adobe Commerce o Magento Open Source, versione 2.3.4 o successiva

La concessione di licenze per le immagini Adobe Stock richiede:

- Un account [Adobe][adobe-signin]
- Un piano a pagamento [Adobe Stock][adobe-stock] associato all&#39;account

## Integrare [!DNL Commerce] e Adobe Stock

La configurazione dell’integrazione di Adobe Stock per Adobe Commerce prevede due fasi:

1. [Crea un&#39;integrazione adobe.developer](#create-an-adobe-developer-integration) per generare una chiave API
1. [Configurare l’integrazione di Adobe Stock nell’amministrazione di Commerce](#configure-the-adobe-stock-integration)

### Creare un’integrazione Adobe Developer

1. Passa a [Adobe Developer Console][dev-console].

1. In _[!UICONTROL Quick Start]_, fare clic su **[!UICONTROL Create new project]**.

1. Nel blocco _[!UICONTROL Project overview]_, fare clic su **[!UICONTROL Add API]**.

1. Selezionare **[!UICONTROL Adobe Stock]** dall&#39;elenco delle integrazioni e fare clic su **[!UICONTROL Next]**.

1. Selezionare OAuth 2.0 **[!UICONTROL Web App]**.

1. Specificare **[!UICONTROL redirect URI]**.

   L&#39;URI di reindirizzamento predefinito è nel formato `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, ad esempio `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, dove:

   - `${HOST}` è il tuo nome di dominio completo [!DNL Commerce] (ad esempio, `https://store.myshop.com`).
   - `${ADMIN_URI}` è l&#39;URI amministratore [!DNL Commerce] (ad esempio `admin_hgkq1l`), che può essere recuperato eseguendo `magento info:adminuri`.

1. Specifica **[!UICONTROL Redirect URI pattern]**, che è lo stesso dell&#39;URI di reindirizzamento con due differenze:

   - Qualsiasi punto (`.`) deve avere un escape con due barre rovesciate (`\\`).
   - Aggiungi `.*` alla fine del modello.

   Se si utilizza l&#39;esempio dell&#39;URI di reindirizzamento predefinito precedente, sarà `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Fare clic su **[!UICONTROL Next]**.

1. Esaminare gli ambiti disponibili e fare clic su **[!UICONTROL Save configured API]**.

1. Nella pagina seguente, copia **[!UICONTROL Client ID]** (chiave API) e **[!UICONTROL Client secret]**.

   Queste informazioni vengono utilizzate nei passaggi della sezione successiva.

### Configurare l’integrazione di Adobe Stock

Per impostare la configurazione di sistema nell&#39;amministratore [!DNL Commerce], utilizzare la _chiave API_ e il _segreto client_ generati nella [sezione precedente][create-integration].

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Enabled Adobe Stock]** su `Yes`.

   - Immetti **[!UICONTROL API Key (Client ID)]**.

   - Immetti **[!UICONTROL Client Secret]**.

   - Fai clic su **[!UICONTROL Test Connection]** per convalidare le chiavi.

   ![Configurazione avanzata - Integrazione Adobe Stock](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Assegna alla convalida alcuni secondi. Se le credenziali sono valide, verrà visualizzata una _Connessione riuscita._ messaggio.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/it/manage-account/using/access-adobe-id-account.html
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
