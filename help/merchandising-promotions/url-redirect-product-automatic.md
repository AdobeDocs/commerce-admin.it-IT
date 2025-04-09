---
title: Reindirizzamenti automatici
description: Scopri come configurare i reindirizzamenti automatici da generare ogni volta che la chiave URL di un prodotto o di una categoria cambia nel tuo store Commerce.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: d088d5833b9c61e7b1c90a0839fdf38527929ce5
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Reindirizzamenti automatici

Il store può essere configurato per generare automaticamente un reindirizzare permanente ogni volta che cambia la chiave URL di un prodotto o di una categoria. Nella sezione Ottimizzazione motore Search, la casella di controllo sotto il tasto URL indica se i reindirizzamenti permanenti sono abilitati. Se lo store è già configurato per reindirizzare automaticamente gli URL del catalogo, un reindirizzamento è un semplice aggiornamento della chiave URL. Il processo per creare un reindirizzare automatico è lo stesso sia per i prodotti che per le categorie.

>[!NOTE]
>
>Quando i reindirizzamenti automatici sono abilitati e si salva una categoria, tutte le riscritture di prodotti e categorie vengono generate in tempo reale e memorizzate in tabelle di database per impostazione predefinita. Ciò potrebbe causare problemi di prestazioni significativi per le categorie con molti prodotti assegnati. La soluzione è cambiare questa impostazione predefinita e saltare la generazione di categoria/prodotti URL riscritture per i prodotti salvati per categoria. In questo caso, le riscritture dei prodotti vengono generate solo per il prodotto canonico URL.

## Impostare i reindirizzamenti automatici

1. _Nella barra laterale Amministratore_, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]**.

   ![Configurazione del catalogo - ottimizzazione motore di ricerca](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.


>[!NOTE]
>
> Le riscritture URL possono essere generate per la vista store o l’ambito del sito web. Impostare l&#39;ambito di riscrittura URL dall&#39;amministratore in **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]****[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**. Selezionare l&#39;ambito nel campo_[!UICONTROL Product URL Rewrite Scope]_.

## Reindirizzare automaticamente gli URL dei prodotti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Individuare il prodotto nell&#39;elenco e fare clic per aprire il record.

1. Espandere ![Il selettore di espansione ](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]**.

   ![Ottimizzazione del motore ricerca del prodotto - reindirizzare permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL URL Key]**, procedi come segue:

   - Verificare che la casella di **[!UICONTROL Create Permanent Redirect for old URL]** controllo sia selezionata. In caso contrario, seguire le istruzioni per [abilitare i reindirizzamenti automatici](url-rewrite.md#configure-url-rewrites).

   - Aggiornare **[!UICONTROL URL Key]** in base alle esigenze, utilizzando tutti i caratteri minuscoli e i trattini non finali tra questi caratteri invece degli spazi.

1. Al termine, fare clic su **[!UICONTROL Save]**.

1. Quando viene richiesto di aggiornare la cache, seguire i collegamenti nel messaggio nella parte superiore dell&#39;area di lavoro.

   La reindirizzare permanente è ora valida per il prodotto e per tutti gli URL di categoria associati.

## reindirizzare automaticamente gli URL delle categorie

1. _Nella barra laterale Amministratore_, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Individuare la categoria nella struttura e fare clic per aprire il record.

1. Espandi ![Espansione selettore](../assets/icon-display-expand.png) sezione **[!UICONTROL Search Engine Optimization]** .

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

1. Espandi ![Espansione selettore](../assets/icon-display-expand.png) sezione **[!UICONTROL Search Engine Optimization]** .

1. Imposta **[!UICONTROL Generate "category/product" URL Rewrites]** su `No`.

1. Nella finestra di dialogo di conferma, fate clic per **[!UICONTROL OK]** confermare la modifica e la rimozione delle riscritture di URL esistenti.

   ![Disattiva le riscritture URL categoria/prodotto - conferma](./assets/seo-rewrite-off.png){width="350"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
