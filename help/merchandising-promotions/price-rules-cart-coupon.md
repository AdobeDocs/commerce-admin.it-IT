---
title: Codici coupon
description: Scopri come utilizzare i codici coupon con le regole del prezzo del carrello per applicare uno sconto quando viene soddisfatta una serie di condizioni.
exl-id: 4f2e6203-0de2-44eb-a5f7-edd7b5f714d1
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: f6f3dba7a43cbadd5ca8bdac15af8141cbf2d260
workflow-type: tm+mt
source-wordcount: '1895'
ht-degree: 0%

---

# Codici coupon

I codici coupon vengono utilizzati con [regole prezzo carrello](price-rules-cart.md) per applicare uno sconto quando viene soddisfatta una serie di condizioni. Ad esempio, è possibile creare un codice coupon per un gruppo di clienti specifico o per chiunque effettui un acquisto su un determinato importo. Per applicare il coupon a un acquisto, il cliente può inserire il codice del coupon nel carrello o eventualmente nel registratore di cassa del tuo negozio _brick and mortar_. Di seguito sono riportati alcuni modi in cui puoi utilizzare i coupon nel tuo negozio:

- Inviare coupon tramite e-mail ai clienti
- Produrre coupon stampati
- Creare coupon in-store per gli utenti di dispositivi mobili

I codici coupon possono essere inviati tramite e-mail o inclusi in newsletter, cataloghi e annunci pubblicitari. L&#39;elenco dei codici coupon può essere esportato e inviato a un servizio di stampa esterno. Puoi anche creare coupon in-store con un codice di risposta rapida che gli acquirenti possono scansionare con i loro smartphone. Il codice QR può essere collegato a una pagina del sito con ulteriori informazioni sulla promozione.

A partire dalla versione 2.4.7 di Commerce, gli acquirenti possono applicare più coupon a un carrello. Gli esercenti possono anche applicare più coupon utilizzando l’assistenza per lo shopping.

>[!NOTE]
>
>Le regole di prezzo del carrello con la stessa priorità non generano uno sconto combinato. Ogni regola (coupon) viene applicata separatamente ai prodotti corrispondenti, uno per uno, in base all’ID della regola di prezzo del carrello nel database. Per controllare l’ordine in cui vengono applicati gli sconti, l’Adobe consiglia di impostare una priorità diversa per ogni regola di prezzo del carrello aggiunto.

## Configurare i codici coupon

