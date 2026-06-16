---
title: Aree e aliquote fiscali
description: Scopri come definire le aliquote per ogni area geografica in cui vengono riscosse e rimesse le imposte.
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
TQID: https://experienceleague.adobe.com/HHCiYX6ihYArvccmTswjnZ5SNP09D29Srn2JvWiw4tY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 380
ht-degree: 0%

---

# Aree e aliquote fiscali

Le aliquote d&#39;imposta si applicano generalmente alle transazioni che si svolgono all&#39;interno di una specifica area geografica. Utilizzare lo strumento _Aree e aliquote fiscali_ per specificare l&#39;aliquota per ogni area geografica da cui si riscuotono e rimettono le imposte. Poiché ogni area fiscale e aliquota ha un identificatore univoco, è possibile avere più aliquote per una determinata area geografica (ad esempio luoghi che non tassano alimenti o medicinali, ma tassano altri articoli).

L&#39;imposta del negozio viene calcolata in base all&#39;indirizzo del negozio. L&#39;imposta effettiva del cliente per un ordine viene calcolata dopo che il cliente ha completato le informazioni sull&#39;ordine. Commerce calcola quindi l&#39;imposta in base alla configurazione dell&#39;imposta del negozio.

![Aree e aliquote fiscali](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## Definisci una nuova aliquota

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add New Tax Rate]**.

   ![Nuova aliquota](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. Immetti **[!UICONTROL Tax Identifier]**.

1. Per applicare l&#39;aliquota a un singolo CAP, immettere il codice per **[!UICONTROL Zip/Post Code]**.

   Il carattere jolly asterisco (`*`) può essere utilizzato per trovare fino a dieci caratteri nel codice. Ad esempio, `90*` rappresenta tutti i codici postali da 90000 a 90999.

1. Per applicare l&#39;aliquota a un intervallo di codici postali o CAP, eseguire le operazioni seguenti:

   - Selezionare la casella di controllo **[!UICONTROL Zip/Post is Range]** e definire l&#39;intervallo immettendo il primo e l&#39;ultimo CAP per **[!UICONTROL Range From]** e **[!UICONTROL Range To]**.

     ![ZIP/Post compreso nell&#39;intervallo](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - Scegliere **[!UICONTROL State]** in cui applicare l&#39;aliquota.

   - Scegliere **[!UICONTROL Country]** in cui applicare l&#39;aliquota.

   - Immettere **[!UICONTROL Rate Percent]** utilizzato per il calcolo dell&#39;aliquota.

1. Se si dispone di più archivi, è possibile impostare **[!UICONTROL Tax Titles]** per ogni visualizzazione dello store.

   >[!NOTE]
   >
   >Lasciare vuoto questo campo se si desidera utilizzare l&#39;identificatore di imposta.

1. Al termine, fare clic su **[!UICONTROL Save Rate]**.

## Modifica un&#39;aliquota esistente

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Trovare l&#39;aliquota nella griglia _[!UICONTROL Tax Zones and Rates]_e aprire il record in modalità di modifica.

   Se nell&#39;elenco sono presenti molte tariffe, utilizzare i [controlli filtro](../getting-started/admin-grid-controls.md) per trovare la tariffa necessaria.

1. Apportare le modifiche necessarie a **[!UICONTROL Tax Rate Information]**.

1. Aggiorna **[!UICONTROL Tax Titles]** in base alle esigenze.

1. Al termine, fare clic su **[!UICONTROL Save Rate]**.

## Elimina aliquota

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Individuare l&#39;aliquota da eliminare e aprirla in modalità di modifica.

1. Nella barra dei menu fare clic su **[!UICONTROL Delete Rate]**.

1. Per confermare l&#39;azione, fare clic su **[!UICONTROL OK]**.
