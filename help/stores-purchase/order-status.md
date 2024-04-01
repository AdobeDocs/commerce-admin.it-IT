---
title: Stato ordine
description: Scopri gli stati degli ordini predefiniti e come definire stati degli ordini personalizzati in base alle tue esigenze operative.
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: c2d5e9b41a76ba58d1343a8b3ee5122104d5bfe0
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Stato ordine

Tutti gli ordini hanno uno stato associato a una fase nell&#39;elaborazione dell&#39;ordine [workflow](order-processing.md).\
La differenza tra gli stati degli ordini e gli stati degli ordini è che **[!UICONTROL order states]** vengono utilizzati a livello di programmazione. Non sono visibili ai clienti o agli utenti amministratori. Essi determinano il flusso di un ordine e quali operazioni sono possibili per un ordine in un determinato stato.\
**[!UICONTROL Order statuses]** vengono utilizzati per comunicare lo stato di un ordine ai clienti e agli utenti amministratori.
Puoi creare stati di ordine aggiuntivi per allinearli alle tue esigenze operative. Gli stati dell’ordine sono utili per visualizzare l’avanzamento al di fuori di Adobe Commerce, ad esempio il prelievo dell’ordine e l’avanzamento della consegna. Non hanno alcun impatto sul flusso di lavoro di elaborazione degli ordini.\
Ogni stato dell&#39;ordine è associato a uno stato dell&#39;ordine. Lo store dispone di una serie di impostazioni predefinite per lo stato dell&#39;ordine e lo stato dell&#39;ordine.

