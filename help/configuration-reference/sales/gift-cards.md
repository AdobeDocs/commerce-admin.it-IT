---
title: '[!UICONTROL Sales] > [!UICONTROL Gift Cards]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Sales] > [!UICONTROL Gift Cards] dell'amministratore di Commerce.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
TQID: https://experienceleague.adobe.com/J-VH-mdaM7HrMRHJMNmmbBPggm1hjtHHWTh3q-5en0w
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: d9ced453-36f4-4eb5-b2f3-1d593e32476b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![Impostazioni e-mail gift card](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | Visualizzazione store | Identifica il [contatto store](../../getting-started/store-details.md#store-email-addresses) che viene visualizzato come mittente dell&#39;e-mail di notifica gift card. Valore predefinito: `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | Visualizzazione store | Determina il [modello](../../systems/email-templates.md) utilizzato per l&#39;e-mail di notifica gift card. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![Impostazioni generali gift card](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Redeemable] | Globale | Determina se il titolare della gift card può riscattare il proprio valore in contanti. Opzioni: `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | Globale | Determina il numero di giorni di validità della scheda. Se lasciata vuota, la scheda non scade. <br/><br/>**_Importante:_** In alcuni casi non è consentito impostare dati di scadenza sulle gift card. Controlla le leggi locali prima di impostare una vita per le tue carte regalo. |
| [!UICONTROL Allow Gift Message] | Visualizzazione store | Determina se l&#39;opzione per includere un messaggio regalo è disponibile per i clienti che acquistano una gift card. Opzioni: `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | Visualizzazione store | Determina il numero massimo di caratteri consentiti in un messaggio gift card. Valore predefinito: 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | Globale | Determina se viene generato un conto gift card quando un cliente effettua un ordine o quando l&#39;ordine viene fatturato. Opzioni: `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![E-mail inviata dalla gestione account gift card](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | Visualizzazione store | Identifica il [contatto store](../../getting-started/store-details.md#store-email-addresses) che viene visualizzato come mittente dell&#39;e-mail gift card. Valore predefinito: `General Contact` |
| [!UICONTROL Gift Card Template] | Visualizzazione store | Determina il [modello](../../systems/email-templates.md) utilizzato per l&#39;e-mail gift card. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![Impostazioni generali account gift card](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Code Length] | Globale | Determina la lunghezza del codice gift card. |
| [!UICONTROL Code Format] | Globale | Determina il formato del codice gift card. Opzioni: `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | Globale | Definisce qualsiasi prefisso aggiunto all&#39;inizio del codice. |
| [!UICONTROL Code Suffix] | Globale | Definisce qualsiasi suffisso aggiunto alla fine del codice. |
| [!UICONTROL Dash Every X Characters] | Globale | Se si desidera includere trattini nel codice, determina il numero di caratteri tra ogni trattino. |
| [!UICONTROL New Pool Size] | Globale | Determina la dimensione del nuovo pool di codici da generare. |
| [!UICONTROL Low Code Pool Threshold] | Globale | Determina il numero di record nel pool di codice che attivano un avviso per segnalare che il pool deve essere rifornito. |
| [!UICONTROL Generate] | Globale | Fare clic per generare l&#39;elenco dei codici gift card. |

{style="table-layout:auto"}
