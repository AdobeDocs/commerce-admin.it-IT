---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payments Standard]'
description: Rivedi le impostazioni di configurazione nella sezione [!UICONTROL PayPal Payments Standard] della pagina [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] dell'amministratore di Commerce.
exl-id: 846d9b6f-92b9-4610-b894-625f67f4cff8
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1291'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Standard]

>[!IMPORTANT]
>
>**Requisiti PSD2:**<br/>
>A partire dal 14 settembre 2019, le banche europee potrebbero rifiutare i pagamenti che non soddisfano i requisiti di [PSD2](../../getting-started/compliance-payment-services-directive.md). Nessuna azione necessaria per [!DNL PayPal Payments Standard] per conformarsi a PSD2 perché tutti i requisiti sono gestiti da PayPal.

{{config}}

## [!UICONTROL Required Settings]

![Impostazioni richieste](./assets/payment-methods-paypal-payments-standard-required.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Sito Web | (Facoltativo) Tutti gli indirizzi e-mail associati al tuo conto PayPal per esercenti. Gli indirizzi e-mail fanno distinzione tra maiuscole e minuscole e devono corrispondere esattamente agli indirizzi presenti nel tuo account. |
| [!UICONTROL Partner] | Sito Web | Il tuo ID Partner PayPal, se applicabile. |
| [!UICONTROL Vendor] | Sito Web | Il nome di accesso dell&#39;utente PayPal. |
| Utente | Sito Web | ID di un altro utente sul tuo conto PayPal. |
| [!UICONTROL Password] | Sito Web | La password associata al tuo conto PayPal per esercenti. |
| [!UICONTROL Test Mode] | Sito Web | Se abilitata, esegue PayPal Payments Pro in un ambiente di test. Disattiva la modalità di test quando sei pronto per andare &quot;live&quot; in modalità di produzione. Opzioni: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Sito Web | Un proxy può essere utilizzato per reindirizzare il traffico quando il firewall del server impedisce l&#39;accesso diretto al server PayPal. Se applicabile, identifica il server proxy utilizzato per stabilire la connessione con il server PayPal. Opzioni: `Yes` / `No` <br/><br/>Se attivata, impostare le opzioni: <br/>**`Proxy Host`**- Indirizzo IP dell&#39;host proxy.<br/>**`Proxy Port`** - Numero della porta proxy. |
| [!UICONTROL Enable this Solution] | Sito Web | Determina se PayPal Payments Pro è disponibile per i clienti come metodo di pagamento. |
| [!UICONTROL Enable PayPal Credit] | Sito Web | Determina se PayPal Credit è disponibile per i clienti come opzione di pagamento. |

{style="table-layout:auto"}

## Pubblicizza credito PayPal

![Pubblicizza credito PayPal](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Sito Web | L&#39;ID editore associato al tuo conto PayPal Credit. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Recupera l&#39;ID editore da PayPal. |
| [!UICONTROL Home Page] | Sito Web | Determina la posizione e le dimensioni del banner [!DNL PayPal Credit] nella home page. Opzioni: <br/>**`Display`**- Determina se un banner [!DNL PayPal Credit] viene visualizzato nella home page dell&#39;archivio. Opzioni: `Yes` / `No`<br/>**`Position`** - Determina la posizione del banner [!DNL PayPal Credit] nella home page. Opzioni: `Header (center)` / `Sidebar (right)` <br/>**`Size`**- Determina le dimensioni del banner [!DNL PayPal Credit] nella home page. Opzioni: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Sito Web | Determina la posizione e le dimensioni del banner [!DNL PayPal Credit] nelle pagine delle categorie. Opzioni: (come per [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Sito Web | Determina la posizione e le dimensioni del banner [!DNL PayPal Credit] nelle pagine dei prodotti. Opzioni: (come per [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Sito Web | Determina la posizione e le dimensioni del banner [!DNL PayPal Credit] sulla pagina del carrello. Opzioni: (come per [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payments Standard]

![Impostazioni di base](./assets/paypal-standard-basic-settings.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Title] | Visualizzazione store | Un nome che identifica PayPal Payments Pro come metodo di pagamento durante il pagamento. |
| [!UICONTROL Sort Order] | Visualizzazione store | Numero che determina l&#39;ordine di visualizzazione di PayPal Payments Pro quando viene elencato con altri metodi di pagamento durante il pagamento. |
| [!UICONTROL Payment Action] | Sito Web | Determina l&#39;azione intrapresa da PayPal quando un ordine viene inviato. Opzioni: <br/>**`Authorization`**- Approva l&#39;acquisto, ma blocca i fondi. L&#39;importo non viene prelevato fino a quando non viene &quot;catturato&quot; dal mercante.<br/>**`Sale`** - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente ritirato dal conto del cliente. |
| [!UICONTROL Credit Card Settings] |  |  |
| [!UICONTROL Allowed Credit Cart Types] | Sito Web | Determina le carte di credito disponibili per i clienti durante il pagamento. Seleziona ogni scheda supportata. Opzioni: `American Express` (richiede un contratto aggiuntivo) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![Impostazioni avanzate](./assets/payment-methods-paypal-payment-standard-advanced.png)<!-- zoom -->

| Campo | Ambito | Descrizione |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Visualizzazione store | Determina se PayPal Express Checkout viene visualizzato come opzione di pagamento nel carrello. Opzioni: `Yes` (consigliato) / `No` |
| [!UICONTROL Payment Action Applicable From] | Sito Web | Determina l&#39;intervallo della selezione paese applicabile. Opzioni: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Sito Web | Identifica ogni paese dal quale il pagamento è accettato. Solo i clienti con un indirizzo di fatturazione in un paese selezionato possono effettuare acquisti con questo metodo di pagamento. |
| [!UICONTROL Debug Mode] | Sito Web | Registra i messaggi inviati tra il tuo negozio e il sistema di pagamento PayPal in un file di registro. Opzioni: `Yes` / `No` <br/><br/>**_Nota:_**&#x200B;Il file di registro è archiviato nel server ed è accessibile solo agli sviluppatori. In conformità agli standard di sicurezza dei dati PCI, le informazioni sulla carta di credito non vengono registrate nel file di registro. |
| [!UICONTROL Enable SSL Verification] | Sito Web | Abilita la verifica del certificato di sicurezza host. Opzioni: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Sito Web | Visualizza un riepilogo completo delle righe presenti nel carrello del cliente sul sito PayPal. Opzioni: `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | Sito Web | Include fino a dieci opzioni di spedizione sul sito PayPal. Opzioni: `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | Visualizzazione store | Determina il tipo di immagine utilizzata per il pulsante di accettazione PayPal. Opzioni: <br/>**`Dynamic`**- (Consigliato) Visualizza un&#39;immagine che può essere modificata dinamicamente dal server PayPal.<br/>**`Static`** - Visualizza un&#39;immagine statica che non può essere modificata dinamicamente. |
| [!UICONTROL Enable PayPal Guest Checkout] | Sito Web | Consente ai clienti che non dispongono di un conto PayPal di effettuare acquisti con PayPal Express Checkout. Opzioni: `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | Sito Web | Determina se l&#39;indirizzo di fatturazione del cliente è obbligatorio. Opzioni: `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | Sito Web | Determina se i clienti possono stipulare un [contratto di fatturazione](../../stores-purchase/paypal-billing-agreements.md) con lo store. Opzioni: <br/>**`Auto`**- Il cliente può iscriversi a un contratto di fatturazione durante il pagamento rapido.<br/>**`Ask Customer`** - Al cliente viene chiesto se desidera iscriversi a un contratto di fatturazione. <br/>**`Never`**- Ai clienti non viene offerta la possibilità di iscriversi a un contratto di fatturazione. |
| [!UICONTROL Skip Order Review Step] | Sito Web | Determina se i clienti possono completare la transazione dal sito PayPal o se devono tornare al tuo negozio e completare il passaggio di revisione dell&#39;ordine prima di sottomettere l&#39;ordine. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Billing Agreement Setting]

![Impostazioni contratto di fatturazione](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| Campo | Ambito | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Sito Web | Quando questa opzione è abilitata, gli accordi di fatturazione vengono visualizzati ai clienti come opzione di pagamento durante il pagamento. Opzioni: `Yes` / `No` |
| [!UICONTROL Title] | Visualizzazione store | Etichetta per l&#39;opzione di contratto di fatturazione PayPal visualizzata come opzione di pagamento durante il pagamento. |
| [!UICONTROL Sort Order] | Visualizzazione store | Determina l&#39;ordine in cui gli accordi di fatturazione vengono elencati con altri metodi di pagamento durante il pagamento. |
| [!UICONTROL Payment Action] | Sito Web | Determina il modo in cui PayPal gestisce la transazione: Opzioni: <br/>**`Authorization`**- Approva l&#39;acquisto, ma blocca i fondi. L&#39;importo non viene prelevato fino a quando non viene &quot;catturato&quot; dal mercante.<br/>**`Sale`** - L&#39;importo dell&#39;acquisto è autorizzato e immediatamente ritirato dal conto del cliente. |
| [!UICONTROL Payment Applicable From] | Sito Web | Determina l&#39;intervallo della selezione paese applicabile. Opzioni: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Sito Web | Identifica ogni paese dal quale il pagamento è accettato. Solo i clienti con un indirizzo di fatturazione in un paese selezionato possono effettuare acquisti con questo metodo di pagamento. |
| [!UICONTROL Debug Mode] | Sito Web | Registra la comunicazione con il sistema di pagamento in un file di registro. Opzioni: `Yes` / `No` <br/><br/>**_Nota:_**&#x200B;Il file di registro è archiviato nel server ed è accessibile solo agli sviluppatori. In conformità agli standard di sicurezza dei dati PCI, le informazioni sulla carta di credito non vengono registrate nel file di registro. |
| [!UICONTROL Enable SSL Verification] | Sito Web | Abilita un passaggio di verifica su per garantire che la transazione avvenga su un canale SSL crittografato. Opzioni: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Sito Web | Quando questa opzione è attivata, visualizza un riepilogo delle righe del carrello nella pagina dei pagamenti di PayPal. Opzioni: `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | Sito Web | Quando questa opzione è abilitata, i clienti possono avviare un contratto di fatturazione dal dashboard del proprio account cliente. |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![Impostazioni report liquidazione](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Login] | Sito Web | Il nome utente necessario per accedere al server FTP protetto di PayPal. |
| [!UICONTROL Password] | Sito Web | La password necessaria per accedere al server FTP protetto di PayPal. |
| [!UICONTROL Sandbox Mode] | Sito Web | Se abilitata, esegue i rapporti in un ambiente di test prima di &quot;andare live&quot; nell’ambiente di produzione. Opzioni: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Sito Web | URL in cui vengono gestiti i report di liquidazione. Valore predefinito: `reports.paypal.com` |
| [!UICONTROL Custom Path] | Sito Web | Percorso in cui vengono salvati i report di liquidazione sul server. Valore predefinito: `/ppreports/outgoing` |
| [!UICONTROL Scheduled Fetching] |  |  |
| [!UICONTROL Enable Automatic Fetching] | Sito Web | Quando questa opzione è abilitata, recupera automaticamente i rapporti di liquidazione secondo programma. Opzioni: `Yes` / `No` |
| [!UICONTROL Schedule] | Globale | Determina la frequenza con cui i rapporti di liquidazione vengono generati da PayPal. Opzioni: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Globale | Determina l&#39;ora, il minuto e il secondo in cui vengono generati i rapporti di liquidazione. |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![Impostazioni esperienza front-end](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Visualizzazione store | Determina il logo PayPal visualizzato nel tuo Negozio. Ci sono quattro stili di base in due dimensioni. Opzioni: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| [!UICONTROL PayPal Merchant Pages Style] |  |  |
| [!UICONTROL Page Style] | Visualizzazione store | Determina l&#39;aspetto della pagina del venditore PayPal. Valori consentiti: <br/>**`paypal`**- Utilizza lo stile di pagina PayPal.<br/>**`primary`** - Utilizza lo stile di pagina identificato come stile &quot;principale&quot; nel profilo dell&#39;account. <br/>**`your_custom_value`**- Utilizza uno stile di pagina di pagamento personalizzato, specificato nel profilo del tuo account. |
| [!UICONTROL Header Image URL] | Visualizzazione store | URL dell&#39;immagine visualizzato nell&#39;angolo superiore sinistro della pagina di pagamento. La dimensione massima è 750 x 90 pixel. <br/><br/>**_Nota:_**&#x200B;PayPal consiglia di memorizzare l&#39;immagine in un server protetto (https). In caso contrario, il browser del cliente potrebbe avvertire che &quot;la pagina contiene sia elementi protetti che non protetti&quot;. |
| [!UICONTROL Header Image Background Color] | Visualizzazione store | Codice di sei caratteri [colore esadecimale](https://en.wikipedia.org/wiki/Web_colors) per il colore di sfondo dell&#39;intestazione nella pagina di estrazione. È possibile immettere il codice in lettere maiuscole e minuscole. |
| [!UICONTROL Header Image Border Color] | Visualizzazione store | Codice di colore esadecimale a sei caratteri per il bordo di due pixel attorno all&#39;intestazione. |
| [!UICONTROL Page Background Color] | Visualizzazione store | Codice di colore esadecimale a sei caratteri per il colore di sfondo della pagina di pagamento visualizzato dietro l&#39;intestazione e il modulo di pagamento. |

{style="table-layout:auto"}
