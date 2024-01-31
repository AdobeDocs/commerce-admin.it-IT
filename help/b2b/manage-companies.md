---
title: Gestione società
description: Amministrazione e gestione semplificate delle organizzazioni B2B con modelli operativi complessi.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Gestione società

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Disponibile solo per i partecipanti ai programmi beta"}

La gestione aziendale semplifica le operazioni aziendali per le aziende con strutture organizzative complesse. Gli utenti amministratori possono creare una gerarchia di società per riflettere un’organizzazione B2B assegnando le società alla società madre designata. Questa assegnazione consente all&#39;amministratore della società madre di visualizzare e gestire le società all&#39;interno dell&#39;organizzazione.

Avvia attività di gestione società da *[!UICONTROL Companies]* visualizzazione. Dall’amministratore, vai a  **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Griglia B2B Manage Companies](./assets/companies-grid-view.png){width="700" zoomable="yes"}

In *[!UICONTROL Companies grid]*, il *[!UICONTROL Company Type]* indica se una società è gestita come parte di un&#39;organizzazione o come società separata.

- `Parent` è un&#39;organizzazione aziendale con una o più società assegnate. Una società madre non può essere assegnata come figlio di un&#39;altra società.

- `Child` è una società che è stata assegnata a un’organizzazione. È possibile assegnare una società a una sola società madre.

- `Company` rappresenta una singola azienda. Una singola azienda può diventare parte di un&#39;organizzazione trasformandola in una società madre o assegnandola a una società madre esistente.

Quando si modifica una società padre o figlio, espandere *[!UICONTROL Company Hierarchy]* per visualizzare tutte le società dell&#39;organizzazione. A `Current` Il flag indica la società che stai modificando.

![Griglia gerarchia società B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## Visualizza e configura [!UICONTROL Company Hierarchy]

Al momento della creazione iniziale della società, il [!UICONTROL Company Hierarchy] griglia vuota. È vuoto anche se l’azienda è una singola azienda.

![Griglia gerarchia società B2B](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Per le società madri, gli utenti amministratori con le autorizzazioni appropriate possono completare le seguenti attività:

- Crea la gerarchia di società creando una nuova organizzazione principale o aggiornandone una esistente.
- Gestisci un&#39;organizzazione esistente per aggiungere o rimuovere società.

Per ulteriori informazioni, consulta [Gestire la gerarchia aziendale](assign-companies.md).
