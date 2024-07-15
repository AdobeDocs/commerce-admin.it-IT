---
title: Struttura dei conti aziendali
description: Scopri le strutture aziendali e come un amministratore aziendale può definirle per supportare i flussi di lavoro e le politiche aziendali.
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Struttura dei conti aziendali

È possibile impostare un conto aziendale per riflettere la struttura dell&#39;attività. Inizialmente, la struttura aziendale include solo l’amministratore della società, ma può essere espansa per includere i team di utenti. Gli utenti possono essere associati a team o organizzati all’interno di una gerarchia di divisioni e suddivisioni all’interno dell’azienda.

![Struttura della società con divisioni](./assets/company-structure-diagram.svg){width="500"}

Nel dashboard degli account dell’amministratore della società, la struttura della società è rappresentata da una struttura ad albero ed è inizialmente costituita solo dall’amministratore della società.

![Struttura della società con amministratore della società](./assets/company-structure-tree-admin.png){width="600" zoomable="yes"}

Quando l’account viene creato e approvato, l’amministratore della società può utilizzare l’indirizzo e-mail della società o riceverne uno diverso.

È possibile che la persona che funge da amministratore dell’azienda abbia più ruoli all’interno dell’azienda. Se per l&#39;amministratore della società viene immesso un indirizzo e-mail distinto, la struttura aziendale iniziale include l&#39;amministratore della società più un account utente singolo a nome dell&#39;amministratore della società. In tal caso, l’amministratore della società può accedere all’account come società o come singolo utente.

![Struttura della società con account amministratore e utente](./assets/company-structure-tree-admin-user.png){width="600" zoomable="yes"}

Per i commercianti, l&#39;intera struttura aziendale si riflette nelle _Aziende_ e _Clienti_ griglie all&#39;interno dell&#39;Amministratore. Nella griglia Società sono elencate tutte le società indipendentemente dallo stato. L&#39;esempio seguente mostra gli account per due società: la società _ACME_ e la società _Vendelay_.

![Griglia Aziende](./assets/companies-grid.png){width="700" zoomable="yes"}

L&#39;esempio seguente mostra la griglia [!UICONTROL Customers] con gli account iniziali dell&#39;amministratore della società per queste società.

![Griglia clienti con account amministratore società](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Dopo aver creato l&#39;account, l&#39;amministratore della società deve definire la struttura aziendale di [team](account-company-structure.md), configurare [utenti della società](account-company-users.md) e stabilire [ruoli e autorizzazioni](account-company-roles-permissions.md) per ciascuno di essi.

## Icone della struttura aziendale

| Icona | Descrizione |
| ---- | ----------------- |
| ![Icona Amministratore società](./assets/company-icon-admin.png) | Rappresenta l&#39;amministratore della società nella struttura della società. |
| ![Icona team](./assets/company-icon-team.png) | Rappresenta un team nella struttura aziendale. |
| ![Icona utente](./assets/company-icon-user.png) | Rappresenta un utente nella struttura aziendale. |
| ![Icona Sposta](./assets/company-icon-move.png) | Sposta un team in un&#39;altra posizione nella struttura aziendale. |
| ![Icona di espansione](./assets/company-icon-expand.png) | Espande un team nella struttura della società. |
| ![Icona Comprimi](./assets/company-icon-collapse.png) | Comprime un team nella struttura aziendale. |

{style="table-layout:auto"}

## Creare team aziendali

La struttura di un conto della società deve riflettere l’organizzazione di acquisto, sia che si tratti di un’organizzazione semplice e piatta o complessa, con team diversi per ogni suddivisione e divisione della società.

Se l&#39;archivio è [configurato](enable-basic-features.md) per consentire alle società di gestire i propri account, la configurazione della struttura della società è una delle prime attività che un amministratore della società deve completare dopo l&#39;approvazione dell&#39;account. Nel conto della società, la struttura della società è rappresentata da una struttura con l’amministratore della società in alto.

![Struttura aziendale con team](./assets/company-structure-teams-diagram.svg){width="450"}

1. L’amministratore della società effettua l’accesso al proprio account.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Company Structure]**.

1. In **[!UICONTROL Business Structure]**, fa clic su **[!UICONTROL Add Team]** e esegue le operazioni seguenti:

   - Immette **[!UICONTROL Team Title]** e **[!UICONTROL Description]**.

     Il Titolo team può essere qualsiasi cosa che rappresenti la struttura dell’azienda, ad esempio un team, un ufficio o una divisione all’interno dell’azienda

     ![Aggiungi team](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - Al termine, fa clic su **[!UICONTROL Save]**.

   - Crea tutti i team necessari.

     ![Struttura aziendale con team](./assets/company-structure-teams.png){width="600" zoomable="yes"}

1. Per creare una gerarchia di team, effettua le seguenti operazioni:

   - Seleziona il team padre e fai clic su **[!UICONTROL Add Team]**.

     ![Struttura della società con divisioni](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - Immette **[!UICONTROL Team Title]** e **[!UICONTROL Description]**.

   - Clic su **[!UICONTROL Save]**.

1. Ripete questi passaggi per creare tutti i team, o divisioni e suddivisioni, necessari.

   ![Struttura della società con divisioni e suddivisioni](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

## Spostare un team

Quando l’amministratore della società lavora con la struttura della società, può trascinare team o divisioni in altre posizioni nella struttura.

1. L&#39;amministratore della società individua il team da spostare.

1. Fa clic e trascina il team in una nuova posizione nella struttura aziendale.

## Eliminare un team

>[!NOTE]
>
>Prima di eliminare un team, è consigliabile assicurarsi che sia selezionato il team corretto, ovvero che i team eliminati non possano essere ripristinati.

1. L&#39;amministratore della società seleziona il team da eliminare.

1. Clic su **[!UICONTROL Delete Selected]**.

1. Quando viene richiesto di confermare, fa clic su **[!UICONTROL Delete]**.

## Espandere o comprimere la struttura del team

Quando l’amministratore della società lavora con la struttura della società, può comprimere o espandere la struttura:

- Fai clic su **[!UICONTROL Collapse All]** o **[!UICONTROL Expand All]**.

- Fai clic su ![Icona espansa](../assets/icon-display-collapse.png) per comprimere un team oppure su ![Icona compressa](../assets/icon-display-expand.png) per espandere un team.

## Assegnare utenti ai team

Quando i team e gli utenti vengono aggiunti per la prima volta alla [struttura aziendale](account-company-structure.md), vengono posizionati allo stesso livello sotto l&#39;amministratore della società.

![Struttura aziendale con utenti e team](./assets/company-users-added.png){width="700" zoomable="yes"}

| Controllo | Descrizione |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | Comprime o espande la struttura ad albero della struttura aziendale |
| [!UICONTROL Add User] | Crea un utente sotto il team corrente |
| [!UICONTROL Add Team] | Crea un team |
| [!UICONTROL Edit Selected / Delete Selected] | Modifica o rimuove utenti dalla struttura aziendale |

{style="table-layout:auto"}

1. Nel pannello a sinistra, l&#39;amministratore della società sceglie **[!UICONTROL Company Structure]**.

1. Per assegnare un utente a un team esistente, trascinano (![Icona Sposta](../assets/icon-move.png)) l&#39;utente nel team appropriato.

   ![Assegnazioni team](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
