---
title: Localizzazione dello store
description: Scopri come localizzare una visualizzazione store o store.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# Localizzazione dello store

La maggior parte del testo che appare hardcoded sulle pagine in tutto il negozio può essere istantaneamente cambiato in una lingua diversa cambiando le impostazioni locali della visualizzazione. La modifica delle impostazioni locali non traduce il testo parola per parola, ma fa semplicemente riferimento a una tabella di traduzione diversa che fornisce il testo di interfaccia utilizzato in tutto l’archivio. Il testo che può essere modificato include titoli di navigazione, etichette, pulsanti e collegamenti quali _Il mio carrello_ e _Il mio account_. È inoltre possibile utilizzare [Traduzione in linea](../configuration-reference/advanced/developer.md) per ritoccare il testo nell’interfaccia.

I Language Pack si trovano in [Traduzioni e localizzazione][1]{:target=&quot;_blank&quot;} sulla Commerce Marketplace. Le nuove estensioni vengono aggiunte in modo continuo a Marketplace, quindi controlla spesso.

## Passaggio 1: installare un Language Pack

Segui le istruzioni standard per l’installazione dell’estensione Language Pack. Per informazioni dettagliate sull’installazione di un’estensione, consulta [Installazione generale di CLI][2] nel _Guida alle estensioni_.

## Passaggio 2: creare una visualizzazione Store per la lingua

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Clic **[!UICONTROL Create Store View]**.

1. Impostare le opzioni per la nuova visualizzazione dello store:

   - **[!UICONTROL Store]** — Scegliere l&#39;archivio padre della visualizzazione.

   - **[!UICONTROL Name]** — Immettere un nome per la visualizzazione archivio. Esempio: portoghese.

     Nell’intestazione del negozio, il nome viene visualizzato nel _selettore lingua_.

   - **[!UICONTROL Code]** — immettere un codice in caratteri minuscoli per identificare la visualizzazione. Ad esempio: `portuguese`.

   - **[!UICONTROL Status]** — Per attivare la vista, impostate su `Enabled`.

   - **[!UICONTROL Sort Order]** — (Facoltativo) Inserire un numero per determinare la sequenza in cui questa vista viene elencata con altre viste.

1. Al termine, fai clic su **[!UICONTROL Save Store View]**.

## Passaggio 3: modificare le impostazioni locali della visualizzazione archivio

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nell&#39;angolo in alto a sinistra, imposta **[!UICONTROL Store View]** alla vista specifica in cui deve essere applicata la configurazione.

1. Quando viene richiesto di confermare il cambio di ambito, fare clic su **[!UICONTROL OK]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Locale Options]** sezione.

1. Cancella **[!UICONTROL Use Website]** casella di controllo e impostazione **[!UICONTROL Locale]** alla lingua che si desidera assegnare alla visualizzazione.

   Se sono disponibili diverse varianti della lingua, assicurati di scegliere quella per la regione o il dialetto specifico.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

   Dopo aver modificato la lingua della lingua, il contenuto rimanente creato, inclusi nomi e descrizioni dei prodotti, categorie, [CMS](../content-design/page-translate.md) Le pagine e i blocchi devono essere tradotti separatamente per ciascuna visualizzazione store.

## Localizzare i prodotti

Se il negozio dispone di più visualizzazioni in lingue diverse, gli stessi prodotti sono disponibili in ogni visualizzazione del negozio. Puoi utilizzare le stesse informazioni di base sul prodotto, ad esempio SKU, prezzo e livello di inventario, indipendentemente dalla lingua. Quindi, traduci solo il nome del prodotto, i campi di descrizione e i metadati, in base alle esigenze per ogni lingua.

### Passaggio 1: tradurre i campi prodotto

1. Il giorno _Amministratore_ barra laterale, vai a  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Nella griglia, individua il prodotto da tradurre e aprilo in modalità di modifica.

1. Nell&#39;angolo in alto a sinistra, imposta **[!UICONTROL Store View]** alla vista per la traduzione e fai clic su **[!UICONTROL OK]** quando viene richiesto di confermare.

1. Per ogni campo da modificare, eseguire le operazioni seguenti:

   - Deseleziona il **[!UICONTROL Use Default Value]** a destra del campo.

   - Incolla o digita il testo tradotto nel campo.

   Assicurati di tradurre tutti i campi di testo, tra cui [immagine](../catalog/catalog-images-video.md) etichette e testo Alt, [Ottimizzazione motore di ricerca](../catalog/product-search-engine-optimization.md) campi e qualsiasi [Opzioni personalizzate](../catalog/settings-advanced-custom-options.md) informazioni.

1. Al termine, fai clic su **[!UICONTROL Save]**.

### Passaggio 2: tradurre le etichette dei campi

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Nell’elenco, individua l’attributo da tradurre e apri in modalità di modifica.

1. Nel pannello a sinistra, scegli **[!UICONTROL Manage Labels]**.

1. In _[!UICONTROL Manage Titles]_, immettere un&#39;etichetta tradotta per ogni visualizzazione store.

   ![Immetti etichette tradotte](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Attribute]**.

### Passaggio 3: tradurre tutte le categorie

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **Categorie**.

1. Nell&#39;angolo in alto a sinistra, impostare **[!UICONTROL Store View]** alla vista per la traduzione e fai clic su **[!UICONTROL OK]** quando viene richiesto di confermare.

1. Nella struttura, individua la categoria da tradurre e aprila in modalità di modifica.

1. Per _Informazioni di base_, traduci **[!UICONTROL Category Name]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il _[!UICONTROL Content]_sezione e traduzione **[!UICONTROL Description]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimization Settings]** e traduci i campi seguenti:

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. Sotto _[!UICONTROL Search Engine Optimization Settings]_per tradurre il **[!UICONTROL URL Key]**:

   - Cancella **[!UICONTROL Use Default Value]** a destra del campo.

   - Inserisci il testo tradotto.

   - Assicurati che il **[!UICONTROL Create Permanent Redirect for old URL]** è selezionata.

   ![Tradurre la chiave URL](./assets/category-translate-url-key.png)

1. Al termine, fai clic su **[!UICONTROL Save Category]**.

1. Ripeti il processo per tutte le categorie utilizzate nell’archivio.

### Passaggio 4: opzioni di traduzione attributi prodotto e attributi

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Seleziona l’attributo da tradurre.

1. Scegli **[!UICONTROL Manage Labels]** a sinistra e impostare **[!UICONTROL Managed Titles]** opzioni per definire le conversioni del titolo dell’attributo.

1. Scegli **[!UICONTROL Properties]** a sinistra e immetti le opzioni dell’attributo tradotto in **[!UICONTROL Manage Options]** sezione.

   ![Opzioni di gestione](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
