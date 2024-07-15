---
title: Regole prezzo catalogo
description: Scopri le regole del prezzo di catalogo che possono essere utilizzate per offrire prodotti agli acquirenti a un prezzo scontato in base a una serie di condizioni definite.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '522'
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

## Risorse per la risoluzione dei problemi

Per informazioni sulla risoluzione dei problemi relativi alle regole dei prezzi di catalogo, vedere i seguenti articoli della Knowledge Base di supporto di Commerce:

- [404 Errore durante l&#39;aggiornamento delle pianificazioni dei prezzi del catalogo nella vetrina](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/404-error-on-store-front-once-catalog-price-rule-schedules-update-is-performed.html)
- [Sono state migliorate le prestazioni della pagina prodotti con prodotti correlati e regole di destinazione](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31791-magento-patch-improvement-for-product-page-with-related-products-and-target-rules.html)
- [Le regole del prezzo del catalogo non funzionano](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-24201-magento-patch-catalog-price-rules-don-t-work.html)
- [Calcolo prezzi GraphQL](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33975-magento-patch-graphql-price-calculations.html)
