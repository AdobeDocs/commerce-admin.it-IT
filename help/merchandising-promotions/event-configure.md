---
title: Configurare gli eventi
description: Scopri come completare la configurazione di base per abilitare gli eventi e impostare il blocco eventi nella barra laterale della vetrina.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: 'https://experienceleague.adobe.com/nALbSUw8Agac54QLSV4bdCLPse53VywtlMiydvL1L8w'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 125c1f49-aefd-5f34-a252-288937f95f6b
    internal-label: Marketing Tools
  - id: 19d9b313-1a3c-5bed-9da7-4364f71c3a28
    internal-label: Promotions/Events
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%
---
# Configurare gli eventi

{{ee-feature}}

Prima di poter creare un evento, devi completare la configurazione di base per abilitare gli eventi e impostare il blocco dell’evento nella barra laterale.

## Abilitare e configurare gli eventi

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Catalog Events]** ed effettuare le seguenti operazioni:

   ![Configurazione catalogo - eventi catalogo](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - Imposta **[!UICONTROL Enable Catalog Events Functionality]** su `Yes`.

   - Imposta **[!UICONTROL Enable Catalog Event Widget on Storefront]** su `Yes`.

   - Immettere **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. Per impostazione predefinita, questo valore è impostato su `5`. Se si desidera visualizzare un solo evento nel dispositivo di scorrimento alla volta, immettere `1`.

   - Immettere il numero di **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. Per impostazione predefinita, questo valore è impostato su `2`. Se si desidera che il dispositivo di scorrimento visualizzi l&#39;evento successivo in sequenza al momento del clic, immettere `1`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Limitazioni di accesso

L’accesso a una vendita, un evento o un sito privato può essere limitato ai clienti registrati che effettuano l’accesso o esteso ai clienti non registrati che devono registrarsi prima di ottenere l’accesso.

![Configurazione generale - restrizioni siti Web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### Limita l’accesso

L’accesso a una vendita, un evento o un sito privato può essere limitato ai clienti registrati che effettuano l’accesso o esteso ai clienti non registrati che devono registrarsi prima di ottenere l’accesso.

![Configurazione generale - restrizioni siti Web](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL General]** e scegli **[!UICONTROL General]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Website Restrictions]**.

1. Imposta **[!UICONTROL Access Restriction]** su `Yes`.

1. Imposta **[!UICONTROL Restriction Mode]** su uno dei seguenti:

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. Imposta **[!UICONTROL Startup Page]** su uno dei seguenti:

   - `To login form (302 Found)` - Gli utenti vengono reindirizzati al modulo di accesso prima di accedere al sito.

   - `To landing page (302 Found)` - Gli utenti vengono reindirizzati alla pagina di destinazione specificata fino al loro accesso.

     >[!IMPORTANT]
     >
     >Assicurati di includere un collegamento alla pagina di accesso dalla pagina di destinazione, in modo che i clienti possano accedere al sito.

1. Scegli **[!UICONTROL Landing Page]** visualizzato prima che i clienti accedano al sito di vendita privato.

1. Per comunicare ai bot e ai spider dei motori di ricerca che la pagina di destinazione è corretta e che non sono presenti altre pagine da indicizzare, impostare **[!UICONTROL HTTP Response]** su `200 OK`.

   In tutti gli altri casi è impostato su `503 Service Unavailable`.

   >[!NOTE]
   >
   >Applicabile solo se la modalità di restrizione è impostata su _Sito Web chiuso_. Viene eseguito il rendering della pagina di destinazione come HTML non elaborato.

1. Se si desidera che i campi nei moduli di accesso cliente e password dimenticata vengano compilati automaticamente dalle voci precedenti, impostare **[!UICONTROL Enable Autocomplete on login/forgot password forms]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

### Limita vendite

Per impostazione predefinita, i prodotti visualizzati negli eventi in programma o chiusi non sono disponibili per la vendita generica e il pulsante _[!UICONTROL Add to Cart]_non viene visualizzato nell&#39;elenco dei prodotti o nella pagina dei prodotti.

Per ripristinare il pulsante _[!UICONTROL Add to Cart]_per un evento chiuso, è necessario eliminare l&#39;evento (vedere [Aggiornare gli eventi](event-create.md#update-events)). Tuttavia, se un prodotto è associato a un’altra categoria senza restrizioni di vendita, il pulsante è disponibile nella pagina del prodotto. Analogamente, il blocco ticker non viene visualizzato nella pagina del prodotto se il prodotto è associato a un’altra categoria senza restrizioni di vendita.
