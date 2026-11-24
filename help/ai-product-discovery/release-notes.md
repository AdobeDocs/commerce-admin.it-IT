---
title: Note sulla versione di AI Product Discovery
description: Consulta le note sulla versione di AI Product Discovery per le funzioni di arricchimento di cataloghi e PDP, le correzioni, le indicazioni per l’aggiornamento, le versioni di Commerce supportate e i problemi noti.
feature: Release Notes
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%
---
# Note sulla versione di AI Product Discovery

Queste note sulla versione descrivono gli aggiornamenti all’arricchimento del catalogo e all’arricchimento della PDP, inclusi nuove funzioni, correzioni, requisiti di aggiornamento e problemi noti. Ogni voce di versione identifica l’estensione o il flusso di lavoro interessato.

![Nuove](../assets/new.svg) nuove funzionalità
![Problema risolto](../assets/fix.svg) correzioni e miglioramenti
![Problema noto](../assets/bug.svg) Problemi noti

## Versione 2.1.3 {#release-2-1-3}

*30 novembre 2026*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 e 2.4.7 su PHP da 8.3 a 8.5. [!DNL Adobe Commerce as a Cloud Service]

La versione 2.1.3 combina l&#39;arricchimento della pagina dei dettagli del prodotto con l&#39;arricchimento del catalogo in una nuova voce del menu Admin denominata **AI Product Discovery**. Inoltre, il supporto si estende a [!DNL Adobe Commerce as a Cloud Service].

## Versione 2.1.2 {#release-2-1-2}

*22 ottobre 2026*

