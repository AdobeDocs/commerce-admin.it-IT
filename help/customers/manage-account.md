---
title: Gestire gli account cliente
description: Utilizza il [!UICONTROL Customers] grid per trovare qualsiasi account cliente e accedere alle informazioni per i singoli account cliente.
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Gestire gli account cliente

Utilizza il _[!UICONTROL Customers]_per trovare un account cliente. Puoi utilizzare lo standard [controlli sul posto di lavoro](../getting-started/admin-workspace.md) per filtrare l’elenco, modifica il [layout colonna](../getting-started/admin-grid-controls.md), salva le visualizzazioni ed esporta i dati. Il [Controllo Azioni](../getting-started/admin-actions-control.md) sopra la griglia può essere utilizzato per applicare un&#39;operazione a più record cliente.

![Tutti i clienti](assets/customers-all-customers.png){width="700" zoomable="yes"}

Consulta [Aggiorna profilo cliente](update-account.md) per informazioni sull&#39;esecuzione di aggiornamenti manuali a un account cliente.

## Azioni dell’account cliente

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Nella prima colonna della griglia selezionare la casella di controllo di ogni record che si desidera aggiornare.

1. Seguire le istruzioni per l&#39;azione che si desidera applicare.

   >[!INFO]
   >
   >Le azioni seguenti possono essere applicate a uno o più record.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

### Iscriviti alla newsletter

In configurazioni multi-store e multi-sito con un [ambito account cliente](../customers/customer-account-scope.md), un account cliente può essere abbonato alle newsletter da più siti o store. Se si applica il _Abbonati_ azione su un account cliente, attiva l’abbonamento alla newsletter solo per la vista predefinita sito/store.

* Imposta il **[!UICONTROL Actions]** controllo a `Subscribe to newsletter`.

Consulta [Gestisci abbonati](../merchandising-promotions/newsletter-subscribers.md) per ulteriori informazioni sulla gestione degli abbonamenti alle newsletter per un cliente.

### Annulla iscrizione alla newsletter

In configurazioni multi-store e multi-sito con un [ambito account cliente](customer-account-scope.md), un account cliente può essere abbonato alle newsletter per più siti/negozi. Se si applica il _Annulla iscrizione_ a un account cliente, tutti gli abbonamenti attivi vengono annullati.

1. Imposta il **[!UICONTROL Actions]** controllo a `Unsubscribe to newsletter`.

1. Quando viene richiesto di confermare, fai clic su **OK**.

### Assegnare un gruppo di clienti

1. Imposta il **[!UICONTROL Actions]** controllo a `Assign a customer group`.

1. Scegliere il gruppo di clienti a cui assegnare tutti i record cliente selezionati.

1. Quando viene richiesto di confermare, fai clic su **[!UICONTROL OK]**.

### Elimina account cliente

Non è possibile ripristinare gli account cliente eliminati. Le informazioni sull&#39;attività del cliente e sulle transazioni vengono conservate nel sistema.

1. Imposta il **[!UICONTROL Actions]** controllo a `Delete`.

1. Quando viene richiesto di confermare, fai clic su **[!UICONTROL OK]**.

## Esporta account clienti

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Nel menu Intestazione tabella, fare clic su **[!UICONTROL Export]** e selezionare il formato desiderato:

   * CSV
   * XML di Excel

1. Clic **[!UICONTROL OK]**.

   Il file passa alla cartella dei download predefinita.

L&#39;istruzione precedente esporta tutti gli account cliente. Se desideri esportare un set limitato, seleziona le caselle di controllo per gli account che desideri esportare oppure utilizza i filtri nel pannello di controllo per selezionare un intervallo di account cliente.

## Azioni/controlli

| Opzione | Descrizione |
|--- |--- |
| **[!UICONTROL Delete]** | Elimina gli account cliente selezionati. Se l’account cliente appartiene a un amministratore società per un archivio B2B, prima di poter eliminare l’account cliente è necessario assegnare come amministratore un altro utente società. |
| **[!UICONTROL Subscribe to Newsletter]** | Iscrive i clienti selezionati alla newsletter. |
| **[!UICONTROL Unsubscribe from Newsletter]** | Annulla l’abbonamento dei clienti selezionati alla newsletter. |
| **[!UICONTROL Assign a Customer Group]** | Assegna i clienti selezionati a un gruppo di clienti. |
| **[!UICONTROL Edit]** | Consente di modificare dalla griglia alcuni valori di un singolo record cliente selezionato. Per impostazione predefinita, per una modifica rapida sono disponibili i seguenti valori: E-mail, Gruppo, Telefono, CAP, Sito Web, Partita IVA e Genere. |

