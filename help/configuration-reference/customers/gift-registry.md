---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Gift Registry]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Customers] &gt; [!UICONTROL Gift Registry] pagina dell’amministratore di Commerce.
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

Per informazioni dettagliate sull&#39;utilizzo di queste impostazioni per abilitare i registri regali per i clienti del tuo negozio, vedi [Configurare i registri dei regali](../../merchandising-promotions/gift-registry-configure.md). Per informazioni sull&#39;inclusione della ricerca nel registro regali nella vetrina, vedere [Aggiungi ricerca registro regali](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![Opzioni generali](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | Visualizzazione store | Determina se sono disponibili registri regali. Opzioni: <br/>**`Yes`**- Abilita i registri delle donazioni per la visualizzazione dello store selezionata. La scheda Registro regali viene visualizzata nel dashboard degli account dei clienti registrati.<br/>**`No`** - I registri dei regali non sono disponibili per la visualizzazione dello store. |
| [!UICONTROL Maximum Registrants] | Visualizzazione store | Imposta il numero di persone che un cliente può aggiungere a un registro regali. Il cliente condivide il registro dei regali con ogni dichiarante. Nella vetrina, il _Aggiungi registrante_ fino al raggiungimento del numero massimo. |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![Notifica proprietario](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Email Template] | Visualizzazione store | Determina il modello utilizzato per l&#39;e-mail di notifica del proprietario inviata quando viene creato un registro regali. Modello predefinito: Notifica proprietario registro regali |
| [!UICONTROL Email Sender] | Visualizzazione store | Identifica il [contatto store](../../getting-started/store-details.md#store-email-addresses) che viene visualizzato come mittente dell’e-mail di notifica al proprietario del registro dei regali. Valore predefinito: `General Contact` |

{style="table-layout:auto"}

## Condivisione registro regali

![Condivisione registro regali](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Email Template] | Visualizzazione store | Determina il modello utilizzato per l&#39;e-mail Condivisione registro regali inviata quando viene creato un registro regali. Quando il proprietario fa clic su _Condividi registro regali_, l’e-mail viene inviata a ciascun destinatario. Modello predefinito: `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | Visualizzazione store | Identifica il [contatto store](../../getting-started/store-details.md#store-email-addresses) che viene visualizzato come mittente dell’e-mail Condivisione registro regali. Valore predefinito: `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | Visualizzazione store | Numero massimo di messaggi di notifica e-mail di Condivisione del Registro regali che possono essere inviati contemporaneamente. |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![Aggiornamento registro regali](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Email Template] | Visualizzazione store | Determina il modello utilizzato per l&#39;e-mail di aggiornamento del registro regali inviata al proprietario del registro regali quando viene effettuato un acquisto dal registro regali. L&#39;aggiornamento include informazioni sull&#39;articolo e sulla quantità acquistata, ma non include il nome della persona che ha effettuato l&#39;ordine. Modello predefinito: `Gift Registry Update` |
| [!UICONTROL Email Sender] | Visualizzazione store | Identifica il [contatto store](../../getting-started/store-details.md#store-email-addresses) che viene visualizzato come mittente dell’e-mail di aggiornamento del registro dei regali. Valore predefinito: `General Contact` |

{style="table-layout:auto"}
