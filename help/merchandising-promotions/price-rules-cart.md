---
title: Regole prezzi carrello
description: Scopri le regole di prezzo del carrello che applicano sconti agli articoli nel carrello in base a una serie di condizioni.
exl-id: f3038f2a-9d34-4696-a39e-f87fbb1294a2
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Regole prezzi carrello

Le regole di prezzo del carrello applicano sconti agli articoli nel carrello, in base a una serie di condizioni. Lo sconto può essere applicato automaticamente quando le condizioni vengono soddisfatte o quando il cliente immette un codice coupon valido. Quando applicato, lo sconto viene visualizzato nel carrello sotto il subtotale. Una regola di prezzo del carrello può essere utilizzata in base alle esigenze per una stagione o una promozione modificandone lo stato e l’intervallo di date.

>[!NOTE]
>
>Se la regola del carrello coupon dispone di condizioni che specificano le opzioni di pagamento, ad esempio alcuni metodi di spedizione o di pagamento, le condizioni vengono soddisfatte solo durante il pagamento dopo la selezione dei metodi di spedizione/pagamento specifici. In questo caso, il coupon può essere applicato al momento del pagamento nell’ultimo passaggio.

![Vetrina di esempio - carrello applica coupon](./assets/storefront-cart-apply-coupon.png){width="600" zoomable="yes"}

## Regole di prezzo del carrello di accesso

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

   ![Regola prezzo carrello](./assets/price-rule-cart.png){width="700" zoomable="yes"}

1. Se hai numerose regole, utilizza le opzioni filtro nella parte superiore di ogni colonna per semplificare l&#39;elenco e fai clic su **[!UICONTROL Search]** per applicare i filtri.

1. Per cancellare tutte le opzioni di filtro e visualizzare l&#39;elenco completo, fare clic su **[!UICONTROL Reset Filter]**.

1. Aggiorna proprietà per una regola:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Fai clic su **[!UICONTROL Edit]** per visualizzare la pagina Informazioni regola.

   - ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Fai clic sulla regola nell&#39;elenco per visualizzare la pagina Informazioni regola.

   Qui è possibile modificare le impostazioni della regola (in modo analogo alla creazione di una regola).

## Filtra opzioni per colonna

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL ID] | Immetti il testo per filtrare l’elenco in base a un numero ID regola specifico. |
| [!UICONTROL Rule] | Immetti il testo per filtrare l’elenco in base al nome della regola definito al momento della creazione della regola. |
| [!UICONTROL Coupon Code] | Inserisci il testo per filtrare l’elenco in base al nome del codice definito al momento della creazione della regola. |
| [!UICONTROL Priority] | Campo di testo libero che filtra l’elenco in base alla priorità definita per una regola. |
| [!UICONTROL Status] | Utilizzare questa opzione per filtrare l&#39;elenco in base allo stato della regola (`Active` o `Inactive`). |
| [!UICONTROL Web Site] | Utilizza questa opzione per filtrare l’elenco in base ai siti web definiti per una regola. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Fai clic su **[!UICONTROL Edit]** per visualizzare la pagina _[!UICONTROL Rule Information]_e aggiornare le impostazioni della regola (in modo analogo alla creazione di una regola). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilizza i campi del calendario dinamico (_[!UICONTROL To:]_e_[!UICONTROL From:]_) per filtrare l&#39;elenco in base alla data di inizio per la regola definita al momento della creazione della regola. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Utilizza i campi del calendario dinamico (_[!UICONTROL To:]_e_[!UICONTROL From:]_) per filtrare l&#39;elenco in base alla data di fine per la regola definita al momento della creazione della regola. |

{style="table-layout:auto"}

## Utilizza i tipi di pubblico di Real-Time CDP per informare le regole di prezzo del carrello

Scopri come [attivare](../customers/audience-activation.md) i tipi di pubblico di Real-Time CDP nella tua istanza di Adobe Commerce per informare le regole del prezzo del carrello.