![Stati e stati dell’ordine](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

Lo stato di ciascun ordine è visualizzato nel _Stato_ colonna del _Ordini_ griglia.

![Stato ordine](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>Un ordine parzialmente rimborsato rimane in `Processing` stato fino a **_tutto_** gli articoli ordinati (inclusi gli articoli rimborsati) vengono spediti. Lo stato dell’ordine non viene modificato in `Complete` fino alla spedizione di ogni articolo dell&#39;ordine.

## Flusso di lavoro per stato ordine

![Flusso di lavoro per stato ordine](./assets/order-state-workflow.png)

## Stato predefinito

| Stato ordine | Codice di stato |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ricevuto | `received` | Questo stato è lo stato iniziale degli ordini inseriti quando è abilitato il posizionamento asincrono degli ordini. |
| Sospetta frode | `fraud` | A volte gli ordini pagati tramite PayPal o un altro gateway di pagamento sono contrassegnati come _Sospetta frode_. Questo stato significa che l’ordine non dispone di una fattura emessa e che anche l’e-mail di conferma non viene inviata. |
| Elaborazione | `processing` | Quando lo stato dei nuovi ordini è impostato su &quot;Elaborazione&quot;, il _Fattura automaticamente tutti gli articoli_ nella configurazione. Le fatture non vengono create automaticamente per gli ordini effettuati utilizzando la Gift Card, il Credito del Negozio, i Punti premio o altri metodi di pagamento offline. |
| Pagamento in sospeso | `pending_payment` | Questo stato viene utilizzato se l&#39;ordine viene creato e viene utilizzato PayPal o un metodo di pagamento simile. Ciò significa che il cliente è stato indirizzato al sito web del gateway dei pagamenti, ma non sono ancora state ricevute informazioni sulla restituzione. Questo stato cambia quando il cliente paga. |
| Revisione pagamento | `payment_review` | Questo stato viene visualizzato quando PayPal revisione pagamenti è attivato. |
| In sospeso | `pending` | Questo stato indica che non sono state sottomesse fatture e spedizioni. |
| In attesa | `holded` | Questo stato può essere assegnato solo manualmente. Puoi mettere in attesa qualsiasi ordine. |
| Completa | `complete` | Questo stato indica che l&#39;ordine è stato creato, pagato e spedito al cliente. |
| Chiuso | `closed` | Questo stato indica che a un ordine è stata assegnata una nota di credito e che il cliente ha ricevuto un rimborso. |
| Annullato | `canceled` | Questo stato viene assegnato manualmente nell’amministratore o, per alcuni gateway di pagamento, quando il cliente non paga entro il tempo specificato. |
| Rifiutato | `rejected` | Questo stato indica che un ordine è stato rifiutato durante l’elaborazione asincrona dell’ordine. Ciò si verifica quando si verifica un errore durante il posizionamento dell’ordine asincrono. |
| Storno annullato da PayPal | `paypay_canceled_reversal` | Questo stato indica che PayPal ha annullato lo storno. |
| PayPal in sospeso | `pending_paypal` | Questo stato significa che l&#39;ordine è stato ricevuto da PayPal, ma il pagamento non è ancora stato elaborato. |
| PayPal stornato | `paypal_reversed` | Questo stato indica che PayPal ha annullato la transazione. |

{style="table-layout:auto"}

## Stato ordine personalizzato

Oltre alle impostazioni predefinite per lo stato dell&#39;ordine, è possibile creare impostazioni personalizzate per lo stato dell&#39;ordine, assegnarle agli stati dell&#39;ordine e impostarne gli stati predefiniti. Lo stato dell’ordine indica la posizione dell’ordine all’interno del flusso di lavoro di elaborazione dell’ordine e lo stato dell’ordine assegna un’etichetta traducibile significativa alla posizione dell’ordine. Ad esempio, potrebbe essere necessario uno stato dell’ordine personalizzato come `packaging"`, `backordered`o uno stato specifico per le tue esigenze. Puoi creare un nome descrittivo per lo stato personalizzato e assegnarlo allo stato dell’ordine associato nel flusso di lavoro.

>[!NOTE]
>
>Nel flusso di lavoro dell’ordine vengono utilizzati solo i valori predefiniti dello stato dell’ordine personalizzati. I valori di stato personalizzati che non sono impostati come predefiniti possono essere utilizzati solo nella sezione dei commenti dell’ordine.

![Impostazioni stato ordine](./assets/order-status.png){width="700" zoomable="yes"}

### Creare uno stato dell’ordine personalizzato

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Create New Status]**.

   ![Crea nuovo stato ordine](./assets/order-status-new.png){width="600" zoomable="yes"}

1. Aggiornare il _[!UICONTROL Order Status Information]_sezione:

   - Immetti un **[!UICONTROL Status Code]** per riferimento interno. Il primo carattere deve essere una lettera (a-z) e il resto può essere costituito da qualsiasi combinazione di lettere e numeri (0-9). Utilizza il carattere di sottolineatura invece di uno spazio.

   - Per **[!UICONTROL Status Label]**, immetti un’etichetta che identifica l’impostazione dello stato sia in Admin che nella vetrina.

1. In _[!UICONTROL Store View Specific Labels]_immettere le etichette necessarie per le diverse visualizzazioni dello store.

1. Clic **[!UICONTROL Save Status]**.

### Assegnare uno stato dell&#39;ordine a uno stato

1. Il giorno _Stato ordine_ pagina, fai clic su **[!UICONTROL Assign Status to State]**.

   ![Assegna stato](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. Aggiornare il **[!UICONTROL Assignment Information]** eseguire le operazioni seguenti:

   - Scegli la **[!UICONTROL Order Status]** che desideri assegnare. Sono elencate per etichetta di stato.

   - Imposta **[!UICONTROL Order State]** al punto del flusso di lavoro a cui appartiene lo stato dell’ordine.

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_** L&#39;elenco include gli stati degli ordini assegnati predefiniti. Ad esempio, il `Pending` viene visualizzato lo stato predefinito dell’ordine al posto del `New` valore dello stato dell’ordine.

   - Per impostare questo stato come predefinito per lo stato dell&#39;ordine, selezionare **[!UICONTROL Use Order Status as Default]** casella di controllo.

     >[!NOTE]
     >
     >Nel flusso di lavoro dell&#39;ordine vengono utilizzati solo gli stati dell&#39;ordine predefiniti. Gli stati non predefiniti possono essere impostati solo nel **[!UICONTROL Order Comments]** in Admin.

   - Per rendere visibile questo stato dalla vetrina, seleziona la **[!UICONTROL Visible On Storefront]** casella di controllo.

   ![Assegna stato a stato](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Status Assignment]**.

### Modifica uno stato ordine esistente

1. In _[!UICONTROL Order Status]_nella griglia, aprire il record di stato in modalità di modifica.

1. Aggiorna le impostazioni dello stato in base alle esigenze.

1. Clic **[!UICONTROL Save Status]**.

### Rimuovere uno stato di ordine da uno stato assegnato

>[!NOTE]
>
>Non è possibile annullare l&#39;assegnazione di un&#39;impostazione di stato da uno stato se lo stato è in uso.

1. In _[!UICONTROL Order Status]_trovare il record dello stato dell&#39;ordine a cui annullare l&#39;assegnazione.

1. In _[!UICONTROL Action]_all&#39;estrema destra della riga, fare clic sul pulsante **[!UICONTROL Unassign]**collegamento.

   Nella parte superiore dell’area di lavoro viene visualizzato un messaggio che informa che lo stato dell’ordine è stato revocato. Sebbene l&#39;etichetta dello stato dell&#39;ordine sia ancora visualizzata nell&#39;elenco, non è più assegnata a uno stato. Impossibile eliminare le impostazioni dello stato dell&#39;ordine.

>[!NOTE]
>
>Se lo stato dell&#39;ordine predefinito viene rimosso dallo stato dell&#39;ordine, _**un altro**_ lo stato dell&#39;ordine è _**imposta automaticamente**_ come impostazione predefinita per questo stato dell’ordine.

## Notifica

I clienti possono tenere traccia dello stato dei loro ordini entro [Feed RSS](../merchandising-promotions/social-rss.md) se il feed RSS dell&#39;ordine è abilitato nella configurazione. Quando questa opzione è attivata, in ogni ordine viene visualizzato un collegamento al feed RSS.

### Abilita notifica stato ordine

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL RSS Feeds]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Order]** sezione.

1. Imposta **[!UICONTROL Customer Order Status Notification]** a `Enable`.

   ![Notifica stato ordine cliente](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Configurare le notifiche e-mail per i nuovi ordini

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales Emails]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Order]** sezione.

   ![Configurazione - Opzioni ordine](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL New Order Confirmation Email Sender]** a uno dei seguenti elementi:

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. Scegli i modelli da utilizzare per ogni tipo di cliente:

   - **[!UICONTROL New Order Confirmation Template]** : scegli un modello da utilizzare per i clienti con un account store registrato.
   - **[!UICONTROL New Order Confirmation Template for Guest]** - Scegliere un modello da utilizzare per i clienti guest senza un account del punto vendita registrato.

1. Per notificare il nuovo ordine a un&#39;altra persona, ad esempio un responsabile commerciale, immettere l&#39;indirizzo di posta elettronica **[!UICONTROL Send Order Email Copy To]**.

   Puoi aggiungere più indirizzi e-mail se è necessario più di un destinatario.

1. Imposta il **[!UICONTROL Send Order Email Copy Method]** a uno dei seguenti elementi:

   - `Bcc` - Viene inviata una sola e-mail relativa al nuovo ordine sia al cliente che al destinatario aggiuntivo, ma il cliente non vede che l’e-mail ricevuta è stata inviata anche al destinatario aggiuntivo.
   - `Separate Email` - Vengono inviate due e-mail separate, una al destinatario e una al cliente.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
