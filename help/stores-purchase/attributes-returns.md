---
title: Restituisce un attributo
description: Scopri gli attributi di restituzione e come creare gli attributi necessari per l’elaborazione dei resi sul tuo store.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
TQID: https://experienceleague.adobe.com/bKSZbmmyG9CWVIf0GzCgGImzHRIUV8HgD6asutC7lFo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 306
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
