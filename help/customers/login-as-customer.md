---
title: Fornire assistenza agli acquirenti
description: Quando utilizzi la funzione Login as a Customer (Accesso come cliente), puoi vedere cosa vedono i clienti e apportare aggiornamenti per loro conto.
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Fornire assistenza agli acquirenti

A volte, i clienti hanno bisogno di assistenza per il loro ordine. Gli amministratori del negozio possono utilizzare _Accedi come cliente_, che consente loro di vedere cosa vede il cliente e di apportare aggiornamenti per assisterlo.

Tutte le azioni intraprese durante l’accesso come cliente vengono applicate all’account del cliente effettivo.

Quando è abilitato per un _Amministratore_ utente, il _[!UICONTROL Login as Customer]_Il pulsante viene visualizzato in più pagine:

* [Pagina Modifica cliente](../customers/update-account.md)
* [Pagina Vista ordine](../stores-purchase/order-processing.md)
* [Pagina Visualizzazione fattura](../stores-purchase/invoices.md)
* [Pagina Visualizzazione spedizione](../stores-purchase/shipments.md)
* [Pagina di visualizzazione nota di credito](../stores-purchase/credit-memo-create.md)

![Accedi come cliente](assets/login-as-customer.png){width="600" zoomable="yes"}

## Abilita accesso come cliente

Abilitazione _Accedi come cliente_ richiede l’abilitazione della funzione nell’istanza Commerce e quindi l’accesso per gli utenti Admin nelle autorizzazioni del ruolo utente.

### Abilita la funzione

1. Nella barra laterale Amministratore, vai a  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli  **[!UICONTROL Login as Customer]**.

   ![Opzioni di configurazione - Accedi come cliente](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enable Login as Customer]** a `Yes`.

1. _(Facoltativo)_ Imposta **[!UICONTROL Disable Page Cache for Admin User]** a `No` per abilitare la cache delle pagine quando l’utente Admin accede come cliente.

   >[!WARNING]
   >
   > Disabilitazione della cache delle pagine (`Yes` : impostazione predefinita) garantisce che l’utente che accede come cliente riceva dati aggiornati e non memorizzati nella cache.

1. _(Facoltativo)_ Imposta **[!UICONTROL Store View to Log in]** a `Manual Selection` se disponi di una configurazione per più siti e/o store e desideri che l’utente amministratore selezioni la vista store quando accedi come cliente.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Abilitare l’accesso per gli utenti amministratori

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _Autorizzazioni_ > **[!UICONTROL User Roles]**.

1. Fare clic sul ruolo nell&#39;elenco.

1. In [!UICONTROL _Informazioni ruolo_] pannello a sinistra, fai clic su **[!UICONTROL Role Resources]**.

1. Cambia **[!UICONTROL Role Resources]** sulla pagina per `Custom`.

   >[!INFO]
   >
   > Quando questa opzione è selezionata, nella pagina viene visualizzata la gerarchia delle risorse.

1. Scorri fino a  **[!UICONTROL Customers]** elemento padre e **[!UICONTROL Login as Customer]** elemento sottostante. Quindi, seleziona le risorse da abilitare per il ruolo:

   * **[!UICONTROL Allow Login as Customer]** : consente all’utente amministratore di utilizzare _Accedi come cliente_ funzionalità.
   * **[!UICONTROL View Login as Customer Log]** - Consente all&#39;utente amministratore di visualizzare _Accedi come cliente_ Registro.

   ![Risorse per il ruolo - Accedi come cliente](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Clic **[!UICONTROL Save Role]**.

## Accedi come cliente dall’Amministratore

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > [!UICONTROL _Tutti i clienti_].

1. Apri un utente in modalità di modifica.

1. In **[!UICONTROL Customer Information]** , scegliere il **[!UICONTROL Account Information]** sezione.

1. Imposta il **[!UICONTROL Allow remote shopping assistance]** a `Yes`.

   >[!INFO]
   >
   >L’amministratore può ora accedere come utente senza la sua autorizzazione dalla vetrina.

## Autorizzazione account cliente per assistenza acquisti remoti

Per abilitare l’accesso all’account per il personale di supporto al negozio da parte dell’amministratore, un cliente deve abilitare la funzione per il proprio account:

1. Il cliente accede al **[!UICONTROL Account Information]** pagina.

1. Seleziona il **[!UICONTROL Allow remote shopping assistance]** casella di controllo.

1. Il cliente fa clic **[!UICONTROL Save]**.

![Pagina Informazioni account](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>Senza questa autorizzazione, un utente amministratore non può accedere come questo cliente.

## Usa l&#39;accesso come cliente

>[!INFO]
>
>Da utilizzare _Accedi come cliente_, accertati che l’amministratore sia configurato come descritto in precedenza.

_Accedi come cliente_ consente di visualizzare il sito esattamente come il cliente, nonché di risolvere i problemi e intraprendere altre azioni per il cliente. Se ti è stato assegnato un ruolo utente con le autorizzazioni necessarie:

1. Puoi fare clic su **[!UICONTROL Login as Customer]** nelle pagine elencate nella sezione precedente.
1. Le azioni Accedi come cliente sono disponibili nel rapporto Azioni.

>[!WARNING]
>
>Qualsiasi azione intrapresa durante l’accesso [!UICONTROL _come Cliente_] (ad esempio, aggiungi/rimuovi prodotti) vengono applicati all’ordine del cliente effettivo. Nella vetrina, quando sei `logged in as customer_name` per ricordare lo stato speciale.

## Accedi come registrazione cliente

{{ee-feature}}

Adobe Commerce fornisce una registrazione per _Accedi come cliente_ azioni. Elenca tutte le sessioni in cui un utente amministratore accede alla funzione. Per accedere alle azioni registrate, vai al [Rapporto Azioni amministratore](../systems/action-log-report.md).

È possibile filtrare l’impostazione del rapporto **[!UICONTROL Action Group]** a `Login As Customer` nella parte superiore della pagina e facendo clic su **[!UICONTROL Search]**.

![Filtrare il rapporto Azioni](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
