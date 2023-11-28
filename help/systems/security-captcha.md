---
title: CAPTCHA
description: Scopri come configurare CAPTCHA per l’accesso come amministratore e varie azioni in vetrina avviate da clienti registrati.
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '946'
ht-degree: 0%

---

# CAPTCHA

Un CAPTCHA è un dispositivo visivo che assicura che un essere umano, anziché un computer (o &quot;bot&quot;), interagisca con il sito. CAPTCHA è un acronimo di _Test di Turing completamente automatizzato per distinguere computer e persone_. Può essere utilizzato sia per l’accesso come amministratore che per varie azioni della vetrina avviate da clienti registrati. Adobe Commerce e il Magento Open Source supportano il CAPTCHA standard descritto in questo argomento e [Google reCAPTCHA](security-google-recaptcha.md).

Per ricaricare il CAPTCHA il numero di volte necessario, fai clic sull’icona Ricarica nell’angolo superiore destro dell’immagine. Il CAPTCHA è completamente configurabile e può essere impostato ogni volta o solo dopo un determinato numero di tentativi di accesso non riusciti.

![Accedi con CAPTCHA](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## Configurare CAPTCHA per l’amministratore

Per un ulteriore livello di sicurezza, puoi aggiungere un CAPTCHA alla pagina Accesso amministratore e Password dimenticata. Gli utenti amministratori possono ricaricare il CAPTCHA visualizzato facendo clic sul pulsante _Ricarica_ ![icona ricarica](./assets/CAPTCHA-icon-reload.png) nell’angolo superiore destro dell’immagine. Il numero di ricaricamenti è illimitato.

![Amministratore - Accedi con CAPTCHA](./assets/security-captcha-admin.png){width="300"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Admin]**.

1. Nell&#39;angolo in alto a destra, imposta **[!UICONTROL Store View]** a `Default`.

   Se il [ambito](../getting-started/websites-stores-views.md#scope-settings) dell’installazione di Commerce include più siti web, scegli quelli in cui desideri applicare la configurazione CAPTCHA.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL CAPTCHA]** sezione.

1. Imposta **[!UICONTROL Enable CAPTCHA in Admin]** a `Yes`. Quindi completare le altre opzioni come segue:

   ![Amministratore - Configurazione CAPTCHA](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - Inserisci il nome del **[!UICONTROL Font]** da utilizzare per i simboli CAPTCHA (impostazione predefinita: `LinLibertine`).

     Per aggiungere un font personalizzato, il file font deve trovarsi nella stessa directory dell’installazione di Commerce e deve essere dichiarato nel `config.xml` file del modulo Captcha in `app/code/Magento/Captcha/etc`.

   - Selezionare una delle opzioni seguenti **[!UICONTROL Forms]** dove deve essere utilizzato il CAPTCHA. Per scegliere più moduli, tenere premuto Ctrl (PC) o Comando (Mac).

      - `Admin Login`
      - `Admin Forgot Password`

   - Imposta **[!UICONTROL Displaying Modes]** a uno dei seguenti elementi:

      - `Always` — CAPTCHA è sempre richiesto per accedere all&#39;amministratore.
      - `After number of attempts to login` — Questa opzione è valida solo per il modulo di accesso amministratore. Se selezionata, la _[!UICONTROL Number of Unsuccessful Attempts to Login]_viene visualizzato. Immetti il numero di tentativi di accesso che desideri consentire. Il valore 0 (zero) è simile all&#39;impostazione Modalità di visualizzazione su `Always`.

     Per tenere traccia del numero di tentativi di accesso non riusciti, viene conteggiato ogni tentativo di accesso con un unico indirizzo e-mail e da un indirizzo IP. Il numero massimo di tentativi di accesso consentiti dallo stesso indirizzo IP è 1.000. Questa limitazione si applica solo quando CAPTCHA è abilitato.

   - Per **[!UICONTROL Number of Unsuccessful Attempts to Login]**, immetti il numero di tentativi di accesso dell’amministratore prima che venga visualizzato il CAPTCHA. Se impostato su zero (`0`), CAPTCHA è sempre obbligatorio.

   - Per **[!UICONTROL CAPTCHA Timeout (minutes)]**, inserisci il numero di minuti prima della scadenza del CAPTCHA. Alla scadenza del CAPTCHA, l’amministratore deve ricaricare la pagina.

   - Inserisci il **[!UICONTROL Number of Symbols]** nel CAPTCHA. Fino a otto (`8`) possono essere utilizzati. Per un numero variabile di simboli che cambiano con ogni CAPTCHA, inserisci un intervallo (ad esempio `5-8`).

   - Per **[!UICONTROL Symbols Used in CAPTCHA]**, immettere le lettere (a-z e A-Z) e i numeri (0-9) che si desidera visualizzare in modo casuale nel CAPTCHA. Simboli difficili da distinguere da altri simboli, ad esempio `i`, `l`, o `1`, non sono inclusi nel set predefinito di simboli CAPTCHA.

   - Imposta **[!UICONTROL Case Sensitive]** a `Yes` se desideri richiedere agli amministratori di immettere i caratteri in maiuscolo o minuscolo esattamente come mostrato nel CAPTCHA.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Configurare CAPTCHA per la vetrina

Ai clienti può essere richiesto di immettere un CAPTCHA ogni volta che accedono ai loro account o dopo diversi tentativi di accesso non riusciti. Inoltre, è possibile configurare numerosi moduli utilizzati nella vetrina per richiedere la verifica da parte di CAPTCHA.

![CAPTCHA durante il pagamento](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Customer Configuration]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL CAPTCHA]** sezione.

![Configurazione CAPTCHA del cliente](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enable CAPTCHA on Storefront]** a `Yes`. Quindi completare le altre opzioni come segue:

   - Inserisci il nome del **[!UICONTROL Font]** da utilizzare per i simboli CAPTCHA (impostazione predefinita: `LinLibertine`).

     Per aggiungere un font personalizzato, il file font deve trovarsi nella stessa directory dell’installazione di Commerce e deve essere dichiarato nel `config.xml` del modulo CAPTCHA.

   - Selezionare una delle opzioni seguenti **[!UICONTROL Forms]** dove deve essere utilizzato il CAPTCHA. Per scegliere più moduli, tenere premuto Ctrl (PC) o Comando (Mac).

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (vedere [patch di sicurezza](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _Knowledge Base_ articolo)
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source)
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)
      - `Create company` ![B2B per Adobe Commerce](../assets/b2b.svg) (Disponibile solo con B2B per Adobe Commerce)

   - Imposta **[!UICONTROL Displaying Mode]** a uno dei seguenti elementi:

      - `Always` — CAPTCHA è sempre necessario per accedere ai moduli selezionati.
      - `After number of attempts to login` — Immetti il numero di tentativi di accesso prima che venga visualizzato il CAPTCHA. Il valore 0 (zero) è simile a &quot;Sempre&quot;. Se questa opzione è selezionata, viene visualizzato il numero di tentativi di accesso non riusciti. Questa opzione non si applica al modulo Password dimenticata, che se attivato mostra sempre il CAPTCHA.

   - Per **[!UICONTROL Number of Unsuccessful Attempts to Login]**, inserisci il numero di volte in cui un cliente può effettuare l’accesso senza riuscirci prima che venga visualizzato il CAPTCHA. Se impostato su zero (`0`), CAPTCHA viene sempre utilizzato.

   - Per **[!UICONTROL CAPTCHA Timeout (minutes)]**, inserisci il numero di minuti prima della scadenza del CAPTCHA. Alla scadenza del CAPTCHA, il cliente deve ricaricare la pagina per generare un nuovo CAPTCHA.

   - Inserisci il **[!UICONTROL Number of Symbols]** nel CAPTCHA. Fino a otto (`8`) possono essere utilizzati. Per un numero variabile di simboli che cambiano con ogni CAPTCHA, inserisci un intervallo (ad esempio `5-8`).

   - Per **[!UICONTROL Symbols Used in CAPTCHA]**, immettere le lettere (a-z e A-Z) e i numeri (0-9) che si desidera visualizzare in modo casuale nel CAPTCHA. Il set di caratteri predefinito non include simboli simili, ad esempio `I` o `1`. Per ottenere risultati ottimali, utilizzare simboli facilmente identificabili dagli utenti.

   - Imposta **[!UICONTROL Case Sensitive]** a `Yes` se desideri richiedere ai clienti di inserire i caratteri in maiuscolo o minuscolo esattamente come mostrato nel CAPTCHA.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
