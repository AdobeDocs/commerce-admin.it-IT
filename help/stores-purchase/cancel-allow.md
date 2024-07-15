---
title: Consenti annullamento ordine
description: Scopri come fornire ai clienti le funzionalità di annullamento.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
source-git-commit: a9d1dc4fe50e98f0f1dfc8ec204930e2cc885d6e
workflow-type: tm+mt
source-wordcount: '300'
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
