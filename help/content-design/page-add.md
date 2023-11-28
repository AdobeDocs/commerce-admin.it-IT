---
title: Aggiungi e rimuovi pagine
description: Scopri come aggiungere e rimuovere le pagine di contenuto utilizzate nel [!DNL Commerce] archiviare.
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# Aggiungi e rimuovi pagine

Il processo di aggiunta di una pagina di contenuto all&#39;archivio è essenzialmente lo stesso per qualsiasi tipo di pagina che si desidera creare. Puoi includere testo, immagini, blocchi di contenuto, variabili e widget. La maggior parte delle pagine di contenuto è progettata per essere letta prima dai motori di ricerca e poi dalle persone. Tieni presente le esigenze di ciascuno di questi due diversi tipi di pubblico quando scegli il titolo della pagina, l’URL e durante la composizione dei metadati e del contenuto. Una volta completata, la pagina può essere aggiunta alla navigazione del negozio, collegata ad altre pagine, collegata dal piè di pagina del negozio o utilizzata come una nuova [home page](page-home-new.md).

![Griglia pagine](./assets/pages-grid.png){width="700" zoomable="yes"}

## Aggiungi una pagina

Le istruzioni seguenti descrivono ogni passaggio per creare una pagina di base. Alcune funzioni avanzate vengono ignorate, ma sono trattate in altri argomenti.

