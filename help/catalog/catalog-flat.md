---
title: Cataloghi semplici
description: Scopri come creare un catalogo flat, in cui ogni riga contiene tutti i dati necessari su un prodotto o una categoria.
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
TQID: https://experienceleague.adobe.com/7D7lHMHFVKh2J35S1Mpr5eudyLyicbpL4xqkvu-KatA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
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
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 704
ht-degree: 0%

---

# Cataloghi semplici

>[!IMPORTANT]
>
>L’utilizzo di un catalogo semplice non è più consigliato come best practice. L’utilizzo continuo di questa funzione può causare il deterioramento delle prestazioni e altri problemi di indicizzazione. Una descrizione dettagliata e una soluzione sono disponibili nel [Centro assistenza](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html?lang=it).<br/><br/>Le versioni interessate includono: <br/>- Adobe Commerce sull&#39;infrastruttura cloud, 2.3.x e versioni successive<br/>- Adobe Commerce (On-Premise), 2.3.x e versioni successive<br/>- Magento Open Source, 2.3.x e versioni successive <br/><br/>In qualsiasi versione, alcune estensioni funzionano solo con tabelle flat, creando in tal modo un rischio se si disabilitano le tabelle flat. Se si è certi di disporre di alcune estensioni che utilizzano gli indicizzatori Flat Catalog, è necessario tenere presente questo rischio quando si impostano tali valori su `No`.

In genere, Commerce memorizza i dati del catalogo in più tabelle, in base al modello Entity-Attribute-Value (EAV). Poiché gli attributi del prodotto sono memorizzati in molte tabelle, le query SQL a volte sono lunghe e complesse.

Al contrario, un catalogo semplice crea tabelle al volo, in cui ogni riga contiene tutti i dati necessari su un prodotto o una categoria. Un catalogo flat viene aggiornato automaticamente, ogni minuto o in base al processo cron. L’indicizzazione di cataloghi semplici può anche velocizzare l’elaborazione delle regole dei prezzi di catalogo e carrello. Un catalogo con un massimo di 500.000 SKU può essere indicizzato rapidamente come catalogo semplice.

>[!NOTE]
>
>Prima di abilitare un catalogo flat per un archivio live, assicurati di testare la configurazione in un ambiente di sviluppo.

## Passaggio 1: abilitare il catalogo flat

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere la sezione _Storefront_ ed eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Use Flat Catalog Category]** su `Yes`. Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]**.

   - Imposta **[!UICONTROL Use Flat Catalog Product]** su `Yes`.

   ![Configurazione catalogo semplice](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Quando viene richiesto di aggiornare la cache, fare clic su **[!UICONTROL Cache Management]** nel messaggio di sistema e seguire le istruzioni per aggiornare la cache.

## Passaggio 2: verificare i risultati

Esistono due metodi per verificare i risultati.

### Metodo 1: verificare i risultati per un singolo prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Apri un prodotto in modalità di modifica.

1. Per **[!UICONTROL Name]**, aggiungere il testo `_TEST` alla fine del nome del prodotto.

1. Fare clic su **[!UICONTROL Save]**.

1. In una nuova scheda del browser, passa alla home page del negozio ed effettua le seguenti operazioni:

   - Cerca il prodotto modificato.

   - Utilizza la navigazione per navigare fino al prodotto nella categoria a esso assegnata.

     Se necessario, aggiorna la pagina per visualizzare i risultati. La modifica verrà visualizzata entro il minuto o in base alla pianificazione di [Cron](../systems/cron.md).

   ![Vetrina con catalogo semplice](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### Metodo 2: verificare i risultati per una categoria

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell&#39;angolo superiore sinistro verificare che **[!UICONTROL Store View]** sia impostato su `All Store Views`.

   Se richiesto, fare clic su **[!UICONTROL OK]** per confermare.

1. Nell&#39;albero delle categorie selezionare una categoria esistente, fare clic su **[!UICONTROL Add Subcategory]** ed eseguire le operazioni seguenti:

   - Per **[!UICONTROL Category Name]**, immettere `Test Category`.

   - Al termine, fare clic su **[!UICONTROL Save]**.

     ![Sottocategoria test](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Products in Category]** e fare clic su **[!UICONTROL Reset Filter]** per visualizzare tutti i prodotti.

   - Seleziona la casella di controllo di diversi prodotti da aggiungere alla nuova categoria.

   - fare clic su **[!UICONTROL Save]**.

   ![Verifica prodotti categoria](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. In una nuova scheda del browser passare alla home page del negozio e utilizzare la navigazione del negozio per passare alla categoria creata.

   Se necessario, aggiorna la pagina per visualizzare i risultati. La modifica viene visualizzata entro il minuto o in base alla pianificazione cron.

## Passaggio 3: rimuovere i dati del test

Per rimuovere i dati di test e ripristinare la configurazione originale del catalogo e del nome del prodotto, eseguire le operazioni seguenti.

### Rimuovi la categoria di test

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell&#39;albero delle categorie selezionare la sottocategoria di test creata.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Delete]**.

1. Quando viene richiesto di confermare, fare clic su **[!UICONTROL OK]**.

   La rimozione di questa categoria non rimuove i prodotti assegnati alla categoria.

### Ripristina il nome del prodotto originale

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Apri il prodotto di test in modalità di modifica.

1. Rimuovi il testo `_TEST` aggiunto a **[!UICONTROL Product Name]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save]**.

### Ripristina la configurazione originale del catalogo

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere la sezione _Storefront_ ed eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Use Flat Catalog Category]** su `No`.

   - Imposta **[!UICONTROL Use Flat Catalog Product]** su `No`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, aggiorna la cache.
