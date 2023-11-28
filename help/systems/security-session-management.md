---
title: Gestione delle sessioni
description: Scopri come configurare la gestione delle sessioni per proteggere l’amministratore e la vetrina.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Gestione delle sessioni

[Gestione delle sessioni](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) è una best practice DoS (Anti-Denial of Service) per la sicurezza API. Una sessione rappresenta il tempo che un visitatore trascorre sul sito e non è correlata al tempo in cui gli utenti amministratore o i clienti hanno effettuato l’accesso ai loro account.

Una sessione è una sequenza di transazioni di richiesta HTTP e risposta di rete associate allo stesso utente. È un modo per associare un client (amministratore) ai propri dati quando accedono al server. Le sessioni vengono utilizzate per stabilire variabili, come i diritti di accesso e le impostazioni di localizzazione, che si applicano a ogni interazione di un utente con un’applicazione web durante la sessione.

## Dimensione sessione

Utilizza le seguenti impostazioni di configurazione per limitare la dimensione massima della sessione per gli utenti amministratori e i visitatori della vetrina:

- **[!UICONTROL Max Session Size in Admin]**- Limita la dimensione massima delle sessioni in byte. Utilizzare `0` per disattivare.
- **[!UICONTROL Max Session Size in Storefront]**- Limita la dimensione massima delle sessioni in byte. Utilizzare `0` per disattivare.

>[!TIP]
>
>Entrambe le impostazioni sono misurate in byte e il valore predefinito è `256000` byte (o 256 KB).

**_Per configurare la dimensione massima della sessione:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]**  > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Security]** per accedere alle impostazioni della sessione.

   ![Impostazioni sessione](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. Immettere le nuove dimensioni di sessione in byte.

   >[!WARNING]
   >
   >L’impostazione di un valore troppo basso può causare problemi. Se si imposta una delle opzioni sotto il valore predefinito di 256000 byte, verrà visualizzato un messaggio di avviso. Se si fa clic su **[!UICONTROL No]**, il sistema modifica il valore in `256000`.

1. Clic **[!UICONTROL Save Config]**.

### Sessioni di amministrazione

Se si supera la dimensione massima della sessione, viene visualizzato un messaggio di errore e il sistema registra il vincolo della dimensione della sessione su `var/log` directory.

Se perdi l’accesso all’amministratore dopo aver impostato le dimensioni della sessione troppo basse, utilizza CLI per reimpostare la configurazione:

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Sessioni vetrina

Se si supera la dimensione massima della sessione, non viene visualizzato alcun errore, ma il sistema registra il vincolo della dimensione della sessione su `var/log` directory.

## Convalida della sessione

Adobe Commerce e Magento Open Source consentono di convalidare le variabili di sessione come misura protettiva contro possibili attacchi di fissazione delle sessioni o tentativi di avvelenare o dirottare le sessioni degli utenti. Le impostazioni di convalida della sessione determinano il modo in cui le variabili di sessione vengono convalidate durante ogni visita dello store e se l’ID sessione è incluso nell’URL dello store.

Per informazioni tecniche, consulta [Usa Redis per l’archiviazione della sessione](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) nel _Guida alla configurazione_.

![Configurazione generale - Convalida della sessione Web](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

La convalida verifica che i visitatori siano quello che dicono di essere confrontando il valore nelle variabili di convalida con i dati della sessione memorizzati in `$_SESSION` dati per l’utente. La convalida non riesce se l’informazione non viene trasmessa come previsto e la variabile corrispondente è vuota. A seconda delle impostazioni di convalida della sessione, se una variabile di sessione non supera il processo di convalida, la sessione client viene terminata immediatamente.

L’abilitazione di tutte le variabili di convalida può contribuire a prevenire gli attacchi, ma potrebbe anche influire sulle prestazioni del server. Per impostazione predefinita, la convalida di tutte le variabili di sessione è disabilitata. È consigliabile sperimentare le impostazioni per trovare la combinazione ottimale per l’installazione di Adobe Commerce o di Magento Open Source. L&#39;attivazione di tutte le variabili di convalida potrebbe rivelarsi eccessivamente restrittiva e potrebbe impedire l&#39;accesso ai clienti con connessioni Internet che passano attraverso un server proxy o provengono da un firewall. Per ulteriori informazioni sulle variabili di sessione e sul loro utilizzo, consulta la documentazione di amministrazione del sistema Linux®.

**_Per configurare la convalida della sessione:_**

1. Il giorno _Amministratore_ barra laterale, vai a  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi _[!UICONTROL General]_e scegli **[!UICONTROL Web]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Session Validation Settings]** sezione.

1. Imposta ciascuna delle opzioni di configurazione:

   - **[!UICONTROL Validate REMOTE_ADDR]** — Imposta su `Yes` per verificare che l’indirizzo IP di una richiesta corrisponda a quello memorizzato in `$_SESSION` variabile.

   - **[!UICONTROL Validate HTTP_VIA]** — Imposta su `Yes` per verificare che l’indirizzo proxy di una richiesta in ingresso corrisponda a quello memorizzato in `$_SESSION` variabile.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — Imposta su `Yes` per verificare che l&#39;indirizzo inoltrato per una richiesta corrisponda a quello memorizzato in `$_SESSION` variabile.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — Imposta su `Yes` per verificare che il browser o il dispositivo utilizzato per accedere all’archivio durante una sessione corrisponda a quello memorizzato in `$_SESSION` variabile.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Durata della sessione di amministrazione

Come misura di sicurezza, il _Amministratore_ inizialmente è impostato su timeout dopo 900 secondi (15 minuti) di inattività della tastiera. Puoi regolare la durata della sessione in base al tuo stile di lavoro.

**_Per regolare la durata della sessione di amministrazione:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Scorri verso il basso ed espandi **[!UICONTROL Advanced]** nel pannello laterale sinistro.

1. Clic **[!UICONTROL Admin]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il _[!UICONTROL Security]_sezione.

1. Per **[!UICONTROL Admin Session Lifetime (seconds)]**, immetti il numero di secondi in cui una sessione rimane attiva prima del timeout.

   ![Configurazione avanzata - Impostazioni di protezione amministratore](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.## Durata sessione amministratore

Come misura di sicurezza, il _Amministratore_ inizialmente è impostato su timeout dopo 900 secondi (15 minuti) di inattività della tastiera. Puoi regolare la durata della sessione in base al tuo stile di lavoro.

**_Per regolare la durata della sessione di amministrazione:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Scorri verso il basso ed espandi **[!UICONTROL Advanced]** nel pannello laterale sinistro.

1. Clic **[!UICONTROL Admin]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il _Sicurezza_ sezione.

1. Per **[!UICONTROL Admin Session Lifetime (seconds)]**, immetti il numero di secondi in cui una sessione rimane attiva prima del timeout.

   ![Configurazione avanzata - Impostazioni di protezione amministratore](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
