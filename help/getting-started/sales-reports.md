---
title: Rapporti sulle vendite
description: Il [!DNL Commerce] i rapporti sulle vendite consentono di tenere traccia di ordini, imposte, fatture, spedizione, rimborsi, coupon e liquidazione PayPal.
exl-id: 928a407f-cbed-4114-ad0b-ee227383bf36
feature: Reporting, Orders
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 1%

---

# Rapporti sulle vendite

La selezione dei rapporti sulle vendite include Ordini, Imposta, Fatturato, Spedizione, Rimborsi, Coupon e Liquidazione PayPal.

## Filtri per i rapporti

Puoi generare un rapporto sulle vendite per un intero sito web o per un negozio. I rapporti sulle vendite possono essere filtrati per intervallo di tempo, data e stato.

![Filtri per i rapporti sulle vendite](./assets/tax-report.png){width="600"}

Per filtrare un rapporto sulle vendite, impostare le opzioni seguenti:

| Opzione | Descrizione |
|--- |--- |
| [!UICONTROL Date Used] | Imposta i dati da utilizzare per il report. |
| [!UICONTROL Period] | Il periodo per il quale vengono utilizzati i dati: Giorno/Mese/Anno. |
| [!UICONTROL From/To] | Utilizzato per definire i dati di ricerca per data di inizio e di fine. |
| [!UICONTROL Order Status] | Indica lo stato dell’ordine |
| [!UICONTROL Empty Rows] | Indica se aggiungere righe vuote al report. |

## [!UICONTROL Orders Report]

Il [!UICONTROL Orders Report] include il numero di ordini effettuati e annullati, con totali per vendite, importi fatturati, rimborsati, imposte riscosse, spese di spedizione e sconti.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Orders]**.

1. In **[!UICONTROL Filter]** , selezionare le opzioni del periodo di reporting e lo stato dell&#39;ordine utilizzati per compilare il rapporto.

1. Clic **[!UICONTROL Show Report]**.

![Ordini - Report record](./assets/order-report-records.png){width="600"}

## [!UICONTROL Tax Report]

Il [!UICONTROL Tax Report] include la regola fiscale applicata, l&#39;aliquota, il numero di ordini e l&#39;importo dell&#39;imposta addebitata.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Tax]**.

1. In **[!UICONTROL Filter]** , selezionare le opzioni del periodo di reporting e lo stato dell&#39;ordine utilizzati per compilare il rapporto.


1. Clic **[!UICONTROL Show Report]**.

![Report fiscale](./assets/tax-report-records.png){width="600"}

## [!UICONTROL Invoice Report]

Il [!UICONTROL Invoice Report] include il numero di ordini e fatture durante il periodo di tempo, con gli importi fatturati, pagati e non pagati.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Invoiced]**.

1. In **[!UICONTROL Filter]** , selezionare le opzioni del periodo di reporting e lo stato dell&#39;ordine utilizzati per compilare il rapporto.

1. Clic **[!UICONTROL Show Report]**.

![Rapporto Fatture](./assets/sales-invoiced.png){width="600"}

## [!UICONTROL Shipping Report]

Il [!UICONTROL Shipping Report] include il numero di ordini per il vettore o il metodo di spedizione utilizzato, inclusi gli importi per le vendite totali e la spedizione totale.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Shipping]**.

1. In **[!UICONTROL Filter]** , selezionare le opzioni del periodo di reporting e lo stato dell&#39;ordine utilizzati per compilare il rapporto.

1. Clic **[!UICONTROL Show Report]**.

![Rapporto di spedizione](./assets/shipping.png){width="600"}

## [!UICONTROL Refunds Report]

Il [!UICONTROL Refunds Report] include il numero di ordini rimborsati e l&#39;importo totale rimborsato online e offline.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Refunds]**.

1. In **[!UICONTROL Filter]** , selezionare le opzioni del periodo di reporting e lo stato dell&#39;ordine utilizzati per compilare il rapporto.

1. Clic **[!UICONTROL Show Report]**.

![Rapporto Rimborsi](./assets/sales-refunds.png){width="600"}

