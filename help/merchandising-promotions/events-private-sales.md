---
title: Vendite ed eventi privati
description: Scopri come utilizzare le vendite private e altri eventi di catalogo per aumentare le vendite per la base di clienti esistente e generare nuovi clienti potenziali.
exl-id: 0b890463-b1e5-4327-8d8a-372afd53312a
feature: Reporting, Promotions/Events
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/8MvnlOp5muOQbx3b7dSKguc4wf-k47v9AtaHXu7b9pU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
subfeature_v2:
  - id: bd0aa680-a881-4f35-9dcf-843b0574bc5f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# Vendite ed eventi privati

{{ee-feature}}

Le vendite private e altri eventi di catalogo sono un ottimo modo per utilizzare la base clienti esistente per generare nuovi clienti potenziali e potenziali clienti o per scaricare le scorte in eccesso. Puoi creare vendite a tempo limitato, limitare le vendite a membri specifici o creare una pagina di vendita privata autonoma. Puoi anche definire inviti e dettagli dell’evento. Aumenta la fidelizzazione al marchio e genera entusiasmo offrendo ai tuoi clienti migliori il trattamento VIP. Offri accesso esclusivo alle vendite dei soli membri o alle vendite private per aumentare la brand loyalty. È inoltre possibile utilizzare queste vendite per liquidare le merci in eccesso. I gruppi di clienti sono utili per impostare solo questi tipi di membri e le vendite VIP.

![Esempio di vetrina - evento nella home page](./assets/storefront-event-home-page.png){width="700" zoomable="yes"}

## Componenti per la gestione degli eventi

- **Categorie** - Ogni evento è associato a una [categoria](../catalog/category-create.md) del catalogo.

- **Eventi** - Le vendite degli eventi si basano su una data di inizio e una data di fine. Puoi utilizzare un [ticker conto alla rovescia](#event-ticker) per visualizzare il tempo rimanente.

- **Carosello eventi catalogo** - Quando il [widget eventi catalogo](../content-design/widget-event-carousel.md) è abilitato nella configurazione, può essere inserito nelle pagine di archivio come elenco di eventi aperti e futuri, ordinati in base alla data di fine. Se due o più eventi hanno la stessa data di fine, gli eventi vengono ordinati in base all’ordine specificato nella configurazione.

- **[!UICONTROL Websites]** - Le autorizzazioni per le categorie si basano principalmente su [gruppi di clienti](../customers/customer-groups.md).

- **Autorizzazioni categoria** - [Autorizzazioni categoria](../catalog/category-permissions.md) offre il controllo completo sulle attività specifiche che possono essere eseguite in una determinata categoria.

- **Limitazioni di accesso** - Impedisce l&#39;[accesso](event-configure.md#restrict-access) pubblico al sito reindirizzandolo a una pagina di destinazione, di accesso o di registrazione.

- **Inviti** - I messaggi e-mail vengono inviati con un collegamento per creare un account nell&#39;archivio. Puoi limitare la possibilità di creare un account solo a coloro che ricevono un [invito](invitations.md).

- **Report vendite private** - I [Report vendite private](../getting-started/private-sales-reports.md) forniscono informazioni sugli inviti inviati, sui clienti invitati e sulle conversioni.

## ticker di evento

Il blocco ticker visualizza un ticker del conto alla rovescia per gli eventi aperti, con la data di inizio e la data di fine per i prossimi eventi. Se un evento è stato chiuso, il ticker mostra le date di inizio e fine.

![Esempio di vetrina - carosello eventi](./assets/storefront-event-ticker-carousel.png){width="700" zoomable="yes"}

Se il ticker della pagina della categoria è abilitato per un evento, il blocco del ticker viene visualizzato nella parte superiore dell’elenco delle categorie. Se il ticker della pagina del prodotto è abilitato, il blocco del ticker viene visualizzato anche nella parte superiore della pagina del prodotto di qualsiasi prodotto associato alla categoria.

Il ticker dell&#39;evento può essere attivato quando [crei eventi](event-create.md).

![Esempio di vetrina - barra laterale evento](./assets/storefront-event-sidebar.png){width="700" zoomable="yes"}
