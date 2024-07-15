---
title: '[!UICONTROL My Quotes]'
description: Scopri l’esperienza del cliente per le offerte, disponibile nel dashboard dell’account.
exl-id: 137f0a99-8f24-4838-b54b-b0ef2c39a32a
feature: B2B, Companies, Quotes
source-git-commit: 27b0c43f72faa2c2e8717fd5929f36d12f9e1b08
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---


# [!UICONTROL My Quotes]

Se i preventivi sono abilitati, nella sezione _[!UICONTROL My Quotes]_del dashboard dei conti cliente sono elencati tutti i preventivi inviati dal cliente. A seconda delle loro autorizzazioni, solo gli acquirenti che effettuano acquisti per conto di una società possono inviare richieste per negoziare il prezzo di un acquisto.

![Le mie citazioni](./assets/account-dashboard-my-quotes.png){width="700" zoomable="yes"}

L&#39;acquirente avvia il processo [inviando una richiesta](quote-request.md) di preventivo dal carrello. L&#39;e-mail viene scambiata tra l&#39;acquirente e il venditore durante il [processo di negoziazione](quote-price-negotiation.md). Per l&#39;acquirente, la pagina [!UICONTROL My Quotes] è il punto focale per tutte le comunicazioni tra l&#39;acquirente e il venditore durante il processo di negoziazione. Un acquirente che accetta il prezzo negoziato offerto dal venditore può passare direttamente alla pagina di pagamento dal preventivo. Impossibile aggiungere ulteriori sconti all&#39;offerta negoziata.

Un acquirente può completare le azioni seguenti durante la negoziazione di un preventivo:

* Rivedi prezzi e aggiornamenti articoli
* Tenere traccia del processo di negoziazione dalle sezioni [!UICONTROL Comments] e [!UICONTROL History]
* Modifica il preventivo per rimuovere gli elementi
* Comunica e negozia con il venditore aggiungendo note a livello di articolo e preventivo
* Invia un preventivo al venditore per la revisione
* Convertire l&#39;offerta in un ordine se i termini sono accettabili
* Chiudi il preventivo
* Elimina l&#39;offerta
* Funzionalità [!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponibile solo per i partecipanti al programma Beta"}

L&#39;esempio seguente mostra un preventivo che è stato aggiornato dall&#39;acquirente e inviato nuovamente al venditore per la revisione.


![Visualizzazione del preventivo per l&#39;acquirente](./assets/account-dashboard-my-quote-detail.png){width="700" zoomable="yes"}

Le offerte con lo stato `Updated` sono bloccate finché il venditore non restituisce il preventivo.

## Mostra virgolette

Con le [autorizzazioni richieste per il loro ruolo](account-company-roles-permissions.md), i clienti associati a un account aziendale possono visualizzare i preventivi richiesti da [utenti subordinati](account-company-structure.md). Gli amministratori della società possono visualizzare tutti i preventivi per l&#39;account della società.

1. Il cliente accede al proprio account nella vetrina.

1. Fai clic su **[!UICONTROL My Quotes]** nel menu di navigazione a sinistra.

1. Per visualizzare tutti i preventivi creati, fare clic sul collegamento **[!UICONTROL Show My Quotes]** (visualizzato solo per l&#39;amministratore della società o per l&#39;account con utenti subordinati).

1. Per visualizzare tutti i preventivi di tutti gli utenti della società, fare clic su **[!UICONTROL Show All Quotes]**.

## Visualizza un preventivo

1. Il cliente accede al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL My Quotes]**.

1. Trova il preventivo nell&#39;elenco e fa clic su **[!UICONTROL View]** nella colonna _[!UICONTROL Action]_.

## Stampare un preventivo

1. Nel preventivo aperto a destra della sezione _[!UICONTROL Items Quoted]_, il cliente fa clic su **[!UICONTROL Print]**.

1. Verifica **[!UICONTROL Destination]** come stampante o PDF.

1. Clic su **[!UICONTROL Print]**.

## Annullare una richiesta di preventivo

1. Nella virgoletta aperta immediatamente sopra la sezione Elementi citati fare clic su **[!UICONTROL Close quote]**.

   La richiesta è stata annullata e lo stato del preventivo cambia in `Closed`. Le virgolette chiuse rimangono nell&#39;elenco delle virgolette e rimangono elencate nella griglia _[!UICONTROL Quotes]_dell&#39;amministratore.

1. Per rimuovere le virgolette annullate dall&#39;elenco, fare clic su **[!UICONTROL Delete]**.

1. Quando viene richiesto di confermare, fa clic su **[!UICONTROL OK]**.

   Le virgolette chiuse vengono rimosse dall&#39;elenco delle virgolette. Tuttavia, rimane elencato nella griglia _[!UICONTROL Quotes]_in Admin, con lo stato `Closed`.

## Azioni preventivo

| Azione | Descrizione |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rinomina | [!BADGE Funzionalità 1.5.0-beta]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Disponibile solo per i partecipanti al programma Beta&quot;} Modificare il nome del preventivo |
| Crea una copia | [!BADGE 1.5.0-beta funzionalità]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Disponibile solo per i partecipanti al programma Beta&quot;} Un buyer può creare un nuovo preventivo dal preventivo corrente copiandolo e rinominandolo. |
| Chiudi preventivo | Quando un acquirente chiude un preventivo, non può riaprirlo. Se necessario, l&#39;acquirente può ricrearlo utilizzando l&#39;azione [!UICONTROL Create Copy]. Questa opzione non è disponibile se lo stato del preventivo è `Draft`. |
| Elimina offerta | Quando un acquirente elimina un preventivo, questo viene rimosso dal sistema e non è più disponibile. |
| Stampa | Apre un modulo di stampa per salvare l&#39;offerta come PDF, file o stamparla con una stampante configurata. |

