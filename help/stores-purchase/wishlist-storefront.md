---
title: Esperienza vetrina elenco desideri
description: Scopri gli strumenti di gestione della lista dei desideri disponibili per i tuoi clienti nella vetrina.
exl-id: df8cf89a-c897-4a9a-9e84-3bae946683a4
feature: Customers, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 0%

---

# Esperienza vetrina elenco desideri

Una lista dei desideri è un modo conveniente per i clienti di richiamare i prodotti che preferiscono, ma non sono pronti per acquistare. Gli articoli di una lista dei desideri possono essere condivisi con altri o aggiunti al carrello. Se il cliente dispone di più elenchi di desideri, il nome della lista corrente viene visualizzato nella parte superiore della pagina. I clienti possono gestire i propri elenchi di desideri dal dashboard dell’account. Gli amministratori del negozio possono inoltre aiutare i clienti a gestire le loro liste dei desideri dall’amministratore.

![Vetrina di esempio - Elenco desideri](./assets/storefront-my-wishlist.png){width="700" zoomable="yes"}

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce supporta l&#39;utilizzo di più elenchi di desideri per account cliente.

![Magento Open Source](../assets/open-source.svg) La base di codice del Magento Open Source supporta l&#39;utilizzo di una singola lista dei desideri per account cliente.

## Creare una lista dei desideri

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

Nella vetrina, un cliente può creare una lista dei desideri dal proprio dashboard dell’account, da una pagina del prodotto, da una pagina del catalogo e dal carrello.

### Metodo 1: da un conto cliente

1. Nella barra laterale del dashboard dell&#39;account, il cliente sceglie **[!UICONTROL My Wish List]**.

1. Nell&#39;angolo superiore destro, fa clic su **[!UICONTROL Create New Wish List]**.

1. Inserire il nome della lista dei desideri.

