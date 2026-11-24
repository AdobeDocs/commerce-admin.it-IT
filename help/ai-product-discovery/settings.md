---
title: Impostazioni di arricchimento
description: Configura la consegna, i processi di traffico agente mensili e gli agenti di IA idonei condivisi da Arricchimento catalogo e Arricchimento PDP nell’individuazione di prodotti AI.
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%
---
# Impostazioni di arricchimento

Utilizza la scheda **[!UICONTROL Settings]** nell&#39;area di lavoro di individuazione prodotti AI per configurare l&#39;istanza di Adobe Commerce. Una volta configurati, gli arricchimenti a catalogo e PDP vengono visualizzati nell’area di lavoro di individuazione prodotti di intelligenza artificiale.

I campi di questa scheda identificano l&#39;ambiente [!DNL Adobe Commerce] e la visualizzazione archivio a cui si connette l&#39;individuazione prodotti AI. Per i requisiti di accesso e organizzazione IMS, consulta i [prerequisiti per l&#39;individuazione dei prodotti AI](prerequisites.md).

1. In Amministrazione, passa a **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]** o **[!UICONTROL Product Details Page Enrichment]**.
1. Nell&#39;elenco **[!UICONTROL Scope]** nella parte superiore della pagina, selezionare la visualizzazione dello store che si desidera configurare oppure lasciare **[!UICONTROL All Store Views]** per gestire le impostazioni tra le visualizzazioni dello store.
1. Apri la scheda **[!UICONTROL Settings]**.
1. In **[!UICONTROL Commerce Configuration]**, espandere il pannello di visualizzazione archivio con l&#39;etichetta con il relativo URL.

   Fornisci i dettagli dell&#39;ambiente [!DNL Adobe Commerce] per abilitare il servizio di individuazione prodotti AI e i flussi di lavoro di controllo.

   ![Configurazione Commerce nella scheda Impostazioni di arricchimento del catalogo](./assets/catalog-enrichment-commerce-config.png){zoomable="yes"}

1. Immettere i dettagli di connessione richiesti per la visualizzazione archivio.

   - **[!UICONTROL Store View URL]**: URL corrispondente alla visualizzazione archivio, ad esempio `https://brand.example.com/fr/`.
   - **[!UICONTROL Environment ID]**: identificatore univoco per l&#39;ambiente [!DNL Adobe Commerce] a cui la connessione accede.
   - **[!UICONTROL Website Code]**, **[!UICONTROL Store Code]** e **[!UICONTROL Store View Code]**: codici di visualizzazione sito Web, archivio e archivio per il sito Web Commerce. Questi valori devono corrispondere ai codici presenti nell’amministratore Commerce.
   - **[!UICONTROL Host Name]**: nome host dell&#39;istanza [!DNL Adobe Commerce].
   - **(Facoltativo - solo per l&#39;arricchimento del catalogo)** In **[!UICONTROL Catalog field limits]**, selezionare **[!UICONTROL Limit maximum characters for product name]** e specificare il limite di caratteri per i nomi di prodotto generati. Selezionare **[!UICONTROL Limit maximum characters for product description]** e specificare il limite di caratteri per le descrizioni dei prodotti generate.

1. Fare clic su **[!UICONTROL Save]**.

Dopo il salvataggio, attendere il completamento di qualsiasi processo di sincronizzazione o convalida iniziale prima di basarsi sui risultati del catalogo o del controllo di audit per la visualizzazione archivio. La visualizzazione dei suggerimenti di prodotto nella pagina **[!UICONTROL Catalog Enrichment]** potrebbe richiedere fino a 24 ore.

Per rimuovere una configurazione della visualizzazione archivio, espandere tale voce e fare clic su **[!UICONTROL Delete]**.

## Descrizioni dei campi {#commerce-connection-fields}

I campi obbligatori sono contrassegnati con un asterisco (*) nel modulo **[!UICONTROL Commerce Configuration]**.

| Campo | Obbligatorio | Descrizione |
| --- | --- | --- |
| URL visualizzazione store | Sì | URL corrispondente alla visualizzazione archivio (ad esempio, `https://brand.example.com/fr/`). |
| ID ambiente | Sì | Identificatore univoco dell&#39;ambiente [!DNL Adobe Commerce] a cui la connessione accede. |
| Codice sito Web | Sì | Codice del sito web Commerce. |
| Codice store | Sì | Codice store del sito Web Commerce. |
| Codice visualizzazione store | Sì | Archivia la visualizzazione del sito Web Commerce. |
| Nome host | Sì | Nome host dell&#39;istanza [!DNL Adobe Commerce]. |
| Limiti dei campi del catalogo (solo arricchimento del catalogo) | No | Definisci i limiti dei caratteri per i nomi e le descrizioni dei prodotti generati. |
