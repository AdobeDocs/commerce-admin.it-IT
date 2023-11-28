---
title: Impostazioni prodotto - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: Per un prodotto, il [!UICONTROL Related Products, Up-Sells, and Cross-Sells] Le impostazioni definiscono semplici blocchi promozionali sulla pagina del prodotto che evidenziano una selezione di prodotti aggiuntivi.
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# Impostazioni prodotto - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

Utilizza il _[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_sezione per impostare semplici blocchi promozionali che presentano una selezione di prodotti aggiuntivi che potrebbero essere di interesse per il cliente. Per ulteriori informazioni, consulta [Relazioni prodotto](../merchandising-promotions/product-relationships.md).

![Prodotti correlati, up-selling e cross-selling](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

Ogni blocco è costituito da un elenco di prodotti che appartengono a un’opzione specifica.

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL ID] | Identificatore numerico univoco assegnato all’entità prodotto. |
| [!UICONTROL Thumbnail] | Immagine miniatura prodotto. |
| [!UICONTROL Name] | Il nome del prodotto. |
| [!UICONTROL Status] | Indica lo stato del prodotto. Opzioni: `Enabled` / `Disabled`. I prodotti disattivati non vengono visualizzati nei blocchi sul front-end. |
| [!UICONTROL Attribute Set] | Nome del set di attributi utilizzato come modello per il prodotto. |
| [!UICONTROL SKU] | Unità di stoccaggio univoca assegnata al prodotto. |
| [!UICONTROL Price] | Il prezzo unitario del prodotto. |
| [!UICONTROL Action] | Opzioni: `Remove`. Rimuovi un prodotto dal blocco. |

{style="table-layout:auto"}

>[!TIP]
>
>![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) **Recommendations di prodotto con tecnologia Adobe Sensei** semplifica il processo di definizione delle relazioni tra i prodotti utilizzando algoritmi di intelligenza artificiale e machine learning per eseguire un’analisi approfondita dei dati aggregati dei visitatori. Quando vengono combinati con il catalogo di Adobe Commerce, questi dati offrono esperienze altamente coinvolgenti, pertinenti e personalizzate per l’acquirente.
><br/>
>Per ulteriori informazioni sull’utilizzo di questa estensione sviluppata dall’Adobe come alternativa alla configurazione manuale di consigli e up-sell, consulta la sezione _[Guida di Recommendations del prodotto](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)_.

## Prodotti correlati

I prodotti correlati devono essere acquistati in aggiunta all&#39;articolo che il cliente sta visualizzando. Il cliente può inserire l’articolo nel carrello semplicemente facendo clic sulla casella di controllo. Posizionamento del _Prodotti correlati_ Il blocco varia in base al tema e al layout di pagina definiti. Nell’esempio seguente, il _Prodotti correlati_ il blocco viene visualizzato nella parte inferiore del _Visualizzazione prodotto_ pagina. Con un layout a due colonne, _Prodotti correlati_ Il blocco viene spesso visualizzato nella barra laterale destra.

![Prodotti correlati](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

Per impostare i prodotti correlati:

1. Apri il prodotto in modalità di modifica.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** sezione.

1. Clic **[!UICONTROL Add Related Products]**.

1. Utilizza il [controlli filtro](../getting-started/admin-grid-controls.md) per trovare i prodotti desiderati.

1. Nell’elenco, seleziona la casella di controllo di qualsiasi prodotto che desideri visualizzare come prodotto correlato.

   ![Prodotti correlati](./assets/products-related-add.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Add Selected Products]**.

## Up-sell

I prodotti di upselling sono articoli che il cliente potrebbe preferire al posto del prodotto attualmente considerato. Un articolo offerto come upselling potrebbe essere di qualità superiore, più popolare o avere un margine di profitto migliore. I prodotti di upselling vengono visualizzati nella pagina del prodotto sotto un’intestazione come _Potresti anche essere interessato ai seguenti prodotti_.

![Up-selling](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

Per selezionare i prodotti di upselling:

1. Apri il prodotto in modalità di modifica.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** sezione.

1. Clic **[!UICONTROL Add Up-Sell Products]**.

1. Utilizza il [controlli filtro](../getting-started/admin-grid-controls.md) per trovare i prodotti desiderati.

1. Nell’elenco, seleziona la casella di controllo di qualsiasi prodotto che desideri visualizzare come prodotto di upselling.

   ![Prodotti up-selling](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Add Selected Products]**.

## Effetti di cross-selling

Gli articoli di cross-selling sono simili agli acquisti di impulso posizionati accanto al registratore di cassa nella linea di pagamento. I prodotti offerti come cross-selling vengono visualizzati sulla pagina del carrello, appena prima che il cliente inizi il processo di pagamento.

>[!NOTE]
>
>Per mostrare o nascondere gli articoli di cross-selling per visualizzazione punto vendita, vedere [Pagamento > Carrello](../configuration-reference/sales/checkout.md) opzione denominata _[!UICONTROL Show Cross-sell Items]_nel carrello. Puoi nascondere le cross-selling durante vendite specifiche o per test A/B in una visualizzazione punto vendita.

![Cross-selling nel carrello](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_Per selezionare i prodotti di cross-selling:_**

1. Apri il prodotto in modalità di modifica.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** sezione.

1. Clic **[!UICONTROL Add Cross-Sell Products]**.

1. Utilizza il [controlli filtro](../getting-started/admin-grid-controls.md) per trovare i prodotti desiderati.

1. Nell’elenco, seleziona la casella di controllo di qualsiasi prodotto che desideri visualizzare come prodotto di cross-selling.

   ![Prodotti di cross-selling](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Add Selected Products]**.
