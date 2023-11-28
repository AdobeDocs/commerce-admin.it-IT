---
title: Reindirizzamenti automatici
description: Scopri come configurare i reindirizzamenti automatici da generare ogni volta che la chiave URL di un prodotto o di una categoria cambia nell’archivio Commerce.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Reindirizzamenti automatici

Il tuo archivio può essere configurato in modo da generare automaticamente un reindirizzamento permanente ogni volta che la chiave URL di un prodotto o di una categoria cambia. Nella sezione Ottimizzazione motore di ricerca, la casella di controllo sotto la chiave URL indica se i reindirizzamenti permanenti sono abilitati. Se lo store è già configurato per reindirizzare automaticamente gli URL del catalogo, un reindirizzamento è un semplice aggiornamento della chiave URL. Il processo per creare un reindirizzamento automatico è lo stesso sia per i prodotti che per le categorie.

>[!NOTE]
>
>Quando i reindirizzamenti automatici sono attivati e si salva una categoria, tutte le riscritture di prodotti e categorie vengono generate in tempo reale e memorizzate nelle tabelle del database per impostazione predefinita. Questo poteva causare problemi di prestazioni significativi per le categorie con molti prodotti assegnati. La soluzione consiste nel modificare questa impostazione predefinita e saltare la generazione di riscritture URL categoria/prodotti per i prodotti al salvataggio categoria. In questo caso, le riscritture del prodotto vengono generate solo per l’URL canonico del prodotto.

## Impostare i reindirizzamenti automatici

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello sinistro, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimization]** sezione.

   ![Configurazione del catalogo - Ottimizzazione del motore di ricerca](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Reindirizzare automaticamente gli URL dei prodotti

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Individuare il prodotto nell&#39;elenco e fare clic per aprire il record.

1. Espandi ![Selettore di espansione ](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimization]** sezione.

   ![Ottimizzazione del motore di ricerca del prodotto - reindirizzamento permanente](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL URL Key]**, eseguire le operazioni seguenti:

   - Assicurati che il **[!UICONTROL Create Permanent Redirect for old URL]** è selezionata. In caso contrario, seguire le istruzioni per [abilita reindirizzamenti automatici](url-rewrite.md#configure-url-rewrites).

   - Aggiornare il **[!UICONTROL URL Key]** se necessario, utilizza tutti i caratteri minuscoli e i trattini non finali tra questi caratteri invece degli spazi.

1. Al termine, fai clic su **[!UICONTROL Save]**.

1. Quando viene richiesto di aggiornare la cache, segui i collegamenti presenti nel messaggio nella parte superiore dell’area di lavoro.

   Il reindirizzamento permanente è ora attivo per il prodotto ed eventuali URL di categoria associati.

## Reindirizza automaticamente gli URL delle categorie

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Individuare la categoria nella struttura e fare clic per aprire il record.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimization]** sezione.

1. Per **[!UICONTROL URL Key]**, eseguire le operazioni seguenti:

   - Assicurati che il **[!UICONTROL Create Permanent Redirect for old URL]** è selezionata. In caso contrario, seguire le istruzioni per [abilita reindirizzamenti automatici](url-rewrite.md#configure-url-rewrites).

   - Aggiornare il **[!UICONTROL URL Key]** se necessario, utilizza tutti i caratteri minuscoli e i trattini non finali tra questi caratteri invece degli spazi.

1. Al termine, fai clic su **[!UICONTROL Save]**.

1. Quando viene richiesto di aggiornare la cache, segui i collegamenti presenti nel messaggio nella parte superiore dell’area di lavoro.

   Il reindirizzamento permanente è ora attivo per la categoria e per tutti gli URL di prodotto associati.

## Salta la generazione di riscritture dell’URL del prodotto per il salvataggio della categoria {#skip-rewrite}

>[!WARNING]
>
>La disattivazione della generazione automatica delle riscritture URL di categorie/prodotti comporta la rimozione definitiva di tutte le riscritture URL di categorie/tipi di prodotto esistenti, che non possono essere ripristinate. Questo potrebbe causare conflitti di URL di tipo categoria/prodotto non risolti che richiedono un aggiornamento manuale della chiave URL per la risoluzione.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello sinistro, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimization]** sezione.

1. Imposta **[!UICONTROL Generate "category/product" URL Rewrites]** a `No`.

1. Nella finestra di dialogo di conferma, fai clic su **[!UICONTROL OK]** per confermare la modifica e la rimozione delle riscritture URL esistenti.

   ![Disattiva riscritture URL categoria/prodotto - conferma](./assets/seo-rewrite-off.png){width="350"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
