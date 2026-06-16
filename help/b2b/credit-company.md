---
title: Gestisci credito società
description: Scopri le linee di credito della società, l’impostazione dei parametri e l’elaborazione dei pagamenti in conto.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
TQID: https://experienceleague.adobe.com/JKyFAE5sOsIyOsM-L73i8fMt8nEeoY2-ZcE321jXjSc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1228
ht-degree: 0%

---

# Gestisci credito società

Il credito aziendale consente alle aziende B2B di effettuare acquisti sulla base di una linea di credito preapprovata, invece di richiedere un pagamento immediato. Quando [Pagamento sul conto](../b2b/enable-basic-features.md#configure-payment-on-account) è abilitato, le aziende possono acquistare fino al limite di credito e visualizzare lo stato del credito dal dashboard del conto.

![Credito società](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

Il credito aziendale consente di:

* **Estendi le condizioni di credito**—Consenti ai clienti aziendali attendibili di effettuare acquisti in acconto con pagamento differito
* **Imposta limiti di credito**—Controlla l&#39;esposizione finanziaria stabilendo limiti di credito per ogni azienda
* **Tieni traccia dell&#39;attività di credito**—Controlla in tempo reale tutte le transazioni di credito, i pagamenti e i saldi in essere
* **Semplificazione delle transazioni B2B**—Semplificazione del processo di acquisto per le aziende con relazioni di credito stabilite
* **Supporto di flussi di lavoro complessi**: integrazione con ordini di acquisto, preventivi e processi di approvazione

## Prerequisiti

Prima di impostare il credito aziendale, verificare che:

* Le funzioni B2B sono abilitate nell’installazione di Adobe Commerce
* [Il pagamento sull&#39;account](../b2b/enable-basic-features.md#configure-payment-on-account) è configurato e abilitato
* Gli account aziendali sono configurati correttamente con le necessarie informazioni commerciali
* Si dispone di autorizzazioni amministrative per gestire le impostazioni di credito della società
* Le impostazioni di valuta sono configurate se si opera in più valute

## Casi d’uso

Il credito aziendale è ideale per:

* **Relazioni B2B consolidate**: clienti aziendali a lungo termine con una comprovata cronologia dei pagamenti
* **Clienti aziendali di grandi dimensioni**—Aziende che effettuano acquisti significativi e regolari che richiedono termini di pagamento estesi
* **Aziende stagionali**—Aziende con un flusso di cassa ciclico che necessitano di tempi di pagamento flessibili
* **Approvvigionamento aziendale**: organizzazioni con centralizzazione degli acquisti ma elaborazione dei pagamenti distribuiti
* **Partner Supply chain**: distributori, rivenditori e partner di canale che richiedono agevolazioni di credito

## Informazioni sulle impostazioni relative al credito della società

Puoi configurare i seguenti parametri relativi al credito per ciascun profilo aziendale:

* **Divisa credito**—Divisa per tutte le transazioni di credito e i saldi
* **Limite di credito**: importo massimo che l&#39;azienda può essere in debito in qualsiasi momento
* **Consenti di superare il limite di credito**— Indica se le società possono effettuare ordini superiori al credito disponibile
* **Motivo della modifica**—Campo della documentazione per la registrazione delle modifiche alle impostazioni di credito

Per informazioni dettagliate su queste impostazioni e sulla configurazione del profilo società, vedere [Creare un account società](account-company-create.md).

>[!NOTE]
>
>Se una società presenta un saldo scoperto, l&#39;amministratore del negozio visualizza un avviso all&#39;inizio degli ordini di vendita quando viene visualizzato dall&#39;amministratore. Questo aiuta a garantire la conoscenza dello stato del credito durante l’elaborazione dell’ordine.

## Attività di credito società

Nella sezione [!UICONTROL Company Credit] del profilo società viene visualizzata una cronologia completa di tutte le transazioni di credito, le modifiche al saldo e le attività di pagamento in un formato griglia.

![Attività di credito aziendale](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

Nella griglia vengono visualizzate le informazioni riportate di seguito per ogni transazione.

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Date] | Data della transazione. Per visualizzare la data e l’ora, passa il cursore del mouse sulla data. |
| [!UICONTROL Operation] | Tipo di attività associata alla transazione. Valori: <br/>**[!UICONTROL Allocated]**- Credito assegnato alla società.<br/>**[!UICONTROL Updated]** - Modifica applicata a uno dei campi seguenti: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- È stato effettuato un ordine.<br/>**[!UICONTROL Reimbursed]** - Il saldo restante è stato rimborsato. <br/>**[!UICONTROL Refunded]**- Rimborso di un importo della nota di accredito.<br/>**[!UICONTROL Reverted]** - L&#39;ordine è stato annullato e l&#39;importo è stato restituito al saldo a credito. |
| [!UICONTROL Amount] | Importo della transazione associata ai seguenti tipi di transazione: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>Per gli importi di acquisto, l&#39;importo viene visualizzato nella valuta di visualizzazione del punto vendita e nel formato dell&#39;impostazione della valuta di credito, seguito dal tasso di conversione corrente (se applicabile). Ad esempio: <br/>EUR 20.000,00 ($22.400,00) <br/>USD/EUR 0,8928 |
| [!UICONTROL Outstanding Balance] | Importo rimborsato, meno il totale dovuto per tutti gli ordini effettuati utilizzando il metodo di pagamento in conto. L’importo può apparire come un valore positivo o negativo. <br/>**[!UICONTROL Positive value]**- Un pagamento anticipato è rappresentato come valore positivo.<br/>**[!UICONTROL Negative value]** - Un importo dovuto è rappresentato come valore negativo. |
| [!UICONTROL Available Credit] | La somma di _[!UICONTROL Credit Limit]_&#x200B;e_[!UICONTROL Outstanding Balance]_. Se l&#39;azienda ha superato il limite di credito, l&#39;importo viene visualizzato come valore negativo. |
| [!UICONTROL Credit Limit] | Importo del credito concesso alla società. |
| [!UICONTROL Updated By] | Nome della persona che ha avviato l&#39;operazione. |
| [!UICONTROL Custom Reference Number] | Numero di riferimento personalizzato associato alla transazione. |
| [!UICONTROL Comment] | Una compilazione dei valori del campo `Reason for Change`, in base al tipo di operazione. <br/>**[!UICONTROL Purchased]**- Include i commenti dell&#39;acquisto, il numero dell&#39;ordine e il collegamento all&#39;ordine.<br/>**[!UICONTROL Reimbursed]** - Include i commenti della transazione rimborsata. |
| [!UICONTROL Action] | Solo per operazioni `Reimbursed`. **[!UICONTROL Edit]** - Consente di aggiornare l&#39;importo del rimborso. |

{style="table-layout:auto"}

## Aggiornare le informazioni sul credito

Quando i clienti effettuano pagamenti, gli amministratori aggiornano le informazioni sul credito in Admin.

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

   * Immetti l&#39;**importo** del pagamento.

     L&#39;importo può essere inserito come valore positivo o negativo.

   * Se applicabile, immettere il **Numero di riferimento personalizzato** per riferimento.

     È possibile inserire un solo numero di riferimento personalizzato per rimborso. Per applicare il pagamento a più OA, creare un rimborso separato per ciascuno di essi.

   * Se necessario, immetti un **commento** per descrivere il rimborso.

1. Fai clic su **Rimborso**.

   Il sistema aggiorna automaticamente i saldi e la cronologia dei crediti per riflettere il rimborso.

### Modificare un rimborso

1. Aprire il profilo società in modalità **[!UICONTROL Edit]**.

1. Espandi ![il selettore di espansione](../assets/icon-display-expand.png) nella sezione **Credito società**.

1. Trovare la transazione di rimborso nella griglia e fare clic su **[!UICONTROL Edit]**.

1. Apportare le modifiche necessarie a **Numero di riferimento personalizzato** e **Commento**.

   L&#39;importo del rimborso non può essere modificato.

1. Fare clic su **[!UICONTROL Save]**.

## Informazioni sul credito Storefront

Gli amministratori della società possono visualizzare le informazioni sul credito nel pannello di controllo del conto, inclusi il saldo in sospeso, il credito disponibile, il limite di credito e le fatture in sospeso. Quando gli ordini vengono annullati, gli importi vengono restituiti al saldo della società e vengono visualizzati nel campo Cronologia allocazione credito.

![Credito società](./assets/company-credit.png){width="700" zoomable="yes"}

## Demo sul credito aziendale

Scopri come gestire il credito aziendale guardando questo video dimostrativo:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12&learn=on)

## Considerazioni sulla sicurezza

Durante la gestione del credito aziendale, implementa solide misure di sicurezza per proteggere i dati finanziari sensibili:

* **Controllo dell&#39;accesso**—Limita le autorizzazioni di gestione del credito solo al personale autorizzato
* **Audit Trail**: gestione di registri completi di tutte le transazioni e le modifiche di credito
* **Protezione dei dati**: crittografia delle informazioni finanziarie riservate sia in transito che a riposo
* **Flussi di lavoro di approvazione**—Implementare processi di approvazione a più livelli per adeguamenti di credito significativi
* **Revisioni regolari**—Eseguire controlli periodici dell&#39;accesso utente e delle relazioni di credito

## Best practice

* &#x200B;
   * **Gestione delle politiche creditizie**: durante la gestione del credito aziendale, definire criteri chiari per l&#39;impostazione dei limiti di credito in base alla cronologia dei pagamenti del cliente e alle relazioni commerciali. Esamina regolarmente i saldi in essere e i modelli di pagamento per valutare il rischio e documenta sempre le modifiche alle impostazioni del credito con motivi dettagliati a scopo di audit.

Elaborare i pagamenti in modo rapido per mantenere saldi accurati e garantire l&#39;allineamento delle impostazioni della valuta di credito con le operazioni aziendali principali di ciascuna società.

* **Conformità e sicurezza**: limita le autorizzazioni di gestione del credito solo al personale autorizzato, implementa flussi di lavoro di approvazione per adeguamenti del credito significativi e proteggi le informazioni finanziarie sensibili in base ai criteri di sicurezza della tua organizzazione. Revisioni regolari dell’accesso degli utenti e delle relazioni di credito contribuiscono a mantenere una supervisione e una conformità corrette.

>[!MORELIKETHIS]
>
>* [Abilita funzionalità B2B](enable-basic-features.md) * Configura pagamento in conto e altre funzionalità B2B
>* [Creare un account società](account-company-create.md) * Configurare account società con funzionalità di credito
>* [Gestione società](manage-companies.md) * Panoramica delle funzionalità di gestione società
>* [Ruoli e autorizzazioni società](account-company-roles-permissions.md) * Configurare l&#39;accesso degli utenti per la gestione del credito
>* [Flusso di lavoro ordine di acquisto](purchase-order-flow.md) * Comprendere in che modo il credito si integra con gli ordini di acquisto
>* [Riferimento configurazione B2B](../configuration-reference/general/b2b-features.md) - Impostazioni di configurazione dettagliate per le funzionalità B2B
