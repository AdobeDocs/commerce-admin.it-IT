---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL General] &gt; [!UICONTROL Content Management] dell'amministratore di Commerce.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![Opzioni WYSIWYG](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/wysiwyg/editor) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | Visualizzazione store | Determina se l&#39;editor è abilitato per l&#39;archivio. Opzioni: Attivato completamente per impostazione predefinita/Disattivato per impostazione predefinita/Disattivato |
| [!UICONTROL WYSIWYG Editor] | Sito Web | Determina la versione dell&#39;editor TinyMCE utilizzata per l&#39;editor WYSIWYG. Opzioni: <br/>**`TinyMCE 5`**- (predefinito) Utilizza TinyMCE versione 5 come editor predefinito di WYSIWYG.<br><br>_ **&#x200B; Nota:**&#x200B;_un aggiornamento alla libreria TinyMCE 5.10 in Adobe Commerce e Magento Open Source 2.4.5 risolve una vulnerabilità che consentiva l&#39;esecuzione arbitraria di JavaScript durante l&#39;aggiornamento di un&#39;immagine o di un collegamento tramite alcuni tipi di URL. TinyMCE 3 è stato dichiarato obsoleto nella versione 2.4.0 e rimosso nella versione 2.4.3. TinyMCE 4 è stato rimosso nella versione 2.4.4. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | Globale | Determina se [URL statici](../../content-design/catalog-urls-dynamic-media.md) vengono utilizzati per i contenuti multimediali a cui si fa riferimento dall&#39;editor di WYSIWYG. L’impostazione si applica a tutte le posizioni in cui è disponibile l’editor di WYSIWYG, inclusi prodotti, categorie, pagine e blocchi. Opzioni: <br/>**`Yes`**- Utilizza URL statici per i contenuti multimediali inseriti con l&#39;editor WYSIWYG. Gli URL statici sono assoluti e si interrompono se l&#39;[URL di base](../../stores-purchase/store-urls.md) dell&#39;archivio cambia.<br/>**`No`** (predefinito) - Utilizza URL dinamici per contenuti multimediali inseriti con l&#39;editor WYSIWYG, in base alla direttiva `{{media url="..."}}`. Gli URL dinamici sono relativi e non si interrompono se l’URL di base dell’archivio cambia. |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![Gerarchia pagine CMS](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/pages/page-hierarchy) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Globale | Attiva l&#39;utilizzo della gerarchia di pagine per le pagine di contenuto. Opzioni: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Globale | Consente di associare i metadati alle pagine della gerarchia. Opzioni: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Globale | Determina lo stile di menu predefinito. Opzioni: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![Strumenti di contenuto avanzati](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://experienceleague.adobe.com/en/docs/commerce-admin/page-builder/walkthrough/3-catalog-content) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | Globale | Determina se sono disponibili gli strumenti di contenuto avanzato [!DNL Page Builder]. Opzioni: <br/>**`Yes`**- L&#39;area di lavoro [!DNL Page Builder] viene visualizzata nella sezione Contenuto di pagine, blocchi, prodotti e categorie.<br/>**`No`** - Gli strumenti di modifica standard di CMS vengono visualizzati nella sezione _[!UICONTROL Content]_&#x200B;di pagine, blocchi, prodotti e categorie. |
| [!UICONTROL Enable Page Builder Content Preview] | Globale | Determina se le anteprime di contenuto [!DNL Page Builder] sono abilitate per prodotti e categorie. Opzioni: `Yes` / `No` <br/>**_Nota:_**&#x200B;Questa opzione è impostata su `Yes` per impostazione predefinita, ma la disattivazione dell&#39;anteprima può evitare problemi di prestazioni derivanti dal caricamento delle anteprime all&#39;interno di un modulo di prodotto o categoria. |
| [!UICONTROL Google Maps API Key] | Globale | La chiave API [!DNL Google Maps] dal tuo account Google. |
| [!UICONTROL Test Key] |  | Convalida la chiave API [!DNL Google Maps]. |
| [!UICONTROL Google Maps Style] | Globale | Incolla qui il codice JSON di stile [!DNL Google Maps] per cambiare l&#39;aspetto del tipo di contenuto Mappa. |
| [!UICONTROL Default Column Grid Size] | Globale | Determina il numero predefinito di colonne nella griglia [!DNL Page Builder]. |
| [!UICONTROL Maximum Column Grid Size] | Globale | Determina il numero massimo di colonne nella griglia [!DNL Page Builder]. |

{style="table-layout:auto"}

>[!TIP]
>
>Page Builder semplifica la creazione di pagine ricche di contenuti con layout personalizzati che migliorano la narrazione visiva e stimolano il coinvolgimento e la fedeltà dei clienti. Queste funzioni sono progettate per migliorare la qualità e ridurre i tempi e i costi della produzione di pagine personalizzate. Per ulteriori informazioni su queste funzioni e su come utilizzarle per creare contenuti coinvolgenti per il tuo archivio Adobe Commerce o Magento Open Source, consulta la [_Guida utente di Page Builder_](../../page-builder/guide-overview.md).
