---
title: Configurare i resi
description: Scopri come abilitare le restituzioni per il tuo archivio e configurare i metodi di spedizione supportati.
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# Configurare i resi

{{ee-feature}}

Quando questa opzione è abilitata, le richieste RMA possono essere inviate dai clienti dalla vetrina. Un RMA può essere generato solo se nell&#39;ordine è presente un articolo disponibile per la restituzione. Le richieste di restituzione di singoli elementi vengono gestite dal _Abilita RMA_ in ciascun record di prodotto. Per impostazione predefinita, le impostazioni di configurazione vengono applicate al prodotto (_[!UICONTROL Use Config Settings]_è selezionato). Se_[!UICONTROL Enable RMA]_ è impostato su `No`, il prodotto non viene visualizzato nell’elenco degli elementi disponibili per la restituzione. Se si modifica il _Abilita RMA_ , si applica sia agli ordini nuovi che a quelli esistenti.

## Abilita RMA per lo store

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL RMA Settings]** sezione.

   ![Impostazioni RMA](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enable RMA on Storefront]** a `Yes`.

   Questa impostazione determina se i clienti possono creare e visualizzare richieste RMA dalla vetrina. Le RMA possono essere applicate sia agli ordini nuovi che a quelli esistenti.

1. Imposta **[!UICONTROL Enable RMA on Product Level]** a `Yes`.

   Questa impostazione determina il comportamento della _Abilita RMA_ attributo per singoli prodotti sulla vetrina:

   - Quando [!UICONTROL Enable RMA on Product Level] è impostato su `Yes`, i clienti della vetrina possono restituire tutti i singoli prodotti. Include entrambi _[!UICONTROL Enable RMA]_= `Yes` e_[!UICONTROL Enable RMA]_ = `No` valori degli attributi del prodotto.
   - Quando [!UICONTROL Enable RMA on Product Level] è impostato su `No`, i clienti della vetrina possono restituire solo i prodotti con un _[!UICONTROL Enable RMA]_= `Yes` valore dell’attributo del prodotto.

1. Imposta **[!UICONTROL Use Store Address]** a uno dei seguenti valori:

   - `Yes` - Inviare i prodotti restituiti all&#39;indirizzo del negozio.
   - `No` - Immettere un indirizzo alternativo per le restituzioni di prodotti.

   ![Impostazioni RMA con indirizzo alternativo](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.

## Configura i metodi di spedizione per le restituzioni

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Delivery Methods]**.

1. Espandere la sezione relativa al vettore che si desidera utilizzare per il servizio di restituzione, ad esempio **[!UICONTROL UPS]**.

   ![Abilita servizio RMA per gestore](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enabled for RMA]** a `Yes`.

1. Clic **[!UICONTROL Save Config]**.

## Modificare le RMA consentite a livello di prodotto

Se si attivano le RMA per il negozio e il catalogo contiene alcuni prodotti che non dovrebbero essere restituiti, è possibile modificare l&#39;impostazione a livello di prodotto,

1. Apri il prodotto in modalità di modifica.

1. Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Autosettings]** sezione.

1. Cancella **[!UICONTROL Use Config Setting]** se necessario.

1. Attiva/disattiva **[!UICONTROL Enable RMA]** impostazione su `No`.

   ![Disattivazione di RMA per un prodotto](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save]**.
