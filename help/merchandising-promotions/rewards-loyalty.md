---
title: Programmi di fidelizzazione e ricompensa
description: Scopri il sistema di punti premio che puoi utilizzare per stimolare il coinvolgimento dei clienti e promuovere la loro fedeltà.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: 3376b6f4fd558f7dd10133beeabf87e7228776a1
workflow-type: tm+mt
source-wordcount: '1395'
ht-degree: 0%

---

# Programmi di fidelizzazione e ricompensa

{{ee-feature}}

Il sistema di _punti premio_ in Adobe Commerce consente di implementare programmi univoci che stimolano il coinvolgimento dei clienti e ne promuovono la fidelizzazione. I punti possono essere assegnati per un&#39;ampia gamma di operazioni e attività dei clienti e la configurazione può essere impostata per controllare l&#39;assegnazione dei punti, il saldo e la scadenza. I clienti possono riscattare i punti verso gli acquisti in base al tasso di conversione stabilito tra punti premio e valuta.

## Regole prezzi carrello

I punti possono essere ricompensati ai clienti in base a una [regola carrello acquisti](price-rules-cart.md). Possono essere ricompensate come unica azione della regola del prezzo, o insieme a uno sconto.

## Saldo cliente

I saldi dei punti premio possono essere gestiti dagli utenti amministratore per cliente. Se abilitati nella vetrina, i clienti possono anche visualizzare i dettagli del saldo dei loro punti.

## Rimborso di punti

>[!NOTE]
>
>[La configurazione dei tassi di cambio premi](reward-exchange-rates.md) è necessaria per il rimborso dei punti premio da parte dei clienti e degli utenti amministratori durante l&#39;estrazione.

I punti possono essere riscattati dagli utenti amministratori e dai clienti (se abilitati) durante il pagamento. Nella sezione Metodo di pagamento, sopra i metodi di pagamento abilitati viene visualizzata la casella di controllo Usa i miei punti premio. Sono inclusi i punti disponibili e il tasso di cambio monetario. Se il saldo disponibile è maggiore del totale complessivo dell&#39;ordine, non è richiesto alcun metodo di pagamento aggiuntivo. Il numero di punti premio applicati all&#39;ordine viene visualizzato con i totali dell&#39;ordine, sottratti dal totale complessivo, in modo analogo alle carte di credito o regalo di un negozio. Se i punti premio vengono utilizzati insieme al credito del negozio o a una gift card, i punti premio vengono dedotti per primi. La carta di credito o regalo del negozio viene quindi detratta se il totale dell&#39;ordine è maggiore del numero di punti premio rimborsabili.

>[!NOTE]
>
>I punti premio non sono consigliati per l&#39;uso con gli acquisti COD, perché la ricezione del pagamento non può essere confermata fino a quando l&#39;ordine non è fatturato.

## Rimborso per punti premio

Gli ordini inseriti con punti premio possono essere rimborsati al saldo dei punti premio fino all&#39;importo rimborsato nell&#39;ordine. Nella pagina [_Nuova nota di credito_](../stores-purchase/credit-memo-create.md) è possibile immettere il numero di punti da applicare al saldo del cliente. Per impostazione predefinita, il campo contiene il numero completo di punti utilizzati nell’ordine.

## Abilitare le operazioni dei punti premio per il punto vendita

La configurazione Punti premio determina la modalità di presentazione dei punti premio nell&#39;archivio e definisce i parametri operativi di base.

![Configurazione clienti - punti premio](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Passaggio 1: Configurare i punti premio

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Reward Points]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Reward Points]** ed effettuare le seguenti operazioni:

   - Per attivare i punti premio, impostare **[!UICONTROL Enable Reward Points Functionality]** su `Yes`.

   - Per consentire ai clienti di guadagnare i propri punti premio, impostare **[!UICONTROL Enable Reward Points Functionality on Storefront]** su `Yes`.

   - Per consentire ai clienti di visualizzare una cronologia dettagliata dei loro premi, impostare **[!UICONTROL Customers May See Reward Point History]** su `Yes`.

1. Per **[!UICONTROL Reward Points Balance Redemption Threshold]**, immettere il numero di punti che devono essere accumulati prima di poter essere riscattati (vuoto per nessun minimo).

1. Per **[!UICONTROL Cap Reward Points Balance At]**, immettere il numero massimo di punti che un cliente può accantonare (vuoto per nessun limite).

