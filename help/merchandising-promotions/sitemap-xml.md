---
title: Mappe del sito
description: Scopri come configurare una mappa del sito per indicizzare tutte le pagine e le immagini dei siti Commerce.
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 0%

---

# Mappe del sito

Una mappa del sito migliora il modo in cui il tuo archivio viene indicizzato dai motori di ricerca ed è progettata per trovare pagine che potrebbero essere ignorate dai crawler web. È possibile configurare una mappa del sito per indicizzare tutte le pagine e le immagini.

Quando questa opzione è attivata, in Commerce viene creato un file denominato `sitemap.xml` salvata nell&#39;installazione nel percorso specificato. La configurazione consente di impostare la frequenza degli aggiornamenti e la priorità per ogni tipo di contenuto. La mappa del sito deve essere aggiornata con la stessa frequenza con cui cambia il contenuto, che può essere giornaliero, settimanale o mensile.

Mentre il sito è in fase di sviluppo, è possibile includere istruzioni nel `robots.txt` file per i crawler web per evitare l’indicizzazione del sito. Quindi, prima del lancio, puoi modificare le istruzioni per consentire l’indicizzazione del sito.

Per informazioni tecniche, consulta [Aggiungi sitemap e robots.txt][1] nel _Guida di Commerce su infrastruttura cloud_.

