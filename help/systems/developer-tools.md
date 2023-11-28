---
title: Strumenti per sviluppatori
description: Scopri gli strumenti per sviluppatori avanzati disponibili per supportare gli sviluppatori che lavorano su progetti di personalizzazione.
exl-id: 34529aa9-201f-4817-b53b-a15b6a78a923
role: Admin, Developer
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1711'
ht-degree: 0%

---

# Strumenti per sviluppatori

Utilizza gli strumenti avanzati per gli sviluppatori per determinare la modalità di compilazione durante lo sviluppo front-end, creare un inserisco nell&#39;elenco Consentiti di indirizzi IP di tipo e visualizzare gli hint di percorso dei modelli. Sono inoltre disponibili strumenti per apportare facilmente modifiche al testo nell’interfaccia della vetrina e dell’amministratore.

- [Registri azioni](action-log.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)
- [Flusso di lavoro di sviluppo front-end](#frontend-development-workflow)
- [Utilizzo delle firme dei file statici](#static-file-signatures)
- [Ottimizzazione dei file di risorse](#optimizing-resource-files)
- [Limitazioni per i client di sviluppo](#client-restrictions)
- [Suggerimenti percorso modello](#template-path-hints)
- [Traduci in linea](#translate-inline)

## Modalità operative

È possibile distribuire l’istanza Adobe Commerce o di Magento Open Source per l’esecuzione in _produzione_ o _modalità sviluppatore_. Gli strumenti e le impostazioni di configurazione progettati appositamente per gli sviluppatori sono accessibili solo mentre lo store è in esecuzione in _modalità sviluppatore_.

La modalità operativa può essere modificata solo dalla riga di comando del server da un utente con le autorizzazioni appropriate. Consulta [Impostare la modalità operativa](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/set-mode.html) nel _Guida alla configurazione_ per ulteriori informazioni.

La maggior parte degli argomenti nella documentazione per esercenti si applica a un’istanza Commerce in esecuzione in modalità di produzione. Tuttavia, le impostazioni di configurazione e gli strumenti seguenti possono essere utilizzati solo quando l&#39;installazione è in esecuzione in modalità sviluppatore.

## Flusso di lavoro di sviluppo front-end

Il tipo di flusso di lavoro di sviluppo front-end determina se la compilazione Less viene eseguita sul lato client o server durante lo sviluppo. Less è un’estensione di CSS che dispone di funzioni e convenzioni aggiuntive e che produce codice semplificato. Per lo sviluppo dei temi, si consiglia la compilazione Less lato client. La compilazione lato server è la modalità predefinita. Le opzioni del flusso di lavoro di sviluppo non sono disponibili per i negozi in modalità di produzione.
Consulta [Compilazione LESS lato client e lato server](https://developer.adobe.com/commerce/frontend-core/guide/css/quickstart/compilation-mode/){:target=&quot;_blank&quot;} nella documentazione per gli sviluppatori di Commerce.

>[!NOTE]
>
>La configurazione del flusso di lavoro di sviluppo front-end è disponibile in [Modalità sviluppatore](../systems/developer-tools.md#operation-modes) solo.

![Configurazione avanzata: flusso di lavoro di sviluppo front-end](../configuration-reference/advanced/assets/developer-frontend-development-workflow.png){width="600" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Front-end Development Workflow]** sezione.

1. Imposta **[!UICONTROL Workflow Type]** a uno dei seguenti elementi:

   - `Client side less compilation` - La compilazione avviene nel browser utilizzando `less.js` libreria.
   - `Server side less compilation` - La compilazione avviene sul server utilizzando la libreria meno PHP. Questa è la modalità predefinita per la produzione.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Firme file statiche

L&#39;aggiunta di una firma digitale all&#39;URL di file statici consente ai browser di rilevare quando è disponibile una versione più recente del file. I file statici che possono essere tracciati con le firme digitali includono JavaScript, CSS, immagini e font. La firma viene aggiunta al percorso direttamente dopo l’URL di base. Se la firma di un file è diversa da quella memorizzata nella cache del browser, viene utilizzata la versione più recente del file.

Consulta [Firma del contenuto statico](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/static-content-signing.html){:target=&quot;_blank&quot;} nella documentazione per gli sviluppatori di Commerce.

>[!NOTE]
>
>La configurazione di Impostazioni file statiche è disponibile solo quando si lavora in [modalità sviluppatore](../systems/developer-tools.md#operation-modes).

![Configurazione avanzata: impostazioni dei file statici](../configuration-reference/advanced/assets/developer-static-files-settings.png){width="600" zoomable="yes"}

Per un elenco dettagliato delle impostazioni di configurazione, vedi [_Impostazioni file statico_](../configuration-reference/advanced/developer.md) nel _Riferimento configurazione_.

**_Per attivare i file statici firmati:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Static Files Settings]** sezione.

1. Imposta **[!UICONTROL Sign Static Files]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Ottimizzazione dei file di risorse

Il tempo necessario per caricare i file di risorse può essere ridotto unendo e raggruppando i file e riducendo al minimo il codice.

- L&#39;unione combina file separati dello stesso tipo in un unico file.
- Il bundling è una tecnica che raggruppa file separati in modo da ridurre il numero di richieste HTTP necessarie per caricare una pagina.
- La minimizzazione rimuove spazi, interruzioni di riga e commenti, ma non influisce sulla funzionalità del codice. Poiché i file ridotti a icona non possono essere modificati, il processo deve essere applicato solo quando si è pronti per l’avvio in produzione.

Per impostazione predefinita, Adobe Commerce e Magento Open Source non uniscono, raggruppano o riducono a icona i file e lo sviluppatore del progetto deve determinare quali metodi di ottimizzazione file utilizzare.

Consulta [Best practice per le prestazioni](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/overview.html) per ulteriori informazioni.

>[!NOTE]
>
>I file CSS e JavaScript possono essere ottimizzati in [Modalità sviluppatore](../systems/developer-tools.md#operation-modes) solo.

| Tipo di file | Operazioni supportate |
| --------------- | -------------------- |
| File CSS | `MergeMinify` |
| File JavaScript | `MergeBundleMinify` |
| File modello | `Minify` |

{style="table-layout:auto"}

**_Per ottimizzare i file di risorse:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Per ottimizzare i file CSS, espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL CSS Settings]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Merge CSS Files]** a `Yes`.
   - Imposta **[!UICONTROL Minify CSS Files]** a `Yes`.

   ![Configurazione avanzata - Impostazioni CSS](../configuration-reference/advanced/assets/developer-css-settings.png){width="600" zoomable="yes"}

[Impostazioni _CSS_](../configuration-reference/advanced/developer.md)

1. Per ottimizzare i file JavaScript, espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL JavaScript Settings]** ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Merge JavaScript Files]** a `Yes`.
   - Imposta **[!UICONTROL Minify JavaScript Files]** a `Yes`.

   ![Configurazione avanzata: impostazioni JavaScript](../configuration-reference/advanced/assets/developer-javascript-settings.png){width="600" zoomable="yes"}

1. Per minimizzare i file modello PHTML, espandete ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Template Settings]** sezione e set **[!UICONTROL Minify Html]** a `Yes`.

   ![Configurazione avanzata - Impostazioni modello](../configuration-reference/advanced/assets/developer-template-settings.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Limitazioni per i client

Prima di utilizzare uno strumento come [suggerimenti percorso modello](#template-path-hints), assicurati di aggiungere il tuo indirizzo IP all’elenco Consentiti Developer Client Restrictions (Limitazioni client sviluppatore) per evitare di interrompere l’esperienza di acquisto dei clienti nel negozio. Se non conosci il tuo indirizzo IP, puoi cercarlo online.

>[!NOTE]
>
>Le restrizioni per i client di sviluppo possono essere impostate in [Modalità sviluppatore](../systems/developer-tools.md#operation-modes) solo.

Per informazioni tecniche, consulta [VCL personalizzato per consentire le richieste](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/custom-vcl-snippets/fastly-vcl-allowlist.html) nel _Guida di Commerce su infrastruttura cloud_.

**_Per aggiungere il tuo indirizzo IP al inserisco nell&#39;elenco Consentiti di:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Developer Client Restrictions]** sezione.

   ![Configurazione avanzata: restrizioni per i client per sviluppatori](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Allow IPs]**, immetti l&#39;indirizzo IP.

   Se è necessario l’accesso da più indirizzi IP, separali con una virgola.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, aggiorna le cache non valide.

## Suggerimenti percorso modello

Gli hint di percorso del modello sono uno strumento diagnostico che aggiunge una notazione con il percorso di ciascun modello utilizzato nella pagina. Gli hint per il percorso del modello possono essere abilitati sia per la vetrina che per l’amministratore.

>[!NOTE]
>
>Gli Hint percorso modello possono essere modificati in [modalità sviluppatore](../systems/developer-tools.md#operation-modes) solo.

Consulta [Individuazione di modelli, layout e stili](https://developer.adobe.com/commerce/frontend-core/guide/themes/debug/){:target=&quot;_blank&quot;} nella documentazione per gli sviluppatori di Commerce.

![Esempio di vetrina: suggerimenti per il percorso del modello](./assets/storefront-template-path-hints.png){width="700" zoomable="yes"}

### Passaggio 1: aggiungi l’indirizzo IP al inserisco nell&#39;elenco Consentiti di

Prima di utilizzare i suggerimenti del percorso del modello, aggiungi il tuo indirizzo IP alla [INSERISCO NELL&#39;ELENCO CONSENTITI DI](#client-restrictions) per evitare interferenze con i clienti che fanno acquisti all&#39;interno del negozio. Al termine, assicurati di cancellare la cache di Commerce per rimuovere tutti gli hint dall’archivio.

![Configurazione avanzata: restrizioni per i client per sviluppatori](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

### Passaggio 2: abilitare gli hint per il percorso del modello

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Debug]** ed effettuare le seguenti operazioni:

   ![Configurazione avanzata - debug](../configuration-reference/advanced/assets/developer-debug.png){width="600" zoomable="yes"}

   - Per attivare i suggerimenti del percorso del modello per l&#39;archivio, impostare **[!UICONTROL Enabled Template Path Hints for Storefront]** a `Yes`.

   - Per abilitare i suggerimenti del percorso del modello per l’archivio solo quando l’URL include `templatehints` parametro, impostato **Abilita suggerimenti per vetrina con parametro URL** a `Yes`. Impostate quindi il valore del parametro, se necessario. Il valore predefinito è `magento`, ma puoi utilizzare un valore personalizzato. Ad esempio, se modifichi il valore in `lorem`, utilizzerai `mymagento.com?templatehints=lorem` per visualizzare gli hint del modello.

   - Per attivare i suggerimenti del percorso del modello per l’amministratore, imposta **[!UICONTROL Enabled Template Path Hints for Admin]** a `Yes`.

   - Per includere i nomi dei blocchi, impostare **[!UICONTROL Add Block Class Type to Hints]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Passaggio 3: cancellare la cache

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Flush Magento Cache]**.

## Traduci in linea

È possibile utilizzare lo strumento Traduci in linea in [modalità sviluppatore](../systems/developer-tools.md#operation-modes) per ritoccare il testo nell’interfaccia in modo da riflettere la voce e il marchio. Quando è attivata la modalità Traduci in linea, tutto il testo sulla pagina che può essere modificato viene evidenziato in rosso. È facile modificare le etichette dei campi, i messaggi e altro testo visualizzato nella vetrina e in Amministrazione. Ad esempio, molti temi utilizzano terminologia come _Il mio account_, _La mia lista desideri_, e _Il mio dashboard_, per aiutare i clienti a trovare il modo di procedere. Tuttavia, potrebbe essere preferibile utilizzare semplicemente le parole _Account_, _Lista dei desideri_, e _Dashboard_.

>[!NOTE]
>
>Lo strumento Traduci in linea è disponibile solo quando si lavora in [modalità sviluppatore](../systems/developer-tools.md#operation-modes).

Consulta [Panoramica sulle traduzioni](https://developer.adobe.com/commerce/frontend-core/guide/translations/) nella documentazione per gli sviluppatori di Commerce.

![Esempio di vetrina: testo traducibile](./assets/storefront-translate-inline.png){width="700" zoomable="yes"}

Se il punto vendita è disponibile in più lingue, è possibile apportare regolazioni precise al testo tradotto per la lingua. Sul server, il testo dell’interfaccia viene mantenuto in un file CSV separato per ciascun blocco di output e organizzato in base alle impostazioni internazionali. Come approccio alternativo, anziché utilizzare il _Traduci in linea_ , puoi anche modificare i file CSV direttamente sul server. I file di traduzione vengono memorizzati in `app/code/Magento/<module_name>/i18n/<language_locale>.csv`.

>[!NOTE]
>
>Per utilizzare lo strumento Traduci in linea, il browser deve consentire la visualizzazione di popup.

### Passaggio 1: disabilitare le cache di output

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Selezionare le caselle di controllo seguenti:

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. Imposta il **[!UICONTROL Actions]** controllo a `Disable` e fai clic su **[!UICONTROL Submit]**.

### Passaggio 2: abilitare lo strumento Traduci in linea

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Per utilizzare una visualizzazione specifica dello store, impostare **[!UICONTROL Store View]** da aggiornare.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Translate Inline]** sezione.

   Cancella **[!UICONTROL Use Website]** per modificare queste impostazioni.

   Il _[!UICONTROL Enabled for Admin]_non è disponibile quando si modifica una visualizzazione store specifica.

   ![Configurazione avanzata - Traduci in linea](../configuration-reference/advanced/assets/developer-translate-inline.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enabled for Storefront]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, aggiorna le cache non valide, ma lascia le cache disabilitate invariate per il momento.

### Passaggio 3: aggiornare il testo

1. Apri la vetrina in un browser e passa alla pagina da modificare.

   Se necessario, utilizza il selettore lingua per modificare la visualizzazione dello store. Ogni stringa di testo che può essere tradotta è evidenziata in rosso. Quando si passa il puntatore del mouse su una casella di testo, viene visualizzata l&#39;icona di un libro ( ![Icona libro](../assets/icon-book.png) ).

1. Fai clic sull’icona libro per aprire _Traduci_ ed effettuare le seguenti operazioni:

   - Se la modifica riguarda una visualizzazione specifica dello store, seleziona la **[!UICONTROL Store View Specific]** casella di controllo.

   - Inserisci il nuovo **[!UICONTROL Custom]** testo.

1. Al termine, fai clic su **[!UICONTROL Submit]**.

   ![Inserisci testo personalizzato](./assets/storefront-translate-inline-detail.png){width="700" zoomable="yes"}

1. Per visualizzare le modifiche nell&#39;archivio, aggiorna il browser.

1. Ripetere questa procedura per modificare tutti gli elementi dell&#39;archivio.

### Passaggio 4: ripristinare le impostazioni originali

1. Torna all’Amministratore del tuo negozio.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Imposta **[!UICONTROL Store View]** alla visualizzazione specifica modificata.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Translate Inline]** sezione.

1. Imposta **[!UICONTROL Enabled for Frontend]** a `No`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. Seleziona la casella di controllo delle seguenti cache di output precedentemente disabilitate:

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. Imposta il **[!UICONTROL Actions]** controllo a `Enable` e fai clic su **[!UICONTROL Submit]**.

1. Quando richiesto, aggiorna le cache non valide.

### Passaggio 5: verificare le modifiche nel punto vendita

Vai alla vetrina ed esamina ogni pagina aggiornata per verificare che le modifiche siano corrette. In questo esempio, `Customer Login` è stato modificato in `Customer Sign In`. Se sono state apportate modifiche a una visualizzazione specifica, utilizza Selezione lingua per passare alla visualizzazione corretta.

![Esempio di vetrina: accesso del cliente tradotto](./assets/storefront-translate-inline-customer-sign-in.png){width="700" zoomable="yes"}
