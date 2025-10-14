---
title: Creazione di un singolo account cliente
description: I visitatori possono creare facilmente un account cliente individuale per gestire i loro acquisti.
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Creazione di un singolo account cliente

I visitatori del tuo negozio possono aprire un account per gestire i loro acquisti e le loro attività. I clienti in genere creano i propri account dal tuo negozio. Tuttavia, puoi anche creare account cliente direttamente dall’amministratore, utile per aiutare i clienti telefonicamente.

Le istruzioni seguenti rappresentano la configurazione predefinita dell’account cliente. Per modificare la selezione e il comportamento di alcuni campi del modulo, vedere [Configurazione degli account cliente](../customers/customer-account-scope.md).

In qualità di amministratore dello store, puoi anche impostare le [nuove opzioni account](../customers/account-options-new.md) per inviare un&#39;e-mail di conferma ai nuovi clienti registrati, in modo da garantire la validità degli account registrati.

>[!NOTE]
>
>A partire dalla versione 2.4.7, i clienti devono reinserire l’e-mail e la password per accedere al proprio account dopo la conferma e-mail, indipendentemente dal browser.

## Crea account dalla vetrina

Un cliente del negozio crea un account nella vetrina.

1. Dalla vetrina, fa clic su **[!UICONTROL Create an Account]** nell&#39;angolo superiore destro dell&#39;intestazione.

   ![Crea un account](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. In **[!UICONTROL Personal Information]**, immette i rispettivi **[!UICONTROL First Name]** e **[!UICONTROL Last Name]**.

   ![Informazioni personali](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. Se si desidera aggiungere il proprio nome e indirizzo di posta elettronica all&#39;elenco degli abbonati alla newsletter, il cliente seleziona la casella di controllo **[!UICONTROL Sign Up for Newsletter]**.

   >[!INFO]
   >
   > Questa opzione viene visualizzata anche se lo store non pubblica una newsletter.

1. Se si desidera che il personale di supporto dello store [veda ciò che vede](../customers/login-as-customer.md) e fornisca assistenza remota, il cliente seleziona la casella di controllo **[!UICONTROL Allow remote shopping assistance]**.

1. In **[!UICONTROL Sign-in Information]**, immette il loro indirizzo **[!UICONTROL Email]**.

   >[!INFO]
   >
   > Questo indirizzo e-mail diventa parte delle credenziali di accesso e non può essere associato ad alcun altro account cliente.

   ![Informazioni di accesso](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. Immette un **[!UICONTROL Password]** che include tre dei seguenti tipi di informazioni:

   - Caratteri minuscoli
   - Caratteri maiuscoli
   - Numeri
   - Caratteri speciali

   Dopo aver premuto **[!UICONTROL Enter]**, l&#39;intensità della password viene valutata e viene visualizzata sotto il campo. Se la password è considerata _Debole_, provarne un&#39;altra finché non viene valutata come _Forte_.

   ![Si consiglia una password complessa](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. Quindi, il cliente lo immette nuovamente in **[!UICONTROL Confirm Password]**.

1. Se necessario, fa clic su **[!UICONTROL Show Password]** per visualizzare la password immessa.

1. Al termine, fa clic su **Crea un account**.

Il cliente può quindi utilizzare il proprio indirizzo e-mail e la propria password per [accedere](../customers/customer-sign-in.md) al proprio account e completare le informazioni sull&#39;indirizzo.

## Creare un account dall’Amministratore

In qualità di esercente, puoi creare un account cliente dall’Amministratore.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Fare clic su **[!UICONTROL Add New Customer]**.

### Passaggio 1: Completare le informazioni sull&#39;account

![Informazioni sul cliente](assets/new-information.png){width="700" zoomable="yes"}

1. Nella sezione **[!UICONTROL Account Information]** eseguire le operazioni seguenti:

   - Per un&#39;installazione multisito, impostare **[!UICONTROL Associate to Website]** sul sito Web in cui si applica l&#39;account del cliente.
   - Se applicabile, assegnare il cliente a un altro **[!UICONTROL Customer Group]**.
   - Se si utilizza la [convalida ID IVA](../stores-purchase/vat.md) e si desidera **[!UICONTROL Disable Automatic Group Change Based on VAT ID]**, selezionare la casella di controllo.

1. Compila i campi obbligatori:

   - **[!UICONTROL First Name]**
   - **[!UICONTROL Last Name]**
   - **[!UICONTROL Email]**

1. Compila i campi facoltativi secondo necessità:

   - **[!UICONTROL Name Prefix]**
   - **[!UICONTROL Middle Name/Initial]**
   - **[!UICONTROL Name Suffix]**
   - **[!UICONTROL Date of Birth]**
   - **[!UICONTROL Tax/VAT Number]**
   - **[!UICONTROL Gender]**

   >[!WARNING]
   >
   >In linea con le attuali best practice in materia di sicurezza e privacy, tieni presente eventuali rischi legali e di sicurezza associati all’archiviazione della data di nascita completa (mese, giorno, anno) dei clienti con altri identificatori personali. Si consiglia di limitare la memorizzazione delle date di nascita complete dei clienti e di utilizzare l’anno di nascita del cliente come alternativa.

1. Impostare **[!UICONTROL Send Welcome Email From]** sulla visualizzazione archivio da cui inviare l&#39;e-mail di _Benvenuto_.

   >[!INFO]
   >
   > Se nell&#39;archivio sono presenti visualizzazioni per [lingue](../stores-purchase/store-localize.md) diverse, questa impostazione determina la lingua dell&#39;e-mail di benvenuto.

1. Fai clic su **[!UICONTROL Save and Continue Edit]** nella parte superiore della pagina.

   >[!INFO]
   >
   >Una volta salvato l’account del cliente, l’intero set di opzioni viene visualizzato nel pannello a sinistra e nel menu nella parte superiore della pagina. Nella scheda _[!UICONTROL Customer View]_&#x200B;viene visualizzato un riepilogo dell&#39;account.

   ![Visualizzazione clienti](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### Passaggio 2: inserire le informazioni sull&#39;indirizzo

1. Nel pannello a sinistra, scegli **[!UICONTROL Addresses]** e fai clic su **[!UICONTROL Add New Addresses]**.

1. Se per la fatturazione e la spedizione viene utilizzato lo stesso indirizzo, attiva entrambe le opzioni.

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![Aggiungi informazioni indirizzo cliente](assets/information-addresses.png){width="600" zoomable="yes"}

1. Scorri verso il basso e completa i campi indirizzo obbligatori nella seconda colonna.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. Immettere **[!UICONTROL Phone Number]** per questo indirizzo.

1. Se applicabile, immettere **[!UICONTROL VAT Number]** associato al cliente.

1. Se questo indirizzo è l&#39;unico necessario per l&#39;account, fare clic su **[!UICONTROL Save]**.

   In caso contrario, fare clic su **[!UICONTROL Save and Continue Edit]** e ripetere i passaggi precedenti per aggiungere altri indirizzi.

   Il nuovo indirizzo viene visualizzato nella pagina [!UICONTROL Addresses] con gli indirizzi selezionati _[!UICONTROL Default Billing]_&#x200B;e&#x200B;_[!UICONTROL Default Shipping]_ sopra l&#39;elenco completo.

   ![Visualizzazione indirizzi](assets/address-list.png){width="600" zoomable="yes"}

### Passaggio 3: reimpostare la password

Agli account cliente creati dall’amministratore non sono inizialmente assegnate password.

1. Trovare il nuovo conto cliente nella griglia.

1. Fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

1. Nella barra dei menu nella parte superiore della pagina, fare clic su **[!UICONTROL Reset Password]**.

1. Viene inviata una notifica al proprietario dell’account, con le istruzioni per l’impostazione della password.

## Barra dei pulsanti

Quando il profilo viene salvato per la prima volta, diventano disponibili pulsanti aggiuntivi. Per ulteriori informazioni, consulta [Aggiornare un profilo cliente](../customers/update-account.md).

| Pulsante | Descrizione |
|--- |--- |
| **[!UICONTROL Back]** | Torna alla pagina _[!UICONTROL Customers]_&#x200B;senza salvare le modifiche. |
| **[!UICONTROL Delete Customer]** | Elimina il cliente corrente. Gli ordini completati associati al cliente non vengono rimossi. |
| **[!UICONTROL Reset]** | Ripristina i valori precedenti delle modifiche non salvate nel modulo per il cliente. |
| **[!UICONTROL Create Order]** | Crea un ordine per il cliente. |
| **[!UICONTROL Reset Password]** | Invia al cliente un collegamento [reimposta password](../customers/password-reset.md) tramite e-mail. |
| **[!UICONTROL Force Sign-in]** | Revoca i token di accesso OAuth associati all’account cliente. Questa funzione può essere utilizzata solo con account cliente a cui sono stati assegnati token OAuth come parte di un&#39;integrazione [API Web](../systems/integrations.md). Per ulteriori informazioni, consulta [Autenticazione basata su OAuth](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) nella documentazione per gli sviluppatori. |
| **[!UICONTROL Manage Shopping Cart]** | Consente all’amministratore di gestire il carrello per il cliente. |
| **[!UICONTROL Save and Continue Edit]** | Salva le modifiche e mantiene aperto il profilo cliente. |
| **[!UICONTROL Save Customer]** | Salva le modifiche e chiude il profilo cliente. |

{style="table-layout:auto"}

## Descrizioni dei campi

### [!UICONTROL Account Information]

| Campo | Descrizione |
|--- |--- |
| **[!UICONTROL Associate to Website]** | Identifica il sito Web associato all&#39;account del cliente. |
| **[!UICONTROL Group]** | Identifica il [gruppo di clienti](../customers/customer-groups.md) di cui il cliente è membro. Se applicabile, selezionare la casella di controllo per disabilitare la modifica di gruppo automatica in base all&#39;IVA. |
| **[!UICONTROL Name Prefix]** | Se utilizzato, il prefisso associato al nome del cliente (ad esempio Sig., Sig.ra o Dott.). I valori del prefisso sono determinati dalla [configurazione](../configuration-reference/customers/customer-configuration.md). A seconda della configurazione, il controllo di input potrebbe essere un campo di testo o un elenco di opzioni. |
| **[!UICONTROL First Name]** | Il nome del cliente. |
| **[!UICONTROL Middle Name / Initial]** | Secondo nome o iniziale del cliente. Questo campo è incluso solo se specificato nell&#39;argomento [configuration](../configuration-reference/customers/customer-configuration.md). |
| **[!UICONTROL Last Name]** | Cognome del cliente. |
| **[!UICONTROL Name Suffix]** | Se utilizzato, il suffisso associato al nome del cliente (ad esempio Jr., Sr. o III). I valori del suffisso sono determinati dalla [configurazione](../configuration-reference/customers/customer-configuration.md). A seconda della configurazione, il controllo di input potrebbe essere un campo di testo o un elenco a discesa di opzioni. |
| **[!UICONTROL Email]** | Indirizzo e-mail del cliente. |
| **[!UICONTROL Date of Birth]** | La data di nascita del cliente. La data di nascita è inclusa se specificata nell&#39;argomento [configuration](../configuration-reference/customers/customer-configuration.md). <br><br>In linea con le attuali best practice in materia di sicurezza e privacy, tieni presente i potenziali rischi legali e di sicurezza associati all&#39;archiviazione della data di nascita completa (mese, giorno, anno) dei clienti con altri identificatori personali. Si consiglia di limitare la memorizzazione delle date di nascita complete dei clienti e, in alternativa, di utilizzare l’anno di nascita del cliente. |
| **[!UICONTROL Tax / VAT Number]** | Numero di imposta o di imposta sul valore aggiunto del cliente, se applicabile. |
| **[!UICONTROL Gender]** | Identifica il genere del cliente. Il genere è incluso se specificato nella [configurazione](../configuration-reference/customers/customer-configuration.md). Opzioni: `Male` / `Female` / `Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | Se sono presenti più visualizzazioni dello store, questa impostazione identifica la visualizzazione dello store da cui viene inviato il messaggio di benvenuto. Se le visualizzazioni dello store vengono utilizzate per lingue diverse, questa impostazione determina la lingua dell&#39;e-mail di benvenuto. |

### [!UICONTROL Addresses]

| Campo | Descrizione |
|--- |--- |
| **[!UICONTROL New Addresses]** | Identifica il tipo di nuovo indirizzo. Opzioni: `Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | Visualizza un&#39;altra sezione Nuovo indirizzo per identificare il tipo di indirizzo da immettere. |
| **[!UICONTROL Company]** | Il nome della società, se applicabile per questo indirizzo. |
| **[!UICONTROL Street Address]** | Indirizzo del cliente. Una seconda riga dell&#39;indirizzo stradale è disponibile se specificato nell&#39;argomento [configuration](../configuration-reference/customers/customer-configuration.md). |
| **[!UICONTROL City]** | La città in cui si trova l’indirizzo del cliente. |
| **[!UICONTROL Country]** | Il paese in cui si trova l’indirizzo del cliente. |
| **[!UICONTROL State/Province]** | Stato o provincia in cui si trova l&#39;indirizzo del cliente. |
| **[!UICONTROL Zip/Postal Code]** | Il codice postale o ZIP in cui si trova l’indirizzo del cliente. |
| **[!UICONTROL Phone Number]** | Numero di telefono del cliente associato all’indirizzo. |
| **[!UICONTROL VAT Number]** | Se applicabile, la partita IVA che si applica al cliente a questo indirizzo. |
