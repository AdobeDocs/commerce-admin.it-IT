---
title: Ottimizzazione dei motori di ricerca
description: Scopri gli strumenti di ottimizzazione dei motori di ricerca (SEO) per i siti Commerce e le best practice per una SEO ottimale.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Panoramica SEO

_Ottimizzazione dei motori di ricerca_ (SEO) è la pratica di perfezionare il contenuto e la presentazione di un sito per migliorare il modo in cui le pagine vengono indicizzate dai motori di ricerca. Commerce include varie funzioni per supportare l’attività SEO (Search Engine Optimization) in corso.

## Metadati

Ulteriori informazioni sull&#39;aggiunta e l&#39;ottimizzazione di parole chiave [metadati](meta-data.md) per il tuo sito e store.

## Utilizzo di una mappa del sito

A [mappa del sito](sitemap-xml.md) migliora il modo in cui lo store viene indicizzato dai motori di ricerca ed è progettato per trovare pagine che potrebbero essere ignorate dai crawler web. È possibile configurare una mappa del sito per indicizzare tutte le pagine e le immagini.

## Riscritture URL

Il [Riscrittura URL](url-rewrite.md) Questo strumento consente di modificare qualsiasi URL associato a un prodotto, una categoria o una pagina CMS.

## Robot per motori di ricerca

La configurazione di Commerce include impostazioni per generare e gestire istruzioni per i crawler web e i bot che indicizzano il sito. Se la richiesta di `robots.txt` raggiunge Commerce (anziché un file fisico), viene indirizzato dinamicamente al controller dei robot. Le istruzioni sono direttive riconosciute e seguite dalla maggior parte dei motori di ricerca.

Per impostazione predefinita, il file robots.txt generato da Commerce contiene istruzioni per il web crawler per evitare l’indicizzazione di determinate parti del sito che contengono file utilizzati internamente dal sistema. Puoi utilizzare le impostazioni predefinite, definire istruzioni personalizzate per tutti o per motori di ricerca specifici. Ci sono molti articoli online che esplorano l&#39;argomento in dettaglio.

### Esempio di istruzioni personalizzate

**Consente l&#39;accesso completo**

    User-agent:*
    Non consentire:

**Non consente l&#39;accesso a tutte le cartelle**

    User-agent:*
    Non consentire: /

**Istruzioni predefinite**

    User-agent: *
    Non consentire: /index.php/
    Non consentire: /*?
    Non consentire: /checkout/
    Non consentire: /app/
    Non consentire: /lib/
    Non consentire: /*.php$
    Non consentire: /pkginfo/
    Non consentire: /report/
    Non consentire: /var/
    Non consentire: /catalog/
    Non consentire: /customer/
    Non consentire: /sendfriend/
    Non consentire: /review/
    Non consentire: /*SID=

### Configura `robots.txt`

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Trova il **[!UICONTROL Global]** nella prima riga della griglia e fare clic su **[!UICONTROL Edit]**.

   ![Configurazione progettazione globale](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Robots]** ed effettuare le seguenti operazioni:

   ![Configurazione del progetto - robot per motori di ricerca](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Default Robots]** a uno dei seguenti elementi:

     | Opzione | Descrizione |
     |------|------------|
     | `INDEX, FOLLOW` | Indica ai Web crawler di indicizzare il sito e di verificare in seguito la presenza di modifiche. |
     | `NOINDEX, FOLLOW` | Indica ai crawler Web di evitare l&#39;indicizzazione del sito, ma di verificare in seguito la presenza di modifiche. |
     | `INDEX, NOFOLLOW` | Indica ai Web crawler di indicizzare il sito una sola volta, ma di non verificare in seguito la presenza di modifiche. |
     | `NOINDEX, NOFOLLOW` | Indica ai Web crawler di evitare l&#39;indicizzazione del sito e di non verificare in seguito la presenza di modifiche. |

     {style="table-layout:auto"}

   - Se necessario, immetti istruzioni personalizzate nel **[!UICONTROL Edit Custom instruction of robots.txt file]** casella. Ad esempio, mentre un sito è in fase di sviluppo, è possibile che si desideri non consentire l&#39;accesso a tutte le cartelle.

   - Per ripristinare le istruzioni predefinite, fai clic su **[!UICONTROL Reset to Default]**.

1. Al termine, fai clic su **[!UICONTROL Save Configuration]**.
