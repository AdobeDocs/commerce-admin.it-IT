---
title: "Configura [!DNL Inventory Management] opzioni di prodotto"
description: Scopri come configurare [!DNL Inventory Management] opzioni di configurazione del prodotto.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# Configura [!DNL Inventory Management] opzioni prodotto

Queste configurazioni si applicano solo al prodotto modificato, ignorando tutte le configurazioni a livello di sito web globale. Modifica queste impostazioni durante la modifica di un prodotto, tramite _[!UICONTROL Sources]_sezione e_[!UICONTROL Advanced Inventory]_ pagina.

- Configurare le opzioni prodotto per origine
- Configurare le opzioni prodotto per l’inventario avanzato

## Opzioni prodotto per origine

Configurare le quantità e le impostazioni aggiuntive per [origine aggiunta](sources-add.md) per il prodotto.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Apri un prodotto in modalità di modifica.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Sources]** e configurare le impostazioni del prodotto per ogni origine:

   - Immetti un **[!UICONTROL Qty]** (quantità) importo.

   - Imposta il **[!UICONTROL Source Item Status]** as `In Stock` o `Out of Stock`.

   - Per modificare la notifica per la quantità inferiore per origine, deselezionare o selezionare la **[!UICONTROL Notify Quantity Use Default]** casella di controllo.

     Se liquidato, inserire l&#39;importo a livello di magazzino che attiva la notifica di esaurimento scorte dell&#39;articolo. L&#39;importo inserito viene sottratto dalla quantità di vendita dell&#39;articolo a livello di magazzino.

     `Select to use Default` - [!DNL Commerce] controlla le opzioni di Inventario avanzato del prodotto per le impostazioni di configurazione.
     `Clear to Modify` - Inserire un valore per la quantità di notifica, sostituendo le impostazioni di configurazione avanzate di magazzino e magazzino.

   ![Sezione Sorgenti per un prodotto](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Done]**, quindi **[!UICONTROL Save]**.

### Descrizioni dei campi

| Campo | Ambito | Descrizione |
|--|--|--|
| [!UICONTROL Source Code] | Globale | Il codice univoco di un [sorgente](sources-manage.md). |
| [!UICONTROL Name] | Globale | Nome univoco di un&#39;origine. |
| [!UICONTROL Status] | Globale | Il prodotto è abilitato o disabilitato nel catalogo. |
| [!UICONTROL Source Item Status] | Globale | Determina la disponibilità corrente del prodotto. Opzioni:<br />`In Stock` - Rende il prodotto disponibile per l&#39;acquisto.<br />`Out of Stock` - A meno che non siano attivati gli ordini inevasi, impedisce che il prodotto sia disponibile per l&#39;acquisto e rimuove l&#39;inserzione dal catalogo. |
| [!UICONTROL Qty] | Globale | Quantità di scorte disponibili per ogni origine o ubicazione. |
| [!UICONTROL Notify Quantity] | Globale | Un importo per _[!UICONTROL Notify for Quantity Below]_per questa origine specifica se_[!UICONTROL Notify Quantity Use Default]_ non è selezionato. |
| [!UICONTROL Notify Quantity Use Default] | Globale | Indica di utilizzare l’impostazione predefinita per _[!UICONTROL Notify for Quantity Below]_nel prodotto_[!UICONTROL Advanced Inventory]_ o globale nella configurazione dell’archivio. |

## Opzioni di prodotto avanzate

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Apri un prodotto in modalità di modifica.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Sources]** e fai clic su **[!UICONTROL Advanced Inventory]**.

