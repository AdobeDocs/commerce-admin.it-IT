---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel] dell'amministratore di Commerce.
exl-id: e4e6771a-487a-43ee-8b98-6acee4599aaf
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]

>[!IMPORTANT]
>
>Prima di configurare Google reCAPTCHA, è necessario assicurarsi che il file `PHP.ini` includa l&#39;impostazione seguente: `allow_url_fopen = 1`. Questo potrebbe richiedere l’assistenza dello sviluppatore. Vedere [Impostazioni PHP richieste](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=it) nella _Guida all&#39;installazione_.

{{config}}

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Google reCAPTCHA](../../systems/security-google-recaptcha.md) nella _Guida dell&#39;amministratore_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;Non sono un robot&quot;)](./assets/recaptcha-admin-v2-not-robot.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--|--|--|
| [!UICONTROL Google API Website Key] | Globale | Chiave del sito Web creata al momento della registrazione dell&#39;account Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Globale | La chiave segreta associata al tuo account Google reCAPTCHA. |
| [!UICONTROL Size] | Globale | Dimensione della casella Google reCAPTCHA visualizzata durante l&#39;accesso. Opzioni: `Normal` (predefinito) / `Compact` |
| [!UICONTROL Theme] | Globale | Determina lo stile della casella Google reCAPTCHA. Opzioni: `Light Theme` (predefinito) / `Dark Theme` |
| [!UICONTROL Language Code] | Globale | [codice a due caratteri](https://developers.google.com/recaptcha/docs/language) che specifica il linguaggio utilizzato per il testo e i messaggi reCAPTCHA di Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 invisibile](./assets/recaptcha-admin-v2-invisible.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--|--|--|
| [!UICONTROL Google API Website Key] | Globale | Chiave del sito Web creata al momento della registrazione dell&#39;account Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Globale | La chiave segreta associata al tuo account Google reCAPTCHA. |
| [!UICONTROL Invisible Badge Position] | Globale | La posizione del badge reCAPTCHA invisibile su ogni pagina. Opzioni: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Globale | Determina lo stile della casella Google reCAPTCHA. Opzioni: `Light Theme` (predefinito) / `Dark Theme` |
| [!UICONTROL Language Code] | Globale | [codice a due caratteri](https://developers.google.com/recaptcha/docs/language) che specifica il linguaggio utilizzato per il testo e i messaggi reCAPTCHA di Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 invisibile](./assets/recaptcha-admin-v3-invisible.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--|--|--|
| [!UICONTROL Google API Website Key] | Globale | Chiave del sito Web creata al momento della registrazione dell&#39;account Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Globale | La chiave segreta associata al tuo account Google reCAPTCHA. |
| [!UICONTROL Minimum Score Threshold] | Globale | Punteggio minimo che identifica un’interazione dell’utente come rischio potenziale, dove 1,0 è una tipica interazione dell’utente e 0,0 è probabilmente un bot. Predefinito: `0.5` |
| [!UICONTROL Invisible Badge Position] | Globale | La posizione del badge reCAPTCHA invisibile su ogni pagina. Opzioni: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Globale | Determina lo stile della casella Google reCAPTCHA. Opzioni: `Light Theme` (predefinito) / `Dark Theme` |
| [!UICONTROL Language Code] | Globale | [codice a due caratteri](https://developers.google.com/recaptcha/docs/language) che specifica il linguaggio utilizzato per il testo e i messaggi reCAPTCHA di Google. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![Messaggi di errore](./assets/recaptcha-admin-failure-messages.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Globale | Messaggio visualizzato nell’amministratore se la verifica non riesce. Testo predefinito: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Globale | Il messaggio visualizzato nell’amministratore se reCAPTCHA non restituisce un risultato di verifica. Testo predefinito: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Admin Panel]

![Pannello di amministrazione](./assets/recaptcha-admin-panel.png)<!-- zoom -->

>[!NOTE]
>
>Il tipo reCAPTCHA scelto deve corrispondere al tipo associato alla chiave API dell’account Google reCAPTCHA.

>[!WARNING]
>
>Quando si utilizza reCAPTCHA versione 3, un utente autentico con un punteggio basso non può procedere. Per la versione 2, un utente autentico con un punteggio basso riceve una sfida. Valuta attentamente se gli utenti autentici con un punteggio basso devono avere l’opportunità di risolvere un problema (versione 2) o essere bloccati (versione 3).

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--|--|--|
| [!UICONTROL Enable for Login] | Globale | Determina il tipo di reCAPTCHA abilitato per il [accesso amministratore](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=it). Opzioni:<br/>**`No`**- (impostazione predefinita) non convalida l&#39;accesso amministratore.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede che l&#39;utente selezioni la casella di controllo _Non sono un robot_.<br />**`Invisible reCAPTCHA v2`**- Convalida il comportamento dell&#39;utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (consigliato) convalida il comportamento dell&#39;utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Forgot Password] | Globale | Determina il tipo di reCAPTCHA abilitato per richiedere una [reimpostazione password amministratore](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=it#reset-your-password). Opzioni:<br/>**`No`**- (impostazione predefinita) non convalida la richiesta di reimpostazione della password.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede che l&#39;utente selezioni la casella di controllo _Non sono un robot_.<br />**`Invisible reCAPTCHA v2`**- Convalida il comportamento dell&#39;utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCaptcha v3`** - (consigliato) convalida il comportamento dell&#39;utente in background in base al punteggio di interazione. |

{style="table-layout:auto"}
