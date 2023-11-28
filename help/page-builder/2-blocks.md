---
title: '''[!DNL Page Builder] Parte 2: blocchi'
description: Scopri la differenza tra blocchi semplici e blocchi dinamici quando utilizzi [!DNL Page Builder].
exl-id: 864a3078-8cb3-4add-bdb7-14189aba535e
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '2053'
ht-degree: 0%

---

# [!DNL Page Builder] Procedura dettagliata, parte 2: blocchi

L&#39;esercizio seguente illustra la differenza tra [blocchi semplici](../content-design/blocks.md) e [blocchi dinamici](dynamic-block.md), e come utilizzare [!DNL Page Builder] per creare ogni tipo di blocco.

>[!NOTE]
>
>[!DNL Page Builder] ha un nuovo tipo di contenuto denominato _Banner_, presentato nel primo esercizio di procedura dettagliata e non correlato alla funzionalità del banner precedente. Precedentemente l&#39;opzione Banner in [Menu Contenuto](../content-design/content-menu.md), è ora _Blocco dinamico_.

![Blocco dinamico nella vetrina](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

Questo esercizio presuppone che tu abbia completato [Parte 1: pagina semplice](1-simple-page.md), compresi i prerequisiti e [file di esempio scaricati](./assets/simple-page-assets.zip). Seguire le parti di questo esercizio di procedura dettagliata in ordine.

>[!NOTE]
>
>Questi esercizi di procedura dettagliata vengono aggiornati per riflettere le recenti modifiche apportate al [!DNL Page Builder] nella versione 2.4.1. Se utilizzi una versione precedente di Adobe Commerce, utilizza [!DNL Page Builder] esercizi inclusi nel [[!DNL Commerce] 2.3 Guida utente](https://docs.magento.com/user-guide/v2.3/cms/page-builder-learn.html).

## Parte 1: Creare un blocco semplice

In questo esercizio di procedura dettagliata, creerai un blocco semplice con il contenuto di [!DNL Google Maps]. I blocchi semplici vengono talvolta chiamati _Blocchi CMS_ o _blocchi statici_, perché il contenuto non cambia. Un blocco semplice è ideale per i contenuti che potresti voler riutilizzare.

### Passaggio 1: creare un blocco

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add New Block]**.

1. Per **[!UICONTROL Block Title]**, immetti `Google Map`.

1. Per **[!UICONTROL Identifier]**, immetti `google-map`.

1. Scegli la **[!UICONTROL Store View]** dove il blocco deve essere disponibile.

   ![Informazioni blocco](./assets/pb-tutorial2-block-new-google-map.png){width="600" zoomable="yes"}

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]**.

### Passaggio 2: aggiungere una [!DNL Google Map]

1. Scorri verso il basso fino a [!DNL Page Builder] anteprima del contenuto (attualmente vuota) e fai clic su **[!UICONTROL Edit with Page Builder]**.

1. In [!DNL Page Builder] pannello, espandere **[!UICONTROL Media]** e trascina un **[!UICONTROL Map]** segnaposto nell&#39;area di visualizzazione.

   ![Trascinamento di una mappa sull&#39;area di visualizzazione](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Viene visualizzata una mappa con la posizione del negozio se [!DNL Google Maps] è configurato per il tuo archivio.

   ![Google Map configurato per lo store](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Viene visualizzata una mappa segnaposto se [!DNL Google Maps] non è ancora configurato per lo store.

   ![[!DNL Google Maps] segnaposto](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

1. Nell&#39;angolo superiore destro dell&#39;area di visualizzazione fare clic sul pulsante _Chiudi schermo intero_ (![Icona Chiudi schermo intero](./assets/pb-icon-reduce.png)).

   Facendo clic su questa icona, si ritorna al _[!UICONTROL Content]_sezione per il blocco con l’anteprima visualizzata.

1. Nell’angolo in alto a destra, fai clic su **[!UICONTROL Save]** freccia e scegli **[!UICONTROL Save & Close]**.

### Passaggio 3: configurare [!DNL Google Maps]

Se [!DNL Google Maps] è già configurato per il tuo archivio, puoi saltare questo passaggio e passare a quello successivo.

1. Vai a [Console della piattaforma Google Cloud](https://console.cloud.google.com/google/maps-apis/overview).

1. Fai clic sull’elenco a discesa del progetto e seleziona o crea il progetto per il quale desideri aggiungere una chiave API.

1. Per configurare le credenziali API, segui la sezione [istruzioni][1] nel [!DNL Google Maps] documentazione.

1. Copia la chiave API negli Appunti.

1. Torna a [!DNL Commerce] Amministra e vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Strumenti di contenuto avanzati](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Per ulteriori informazioni su [!UICONTROL Content Management Advanced Tools] opzioni di configurazione, vedi [_Guida di riferimento alla configurazione_](../configuration-reference/general/content-management.md).

1. Per **[!UICONTROL Google Maps API Key]**, incolla la chiave copiata.

1. Clic **[!UICONTROL Test Key]**.

   Se si è verificato un problema con la chiave, tornare al [!DNL Google Maps] Sito di Platform per risolvere il problema. Riprovare.

1. Dopo aver verificato la chiave, fai clic su **[!UICONTROL Save Config]**.

### Passaggio 4: aggiungere il blocco a una pagina

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Nella griglia, individua _[!UICONTROL Simple Page]_creato nel primo tutorial e seleziona **[!UICONTROL Edit]**nel_[!UICONTROL Action]_ colonna.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Content]** e fai clic su **[!UICONTROL Edit with Page Builder]** o all&#39;interno dell&#39;area di anteprima dei contenuti.

1. In [!DNL Page Builder] pannello in _[!UICONTROL Layout]_, trascina un **[!UICONTROL Row]**segnaposto all&#39;inizio dello stage.

   ![Aggiunta della riga all&#39;inizio dello stage](./assets/pb-tutorial2-elements-row-drag-top.png){width="600" zoomable="yes"}

1. In [!DNL Page Builder] pannello, espandere **[!UICONTROL Add Content]** e trascina un **[!UICONTROL Block]** segnaposto per la nuova riga.

1. Passa il puntatore del mouse sul contenitore di blocchi vuoto per visualizzare la casella degli strumenti e scegli _Impostazioni_ (![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

   ![Casella degli strumenti Blocca](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Nella pagina Modifica blocco fare clic su **[!UICONTROL Select Block]**.

   ![Seleziona blocco](./assets/pb-add-content-block-settings-block-select.png){width="600" zoomable="yes"}

1. Nella casella di ricerca immettere `map` e premere Invio/Ritorna per trovare il blocco creato.

   ![Trova blocco nell’elenco](./assets/pb-add-content-block-settings-block-find.png){width="600" zoomable="yes"}

1. Nella griglia, fai clic su **[!UICONTROL Select]** per scegliere [!DNL Google Maps] blocco.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]** per salvare le impostazioni e tornare a [!DNL Page Builder] Workspace.

1. Nell&#39;angolo superiore destro dell&#39;area di visualizzazione fare clic sul pulsante _Chiudi schermo intero_ (![Icona Chiudi schermo intero](./assets/pb-icon-reduce.png)).

   Facendo clic su questa icona, si ritorna al _[!UICONTROL Content]_per la pagina con l&#39;anteprima visualizzata.

1. Nell’angolo in alto a destra, fai clic su **[!UICONTROL Save]** freccia e scegli **[!UICONTROL Save & Close]**.

**Congratulazioni!** La prima parte dell&#39;esercizio Blocca è stata completata. Assicurati di conservare il tuo lavoro come riferimento.

## Parte 2: Creare un blocco dinamico

Un blocco dinamico include una logica che determina dove, quando e a chi viene visualizzato. In questo esercizio di procedura dettagliata, viene creato un blocco dinamico per una promozione che viene attivato quando vengono soddisfatte le condizioni della regola di prezzo e che viene visualizzato solo a un segmento di clienti specifico. Il risultato di questo esempio è simile al banner creato nel primo esercizio, ma con una logica che controlla quando viene visualizzato nella vetrina.

![Esempio di promozione tee Luma](./assets/pb-tutorial2-dynamic-block-row-page.png){width="600" zoomable="yes"}

### Passaggio 1: creare un nuovo blocco dinamico

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Elenco Blocchi dinamici](./assets/pb-tutorial2-block-dynamic-add.png){width="700" zoomable="yes"}

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Dynamic Block]**.

   ![Nuova pagina Blocco dinamico](./assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Completa le impostazioni di base per il nuovo blocco dinamico:

   - Imposta **[!UICONTROL Enable Dynamic Block]** a `Yes`.

   - Per **[!UICONTROL Dynamic Block Name]**, immetti `Tee Shirt Promo`.

   - Imposta **[!UICONTROL Dynamic Block Type]** a `Content Area` e fai clic su **[!UICONTROL Done]**.

     Il tipo di blocco dinamico determina dove [layout di pagina](../content-design/page-layout.md) che il blocco sia posizionato. Quando imposti un blocco dinamico per il punto vendita, considera sia il layout di pagina che il [tema](../content-design/themes.md), in modo da sfruttare al meglio lo spazio disponibile. Alcuni negozi hanno un’area di contenuto attiva limitata a una larghezza fissa, mentre altri estendono l’intera larghezza dello schermo.

     ![Impostazione Dynamic Block Type](./assets/pb-dynamic-block-type.png){width="600" zoomable="yes"}

   - Per **[!UICONTROL Customer Segment]**, seleziona la casella di controllo di ciascun segmento che desideri applicare al blocco dinamico e fai clic su **Fine** per salvare l’elenco dei segmenti.

     Nell&#39;esempio seguente sono presenti due [segmenti cliente](../customers/customer-segments.md) che identificano i clienti registrati in base al sesso. Questo blocco dinamico viene visualizzato solo per le clienti di sesso femminile registrate che hanno effettuato l’accesso ai loro account mentre fanno acquisti nel tuo negozio.

     ![Scelta dei segmenti di clienti](./assets/pb-dynamic-block-customer-segment.png){width="600" zoomable="yes"}

### Passaggio 2: completare le impostazioni

Scorri verso il basso fino a _[!UICONTROL Content]_, che visualizza una sezione vuota [!DNL Page Builder] anteprima del contenuto e fai clic su **[!UICONTROL Edit with Page Builder]**. Quindi, completa le seguenti attività:

**Attività 1:** Aggiungi un&#39;immagine di sfondo

1. Passa il puntatore del mouse sul contenitore righe per visualizzare la casella degli strumenti e scegli _Impostazioni_ (![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

1. Sotto _[!UICONTROL Appearance]_, scegli **[!UICONTROL Full Bleed]**.

1. Per **[!UICONTROL Minimum Height]**, immetti `400px`.

1. Scorri fino a _[!UICONTROL Background]_e impostare **[!UICONTROL Background Image]**facendo clic su **[!UICONTROL Select from Gallery]**e la scelta della `wide-banner-background.png` immagine caricata nella prima esercitazione.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare al [!DNL Page Builder] Workspace.

   ![Riga con l&#39;immagine](./assets/pb-tutorial2-row-image.png){width="600" zoomable="yes"}

**Attività 2:** Aggiungi colonne

In [!DNL Page Builder] pannello in _[!UICONTROL Layout]_, trascina un **[!UICONTROL Column]**segnaposto sulla riga.

![Trascinamento del tipo di colonna nella riga](./assets/pb-tutorial2-column-drag.png){width="600" zoomable="yes"}

La riga è ora divisa in due colonne di uguale larghezza.

**Attività 3:** Aggiungi testo

1. In [!DNL Page Builder] pannello, espandere **[!UICONTROL Elements]** e trascina un **Testo** segnaposto per la seconda colonna.

   ![Trascinamento di una casella di testo nella seconda colonna](./assets/pb-tutorial2-column-text-drag.png){width="600" zoomable="yes"}

1. Immetti nell’editor le tre righe di testo seguenti:

   `Even more ways to mix and match.`

   `Buy 3 Luma tees and get a 4th free.`

   `Shop Tees >`

   ![Inserimento del testo per la colonna](./assets/pb-tutorial2-column-text-editor.png){width="600" zoomable="yes"}

1. Seleziona tutte e tre le righe di testo e utilizza la barra degli strumenti per impostare **Altezza riga** a `40px`.

   ![Impostazione dell&#39;altezza della linea](./assets/pb-tutorial2-column-text-editor-line-height.png){width="600" zoomable="yes"}

1. Imposta il **[!UICONTROL Font Size]** per ciascuna riga, come segue:

   | Linea | Dimensione font |
   |-----| ---------- |
   | Riga 1: | `28px` |
   | Riga 2: | `24px` |
   | Riga 3: | `18px` |

   Poiché questo blocco può essere posizionato in qualsiasi punto della pagina, utilizza lo stile di paragrafo predefinito, anziché i livelli di intestazione. Inoltre, non preoccuparti che il testo non venga ancora disposto correttamente nella colonna.  

   ![Testo formattato](./assets/pb-tutorial2-column-text-editor-text-formatted.png){width="600" zoomable="yes"}

**Attività 4:** Aggiungi un collegamento

Nel primo esercizio imparerete a utilizzare [Pulsante](buttons.md) tipo di contenuto per creare un collegamento. Questo esempio mostra come inserire un collegamento dalla barra degli strumenti dell’editor.

1. In un’altra scheda del browser, apri la vetrina e passa alla pagina che deve essere la destinazione del collegamento.

   Puoi utilizzare l’URL completo o un URL relativo che omette il riferimento al dominio dello store.

   URL completo: `https://mystore.com/women/tops-women/tees-women.html`

   URL relativo: `../women/tops-women/tees-women.html`

1. Torna a [!DNL Page Builder] scheda workspace ed editor di testo, selezionare `Shop Tees >` testo nella terza riga e scegliere **Bold** (![Pulsante grassetto](./assets/editor-btn-bold.png)) nella barra degli strumenti dell’editor.

1. Con il `Shop Tees >` testo nella terza riga ancora selezionato, scegli **Inserisci/modifica collegamento** (![Pulsante Inserisci/modifica collegamento](./assets/pb-icon-add-link.png)) nella barra degli strumenti dell’editor.

   ![Inserimento di un collegamento](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL URL]**, immetti il collegamento relativo preparato.

1. Imposta **[!UICONTROL Target]** a `None`.

   Questa impostazione consente di aprire la pagina nella stessa finestra del browser, anziché aprire una nuova scheda.

1. Per **[!UICONTROL Title]**, immetti `Shop Tees`.

   L’attributo di collegamento Titolo viene utilizzato da alcuni browser come descrizione comando.

1. Per salvare il collegamento e tornare al [!DNL Page Builder] Workspace, fai clic su **[!UICONTROL OK]**.

   ![Dettagli collegamento](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="600" zoomable="yes"}

1. Nell&#39;angolo superiore destro dell&#39;area di visualizzazione fare clic sul pulsante _Chiudi schermo intero_ (![Icona Chiudi schermo intero](./assets/pb-icon-reduce.png)).

   Facendo clic su questa icona, si ritorna al _[!UICONTROL Content]_sezione per il blocco dinamico con l’anteprima visualizzata.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]**.

### Passaggio 3: aggiungere una regola di prezzo

1. Apri _Tee Shirt Promo_ blocco dinamico di nuovo in modalità di modifica.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Related Promotions]** e fai clic su **[!UICONTROL Add Cart Price Rules]**.

   ![Promozioni correlate](./assets/pb-dynamic-blocks-related-promotions.png){width="600" zoomable="yes"}

1. Il giorno _Aggiungi regole prezzo carrello correlato_ , selezionare la casella di controllo per _Acquista 3 magliette e ottenere il 4° gratis_ regola di prezzo e fai clic su **[!UICONTROL Add Selected]**.

   ![Aggiunta di una regola di prezzo del carrello correlata](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

   La regola del prezzo viene visualizzata nel _Promozioni correlate_ sezione, sotto _Regola prezzo carrello correlato_. È possibile associare più regole di prezzo a un blocco dinamico. Tuttavia, questo semplice esempio ne utilizza solo uno.

   ![Regola prezzo carrello selezionato](./assets/pb-dynamic-block-related-cart-price-rule-list.png){width="600" zoomable="yes"}

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]**.

### Passaggio 4: aggiungere il blocco dinamico a una pagina

1. In _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**

1. Trova il _Pagina semplice_ che hai creato in [primo esercizio di procedura dettagliata](1-simple-page.md) e aprilo in modalità di modifica.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Content]** e fai clic su **[!UICONTROL Edit with Page Builder]**.

1. Passa il puntatore del mouse sulla riga superiore con la stessa immagine del blocco dinamico per visualizzare la casella degli strumenti e _Rimuovi_ ( ![Icona Rimuovi](./assets/pb-icon-remove.png){width="20"} ).

   Per confermare la rimozione della riga dalla pagina, fai clic su  **[!UICONTROL OK]** .

1. In [!DNL Page Builder] pannello in _[!UICONTROL Layout]_, trascina un nuovo **[!UICONTROL Row]**segnaposto all&#39;inizio dello stage.

1. In [!DNL Page Builder] pannello, espandere **[!UICONTROL Add Content]** e trascina un **[!UICONTROL Dynamic Block]** segnaposto per la nuova riga.

   ![Trascinamento di un blocco dinamico sulla riga](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. Passa il puntatore del mouse sul contenitore di blocchi dinamici per visualizzare la casella degli strumenti e scegli _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

   ![Casella degli strumenti Blocco dinamico](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. Il giorno _[!UICONTROL Edit Dynamic Block]_pagina, fai clic su **[!UICONTROL Select Dynamic Block]**.

   ![Seleziona blocco dinamico](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

1. Trova il _[!DNL Tee Shirt Promo]_blocco dinamico creato e fai clic su **[!UICONTROL Select]**.

   Di seguito viene visualizzato un riepilogo delle informazioni sul blocco dinamico.

   ![Informazioni blocco dinamico](./assets/pb-tutorial2-dynamic-block-edit.png){width="600" zoomable="yes"}

1. Accetta il valore predefinito **[!UICONTROL Template]**, `Dynamic Block Block Template`.

1. Al termine, fai clic su **[!UICONTROL Save]** per salvare le impostazioni e tornare a [!DNL Page Builder] Workspace.

   ![Blocco dinamico nell’anteprima della pagina](./assets/pb-tutorial2-dynamic-block-on-page.png){width="600" zoomable="yes"}

1. Nell&#39;angolo superiore destro dell&#39;area di visualizzazione fare clic sul pulsante _Chiudi schermo intero_ (![Icona Chiudi schermo intero](./assets/pb-icon-reduce.png)).

   Facendo clic su questa icona, si ritorna al _[!UICONTROL Content]_per la pagina con l&#39;anteprima visualizzata.

1. Nell’angolo in alto a destra, fai clic su **[!UICONTROL Save]** freccia e scegli **[!UICONTROL Save & Close]**.

La seconda parte dell&#39;esercizio Blocca è stata completata. Assicurati di conservare il tuo lavoro come riferimento.

## Parte 3: Aggiornare il blocco dinamico

In questa parte finale dell’esercizio modificherai un blocco dinamico mentre la pagina è attiva nel tuo store. Quindi, accedi al negozio come membro del segmento del cliente per far apparire il blocco.

![Esempio di blocco dinamico nella vetrina](./assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

### Passaggio 1: modificare il blocco dinamico

1. In _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Trova il _[!DNL Tee Shirt Promo]_nella griglia e aprirla in modalità di modifica.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Content]** e fai clic su **[!UICONTROL Edit with Page Builder]**.

1. Modifica la larghezza delle colonne:

   - Passa il cursore del mouse sul bordo tra le due colonne.

   - Tenere premuto il pulsante del mouse e trascinare il bordo di due divisioni verso sinistra.

     ![Divisioni griglia](./assets/pb-tutorial2-dynamic-block-edit-column-width.png){width="600" zoomable="yes"}

     La prima colonna è ora quattro su 12 (4/12) divisioni di griglia, e la seconda colonna è otto su 12 (8/12) divisioni di larghezza.

     ![Due colonne non uguali](./assets/pb-tutorial2-dynamic-block-edit-column-width-changed.png){width="600" zoomable="yes"}

1. Modificare il colore del testo:

   - Selezionare le prime due righe di testo.

   - Sulla barra degli strumenti dell’editor, scegli **[!UICONTROL Text Color]** e fai clic su **[!UICONTROL White]** campione.

   ![Colore testo](./assets/pb-tutorial2-dynamic-block-edit-text-color.png){width="600" zoomable="yes"}

1. Nell&#39;angolo superiore destro dell&#39;area di visualizzazione fare clic sul pulsante _Chiudi schermo intero_ (![Icona Chiudi schermo intero](./assets/pb-icon-reduce.png)).

   Facendo clic su questa icona, si ritorna al _[!UICONTROL Content]_sezione per il blocco dinamico con l’anteprima visualizzata.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]**.

### Passaggio 2: visualizzare il blocco dinamico

Poiché questo blocco dinamico è visibile solo ai membri di uno specifico segmento di clienti, è necessario accedere come cliente membro del segmento di clienti per visualizzare la promozione. In questo esempio, il blocco viene visualizzato solo ai clienti di sesso femminile.

1. Apri una finestra del browser nella vetrina.

1. Per visualizzare la pagina di esempio, modifica l’URL nella barra degli indirizzi come segue:

   mystore.com/sample-page

   Se l’archivio è configurato per includere il suffisso html, includi il suffisso come segue:

   mystore.com/sample-page.html

1. Accedi come cliente donna:

   - Nell&#39;angolo superiore destro della home page, fare clic su **[!UICONTROL Sign In]**.

   - Se i dati Luma di esempio sono installati nel sistema, usa le seguenti credenziali:

     **[!UICONTROL Email]** - `roni_cost@example.com`

     **[!UICONTROL Password]** -  `roni_cost3@example.com`

   - Clic **[!UICONTROL Sign In]**.

   - Torna alla pagina di esempio per visualizzare il blocco dinamico creato con la promozione Tee Shirt.

   ![Blocco dinamico visualizzato per un segmento di clienti](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

Hai completato l&#39;esercizio Blocca. Assicurati di conservare il tuo lavoro come riferimento.

Quando sei pronto, procedi a [Parte 3: Contenuto del catalogo](3-catalog-content.md)

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
