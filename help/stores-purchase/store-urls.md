---
title: URL store
description: Scopri gli URL del negozio e come configurare l’URL di base e i codici del negozio.
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1519'
ht-degree: 0%

---

# URL store

Ogni sito web in un’installazione di Adobe Commerce o di Magento Open Source ha un URL di base assegnato alla vetrina e un altro URL assegnato all’amministratore. In questo Adobe le variabili vengono utilizzate per definire collegamenti interni in relazione all’URL di base, consentendo di spostare un intero archivio da una posizione all’altra senza aggiornare i collegamenti. Gli URL di base standard iniziano con `http`, e gli URL di base sicuri iniziano con `https`.

- **URL di base** — `http://www.yourdomain.com/magento/`
- **URL di base sicuro** — `https://www.yourdomain.com/magento/`
- **URL con indirizzo IP** — `http://###.###.###.###/magento/` o `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>Non modificare l’URL amministratore dalla configurazione URL di base predefinita. Per modificare l’URL o il percorso dell’amministratore, consulta [Utilizza un URL amministratore personalizzato](#use-a-custom-admin-url).

## Utilizzare un protocollo sicuro

Gli URL di base per il tuo archivio sono stati inizialmente impostati durante l’installazione di Adobe Commerce. Se al momento era disponibile un certificato di protezione, è possibile specificare per `HTTPS` URL da utilizzare per l’archivio, l’amministratore o entrambi. Se l&#39;installazione di Adobe Commerce include più store o prevedi di aggiungerne altri in un secondo momento, puoi includere il codice dello store nell&#39;URL. Tutte le risorse e le operazioni di Adobe possono essere utilizzate con un protocollo sicuro.

Se al momento dell’installazione non era disponibile un certificato di sicurezza per il dominio, assicurati di aggiornare la configurazione prima di avviare l’archivio. Dopo aver stabilito un certificato di sicurezza per il dominio, è possibile configurare uno o entrambi gli URL di base per il funzionamento con Secure Sockets Layer (SSL) crittografato e [Transport Layer Security][1] (TLS).

>[!IMPORTANT]
>
>L’Adobe consiglia vivamente di trasmettere tutte le pagine di un sito di produzione, incluse le pagine di contenuto e di prodotto, utilizzando un protocollo sicuro.

Adobe Commerce e Magento Open Source possono essere configurati per distribuire tutte le pagine tramite `HTTPS` per impostazione predefinita. Se il tuo archivio è stato funzionante con il protocollo standard, puoi migliorare la sicurezza abilitando [HTTP Strict Transport Security][2] (HSTS) e l’aggiornamento di eventuali richieste di pagina non sicure. HSTS è un protocollo opt-in che impedisce ai browser di eseguire il rendering standard `HTTP` pagine trasmesse con protocollo non sicuro per il dominio specificato. Perché i motori di ricerca potrebbero aver già indicizzato ogni pagina del tuo store con `HTTP` URL, puoi configurare Commerce in modo da aggiornare eventuali richieste di pagine non sicure a `HTTPS` automaticamente, in modo da non perdere traffico. Quando Commerce è configurato per utilizzare URL sicuri sia per la vetrina che per l’amministratore, vengono visualizzati due campi aggiuntivi che ti consentono di abilitare `HSTS`.

## Configurare l’URL di base

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sotto _Generale_ nel pannello a sinistra, scegli **[!UICONTROL Web]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Base URL]** sezione.

   - **[!UICONTROL Base URL]** — Immettere l&#39;URL di base completo per il punto vendita. Assicurati di terminare l’URL con una barra, in modo che possa essere esteso con chiavi URL aggiuntive dal tuo archivio. Ad esempio: `http://yourdomain.com/`

     >[!NOTE]
     >
     >Non modificare il segnaposto nel _[!UICONTROL Base Link URL]_campo. È un segnaposto utilizzato per creare collegamenti relativi all’URL di base.

   - **[!UICONTROL Base URL for Static View Files]** — (Facoltativo) Specificare un percorso alternativo per l&#39;URL di base per i file di visualizzazione statica immettendo il percorso che inizia con il segnaposto seguente:

     \{\{unsecure_base_url}}

   - **[!UICONTROL Base URL for User Media Files]** — (Facoltativo) Specificare un percorso alternativo per l&#39;URL di base dei file multimediali utente immettendo il percorso che inizia con il segnaposto seguente:

     \{\{unsecure_base_url}}

     In un&#39;installazione tipica, non è necessario aggiornare i percorsi dei file di visualizzazione statica o dei file multimediali perché sono relativi all&#39;URL di base.

   ![Configurazione generale: URL della base web](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >I segnaposto racchiusi tra parentesi graffe sono tag di markup per le variabili.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Configurare l’URL di base sicuro

Se il dominio dispone di un certificato di sicurezza valido, puoi configurare gli URL sia della vetrina che dell’amministratore per trasmettere i dati su un canale sicuro (https). Senza un certificato di sicurezza valido, l’archivio non può funzionare con il protocollo protetto (SSL/TLS).

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il _[!UICONTROL Base URLs (Secure])_ ed effettuare le seguenti operazioni:

   ![Configurazione generale - URL di base sicuri](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]** — immettere l&#39;URL di base sicuro completo, seguito da una barra. Ad esempio: `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]** — non modificare il segnaposto nel campo URL del collegamento di base protetto. Viene utilizzato per creare collegamenti relativi all’URL di base sicuro.

   - **[!UICONTROL Secure Base URL for Static View Files]** — (Facoltativo) Specificare un percorso alternativo per l&#39;URL di base protetto per i file di visualizzazione statica immettendo il percorso che inizia con il segnaposto seguente:

     \{\{secure_base_url}}

   - **[!UICONTROL Secure Base URL for User Media Files]** — (Facoltativo) Specificare un percorso alternativo per l&#39;URL di base protetto per i file multimediali utente immettendo il percorso che inizia con il segnaposto seguente:

     \{\{secure_base_url}}

1. Per migliorare la sicurezza, impostare entrambe le opzioni seguenti su `Yes`.

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. Per _[!UICONTROL Enhanced Security Settings]_, eseguire le operazioni seguenti:

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]** — Se si desidera che nell&#39;archivio vengano visualizzate solo le richieste di pagina HTTPS protette, impostare su `Yes`.

   - **[!UICONTROL Upgrade Insecure Requests]** — Per aggiornare le richieste di pagine HTTP standard non protette a HTTPS protetto, impostare su `Yes`.

