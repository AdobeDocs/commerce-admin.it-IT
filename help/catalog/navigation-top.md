---
title: Navigazione superiore
description: Scopri come definire il menu principale di un negozio, che funziona come una directory per i diversi reparti.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
TQID: https://experienceleague.adobe.com/REad4AtBdJeK2eVNRo1XiTrrjJqmTs6oJfum260IfOk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 0%

---

# Navigazione superiore

Il menu principale del tuo negozio è come un elenco dei diversi reparti del negozio. Ogni opzione rappresenta una categoria diversa di prodotti. La posizione e la presentazione della navigazione superiore possono variare in base al tema, ma il modo in cui funziona è essenzialmente lo stesso.

![Navigazione superiore](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

La struttura delle categorie del catalogo può influenzare l’indicizzazione del sito da parte dei motori di ricerca. Più una categoria è annidata in profondità, meno è probabile che venga indicizzata in modo completo. In genere, l’utilizzo di un numero di livelli visibili compreso tra uno e tre è il più efficace. La [categoria principale](category-root.md) conta come primo livello, anche se non viene visualizzata nel menu. Il numero massimo di livelli disponibili nella navigazione superiore è determinato dalla configurazione. Inoltre, potrebbe esserci un limite al numero di livelli di menu supportati dal tema del negozio. Ad esempio, il tema Luma di esempio supporta fino a cinque livelli, inclusa la directory principale.

## Livelli del menu di conteggio

| Elemento | Descrizione |
|--- |--- |
| Livello 1 | Il primo livello è la categoria principale, che nei dati di esempio è denominata &quot;Categoria predefinita&quot;. La directory principale è un contenitore per il menu e il suo nome non viene visualizzato come opzione nel menu. |
| Livello 2 | Su uno schermo desktop, la navigazione superiore è il menu principale visualizzato nella parte superiore della pagina. Su un dispositivo mobile, il menu principale viene in genere visualizzato come un menu a comparsa di opzioni. Le opzioni di secondo livello nell&#39;archivio Luma sono _Novità_, _Donne_, _Uomini_, _Attrezzo_, _Formazione_ e _Vendita_. |
| Livello 3 | Il terzo livello viene visualizzato sotto ogni opzione del menu principale. Ad esempio, in _Donne_, le opzioni di terzo livello sono _Superiori_ e _Inferiori_. |
| Livello 4 | Le opzioni di quarto livello sono sottocategorie che si discostano da un’opzione di terzo livello. Ad esempio, in _Tops_, le opzioni di menu di quarto livello sono _Giacche_, _Felpe e felpe_, _Tees_ e _Bras e carrelli armati_. |

{style="table-layout:auto"}

## Impostare la navigazione superiore

La procedura seguente illustra come visualizzare una categoria nella navigazione superiore di un archivio:

### Passaggio 1: creare una categoria

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Imposta **[!UICONTROL Store View]** per determinare dove sarà disponibile la nuova categoria.

1. Nell&#39;albero delle categorie selezionare la categoria padre della nuova categoria.

   Se si inizia dall&#39;inizio senza dati, è possibile che nell&#39;elenco siano presenti solo due categorie: _Categoria predefinita_, ovvero la radice, e _Categoria di esempio_.

1. Fare clic su **[!UICONTROL Add Subcategory]**.

1. Completa le informazioni di base con le seguenti impostazioni:

   - **[!UICONTROL Enable Category]** impostato su `Yes`
   - **[!UICONTROL Include in Menu]** impostato su `Yes`

1. In Impostazione di visualizzazione impostare **[!UICONTROL Anchor]** su `Yes`.

1. Completa le altre [impostazioni di categoria](category-create.md) richieste.

1. Al termine, fare clic su **[!UICONTROL Save]**.

Per un&#39;installazione multistore, è possibile assegnare un menu principale diverso come [categoria principale](category-root.md) per ogni [archivio](../stores-purchase/stores.md#add-stores).

### Passaggio 2: impostare la profondità della navigazione superiore

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere la sezione **[!UICONTROL Category Top Navigation]**.

   ![Navigazione superiore categoria](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   Poiché la profondità della navigazione superiore ha un ambito di configurazione [globale](../getting-started/websites-stores-views.md#scope-settings), l&#39;impostazione si applica a tutti i siti Web, gli archivi e le visualizzazioni degli archivi nell&#39;installazione di Commerce. La sezione di configurazione _[!UICONTROL Category Top Navigation]_è disponibile solo quando_[!UICONTROL Store View]_ nell&#39;angolo superiore sinistro è impostato su `Default Config`.

   Per un elenco dettagliato di queste opzioni, vedere [Navigazione superiore categoria](../configuration-reference/catalog/catalog.md#layered-navigation) nella _Guida di riferimento configurazione_.

1. Per limitare il numero di sottocategorie visualizzate nella navigazione superiore, immettere il numero per **[!UICONTROL Maximal Depth]**.

   Il valore predefinito è `0`, che non pone alcun limite al numero di livelli di sottocategoria.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
