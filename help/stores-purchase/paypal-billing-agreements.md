---
title: Accordi di fatturazione PayPal
description: Scopri come supportare i contratti di fatturazione PayPal e un metodo di pagamento all’interno del tuo Negozio.
exl-id: b0800b41-816a-4c48-a54d-41ddc1d586ce
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Accordi di fatturazione PayPal

Per semplificare il processo di pagamento, i clienti possono stipulare un contratto di fatturazione con PayPal come fornitore di servizi di pagamento. Durante il pagamento, il cliente sceglie il contratto di fatturazione come metodo di pagamento. Il sistema di pagamento verifica il contratto di fatturazione con il relativo numero univoco e addebita l&#39;importo al conto cliente. Con un contratto di fatturazione in vigore, non è più necessario che il cliente inserisca le informazioni di pagamento per ogni acquisto. I clienti possono gestire i propri accordi di fatturazione dal dashboard dell’account del cliente, dove lo stato di ciascuno di essi viene visualizzato come _Attivo_ o _Annullato_. Quando un contratto di fatturazione viene annullato, non può essere riattivato.

## Flusso di lavoro contratto di fatturazione

1. **Il cliente si iscrive a un contratto di fatturazione**. Dopo aver stipulato un contratto di fatturazione, è possibile aggiungere altri contratti di fatturazione solo dal conto cliente. Non esiste alcun limite al numero di accordi di fatturazione che un cliente può creare. I clienti possono utilizzare uno dei seguenti metodi per sottoscrivere accordi di fatturazione:

   - **Registrati all&#39;account cliente** - I clienti possono iscriversi a un contratto di fatturazione dai propri account cliente.
   - **Registrati al pagamento** - I clienti che pagano un acquisto con PayPal Express Checkout possono selezionare una casella di controllo per creare un contratto di fatturazione. Anche se il contratto di fatturazione non viene utilizzato per l&#39;ordine corrente, diventa disponibile come opzione del metodo di pagamento alla successiva immissione di un ordine da parte del cliente.
   - **Registrati dall&#39;amministratore del negozio** - Su richiesta del cliente, l&#39;amministratore del negozio può creare un ordine di vendita utilizzando il contratto di fatturazione del cliente.

1. **PayPal verifica e registra l&#39;accordo**. Quando il cliente effettua l&#39;ordine con il pagamento tramite contratto di fatturazione, l&#39;ID di riferimento del contratto di fatturazione e i dettagli di pagamento dell&#39;ordine di vendita vengono trasferiti a PayPal e registrati nel conto cliente, insieme alle informazioni di riferimento. Se il pagamento è autorizzato, viene creato un ordine in Commerce. L&#39;ID di riferimento del contratto di fatturazione viene inviato al cliente e al negozio.

## Gestisci accordi di fatturazione

Il _[!UICONTROL Billing Agreements]_Questa pagina elenca tutti gli accordi di fatturazione tra il tuo negozio e i suoi clienti. Gli esercenti possono filtrare i record in base alle informazioni relative al cliente o al contratto di fatturazione, inclusi l&#39;ID di riferimento del contratto di fatturazione, lo stato e la data di creazione. Ogni record include informazioni generali sul contratto di fatturazione e tutti gli ordini di vendita che lo hanno utilizzato come metodo di pagamento. È possibile visualizzare, annullare o eliminare i contratti di fatturazione dei clienti. Un contratto di fatturazione annullato può essere eliminato solo dall&#39;amministratore del punto vendita.

### Visualizza un contratto di fatturazione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Individuare il contratto di fatturazione nell&#39;elenco e fare clic per aprirlo.

Ogni pagina del contratto di fatturazione è costituita da due schede: _[!UICONTROL General Information]_e_[!UICONTROL Related Orders]_.

#### Informazioni generali

Questa scheda include le informazioni generali sul contratto di fatturazione:

- [!UICONTROL Reference ID]: identificatore numerico univoco assegnato al contratto di fatturazione corrente.
- [!UICONTROL Customer]: account del cliente assegnato al contratto di fatturazione corrente.
- [!UICONTROL Status]: stato contratto di pagamento.
- [!UICONTROL Created At]: data di creazione.
- [!UICONTROL Updated At]: data di aggiornamento.

