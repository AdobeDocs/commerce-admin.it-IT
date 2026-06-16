---
title: '[!UICONTROL General] > [!UICONTROL B2B Features]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL General] > [!UICONTROL B2B Features] dell'amministratore di Commerce.
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
TQID: https://experienceleague.adobe.com/s9-xEtVsEhdegXaObYrfbu-tSvvcqlXVagEw4QJejlk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 347
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Con l’installazione e l’abilitazione di Adobe Commerce B2B, l’esperienza di acquisto può essere personalizzata con funzioni specifiche per l’azienda. Adobe Commerce B2B è una soluzione integrata che supporta sia i modelli B2B che B2C. Per ulteriori informazioni sulle funzionalità B2B, consulta la [_Guida utente di Adobe Commerce B2B_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## [!UICONTROL B2B Features]

![Funzionalità B2B](./assets/b2b-features.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | Sito Web | Quando questa opzione è attivata, consente ai clienti di gestire l’assegnazione della società dal dashboard account e abilita le funzioni Catalogo condiviso e Offerta B2B per impostazione predefinita. Opzioni: `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | Sito Web | Se questa opzione è abilitata, consente ai clienti e agli ospiti di effettuare rapidamente gli ordini in base allo SKU o al nome del prodotto. Opzioni: `Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | Sito Web | Quando questa opzione è attivata, consente ai clienti di creare e gestire gli elenchi delle richieste di acquisto dal dashboard dei conti. |

{style="table-layout:auto"}

![Funzionalità B2B con aziende e cataloghi condivisi abilitati](./assets/b2b-features-company-enabled.png)<!-- zoom -->

Quando la funzione Società è abilitata, sono disponibili campi aggiuntivi per il catalogo condiviso e il preventivo B2B.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | Sito Web | Se abilitata, consente di creare cataloghi curati con prezzi personalizzati disponibili a livello globale o limitati a specifiche aziende. Opzioni: `Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | Sito Web | Quando il campo _[!UICONTROL Enable Shared Catalog]_è impostato su `Yes`, questa opzione è disponibile. Quando questa opzione è attivata, solo i prodotti assegnati a un catalogo condiviso vengono memorizzati nell&#39;indice dei prezzi. I prodotti non assegnati al catalogo condiviso non vengono visualizzati nella vetrina. Opzioni: `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | Sito Web | Quando questa opzione è attivata, consente agli acquirenti aziendali di inviare una richiesta di preventivo dal carrello. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Payment Methods]

![Configurazione B2B - impostazioni metodo di pagamento predefinito](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Payment Methods] | Globale | Determina la selezione dei metodi di pagamento disponibili per gli acquirenti B2B. Opzioni: `All Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | Globale | Specifica ogni metodo di pagamento disponibile per gli acquirenti B2B. |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Shipping Methods]

![Configurazione B2B - metodi di spedizione predefiniti](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Shipping Methods] | Globale | Determina la selezione dei metodi di spedizione disponibili per impostazione predefinita per gli acquirenti B2B. Opzioni: `All Shipping Methods` / `Specific Shipping Methods` |
| [!UICONTROL Shipping Methods] | Globale | Specifica ogni metodo di spedizione disponibile per impostazione predefinita per gli acquirenti B2B. <br/>**_Note:_** Puoi anche limitare i metodi di spedizione per un [account aziendale](../../b2b/account-companies.md) specifico. |

{style="table-layout:auto"}

## [!UICONTROL Order Approval Configuration]

![Caratteristiche B2B - Configurazione approvazione ordine](./assets/b2b-features-order-approval.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | Sito Web | Se abilitata, consente alle società di creare ordini fornitore. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}


