---
title: '[!DNL Google Tag Manager]'
description: Scopri come utilizzare [!DNL Google Tag Manager] per gestire i numerosi tag (snippet di codice) correlati agli eventi delle campagne di marketing nei siti Adobe Commerce.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 22a619db0b0673dc520b9bdc5d6cd0c8ffecdf08
workflow-type: tm+mt
source-wordcount: '1459'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] è uno strumento potente che consente di gestire e distribuire in modo efficiente i vari tag (snippet di codice) associati agli eventi della campagna di marketing. [!DNL Google Tag Manager] consente di aggiungere tag di tracciamento al sito per misurare il pubblico, personalizzare, eseguire il retargeting o condurre iniziative di marketing per motori di ricerca.

[!DNL Google Tag Manager] trasferisce direttamente dati ed eventi a [!DNL Google Analytics], e-commerce avanzato e altre soluzioni di analisi di terze parti per ottenere un quadro chiaro delle prestazioni del sito, dei prodotti e delle promozioni.

Per continuare il processo, è necessario disporre di un account [!DNL Google Analytics] e di un account [!DNL Tag Manager]. Le istruzioni seguenti illustrano come configurare gli account Google, configurare il Commerce store e creare un tag.

>[!NOTE]
>
>Se la tua azienda è soggetta alle normative sulla privacy come il [Regolamento generale sulla protezione dei dati](../getting-started/compliance-gdpr.md) e/o il [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), consulta [Impostazioni sulla privacy di Google](google-tools.md#google-privacy-settings).

## Passaggio 1: Configura l&#39;account [!DNL Google Analytics]

Consulta [Configurare la ricerca del sito](https://support.google.com/analytics/answer/1012264) nella Guida di Google per le nozioni di base necessarie per iniziare. Consulta anche le guide di Google per [Google Analytics](https://support.google.com/analytics/answer/9304153) e [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Accedi al tuo account [!DNL Google Analytics].

1. Per abilitare **[!UICONTROL Internal Site Search Tracking]**, eseguire le operazioni seguenti:

   - Passa a **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Imposta **[!UICONTROL Site Search Tracking]** su `On`.

   - Imposta il parametro **[!UICONTROL Query]** su `q`.

   - Al termine, **[!UICONTROL Save]** le impostazioni.

1. Per attivare le funzioni di visualizzazione, effettuare le seguenti operazioni:

   - Scegli **[!UICONTROL Property Settings]**.

   - In _[!UICONTROL Advertising Features]_, impostare **[!UICONTROL Enable Demographics and Interest Reports]**su `On`.

   - **[!UICONTROL Save]** le impostazioni.

1. Per abilitare il tracciamento di e-commerce, effettuare le seguenti operazioni:

   - Passa a **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Imposta **[!UICONTROL Enable Ecommerce]** su `On`.

   - Imposta **[!UICONTROL Enable Enhanced Ecommerce Reporting]** su `On`.

   - **[!UICONTROL Save]** le impostazioni.

1. Ricarica la pagina e verifica che tutte le impostazioni rimangano `On`.

   >[!NOTE]
   >
   >Se non tutte le impostazioni sono `On`, ripetere i passaggi precedenti, salvare e ricaricare la pagina. Ripetere il processo finché tutte le impostazioni non sono impostate su `On`.

## Passaggio 2: Configura l&#39;account [!DNL Google Tag Manager]

Le istruzioni seguenti mostrano come configurare un nuovo contenitore con le impostazioni di base. Un esempio di file di configurazione [Composer](https://developer.adobe.com/commerce/php/development/composer/) (.json) viene utilizzato per semplificare il processo, importando per generare un tag in un nuovo contenitore. In questo esempio, si consiglia di creare un contenitore, anziché modificare un contenitore esistente.

>[!NOTE]
>
>Per ulteriori informazioni, vedere l&#39;esportazione e l&#39;importazione del contenitore [Google](https://support.google.com/tagmanager/answer/6106997). Queste istruzioni forniscono una procedura dettagliata per importare un JSON di esempio in un nuovo contenitore.

1. Scarica il file collegato [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), apri il file in un editor e salvalo come `GTM_M2_Config.json`.

   Il file JSON viene caricato direttamente in [!DNL Google Tag Manager].

1. Passa a **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Fare clic su **[!UICONTROL Choose container file]** e selezionare il file JSON.

1. In **[!UICONTROL Choose workspace]**, fare clic su **[!UICONTROL New]**.

1. Immettere un titolo e una descrizione, quindi fare clic su **[!UICONTROL Save]**.

1. Per importare il file, selezionate una delle seguenti azioni:

   - Selezionare l&#39;opzione **[!UICONTROL Overwrite]** per un nuovo contenitore.

   - L&#39;opzione **[!UICONTROL Merge]** deve essere selezionata se si utilizza un contenitore esistente.

1. Fare clic su **[!UICONTROL Preview]** per esaminare tag, trigger e variabili.

1. Per modificare **[!UICONTROL Google Analytics ID]** a cui si fa riferimento nelle variabili, eseguire le operazioni seguenti:

   - Passa a **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Scegli **[!UICONTROL Google Analytics]** e aggiorna il segnaposto (`UA-xxxxxx-x`) con il tuo **[!UICONTROL GA ID]**.

1. Segui le istruzioni di Google per aggiungere tag, trigger e variabili al nuovo contenitore.

   Se disponi di impostazioni in un altro contenitore che desideri utilizzare, puoi spostarle nel nuovo contenitore.

1. Al termine, fai clic su **[!UICONTROL Confirm]**.

1. Segui le istruzioni di Google per la pubblicazione del nuovo contenitore.

## Passaggio 3: Configurare lo store

{{gtag-api-note}}

1. Accedi all’amministratore del tuo store di Commerce.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Google API]**.

1. Espandi ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Google Analytics]** e configura quanto segue:

   ![Configurazione vendite - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Enable]** su `Yes`.

   - Imposta **[!UICONTROL Account type]** su `Google Tag Manager`.

   - Nel campo **[!UICONTROL Container ID]**, immetti il tuo ID GTM (`GTM-xxxxxx`).

   - Se si utilizza anche Google Analytics per gli esperimenti di contenuto, impostare **Abilita esperimenti di contenuto** su `Yes`.

   - Utilizzare i valori predefiniti per i campi rimanenti.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Verifica le impostazioni di [!DNL Google Tag Manager] e che tutto funzioni correttamente.

>[!NOTE]
>
>Ogni contenitore è associato a un sito web e serve un solo contenitore per account. Se disponi di un’istanza Commerce multisito, sono necessari contenitori separati.

## Descrizioni dei campi

| Campo | Ambito | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable] | Visualizzazione store | Determina se l’e-commerce avanzato di Google Analytics può essere utilizzato per analizzare l’attività nel tuo store. Opzioni: `Yes` / `No` |
| [!UICONTROL Account type] | Visualizzazione store | Determina il codice di tracciamento di Google utilizzato per monitorare l&#39;attività e il traffico dell&#39;archivio. Opzioni: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Visualizzazione store | Determina se rimuovere le informazioni di identificazione dagli indirizzi IP visualizzati nei risultati di Google Analytics. |
| [!UICONTROL Enable Content Experiments] | Visualizzazione store | Attiva Google Content Experiments, che può essere utilizzato per testare fino a dieci versioni diverse della stessa pagina. Opzioni: `Yes` / `No` |
| [!UICONTROL Container Id] | Visualizzazione store | Se [!DNL Google Tag Manager] è già installato e configurato per il tuo archivio, l&#39;ID contenitore viene visualizzato automaticamente in questo campo. |
| [!UICONTROL List property for the catalog page] | Visualizzazione store | Identifica la proprietà Tag Manager associata alla pagina del catalogo. Valore predefinito: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Visualizzazione store | Identifica la proprietà Tag Manager associata al blocco di cross-selling. Valore predefinito: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Visualizzazione store | Identifica la proprietà Tag Manager associata al blocco di up-sell. Valore predefinito: `Up-sell` |
| [!UICONTROL List property for the related products block] | Visualizzazione store | Identifica la proprietà Tag Manager associata al blocco di prodotti correlati. Valore predefinito: `Related Products` |
| [!UICONTROL List property for the search results page] | Visualizzazione store | Identifica la proprietà Tag Manager associata alla pagina dei risultati della ricerca. Valore predefinito: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Visualizzazione store | Identifica la proprietà Tag Manager associata alle etichette per le promozioni interne. Valore predefinito: `Label` |

