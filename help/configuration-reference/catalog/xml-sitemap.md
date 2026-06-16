---
title: '[!UICONTROL Catalog] > [!UICONTROL XML Sitemap]'
description: Rivedi le impostazioni di configurazione nella pagina [!UICONTROL Catalog] > [!UICONTROL XML Sitemap] dell'amministratore di Commerce.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
TQID: https://experienceleague.adobe.com/1oTTRT977C3zcifhCRFBuXf7ny-6rqGSC--enriyj-Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 381
ht-degree: 2%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![Opzioni Categorie](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://experienceleague.adobe.com/it/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui le categorie della mappa del sito vengono aggiornate. Opzioni: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Visualizzazione store | Valore compreso tra `0.0` e `1.0` che determina la priorità degli aggiornamenti di sitemap di categoria in relazione ad altri contenuti. Zero (`0.0`) ha la priorità più bassa. |

{style="table-layout:auto"}

## [!UICONTROL Products Options]

![Opzioni prodotti](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://experienceleague.adobe.com/it/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui i prodotti sitemap vengono aggiornati. Opzioni: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Visualizzazione store | Valore compreso tra `0.0` e `1.0` che determina la priorità degli aggiornamenti di sitemap del prodotto in relazione ad altri contenuti. Zero (`0.0`) ha la priorità più bassa. |
| [!UICONTROL Add Images into Sitemap] | Visualizzazione store | Determina il livello di inclusione delle immagini nella sitemap. Opzioni: `None` / `Base Only` / `All` |

{style="table-layout:auto"}

## [!UICONTROL CMS Pages Options]

![Opzioni pagine CMS](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://experienceleague.adobe.com/it/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui vengono aggiornate le pagine CMS di sitemap. Opzioni: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Visualizzazione store | Valore compreso tra `0.0` e `1.0` che determina la priorità degli aggiornamenti della mappa del sito della pagina di CMS in relazione ad altri contenuti. Zero (`0.0`) ha la priorità più bassa. |

{style="table-layout:auto"}

## [!UICONTROL Store Url Options]

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui vengono aggiornati gli URL dei negozi. Opzioni: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | Visualizzazione store | Valore compreso tra `0.0` e `1.0` che determina la priorità degli aggiornamenti dell&#39;URL dell&#39;archivio in relazione ad altri contenuti. Zero (`0.0`) ha la priorità più bassa. |

{style="table-layout:auto"}

## [!UICONTROL Generation Settings]

![Impostazioni generazione](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://experienceleague.adobe.com/it/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Visualizzazione store | Determina se una mappa del sito XML è disponibile per l&#39;archivio. Opzioni: `Yes` / `No` |
| [!UICONTROL Generation Method] | Visualizzazione store | Determina la modalità di generazione della mappa del sito XML. `Standard` utilizza il tradizionale processo di generazione sincrona ed elabora tutti i dati in memoria, mentre `Batch` utilizza una modalità batch asincrona con ottimizzazione per la memoria per una maggiore flessibilità e scalabilità. Questa opzione è disponibile a partire dalla versione 2.4.9 di. Opzioni: `Standard` / `Batch` |
| [!UICONTROL Start Time] | Visualizzazione store | Specifica l’ora, il minuto e il secondo del giorno in cui viene aggiornata la mappa del sito. |
| [!UICONTROL Frequency] | Visualizzazione store | Determina la frequenza con cui viene aggiornata la mappa del sito. Opzioni: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | Visualizzazione store | L’indirizzo e-mail della persona che riceve la notifica se si verifica un errore durante il processo di aggiornamento di sitemap. Per più indirizzi, separali con una virgola. |
| [!UICONTROL Error Email Sender] | Sito Web | Identifica il contatto dell&#39;archivio che viene visualizzato come mittente della notifica di errore. Opzioni: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | Sito Web | Identifica il modello e-mail utilizzato per la notifica dell’errore. Modello predefinito: `Sitemap generate Warnings` |

{style="table-layout:auto"}

## [!UICONTROL Sitemap File Limits]

![Limiti file Sitemap](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://experienceleague.adobe.com/it/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | Visualizzazione store | Determina il numero massimo di URL che possono essere inclusi in una singola sitemap. |
| [!UICONTROL Maximum File Size] | Visualizzazione store | Determina la dimensione massima in byte della mappa del sito generata. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Submission Settings]

![Impostazioni invio motore di ricerca](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://experienceleague.adobe.com/it/docs/commerce-admin/marketing/seo/sitemap-xml) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | Visualizzazione store | Consente di inviare le direttive per il file robots.txt. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}
