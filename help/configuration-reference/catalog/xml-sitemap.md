---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap] pagina dell’amministratore di Commerce.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Opzioni Categorie](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui le categorie della mappa del sito vengono aggiornate. Opzioni: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Visualizzazione store | Un valore compreso tra `0.0` e `1.0` che determina la priorità degli aggiornamenti di sitemap di categoria in relazione ad altri contenuti. Zero (`0.0`) ha la priorità più bassa. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Products Options]

![Opzioni prodotti](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui i prodotti sitemap vengono aggiornati. Opzioni: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Visualizzazione store | Un valore compreso tra `0.0` e `1.0` che determina la priorità degli aggiornamenti di sitemap del prodotto in relazione ad altri contenuti. Zero (`0.0`) ha la priorità più bassa. |
| [!UICONTROL Add Images into Sitemap] | Visualizzazione store | Determina il livello di inclusione delle immagini nella sitemap. Opzioni: `None` / `Base Only` / `All` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CMS Pages Options]

![Opzioni pagine CMS](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui vengono aggiornate le pagine CMS di sitemap. Opzioni: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Visualizzazione store | Un valore compreso tra `0.0` e `1.0` che determina la priorità degli aggiornamenti della mappa del sito della pagina CMS in relazione ad altri contenuti. Zero (`0.0`) ha la priorità più bassa. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Store Url Options]

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui vengono aggiornati gli URL dei negozi. Opzioni: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Visualizzazione store | Un valore compreso tra `0.0` e `1.0` che determina la priorità degli aggiornamenti dell’URL del punto vendita in relazione ad altri contenuti. Zero (`0.0`) ha la priorità più bassa. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Generation Settings]

![Impostazioni di generazione](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Visualizzazione store | Determina se una mappa del sito XML è disponibile per l&#39;archivio. Opzioni: `Yes` / `No` |
| [!UICONTROL Start Time] | Visualizzazione store | Specifica l’ora, il minuto e il secondo del giorno in cui viene aggiornata la mappa del sito. |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui viene aggiornata la mappa del sito. Opzioni: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Visualizzazione store | L’indirizzo e-mail della persona che riceve la notifica se si verifica un errore durante il processo di aggiornamento di sitemap. Per più indirizzi, separali con una virgola. |
| [!UICONTROL Error Email Sender] | Sito Web | Identifica il contatto dell&#39;archivio che viene visualizzato come mittente della notifica di errore. Opzioni: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Sito Web | Identifica il modello e-mail utilizzato per la notifica dell’errore. Modello predefinito: `Sitemap generate Warnings` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Sitemap File Limits]

![Limiti file Sitemap](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | Visualizzazione store | Determina il numero massimo di URL che possono essere inclusi in una singola sitemap. |
| [!UICONTROL Maximum File Size] | Visualizzazione store | Determina la dimensione massima in byte della mappa del sito generata. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Search Engine Submission Settings]

![Impostazioni invio motore di ricerca](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | Visualizzazione store | Consente di inviare le direttive per il file robots.txt. Opzioni: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
