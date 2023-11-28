---
title: Creare etichette e pacchetti di spedizione
description: Scopri come imballare gli articoli in un ordine e creare etichette di spedizione.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '1896'
ht-degree: 0%

---

# Crea etichette di spedizione

Per creare le etichette di spedizione, devi prima impostare l&#39;account del vettore di spedizione per supportare le etichette. Quindi, seguire le istruzioni per immettere una descrizione del pacchetto e del relativo contenuto.

Dopo aver configurato le informazioni sull’etichetta di spedizione e aver inviato un ordine, Commerce si connette al sistema del vettore di spedizione, invia un ordine e riceve un’etichetta di spedizione e un numero di registrazione. Se nel sistema esiste un&#39;etichetta di spedizione per questa spedizione, questa viene sostituita con una nuova. Tuttavia, i numeri di tracciamento esistenti non vengono sostituiti. Qualsiasi nuovo numero di tracciamento viene aggiunto a quello esistente.

## Passo 1: Contattare i vettori di spedizione

Prima di iniziare, assicurati che gli account di spedizione siano impostati per elaborare le etichette. Alcuni vettori potrebbero addebitare una tariffa aggiuntiva per aggiungere le etichette di spedizione al tuo account.

Contatta ogni vettore che utilizzi per attivare le etichette di spedizione per il tuo negozio.

Segui le istruzioni fornite da ciascun vettore per aggiungere il supporto per le etichette di spedizione al tuo account.

- **FedEx** - Contatto [Servizi di integrazione Web FedEx][1] per informazioni sui requisiti di stampa delle etichette per il tuo account.
- **USP** - Fare riferimento alla [Portale API degli strumenti web][4] in Centro di supporto corriere per scoprire come impostare le credenziali per la stampa delle etichette.
- **UPS**- Contatto [UPS][2] per confermare che il tuo account supporta le etichette di spedizione. Per generare le etichette di spedizione, è necessario utilizzare l&#39;opzione XML UPS.
- **DHL** - Contatto [Soluzioni eCommerce DHL][3] per informazioni sui requisiti di stampa delle etichette per il tuo account.

## Passaggio 2: aggiorna la configurazione per ciascun gestore

1. Assicurati che il tuo [Informazioni sul negozio](../getting-started/store-details.md#store-information) è stato completato.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e seleziona **[!UICONTROL Shipping Settings]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Origin]** e configurare il **[!UICONTROL Shipping Origin Address]**.

1. Segui le istruzioni riportate di seguito per ogni account vettore attivato per la stampa delle etichette.

### Configurazione gruppo di continuità

La United Parcel Service è un servizio di spedizione pacchi sia a livello nazionale che internazionale. Tuttavia, le etichette di spedizione possono essere generate solo per le spedizioni provenienti dagli Stati Uniti.

1. In _[!UICONTROL Sales]_nel pannello a sinistra, scegli **[!UICONTROL Delivery Methods]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL UPS]** sezione.

1. Verificare che il gruppo di continuità **[!UICONTROL Shipper Number]** è corretta.

   Il numero del corriere viene visualizzato solo quando [!DNL United Parcel Service XML] è abilitato.

1. Clic **[!UICONTROL Save Config]**.

### Configurazione USPS

Il [!DNL United States Postal Service] navi sia a livello nazionale che internazionale.

1. Continuando in **[!UICONTROL Delivery Methods]** , espandere ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL USPS]** sezione.

1. Verificare che **[!UICONTROL Secure Gateway URL]** è corretta.

1. Inserisci il **[!UICONTROL Password]** forniti da USPS.

1. Imposta **[!UICONTROL Size]** a `Large` e immettere i valori per le dimensioni seguenti:

   - Lunghezza
   - Larghezza
   - Altezza
   - Girth

1. Clic **[!UICONTROL Save Config]**.

### Configurazione FedEx

FedEx viene spedito a livello nazionale e internazionale. I negozi situati al di fuori degli Stati Uniti possono creare etichette FedEx solo per le spedizioni internazionali.

{{beta2-updates}}

1. Continuando in **[!UICONTROL Delivery Methods]** , espandere ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL FedEx]** sezione.

1. Verifica che le seguenti credenziali FedEx siano corrette:

   - Numero misuratore
   - Chiave
   - Password

1. Clic **[!UICONTROL Save Config]**.

### Configurazione DHL

DHL fornisce servizi di spedizione internazionali.

