---
title: Abilitare le funzioni B2B
description: Scopri come abilitare le funzioni B2B per il tuo store di Adobe Commerce, inclusi gli account aziendali, i metodi di pagamento e spedizione predefiniti, gli ordini di acquisto e le approvazioni degli ordini.
exl-id: aed203ef-f39b-4f7e-b32f-ded53eca09a8
feature: B2B, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '1629'
ht-degree: 0%

---

# Abilitare le funzioni B2B

Per impostazione predefinita, tutte le funzioni B2B sono inizialmente disabilitate. L’amministratore dello store può abilitare o disabilitare le funzioni B2B in base alle esigenze degli store di Commerce. Per un elenco completo delle impostazioni di configurazione B2B, vedi [Riferimento alla configurazione delle funzionalità B2B](../configuration-reference/general/b2b-features.md).

Quando abiliti il supporto per le aziende dei clienti, vengono abilitate automaticamente ulteriori funzioni B2B:

- [!DNL Shared Catalog]

  Supporta la configurazione personalizzata dei prezzi per diverse società e abilita le autorizzazioni per le categorie per tutti i negozi.

- [!DNL Enable Shared Catalog direct products price assigning]

  Migliora le prestazioni del sito memorizzando nell&#39;indice dei prezzi solo i prodotti assegnati a un catalogo condiviso. Abilitare questa funzione è una best practice per i commercianti che hanno molti cataloghi condivisi, per gestire i prezzi personalizzati per diverse aziende.

- [!DNL B2B Quotes]

  Consente ai venditori e agli acquirenti aziendali di negoziare i prezzi.

- [!DNL B2B default payment and shipping methods]

  Determina la selezione delle opzioni di pagamento e spedizione disponibili per gli acquirenti B2B sul punto vendita.

Le impostazioni di configurazione per queste funzioni sono visibili solo quando [!DNL Enable Company] è impostato su `Yes`.

B2B [!DNL Quick Order] e [!DNL Requisition List] Le funzioni possono essere attivate e disattivate in modo indipendente.

## Configurare le funzioni B2B

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   In caso di installazione multisito, impostare **[!UICONTROL Store View]** nell&#39;angolo in alto a sinistra del sito Web a cui si applica la configurazione.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL B2B Features]**:

   ![Configurazione B2B - Generale](./assets/b2b-features.png){width="600"}

   - Consenti ai clienti di gestire i propri account aziendali e abilitare il supporto per funzionalità B2B aggiuntive impostando **[!UICONTROL Enable Company]**  a `Yes`.

     Quando abiliti il supporto aziendale, il catalogo condiviso, il preventivo B2B, i metodi di pagamento B2B e i metodi di spedizione B2B vengono abilitati automaticamente.

   - Per consentire ai clienti e agli ospiti di effettuare rapidamente gli ordini in base allo SKU o al nome del prodotto, impostare **[!UICONTROL Enable Quick Order]** a `Yes`.

   - Per consentire ai clienti di creare e gestire gli elenchi delle richieste di acquisto dal dashboard dei conti, impostare **[!UICONTROL Enable Requisition List]** a `Yes`.

     È inoltre possibile [configurare il numero massimo di elenchi](configure-requisition-lists.md) un cliente può avere per il proprio account.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Configurare i metodi di pagamento e di spedizione B2B predefiniti

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Default B2B Payment Methods]** sezione.

1. Per stabilire i metodi di pagamento predefiniti per gli ordini B2B, impostare **[!UICONTROL Applicable Payment Methods]** a uno dei seguenti elementi:

   - `All Payment Methods`

   - `Selected Payment Methods`

     Per l’opzione specifica, seleziona la **[!UICONTROL Payment Methods]** che si desidera rendere disponibile ai clienti tenendo premuto Ctrl (PC) o Comando (Mac) mentre si fa clic su ciascuna opzione.

   L’elenco di [metodi di pagamento](../configuration-reference/sales/payment-methods.md) mostra quali opzioni sono attualmente abilitate o disabilitate nell&#39;archivio. Oltre ai metodi di pagamento standard, l&#39;elenco include anche i seguenti:

   - Non sono richieste informazioni sul pagamento
   - [Pagamento in acconto](#configure-payment-on-account)
   - Account archiviati
   - Schede memorizzate

   ![Configurazione B2B: impostazioni del metodo di pagamento predefinito](./assets/b2b-features-default-payment-methods.png){width="600"}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Default B2B Shipping Methods]** sezione.