1. Per **[!UICONTROL Reward Points Expire in (days)]**, immettere il numero di giorni prima della scadenza dei punti premio (vuoto per nessuna scadenza).

1. Imposta **[!UICONTROL Reward Points Expiry Calculation]** su uno dei seguenti:

   - `Static` - Determina la durata residua dei punti premio in base al numero di giorni impostati nella configurazione. Se il limite di scadenza nella configurazione cambia, la data di scadenza dei punti esistenti non cambia.

   - `Dynamic` - Calcola il numero di giorni rimanenti ogni volta che il saldo del punto premio aumenta. Se il limite di scadenza nella configurazione cambia, la scadenza di tutti i punti esistenti viene aggiornata di conseguenza.

1. Per rimborsare automaticamente i punti premio disponibili, impostare **[!UICONTROL Refund Reward Points Automatically]** su `Yes`.

1. Per annullare i punti premio ottenuti con gli acquisti quando l&#39;ordine che ha ottenuto i punti viene rimborsato completamente o parzialmente, impostare **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** su `Yes`.

   >[!NOTE]
   >
   >Sono interessati solo i punti guadagnati con l&#39;ordine che viene rimborsato.

1. Impostare **[!UICONTROL Landing Page]** sulla pagina di contenuto che spiega il programma dei punti premio.

   Assicurati di aggiornare la pagina Punti premio predefinita con le tue informazioni.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

### Passaggio 2: Configurare i punti guadagnati per le attività del cliente

