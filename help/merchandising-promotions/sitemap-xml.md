---
title: Mappe del sito
description: Scopri come configurare una mappa del sito per indicizzare tutte le pagine e le immagini dei siti Commerce.
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# Mappe del sito

>[!TIP]
>
>Per Adobe Commerce as a Cloud Service, consulta le [linee guida SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=it) nella documentazione di Commerce Storefront

Una mappa del sito migliora il modo in cui il tuo archivio viene indicizzato dai motori di ricerca ed è progettata per trovare pagine che potrebbero essere ignorate dai crawler web. È possibile configurare una mappa del sito per indicizzare tutte le pagine e le immagini.

Quando è abilitato, Commerce crea un file denominato `sitemap.xml` che viene salvato nell&#39;installazione nel percorso specificato. La configurazione consente di impostare la frequenza degli aggiornamenti e la priorità per ogni tipo di contenuto. La mappa del sito deve essere aggiornata con la stessa frequenza con cui cambia il contenuto, che può essere giornaliero, settimanale o mensile.

Mentre il sito è in fase di sviluppo, è possibile includere istruzioni nel file `robots.txt` per i crawler Web per evitare l&#39;indicizzazione del sito. Quindi, prima del lancio, puoi modificare le istruzioni per consentire l’indicizzazione del sito.

Per informazioni tecniche, consulta [Aggiungere sitemap e robots.txt][1] nella _Guida di Commerce sull&#39;infrastruttura cloud_.

