---
title: Account società
description: Scopri in che modo gli account aziendali gestiti nel tuo store di Adobe Commerce consentono di unire più acquirenti che appartengono alla stessa azienda in un unico account aziendale.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Account società

Quando incorpori account aziendali B2B nel tuo negozio, puoi semplificare l’esperienza di acquisto aziendale consentendo alle aziende di creare più account secondari con autorizzazioni flessibili in base ai ruoli utente nella loro organizzazione. A seconda dell&#39;azienda, l&#39;amministratore del negozio può modificare le promozioni e i prezzi in base alle esigenze, e creare offerte personalizzate in base alle esigenze e agli ordini. Aggiunta di un&#39;associazione di account società a uno standard [singolo](../customers/account-create.md) consente al cliente di utilizzare i flussi di lavoro di acquisto specifici definiti per l’azienda.

Vantaggi di un account aziendale:

- Offerte illimitate [utenti società](account-company-users.md) e la creazione di conti aggiuntivi, che semplifica gli acquisti aziendali.

- Include il supporto per _intelligente_ gerarchia di conti società con diversi [ruoli e autorizzazioni](account-company-roles-permissions.md) per effettuare ordini.

- Fornisce un meccanismo per gli esercenti per aumentare il reddito offrendo [credito negozio società](credit-company.md) come metodo di pagamento.

- Supporta [gestione](account-company-manage.md) di tutti gli account aziendali nell’amministratore.

## Visualizza account società

Il _Aziende_ nella griglia sono elencati tutti gli account società attivi e le richieste in sospeso, indipendentemente dall&#39;impostazione dello stato. Fornisce inoltre gli strumenti per [creazione](account-company-create.md) e [gestione](account-company-manage.md) account aziendali. Utilizzare i controlli griglia standard per filtrare l&#39;elenco e modificare il layout delle colonne. Per un elenco delle descrizioni delle colonne, vedere _Descrizioni colonne_ sezione in [Gestione degli account aziendali](account-company-manage.md).

I clienti possono creare un account aziendale dalla vetrina, oppure un commerciante può crearne uno dall’amministratore. Per impostazione predefinita, la possibilità di creare account società dalla vetrina è abilitata. Se consentito dalla configurazione, un visitatore dello store può richiedere di aprire un account aziendale. Dopo l’approvazione dell’account aziendale, l’amministratore dell’azienda può impostare la struttura aziendale e gli utenti con vari livelli di autorizzazione.

In _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Griglia Aziende](./assets/companies-grid.png){width="700" zoomable="yes"}

Il [!UICONTROL Companies] grid elenca tutte le aziende indipendentemente dallo stato. L’esempio visualizzato mostra gli account per due società: la società &quot;ACME&quot; e la società &quot;Vandelay&quot;.

## Amministratore società

L&#39;esempio seguente mostra _Clienti_ griglia con gli account iniziali dell&#39;amministratore della società.

![Griglia clienti con account amministratore società](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

È possibile che la persona che funge da amministratore dell’azienda abbia più ruoli all’interno dell’azienda. Se per l&#39;amministratore della società viene immesso un indirizzo e-mail distinto, la struttura aziendale iniziale include l&#39;amministratore della società più un account utente singolo a nome dell&#39;amministratore della società. In tal caso, l’amministratore della società può accedere all’account come società o come singolo utente.

Dopo aver creato l’account, l’amministratore della società definisce la struttura aziendale di [team](account-company-structure.md), imposta [utenti società](account-company-users.md), e stabilisce [ruoli e autorizzazioni](account-company-roles-permissions.md) per ciascuno.

### Imposta la password dell&#39;amministratore della società prima del primo accesso

1. L’amministratore della società trova un messaggio e-mail di benvenuto dallo store.

   ![Esempio di e-mail di benvenuto](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >Le destinazioni degli indirizzi e-mail e il contenuto dell’e-mail sono determinati dalle opzioni specificate nella [opzioni e-mail società](email-company-configuration.md) configurazione.

1. Segue le istruzioni e i clic [!UICONTROL **link**] per impostare la password.

1. Immette un valore [!UICONTROL **Nuova password**] per il loro account e di nuovo per confermare.

   La password deve includere almeno tre dei seguenti tipi di caratteri:

   - Caratteri minuscoli (abc...)
   - Caratteri maiuscoli (ABC)
   - Numeri (1234567890)
   - Caratteri speciali (!@#$...)

1. Clic [!UICONTROL **Imposta una nuova password**].

   ![Accesso cliente - Amministratore società](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. Quando [!UICONTROL Customer Login] pagina, il cliente immette il proprio [!UICONTROL **E-mail**] e [!UICONTROL **Password**].

1. Clic [!UICONTROL **Accedi**] per accedere al dashboard dell’account.

   ![Dashboard account - Società](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Struttura aziendale

È possibile impostare un conto aziendale per riflettere la struttura dell&#39;attività. Inizialmente, la struttura aziendale include solo l’amministratore della società, ma può essere espansa per includere i team di utenti. Gli utenti possono essere associati a team o organizzati all’interno di una gerarchia di divisioni e suddivisioni all’interno dell’azienda. La struttura è progettata per supportare l&#39;uso di [regole di approvazione](account-dashboard-approval-rules.md) per [ordini fornitore](purchase-order-flow.md) (OA) associate al conto della società.

![Struttura societaria con divisioni](./assets/company-structure-diagram.svg){width="450"}

Nel dashboard degli account dell’amministratore della società, la struttura della società è rappresentata da una struttura ad albero ed è inizialmente costituita solo dall’amministratore della società.

![Struttura aziendale con amministratore società](./assets/company-structure-tree-admin.png){width="600"}

Al momento della creazione dell’account, l’amministratore della società può utilizzare l’indirizzo e-mail della società o riceverne uno diverso.

Nell&#39;esempio seguente, la struttura aziendale iniziale include l&#39;amministratore della società più un singolo account utente nel nome dell&#39;amministratore della società. Tuttavia, le funzioni di amministratore della società (come la struttura della società e le regole di approvazione) sono disponibili solo quando si accede all’account utente designato come amministratore della società.

![Struttura aziendale con account amministratore e utente](./assets/company-structure-tree-admin-user.png){width="600"}
