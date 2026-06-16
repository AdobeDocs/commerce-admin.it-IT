---
title: Gestire un carrello
description: Scopri come assistere un cliente nel carrello direttamente dall’Amministratore.
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
TQID: https://experienceleague.adobe.com/6kRS38XXT2krhGWypaXChWpBdtvfLupBJX2k6cE4y6w
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 746
ht-degree: 0%

---

# Gestire un carrello

{{ee-feature}}

Per iniziare una sessione di acquisto assistito, il cliente deve aver effettuato l’accesso al proprio account dalla vetrina per rendere disponibili le informazioni. Se il cliente non ha un account, puoi [crearne uno](../customers/account-create.md).

![Carrello acquisti nell&#39;account cliente](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## Controllo Azioni

| Opzione | Descrizione |
|--- |--- |
| [!UICONTROL Remove] | Rimuove gli articoli dal carrello corrente |
| [!UICONTROL Move to Wish List] | Sposta gli elementi nella lista dei desideri cliente selezionata |

{style="table-layout:auto"}

## Pulsanti di controllo

| Pulsante | Descrizione |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | Rimuove tutti gli elementi dal carrello. |
| [!UICONTROL Update Items and Quantities|]Immettere la quantità richiesta nel campo **[!UICONTROL Qty]** e aggiornare il numero di elementi nel carrello. |
| [!UICONTROL Add selections to my cart] | Aggiunge al carrello i prodotti di tutte le sezioni. |

{style="table-layout:auto"}

## Verificare che il cliente abbia effettuato l’accesso

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Now Online]**.

   Tutti i visitatori del negozio e i clienti connessi vengono visualizzati nell’elenco.

   ![Clienti online](./assets/customers-now-online.png){width="700" zoomable="yes"}