{style="table-layout:auto"}

## Creare un tag per tracciare le conversioni

Se disponi di un account Google AdWords, puoi creare un tag che tiene traccia delle conversioni. Nell&#39;esempio seguente viene illustrato come utilizzare sia [!DNL Google Tag Manager] che [!DNL Google Analytics] per creare un tag che viene attivato nella pagina di conversione _Operazione riuscita_ del tuo archivio.

### Passaggio 1: Creare un tag

1. Accedi al tuo account [!DNL Google Tag Manager] e fai clic sul collegamento per il contenitore creato per il tuo archivio.

1. Nella casella **[!UICONTROL New Tag]** fare clic su **[!UICONTROL Add a new tag]**.

1. Ottieni le seguenti informazioni dal tuo account AdWords:

   - ID conversione
   - Etichetta di conversione

   Se hai bisogno di assistenza, visita il [sito di supporto](https://support.google.com/tagmanager/answer/6105160) di Google.

1. Dal dashboard [!DNL Google Tag Manager], fare clic su **[!UICONTROL Google AdWords]** ed eseguire le operazioni seguenti:

   - Fare clic sul segnaposto del titolo e immettere un nome per il nuovo tag.

   - In **[!UICONTROL Choose Product]**, selezionare **[!UICONTROL Google AdWords]**.

   - In _[!UICONTROL Choose a Tag Type]_, selezionare **[!UICONTROL AdWords Conversion Tracking]**e fare clic su **[!UICONTROL Continue]**.

1. Immetti **[!UICONTROL Conversion ID]** e **[!UICONTROL Conversion Label]** dal tuo account AdWords e fai clic su **[!UICONTROL Continue]**.

### Passaggio 2: Creare una regola

Continuando dal dashboard [!DNL Google Tag Manager], il passaggio successivo consiste nel creare una regola che attivi il tag nella pagina di conversione.

1. In **[!UICONTROL Fire On]**, fare clic su **[!UICONTROL Some Pages]**.

1. Nella sezione _[!UICONTROL Choose Pages]_, completare le impostazioni seguenti:

   - **[!UICONTROL Name]** - Immettere un nome per la descrizione della pagina.

   - **[!UICONTROL Variable]** `url`

   - **Operazione** - `matches RegEx`

     Per ulteriori informazioni, vedere [Operatori di selettori Regex e CSS](https://support.google.com/tagmanager/answer/7679109) nella Guida di Google Tag Manager.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Selezionare la casella di controllo verde e fare clic su **[!UICONTROL Save]**.

   Il trigger impostato viene visualizzato come pulsante blu nella sezione Attivato.

1. Al termine, fare clic su **[!UICONTROL Save Tag]**.

### Passaggio 3: Anteprima e pubblicazione

Il passaggio successivo nel processo consiste nell’visualizzare in anteprima il tag. Ogni volta che il tag viene visualizzato in anteprima, viene salvata un’istantanea della versione. Quando si è soddisfatti dei risultati, passare alla versione che si desidera utilizzare e fare clic su **[!UICONTROL Publish]**.

## Tag HTML personalizzato con JavaScript

Questa sezione spiega come aggiungere un Nonce CSP al JavaScript di tag HTML personalizzato per l’esecuzione sulla pagina di pagamento, garantendo la conformità con i requisiti Content Security Policy (CSP). Questa aggiunta migliora la sicurezza del sito impedendo l&#39;esecuzione di script non autorizzati. Per informazioni più dettagliate, consulta la documentazione di [Content Security Policy](https://developer.adobe.com/commerce/php/development/security/content-security-policies).

>[!NOTE]
>
>L&#39;importazione della variabile globale `cspNonce` in Google Tag Manager è supportata solo in Adobe Commerce versione 2.4.8 e successive.

>[!WARNING]
>
>L&#39;aggiunta di script sconosciuti al tuo archivio può comportare il rischio di compromissione dei dati. Gli script autorizzati nella pagina di pagamento possono sottrarre informazioni riservate dei clienti, inclusi i dettagli di pagamento. È essenziale prendere precauzioni per proteggere il tuo account Google Tag Manager. Aggiungi solo script attendibili, controlla e controlla regolarmente i tag e implementa misure di sicurezza avanzate come l’autenticazione a due fattori (2FA) e i controlli di accesso.

### Passaggio 1: Creare una variabile Nonce CSP

Puoi creare una variabile Nonce CSP che può essere utilizzata all’interno di Google Tag Manager importando la configurazione della variabile o configurandola manualmente.

#### Importare la configurazione della variabile

La variabile Nonce CSP è inclusa nel contenitore di esempio [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt). Puoi creare la variabile importando questo codice nell’area di lavoro.

#### Creare la variabile manualmente

Se non riesci a importare la configurazione della variabile, completa i passaggi seguenti per crearla.

1. Nell&#39;area di lavoro, passa alla sezione **Variabili** nella barra laterale.
1. Fai clic sul pulsante **Nuovo** nella parte inferiore della pagina nella sezione **Variabili definite dall&#39;utente**.
1. Denomina la variabile `gtmNonce`.
1. Fai clic sull’icona della matita per modificare la variabile.
1. Seleziona **Variabile JavaScript** dalla sezione **Variabile pagina**.
1. Nel campo **Nome variabile globale** immettere `window.cspNonce`.
1. Salva la variabile.

Per ulteriori informazioni sulle [variabili di Google Tag Manager](https://support.google.com/tagmanager/answer/7683056?hl=en), consulta [Tipi di variabili definite dall&#39;utente per il Web](https://support.google.com/tagmanager/answer/7683362?hl=en) nella documentazione di Google. Questa documentazione offre indicazioni dettagliate sulla creazione e la gestione di variabili personalizzate per adattare la gestione dei tag a esigenze di marketing e analisi specifiche.

### Passaggio 2: Creare un tag HTML personalizzato

1. Nell&#39;area di lavoro, passa alla sezione **Tag** nella barra laterale.
1. Fare clic sul pulsante **Nuovo**.
1. Nella sezione **Configurazione tag**, seleziona **Tag HTML personalizzato**.
1. Immettere il JavaScript richiesto nell&#39;area di testo e aggiungere un attributo nonce al tag di apertura `<script>` che punta alla variabile creata nel passaggio precedente. Ad esempio:

   ```html
   <script nonce="{{gtmNonce}}">
       // Your JavaScript code here
   </script>
   ```

1. Selezionare **Documento di supporto.scrittura**.
1. Nella sezione **Attivazione** selezionare il trigger desiderato. Ad esempio, **Inizializzazione del consenso - Tutte le pagine**.

Per ulteriori informazioni su [Tag](https://support.google.com/tagmanager/answer/3281060) in Gestione tag di Google, vedere [Tag personalizzati](https://support.google.com/tagmanager/answer/6107167) nella documentazione di Google.
