---
title: Persistenza carrello
description: Scopri in che modo un carrello permanente tiene traccia degli articoli del carrello non acquistati e salva le informazioni per la visita successiva del cliente.
exl-id: 95c336b3-77ac-4cf6-8fb5-23f4ac4b67d6
feature: Shopping Cart, Configuration
source-git-commit: 26d4bb35c6e1878a8ea8c5f05a982559e5d6dc35
workflow-type: tm+mt
source-wordcount: '1475'
ht-degree: 0%

---

# Persistenza carrello

Un carrello acquisti permanente tiene traccia degli articoli non acquistati che vengono lasciati nel carrello e salva le informazioni per la visita successiva del cliente. I clienti _ricordati_ possono far ripristinare il contenuto dei loro carrelli alla prossima visita al tuo negozio.

L’utilizzo di un carrello persistente può contribuire a ridurre il numero di carrelli abbandonati e ad aumentare le vendite. È importante comprendere che il carrello persistente non espone mai informazioni sensibili dell’account. Mentre il carrello acquisti persistente è in uso, sia i clienti registrati che gli acquirenti ospiti devono accedere a un account esistente o creare un account prima di passare attraverso il pagamento. Per gli acquirenti ospiti, un carrello persistente è l’unico modo per recuperare informazioni da una sessione precedente.

Per gestire l&#39;utilizzo della persistenza del carrello per il sito o all&#39;interno di specifiche visualizzazioni dello store, puoi [configurare le impostazioni del carrello acquisti persistente](#configure-a-persistent-cart). Per ulteriori informazioni su come queste impostazioni influiscono sull&#39;esperienza dell&#39;acquirente nella vetrina, vedi [Flusso di lavoro del carrello permanente](#persistent-cart-workflow).

>[!NOTE]
>
>Quando utilizzi un carrello persistente, ti consigliamo di impostare la durata della sessione del server e del cookie di sessione su un periodo di tempo lungo. Per ulteriori informazioni, vedere [Durata sessione](../customers/customer-online-options.md).

Per utilizzare il carrello acquisti persistente, il browser del cliente deve essere impostato in modo da consentire i cookie. Esistono due tipi di cookie utilizzati per le operazioni del carrello:

- **Cookie di sessione** - Un cookie di sessione a breve termine esiste durante una singola visita al sito e scade quando il cliente se ne va o dopo un periodo di tempo impostato.

- **Cookie persistente** - Un cookie persistente a lungo termine continua a esistere dopo la fine della sessione e salva un record del contenuto del carrello acquisti del cliente per riferimento futuro.

## Flusso di lavoro del carrello persistente