1. Per consentire ad altri utenti di visualizzare la propria lista dei desideri, seleziona la casella di controllo **[!UICONTROL Public Wish List]**.

   >[!NOTE]
   >
   >La differenza principale tra `Public` e `Private` elenchi desideri è che gli elenchi desideri privati non sono [ricercabili](wishlist-configuration.md#add-wish-list-search) tramite elenchi desideri.

1. Al termine, fare clic su **[!UICONTROL Save]**.

   ![Crea nuovo elenco desideri](./assets/account-dashboard-wishlist-create-new.png){width="700" zoomable="yes"}

### Metodo 2: dalla pagina del catalogo

1. Dalla vetrina, il cliente accede alla pagina del catalogo contenente il prodotto che desidera aggiungere a una lista dei desideri.

1. Passa il mouse sopra il prodotto.

1. Il cliente fa clic sulla freccia accanto all&#39;icona _Aggiungi a elenco desideri_ e seleziona **[!UICONTROL Create New Wish List]**.

1. Inserisce il nome della lista dei desideri.

1. Per consentire ad altri utenti di visualizzare la propria lista dei desideri, seleziona la casella di controllo **[!UICONTROL Public Wish List]**.

1. Al termine, fa clic su **[!UICONTROL Save]**.

### Metodo 3: dalla pagina dei dettagli del prodotto

1. Dalla vetrina, il cliente accede alla pagina dei dettagli del prodotto che desidera aggiungere a una lista dei desideri.

1. Fare clic sulla freccia accanto a **[!UICONTROL Add to Wish List]** e scegliere **[!UICONTROL Create New Wish List]**.

1. Immette **[!UICONTROL Wish List Name]**.

1. Per consentire ad altri utenti di visualizzare la propria lista dei desideri, seleziona la casella di controllo **[!UICONTROL Public Wish List]**.

1. Al termine, fa clic su **[!UICONTROL Save]**.

   ![Crea nuovo elenco desideri dalla pagina Dettagli prodotto](./assets/account-dashboard-wishlist-create-from-pdp.png){width="700" zoomable="yes"}

### Metodo 4: dal carrello

1. Il cliente apre la pagina **[!UICONTROL Shopping Cart]**.

1. Sotto l&#39;elemento fare clic sulla freccia accanto a **[!UICONTROL Move to Wishlist]** e scegliere **[!UICONTROL Create New Wish List]**.

1. Immette **[!UICONTROL Wish List Name]**.

1. Per consentire ad altri utenti di visualizzare la propria lista dei desideri, seleziona la casella di controllo **[!UICONTROL Public Wish List]**.

1. Al termine, fa clic su **[!UICONTROL Save]**.

![Crea nuovo elenco desideri dalla pagina del carrello acquisti](./assets/account-dashboard-wishlist-create-from-cart.png){width="700" zoomable="yes"}

## Aggiornare l’elenco dei prodotti

1. Dalla lista dei desideri, il cliente punta al prodotto per visualizzare le opzioni.

1. Per aggiungere un **[!UICONTROL Comment]** sul prodotto, immetti il testo nella casella sotto il prezzo.

   ![Modifica opzioni](./assets/account-dashboard-wishlist-edit-options.png){width="700" zoomable="yes"}

1. Per modificare la selezione delle opzioni di prodotto, fare clic su **[!UICONTROL Edit]** ed eseguire le operazioni seguenti:

   - Aggiorna le opzioni nella pagina dei dettagli del prodotto.
   - Clic su **[!UICONTROL Update Wish List]**.

## Aggiungere un prodotto della lista dei desideri al carrello

1. Nella lista dei desideri, il cliente punta al prodotto che desideri aggiungere.

1. Aggiorna **[!UICONTROL Qty]** e modifica le altre opzioni in base alle esigenze.

1. Clic su **[!UICONTROL Add to Cart]**.

## Condividi la lista desideri

1. Il cliente fa clic su **[!UICONTROL Share Wishlist]**.

1. Inserisce l&#39;indirizzo e-mail di ogni persona che deve ricevere la lista dei desideri, separati da una virgola.

1. Aggiunge un **[!UICONTROL Message]** da includere nell&#39;e-mail.

1. Clic su **[!UICONTROL Share Wish List]**.

   ![Condividi elenco desideri](./assets/account-dashboard-wishlist-sharing.png){width="700" zoomable="yes"}

   Il messaggio viene inviato dal [contatto dell&#39;archivio](../getting-started/store-details.md#store-email-addresses) principale e include una miniatura di ciascun prodotto, con collegamenti all&#39;archivio.

   ![E-mail elenco desideri condivisi](./assets/account-dashboard-wishlist-sharing-email.png){width="500" zoomable="yes"}

## Modifica elenchi di desideri

I clienti possono modificare la propria lista dei desideri in diversi modi dalla dashboard dell’account.

### Sposta elementi in un altro elenco

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

1. Il cliente seleziona la casella di controllo di ogni elemento da spostare.

1. Fai clic su **[!UICONTROL Move Selected to Wish List]** ed effettua una delle seguenti operazioni:

   - Seleziona una lista desideri esistente.
   - Clic su **[!UICONTROL Create New Wish List]**.

### Copia elementi in un altro elenco

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

1. Seleziona la casella di controllo di ogni elemento da spostare.

1. Fai clic su **[!UICONTROL Copy Selected to Wish List]** ed effettua una delle seguenti operazioni:

   - Seleziona una lista desideri esistente.
   - Clic su **[!UICONTROL Create New Wish List]**.

## Eliminare una lista dei desideri

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

1. Il cliente apre la lista dei desideri da eliminare.

1. Clic su **[!UICONTROL Delete Wish List]**.

1. Quando viene richiesto di confermare, fa clic su **[!UICONTROL OK]**.

>[!IMPORTANT]
>
>Questa azione non può essere annullata.

## Trasferisci voci elenco desideri al carrello

Per trasferire tutti gli elementi della lista dei desideri al carrello, il cliente fa clic su **[!UICONTROL Add All to Cart]**.

Per aggiungere un singolo articolo, il cliente effettua le seguenti operazioni:

1. Passa il puntatore del mouse sull&#39;elemento e immette **[!UICONTROL Qty]** che si desidera aggiungere al carrello.

1. Clic su **[!UICONTROL Add to Cart]**.

## Trovare una lista dei desideri del cliente

Se il widget [Ricerca elenco desideri](wishlist-configuration.md#add-wish-list-search) è incluso nelle pagine del tuo negozio, i clienti possono eseguire ricerche in base al nome o all&#39;indirizzo e-mail del proprietario della lista desideri.

1. Dal widget di ricerca della lista dei desideri, il cliente seleziona un’opzione di ricerca.

1. Immette il nome o l&#39;indirizzo di posta elettronica del proprietario della lista dei desideri e fa clic su **[!UICONTROL Search]**.

   Viene aperta la pagina _Ricerca elenco desideri_ e nella sezione dei risultati della ricerca vengono visualizzate tutte le liste dei desideri corrispondenti.

   >[!NOTE]
   >
   >Nei risultati della ricerca vengono visualizzate solo le liste dei desideri pubbliche; le liste dei desideri private dei clienti non sono visualizzabili pubblicamente.

1. Per visualizzare l&#39;elenco degli elementi dell&#39;elenco dei desideri, fare clic su **[!UICONTROL View]**.

   Per ogni lista dei desideri vengono visualizzati il nome del proprietario e la data dell&#39;ultimo aggiornamento.

1. Per aggiungere un prodotto al carrello, il cliente seleziona la casella di controllo sotto il prodotto e fa clic su **[!UICONTROL Add to Cart]**.

   Puoi anche aggiungere alla tua lista dei desideri articoli che ti piacciono di un altro cliente.
