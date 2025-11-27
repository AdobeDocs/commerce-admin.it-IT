---
title: Panoramica sull’integrazione del servizio Adobe Identity Management (IMS)
description: Introduce l’integrazione opzionale dell’accesso amministratore di Adobe Commerce con Adobe IMS
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '784'
ht-degree: 0%

---

# Panoramica sull’integrazione del servizio Adobe Identity Management (IMS)

{{ee-feature}}

Gli utenti amministratore di Adobe Commerce che dispongono di un account Adobe ora possono utilizzare il proprio Adobe ID per accedere ad Adobe Commerce. Adobe Identity Management Service (IMS) è la funzione di gestione delle identità basata su OAuth 2.0 di Adobe che supporta l’autenticazione. L’integrazione dell’autenticazione amministratore di Commerce nel flusso di lavoro di autenticazione IMS del prodotto Adobe Business può semplificare il processo di autenticazione per gli utenti che lavorano con altri prodotti Adobe. Questa integrazione è facoltativa ed è abilitata per singole istanze. Quando questa integrazione è abilitata, vengono interessati solo i flussi di lavoro degli utenti Admin. 

I moduli necessari per l&#39;integrazione Commerce Admin IMS sono inclusi nel pacchetto in `adobe-ims-metapackage`, fornito con le versioni di base di Adobe Commerce.

Per implementare questa integrazione, vedere [Configurare l&#39;integrazione dell&#39;amministratore di Commerce con IMS](./adobe-ims-config.md).

## Modifiche ai flussi di lavoro e all’interfaccia di amministrazione dopo l’integrazione con IMS

Quando questa integrazione è abilitata, gli utenti amministratore di Commerce visualizzano le modifiche al flusso di lavoro di autenticazione e accesso predefinito di Amministratore Commerce durante l’esecuzione di attività di routine in Amministratore che richiedono la riautenticazione, ad esempio la creazione di un utente amministratore. Per l’abilitazione del modulo è necessaria l’autenticazione a due fattori (2FA) a livello di organizzazione Adobe. L&#39;accesso predefinito per l&#39;amministratore e 2FA sono disabilitati e il pulsante _[!UICONTROL Sign In with Adobe ID]_&#x200B;sostituisce il modulo di accesso predefinito per l&#39;amministratore. I diritti sono ancora gestiti dall’amministratore.

## Effetti dell’integrazione dell’amministratore con IMS sulle password di Commerce

Le implementazioni Commerce integrate con Adobe IMS richiedono un account Adobe ID con accesso all’organizzazione Adobe IMS configurata per l’applicazione Commerce durante il processo di abilitazione IMS.  Quando l’integrazione IMS è abilitata, gli utenti amministratori si autenticano tramite la pagina di accesso di Adobe utilizzando le loro credenziali Adobe. Le password e i nomi utente di Commerce per gli utenti amministratori non vengono più utilizzati per l’autenticazione purché sia abilitata l’integrazione Adobe IMS.

Se l’integrazione IMS è disabilitata, gli utenti amministratori devono eseguire di nuovo l’autenticazione tramite Adobe Commerce utilizzando il nome utente e la password Commerce. Gli utenti amministratori devono salvare le credenziali amministratore di Commerce (nome utente e password) e le credenziali 2FA prima di abilitare questa integrazione.

Alcuni componenti back-end coinvolti nell’autenticazione dell’utente richiedono ancora una password non null. Per soddisfare questo requisito, Commerce crea password casuali per gli utenti amministratori appena creati nella tabella `admin_user`.

Gli account utente e le autorizzazioni dei ruoli per l’applicazione Commerce vengono ancora gestiti dall’amministratore Commerce.


## Generazione di token API web con credenziali IMS

Le API dell’amministratore di Commerce sono interessate quando l’autenticazione dell’amministratore con Adobe IMS è abilitata in un’istanza di Commerce. Gli utenti amministratori non possono più utilizzare le credenziali rilasciate dall’istanza di Commerce. Si tratta delle credenziali necessarie per accedere all’amministratore e ottenere i token di accesso che i servizi possono utilizzare per effettuare richieste alle API REST e SOAP dell’amministratore.

Dopo l&#39;abilitazione dell&#39;integrazione Adobe IMS, gli utenti amministratori devono utilizzare [token Adobe IMS OAuth](https://developer.adobe.com/developer-console/docs/guides/authentication/) per gli endpoint API di Adobe Commerce che richiedono l&#39;autenticazione. Le soluzioni client ottengono i token in modo dinamico per l’utilizzo dell’API web. Questo meccanismo di autenticazione è abilitato per le aree REST e API web SOAP come parte della configurazione di questa integrazione.

Consulta [Autenticazione basata su token](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/) per una panoramica dell&#39;utilizzo dei token di accesso Commerce da parte delle API Web, inclusi i token di accesso IMS.

## Gestione delle sessioni Commerce e token di accesso Adobe IMS

I token di accesso contengono sia le credenziali utente che le informazioni sulla sessione di accesso. Una volta che un utente è stato autenticato ed è stata avviata una sessione, le due variabili seguenti vengono aggiunte alla sessione dell’utente:

`token_last_check_time`. Identifica l&#39;ora corrente ed è utilizzato dal plug-in `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin`.

`adobe_access_token` — Identifica il valore `ACCESS_TOKEN` ricevuto durante l&#39;autorizzazione.

Il plug-in `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` controlla se `token_last_check_time` è stato aggiornato 10 minuti fa. Se `token_last_check_time` è stato controllato dieci minuti fa, il flusso di lavoro di autenticazione effettua una chiamata API a IMS per convalidare il token di accesso e la sessione continua. Se il token di accesso è valido, il valore `token_last_check_time` viene aggiornato all&#39;ora corrente. Se il token non è valido, la sessione viene terminata.

## File importanti

`adminAdobeIms` - Fornisce un&#39;implementazione dell&#39;accesso amministratore basato sul modulo `AdobeImsApi`.

`admin_adobe_ims_webapi` - Mantiene un record di tutti i token di accesso convalidati. Quando un token viene convalidato o invalidato, in questa tabella viene mantenuto un record del relativo stato.

`adobeIms` - Implementa tutte le regole business correlate all&#39;integrazione con Adobe IMS (conservate per evitare incompatibilità con le versioni precedenti).

`adobeImsApi` - Dichiara le interfacce che supportano l&#39;integrazione con Adobe IMS.

`adminadobe-ims.log` - File di log degli errori.

## Abilitare l’integrazione

Il metapacchetto Adobe IMS è installato con Adobe Commerce 2.4.5 e versioni successive, ma deve essere configurato per l’utilizzo. Estende il modulo `AdobeIms` per supportare il modulo che abilita la logica di autenticazione (`AdminAdobeIms`).

Per ulteriori informazioni sull&#39;abilitazione dell&#39;integrazione, vedere [Configurare l&#39;integrazione amministratore di Commerce con Adobe IMS](./adobe-ims-config.md).
