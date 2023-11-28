---
title: Panoramica sull’integrazione di Adobe Identity Management Service (IMS)
description: Introduce l’integrazione opzionale dell’accesso amministratore di Adobe Commerce con Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Panoramica sull’integrazione di Adobe Identity Management Service (IMS)

{{ee-feature}}

Gli utenti amministratore di Adobe Commerce che dispongono di un account Adobe ora possono utilizzare il proprio Adobe ID per accedere ad Adobe Commerce. Adobe Identity Management Service (IMS) è la funzione di gestione delle identità basata su OAuth 2.0 di Adobe che supporta l’autenticazione. L’integrazione dell’autenticazione dell’amministratore Commerce nel flusso di lavoro di autenticazione IMS del prodotto Adobe Business può semplificare il processo di autenticazione per gli utenti che lavorano con altri prodotti Adobe. Questa integrazione è facoltativa ed è abilitata per singole istanze. Quando questa integrazione è abilitata, vengono interessati solo i flussi di lavoro degli utenti Admin. 

I moduli necessari per l’integrazione Commerce Admin IMS sono inclusi in  `adobe-ims-metapackage`, in bundle con le versioni di base di Adobe Commerce.

Per implementare questa integrazione, consulta [Configurare l’integrazione dell’amministratore di Commerce con IMS](./adobe-ims-config.md).

## Modifiche ai flussi di lavoro e all’interfaccia di amministrazione dopo l’integrazione con IMS

Quando questa integrazione è abilitata, gli utenti Commerce Admin visualizzano le modifiche al flusso di lavoro di accesso e autenticazione predefinito dell’amministratore Commerce quando eseguono attività di routine in Admin che richiedono la riautenticazione, ad esempio la creazione di un utente Admin. Per l’abilitazione del modulo è necessaria l’autenticazione a due fattori (2FA) a livello di organizzazione Adobe. L’accesso predefinito per amministratori e 2FA sono disabilitati e il _[!UICONTROL Sign In with Adobe ID]_sostituisce il modulo di accesso Amministratore predefinito. I diritti sono ancora gestiti dall’amministratore.

## Effetti dell’integrazione dell’amministratore con IMS sulle password di Commerce

Le implementazioni Commerce integrate con Adobe IMS richiedono un account Adobe ID con accesso all’organizzazione Adobe IMS configurata per l’applicazione Commerce durante il processo di abilitazione IMS.  Quando l’integrazione IMS è abilitata, gli utenti amministratori si autenticano tramite la pagina di accesso di Adobe utilizzando le loro credenziali di Adobe. Le password Commerce e i nomi utente per gli utenti amministratori non vengono più utilizzati per l’autenticazione purché sia abilitata l’integrazione Adobe IMS.

Se l’integrazione IMS è disabilitata, gli utenti amministratori devono eseguire di nuovo l’autenticazione tramite Adobe Commerce utilizzando il nome utente e la password Commerce. Gli utenti amministratore devono salvare le credenziali amministratore di Commerce (nome utente e password) e le credenziali 2FA prima di abilitare questa integrazione.

Alcuni componenti back-end coinvolti nell’autenticazione dell’utente richiedono ancora una password non null. Per soddisfare questo requisito, Commerce crea password casuali per i nuovi utenti amministratori creati in `admin_user` tabella.

Gli account utente e le autorizzazioni per il ruolo dell’applicazione Commerce vengono ancora gestiti dall’amministratore di Commerce.


## Generazione di token API web con credenziali IMS

Le API dell’amministratore di Commerce sono interessate quando l’autenticazione dell’amministratore con Adobe IMS è abilitata in un’istanza di Commerce. Gli utenti amministratori non possono più utilizzare le credenziali rilasciate dall’istanza Commerce. Si tratta delle credenziali necessarie per accedere all’amministratore e ottenere i token di accesso che i servizi possono utilizzare per effettuare richieste alle API REST e SOAP dell’amministratore.

Dopo l’abilitazione dell’integrazione Adobe IMS, gli utenti amministratori devono utilizzare [Token OAuth di Adobe IMS](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/) per gli endpoint API di Adobe Commerce che richiedono l’autenticazione. Le soluzioni client ottengono i token in modo dinamico per l’utilizzo dell’API web. Questo meccanismo di autenticazione è abilitato per le aree REST e API web SOAP durante la configurazione di questa integrazione.

Consulta [Autenticazione basata su token](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) per una panoramica dell’utilizzo dei token di accesso Commerce da parte delle API web, inclusi i token di accesso IMS.

## Gestione delle sessioni Commerce e token di accesso Adobe IMS

I token di accesso contengono sia le credenziali utente che le informazioni sulla sessione di accesso. Una volta che un utente è stato autenticato ed è stata avviata una sessione, le due variabili seguenti vengono aggiunte alla sessione dell’utente:

`token_last_check_time`. Identifica l’ora corrente e viene utilizzato da `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` plugin.

`adobe_access_token` — Identifica il `ACCESS_TOKEN` valore ricevuto durante l&#39;autorizzazione.

Il `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` il plug-in controlla se `token_last_check_time` è stato aggiornato 10 minuti fa. Se il `token_last_check_time` è stato controllato dieci minuti fa, poi il flusso di lavoro di autenticazione effettua una chiamata API a IMS per convalidare il token di accesso e la sessione continua. Se il token di accesso è valido, allora il `token_last_check_time` viene aggiornato all’ora corrente. Se il token non è valido, la sessione viene terminata.

## File importanti

`adminAdobeIms` : fornisce un’implementazione dell’accesso come amministratore in base al `AdobeImsApi` modulo.

`admin_adobe_ims_webapi` - Mantiene un record di tutti i token di accesso convalidati. Quando un token viene convalidato o invalidato, in questa tabella viene mantenuto un record del relativo stato.

`adobeIms` : implementa tutte le regole business correlate all’integrazione con Adobe IMS (conservate per evitare incompatibilità con le versioni precedenti).

`adobeImsApi` : dichiara le interfacce che supportano l’integrazione con Adobe IMS.

`adminadobe-ims.log` - File di log degli errori.

## Abilitare l’integrazione

Il metapacchetto Adobe IMS è installato con Adobe Commerce 2.4.5 e versioni successive, ma deve essere configurato per l’utilizzo. Estende il `AdobeIms` per supportare il modulo che abilita la logica di autenticazione (`AdminAdobeIms`).

Per ulteriori informazioni sull’abilitazione dell’integrazione, consulta [Configurare l’integrazione dell’amministratore di Commerce con Adobe IMS](./adobe-ims-config.md).
