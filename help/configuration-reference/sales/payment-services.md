---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Payment Services]'
description: Rivedi le impostazioni di configurazione nella sezione [!UICONTROL Payment Services] della pagina [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] dell'amministratore di Commerce.
exl-id: 255b7bd8-1d32-4393-9eba-43dc7754c752
feature: Configuration, Payments
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]



Payment Services offre una soluzione self-service chiavi in mano, che include test sandbox e una configurazione semplice per fornire un’elaborazione dei pagamenti solida e sicura. Per ulteriori informazioni, vedere la [_Guida utente di Payment Services_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=it).

Per accedere alle impostazioni di configurazione per Payment Services, nella barra laterale _Amministratore_ vai a **[!UICONTROL Sales]** > **[!UICONTROL Payment Services]** e fai clic su **[!UICONTROL Settings]**.

![Impostazioni servizi di pagamento](assets/payment-services-menu-small.png){width="400"}

>[!NOTE]
>
>Per utilizzare la configurazione precedente invece di [Impostazioni](https://experienceleague.adobe.com/docs/commerce/payment-services/configure/settings.html?lang=it), vedere [Configurazione precedente](https://experienceleague.adobe.com/docs/commerce/payment-services/configure/configure-admin.html?lang=it).

## [!UICONTROL General]

![Impostazioni generali](assets/payments-general-settings.png){width="600" zoomable="yes"}

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|---|---|---|
| [!UICONTROL Enable] | sito web | Attiva o disattiva [!DNL Payment Services] per il tuo sito Web. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Payment mode] | visualizzazione store | Imposta il metodo o l’ambiente per lo store. Opzioni: [!UICONTROL Sandbox] / [!UICONTROL Production] |
| [!UICONTROL Sandbox Merchant ID] | visualizzazione store | L’ID venditore della sandbox, generato automaticamente durante l’onboarding della sandbox. |
| [!UICONTROL Production Merchant ID] | visualizzazione store | L’ID esercente di produzione, generato automaticamente durante l’onboarding della sandbox. |
| [!UICONTROL Soft Descriptor] | visualizzazione sito Web o store | Aggiungi un soft descriptor ai tuoi siti web e alle visualizzazioni dei negozi che fornisca informazioni sulle transazioni dei clienti e delinei marchi, negozi o linee di prodotti. L&#39;opzione [!UICONTROL Use website] applica qualsiasi soft descriptor aggiunto a livello di sito Web. L&#39;opzione [!UICONTROL Use default] applica qualsiasi descrittore soft aggiunto come predefinito. |

{style="table-layout:auto"}

## [!UICONTROL Credit card fields]