1. Per abilitare [controllo di inventario](enable.md) per il catalogo, imposta **[!UICONTROL Manage Stock]** a `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] le impostazioni nei prodotti secondari sovrascrivono un prodotto configurabile.

   ![Inventario avanzato per un prodotto](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Immetti un importo per **[!UICONTROL Out-of-Stock Threshold]**:

   | Valore | Descrizione |
   | ----- | ----- |
   | Importo positivo | Con _[!UICONTROL Backorders]_disattivato, inserisci un valore positivo. |
   | Zero | Con _[!UICONTROL Backorders]_abilitato, immissione `0` consente ordini inevasi infiniti. |
   | Importo negativo | Con _[!UICONTROL Backorders]_attivato, si consiglia di immettere un valore negativo. L&#39;importo viene aggiunto alla quantità di vendita. Ad esempio, immetti `-50` per consentire ordini fino a questo importo. |

1. Inserisci il **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. Inserisci il **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. Imposta **[!UICONTROL Qty uses Decimals]** a `Yes` se i clienti possono utilizzare un valore decimale anziché un numero intero quando inseriscono la quantità ordinata.

1. Imposta **[!UICONTROL Allow Multiple Boxes for Shipping]** a `Yes` se il prodotto può essere venduto separatamente, in più scatole. Questa opzione è visibile quando **[!UICONTROL Qty Uses Decimals]** è impostato su `Yes` solo.

1. Imposta **[!UICONTROL Backorders]** a uno dei seguenti elementi:

   | Opzione | Descrizione |
   | ----- | ----- |
   | `No Backorders` | Non accettare ordini inevasi quando il prodotto è esaurito. |
   | `Allow Qty Below 0` | Accettare ordini inevasi quando la quantità scende al di sotto di zero. |
   | `Allow Qty Below 0 and Notify Customer` | Accettare ordini inevasi quando la quantità scende al di sotto di zero e avvisare il cliente che l&#39;ordine può ancora essere effettuato. |

   Per ulteriori informazioni, consulta [Configurazione degli ordini arretrati](backorders.md).

1. Per attivare gli incrementi di quantità per il prodotto, impostare **[!UICONTROL Enable Qty Increments]** a `Yes` e inserire il numero di articoli che devono essere acquistati per soddisfare il fabbisogno nel **[!UICONTROL Qty Increments]** campo.

   Ad esempio, un articolo venduto con incrementi di sei può essere acquistato in quantità di 6, 12, 18 e così via.

   **[!UICONTROL Qty Increments]** Questo campo imposta quanti articoli di prodotto devono essere acquistati come singolo prodotto e come figlio di prodotti configurabili, raggruppati e in bundle.

1. Al termine, fai clic su **[!UICONTROL Done]** e poi **[!UICONTROL Save]**.

### Descrizioni dei campi

| Campo | Ambito | Descrizione |
|--|--|--|
| [!UICONTROL Manage Stock] | Globale | Determina se il controllo dell&#39;inventario viene utilizzato per gestire questo prodotto nel catalogo. Imposta per abilitare o disabilitare tutti [!DNL Inventory Management] funzioni. Quando si completa una restituzione o una nota di accredito, la quantità del prodotto viene automaticamente restituita alla quantità di origine interessata. Se si utilizza un sistema ERP di terze parti, potrebbe essere opportuno disattivarlo. |
| [!UICONTROL Out-of-Stock Threshold] | Globale | Determina il livello di scorte al quale un prodotto viene considerato esaurito. Opzioni:<br />Valore positivo: con gli ordini inevasi disabilitati, immettere un importo positivo.<br />Zero (0) - Con ordini inevasi abilitati, l&#39;inserimento di zero consente ordini inevasi infiniti.<br />Valore negativo: con gli ordini inevasi abilitati, si consiglia di immettere un importo negativo. L&#39;importo viene aggiunto alla quantità di vendita. Ad esempio, immetti `-50` per consentire ordini fino a questo importo. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Globale | Determina il numero minimo di prodotti che possono essere acquistati in un singolo ordine. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Globale | Determina il numero massimo di prodotti che possono essere acquistati in un singolo ordine. |
| [!UICONTROL Qty Uses Decimals] | Globale | Determina se i clienti possono utilizzare un valore decimale anziché un numero intero quando inseriscono la quantità ordinata. Opzioni:<br />`Yes` - Consente di immettere i valori come decimali anziché come numeri interi. I decimali sono adatti per i prodotti venduti in base a peso, volume o lunghezza.<br />`No` - Richiede l&#39;immissione di valori di quantità come numeri interi. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Globale | Determina se le parti del prodotto possono essere spedite separatamente. Questa opzione è visibile quando **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Globale | Determina la modalità di gestione degli ordini inevasi. Gli ordini inevasi non modificano lo stato di elaborazione dell&#39;ordine. I fondi vengono comunque autorizzati o acquisiti immediatamente al momento dell&#39;ordine, indipendentemente dal fatto che il prodotto sia in magazzino. I prodotti vengono spediti non appena diventano disponibili. Se questa opzione è abilitata, è consigliabile immettere un importo negativo per la soglia esaurita. Opzioni:<br/>`No Backorders` - Non accetta ordini inevasi quando il prodotto è esaurito.<br />`Allow Qty Below 0` - Accetta ordini inevasi quando la quantità scende sotto zero.<br />`Allow Qty Below 0 and Notify Customer` - Accetta ordini inevasi quando la quantità scende al di sotto di zero, ma notifica ai clienti che gli ordini possono ancora essere effettuati. |
| [!UICONTROL Enable Qty Increments] | Globale | Determina se il prodotto può essere venduto in incrementi di quantità. Gli incrementi impostano il numero di articoli da acquistare come singolo prodotto e come figlio di prodotti configurabili, raggruppati e in bundle. |

>[!NOTE]
>
>La semplice configurazione del prodotto sostituisce le configurazioni di prodotto configurabili per un prodotto specifico.
