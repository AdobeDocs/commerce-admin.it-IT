---
title: Regole fiscali
description: Scopri come definire le regole fiscali utilizzando la classe di prodotto, la classe di cliente e l’aliquota.
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Regole fiscali

Le regole fiscali includono una combinazione di classe di prodotto, classe di cliente e aliquota. A ogni cliente viene assegnata una classe di clienti e a ogni prodotto viene assegnata una classe di prodotti. Commerce analizza il carrello di ciascun cliente e calcola l’imposta appropriata in base al cliente, alle classi di prodotti e all’area geografica. L&#39;area geografica si basa sull&#39;indirizzo di spedizione, sull&#39;indirizzo di fatturazione o sull&#39;origine di spedizione del cliente.

>[!NOTE]
>
>Quando è necessario definire numerose aliquote fiscali, è possibile semplificarne il processo importandole.

![Regole fiscali](./assets/tax-rules.png){width="600" zoomable="yes"}

## Passaggio 1: Completare le informazioni sulle regole fiscali

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add New Tax Rule]**.

1. Sotto _Informazioni sulle regole fiscali_, immetti un **[!UICONTROL Name]** per la nuova regola.

   ![Informazioni sulle regole fiscali](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. Scegli la **[!UICONTROL Tax Rate]** questo vale per la regola.

   Per modificare un&#39;aliquota esistente, effettuare le seguenti operazioni:

   - Passa il puntatore del mouse sull’aliquota e fai clic su _Modifica_ ![Icona matita](../assets/icon-edit-pencil.png) icona.

   - Aggiorna il modulo secondo necessità e fai clic su **[!UICONTROL Save]**.

1. Per inserire le aliquote, utilizzare uno dei metodi seguenti:

### Metodo 1: inserire manualmente le aliquote

1. Clic **[!UICONTROL Add New Tax Rate]**.

1. Completare il modulo in base alle esigenze (vedere [Aree e aliquote fiscali](tax-zones-rates.md)).

1. Al termine, fai clic su **[!UICONTROL Save]**.

   ![Nuova aliquota](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### Metodo 2: Aliquote di imposta all&#39;importazione

1. Scorri fino alla sezione nella parte inferiore della pagina.

1. Per importare le aliquote, effettuare le seguenti operazioni:

   - Clic **[!UICONTROL Choose File]** e passa al file CSV con le aliquote da importare.

   - Clic **[!UICONTROL Import Tax Rates]**.

1. Per esportare le aliquote, fare clic su **[!UICONTROL Export Tax Rates]** (vedere [Importa/Esporta aliquote](../systems/data-transfer-tax-rates.md)).

![Importa/Esporta aliquote](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## Passaggio 2: completare le impostazioni aggiuntive

1. Per aprire la sezione, fare clic su **[!UICONTROL Additional Settings]**.

   ![Impostazioni aggiuntive per la regola fiscale](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. Scegli la **[!UICONTROL Customer Tax Class]** a cui si applica la regola.

   - Per modificare una classe fiscale cliente, fare clic su _Modifica_ ![Icona matita](../assets/icon-edit-pencil.png) , aggiorna il modulo in base alle esigenze e fai clic su **[!UICONTROL Save]**.

   - Per creare una classe fiscale, fare clic su **[!UICONTROL Add New Tax Class]**, completare il modulo in base alle esigenze e fare clic su **[!UICONTROL Save]**.

1. Scegli la **[!UICONTROL Product Tax Class]** a cui si applica la regola.

   - Per modificare una classe di imposta prodotto, fare clic su _Modifica_ ![Icona matita](../assets/icon-edit-pencil.png) , aggiorna il modulo in base alle esigenze e fai clic su **[!UICONTROL Save]**.

   - Per creare una classe fiscale, fare clic su **[!UICONTROL Add New Tax Class]**, completare il modulo in base alle esigenze e fare clic su **[!UICONTROL Save]**.

1. Quando sono applicabili più imposte, immettere un numero per indicare la priorità di questa imposta per **[!UICONTROL Priority]**.

   Se si applicano due regole fiscali con la stessa priorità, le imposte vengono aggiunte. Se vengono applicate due imposte con impostazioni di priorità diverse, le imposte vengono composte.

1. Se si desidera che le imposte siano basate sul subtotale dell&#39;ordine, selezionare **[!UICONTROL Calculate off Subtotal Only]** casella di controllo.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per indicare l&#39;ordine di questa regola fiscale quando elencata con altri.

1. Al termine, fai clic su **[!UICONTROL Save Rule]**.

## Demo sulle regole di valuta e fiscali

Scopri come gestire la valuta e le regole fiscali guardando questo video:

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12)