Quando il carrello acquisti permanente è [abilitato](#configure-a-persistent-cart), il flusso di lavoro dipende da:

- I valori delle impostazioni _Abilita Memorizza_ e _Cancella persistenza alla disconnessione_
- La decisione del cliente di selezionare o deselezionare la casella di controllo _Ricorda utente_
- Quando il cookie persistente viene cancellato

Quando viene applicato un cookie persistente, nell&#39;intestazione della pagina viene visualizzato il collegamento `Not Jane Smith?`. Questo prompt consente al cliente di terminare la sessione persistente e iniziare a lavorare come ospite o di accedere come un altro cliente. Il sistema conserva una registrazione del contenuto del carrello, anche se il cliente successivamente utilizza diversi dispositivi per effettuare acquisti nel negozio. Ad esempio, un cliente può aggiungere un articolo al carrello da un computer portatile, aggiungere altri articoli da un dispositivo mobile e completare il processo di pagamento da un tablet.

Esiste un cookie persistente indipendente separato per ogni browser. Se il cliente utilizza più browser durante la visita al tuo store durante una singola sessione persistente, le modifiche apportate in un browser si riflettono in qualsiasi altro browser al momento dell’aggiornamento della pagina. Quando il carrello acquisti persistente è abilitato, il tuo negozio crea e mantiene un cookie persistente separato per ogni browser utilizzato da un cliente per accedere o creare un account.

### Esempio: sessione aperta in un computer condiviso

Jane sta finendo il suo shopping di vacanza con una sessione persistente. Aggiunge un regalo per John al suo carrello, e qualcosa per sua madre. Poi va in cucina per uno spuntino.

John si siede al computer per fare qualche acquisto rapido mentre Jane è in cucina. Senza notare il link `Not Jane Smith?` in alto, trova un bel regalo per Jane e lo aggiunge al carrello. Quando va a controllare e accede come se stesso, entrambi gli elementi nel carrello di Jane vengono aggiunti al suo carrello. John ha talmente fretta da non notare gli elementi aggiuntivi durante la _revisione dell&#39;ordine_ e invia l&#39;ordine. Il carrello di Jane ora è vuoto, e John ha comprato tutti i regali.

### Ricordami

I clienti possono selezionare la casella di controllo _Ricorda utente_ nella pagina di accesso per salvare il contenuto dei carrelli acquisti.

| Ti Ricordi Di Me? | Risultato |
| ------------ |  ------ |
| Selezionato | Crea un cookie persistente e salva il contenuto del carrello per la successiva sessione di accesso del cliente. |
| Non selezionato | Non crea un cookie persistente e non salva le informazioni del carrello per la successiva sessione di accesso del cliente. |

{style="table-layout:auto"}

### Continua persistenza alla disconnessione - no

| Azione | Risultato |
| ------ | ------ |
| Accesso del cliente | Richiama il cookie persistente oltre al cookie di sessione, già in uso. |
| Disconnessione cliente | Elimina il cookie di sessione ma il cookie persistente rimane attivo. Al successivo accesso, il cliente ripristina gli elementi del carrello o li aggiunge a eventuali nuovi elementi inseriti nel carrello. |
| Il cliente non si disconnette e il cookie di sessione scade | Il cookie persistente rimane attivo. |

{style="table-layout:auto"}

### Cancella persistenza alla disconnessione

| Azione | Risultato |
| ------ | ------ |
| Accesso del cliente | Richiama il cookie persistente oltre al cookie di sessione, già in uso. |
| Disconnessione cliente | Elimina entrambi i cookie. |
| Il cliente non si disconnette ma il cookie di sessione scade | Il cookie persistente rimane attivo. |

{style="table-layout:auto"}

## Impostazioni ed effetti del carrello persistenti

| Impostazioni | Effetto |
|----------|--------|
| **[!UICONTROL Enable Remember Me]** è impostato su `No`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**ha un valore qualsiasi.<br/><br/>La casella di controllo** Ricorda utente **non è disponibile nella pagina di accesso e registrazione. | Il cookie persistente non viene utilizzato. |
| **[!UICONTROL Enable Remember Me]** è impostato su `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**ha un valore qualsiasi.<br/><br/>** Ricorda utente **non selezionato. | Il cookie di sessione viene applicato come di consueto; il cookie persistente non viene utilizzato. |
| **[!UICONTROL Enable Remember Me]** è impostato su `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**è impostato su `Yes`.<br/><br/>** Ricorda **è impostato su `Yes`. | Quando un cliente effettua l’accesso, vengono applicati entrambi i cookie. Quando un cliente si disconnette, entrambi i cookie vengono eliminati. Se un cliente non effettua l’accesso ma il cookie di sessione scade, viene comunque utilizzato il cookie persistente. A parte la disconnessione, il cookie persistente viene eliminato quando la sua durata si esaurisce o quando il cliente fa clic sul collegamento `Not Jane Smith`. |
| **[!UICONTROL Enable Remember Me]** è impostato su `Yes`.<br/><br/>**[!UICONTROL Clear Persistence on Log Out]**è impostato su `No`.<br/><br/>** Ricorda **è impostato su `Yes` | Quando un cliente effettua l’accesso, vengono applicati entrambi i cookie. Quando un cliente si disconnette, il cookie di sessione viene eliminato e la sessione persistente continua. Il cookie persistente viene eliminato quando il suo ciclo di vita termina o quando il cliente fa clic sul collegamento `Not Jane Smith`. |

{style="table-layout:auto"}

## Configurare un carrello permanente

Durante l’impostazione di un carrello permanente, puoi specificare la durata dei cookie e le opzioni che desideri rendere disponibili per le varie attività dei clienti.

Per ulteriori informazioni sul modo in cui il flusso di lavoro del cliente viene determinato da queste impostazioni, vedere [Flusso di lavoro del carrello permanente](#persistent-cart-workflow).

>[!NOTE]
>
>Se il cookie di sessione scade durante l’accesso del cliente, il cookie persistente rimane attivo.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Persistent Shopping Cart]**.

1. Per abilitare il carrello acquisti permanente e visualizzare opzioni aggiuntive, impostare **[!UICONTROL Enable Persistence]** su `Yes`.

   ![Abilitazione e configurazione della persistenza del carrello](../configuration-reference/customers/assets/persistent-shopping-cart-general.png){width="600" zoomable="yes"}

   Per ulteriori informazioni su ciascuna di queste impostazioni di configurazione, vedere [_Riferimento configurazione_](../configuration-reference/customers/persistent-shopping-cart.md)

   >[!NOTE]
   >
   >Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare queste impostazioni.

1. Per **[!UICONTROL Persistence Lifetime (seconds)]**, immettere il periodo di tempo, in secondi, in cui si desidera che il cookie persistente duri.

   Il valore predefinito di 31.536.000 secondi è uguale a un anno. Il tempo massimo consentito è di 100 anni.

1. Imposta **[!UICONTROL Enable "Remember Me"]** su uno dei seguenti:

   - `Yes` - Visualizza la casella di controllo _Ricorda utente_ nella pagina di accesso del tuo negozio, in modo che i clienti possano scegliere di salvare le informazioni del carrello acquisti.

   - `No` - La persistenza può ancora essere abilitata, ma ai clienti non viene data la possibilità di scegliere se salvare le informazioni.

1. Per preselezionare la casella di controllo _Ricorda utente_ per il cliente, impostare **[!UICONTROL Remember Me Default Value]** su `Yes`.

   Il cliente può deselezionare questa opzione se lo desidera.

1. Imposta **[!UICONTROL Clear Persistence on Log Out]** su uno dei seguenti:

   - `Yes` - Il carrello viene cancellato quando un cliente registrato si disconnette.

   - `No` - Il carrello viene salvato quando un cliente registrato si disconnette.

   >[!NOTE]
   >
   >Se il cookie di sessione scade mentre il cliente è ancora connesso, il cookie persistente rimane in uso.

1. Imposta **[!UICONTROL Persist Shopping Cart]** su uno dei seguenti:

   - `Yes` - Se il cookie di sessione scade, il cookie persistente viene mantenuto. Se un acquirente ospite successivamente effettua l’accesso o crea un account, il carrello viene ripristinato.

   - `No` - Il carrello non viene mantenuto per gli ospiti dopo la scadenza del cookie di sessione.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Imposta **[!UICONTROL Persist Wish List]** per determinare se lo stato degli elenchi dei desideri del cliente viene mantenuto al termine della sessione:

   - `Yes` - Il contenuto della lista dei desideri viene salvato al termine della sessione.

   - `No` - La lista dei desideri non viene salvata al termine della sessione.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Imposta **[!UICONTROL Persist Recently Ordered Items]** per determinare se lo stato degli elementi ordinati di recente viene mantenuto al termine della sessione:

   - `Yes` - Lo stato degli elementi ordinati di recente viene salvato al termine della sessione.

   - `No` - Lo stato degli elementi ordinati di recente non viene salvato al termine della sessione.

1. Imposta **[!UICONTROL Persist Currently Compared Products]** su `Yes` o `No`.

1. Imposta **[!UICONTROL Persist Comparison History]** su `Yes` o `No`.

1. Imposta **[!UICONTROL Persist Recently Viewed Products]** su `Yes` o `No`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Imposta **[!UICONTROL Persist Customer Group Membership and Segmentation]** per determinare se lo stato dell&#39;appartenenza al gruppo e i criteri di segmentazione del cliente vengono mantenuti al termine della sessione:

   - `Yes` - Lo stato dei dati di segmentazione e appartenenza al gruppo del cliente viene salvato al termine della sessione.

   - `No` - Lo stato dei dati di segmentazione e appartenenza al gruppo del cliente non viene salvato al termine della sessione.

1. Fare clic su **[!UICONTROL Save Config]**.
