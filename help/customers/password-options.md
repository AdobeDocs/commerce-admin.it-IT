---
title: Opzioni password cliente
description: Le opzioni della password del cliente determinano il livello di sicurezza per le varie funzioni rivolte al cliente del vostro negozio.
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Opzioni password cliente

Le opzioni relative alla password del cliente determinano il livello di protezione utilizzato per le richieste di reimpostazione della password, i modelli e-mail utilizzati per la notifica al cliente e la durata del collegamento di recupero della password. Puoi consentire ai clienti di modificare le proprie password o richiedere che solo gli amministratori degli archivi possano farlo.

## Configurare le opzioni della password del cliente

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Customer Configuration]**.

1. Espandi **[!UICONTROL Password Options]** sezione.

   ![Opzioni password](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. Imposta il **[!UICONTROL Password Reset Protection Type]** al metodo che si desidera utilizzare per controllare le richieste di reimpostazione password:

   - `By IP and Email` - Verificare la presenza di tentativi precedenti di reimpostazione della password per un indirizzo e-mail specifico o da un IP specifico.
   - `By IP` - Controllare eventuali tentativi precedenti di reimpostazione della password da un IP specifico.
   - `By Email` - Verificare la presenza di tentativi precedenti di reimpostazione della password per un messaggio e-mail specifico.
   - `None` - Protezione disabilitata (nessun limite per il ripristino della password).

   Il **[!UICONTROL Max Number of Password Reset Requests]** e **[!UICONTROL Min Time Between Password Reset Requests]** sono calcolati in base a questa configurazione.

1. Per limitare il numero di richieste di reimpostazione della password inviate all&#39;ora, eseguire le operazioni seguenti:

   - Per **[!UICONTROL Max Number of Password Reset Requests]**, immetti il numero massimo di richieste di reimpostazione della password che possono essere inviate all&#39;ora.

   - Per **[!UICONTROL Min Time Between Password Reset Requests]**, inserisci il numero minimo di minuti che devono trascorrere tra le richieste.

1. Per configurare la notifica e-mail di reimpostazione password, effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Forgot Email Template]** al modello utilizzato per l’e-mail inviata ai clienti che hanno dimenticato le password.

   - Imposta **[!UICONTROL Remind Email Template]** al modello utilizzato quando un utente amministratore reimposta la password di un cliente.

   - Imposta **[!UICONTROL Reset Password Template]** al modello utilizzato quando i clienti modificano le password.

   - Imposta **[!UICONTROL Password Template Email Sender]** al [contatto store](../getting-started/store-details.md) che viene visualizzato come mittente delle notifiche relative alla password.

1. Completa le seguenti opzioni di sicurezza per la reimpostazione della password:

   - Per **[!UICONTROL Recovery Link Expiration Period (hours)]**, immettere il numero di ore prima della scadenza del collegamento di recupero password.

   - Se desideri che i campi nei moduli per l’accesso ai clienti e per le password dimenticate vengano compilati automaticamente dalle voci precedenti, imposta **[!UICONTROL Enable Autocomplete on login/forgot password forms]** a `Yes`.

   - Per **[!UICONTROL Number of Required Character Classes]**, immettere il numero di tipi di carattere diversi che devono essere inclusi in una password in base alle seguenti classi di caratteri:

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - Per **[!UICONTROL Maximum Login Failures to Lockout Account]**, inserisci il numero di tentativi di accesso non riusciti fino a quando l’account del cliente non viene bloccato. Per tentativi illimitati, immetti zero (`0`).

   - Per **[!UICONTROL Minimum Password Length]**, immettere il numero minimo di caratteri utilizzabili in una password. Il numero deve essere maggiore di zero.

   - Per **[!UICONTROL Lockout Time (minutes)]**, immetti il numero di minuti in cui un account cliente è bloccato dopo troppi tentativi di accesso non riusciti.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
