---
title: Configurare l’integrazione amministratore di Commerce con ID
description: Segui questa procedura opzionale per integrare gli accessi dell’account utente amministratore Adobe Commerce con Adobe ID.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 446fe9a5c7cc7178f5bbac0045bdea7e93a73699
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Configurare l’integrazione dell’amministratore di Commerce con Adobe ID

{{ee-feature}}

Questa integrazione supporta i rivenditori Commerce con utenti amministratori che dispongono di un Adobe ID e desiderano accedere in modo più semplice ai prodotti Adobe Commerce e Adobe Business. È facoltativo ed è abilitato per singole istanze. Solo i flussi di lavoro degli utenti amministratori sono interessati quando sono abilitati. 

>[!IMPORTANT]
>
>Gli utenti amministratori devono salvare le credenziali amministratore di Commerce (nome utente e password) e le credenziali 2FA prima di abilitare questa integrazione. Queste credenziali sono necessarie se l’integrazione IMS è disabilitata.

## Prerequisiti

* Adobe Commerce 2.4.5 o versione successiva
* Un account Adobe.com con accesso a [Adobe Admin Console](https://adminconsole.adobe.com/).

Durante l’abilitazione del modulo, l’amministratore che configura questa integrazione deve disporre delle seguenti credenziali:

* ID organizzazione (ottenuto da [Adobe Admin Console](https://adminconsole.adobe.com/)), che deve contenere almeno 24 caratteri. L’utente autenticato deve appartenere a questa organizzazione IMS. Per informazioni su come trovare l&#39;ID organizzazione, vedere [Organizzazioni nell&#39;Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA deve essere applicato a livello di organizzazione in Adobe Admin Console per abilitare il modulo. Controlla [Impostazioni autenticazione](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* ID client
* Segreto client
* ID client e segreto client sono disponibili dopo il recupero delle chiavi API da [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Per accedere, gli utenti amministratore di Commerce devono creare un account con un Adobe ID.

## Passaggi generali

* Ottieni ID organizzazione Adobe da [Adobe Admin Console](https://adminconsole.adobe.com/)
* Genera un nuovo progetto, chiavi API IMS e segreto da [Adobe Developer Console](https://developer.adobe.com/)
* Configurare gli utenti di Adobe Commerce in Adobe Admin Console
* Abilita il modulo `AdminAdobeIms`.

Per il successo dell’integrazione è necessario che tutti gli utenti di Adobe Commerce dispongano di account utente amministratore con lo stesso nome e indirizzo e-mail principale. Se non esiste un account utente Amministratore corrispondente, un utente con le autorizzazioni necessarie (in genere assegnato al ruolo Amministratore) deve [creare manualmente l&#39;account utente Amministratore](../systems/permissions-users-all.md#create-a-user) con lo stesso nome e indirizzo di posta elettronica.

## Configurare l’integrazione

Dopo che un amministratore o uno sviluppatore con accesso al sistema ha completato i passaggi seguenti, il pulsante _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_viene visualizzato nella pagina di accesso dell&#39;amministratore di Commerce per tutti gli utenti amministratori.

### Passaggio 1: ottieni ID organizzazione Adobe

Per abilitare questa funzione è necessaria l’appartenenza ad almeno un’organizzazione IMS. Se disponi di un’Adobe ID, per impostazione predefinita appartieni ad almeno un’organizzazione Adobe. Accedi a [Adobe Admin Console](https://adminconsole.adobe.com/) per recuperare l&#39;ID organizzazione.

### Passaggio 2: generare un nuovo progetto, le chiavi API IMS e il segreto

Per creare progetti per un’organizzazione, l’account amministratore di Adobe per l’organizzazione deve avere il ruolo di amministratore di sistema o sviluppatore. Consulta la [Guida di Developer Console](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. Accedi a [Adobe Developer Console](https://developer.adobe.com/).
1. Passare alla scheda **[!UICONTROL Projects]** (adobe.io/projects) e fare clic su **[!UICONTROL Create a new project]**.
1. Fare clic su **[!UICONTROL Add API]** nella pagina Progetto appena creata.
1. Selezionare **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. Selezionare **[!UICONTROL Oauth 2.0 Web]**.
1. Specificare **[!UICONTROL Redirect URI]**: `https://<hostname>/admin/adobe_ims_auth/oauth/imscallback/`
1. Specificare **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/admin/adobe_ims_auth/oauth/imscallback/`

   Esci da qualsiasi punto nel nome host precedendo i punti con `\\`. L’aggiunta di un carattere jolly alla fine dell’URL supporta la chiave segreta di amministrazione di Adobe Commerce.

1. Fare clic su **[!UICONTROL Save configured API]**.
1. Copia le chiavi [!UICONTROL Client ID] e [!UICONTROL Client Secret] dal progetto creato.

### Passaggio 3: configurare gli utenti di Adobe Commerce in Adobe Admin Console

Prima di abilitare l’integrazione, verifica che ogni account utente di Adobe Commerce Admin disponga di un account Adobe IMS corrispondente. Gli utenti di Adobe Commerce devono appartenere a una specifica organizzazione Adobe per accedere utilizzando un Adobe ID.

>[!TIP]
>
>Puoi creare più account utente caricando le informazioni utente da un file CSV. Vedi [Gestione di più utenti](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. In [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/using/admin-console.html), passa a **[!UICONTROL Users]** > **[!UICONTROL Users]**.

1. Fare clic su **[!UICONTROL Add User]**.

1. Inserisci l’indirizzo e-mail dell’utente.

   Se applicabile, il tipo di ID consigliato viene popolato automaticamente. Puoi modificare questa impostazione in uno degli ID prodotto nell’elenco, che si basa sul piano di acquisto della tua organizzazione.

   Puoi aggiungere fino a dieci utenti alla volta. Per aggiungerne altri, ripeti i passaggi precedenti dopo aver salvato le modifiche.

1. Fare clic su **[!UICONTROL Save]**.

L&#39;utente viene aggiunto e visualizzato nell&#39;elenco [!UICONTROL Users].

### Passaggio 4: abilitare il modulo AdminAdobeIms

Il modulo `AdminAdobeIms` è responsabile dell&#39;integrazione Adobe Commerce/Adobe IMS. Dopo aver configurato il nuovo progetto e copiato l&#39;ID organizzazione, l&#39;ID client e il segreto client, è possibile abilitare il modulo `AdminAdobeIms`.

Immettere `bin/magento admin:adobe-ims:enable`. Viene chiesto di immettere i seguenti parametri. Utilizza i valori generati durante la creazione del progetto.

* ID organizzazione
* ID client
* Segreto client
* 2FA abilitato

Adobe Commerce visualizza un messaggio che indica se l’abilitazione è riuscita o meno.

Dopo aver abilitato correttamente questa funzione, puoi effettuare la transizione da altri account utente di Adobe Commerce ad account Adobe IMS. Per accedere tramite Adobe Commerce, gli utenti devono appartenere all’organizzazione Adobe Adobe ID configurata.
