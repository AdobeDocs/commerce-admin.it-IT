---
title: Opzioni password cliente
description: Le opzioni della password del cliente determinano il livello di sicurezza per le varie funzioni rivolte al cliente del vostro negozio.
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/ttWsiKhuvquDE2oQRWLF9rTDTZ64BHkKD0Lbv-EDnHs
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# Opzioni password cliente

Le opzioni relative alla password del cliente determinano il livello di protezione utilizzato per le richieste di reimpostazione della password, i modelli e-mail utilizzati per la notifica al cliente e la durata del collegamento di recupero della password. Puoi consentire ai clienti di modificare le proprie password o richiedere che solo gli amministratori degli archivi possano farlo.

## Configurare le opzioni della password del cliente

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Customer Configuration]**.

1. Espandere la sezione **[!UICONTROL Password Options]**.

   ![Opzioni password](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. Impostare **[!UICONTROL Password Reset Protection Type]** sul metodo che si desidera utilizzare per controllare le richieste di reimpostazione password:

   - `By IP and Email` - Verificare la presenza di tentativi precedenti di reimpostazione della password per un indirizzo e-mail specifico o da un IP specifico.
   - `By IP` - Verificare la presenza di tentativi precedenti di reimpostazione della password da un IP specifico.
   - `By Email` - Verificare la presenza di tentativi precedenti di reimpostazione della password per l&#39;indirizzo e-mail specifico.
   - `None` - Protezione disabilitata (nessun limite per il ripristino della password).

   **[!UICONTROL Max Number of Password Reset Requests]** e **[!UICONTROL Min Time Between Password Reset Requests]** sono calcolati in base a questa configurazione.

1. Per limitare il numero di richieste di reimpostazione della password inviate all&#39;ora, eseguire le operazioni seguenti:

   - Per **[!UICONTROL Max Number of Password Reset Requests]**, immettere il numero massimo di richieste di reimpostazione della password che è possibile inviare all&#39;ora.

   - Per **[!UICONTROL Min Time Between Password Reset Requests]**, immettere il numero minimo di minuti che devono trascorrere tra le richieste.

1. Per configurare la notifica e-mail di reimpostazione password, effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Forgot Email Template]** sul modello utilizzato per l&#39;e-mail inviata ai clienti che hanno dimenticato le password.

   - Impostare **[!UICONTROL Remind Email Template]** sul modello utilizzato quando un utente amministratore reimposta la password di un cliente.

   - Imposta **[!UICONTROL Reset Password Template]** sul modello utilizzato quando i clienti modificano le password.

   - Imposta **[!UICONTROL Password Template Email Sender]** sul [contatto archivio](../getting-started/store-details.md) che viene visualizzato come mittente delle notifiche relative alla password.

1. Completa le seguenti opzioni di sicurezza per la reimpostazione della password:

   - Per **[!UICONTROL Recovery Link Expiration Period (hours)]**, immettere il numero di ore che precedono la scadenza del collegamento di recupero password.

   - Se si desidera che i campi nei moduli di accesso cliente e password dimenticata vengano compilati automaticamente dalle voci precedenti, impostare **[!UICONTROL Enable Autocomplete on login/forgot password forms]** su `Yes`.

   - Per **[!UICONTROL Number of Required Character Classes]**, immettere il numero di tipi di carattere diversi che devono essere inclusi in una password in base alle seguenti classi di caratteri:

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - Per **[!UICONTROL Maximum Login Failures to Lockout Account]**, immettere il numero di tentativi di accesso non riusciti fino al blocco dell&#39;account cliente. Per tentativi illimitati, immettere zero (`0`).

   - Per **[!UICONTROL Minimum Password Length]**, immettere il numero minimo di caratteri utilizzabili in una password. Il numero deve essere maggiore di zero.

   - Per **[!UICONTROL Lockout Time (minutes)]**, immettere il numero di minuti di blocco di un account cliente dopo troppi tentativi di accesso non riusciti.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
