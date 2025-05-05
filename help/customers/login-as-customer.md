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

A volte, i clienti hanno bisogno di assistenza per il loro ordine. Gli amministratori dello store possono utilizzare _Accedi come cliente_, per consentire loro di visualizzare ciò che vede il cliente e apportare aggiornamenti per assisterlo.

Tutte le azioni intraprese durante l’accesso come cliente vengono applicate all’account del cliente effettivo.

Quando è abilitato per un utente _Admin_, il pulsante _[!UICONTROL Login as Customer]_&#x200B;viene visualizzato in più pagine:

* [Pagina Modifica cliente](../customers/update-account.md)
* [Pagina Vista ordine](../stores-purchase/order-processing.md)
* [Pagina Visualizzazione fattura](../stores-purchase/invoices.md)
* [Pagina Visualizzazione spedizione](../stores-purchase/shipments.md)
* [Pagina di visualizzazione nota di credito](../stores-purchase/credit-memo-create.md)

![Accedi come cliente](assets/login-as-customer.png){width="600" zoomable="yes"}

## Abilita accesso come cliente

Per abilitare _l&#39;accesso come cliente_ è necessario abilitare la funzionalità nell&#39;istanza di Commerce e quindi l&#39;accesso per gli utenti amministratori nelle autorizzazioni del ruolo utente.

### Abilita la funzione

1. Nella barra laterale di amministrazione, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Login as Customer]**.

   ![Opzioni di configurazione - Accesso come cliente](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enable Login as Customer]** su `Yes`.

1. _(Facoltativo)_ Imposta **[!UICONTROL Disable Page Cache for Admin User]** su `No` per abilitare la cache delle pagine quando l&#39;utente amministratore effettua l&#39;accesso come cliente.

   >[!WARNING]
   >
   > La disabilitazione della cache delle pagine (`Yes` - impostazione predefinita) garantisce che l&#39;utente che accede come cliente riceva dati aggiornati e non memorizzati nella cache.

1. _(Facoltativo)_ Impostare **[!UICONTROL Store View to Log in]** su `Manual Selection` se si dispone di una configurazione multisito e/o multisito e si desidera che l&#39;utente amministratore selezioni la visualizzazione archivio quando si effettua l&#39;accesso come cliente.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

### Abilitare l’accesso per gli utenti amministratori

1. Nella barra laterale _Admin_, vai a **[!UICONTROL System]** > _Autorizzazioni_ > **[!UICONTROL User Roles]**.

1. Fare clic sul ruolo nell&#39;elenco.

1. Nel pannello sinistro [!UICONTROL _Informazioni ruolo_], fare clic su **[!UICONTROL Role Resources]**.

1. Cambia **[!UICONTROL Role Resources]** sulla pagina in `Custom`.

   >[!INFO]
   >
   > Quando questa opzione è selezionata, nella pagina viene visualizzata la gerarchia delle risorse.

1. Scorri fino all&#39;elemento padre **[!UICONTROL Customers]** e all&#39;elemento **[!UICONTROL Login as Customer]** sottostante. Quindi, seleziona le risorse da abilitare per il ruolo:

   * **[!UICONTROL Allow Login as Customer]** - Consente all&#39;utente amministratore di utilizzare la funzionalità _Accedi come cliente_.
   * **[!UICONTROL View Login as Customer Log]** - Consente all&#39;utente amministratore di visualizzare il registro _Accedi come cliente_.

   ![Risorse per il ruolo - Accesso come cliente](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. Fare clic su **[!UICONTROL Save Role]**.

## Accedi come cliente dall’Amministratore

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > [!UICONTROL _Tutti i clienti_].

1. Apri un utente in modalità di modifica.

1. Nel pannello **[!UICONTROL Customer Information]** scegliere la sezione **[!UICONTROL Account Information]**.

1. Imposta **[!UICONTROL Allow remote shopping assistance]** su `Yes`.

   >[!INFO]
   >
   >L’amministratore può ora accedere come utente senza la sua autorizzazione dalla vetrina.

## Autorizzazione account cliente per assistenza acquisti remoti

Per abilitare l’accesso all’account per il personale di supporto al negozio da parte dell’amministratore, un cliente deve abilitare la funzione per il proprio account:

1. Il cliente passa alla pagina **[!UICONTROL Account Information]**.

1. Seleziona la casella di controllo **[!UICONTROL Allow remote shopping assistance]**.

1. Il cliente fa clic su **[!UICONTROL Save]**.

![Pagina informazioni account](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>Senza questa autorizzazione, un utente amministratore non può accedere come questo cliente.

## Usa l&#39;accesso come cliente

>[!INFO]
>
>Per utilizzare _Accedi come cliente_, assicurati che l&#39;amministratore sia configurato come descritto in precedenza.

_Accedi come cliente_ ti consente di visualizzare il sito esattamente come il cliente, nonché di risolvere i problemi e intraprendere altre azioni per il cliente. Se ti è stato assegnato un ruolo utente con le autorizzazioni necessarie:

1. È possibile fare clic su **[!UICONTROL Login as Customer]** nelle pagine elencate nella sezione precedente.
1. Le azioni Accedi come cliente sono disponibili nel rapporto Azioni.

>[!WARNING]
>
>Tutte le azioni intraprese durante l&#39;accesso a [!UICONTROL _come cliente_] (ad esempio aggiungere/rimuovere prodotti) vengono applicate all&#39;ordine del cliente effettivo. Nella vetrina viene visualizzato un banner quando sei `logged in as customer_name` per fornire un promemoria dello stato speciale.

## Accedi come registrazione cliente

{{ee-feature}}

Adobe Commerce fornisce una registrazione per le azioni _Accedi come cliente_. Elenca tutte le sessioni in cui un utente amministratore accede alla funzione. Per accedere alle azioni registrate, passare al [Rapporto azioni amministratore](../systems/action-log-report.md).

È possibile filtrare l&#39;impostazione del report **[!UICONTROL Action Group]** su `Login As Customer` nella parte superiore della pagina e fare clic su **[!UICONTROL Search]**.

![Filtra il report delle azioni](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