1. Imposta il **[!UICONTROL Offloader Header]** per il server.

   La maggior parte delle installazioni di Commerce utilizza il valore predefinito `X-Forward-Proto` per identificare il protocollo come `HTTP` o `HTTPS`. Se la configurazione del server utilizza un offloader_header diverso, immetterlo qui.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Includi il codice store negli URL

>[!NOTE]
>
>Quando _Aggiungi codice store agli URL_ è impostata su `Yes`, è necessario includere i codici store negli URL del browser. Questa impostazione assicura che le riscritture URL siano mappate correttamente e che tutte le pagine vengano aperte correttamente, senza _&quot;Pagina 404 non trovata&quot;_ errori.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Sotto _[!UICONTROL General]_nel pannello a sinistra, scegli **[!UICONTROL Web]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL URL Options]** sezione.

1. Imposta **[!UICONTROL Add Store Code]** secondo le tue preferenze:

   - **[!UICONTROL URL with Store Code]**: `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**: `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![Configurazione generale - Opzioni URL web](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Fai clic su **[!UICONTROL Cache Management]** nel messaggio nella parte superiore dell’area di lavoro. Quindi, segui le istruzioni per aggiornare la cache.

   ![Messaggio di gestione della cache](./assets/msg-cache-management.png)

## Risoluzione dei problemi degli URL

Se dopo aver seguito le istruzioni di configurazione, alcune pagine continuano a essere servite con l’URL non sicuro (`http://`), effettuare le seguenti operazioni:

- Modifica l’URL di base (non sicuro) con l’URL HTTPS sicuro.
- Sul server, modifica il `.htaccess` file (o load balancer) in modo che l’URL non protetto venga reindirizzato all’URL protetto.

## Utilizza un URL amministratore personalizzato

As a [best practice per la sicurezza](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf), l’Adobe consiglia di utilizzare un URL amministratore univoco invece del predefinito _admin_ o un termine comune come _backend_. Anche se non protegge direttamente il sito da un determinato attore non valido, può ridurre l&#39;esposizione a script che tentano di ottenere l&#39;accesso non autorizzato.

>[!NOTE]
>
>Verifica con il provider di hosting prima di implementare un URL amministratore personalizzato. Alcuni provider di hosting richiedono un URL standard per soddisfare le regole di protezione del firewall.

In un’installazione tipica, l’URL e il percorso dell’amministratore seguono immediatamente l’URL di base. Il percorso di amministrazione è una directory sotto la directory principale.

- **URL di base predefinito**: `http://yourdomain.com/magento/`
- **Percorso amministratore predefinito**: `admin`
- **URL e percorso predefiniti per amministratori**: `http://yourdomain.com/magento/admin`

Anche se è possibile modificare l’URL e il percorso dell’amministratore in un’altra posizione, eventuali errori rimuovono l’accesso all’amministratore e devono essere corretti dal server.

>[!NOTE]
>
>Per precauzione, non provare a modificare l’URL amministratore personalmente, a meno che non si sappia come modificare i file di configurazione sul server.

### Metodo 1: Cambiare da Amministratore

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL Admin]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Admin Base URL]** sezione.

