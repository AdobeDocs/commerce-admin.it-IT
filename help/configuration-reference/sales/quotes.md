---
title: '[!UICONTROL Sales] > [!UICONTROL Quotes]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Sales] > [!UICONTROL Quotes] dell'amministratore di Commerce.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
TQID: https://experienceleague.adobe.com/puZjB2YCCyZXT0U6AdDBd-YjxopU637-yxgOaB6hkvM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Con l’installazione e l’abilitazione di Adobe Commerce B2B, l’esperienza di acquisto può essere personalizzata con funzioni specifiche per l’azienda. Adobe Commerce B2B è una soluzione integrata che supporta sia i modelli B2B che B2C. Per ulteriori informazioni sulle funzionalità B2B, consulta la [Guida utente di Adobe Commerce B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=it).

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/it/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![Generale](./assets/quotes-general.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | Sito Web | La quantità minima del subtotale del carrello, dopo eventuali sconti, necessaria prima che un cliente possa inviare una richiesta di preventivo. Valore predefinito: `0` |
| [!UICONTROL Minimum Amount Message] | Visualizzazione store | Il messaggio visualizzato nel carrello quando un cliente tenta di inviare una richiesta di preventivo, ma l’importo minimo richiesto non viene raggiunto. |
| [!UICONTROL Default Expiration Period] | Sito Web | Determina la durata predefinita di un [preventivo](../../b2b/quote-price-negotiation.md) come periodo di tempo a partire dalla data di invio della richiesta di preventivo. Opzioni: `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![File allegati](./assets/quotes-attached-files.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | Globale | Determina i formati di file che possono essere allegati a un&#39;offerta. Valori predefiniti supportati: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` e `jpeg` |
| [!UICONTROL Maximum file size] | Globale | Determina la dimensione massima di un file allegato a un&#39;offerta. Questa impostazione può essere ignorata dalla configurazione del server. |

{style="table-layout:auto"}
