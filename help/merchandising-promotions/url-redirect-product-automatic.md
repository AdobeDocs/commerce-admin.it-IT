---
title: Reindirizzamenti automatici
description: Scopri come configurare i reindirizzamenti automatici da generare ogni volta che la chiave URL di un prodotto o di una categoria cambia nel tuo store di Commerce.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/Vscg-TDdLnzKjdi-SMwrcpR-QDPvlHpPzgmcLe63-4Q
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 571
ht-degree: 0%

---

# Reindirizzamenti automatici

Il tuo archivio può essere configurato in modo da generare automaticamente un reindirizzamento permanente ogni volta che la chiave URL di un prodotto o di una categoria cambia. Nella sezione Ottimizzazione motore di ricerca, la casella di controllo sotto la chiave URL indica se i reindirizzamenti permanenti sono abilitati. Se lo store è già configurato per reindirizzare automaticamente gli URL del catalogo, un reindirizzamento è un semplice aggiornamento della chiave URL. Il processo per creare un reindirizzamento automatico è lo stesso sia per i prodotti che per le categorie.

>[!NOTE]
>
>Quando i reindirizzamenti automatici sono attivati e si salva una categoria, tutte le riscritture di prodotti e categorie vengono generate in tempo reale e memorizzate nelle tabelle del database per impostazione predefinita. Questo poteva causare problemi di prestazioni significativi per le categorie con molti prodotti assegnati. La soluzione consiste nel modificare questa impostazione predefinita e saltare la generazione di riscritture URL categoria/prodotti per i prodotti al salvataggio categoria. In questo caso, le riscritture del prodotto vengono generate solo per l’URL canonico del prodotto.

## Impostare i reindirizzamenti automatici

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]**.

   ![Configurazione del catalogo - ottimizzazione motore di ricerca](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.


>[!NOTE]
>
> Le riscritture URL possono essere generate per la vista store o l’ambito del sito web. Impostare l&#39;ambito di riscrittura URL dall&#39;amministratore in **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;**[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**. Selezionare l&#39;ambito nel campo&#x200B;_[!UICONTROL Product URL Rewrite Scope]_.

## Reindirizzare automaticamente gli URL dei prodotti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Individuare il prodotto nell&#39;elenco e fare clic per aprire il record.

1. Espandere ![Il selettore di espansione &#x200B;](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]**.

   ![Ottimizzazione motore di ricerca prodotti - reindirizzamento permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL URL Key]**, eseguire le operazioni seguenti:

   - Verificare che la casella di controllo **[!UICONTROL Create Permanent Redirect for old URL]** sia selezionata. In caso contrario, seguire le istruzioni per [abilitare i reindirizzamenti automatici](url-rewrite.md#configure-url-rewrites).

   - Aggiornare **[!UICONTROL URL Key]** in base alle esigenze, utilizzando tutti i caratteri minuscoli e i trattini non finali tra questi caratteri invece degli spazi.

1. Al termine, fare clic su **[!UICONTROL Save]**.

1. Quando viene richiesto di aggiornare la cache, segui i collegamenti presenti nel messaggio nella parte superiore dell’area di lavoro.

   Il reindirizzamento permanente è ora attivo per il prodotto ed eventuali URL di categoria associati.

## Reindirizza automaticamente gli URL delle categorie

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Individuare la categoria nella struttura e fare clic per aprire il record.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]**.

1. Per **[!UICONTROL URL Key]**, eseguire le operazioni seguenti:

   - Verificare che la casella di controllo **[!UICONTROL Create Permanent Redirect for old URL]** sia selezionata. In caso contrario, seguire le istruzioni per [abilitare i reindirizzamenti automatici](url-rewrite.md#configure-url-rewrites).

   - Aggiornare **[!UICONTROL URL Key]** in base alle esigenze, utilizzando tutti i caratteri minuscoli e i trattini non finali tra questi caratteri invece degli spazi.

1. Al termine, fare clic su **[!UICONTROL Save]**.

1. Quando viene richiesto di aggiornare la cache, segui i collegamenti presenti nel messaggio nella parte superiore dell’area di lavoro.

   Il reindirizzamento permanente è ora attivo per la categoria e per tutti gli URL di prodotto associati.

## Salta la generazione di riscritture dell’URL del prodotto per il salvataggio della categoria {#skip-rewrite}

>[!WARNING]
>
>La disattivazione della generazione automatica delle riscritture URL di categorie/prodotti comporta la rimozione definitiva di tutte le riscritture URL di categorie/tipi di prodotto esistenti, che non possono essere ripristinate. Questo potrebbe causare conflitti di URL di tipo categoria/prodotto non risolti che richiedono un aggiornamento manuale della chiave URL per la risoluzione.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]**.

1. Imposta **[!UICONTROL Generate "category/product" URL Rewrites]** su `No`.

1. Nella finestra di dialogo di conferma, fare clic su **[!UICONTROL OK]** per confermare la modifica e la rimozione delle riscritture URL esistenti.

   ![Disattiva le riscritture URL categoria/prodotto - conferma](./assets/seo-rewrite-off.png){width="350"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
