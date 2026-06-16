---
title: Categorie - Impostazioni di visualizzazione
description: Informazioni sull'utilizzo delle impostazioni [!UICONTROL Display] per definire gli elementi di contenuto da visualizzare in una pagina categoria e l'ordine di visualizzazione dei prodotti.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/t5UfvWvJ7R-kZb5kyMwpzwI2gfs3x3g1amlfWzQcAsw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# Categorie - Impostazioni di visualizzazione

Le impostazioni di visualizzazione determinano gli elementi di contenuto da visualizzare in una pagina di categoria e l&#39;ordine di visualizzazione dei prodotti. È possibile abilitare i blocchi di CMS, impostare lo stato di ancoraggio della categoria e gestire le opzioni di ordinamento dalla scheda _[!UICONTROL Display Settings]_. Per alcuni esempi sulla visualizzazione delle categorie nella vetrina, vedere [Navigazione catalogo](navigation.md).

![Impostazioni di visualizzazione per le categorie](./assets/category-display-settings.png){width="600" zoomable="yes"}

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Display Mode] | Determina gli elementi di contenuto visualizzati nella pagina della categoria. Opzioni: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | Se è impostato su `Yes`, visualizza i prodotti delle sottocategorie nella categoria anche se non sono stati aggiunti in modo esplicito alla categoria e abilita la visualizzazione della sezione _[!UICONTROL filter by attribute]_&#x200B;nella navigazione a livelli. Opzioni: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (Obbligatorio) I valori predefiniti sono `Position`, `Name` e `Price`. Per personalizzare l&#39;opzione di ordinamento, deselezionare la casella di controllo **[!UICONTROL Use All Available Attributes]** e selezionare gli attributi che si desidera utilizzare. Puoi definire e aggiungere attributi in base alle esigenze. Questa impostazione non è applicabile al [!DNL Live Search] [widget pagina elenco prodotti](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (Obbligatorio) Per definire l&#39;opzione predefinita _[!UICONTROL Sort By]_, deselezionare la casella di controllo **[!UICONTROL Use Config Settings]**&#x200B;e selezionare un attributo. Questa impostazione non è applicabile al [!DNL Live Search] [widget pagina elenco prodotti](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | Per impostazione predefinita, Commerce visualizza la fascia di prezzo con incrementi di 10, 100 e 1000, a seconda dei prodotti presenti nell&#39;elenco. Per modificare l&#39;intervallo di incrementi di prezzo, deselezionare la casella di controllo **[!UICONTROL Use Config Settings]**. |

{style="table-layout:auto"}