1. Continuando in **[!UICONTROL Delivery Methods]** , espandere ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL DHL]** sezione.

1. Verificare che **[!UICONTROL Gateway URL]** è corretta.

1. Verifica che le seguenti credenziali siano complete:

   - ID accesso
   - Password
   - Numero account

1. Clic **[!UICONTROL Save Config]**.

## Passaggio 3: creare le etichette di spedizione

### Metodo 1: creare l&#39;etichetta per la nuova spedizione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Individuare l&#39;ordine nella griglia e aprire il record.

   Lo stato dell’ordine deve essere `Pending` o `Processing`.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Ship]**.

1. Confermare le informazioni sulla spedizione in base ai requisiti del vettore.

1. Nell’angolo in basso a destra, seleziona la **[!UICONTROL Create Shipping Label]** casella di controllo.

1. Clic **[!UICONTROL Submit Shipment]**.

1. Aggiungi o aggiorna prodotti nel pacchetto:

   - Per aggiungere prodotti dall’ordine al pacchetto, fai clic su **[!UICONTROL Add Products]**. Il _[!UICONTROL Quantity]_Questa colonna mostra il numero massimo di prodotti disponibili per il pacchetto.

   - Selezionare la casella di controllo di ciascun prodotto da aggiungere alla confezione e immettere **[!UICONTROL Quantity]** di ciascuno. Quindi, fai clic su **[!UICONTROL Add Selected Product(s) to Package]**.

   - Per aggiungere un pacchetto, fai clic su **[!UICONTROL Add Package]**.

   - Per eliminare un pacchetto, fare clic su **[!UICONTROL Delete Package]**.

   - Per annullare un ordine, fai clic su **[!UICONTROL Cancel]**. L&#39;etichetta di spedizione non viene creata e _[!UICONTROL Create Shipping Label]_la casella di controllo è deselezionata.

   >[!NOTE]
   >
   >Se si utilizza un tipo di pacchetto diverso da quello predefinito o si richiede una firma, il costo di spedizione potrebbe essere diverso da quello applicato al cliente. Qualsiasi differenza nel costo di spedizione non si riflette nel tuo negozio.

1. Clic **[!UICONTROL OK]**.

   Commerce si connette al sistema del vettore di spedizione, invia l’ordine e riceve un’etichetta di spedizione e un numero di registrazione per ciascun pacchetto.

### Metodo 2: creazione dell&#39;etichetta per la spedizione esistente

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Individuare l&#39;ordine nella griglia e aprire il modulo di spedizione.

1. In _[!UICONTROL Shipping and Tracking Information]_, fare clic su **[!UICONTROL Create Shipping Label]**.

1. Distribuisci i prodotti ordinati nei pacchetti appropriati e fai clic su **[!UICONTROL OK]**.

1. Per rivedere le informazioni del pacchetto, fare clic su **[!UICONTROL Show Packages]**.

## Passaggio 4: stampare le etichette

Le etichette di spedizione vengono generate in formato PDF e possono essere stampate dall’amministratore. Ciascuna etichetta include il numero d’ordine e il numero della confezione.

>[!NOTE]
>
>Poiché viene creato un singolo ordine di spedizione per ciascun pacchetto, è possibile che vengano ricevute più etichette di spedizione per una singola spedizione.

### Metodo 1: Stampa etichetta da modulo spedizione

1. Il giorno _Barra laterale di amministrazione_, passare a una delle pagine seguenti e quindi individuare il record di spedizione:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Individuare l&#39;ordine nella griglia e aprire il record. Nel pannello a sinistra, scegli **[!UICONTROL Shipments]**. Quindi, aprire il record di spedizione.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Individuare la spedizione nella griglia e aprire il record.

1. Per scaricare il file PDF, vai al _[!UICONTROL Shipping and Tracking]_del modulo e fai clic su **[!UICONTROL Print Shipping Label]**.

   A seconda delle impostazioni del browser, le etichette di spedizione possono essere visualizzate e stampate direttamente dal file PDF.

   Il _[!UICONTROL Print Shipping Label]_viene visualizzato solo dopo che il vettore ha generato le etichette per la spedizione. Se manca il pulsante, fai clic su **[!UICONTROL Create Shipping Label]**. Il pulsante viene visualizzato dopo che Commerce riceve l’etichetta dal gestore.

### Metodo 2: Stampa etichette per più ordini

