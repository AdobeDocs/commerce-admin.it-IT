---
title: Aggiungi un'origine inventario
description: Scopri come creare un’origine per un’ubicazione, ad esempio un magazzino, un magazzino, un centro di distribuzione o uno spedizioniere.
exl-id: 1bff9986-8722-4fb5-ac83-41de82325f7b
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---

# Aggiungi un&#39;origine

Gestire l&#39;evasione di scorte e ordini da più ubicazioni con origini personalizzate. Creare un&#39;origine per ogni posizione, ad esempio magazzini, magazzini fisici, centri di distribuzione e corrieri diretti. Assegna origini e aggiorna quantità per prodotto

Se si modifica Origine predefinita, è possibile modificare tutte le configurazioni ad eccezione del nome e del codice. È consigliabile che i commercianti single-source aggiungano informazioni corrispondenti alla loro posizione.

## Aggiungi un&#39;origine inventario

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**.

1. Clic **[!UICONTROL Add New Source]**.

   ![Gestisci origini](assets/inventory-sources.png)

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL General]** ed effettuare le seguenti operazioni:

   - Per identificare l&#39;origine del magazzino, inserire un valore univoco **[!UICONTROL Name]**.

   - Inserisci un valore univoco **[!UICONTROL Code]**.

     Il codice supporta lettere maiuscole e minuscole, numeri, trattini e trattini bassi. Il codice è un ID univoco utilizzato per l’assegnazione alle scorte e per l’esportazione-importazione dei dati.

   - Se l&#39;origine inventario è pronta per l&#39;uso, impostare **[!UICONTROL Is Enabled]** a `Yes`.

   - Inserisci una descrizione **[!UICONTROL Description]** per questa posizione come riferimento rapido o per ulteriori dettagli.

   - Per **[!UICONTROL Latitude]** e **[!UICONTROL Longitude]**, immettere le coordinate GPS della posizione dell&#39;impianto.

     Per trovare le coordinate GPS con [Mappe Google][1], immetti l&#39;indirizzo nella casella di ricerca. Fare clic con il pulsante destro del mouse sul marcatore sulla mappa e scegliere **[!UICONTROL What's here?]**. Le coordinate GPS vengono visualizzate nella casella dei dettagli sotto l&#39;indirizzo stradale.

     ![Opzioni di origine generali](assets/inventory-source-general.png)

   - Se l&#39;origine inventario è un&#39;ubicazione di prelievo, impostare **[!UICONTROL Use as Pickup Location]** a `Yes`.

     L&#39;origine predefinita non può essere utilizzata come ubicazione di prelievo per gli ordini di prelievo in-store.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Contact Info]** ed effettuare le seguenti operazioni:

   - Per **[!UICONTROL Contact Name]**, immettere il nome completo del contatto principale nel percorso.

   - Immetti un **[!UICONTROL Email]** indirizzo per contattare la posizione.

   - Per **[!UICONTROL Phone]**, immettere l&#39;indicativo di località e il numero di telefono.

   - Per **[!UICONTROL Fax]**, immettere l&#39;indicativo di località e il numero di telefono del fax, se disponibile.

     ![Informazioni di contatto](assets/inventory-source-contact-info.png)

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Address Data]** ed effettuare le seguenti operazioni:

   - Scegli la **[!UICONTROL Country]**.

   - Per **[!UICONTROL State/Province]**, immettere l&#39;abbreviazione standard per lo stato o la provincia.

   - Inserisci il **[!UICONTROL City]**.

   - Inserisci il valore fisico **[!UICONTROL Street]** indirizzo.

   - Per **[!UICONTROL Postcode]**, immetti il CAP.

     ![Dati indirizzo](assets/inventory-source-address.png)

1. Se si imposta l&#39;origine come posizione di prelievo nel passaggio precedente, espandere ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Pickup Location]** e forniscono informazioni descrittive sulla posizione:

   - Inserisci il **[!UICONTROL Frontend Name]** del luogo di prelievo.

   - Immetti un **[!UICONTROL Frontend Description]** del luogo di prelievo. Utilizzare questa casella di testo per visualizzare le ore del punto vendita, la posizione relativa ad altri punti di riferimento o altre informazioni utili che consentono al cliente di selezionare la posizione di prelievo corretta.

     ![Luogo di ritiro](assets/inventory-pickup-location.png)

   Per ulteriori informazioni su come configurare le notifiche e-mail quando si utilizza un’origine come percorso di prelievo, consulta [E-mail vendite](../configuration-reference/sales/sales-emails.md) nel _Guida di riferimento alla configurazione_.

