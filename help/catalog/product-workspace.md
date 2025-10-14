---
title: Area di lavoro prodotto
description: Scopri le impostazioni e i controlli disponibili nell’area di lavoro del prodotto.
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Area di lavoro prodotto

L’area di lavoro del prodotto è sostanzialmente la stessa per tutti i tipi di prodotto, anche se la selezione dei campi cambia a seconda del set di attributi utilizzato. Gli attributi del prodotto si trovano nella parte superiore del modulo, seguiti da sezioni espandibili di informazioni sul prodotto. Quando si salva un nuovo prodotto per la prima volta, il selettore _[!UICONTROL Store View]_&#x200B;viene visualizzato in alto a sinistra nel modulo.

![Area di lavoro prodotto](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## Impostazione [!UICONTROL Enable Product]

Lo stato online del prodotto è indicato dal pulsante nella parte superiore del modulo. Per modificare lo stato in linea, impostare l&#39;opzione **[!UICONTROL Enable Product]** su `Yes` o `No`.

| Controllo | Descrizione |
|-------- | ----------- |
| ![Attiva/Disattiva Sì](../assets/toggle-yes.png) | Indica che il prodotto è online. |
| ![Attiva/Disattiva &#x200B;](../assets/toggle-no.png) | Indica che il prodotto è offline. |

{style="table-layout:auto"}

## Set di attributi

Il nome del [set di attributi](attribute-sets.md) viene visualizzato nell&#39;angolo superiore sinistro e determina i campi visualizzati nel record di prodotto. Per scegliere una serie di attributi diversa, fare clic sulla freccia rivolta verso il basso accanto al nome della serie di attributi predefinita.

![Set di attributi](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## Espandi/comprimi

Per espandere o comprimere una sezione, fare clic sull&#39;icona Espandi ![Selettore di espansione](../assets/icon-display-expand.png) o Comprimi ![Comprimi selettore](../assets/icon-display-collapse.png).

## Menu [!UICONTROL Save]

Il menu _[!UICONTROL Save]_&#x200B;include diverse opzioni che consentono di salvare e continuare, salvare e creare un prodotto, salvare e duplicare il prodotto o salvare e chiudere.

![Salva menu](./assets/product-save-menu.png){width="600" zoomable="yes"}

| Comando | Descrizione |
|--- |--- |
| [!UICONTROL Save] | Salva il prodotto corrente e continua a lavorare. |
| [!UICONTROL Save & New] | Salva e chiudi il prodotto corrente e inizia un nuovo prodotto basato sullo stesso tipo di prodotto e modello. |
| [!UICONTROL Save & Duplicate] | Salva e chiudi il prodotto corrente e apri una nuova copia duplicata. |
| [!UICONTROL Save & Close] | Salvare il prodotto corrente e tornare all&#39;area di lavoro _[!UICONTROL Products]_. |

{style="table-layout:auto"}

## Valori di campo predefiniti

Per risparmiare tempo durante la creazione dei prodotti, il valore predefinito di diversi campi prodotto fa riferimento a valori provenienti da un altro campo. Potete accettare il valore predefinito o immetterne un altro. I seguenti campi hanno generato automaticamente i valori predefiniti:

| Campo | Predefinito |
|----- |------- |
| [!UICONTROL SKU] | In base al nome del prodotto. |
| [!UICONTROL Meta Title] | In base al nome del prodotto. |
| [!UICONTROL Meta Keywords] | In base al nome del prodotto. |
| [!UICONTROL Meta Description] | In base al nome e alla descrizione del prodotto. |

{style="table-layout:auto"}

I segnaposto che rappresentano il valore di un altro campo sono racchiusi tra parentesi graffe. Qualsiasi codice di attributo incluso nel prodotto [set di attributi](attribute-sets.md) può essere utilizzato come segnaposto.

![Generazione automatica campi prodotto](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

Per un elenco dettagliato di queste impostazioni, vedere [Generazione automatica campi prodotto](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) nel _Riferimento configurazione_.

### Modifica il valore del segnaposto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Product Fields Auto-Generation]** e apportare le modifiche necessarie ai valori dei segnaposto.

   Ad esempio, se è presente una parola chiave specifica che si desidera includere per ogni prodotto o una frase da includere in ogni descrizione meta, immettere il valore direttamente nel campo appropriato.

   >[!NOTE]
   >
   >Se si desidera mantenere i valori dei segnaposto esistenti, mantenere le doppie parentesi graffe che racchiudono ogni tag di markup.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

### Segnaposto comuni

- `{{color}}`
- `{{country_of_manufacture}}`
- `{{description}}`
- `{{gender}}`
- `{{material}}`
- `{{name}}`
- `{{short_description}}`
- `{{size}}`
- `{{sku}}`
