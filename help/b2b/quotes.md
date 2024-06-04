---
title: Offerte negoziabili
description: Scopri i flussi di lavoro delle offerte e come fornire questo servizio agli account aziendali.
exl-id: c278818b-fa5a-4e7a-8ca2-c4b757da4f05
feature: B2B, Quotes
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Offerte negoziabili

Acquirenti e venditori utilizzano i Preventivi per gestire il processo di negoziazione per l&#39;aggiunta di un ordine, l&#39;aggiornamento delle quantità, la richiesta e l&#39;applicazione di sconti e così via, fino al raggiungimento di un accordo. Il processo di negoziazione dei preventivi può essere avviato da un acquirente autorizzato della società o da un rappresentante commerciale della società.

Le offerte possono essere avviate da un acquirente autorizzato della società o da un rappresentante commerciale. Dopo la creazione del preventivo, il processo di negoziazione inizia quando il buyer o il venditore sottomette il preventivo per la revisione. Il _Virgolette_ griglia che elenca ogni preventivo ricevuto e mantiene una cronologia della comunicazione tra acquirente e venditore. Utilizza lo standard [controlli sul posto di lavoro](../getting-started/admin-workspace.md) per filtrare l’elenco, modifica il layout delle colonne, salva le viste ed esporta i dati.

- Nella vetrina, gli acquirenti inviano il preventivo come [richiesta di negoziazione](quote-price-negotiation.md) il prezzo dal carrello. Durante la creazione della richiesta di preventivo, l&#39;acquirente può salvare il preventivo come bozza o inviarlo direttamente al venditore.

- Nell&#39;amministratore, i rappresentanti possono creare preventivi per conto dell&#39;acquirente della società. Durante la creazione del preventivo, il venditore può salvare il preventivo come bozza o inviarlo direttamente al buyer per avviare il processo di negoziazione.

Durante il processo di negoziazione, il preventivo può essere aggiornato solo dalla persona che rivede e propone le condizioni per ulteriori negoziazioni.

## Prerequisiti

I preventivi negoziabili sono disponibili solo se Adobe Commerce dispone delle seguenti impostazioni di configurazione:

- [L’estensione Adobe Commerce B2B è installata](install.md)
- [Funzioni B2B configurate](enable-basic-features.md)
   - Abilita account società
   - Abilita offerta B2B

## Flusso di lavoro preventivo

Le offerte possono essere ordinate dall&#39;acquirente o dal venditore.

**Passaggio 1: creazione di preventivi**

- **Offerta di richieste di acquisto** - L&#39;acquirente [richiede un preventivo](quote-request.md) dal carrello. La richiesta viene visualizzata nella _Le Mie Virgolette_ l&#39;elenco nel dashboard account dell&#39;acquirente e la notifica e-mail viene inviata al rappresentante commerciale assegnato all&#39;account aziendale. In Admin, la richiesta viene visualizzata nel _Virgolette_ grid, con stato `New`. Una richiesta di preventivo può essere modificata dall&#39;acquirente fino a quando non viene aperta dal venditore.

  ![Virgolette](./assets/quote-request-from-shopping-cart.png){width="700" zoomable="yes"}


