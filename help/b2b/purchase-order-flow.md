---
title: Ordini di acquisto per società
description: Scopri i flussi di lavoro degli ordini di acquisto che consentono alle aziende di tenere traccia e controllare la spesa.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
source-git-commit: 4b34645377102e890779059e57c61cf23f71f34c
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 0%

---

# Ordini di acquisto per società

Gli ordini di acquisto (OA) sono un modo comune per le aziende di tenere traccia e controllare la spesa. [Ordine fornitore](../stores-purchase/purchase-order.md) è uno dei metodi di pagamento offline standard supportati in Adobe Commerce e Magento Open Source. Quando viene installato B2B di Adobe Commerce e [_Abilita ordini di acquisto_](account-company-manage.md#advanced-settings) è attivato per un conto società, tutti gli ordini vengono creati automaticamente come Ordini di acquisto (OA). Utenti aziendali con il necessario [autorizzazioni](account-company-roles-permissions.md) può creare, modificare ed eliminare gli OA creati e quelli creati da utenti subordinati.

## Flusso degli ordini fornitore

A seconda del ruolo e dell’ordine, gli utenti aziendali possono essere soggetti a diverse regole di approvazione. E a seconda che si utilizzino metodi di pagamento online o offline, il flusso è leggermente diverso. Gli amministratori aziendali possono creare gli ordini automaticamente, ignorando le regole di approvazione. Poiché la memorizzazione dei dettagli del pagamento online durante il processo di approvazione rappresenta un rischio per la sicurezza, questi dettagli vengono aggiunti dopo l&#39;approvazione e quindi l&#39;ordine di acquisto viene convertito in un ordine reale.

![Flusso degli ordini fornitore](./assets/purchase-order-flow.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Non è possibile effettuare un ordine se uno o più prodotti nell&#39;ordine di acquisto sono attualmente disabilitati o esauriti.

Il flusso di lavoro degli ordini di acquisto per un’azienda può variare in alcuni modi:

- Se non vengono impostate regole di approvazione, è possibile inserire gli ordini di acquisto e completare direttamente l&#39;ordine.

  >[!NOTE]
  >
  >Per impostazione predefinita, un `Purchase order has been submitted for approval` Il messaggio viene sempre visualizzato agli utenti aziendali, anche quando non sono impostate regole di approvazione. Quando non è richiesto alcun processo di approvazione, gli utenti aziendali ricevono automaticamente un’e-mail che li informa che l’ordine è stato creato e approvato.

- Se le regole di approvazione sono definite dall’amministratore della società, gli utenti passano attraverso il processo di approvazione.
- I dettagli del pagamento offline vengono immessi durante la creazione dell&#39;ordine fornitore.
- I dettagli del pagamento online vengono immessi dopo l&#39;approvazione dell&#39;ordine fornitore.

>[!NOTE]
>
>Gli ordini di acquisto creano un _istantanea_ di prezzi degli articoli, sconti e prezzi di spedizione al momento della creazione dell&#39;ordine. Se il prezzo di un articolo cambia dopo la creazione dell&#39;ordine di acquisto, viene utilizzato il prezzo originale.

### Esempio di workflow di base

Le aziende utilizzano gli ordini di acquisto per controllare ciò che i dipendenti possono acquistare per conto dell&#39;azienda e spesso impostano regole di approvazione per applicare le linee guida aziendali. A seconda delle regole di approvazione, più persone potrebbero dover approvare l’ordine.

1. L&#39;utente crea un ordine di acquisto per beni del valore di 25.000 dollari.
1. Il loro responsabile deve approvare.
1. Poiché l&#39;ordine è superiore a $ 10.000, anche il V.P. deve approvare.
1. A seconda del metodo di pagamento, dopo le approvazioni l&#39;ordine di acquisto viene convertito automaticamente in un ordine oppure l&#39;utente restituisce per immettere i dettagli di pagamento.

### Regole di approvazione

Le regole di approvazione vengono utilizzate per controllare la spesa in base alle linee guida aziendali. Di seguito sono riportati alcuni esempi di regole di approvazione:

- Per ordini superiori a 100 dollari è necessaria l&#39;approvazione del tuo responsabile.
- Per ordini superiori a 1000 dollari è necessaria l&#39;approvazione del tuo responsabile e dell&#39;amministratore della società.
- Qualsiasi ordine con più di 30 SKU univoci deve essere approvato dall’amministratore della società.

Con queste regole in vigore per un&#39;azienda, un utente aziendale può completare l&#39;ordine immediatamente quando l&#39;ordine è inferiore a 100 $. Per scoprire la definizione della regola di approvazione, consulta [Regole di approvazione](account-dashboard-approval-rules.md)

### Tipi di utenti dello store

Il flusso di lavoro dell’ordine di acquisto può anche essere diverso a seconda di chi effettua l’acquisto.

- Un dipendente regolare può essere soggetto a tutte le regole di approvazione
- Un manager potrebbe avere più potere d&#39;acquisto e avere diverse regole di approvazione
- Gli amministratori della società possono ignorare tutte le regole di approvazione e far completare automaticamente i loro ordini di acquisto.

Tutti questi fattori possono influenzare l&#39;esatto processo di pagamento.

## [!UICONTROL My Purchase Orders]

Quando gli ordini di acquisto sono abilitati per una società, il **[!UICONTROL My Purchase Orders]** l&#39;elemento viene visualizzato nel pannello a sinistra per i clienti che hanno effettuato l&#39;accesso a un account utente della società. Sono disponibili tre schede che forniscono elenchi e funzioni diversi per gli ordini di acquisto:

- **[!UICONTROL My Purchase Orders]**: OA creati dal cliente.
- **[!UICONTROL Company Purchase Orders]**: ordini di acquisto effettuati da utenti subordinati all’interno dell’azienda (dipende dalla struttura e dai ruoli dell’azienda).
- **[!UICONTROL Requires My Approval]**: (Visibile per gli approvatori designati) OA in attesa dell&#39;approvazione del cliente. Il contatore indica il numero di ordini in attesa di approvazione.

![I miei ordini di acquisto](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Per ulteriori informazioni sulle funzioni supportate per gli ordini di acquisto disponibili per gli utenti aziendali sul vetrina, vedi [I miei ordini di acquisto](account-dashboard-my-purchase-orders.md).

## Metodi di pagamento offline e online

I flussi di lavoro possono variare a seconda del metodo di pagamento. Per ulteriori informazioni sui metodi di pagamento di Adobe Commerce, consulta [Metodi di pagamento](../stores-purchase/payments.md) nel _Guida all’esperienza di vendita e acquisto_.

>[!IMPORTANT]
>
>Gli ordini fornitore devono utilizzare un _Nel contesto_ esperienza di pagamento. _Fuori contesto_ le estrazioni non sono supportate perché ignorano il normale flusso di estrazione. Generalmente, _Nel contesto_ significa che il cliente rimane sul sito di commerce per completare il processo. _Fuori contesto_ è il momento in cui il cliente viene portato in un’altra sede per completare l’acquisto.

### Pagamenti online

Per motivi di sicurezza, in genere i negozi online non desiderano raccogliere i dettagli della carta di credito del negozio in attesa del completamento del processo di approvazione. Pertanto, se è selezionata un&#39;opzione di pagamento online, il creatore dell&#39;ordine fornitore ritorna allo store dopo l&#39;approvazione, immette i dettagli di pagamento e completa l&#39;ordine. Esempi di pagamenti online sono:

- Carte di credito
- PayPal
- Braintree

>[!IMPORTANT]
>
>L&#39;utilizzo di carte regalo, punti di credito del negozio o punti premio con metodi di pagamento online per gli ordini di acquisto non è supportato. L&#39;attivazione di queste funzioni con i pagamenti online può causare alcuni comportamenti imprevisti. Quando i pagamenti online sono abilitati per gli ordini di acquisto, si consiglia di disattivare le carte regalo, il credito del negozio e i punti premio.

### Pagamenti offline

Poiché i metodi di pagamento offline, come un vaglia postale, sono gestiti al di fuori del sito web, sono più sicuri. Gli ordini di acquisto con pagamenti offline possono essere elaborati automaticamente, dopo qualsiasi processo di approvazione.

Di seguito sono riportati alcuni esempi di pagamenti offline:

- Assegno/vaglia postale
- Pagamento in acconto
- Consegna in contanti
- Bonifici bancari
- Credito store
