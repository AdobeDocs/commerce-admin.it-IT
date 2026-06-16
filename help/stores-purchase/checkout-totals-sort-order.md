---
title: Ordinamento per i totali di pagamento
description: Scopri il totale di pagamento visualizzato e come configurare l’ordinamento dei totali di pagamento nel riepilogo dell’ordine.
exl-id: 2b1345e3-6ad3-472a-af3e-3f7b24577b13
feature: Checkout, Configuration
TQID: https://experienceleague.adobe.com/cXt3dbS5Jd8baKFk8K8HP1Cypk1oMS85iCq-WZ8cIgg
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
source-wordcount: 257
ht-degree: 0%

---

# Ordinamento per i totali di pagamento

Durante la revisione dell&#39;ordine, il totale viene visualizzato nella parte inferiore dell&#39;ordine, con eventuali adeguamenti per sconti, spese di spedizione, credito di magazzino e imposte. L&#39;ordine di ciascun elemento determina la sequenza dei calcoli e viene impostato nella configurazione da un numero assegnato a ciascun elemento. Ad esempio, il Subtotale è il primo elemento della sezione e gli viene assegnato il valore 10. Il Totale complessivo viene visualizzato per ultimo e gli viene assegnato il valore 100. A tutti gli altri elementi della sezione Totali viene assegnato un valore compreso tra tali valori.

![Riepilogo ordini visualizza il totale di pagamento](./assets/storefront-checkout-totals.png){width="700" zoomable="yes"}

**_Per configurare l&#39;ordinamento dei totali di estrazione:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi la sezione **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Checkout Totals Sort Order]**.

   ![Opzioni di estrazione totali numerate per determinare l&#39;ordinamento](../configuration-reference/sales/assets/sales-checkout-totals-sort-order.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedere [Ordinamento dei totali di estrazione](../configuration-reference/sales/sales.md#checkout-totals-sort-order) nella _Guida di riferimento alla configurazione_.

1. Se l&#39;impostazione è per una visualizzazione archivio specifica, [scegliere la visualizzazione archivio](../configuration-reference/scope-change.md#set-the-scope) in cui si applica la configurazione.

   Quando richiesto, fare clic su **[!UICONTROL OK]** per continuare.

1. Per determinare l&#39;ordine nella sezione _Totali_, modificare il numero assegnato a ogni elemento.

   Più basso è il valore, più precoce sarà la posizione nell&#39;elenco. Nella configurazione predefinita, il subtotale (`10`) è il primo e il totale complessivo (`100`) è l&#39;ultimo.

   Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per completare le modifiche.

1. Fare clic su **[!UICONTROL Save Config]**.