- **Rappresentante commerciale** — Un rappresentante commerciale può [creare un preventivo](sales-rep-initiates-quote.md) dall’amministratore per conto di un acquirente aziendale specifico. Il rappresentante commerciale deve aggiornare il preventivo per aggiungere prodotti e altre informazioni, ad esempio sconti e note, all&#39;acquirente. Il rappresentante commerciale può salvare il preventivo come `draft` o inviarlo all&#39;acquirente per avviare la negoziazione. In stato di bozza, il preventivo è visibile solo al venditore. Una volta inviato il preventivo, lo stato è `Submitted`. Non può essere modificato dal venditore finché l&#39;acquirente non lo rispedisce indietro.

  ![Venditore che avvia un preventivo dell&#39;acquirente dalla griglia Preventivi dell&#39;Amministratore](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}


**Passaggio 2: revisione e negoziazione dei preventivi**

**Il venditore visualizza la richiesta e invia una risposta** - Nell&#39;amministratore, il venditore visualizza la richiesta di preventivo. Lo stato dell&#39;offerta cambia in `Pending`e l&#39;acquirente non può apportare alcuna modifica. Il [il venditore risponde](quote-price-negotiation.md) offrendo prezzi scontati per i prodotti del preventivo, inserisce un commento e invia nuovamente il preventivo all&#39;acquirente. L&#39;acquirente e il rappresentante commerciale ricevono una notifica via e-mail che informa che il venditore ha risposto.

**L&#39;acquirente visualizza il preventivo del venditore e invia una risposta** - L&#39;acquirente fa clic sul collegamento nella notifica e-mail per aprire il preventivo o apre il preventivo da _Le Mie Virgolette_ pagina del dashboard dell’account. L&#39;acquirente può lasciare note al venditore a livello di articolo riga o preventivo e rimuovere gli articoli.

L&#39;acquirente e il venditore possono continuare il processo di negoziazione fino a quando non viene raggiunto un accordo o il venditore rifiuta il preventivo. Se l&#39;acquirente apporta modifiche al preventivo, ovvero aggiungendo o rimuovendo prodotti o modificando quantità di prodotti, il preventivo deve essere restituito al venditore per la revisione.

**Passaggio 4: l&#39;acquirente accetta il preventivo** - L&#39;acquirente accetta il prezzo proposto e continua a effettuare il pagamento. Impossibile aggiungere ulteriori sconti all&#39;offerta negoziata.

## Risorse del ruolo B2B per i preventivi dei punti vendita

Le opzioni di configurazione per i preventivi sono controllate utilizzando [risorse ruolo](../systems/permissions-user-roles.md#role-resources). Queste risorse ruolo devono essere impostate per il ruolo utente amministratore assegnato all&#39;amministratore archivio.

Per concedere l&#39;accesso alle funzioni di preventivo nell&#39;amministratore, passare a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, selezionare il ruolo e passare a [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] nel_ Risorse per il ruolo _albero.

## Applicare un’azione

In Amministrazione, gli amministratori e i venditori B2B possono gestire le offerte dalla griglia delle offerte utilizzando [!UICONTROL Actions] menu.

![Virgolette](./assets/quotes-grid.png){width="700" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > **[!UICONTROL Quotes]**.

1. Nella prima colonna della griglia selezionare la casella di controllo per ogni record a cui si desidera applicare l&#39;azione.

1. In **[!UICONTROL Actions]** seleziona l’azione da applicare.

### Visualizza un preventivo

1. In **[!UICONTROL Actions]** per un record, fare clic su **[!UICONTROL View]**.

1. Per rispondere alla richiesta del cliente, seguire le istruzioni e iniziare [negoziazione dei prezzi](quote-price-negotiation.md) processo.

### Visualizza attività offerta

Visualizzare la sequenza temporale della negoziazione, la comunicazione e altre attività di offerta dall&#39; [!UICONTROL Comments] e [!UICONTROL History Log]—le informazioni includono modifiche di stato, aggiornamenti alle informazioni su clienti e spedizione, aggiornamenti su articoli e prezzi e altre informazioni importanti.

1. Apri un preventivo.

1. Visualizzare i commenti e la cronologia delle negoziazioni dei preventivi scorrendo fino a **[!UICONTROL Negotiation]**, e selezione **[!UICONTROL Comments]** e **[!UICONTROL History Log]**.

   ![Visualizza cronologia](./assets/quote-view-history.png){width="400"}

1. La cronologia viene anche tracciata a livello di elemento riga.

   ![Visualizza cronologia elemento riga](./assets/quote-view-line-item-history.png){width="400"}


### Rifiuta una richiesta di offerta

Solo le richieste di preventivo con un `Open` lo stato può essere rifiutato.

1. Selezionare ogni richiesta di offerta aperta che si desidera rifiutare.

1. Imposta il _[!UICONTROL Actions]_controllo a `Declined`.

1. Quando richiesto, immettere il motivo del rifiuto e fare clic su **[!UICONTROL Confirm]**.

   ![Rifiuta offerta?](./assets/quote-decline-confirm.png){width="400"}


## Descrizioni delle colonne

| Colonna | Descrizione |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Per selezionare le virgolette da sottoporre a un&#39;azione, selezionare la casella di controllo o utilizzare il controllo di selezione nell&#39;intestazione di colonna. Opzioni: Seleziona tutto / Deseleziona tutto |
| [!UICONTROL ID] | Identificatore numerico univoco assegnato quando una richiesta di preventivo viene inviata dal carrello di un acquirente. Quando si visualizzano i dettagli dell&#39;offerta, l&#39;ID viene visualizzato nella parte superiore della pagina, invece del nome dell&#39;offerta. |
| [!UICONTROL Name] | Nome assegnato a una richiesta di preventivo da parte dell&#39;acquirente. |
| [!UICONTROL Created Date] | La data e l&#39;ora in cui il buyer ha inviato per la prima volta la richiesta di preventivo. |
| [!UICONTROL Company] | Il nome della società per conto della quale un acquirente presenta una richiesta di offerta. |
| [!UICONTROL Submitted By] | Il nome e il cognome dell&#39;acquirente della società che invia una richiesta di preventivo. |
| [!UICONTROL Last Updated] | La data e l&#39;ora dell&#39;ultima comunicazione tra l&#39;acquirente e il venditore relativa al preventivo. |
| [!UICONTROL Sales Rep] | Nome e cognome del rappresentante commerciale che gestisce l&#39;account dell&#39;acquirente. |
| [!UICONTROL Quote Total (Base)] | Il prezzo totale dei prodotti da acquistare in base al preventivo originale. L’importo totale viene visualizzato nella valuta di base del sito web e nella valuta della vetrina. |
| [!UICONTROL Quote Total (Negotiated)] | Il prezzo totale dei prodotti da acquistare in base al preventivo negoziato. Questo totale viene calcolato automaticamente dal sistema e include tutti gli sconti a livello di riga o preventivo applicati dal venditore. L’importo totale viene visualizzato nella valuta di base del sito web e nella valuta della vetrina. |
| [!UICONTROL Status] | Indica lo stato corrente di una richiesta di preventivo. Lo stato di un preventivo può essere modificato solo da un&#39;azione dell&#39;acquirente o del venditore. Vedere anche le impostazioni di stato della [account dell&#39;acquirente](account-dashboard-my-quotes.md).<ul><li>**[!UICONTROL New]** - L&#39;acquirente ha presentato una richiesta di preventivo, che non è stata tuttavia visualizzata dal venditore. La richiesta può essere aggiornata dall&#39;acquirente fino a quando non viene aperta dal venditore.</li><li>**[!UICONTROL Draft]** - Il venditore crea un preventivo provvisorio per un acquirente. Il preventivo non è visibile all&#39;acquirente finché il venditore non aggiunge i dettagli dell&#39;offerta (articoli, quantità, sconto e così via) e non invia il preventivo all&#39;acquirente.</li> <li>**[!UICONTROL Open]** - Il venditore ha aperto la richiesta e sta esaminando la richiesta e preparando una risposta. </li><li>**[!UICONTROL Submitted]** - Il venditore ha inviato una risposta all&#39;acquirente. Impossibile modificare il record del preventivo durante il processo di negoziazione.</li><li>**[!UICONTROL Client Reviewed]** - L&#39;acquirente ha visto la risposta del venditore e sta preparando una risposta.</li><li>**[!UICONTROL Updated]** - L&#39;acquirente ha inviato una risposta, che però non è stata vista dal venditore.</li><li>**[!UICONTROL Ordered]** - L&#39;acquirente ha inoltrato l&#39;ordine in base al preventivo negoziato.</li><li>**[!UICONTROL Closed]** - L&#39;acquirente ha annullato la richiesta di preventivo.</li><li>**[!UICONTROL Declined]** - Il venditore ha rifiutato la richiesta di preventivo. Eventuali prezzi personalizzati vengono rimossi dal preventivo e il record è bloccato da ulteriori modifiche.</li><li>**[!UICONTROL Expired]** - L&#39;acquirente non ha risposto alla risposta del venditore entro il termine stabilito e il preventivo non è più valido.</li></ul> |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Apre la richiesta di preventivo e conserva una registrazione della negoziazione tra l&#39;acquirente e il venditore. |

{style="table-layout:auto"}

## Barra dei pulsanti

| Pulsante | Descrizione |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Send] | Invia il preventivo aggiornato come risposta alla richiesta di informazioni dell&#39;acquirente. Questo pulsante è disattivato se il venditore è in attesa di una risposta da parte dell&#39;acquirente. |
| [!UICONTROL Back] | Torna a _Virgolette_ senza salvare le modifiche. |
| [!UICONTROL Create Copy] | [!BADGE Funzionalità 1.5.0-beta]{type=Informative url=&quot;/help/b2b/release-notes.md&quot; tooltip=&quot;Disponibile solo per i partecipanti ai programmi beta&quot;} Creare un nuovo preventivo dal preventivo corrente copiandolo e rinominandolo. Quando viene aperta la nuova virgoletta, il nome predefinito è `<original quote name> (copy)`. Modificare il nome modificando il valore in [!UICONTROL Name] e salvare l&#39;offerta come bozza. |
| [!UICONTROL Print] | Invia l&#39;offerta a una stampante o la salva come file PDF. |
| [!UICONTROL Create a copy] | Crea una copia del preventivo denominato `<original quote name> (copy)` e lo apre. Rinominare e aggiornare il nuovo preventivo in base alle esigenze prima di salvarlo come bozza o di inviarlo all&#39;acquirente. |
| [!UICONTROL Save as Draft] | Salva le modifiche apportate al preventivo, ma non lo restituisce all&#39;acquirente. |
| [!UICONTROL Decline] | Rifiuta la richiesta di negoziare i prezzi, sia nell&#39;indagine iniziale che durante le negoziazioni in corso. Quando un preventivo viene rifiutato, il venditore deve aggiungere un commento per spiegare la decisione. Quando un preventivo viene rifiutato, tutti i prezzi negoziati vengono reimpostati sui valori originali. Questo pulsante è disabilitato mentre il venditore è in attesa di una risposta dall&#39;acquirente. |

{style="table-layout:auto"}

## Virgoletta di esempio

Nella figura seguente viene illustrato un esempio della vista dei dettagli delle virgolette in Amministrazione con alcune impostazioni configurate.

![Virgoletta di esempio](./assets/quote-full.png){width="700" zoomable="yes"}


>[!NOTE]
>
>[!BADGE Funzionalità 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponibile solo per i partecipanti ai programmi beta"}
