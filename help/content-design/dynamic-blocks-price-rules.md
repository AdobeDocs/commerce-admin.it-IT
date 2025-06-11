---
title: Blocchi dinamici nelle regole di prezzo
description: Associare un blocco dinamico a una regola di prezzo promozionale.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Blocchi dinamici nelle regole di prezzo

{{ee-feature}}

Qualsiasi [blocco dinamico](dynamic-blocks.md) creato può essere associato a una promozione. Per creare l&#39;associazione, è necessario innanzitutto creare sia il blocco dinamico che la [regola prezzo catalogo](../merchandising-promotions/price-rules-catalog.md) o la [regola prezzo carrello](../merchandising-promotions/price-rules-cart.md). L’associazione può essere effettuata mentre si lavora su una regola di prezzo o su un blocco dinamico.

>[!IMPORTANT]
>
>Dopo aver creato questa associazione, il blocco dinamico viene visualizzato **solo** quando la regola viene attivata. Se la promozione è indirizzata al segmento A, il blocco viene visualizzato al segmento A. Se la promozione non è attiva, il blocco non viene visualizzato.

## Associare un blocco dinamico a una regola di prezzo

1. Nella barra laterale _Admin_, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_e scegli una delle seguenti opzioni:

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. Nella griglia, individua la regola da associare al blocco dinamico e aprila in modalità di modifica.

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. Nella prima colonna impostare il filtro su `Any` e fare clic su **[!UICONTROL Reset Filter]**.

   Nella griglia sono ora elencati tutti i blocchi dinamici disponibili.

1. Selezionare la casella di controllo di ogni blocco dinamico che si desidera associare alla regola.

   ![Aggiunta di blocchi dinamici selezionati](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Associare una regola di prezzo a un blocco dinamico

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Trova il blocco dinamico nella griglia e aprilo in modalità di modifica.

1. Scorri verso il basso ed espandi **[!UICONTROL Related Promotions]**.

   Tutte le regole di prezzo attualmente associate vengono visualizzate nella griglia.

1. Aggiungi una nuova regola associata o rimuovi un&#39;associazione corrente.

   - Per associare una promozione carrello, fare clic su **[!UICONTROL Add Cart Price Rules]**.

   - Per associare una promozione relativa al prodotto, fare clic su **[!UICONTROL Add Catalog Price Rules]**.

1. Nella griglia selezionare la casella di controllo di ogni regola che si desidera associare al blocco dinamico.

1. Fare clic su **[!UICONTROL Add Selected]**.

   ![Aggiunta delle regole di prezzo selezionate a un blocco dinamico](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save]**.
