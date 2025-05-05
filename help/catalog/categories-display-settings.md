---
title: Categorie - Impostazioni di visualizzazione
description: Informazioni sull'utilizzo delle impostazioni [!UICONTROL Display] per definire gli elementi di contenuto da visualizzare in una pagina categoria e l'ordine di visualizzazione dei prodotti.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Categorie - Impostazioni di visualizzazione

Le impostazioni di visualizzazione determinano gli elementi di contenuto da visualizzare in una pagina di categoria e l&#39;ordine di visualizzazione dei prodotti. È possibile abilitare i blocchi di CMS, impostare lo stato di ancoraggio della categoria e gestire le opzioni di ordinamento dalla scheda _[!UICONTROL Display Settings]_. Per alcuni esempi sulla visualizzazione delle categorie nella vetrina, vedere [Navigazione catalogo](navigation.md).

![Impostazioni di visualizzazione per le categorie](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Display Mode] | Determina gli elementi di contenuto visualizzati nella pagina della categoria. Opzioni: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Se è impostato su `Yes`, visualizza i prodotti delle sottocategorie nella categoria anche se non sono stati aggiunti in modo esplicito alla categoria e abilita la visualizzazione della sezione _[!UICONTROL filter by attribute]_&#x200B;nella navigazione a livelli. Opzioni: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obbligatorio) I valori predefiniti sono `Position`, `Name` e `Price`. Per personalizzare l&#39;opzione di ordinamento, deselezionare la casella di controllo **[!UICONTROL Use All Available Attributes]** e selezionare gli attributi che si desidera utilizzare. Puoi definire e aggiungere attributi in base alle esigenze. Questa impostazione non è applicabile al [!DNL Live Search] [widget pagina elenco prodotti](https://experienceleague.adobe.com/it/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Obbligatorio) Per definire l&#39;opzione predefinita _[!UICONTROL Sort By]_, deselezionare la casella di controllo **[!UICONTROL Use Config Settings]**&#x200B;e selezionare un attributo. Questa impostazione non è applicabile al [!DNL Live Search] [widget pagina elenco prodotti](https://experienceleague.adobe.com/it/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | Per impostazione predefinita, Commerce visualizza la fascia di prezzo con incrementi di 10, 100 e 1000, a seconda dei prodotti presenti nell&#39;elenco. Per modificare l&#39;intervallo di incrementi di prezzo, deselezionare la casella di controllo **[!UICONTROL Use Config Settings]**. |

{style="table-layout:auto"}
