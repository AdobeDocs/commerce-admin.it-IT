---
title: Aree e aliquote fiscali
description: Scopri come definire le aliquote per ogni area geografica in cui vengono riscosse e rimesse le imposte.
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Aree e aliquote fiscali

Le aliquote d&#39;imposta si applicano generalmente alle transazioni che si svolgono all&#39;interno di una specifica area geografica. Utilizza il _Aree fiscali e aliquote_ strumento per specificare l&#39;aliquota per ogni area geografica da cui si riscuotono e rimettono le imposte. Poiché ogni area fiscale e aliquota ha un identificatore univoco, è possibile avere più aliquote per una determinata area geografica (ad esempio luoghi che non tassano alimenti o medicinali, ma tassano altri articoli).

L&#39;imposta del negozio viene calcolata in base all&#39;indirizzo del negozio. L&#39;imposta effettiva del cliente per un ordine viene calcolata dopo che il cliente ha completato le informazioni sull&#39;ordine. Commerce calcola quindi l’imposta in base alla configurazione dell’imposta del negozio.

![Aree fiscali e aliquote](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## Definisci una nuova aliquota

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add New Tax Rate]**.

   ![Nuova aliquota](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. Immetti un **[!UICONTROL Tax Identifier]**.

1. Per applicare l&#39;aliquota a un singolo CAP, immettere il codice per **[!UICONTROL Zip/Post Code]**.

   Carattere jolly asterisco (`*`) può essere utilizzato per far corrispondere fino a dieci caratteri nel codice. Ad esempio: `90*` rappresenta tutti i codici postali da 90000 a 90999.

1. Per applicare l&#39;aliquota a un intervallo di codici postali o CAP, eseguire le operazioni seguenti:

   - Seleziona la **[!UICONTROL Zip/Post is Range]** e definisci l’intervallo immettendo il primo e l’ultimo CAP per **[!UICONTROL Range From]** e **[!UICONTROL Range To]**.

     ![ZIP/Post è intervallo](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - Scegli la **[!UICONTROL State]** dove si applica l’aliquota.

   - Scegli la **[!UICONTROL Country]** dove si applica l’aliquota.

   - Inserisci il **[!UICONTROL Rate Percent]** utilizzato per il calcolo dell&#39;aliquota.

1. Se disponi di più store, puoi impostare **[!UICONTROL Tax Titles]** per ogni visualizzazione store.

   >[!NOTE]
   >
   >Lasciare vuoto questo campo se si desidera utilizzare l&#39;identificatore di imposta.

1. Al termine, fai clic su **[!UICONTROL Save Rate]**.

## Modifica un&#39;aliquota esistente

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Trova l’aliquota in _[!UICONTROL Tax Zones and Rates]_e aprire il record in modalità di modifica.

   Se l&#39;elenco contiene molte tariffe, utilizzare [controlli filtro](../getting-started/admin-grid-controls.md) per trovare la tariffa desiderata.

1. Apporta le modifiche necessarie al **[!UICONTROL Tax Rate Information]**.

1. Aggiornare il **[!UICONTROL Tax Titles]** secondo necessità.

1. Al termine, fai clic su **[!UICONTROL Save Rate]**.

## Elimina aliquota

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. Individuare l&#39;aliquota da eliminare e aprirla in modalità di modifica.

1. Nella barra dei menu, fai clic su **[!UICONTROL Delete Rate]**.

1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.
