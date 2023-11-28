---
title: Integrazioni
description: Scopri come configurare le credenziali OAuth e l’URL di reindirizzamento per le integrazioni di terze parti.
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Integrazioni

La definizione di un’integrazione nell’amministratore di Commerce stabilisce la posizione delle credenziali OAuth e l’URL di reindirizzamento per le integrazioni di terze parti e identifica le risorse API disponibili necessarie per l’integrazione. Per informazioni più dettagliate sul processo di registrazione dell’integrazione, consulta [Autenticazione basata su OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) nella documentazione per gli sviluppatori di Commerce.

![Integrazioni](./assets/integrations.png){width="700" zoomable="yes"}

## Flusso di lavoro di onboarding

1. **Autorizzare l’integrazione** - Passa a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**, trovare l’integrazione pertinente e autorizzare.
1. **Verificare e stabilire l’accesso** - Quando richiesto, accettare l&#39;accesso richiesto. Se viene reindirizzato a una terza parte, accedi al sistema o crea un account. Dopo aver effettuato correttamente l’accesso, torni alla pagina di integrazione.
1. **Ricevi conferma dell’integrazione autorizzata** - Il sistema invia una notifica per informare che l’integrazione è stata autorizzata correttamente. Dopo aver configurato un’integrazione e ricevuto le credenziali, non è più necessario effettuare chiamate per accedere o richiedere token.

## Aggiungere un’integrazione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![Nuova integrazione](./assets/integration-new.png){width="600" zoomable="yes"}

1. Immetti le seguenti informazioni sull’integrazione:

   - Inserisci il **[!UICONTROL Name]** dell&#39;integrazione e del contatto **[!UICONTROL Email]** indirizzo.

   - Inserisci il **[!UICONTROL Callback URL]** dove è possibile inviare le credenziali OAuth quando si utilizza OAuth per lo scambio di token. Utilizzo di `https://` è vivamente consigliato.

   - Inserisci il **[!UICONTROL Identity Link URL]** per reindirizzare gli utenti a un account di terze parti con queste credenziali di integrazione di Adobe Commerce o di Magento Open Source.

   >[!NOTE]
   >
   > Il `Integration not secure` l’etichetta di avvertenza viene visualizzata accanto a ogni nome di integrazione sulla [!UICONTROL Integrations] grid come promemoria, fino a quando gli URL HTTPS non vengono salvati in [!UICONTROL Callback URL] e [!UICONTROL Identity Link URL] campi.

   - Quando richiesto, immettere la password per confermare l&#39;identità.

1. Nel pannello a sinistra, scegli **[!UICONTROL API]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Resource Access]** a uno dei seguenti elementi:

      - `All`
      - `Custom`

   - Per l’accesso personalizzato, seleziona la casella di controllo di ogni risorsa necessaria.

     ![Integrazioni - API disponibili](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save]**.

## Attivare un’integrazione

Per impostazione predefinita, nella griglia viene visualizzata un&#39;integrazione salvata con un `Inactive` stato. La procedura seguente illustra come attivarla:

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Trova la nuova integrazione creata e fai clic su **[!UICONTROL Activate]** collegamento.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Allow]**.

   Questa azione visualizza i token di integrazione per le estensioni. Copiare queste informazioni in una posizione crittografata sicura da utilizzare con l&#39;integrazione.

   ![Token di integrazione per le estensioni](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Done]**.

## Autorizzare nuovamente un’integrazione

Per generare un nuovo token di accesso all’integrazione e un nuovo segreto per token di accesso, l’integrazione è stata nuovamente autorizzata dall’amministratore:

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Trova l’integrazione con **[!UICONTROL Active]** stato.

1. In entrata _[!UICONTROL Activate]_, fare clic sul pulsante **[!UICONTROL Reauthorize]**.

1. Clic **[!UICONTROL Reauthorize]** per approvare l’accesso alle risorse API.

1. Salva i nuovi token di integrazione per le estensioni e fai clic su **[!UICONTROL Done]**.

## Modificare l’impostazione di sicurezza dell’accesso guest API

Per impostazione predefinita, il sistema non consente l’accesso come ospite anonimo a CMS, catalogo e altre risorse dello store. Se è necessario modificare l&#39;impostazione, effettuare le seguenti operazioni:

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Services]** e scegli **[!UICONTROL Magento Web API]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Web API Security Setting]** sezione.

   ![Configurazione servizi - Impostazioni di sicurezza API web](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Allow Anonymous Guest Access]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

Per ulteriori informazioni, consulta [Limitazione dell’accesso alle API web anonime](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) nella documentazione per gli sviluppatori di Commerce.

## Eliminare un’integrazione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. Trova l’integrazione esistente e fai clic sull’icona ( ![icona cestino](../assets/icon-delete-trashcan-solid.png) ) in **[!UICONTROL Delete]** colonna.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.
