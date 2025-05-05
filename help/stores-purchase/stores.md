---
title: Struttura dello store e del sito
description: Scopri la gerarchia di visualizzazione del sito web, dello store e dello store.
exl-id: d745cbd0-151b-4f82-bb6c-fb6b9565a014
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Struttura dello store e del sito

Quando si installa Adobe Commerce o Magento Open Source, viene creata una gerarchia che include una visualizzazione principale per il sito Web, lo store e lo store. Se necessario, puoi creare siti web, store e visualizzazioni dello store aggiuntivi. Ad esempio, oltre al sito web principale, potresti avere altri siti web con un dominio diverso. All&#39;interno di ogni sito web, puoi avere più store e, all&#39;interno di ogni store, visualizzazioni store separate. Molte installazioni hanno un sito web e uno store, ma con più visualizzazioni per supportare lingue diverse.

Prima di iniziare, pianifica in anticipo la gerarchia del catalogo del negozio perché vi si fa riferimento durante l’intera configurazione. Ogni archivio può avere una [categoria principale](../catalog/category-root.md) separata, il che rende possibile avere un set completamente diverso di opzioni del menu principale per ogni archivio.

![Diagramma ambito](./assets/scope-multisite.svg){width="550"}

## Aggiungi store

Una singola installazione di Adobe Commerce o di un Magento Open Source può avere più archivi che condividono un amministratore. Gli archivi che si trovano nello stesso sito web hanno lo stesso indirizzo IP e lo stesso dominio, utilizzano lo stesso certificato di sicurezza e condividono un unico processo di pagamento.

La cosa importante da capire è che gli store utilizzano lo stesso codice e condividono un amministratore. Ogni negozio può avere un catalogo separato, oppure può condividere un catalogo. Ogni archivio può avere una [categoria principale](../catalog/category-root.md) separata, il che rende possibile avere un menu principale diverso per ogni archivio. Gli store possono inoltre disporre di branding, presentazione e contenuto diversi. Pianifica la gerarchia dei punti vendita tenendo conto della crescita futura prima di iniziare, in quanto viene utilizzata durante la configurazione.

![Ambito - più archivi](./assets/scope-multistore.svg){width="550"}

Di seguito sono riportati alcuni esempi di configurazione degli URL per più store:

| URL | Descrizione |
| --- | ----------- |
| `yourdomain.com/store1`<br>`yourdomain.com/store2` | Ogni archivio ha un percorso diverso, ma condivide un dominio. |
| `store1.yourdomain.com`<br>`store2.yourdomain.com` | Ogni archivio ha un sottodominio diverso del dominio primario. |

Le installazioni multi-store di Adobe Commerce devono essere configurate dall’amministratore e anche dalla riga di comando del server. La [Guida alla configurazione](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) di Adobe Commerce fornisce istruzioni dettagliate per la configurazione dell&#39;ambiente server.

### Passaggio 1: scegliere il dominio dello store

Il primo passo è scegliere come posizionare il negozio. Gli archivi devono condividere un dominio, ciascuno deve avere un sottodominio o avere domini chiaramente diversi? Per ogni punto vendita, effettuare una delle seguenti operazioni:

- Per posizionare lo store di un livello sotto il dominio primario, non è necessario eseguire alcuna operazione.
- Configura un sottodominio del dominio principale.
- Imposta un dominio primario diverso.

### Passaggio 2: creare il negozio

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Fare clic su **[!UICONTROL Create Store]** e impostare le opzioni per il nuovo archivio:

   - **[!UICONTROL Web Site]** — Scegliere un sito Web da utilizzare come padre del nuovo archivio. Se l&#39;installazione dispone di un solo sito Web, accettare l&#39;impostazione predefinita (`Main Website`).

   - **[!UICONTROL Name]** — Immettere un nome per il nuovo archivio. Il nome è solo per riferimento interno.

   - **[!UICONTROL Code]** — Immettere un codice in caratteri minuscoli per identificare l&#39;archivio. Esempio: `mainstore`.

   - **[!UICONTROL Root Category]** — Imposta sulla [categoria principale](../catalog/category-root.md) che definisce la struttura delle categorie per il menu principale del nuovo archivio. Se hai già creato una categoria principale specifica per l’archivio, selezionala. In caso contrario, selezionare `Default Category`. Potrai tornare in un secondo momento e aggiornare l’impostazione.

   ![Crea archivio - Opzioni archivio](./assets/stores-all-store-information.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Save Store]**.

### Passaggio 3: creare una visualizzazione predefinita dello store

1. Fare clic su **[!UICONTROL Create Store View]** e impostare le opzioni di visualizzazione dello store:

   - **[!UICONTROL Store]** — Imposta sul nuovo archivio creato.

   - **[!UICONTROL Name]** - Immettere un nome per la visualizzazione. Ad esempio, `English`.

   - **[!UICONTROL Code]** — Immettere un codice per la visualizzazione in caratteri minuscoli.

   - **[!UICONTROL Status]** - Imposta su `Enabled`.

   - **[!UICONTROL Sort Order]** — Immettere un numero per determinare la posizione dell&#39;archivio quando viene elencato con altri archivi.

