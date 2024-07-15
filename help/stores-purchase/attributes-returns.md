---
title: Restituisce un attributo
description: Scopri gli attributi di restituzione e come creare gli attributi necessari per l’elaborazione dei resi sul tuo store.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Restituisce un attributo

{{ee-feature}}

Gli attributi return vengono utilizzati per memorizzare le informazioni necessarie durante il processo di restituzione del prodotto. Gli attributi predefiniti includono la condizione del prodotto restituito, il motivo della restituzione e un campo che indica come è stata risolta la restituzione. Il processo di creazione di un attributo returns è simile alla creazione di un [attributo cliente](../customers/attribute-properties.md).

![Amministratore - Restituisce gli attributi](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Creare un attributo returns

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add New Attribute]**.

   ![Nuovo valore restituito - Proprietà attributo](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Definire le proprietà

1. Per identificare l&#39;attributo durante l&#39;immissione dei dati, impostare **[!UICONTROL Default Label]**.

1. Per **[!UICONTROL Attribute Code]**, immettere un codice che identifichi l&#39;attributo nel sistema.

1. Per determinare il tipo di controllo di input utilizzato per l&#39;immissione dei dati, impostare **[!UICONTROL Input Type]** su uno dei seguenti valori:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Per rendere obbligatorio il campo, impostare **[!UICONTROL Values Required]** su `Yes`.

1. Per assegnare un valore iniziale al campo, immettere **[!UICONTROL Default Value]**.

1. Per verificare la precisione dei dati immessi nel campo prima del salvataggio del record, impostare **[!UICONTROL Input Validation]** su una delle seguenti opzioni:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Per i tipi di input `Text Field` e `Text Area`, immettere **[!UICONTROL Minimum Text Length]** e **[!UICONTROL Maximum Text Length]**.

1. Per applicare un filtro di pre-elaborazione, impostare **[!UICONTROL Input/Output Filter]** su uno dei seguenti valori:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Per rendere visibile l&#39;attributo ai clienti, impostare **[!UICONTROL Show on Storefront]** su `Yes` nella sezione _[!UICONTROL Storefront Properties]_.

1. (Facoltativo) Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la posizione di questo attributo rispetto agli altri nella stessa parte della pagina. (`0` = primo, `1` = secondo, `2` = terzo e così via).

### Gestione delle etichette/opzioni

1. Nel pannello a sinistra, scegli **[!UICONTROL Manage Labels/Options]**.

1. Nella sezione **[!UICONTROL Manage Titles (Size, Color, etc.)]** immettere l&#39;etichetta per ogni visualizzazione dello store.

   ![Gestisci etichette](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Se **[!UICONTROL Input Type]** per l&#39;attributo è `Dropdown`, gestire le opzioni nella sezione **[!UICONTROL Manage Options (Values of Your Attribute)]**.

   - Per aggiungere un&#39;opzione, fare clic su **[!UICONTROL Add Option]** e immettere l&#39;etichetta per Admin e ogni visualizzazione dello store.
   - Per impostare un&#39;opzione come predefinita selezionata, scegliere **[!UICONTROL Is Default]**.
   - Per rimuovere un&#39;opzione, scegliere **[!UICONTROL Delete]**.

1. Per salvare le modifiche, fare clic su **[!UICONTROL Save Attribute]**.