## Descrizioni delle colonne

| Colonna | Descrizione |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Quote Name] | Nome assegnato alla richiesta di preventivo dall&#39;acquirente. |
| [!UICONTROL Created] | Data in cui è stata inviata la prima richiesta di preventivo. |
| [!UICONTROL Created By] | Il nome e il cognome dell&#39;acquirente che ha inviato la richiesta di preventivo. |
| [!UICONTROL Status] | Indica lo stato dell&#39;offerta. Lo stato di un preventivo può essere modificato solo da un&#39;azione dell&#39;acquirente o del venditore. <br/>**[!UICONTROL Submitted]**- La richiesta di offerta dell&#39;acquirente non è ancora stata aperta dal venditore. In questo stato, l&#39;acquirente può comunque modificare la richiesta di preventivo. Azioni disponibili: `View` / `Close` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Pending]** - Il venditore ha aperto la richiesta e sta per esaminarla e preparare una risposta. Azioni disponibili: `View` / `Close` <br/>**[!UICONTROL Updated]**- Il venditore ha inviato una risposta all&#39;acquirente e il pulsante _[!UICONTROL Proceed to Checkout]_è abilitato. In questo stato, il buyer può continuare a modificare il preventivo. Azioni disponibili: `View` / `Send for Review` / `Proceed to Checkout` / `Delete Quote` / `Close` / `Edit Quantity` / `Delete SKU` / `Add comments` / `Edit Shipping Address`<br/>**[!UICONTROL Open]**- L&#39;acquirente sta ancora aggiornando il preventivo e il pulsante_[!UICONTROL Proceed to Checkout]_ è disabilitato. Azioni disponibili: `View` / `Send for Review` / `Delete Quote` / `Edit quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` <br/>**[!UICONTROL Ordered]**- L&#39;acquirente ha inviato un ordine basato sul preventivo negoziato. Il preventivo è bloccato e non può essere modificato. Azione disponibile: visualizzazione<br/>**[!UICONTROL Closed]** - Il buyer ha terminato la negoziazione e annulla il preventivo. Il preventivo è bloccato e non può essere modificato né dall&#39;acquirente né dal venditore. Azioni disponibili: `View` / `Delete` <br/>**[!UICONTROL Declined]**- Il venditore ha rifiutato la richiesta di preventivo o di modifica proposta durante il processo di negoziazione. Un preventivo può essere rifiutato in qualsiasi fase del flusso di lavoro. Qualsiasi prezzo personalizzato viene rimosso dal preventivo. L&#39;acquirente può continuare a modificare il preventivo e inviarlo nuovamente oppure effettuare l&#39;acquisto con prezzi di catalogo standard. Azioni disponibili: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address`<br/>**[!UICONTROL Expired]** - La durata del preventivo è scaduta. Tutti i prezzi proposti vengono azzerati. L&#39;acquirente può completare l&#39;acquisto in base ai prezzi di catalogo standard o avviare un&#39;altra serie di negoziazioni. Azioni disponibili: `View` / `Send for Review` / `Delete Quote` / `Edit Quantity` / `Delete SKU` / `Add Comments` / `Edit Shipping Address` |

{style="table-layout:auto"}
