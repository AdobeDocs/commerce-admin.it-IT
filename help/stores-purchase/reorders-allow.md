---
title: Consenti riordini
description: Scopri come fornire ai clienti funzionalità di riordino.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Consenti riordini

Quando questa opzione è abilitata, è possibile effettuare i riordini direttamente dall&#39;account cliente o dall&#39;ordine originale in _Amministratore_. I riordini sono attivati per impostazione predefinita.

![Collegamento per riordinare il cliente nell&#39;amministratore](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Criteri per l&#39;abilitazione del riordino per un ordine

- L&#39;opzione di configurazione _Consenti riordino_ deve essere abilitata.

- Se l&#39;ordine è nello stato `Hold` o `Payment Review`, l&#39;opzione di riordino è disabilitata.

- Se uno degli elementi nell&#39;ordine non è disponibile, non è disponibile o è disattivato, l&#39;opzione di riordino è disattivata nella vetrina.

- Un _Amministratore_ può riordinare anche se uno degli elementi è esaurito o disabilitato.

## Configura per consentire riordini cliente

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Reorder]**.

   ![Opzioni di riordino](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Allow Reorder]** su `Yes`.

   Questa impostazione abilita la funzionalità di riordino dal conto cliente nella vetrina o nell&#39;elenco degli ordini in Admin.

1. Fare clic su **[!UICONTROL Save Config]**.

## Riordina dalla vetrina

Un cliente può avviare la funzionalità di riordino per un ordine specifico da due pagine:

- _I miei ordini_ pagina

- _Visualizzazione ordine_ pagina

### I miei ordini

Il pulsante _Riordina_ è sempre visualizzato nell&#39;elenco con Ordini (anche se tutti i prodotti dell&#39;ordine non sono disponibili per il riordino).

![Esempio di vetrina: pagina I miei ordini](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Caso 1.** Tutti i prodotti dell&#39;ordine sono **disponibili** per il riordino

L’utente viene reindirizzato al carrello e tutti i prodotti vengono aggiunti al carrello

![Carrello acquisti](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Caso 2.** Alcuni/tutti i prodotti dell&#39;ordine sono **non disponibili** per il riordino

>[!NOTE]
>
>È possibile riordinare `Not Visible Individually` prodotti.

Il pulsante _Riordina_ non viene visualizzato nelle pagine _I miei ordini_ e _Visualizza ordine_.

![Ordini personali pagina 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Pagina di visualizzazione ordine

**Caso 1.** Tutti i prodotti dell&#39;ordine sono disponibili per il riordino

L’utente viene reindirizzato al carrello e tutti i prodotti vengono aggiunti al carrello

**Caso 2.** Alcuni/tutti i prodotti dell&#39;ordine sono **non disponibili** per il riordino

>[!NOTE]
>
>È possibile riordinare `Not Visible Individually` prodotti.

Il pulsante _Riordina_ non viene visualizzato nelle pagine _I miei ordini_ e _Visualizza ordine_.

![Pagina dettagli ordine](./assets/order-view-page.png){width="700" zoomable="yes"}

### Il carrello non è vuoto

Se il carrello non è vuoto e l&#39;utente fa clic su **[!UICONTROL Reorder]** (dalla pagina _I miei ordini_ o _Visualizzazione ordine_), i prodotti esistenti rimangono nel carrello con i prodotti di riordino aggiunti.

![Riordina elementi](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Riordina dall’Amministratore

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Individuare l&#39;ordine e aprire in modalità **[!UICONTROL View]**.

1. Fare clic su **[!UICONTROL Reorder]** che viene visualizzato nella barra dei pulsanti superiore.

   ![Dettagli ordine nell&#39;amministratore](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Dopo aver fatto clic su **[!UICONTROL Reorder]**, viene aperta la pagina _Crea nuovo ordine_ con i prodotti di riordino.

   ![Crea riordino](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Completa tutti i campi obbligatori in base alle esigenze.

1. Per inviare l&#39;ordine, fare clic su **[!UICONTROL Submit Order]**.