1. Per salvare i dati, eseguire una delle operazioni seguenti:

   - Per salvare il lavoro e continuare la modifica, fare clic su **[!UICONTROL Save & Continue]**.

   - Per salvare i dati e tornare alla pagina Gestisci origini, fare clic sulla freccia in giù (![Freccia del menu](../assets/icon-menu-down-arrow-red.png)) e scegliere **[!UICONTROL Save & Close]**.

   - Per salvare i dati nel record di origine corrente e immettere una nuova origine, scegliere **[!UICONTROL Save & New]**.

## Barra dei pulsanti

| Pulsante | Descrizione |
|--|--|
| [!UICONTROL Back] | Torna alla pagina Gestisci origini. |
| [!UICONTROL Reset] | Ripristina i valori di tutti i campi del modulo al momento dell&#39;ultimo salvataggio. |
| [!UICONTROL Save & Continue] | Salva tutte le modifiche e mantiene il modulo aperto per ulteriori modifiche. Fai clic sulla freccia giù per visualizzare altre opzioni:<br/>**[!UICONTROL Save & Close]**- Salva le modifiche al record corrente, chiude la maschera e torna alla pagina Gestisci origini.<br/>**[!UICONTROL Save & New]** - Salva le modifiche, chiude il record corrente e apre un nuovo modulo vuoto. |

## Descrizioni dei campi

| Campo | Descrizione |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | (Obbligatorio) Nome univoco che identifica l’origine dell’inventario per gli utenti amministratori. |
| [!UICONTROL Code] | (Obbligatorio) Codice alfanumerico univoco utilizzato dal sistema per identificare l&#39;origine del magazzino. Inserisci il codice in caratteri maiuscoli o minuscoli e/o numeri, senza spazi. Se necessario, è possibile utilizzare un trattino o un carattere di sottolineatura anziché uno spazio. Impossibile modificare il codice dopo la creazione dell’origine. Si tratta di un ID univoco utilizzato quando si assegnano le origini alle scorte e si esportano e/o importano i dati dei prodotti. |
| [!UICONTROL Is Enabled] | Determina se l&#39;origine del magazzino è disponibile per l&#39;uso. Opzioni: Sì / No |
| [!UICONTROL Description] | Breve descrizione dell&#39;ubicazione origine magazzino. Includi dettagli utili per gli utenti amministratori. |
| [!UICONTROL Latitude] | Specifica la coordinata di latitudine dell&#39;origine inventario per GPS. Immetti il valore come numero, preceduto dal segno più o meno, a seconda delle necessità. Il simbolo di grado e le lettere non sono consentiti. Ad esempio: Latitude 32.7555 |
| [!UICONTROL Longitude] | Specifica la coordinata della longitudine dell&#39;origine di inventario per il GPS. Immetti il valore come numero, preceduto dal segno più o meno, a seconda delle necessità. Il simbolo di grado e le lettere non sono consentiti. Ad esempio: `-97.3308` |
| **[!UICONTROL Contact Info]** | |
| [!UICONTROL Contact Name] | Nome del contatto principale nell&#39;ubicazione di origine del magazzino. |
| [!UICONTROL Email] | Indirizzo e-mail del contatto principale. |
| [!UICONTROL Phone] | L&#39;indicativo di località e il numero di telefono del contatto principale, nel formato desiderato. Ad esempio: `(123) 456-7890` o `123-456-7890` |
| [!UICONTROL Fax] | L&#39;indicativo di località e il numero di fax del contatto principale. |
| **[!UICONTROL Address Data]** | |
| [!UICONTROL Country] | (Obbligatorio) Il paese in cui si trova l’origine delle scorte. |
| [!UICONTROL State/Province] | Stato o provincia in cui si trova l&#39;origine inventario. |
| [!UICONTROL City] | Città in cui si trova l&#39;origine inventario. |
| [!UICONTROL Street] | Indirizzo dell&#39;origine inventario. |
| [!UICONTROL Postcode] | (Obbligatorio) Il codice postale o ZIP dell’origine inventario. |
| **[!UICONTROL Pickup Location]** | |
| [!UICONTROL Frontend Name] | Nome della posizione di prelievo per l&#39;origine visualizzata nella vetrina. |
| [!UICONTROL Frontend Description] | Descrizione della posizione di prelievo per l&#39;origine visualizzata nella vetrina. Può contenere immagini allegate. |

[1]: https://www.google.com/maps
