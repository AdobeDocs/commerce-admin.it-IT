---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL General] &gt; [!UICONTROL Content Management] pagina dell’amministratore di Commerce.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![Opzioni WYSIWYG](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Visualizzazione store | Determina se l&#39;editor è abilitato per l&#39;archivio. Opzioni: Attivato completamente per impostazione predefinita/Disattivato per impostazione predefinita/Disattivato |
| [!UICONTROL WYSIWYG Editor] | Sito Web | Determina la versione dell&#39;editor TinyMCE utilizzata per l&#39;editor WYSIWYG. Opzioni: <br/>**`TinyMCE 5`**- (Impostazione predefinita) Utilizza la versione 5 di TinyMCE come editor WYSIWYG predefinito.<br><br>_** Nota:**_Un aggiornamento della libreria TinyMCE 5.10 in Adobe Commerce e Magento Open Source 2.4.5 risolve una vulnerabilità che consentiva l’esecuzione arbitraria di JavaScript durante l’aggiornamento di un’immagine o di un collegamento utilizzando alcuni tipi di URL. TinyMCE 3 è stato dichiarato obsoleto nella versione 2.4.0 e rimosso nella versione 2.4.3. TinyMCE 4 è stato rimosso nella versione 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Globale | Determina se [URL statici](../../content-design/catalog-urls-dynamic-media.md) sono utilizzati per i contenuti multimediali a cui si fa riferimento dall’editor WYSIWYG. L’impostazione si applica a tutte le posizioni in cui è disponibile l’editor WYSIWYG, inclusi prodotti, categorie, pagine e blocchi. Opzioni: <br/>**`Yes`**: utilizza URL statici per i contenuti multimediali inseriti con l’editor WYSIWYG. Gli URL statici sono assoluti e si interrompono se [URL di base](../../stores-purchase/store-urls.md) dell&#39;archivio cambia.<br/>**`No`** (Impostazione predefinita) - Utilizza URL dinamici per i contenuti multimediali inseriti con l’editor WYSIWYG, in base al  `{{media url="..."}}` direttiva. Gli URL dinamici sono relativi e non si interrompono se l’URL di base dell’archivio cambia. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![Gerarchia pagine CMS](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Globale | Attiva l&#39;utilizzo della gerarchia di pagine per le pagine di contenuto. Opzioni: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Globale | Consente di associare i metadati alle pagine della gerarchia. Opzioni: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Globale | Determina lo stile di menu predefinito. Opzioni: `Content` / `Left Column` / `Right Column` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Content Tools]

![Strumenti di contenuto avanzati](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Globale | Determina se [!DNL Page Builder] sono disponibili strumenti di contenuto avanzati. Opzioni: <br/>**`Yes`**- Il [!DNL Page Builder] L’area di lavoro viene visualizzata nella sezione Contenuto di pagine, blocchi, prodotti e categorie.<br/>**`No`** - Gli strumenti di modifica CMS standard vengono visualizzati nel _[!UICONTROL Content]_sezione di pagine, blocchi, prodotti e categorie. |
| [!UICONTROL Enable Page Builder Content Preview] | Globale | Determina se [!DNL Page Builder] le anteprime dei contenuti sono abilitate per prodotti e categorie. Opzioni: `Yes` / `No` <br/>**_Nota:_**Questo è impostato su `Yes` per impostazione predefinita, ma la disattivazione dell’anteprima può evitare problemi di prestazioni derivanti dal caricamento delle anteprime all’interno di un modulo di prodotto o categoria. |
| [!UICONTROL Google Maps API Key] | Globale | Il [!DNL Google Maps] Chiave API dal tuo account Google. |
| [!UICONTROL Test Key] |  | Convalida il [!DNL Google Maps] Chiave API. |
| [!UICONTROL Google Maps Style] | Globale | Incolla il [!DNL Google Maps] applica uno stile al codice JSON qui per cambiare l’aspetto del tipo di contenuto Mappa. |
| [!UICONTROL Default Column Grid Size] | Globale | Determina il numero predefinito di colonne nel [!DNL Page Builder] griglia. |
| [!UICONTROL Maximum Column Grid Size] | Globale | Determina il numero massimo di colonne nel [!DNL Page Builder] griglia. |

{:style=&quot;table-layout:auto&quot;}

>[!TIP]
>
>Page Builder semplifica la creazione di pagine ricche di contenuti con layout personalizzati che migliorano la narrazione visiva e stimolano il coinvolgimento e la fedeltà dei clienti. Queste funzioni sono progettate per migliorare la qualità e ridurre i tempi e i costi della produzione di pagine personalizzate. Per ulteriori informazioni su queste funzioni e su come utilizzarle per creare contenuti coinvolgenti per il tuo archivio Adobe Commerce o Magento Open Source, vedi [_Guida utente di Page Builder_](../../page-builder/guide-overview.md).

{:style=&quot;table-layout:auto&quot;}
