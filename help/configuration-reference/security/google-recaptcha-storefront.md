---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] pagina dell’amministratore di Commerce.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Prima di configurare Google reCAPTCHA, è necessario assicurarsi che il `PHP.ini` Il file include le seguenti impostazioni: `allow_url_fopen = 1`. Questo potrebbe richiedere l’assistenza dello sviluppatore. Consulta [Impostazioni PHP](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) nel _Guida all’installazione_.

{{config}}

Per ulteriori informazioni sull&#39;utilizzo di Google reCAPTCHA per proteggere il tuo negozio, consulta Google [reCAPTCHA](../../systems/security-google-recaptcha.md) nel _Guida ai sistemi di amministrazione_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2 (&quot;Io non sono un robot&quot;)](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--|--|--|
| [!UICONTROL Google API Website Key] | Sito Web | Chiave del sito Web creata al momento della registrazione dell&#39;account Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Sito Web | La chiave segreta associata al tuo account Google reCAPTCHA. |
| [!UICONTROL Size] | Sito Web | La dimensione della casella Google reCAPTCHA che viene visualizzata quando un cliente accede al proprio account. Opzioni: `Normal` (impostazione predefinita) / `Compact` |
| [!UICONTROL Theme] | Sito Web | Determina lo stile della casella Google reCAPTCHA. Opzioni: `Light Theme` (impostazione predefinita) / `Dark Theme` |
| [!UICONTROL Language Code] | Visualizzazione store | Il [codice a due caratteri](https://developers.google.com/recaptcha/docs/language) specifica la lingua utilizzata per il testo e i messaggi reCAPTCHA di Google. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 Invisibile](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--|--|--|
| [!UICONTROL Google API Website Key] | Sito Web | Chiave del sito Web creata al momento della registrazione dell&#39;account Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Sito Web | La chiave segreta associata al tuo account Google reCAPTCHA. |
| [!UICONTROL Invisible Badge Position] | Sito Web | La posizione del badge reCAPTCHA invisibile su ogni pagina. Opzioni: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Globale | Determina lo stile della casella Google reCAPTCHA. Opzioni: `Light Theme` (impostazione predefinita) / `Dark Theme` |
| [!UICONTROL Language Code] | Visualizzazione store | A [codice a due caratteri](https://developers.google.com/recaptcha/docs/language) specifica la lingua utilizzata per il testo e i messaggi reCAPTCHA di Google. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 Invisibile](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--|--|--|
| [!UICONTROL Google API Website Key] | Sito Web | Chiave del sito Web creata al momento della registrazione dell&#39;account Google reCAPTCHA. |
| [!UICONTROL Google API Secret Key] | Sito Web | La chiave segreta associata al tuo account Google reCAPTCHA. |
| [!UICONTROL Minimum Score Threshold] | Globale | Punteggio minimo che identifica un’interazione dell’utente come rischio potenziale, dove 1,0 è una tipica interazione dell’utente e 0,0 è probabilmente un bot. Predefinito: `0.5` |
| [!UICONTROL Invisible Badge Position] | Sito Web | La posizione del badge reCAPTCHA invisibile su ogni pagina. Opzioni: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | Sito Web | Determina lo stile della casella Google reCAPTCHA. Opzioni: `Light Theme` (impostazione predefinita) / `Dark Theme` |
| [!UICONTROL Language Code] | Visualizzazione store | A [codice a due caratteri](https://developers.google.com/recaptcha/docs/language) specifica la lingua utilizzata per il testo e i messaggi reCAPTCHA di Google. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA Failure Messages]

![Messaggi di errore](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | Visualizzazione store | Messaggio visualizzato nella vetrina se la verifica non riesce. Testo predefinito: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | Visualizzazione store | Messaggio visualizzato nella vetrina se reCAPTCHA non restituisce un risultato di verifica. Testo predefinito: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Storefront]

![Vetrina](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>Il tipo reCAPTCHA scelto deve corrispondere al tipo associato alla chiave API dell’account Google reCAPTCHA.

>[!WARNING]
>
>Quando si utilizza reCAPTCHA versione 3, un utente autentico con un punteggio basso non può procedere. Per la versione 2, un utente autentico con un punteggio basso riceve una sfida. Valuta attentamente se gli utenti autentici con un punteggio basso devono avere l’opportunità di risolvere un problema (versione 2) o essere bloccati (versione 3).

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato quando i clienti [accedi](../../customers/customer-sign-in.md) ai loro conti. Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida la richiesta di accesso.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Forgot Password] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato quando i clienti richiedono un [reimpostazione password](../../customers/password-reset.md). Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida la richiesta di reimpostazione della password.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Create New Customer Account] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato quando il cliente si registra per un [nuovo account](../../customers/account-create.md). Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida la richiesta dell&#39;account.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Edit Customer Account] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato quando il cliente modifica il proprio [informazioni account](../../customers/account-dashboard-account-information.md). Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida la richiesta dell&#39;account.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Create New Company Account] | Sito Web | ![B2B per Adobe Commerce](../../assets/b2b.svg) (Disponibile solo con B2B per Adobe Commerce) Specifica il tipo di reCAPTCHA utilizzato quando viene [account società](../../b2b/account-company-create.md) viene creato. Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida la richiesta dell&#39;account.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Contact Us] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato per inviare un messaggio da [Contattaci](../../getting-started/store-details.md#contact-us-form) pagina del tuo negozio. Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida la richiesta del messaggio.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Product Review] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato quando i clienti inviano un [recensione prodotto](../../merchandising-promotions/product-reviews.md). Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida la richiesta di revisione del prodotto.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Newsletter Subscription] | Sito Web | Specifica il tipo di reCAPTCHA invisibile utilizzato quando i clienti si registrano a [abbonamento a newsletter](../../merchandising-promotions/newsletter-subscribers.md). Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida la richiesta di abbonamento alla newsletter.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Gift Card] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo per Adobe Commerce) Specifica il tipo di reCAPTCHA utilizzato quando i clienti immettono un [gift card](../../catalog/product-gift-card-create.md) codice. Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida l&#39;invio del codice gift card.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Invitation Create Account] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato quando i clienti inviano la creazione di un account [invito](../../merchandising-promotions/invitations.md) codice. Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida l&#39;invio dell&#39;e-mail di invito.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Send to Friend] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato quando i clienti [condividere un prodotto](../../stores-purchase/email-a-friend.md) con un amico. Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida l’invio dell’e-mail.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Wishlist Sharing] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato quando i clienti [condividere una lista dei desideri](../../stores-purchase/wishlist-storefront.md#share-the-wish-list). Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida l’invio del messaggio e dell’e-mail.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for Coupon Codes] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato quando i clienti immettono un [codice coupon](../../merchandising-promotions/price-rules-cart-coupon.md). Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida l’invio del codice coupon.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | Sito Web | Specifica il tipo di reCAPTCHA utilizzato quando i clienti pagano per un acquisto con [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md). Opzioni:<br/>**`No`**- (impostazione predefinita) Non convalida la richiesta di reimpostazione della password.<br />**`reCAPTCHA v2 ("I am not a robot")`** - Richiede all&#39;utente di selezionare _Io non sono un robot_ casella di controllo.<br />**`Invisible reCAPTCHA v2`**: convalida il comportamento dell’utente in background senza richiedere interazioni in base al punteggio.<br/>**`Invisible reCAPTCHA v3`** - (Consigliato) Convalida il comportamento dell’utente in background in base al punteggio di interazione. |

{:style=&quot;table-layout:auto&quot;}