![Visualizzazione contratto di fatturazione](./assets/billing-agreement-view.png){width="600" zoomable="yes"}

#### Ordini correlati

In questa scheda viene visualizzato l&#39;elenco degli ordini effettuati utilizzando il contratto di fatturazione corrente.

![Visualizzazione contratto di fatturazione](./assets/billing-agreement-related-orders.png){width="600" zoomable="yes"}

### Annullare un contratto di fatturazione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Individuare il contratto di fatturazione nell&#39;elenco e fare clic per aprirlo.

1. Nell’angolo in alto a destra, fai clic su **[!UICONTROL Cancel]**.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.

### Eliminare un contratto di fatturazione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Individuare il contratto di fatturazione nell&#39;elenco e fare clic per aprirlo.

1. Nell’angolo in alto a destra, fai clic su **[!UICONTROL Delete]**.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.

### Descrizioni delle colonne

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL ID] | Un identificatore numerico univoco assegnato a ogni contratto di fatturazione |
| [!UICONTROL Email] | E-mail di contatto di un cliente |
| [!UICONTROL First Name] | Nome di un cliente |
| [!UICONTROL Last Name] | Cognome di un cliente |
| [!UICONTROL Reference ID] | Identificatore di riferimento numerico univoco assegnato a ogni contratto di fatturazione |
| [!UICONTROL Status] | Stato contratto di pagamento. Opzioni: `Active` o `Canceled` |
| [!UICONTROL Created] | Data di creazione |
| [!UICONTROL Updated] | Data di aggiornamento |

{style="table-layout:auto"}

## Esperienza vetrina

I clienti che stipulano un accordo di fatturazione con un fornitore di servizi di pagamento possono effettuare acquisti ora e pagarli in un secondo momento, in base all&#39;accordo. Il

![Elenco dei contratti di fatturazione nel dashboard del cliente](./assets/billing-agreements-dashboard.png){width="700" zoomable="yes"}

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Reference ID] | Identificatore di riferimento numerico univoco assegnato a ogni contratto di fatturazione |
| [!UICONTROL Status] | Stato contratto di pagamento. Opzioni: `Active` o `Canceled` |
| [!UICONTROL Created At] | Data di creazione |
| [!UICONTROL Updated At] | Data di aggiornamento |
| [!UICONTROL Payment Method] | Un fornitore di servizi di pagamento di un contratto di fatturazione |
| [!UICONTROL View] | Pulsante utilizzato per visualizzare i contratti di fatturazione |

{style="table-layout:auto"}

### Creare un contratto di fatturazione

1. Dal dashboard dell’account, il cliente seleziona **[!UICONTROL Billing Agreements]**.

1. Sotto **[!UICONTROL New Billing Agreement]**, seleziona un provider di pagamenti.

1. Clic **[!UICONTROL Create]**.

Questa azione reindirizza il cliente al sito Web del sistema di pagamento.

![Nuovo contratto di fatturazione nel pannello di controllo dell’account cliente](./assets/create-billing-agreement-dashboard.png){width="700" zoomable="yes"}

### Visualizza un contratto di fatturazione

1. Dal dashboard dell’account, il cliente seleziona **[!UICONTROL Billing Agreements]**.

1. Seleziona il contratto di fatturazione e fa clic su **[!UICONTROL View]**.

![Visualizza contratto di fatturazione nel dashboard del cliente](./assets/view-billing-agreement.png){width="700" zoomable="yes"}

### Annullare un contratto di fatturazione

1. Dal dashboard dell’account, il cliente seleziona **[!UICONTROL Billing Agreements]**.

1. Seleziona il contratto di fatturazione e fa clic su **[!UICONTROL View]**.

1. Nell’angolo in alto a destra, fa clic su **[!UICONTROL Cancel]** e poi **[!UICONTROL OK]** per confermare.

>[!NOTE]
>
>Se un utente amministratore (commerciante) annulla il contratto di fatturazione, non può annullarlo nella vetrina. Il _Annullato_ per questo contratto viene visualizzato lo stato.