1. Fare clic su **[!UICONTROL Save Store View]**.

   Se apri il Negozio in modalità di modifica, puoi vedere che ora dispone di una vista predefinita.

   ![Nuovo archivio con visualizzazione predefinita](./assets/new-store-default-view.png){width="600" zoomable="yes"}

### Passaggio 4: configurare l’URL dello store

1. Nella barra laterale _Admin_, fare clic su **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. In _[!UICONTROL General]_&#x200B;nel pannello a sinistra, scegli **[!UICONTROL Web]**.

1. Nell&#39;angolo in alto a sinistra, impostare **[!UICONTROL Store View]** sulla visualizzazione creata per il nuovo archivio.

1. Quando viene richiesto di confermare il passaggio a [scope](../getting-started/websites-stores-views.md#scope-settings), fare clic su **[!UICONTROL OK]**.

   ![Scegliere la visualizzazione dello store](./assets/create-store-config-view.png){width="600" zoomable="yes"}

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Base URLs]** e immettere l&#39;URL di base per l&#39;archivio.

   Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare l&#39;impostazione.

   ![Configurazione generale - URL di base Web](./assets/config-general-web-base-urls-clear-checkbox.png){width="600" zoomable="yes"}

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) della sezione **[!UICONTROL Secure Base URLs]** e ripetere il passaggio precedente se si desidera configurare l&#39;archivio [URL protetto](store-urls.md).

1. Fare clic su **[!UICONTROL Save Config]**.

### Passaggio 5: configurare il server

Per configurare il server per il supporto di più siti Web, vedere [Più siti Web o store](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) nella _Guida alla configurazione_.

Per assistenza nella configurazione del server web, consulta le risorse seguenti:

- [Configura più siti Web con NGNX](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html)
- [Configura più siti Web con Apache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html)

Per Adobe Commerce sull&#39;infrastruttura cloud, vedere [Configurazione di più siti Web o store](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html).

## Aggiungi siti Web

È possibile configurare più siti web da una singola installazione Adobe Commerce o di Magento Open Source con lo stesso dominio o domini diversi. Per impostazione predefinita, gli archivi che si trovano nello stesso sito web hanno lo stesso indirizzo IP e dominio, utilizzano lo stesso certificato di sicurezza e condividono un singolo processo di pagamento. Se desideri che ogni archivio abbia un processo di pagamento dedicato nel proprio dominio, ogni archivio deve avere un indirizzo IP e un certificato di sicurezza separati.

Le installazioni multisito di Adobe Commerce o Magento Open Source devono essere configurate dall’amministratore e anche dalla riga di comando del server. La [Guida alla configurazione](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) di Commerce fornisce istruzioni dettagliate per la configurazione dell&#39;ambiente server.

![Ambito - siti Web](./assets/scope-multisite.svg){width="550"}

### Passaggio 1: creare un sito Web

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Create Website]**.

1. Impostare le opzioni **[!UICONTROL Web Site Information]**:

   ![Crea sito Web - opzioni](./assets/create-website-info.png){width="600" zoomable="yes"}

   - **[!UICONTROL Name]** - Immettere il dominio del nuovo sito Web. Ad esempio, `domain.com`.

   - **[!UICONTROL Code]** — Immettere un codice utilizzato nel server per puntare al dominio.

     Il codice deve iniziare con una lettera minuscola (a-z) e può includere qualsiasi combinazione di lettere (a-z), numeri (0-9) e il simbolo di sottolineatura (_).

   - **[!UICONTROL Sort Order]** — _(Facoltativo)_ Immettere un numero per determinare la sequenza di elencazione del sito con altri siti. Per visualizzare il sito nella parte superiore dell&#39;elenco, immettere uno zero (`0`).

1. Fare clic su **[!UICONTROL Save Web Site]**.

1. Configura ogni [store](#add-stores) e [store view](store-views.md) necessari per il nuovo sito Web.

   Puoi quindi aprire il sito web in modalità di modifica per impostare lo store predefinito.

### Passaggio 2: configurare l’URL dello store

Per configurare gli URL dell&#39;archivio [&#128279;](store-urls.md), seguire le istruzioni.

### Passaggio 3: configurare il server

Per configurare il server per il supporto di più siti Web, vedere [Più siti Web o store](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) nella _Guida alla configurazione_.

Per assistenza nella configurazione del server web, consulta le seguenti esercitazioni:

- [Configura più siti Web con NGNX](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-nginx.html)
- [Configura più siti Web con Apache](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-apache.html)

Per Adobe Commerce sull&#39;infrastruttura cloud, vedere [Configurazione di più siti Web o store](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/multiple-sites.html).
