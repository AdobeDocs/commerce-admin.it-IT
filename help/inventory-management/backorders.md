---
title: Configura  [!DNL Inventory Management]  ordini inevasi
description: Scopri come configurare gli ordini inevasi per supportare la vendita di prodotti esauriti.
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

---

# Configura [!DNL Inventory Management] ordini arretrati

Gli ordini in inevaso consentono al tuo negozio di continuare a vendere prodotti una volta che la quantità raggiunge lo zero o che è effettivamente esaurita. Quando un ordine cliente è un ordine inevaso, i fondi vengono autorizzati e acquisiti immediatamente, lo stato di elaborazione dell&#39;ordine non cambia e la spedizione rimane in sospeso fino a quando non sono disponibili scorte.

A seconda del negozio e delle vendite, può essere opportuno abilitare o disabilitare gli ordini inevasi ai seguenti livelli:

- **[!UICONTROL Global]** - Tutti i prodotti nel catalogo a livello di sito

- **[!UICONTROL Product]** - Impostazioni di sostituzione prodotti specifici per sito, origine e stock

## Comprendere le impostazioni dell&#39;ordine arretrato

Si consiglia vivamente di configurare soglie e impostazioni specifiche per supportare al meglio gli ordini inevasi.

### Soglia scorte esaurite

Utilizza un valore negativo per questa soglia per impostare la quantità massima di prodotti che possono essere inevasi prima che il prodotto sia considerato esaurito. Questo importo viene aggiunto alla quantità vendibile. Il valore impostato a livello di prodotto sostituisce qualsiasi valore impostato a livello globale.

La formula per la quantità di vendita è `(Quantity - (Out-of-Stock Threshold))`.

Di seguito è riportato un esempio:

- Quantità: 25
- Notifica per quantità inferiore: 10
- Solo X soglia sinistra: 5
- Soglia esaurita: -50

La quantità disponibile per questo prodotto è `75 (25 - (-50))`.

![Quantità di vendita di esempio prima dell&#39;abilitazione degli ordini inevasi](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![Esempio di quantità vendibile dopo ordini inevasi abilitati](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

Quando i clienti acquistano i 25 prodotti disponibili, i nuovi ordini vengono inseriti come ordini inevasi. Poiché la quantità vendibile del prodotto si riduce a 5 (sono stati venduti 70 articoli), nella pagina _Prodotto_ viene visualizzato un messaggio `Only 5 left` nella vetrina. Quando la quantità vendibile raggiunge `0`, il prodotto viene visualizzato come `Out of Stock` nella vetrina.

>[!NOTE]
>
>Quando un cliente effettua un ordine utilizzando _[!UICONTROL backorder qty]_, [!DNL Inventory Management] sottrae automaticamente la quantità dalla quantità vendibile. Se un ordine non viene spedito e viene annullato, la quantità viene restituita alla quantità di vendita virtuale aggregata. La quantità dell&#39;ordine **_annullata non è assegnata ad alcuna origine_**, ma viene restituita al numero totale di prodotti disponibili per la vendita (colonna_[!UICONTROL Salable Quantity]_ nella griglia prodotti).

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### Stato del magazzino

I prodotti devono essere impostati sullo stato `In Stock` quando si abilitano gli ordini inevasi. È possibile impostare questo valore dalla pagina _Prodotto_. Per i commercianti multi-sorgente, è necessario che almeno un&#39;origine sia contrassegnata come `In Stock`. Accedi e imposta lo stato tramite la pagina _Prodotto_ e assegna _Origini_ alla griglia.

## Configurare gli ordini inevasi a livello globale

Questi passaggi abilitano gli ordini arretrati per tutti i prodotti a livello di sito.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Imposta **[!UICONTROL Store View]** su `Default Config`.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Inventory]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**.

