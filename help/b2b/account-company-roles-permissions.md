---
title: Ruoli e autorizzazioni aziendali
description: Scopri i ruoli e le autorizzazioni che un amministratore aziendale può applicare agli utenti aziendali, consentendo l’accesso a vari livelli alle informazioni e alle risorse dell’ordine.
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# Ruoli e autorizzazioni aziendali

I ruoli per gli utenti aziendali vengono configurati con vari livelli di autorizzazione per accedere alle informazioni e alle risorse di vendita. Per impostazione predefinita, l&#39;amministratore della società è un _utente privilegiato_ con autorizzazioni complete. La pagina [Accesso negato](../content-design/pages.md#access-denied) viene visualizzata se l&#39;utente non dispone delle autorizzazioni necessarie per accedere alla pagina.

![Pagina Ruoli e autorizzazioni con ruolo predefinito](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

Il sistema dispone di un ruolo utente predefinito predefinito, che puoi utilizzare _così com&#39;è_ o modificare in base alle tue esigenze. Puoi creare tutti i ruoli necessari per adattarli alla struttura aziendale e alle responsabilità organizzative, ad esempio:

- **Utente predefinito**: l&#39;utente predefinito ha accesso completo alle attività relative alle vendite e alle offerte e accesso in sola visualizzazione al profilo aziendale e alle informazioni sul credito.

- **Acquirente senior**: un acquirente senior potrebbe avere accesso a tutte le risorse Vendite e Preventivi e alle autorizzazioni di sola visualizzazione per il profilo aziendale, l&#39;utente e i team, le informazioni sul pagamento e il credito aziendale.

- **Acquirente assistente**: un acquirente assistente potrebbe disporre dell&#39;autorizzazione per effettuare un ordine utilizzando _Estrai con preventivo_ e per visualizzare ordini, preventivi e informazioni nel profilo aziendale.

## Gestire ruoli e autorizzazioni

1. L’amministratore della società effettua l’accesso al proprio account store.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Roles and Permissions]**.

1. Completa una delle seguenti attività.

### Creare un ruolo

1. Clic su **[!UICONTROL Add New Role]**.

   ![Aggiungi nuovo ruolo](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. Immette un **[!UICONTROL Role Name]** descrittivo.

1. In _[!UICONTROL Role Permissions]_, esegue una delle operazioni seguenti:

   - Seleziona la casella di controllo di ogni risorsa o attività a cui gli utenti assegnati al ruolo dispongono dell&#39;autorizzazione di accesso.

   - Seleziona la casella di controllo **[!UICONTROL All]** e deseleziona la casella di controllo di ogni risorsa o attività a cui gli utenti assegnati al ruolo non dispongono dell&#39;autorizzazione di accesso.

1. Clic su **[!UICONTROL Save Role]**.

1. Crea tutti i ruoli necessari ripetendo questi passaggi.

### Modificare un ruolo

1. Per modificare il ruolo, l&#39;amministratore della società fa clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Actions]_.

1. Apporta le modifiche necessarie alle impostazioni del nome e delle autorizzazioni.

1. Al termine, fa clic su **[!UICONTROL Save Role]**.

### Duplicare un ruolo

1. Per duplicare il ruolo, l&#39;amministratore della società fa clic su **[!UICONTROL Duplicate]** nella colonna _[!UICONTROL Actions]_.

1. Apporta le modifiche necessarie alle impostazioni del nome e delle autorizzazioni.

1. Al termine, fa clic su **[!UICONTROL Save Role]**.

### Eliminare una mansione

1. L’amministratore della società trova il ruolo da eliminare nell’elenco dei ruoli.

   È possibile eliminare solo i ruoli senza utenti assegnati.

1. Fa clic su **[!UICONTROL Delete]** nella colonna _[!UICONTROL Actions]_.

1. Quando viene richiesto di confermare, fa clic su **[!UICONTROL OK]**.

## Azioni

| Azione | Descrizione |
|-----------| ----------- |
| [!UICONTROL Duplicate] | Crea una copia del ruolo selezionato. Alla fine è stato aggiunto `- Duplicated` al nome del ruolo duplicato. |
| [!UICONTROL Edit] | Modifica il nome e/o il set di autorizzazioni. |
| [!UICONTROL Delete] | Elimina il ruolo. È possibile eliminare solo i ruoli senza utenti assegnati. |

{style="table-layout:auto"}

## Autorizzazioni ruolo

- Tutti
   - Vendite
      - Consenti ritiro (ordine di registrazione)
         - Usa metodo di pagamento in conto
      - Visualizza ordini
         - Visualizza ordini di utenti subordinati
- Virgolette
   - Visualizza
      - Richiedi, Modifica, Elimina
      - Pagamento con preventivo
      - Visualizza preventivi di utenti subordinati
- Approvazioni ordine
   - Visualizza i miei ordini di acquisto
      - Visualizza per subordinati
      - Visualizza per tutte le società
   - Approva automaticamente gli OA creati all&#39;interno di questo ruolo
   - Approva ordini di acquisto senza altre approvazioni
   - Visualizza regole di approvazione
      - Creare, modificare ed eliminare
- Profilo società
   - Informazioni account (visualizzazione)
      - Modifica
   - Indirizzo legale
      - Modifica
   - Contatti (visualizzazione)
   - Informazioni sul pagamento (visualizzazione)
   - Informazioni sulla spedizione (Visualizza)
- Gestione utente società
   - Visualizza ruoli e autorizzazioni
      - Gestire ruoli e autorizzazioni
   - Visualizza utenti e team
      - Gestione di utenti e team
- Credito società
   - Visualizza

## Assegnare un ruolo a un utente della società

Dopo aver definito i ruoli necessari, l’amministratore della società assegna un ruolo a ogni utente della società.

1. Accedi al proprio account aziendale come amministratore della società.

1. Nel pannello a sinistra, seleziona **[!UICONTROL Company Users]**.

   ![Utenti società](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Trova l&#39;utente nell&#39;elenco e seleziona **[!UICONTROL Edit]**.

1. Seleziona **[!UICONTROL User Role]** appropriato per l&#39;utente.

   ![Modifica utente - scegli un ruolo utente](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. Clic su **[!UICONTROL Save]**.
