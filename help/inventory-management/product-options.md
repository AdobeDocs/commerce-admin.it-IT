---
title: "Configura  [!DNL Inventory Management]  opzioni prodotto"
description: Scopri come configurare le opzioni di configurazione del prodotto  [!DNL Inventory Management] .
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# Configura opzioni prodotto [!DNL Inventory Management]

Queste configurazioni si applicano solo al prodotto modificato, ignorando tutte le configurazioni a livello di sito web globale. Modificare queste impostazioni durante la modifica di un prodotto, tramite la sezione _[!UICONTROL Sources]_e la pagina_[!UICONTROL Advanced Inventory]_.

- Configurare le opzioni prodotto per origine
- Configurare le opzioni prodotto per l’inventario avanzato

## Opzioni prodotto per origine

Configura le quantità e le impostazioni aggiuntive per [origine aggiunta](sources-add.md) per il prodotto.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Apri un prodotto in modalità di modifica.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Sources]** e configurare le impostazioni del prodotto per ogni origine:

   - Immettere un importo di **[!UICONTROL Qty]** (quantità).

   - Imposta **[!UICONTROL Source Item Status]** come `In Stock` o `Out of Stock`.

   - Per modificare la notifica per la quantità seguente per origine, deselezionare o selezionare la casella di controllo **[!UICONTROL Notify Quantity Use Default]**.

     Se liquidato, inserire l&#39;importo a livello di magazzino che attiva la notifica di esaurimento scorte dell&#39;articolo. L&#39;importo inserito viene sottratto dalla quantità di vendita dell&#39;articolo a livello di magazzino.

     `Select to use Default` - [!DNL Commerce] controlla le opzioni di inventario avanzato del prodotto per le impostazioni di configurazione.
     `Clear to Modify` - Immettere un valore per la quantità di notifica, sostituendo le impostazioni di configurazione avanzate di magazzino e magazzino.

   ![Sezione origini per un prodotto](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Done]**, quindi su **[!UICONTROL Save]**.

### Descrizioni dei campi

| Campo | Ambito | Descrizione |
|--|--|--|
| [!UICONTROL Source Code] | Globale | Il codice univoco per una [sorgente](sources-manage.md). |
| [!UICONTROL Name] | Globale | Nome univoco di un&#39;origine. |
| [!UICONTROL Status] | Globale | Il prodotto è abilitato o disabilitato nel catalogo. |
| [!UICONTROL Source Item Status] | Globale | Determina la disponibilità corrente del prodotto. Opzioni:<br />`In Stock` - Rende il prodotto disponibile per l&#39;acquisto.<br />`Out of Stock` - A meno che non siano attivati gli ordini inevasi, impedisce che il prodotto sia disponibile per l&#39;acquisto e rimuove l&#39;inserzione dal catalogo. |
| [!UICONTROL Qty] | Globale | Quantità di scorte disponibili per ogni origine o ubicazione. |
| [!UICONTROL Notify Quantity] | Globale | Importo per _[!UICONTROL Notify for Quantity Below]_per questa origine specifica se_[!UICONTROL Notify Quantity Use Default]_ non è selezionato. |
| [!UICONTROL Notify Quantity Use Default] | Globale | Indica di utilizzare l&#39;impostazione predefinita per _[!UICONTROL Notify for Quantity Below]_nel prodotto_[!UICONTROL Advanced Inventory]_ o l&#39;impostazione globale nella configurazione dell&#39;archivio. |

## Opzioni di prodotto avanzate

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Apri un prodotto in modalità di modifica.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Sources]** e fare clic su **[!UICONTROL Advanced Inventory]**.

