---
title: Gestisci credito società
description: Scopri le linee di credito della società, l’impostazione dei parametri e l’elaborazione dei pagamenti in conto.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# Gestisci credito società

Se nella configurazione è abilitato [Pagamento in conto](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account), le società possono effettuare acquisti in conto fino al limite di credito concesso alla società. Quando questa opzione è abilitata, i clienti possono controllare lo stato del credito della loro azienda dal dashboard dei conti.

![Credito società](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

È possibile impostare i seguenti parametri relativi al credito per ciascun profilo società:

- Divisa credito
- Limite di credito
- Consenti di superare il limite di credito
- Motivo della modifica

Se la società presenta un saldo scoperto, viene visualizzato un avviso all&#39;amministratore del negozio nella parte superiore dell&#39;ordine di vendita quando viene visualizzato dall&#39;amministratore. Per ulteriori informazioni, consulta [Creare un account aziendale](account-company-create.md).

## Attività di credito società

Nella sezione [!UICONTROL Company Credit] del profilo società viene visualizzato un riepilogo dell&#39;attività di credito del cliente, con una griglia della cronologia credito della società.

![Attività di credito aziendale](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Date] | Data della transazione. Per visualizzare la data e l’ora, passa il cursore del mouse sulla data. |
| [!UICONTROL Operation] | Tipo di attività associata alla transazione. Valori: <br/>**[!UICONTROL Allocated]**- Credito assegnato alla società.<br/>**[!UICONTROL Updated]** - Modifica applicata a uno dei campi seguenti: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- È stato effettuato un ordine.<br/>**[!UICONTROL Reimbursed]** - Il saldo in sospeso è stato rimborsato. <br/>**[!UICONTROL Refunded]**- Rimborso di un importo della nota di accredito.<br/>**[!UICONTROL Reverted]** - L&#39;ordine è stato annullato e l&#39;importo è stato restituito al saldo a credito. |
| [!UICONTROL Amount] | Importo della transazione associata ai seguenti tipi di transazione: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>Per gli importi di acquisto, l&#39;importo viene visualizzato nella valuta di visualizzazione del punto vendita e nel formato dell&#39;impostazione della valuta di credito, seguito dal tasso di conversione corrente (se applicabile). Ad esempio: <br/>EUR 20.000,00 ($22.400,00) <br/>USD/EUR 0,8928 |
| [!UICONTROL Outstanding Balance] | Importo rimborsato, meno il totale dovuto per tutti gli ordini effettuati utilizzando il metodo di pagamento in conto. L’importo può apparire come un valore positivo o negativo. <br/>**[!UICONTROL Positive value]**- Un pagamento anticipato è rappresentato come valore positivo.<br/>**[!UICONTROL Negative value]** - Un importo dovuto è rappresentato come valore negativo. |
| [!UICONTROL Available Credit] | La somma di _[!UICONTROL Credit Limit]_e_[!UICONTROL Outstanding Balance]_. Se l&#39;azienda ha superato il limite di credito, l&#39;importo viene visualizzato come valore negativo. |
| [!UICONTROL Credit Limit] | Importo del credito concesso alla società. |
| [!UICONTROL Updated By] | Nome della persona che ha avviato l&#39;operazione. |
| [!UICONTROL Custom Reference Number] | Numero di riferimento personalizzato associato alla transazione. |
| [!UICONTROL Comment] | Una compilazione dei valori del campo `Reason for Change`, in base al tipo di operazione. <br/>**[!UICONTROL Purchased]**- Include i commenti dell&#39;acquisto, il numero dell&#39;ordine e il collegamento all&#39;ordine.<br/>**[!UICONTROL Reimbursed]** - Include i commenti della transazione rimborsata. |
| [!UICONTROL Action] | Solo per operazioni `Reimbursed`. **[!UICONTROL Edit]** - Consente di aggiornare l&#39;importo del rimborso. |

{style="table-layout:auto"}

## Aggiornare le informazioni sul credito

Quando il cliente effettua il pagamento del credito in essere all&#39;esercente, l&#39;amministratore del negozio deve quindi aggiornare le informazioni sul credito del cliente nell&#39;amministratore.

1. Nella barra laterale _Amministratore_, vai a **Clienti > Aziende**.

1. Trova la società nella griglia e apri in modalità _Modifica_.

1. Espandi la sezione **Credito società**.

1. Per **Limite di credito**, immettere il nuovo valore.

1. Modificare gli altri valori in base alle esigenze.

1. Al termine degli aggiornamenti, fare clic su **[!UICONTROL Save]**.

## Ricevi pagamenti

Un saldo rimborsato è un pagamento offline effettuato da una società verso il saldo del proprio conto. L&#39;amministratore dello store immette manualmente l&#39;importo nel profilo della società utilizzando il pulsante _Saldo rimborso_. Quando l&#39;importo viene sottomesso, il sistema ricalcola il saldo in sospeso e il credito della società disponibile e registra l&#39;azione nella cronologia dei crediti della società. L&#39;importo rimborsato viene inserito nella valuta del credito, come specificato nella configurazione.

### Applicare un pagamento a un account società

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Trovare il record società nell&#39;elenco e aprirlo in modalità **[!UICONTROL Edit]**.

1. Nella parte superiore della pagina, fai clic su **Saldo rimborso**.

1. Nella finestra di dialogo, aggiungi le informazioni di pagamento:

   ![Saldo rimborso](./assets/company-reimburse-balance.png){width="500"}

   - Immetti l&#39;**importo** del pagamento.

     L&#39;importo può essere inserito come valore positivo o negativo.

   - Se applicabile, immettere il **Numero di riferimento personalizzato** per riferimento.

     È possibile inserire un solo numero di riferimento personalizzato per rimborso. Per applicare il pagamento a più OA, creare un rimborso separato per ciascuno di essi.

   - Se necessario, immetti un **commento** per descrivere il rimborso.

1. Fai clic su **Rimborso**.

   Il saldo in sospeso e il credito disponibile della società vengono ricalcolati e la cronologia del credito della società viene aggiornata per riflettere il rimborso.

### Modificare un rimborso

1. Aprire il profilo società in modalità **[!UICONTROL Edit]**.

1. Espandi ![il selettore di espansione](../assets/icon-display-expand.png) nella sezione **Credito società**.

1. Trovare la transazione di rimborso nella griglia e fare clic su **[!UICONTROL Edit]**.

1. Apportare le modifiche necessarie a **Numero di riferimento personalizzato** e **Commento**.

   L&#39;importo del rimborso non può essere modificato.

1. Fare clic su **[!UICONTROL Save]**.

## Informazioni sul credito Storefront

Per l&#39;amministratore della società, nel dashboard account viene visualizzata la sezione _Credito società_. Fornisce il saldo in sospeso corrente, il credito disponibile e il limite di credito allocato al conto della società seguito da un elenco di fatture in sospeso.

Se il commerciante annulla un ordine addebitato al credito aziendale, l&#39;importo dell&#39;ordine viene restituito al saldo della società e la _cronologia allocazioni credito_ include un record dell&#39;azione.

![Credito società](./assets/company-credit.png){width="700" zoomable="yes"}

## Demo sul credito aziendale

Scopri come gestire il credito aziendale guardando questo video dimostrativo:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12)
