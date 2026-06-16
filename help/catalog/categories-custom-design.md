---
title: Categorie - Impostazioni di progettazione
description: Scopri come utilizzare le impostazioni [!UICONTROL Design] per definire l'aspetto di una categoria, tutte le pagine di prodotto associate e il layout di pagina.
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/cRTRPl-UTfAKXY8rmtVKlnAZooVWpTCjSkVSdNHXp28
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 379
ht-degree: 0%

---

# Categorie - Impostazioni di progettazione

La sezione _[!UICONTROL Design]_consente di controllare l&#39;aspetto di una categoria, tutte le pagine di prodotto associate e il layout di pagina. È possibile personalizzare una pagina categoria e i relativi prodotti associati per una promozione o per differenziare la categoria. Ad esempio, puoi sviluppare un design distintivo per un marchio o una linea di prodotti speciale, oppure applicare un aggiornamento per un periodo di tempo specifico.

![Impostazioni di progettazione per una categoria](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Quando lo stesso prodotto viene assegnato a più categorie con impostazioni di progettazione diverse per ciascuna categoria, si consiglia di impostare **Usa percorso categorie per URL prodotto** = `Yes` nelle [opzioni di configurazione Ottimizzazione motore di ricerca](../configuration-reference/catalog/catalog.md#search-engine-optimization). Per accedere a questa impostazione, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**, espandi **[!UICONTROL Catalog]**e scegli **Catalogo**sotto nel pannello a sinistra, quindi espandi la sezione **Ottimizzazione motore di ricerca**nella pagina.

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | Consente alla categoria corrente di ereditare le impostazioni di progettazione dalla categoria padre. Se utilizzati, tutti gli altri campi della sezione Progettazione diventano non disponibili. Opzioni: `Yes` / ` No` |
| [!UICONTROL Theme] | Applica un tema personalizzato alla categoria. |
| [!UICONTROL Layout] | Applica un layout diverso alla pagina della categoria. Opzioni: <br/>**[!UICONTROL No layout updates]**- Per impostazione predefinita, gli aggiornamenti del layout non sono disponibili per le pagine delle categorie.<br/>**[!UICONTROL Empty]** - Consente di definire il layout di pagina. (Richiede la comprensione di XML) <br/>**[!UICONTROL 1 column]**- Applica un layout a una colonna alla pagina della categoria.<br/>**[!UICONTROL 2 columns with left bar]** - Applica un layout a due colonne con barra laterale a sinistra alla pagina della categoria. <br/>**[!UICONTROL 2 columns with right bar]**- Applica un layout a due colonne con una barra laterale a destra alla pagina della categoria.<br/>**[!UICONTROL 3 columns]** - Applica un layout a tre colonne alla pagina della categoria.<br/>**[!UICONTROL Page -- Full Width]**- (Richiede [Page Builder](../page-builder/introduction.md)) Applica il layout a larghezza intera per le pagine CMS alla pagina della categoria.<br/>**[!UICONTROL Category -- Full Width]** - (Richiede Page Builder) Applica il layout a larghezza intera per le pagine delle categorie alla pagina delle categorie. <br/>**[!UICONTROL Product -- Full Width]**- (Richiede Page Builder) Applica il layout a larghezza intera per le pagine dei prodotti alla pagina della categoria. |
| [!UICONTROL Custom Layout Update] | Elenca i file di aggiornamento del layout personalizzato disponibili sul server. Scegliere l&#39;aggiornamento del layout personalizzato da applicare alla categoria. |
| [!UICONTROL Apply Design to Products] | Se questa opzione è selezionata, applica le impostazioni personalizzate a tutti i prodotti della categoria. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

La sezione _[!UICONTROL Scheduled Design Update]_determina l&#39;intervallo di date in cui viene applicata una struttura personalizzata alle pagine delle categorie.

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Determina l’intervallo di date in cui viene applicato un layout personalizzato alla categoria. |

![Aggiornamento Progettazione Pianificato](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