1. Per specificare i metodi di spedizione predefiniti per gli ordini B2B, impostare **[!UICONTROL Applicable Shipping Methods]** a uno dei seguenti elementi:

   - `All Shipping Methods`
   - `Selected Shipping Methods`

     Per l’opzione specifica, seleziona la **[!UICONTROL Shipping Methods]** che si desidera rendere disponibile ai clienti tenendo premuto Ctrl (PC) o Comando (Mac) mentre si fa clic su ciascuna opzione.

     L’elenco dei metodi di spedizione mostra quali sono attualmente [abilitato o disabilitato](../configuration-reference/sales/delivery-methods.md).

   ![Configurazione B2B: metodi di spedizione predefiniti](./assets/b2b-features-shipping-methods.png){width="600"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Configurare le opzioni e-mail aziendali

Il [rappresentante commerciale](account-company-manage.md#assign-a-sales-representative) che viene assegnato come contatto principale per una società è configurato per impostazione predefinita come mittente di molti messaggi e-mail automatizzati inviati alla società.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Company Configuration]**.

1. Se necessario, impostare **[!UICONTROL Store View]** nella vista store per definire [ambito](../getting-started/websites-stores-views.md#scope-settings) della configurazione.

1. Completa il **[!UICONTROL Company Registration]** sezione:

   >[!NOTE]
   >
   >Cancella **[!UICONTROL Use system value]** per rendere il campo modificabile.

   - Imposta **[!UICONTROL Company Registration Email Recipient]** al [contatto store](../getting-started/store-details.md#store-email-addresses) chi deve essere informato quando viene ricevuta una nuova richiesta di registrazione dell’azienda.

   - Per **[!UICONTROL Send Company Registration Email Copy To]**, immettere l&#39;indirizzo di posta elettronica di ogni persona che deve ricevere una copia della notifica di registrazione. Separa più indirizzi e-mail con una virgola.

   - Per determinare la modalità di invio della copia della notifica, impostare **Metodo Send Email Copy** a uno dei seguenti elementi:

      - `Bcc` - Invia una _copia per cortesia cieca_ includendo il destinatario nell’intestazione della stessa e-mail inviata al cliente. Il destinatario Ccn non è visibile al cliente.
      - `Separate Email` - Invia la copia come e-mail separata.

   - Se hai preparato un modello e-mail da utilizzare al posto del predefinito, imposta **[!UICONTROL Default Company Registration Email]** al nome del modello. Per impostazione predefinita, il `Company Registration Request` viene utilizzato il modello.

     ![Configurazione clienti - Registrazione società](./assets/company-email-options-company-registration.png){width="600"}

1. Completa il **[!UICONTROL Customer-Related Emails]** sezione:

   Se hai preparato modelli e-mail alternativi da utilizzare al posto dei predefiniti, scegli il modello da utilizzare per ciascuno dei seguenti elementi:

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![Configurazione clienti: e-mail relative al cliente](./assets/company-email-options-customer-related-emails.png){width="600"}

1. Completa il **[!UICONTROL Company Status Change]** sezione:

   - Per **[!UICONTROL Send Company Status Change Email Copy To]**, immettere l&#39;indirizzo di posta elettronica di ogni persona che deve ricevere una copia della notifica di modifica dello stato. Separa più indirizzi e-mail con una virgola.

   - Per determinare la modalità di invio della copia della notifica, impostare **Metodo Send Email Copy** a uno dei seguenti elementi:

      - `Bcc` - Invia una _copia per cortesia cieca_ includendo il destinatario nell’intestazione della stessa e-mail inviata al cliente. Il destinatario Ccn non è visibile al cliente.
      - `Separate Email` - Invia la copia come e-mail separata.

   - Se hai preparato un modello e-mail da utilizzare quando lo stato dell’azienda cambia da `Pending Approval` a `Active`, impostato **[!UICONTROL Default 'Company Status Change to Active 1' Email]** al nome del modello. Per impostazione predefinita, il `Company Status Active 1` viene utilizzato il modello.

   - Se hai preparato un modello e-mail da utilizzare quando lo stato dell’azienda cambia da `Rejected` o `Blocked` a `Active`, impostato **[!UICONTROL Default 'Company Status Change to Active 2' Email]** al nome del modello. Per impostazione predefinita, il `Company Status Active 2` viene utilizzato il modello.

   - Se hai preparato un modello e-mail da utilizzare quando lo stato dell’azienda cambia in `Rejected`, impostato **[!UICONTROL Default 'Company Status Change to Rejected' Email]** al nome del modello. Per impostazione predefinita, il `Company Status Rejected` viene utilizzato il modello.

   - Se hai preparato un modello e-mail da utilizzare quando lo stato dell’azienda cambia in `Blocked`, impostato **[!UICONTROL Default 'Company Status Change to Blocked' Email]** al nome del modello. Per impostazione predefinita, il `Company Status Blocked` viene utilizzato il modello.

   - Se hai preparato un modello e-mail da utilizzare quando lo stato dell’azienda cambia in `Pending Approval`, impostato **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** al nome del modello. Per impostazione predefinita, il `Company Status Pending Approval` viene utilizzato il modello.

   ![Configurazione clienti: modifica dello stato della società](./assets/company-email-options-company-status-change.png){width="600"}

1. Completa il **[!UICONTROL Company Credit Emails]** sezione:

   - Imposta **[!UICONTROL Company Credit Change Email Sender]** al [contatto store](../getting-started/store-details.md#store-email-addresses) chi deve essere informato quando viene apportata una modifica al limite di credito assegnato a una società. Per impostazione predefinita, la notifica viene inviata a _Rappresentante commerciale_.

   - Per **[!UICONTROL Send Company Credit Change Email Copy To]**, immettere l&#39;indirizzo di posta elettronica di ogni persona che deve ricevere una copia della notifica di modifica del credito. Separa più indirizzi e-mail con una virgola.

   - Per determinare la modalità di invio della copia della notifica, impostare **Metodo Send Email Copy** a uno dei seguenti elementi:

      - `Bcc` - Invia una _copia per cortesia cieca_ includendo il destinatario nell’intestazione della stessa e-mail inviata al cliente. Il destinatario Ccn non è visibile al cliente.
      - `Separate Email` - Invia la copia come e-mail separata.

   - Se hai preparato dei modelli e-mail da utilizzare al posto dei predefiniti, scegli il modello per ciascuna delle seguenti notifiche inviate all’amministratore della società.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![Configurazione clienti - e-mail di accredito aziendale](./assets/company-email-options-company-credit.png){width="600"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Configura approvazione ordine

La possibilità di tenere traccia dell&#39;elaborazione degli ordini e degli ordini di acquisto consente agli amministratori della società di controllare le azioni degli acquirenti. La funzionalità di approvazione degli ordini è disponibile quando la funzione ordini fornitore è abilitata da un amministratore del negozio.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL General]** e scegli **[!UICONTROL B2B Features]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Order Approval Configuration]** sezione.

   ![Configurazione approvazione ordine](./assets/b2b-features-order-approval.png){width="600"}

1. Per consentire alle società di creare i propri ordini di acquisto, impostare **[!UICONTROL Enable Purchase Orders]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

   La funzione Ordini di acquisto è abilitata a livello di sito Web. Per attivare questo tipo di ordine per un&#39;azienda, eseguire le stesse operazioni con le impostazioni appropriate in ogni [profilo società](account-company-manage.md).

## Configurare gli ordini fornitore

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Trova la società nell’elenco e fai clic su **[!UICONTROL Edit]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Advanced Settings]** sezione.

1. Imposta **[!UICONTROL Enable Purchase Orders]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save]**.

Dopo l&#39;attivazione, **[!UICONTROL Approval Rules]** viene visualizzata nella vetrina [Dashboard account](../customers/account-dashboard.md) per un amministratore della società.

>[!NOTE]
>
>L’accesso all’ordine fornitore nella vetrina deve essere concesso dall’amministratore della società in base a [autorizzazioni ruolo utente società](account-company-roles-permissions.md).

## Configura pagamento in acconto

Payment on Account è un metodo di pagamento offline che consente alle aziende di effettuare acquisti fino al limite di credito specificato nel loro profilo. Il pagamento in conto può essere abilitato a livello globale o per società e viene visualizzato durante l&#39;estrazione solo se abilitato. Quando _Pagamento in acconto_ viene utilizzato come metodo di pagamento, viene visualizzato un messaggio nella parte superiore dell’ordine che indica lo stato del conto. Per configurare questo metodo di pagamento per una società specifica, consulta [Gestire gli account aziendali](account-company-manage.md).

>[!NOTE]
>
>Il pagamento in conto non è supportato per gli ordini con [più indirizzi di spedizione](../stores-purchase/shipping-settings.md#multiple-addresses) e non compare tra le opzioni di pagamento per questi ordini.

Per abilitare Pagamento in conto per il tuo Negozio:

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Payment on Account]** sezione.

   ![Pagamento in acconto](./assets/payment-methods-payment-on-account.png){width="600"}

   >[!NOTE]
   >
   >Se necessario, deselezionare **[!UICONTROL Use system value]** per modificare queste impostazioni.

1. Per consentire il pagamento in acconto, impostare **[!UICONTROL Enabled]** a `Yes`.

1. Immetti un **[!UICONTROL Title]** che identifica il metodo di pagamento durante il pagamento, oppure puoi accettare il `Payment on Account` titolo predefinito.

1. Se gli ordini in genere attendono l’approvazione, accetta l’impostazione predefinita **[!UICONTROL New Order Status]** as `Pending` fino all&#39;approvazione.

   Se preferisci, puoi utilizzare il `Processing` o `Suspected Fraud` stato dei nuovi ordini con questo metodo di pagamento.

1. Imposta **[!UICONTROL Payment from Applicable Countries]** a uno dei seguenti elementi:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione del negozio può utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, il _[!UICONTROL Payment from Specific Countries]_viene visualizzato. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Imposta **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** agli importi degli ordini necessari per qualificarsi per questo metodo di pagamento.

   >[!NOTE]
   >
   >Un ordine è qualificato se il totale è compreso tra i valori totali minimi o massimi o corrisponde esattamente a tali valori.

1. Immetti un **[!UICONTROL Sort Order]** numero che imposta la posizione di questo elemento nell&#39;elenco dei metodi di pagamento visualizzato durante l&#39;estrazione.

   Il valore è relativo agli altri metodi di pagamento. (`0` = innanzitutto, `1` = secondo, `2` = terzo e così via.)

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