## Acquisti assistiti da offerte

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Nell’elenco, apri il record cliente in modalità di modifica.

   >[!TIP]
   >
   >Per trovare rapidamente il record cliente, utilizzare il controllo [Filtri](../getting-started/admin-grid-controls.md).

   Nel profilo cliente in _[!UICONTROL Personal Information]_, la data e l&#39;ora_[!UICONTROL Last Logged In]_ mostrano che il cliente è online.

   ![Profilo cliente di un cliente online](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. Per accedere alla modalità di acquisto assistito, fare clic su **[!UICONTROL Manage Shopping Cart]** nella barra dei pulsanti superiore.

   ![Modalità di acquisto assistito](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## Aggiungi prodotti al carrello per attributo

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Products]**.

1. Trova un prodotto utilizzando uno dei filtri nella parte superiore di ogni colonna.

1. Fare clic su **[!UICONTROL Search]**.

1. Utilizza una delle seguenti serie di passaggi in base al tipo di prodotto:

### Aggiungere un prodotto semplice

1. Fare clic sul prodotto che si desidera ordinare.

   Questa azione seleziona il record e imposta **[!UICONTROL Quantity]** sul valore predefinito di `1`.

1. Se necessario, aggiornare la quantità ordinata.

1. Sulla sinistra sopra la griglia, fare clic su **[!UICONTROL Add selections to my cart]**.

   ![Aggiungi prodotto al carrello](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   La riga viene aggiunta al carrello nella parte superiore della pagina.

   ![Carrello aggiornato](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### Aggiungi un prodotto con configurazione

Prima di aggiungere al carrello è necessario configurare tre tipi di prodotti: `Bundle Product`, `Configurable Product` e `Grouped Product`.

1. Nella griglia, fare clic su **[!UICONTROL Configure]** accanto al nome del prodotto.

   ![Configura il prodotto](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. Nella finestra di dialogo _Prodotti associati_, scegli ogni opzione di prodotto per descrivere l&#39;elemento da ordinare, immetti **[!UICONTROL Quantity]** e fai clic su **[!UICONTROL OK]**.

   Il prodotto viene selezionato con un segno di spunta e la quantità ordinata viene visualizzata nella griglia.

1. Per aggiungere il prodotto al carrello, fare clic su **[!UICONTROL Add selections to my cart]**.

   ![Prodotto configurabile nel carrello](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. Se necessario, aggiorna le opzioni prodotto nel carrello:

   - Fare clic su **[!UICONTROL Configure]**.

   - Aggiornare le opzioni e quindi fare clic su **[!UICONTROL OK]**.

## Aggiungi prodotto per SKU

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Add to Shopping Cart by SKU]**.

1. Aggiungi i prodotti singolarmente per **[!UICONTROL SKU]** o aggiungi i prodotti caricando un file CSV.

### Aggiungi elementi singolarmente per SKU

1. Immettere **[!UICONTROL SKU]** e **[!UICONTROL Qty]** dell&#39;elemento da ordinare.

1. Per ordinare un altro prodotto, fare clic su **[!UICONTROL Add another]**.

   ![Aggiungi prodotti per SKU](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Add selections to my cart]**.

1. Se l&#39;elemento è un prodotto configurabile, scegliere le opzioni del prodotto quando richiesto e quindi fare clic su **[!UICONTROL Add to Shopping Cart]**.

### Aggiungere prodotti caricando un file CSV

1. Prepara un [file csv](../systems/data-csv.md) con gli elementi da aggiungere al carrello.

   Il file deve contenere solo due colonne, con `sku` e `qty` nell&#39;intestazione.

1. Carica il file preparato:

   - Fare clic su **[!UICONTROL Choose File]**.

   - Seleziona il file da caricare dalla directory.

## Trasferisci un articolo

Puoi trasferire gli articoli nel carrello dalla lista dei desideri di un cliente e gli articoli visualizzati, confrontati o ordinati di recente. Il numero di elementi in ogni sezione viene visualizzato tra parentesi dopo l&#39;intestazione della sezione.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) in una delle sezioni seguenti:

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. Nella griglia, selezionare ogni prodotto da ordinare e immettere **[!UICONTROL Quantity]**.

1. Per immettere le opzioni per un prodotto configurabile, fare clic su **[!UICONTROL Configure]** e impostare le opzioni del prodotto in base alle esigenze.

1. Fare clic su **[!UICONTROL Add selections to my cart]**.

1. Applica uno o più codici coupon, se disponibili:

   - Per **[!UICONTROL Apply Coupon Code]**, immettere un codice coupon valido.

   - Fai clic sulla freccia _Applica_ ( ![Icona freccia](../assets/icon-apply-arrow.png) ).

1. Regola la quantità ordinata in base alle esigenze:

   - Nella colonna **[!UICONTROL Qty]** del prodotto da adeguare, immettere l&#39;importo corretto.

   - Fare clic su **[!UICONTROL Update Items and Quantities]**.

## Crea l’ordine

1. Fare clic su **[!UICONTROL Create Order]**.

   Nella pagina _[!UICONTROL Create New Order]_sono visualizzati gli articoli nel carrello, seguiti dalle informazioni di spedizione e pagamento.

1. Completare le informazioni relative alla spedizione e al pagamento.

1. Fare clic su **[!UICONTROL Submit Order]**.

Per ulteriori informazioni, consulta [Creare un ordine](customer-account-create-order.md).

## Rimuovere tutti gli elementi da un carrello

La rimozione di tutti gli articoli dal carrello di un cliente in modalità di acquisto assistito è utile se il cliente desidera ricominciare da capo, ha aggiunto articoli non corretti o deve cancellare il carrello prima di effettuare un nuovo ordine. In questo modo il carrello conterrà solo i prodotti che il cliente desidera acquistare.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Nell’elenco, apri il record cliente in modalità di modifica.

1. Fai clic su **[!UICONTROL Manage Shopping Cart]** nella barra dei pulsanti superiore.

1. Fare clic su **[!UICONTROL Clear my shopping cart]**.

   ![Cancella il carrello](./assets/customer-manage-shopping-cart-clear.png){width="600" zoomable="yes"}

1. Quando richiesto, fare clic su **[!UICONTROL OK]** per confermare l&#39;azione.
