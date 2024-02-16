---
title: "[!DNL Audience Activation]"
description: Scopri come attivare i tipi di pubblico di Real-Time CDP in Adobe Commerce per promuovere la personalizzazione nel tuo store.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: db8344ab8890c20bb0b3c7d25da95b6007858d6a
workflow-type: tm+mt
source-wordcount: '1409'
ht-degree: 0%

---

# [!DNL Audience Activation]

Il [!DNL Audience Activation] estensione consente di attivare i tipi di pubblico di Real-Time CDP in Adobe Commerce per creare offerte univoche nel carrello. Queste offerte e incentivi includono tecniche di merchandising comuni per l’e-commerce, come _acquistare 2 ottenere 1 gratis_, i banner hero rivolti a quel cliente e i prezzi dei prodotti modificati attraverso varie offerte. I tipi di pubblico generati in Real-Time CDP si basano su dati provenienti da vari sistemi aziendali, come Enterprise Resource Planning (ERP), Customer Relationship Management (CRM), punti vendita e sistemi di marketing. Poiché le informazioni sui segmenti dei clienti vengono costantemente aggiornate, i clienti possono associarsi e dissociarsi da un segmento mentre fanno acquisti nel negozio.

Puoi attivare i tipi di pubblico in una vetrina Luma o [headless](#headless-support) vetrina. In una vetrina Luma, le informazioni sul pubblico (iscrizione al segmento) vengono memorizzate in un cookie sul lato Commerce. In una vetrina headless, le informazioni sul pubblico vengono trasmesse nell’intestazione API di GraphQL come parametro denominato: `aep-segments-membership`.

## Note sulla versione

Questa sezione contiene informazioni sugli aggiornamenti dell&#39;estensione Audience Activation e include:

![Nuovo](../assets/new.svg) - Nuove funzioni
![Correzione](../assets/fix.svg) - Correzioni e miglioramenti
![Bug](../assets/bug.svg) - Problemi noti

Consulta [Prossime versioni](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) per informazioni sulle pianificazioni delle versioni e sul supporto.

Consulta la documentazione per gli sviluppatori per [informazioni sulla compatibilità dei prodotti](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## Aggiornamenti dei servizi supportati

Queste note sulla versione descrivono modifiche e correzioni di funzioni relative alle estensioni utilizzate da Audience Activation.

+++Aggiornamenti dei servizi supportati

_15 agosto 2023_

![Correzione](../assets/fix.svg) - Aggiornato il [Dashboard di Real-Time CDP Audiences](#real-time-cdp-audiences-dashboard) per semplificare il filtro.

_27 giugno 2023_

![Correzione](../assets/fix.svg) - Aggiunta del supporto per PHP 8.2 nel `magento/module-data-services-graphql` pacchetto.

_30 maggio 2023_

![Nuovo](../assets/new.svg) - Aggiornato il [Dashboard di Real-Time CDP Audiences](#real-time-cdp-audiences-dashboard) per includere la possibilità di ordinare, cercare e filtrare i tipi di pubblico attivi all’interno della tua istanza di Adobe Commerce.

+++

### 2.2.0-beta1

[!BADGE Compatibilità]{type=Informative tooltip="Compatibilità"}

_16 febbraio 2024_

![Nuovo](../assets/new.svg) - Se partecipi alla versione beta, assicurati che il tuo `composer.json` il file presenta le seguenti caratteristiche a livello di radice: ` "minimum-stability": "beta"`.
![Nuovo](../assets/new.svg) - (**Beta** a) Aggiunta la possibilità di creare [regole prodotto correlate](../merchandising-promotions/product-related-rule-create.md) informato dal pubblico.

### 2.1.0.

[!BADGE Compatibilità]{type=Informative tooltip="Compatibilità"}

_24 gennaio 2024_

![Nuovo](../assets/new.svg) - Aggiornato il [Dashboard di Real-Time CDP Audiences](#real-time-cdp-audiences-dashboard) per includere i siti web che contengono i tipi di pubblico e specificare quali blocchi dinamici e regole di prezzo del carrello sono configurati per utilizzare tali tipi di pubblico.

### 2.0.1.

[!BADGE Compatibilità]{type=Informative tooltip="Compatibilità"}

_16 novembre 2023_

![Correzione](../assets/fix.svg) - Maggiore stabilità.

### 2,0,0

[!BADGE Compatibilità]{type=Informative tooltip="Compatibilità"}

_10 ottobre 2023_

![Nuovo](../assets/new.svg) - Aggiunta del supporto per OAuth 2.0 quando [configura](#configure-the-extension) l’estensione Audience Activation.
![Correzione](../assets/fix.svg) - Maggiore stabilità.

### 1.2.0.

[!BADGE Compatibilità]{type=Informative tooltip="Compatibilità"}

_15 agosto 2023_

![Correzione](../assets/fix.svg) - È stata aggiornata la versione dei componenti dell’interfaccia utente.

### 1.1.0.

_30 maggio 2023_

[!BADGE Compatibilità]{type=Informative tooltip="Compatibilità"}

![Nuovo](../assets/new.svg) - Aggiunta del supporto per [blocchi dinamici](#headless-support) in una vetrina headless.

### 1.0.1.

_11 maggio 2023_

[!BADGE Compatibilità]{type=Informative tooltip="Compatibilità"}

![Correzione](../assets/fix.svg) - È stato risolto un problema a causa del quale una regola del prezzo di blocco dinamico o carrello non veniva applicata alla vetrina.
![Correzione](../assets/fix.svg) - È stato risolto un problema che causava un errore durante l’installazione non configurata dell’estensione Audience Activation quando un commerciante tentava di creare o aggiornare un blocco dinamico.

### 1,0,0

_31 marzo 2023_

[!BADGE Compatibilità]{type=Informative tooltip="Compatibilità"}

![Nuovo](../assets/new.svg) - Versione di disponibilità generale

## Implementazione

Le seguenti attività si applicano sia alle implementazioni Luma che alla vetrina headless. Per attivare i tipi di pubblico in Adobe Commerce, devi:

- Installare Adobe Commerce versione 2.4.4 o successiva
- [Attiva](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Adobe Commerce come destinazione in Real-Time CDP
- [Installa](#install-the-extension) il [!DNL Audience Activation] estensione in Admin
- [Configura](#configure-the-extension) il [!DNL Audience Activation] estensione in Admin

### Installare l’estensione

Installare [!DNL Audience Activation] estensione da [marketplace](https://commercemarketplace.adobe.com/magento-audiences.html), o esegui il seguente comando:

```bash
composer require magento/audiences
```

### Configurare l&#39;estensione

Dopo aver installato [!DNL Audience Activation] devi accedere al tuo amministratore Commerce e completare le seguenti operazioni:

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [Accedi](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) sul tuo account Adobe e seleziona il tuo ID organizzazione.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. In **[!UICONTROL Datastream ID]** incolla l’ID dello stream di dati creato quando [attivato](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Adobe Commerce come destinazione in Real-Time CDP.

   Questo flusso di dati invia i dati dal sito Web Commerce a Real-Time CDP per determinare se un acquirente appartiene a un pubblico. Se non hai ancora creato un flusso di dati, [creare](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) uno in Experience Platform, [aggiungi](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) alla destinazione Commerce in Real-Time CDP e alla [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) in Admin.

   >[!NOTE]
   >
   >Quando specifichi un ID dello stream di dati, [associarlo a un sito Web specifico](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) nel [!DNL Data Connection] estensione. Se il tuo punto vendita Commerce ha più siti web, [creare una destinazione](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) per ogni sito web in Real-Time CDP e utilizza un ID di flusso di dati diverso per ciascuno di essi.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Espandi **[!UICONTROL Services]** e seleziona **[!UICONTROL [!DNL Data Connection]]**.

1. [Aggiungi](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details) dettagli dell&#39;account del servizio e delle credenziali.

## Dove utilizzare i tipi di pubblico di Real-Time CDP in Commerce

Con il [!DNL Audience Activation] abilitata, puoi:

- [Creare una regola di prezzo del carrello](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) informato dal pubblico
- [Creare un blocco dinamico](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) informato dal pubblico
- [(**Beta** a) Creare una regola di prodotto correlata](../merchandising-promotions/product-related-rule-create.md) informato dal pubblico

## Dashboard dei tipi di pubblico di Real-Time CDP

Puoi visualizzare tutto [attivo](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) tipi di pubblico disponibili per la personalizzazione all’interno dell’istanza di Adobe Commerce utilizzando **Pubblico Real-Time CDP** dashboard.

Per accedere al **Pubblico Real-Time CDP** dashboard, vai al _Amministratore_ barra laterale, quindi vai a **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

![Dashboard di Real-Time CDP Audiences](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

Il dashboard contiene i campi seguenti:

| Colonna | Descrizione |
|--- |--- |
| `Hide filters` | Consente di mostrare o nascondere i filtri che è possibile applicare al dashboard. Attualmente, l’unico filtro applicabile è `Last updated`. Questo filtro consente di selezionare un intervallo di date per i tipi di pubblico in base a quando sono stati aggiornati l’ultima volta. |
| `Search` | Consente di cercare i tipi di pubblico attivi nell’istanza Commerce. |
| `Name` | Nome assegnato al pubblico in Real-Time CDP. |
| `Origin` | Indica da dove proviene il pubblico, ad esempio `Experience Platform`. |
| `Websites` | Indica quali siti web sono configurati per utilizzare i tipi di pubblico. |
| `Dynamic Blocks` | Indica quali blocchi dinamici sono configurati per utilizzare i tipi di pubblico. |
| `Cart Price Rules` | Indica quali regole di prezzo del carrello sono configurate per utilizzare i tipi di pubblico. |
| `Last updated` | Indica quando il pubblico è stato modificato in Real-Time CDP. |
| `Sync now` | Recupera il pubblico nuovo o aggiornato da Real-Time CDP. |
| `Customize table` | Consente di mostrare o nascondere `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules`, e `Last updated` colonne. |

{style="table-layout:auto"}

## Supporto headless

Puoi attivare i tipi di pubblico in un’istanza di Adobe Commerce headless, ad esempio AEM e PWA, per visualizzare le regole del prezzo del carrello, le regole dei prodotti correlate o i blocchi dinamici in base ai tipi di pubblico.

### Regole di prezzo del carrello e regole di prodotto correlate

Per le regole di prezzo del carrello e le regole di prodotto correlate, una vetrina headless comunica all’Experience Platform tramite [Commerce integration framework (CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). Il framework fornisce un’API lato server che viene implementata utilizzando GraphQL. Le informazioni sul pubblico, come il segmento di un acquirente, passano a Commerce tramite un parametro di intestazione GraphQL denominato: `aep-segments-membership`.

L’architettura generale è la seguente:

![Invio di dati da Headless Storefront al back-end](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

Dopo di te [installare](#install-the-extension) e [configura](#configure-the-extension) L’estensione, Experienci Platform Web SDK, contiene le informazioni sul pubblico sotto forma di iscrizione al segmento.

Per acquisire le appartenenze ai segmenti dall’SDK, consulta questa [frammento di codice](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

Una volta recuperato, puoi passare tali segmenti a Commerce all’interno dell’intestazione GraphQL. Ad esempio:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### Blocchi dinamici

Per i blocchi dinamici, GraphQL `dynamicBlocks` le query possono contenere `audience_id` attributo di input. Se si specificano uno o più `audience_id` valori in una `dynamicBlocks` restituisce un elenco di blocchi dinamici assegnati a tali tipi di pubblico.

#### Esempio di utilizzo

La query seguente restituisce tutti i blocchi dinamici associati a più ID di pubblico.

**Richiesta:**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**Risposta:**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

Ulteriori informazioni su `dynamicBlocks` Query GraphQL in [documentazione per sviluppatori](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Recuperare il pubblico con l’SDK di Adobe Experience Platform Mobile

Prima di poter recuperare i tipi di pubblico di Real-Time CDP con l’SDK di Adobe Experience Platform Mobile, è necessario: [installare e configurare l’SDK per il sito Commerce mobile](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>L’SDK di Adobe Experience Platform Mobile per iOS supporta iOS 11 o versione successiva.

Dopo aver completato la configurazione, utilizza le operazioni SDK per dispositivi mobili per recuperare i dati sul pubblico. Ad esempio:

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }
         
                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

Una volta recuperati i dati, puoi utilizzarli per creare contenuti informati sul pubblico [regole prezzi carrello](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [blocchi dinamici](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) e  [regole prodotto correlate](../merchandising-promotions/product-related-rule-create.md) nell’app Commerce.

## I tipi di pubblico non vengono visualizzati in Commerce

Se i tipi di pubblico di Real-Time CDP non vengono visualizzati in Commerce, la causa potrebbe essere:

- Tipo di autenticazione non corretto selezionato in **Connessione dati** pagina di configurazione
- Privilegi insufficienti sul token generato

Nelle due sezioni seguenti viene descritto come risolvere i problemi relativi a entrambi i casi.

### Tipo di autenticazione non corretto selezionato nella configurazione

1. Apri l’istanza Commerce.
1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. Espandi **[!UICONTROL Services]** e seleziona **[!UICONTROL [!DNL Data Connection]]**.
1. Verificare il metodo di autorizzazione server-to-server specificato in **[!UICONTROL Authentication Type]** il campo è corretto. L’Adobe consiglia di utilizzare **OAuth**. Il codice JWT è stato dichiarato obsoleto. [Ulteriori informazioni](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### Privilegi insufficienti sul token generato

Questo problema può essere causato da privilegi API insufficienti per il token generato. Per verificare che il token disponga dei privilegi corretti:

1. Identifica l’amministratore di sistema per Adobe Experience Platform nella tua organizzazione.
1. Trova il progetto e le credenziali che userai.
1. Identifica l’e-mail dell’account tecnico, ad esempio: `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`.
1. Chiedere all&#39;amministratore di sistema di avviare Adobe Experience Platform e passare a **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**.
1. Utilizzando l’e-mail dell’account tecnico di cui sopra, cerca le credenziali da modificare.
1. Apri le credenziali, quindi seleziona **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**.
1. Aggiungi **Production all access**.
1. Clic **[!UICONTROL Save]**.
1. [Rigenera](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token) il token di accesso nella console.
1. Verifica che il token fornisca una risposta valida utilizzando [API connessioni di Target](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections).
