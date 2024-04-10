---
title: Consenti annullamento ordine
description: Scopri come fornire ai clienti le funzionalità di annullamento.
feature: Orders, Storefront
source-git-commit: 613c081c02dd9b5e55de37dccd021af4e429d424
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Consenti annullamento ordine

Se questa opzione è abilitata, puoi annullare un ordine direttamente dal conto del cliente. Annulla è disattivato per impostazione predefinita.

## Criteri per abilitare l’annullamento per un ordine

- Il _Consenti annullamento ordine_ l&#39;opzione di configurazione deve essere abilitata.

- Se l&#39;ordine è in `Hold`, `Canceled`, `Complete`, o `Closed` stato, l&#39;opzione di annullamento è disabilitata nella vetrina.

- Se uno degli articoli dell&#39;ordine è stato spedito, l&#39;opzione di annullamento è disabilitata nella vetrina.

- Se è stato pagato un articolo, l&#39;opzione di annullamento è abilitata e il rimborso viene creato per tale articolo.

- Se l&#39;ordine è in `Pending` o `Processing` stato, l&#39;opzione di annullamento è abilitata nella vetrina.

## Configura per consentire l’annullamento del cliente e personalizzarne i motivi

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e seleziona **[!UICONTROL Sales]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Order cancellation]** sezione.

   ![Opzioni di annullamento ordine](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Order cancellation through GraphQL]** a `Yes`.

   Questa impostazione abilita la funzionalità di annullamento dall’account del cliente nella vetrina.

1. In **[!UICONTROL Order Order cancellation reasons]** puoi aggiungere, eliminare o modificare qualsiasi motivo di annullamento.

   Con questa impostazione, i motivi di annullamento vengono visualizzati sul vetrina al cliente quando annulla un ordine.
Assicurati di aver specificato almeno un motivo.

1. Clic **[!UICONTROL Save Config]**.

## Annulla dalla vetrina

Il cliente può avviare la funzionalità di annullamento per un ordine specifico da tre pagine:

- _I miei ordini_ pagina

- _Vista ordine_ pagina

- _Il mio account_ pagina

### I miei ordini

Il _Annulla ordine_ viene visualizzato nella pagina Ordini personali se l&#39;ordine può essere annullato.

![Esempio di vetrina: pagina I miei ordini](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Pagina di visualizzazione ordine

Il _Annulla ordine_ viene visualizzato nella pagina Visualizza ordine se l&#39;ordine può essere annullato.

![Pagina dettagli ordine](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Il mio account

Il _Annulla ordine_ viene visualizzato nella sezione Ordini recenti della pagina Account personale, se l&#39;ordine può essere annullato.

![Pagina Il mio account](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}


