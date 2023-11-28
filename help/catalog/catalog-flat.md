---
title: Cataloghi semplici
description: Scopri come creare un catalogo flat, in cui ogni riga contiene tutti i dati necessari su un prodotto o una categoria.
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Cataloghi semplici

>[!IMPORTANT]
>
>L’utilizzo di un catalogo semplice non è più consigliato come best practice. L’utilizzo continuo di questa funzione può causare il deterioramento delle prestazioni e altri problemi di indicizzazione. Una descrizione dettagliata e la soluzione sono disponibili nel [Centro risorse](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html).<br/><br/>Le versioni interessate includono: <br/>- Adobe Commerce sull’infrastruttura cloud, versione 2.3.x e successive<br/>- Adobe Commerce (On-Premise), 2.3.x e versioni successive<br/>- Magento Open Source, 2.3.x e versioni successive <br/><br/>In qualsiasi versione di rilascio, alcune estensioni funzionano solo con le tabelle a comparsa, creando in tal modo un rischio se si disattivano le tabelle a comparsa. Se si è certi di disporre di alcune estensioni che utilizzano gli indicizzatori Flat Catalog, è necessario tenere presente questo rischio quando si impostano tali valori su `No`.

Commerce in genere memorizza i dati del catalogo in più tabelle, in base al modello Entity-Attribute-Value (EAV). Poiché gli attributi del prodotto sono memorizzati in molte tabelle, le query SQL a volte sono lunghe e complesse.

Al contrario, un catalogo semplice crea tabelle al volo, in cui ogni riga contiene tutti i dati necessari su un prodotto o una categoria. Un catalogo flat viene aggiornato automaticamente, ogni minuto o in base al processo cron. L’indicizzazione di cataloghi semplici può anche velocizzare l’elaborazione delle regole dei prezzi di catalogo e carrello. Un catalogo con un massimo di 500.000 SKU può essere indicizzato rapidamente come catalogo semplice.

>[!NOTE]
>
>Prima di abilitare un catalogo flat per un archivio live, assicurati di testare la configurazione in un ambiente di sviluppo.

## Passaggio 1: abilitare il catalogo flat

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi _Vetrina_ ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Use Flat Catalog Category]** a `Yes`. Se necessario, deselezionare la **[!UICONTROL Use system value]** casella di controllo.)

   - Imposta **[!UICONTROL Use Flat Catalog Product]** a `Yes`.

   ![Configurazione catalogo semplice](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando viene richiesto di aggiornare la cache, fare clic su **[!UICONTROL Cache Management]** nel messaggio di sistema e seguire le istruzioni per aggiornare la cache.

## Passaggio 2: verificare i risultati

Esistono due metodi per verificare i risultati.

### Metodo 1: verificare i risultati per un singolo prodotto

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Apri un prodotto in modalità di modifica.

1. Per **[!UICONTROL Name]**, aggiungi il testo `_TEST` alla fine del nome del prodotto.

1. Clic **[!UICONTROL Save]**.

1. In una nuova scheda del browser, passa alla home page del negozio ed effettua le seguenti operazioni:

   - Cerca il prodotto modificato.

   - Utilizza la navigazione per navigare fino al prodotto nella categoria a esso assegnata.

     Se necessario, aggiorna la pagina per visualizzare i risultati. La modifica viene visualizzata entro il minuto o in base al [Cron](../systems/cron.md) pianificazione.

   ![Vetrina con catalogo semplice](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### Metodo 2: verificare i risultati per una categoria

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell’angolo superiore sinistro, verifica che **[!UICONTROL Store View]** è impostato su `All Store Views`.

   Se richiesto, fare clic su **[!UICONTROL OK]** per confermare.

1. Nell&#39;albero delle categorie selezionare una categoria esistente e fare clic su **[!UICONTROL Add Subcategory]** ed eseguire le operazioni seguenti:

   - Per **[!UICONTROL Category Name]**, immetti `Test Category`.

   - Al termine, fai clic su **[!UICONTROL Save]**.

     ![Sottocategoria di prova](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Products in Category]** e fai clic su **[!UICONTROL Reset Filter]** per visualizzare tutti i prodotti.

   - Seleziona la casella di controllo di diversi prodotti da aggiungere alla nuova categoria.

   - click **[!UICONTROL Save]**.

   ![Prodotti categoria di prova](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. In una nuova scheda del browser passare alla home page del negozio e utilizzare la navigazione del negozio per passare alla categoria creata.

   Se necessario, aggiorna la pagina per visualizzare i risultati. La modifica viene visualizzata entro il minuto o in base alla pianificazione cron.

## Passaggio 3: rimuovere i dati del test

Per rimuovere i dati di test e ripristinare la configurazione originale del catalogo e del nome del prodotto, eseguire le operazioni seguenti.

### Rimuovi la categoria di test

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell&#39;albero delle categorie selezionare la sottocategoria di test creata.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Delete]**.

1. Quando viene richiesto di confermare, fai clic su **[!UICONTROL OK]**.

   La rimozione di questa categoria non rimuove i prodotti assegnati alla categoria.

### Ripristina il nome del prodotto originale

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Apri il prodotto di test in modalità di modifica.

1. Rimuovi il `_TEST` testo aggiunto al **[!UICONTROL Product Name]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]**.

### Ripristina la configurazione originale del catalogo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi _Vetrina_ ed effettuare le seguenti operazioni:

   - Imposta **[!UICONTROL Use Flat Catalog Category]** a `No`.

   - Imposta **[!UICONTROL Use Flat Catalog Product]** a `No`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, aggiorna la cache.
