---
title: Localizzazione dello store
description: Scopri come localizzare una visualizzazione store o store.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 248c60b20d8554fc73f94cfd249ac3fd7b677f62
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# Localizzazione dello store

La maggior parte del testo che appare hardcoded sulle pagine in tutto il negozio può essere istantaneamente cambiato in una lingua diversa cambiando le impostazioni locali della visualizzazione. La modifica delle impostazioni locali non traduce il testo parola per parola, ma fa semplicemente riferimento a una tabella di traduzione diversa che fornisce il testo di interfaccia utilizzato in tutto l’archivio. Il testo che può essere modificato include titoli di navigazione, etichette, pulsanti e collegamenti quali _Carrello_ e _Account personale_. È inoltre possibile utilizzare lo strumento [Traduzione in linea](../configuration-reference/advanced/developer.md) per ritoccare il testo nell&#39;interfaccia.

I Language Pack si trovano in [Traduzioni e localizzazione][1]{:target="_blank"} su Commerce Marketplace. Le nuove estensioni vengono aggiunte in modo continuo a Marketplace, quindi controlla spesso.

## Passaggio 1: installare un Language Pack

Segui le istruzioni standard per l’installazione dell’estensione Language Pack. Per informazioni dettagliate sull&#39;installazione di un&#39;estensione, vedere [Installazione generale di CLI][2] nella _Guida alle estensioni_.

## Passaggio 2: creare una visualizzazione Store per la lingua

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Fare clic su **[!UICONTROL Create Store View]**.

1. Impostare le opzioni per la nuova visualizzazione dello store:

   - **[!UICONTROL Store]** — Scegliere l&#39;archivio padre della visualizzazione.

   - **[!UICONTROL Name]** — Immettere un nome per la visualizzazione archivio. Esempio: portoghese.

     Nell&#39;intestazione dell&#39;archivio, il nome viene visualizzato nel _selettore lingua_.

   - **[!UICONTROL Code]** — Immettere un codice in caratteri minuscoli per identificare la visualizzazione. Esempio: `portuguese`.

   - **[!UICONTROL Status]** - Per attivare la visualizzazione, impostare su `Enabled`.

   - **[!UICONTROL Sort Order]** — (Facoltativo) Immettere un numero per determinare la sequenza in cui la visualizzazione è elencata con altre visualizzazioni.

1. Al termine, fare clic su **[!UICONTROL Save Store View]**.

## Passaggio 3: modificare le impostazioni locali della visualizzazione archivio

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel menu a discesa **[!UICONTROL Scope]**, selezionare la visualizzazione archivio da configurare e fare clic su **[!UICONTROL OK]** quando richiesto.

1. Nella pagina di configurazione *[!UICONTROL General]*, espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Locale Options]**.

1. Deselezionare la casella di controllo **[!UICONTROL Use Website]** e impostare **[!UICONTROL Locale]** nella lingua che si desidera assegnare alla visualizzazione.

   Se sono disponibili diverse varianti della lingua, assicurati di scegliere quella per la regione o il dialetto specifico.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

   Dopo aver modificato la lingua delle impostazioni locali, il contenuto rimanente creato, inclusi i nomi e le descrizioni dei prodotti, le categorie, le [pagine CMS](../content-design/page-translate.md) e i blocchi, deve essere tradotto separatamente per ogni visualizzazione dello store.

## Localizzare i prodotti

Se il negozio dispone di più visualizzazioni in lingue diverse, gli stessi prodotti sono disponibili in ogni visualizzazione del negozio. Puoi utilizzare le stesse informazioni di base sul prodotto, ad esempio SKU, prezzo e livello di inventario, indipendentemente dalla lingua. Quindi, traduci solo il nome del prodotto, i campi di descrizione e i metadati, in base alle esigenze per ogni lingua.

### Passaggio 1: tradurre i campi prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Nella griglia, individua il prodotto da tradurre e aprilo in modalità di modifica.

1. Nell&#39;angolo in alto a sinistra, impostare **[!UICONTROL Store View]** sulla visualizzazione per la traduzione e fare clic su **[!UICONTROL OK]** quando richiesto per confermare.

1. Per ogni campo da modificare, eseguire le operazioni seguenti:

   - Deselezionare la casella di controllo **[!UICONTROL Use Default Value]** a destra del campo.

   - Incolla o digita il testo tradotto nel campo.

   Assicurati di tradurre tutti i campi di testo, tra cui [etichette immagine](../catalog/catalog-images-video.md) e testo alternativo, [campi di ottimizzazione motore di ricerca](../catalog/product-search-engine-optimization.md) ed eventuali [informazioni sulle opzioni personalizzate](../catalog/settings-advanced-custom-options.md).

1. Al termine, fare clic su **[!UICONTROL Save]**.

### Passaggio 2: tradurre le etichette dei campi

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Nell’elenco, individua l’attributo da tradurre e apri in modalità di modifica.

1. Nel pannello a sinistra, scegli **[!UICONTROL Manage Labels]**.

1. Nella sezione _[!UICONTROL Manage Titles]_&#x200B;immettere un&#39;etichetta tradotta per ogni visualizzazione dello store.

   ![Immetti etichette tradotte](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Attribute]**.

### Passaggio 3: tradurre tutte le categorie

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **Categories**.

1. Nell&#39;angolo in alto a sinistra, impostare **[!UICONTROL Store View]** sulla visualizzazione per la traduzione e fare clic su **[!UICONTROL OK]** quando richiesto per confermare.

1. Nella struttura, individua la categoria da tradurre e aprila in modalità di modifica.

1. Per _Informazioni di base_, traduci **[!UICONTROL Category Name]**.

1. Espandi ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione _[!UICONTROL Content]_&#x200B;e traduci **[!UICONTROL Description]**.

1. Espandi ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization Settings]** e traduci i campi seguenti:

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. Nella sezione _[!UICONTROL Search Engine Optimization Settings]_, eseguire le operazioni seguenti per tradurre **[!UICONTROL URL Key]**:

   - Deselezionare la casella di controllo **[!UICONTROL Use Default Value]** a destra del campo.

   - Inserisci il testo tradotto.

   - Verificare che la casella di controllo **[!UICONTROL Create Permanent Redirect for old URL]** sia selezionata.

   ![Traduci chiave URL](./assets/category-translate-url-key.png)

1. Al termine, fare clic su **[!UICONTROL Save Category]**.

1. Ripeti il processo per tutte le categorie utilizzate nell’archivio.

### Passaggio 4: opzioni di traduzione attributi prodotto e attributi

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Seleziona l’attributo da tradurre.

1. Scegliere **[!UICONTROL Manage Labels]** a sinistra e impostare le opzioni **[!UICONTROL Managed Titles]** per definire le conversioni del titolo dell&#39;attributo.

1. Scegliere **[!UICONTROL Properties]** a sinistra e immettere le opzioni dell&#39;attributo tradotto nella sezione **[!UICONTROL Manage Options]**.

   ![Opzioni di gestione](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html?lang=it
