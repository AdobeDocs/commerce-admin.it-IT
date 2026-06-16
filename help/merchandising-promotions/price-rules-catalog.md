---
title: Regole prezzo catalogo
description: Scopri le regole del prezzo di catalogo che possono essere utilizzate per offrire prodotti agli acquirenti a un prezzo scontato in base a una serie di condizioni definite.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
TQID: https://experienceleague.adobe.com/JZE2DF0tp-XOsKjxo-WaQiwA3Y-FrM4TI5qq-Nze-qo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 468
ht-degree: 0%

---

# Regole prezzo catalogo

Le regole del prezzo di catalogo possono essere utilizzate per offrire prodotti agli acquirenti a un prezzo scontato, in base a una serie di condizioni definite. Le regole di prezzo del catalogo non utilizzano [codici coupon](price-rules-cart-coupon.md), perché vengono attivati prima che un prodotto venga inserito nel carrello.

Ad esempio, puoi definire e impostare le condizioni per una regola di prezzo che, una volta soddisfatta, visualizza automaticamente i prodotti con un prezzo speciale o promozionale. Le proprietà della regola definite possono includere gruppi di clienti, categorie di prodotti, un importo o una percentuale di sconto, il colore del prodotto, la dimensione del prodotto o quasi qualsiasi attributo di prodotto impostato nel punto vendita. È possibile impostare le date di inizio e di fine per una regola di prezzo che avvia e interrompe automaticamente una promozione alle date definite nella regola. Le proprietà di una regola salvata possono essere aggiornate o modificate in base alle esigenze.

- ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Puoi anche collegare una regola definita a un [blocco dinamico](../content-design/dynamic-blocks.md) per promuovere l&#39;evento o il prodotto nell&#39;archivio.

- ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Per le promozioni ricorrenti, puoi impostare manualmente una regola salvata sullo stato _Attivo_ o _Inattivo_ ogni volta che desideri eseguire la promozione.

## Accedere alle regole di prezzo del catalogo

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

   ![Regole prezzo catalogo](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. Aggiorna proprietà per una regola:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Fai clic su **[!UICONTROL Edit]** per visualizzare la pagina _Informazioni sulle regole_.

   - ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Fai clic sulla regola nell&#39;elenco per visualizzare la pagina Informazioni regola.

   È possibile modificare le impostazioni per la regola (in modo simile a [creare una regola](price-rules-catalog-create.md)).

## Opzioni filtro

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL ID] | Immetti il testo per filtrare l’elenco in base a un numero ID regola specifico. |
| [!UICONTROL Rule] | Immetti il testo per filtrare l’elenco in base al nome della regola definito al momento della creazione della regola. |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Immetti il testo in questo campo per filtrare l&#39;elenco in base alla priorità definita per una regola. |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) utilizza questa opzione per filtrare l&#39;elenco in base ai siti Web definiti per una regola. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Fai clic su **[!UICONTROL Edit]** per visualizzare le informazioni sulla regola e aggiornare le impostazioni della regola (in modo analogo alla creazione di una regola). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilizza i campi del calendario dinamico (A: e Da:) per filtrare l&#39;elenco in base alla data di inizio della regola definita al momento della creazione della regola. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilizza i campi del calendario dinamico (A: e Da:) per filtrare l&#39;elenco in base alla data di fine per la regola definita al momento della creazione della regola. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilizzare questa opzione per filtrare l&#39;elenco in base allo stato della regola (`Active` o `Inactive`). |

{style="table-layout:auto"}