![Griglia mappa del sito](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## Passaggio 1: Configurare la mappa del sito

Completa il [Configurazione mappa del sito XML](#site-map-configuration) per determinare cosa è incluso e con quale frequenza viene aggiornata la mappa del sito.

## Passaggio 2: Genera la mappa del sito

1. Il giorno _Amministratore_ menu, vai a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Clic **[!UICONTROL Add Site Map]**.

   ![Griglia mappa del sito](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. Immetti la mappa del sito **[!UICONTROL Filename]**. Ad esempio: `sitemap.xml`

1. Inserisci il **[!UICONTROL Path]** per determinare la posizione del file di mappa del sito sul server. Assicurati che il percorso sia scrivibile.

   - `/sitemap/` - Inserisce il file di mappa del sito in una directory denominata _sitemap_.

   - `/` : inserisce il file di mappa del sito nel percorso di base o nella directory principale dell’installazione di Commerce.

   ![Nuova mappa del sito](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save & Generate]**.

   La visualizzazione della mappa del sito nella griglia potrebbe richiedere alcuni minuti.

## Passaggio 3: Configurare e abilitare robots.txt (facoltativo)

Completa il [robot per motori di ricerca](seo-overview.md#search-engine-robots) con istruzioni che indirizzano i motori di ricerca a eseguire la ricerca per indicizzazione delle parti del sito che si desidera indicizzare.

## Passaggio 4: Inviare la mappa del sito ai motori di ricerca

Puoi inviare la mappa del sito a diversi motori di ricerca fornendo il collegamento a `sitemap.xml` nell’installazione di Commerce. Per copiare il collegamento, effettuare le seguenti operazioni:

1. In _Mappa del sito_ , fare clic con il pulsante destro del mouse sull&#39;URL nella **[!UICONTROL Link for Google]** colonna.

1. Scegliere dal menu **[!UICONTROL Copy Link Address]**.

Per ulteriori informazioni, consulta le istruzioni per il motore di ricerca specifico. Di seguito sono riportati i collegamenti alle istruzioni per i due principali motori di ricerca:

- [Google][2]
- [Microsoft® Bing][3]

## Passaggio 5: ripristinare le istruzioni robot precedenti (facoltativo)

Ora puoi ripristinare le restrizioni originali (predefinite).

## Gestione di sitemap e robots.txt per più siti Web

Se disponi di più siti web, puoi semplificare il processo di creazione e invio di sitemap. Semplicemente [creare](#site-map-configuration) una o più sitemap che includono URL per tutti gli archivi verificati e salvano le sitemap in un’unica posizione. Tutti i siti devono essere verificati in [Console di ricerca Google](https://support.google.com/webmasters/answer/7451001).

Per creare sitemap per un&#39;istanza multistore, effettuare le seguenti operazioni:

1. Crea una cartella denominata `sitemaps` nella directory principale del sito web, quindi crea sottocartelle per ciascun dominio:

       /sitemaps/domain_1/
       /sitemaps/domain_2/
   
1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Crea o modifica gli elenchi di sitemap per ogni store e imposta la **[!UICONTROL Path]** a quello creato per lo store:

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. Se necessario, aggiorna il file robots.txt.

   Per fare in modo che i spider del motore di ricerca siano correttamente indirizzati alle nuove sitemap, puoi aggiornare o creare il file robots.txt. Aggiungi le seguenti righe in alto.

       Mappa del sito web
       Mappa del sito: https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       Mappa del sito: https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>Se il sito utilizza [Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html) motore del server web, è necessario aggiornare il [`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html) nella directory principale del sito web per indirizzare eventuali altre richieste di sitemap nella posizione corretta.

## Descrizioni delle colonne

| Colonna | Descrizione |
|------|-----------|
| [!UICONTROL ID] | Numero di record sequenziale della mappa del sito corrente. |
| [!UICONTROL Filename] | Nome file della mappa del sito. |
| [!UICONTROL Path] | Posizione in cui risiede la mappa del sito sul server. Ad esempio: <br/>`/sitemap/` - Inserisce il file di mappa del sito in una directory denominata _sitemap_, un livello sotto la radice dell’installazione Commerce. <br/>`/` : inserisce il file di mappa del sito nel percorso di base o nella directory principale dell’installazione di Commerce. |
| [!UICONTROL Link for Google] | URL della mappa del sito da inviare a Google e ad altri motori di ricerca. |
| [!UICONTROL Last Generated] | Indica la data e l&#39;ora dell&#39;ultima generazione della mappa del sito. |
| [!UICONTROL Store View] | Visualizzazione del punto vendita in cui si applica la mappa del sito. |
| [!UICONTROL Generate] | Rigenera la mappa del sito. |

{style="table-layout:auto"}

## Configurazione mappa del sito

La mappa del sito deve essere aggiornata con la stessa frequenza con cui cambia il contenuto sul sito, che può essere su base giornaliera, settimanale o mensile. La configurazione ti consente di impostare la frequenza e la priorità per ciascun tipo di contenuto.

### Passaggio 1: Impostare la frequenza e la priorità degli aggiornamenti dei contenuti

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL XML Sitemap]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Categories Options]** ed effettuare le seguenti operazioni:

   >[!NOTE]
   >
   >Se necessario, cancellare il **[!UICONTROL Use system value]** per modificare queste impostazioni.

   - Imposta **[!UICONTROL Frequency]** a uno dei seguenti elementi:

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - Per **[!UICONTROL Priority]**, immetti un valore compreso tra `0.0` e `1.0`. Zero ha la priorità più bassa.

   ![Mappa del sito XML - Opzioni Categorie](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedi [Opzioni Categorie](../configuration-reference/catalog/xml-sitemap.md#categories-options) nel _Riferimento configurazione_.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Products Options]** e completare la sezione **[!UICONTROL Frequency]** e **[!UICONTROL Priority]** in base alle esigenze.

   Per un elenco dettagliato di queste opzioni, vedi [Opzioni prodotti](../configuration-reference/catalog/xml-sitemap.md#products-options) nel _Riferimento configurazione_.

1. Per determinare l’estensione dell’inclusione delle immagini nella mappa del sito, imposta **[!UICONTROL Add Images into Sitemap]** a uno dei seguenti elementi:

   - `None`
   - `Base Only`
   - `All`

   ![Configurazione del catalogo - Prodotti sitemap XML](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL CMS Pages Options]** e completare la sezione **[!UICONTROL Frequency]** e **[!UICONTROL Priority]** in base alle esigenze.

   ![Configurazione del catalogo - Pagine CMS di sitemap XML](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedi [Opzioni pagine CMS](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options) nel _Riferimento configurazione_.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Store Url Options]** e completare la sezione **[!UICONTROL Frequency]** e **[!UICONTROL Priority]** in base alle esigenze.

   ![Configurazione del catalogo - URL archivio mappa del sito XML](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedi [Opzioni URL store](../configuration-reference/catalog/xml-sitemap.md#store-url-options) nel _Riferimento configurazione_.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Passaggio 2: Completare le impostazioni di generazione

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Generation Settings]** sezione.

   Se necessario, cancellare il **Usa valore di sistema** per modificare queste impostazioni.

   ![Configurazione del catalogo - Impostazioni di generazione sitemap XML](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedi [Impostazioni di generazione](../configuration-reference/catalog/xml-sitemap.md#generation-settings) nel _Riferimento configurazione_.

1. Per generare una mappa del sito, imposta **[!UICONTROL Enabled]** a `Yes` ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Start Time]** all’ora, al minuto e al secondo in cui desideri aggiornare la mappa del sito.

   - Imposta **[!UICONTROL Frequency]** a uno dei seguenti elementi:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - Per **[!UICONTROL Error Email Recipient]**, immetti l’indirizzo e-mail della persona che deve ricevere la notifica se si verifica un errore durante l’aggiornamento di una sitemap.

   - Imposta **[!UICONTROL Error Email Sender]** al contatto dell&#39;archivio che viene visualizzato come mittente della notifica di errore.

   - Imposta **[!UICONTROL Error Email Template]** al modello utilizzato per la notifica di errore.

### Passaggio 3: Impostare i limiti per i file di mappa del sito

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Sitemap File Limits]** sezione.

   ![Configurazione del catalogo - Limiti del file sitemap XML](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedi [Limiti file Sitemap](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits) nel _Riferimento configurazione_.

1. Per **[!UICONTROL Maximum No of URLs per File]**, immetti il numero massimo di URL che possono essere inclusi in sitemap.

   Per impostazione predefinita, il limite è 50.000.

1. Per **[!UICONTROL Maximum File Size]**, immetti la dimensione maggiore in byte allocata per la mappa del sito.

   La dimensione predefinita è 10.485.760 byte.

### Passaggio 4: Impostare le impostazioni di invio del motore di ricerca

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Submission Settings]** sezione.

   ![Configurazione del catalogo - Impostazioni di invio del motore di ricerca XML sitemap](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. Se si utilizza un `robots.txt` file per fornire istruzioni ai motori di ricerca che eseguono la ricerca per indicizzazione del sito, impostare **[!UICONTROL Enable Submission to Robots.txt]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed
