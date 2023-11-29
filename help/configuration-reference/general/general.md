---
title: '[!UICONTROL General] &gt; [!UICONTROL General]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL General] &gt; [!UICONTROL General] pagina dell’amministratore di Commerce.
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

Consulta [Opzioni paese](../../getting-started/store-details.md#country-options) per ulteriori dettagli su questi campi e opzioni di configurazione.

![Generale > Opzioni paese](./assets/general-country-options.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Default Country] | Visualizzazione store | Il paese in cui si trova il tuo negozio. |
| [!UICONTROL Allow Countries] | Sito Web | I paesi in cui si accettano gli ordini. |
| [!UICONTROL Zip/Postal Code is Optional for] | Globale | Paesi che non richiedono un CAP nell&#39;indirizzo di spedizione. |
| [!UICONTROL European Union Countries] | Globale | Paesi che sono membri dell&#39;Unione Europea. |
| [!UICONTROL Top Destinations] | Visualizzazione store | Paesi principali di destinazione delle vendite. |

{style="table-layout:auto"}

## [!UICONTROL State Options]

Consulta [Opzioni stato](../../getting-started/store-details.md#state-options) per ulteriori dettagli su questi campi e opzioni di configurazione.

![Generale > Opzioni stato](./assets/general-state-options.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL State is required for] | Globale | I paesi (in cui conduci attività commerciali) che richiedono l’inclusione di un’area geografica o di uno Stato nell’indirizzo postale. |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | Globale | Per i paesi in cui non è richiesto, determina se _Regione/Stato_ è incluso nell’indirizzo postale del cliente.<br /> <br />**`Yes`**- Include _Regione/Stato_ campo nell’indirizzo del cliente, anche se non richiesto dal paese.<br />**`No`** - Omette il campo Regione/Stato dall&#39;indirizzo del cliente se non richiesto dal paese. |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

Consulta [Opzioni internazionali](../../getting-started/store-details.md#locale-options) per ulteriori dettagli su questi campi e opzioni di configurazione.

![Generale > Opzioni internazionali](./assets/general-locale-options.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Timezone] | Sito Web | Il fuso orario del mercato primario servito dal sito web. Di solito il fuso orario è lo stesso utilizzato nella posizione fisica della tua azienda. |
| [!UICONTROL Locale] | Visualizzazione store | Lingua, valuta e sistema di misurazione utilizzati nel mercato gestito dalla visualizzazione punto vendita. |
| [!UICONTROL Weight Unit] | Visualizzazione store | L&#39;unità di misura generalmente utilizzata per le spedizioni dalla lingua. Opzioni: `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | Visualizzazione store | Il giorno considerato come il primo giorno della settimana nel mercato servito dalla visualizzazione del negozio. |
| [!UICONTROL Weekend Days] | Visualizzazione store | I giorni che cadono nel fine settimana nel mercato servito dalla vista del negozio. |

{style="table-layout:auto"}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![Generale > Limitazioni per i siti Web](./assets/general-website-restrictions.png)<!-- zoom -->

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Limitazioni di accesso](../../merchandising-promotions/event-configure.md#access-restrictions) nel _Guida al merchandising e alle promozioni_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | Sito Web | Determina se il sito Web funziona in modalità con restrizioni.<br /> <br />**`Yes`**- L&#39;accesso al sito web è limitato secondo le modalità stabilite nei campi seguenti.<br />**`No`** - Le restrizioni sono disattivate e le seguenti impostazioni non hanno alcun effetto. |
| [!UICONTROL Restriction Mode] | Sito Web | Determina il tipo di restrizione di accesso applicabile al sito Web.<br /> <br />**`Website Closed`**: tutti gli accessi alla vetrina sono soggetti a restrizioni e gli URL della vetrina vengono temporaneamente reindirizzati alla pagina di destinazione. Questa impostazione può essere utile durante la manutenzione del sito o prima del lancio.<br />**`Private Sales: Login Only`** - Solo i clienti registrati possono effettuare l&#39;accesso per accedere allo store. Tutti gli URL della vetrina vengono temporaneamente reindirizzati alla pagina di destinazione o al modulo di accesso specificato. Gli utenti non possono creare un account in questa modalità.<br />**`Private Sales: Login and Register`**- Gli utenti devono accedere per accedere alla vetrina. Tutti gli URL della vetrina vengono temporaneamente reindirizzati al modulo di accesso fino a quando l’utente non effettua l’accesso. Gli utenti possono registrarsi per un account mentre il sito è in questa modalità. |
| [!UICONTROL Startup Page] | Visualizzazione store | Quando il sito web è in modalità Vendite private, questa impostazione determina la pagina visualizzata fino a quando il cliente non effettua l’accesso.<br />  <br />**`To login form`**- Gli utenti vengono reindirizzati al modulo di accesso fino al momento dell’accesso.<br />**`To landing page`** : gli utenti vengono reindirizzati alla pagina statica specificata di seguito fino a quando non effettuano l’accesso.<br /> <br />**_Importante!_**Assicurati di includere un collegamento alla pagina di accesso dalla pagina di destinazione specificata, in modo che i clienti possano effettuare l’accesso per accedere al sito completo. |
| [!UICONTROL Landing Page] | Visualizzazione store | Determina la prima pagina visualizzata quando il sito Web è in modalità Vendite private. |
| [!UICONTROL HTTP Response] | Sito Web | Determina la risposta HTTP inviata quando il sito Web viene chiuso e viene tentata una connessione da un bot, un crawler o un spider.<br /> <br />**`503 Service unavailable`**- La pagina non è disponibile, ma il spider non deve aggiornare l’indice.<br />**`200 OK`** - La pagina di destinazione è corretta e deve essere trattata dal ragno come l’unica pagina del sito. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Sito Web | Determina se i campi del _Login_ e _Password dimenticata_ i moduli vengono compilati automaticamente dalle voci precedenti. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![Generale > Informazioni sul negozio](./assets/general-store-information.png)<!-- zoom -->

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Informazioni sul negozio](../../getting-started/store-details.md) nel _Guida introduttiva_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Store Name] | Visualizzazione store | Nome dell&#39;archivio associato alla visualizzazione archivio. |
| [!UICONTROL Store Phone Number] | Visualizzazione store | Il numero di telefono principale del negozio (associato alla visualizzazione del negozio) è aperto per le aziende. Ad esempio: lun - ven, 9-5, sab 9-mezzogiorno PST |
| Paese | Sito Web | Il paese dell’azienda che gestisce il sito web. |
| [!UICONTROL Region/State] | Sito Web | L’area geografica o lo stato dell’azienda che gestisce il sito web. |
| [!UICONTROL ZIP/Postal Code] | Sito Web | Il codice postale o ZIP dell’azienda che gestisce il sito web. |
| [!UICONTROL City] | Sito Web | La città in cui si trova l’azienda che gestisce il sito web. |
| [!UICONTROL Street Address] | Sito Web | La via o l’indirizzo postale dell’azienda che gestisce il sito web. |
| [!UICONTROL Street Address Line 2|]Sito Web | La seconda riga dell’indirizzo della via aziendale, se necessario. |
| [!UICONTROL VAT Number] | Sito Web | Numero di imposta sul valore aggiunto dell’azienda proprietaria dell’installazione Commerce, se applicabile. |
| [!UICONTROL Validate VAT Number] |  | Verifica il numero di identificazione IVA. |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![Generale > Modalità store singolo](./assets/general-single-store-mode.png)<!-- zoom -->

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Modalità store singolo](../../getting-started/websites-stores-views.md#single-store-mode) nel _Guida introduttiva_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | Globale | Se l&#39;opzione è abilitata per le installazioni di un solo archivio, nasconde la casella Ambito configurazione e le relative etichette di campo Opzioni: `Yes` / `No` <br/>**_Nota:_**La modalità a archivio singolo viene ignorata per gli archivi con più visualizzazioni. |

{style="table-layout:auto"}