1. Il giorno _Barra laterale di amministrazione_, passare a una delle pagine seguenti e quindi selezionare gli ordini o le spedizioni da stampare:

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - Nella griglia, selezionare la casella di controllo di ogni ordine con le etichette di spedizione da stampare.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - Nella griglia selezionare la casella di controllo di ogni spedizione con le etichette da stampare.

1. Imposta il **[!UICONTROL Actions]** controllo a `Print Shipping Labels`.

1. Clic **[!UICONTROL Submit]**.

Viene stampato un set completo di etichette di spedizione per ogni spedizione correlata agli ordini selezionati.

## Impostazioni vettore richieste

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Type] | I tipi di pacchetti variano in base al vettore e al metodo. Inizialmente viene selezionato il tipo di pacchetto predefinito per ogni gestore. USPS non richiede il tipo di imballaggio per le spedizioni nazionali. |
| [!UICONTROL Customs Value] | (Solo spedizioni internazionali) Valore o prezzo di vendita dichiarato del contenuto di una spedizione internazionale. |
| [!UICONTROL Total Weight] | Il peso totale di tutti i prodotti aggiunti alla confezione viene calcolato automaticamente. Il valore può anche essere modificato manualmente e immesso come libbre o chilogrammi. |
| [!UICONTROL Length, Width, Height] | (Facoltativo) Le dimensioni del pacchetto vengono utilizzate solo per i pacchetti personalizzati. È possibile specificare le unità di misura in pollici o centimetri.<br/><br/>**[!UICONTROL Not Required]**: il vettore non invia alcuna conferma di consegna al negozio.<br/><br/>**[!UICONTROL No Signature]**: una conferma di consegna senza la firma del destinatario viene inviata al negozio dal vettore di spedizione.<br/><br/>**[!UICONTROL Signature Required]**: il vettore ottiene la firma del destinatario e fornisce al negozio una copia stampata.<br/><br/>**[!UICONTROL Direct]**: (Solo FedEx) FedEx ottiene una firma da qualcuno all’indirizzo di consegna. Se nessuno è disponibile per firmare il pacchetto, il vettore tenta di consegnarlo in un altro momento.<br/><br/>**[!UICONTROL Indirect]**: (Solo consegne residenziali FedEx) FedEx ottiene la firma di qualcuno (possibilmente un vicino o un responsabile dell’edificio) all’indirizzo di consegna. Il destinatario può lasciare un cartellino FedEx firmato per autorizzare il pacchetto a rimanere senza nessuno presente per firmarlo.<br/><br/>**[!UICONTROL Contents]**: (Solo USPS) seleziona una delle seguenti descrizioni del pacchetto:<br/>- Regalo<br/>- Documenti<br/>- Campione commerciale<br/>- Merci in reintroduzione<br/>- Merci<br/>- Altro <br/><br/>**[!UICONTROL Explanation]**: (solo USPS) descrizione dettagliata del contenuto del pacchetto.<br/><br/>**[!UICONTROL Adult Required]**: il corriere ottiene la firma di un destinatario adulto e fornisce al negozio una copia stampata. |

{style="table-layout:auto"}

## Creare pacchetti

Il _[!UICONTROL Create Packages]_viene visualizzata quando si sceglie di creare un&#39;etichetta di spedizione. Puoi iniziare immediatamente a configurare il primo pacchetto.

### Configurare un pacchetto

>[!NOTE]
>
>Se si seleziona il valore non predefinito per [!UICONTROL Type] o scegliere di richiedere una conferma della firma, il prezzo di una spedizione può differire da quello che hai addebitato al cliente.

1. Per visualizzare un elenco dei prodotti spediti e aggiungerli alla confezione, fare clic su **[!UICONTROL Add Products]**.

   - Specifica i prodotti e le quantità.

     Il _[!UICONTROL Qty]_nella colonna viene visualizzata la quantità massima disponibile da aggiungere. Per il primo imballaggio, il numero corrisponde alla quantità totale del prodotto da spedire.

   - Per aggiungere i prodotti al pacchetto, fai clic su **[!UICONTROL Add Selected Product(s) to Package]**.

1. Per aggiungere un pacchetto, fai clic su **[!UICONTROL Add Package]**.

   Puoi aggiungere più pacchetti e modificarli contemporaneamente.

1. Per eliminare un pacchetto, fare clic su **[!UICONTROL Delete Package]**.

Dopo l’aggiunta dei prodotti alla confezione, la quantità non può essere modificata direttamente.

### Aumenta la quantità

