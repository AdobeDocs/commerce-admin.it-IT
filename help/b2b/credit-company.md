---
title: Gestisci credito società
description: Scopri le linee di credito della società, l’impostazione dei parametri e l’elaborazione dei pagamenti in conto.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Gestisci credito società

Se [Pagamento in acconto](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) è abilitato nella configurazione, le aziende possono effettuare acquisti sul loro conto fino al limite di credito concesso alla società. Quando questa opzione è abilitata, i clienti possono controllare lo stato del credito della loro azienda dal dashboard dei conti.

![Credito società](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

È possibile impostare i seguenti parametri relativi al credito per ciascun profilo società:

- Divisa credito
- Limite di credito
- Consenti di superare il limite di credito
- Motivo della modifica

Se la società presenta un saldo scoperto, viene visualizzato un avviso all&#39;amministratore del negozio nella parte superiore dell&#39;ordine di vendita quando viene visualizzato dall&#39;amministratore. Per ulteriori informazioni, consulta [Creare un account società](account-company-create.md).

## Attività di credito società

Il [!UICONTROL Company Credit] nella sezione del profilo società viene visualizzato un riepilogo dell&#39;attività credito cliente, con una griglia della cronologia credito società.

![Attività di credito società](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Date] | Data della transazione. Per visualizzare la data e l’ora, passa il cursore del mouse sulla data. |
| [!UICONTROL Operation] | Tipo di attività associata alla transazione. Valori: <br/>**[!UICONTROL Allocated]**- Credito assegnato alla società.<br/>**[!UICONTROL Updated]** - È stata applicata una modifica a uno dei seguenti campi: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- È stato effettuato un ordine.<br/>**[!UICONTROL Reimbursed]** - Il saldo restante è stato rimborsato. <br/>**[!UICONTROL Refunded]**- Importo della nota di accredito rimborsato.<br/>**[!UICONTROL Reverted]** - L&#39;ordine è stato annullato e l&#39;importo è stato riportato al saldo del credito. |
| [!UICONTROL Amount] | Importo della transazione associata ai seguenti tipi di transazione: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>Per gli importi di acquisto, l’importo viene visualizzato nella valuta di visualizzazione del negozio e nel formato dell’impostazione della valuta di credito, seguito dal tasso di conversione corrente (se applicabile). Ad esempio: <br/>20.000,00 EUR ($22.400,00) <br/>USD/EUR 0,8928 |
| [!UICONTROL Outstanding Balance] | Importo rimborsato, meno il totale dovuto per tutti gli ordini effettuati utilizzando il metodo di pagamento in conto. L’importo può apparire come un valore positivo o negativo. <br/>**[!UICONTROL Positive value]**- Un acconto è rappresentato da un valore positivo.<br/>**[!UICONTROL Negative value]** - Un importo dovuto è rappresentato da un valore negativo. |
| [!UICONTROL Available Credit] | La somma dei _[!UICONTROL Credit Limit]_e_[!UICONTROL Outstanding Balance]_. Se l&#39;azienda ha superato il limite di credito, l&#39;importo viene visualizzato come valore negativo. |
| [!UICONTROL Credit Limit] | Importo del credito concesso alla società. |
| [!UICONTROL Updated By] | Nome della persona che ha avviato l&#39;operazione. |
| [!UICONTROL Custom Reference Number] | Numero di riferimento personalizzato associato alla transazione. |
| [!UICONTROL Comment] | Una compilazione dei valori dalla sezione `Reason for Change` in base al tipo di operazione. <br/>**[!UICONTROL Purchased]**- Include i commenti dell&#39;acquisto, il numero dell&#39;ordine e il link all&#39;ordine.<br/>**[!UICONTROL Reimbursed]** - Comprende le osservazioni relative all&#39;operazione rimborsata. |
| [!UICONTROL Action] | Per `Reimbursed` solo operazioni. **[!UICONTROL Edit]** - Consente di aggiornare l&#39;importo del rimborso. |

{style="table-layout:auto"}

## Aggiornare le informazioni sul credito

Quando il cliente effettua il pagamento del credito in essere all&#39;esercente, l&#39;amministratore del negozio deve quindi aggiornare le informazioni sul credito del cliente nell&#39;amministratore.

1. Il giorno _Amministratore_ barra laterale, vai a **Clienti > Aziende**.

1. Trova la società nella griglia e apri in _Modifica_ modalità.

1. Espandi **Credito società** sezione.

1. Per **Limite di credito**, immetti il nuovo valore.

1. Modificare gli altri valori in base alle esigenze.

1. Al termine degli aggiornamenti, fai clic su **[!UICONTROL Save]**.

## Ricevi pagamenti

Un saldo rimborsato è un pagamento offline effettuato da una società verso il saldo del proprio conto. L’amministratore dello store immette manualmente l’importo nel profilo aziendale utilizzando _Saldo rimborso_ pulsante. Quando l&#39;importo viene sottomesso, il sistema ricalcola il saldo in sospeso e il credito della società disponibile e registra l&#39;azione nella cronologia dei crediti della società. L&#39;importo rimborsato viene inserito nella valuta del credito, come specificato nella configurazione.

### Applicare un pagamento a un account società

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Trova il record azienda nell’elenco e apri in **[!UICONTROL Edit]** modalità.

1. Nella parte superiore della pagina, fai clic su **Saldo rimborso**.

1. Nella finestra di dialogo, aggiungi le informazioni di pagamento:

   ![Saldo rimborso](./assets/company-reimburse-balance.png){width="500"}

   - Inserisci il **Quantità** del pagamento.

     L&#39;importo può essere inserito come valore positivo o negativo.

   - Se applicabile, inserire **Numero di riferimento personalizzato** per riferimento.

     È possibile inserire un solo numero di riferimento personalizzato per rimborso. Per applicare il pagamento a più OA, creare un rimborso separato per ciascuno di essi.

   - Se necessario, immetti un **Commento** descrivere il rimborso.

1. Clic **Rimborso**.

   Il saldo in sospeso e il credito disponibile della società vengono ricalcolati e la cronologia del credito della società viene aggiornata per riflettere il rimborso.

### Modificare un rimborso

1. Apri il profilo aziendale in **[!UICONTROL Edit]** modalità.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **Credito società** sezione.

1. Trovare la transazione di rimborso nella griglia e fare clic su **[!UICONTROL Edit]**.

1. Apporta le modifiche necessarie per **Numero di riferimento personalizzato** e **Commento**.

   L&#39;importo del rimborso non può essere modificato.

1. Clic **[!UICONTROL Save]**.

## Informazioni sul credito Storefront

Per l’amministratore della società, nel dashboard dell’account viene visualizzato _Credito società_ sezione. Fornisce il saldo in sospeso corrente, il credito disponibile e il limite di credito allocato al conto della società seguito da un elenco di fatture in sospeso.

Se il commerciante annulla un ordine addebitato al credito aziendale, l&#39;importo dell&#39;ordine viene restituito al saldo aziendale e al _Cronologia allocazione credito_ include un record dell’azione.

![Credito società](./assets/company-credit.png){width="700" zoomable="yes"}

## Demo sul credito aziendale

Scopri come gestire il credito aziendale guardando questo video dimostrativo:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12)
