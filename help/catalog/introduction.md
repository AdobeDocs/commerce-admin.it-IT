---
title: Introduzione alla gestione del catalogo
description: Scopri come funzionano il catalogo e l’ambito del prodotto nella gestione del catalogo.
exl-id: 3c58fc1c-d7a3-4f51-8a78-6bf2fd0dbeee
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Introduzione alla gestione del catalogo

Adobe Commerce e Magento Open Source utilizzano il termine _catalogo_ per fare riferimento al database di prodotti nel suo complesso.

Una delle aree più importanti nella creazione e gestione del negozio è la creazione di prodotti e categorie. L&#39;amministratore fornisce diversi strumenti utili per la configurazione iniziale del negozio e per la manutenzione del negozio e l&#39;ottimizzazione dell&#39;attività.

>[!TIP]
>
>Inventory management per Adobe Commerce e Magento Open Source offre gli strumenti per gestire l’inventario dei prodotti. I commercianti con un singolo punto vendita in più magazzini, magazzini, ubicazioni di prelievo, corrieri diretti e altro ancora possono utilizzare queste funzioni per gestire le quantità per le vendite e gestire le spedizioni per completare gli ordini. Per ulteriori informazioni su queste funzioni e su come utilizzarle per gestire le scorte in più posizioni, consulta la [Guida utente di Inventory management](../inventory-management/introduction.md).

## Ambito del catalogo

L&#39;accesso ai dati del catalogo è determinato da diversi fattori, tra cui l&#39;impostazione [scope](../getting-started/websites-stores-views.md#scope-settings), la configurazione del catalogo e la [categoria principale](category-root.md) assegnata all&#39;archivio. Il catalogo include i prodotti abilitati e disponibili per la vendita e i prodotti attualmente non in vendita.

Nelle vendite, il termine _catalogo_ si riferisce in genere a una selezione curata di prodotti disponibili per la vendita. Ad esempio, un negozio potrebbe avere un &quot;Catalogo primaverile&quot; e un &quot;Catalogo autunnale&quot;.

Analogamente al sommario di un catalogo stampato, il menu principale del tuo negozio, o _navigazione superiore_, organizza i prodotti per categoria in modo che i clienti possano trovare facilmente ciò che desiderano. Il menu principale si basa su una _categoria principale_, che è un contenitore per il menu assegnato all&#39;archivio. Poiché le opzioni di menu specifiche sono definite a livello della vista archivio, ogni vista può avere un menu principale diverso basato sulla stessa categoria principale. All’interno di ogni menu, puoi offrire una selezione curata di prodotti adatti al negozio.

![Diagramma della gerarchia del catalogo](./assets/catalog-hierarchy-scope.svg){width="550"}

## Ambito del prodotto

Per le installazioni con più siti Web, store e visualizzazioni, l&#39;impostazione [ambito](../getting-started/websites-stores-views.md#scope-settings) determina dove sono disponibili i prodotti per la vendita e le informazioni sul prodotto disponibili per ogni visualizzazione dello store. Inizialmente, tutti i prodotti creati vengono pubblicati nella visualizzazione predefinita per siti Web, store e store.

![diagramma archivio multisito](./assets/scope-multisite.svg){width="550"}

Se si dispone di un solo archivio con la visualizzazione predefinita, è possibile eseguirlo in [modalità archivio singolo](../getting-started/websites-stores-views.md#single-store-mode) per nascondere le impostazioni dell&#39;ambito. Tuttavia, se lo store dispone di più visualizzazioni, sotto il nome di ciascun campo viene visualizzato un indicatore di ambito.

- Per modificare le informazioni sul prodotto per una visualizzazione specifica, utilizzare il controllo _Visualizzazione store_ nell&#39;angolo superiore sinistro per scegliere la visualizzazione. Controlli aggiuntivi diventano disponibili per qualsiasi campo che può essere modificato a livello di visualizzazione punto vendita.

- Per definire l&#39;ambito di un prodotto in un&#39;installazione multisito, vedere la sezione [Product in Websites](settings-basic-websites.md) delle informazioni sul prodotto.

Il processo di modifica di un prodotto per una visualizzazione store è simile all&#39;aggiunta di un livello di informazioni sul prodotto specifico per la visualizzazione.

È possibile modificare o assegnare prodotti solo per il sito per il quale si dispone delle autorizzazioni, non per tutti i siti a cui il prodotto è assegnato.

Anche se la visualizzazione archivio _Spagnolo_ è selezionata nell&#39;esempio seguente, le informazioni sul prodotto vengono comunque visualizzate nella lingua originale della visualizzazione archivio predefinita. Per tradurre le informazioni sul prodotto, devi passare alla visualizzazione dello store _Spagnolo_ e tradurre i campi di testo, ad esempio il titolo del prodotto, la descrizione e i metadati. Per ulteriori informazioni, vedere [Localizzare i prodotti](../stores-purchase/store-localize.md#localize-products).

## Modificare un prodotto per una visualizzazione diversa

>[!NOTE]
>
>L&#39;ambito _Tutte le visualizzazioni archivio_ è disabilitato per gli utenti amministratori limitati a un ambito specifico quando il prodotto viene pubblicato anche al di fuori dell&#39;ambito consentito. Il primo ambito disponibile per la modifica è selezionato per impostazione predefinita perché gli utenti con restrizioni non possono eseguire azioni _global_ o azioni che interessano ambiti ai quali non hanno accesso.

1. Nell&#39;angolo in alto a sinistra, impostare **[!UICONTROL Store View]** sulla visualizzazione specifica da modificare.

1. Per confermare la modifica dell&#39;ambito, fare clic su **[!UICONTROL OK]**.

1. Aggiorna il campo con il nuovo valore per la vista Store.

   Sotto qualsiasi campo modificabile per la visualizzazione Store viene visualizzata una casella di controllo. Per ignorare il valore predefinito, deselezionare la casella di controllo **Usa valore predefinito**.

   ![Traduzione del nome del prodotto per la visualizzazione dello store spagnolo](./assets/product-translate-field-french.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save]**.

1. Nell&#39;angolo superiore sinistro impostare nuovamente il selettore **[!UICONTROL Store View]** sul valore predefinito.

1. Per verificare la modifica nel tuo archivio, effettua le seguenti operazioni:

   - Nell&#39;angolo superiore destro fare clic sulla freccia del menu _Amministratore_ e scegliere **[!UICONTROL Customer View]**.

     ![Visualizzazione clienti](./assets/product-admin-menu-customer-view.png){width="600" zoomable="yes"}

   - Nell&#39;angolo superiore destro dello store, impostare **[!UICONTROL Language Chooser]** sulla visualizzazione dello store del prodotto modificato e trovare il prodotto modificato per la visualizzazione.

     ![Selettore lingua](./assets/storefront-language-chooser.png){width="700" zoomable="yes"}
