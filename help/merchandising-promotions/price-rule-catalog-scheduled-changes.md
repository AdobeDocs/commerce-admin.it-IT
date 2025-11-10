---
title: Modifiche pianificate per le regole prezzo catalogo
description: Scopri come applicare le regole del prezzo di catalogo alla pianificazione come parte di una campagna e raggruppate con altre modifiche al contenuto.
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: e4c18621d0607446b48bf2447ac1a978d33ac24a
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# Modifiche pianificate per le regole prezzo catalogo

{{ee-feature}}

La casella Modifiche pianificate viene visualizzata nella parte superiore della pagina quando viene salvata o aggiornata una nuova regola prezzo. Le regole del prezzo del catalogo possono essere applicate secondo programma come parte di una campagna e raggruppate con altre modifiche al contenuto. Puoi creare una campagna in base alle modifiche pianificate per una regola di prezzo o applicare le modifiche a una campagna esistente.

![Regola prezzo catalogo - modifiche pianificate](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## Funzionamento degli aggiornamenti programmati delle regole di prezzo

- Tutti gli aggiornamenti pianificati vengono applicati consecutivamente. Ciò significa che qualsiasi entità può avere un solo aggiornamento pianificato alla volta.

- Qualsiasi aggiornamento pianificato viene applicato a tutte le visualizzazioni dello store entro il relativo intervallo di tempo. Di conseguenza, un’entità non può avere diversi aggiornamenti pianificati per diverse visualizzazioni dello store contemporaneamente. Tutti i valori degli attributi di entità all’interno di tutte le visualizzazioni archivio, che non sono influenzati dall’aggiornamento pianificato corrente, vengono presi dai valori predefiniti e non dal precedente aggiornamento pianificato.

- Se nella stessa campagna sono in esecuzione più regole di prezzo, l&#39;impostazione Priorità della regola di prezzo determina quale regola ha la precedenza. Per ulteriori informazioni, consulta [Gestione temporanea dei contenuti](../content-design/content-staging.md).

## Chiusura di una vendita di una regola di prezzo in un momento specifico

Se una regola di prezzo attiva è stata creata senza una data di fine e occorre terminarla in un momento specifico, non è possibile modificare l&#39;aggiornamento pianificato esistente per aggiungere una data di fine. È invece necessario creare un nuovo aggiornamento pianificato che modifichi lo stato della regola in `Inactive`. Imposta la data di inizio di questo nuovo aggiornamento sulla data e sull&#39;ora in cui desideri che termini la vendita.

## Pianificare un aggiornamento a una regola del prezzo di catalogo

1. Nella barra laterale _Amministratore_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**Regola prezzo catalogo**.

1. Apri la regola in modalità di modifica.

1. Nella casella **[!UICONTROL Scheduled Changes]** nella parte superiore della pagina, fare clic su **[!UICONTROL Schedule New Update]**.

1. Con l&#39;opzione **[!UICONTROL Save as a New Update]** selezionata, eseguire le operazioni seguenti:

   - Per **[!UICONTROL Update Name]**, immettere un nome per l&#39;aggiornamento della regola.

   - Immettere un breve **[!UICONTROL Description]** dell&#39;aggiornamento, specificando come o perché è applicato.

   - Utilizza _Calendario_ (![Icona Calendario](../assets/icon-calendar.png)) per scegliere **[!DNL Start Date]** e **[!UICONTROL End Date]** per rendere effettiva la modifica pianificata. Per creare una modifica di tipo aperto, lasciare vuota la data di fine.

   ![Regole prezzo catalogo - nuove modifiche pianificate](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >La data/ora di inizio e di fine è determinata dalla data/ora e dal fuso orario predefiniti del pannello di amministrazione, non dal fuso orario di un particolare sito web. Considera il fuso orario del sito web per determinare correttamente gli orari di inizio e fine. Crea regole separate per i siti web in fusi orari diversi che devono iniziare e/o fermarsi in orari locali specifici.

1. Scorri verso il basso fino alla sezione **[!UICONTROL Rule Information]** e modifica la regola in base alle esigenze.

   Puoi pianificare le modifiche per qualsiasi parametro della regola, inclusi i siti web (ambito)/gruppi di clienti per la regola, le condizioni della regola e le azioni applicate dalla regola. Per ulteriori informazioni, vedere [Creazione di una regola del prezzo catalogo](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >Ogni volta che si aggiornano i parametri delle informazioni sulle regole, verificare che _[!UICONTROL Status]_sia impostato correttamente. Se si desidera che la modifica generi una regola applicata attivamente, impostare lo stato su `Active`.

1. Al termine, fare clic su **[!UICONTROL Save]**.

   La modifica pianificata viene visualizzata nella parte superiore della pagina, con le date di inizio e di fine della campagna.

## Modificare una modifica di regola pianificata

>[!NOTE]
>
>Se una campagna è collegata a più di una regola del prezzo di catalogo, è possibile modificarla solo dal [Dashboard di gestione temporanea del contenuto](../content-design/content-staging-dashboard.md).

1. Nella casella **[!UICONTROL Scheduled Changes]** nella parte superiore della pagina, fare clic su **[!UICONTROL View/Edit]**.

1. Apporta le modifiche necessarie all’aggiornamento pianificato.

1. Fare clic su **[!UICONTROL Save]**.

## Anteprima della modifica della regola pianificata

1. Nella casella **[!UICONTROL Scheduled Changes]** nella parte superiore della pagina, fare clic su **[!UICONTROL Preview]**.

   L’anteprima apre una nuova scheda del browser che carica la vetrina con la modifica pianificata applicata. Passa a un prodotto interessato dalla modifica.

   ![Anteprima modifica pianificata](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. Nell&#39;angolo superiore sinistro della finestra Anteprima fare clic su **[!UICONTROL Calendar]**.

   I dettagli del calendario mostrano altre campagne pianificate per lo stesso giorno. Ogni record dell’elenco è un aggiornamento separato della regola.

   ![Elenco di aggiornamenti pianificati per una data specifica](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. Per visualizzare in anteprima un giorno o un&#39;ora diversa, fare clic sull&#39;icona Calendario **[!UICONTROL Date & Time]** ![Calendario](../assets/icon-calendar.png) ed eseguire le operazioni seguenti:

   - Scegli una data e/o un’ora diversa.

   - Fare clic su **[!UICONTROL Preview]**.

1. Per tornare al calendario, fare clic su **[!UICONTROL Calendar]** nell&#39;intestazione della pagina Anteprima.

   Da qui è possibile effettuare le seguenti operazioni:

   **Condividi un collegamento all&#39;anteprima**

   Per condividere un collegamento all&#39;anteprima dello store con altri utenti amministratori, fare clic su **[!UICONTROL Share]**. Copia il collegamento negli Appunti e incollalo nel corpo di un messaggio e-mail.

   >[!NOTE]
   >
   >Se il tuo ruolo [dispone dell&#39;accesso](../systems/permissions-user-roles.md) per gestire gli account utente amministratore, puoi creare o aggiornare un account utente esistente con autorizzazioni di amministratore in modo da poter condividere il collegamento di anteprima.

   **Modifica l&#39;ambito dell&#39;anteprima**

   Per visualizzare le modifiche pianificate per diverse visualizzazioni dello store, fare clic su **[!UICONTROL Scope]** nell&#39;intestazione della pagina Anteprima. Scegliere la visualizzazione del sito Web, dello store o dello store che si desidera visualizzare in anteprima.

1. Se necessario, tornare al calendario e fare clic su **[!UICONTROL View/Edit]** nella colonna _[!UICONTROL Action]_per aprire un altro aggiornamento pianificato.