![Griglia mappa del sito](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## Passaggio 1: Configurare la mappa del sito

Completare la [configurazione XML Sitemap](#site-map-configuration) per determinare gli elementi inclusi e la frequenza con cui viene aggiornato il mapping del sito.

## Passaggio 2: Genera la mappa del sito

1. Nel menu _Amministratore_, vai a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Fare clic su **[!UICONTROL Add Site Map]**.

   ![Griglia mappa sito](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. Immettere la mappa del sito **[!UICONTROL Filename]**. Esempio: `sitemap.xml`

1. Immettere **[!UICONTROL Path]** per determinare la posizione in cui deve risiedere il file di mappa del sito sul server. Assicurati che il percorso sia scrivibile.

   - `/sitemap/` - Inserisce il file di mappa del sito in una directory denominata _sitemap_.

   - `/` - Inserisce il file di mappa del sito nel percorso di base o nella directory principale dell&#39;installazione di Commerce.

   ![Nuova mappa del sito](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save & Generate]**.

   La visualizzazione della mappa del sito nella griglia potrebbe richiedere alcuni minuti.

## Passaggio 3: Configurare e abilitare robots.txt (facoltativo)

Completa la configurazione di [robot per motori di ricerca](seo-overview.md#search-engine-robots) con istruzioni che indicano ai motori di ricerca di eseguire la ricerca per indicizzazione delle parti del sito che desideri indicizzare.

## Passaggio 4: Inviare la mappa del sito ai motori di ricerca

È possibile inviare la mappa del sito a diversi motori di ricerca fornendo loro il collegamento al file `sitemap.xml` nell&#39;installazione di Commerce. Per copiare il collegamento, effettuare le seguenti operazioni:

1. Nell&#39;elenco _Mappa sito_ fare clic con il pulsante destro del mouse sull&#39;URL nella colonna **[!UICONTROL Link for Google]**.

1. Scegliere **[!UICONTROL Copy Link Address]** dal menu.

Per ulteriori informazioni, consulta le istruzioni per il motore di ricerca specifico. Di seguito sono riportati i collegamenti alle istruzioni per i due principali motori di ricerca:

- [Google][2]
- [Microsoft® Bing][3]

## Passaggio 5: ripristinare le istruzioni robot precedenti (facoltativo)

Ora puoi ripristinare le restrizioni originali (predefinite).

## Gestione di sitemap e robots.txt per più siti Web

Se disponi di più siti web, puoi semplificare il processo di creazione e invio di sitemap. È sufficiente [creare](#site-map-configuration) una o più sitemap che includano URL per tutti gli archivi verificati e salvare le sitemap in un&#39;unica posizione. Tutti i siti devono essere verificati in [Console di Google Search](https://support.google.com/webmasters/answer/7451001).

Per creare sitemap per un&#39;istanza multistore, effettuare le seguenti operazioni:

1. Creare una cartella denominata `sitemaps` nella directory principale del sito Web, quindi creare sottocartelle per ciascun dominio:

       /sitemaps/domain_1/
       /sitemaps/domain_2/
   
1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**.

1. Crea o modifica gli elenchi di sitemap per ogni store e imposta **[!UICONTROL Path]** su quello creato per lo store:

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. Se necessario, aggiorna il file robots.txt.

   Per fare in modo che i spider del motore di ricerca siano correttamente indirizzati alle nuove sitemap, puoi aggiornare o creare il file robots.txt. Aggiungi le seguenti righe in alto.

       Mappa sito Web
       Mappa del sito: https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       Mappa del sito: https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>Se il sito utilizza il motore del server Web [Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html?lang=it), è necessario aggiornare il file [`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html) nella directory principale del sito Web per indirizzare eventuali altre richieste di sitemap nella posizione corretta.

## Descrizioni delle colonne

| Colonna | Descrizione |
|------|-----------|
| [!UICONTROL ID] | Numero di record sequenziale della mappa del sito corrente. |
| [!UICONTROL Filename] | Nome file della mappa del sito. |
| [!UICONTROL Path] | Posizione in cui risiede la mappa del sito sul server. Ad esempio: <br/>`/sitemap/` - Inserisce il file di mappa del sito in una directory denominata _sitemap_, un livello sotto la radice dell&#39;installazione di Commerce. <br/>`/` - Inserisce il file di mappa del sito nel percorso di base o nella directory principale dell&#39;installazione di Commerce. |
| [!UICONTROL Link for Google] | URL della mappa del sito da inviare a Google e ad altri motori di ricerca. |
| [!UICONTROL Last Generated] | Indica la data e l&#39;ora dell&#39;ultima generazione della mappa del sito. |
| [!UICONTROL Store View] | Visualizzazione del punto vendita in cui si applica la mappa del sito. |
| [!UICONTROL Generate] | Rigenera la mappa del sito. |

{style="table-layout:auto"}

## Configurazione mappa del sito

La mappa del sito deve essere aggiornata con la stessa frequenza con cui cambia il contenuto sul sito, che può essere su base giornaliera, settimanale o mensile. La configurazione ti consente di impostare la frequenza e la priorità per ciascun tipo di contenuto.

### Passaggio 1: Impostare la frequenza e la priorità degli aggiornamenti dei contenuti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL XML Sitemap]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Categories Options]** ed effettuare le seguenti operazioni:

   >[!NOTE]
   >
   >Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare queste impostazioni.

   - Imposta **[!UICONTROL Frequency]** su uno dei seguenti:

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - Per **[!UICONTROL Priority]**, immettere un valore compreso tra `0.0` e `1.0`. Zero ha la priorità più bassa.

   ![Mappa del sito XML - Opzioni delle categorie](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedere [Opzioni categorie](../configuration-reference/catalog/xml-sitemap.md#categories-options) nel _Riferimento configurazione_.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Products Options]** e completare le impostazioni **[!UICONTROL Frequency]** e **[!UICONTROL Priority]** in base alle esigenze.

   Per un elenco dettagliato di queste opzioni, vedere [Opzioni prodotti](../configuration-reference/catalog/xml-sitemap.md#products-options) nel _Riferimento configurazione_.

1. Per determinare l&#39;estensione dell&#39;inclusione delle immagini nella mappa del sito, impostare **[!UICONTROL Add Images into Sitemap]** su una delle opzioni seguenti:

   - `None`
   - `Base Only`
   - `All`

   ![Configurazione del catalogo - Prodotti sitemap XML](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL CMS Pages Options]** e completare le impostazioni **[!UICONTROL Frequency]** e **[!UICONTROL Priority]** in base alle esigenze.

   ![Configurazione del catalogo - Pagine CMS sitemap XML](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedere [Opzioni pagine CMS](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options) nella _Guida di riferimento alla configurazione_.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Store Url Options]** e completare le impostazioni **[!UICONTROL Frequency]** e **[!UICONTROL Priority]** in base alle esigenze.

   ![Configurazione del catalogo - URL archivio mappa del sito XML](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedere [Opzioni URL store](../configuration-reference/catalog/xml-sitemap.md#store-url-options) nel _Riferimento configurazione_.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

### Passaggio 2: Completare le impostazioni di generazione

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Generation Settings]**.

   Se necessario, deselezionare la casella di controllo **Usa valore di sistema** per modificare le impostazioni.

   ![Configurazione del catalogo - Impostazioni di generazione sitemap XML](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedere [Impostazioni di generazione](../configuration-reference/catalog/xml-sitemap.md#generation-settings) nel _Riferimento configurazione_.

1. Per generare una mappa del sito, impostare **[!UICONTROL Enabled]** su `Yes` ed effettuare le seguenti operazioni:

   - Impostare **[!UICONTROL Start Time]** sull&#39;ora, il minuto e il secondo per l&#39;aggiornamento della mappa del sito.

   - Imposta **[!UICONTROL Frequency]** su uno dei seguenti:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - Per **[!UICONTROL Error Email Recipient]**, immetti l&#39;indirizzo e-mail della persona che deve ricevere la notifica se si verifica un errore durante un aggiornamento della sitemap.

   - Impostare **[!UICONTROL Error Email Sender]** sul contatto dell&#39;archivio che viene visualizzato come mittente della notifica di errore.

   - Impostare **[!UICONTROL Error Email Template]** sul modello utilizzato per la notifica di errore.

### Passaggio 3: Impostare i limiti per i file di mappa del sito

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Sitemap File Limits]**.

   ![Configurazione del catalogo - Limiti del file sitemap XML](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedere [Limiti file Sitemap](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits) nel _Riferimento configurazione_.

1. Per **[!UICONTROL Maximum No of URLs per File]**, immetti il numero massimo di URL che possono essere inclusi nella sitemap.

   Per impostazione predefinita, il limite è 50.000.

1. Per **[!UICONTROL Maximum File Size]**, immettere la dimensione maggiore in byte allocata per la mappa del sito.

   La dimensione predefinita è 10.485.760 byte.

### Passaggio 4: Impostare le impostazioni di invio del motore di ricerca

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Submission Settings]**.

   ![Configurazione del catalogo - Impostazioni di invio del motore di ricerca sitemap XML](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. Se si utilizza un file `robots.txt` per fornire istruzioni ai motori di ricerca che eseguono la ricerca per indicizzazione del sito, impostare **[!UICONTROL Enable Submission to Robots.txt]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html?lang=it
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed
