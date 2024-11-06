---
title: Creare un account società
description: Scopri come creare un account aziendale nell’amministratore di Adobe Commerce e nella vetrina.
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 5312aa3f483399ecc4e9491b39f8300d8616e9e5
workflow-type: tm+mt
source-wordcount: '1762'
ht-degree: 0%

---

# Creare un account società

Gli account aziendali possono essere impostati dalla vetrina dal cliente o dall’amministratore. Tutte le richieste di creazione di un account aziendale devono essere approvate dall&#39;amministratore dello store prima che l&#39;account diventi attivo.

Alla persona che imposta un account società dalla vetrina viene assegnato un ruolo come [amministratore società](account-company-admin.md). Dopo l&#39;approvazione della richiesta di creazione di un account aziendale, l&#39;amministratore della società può impostare una password per l&#39;account e accedervi.

## Metodo 1: il cliente crea il conto dalla vetrina

>[!IMPORTANT]
>
>Per supportare questo metodo (che consente ai clienti di registrare la propria società dalla vetrina), assicurati che le [funzionalità B2B](enable-basic-features.md) siano abilitate.

1. Nell&#39;angolo superiore destro dell&#39;intestazione della vetrina, il cliente fa clic su **[!UICONTROL Create an Account]** e sceglie **[!UICONTROL Create New Company Account]**.

   ![Crea nuovo account società](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >Se un visitatore ha effettuato l&#39;accesso a un account utente registrato, può creare un account aziendale passando a _[!UICONTROL Customer Profile]_>**[!UICONTROL Company Structure]**>**[!UICONTROL Create a Company Account]**.

1. Nella sezione _[!UICONTROL Company Information]_, il cliente effettua le seguenti operazioni:

   - Compila i campi obbligatori:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - Compila i campi rimanenti, come applicabile:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   ![Informazioni sulla società](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. Completa i campi obbligatori nella sezione _[!UICONTROL Legal Address]_.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

   ![Indirizzo legale](./assets/company-legal-address-storefront.png){width="700" zoomable="yes"}

1. Nella sezione _[!UICONTROL Company Administrator]_, esegue le operazioni seguenti:

   - Immette **[!UICONTROL Email address]** per l&#39;amministratore della società.

     L’indirizzo e-mail dell’amministratore della società può essere lo stesso dell’indirizzo e-mail della società o un indirizzo e-mail diverso. Se si immette un indirizzo e-mail diverso, viene creato un account utente della società, oltre all&#39;account amministratore della società.

   - Immette **[!UICONTROL First Name]** e **[!UICONTROL Last Name]** dell&#39;amministratore della società.

   - Facoltativamente, completa i campi seguenti:

      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Work Phone Number]**
      - **[!UICONTROL Gender]**

   ![Amministratore società](./assets/company-administrator-account-storefront.png)

1. Completa la convalida se reCAPTCHA è abilitato per questa funzione storefront.

1. Al termine delle informazioni, selezionare **[!UICONTROL Submit]**.

   Quando la richiesta di creazione di un account aziendale viene approvata dall’esercente, viene inviata una notifica e-mail all’amministratore della società.

   ![E-mail di benvenuto di esempio](./assets/company-admin-welcome-email.png){width="500"}

   Una volta impostata la password, l&#39;amministratore della società può [accedere](../customers/customer-sign-in.md) all&#39;account.

## Metodo 2: l’esercente crea l’account dall’amministratore

Il processo di creazione di una società dall’amministratore è essenzialmente lo stesso della vetrina, ma con campi aggiuntivi.

![Aggiungi una nuova società dall&#39;amministratore](./assets/company-add-new.png){width="700" zoomable="yes"}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Fare clic su **[!UICONTROL Add New Company]** ed effettuare le seguenti operazioni:

   - Completa i campi obbligatori seguenti:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - Se non sei pronto per la pubblicazione dell&#39;account, imposta **[!UICONTROL Status]** su `Pending Approval`. (Imposta su `Active` per impostazione predefinita.)

   - Se applicabile, scegliere l&#39;account amministratore di **[!UICONTROL Sales Representative]** che deve gestire l&#39;account.

1. Nella sezione _[!UICONTROL Account Information]_eseguire le operazioni seguenti:

   - Compila i campi seguenti, a seconda dei casi:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   - Per **[!UICONTROL Comment]**, immettere le informazioni aggiuntive sul cliente che potrebbero essere necessarie.

     I commenti sono visibili solo dall’amministratore.

   ![Informazioni account](./assets/company-create-account-information-admin.png){width="700" zoomable="yes"}

1. Al momento della creazione iniziale della società, la griglia _[!UICONTROL Company Hierarchy]_è vuota quando la si espande. Dopo aver salvato la società, è possibile includerla in una gerarchia di società. Consulta [Gestione società](manage-companies.md).

1. Nella sezione _[!UICONTROL Legal Address]_, completa i seguenti campi obbligatori:

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City Country]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

1. Nella sezione _[!UICONTROL Company Admin]_eseguire le operazioni seguenti:

   - Completa i campi obbligatori seguenti:

      - **[!UICONTROL Email]**
      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**

   - Completa le seguenti parti facoltative del nome, che possono essere applicabili ad alcuni nomi di clienti più di altri e possono essere utilizzate a tua discrezione:

      - **[!UICONTROL Prefix]**
      - **[!UICONTROL Middle Name/Initial]**
      - **[!UICONTROL Suffix]**

   - Se le informazioni sono disponibili, compila i campi rimanenti per descrivere l’amministratore della società:

      - **[!UICONTROL Website]**
      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Work Phone Number]**
      - **[!UICONTROL Gender]**
      - **[!UICONTROL Send Welcome Email From]**

   ![Amministratore società](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Nella sezione _[!UICONTROL Company Credit]_, che visualizza un riepilogo dell&#39;attività di credito del cliente, completare tutti i campi nella parte inferiore della sezione, a seconda delle necessità:

   - **[!UICONTROL Credit Currency]**
   - **[!UICONTROL Credit Limit]**
   - **[!UICONTROL Allow to Exceed Credit Limit]**
   - **[!UICONTROL Reason for Change]**

   ![Credito società](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

1. Nella sezione _[!UICONTROL Advanced Settings]_eseguire le operazioni seguenti:

   >[!NOTE]
   >
   >L&#39;assegnazione del gruppo di clienti determina quale catalogo condiviso è disponibile per l&#39;azienda e i suoi dipendenti. Per impostazione predefinita, la società viene assegnata al gruppo di clienti impostato come predefinito nella configurazione.

   - È possibile modificare l&#39;assegnazione **[!UICONTROL Customer Group]** per la società e i relativi dipendenti in un gruppo che ha accesso a un catalogo condiviso diverso o a un gruppo di clienti standard. Viene chiesto di confermare prima di modificare il gruppo.

     ![Modifica del gruppo di clienti](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   - Se si desidera consentire ai dipendenti della società di generare preventivi dal proprio account, impostare **[!UICONTROL Allow Quotes]** su `Yes`.

   - Se si desidera consentire ai dipendenti della società di creare e utilizzare ordini fornitore dal proprio account, impostare **[!UICONTROL Enable Purchase Orders]** su `Yes`.

   - Per modificare **[!UICONTROL Applicable Payment Methods]** disponibili per la società, deselezionare la casella di controllo **[!UICONTROL Use config settings]** e scegliere una delle opzioni seguenti:

     | Opzione | Descrizione |
     |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Payment Methods` | (Impostazione predefinita) Abilita tutti i [metodi di pagamento impostati come predefiniti](../configuration-reference/general/b2b-features.md#default-b2b-payment-methods) per gli ordini B2B. |
     | `All Enabled Payment Methods` | Rende disponibili tutti i [metodi di pagamento abilitati](../configuration-reference/sales/payment-methods.md) per gli account cliente associati all&#39;account società. |
     | `Selected Payment Methods` | Consente di selezionare i metodi di pagamento disponibili per i conti cliente associati al conto società. Per selezionare più metodi di pagamento, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e selezionare ciascuna opzione. |

     {style="table-layout:auto"}

   - Per modificare **[!UICONTROL Applicable Shipping Methods]** disponibili per la società, deselezionare la casella di controllo **[!UICONTROL Use config settings]** e scegliere una delle opzioni seguenti:

     | Opzione | Descrizione |
     |--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Shipping Methods` | (Impostazione predefinita) Abilita tutti i [metodi di spedizione impostati come predefiniti](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods) per gli ordini B2B. |
     | `All Enabled Shipping Methods` | Rende disponibili tutti i [metodi di spedizione abilitati](../configuration-reference/sales/delivery-methods.md) per gli account cliente associati all&#39;account società. |
     | `Selected Shipping Methods` | Consente di selezionare i metodi di spedizione disponibili per gli account cliente associati all&#39;account società. Per selezionare più metodi di spedizione, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e selezionare ciascuna opzione. |

     {style="table-layout:auto"}

1. Al termine, selezionare **[!UICONTROL Save]**.

   Quando la richiesta di creazione di un account aziendale viene approvata dall’esercente, viene inviata una notifica e-mail all’indirizzo e-mail dell’amministratore della società.

   Una volta impostata la password, l&#39;amministratore della società può [accedere](../customers/customer-sign-in.md) all&#39;account.

## Barra dei pulsanti

| Pulsante | Descrizione |
|---------------------------|------------------------------------------------------------------|
| [!UICONTROL Back] | Torna alla pagina Società senza salvare le modifiche. |
| [!UICONTROL Reset] | Ripristina i valori originali in tutti i campi con modifiche non salvate. |
| [!UICONTROL Save] | Salva le modifiche all&#39;azienda e mantiene aperto il profilo. |
| [!UICONTROL Save & Close] | Salva le modifiche all&#39;azienda e chiude il profilo. |

{style="table-layout:auto"}

## Descrizioni dei campi

| Campo | Descrizione |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | Il nome della società viene immesso al momento della creazione dell&#39;account della società e può essere una versione ridotta della ragione sociale completa. |
| [!UICONTROL Status] | (Solo amministratore) indica lo stato corrente dell’account aziendale. Opzioni: <br/>**[!UICONTROL Active]**- L&#39;account società è approvato dall&#39;amministratore dello store. L’amministratore della società e i membri associati possono accedere all’account dalla vetrina e effettuare acquisti.<br/>**[!UICONTROL Pending Approval]** - Una richiesta di apertura di un account società è stata inviata, ma non è ancora stata approvata dall&#39;amministratore dello store. <br/>**[!UICONTROL Rejected]**- Richiesta di apertura di un account società inviata, ma non approvata dall&#39;amministratore dello store. Le credenziali di accesso iniziali utilizzate per inviare la richiesta sono bloccate.<br/>** Bloccato **- I membri della società possono accedere al catalogo e accedervi, ma non possono effettuare acquisti. L’amministratore dello store potrebbe bloccare un account aziendale che non è in buono stato. Il blocco sull’account può essere rimosso dall’amministratore dello store in qualsiasi momento. |
| [!UICONTROL Company Email] | L’indirizzo e-mail associato all’account aziendale. |
| [!UICONTROL Sales Representative] | (Solo amministratore) L’utente amministratore che è il contatto principale per l’account aziendale. |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| Campo | Descrizione |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | La ragione sociale completa della società. |
| [!UICONTROL VAT / TAX ID] | Il numero [imposta sul valore aggiunto](../stores-purchase/vat.md) assegnato alla società da alcune giurisdizioni a scopo di dichiarazione fiscale. Per configurare l&#39;ID IVA/IVA cliente in modo che venga visualizzato nella vetrina, vedere [Crea nuove opzioni account](../configuration-reference/customers/customer-configuration.md). <br/> **_Nota:_** l&#39;amministratore della società e gli altri utenti della società non dispongono di numeri identificativi IVA/FISCALE separati nei propri account cliente. |
| [!UICONTROL Reseller ID] | Numero di rivendita assegnato alla società a scopo di dichiarazione fiscale. |
| [!UICONTROL Comment] | (Solo amministratori) Queste note sull’account aziendale sono da consultare e sono visibili solo dall’amministratore. |

{style="table-layout:auto"}

### [!UICONTROL Company Hierarchy]

| Campo | Descrizione |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Il numero ID della società. |
| [!UICONTROL Company Name] | Il nome completo della società. <br/>Un `current company indicator` viene visualizzato nella riga società in fase di modifica. |
| [!UICONTROL Company Email] | L’indirizzo e-mail associato all’account aziendale. |
| [!UICONTROL Phone Number] | Il numero di telefono principale della società. |
| [!UICONTROL Country] | Il paese in cui la società è registrata per condurre gli affari. |
| [!UICONTROL State/Province] | Lo stato o la provincia in cui la società è registrata per condurre affari. |
| [!UICONTROL City] | La città in cui la società è registrata per condurre gli affari. |
| [!UICONTROL Group/Shared Catalog] | (Solo amministratore) indica il [gruppo di clienti](../customers/customer-groups.md) o il [catalogo condiviso](catalog-shared.md) assegnato alla società. |
| [!UICONTROL Company Admin] | Nome completo dell&#39;amministratore della società. |
| [!UICONTROL Action] | L’elenco delle azioni possibili per quella riga aziendale. |

{style="table-layout:auto"}

### [!UICONTROL Legal Address]

| Campo | Descrizione |
|------------------------------|-----------------------------------------------------------------------------|
| [!UICONTROL Street Address] | Indirizzo in cui è registrata la società per la conduzione di affari. |
| [!UICONTROL City] | La città in cui la società è registrata per condurre gli affari. |
| [!UICONTROL Country] | Il paese in cui la società è registrata per condurre gli affari. |
| [!UICONTROL State/Province] | Lo stato o la provincia in cui la società è registrata per condurre affari. |
| [!UICONTROL ZIP/Postal Code] | Il codice postale o ZIP in cui la società è registrata per condurre affari. |
| [!UICONTROL Phone Number] | Il numero di telefono principale della società. |

{style="table-layout:auto"}

### [!UICONTROL Company Admin]

| Campo | Descrizione |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | Determina il sito Web a cui appartiene l&#39;amministratore della società. |
| [!UICONTROL Job Title] | Titolo dell&#39;amministratore della società che gestisce l&#39;account della società. |
| [!UICONTROL Work Phone Number] | Numero di telefono dell&#39;amministratore della società che gestisce l&#39;account della società. |
| [!UICONTROL Email] | L’indirizzo e-mail dell’amministratore della società può essere lo stesso dell’indirizzo e-mail della società. Se si immette un indirizzo e-mail diverso, viene creato un account individuale separato per l’amministratore della società, oltre all’account aziendale. |
| [!UICONTROL Prefix] | Se applicabile, il prefisso associato al nome dell&#39;amministratore della società (ad esempio `Mr.`, `Ms.`, `Mrs.` o `Dr.`). A seconda della configurazione, il campo di input potrebbe essere un campo di testo o un elenco. |
| [!UICONTROL First Name] | Nome dell&#39;amministratore della società. |
| [!UICONTROL Middle Name/Initial] | Secondo nome o iniziale dell&#39;amministratore della società. |
| [!UICONTROL Last Name] | Cognome dell&#39;amministratore della società. |
| [!UICONTROL Suffix] | Se applicabile, il suffisso associato al nome dell&#39;amministratore della società (ad esempio `Jr.`, `Sr.` o `III.`). A seconda della configurazione, il campo di input potrebbe essere un campo di testo o un elenco. |
| [!UICONTROL Gender] | Genere dell&#39;amministratore della società. Opzioni: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | Visualizzazione dello store da cui deve essere inviato il messaggio e-mail di benvenuto. |

{style="table-layout:auto"}

### [!UICONTROL Company Credit]

| Campo | Descrizione |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | (Solo amministratori) Valuta accettata dal punto vendita per gli acquisti a credito della società. |
| [!UICONTROL Credit Limit] | (Solo amministratori) Limite di credito esteso al conto aziendale. |
| [!UICONTROL Allow to Exceed Credit Limit] | (Solo amministratori) indica se l’azienda dispone dell’autorizzazione per superare il limite di credito. Opzioni: `Yes` / `No` |
| [!UICONTROL Reason for Change] | (Solo amministratori) Una nota che spiega perché alla società è consentito o non è consentito superare il limite di credito. Questo campo è attivo solo se cambia l’autorizzazione per il superamento del limite di credito. |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

| Campo | Descrizione |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | (Solo amministratore) indica il [gruppo di clienti](../customers/customer-groups.md) o il [catalogo condiviso](catalog-shared.md) assegnato alla società. |
| [!UICONTROL Allow Quotes] | (Solo amministratore) Determina se i membri della società possono preparare e inviare preventivi negoziabili per conto della società. |
| [!UICONTROL Enable Purchase Orders] | (Solo amministratore) Determina se i membri della società possono inviare ordini come [ordini di acquisto](account-dashboard-my-purchase-orders.md) per conto della società. |
| Metodi di pagamento applicabili | (Solo amministratori) indica i metodi di pagamento disponibili per gli acquisti aziendali. Opzioni: `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods` |
| [!UICONTROL Payment Methods] | (Solo amministratori) diventa attivo se sono attivati metodi di pagamento specifici. Per rendere disponibili più metodi di pagamento per l&#39;account aziendale, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e selezionare ciascuna opzione. |
| [!UICONTROL Applicable Shipping Methods] | (Solo amministratori) indica i metodi di spedizione disponibili per gli acquisti aziendali. Opzioni: `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | (Solo amministratori) diventa attivo se sono attivati metodi di spedizione specifici. Per rendere disponibili più metodi di pagamento per l&#39;account aziendale, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e selezionare ciascuna opzione. |

{style="table-layout:auto"}
