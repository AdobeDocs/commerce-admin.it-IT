---
title: Spedizioni
description: Scopri come creare record di spedizione per le fatture e annullare le spedizioni.
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---

# Spedizioni

Nella griglia _[!UICONTROL Shipments]_sono elencati i record di spedizione di tutte le fatture preparate per la spedizione. È possibile generare un record di spedizione quando un ordine è [fatturato](invoices.md) o successivo.

Adobe Commerce e il Magento Open Source supportano la spedizione parziale e completa degli ordini, con opzioni aggiuntive disponibili da [Inventory management](../inventory-management/introduction.md) ed estensioni di terze parti.

![Griglia spedizioni](./assets/shipments.png){width="600" zoomable="yes"}

## Descrizioni delle colonne

| Colonna o controllo | Descrizione |
|--- |--- |
| [!UICONTROL Select] | Selezionare la casella di controllo di ogni preventivo da sottoporre a un&#39;azione oppure utilizzare il controllo di selezione nell&#39;intestazione di colonna. Opzioni: `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | Numero sequenziale univoco assegnato al primo salvataggio di una nuova spedizione |
| [!UICONTROL Ship Date] | Data di spedizione |
| [!UICONTROL Order] | Numero univoco dell’ordine |
| [!UICONTROL Order Date] | Data e ora in cui è stato effettuato l’ordine |
| [!UICONTROL Ship-to Name] | Nome della persona a cui viene spedito l&#39;ordine |
| [!UICONTROL Total Quantity] | Quantità totale di articoli da spedire |
| [!UICONTROL Action] | Visualizza apre la spedizione in modalità di modifica |

{style="table-layout:auto"}

Colonne aggiuntive:

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Order Status] | Indica lo stato dell’ordine |
| [!UICONTROL Purchased From] | Indica la visualizzazione del sito Web, del punto vendita e del punto vendita in cui è stato effettuato l&#39;ordine |
| [!UICONTROL Customer Name] | Il nome del cliente o dell&#39;acquirente che ha effettuato l&#39;ordine |
| [!UICONTROL Email] | Indirizzo e-mail di un cliente registrato |
| [!UICONTROL Customer Group] | Nome del gruppo di clienti o del catalogo condiviso a cui è assegnato il cliente |
| [!UICONTROL Billing Address] | Il nome del cliente o dell&#39;acquirente che ha effettuato l&#39;ordine |
| [!UICONTROL Shipping Address] | Nome della persona a cui viene spedito l&#39;ordine |
| [!UICONTROL Payment Method] | Metodo di pagamento da utilizzare per l’ordine |
| [!UICONTROL Shipping Information] | Metodo da utilizzare per la spedizione dell&#39;ordine |

{style="table-layout:auto"}

## Creare una spedizione

Le istruzioni seguenti illustrano la procedura per la creazione di una spedizione in Adobe Commerce o Magento Open Source. Se Inventory management è abilitato, è possibile esaminare [Creazione di spedizioni con più Source](../inventory-management/shipments-create.md) e selezionare un&#39;origine (o un&#39;ubicazione) e una quantità da inviare per riga.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Individuare l&#39;ordine nella griglia e aprirlo.

1. Se l&#39;ordine è stato pagato, fatturato e pronto per la spedizione, fare clic su **[!UICONTROL Ship]**.

   Le sezioni nella parte superiore della spedizione contengono il nome, l&#39;indirizzo e le informazioni di pagamento dell&#39;ordine di vendita.

1. Completare ogni sezione del modulo di spedizione seguendo le istruzioni riportate nelle sezioni seguenti.

### [!UICONTROL Items to Ship]

Per ogni riga nell&#39;ordine, modificare **[!UICONTROL Qty to Ship]** in base alle esigenze.

### [!UICONTROL Shipping Information]

**Metodo 1:** Utilizzo della pagina dell&#39;ordine

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Nella colonna **[!UICONTROL Action]** dell&#39;ordine selezionato, fare clic su **[!UICONTROL View]**.

1. Fare clic su **[!UICONTROL Ship]**.

1. Scorri verso il basso fino al blocco _[!UICONTROL Payment & Shipping Method]_e fai clic su **[!UICONTROL Add Tracking Number]**.

1. Imposta **[!UICONTROL Carrier]**:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. Per tenere traccia della spedizione, immettere **[!UICONTROL Title]** e **[!UICONTROL Number]**.

**Metodo 2:** Utilizzo della pagina di spedizione

Questo metodo è consentito solo se la spedizione dell&#39;ordine è già stata creata dalla pagina ordine.
Puoi modificare le informazioni di spedizione e di tracciamento in base alle esigenze utilizzando la pagina di spedizione diretta:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Trova e apri la spedizione in modalità di modifica.

1. Scorri verso il basso fino al blocco _[!UICONTROL Payment & Shipping Method]_.

1. Selezionare **[!UICONTROL Carrier]**.

1. Immettere **[!UICONTROL Title]** per il pacchetto.

1. Immettere il tracciamento **[!UICONTROL Number]**.

1. Fare clic su **[!UICONTROL Add]**.

1. Per inviare un&#39;e-mail con le informazioni di tracciamento al cliente, fare clic su **[!UICONTROL Send Tracking Information]** e confermare l&#39;azione.

   Per tenere traccia dell&#39;ubicazione di qualsiasi spedizione, aprire la spedizione richiesta in modalità di modifica e fare clic su **[!UICONTROL Track this shipment]**.

   ![Informazioni su spedizione e monitoraggio](./assets/tracking-information.png){width="600" zoomable="yes"}