{style="table-layout:auto"}

## Colonne

| Colonna | Descrizione |
|--- |--- |
| **[!UICONTROL Select]** | Gestisce le selezioni delle caselle di controllo per i record cliente per l&#39;applicazione di un&#39;azione. È inoltre possibile utilizzare il controllo di selezione nell&#39;intestazione di colonna per selezionare/deselezionare tutti gli elementi. |
| **[!UICONTROL ID]** | Un identificatore numerico univoco assegnato al momento della creazione dell’account del cliente. |
| **[!UICONTROL Name]** | Nome e cognome del cliente. |
| **[!UICONTROL Email]** | L’indirizzo e-mail del cliente. |
| **[!UICONTROL Group]** | Il gruppo di clienti a cui è assegnato il cliente. |
| **[!UICONTROL Phone]** | Numero di telefono del cliente. |
| **[!UICONTROL ZIP]** | Il codice postale del cliente. |
| **[!UICONTROL Country]** | Il paese in cui si trova il cliente. |
| **[!UICONTROL State/Province]** | Stato o provincia in cui si trova il cliente. |
| **[!UICONTROL Customer Since]** | Data e ora di creazione dell&#39;account cliente. |
| **[!UICONTROL Web Site]** | Sito Web nella gerarchia del punto vendita a cui è associato l&#39;account del cliente. |
| **[!UICONTROL Confirmed Email]** | Indica se è necessario un messaggio e-mail di conferma. |
| **[!UICONTROL Account Created In]** | Indica la visualizzazione del punto vendita da cui è stato creato l&#39;account cliente. |
| **[!UICONTROL Date of Birth]** | La data di nascita del cliente. In linea con le attuali best practice in materia di sicurezza e privacy, tieni presente eventuali rischi legali e di sicurezza associati all’archiviazione della data di nascita completa (mese, giorno, anno) dei clienti con altri identificatori personali. Si consiglia di limitare la memorizzazione delle date di nascita complete dei clienti e, in alternativa, di utilizzare l’anno di nascita del cliente. |
| **[!UICONTROL Tax / VAT Number]** | Se applicabile, il codice fiscale o [imposta sul valore aggiunto](../stores-purchase/vat.md) numero assegnato al cliente. <br/><br/> Questo campo non corrisponde alla partita IVA. |
| **[!UICONTROL Gender]** | Il genere del cliente. |
| **[!UICONTROL Action]** | Modifica: apre l’account società in modalità di modifica. |

{style="table-layout:auto"}

### Colonne aggiuntive

Queste colonne sono disponibili modificando la [layout colonna](../getting-started/admin-grid-controls.md) della griglia.

| Colonna | Descrizione |
|--- |--- |
| **[!UICONTROL Company]** | Il nome aziendale del cliente. |
| **[!UICONTROL Street Address]** | Indirizzo del cliente. |
| **[!UICONTROL City]** | La città in cui si trova il cliente. |
| **[!UICONTROL Fax]** | Numero di fax del cliente, se applicabile. |
| **[!UICONTROL Billing Firstname]** | Il nome nell’indirizzo di fatturazione del cliente. |
| **[!UICONTROL Billing Lastname]** | Cognome nell’indirizzo di fatturazione del cliente. |
| **[!UICONTROL Billing Address]** | Indirizzo a cui devono essere inviate le informazioni di fatturazione. |
| **[!UICONTROL Shipping Address]** | Indirizzo dove devono essere spediti gli ordini. |
| **[!UICONTROL VAT Number]** | Numero di partita IVA associato all&#39;indirizzo del cliente. Per [beni digitali](../stores-purchase/taxes.md) venduta nell&#39;UE, l&#39;IVA si basa sull&#39;indirizzo di fatturazione del cliente. <br/><br/> Questo campo non corrisponde alla partita IVA/imposta. |
| **[!UICONTROL Account Lock]** | Indica lo stato dell’account. Come misura di sicurezza, i conti cliente possono essere [bloccato](../customers/password-options.md) dopo troppi tentativi di accesso. Valori: `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | Lo stato utente corrente. Opzioni: `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | Classificazione del cliente. Opzioni: `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | Il rappresentante commerciale che viene assegnato come punto di contatto per un account aziendale e riceve tutti i messaggi e-mail automatizzati relativi all&#39;azienda. |

{style="table-layout:auto"}