In questo passaggio viene specificato il numero di punti premio che possono essere ottenuti per varie attività del cliente. Quando i clienti completano un’azione a cui sono assegnati punti, viene visualizzato un messaggio che indica quanti punti hanno guadagnato.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Actions for Acquiring Reward Points by Customer]**.

   ![Configurazione clienti - azioni per l&#39;acquisizione di punti premio da parte del cliente](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. Per consentire l&#39;accumulo di punti premio per gli acquisti basati sui [tassi di cambio premio](reward-exchange-rates.md) configurati, impostare **[!UICONTROL Purchase]** su `Yes`.

   >[!NOTE]
   >
   >Per guadagnare punti premio per il loro ordine _first_, il cliente deve essere registrato _prima_ che la transazione venga acquisita dal metodo di pagamento. La maggior parte dei metodi di pagamento potrebbe essere configurata per acquisire le transazioni _automaticamente_ quando l&#39;ordine viene effettuato, ma _prima_ la registrazione dell&#39;account cliente è terminata.

1. Per **[!UICONTROL Registration]**, immettere il numero di punti guadagnati per l&#39;apertura di un conto cliente.

1. Per **[!UICONTROL Newsletter Signup]**, immettere il numero di punti guadagnati dai clienti registrati che si abbonano a una newsletter.

1. Per **[!UICONTROL Converting Invitation to Customer]**, immettere il numero di punti guadagnati da un cliente che invia un invito e il destinatario apre un account cliente.

   Puoi limitare il numero di conversioni di inviti che possono essere utilizzate per guadagnare punti per il cliente che invia l’invito (vuoto per nessun limite). A tale scopo, immettere un numero nel campo **[!UICONTROL Invitation to Customer Conversions Quantity Limit]**.

1. Per **[!UICONTROL Converting Invitation to Order]**, immetti il numero di punti guadagnati da un cliente che invia un invito al destinatario che effettua un ordine ed effettua le seguenti operazioni:

   - Per **Invito a conversioni ordine Limite quantità**, immettere il numero di punti guadagnati dal cliente che invia l&#39;invito quando il destinatario effettua un ordine iniziale (vuoto per nessun limite).

   - Per **[!UICONTROL Invitation Conversion to Order Reward]**, selezionare l&#39;opzione `Each` per guadagnare punti per ogni ordine effettuato dal destinatario oppure selezionare l&#39;opzione `First` per guadagnare punti solo per il primo ordine effettuato dal destinatario.

1. Per **[!UICONTROL Review Submission]**, immettere il numero di punti guadagnati da un cliente che invia una revisione approvata per la pubblicazione.

1. Quindi, per limitare il numero di recensioni che possono essere utilizzate per guadagnare punti per cliente, immetti il numero nel campo **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** (vuoto per nessun limite).

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

### Passaggio 3: Completa le impostazioni delle notifiche e-mail

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Email Notification Settings]**.

   ![Configurazione clienti - Notifiche e-mail punti premio](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Impostare **[!UICONTROL Email Sender]** sul contatto dell&#39;archivio che viene visualizzato come mittente degli aggiornamenti del saldo e delle notifiche di scadenza.

1. Se si desidera sottoscrivere i clienti per impostazione predefinita per ricevere notifiche sugli aggiornamenti del saldo e sulle prossime date di scadenza, impostare **[!UICONTROL Subscribe Customers by Default]** su `Yes`.

1. Imposta **[!UICONTROL Balance Update Email]** sul modello utilizzato per la notifica inviata ai clienti ogni volta che il loro saldo punti viene aggiornato.

1. Impostare **[!UICONTROL Reward Points Expiry Warning Email]** sul modello utilizzato per la notifica inviata ai clienti quando viene raggiunto il limite di scadenza per un batch di punti.

1. Per **[!UICONTROL Expiry Warning Before (days)]**, immettere il numero di giorni prima della scadenza dei punti per l&#39;invio della notifica.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Aggiorna il saldo dei punti premio

Il saldo dei punti premio può essere aggiornato dall’Amministratore.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Trovare il cliente nella griglia e fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

1. In _Informazioni cliente_, scegliere la sezione **[!UICONTROL Reward Points]**.

1. Immettere il numero di **[!UICONTROL Update Points]**:

   - Per aggiornare l&#39;importo dei punti premio, inserire il numero per aumentare il saldo totale dei punti.
   - Per sottrarre l&#39;importo dei punti premio, immettere il numero negativo che si desidera ridurre il saldo totale dei punti.

1. Immettere **[!UICONTROL Comments]** relativi all&#39;adeguamento dei punti premio, se necessario.

   ![Saldo punti premio](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. È possibile sottoscrivere il cliente a _Notifiche punti premio_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Fare clic su **[!UICONTROL Save Customer]**.

Tutte le azioni relative ai punti premio vengono visualizzate nel blocco _[!UICONTROL Reward Points History]_del cliente sul suo account nella vetrina.

## Descrizioni dei campi

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Balance] | Saldo corrente dei punti premio per il cliente |
| [!UICONTROL Amount Balance] | Importo del saldo di cassa corrente |
| [!UICONTROL Points] | Numero di punti aggiunti o sottratti |
| [!UICONTROL Amount] | Somma di denaro aggiunto o sottratto |
| [!UICONTROL Rate] | Il [tasso di cambio premio](reward-exchange-rates.md) |
| [!UICONTROL Website] | Sito Web a cui è assegnata la cronologia dei punti premio |
| [!UICONTROL Reason] | Motivi per l&#39;assegnazione dei punti:<br>**[!UICONTROL Making purchases]**— Ogni volta che il cliente effettua un acquisto, può guadagnare punti.<br>**[!UICONTROL Registering on the site]** - Accantonato al momento della registrazione (una volta).<br>**[!UICONTROL Subscribing to a newsletter]**- Accantonata per la prima sottoscrizione (una volta).<br>**[!UICONTROL Sending Invitations]** - Guadagna punti invitando i propri amici a partecipare al sito.<br>**[!UICONTROL Converting Invitations to Customer]**— Guadagna punti per ogni invito inviato, amici principali che si registrano sul sito.<br>**[!UICONTROL Converting Invitations to Order]** — Guadagna punti per ogni vendita derivante da un invito inviato.<br>**[!UICONTROL Review Submission]**— Guadagna punti per l&#39;invio di recensioni di prodotti. |
| [!UICONTROL Created] | Data e ora dell&#39;aggiornamento dei punti premio |
| [!UICONTROL Expired] | Numero di punti premio scaduti |
| [!UICONTROL Comment] | Commenti durante l&#39;aggiunta o la sottrazione di punti |

{style="table-layout:auto"}

## Risorse per la risoluzione dei problemi

Per informazioni sulla risoluzione dei problemi relativi ai punti premio, vedere i seguenti articoli della Knowledge Base di supporto Commerce:

- [Punti fedeltà su ordini parziali](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31295-magento-patch-loyalty-points-on-partial-orders.html)
- [errore 404 - rimozione dei punti premio in caso di pagamento con spedizione multipla](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
