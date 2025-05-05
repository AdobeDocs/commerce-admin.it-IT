---
title: Spedizione gratuita
description: Scopri come impostare un’opzione di spedizione gratuita per il tuo negozio.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Spedizione gratuita

_La spedizione gratuita_ è una delle promozioni più efficaci che puoi offrire. Può essere basato su un acquisto minimo o impostato come [regola prezzo carrello](../merchandising-promotions/price-rules-cart.md) applicata quando viene soddisfatta una serie di condizioni. Se entrambi si applicano allo stesso ordine, l’impostazione di configurazione ha la precedenza sulla regola del carrello.

>[!NOTE]
>
>Controlla la configurazione del vettore di spedizione per eventuali impostazioni aggiuntive necessarie per la spedizione gratuita.

## Passaggio 1: configurare la spedizione gratuita

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Delivery Methods]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Free Shipping]**.

   >[!NOTE]
   >
   >Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare le impostazioni seguenti come descritto.

1. Imposta **[!UICONTROL Enabled]** su `Yes`.

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi il metodo di spedizione gratuita durante il pagamento e un **[!UICONTROL Method Name]** per descriverlo.

1. Per **[!UICONTROL Minimum Order Amount]**, immettere il valore totale minimo idoneo per la spedizione gratuita.

   >[!TIP]
   >
   >Per utilizzare la spedizione gratuita con [tariffe di tabella](shipping-table-rate.md), impostare _[!UICONTROL Minimum Order Amount]_&#x200B;su un valore talmente alto da non essere mai raggiunto. L&#39;utilizzo di questo valore elevato impedisce l&#39;applicazione della spedizione gratuita, a meno che non venga attivata da una regola di prezzo.

1. Imposta **[!UICONTROL Include Tax to Amount]**:

   - `Yes` - Include l&#39;imposta durante il calcolo dell&#39;importo minimo dell&#39;ordine (Subtotale + Imposta - Sconto).
   - `No` - Non include l&#39;imposta durante il calcolo dell&#39;importo minimo dell&#39;ordine (Subtotale - Sconto).

   ![Spedizione gratuita](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Displayed Error Message]**, immettere il messaggio da visualizzare se la spedizione gratuita non è disponibile.

1. Imposta **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione dell&#39;archivio possono utilizzare la spedizione gratuita.

   - `Specific Countries` - Dopo aver scelto questo valore, viene visualizzato l&#39;elenco _[!UICONTROL Ship to Specific Countries]_. Selezionare ogni paese nell&#39;elenco in cui è possibile utilizzare la spedizione gratuita.

1. Imposta **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Mostra sempre il metodo di spedizione gratuita, anche quando non applicabile.
   - `No` - Mostra il metodo di spedizione gratuita solo se applicabile.

1. Per **[!UICONTROL Sort Order]**, immettere il numero che determina la posizione della spedizione gratuita nell&#39;elenco dei metodi di consegna durante l&#39;estrazione.

   `0` = primo, `1` = secondo, `2` = terzo e così via.

1. Fare clic su **[!UICONTROL Save Config]**.

## Passaggio 2: abilitare la spedizione gratuita nella configurazione del vettore

Assicurati di completare tutte le configurazioni necessarie per ogni vettore che intendi utilizzare per la spedizione gratuita. Se, ad esempio, la configurazione del [gruppo di continuità](ups.md) è stata completata, aggiornare le impostazioni seguenti per abilitare e configurare la spedizione gratuita.

1. Nella configurazione _[!UICONTROL Delivery Methods]_, espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL UPS]**.

1. Impostare **[!UICONTROL Free Method]** su `UPS Ground` o un altro tipo che si desidera designare per la spedizione gratuita.

1. Per richiedere un ordine minimo per la spedizione gratuita, impostare **[!UICONTROL Enable Free Shipping Threshold]** su `Enable`.

   Se si sceglie di utilizzare un ordine minimo, immettere l&#39;importo richiesto per **[!UICONTROL Free Shipping Amount Threshold]**.

1. Fare clic su **[!UICONTROL Save Config]**.
