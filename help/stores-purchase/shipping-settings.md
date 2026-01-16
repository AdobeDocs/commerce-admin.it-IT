---
title: Impostazioni spedizione
description: Scopri come configurare le impostazioni di spedizione che definiscono il punto di origine e la politica di spedizione per il tuo Negozio.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 0%

---

# Impostazioni spedizione

La configurazione di spedizione stabilisce il punto di origine per tutte le spedizioni, la politica di spedizione e la gestione delle spedizioni a più indirizzi.

## Punto di origine

Il punto di origine viene utilizzato per calcolare l&#39;addebito per le spedizioni effettuate dal negozio o dal magazzino e determina anche l&#39;aliquota fiscale per i prodotti venduti. Durante il calcolo di [imposte UE](international-tax-guidelines.md#eu-tax-configuration), assicurati che il [calcolo della destinazione imposta predefinita](../configuration-reference/sales/tax.md) per ogni visualizzazione dello store corrisponda al punto di origine delle impostazioni di spedizione.

![Origine](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Shipping Settings]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Origin]** e completare le operazioni seguenti:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (e riga 2, se necessario)

1. Fare clic su **[!UICONTROL Save Config]**.

## Politica di spedizione

La politica di spedizione deve spiegare le regole commerciali e le linee guida aziendali relative alle spedizioni. Ad esempio, se disponi di regole di prezzo che attivano la spedizione gratuita, puoi spiegare i termini della tua politica di spedizione.

![Regole di spedizione durante l&#39;estrazione](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Per visualizzare le regole di spedizione durante il pagamento, completare la sezione Parametri delle regole di spedizione nella configurazione. Il testo viene visualizzato quando i clienti fanno clic su _Consulta i nostri criteri di spedizione_ durante l&#39;estrazione.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Shipping Settings]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Shipping Policy Parameters]**.

1. Imposta **[!UICONTROL Apply Custom Shipping Policy]** su `Yes`.

1. Incolla o immetti **[!UICONTROL Shipping Policy]** nella casella di testo.

   >[!NOTE]
   >
   >Se si utilizza un elaboratore di testi per comporre il testo, assicurarsi di salvare il documento come file TXT per rimuovere eventuali caratteri di controllo dal testo. Copiare e incollare il testo nella casella di testo Politica di spedizione.

   ![Parametri criteri di spedizione](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Save Config]**.

## Più indirizzi

Le opzioni di spedizione con più indirizzi consentono ai clienti di spedire un ordine a più indirizzi durante il pagamento e di determinare il numero massimo di indirizzi a cui un ordine può essere spedito.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Multishipping Settings]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Options]**.

   ![Opzioni di spedizione multiindirizzo](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Allow Shipping to Multiple Addresses]** su `Yes`.

1. Immettere **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Fare clic su **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B) Per gli ordini con più indirizzi di spedizione, il metodo di pagamento [Pagamento sull&#39;account](../b2b/enable-basic-features.md#configure-payment-on-account), anche se abilitato, non è disponibile durante l&#39;estrazione.

## URL di tracciamento spedizione e-mail

[!BADGE Solo SaaS]{type=Positive url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce as a Cloud Service (infrastruttura SaaS gestita da Adobe)."}

[!BADGE Sandbox]{type=Caution tooltip="Gli elementi elencati sono attualmente disponibili solo negli ambienti Sandbox. Adobe rende disponibili le nuove versioni negli ambienti Sandbox per consentire di testare le modifiche imminenti prima che siano disponibili negli ambienti di produzione."}

Per impostazione predefinita, i numeri di registrazione delle spedizioni inviati nelle e-mail dei clienti sono in testo normale. Puoi convertire questi numeri di tracciamento in collegamenti cliccabili abilitando la funzione URL di tracciamento personalizzato. Questa funzione ti consente di definire un modello per il tracciamento degli URL di vari vettori di spedizione. Ogni modello include l’URL completo del sito web di tracciamento e un segnaposto per il numero di tracciamento. Commerce sostituisce il segnaposto con il numero di tracciamento effettivo nell’e-mail.

Sono supportati i seguenti vettori di spedizione:

- Servizio postale degli Stati Uniti (USPS)
- United Parcel Service (UPS)
- Federal Express (FedEx)
- DHL Express (DHL)

Per abilitare o modificare gli URL di tracciamento personalizzati:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Shipping Settings]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Shipment Tracking URLs]**.

1. Imposta **[!UICONTROL Enable Custom Tracking URLs]** su `Yes`.

1. Vengono forniti modelli URL predefiniti per ogni gestore supportato. Se devi modificare uno di questi valori, inserisci un nuovo modello URL nel campo corrispondente. Utilizza `{{tracking_number}}` come segnaposto per il numero di tracciamento effettivo. Se, ad esempio, UPS modifica il proprio URL in `https://www.ups.com/newtracker?tracknumber`, il nuovo modello di URL di tracciamento potrebbe essere simile al seguente:

   ```text
   https://www.ups.com/newtracker?tracknumber={{tracking_number}}
   ```

1. Fare clic su **[!UICONTROL Save Config]**.