1. Per abilitare [il controllo inventario](enable.md) per il catalogo, impostare **[!UICONTROL Manage Stock]** su `Yes`.

   >[!NOTE]
   >
   >Le impostazioni di [!UICONTROL Manage Stock] nei prodotti secondari sovrascrivono un prodotto configurabile.

   ![Inventario avanzato per un prodotto](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Immettere un importo per **[!UICONTROL Out-of-Stock Threshold]**:

   | Valore | Descrizione |
   | ----- | ----- |
   | Importo positivo | Se _[!UICONTROL Backorders]_è disabilitato, immettere un valore positivo. |
   | Zero | Con _[!UICONTROL Backorders]_abilitato, l&#39;immissione di `0` consente ordini inevasi infiniti. |
   | Importo negativo | Se _[!UICONTROL Backorders]_è abilitato, si consiglia di immettere un valore negativo. L&#39;importo viene aggiunto alla quantità di vendita. Ad esempio, immettere `-50` per consentire ordini fino a questo importo. |

1. Immettere **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. Immettere **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. Impostare **[!UICONTROL Qty uses Decimals]** su `Yes` se i clienti possono utilizzare un valore decimale anziché un numero intero quando si immette la quantità ordinata.

1. Impostare **[!UICONTROL Allow Multiple Boxes for Shipping]** su `Yes` se il prodotto può essere venduto separatamente, in molte scatole. Questa opzione è visibile quando **[!UICONTROL Qty Uses Decimals]** è impostato solo su `Yes`.

1. Imposta **[!UICONTROL Backorders]** su uno dei seguenti:

   | Opzione | Descrizione |
   | ----- | ----- |
   | `No Backorders` | Non accettare ordini inevasi quando il prodotto è esaurito. |
   | `Allow Qty Below 0` | Accettare ordini inevasi quando la quantità scende al di sotto di zero. |
   | `Allow Qty Below 0 and Notify Customer` | Accettare ordini inevasi quando la quantità scende al di sotto di zero e avvisare il cliente che l&#39;ordine può ancora essere effettuato. |

   Per ulteriori informazioni, vedere [Configurazione degli ordini arretrati](backorders.md).

1. Per attivare incrementi di quantità per il prodotto, impostare **[!UICONTROL Enable Qty Increments]** su `Yes` e immettere il numero di articoli che devono essere acquistati per soddisfare il requisito nel campo **[!UICONTROL Qty Increments]**.

   Ad esempio, un articolo venduto con incrementi di sei può essere acquistato in quantità di 6, 12, 18 e così via.

   Il campo **[!UICONTROL Qty Increments]** imposta il numero di articoli prodotto da acquistare come singolo prodotto e come figlio di prodotti configurabili, raggruppati e raggruppati.

1. Al termine, fare clic su **[!UICONTROL Done]** e quindi su **[!UICONTROL Save]**.

### Descrizioni dei campi

| Campo | Ambito | Descrizione |
|--|--|--|
| [!UICONTROL Manage Stock] | Globale | Determina se il controllo dell&#39;inventario viene utilizzato per gestire questo prodotto nel catalogo. Impostato per abilitare o disabilitare tutte le funzionalità di [!DNL Inventory Management]. Quando si completa una restituzione o una nota di accredito, la quantità del prodotto viene automaticamente restituita alla quantità di origine interessata. Se si utilizza un sistema ERP di terze parti, potrebbe essere opportuno disattivarlo. |
| [!UICONTROL Out-of-Stock Threshold] | Globale | Determina il livello di scorte al quale un prodotto viene considerato esaurito. Opzioni:<br />Valore positivo - Con gli ordini inevasi disabilitati, immettere un importo positivo.<br />Zero (0) - Se sono abilitati gli ordini inevasi, l&#39;immissione di zero consente di creare ordini inevasi infiniti.<br />Valore negativo: se gli ordini inevasi sono abilitati, si consiglia di immettere un importo negativo. L&#39;importo viene aggiunto alla quantità di vendita. Ad esempio, immettere `-50` per consentire ordini fino a questo importo. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Globale | Determina il numero minimo di prodotti che possono essere acquistati in un singolo ordine. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Globale | Determina il numero massimo di prodotti che possono essere acquistati in un singolo ordine. |
| [!UICONTROL Qty Uses Decimals] | Globale | Determina se i clienti possono utilizzare un valore decimale anziché un numero intero quando inseriscono la quantità ordinata. Opzioni:<br />`Yes` - Consente di immettere valori come decimali anziché come numeri interi. I decimali sono adatti per i prodotti venduti in base a peso, volume o lunghezza.<br />`No` - Richiede l&#39;immissione di valori di quantità come numeri interi. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Globale | Determina se le parti del prodotto possono essere spedite separatamente. Questa opzione è visibile quando **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Globale | Determina la modalità di gestione degli ordini inevasi. Gli ordini inevasi non modificano lo stato di elaborazione dell&#39;ordine. I fondi vengono comunque autorizzati o acquisiti immediatamente al momento dell&#39;ordine, indipendentemente dal fatto che il prodotto sia in magazzino. I prodotti vengono spediti non appena diventano disponibili. Se questa opzione è abilitata, è consigliabile immettere un importo negativo per la soglia esaurita. Opzioni:<br/>`No Backorders` - Non accetta ordini inevasi quando il prodotto è esaurito.<br />`Allow Qty Below 0` - Accetta ordini inevasi quando la quantità scende sotto zero.<br />`Allow Qty Below 0 and Notify Customer` - Accetta ordini inevasi quando la quantità scende al di sotto di zero, ma notifica ai clienti che gli ordini possono ancora essere effettuati. |
| [!UICONTROL Enable Qty Increments] | Globale | Determina se il prodotto può essere venduto in incrementi di quantità. Gli incrementi impostano il numero di articoli da acquistare come singolo prodotto e come figlio di prodotti configurabili, raggruppati e in bundle. |

>[!NOTE]
>
>La semplice configurazione del prodotto sostituisce le configurazioni di prodotto configurabili per un prodotto specifico.
