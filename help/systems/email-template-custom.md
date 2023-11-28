---
title: Personalizzare i modelli e-mail
description: Scopri come personalizzare i modelli e-mail per ogni visualizzazione di siti web, store o store.
exl-id: d328b84d-fab7-4956-9071-2d8848f7c21e
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 0%

---

# Personalizzare i modelli e-mail

Commerce include un modello e-mail predefinito per la sezione del corpo di ogni messaggio inviato dal sistema. Per creare il messaggio completo, il modello per il contenuto del corpo viene combinato con i modelli di intestazione e piè di pagina. Il contenuto è formattato con HTML e CSS e può essere facilmente modificato e personalizzato aggiungendo [Variabili](variables-predefined.md) e [widget](../content-design/widgets.md). I modelli e-mail possono essere personalizzati per ogni sito web, store o visualizzazione store. Se utilizzi modelli personalizzati, assicurati di aggiornare la [configurazione del sistema](email-templates.md#configure-email-templates) per garantire che venga utilizzato il modello corretto.

![Esempio: anteprima e-mail di benvenuto](./assets/email-template-preview.png){width="500" zoomable="yes"}

I modelli predefiniti includono il logo e le informazioni di archiviazione e possono essere utilizzati senza ulteriori personalizzazioni. Tuttavia, come best practice, è consigliabile visualizzare ogni modello e apportare le modifiche necessarie prima di inviarlo ai clienti.

- [Modello intestazione](email-template-custom.md#header-template)
- [Modello piè di pagina](email-template-custom.md#footer-template)
- [Modelli di messaggio](email-template-custom.md#message-templates)

![Modelli e-mail](./assets/email-templates.png){width="700" zoomable="yes"}

## Informazioni sul modello

| Campo | Descrizione |
| ----- | ----------- |
| [!UICONTROL Template Name] | Nome del modello personalizzato. |
| [!UICONTROL Insert Variable] | Inserisce una variabile nel modello in corrispondenza della posizione del cursore. |
| [!UICONTROL Template Subject] | L&#39;oggetto del modello viene visualizzato nella colonna Oggetto e può essere utilizzato per ordinare e filtrare i modelli nell&#39;elenco. |
| [!UICONTROL Template Content] | Il contenuto del modello in HTML. |
| [!UICONTROL Template Styles] | Tutte le dichiarazioni di stile CSS necessarie per formattare il modello possono essere immesse nel _[!UICONTROL Template Styles]_casella. |

{style="table-layout:auto"}

## Modello intestazione

Dopo aver completato [configurazione](email-templates.md#configure-email-templates), il modello di intestazione e-mail include il logo collegato al negozio. Se hai una conoscenza di base di HTML, puoi facilmente utilizzare [variabili predefinite](variables-predefined.md) per aggiungere le informazioni di contatto del punto vendita all&#39;intestazione.

### Passaggio 1: Carica il modello predefinito

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Clic **[!UICONTROL Add New Template]**.

1. In **[!UICONTROL Load default template]** , fare clic sul pulsante **[!UICONTROL Template]** e scegli `Magento_Email` > `Header`.

   ![Intestazione modello e-mail - Carica modello predefinito](./assets/email-template-select-default-header.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Load Template]**.

   Il codice HTML e le variabili del modello vengono visualizzati nel modulo.

### Passaggio 2: Personalizzare il modello

1. Inserisci il **[!UICONTROL Template Name]** per l’intestazione personalizzata.

1. Immetti un **[!UICONTROL Template Subject]** per organizzare meglio i modelli.

   Nella griglia, l’elenco dei modelli può essere ordinato e filtrato in base al _[!UICONTROL Subject]_colonna.

   ![Informazioni sull’intestazione del modello e-mail](./assets/email-template-information.png){width="600" zoomable="yes"}

1. In **[!UICONTROL Template Content]** , modificare il HTML in base alle esigenze.

   >[!NOTE]
   >
   >Quando lavori nel codice del modello, fai attenzione a non sovrascrivere nulla che sia racchiuso tra parentesi graffe.

1. Per inserire un [variabile](variables-reference.md), posiziona il cursore nel codice in cui desideri inserire la variabile e fai clic su **[!UICONTROL Insert Variable]**.

1. Scegli la variabile da inserire.

   ![Modello intestazione - Inserisci variabile](./assets/email-template-insert-variable.png){width="600" zoomable="yes"}

   Quando viene selezionata una variabile, viene visualizzata una [tag markup](markup-tags.md) per la variabile viene inserito nel codice.

   Anche se le variabili dell’indirizzo e-mail del negozio sono quelle più spesso incluse nell’intestazione, puoi immettere il codice per qualsiasi sistema o [variabile personalizzata](variables-custom.md) direttamente nel modello.

1. Se devi effettuare una dichiarazione CSS, inserisci gli stili nella sezione **[!UICONTROL Template Styles]** casella.

1. Quando sei pronto per rivedere il tuo lavoro, fai clic su **[!UICONTROL Preview Template]**.

   Apporta le modifiche necessarie al modello.

1. Al termine, fai clic su **[!UICONTROL Save Template]**.

   L’intestazione personalizzata viene ora visualizzata nell’elenco dei modelli e-mail disponibili.

### Passaggio 3: Aggiornare la configurazione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Nella griglia, individuare la visualizzazione archivio che si desidera configurare e fare clic su **[!UICONTROL Edit]** nel _[!UICONTROL Action]_colonna.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Transactional Emails]** sezione.

1. Scegli la **[!UICONTROL Header Template]** viene utilizzato come impostazione predefinita per le notifiche e-mail.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

![Configurazione della progettazione delle e-mail transazionali: modello di intestazione](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Modello piè di pagina

Il piè di pagina del modello e-mail contiene la riga di chiusura e di firma del messaggio e-mail. È possibile modificare la chiusura per adattarla al proprio stile e aggiungere ulteriori informazioni, ad esempio il nome e l&#39;indirizzo dell&#39;azienda sotto il proprio nome.

### Passaggio 1: Carica il modello predefinito

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Clic **[!UICONTROL Add New Template]**.

1. In **[!UICONTROL Load default template]** , fare clic sul pulsante **[!UICONTROL Template]** e scegli `Magento_Email` > `Footer`.

1. Clic **[!UICONTROL Load Template]**.

   Il codice HTML e le variabili del modello vengono visualizzati nel modulo.

### Passaggio 2: Personalizzare e visualizzare in anteprima il modello

1. Inserisci il **[!UICONTROL Template Name]** per il piè di pagina personalizzato.

1. Immetti un **[!UICONTROL Template Subject]** per organizzare meglio i modelli.

   Nella griglia, i modelli possono essere ordinati e filtrati in base al _[!UICONTROL Subject]_colonna.

   ![Piè di pagina modello e-mail - Informazioni](./assets/email-template-footer-information.png){width="600" zoomable="yes"}

1. In **[!UICONTROL Template Content]** , modificare il HTML in base alle esigenze.

   >[!NOTE]
   >
   >Quando lavori nel codice del modello, fai attenzione a non sovrascrivere nulla che sia racchiuso tra parentesi graffe.

1. Per inserire un [variabile](variables-reference.md), posiziona il cursore nel codice in cui desideri inserire la variabile e fai clic su **[!UICONTROL Insert Variable]**.

1. Scegli la variabile da inserire.

   Quando viene selezionata una variabile, viene visualizzata una [tag markup](markup-tags.md) per la variabile viene inserito nel codice.

   Anche se le variabili Contatto store sono quelle più spesso incluse nel piè di pagina, puoi immettere il codice per qualsiasi sistema o [variabile personalizzata](variables-custom.md) direttamente nel modello.

1. Se devi effettuare una dichiarazione CSS, inserisci gli stili nella sezione **[!UICONTROL Template Styles]** casella.

### Passaggio 3: Aggiornare la configurazione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Nella griglia, individuare la visualizzazione archivio che si desidera configurare e fare clic su **[!UICONTROL Edit]** nel _[!UICONTROL Action]_colonna.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Transactional Emails]** sezione.

1. Scegli la **[!UICONTROL Footer Template]** viene utilizzato come piè di pagina predefinito nelle notifiche e-mail.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

![Configurazione della progettazione delle e-mail transazionali: modello di piè di pagina](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

## Modelli di messaggio

Il processo di personalizzazione del corpo di ogni messaggio è lo stesso utilizzato per personalizzare l’intestazione o il piè di pagina. L’unica differenza è il modello di messaggio per ogni attività o evento che attiva una notifica. Puoi utilizzare i modelli così come sono o personalizzarli in base alla tua voce e al tuo marchio. Oltre al testo del modello, è disponibile un’ampia selezione di [predefinito](variables-predefined.md) variabili e [personalizzato](variables-custom.md) variabili che puoi creare e incorporare nel modello.

### Passaggio 1: Carica il modello predefinito

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Clic **[!UICONTROL Add New Template]**.

   ![Modelli e-mail - Carica modello predefinito](./assets/email-templates-message-load-default.png){width="600" zoomable="yes"}

1. Effettua le seguenti operazioni:

   - Sotto **[!UICONTROL Load default template]**, scegli il **[!UICONTROL Template]** che desideri personalizzare.

   - Clic **[!UICONTROL Load Template]**.

### Passaggio 2: Personalizzare il modello

1. Per **[!UICONTROL Template Name]**, immetti un nome per il modello personalizzato.

1. Se necessario, modificare il **[!UICONTROL Template Subject]**.

   Questa è la prima riga del messaggio, che è la formula di apertura predefinita. Puoi lasciarla così com’è, oppure inserire qualcosa di più descrittivo.

1. Prendi nota della **[!UICONTROL Currently Used For]** percorso del modello, che è il percorso utilizzato per aggiornare la configurazione.

   ![Modelli e-mail - informazioni sul modello](./assets/email-template-message-information.png){width="600" zoomable="yes"}

1. In **[!UICONTROL Template Content]** , modificare il HTML in base alle esigenze.

   Il contenuto è costituito da una combinazione di tag HTML, direttive CSS, variabili e testo.

   >[!NOTE]
   >
   >Quando lavori nel codice del modello, fai attenzione a non sovrascrivere accidentalmente il codice racchiuso tra parentesi graffe.

1. Per inserire una variabile, posizionare il cursore nel codice nel punto in cui si desidera visualizzare la variabile.

   La selezione delle variabili varia in base al modello e include i valori consentiti [predefinito](variables-predefined.md) e [personalizzato](variables-custom.md) variabili, se disponibili.

1. Clic **[!UICONTROL Insert Variable]** e scegli la variabile da inserire.

   Un comando per inserire la variabile è racchiuso tra parentesi graffe e aggiunto al codice nella posizione del cursore. Ad esempio:

   `customVar code=my_custom_variable`

1. Per creare dichiarazioni CSS, immetti gli stili in **[!UICONTROL Template Styles]**.

   ![Modelli e-mail - Aggiungere stili personalizzati](./assets/email-template-add-custom-styles-min.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Gli stili personalizzati vengono applicati all’e-mail solo se `{{template config_path="design/email/header_template"}}` è presente in _[!UICONTROL Template Styles]_. Per utilizzare CSS personalizzati senza un modello di intestazione predefinito, è necessario fornirli qui all’interno di `<style>` HTML.

### Passaggio 3: Aggiornare la configurazione

Il _[!UICONTROL Currently Used For]_la traccia delle breadcrumb mostra dove viene utilizzato il modello. In questo esempio, la configurazione del modello si trova sul_[!UICONTROL Customer Configuration]_ pagina, nella _[!UICONTROL Create New Account Options]_e nella sezione_[!UICONTROL Default Welcome Email]_ campo.

- Pagina - [!UICONTROL Customer Configuration]
- Sezione - [!UICONTROL Create New Account Options]
- Campo - [!UICONTROL Default Welcome Email]

1. In **[!UICONTROL Currently Used For]** percorso breadcrumb, fai clic sul collegamento per aprire la pagina di configurazione del modello.

   ![Modello e-mail corrente](./assets/email-template-new-currently-used-for.png){width="600" zoomable="yes"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) e trova il campo per il modello e-mail personalizzato.

1. Cancella **[!UICONTROL Use system value]** e fai clic sul nome del modello personalizzato.

   ![Configurazione clienti - Modello e-mail di benvenuto predefinito](./assets/email-template-message-configuration-default-template.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Nel messaggio nella parte superiore dell’area di lavoro, fai clic su **[!UICONTROL Cache Management]** e cancellare eventuali cache non valide.

### Passaggio 4: Anteprima e salvataggio del modello

1. Quando sei pronto per rivedere il tuo lavoro, fai clic su **[!UICONTROL Preview Template]**.

1. Aggiorna il modello in base alle esigenze.

1. Al termine, fai clic su **[!UICONTROL Save Template]**.

   Il modello personalizzato è ora disponibile nell’elenco dei modelli e-mail.