1. Clic **[!UICONTROL Add Selection]**.

1. Inserire la quantità aggiuntiva.

   Il numero viene aggiunto alla quantità precedente del prodotto nella confezione.

### Diminuisci la quantità

1. Elimina il prodotto dalla confezione.

1. Clic **[!UICONTROL Add Selection]**.

1. Immetti il nuovo valore più piccolo.

### Genera etichette di spedizione

Dopo aver distribuito tutti i prodotti, il numero totale dei pacchetti da utilizzare è uguale al numero dell&#39;ultimo pacchetto nell&#39;elenco. Il _OK_ viene disattivato fino a quando tutti gli articoli spediti non vengono distribuiti ai pacchetti e tutte le informazioni necessarie non sono complete.

Per generare le etichette, fai clic su **[!UICONTROL OK]**.

Puoi fare clic su **[!UICONTROL Cancel]** per interrompere il processo, se necessario. I pacchetti non vengono salvati e il processo delle etichette di spedizione viene annullato.

### Descrizioni dei campi

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Type] | Specifica il tipo di pacchetto. Selezionare uno dei valori predefiniti. I tipi di pacchetto disponibili sono diversi per ciascun vettore di spedizione. Quando viene visualizzata la finestra a comparsa Crea pacchetti, nel campo Tipo viene visualizzato il pacchetto predefinito per il vettore di spedizione. Se si seleziona un pacchetto non progettato da un vettore di spedizione, è necessario immettere le dimensioni del pacchetto. Per le etichette di spedizione create per le spedizioni DHL, FedEx e UPS, il campo Tipo di merce è impostato su `Merchandise`. Per USPS, il campo riflette il valore della _Sommario_ campo in _[!UICONTROL Create Packages]_finestra. |
| [!UICONTROL Total Weight] | Peso totale di un pacchetto. Il campo è precompilato con il peso totale dei prodotti in un pacchetto. L&#39;unità di misura può essere impostata su libbre o chilogrammi. |
| [!UICONTROL Length] | Lunghezza di un pacchetto, numeri interi e numeri a virgola mobile. Il campo è abilitato se si utilizza il tipo di pacchetto personalizzato. L&#39;unità di misura può essere impostata su pollici o centimetri. |
| [!UICONTROL Width] | Larghezza di un pacchetto, numeri interi e numeri a virgola mobile. Il campo è abilitato se si utilizza il tipo di pacchetto personalizzato. Le unità di misura possono essere specificate utilizzando il menu a discesa accanto al campo Altezza; selezionare tra pollici e centimetri. |
| [!UICONTROL Height] | Altezza di un pacchetto, numeri interi e numeri a virgola mobile. Il campo è abilitato se si utilizza il tipo di pacchetto personalizzato. Le unità di misura possono essere specificate utilizzando il menu a discesa accanto al campo Altezza; selezionare tra pollici e centimetri. |
| [!UICONTROL Signature] | Definisce la conferma della consegna. Opzioni:<br/><br/>**[!UICONTROL Not Required]**: non ti viene inviata alcuna lettera di conferma della consegna.<br/><br/>**[!UICONTROL No Signature]**: viene inviata all’utente una lettera di conferma della consegna senza la firma di un destinatario.<br/><br/>**[!UICONTROL Signature Required]**: il vettore ottiene la firma del destinatario e ti fornisce la copia stampata.<br/><br/>**[!UICONTROL Adult Required]**: il corriere ottiene la firma del destinatario adulto e ti fornisce la sua copia stampata.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx ottiene una firma da qualcuno all’indirizzo di consegna e ritenta la consegna se nessuno è disponibile per firmare il pacchetto.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx ottiene una firma in uno dei tre modi seguenti:<br/>(1) da qualcuno all’indirizzo di consegna; <br/>2) da un vicino, un responsabile immobiliare o un&#39;altra persona all&#39;indirizzo; o <br/>(3) il destinatario può lasciare un FedEx Door Tag firmato che autorizza il rilascio del pacchetto senza nessuno presente. Disponibile solo per consegne residenziali. Le opzioni possono variare leggermente in base ai diversi metodi di spedizione. Per informazioni più recenti, consulta le risorse del vettore di spedizione. |
| [!UICONTROL Contents] | (Disponibile solo per spedizioni USPS) Descrizione del contenuto del pacchetto. Opzioni: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (Solo spedizioni USPS) Descrizione dettagliata del contenuto della confezione. |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
