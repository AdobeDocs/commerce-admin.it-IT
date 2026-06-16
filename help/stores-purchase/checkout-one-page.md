---
title: Pagamento di una pagina
description: Scopri come offrire un processo di pagamento semplificato per il tuo negozio.
exl-id: c91347b6-bb6f-44e7-b470-f237bf430d5f
feature: Checkout
TQID: https://experienceleague.adobe.com/rY0sw7iSq7-4Y5EPQ1cL8bJ7cuqdDfDqvjEQvH-jsvM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
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
source-wordcount: 181
ht-degree: 0%

---

# Pagamento di una pagina

Lo scopo del pagamento di una pagina è quello di raccogliere le informazioni necessarie e completare la vendita il più rapidamente possibile senza richiedere clic aggiuntivi per l&#39;acquirente. Quando è abilitata l’estrazione di una pagina, l’intero processo di estrazione si svolge su una singola pagina. Ogni sezione delle informazioni di pagamento viene espansa in base alle esigenze.

Il pagamento di una pagina è abilitato per impostazione predefinita. Se implementi un’integrazione personalizzata o un’estensione di pagamento, potrebbe essere necessario disattivare il Check-Out di una pagina.

**_Per disattivare l&#39;estrazione di una pagina:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Checkout Options]**.

   ![Configurazione - Opzioni di estrazione](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedere [Opzioni di estrazione](../configuration-reference/sales/checkout.md#checkout-options) nella _Guida di riferimento alla configurazione_.

1. Se l&#39;impostazione è per una visualizzazione archivio specifica, [scegliere la visualizzazione archivio](../configuration-reference/scope-change.md#set-the-scope) in cui si applica la configurazione.

   Quando richiesto, fare clic su **[!UICONTROL OK]** per continuare.

1. Imposta **[!UICONTROL Enable Onepage Checkout]** su `No`.

   Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare questa impostazione.

1. Fare clic su **[!UICONTROL Save Config]**.
