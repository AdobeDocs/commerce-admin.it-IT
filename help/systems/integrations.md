---
title: Integrazioni
description: Scopri come configurare le credenziali OAuth e l’URL di reindirizzamento per le integrazioni di terze parti.
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Integrazioni

La definizione di un’integrazione nell’amministratore di Commerce stabilisce la posizione delle credenziali OAuth e l’URL di reindirizzamento per le integrazioni di terze parti e identifica le risorse API disponibili necessarie per l’integrazione. Per informazioni più dettagliate sul processo di registrazione dell&#39;integrazione, vedi [Autenticazione basata su OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) nella documentazione per gli sviluppatori di Commerce.

![Integrazioni](./assets/integrations.png){width="700" zoomable="yes"}

## Flusso di lavoro di onboarding

1. **Autorizza l&#39;integrazione**. Passare alla pagina **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**, trovare l&#39;integrazione pertinente e autorizzare.
1. **Verifica e stabilisci l&#39;accesso**. Quando richiesto, accetta l&#39;accesso richiesto. Se viene reindirizzato a una terza parte, accedi al sistema o crea un account. Dopo aver effettuato correttamente l’accesso, torni alla pagina di integrazione.
1. **Ricevi conferma dell&#39;integrazione autorizzata**. Il sistema invia una notifica per informare che l&#39;integrazione è stata autorizzata correttamente. Dopo aver configurato un’integrazione e ricevuto le credenziali, non è più necessario effettuare chiamate per accedere o richiedere token.

## Aggiungere un’integrazione

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![Nuova integrazione](./assets/integration-new.png){width="600" zoomable="yes"}

1. Immetti le seguenti informazioni sull’integrazione:

   - Immettere **[!UICONTROL Name]** dell&#39;integrazione e l&#39;indirizzo **[!UICONTROL Email]** del contatto.

   - Immetti **[!UICONTROL Callback URL]** in cui è possibile inviare le credenziali OAuth quando si utilizza OAuth per lo scambio di token. Si consiglia vivamente di utilizzare `https://`.

   - Immetti **[!UICONTROL Identity Link URL]** per reindirizzare gli utenti a un account di terze parti con queste credenziali di integrazione di Adobe Commerce o di Magento Open Source.

   >[!NOTE]
   >
   > L&#39;etichetta di avviso `Integration not secure` viene visualizzata accanto a ogni nome di integrazione nella griglia [!UICONTROL Integrations] come promemoria, finché gli URL HTTPS non vengono salvati nei campi [!UICONTROL Callback URL] e [!UICONTROL Identity Link URL].

   - Quando richiesto, immettere la password per confermare l&#39;identità.

1. Nel pannello a sinistra, scegli **[!UICONTROL API]** ed effettua le seguenti operazioni:

   - Imposta **[!UICONTROL Resource Access]** su uno dei seguenti:

      - `All`
      - `Custom`

   - Per l’accesso personalizzato, seleziona la casella di controllo di ogni risorsa necessaria.

     ![Integrazioni - API disponibile](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Attivare un’integrazione

Per impostazione predefinita, nella griglia viene visualizzata un&#39;integrazione salvata con lo stato `Inactive`. La procedura seguente illustra come attivarla:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Trova la nuova integrazione creata e fai clic sul collegamento **[!UICONTROL Activate]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Allow]**.

   Questa azione visualizza i token di integrazione per le estensioni. Copiare queste informazioni in una posizione crittografata sicura da utilizzare con l&#39;integrazione.

   ![Token di integrazione per le estensioni](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Done]**.

## Autorizzare nuovamente un’integrazione

Per generare un nuovo token di accesso all’integrazione e un nuovo segreto per token di accesso, l’integrazione è stata nuovamente autorizzata dall’amministratore:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Trovare l&#39;integrazione con lo stato **[!UICONTROL Active]**.

1. Nella colonna _[!UICONTROL Activate]_&#x200B;fare clic su **[!UICONTROL Reauthorize]**.

1. Fare clic su **[!UICONTROL Reauthorize]** per approvare l&#39;accesso alle risorse API.

1. Salvare i nuovi token di integrazione per le estensioni e fare clic su **[!UICONTROL Done]**.

## Modificare l’impostazione di sicurezza dell’accesso guest API

Per impostazione predefinita, il sistema non consente l’accesso come ospite anonimo a CMS, catalogo e altre risorse dello store. Se è necessario modificare l&#39;impostazione, effettuare le seguenti operazioni:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Services]** e scegli **[!UICONTROL Magento Web API]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Web API Security Setting]**.

   ![Configurazione servizi - Impostazioni di sicurezza API Web](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Allow Anonymous Guest Access]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

Per ulteriori informazioni, vedere [Limitazione dell&#39;accesso alle API Web anonime](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) nella documentazione per gli sviluppatori di Commerce.

## Eliminare un’integrazione

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Trova l&#39;integrazione esistente e fai clic sull&#39;icona ( ![icona cestino](../assets/icon-delete-trashcan-solid.png) ) nella colonna **[!UICONTROL Delete]**.

1. Per confermare l&#39;azione, fare clic su **[!UICONTROL OK]**.
