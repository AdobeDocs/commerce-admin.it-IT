---
title: Configura [!DNL Inventory Management] opzioni globali
description: Scopri come configurare le opzioni di configurazione  [!DNL Inventory Management]  predefinite per prodotto e stock per i siti web.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# Configura [!DNL Inventory Management] opzioni globali

Configura le opzioni di configurazione predefinite per prodotto e magazzino per i siti web. Alcune di queste impostazioni possono essere ignorate per prodotto tramite [Configurazione delle opzioni di prodotto](product-options.md). Per configurare le impostazioni di priorità della distanza, vedere [Configurazione dell&#39;algoritmo di priorità della distanza](distance-priority-algorithm.md).

## Configurare le opzioni di prodotto e stock a livello globale

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Inventory]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Stock Options]** e impostare le opzioni:

   ![Opzioni Stock](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Per regolare la quantità disponibile quando viene effettuato un ordine, impostare **[!UICONTROL Decrease Stock When Order is Placed]** su `Yes`.

   - Per restituire gli articoli alle scorte se un ordine viene annullato, **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** a `Yes`.

   - Per continuare a visualizzare nel catalogo i prodotti non più in magazzino, impostare **[!UICONTROL Display Out of Stock Products]** su `Yes`.

   - Se sono abilitati [avvisi sui prezzi](alert-setup.md), i clienti possono registrarsi per ricevere una notifica quando il prodotto è di nuovo disponibile.

   - Per impostare l&#39;inizio della visualizzazione dell&#39;ultima quantità di scorte rimanente nella pagina del prodotto, immettere un valore per **[!UICONTROL Only X left Threshold]**.

     Il messaggio inizia a essere visualizzato quando la quantità in magazzino raggiunge la soglia. Se ad esempio è impostato su `3`, il messaggio `Only 3 left` viene visualizzato quando la quantità in magazzino raggiunge le tre unità. Il messaggio viene modificato in modo da riflettere la quantità in magazzino, fino a quando la quantità non raggiunge zero.

   - Per visualizzare un messaggio &quot;Disponibile&quot; o &quot;Esaurito&quot; nella pagina del prodotto, impostare **[!UICONTROL Display Products Availability In Stock on Storefront]** su `Yes`.

   - Per controllare l&#39;inventario durante il caricamento di un prodotto nel carrello, impostare **[!UICONTROL Enable Inventory Check On Cart Load]** su `Yes`. Se questa opzione è disattivata, il controllo dell&#39;inventario viene ignorato. La disattivazione di questa opzione accelera il pagamento, soprattutto se nel carrello sono presenti molti articoli. Tuttavia, se salti la pre-convalida, i clienti potrebbero visualizzare errori &quot;esauriti&quot; in un secondo momento nel processo di pagamento.

   - Per mantenere la coerenza tra inventario e catalogo, impostare **[!UICONTROL Synchronize with Catalog]** su `Yes`. Se questa opzione è abilitata, i dati di inventario vengono regolati in base alle modifiche apportate al catalogo (ad esempio, prodotto rimosso, SKU prodotto modificato e tipo di prodotto modificato).

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Product Stock Options]** e impostare le opzioni:

   - Per attivare il [controllo inventario](enable.md) per il catalogo, impostare **[!UICONTROL Manage Stock]** su `Yes`.

     ![Opzioni Stock Di Prodotto](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Backorders]** su uno dei seguenti:

     | Opzione | Descrizione |
     | ----- | ----- |
     | `No Backorders` | [Gli ordini inevasi](backorders.md) non sono accettati quando il prodotto è esaurito. |
     | `Allow Qty Below 0` | Gli ordini inevasi vengono accettati quando la quantità scende sotto zero. |
     | `Allow Qty Below 0 and Notify Customer` | Gli ordini arretrati vengono accettati quando la quantità scende al di sotto di zero e il sistema notifica al cliente che l&#39;ordine può ancora essere effettuato. |

   - Immettere **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - Immettere un importo per **[!UICONTROL Out-of-Stock Threshold]**:

     | Valore | Descrizione |
     | ----- |-----|
     | Importo positivo | Se l&#39;opzione Ordini arretrati è disabilitata, immettere un importo positivo. |
     | Zero | Con gli ordini inevasi abilitati, l&#39;immissione di `0` consente ordini inevasi infiniti. |
     | Importo negativo | Se l&#39;opzione Ordini arretrati è abilitata, si consiglia di immettere un importo negativo. L&#39;importo viene aggiunto alla quantità di vendita. Ad esempio, immettere `-50` per consentire ordini fino a questo importo. |

   - Immettere **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** per il gruppo e gli importi selezionati.

   - Per **[!UICONTROL Notify for Quantity Below]**, immettere il livello azionario che attiva la notifica che l&#39;articolo è esaurito.

   - Per attivare incrementi di quantità per il prodotto, impostare **[!UICONTROL Enable Qty Increments]** su `Yes`. Quindi, per **[!UICONTROL Qty Increments]**, immettere il numero di articoli che devono essere acquistati per soddisfare il requisito.

     Ad esempio, un articolo venduto con incrementi di sei può essere acquistato in quantità di `6`, `12`, `18` e così via.

   - Per [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** è impostato su `No`. Quando si sottomette una nota di accredito, è necessario inserire e selezionare questa opzione per restituire le scorte alle origini.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Admin bulk operations]** e impostare le opzioni:

   ![Operazioni in blocco per amministratori](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Run asynchronously]** per eseguire operazioni in blocco in modo asincrono per azioni di massa sui prodotti

     Queste operazioni includono [assegnazione e annullamento dell&#39;assegnazione di origini](bulk-assignment.md) in blocco e [trasferimento dell&#39;inventario all&#39;origine](inventory-transfer.md). Raccoglie le azioni in blocco fino alla dimensione del batch asincrono, quindi le esegue. Questa opzione è disabilitata per impostazione predefinita. Si consiglia di rivedere le prestazioni con azioni in blocco prima dell’abilitazione.

     >[!NOTE]
     >
     >Per configurare e supportare i _gestori di code asincrone_, è necessario eseguire un comando tramite la riga di comando. Questo passaggio potrebbe richiedere l’assistenza degli sviluppatori. Vedere [Avvia consumer della coda messaggi](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) nella _Guida alla configurazione_.

   - Se abilitato, impostare **[!UICONTROL Asynchronous batch size]**. La dimensione predefinita del batch è 100. Quando i processi in blocco raggiungono questa quantità, il sistema la attiva.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
