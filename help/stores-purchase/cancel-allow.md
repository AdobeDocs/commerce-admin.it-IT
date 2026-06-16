---
title: Consenti annullamento ordine
description: Scopri come fornire ai clienti le funzionalità di annullamento.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
TQID: https://experienceleague.adobe.com/a0jMKgF4a0qXUe15oT2syai6-kGSegU1BX56PO9SSKs
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-wordcount: 291
ht-degree: 0%

---

# Consenti annullamento ordine

Se questa opzione è abilitata, puoi annullare un ordine direttamente dal conto del cliente. Annulla è disattivato per impostazione predefinita.

## Criteri per abilitare l’annullamento per un ordine

- L&#39;opzione di configurazione _Consenti annullamento ordine_ deve essere abilitata.

- Se l&#39;ordine è nello stato `Hold`, `Canceled`, `Complete` o `Closed`, l&#39;opzione di annullamento è disabilitata nella vetrina.

- Se uno degli articoli dell&#39;ordine è stato spedito, l&#39;opzione di annullamento è disabilitata nella vetrina.

- Se è stato pagato un articolo, l&#39;opzione di annullamento è abilitata e il rimborso viene creato per tale articolo.

- Se l&#39;ordine è nello stato `Pending` o `Processing`, l&#39;opzione di annullamento è abilitata nella vetrina.

## Configura per consentire l’annullamento del cliente e personalizzarne i motivi

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e seleziona **[!UICONTROL Sales]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Order cancellation]**.

   ![Opzioni di annullamento ordine](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Order cancellation through GraphQL]** su `Yes`.

   Questa impostazione abilita la funzionalità di annullamento dall’account del cliente nella vetrina.

1. In **[!UICONTROL Order Order cancellation reasons]** è possibile aggiungere, eliminare o modificare qualsiasi motivo di annullamento.

   Con questa impostazione, i motivi di annullamento vengono visualizzati sul vetrina al cliente quando annulla un ordine.
Assicurati di aver specificato almeno un motivo.

1. Fare clic su **[!UICONTROL Save Config]**.

## Annulla dalla vetrina

Il cliente può avviare la funzionalità di annullamento per un ordine specifico da tre pagine:

- _I miei ordini_ pagina

- _Visualizzazione ordine_ pagina

- _Pagina Il mio account_

### I miei ordini

Il pulsante _Annulla ordine_ viene visualizzato nella pagina Ordini personali se è possibile annullare l&#39;ordine.

![Esempio di vetrina: pagina I miei ordini](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Pagina di visualizzazione ordine

Se l&#39;ordine può essere annullato, nella pagina Visualizza ordine viene visualizzato il pulsante _Annulla ordine_.

![Pagina dettagli ordine](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Il mio account

Il pulsante _Annulla ordine_ viene visualizzato nella sezione Ordini recenti della pagina Il mio account, se l&#39;ordine può essere annullato.

![Pagina del mio account](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
