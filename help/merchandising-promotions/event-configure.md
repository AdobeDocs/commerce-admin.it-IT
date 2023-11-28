---
title: Configurare gli eventi
description: Scopri come completare la configurazione di base per abilitare gli eventi e impostare il blocco eventi nella barra laterale della vetrina.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Configurare gli eventi

{{ee-feature}}

Prima di poter creare un evento, devi completare la configurazione di base per abilitare gli eventi e impostare il blocco dell’evento nella barra laterale.

## Abilitare e configurare gli eventi

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Catalog Events]** ed effettuare le seguenti operazioni:

   ![Configurazione del catalogo - Eventi catalogo](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Enable Catalog Events Functionality]** a `Yes`.

   - Imposta **[!UICONTROL Enable Catalog Event Widget on Storefront]** a `Yes`.

   - Inserisci il **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. Per impostazione predefinita, questo valore è impostato su `5`. Se si desidera visualizzare un solo evento nel dispositivo di scorrimento alla volta, immettere: `1`.

   - Immetti il numero di **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. Per impostazione predefinita, questo valore è impostato su `2`. Se si desidera che il dispositivo di scorrimento visualizzi l&#39;evento successivo in sequenza quando si fa clic su, immettere: `1`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Limitazioni di accesso

L’accesso a una vendita, un evento o un sito privato può essere limitato ai clienti registrati che effettuano l’accesso o esteso ai clienti non registrati che devono registrarsi prima di ottenere l’accesso.

![Configurazione generale - Restrizioni per i siti Web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Limita l’accesso

L’accesso a una vendita, un evento o un sito privato può essere limitato ai clienti registrati che effettuano l’accesso o esteso ai clienti non registrati che devono registrarsi prima di ottenere l’accesso.

![Configurazione generale - Restrizioni per i siti Web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL General]** e scegli **[!UICONTROL General]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Website Restrictions]** sezione.

1. Imposta **[!UICONTROL Access Restriction]** a `Yes`.

1. Imposta **[!UICONTROL Restriction Mode]** a uno dei seguenti elementi:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Imposta **[!UICONTROL Startup Page]** a uno dei seguenti elementi:

   - `To login form (302 Found)` - Gli utenti vengono reindirizzati al modulo di accesso prima di accedere al sito.

   - `To landing page (302 Found)` : gli utenti vengono reindirizzati alla pagina di destinazione specificata fino al momento dell’accesso.

     >[!IMPORTANT]
     >
     >Assicurati di includere un collegamento alla pagina di accesso dalla pagina di destinazione, in modo che i clienti possano accedere al sito.

1. Scegli la **[!UICONTROL Landing Page]** che viene visualizzato prima che i clienti accedano al sito di vendita privato.

1. Per comunicare ai bot e ai ragni dei motori di ricerca che la pagina di destinazione è corretta e che non vi sono altre pagine da indicizzare, imposta **[!UICONTROL HTTP Response]** a `200 OK`.

   In tutti gli altri casi impostati su `503 Service Unavailable`.

   >[!NOTE]
   >
   >Applicabile solo se la modalità di restrizione è impostata su _Sito Web chiuso_. Viene eseguito il rendering della pagina di destinazione come HTML non elaborato.

1. Se desideri che i campi nei moduli per l’accesso ai clienti e per le password dimenticate vengano compilati automaticamente dalle voci precedenti, imposta **[!UICONTROL Enable Autocomplete on login/forgot password forms]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Limita vendite

Per impostazione predefinita, i prodotti visualizzati negli eventi in programma o chiusi non sono disponibili per la vendita generale e il _[!UICONTROL Add to Cart]_non viene visualizzato nell’elenco o nella pagina del prodotto.

Per ripristinare _[!UICONTROL Add to Cart]_per un evento chiuso, l’evento deve essere eliminato (vedi [Aggiornare gli eventi](event-create.md#update-events)). Tuttavia, se un prodotto è associato a un’altra categoria senza restrizioni di vendita, il pulsante è disponibile nella pagina del prodotto. Analogamente, il blocco ticker non viene visualizzato nella pagina del prodotto se il prodotto è associato a un’altra categoria senza restrizioni di vendita.
