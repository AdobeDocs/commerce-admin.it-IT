---
title: Restituisce
description: Scopri il flusso di lavoro di restituzione e come rilasciare l’autorizzazione per la merce restituita.
exl-id: 9dde0360-aa99-4fc4-92ff-976d9874ffec
feature: Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Restituisce

A _autorizzazione merce restituita_ (RMA) può essere concesso ai clienti che richiedono la restituzione di un articolo per la sostituzione o il rimborso. In genere, il cliente contatta il commerciante per richiedere un rimborso. Se approvato, viene assegnato un numero RMA univoco per identificare il prodotto restituito. Nella configurazione, è possibile abilitare RMA per tutti i prodotti o consentire RMA solo per determinati prodotti. Il _[!UICONTROL Returns]_La griglia elenca le richieste di merce (RMA) restituite correnti e viene utilizzata per immettere nuove richieste di restituzione.

![Restituisce una griglia](./assets/return.png){width="600" zoomable="yes"}

Le RMA possono essere rilasciate per tipi di prodotto semplici, raggruppati, configurabili e in bundle. Tuttavia, le RMA non sono disponibili per i prodotti virtuali, i prodotti scaricabili e le carte regalo.

## Descrizioni delle colonne

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Select] | Seleziona le caselle di controllo per i resi da sottoporre a un&#39;azione, oppure utilizza il controllo di selezione nell&#39;intestazione della colonna. Opzioni: `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL RMA] | Identificatore numerico univoco assegnato a ogni ritorno |
| [!UICONTROL Requested] | Data e ora in cui è stato effettuato il reso |
| [!UICONTROL Order] | Numero univoco dell&#39;ordine originale |
| [!UICONTROL Ordered] | Data e ora in cui è stato effettuato l’ordine |
| [!UICONTROL Customer] | Il nome del cliente o dell&#39;acquirente che ha effettuato l&#39;ordine |
| [!UICONTROL Status] | Stato di ritorno. Opzioni: `Pending` / `Authorized` / `Partially Authorized` / `Approved` / `Rejected` / `Processed and Closed` / `Closed` |
| [!UICONTROL Action] | **[!UICONTROL View]** apre il ritorno in modalità di modifica. |

{style="table-layout:auto"}

## RMA e flusso di lavoro di ritorno

1. **Ricevi richiesta** - Se [abilitato](rma-configure.md#enable-rmas-for-your-store) per la vetrina, sia i clienti registrati che gli ospiti possono richiedere un RMA. È inoltre possibile [inviare una richiesta RMA in Admin](#create-a-return-request-in-the-admin).

2. **RMA emessa** - Dopo aver esaminato la richiesta, è possibile autorizzarla parzialmente, completamente o annullare la richiesta. Se autorizzi la restituzione e accetti di pagare per la spedizione di reso, puoi creare un ordine di spedizione dall&#39;amministratore con un vettore supportato.

3. **Merce ricevuta e prodotto restituito elaborato** - Il seguente diagramma di flusso descrive l&#39;ordine operativo per completare il processo di restituzione:

   ![Flusso di lavoro di restituzione prodotti](./assets/workflow-customer-returns.png){width="500"}

## Stato RMA

Durante il suo ciclo di vita, a un’autorizzazione di merce (RMA) restituita possono essere assegnati molti stati (ad esempio In sospeso o Autorizzata). Lo stato RMA indica l&#39;avanzamento di una richiesta RMA generata dall&#39;utente o dal commerciante.

| Stato | Descrizione |
|--- |--- |
| [!UICONTROL Pending] | Lo stato iniziale assegnato a una richiesta RMA quando viene generata da un utente nella vetrina o dal commerciante nell’amministratore. |
| [!UICONTROL Authorized] | Questo stato viene assegnato alla RMA quando tutti gli elementi richiesti sono autorizzati dall’esercente nell’Amministratore per le restituzioni. |
| [!UICONTROL Partially Authorized] | Questo stato viene assegnato alla RMA se uno qualsiasi degli elementi richiesti è stato negato e altri prodotti sono autorizzati. |
| [!UICONTROL Denied] | Questo stato viene assegnato alla RMA se tutti gli elementi richiesti vengono rifiutati dall’esercente nell’Amministratore per le restituzioni. |
| [!UICONTROL Return Received] | Questo stato viene assegnato dall&#39;esercente alla RMA quando gli elementi richiesti vengono ricevuti dall&#39;utente. |
| [!UICONTROL Return Partially Received] | Questo stato viene assegnato dall&#39;esercente alla RMA quando gli elementi richiesti vengono parzialmente restituiti e alcuni elementi non vengono elaborati. |
| [!UICONTROL Approved] | Questo stato viene assegnato dall&#39;esercente alla RMA quando gli elementi richiesti vengono approvati per l&#39;ulteriore elaborazione. |
| [!UICONTROL Rejected] | Questo stato viene assegnato dall&#39;esercente alla RMA quando gli elementi richiesti vengono rifiutati per essere elaborati ulteriormente. |
| [!UICONTROL Processed and Closed] | Questo stato viene assegnato dall&#39;esercente alla RMA quando tutti gli elementi richiesti vengono approvati per l&#39;ulteriore elaborazione. |
| [!UICONTROL Closed] | Questo stato viene assegnato dall&#39;esercente alla RMA quando gli elementi richiesti non vengono elaborati per la restituzione. |

{style="table-layout:auto"}

## Creare una richiesta di ritorno in Admin

Un esercente può creare una richiesta di restituzione dall’amministratore per conto del cliente. I clienti possono [creare una richiesta di ritorno](rma-customer-experience.md) nella vetrina di un negozio Adobe Commerce.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > **[!UICONTROL Returns]**.

1. Clic **[!UICONTROL New Return Request]**.

1. Per creare una richiesta di reso, fai clic su un ordine con un `Complete` stato.

1. Sotto _[!UICONTROL Return Information]_, seleziona la sezione **[!UICONTROL Return Items]**scheda.

1. Per aggiungere elementi da restituire, fai clic su **[!UICONTROL Add Items]**.

1. Seleziona la casella di controllo per il prodotto richiesto e fai clic su **[!UICONTROL Add Selected Product to returns]**.

1. Per **[!UICONTROL Requested]**, immettere il numero di elementi da restituire.

1. Imposta **[!UICONTROL Return Reason]** a uno dei seguenti elementi:

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   Se il motivo della restituzione è diverso dalle scelte elencate, è possibile immettere un valore personalizzato selezionando la `Other` opzione.

1. Imposta **[!UICONTROL Item Condition]** a uno dei seguenti elementi:

   - `Unopened`
   - `Opened`
   - `Damaged`

1. Imposta **[!UICONTROL Resolution]** a uno dei seguenti elementi:

   - `Exchange`
   - `Refund`
   - `Store Credit`

1. Per creare un ritorno, fai clic su **[!UICONTROL Submit Returns]**.

   ![Elementi RMA richiesti](./assets/return-item-request.png){width="600" zoomable="yes"}

   La richiesta RMA appena inviata viene visualizzata sul **[!UICONTROL Returns]** pagina con un `Pending` stato.
