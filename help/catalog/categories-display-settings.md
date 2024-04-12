---
title: Categorie - Impostazioni di visualizzazione
description: Scopri come utilizzare il [!UICONTROL Display] impostazioni per definire gli elementi di contenuto da visualizzare in una pagina categoria e l’ordine in cui vengono visualizzati i prodotti.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: b99212b2c6977fc788e75df4bdce608fc4998dc4
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Categorie - Impostazioni di visualizzazione

Le impostazioni di visualizzazione determinano gli elementi di contenuto da visualizzare in una pagina di categoria e l&#39;ordine di visualizzazione dei prodotti. Puoi abilitare i blocchi CMS, impostare lo stato di ancoraggio della categoria e gestire le opzioni di ordinamento dalla sezione _[!UICONTROL Display Settings]_scheda. Per esempi sul modo in cui le categorie si riflettono nella vetrina, vedi [Navigazione nel catalogo](navigation.md).

![Impostazioni di visualizzazione per le categorie](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Display Mode] | Determina gli elementi di contenuto visualizzati nella pagina della categoria. Opzioni: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Se impostato su `Yes`, include _[!UICONTROL filter by attribute]_nella navigazione a livelli. Opzioni: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obbligatorio) I valori predefiniti sono `Position`, `Name`, e `Price`. Per personalizzare l’opzione di ordinamento, deseleziona la **[!UICONTROL Use All Available Attributes]** e selezionare gli attributi che si desidera utilizzare. Puoi definire e aggiungere attributi in base alle esigenze. Questa impostazione non si applica al [!DNL Live Search] [Widget pagina elenco prodotti](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Obbligatorio) Per definire il valore predefinito _[!UICONTROL Sort By]_deselezionare l&#39;opzione **[!UICONTROL Use Config Settings]**e selezionare un attributo. Questa impostazione non si applica al [!DNL Live Search] [Widget pagina elenco prodotti](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | Per impostazione predefinita, Commerce visualizza la fascia di prezzo con incrementi di 10, 100 e 1000, a seconda dei prodotti presenti nell&#39;elenco. Per modificare l&#39;intervallo di incrementi di prezzo, deselezionare **[!UICONTROL Use Config Settings]** casella di controllo. |

{style="table-layout:auto"}