1. Per **[!UICONTROL Backorders]**, deselezionare la casella di controllo **[!UICONTROL Use system value]** e selezionare un&#39;opzione:

   | Opzione | Descrizione |
   | -- | -- |
   | `No Backorders` | Non accettare ordini inevasi quando il prodotto è esaurito. |
   | `Allow Qty Below 0` | Accettare ordini inevasi quando la quantità scende al di sotto di zero. |
   | `Allow Qty Below 0 and Notify Customer` | Accettare ordini inevasi quando la quantità scende al di sotto di zero e avvisare il cliente che l&#39;ordine può ancora essere effettuato. |

1. Per **[!UICONTROL Out-of-Stock Threshold]**, deselezionare la casella di controllo **[!UICONTROL Use system value]** e immettere un valore diverso.

   | Valore | Descrizione |
   | -- | -- |
   | Importo positivo | Se l&#39;opzione Ordini arretrati è disattivata, immettere un valore positivo. |
   | Zero | Con gli ordini inevasi abilitati, l&#39;immissione di `0` consente ordini inevasi infiniti. |
   | Importo negativo | Se l&#39;opzione Ordini arretrati è abilitata, si consiglia di immettere un valore negativo. L&#39;importo viene aggiunto alla quantità di vendita. Ad esempio, immettere `-50` per consentire ordini fino a questo importo. |

1. Fare clic su **[!UICONTROL Save Config]**.

## Configurare gli ordini inevasi per un prodotto

Le configurazioni a livello di prodotto sovrascrivono le configurazioni globali. Puoi configurare gli ordini inevasi a livello di prodotto in modo da ignorare le impostazioni a livello di store globale o sorgente. Ad esempio, il tuo negozio potrebbe supportare a livello globale gli ordini inevasi. Con le impostazioni del prodotto, puoi disabilitare gli ordini inevasi o modificare la soglia esaurita senza influire su altri prodotti e origini.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Aprire un prodotto in modalità **[!UICONTROL Edit]** e scorrere la pagina fino all&#39;area _[!UICONTROL Sources]_.

   Per i prodotti configurati senza [!DNL Inventory Management], la scheda non viene visualizzata. Il pulsante `Advanced Inventory` viene visualizzato nel campo _[!UICONTROL Quantity]_.

1. Fare clic su **[!UICONTROL Advanced Inventory]**.

   Questa azione visualizza una pagina di configurazioni specifiche per il prodotto. Qualsiasi impostazione elencata come `global` visualizza l&#39;impostazione globale corrente per l&#39;archivio.

1. Per **[!UICONTROL Backorders]**, deselezionare la casella di controllo **[!UICONTROL Use Config Setting]** e selezionare un&#39;opzione:

   | Opzione | Descrizione |
   | -- | -- |
   | `No Backorders` | Non accettare ordini inevasi quando il prodotto è esaurito. |
   | `Allow Qty Below 0` | Accettare ordini inevasi quando la quantità scende al di sotto di zero. |
   | `Allow Qty Below 0 and Notify Customer` | Accettare ordini inevasi quando la quantità scende al di sotto di zero e avvisare il cliente che l&#39;ordine può ancora essere effettuato. |

1. Per **[!UICONTROL Out-of-Stock Threshold]**, deselezionare la casella di controllo **[!UICONTROL Use Config Setting]** e immettere un importo:

   | Valore | Descrizione |
   | -- | -- |
   | Importo positivo | Se l&#39;opzione Ordini arretrati è disattivata, immettere un valore positivo. |
   | Zero | Con gli ordini inevasi abilitati, l&#39;immissione di `0` consente ordini inevasi infiniti. |
   | Importo negativo | Se l&#39;opzione Ordini arretrati è abilitata, si consiglia di immettere un valore negativo. L&#39;importo viene aggiunto alla quantità di vendita. Ad esempio, immettere `-50` per consentire ordini fino a tale importo. |

   ![Inventario avanzato configurato per ordini inevasi](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Done]** e quindi su **[!UICONTROL Save]**.
