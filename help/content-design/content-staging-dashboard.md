---
title: Dashboard di staging del contenuto
description: Utilizza il dashboard di staging del contenuto per accedere a una panoramica di tutte le campagne attive e future.
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Dashboard di staging del contenuto

{{ee-feature}}

Il [!UICONTROL Content Staging] Il dashboard offre una panoramica di tutte le campagne attive e future. Il formato del dashboard può essere modificato da una griglia a una timeline. Puoi inoltre utilizzare i filtri per trovare le campagne, personalizzare il layout delle colonne e salvare diverse visualizzazioni della griglia. Per ulteriori informazioni sui controlli del workspace, vedere [Admin Workspace](../getting-started/admin-workspace.md).

![Dashboard gestione temporanea in visualizzazione griglia](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## Visualizzare il dashboard di staging

1. Il giorno _Amministratore_ barra laterale, vai a  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Per modificare il formato del dashboard, impostare **[!UICONTROL View As]** controllo a `list`, `Grid`, o `Timeline`.

   ![Vista Timeline](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   Quando viene visualizzata la timeline, il cursore nell’angolo in basso a destra può essere utilizzato per regolare la visualizzazione da una a quattro settimane. Ogni colonna rappresenta un giorno.

1. Se viene visualizzata la timeline, trascinate il dispositivo di scorrimento nella `4w` all&#39;estrema destra per visualizzare un intervallo di tempo più lungo.

   ![Visualizzazione per quattro settimane](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. Per visualizzare informazioni generali sulla campagna, fai clic su qualsiasi elemento nella pagina.

   - Per aprire la campagna, fai clic su **[!UICONTROL View/Edit]**.

   - Per visualizzare l’aspetto della campagna per i clienti nel negozio in quel giorno, fai clic su **[!UICONTROL Preview]**.

   ![Informazioni sulla campagna](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## Descrizioni delle colonne del dashboard di staging

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Status] | Stato della campagna. `Active` o `Upcoming`. |
| [!UICONTROL Update Name] | Nome della campagna. |
| [!UICONTROL Includes] | Definisce il numero di oggetti inclusi nella campagna. |
| [!UICONTROL Start Time] | La data di inizio della campagna. |
| [!UICONTROL End Time] | La data di fine della campagna. |
| [!UICONTROL Description] | Descrizione aggiuntiva di ciascuna campagna. |
| [!UICONTROL Action] | Le azioni che possono essere applicate a un singolo record includono:<br/>**[!UICONTROL View/Edit]**- Apre la campagna in modalità di modifica.<br/>**[!UICONTROL Preview]** - Visualizza la campagna in modalità anteprima. |

{style="table-layout:auto"}

## Modificare una campagna

Gli oggetti campagna esistenti possono essere modificati dal dashboard di staging, ad eccezione delle campagne per le regole di prezzo che non hanno date di fine.

>[!NOTE]
>
>Se una campagna che include una regola di prezzo viene creata inizialmente senza una data di fine, non può essere modificata in un secondo momento in modo da includere una data di fine. In tal caso, è necessario creare una campagna duplicata e immettere la data di fine necessaria.

![Dettagli della campagna](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

La campagna in questo esempio include due categorie e tre singoli prodotti.

Segui i passaggi seguenti per modificare uno qualsiasi degli oggetti di questa campagna.

1. Il giorno _Amministratore_ barra laterale, vai a  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Trova la campagna nell’elenco o nella timeline visualizzata e aprila per accedere ai dettagli:

   - Per visualizzare un elenco, fai clic su **[!UICONTROL Select]** e poi **[!UICONTROL View/Edit]** nel _[!UICONTROL Action]_colonna.
   - Per visualizzare la timeline, fai clic una volta per visualizzare il riepilogo, quindi fai clic su **[!UICONTROL View/Edit]**.

1. Aggiornare una qualsiasi delle impostazioni in _[!UICONTROL General]_in base alle esigenze.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) qualsiasi sezione che contiene un elemento da modificare.

   ![Aggiornamento dei prodotti assegnati per un elemento della campagna](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save]**.
