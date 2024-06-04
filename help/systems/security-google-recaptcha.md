---
title: Google reCAPTCHA
description: Scopri come configurare Google reCAPTCHA per l’accesso come amministratore e varie azioni in vetrina avviate da clienti registrati.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1046'
ht-degree: 0%

---

# Google reCAPTCHA

[Google reCAPTCHA](https://developers.google.com/recaptcha) assicura che un essere umano, anziché un computer (o &quot;bot&quot;), interagisca con il sito web. A differenza di Adobe Commerce e Magento Open Source standard [CAPTCHA](security-captcha.md), Google reCAPTCHA offre una maggiore sicurezza con una selezione di opzioni e metodi di visualizzazione diversi. Ulteriori informazioni sul traffico del sito web sono disponibili nel dashboard dell’account Google reCAPTCHA.

Google reCAPTCHA è configurato separatamente per l’amministratore e la vetrina.

- Per l’amministratore, è possibile utilizzare Google reCAPTCHA sul [Accedi](../getting-started/admin-signin.md) e quando un utente richiede la reimpostazione della password. Se il Commerce standard [CAPTCHA](security-captcha.md) è anche abilitato, Google reCAPTCHA può essere utilizzato allo stesso tempo senza alcun problema.

- Per la vetrina, Google reCAPTCHA può essere utilizzato per accedere a [account cliente](../customers/customer-sign-in.md), invia un messaggio da [Contattaci](../getting-started/store-details.md#contact-us-form) e in numerose altre posizioni della vetrina.

  ![Google reCAPTCHA - accesso del cliente](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA può essere implementato in diversi modi:

- _reCAPTCHA v3 Invisibile_ — Utilizza un algoritmo per valutare le interazioni dell&#39;utente e determinare la probabilità che l&#39;utente sia umano in base a un punteggio.

- _reCAPTCHA v2 Invisibile_ — Esegue la verifica in background senza interazione dell&#39;utente. Gli utenti e i clienti vengono verificati automaticamente, ma potrebbe essere necessario selezionare immagini specifiche per completare una sfida.

- _reCAPTCHA v2 (&quot;Io non sono un robot&quot;)_ — Convalida le richieste con _&quot;Non sono un robot&quot;_ casella di controllo.

>[!IMPORTANT]
>
>Prima di configurare Google reCAPTCHA, assicurati che il tuo `PHP.ini` Il file include le seguenti impostazioni: `allow_url_fopen = 1`. Questo potrebbe richiedere l’assistenza dello sviluppatore. Consulta [Impostazioni PHP richieste](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html){:target=&quot;_blank&quot;} nella Guida all’installazione.

## Passaggio 1: generare le chiavi reCAPTCHA di Google

Google reCAPTCHA richiede una coppia di chiavi API per abilitare. Puoi ottenere queste chiavi gratuitamente tramite il sito reCAPTCHA. Prima di generare le chiavi, è necessario conoscere il tipo di reCAPTCHA che si desidera utilizzare.

1. Apri la pagina Google reCAPTCHA e accedi al tuo account.

1. Per **[!UICONTROL Label]**, immetti un nome per identificare le chiavi per riferimento interno.

   È necessario un set di chiavi per ogni tipo reCAPTCHA utilizzato nell’installazione di Adobe Commerce o di Magento Open Source. Ad esempio: `Commerce Invisible`

1. Per **[!UICONTROL reCAPTCHA type]**, scegliere il metodo che si desidera utilizzare.

   - _reCAPTCHA v3 Invisibile_
   - _reCAPTCHA v2 Invisibile_
   - _reCAPTCHA v2 (&quot;Io non sono un robot&quot;)_

1. Per **[!UICONTROL Domain]**, immetti il dominio dello store. Ad esempio: mystore.com

   Se disponi di più archivi con domini diversi, inserisci ciascun dominio su una riga separata.

   - Aggiungi il dominio dello store ed eventuali sottodomini.
   - Puoi aggiungere `localhost`, altri domini VM locali e domini di staging necessari per il test.

1. Seleziona la casella di controllo per **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. (Facoltativo) Seleziona la **[!UICONTROL Send alerts to owners]** casella di controllo per inviare una notifica se Google rileva problemi o traffico sospetto.

1. Clic **[!UICONTROL Submit]** per completare la registrazione e ricevere le chiavi.

   >[!IMPORTANT]
   >
   >Non tutte le chiavi sono applicabili a tutti i tipi di reCAPTCHA e la loro applicazione errata potrebbe causare un comportamento imprevisto. Ad esempio, le chiavi Google reCAPTCHA generate per reCAPTCHA v2 &quot;I&#39;m not a robot&quot; non funzionano con _reCAPTCHA v2 Invisibile_ e potrebbero bloccare la funzionalità in cui è abilitato reCAPTCHA.

## Passaggio 2: configurare Google reCAPTCHA per l’amministratore

1. Accedi al tuo account amministratore.

1. Nella barra laterale Amministratore, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nell&#39;angolo in alto a destra, imposta **[!UICONTROL Store View]** a `Default Config`.

1. Nel pannello a sinistra, espandi **[!UICONTROL Security]** e fai clic su **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >Cancella **[!UICONTROL Use system value]** per ogni campo da configurare.

1. Da utilizzare _[!DNL reCAPTCHA v2 ("I am not a robot")]_, espandi **[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**ed effettuare le seguenti operazioni:

   - Per **[!UICONTROL Google API Website Key]**, immetti la chiave del sito web creata per questo tipo di reCAPTCHA al momento della registrazione dell’account Google reCAPTCHA.

   - Per **[!UICONTROL Google API Secret Key]**, immetti la chiave segreta associata al tuo account Google reCAPTCHA.

   - Per **[!UICONTROL Size]**, scegliere le dimensioni della casella Google reCAPTCHA che si desidera visualizzare. Opzioni: `Normal (default)` / `Compact`

   - Per **[!UICONTROL Theme]**, scegli il tema da utilizzare per assegnare uno stile alla casella Google reCAPTCHA. Opzioni: `Light Theme (default)` / `Dark Theme`

   - Per **[!UICONTROL Language Code]**, immettere il codice a due caratteri per specificare [lingua utilizzata per il testo e i messaggi reCAPTCHA di Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - &quot;Io non sono un robot&quot;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. Da utilizzare _[!DNL reCAPTCHA v2 Invisible]_, espandi **[!UICONTROL reCAPTCHA v2 Invisible]**ed effettuare le seguenti operazioni:

   - Per **[!UICONTROL Google API Website Key]**, immetti la chiave del sito web creata per questo tipo di reCAPTCHA al momento della registrazione dell’account Google reCAPTCHA.

   - Per **[!UICONTROL Google API Secret Key]**, immetti la chiave segreta associata al tuo account Google reCAPTCHA.

   - Per **[!UICONTROL Invisible Badge Position]**, scegli la posizione del badge da utilizzare in ogni pagina. Opzioni: `Inline` / `Bottom Right` / `Bottom Left`

   - Per **[!UICONTROL Theme]**, scegli il tema da utilizzare per assegnare uno stile alla casella Google reCAPTCHA. Opzioni: `Light Theme (default)` / `Dark Theme`

   - Per **[!UICONTROL Language Code]**, immettere un codice a due caratteri che specifichi [lingua utilizzata per il testo e i messaggi reCAPTCHA di Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 Invisibile](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. Da utilizzare _[!DNL reCAPTCHA v3 Invisible]_, espandi **[!UICONTROL reCAPTCHA v3 Invisible]**ed effettuare le seguenti operazioni:

   - Per **[!UICONTROL Google API Website Key]**, immetti la chiave del sito web creata per questo tipo di reCAPTCHA al momento della registrazione dell’account Google reCAPTCHA.

   - Per **[!UICONTROL Google API Secret Key]**, immetti la chiave segreta associata al tuo account Google reCAPTCHA.

   - Inserisci il **[!UICONTROL Minimum Score Threshold]** identificare quando un’interazione dell’utente è contrassegnata come rischio potenziale; dove 1.0 è una tipica interazione dell’utente e 0.0 è probabilmente un bot. Predefinito: `0.5`

   - Per **[!UICONTROL Invisible Badge Position]**, scegli la posizione da utilizzare in ogni pagina. Opzioni: `Inline` / `Bottom Right` / `Bottom Left`

   - Per **[!UICONTROL Theme]**, scegli il tema da utilizzare per assegnare uno stile alla casella Google reCAPTCHA. Opzioni: `Light Theme (default)` / `Dark Theme`

   - Per **[!UICONTROL Language Code]**, immettere un codice a due caratteri che specifichi [lingua utilizzata per il testo e i messaggi reCAPTCHA di Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 Invisibile](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. Espandi **[!UICONTROL reCAPTCHA Validation Failure Messages]** e immetti i messaggi visualizzati nell’Amministratore se la convalida non riesce o non può essere completata.

   ![Messaggi di errore reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. Espandi **[!UICONTROL Admin Panel]** e configura quanto segue in base alle esigenze:

   - Imposta **[!UICONTROL Enable for Login]** al tipo reCAPTCHA che desideri utilizzare per la pagina di accesso amministratore.

   - Imposta **[!UICONTROL Enable for Forgot Password]** al tipo reCAPTCHA che desideri utilizzare per le richieste di reimpostazione della password.

   ![Opzioni di amministrazione reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## Passaggio 3: configurare Google reCAPTCHA per la vetrina

1. Nel pannello a sinistra sotto _[!UICONTROL Security]_, scegli **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Completa la sezione per ogni tipo reCAPTCHA che desideri utilizzare nella vetrina.

   Consulta le informazioni in _Passaggio 2: configurare Google reCAPTCHA per l’amministratore_ per informazioni dettagliate sulle opzioni per ciascun tipo reCAPTCHA.

1. Espandi **[!UICONTROL reCAPTCHA Validation Failure Messages]** e inserisci i messaggi visualizzati nella vetrina se la convalida non riesce o non può essere completata.

1. Espandi **[!UICONTROL Storefront]** sezione.

   >[!NOTE]
   >
   >Cancella **[!UICONTROL Use system value]** per ogni campo da configurare.

1. Imposta ogni campo della posizione della vetrina sul tipo di reCAPTCHA configurato per l’utilizzo.

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg) (Disponibile solo con Adobe Commerce B2B)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![Configurazione delle opzioni Storefront](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Passaggio 4: salvare la configurazione

1. Al termine delle impostazioni di configurazione, fai clic su **[!UICONTROL Save Config]**.

1. Nel messaggio nella parte superiore dell’area di lavoro, fai clic su **[!UICONTROL Cache Management]** e aggiorna ogni cache non valida.