### Pulsanti

| Pulsante | Descrizione |
|--- |--- |
| **[!UICONTROL Back]** | Chiude la maschera Nuova spedizione e torna all&#39;ordine |
| **[!UICONTROL Submit Shipment]** | Aggiunge la spedizione per l&#39;ordine. |
| **[!UICONTROL Reset]** | Ripristina tutti i campi ai valori originali. |

{style="table-layout:auto"}

### Commenti sulla spedizione

1. Immetti **Commenti** per la spedizione, se necessario.

1. Quando la spedizione è pronta, fare clic su **Invia spedizione**.

## Imposta commenti per le spedizioni

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In _[!UICONTROL Sales]_, selezionare **[!UICONTROL Sales Email]**.

1. Espandere la sezione **Commenti spedizione** e modificare le impostazioni in base alle esigenze:

   ![Configurazione commento spedizione](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - L&#39;opzione **[!UICONTROL Enabled]** è impostata su `Yes` per impostazione predefinita, il che significa che l&#39;e-mail viene inviata a un cliente quando viene inserito un commento sulla spedizione.

   - Per **[!UICONTROL Shipment Comment Email Sender]**, selezionare la persona dalla quale inviare l&#39;e-mail di commento della spedizione. L’impostazione predefinita offre cinque indirizzi e-mail.

   - Per **[!UICONTROL Shipment Comment Email Template]**, selezionare il modello in base alle proprie esigenze oppure selezionare l&#39;opzione predefinita.

   - Per **[!UICONTROL Shipment Comment Email Template for Guests]**, scegli il modello utilizzato per i clienti che non hanno un account nello store.

   - Per **[!UICONTROL Shipment Comment Email Copy To]**, immettere gli indirizzi di posta elettronica per inviare una copia dell&#39;e-mail di commento della spedizione. Separa più indirizzi e-mail con una virgola.

   - Per **[!UICONTROL Shipment Comment Email Copy Method]**, selezionare `bcc` (copia per conoscenza nascosta) o il metodo `separate email copy` in base alle proprie preferenze.

1. Fare clic su **[!UICONTROL Save Config]**.

## Annullare una spedizione

Prima che una spedizione venga inviata a un vettore, è possibile annullarla aprendo l&#39;ordine e passando alla spedizione, a condizione che il vettore supporti gli annullamenti. Alcuni vettori limitano o limitano le cancellazioni dopo una prenotazione. Ad esempio, UPS consente gli annullamenti, ma richiede di attendere 24 ore dopo la prenotazione della spedizione. Se una spedizione viene annullata, l&#39;annullamento non può essere stornato. L&#39;unico ricorso è quello di ricreare l&#39;ordine.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Trovare l&#39;ordine nella griglia.

1. Nella colonna _Azione_ scegliere **[!UICONTROL View]**.

1. Nel pannello a sinistra, scegli **[!UICONTROL Shipments]**.

   Se la spedizione può essere annullata, _[!UICONTROL Cancel Shipment]_viene visualizzato come opzione nella barra dei pulsanti superiore.

1. Fare clic su **[!UICONTROL Cancel Shipment]**.

1. Quando viene richiesto di confermare, fare clic su **[!UICONTROL OK]**.

Lo stato della spedizione cambia in `Canceled`. Se il vettore non supporta gli annullamenti, viene visualizzato un messaggio di errore che spiega perché non è stato possibile annullare la spedizione.

## Descrizioni dei campi spedizione

### [!UICONTROL Shipping Information]

| Campo | Descrizione |
|-----|-----------|
| [!UICONTROL Carrier] | Nome del vettore selezionato |
| [!UICONTROL Title] | Nome descrittivo assegnato al pacchetto dal gestore. |
| [!UICONTROL Number] | Il numero di tracciamento collegato assegnato al pacchetto. |
| [!UICONTROL Action] | ![Icona cestino](../assets/icon-delete-trashcan-solid.png) - Elimina le informazioni sul pacchetto dal record di spedizione. |
| [!UICONTROL Add] | Aggiungi un altro pacchetto alla spedizione. |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| Campo | Descrizione |
|-----|-----------|
| [!UICONTROL Origin Location] | Visualizza un elenco delle posizioni disponibili. |
| [!UICONTROL International] | Se selezionato, identifica la spedizione come spedizione internazionale. |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| Campo | Descrizione |
|-----|-----------|
| [!UICONTROL Description] | Descrizione dell&#39;elemento. |
| [!UICONTROL SKU] | L&#39;unità di immagazzinaggio dell&#39;articolo. |
| [!UICONTROL Weight] | Peso dell&#39;articolo. |
| [!UICONTROL Qty Ordered] | Quantità dell&#39;articolo ordinato. |
| [!UICONTROL Qty Shipped] | Quantità di articoli spediti. |
| [!UICONTROL Qty Packed] | Il numero di elementi inclusi in questo pacchetto. |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| Campo | Descrizione |
|-----|-----------|
| [!UICONTROL Comments] | I commenti sulla spedizione sono per uso interno. |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| Campo | Descrizione |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG** - Scarica l&#39;etichetta del pacchetto di spedizione. Dimensioni: A6 (105 x 148 mm, 4,1 x 5,6 pollici) |

{style="table-layout:auto"}
