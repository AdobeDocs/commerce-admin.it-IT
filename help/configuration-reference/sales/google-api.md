---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Sales] &gt; [!UICONTROL Google API] dell'amministratore di Commerce.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: 5ee52e8d4f2ebb8fc28f13cca53e87c3529f76d3
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://experienceleague.adobe.com/it/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Visualizzazione store | Abilita [!DNL Google Analytics] per il tuo archivio. Opzioni: `Yes` / `No` |
| [!UICONTROL Account Type] | Visualizzazione store | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) determina le opzioni di configurazione in base al tipo di account Google Analytics. Opzioni: Universal Analytics (predefinito) / Google Tag Manager |
| [!UICONTROL Account Number] | Visualizzazione store | Numero di account, o codice di registrazione, assegnato al momento della creazione dell&#39;account [!DNL Google Analytics]. |
| [!UICONTROL Anonymize IP] | Visualizzazione store | Determina se le informazioni di identificazione vengono rimosse dagli indirizzi IP visualizzati nei risultati [!DNL Google Analytics]. |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Tipo di account Google Tag Manager](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

Quando **[!UICONTROL Account Type]** è impostato su `Google Tag Manager`, sono visualizzati campi aggiuntivi.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | Visualizzazione store | ID univoco del contenitore [!DNL Google Tag Manager]. Questo valore inizia in genere con `GTM-`. Questo ID si trova nel tuo account [!DNL Google Tag Manager]. Se [!DNL Google Tag Manager] è già installato e configurato per il tuo archivio, l&#39;ID contenitore viene visualizzato automaticamente in questo campo. |
| [!UICONTROL List property for the catalog page] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata alla pagina del catalogo. Valore predefinito: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata al blocco di cross-selling. Valore predefinito: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata al blocco di up-sell. Valore predefinito: `Up-sell` |
| [!UICONTROL List property for the related products block] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata al blocco prodotti correlati. Valore predefinito: `Related Products` |
| [!UICONTROL List property for the search results page] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata alla pagina dei risultati di ricerca. Valore predefinito: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata alle etichette per le promozioni interne. Valore predefinito: `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://experienceleague.adobe.com/it/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Visualizzazione store | Abilita Google AdWords per lo store. Opzioni: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Visualizzazione store | L’ID dall’account Google AdWords. |
| [!UICONTROL Conversion Language] | Visualizzazione store | Linguaggio utilizzato per le conversioni AdWords. Opzioni: `All available languages` |
| [!UICONTROL Conversion Format] | Visualizzazione store | Determina il formato della notifica [!DNL Google Site Stats] visualizzata nella pagina di conversione. La notifica è collegata a una pagina che informa i visitatori in merito ai cookie utilizzati per tenere traccia delle loro visite. Questo valore numerico è assegnato alla variabile `google_conversion_format` nello script AdWords. Per ulteriori informazioni, consulta [Informazioni sul monitoraggio delle conversioni](https://support.google.com/google-ads/answer/1722022?hl=en) sul sito Web Google. Opzioni: <br/>**`1`**- Visualizza una notifica su una riga.<br/>**`2`** - (Predefinito) Visualizza una notifica su due righe. <br/>**`3`**- Nessuna notifica del cliente. |
| [!UICONTROL Conversion Color] | Visualizzazione store | Determina il colore dell&#39;etichetta di conversione. Utilizza un selettore [colori](https://www.w3schools.com/colors/colors_picker.asp) per scegliere il valore esadecimale. Questo valore esadecimale è assegnato alla variabile `google_conversion_color` nello script AdWords. Esempio: ffffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Visualizzazione store | Etichetta di testo visualizzata con la notifica [!DNL Google Site Stats]. Questa stringa di testo è assegnata alla variabile `~` nello script AdWords. Ad esempio: &quot;Grazie per lo shopping!&quot; |
| [!UICONTROL Conversion Value Type] | Visualizzazione store | Specifica il tipo di valore utilizzato per determinare quando si verifica una conversione. Opzioni: <br/>**`Dynamic`**- Determina che si è verificata una conversione in base all&#39;importo dell&#39;ordine dinamico.<br/>**`Constant`** - Determina che si è verificata una conversione in base al valore immesso. |
| [!UICONTROL Conversion Value] | Visualizzazione store | Specifica il valore utilizzato per un tipo di valore di conversione _[!UICONTROL Constant]_. |
| [!UICONTROL Send Order Currency] | Visualizzazione store | Abilita i valori di conversione della valuta specifici della transazione in AdWords (per siti Web con valute di base diverse). |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![Google Analytics4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://experienceleague.adobe.com/it/docs/commerce-admin/marketing/google-tools/google-analytics) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Visualizzazione store | Abilita Google Analytics 4 per lo store. Opzioni: `Yes` / `No` |
| [!UICONTROL Account Type] | Visualizzazione store | ![Adobe Commerce](../../assets/adobe-logo.svg) (solo Adobe Commerce) determina le opzioni di configurazione in base al tipo di account Google Analytics. Opzioni: `Google Analytics4` (predefinito) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | Visualizzazione store | Il numero di account, o codice di tracciamento, assegnato al momento della creazione dell&#39;account Google Analytics. |
| [!UICONTROL Anonymize IP] | Visualizzazione store | Determina se rimuovere le informazioni di identificazione dagli indirizzi IP visualizzati nei risultati di Google Analytics. |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Tipo di account Google Tag Manager](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

Quando **[!UICONTROL Account Type]** è impostato su `Google Tag Manager`, sono visualizzati campi aggiuntivi.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | Visualizzazione store | ID univoco del contenitore [!DNL Google Tag Manager]. Questo valore inizia in genere con `GTM-`. L&#39;ID si trova nell&#39;account Google Tab Manager. Se [!DNL Google Tag Manager] è già installato e configurato per il tuo archivio, l&#39;ID contenitore viene visualizzato automaticamente in questo campo. |
| [!UICONTROL List property for the catalog page] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata alla pagina del catalogo. Valore predefinito: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata al blocco di cross-selling. Valore predefinito: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata al blocco di up-sell. Valore predefinito: `Up-sell` |
| [!UICONTROL List property for the related products block] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata al blocco prodotti correlati. Valore predefinito: `Related Products` |
| [!UICONTROL List property for the search results page] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata alla pagina dei risultati di ricerca. Valore predefinito: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | Visualizzazione store | Identifica la proprietà [!DNL Google Tag Manager] associata alle etichette per le promozioni interne. Valore predefinito: `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://experienceleague.adobe.com/it/docs/commerce-admin/marketing/google-tools/google-adwords) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | Visualizzazione store | Abilita Google AdWords per lo store. Opzioni: `Yes` / `No` |
| [!UICONTROL Conversion ID] | Visualizzazione store | L’ID dall’account Google AdWords. |
| [!UICONTROL Conversion Language] | Visualizzazione store | Linguaggio utilizzato per le conversioni AdWords. Opzioni: tutte le lingue disponibili |
| [!UICONTROL Conversion Format] | Visualizzazione store | Determina il formato della notifica Google Site Stats visualizzata nella pagina di conversione. La notifica è collegata a una pagina che informa i visitatori in merito ai cookie utilizzati per tenere traccia delle loro visite. Questo valore numerico è assegnato alla variabile `google_conversion_format` nello script AdWords. Per ulteriori informazioni, consulta [Informazioni sul monitoraggio delle conversioni](https://support.google.com/google-ads/answer/1722022?hl=en) sul sito Web Google. Opzioni: <br/>**`1`**- Visualizza una notifica su una riga.<br/>**`2`** - (Predefinito) Visualizza una notifica su due righe. <br/>**`3`**- Nessuna notifica del cliente. |
| [!UICONTROL Conversion Color] | Visualizzazione store | Determina il colore dell&#39;etichetta di conversione. Utilizza un selettore [colori](https://www.w3schools.com/colors/colors_picker.asp) per scegliere il valore esadecimale. Questo valore esadecimale è assegnato alla variabile `google_conversion_color` nello script AdWords. Esempio: ffffffff `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | Visualizzazione store | Etichetta di testo visualizzata con la notifica Statistiche sito Google. Questa stringa di testo è assegnata alla variabile `~` nello script AdWords. Ad esempio: &quot;Grazie per lo shopping!&quot; |
| [!UICONTROL Conversion Value Type] | Visualizzazione store | Specifica il tipo di valore utilizzato per determinare quando si verifica una conversione. Opzioni: <br/>**`Dynamic`**- Determina che si è verificata una conversione in base all&#39;importo dell&#39;ordine dinamico.<br/>**`Constant`** - Determina che si è verificata una conversione in base al valore immesso. |
| [!UICONTROL Conversion Value] | Visualizzazione store | Specifica il valore utilizzato per un tipo di valore di conversione _[!UICONTROL Constant]_. |
| [!UICONTROL Send Order Currency] | Visualizzazione store | Abilita i valori di conversione della valuta specifici della transazione in AdWords (per siti Web con valute di base diverse). |

{style="table-layout:auto"}