1. Imposta le opzioni di configurazione per l’URL personalizzato:

   ![Configurazione avanzata - URL Admin Base](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   Se necessario, cancellare il **[!UICONTROL Use system value]** per modificare l&#39;impostazione.

   - Imposta **[!UICONTROL Use Custom Admin URL]** a `Yes`.

   - Inserisci il **[!UICONTROL Custom Admin URL]**: `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >L’URL amministratore deve trovarsi nella stessa installazione di Commerce e avere la stessa directory principale dei documenti della vetrina.

   - Imposta **[!UICONTROL Custom Admin Path]** a `Yes`.

   - Per **[!UICONTROL Custom Admin Path]**, immetti il percorso da utilizzare come nome della cartella di amministrazione personalizzata.

     Esempio: `sample_custom_admin`

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Dopo aver salvato le modifiche, esci dall’amministratore e accedi di nuovo utilizzando il nuovo URL e percorso di amministratore.

### Metodo 2: modificare il percorso di amministrazione dalla riga di comando del server

1. Apri `app/etc/env.php` in un editor di testo e modificare il valore della proprietà `frontName` parametro di `backend` sezione. Quindi, salva il file.

   Assicurati di utilizzare solo caratteri minuscoli.

   >[!NOTE]
   >
   >   Questo metodo consente di modificare il percorso dell’amministratore, ma non l’URL dell’amministratore.

   >[!TIP]
   >
   >Per l’infrastruttura cloud di Adobe Commerce, puoi impostare un percorso di amministrazione personalizzato utilizzando `ADMIN_URL` nell’interfaccia utente di Cloud. Consulta la [Argomento variabili amministratore](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html) nel _Guida di Commerce su infrastruttura cloud_.

   - **Percorso amministratore predefinito**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **Nuovo percorso amministratore**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. Per cancellare la cache, utilizza uno dei seguenti metodi:

   - Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. Quindi, fai clic su **[!UICONTROL Flush Magento Cache]**.
   - Sul server, eseguire le operazioni seguenti:

     ```terminal
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >Le modifiche apportate utilizzando il metodo 1 hanno la priorità rispetto alle modifiche apportate nel `app/etc/env.php` file.

### Metodo 3: modificare il percorso di amministrazione utilizzando Commerce CLI

È possibile utilizzare CLI `setup:config:set` per modificare il percorso di amministrazione. Nell&#39;esempio seguente viene utilizzato `--backend-frontname` opzione per cambiare il percorso dalla directory principale di Commerce a un nuovo percorso amministratore:

```terminal
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

Questo comando aggiorna il `backend` > `frontName` opzione di configurazione in `app/etc/env.php` file.

## Ripristina l’URL amministratore e il percorso amministratore predefiniti

Se hai impostato un URL amministratore non valido o un percorso amministratore e hai perso l’accesso al backend, esiste un modo per correggerlo dalla riga di comando.

1. Per ripristinare l’URL amministratore predefinito, esegui questo comando:

   ```terminal
   php bin/magento config:set admin/url/use_custom 0
   ```

1. Per ripristinare il percorso di amministrazione predefinito (impostato nel `app/etc/env.php` come descritto nel metodo 2), eseguire questo comando:

   ```terminal
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. Per cancellare la cache, utilizza uno dei seguenti metodi:

   - Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**. Quindi, fai clic su **[!UICONTROL Flush Magento Cache]**.
   - Sul server, eseguire le operazioni seguenti:

     ```terminal
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
