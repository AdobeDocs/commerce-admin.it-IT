---
title: Assegni e vaglia postali
description: Scopri come impostare assegni e vaglia postale come metodo di pagamento offline sul tuo Negozio.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
TQID: https://experienceleague.adobe.com/mmlEdLGANV93nvet3YwYoBGZKcft1qYuA6HboQ0Buvw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# Assegni e vaglia postali

Adobe Commerce e Magento Open Source consentono di accettare pagamenti tramite assegno o vaglia postale. Per impostazione predefinita, il metodo di pagamento _Assegno/Vaglia postale_ è abilitato per il tuo Negozio. È possibile accettare assegni e ordini di pagamento solo da paesi specifici e perfezionare la configurazione con limiti totali minimi e massimi per gli ordini.

**_Per configurare il pagamento tramite assegno o vaglia postale:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. In _[!UICONTROL Other Payment Methods]_, espandere ![Selettore di espansione](../assets/icon-display-expand.png) la sezione **[!UICONTROL Check / Money Order]**.

   ![Assegno/vaglia postale](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedere [Verifica / Vaglia postale](../configuration-reference/sales/payment-methods.md#check--money-order) nella _Guida di riferimento alla configurazione_.

   >[!NOTE]
   >
   >Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare le impostazioni.

1. Per accettare il pagamento tramite assegno o vaglia postale, impostare **[!UICONTROL Enabled]** su `Yes`.

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi il metodo di pagamento dell&#39;assegno o del vaglia postale durante l&#39;estrazione.

1. Se gli ordini in genere attendono l&#39;approvazione, accettare **[!UICONTROL New Order Status]** come `Pending"` predefinito fino all&#39;approvazione.

   Se si preferisce, è possibile utilizzare lo stato `Processing` o `Suspected Fraud` per i nuovi ordini con questo metodo di pagamento.

1. Imposta **[!UICONTROL Payment from Applicable Countries]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del tuo negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco _[!UICONTROL Payment from Specific Countries]_. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Per **[!UICONTROL Make Check Payable To]**, immettere il nome della parte a cui deve essere dovuto l&#39;assegno.

1. Per **[!UICONTROL Send Check To]**, immettere l&#39;indirizzo stradale o la casella postale in cui vengono inviati gli assegni.

1. Impostare **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** sugli importi degli ordini necessari per qualificarsi per questo metodo di pagamento.

   >[!NOTE]
   >
   >Un ordine è qualificato se il totale è compreso tra i valori totali minimi o massimi o corrisponde esattamente a tali valori.

1. Per **[!UICONTROL Sort Order]**, immettere un numero che determini la posizione di questo elemento nell&#39;elenco dei metodi di pagamento visualizzato durante l&#39;estrazione.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = primo, `1` = secondo, `2` = terzo e così via).

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