## [!UICONTROL Coupons Report]

Il [!UICONTROL Coupons Report] include ogni codice coupon utilizzato durante l&#39;intervallo di tempo specificato, la regola prezzo correlata e il numero di volte utilizzate, con totali e subtotali per vendite e sconti.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Coupons]**.

1. In **[!UICONTROL Filter]** , selezionare le opzioni del periodo di reporting e lo stato dell&#39;ordine utilizzati per compilare il rapporto.

1. Clic **[!UICONTROL Show Report]**.

Per ulteriori informazioni sull&#39;utilizzo di [!UICONTROL Coupons Report] per raccogliere i dati per le campagne promozionali, consulta [Segnalazione di coupon](../merchandising-promotions/price-rules-cart-coupon.md#coupons-report) nel _Guida al merchandising e alle promozioni_.

<!--- ![Coupons Report](./assets/sales-coupons.png) need coupon data  -->

## [!UICONTROL PayPal Settlement Reports]

Il [Rapporti di liquidazione PayPal] La pagina include il tipo di evento, ad esempio una transazione con carta di debito, le date di inizio e di fine, l&#39;importo lordo e le relative commissioni. Il report può essere aggiornato automaticamente con i dati più recenti di PayPal. Sono disponibili opzioni di filtro per l&#39;intervallo di date, il conto dell&#39;esercente, l&#39;ID transazione, l&#39;ID fattura o l&#39;ID di riferimento PayPal.

Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL PayPal Settlement]**.

![Rapporto liquidazione PayPal](./assets/reports-sales-paypal-settlement.png){width="600"}

Per ulteriori informazioni sull&#39;utilizzo di [!UICONTROL PayPal Settlement Reports] per recuperare informazioni su ogni transazione PayPal che influisce sulla liquidazione dei fondi, vedi [Report liquidazione PayPal](../stores-purchase/paypal-settlement-reports.md) nel _Guida ai negozi e all’esperienza di acquisto_.

## [!UICONTROL Braintree Settlement Report]

Il [Braintree](../stores-purchase/braintree.md) Il rapporto di liquidazione può essere filtrato in base alla data di creazione, all&#39;importo, allo stato, al tipo di transazione, al tipo di pagamento, all&#39;ID transazione, all&#39;ID ordine, all&#39;ID pagamento PayPal, al tipo, all&#39;ID conto esercente o all&#39;ID batch di regolamenti. Il rapporto contiene l&#39;ID transazione, l&#39;ID ordine, l&#39;ID pagamento PayPal, il tipo, la data di creazione, l&#39;importo, il codice di liquidazione, lo stato, il testo della risposta di liquidazione, gli ID rimborso, l&#39;ID conto esercente, l&#39;ID batch di liquidazione e la divisa.

Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Sales]_>**[!UICONTROL Braintree Settlement]**.

<!--- ![Braintree Settlement Report](./assets/braintree-settlement.png) need a Braintree connection to update report screen -->

## Esportare rapporti

1. Per esportare il report, selezionare il tipo di file: `Excel XML` o `CSV`

1. Clic **[!UICONTROL Export]**.

## Aggiorna statistiche

Per ridurre l&#39;impatto sulle prestazioni derivante dalla generazione di rapporti sulle vendite, [!DNL Commerce] calcola e memorizza le statistiche richieste per ciascun rapporto. Anziché ricalcolare le statistiche ogni volta che viene generato un rapporto, vengono utilizzate le statistiche memorizzate, a meno che non vengano aggiornate. Per includere i dati più recenti, è necessario aggiornare le statistiche del rapporto prima di generare un rapporto sulle vendite.

![Aggiorna statistiche](./assets/refresh-stats.png){width="700"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Reports]** > _[!UICONTROL Statistics]_>**[!UICONTROL Refresh Statistics]**.

1. Nell’elenco, seleziona la casella di controllo per ogni rapporto da aggiornare.

1. Imposta il **[!UICONTROL Actions]** controllo a uno dei seguenti elementi:

   - `Refresh Lifetime Statistics`
   - `Refresh Statistics for the Last Day`

1. Clic **[!UICONTROL Submit]**.
