---
title: Panoramica del catalogo condiviso
description: Scopri i cataloghi condivisi forniti da Adobe Commerce B2B e come utilizzarli per gestire i cataloghi gestiti con prezzi personalizzati per diversi account aziendali.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Panoramica del catalogo condiviso

Adobe Commerce B2B consente di gestire cataloghi _condivisi_ con gate con prezzi personalizzati per diverse aziende. Oltre al catalogo prodotti standard _primario_, fornisce l&#39;accesso del cliente a due tipi di cataloghi condivisi con strutture di prezzo diverse.

Se la funzione [Catalogo condiviso](enable-basic-features.md) è abilitata nella configurazione, il catalogo primario originale rimane visibile dall&#39;amministratore, ma solo il catalogo condiviso pubblico predefinito (Generale) è visibile dalla vetrina. È inoltre possibile creare cataloghi personalizzati visibili solo ai membri di account [società](account-companies.md) specifici.

Per il catalogo condiviso pubblico `Default (General)`, è necessario assegnare i prodotti per visualizzare il catalogo nella vetrina. Per impostazione predefinita, è vuoto e non contiene alcun prodotto.

>[!NOTE]
>
>**[Versione B2B 1.3.0](release-notes.md#b2b-v130) e successiva** — Quando si crea un catalogo condiviso, ogni [autorizzazione categoria](../catalog/category-permissions.md) per il catalogo è impostata su _[!UICONTROL Allow for the Display Product Prices]_&#x200B;e&#x200B;_[!UICONTROL Add to Cart]_ per i gruppi di clienti a cui viene assegnato questo accesso nelle impostazioni delle autorizzazioni del catalogo. In precedenza, queste impostazioni venivano impostate automaticamente su `Deny` anche quando le autorizzazioni del catalogo erano impostate su `Allow`.

>[!IMPORTANT]
>
>Tutte le [impostazioni delle autorizzazioni di gruppo](../configuration-reference/catalog/catalog.md#category-permissions) esistenti vengono ignorate da **_tutte_** categorie nel catalogo quando la funzionalità **_[!UICONTROL Shared Catalog]_** è abilitata. [!UICONTROL Shared Catalog] controlla completamente tutte le autorizzazioni di categoria nel catalogo quando è abilitato.

La pagina _[!UICONTROL Shared Catalogs]_&#x200B;consente di accedere agli strumenti utilizzati per la gestione dei cataloghi condivisi. La pagina è simile all&#39;[Area di lavoro di amministrazione](../getting-started/admin-workspace.md) standard, con filtri e controlli delle azioni. Nella griglia sono elencati tutti i cataloghi condivisi, incluso il catalogo condiviso pubblico predefinito e tutti i cataloghi personalizzati impostati.

![Cataloghi condivisi](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## Accedi alla pagina [!UICONTROL Shared Catalogs]

Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

## Controlli delle azioni

I [controlli azioni](../getting-started/admin-actions-control.md) nell&#39;angolo superiore sinistro possono essere utilizzati con il controllo Azioni di massa per eliminare i cataloghi condivisi selezionati che non sono più necessari. Nella griglia, la colonna _[!UICONTROL Actions]_&#x200B;contiene la selezione completa di strumenti per la gestione dei cataloghi condivisi.

![Azioni catalogo condiviso](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| Controllo | Descrizione |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | Determina la selezione dei prodotti e i prezzi personalizzati disponibili nel catalogo condiviso. |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | Determina quali società possono accedere a un catalogo condiviso. |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | Determina le informazioni di dettaglio del catalogo, tra cui il nome, il tipo di catalogo, la classe fiscale del cliente e la descrizione. |
| [!UICONTROL Delete] | Elimina i cataloghi condivisi selezionati. |

{style="table-layout:auto"}

## Descrizioni delle colonne

| Intestazione | Descrizione |
|--- |--- |
| [!UICONTROL Select] | Seleziona i record di catalogo condiviso per applicare un&#39;azione. Il controllo nell&#39;intestazione può essere utilizzato per selezionare tutti o deselezionare tutti i record di catalogo condivisi nella griglia. Per selezionare un singolo catalogo condiviso, selezionare la casella di controllo. |
| [!UICONTROL ID] | Identificatore numerico univoco assegnato in sequenza al momento della creazione del catalogo. |
| [!UICONTROL Name] | Nome del catalogo condiviso. Per impostazione predefinita, è disponibile il catalogo condiviso predefinito (Generale). |
| [!UICONTROL Type] | Identifica il tipo di catalogo condiviso come: <br/>**[!UICONTROL Public]**- Il catalogo condiviso pubblico predefinito viene creato automaticamente quando si installa Adobe Commerce B2B. È inizialmente assegnato ai gruppi di clienti `General` e `Not Logged In` ed è visibile agli ospiti e ai singoli clienti connessi che non sono associati a una società. Il sistema supporta un solo catalogo condiviso pubblico alla volta.<br/>**[!UICONTROL Custom]** - Un catalogo condiviso personalizzato contiene prezzi visibili solo ai soci connessi degli account società assegnati. Puoi creare tutti i cataloghi condivisi personalizzati necessari. |
| [!UICONTROL Customer Tax Class] | Classe di imposta assegnata al gruppo di clienti corrispondente. Questa colonna non viene visualizzata nella griglia predefinita, ma può essere aggiunta modificando il layout della colonna. |
| [!UICONTROL Created At] | Data e ora di creazione del catalogo condiviso. |
| [!UICONTROL Created By] | Nome e cognome dell&#39;amministratore del negozio che ha creato il catalogo condiviso. |
| [!UICONTROL Action] | Elenca le azioni da applicare ai cataloghi selezionati. Opzioni: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