![Impostazioni campo carta di credito](assets/payments-ccfields-settings.png){width="600" zoomable="yes"}

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|---|---|---|
| [!UICONTROL Title] | visualizzazione store | Aggiungere il testo da visualizzare come titolo per questa opzione di pagamento nella vista Metodo di pagamento durante l&#39;estrazione. |
| [!UICONTROL Payment Action] | sito web | [azione di pagamento](payment-methods.md#payment-actions) per il metodo di pagamento specificato. Opzioni: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL 3DS Secure authentication] | sito web | Attiva o disattiva [3DS Secure Authentication](https://experienceleague.adobe.com/docs/commerce/payment-services/security-compliance/security.html?lang=it#3ds). Opzioni: [!UICONTROL Always] / [!UICONTROL When Required] / [!UICONTROL Off] |
| [!UICONTROL Show on checkout page] | sito web | Attiva o disattiva i campi della carta di credito da visualizzare nella pagina di pagamento. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Vault enabled] | visualizzazione store | Attiva o disattiva [il vaulting della carta di credito](https://experienceleague.adobe.com/docs/commerce/payment-services/payments-checkout/vaulting.html?lang=it). Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show vaulted payment methods in Admin] | visualizzazione store | Abilita o disabilita la possibilità di completare gli ordini per i clienti nell&#39;amministratore [utilizzando un metodo di pagamento con Vault](https://experienceleague.adobe.com/docs/commerce/payment-services/payments-checkout/vaulting.html?lang=it). Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | sito web | Attiva o disattiva la modalità di debug. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL Payment buttons]

![Impostazioni pulsanti di pagamento Paypal](assets/payments-ppbuttons-settings.png){width="600" zoomable="yes"}

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|---|---|---|
| [!UICONTROL Title] | visualizzazione store | Aggiungere il testo da visualizzare come titolo per questa opzione di pagamento nella visualizzazione Metodo di pagamento durante l&#39;estrazione. |
| [!UICONTROL Payment Action] | sito web | [azione di pagamento](payment-methods.md#payment-actions){target="_blank"} per il metodo di pagamento specificato. Opzioni: [!UICONTROL Authorize] / [!UICONTROL Authorize and Capture] |
| [!UICONTROL Show PayPal buttons on checkout page] | visualizzazione store | Attiva o disattiva [!DNL PayPal Smart Buttons] nella pagina di estrazione. Opzioni: [!UICONTROL &#x200B; Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on product detail page] | visualizzazione store | Attiva o disattiva [!DNL PayPal Smart Buttons] nella pagina dei dettagli del prodotto. Opzioni: [!UICONTROL &#x200B; Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons in mini-cart preview] | visualizzazione store | Attiva o disattiva [!DNL PayPal Smart Buttons] nell&#39;anteprima del mini-carrello. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal buttons on cart page] | visualizzazione store | Attiva o disattiva [!DNL PayPal Smart Buttons] nella pagina del carrello. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later button] | visualizzazione store | Abilita o disabilita l&#39;aspetto dell&#39;opzione di pagamento successivo in cui vengono visualizzati i pulsanti di pagamento. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Pay Later Message] | sito web | Abilita o disabilita la funzione di messaggistica Paga più tardi nel carrello, nella pagina del prodotto, nel mini-carrello e durante il flusso di pagamento. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Venmo button] | visualizzazione store | Abilita o disabilita l&#39;opzione di pagamento Venmo in cui sono visualizzati i pulsanti di pagamento. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show Apple Pay button] | visualizzazione store | Abilita o disabilita l&#39;opzione di pagamento Apple Pay in cui sono visualizzati i pulsanti di pagamento. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show PayPal Credit and Debit card button] | visualizzazione store | Abilita o disabilita l&#39;opzione di pagamento con carta di credito e debito in cui sono visualizzati i pulsanti di pagamento. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Debug Mode] | sito web | Attiva o disattiva la modalità di debug. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |

{style="table-layout:auto"}

## [!UICONTROL PayPal Smart Button Styling]

![Impostazioni di stile dei pulsanti di pagamento Paypal](assets/payments-buttonstyle-settings.png){width="600" zoomable="yes"}

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Layout] | Visualizzazione store | Consente di definire lo stile del layout dei pulsanti di pagamento. Opzioni: [!UICONTROL Vertical] / [!UICONTROL Horizontal] |
| [!UICONTROL Tagline] | Visualizzazione store | Attiva/disattiva tagline. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Color] | Visualizzazione store | Definire il colore dei pulsanti di pagamento. Opzioni: [!UICONTROL Blue] / [!UICONTROL Gold] / [!UICONTROL Silver] / [!UICONTROL White] / [!UICONTROL Black] |
| [!UICONTROL Shape] | Visualizzazione store | Definire la forma dei pulsanti di pagamento. Opzioni: [!UICONTROL Rectangular] / [!UICONTROL Pill] |
| [!UICONTROL Responsive Button Height] | Visualizzazione store | Definisce se i pulsanti di pagamento utilizzano un&#39;altezza predefinita. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Height] | Visualizzazione store | Definire l&#39;altezza dei pulsanti di pagamento. Valore predefinito: nessuno |
| [!UICONTROL Label] | Visualizzazione store | Definire l&#39;etichetta visualizzata nei pulsanti di pagamento. Opzioni: [!UICONTROL PayPal] / [!UICONTROL Checkout] / [!UICONTROL Buynow] / [!UICONTROL Pay] / [!UICONTROL Installment] |

{style="table-layout:auto"}
