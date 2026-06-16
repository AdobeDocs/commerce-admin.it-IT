---
title: '[!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]'
description: Rivedi le impostazioni di configurazione nella sezione [!UICONTROL Payment Services] della pagina [!UICONTROL Sales] > [!UICONTROL Payment Methods] dell'amministratore di Commerce.
exl-id: 255b7bd8-1d32-4393-9eba-43dc7754c752
feature: Configuration, Payments
TQID: https://experienceleague.adobe.com/lTYf9W1u7bIxNzypWBj20Eo42VPShCmL-qLwSAmJ8a0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 575
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Payment Services]



Payment Services offre una soluzione self-service chiavi in mano, che include test sandbox e una configurazione semplice per fornire un’elaborazione dei pagamenti solida e sicura. Per ulteriori informazioni, vedere la [_Guida utente di Payment Services_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html).

Per accedere alle impostazioni di configurazione per Payment Services, nella barra laterale _Amministratore_ vai a **[!UICONTROL Sales]** > **[!UICONTROL Payment Services]** e fai clic su **[!UICONTROL Settings]**.

![Impostazioni servizi di pagamento](assets/payment-services-menu-small.png){width="400"}

>[!NOTE]
>
>Per utilizzare la configurazione precedente invece di [Impostazioni](https://experienceleague.adobe.com/docs/commerce/payment-services/configure/settings.html), vedere [Configurazione precedente](https://experienceleague.adobe.com/docs/commerce/payment-services/configure/configure-admin.html).

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
| [!UICONTROL 3DS Secure authentication] | sito web | Attiva o disattiva [3DS Secure Authentication](https://experienceleague.adobe.com/docs/commerce/payment-services/security-compliance/security.html#3ds). Opzioni: [!UICONTROL Always] / [!UICONTROL When Required] / [!UICONTROL Off] |
| [!UICONTROL Show on checkout page] | sito web | Attiva o disattiva i campi della carta di credito da visualizzare nella pagina di pagamento. Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Vault enabled] | visualizzazione store | Attiva o disattiva [il vaulting della carta di credito](https://experienceleague.adobe.com/docs/commerce/payment-services/payments-checkout/vaulting.html). Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
| [!UICONTROL Show vaulted payment methods in Admin] | visualizzazione store | Abilita o disabilita la possibilità di completare gli ordini per i clienti nell&#39;amministratore [utilizzando un metodo di pagamento con Vault](https://experienceleague.adobe.com/docs/commerce/payment-services/payments-checkout/vaulting.html). Opzioni: [!UICONTROL Yes] / [!UICONTROL No] |
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
