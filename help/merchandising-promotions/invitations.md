---
title: Inviti evento
description: Scopri come i clienti possono inviare e visualizzare gli inviti a eventi e vendite private dal dashboard dei loro account cliente.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Inviti evento

{{ee-feature}}

Quando gli inviti sono abilitati, i clienti possono inviare e visualizzare gli inviti dal dashboard dei propri account cliente. L&#39;e-mail di invito include un collegamento alla pagina di accesso del cliente del negozio.

## Inviti personali

Nella sezione _[!UICONTROL My Invitations]_dell&#39;account cliente sono elencati tutti gli inviti inviati dal cliente. I clienti possono inviare inviti ad amici e familiari per eventi del negozio, registri di regali, elenchi di desideri e così via.

![Inviti personali](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### Flusso di lavoro invito

1. **Il cliente prepara gli inviti**: dal dashboard dell&#39;account, il cliente prepara l&#39;elenco dei destinatari e completa l&#39;invito. A seconda della configurazione, è possibile includere un messaggio personalizzato.
1. **Il cliente invia inviti**: quando è pronto, il cliente fa clic sul pulsante _[!UICONTROL Send Invitations]_.
1. **Il sistema gestisce la trasmissione**: il sistema invia gli inviti in batch, in base al numero impostato nella configurazione.
1. **Il cliente monitora la risposta**: il cliente controlla lo stato di ogni invito dal dashboard account, come `Sent`, `Accepted` o `Canceled`.

### Inviare un invito

1. Nella barra laterale del proprio account sulla vetrina, il cliente sceglie **[!UICONTROL My Invitations]**.

1. Nella pagina _Invito personale_, seleziona **[!UICONTROL Send Invitation]**.

1. Definisce il nuovo invito:

   - Completa le informazioni e-mail.

   - (Facoltativo) Crea un invito con più indirizzi facendo clic su **+** e aggiungendo un altro indirizzo e-mail.

     Un singolo invito ha un limite di cinque indirizzi e-mail.

   - (Facoltativo) Immette un messaggio allegato.

1. Al termine, fa clic su **[!UICONTROL Send Invitation]**.

Viene inviata una notifica di invito all’indirizzo e-mail dell’utente invitato con il collegamento di istruzioni per impostare l’account.

>[!NOTE]
>
>Un utente può inviare un solo invito a un indirizzo e-mail specifico. Se si tenta di inviare nuovamente un invito allo stesso indirizzo e-mail, viene visualizzato un messaggio di errore e l’invito non viene inviato.

## Abilita inviti per il tuo punto vendita

La configurazione dell&#39;invito abilita gli inviti per l&#39;archivio e determina la modalità di invio.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Invitations]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL General]**.

   ![Configurazione clienti - inviti opzioni generali](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enable Invitations Functionality]** su `Yes`.

1. Per consentire ai clienti di gestire gli inviti dalla vetrina, impostare **Abilita inviti su vetrina** su `Yes`.

1. Imposta **[!UICONTROL Referred Customer Group]** su uno dei seguenti:

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. Imposta **[!UICONTROL New Accounts Registration]** su uno dei seguenti:

   - `By Invitation Only`
   - `Available to All`

1. A **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**, selezionare `Yes`.

1. Per limitare il numero di inviti che è possibile inviare contemporaneamente, immettere il numero nel campo **[!UICONTROL Max Invitations Allowed to be Sent at One Time]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Email]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - opzioni e-mail inviti](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - Selezionare l&#39;identità dell&#39;archivio da utilizzare come **[!UICONTROL Customer Invitation Email Sender]**.

   - Selezionare **[!UICONTROL Customer Invitation Email Template]** utilizzato per gli inviti inviati.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Inviare e gestire gli inviti nell’Amministratore

Nella sezione [Rapporti sulle vendite private](../getting-started/private-sales-reports.md) è possibile visualizzare il numero di inviti inviati durante un periodo specificato o i clienti a cui sono stati inviati inviti.

### Creare un invito in Amministratore

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add Invitations]**.

1. Nella schermata successiva, immetti gli indirizzi e-mail per invitare nuovi clienti, aggiungi un messaggio personalizzato, scegli un mittente e seleziona un gruppo di invitati.

   Se sono presenti più visualizzazioni dello store, utilizzare l&#39;opzione **[!UICONTROL Send From]** per specificare la visualizzazione dello store da cui viene inviato un invito.

   ![Informazioni sugli inviti](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save]**.

### Elimina inviti per singola entità

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Trova l’invito necessario utilizzando i filtri e aprilo in modalità di modifica.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Discard Invitation]**.

1. Per confermare l&#39;azione, fare clic su **[!UICONTROL OK]**.

### Elimina inviti per più entità

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. Individuare e selezionare gli inviti da eliminare.

1. In alto a sinistra, utilizzare il menu **[!UICONTROL Actions]** per scegliere **[!UICONTROL Discard Selected]** e fare clic su **[!UICONTROL Submit]**.

1. Per confermare l&#39;azione, fare clic su **[!UICONTROL OK]**.

### Descrizioni dei campi

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Select] | Selezionare la casella di controllo per selezionare gli inviti da sottoporre a un&#39;azione oppure utilizzare il controllo di selezione nell&#39;intestazione di colonna. Opzioni: `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | Numero ID interno di un invito |
| [!UICONTROL Email] | Un indirizzo e-mail del cliente corrispondente |
| [!UICONTROL Invitee] | E-mail utente invitato |
| [!UICONTROL Sent] | Ora e data di invio di un invito |
| [!UICONTROL Registered] | Ora e dati di registrazione di un cliente |
| [!UICONTROL Status] | Stato invito. Opzioni: `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | Il sito web corrispondente |
| [!UICONTROL Invitee Group] | Un gruppo di clienti di un invitato |

{style="table-layout:auto"}
