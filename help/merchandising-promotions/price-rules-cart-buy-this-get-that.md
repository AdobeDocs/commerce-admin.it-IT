---
title: 'Esempio di regola di prezzo del carrello: acquista questo per ottenerlo'
description: Rivedi un esempio di utilizzo di una regola di prezzo del carrello per offrire una promozione di acquisto-questo-ottenere-che.
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# Esempio di regola di prezzo del carrello: acquista questo per ottenerlo

Questo esempio mostra come impostare un [regola prezzo carrello](price-rules-cart.md) per un _Compra questo, prendi quello gratis_ promozione. Il formato dello sconto è il seguente:

_Acquista X quantità di prodotto, ottenere Y quantità gratis_

## Passaggio 1: Creare una regola di prezzo del carrello

Completa [Passaggio 1](price-rules-cart.md) delle istruzioni per la regola di prezzo del carrello per completare le informazioni sulla regola.

## Passaggio 2: Definire le condizioni

Completa [Passaggio 2](price-rules-cart.md) delle istruzioni del carrello per definire le condizioni per la regola prezzo. Questa è la prima delle due condizioni che possono essere aggiunte alla regola e determina quando viene attivata la regola. Può essere basata su una combinazione dei seguenti elementi:

- Attributi del prodotto
- Prodotti
- Attributi del carrello
- ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Segmenti cliente

Se non specificato, la regola viene attivata per ogni carrello.

![Regola prezzo carrello - Condizione](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## Passaggio 3: Definire le azioni

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Actions]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Apply]** a `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - Imposta **[!UICONTROL Discount Amount]** a `1`. Si tratta della quantità che il cliente riceve gratuitamente.

   - Per limitare il numero di sconti che possono essere applicati quando la condizione viene soddisfatta, immettere il numero nel campo **[!UICONTROL Maximum Qty Discount is Applied To]** campo. Questo viene calcolato utilizzando [formula](#maximum-quantity-discount).

   - Per **[!UICONTROL Discount Qty Step (Buy X)]**, inserire la quantità che il cliente deve acquistare per ottenere lo sconto. In questo esempio, il cliente deve acquistarne tre.

   - Se si desidera impedire l&#39;applicazione di altri sconti all&#39;acquisto, impostare **[!UICONTROL Discard subsequent rules]** a `Yes`.

   ![Regola prezzo carrello - acquistare 3 ottenere 1 gratis](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. Per applicare la regola solo ad articoli specifici nel carrello, completa la condizione per descrivere gli articoli del carrello e/o gli attributi del prodotto necessari per la promozione.

   L’esempio seguente utilizza lo SKU per applicare la regola a tutte le varianti associate di un prodotto configurabile.

   ![Regola prezzo carrello - condizione per articoli carrello](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. Da includere **[!UICONTROL Free Shipping]**, scegli `For matching items only`.

1. Clic **[!UICONTROL Save and Continue Edit]** e completa il resto della regola come necessario.

## Passaggio 4: Completa l’etichetta

Completa [Passaggio 4](price-rules-cart.md) delle istruzioni della regola prezzo carrello per inserire l&#39;etichetta visualizzata durante il pagamento.

## Passaggio 5: salvare e verificare la regola

{{new-price-rule}}

1. Al termine della regola, fai clic su **[!UICONTROL Save Rule]**.

1. Verifica la regola per assicurarti che funzioni correttamente.

## Varianti

Acquista X Ottieni Y Gratis viene elaborato come una singola azione, con un _totale riga_ dipendenza. Tutti gli articoli devono appartenere alla stessa SKU per essere idonei per la promozione. Ad esempio:

Acquista X quantità di prodotto dalla categoria A, ottenere Y quantità dello stesso prodotto gratuitamente.

Per limitare il prodotto libero alle categorie A, B e C, impostare l&#39;azione come segue:

Se TUTTE queste condizioni sono TRUE: la categoria è una delle seguenti: A, B, C

Per limitare gli articoli liberi di qualsiasi categoria (A, B o C) e ricevere Y dagli SKU (D123, E123 o F123), impostare l&#39;azione come segue:

Se TUTTE queste condizioni sono TRUE: SKU è uno dei valori D123, E123, F123

## Sconto quantità massima

Utilizzare la formula seguente per determinare il valore corretto per lo sconto Qtà massima:

Formula = `(X+Y) * (M/Y)`
Dove
`X` = numero di articoli acquistati
`Y` = numero di elementi liberi
`M` = Numero massimo di elementi liberi consentiti

Ad esempio:

Acquista cinque e ne ottieni due gratis con un massimo di quattro articoli gratuiti consentiti.

    Dove
    X = 5
    Y = 2
    M = 4
    Sconto qtà massimo = (5+2)*(4/2)=(7)*(2)=14

Compra cinque e ottieni tre gratis con un massimo di nove articoli gratuiti consentiti.

    Dove
    X = 5
    Y = 3
    M = 9
    Sconto qtà massimo = (5+3)*(9/3)=24

Compra 20 e ottieni due gratis con un massimo di 20 articoli gratuiti consentiti.

    Dove
    X = 20
    Y = 2
    M = 20
    Sconto qtà massimo = (20+2)*(20/2)=(22)*(10)=220