[!BADGE Supportato]{type=Informative tooltip="Supportato"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 e 2.4.7 su PHP da 8.3 a 8.5.

La versione 2.1.2 rende l’arricchimento dei cataloghi un’estensione autonoma. Ora include tutto ciò che era stato fornito in precedenza dall&#39;estensione [!DNL Adobe Brand Visibility] separata (`magento/llm-optimizer`): l&#39;applicazione dei suggerimenti approvati al catalogo, il loro rollback e la protezione delle proprie modifiche dalla sovrascrittura.

### Aggiornamento da versioni precedenti {#upgrade-from-earlier-versions}

>[!IMPORTANT]
>
>Impossibile installare la versione 2.1.2 insieme all&#39;estensione [!DNL Adobe Brand Visibility]. Se è installato, rimuoverlo come parte dell’aggiornamento.

1. Rimuovere l&#39;estensione [!DNL Adobe Brand Visibility], se installata:

   ```bash
   composer remove magento/llm-optimizer
   ```

   Se l&#39;estensione è stata installata tramite copia o collegamento simbolico di `Magento/LlmoCatalog` in `app/code`, eliminare la directory. Non disabilitare solo il modulo: un modulo disabilitato che è ancora su disco può causare l&#39;eliminazione di `setup:upgrade` dalla tabella in cui sono memorizzati i valori originali dei prodotti arricchiti.

1. Aggiorna l’arricchimento del catalogo e applica le modifiche:

   ```bash
   composer require magento/module-catalog-enrichment:^2.1
   bin/magento setup:upgrade
   bin/magento cache:flush
   ```

   Svuota la cache dopo l’aggiornamento. L’aggiornamento sposta le concessioni di accesso esistenti in nuove risorse di autorizzazione, che diventano effettive solo dopo che la cache sarà stata cancellata.

### Requisiti

![Nuovo](../assets/new.svg) **PHP 8.3 e [!DNL Adobe Commerce] 2.4.7 o versione successiva**: PHP 8.1 è terminato e PHP 8.2 ha raggiunto la fine del ciclo di vita il 31 dicembre 2026, quindi nessuno dei due è supportato. [!DNL Adobe Commerce] 2.4.6 e versioni precedenti non sono supportati.

### Nuove funzioni

![Nuovo](../assets/new.svg) **[!UICONTROL AI Product Discovery]menu**: le pagine di arricchimento del catalogo dispongono ora di una sezione specifica nella barra laterale di amministrazione. Vai a **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**. In precedenza, la pagina si trovava in **[!UICONTROL Catalog]**.

![Nuovo](../assets/new.svg) [!BADGE Beta]{type=Informative tooltip="Non ancora generalmente disponibile"} **[!UICONTROL Product Details Page Enrichment (Beta)]**—Una nuova pagina in **[!UICONTROL AI Product Discovery]** per rivedere i suggerimenti di arricchimento per le pagine dei dettagli del prodotto. L’arricchimento della pagina con i dettagli del prodotto è in versione beta e non è ancora disponibile a livello generale.

![Nuovo](../assets/new.svg) **Applica e ripristina i suggerimenti approvati**—Gli aggiornamenti di nome e descrizione approvati vengono scritti nel catalogo da questa estensione. Commerce registra il valore originale di ogni attributo arricchito la prima volta che viene modificato, pertanto un rollback ripristina sempre il valore esistente prima dell’arricchimento, anche dopo l’applicazione di diversi suggerimenti allo stesso attributo.

![Nuovo](../assets/new.svg) **Le modifiche vengono rispettate**. Quando si modifica un nome o una descrizione arricchiti nel modulo del prodotto Admin, con **[!UICONTROL Update Attributes]**, o tramite un&#39;importazione, il valore viene mantenuto e il suggerimento correlato viene contrassegnato come *Obsoleto*. Una modifica apportata all&#39;ambito predefinito influisce solo sulle viste archivio che ereditano il valore.

![Nuovo](../assets/new.svg) **Accesso al catalogo in sola lettura per i suggerimenti**—[!DNL Commerce Catalog Agent] consente di leggere i dati relativi a prodotti, categorie, set di attributi e tipi di prodotto per selezionare i prodotti da analizzare. La lettura restituisce solo gli attributi contrassegnati **[!UICONTROL Used in Product Listing]**, oltre agli attributi che possono essere arricchiti. Non può modificare i dati del catalogo.

### Correzioni e miglioramenti

![È stato risolto il problema](../assets/fix.svg) **I report di applicazione sono stati ritentati correttamente**. Se una richiesta di applicazione viene ritentata dopo il suo completamento, il nuovo tentativo ora segnala le modifiche come applicate invece di segnalare nessuna modifica. Nulla è scritto due volte.

![È stato risolto il problema](../assets/fix.svg) **Solo i servizi approvati possono modificare il catalogo**. Applica e ripristina accetta solo le richieste di [!DNL Commerce Catalog Agent]. In precedenza, venivano accettati tutti i token Adobe IMS validi. Lo stesso controllo ora si applica anche alle richieste SOAP.

![È stato risolto il problema](../assets/fix.svg) **Errori più chiari**. Un&#39;interruzione Adobe IMS ora restituisce `401` invece di `500`, pertanto la richiesta non viene ritentata rispetto al catalogo e un ambiente Adobe IMS non riconosciuto viene rifiutato invece di essere trattato come gestione temporanea.

![È stato risolto il problema](../assets/fix.svg) **Ambiente Adobe IMS**. L&#39;arricchimento del catalogo ora accede all&#39;ambiente Adobe IMS di produzione per impostazione predefinita, anche nelle istanze connesse a uno spazio dati [!DNL Commerce Services] non di produzione. In precedenza, tali istanze venivano inviate all’ambiente di staging.

![È stato risolto il problema](../assets/fix.svg) **Accesso dopo la modifica del dominio [!DNL Adobe Brand Visibility]**. La pagina di arricchimento del catalogo ora viene caricata da `abv.adobe.com`, che corregge un loop di accesso dopo che il dominio precedente ha iniziato il reindirizzamento.

### Problemi noti

![Problema noto](../assets/bug.svg) **Ruoli con accesso completo a [!UICONTROL Catalog]**—Un ruolo utente salvato prima di questa versione con tutti i **[!UICONTROL Catalog]** concessi mantiene l&#39;accesso alla risorsa **[!UICONTROL Catalog Enrichment Service API]**. Rivedi tali ruoli in **[!UICONTROL System]** > **[!UICONTROL Permissions]** > **[!UICONTROL User Roles]** e cancella la risorsa dove non è necessaria.

## Versione 1.0.2 {#release-1-0-2}

Versione iniziale della pagina di amministrazione dell’arricchimento del catalogo. Richiede l&#39;estensione [!DNL Adobe Brand Visibility] per applicare suggerimenti al catalogo.
