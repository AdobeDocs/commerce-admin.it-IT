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

Le classi imposta possono essere assegnate a clienti, prodotti e spedizione. Commerce analizza il carrello di ciascun cliente e calcola l’imposta appropriata in base alla classe del cliente, alla classe dei prodotti nel carrello e all’area geografica. L&#39;area geografica è determinata dall&#39;indirizzo di spedizione, dall&#39;indirizzo di fatturazione o dall&#39;origine di spedizione del cliente. È possibile creare nuove classi di imposta quando [regola fiscale](tax-rules.md) è definito.

- **Cliente** — È possibile creare tutte le classi di imposta cliente necessarie e assegnarle a [gruppi di clienti](../customers/customer-groups.md). In alcune giurisdizioni, ad esempio, le transazioni all&#39;ingrosso non sono tassate, mentre le transazioni al dettaglio lo sono. È possibile associare i membri del gruppo di clienti all&#39;ingrosso alla classe imposta all&#39;ingrosso.

- **Prodotto** — Le classi di prodotti vengono utilizzate nei calcoli per determinare l&#39;aliquota corretta applicata nel carrello. Quando si crea un prodotto, questo viene assegnato a una classe fiscale specifica. Ad esempio, gli alimenti potrebbero non essere tassati o essere soggetti a un&#39;aliquota diversa.

- **Spedizione** — Se il tuo negozio addebita un&#39;imposta aggiuntiva sulla spedizione, devi designare una classe di imposta del prodotto specifica per la spedizione. Quindi nella configurazione, specificala come classe di imposta utilizzata per la spedizione.

## Configurare le classi imposta

Classe imposta utilizzata per la spedizione e classi imposta predefinite per [prodotti e clienti](#add-a-product-tax-class) sono impostati in _[!UICONTROL Sales]_configurazione.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Tax]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Tax Classes]** sezione.

   ![Configurazione - Classi di imposta](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Scegliere la classe di imposta per ciascuno dei seguenti elementi:

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Aggiungi classi imposta

Le classi di imposta per clienti e prodotti possono essere facilmente aggiunte, quindi assegnate a singoli clienti e prodotti e utilizzate nelle regole fiscali.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Clic **[!UICONTROL Add New Tax Rule]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Additional Settings]** sezione.

   ![Aggiungi nuova classe fiscale](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Sotto _Classe imposta cliente_, fai clic su **[!UICONTROL Add New Tax Class]**.

1. Inserisci il **[!UICONTROL Name]** della nuova classe di imposta nella casella di testo.

   ![Aggiungi nuova classe fiscale](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. Per aggiungere la nuova classe all&#39;elenco delle classi imposta cliente disponibili, fare clic sul segno di spunta.

   ![Nuove classi di imposta](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## Aggiungere una classe di imposta prodotto

1. Sotto _Classe imposta prodotto_, fai clic su **[!UICONTROL Add New Tax Class]**.

1. Inserisci il **[!UICONTROL Name]** della nuova classe di imposta nella casella di testo.

1. Per aggiungere la nuova classe all&#39;elenco delle classi IVA prodotti disponibili, fare clic sul segno di spunta.

1. Al termine, fai clic su **[!UICONTROL Back]** nella barra dei pulsanti per tornare al _Regole fiscali_ griglia.

## Destinazione imposta predefinita

Le impostazioni di destinazione imposta predefinite determinano il paese, lo stato e il CAP utilizzati come base per i calcoli delle imposte.

**_Per configurare la destinazione imposta predefinita per i calcoli:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Tax]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Default Tax Destination Calculation]** sezione.

   ![Calcolo destinazione imposta predefinita](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Default Country]** al paese su cui si basano i calcoli fiscali.

1. Imposta **[!UICONTROL Default State]** allo stato o alla provincia utilizzata come base per i calcoli delle imposte.

1. Imposta **[!UICONTROL Default Post Code]** al CAP utilizzato come base per il calcolo delle imposte locali.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
