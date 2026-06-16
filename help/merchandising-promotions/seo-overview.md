---
title: Ottimizzazione dei motori di ricerca
description: Scopri gli strumenti di ottimizzazione dei motori di ricerca (SEO) per i siti Commerce e le best practice per una SEO ottimale.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
TQID: https://experienceleague.adobe.com/cEXR2743G7ZzRSKqb9r344Osipo-R-GlqxNZwC-u-Nk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 551
ht-degree: 0%

---

# Panoramica SEO

_L&#39;ottimizzazione per i motori di ricerca_ (SEO) consiste nel perfezionare il contenuto e la presentazione di un sito per migliorare il modo in cui le pagine vengono indicizzate dai motori di ricerca. Commerce include varie funzioni per supportare l’attività SEO (Search Engine Optimization) in corso.

>[!TIP]
>
>Per Adobe Commerce as a Cloud Service, consulta le [linee guida SEO](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=it) nella documentazione di Commerce Storefront

## Metadati

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

Ulteriori informazioni sull&#39;aggiunta e l&#39;ottimizzazione di [metadati](meta-data.md) ricchi di parole chiave per il sito e l&#39;archivio.

## Utilizzo di una mappa del sito

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

Una [mappa del sito](sitemap-xml.md) migliora l&#39;indicizzazione dello store da parte dei motori di ricerca ed è progettata per trovare pagine che potrebbero essere ignorate dai crawler Web. È possibile configurare una mappa del sito per indicizzare tutte le pagine e le immagini.

## Riscritture URL

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

Lo strumento [URL Riscrittura](url-rewrite.md) consente di modificare qualsiasi URL associato a una pagina di prodotto, categoria o CMS.

## Robot per motori di ricerca

La configurazione di Commerce include impostazioni per generare e gestire istruzioni per crawler web e bot che indicizzano il sito. Se la richiesta per `robots.txt` raggiunge Commerce (anziché un file fisico), viene instradata dinamicamente al controller robots. Le istruzioni sono direttive riconosciute e seguite dalla maggior parte dei motori di ricerca.

Per impostazione predefinita, il file robots.txt generato da Commerce contiene istruzioni per il crawler Web per evitare l&#39;indicizzazione di determinate parti del sito che contengono file utilizzati internamente. Puoi utilizzare le impostazioni predefinite, definire istruzioni personalizzate per tutti o per motori di ricerca specifici. Ci sono molti articoli online che esplorano l&#39;argomento in dettaglio.

### Esempio di istruzioni personalizzate

**Consente L&#39;Accesso Completo**

    Agente utente:*
    Non consentire:

**Accesso negato a tutte le cartelle**

    Agente utente:*
    Non consentire: /

**Istruzioni predefinite**

    Agente utente: *
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

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Trovare la configurazione **[!UICONTROL Global]** nella prima riga della griglia e fare clic su **[!UICONTROL Edit]**.

   ![Configurazione progettazione globale](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Robots]** ed effettua le seguenti operazioni:

   ![Configurazione progettazione - robot motore di ricerca](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Default Robots]** su uno dei seguenti:

     | Opzione | Descrizione |
     |------|------------|
     | `INDEX, FOLLOW` | Indica ai crawler Web di indicizzare il sito e di verificare in un secondo momento se sono presenti modifiche. |
     | `NOINDEX, FOLLOW` | Indica ai crawler Web di evitare l&#39;indicizzazione del sito, ma di verificare in seguito se sono presenti modifiche. |
     | `INDEX, NOFOLLOW` | Indica ai crawler Web di indicizzare il sito una sola volta, ma di non seguire alcun collegamento nella pagina. |
     | `NOINDEX, NOFOLLOW` | Indica ai crawler Web di evitare l&#39;indicizzazione del sito e di non seguire alcun collegamento nella pagina. |

     {style="table-layout:auto"}

   - Se necessario, immettere istruzioni personalizzate nella casella **[!UICONTROL Edit Custom instruction of robots.txt file]**. Ad esempio, mentre un sito è in fase di sviluppo, è possibile che si desideri non consentire l&#39;accesso a tutte le cartelle.

   - Per ripristinare le istruzioni predefinite, scegliere **[!UICONTROL Reset to Default]**.

1. Al termine, fare clic su **[!UICONTROL Save Configuration]**.
