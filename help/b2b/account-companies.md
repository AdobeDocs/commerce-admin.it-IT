---
title: Account società
description: Scopri in che modo gli account aziendali gestiti nel tuo store di Adobe Commerce consentono di unire più acquirenti che appartengono alla stessa azienda in un unico account aziendale.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Account società

Quando incorpori account aziendali B2B nel tuo negozio, puoi semplificare l’esperienza di acquisto aziendale consentendo alle aziende di creare più account secondari con autorizzazioni flessibili in base ai ruoli utente nella loro organizzazione.

Depending on the company, a store administrator can adjust promotions and prices to suit their needs, and create highly customized offers that cater to the shoppers&#39; demands and increase orders.

L&#39;aggiunta di un&#39;associazione di account società a un [individuo](../customers/account-create.md) standard consente al cliente di utilizzare i flussi di lavoro di acquisto specifici definiti per la società.

Vantaggi di un account aziendale:

- Offre [utenti aziendali](account-company-users.md) illimitati e la creazione di account aggiuntivi, semplificando gli acquisti aziendali.

- Include il supporto per una gerarchia di account aziendali _smart_ con [ruoli e autorizzazioni](account-company-roles-permissions.md) diversi per l&#39;invio di ordini.

- Fornisce un meccanismo che consente ai commercianti di aumentare le entrate offrendo [credito del negozio aziendale](credit-company.md) come metodo di pagamento.

- [&#128279;](account-company-manage.md)

## View company accounts

__ [&#128279;](account-company-create.md) [&#128279;](account-company-manage.md) Utilizzare i controlli griglia standard per filtrare l&#39;elenco e modificare il layout delle colonne. Per un elenco delle descrizioni delle colonne, vedere la sezione _Descrizioni colonne_ in [Gestione degli account società](account-company-manage.md).

I clienti possono creare un account aziendale dalla vetrina, oppure un commerciante può crearne uno dall’amministratore. Per impostazione predefinita, la possibilità di creare account società dalla vetrina è abilitata. If allowed by the configuration, a visitor to the store can request to open a company account. After the company account is approved, the company administrator can set up the company structure and users with various levels of permission.

__&#x200B;**[!UICONTROL Customers]**&#x200B;**[!UICONTROL Companies]**

![](./assets/companies-grid.png){width="700" zoomable="yes"}

[!UICONTROL Companies] [&#128279;](manage-company-hierarchy.md) [&#128279;](/help/b2b/account-company-manage.md#company-options-and-columns) [&#128279;](../getting-started/admin-grid-controls.md)

## Amministratore società

L&#39;esempio seguente mostra la griglia _Clienti_ con gli account iniziali dell&#39;amministratore della società.

![Griglia clienti con account amministratore società](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Ogni società dispone di un amministratore unico identificato dall’indirizzo e-mail dell’account e dal nome e cognome dell’amministratore. The administrator can be assigned to other companies as a user, but they can be an administrator for only one company.

[&#128279;](account-company-structure.md) [&#128279;](account-company-users.md) [&#128279;](account-company-roles-permissions.md)

### Imposta la password dell&#39;amministratore della società prima del primo accesso

1. L’amministratore della società trova un messaggio e-mail di benvenuto dallo store.

   ![E-mail di benvenuto di esempio](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >Le destinazioni degli indirizzi e-mail e il contenuto dell&#39;e-mail sono determinati dalle opzioni specificate nella configurazione [opzioni e-mail società](email-company-configuration.md).

1. Segue le istruzioni e fa clic su [!UICONTROL **link**] per impostare la password.

1. Immette una [!UICONTROL **nuova password**] e una password di conferma per il proprio account.

   The password must include at least three of the following character types:

   - Lowercase characters (abc...)
   - Caratteri maiuscoli (ABC)
   - Numeri (1234567890)
   - Caratteri speciali (!@#$...)

1. [!UICONTROL **&#x200B;**]

   ![](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. [!UICONTROL Customer Login]&#x200B;[!UICONTROL **&#x200B;**]&#x200B;[!UICONTROL **&#x200B;**]

1. [!UICONTROL **&#x200B;**]

   ![](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Struttura aziendale

È possibile impostare un conto aziendale per riflettere la struttura dell&#39;attività. Inizialmente, la struttura aziendale include solo l’amministratore della società, ma può essere espansa per includere i team di utenti. Gli utenti possono essere associati a team o organizzati all’interno di una gerarchia di divisioni e suddivisioni all’interno dell’azienda. La struttura è progettata per supportare l&#39;utilizzo di [regole di approvazione](account-dashboard-approval-rules.md) per [ordini fornitore](purchase-order-flow.md) (OA) associati all&#39;account società.

![](./assets/company-structure-diagram.svg){width="450"}

In the company administrator&#39;s account dashboard, the company structure is represented as a tree and initially consists of only the company administrator.

![Struttura della società con amministratore della società](./assets/company-structure-tree-admin.png){width="600"}

When the account is created, the company administrator can use the company email address or be assigned a different email address.

Nell&#39;esempio seguente, la struttura aziendale iniziale include l&#39;amministratore della società più un singolo account utente nel nome dell&#39;amministratore della società. But company administrator functions (such as company structure and approval rules) are available only when they are logged in to the user account that is designated as the company administrator.

![Struttura della società con account amministratore e utente](./assets/company-structure-tree-admin-user.png){width="600"}