### Passaggio 1: creare la pagina

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Clic **[!UICONTROL Add New Page]**.

   ![Nuova pagina](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. Se non desideri pubblicare la pagina immediatamente, imposta **[!UICONTROL Enable Page]** a `No`.

1. Inserisci il **[!UICONTROL Page Title]**.

   Il titolo della pagina viene visualizzato nel [breadcrumb](../catalog/navigation-breadcrumb-trail.md) navigazione.

### Passaggio 2: Completare il contenuto

A seconda del [Configurazione avanzata degli strumenti di contenuto](../configuration-reference/general/content-management.md), aggiungi il contenuto della pagina.

#### Utilizzare gli strumenti di contenuto di Page Builder

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Contenuto con Page Builder](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. In **[!UICONTROL Content Heading]** immettere l&#39;intestazione che si desidera visualizzare nella parte superiore della pagina.

   Se l&#39;opzione è abilitata, [Page Builder](../page-builder/introduction.md) L’area di visualizzazione e il pannello vengono visualizzati sotto l’intestazione del contenuto. Per ulteriori informazioni, consulta [Workspace](../page-builder/workspace.md). Se _Page Builder_ non è abilitato, l’editor si apre in modalità WYSIWYG con la barra degli strumenti nella parte superiore.

1. Completa il contenuto e formatta il testo come necessario.

#### Utilizzare la barra degli strumenti dell’editor

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Contenuto](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. In **[!UICONTROL Content Heading]** immettere l&#39;intestazione che si desidera visualizzare nella parte superiore della pagina.

1. Completa il contenuto e formatta il testo come necessario.

   Puoi aggiungere [immagini](media-storage.md), [Variabili](../systems/variables-predefined.md), e [widget](widgets.md) secondo necessità. Per ulteriori informazioni, consulta [Utilizzo dell’editor](editor.md).

### Passaggio 3: Completare le informazioni SEO (Search Engine Optimization)

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**.

   ![Ottimizzazione motore di ricerca](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. Accettate il valore predefinito o immettete un altro valore **[!UICONTROL URL Key]** costituito da tutti i caratteri minuscoli, con trattini invece degli spazi.

   La chiave URL predefinita è stata creata quando la pagina è stata salvata ed è basata sull’intestazione del contenuto.

1. Immetti un **[!UICONTROL Meta Title]** per la pagina.

   Il metatitolo deve contenere meno di 70 caratteri e viene visualizzato nella barra del titolo e nella scheda del browser.

1. Immetti il valore massimo che desideri **[!UICONTROL Meta Keywords]** che i motori di ricerca possono utilizzare per indicizzare la pagina.

   Separa più parole con una virgola. Le parole chiave meta vengono ignorate da alcuni motori di ricerca, ma utilizzate da altri.

1. Per **[!UICONTROL Meta Description]**, immettere una breve descrizione della pagina per l&#39;elenco dei risultati di ricerca.

   Idealmente, la descrizione dovrebbe essere lunga 150-160 caratteri, con un limite massimo di 255.

1. Clic **[!UICONTROL Save]**.

### Passaggio 4: specificare l’ambito della pagina

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**.

   ![Pagine nei siti Web](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. In **[!UICONTROL Store View]** selezionare ogni visualizzazione in cui la pagina sarà disponibile.

   Se nell&#39;installazione sono presenti più siti Web, selezionare ogni sito Web e archiviare la visualizzazione in cui la pagina sarà disponibile.

### Passaggio 5: identificare la pagina padre (se applicabile)

{{ee-feature}}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**.

   ![Gerarchia](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. Se questa pagina è figlia di un’altra pagina, seleziona la casella di controllo della proprietà **[!UICONTROL Parent page]**.

### Passaggio 6: inserire le modifiche di progettazione (facoltativo)

1. Per modificare il layout della pagina, espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Design]**.

   ![Progettazione](./assets/page-design.png){width="600" zoomable="yes"}

1. Per modificare il layout delle colonne della pagina, impostare **[!UICONTROL Layout]** a uno dei seguenti elementi:

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` (Richiede [Page Builder](../page-builder/introduction.md))
   - `Category -- Full Width` (Richiede Page Builder)
   - `Product -- Full Width` (Richiede Page Builder)

1. Per applicare una **[!UICONTROL Custom Layout Update]**, scegliere il nome del file dall&#39;elenco.

   Per ulteriori informazioni, consulta [Aggiornamenti del layout](layout-updates.md).

1. Per cambiare il tema della pagina, imposta **[!UICONTROL New Theme]** a uno dei seguenti elementi:

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Per pianificare una modifica della progettazione, espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]** ed effettuare le seguenti operazioni:

   ![Aggiornamento progettazione personalizzato](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - Utilizza il calendario (![Icona Calendario](../assets/icon-calendar.png)) per scegliere il **[!UICONTROL From]** e **[!UICONTROL To]** le date di entrata in vigore della modifica.

   - Per applicare un tema diverso alla pagina, seleziona il nome del **[!UICONTROL New Theme]**.

   - Per modificare il layout delle colonne della pagina, scegliere **[!UICONTROL Layout]** che desideri applicare.

### Passaggio 7: visualizzare l’anteprima della pagina

1. Fai clic su **[!UICONTROL Save]** freccia e scegli **[!UICONTROL Save & Close]** per tornare alla griglia Pagine.

1. Trova la pagina nella griglia e seleziona **[!UICONTROL View]** nel _[!UICONTROL Action]_colonna.

1. Per tornare alla griglia, fare clic su **[!UICONTROL Back]** nell&#39;angolo superiore sinistro della finestra del browser.

### Passaggio 8: pubblicare la pagina

1. Seleziona **[!UICONTROL Edit]** nel _[!UICONTROL Action]_della griglia.

1. Imposta **[!UICONTROL Enable Page]** a `Yes`.

1. Fai clic su **[!UICONTROL Save]** freccia e scegli **[!UICONTROL Save & Close]**.

## Duplicare una pagina

Qualsiasi pagina di contenuto può essere utilizzata come modello e salvata come duplicato. È possibile utilizzare questa tecnica che consente di risparmiare tempo per creare una progettazione coerente per le pagine di contenuto in tutto il sito. La pagina duplicata mantiene il titolo della pagina originale, ma è necessario aggiornare i campi Chiave URL e Stato.

![Salva e duplica](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Nella griglia individuare la pagina da duplicare e fare clic su **[!UICONTROL Edit]** nel _[!UICONTROL Action]_colonna.

1. Fai clic su **[!UICONTROL Save]** freccia e scegli **[!UICONTROL Save & Duplicate]**.

1. Quando ricevi i messaggi che indicano che la pagina è stata salvata e duplicata, fai clic su **[!UICONTROL Back]** nella barra dei pulsanti superiore per tornare alla griglia.

1. Individuare la pagina duplicata nella griglia e prendere nota di quanto segue:

   - Il titolo della pagina è lo stesso dell’originale.
   - Viene assegnata una chiave URL univoca ma temporanea.
   - Lo stato della pagina è `Disabled`.

1. Apri la pagina duplicata in _Modifica_ ed effettuare le seguenti operazioni:

   - Se desideri pubblicare la pagina immediatamente, imposta **[!UICONTROL Enable Page]** a `Yes`.

   - Aggiornare il **[!UICONTROL Page Title]**, in base alle esigenze.

   - Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimization]** e immettere il valore univoco **[!UICONTROL URL Key]** da utilizzare per la pagina duplicata.

     ![Chiave URL temporanea](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - Se necessario, aggiorna il contenuto della pagina rimanente.

1. Fai clic su **[!UICONTROL Save]** freccia e scegli **[!UICONTROL Save & Close]**.

   La pagina duplicata nella griglia riflette le modifiche apportate.

## Menu Salva

| Comando | Descrizione |
|--- |--- |
| [!UICONTROL Save] | Salvare la pagina corrente e continuare a lavorare. |
| [!UICONTROL Save & New] | Salva e chiudi la pagina corrente e inizia una nuova pagina. |
| [!UICONTROL Save & Duplicate] | Salva e chiudi la pagina corrente e apri una nuova copia duplicata. |
| [!UICONTROL Save & Close] | Salvare e chiudere la pagina corrente e tornare alla griglia Pagine. |

{style="table-layout:auto"}

## Eliminare una pagina

Esistono due modi per rimuovere una pagina creata. Puoi rimuoverlo dal _[!UICONTROL Pages]_griglia o dalla_[!UICONTROL Edit]_ pagina.

### Metodo 1: rimuovere una pagina dalla griglia Pagine

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Individua le pagine utilizzando i filtri sopra la griglia e seleziona la casella di controllo per una o più pagine da eliminare.

1. Nell&#39;angolo superiore sinistro dell&#39;elenco, impostare **[!UICONTROL Actions]** a `Delete`.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.

### Metodo 2: rimuovere una pagina dalla pagina di modifica

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Trova la pagina da eliminare.

1. In _[!UICONTROL Actions]_per l’entità pagina, fai clic su **[!UICONTROL Select]**e scegli **[!UICONTROL Edit]**.

1. Nella barra dei pulsanti, fai clic su **[!UICONTROL Delete Page]**.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.