La lunghezza e il formato dei codici coupon generati automaticamente sono controllati dalla configurazione. I caratteri possono essere impostati su tutti i numeri, su tutte le lettere o su una combinazione. È possibile inserire un trattino a intervalli impostati per facilitarne la lettura e aggiungere un prefisso e un suffisso per associare il codice a una campagna o iniziativa specifica.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Promotions]**.

   ![Configurazione clienti - codici coupon specifici generati automaticamente](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Espandere la sezione **[!UICONTROL Auto Generated Specific Coupon Codes]**.

   ![Configurazione clienti - codici coupon specifici generati automaticamente](../configuration-reference/customers/assets/promotions-auto-generated-specific-coupon-codes.png){width="600" zoomable="yes"}

1. Immettere **[!UICONTROL Code Length]**, inclusi prefisso, suffisso e separatori.

1. Impostare **[!UICONTROL Code Format]** su uno dei seguenti valori:

   - `Alphanumeric`
   - `Alphabetical`
   - `Numeric`

1. Per **[!UICONTROL Code Prefix]**, immettere il valore che si desidera visualizzare all&#39;inizio di tutti i codici coupon.

1. Per **[!UICONTROL Code Suffix]**, immettere il valore che si desidera visualizzare alla fine di tutti i codici coupon.

1. Per **[!UICONTROL Dash Every X Characters]**, immettere il numero di caratteri tra ogni trattino.

   I codici coupon con pattern di trattino diversi sono considerati codici diversi, anche se i numeri sono gli stessi.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Crea coupon

>[!NOTE]
>
>Prima di creare i coupon, utilizzare il comando `bin/magento cron:run` per verificare che cron sia in esecuzione. Per ulteriori informazioni, vedere [Esegui cron dalla riga di comando](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html#run-cron-from-the-command-line) nella _Guida alla configurazione_.

### Metodo 1: creazione di un coupon specifico

1. Segui le istruzioni per creare una [regola prezzo carrello](price-rules-cart.md).

1. Nella sezione **[!UICONTROL Rule Information]**, impostare **[!UICONTROL Coupon]** su `Specific Coupon`.

1. Immettere un **[!UICONTROL Coupon Code]** da utilizzare con la promozione.

   Il formato del codice (numerico, alfanumerico o alfabetico) è determinato dalla [configurazione](#configure-coupon-codes).

1. Per limitare il numero di volte in cui è possibile utilizzare il coupon, eseguire le operazioni seguenti:

   - Immettere il numero di **[!UICONTROL Uses per Coupon]**.
   - Immettere il numero di **[!UICONTROL Uses per Customer]**.

   Per un utilizzo illimitato, lascia vuoti questi campi.

   ![Regola prezzo carrello - informazioni coupon](./assets/coupon-info.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >In caso di utilizzo simultaneo dello stesso coupon da parte di più clienti contemporaneamente, è possibile che il limite di utilizzo impostato possa essere superato a causa di un ritardo nell’elaborazione del coupon.

1. Per rendere valido il coupon per un periodo di tempo, effettuare le seguenti operazioni:

   - ![Magento Open Source](../assets/open-source.svg) (solo Magento Open Source) Completa le date **Da** e **A**. Per selezionare la data, fare clic sull&#39;icona **Calendario** (![Icona Calendario](../assets/icon-calendar.png)) accanto a ogni campo. Se lasci vuoto l’intervallo di date, la regola non scade.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Effettua una delle seguenti operazioni:

     **Opzione 1:** Pianifica un nuovo aggiornamento

      - Fare clic su **[!UICONTROL Schedule New Update]** nell&#39;angolo superiore destro della pagina.

        ![Pianifica aggiornamento](./assets/coupon-schedule-new-update.png){width="600" zoomable="yes"}

      - Immettere **[!UICONTROL Update Name]** e **[!UICONTROL Description]**.

      - Scegli la **Data inizio** e la **[!UICONTROL End Date]** dal Calendario ( ![Icona Calendario](../assets/icon-calendar.png) ). Se lasci vuoto l’intervallo di date, la regola non scade.

      - Al termine, fare clic su **[!UICONTROL Save]**.

        ![Regola prezzo carrello - modifica pianificata](./assets/coupon-scheduled-change.png){width="600" zoomable="yes"}

     **Opzione 2:** Assegna a un aggiornamento esistente:

      - Selezionare **[!UICONTROL Assign to Another Update]**.

      - Trovare l&#39;aggiornamento nell&#39;elenco e fare clic su **[!UICONTROL Select]**.

1. Completa la [regola prezzo carrello](price-rules-cart.md) in base alle esigenze.

### Metodo 2: generare un batch di coupon

La generazione di buoni sconto è un’operazione asincrona, che viene eseguita in background in modo da poter continuare a lavorare in Admin senza attendere il completamento dell’operazione. Il sistema visualizza un messaggio al completamento dell&#39;operazione.

1. Segui le istruzioni per creare una [regola prezzo carrello](price-rules-cart.md).

1. In **[!UICONTROL Coupon Code]** selezionare la casella di controllo **[!UICONTROL Use Auto Generation]**.

1. Per limitare il numero di volte in cui ogni cliente può utilizzare il coupon, immettere il numero di **[!UICONTROL Uses per Customer]**.

   ![Regola prezzo carrello - genera coupon con numerazione automatica](./assets/coupon-auto.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >In caso di utilizzo simultaneo dello stesso coupon da parte di più clienti contemporaneamente, è possibile che il limite di utilizzo impostato possa essere superato a causa di un ritardo nell’elaborazione del coupon.

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Manage Coupon Codes]** ed effettua le seguenti operazioni:

   ![Regola prezzo carrello - gestisci codici coupon](./assets/manage-coupon-codes.png){width="600" zoomable="yes"}

   - Per **[!UICONTROL Coupons Qty]**, immettere il numero di coupon che si desidera generare.

   - Immettere **[!UICONTROL Code Length]**, senza il prefisso, il suffisso o i separatori.

   - Impostare **[!UICONTROL Code Format]** su uno dei seguenti valori:

      - `Alphanumeric`
      - `Alphabetical`
      - `Numeric`

   - (Facoltativo) Immettere **[!UICONTROL Code Prefix]** da aggiungere all&#39;inizio del codice.

   - (Facoltativo) Immettere **[!UICONTROL Code Suffix]** da aggiungere alla fine del codice.

   - (Facoltativo) Per **[!UICONTROL Dash Every X Characters]**, immettere il numero di caratteri tra ogni trattino. Se, ad esempio, la lunghezza del codice è di 12 caratteri ed è presente un trattino ogni quattro caratteri, l&#39;aspetto sarà `xxxx-xxxx-xxxx`. I trattini facilitano la lettura e l&#39;immissione dei codici.

1. Al termine, fare clic su **[!UICONTROL Generate]**.

   Il sistema visualizza `Message is added to queue, wait to get your coupons soon`.

   Al termine del processo cron, viene visualizzato l’elenco dei codici generati.

   | Campo | Descrizione |
   |-------------|-------------|
   | [!UICONTROL Coupon Code] | Codice univoco del coupon creato che può essere utilizzato per ricevere condizioni speciali. |
   | [!UICONTROL Created] | Data di creazione del codice coupon. |
   | [!UICONTROL Used] | Indica se è stato utilizzato il coupon. |
   | [!UICONTROL Times Used] | Indica quante volte è stato utilizzato il codice coupon. |

   {style="table-layout:auto"}

È possibile esportare i codici coupon in un file CSV o Excel XML selezionando il formato di file e facendo clic su **[!UICONTROL Export]**.

Per eliminare i codici coupon, selezionare uno o più codici dall&#39;elenco. Selezionare `Delete` dal selettore **[!UICONTROL Actions]**, quindi fare clic su **[!UICONTROL Submit]**.

>[!NOTE]
>
>Anche se Commerce consente la configurazione di più codici coupon, un cliente può utilizzare un solo codice coupon nel carrello. Per consentire l&#39;utilizzo simultaneo di più codici coupon nel carrello, è possibile utilizzare un&#39;estensione corrispondente di [Commerce Marketplace](https://marketplace.magento.com/).

## Rapporto Coupon

Il rapporto _Coupon_ aggrega i dati di ogni coupon utilizzato durante un intervallo di date specifico. Poiché i coupon vengono applicati dal carrello, il rapporto include i dati di tutti i coupon riscattati, indipendentemente dallo [stato ordine](../stores-purchase/order-status.md). Di conseguenza, il rapporto potrebbe includere sia i totali previsti che quelli effettivi. Il rapporto può essere filtrato per una specifica vista negozio, periodo di tempo, stato dell’ordine e regola del prezzo del carrello.

Nell&#39;esempio seguente, il codice coupon &quot;H20&quot; è stato utilizzato da due clienti. Uno degli ordini è fatturato, ma l&#39;altro è ancora _in sospeso_. Nelle colonne Subtotale vendite previsto, Sconto vendite e Totale vendite vengono visualizzati gli importi aggregati di entrambi gli ordini, ma solo l&#39;ordine fatturato effettivo viene visualizzato nelle colonne Subtotale, Sconto e Totale. Ogni riga del rapporto rappresenta una singola promozione di coupon.

![Rapporto coupon](./assets/reports-coupons.png){width="600" zoomable="yes"}

### Eseguire il rapporto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. Se sono presenti più visualizzazioni archivio, impostare **[!DNL Store View]** nell&#39;angolo superiore sinistro per stabilire l&#39;ambito del report.

1. Per aggiornare le [statistiche](../getting-started/sales-reports.md#refresh-statistics) di vendita per il giorno, fai clic sul messaggio _Ultimo aggiornamento_ nella parte superiore dell&#39;area di lavoro.

   Fare quindi clic per selezionare la casella di controllo **[!UICONTROL Coupons]** e fare clic su **[!UICONTROL Refresh]**.

   Rapporto ![Coupon - aggiornamento statistiche](./assets/reports-coupons-refresh-statistics.png){width="600" zoomable="yes"}

1. Per filtrare i dati, eseguire le operazioni seguenti:

   ![Rapporto coupon - Filtri](./assets/reports-coupons-filters.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Date Used]** su uno dei seguenti:

      - `Order Created`
      - `Order Updated`

     Il report _Ordine aggiornato_ viene creato in tempo reale e non richiede un aggiornamento.

   - Per definire il periodo di tempo coperto dal report, impostare **[!UICONTROL Period]** su uno dei seguenti valori:

      - `Day`
      - `Month`
      - `Year`

   - Per definire l&#39;intervallo di date del report, immettere le date **Da** e **A** in formato M/G/AA.

   - Per stampare un report per uno specifico [stato ordine](../stores-purchase/order-status.md), impostare **[!UICONTROL Order Status]** su `Specified` e scegliere lo stato ordine dall&#39;elenco.

   - Per omettere righe senza dati dal report, impostare **[!UICONTROL Empty Rows]** su `No`.

   - Per definire l&#39;attività coupon inclusa nel rapporto, effettuare una delle seguenti operazioni:

      - Per includere tutte le attività coupon da tutte le regole di prezzo, impostare **[!UICONTROL Cart Price Rule]** su `Any`.
      - Per includere solo le attività correlate a una regola di prezzo specifica, impostare **[!UICONTROL Cart Price Rule]** su `Specified` e selezionare la regola di prezzo del carrello nell&#39;elenco.

1. Al termine dell&#39;esecuzione del report, fare clic su **[!UICONTROL Show Report]**.

   Il rapporto viene visualizzato nella parte inferiore della pagina.

### Opzioni filtro

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Date Used] | Identifica il campo data utilizzato come base del rapporto. Opzioni:<br/>**[!UICONTROL Order Created]**: genera il report in base alla data in cui l&#39;ordine è stato effettuato dal cliente. Per includere i dati più recenti, fai clic sul collegamento nel messaggio per aggiornare le statistiche.<br/>**[!UICONTROL Order Updated]**: genera il report in base alla data dell&#39;ultimo aggiornamento degli ordini. Questo report utilizza dati in tempo reale e non richiede l&#39;aggiornamento delle statistiche. |
| [!UICONTROL Period] | Determina il tipo di intervallo di date utilizzato per il rapporto. Opzioni: `Day` / `Month` / `Year` |
| [!UICONTROL From] | Indica la prima data nell&#39;intervallo di dati dell&#39;ordine inclusa nel rapporto. |
| [!UICONTROL To] | Indica l&#39;ultima data dell&#39;intervallo di dati dell&#39;ordine incluso nel rapporto. |
| [!UICONTROL Order Status] | Filtra il report in base allo stato dell&#39;ordine. Il rapporto può essere generato per tutti gli ordini o limitato a uno stato specifico dell’ordine. Opzioni: <br/>**[!UICONTROL Any]**: include tutti gli ordini indipendentemente dallo stato.<br/>**[!UICONTROL Specified]**: include solo gli ordini con lo stato specificato. Gli ordini annullati non sono inclusi nel rapporto. |
| [!UICONTROL Empty Rows] | Determina se il report include righe di dati vuoti che possono essere recuperate. Opzioni: `Yes` / `No` |
| [!UICONTROL Cart Price Rules] | Determina quali promozioni coupon includere nel rapporto. Opzioni:<br/>**[!UICONTROL Any]**: include informazioni sull&#39;ordine per qualsiasi promozione coupon utilizzata durante l&#39;intervallo di date specificato.<br/>**[!UICONTROL Specified]**: include solo le informazioni sull&#39;ordine per la promozione del coupon selezionata durante l&#39;intervallo di date specificato. |

{style="table-layout:auto"}

### Colonne report

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Interval] | Indica l’intervallo di date dell’utilizzo della cedola da includere nel rapporto. L’intervallo può essere un giorno, un mese, un anno o un intervallo di date specifico. La data intervallo viene formattata come negli esempi seguenti, in base al valore impostato nell&#39;impostazione **[!UICONTROL Period]**:<br/>`Day`: 6/21/19<br/>`Month`: 6/2019<br/>`Year`: 2019 |
| [!UICONTROL Coupon Code] | Codice sconto inserito dai clienti nel carrello per ricevere lo sconto. |
| [!UICONTROL Price Rule] | Nome della regola di prezzo associata al coupon. |
| [!UICONTROL Uses] | Il numero di volte in cui il coupon è stato utilizzato durante l’intervallo di date specificato per il rapporto. |
| [!UICONTROL Sales Subtotal] | Subtotale previsto da tutti gli ordini inseriti con il coupon. <br/>Il subtotale vendite rappresenta il subtotale aggregato di tutti gli ordini qualificati e include `Pending` ordini cliente non ancora fatturati. |
| [!UICONTROL Sales Discount] | Importo dello sconto previsto da tutti gli ordini emessi con la cedola. <br/>Lo sconto rappresenta l&#39;importo dello sconto aggregato di tutti gli ordini idonei e include `Pending` ordini cliente non ancora fatturati. |
| [!UICONTROL Sales Total] | Il totale complessivo previsto da tutti gli ordini effettuati con il buono sconto. Il totale vendite include tutte le spese di spedizione e imballaggio, meno l&#39;importo dello sconto. <br/>Il totale vendite rappresenta l&#39;importo totale aggregato di tutti gli ordini qualificati e include `Pending` ordini cliente non ancora fatturati. Il valore include il subtotale più la spedizione e la movimentazione, meno lo sconto, più l&#39;imposta. <br/> Calcolato da: `((Subtotal + Shipping & Handling) - Discount) + Tax` |
| [!UICONTROL Subtotal] | Subtotale aggregato da tutti gli ordini fatturati che hanno utilizzato la cedola. |
| [!UICONTROL Discount] | Sconto aggregato da tutti gli ordini fatturati che hanno utilizzato la cedola. |
| [!UICONTROL Total] | Totale aggregato di tutti gli ordini fatturati che hanno utilizzato la cedola. |

{style="table-layout:auto"}
