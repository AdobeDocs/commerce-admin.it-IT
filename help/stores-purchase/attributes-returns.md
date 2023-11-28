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

![Amministratore - Restituisce attributi](./assets/attribute-returns.png){width="700" zoomable="yes"}

## Creare un attributo returns

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add New Attribute]**.

   ![Nuovo valore restituito: proprietà attributo](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### Definire le proprietà

1. Per identificare l&#39;attributo durante l&#39;immissione dei dati, impostare **[!UICONTROL Default Label]**.

1. Per **[!UICONTROL Attribute Code]**, immettere un codice che identifichi l&#39;attributo nel sistema.

1. Per determinare il tipo di controllo di input utilizzato per l&#39;immissione dei dati, impostare **[!UICONTROL Input Type]** a uno dei seguenti elementi:

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. Per rendere obbligatorio il campo, impostare **[!UICONTROL Values Required]** a `Yes`.

1. Per assegnare un valore iniziale al campo, immettere un valore **[!UICONTROL Default Value]**.

1. Per verificare l&#39;accuratezza dei dati immessi nel campo prima del salvataggio del record, impostare **[!UICONTROL Input Validation]** a uno dei seguenti elementi:

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. Per `Text Field` e `Text Area` tipi di input, immettere **[!UICONTROL Minimum Text Length]** e **[!UICONTROL Maximum Text Length]**.

1. Per applicare un filtro di pre-elaborazione, impostare **[!UICONTROL Input/Output Filter]** a uno dei seguenti elementi:

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. Per rendere visibile l’attributo ai clienti, imposta **[!UICONTROL Show on Storefront]** a `Yes` nel _[!UICONTROL Storefront Properties]_sezione.

1. (Facoltativo) Per **[!UICONTROL Sort Order]**, immettere un numero per determinare dove viene visualizzato l&#39;attributo rispetto agli altri nella stessa parte della pagina. (`0` = innanzitutto, `1` = secondo, `2` = terzo e così via.)

### Gestione delle etichette/opzioni

1. Nel pannello a sinistra, scegli **[!UICONTROL Manage Labels/Options]**.

1. In **[!UICONTROL Manage Titles (Size, Color, etc.)]** , immettere l&#39;etichetta per ogni visualizzazione store.

   ![Gestisci etichette](./assets/return-attributes.png){width="600" zoomable="yes"}

1. Se il **[!UICONTROL Input Type]** per l’attributo è `Dropdown`, gestisci le opzioni in **[!UICONTROL Manage Options (Values of Your Attribute)]** sezione.

   - Per aggiungere un’opzione, fai clic su **[!UICONTROL Add Option]** e inserisci l’etichetta per Admin e ogni visualizzazione store.
   - Per impostare un&#39;opzione come predefinita selezionata, scegliete **[!UICONTROL Is Default]**.
   - Per rimuovere un’opzione, fai clic su **[!UICONTROL Delete]**.

1. Per salvare le modifiche, fai clic su **[!UICONTROL Save Attribute]**.
