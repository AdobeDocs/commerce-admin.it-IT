---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Customers] &gt; [!UICONTROL Promotions] dell'amministratore di Commerce.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![Regole promemoria e-mail automatizzati](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://docs.magento.com/user-guide/marketing/email-reminder-rules-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | Globale | Abilita i promemoria e-mail automatizzati. Se questa opzione è impostata su No, le altre impostazioni vengono ignorate. Opzioni: `Yes` / `No` |
| [!UICONTROL Frequency] | Globale | Indica la frequenza con cui Commerce deve verificare la presenza di nuovi clienti idonei per i promemoria e-mail automatizzati. Opzioni: <br/>**`Minute Intervals`**- Invia l&#39;e-mail in base all&#39;intervallo selezionato. (5 minuti, 10 minuti, 15 minuti, 20 minuti o 30 minuti)<br/>**`Hourly`** - Invia e-mail ogni ora, al minuto successivo all&#39;ora specificata. Immettere un valore compreso tra 0 e 59. <br/>**`Daily`**- Invia e-mail ogni giorno, dall&#39;ora di inizio. |
| [!UICONTROL Interval] | Globale | L’intervallo deve essere uguale o maggiore del periodo di avvio di cron.php. Opzioni: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | Globale | Imposta il giorno, il minuto e il secondo in cui l’e-mail viene inviata. Specificato in formato 24 ore, in base all&#39;ora di sistema sul server. |
| [!UICONTROL Maximum Emails per One Run] | Globale | Limita il numero di e-mail inviate in un blocco pianificato. |
| [!UICONTROL Email Send Failure Threshold] | Globale | Il numero di volte in cui il promemoria tenta di inviare notifiche a un indirizzo e-mail specifico e ha esito negativo. Quando il valore è impostato su 0, non esiste una soglia e le notifiche continuano a essere inviate nonostante eventuali errori. |
| [!UICONTROL Reminder Email Sender] | Visualizzazione store | L’identità dell’archivio visualizzata come mittente dell’e-mail. |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![Codici coupon specifici generati automaticamente](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://docs.magento.com/user-guide/marketing/price-rules-cart-coupon-code-configure.md  -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Code Length] | Globale | Definisce la lunghezza del codice coupon, esclusi prefisso, suffisso e separatori. |
| [!UICONTROL Code Format] | Globale | Definisce il formato del codice coupon. Le opzioni includono: <br/>**`Alphanumeric`**- Qualsiasi combinazione di lettere e numeri.<br/>**`Alphabetical`** - Solo lettere. <br/>**`Numeric`**- Solo numeri. |
| [!UICONTROL Code Prefix] | Globale | Valore aggiunto all&#39;inizio di tutti i codici coupon. Se non desideri utilizzare un prefisso, lascia vuoto il campo. |
| [!UICONTROL Code Suffix] | Globale | Valore aggiunto alla fine di tutti i codici. Se non desideri utilizzare un suffisso, lascia vuoto il campo. |
| [!UICONTROL Dash Every X Characters] | Globale | Intervallo di inserimento di un trattino (-) in tutti i codici coupon. Se non desideri utilizzare un trattino, lascia vuoto il campo. <br/>_**Nota:**_ i codici coupon che differiscono solo di un trattino sono considerati codici diversi. |

{style="table-layout:auto"}
