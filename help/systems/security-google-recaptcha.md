---
title: Google reCAPTCHA V3 e V2
description: Scopri come configurare Google reCAPTCHA per l’accesso come amministratore e varie azioni in vetrina avviate da clienti registrati.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 80b2ecc9fddd7a20d6824182f41f0d19f6d51003
workflow-type: tm+mt
source-wordcount: '1053'
ht-degree: 0%

---

# Google reCAPTCHA V3 e V2

[Google reCAPTCHA](https://developers.google.com/recaptcha) garantisce che un essere umano, anziché un computer (o &quot;bot&quot;), interagisca con il sito Web. A differenza di Adobe Commerce e Magento Open Source [CAPTCHA](security-captcha.md) standard, Google reCAPTCHA offre una protezione avanzata con una selezione di opzioni e metodi di visualizzazione diversi. Ulteriori informazioni sul traffico del sito web sono disponibili nel dashboard dell’account Google reCAPTCHA.

Google reCAPTCHA è configurato separatamente per l’amministratore e la vetrina.

- Per l&#39;amministratore, Google reCAPTCHA può essere utilizzato nella pagina [Accedi](../getting-started/admin-signin.md) e quando un utente richiede la reimpostazione della password. Se è abilitato anche il Commerce standard [CAPTCHA](security-captcha.md), è possibile utilizzare Google reCAPTCHA contemporaneamente senza alcun problema.

- Per la vetrina, Google reCAPTCHA può essere utilizzato per accedere a un [account cliente](../customers/customer-sign-in.md), inviare un messaggio dalla pagina [Contattaci](../getting-started/store-details.md#contact-us-form) e in numerose altre posizioni della vetrina.

  ![Google reCAPTCHA - accesso cliente](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA può essere implementato in diversi modi:

- _reCAPTCHA v3 Invisibile_: utilizza un algoritmo per valutare le interazioni dell&#39;utente e determinare la probabilità che l&#39;utente sia umano in base a un punteggio.

- _reCAPTCHA v2 Invisible_: esegue la verifica in background senza interazione dell&#39;utente. Gli utenti e i clienti vengono verificati automaticamente, ma potrebbe essere necessario selezionare immagini specifiche per completare una sfida.

- _reCAPTCHA v2 (&quot;Non sono un robot&quot;)_ — Convalida le richieste con la casella di controllo _&quot;Non sono un robot&quot;_.

>[!IMPORTANT]
>
>Prima di configurare Google reCAPTCHA, verificare che il file `PHP.ini` includa l&#39;impostazione seguente: `allow_url_fopen = 1`. Questo potrebbe richiedere l’assistenza dello sviluppatore. Vedere [Impostazioni PHP richieste](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=it){:target="_blank"} nella Guida all&#39;installazione.

## Passaggio 1: generare le chiavi reCAPTCHA di Google

Google reCAPTCHA richiede una coppia di chiavi API per abilitare. Puoi ottenere queste chiavi gratuitamente tramite il sito reCAPTCHA. Prima di generare le chiavi, è necessario conoscere il tipo di reCAPTCHA che si desidera utilizzare.

1. Apri la pagina Google reCAPTCHA e accedi al tuo account.

1. Per **[!UICONTROL Label]**, immettere un nome per identificare le chiavi per il riferimento interno.

   È necessario un set di chiavi per ogni tipo reCAPTCHA utilizzato nell’installazione di Adobe Commerce o Magento Open Source. Esempio: `Commerce Invisible`

1. Per **[!UICONTROL reCAPTCHA type]**, scegliere il metodo che si desidera utilizzare.

   - _reCAPTCHA v3 invisibile_
   - _reCAPTCHA v2 invisibile_
   - _reCAPTCHA v2 (&quot;Non sono un robot&quot;)_

1. Per **[!UICONTROL Domain]**, immetti il dominio del tuo archivio. Ad esempio: mystore.com

   Se disponi di più archivi con domini diversi, inserisci ciascun dominio su una riga separata.

   - Aggiungi il dominio dello store ed eventuali sottodomini.
   - È possibile aggiungere `localhost`, altri domini VM locali e domini di gestione temporanea in base alle esigenze per il test.

1. Selezionare la casella di controllo per **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. (Facoltativo) Selezionare la casella di controllo **[!UICONTROL Send alerts to owners]** per inviare una notifica se Google rileva problemi o traffico sospetto.

1. Fare clic su **[!UICONTROL Submit]** per completare la registrazione e ricevere le chiavi.

   >[!IMPORTANT]
   >
   >Non tutte le chiavi sono applicabili a tutti i tipi di reCAPTCHA e la loro applicazione errata potrebbe causare un comportamento imprevisto. Ad esempio, le chiavi reCAPTCHA di Google generate per reCAPTCHA v2 &quot;Non sono un robot&quot; non funzionano con _reCAPTCHA v2 Invisible_ e potrebbero bloccare la funzionalità in cui reCAPTCHA è abilitato.

## Passaggio 2: configurare Google reCAPTCHA per l’amministratore

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

1. Accedi al tuo account amministratore.

1. Nella barra laterale di amministrazione, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nell&#39;angolo superiore destro impostare **[!UICONTROL Store View]** su `Default Config`.

1. Nel pannello a sinistra, espandi **[!UICONTROL Security]** e fai clic su **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >Deselezionare la casella di controllo **[!UICONTROL Use system value]** per ogni campo che si desidera configurare.

1. Per utilizzare _[!DNL reCAPTCHA v2 ("I am not a robot")]_, espandere la sezione **[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**&#x200B;ed eseguire le operazioni seguenti:

   - Per **[!UICONTROL Google API Website Key]**, immettere la chiave del sito Web creata per questo tipo reCAPTCHA al momento della registrazione dell&#39;account Google reCAPTCHA.

   - Per **[!UICONTROL Google API Secret Key]**, immetti la chiave segreta associata al tuo account Google reCAPTCHA.

   - Per **[!UICONTROL Size]**, scegliere le dimensioni della casella Google reCAPTCHA che si desidera visualizzare. Opzioni: `Normal (default)` / `Compact`

   - Per **[!UICONTROL Theme]**, scegliere il tema da utilizzare per assegnare uno stile alla casella reCAPTCHA di Google. Opzioni: `Light Theme (default)` / `Dark Theme`

   - Per **[!UICONTROL Language Code]**, immettere il codice a due caratteri per specificare il linguaggio [&#x200B; utilizzato per il testo e la messaggistica Google reCAPTCHA](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - &quot;Non sono un robot&quot;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. Per utilizzare _[!DNL reCAPTCHA v2 Invisible]_, espandere la sezione **[!UICONTROL reCAPTCHA v2 Invisible]**&#x200B;ed eseguire le operazioni seguenti:

   - Per **[!UICONTROL Google API Website Key]**, immettere la chiave del sito Web creata per questo tipo reCAPTCHA al momento della registrazione dell&#39;account Google reCAPTCHA.

   - Per **[!UICONTROL Google API Secret Key]**, immetti la chiave segreta associata al tuo account Google reCAPTCHA.

   - Per **[!UICONTROL Invisible Badge Position]**, scegli la posizione del badge da utilizzare in ogni pagina. Opzioni: `Inline` / `Bottom Right` / `Bottom Left`

   - Per **[!UICONTROL Theme]**, scegliere il tema da utilizzare per assegnare uno stile alla casella Google reCAPTCHA. Opzioni: `Light Theme (default)` / `Dark Theme`

   - Per **[!UICONTROL Language Code]**, immettere un codice a due caratteri che specifica il linguaggio [&#x200B; utilizzato per il testo e i messaggi reCAPTCHA di Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 invisibile](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. Per utilizzare _[!DNL reCAPTCHA v3 Invisible]_, espandere la sezione **[!UICONTROL reCAPTCHA v3 Invisible]**&#x200B;ed eseguire le operazioni seguenti:

   - Per **[!UICONTROL Google API Website Key]**, immettere la chiave del sito Web creata per questo tipo reCAPTCHA al momento della registrazione dell&#39;account Google reCAPTCHA.

   - Per **[!UICONTROL Google API Secret Key]**, immetti la chiave segreta associata al tuo account Google reCAPTCHA.

   - Immettere **[!UICONTROL Minimum Score Threshold]** per identificare quando un&#39;interazione utente è contrassegnata come rischio potenziale; dove 1.0 è una tipica interazione utente e 0.0 è probabilmente un bot. Predefinito: `0.5`

   - Per **[!UICONTROL Invisible Badge Position]**, scegliere la posizione da utilizzare in ogni pagina. Opzioni: `Inline` / `Bottom Right` / `Bottom Left`

   - Per **[!UICONTROL Theme]**, scegliere il tema da utilizzare per assegnare uno stile alla casella Google reCAPTCHA. Opzioni: `Light Theme (default)` / `Dark Theme`

   - Per **[!UICONTROL Language Code]**, immettere un codice a due caratteri che specifica il linguaggio [&#x200B; utilizzato per il testo e i messaggi reCAPTCHA di Google](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 invisibile](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. Espandere **[!UICONTROL reCAPTCHA Validation Failure Messages]** e immettere i messaggi visualizzati nell&#39;amministratore se la convalida non riesce o non può essere completata.

   ![messaggi di errore CAPTCHA](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. Espandi la sezione **[!UICONTROL Admin Panel]** e configura quanto segue in base alle esigenze:

   - Impostare **[!UICONTROL Enable for Login]** sul tipo reCAPTCHA che si desidera utilizzare per la pagina di accesso amministratore.

   - Impostare **[!UICONTROL Enable for Forgot Password]** sul tipo reCAPTCHA che si desidera utilizzare per le richieste di reimpostazione della password.

   ![opzioni di amministrazione di reCAPTCHA](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## Passaggio 3: configurare Google reCAPTCHA per la vetrina

1. Nel pannello a sinistra in _[!UICONTROL Security]_, scegli **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Completa la sezione per ogni tipo reCAPTCHA che desideri utilizzare nella vetrina.

   Vedi le informazioni in _Passaggio 2: configurare Google reCAPTCHA per l&#39;amministratore_ per informazioni dettagliate sulle opzioni per ciascun tipo reCAPTCHA.

1. Espandere **[!UICONTROL reCAPTCHA Validation Failure Messages]** e immettere i messaggi visualizzati nella vetrina se la convalida non riesce o non è possibile completarla.

1. Espandere la sezione **[!UICONTROL Storefront]**.

   >[!NOTE]
   >
   >Deselezionare la casella di controllo **[!UICONTROL Use system value]** per ogni campo che si desidera configurare.

1. Imposta ogni campo della posizione della vetrina sul tipo di reCAPTCHA configurato per l’utilizzo.

   {{recaptcha-forms-list}}

   ![Configurazione opzioni storefront](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Passaggio 4: salvare la configurazione

1. Al termine delle impostazioni di configurazione, fare clic su **[!UICONTROL Save Config]**.

1. Nel messaggio nella parte superiore dell&#39;area di lavoro, fare clic su **[!UICONTROL Cache Management]** e aggiornare ogni cache non valida.
