---
title: Classi di imposta
description: Scopri come configurare le classi di imposta utilizzate per le regole fiscali.
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# Classi di imposta

Le classi imposta possono essere assegnate a clienti, prodotti e spedizione. Commerce analizza il carrello di ogni cliente e calcola l&#39;imposta appropriata in base alla classe del cliente, alla classe dei prodotti nel carrello e all&#39;area. L&#39;area geografica è determinata dall&#39;indirizzo di spedizione, dall&#39;indirizzo di fatturazione o dall&#39;origine di spedizione del cliente. È possibile creare nuove classi di imposta quando viene definita una [regola fiscale](tax-rules.md).

- **Cliente**: è possibile creare tutte le classi di imposta cliente necessarie e assegnarle a [gruppi di clienti](../customers/customer-groups.md). In alcune giurisdizioni, ad esempio, le transazioni all&#39;ingrosso non sono tassate, mentre le transazioni al dettaglio lo sono. È possibile associare i membri del gruppo di clienti all&#39;ingrosso alla classe imposta all&#39;ingrosso.

- **Prodotto** — Le classi di prodotto vengono utilizzate nei calcoli per determinare l&#39;aliquota corretta applicata al carrello. Quando si crea un prodotto, questo viene assegnato a una classe fiscale specifica. Ad esempio, gli alimenti potrebbero non essere tassati o essere soggetti a un&#39;aliquota diversa.

- **Spedizione**: se il tuo negozio addebita un&#39;imposta aggiuntiva sulla spedizione, devi designare una classe di imposta del prodotto specifica per la spedizione. Quindi nella configurazione, specificala come classe di imposta utilizzata per la spedizione.

## Configurare le classi imposta

La classe fiscale utilizzata per la spedizione e le classi fiscali predefinite per [prodotti e clienti](#add-a-product-tax-class) sono impostate nella configurazione _[!UICONTROL Sales]_.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Tax]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Tax Classes]**.

   ![Configurazione - classi fiscali](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Scegliere la classe di imposta per ciascuno dei seguenti elementi:

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Aggiungi classi imposta

Le classi di imposta per clienti e prodotti possono essere facilmente aggiunte, quindi assegnate a singoli clienti e prodotti e utilizzate nelle regole fiscali.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Fare clic su **[!UICONTROL Add New Tax Rule]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Additional Settings]**.

   ![Aggiungi nuova classe fiscale](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. In _Classe imposta cliente_, fare clic su **[!UICONTROL Add New Tax Class]**.

1. Immettere **[!UICONTROL Name]** della nuova classe di imposta nella casella di testo.

   ![Aggiungi nuova classe fiscale](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. Per aggiungere la nuova classe all&#39;elenco delle classi imposta cliente disponibili, fare clic sul segno di spunta.

   ![Nuove classi imposta](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## Aggiungere una classe di imposta prodotto

1. In _Classe imposta prodotto_, fare clic su **[!UICONTROL Add New Tax Class]**.

1. Immettere **[!UICONTROL Name]** della nuova classe di imposta nella casella di testo.

1. Per aggiungere la nuova classe all&#39;elenco delle classi IVA prodotti disponibili, fare clic sul segno di spunta.

1. Al termine, fare clic su **[!UICONTROL Back]** nella barra dei pulsanti per tornare alla griglia _Regole fiscali_.

## Destinazione imposta predefinita

Le impostazioni di destinazione imposta predefinite determinano il paese, lo stato e il CAP utilizzati come base per i calcoli delle imposte.

**_Per configurare la destinazione imposta predefinita per i calcoli:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Tax]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Default Tax Destination Calculation]**.

   ![Calcolo destinazione imposta predefinita](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Impostare **[!UICONTROL Default Country]** sul paese su cui si basano i calcoli delle imposte.

1. Impostare **[!UICONTROL Default State]** sullo stato o sulla provincia utilizzata come base per i calcoli delle imposte.

1. Impostare **[!UICONTROL Default Post Code]** sul CAP utilizzato come base per il calcolo delle imposte locali.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
