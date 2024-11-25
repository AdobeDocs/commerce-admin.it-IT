---
title: Regole prezzo catalogo
description: Scopri le regole del prezzo di catalogo che possono essere utilizzate per offrire prodotti agli acquirenti a un prezzo scontato in base a una serie di condizioni definite.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '468'
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
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilizza i campi del calendario dinamico (A: e Da:) per filtrare l&#39;elenco in base alla data di inizio per la regola definita al momento della creazione della regola. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilizza i campi del calendario dinamico (A: e Da:) per filtrare l&#39;elenco in base alla data di fine per la regola definita al momento della creazione della regola. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilizzare questa opzione per filtrare l&#39;elenco in base allo stato della regola (`Active` o `Inactive`). |

{style="table-layout:auto"}
