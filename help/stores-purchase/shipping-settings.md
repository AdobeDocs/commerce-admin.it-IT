---
title: Impostazioni spedizione
description: Scopri come configurare le impostazioni di spedizione che definiscono il punto di origine e la politica di spedizione per il tuo Negozio.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Impostazioni spedizione

La configurazione di spedizione stabilisce il punto di origine per tutte le spedizioni, la politica di spedizione e la gestione delle spedizioni a più indirizzi.

## Punto di origine

Il punto di origine viene utilizzato per calcolare l&#39;addebito per le spedizioni effettuate dal negozio o dal magazzino e determina anche l&#39;aliquota fiscale per i prodotti venduti. Durante il calcolo [Imposte UE](international-tax-guidelines.md#eu-tax-configuration), assicurati che il [Calcolo destinazione imposta predefinita](../configuration-reference/sales/tax.md) per ogni visualizzazione store corrisponde al punto di origine Impostazioni spedizione.

![Origine](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Shipping Settings]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Origin]** e completare quanto segue:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (e riga 2, se necessario)

1. Clic **[!UICONTROL Save Config]**.

## Politica di spedizione

La politica di spedizione deve spiegare le regole commerciali e le linee guida aziendali relative alle spedizioni. Ad esempio, se disponi di regole di prezzo che attivano la spedizione gratuita, puoi spiegare i termini della tua politica di spedizione.

![Regole di spedizione durante il pagamento](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Per visualizzare le regole di spedizione durante il pagamento, completare la sezione Parametri delle regole di spedizione nella configurazione. Il testo viene visualizzato quando i clienti fanno clic su _Consulta la nostra politica di spedizione_ durante il pagamento.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Shipping Settings]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Shipping Policy Parameters]** sezione.

1. Imposta **[!UICONTROL Apply Custom Shipping Policy]** a `Yes`.

1. Incolla o immetti il **[!UICONTROL Shipping Policy]** nella casella di testo.

   >[!NOTE]
   >
   >Se si utilizza un elaboratore di testi per comporre il testo, assicurarsi di salvare il documento come file TXT per rimuovere eventuali caratteri di controllo dal testo. Copiare e incollare il testo nella casella di testo Politica di spedizione.

   ![Parametri criteri di spedizione](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.

## Più indirizzi

Le opzioni di spedizione con più indirizzi consentono ai clienti di spedire un ordine a più indirizzi durante il pagamento e di determinare il numero massimo di indirizzi a cui un ordine può essere spedito.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Multishipping Settings]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Options]** sezione.

   ![Opzioni di spedizione multiindirizzo](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Allow Shipping to Multiple Addresses]** a `Yes`.

1. Inserisci il **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Clic **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![B2B per Adobe Commerce](../assets/b2b.svg) (B2B per Adobe Commerce) Per gli ordini con più indirizzi di spedizione, il [Pagamento in acconto](../b2b/enable-basic-features.md#configure-payment-on-account) il metodo di pagamento, anche se abilitato, non è disponibile durante l&#39;estrazione.
