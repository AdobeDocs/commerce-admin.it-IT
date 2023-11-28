---
title: Staging dei contenuti
description: La gestione temporanea dei contenuti offre al team aziendale la possibilità di creare, visualizzare in anteprima e pianificare facilmente un’ampia gamma di aggiornamenti dei contenuti per il tuo archivio direttamente dall’amministratore.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# Staging dei contenuti

{{ee-feature}}

La gestione temporanea dei contenuti offre al team aziendale la possibilità di creare, visualizzare in anteprima e pianificare facilmente un&#39;ampia gamma di aggiornamenti dei contenuti per il negozio direttamente dal _Amministratore_. Ad esempio, anziché considerare una pagina statica, considera una pagina come una raccolta di elementi diversi che è possibile trasformare _il_ o _disattivato_ in base a una pianificazione. Puoi utilizzare la gestione temporanea del contenuto per creare una pagina che cambia automaticamente nel corso dell’anno secondo una pianificazione.

Il termine _campagna_ fa riferimento al record di una modifica pianificata o a una raccolta di modifiche gestite dal dashboard di staging. Le modifiche possono essere visualizzate in un calendario o in una sequenza temporale. I termini _modifica pianificata_ e _aggiornamento pianificato_ sono intercambiabili e si riferiscono a una singola modifica.

Quando pianifichi una modifica del contenuto per un periodo di tempo specifico, alla scadenza della modifica pianificata il contenuto ritorna alla versione precedente. È possibile creare più versioni dello stesso contenuto della linea di base da utilizzare per aggiornamenti futuri. Puoi anche tornare indietro nella timeline per visualizzare le versioni precedenti del contenuto. Per salvare una bozza di versione, è sufficiente assegnare una data sulla timeline che sia così lontana nel futuro da non entrare mai in produzione.

## Oggetti e campagne di staging del contenuto

Quando viene creato un nuovo aggiornamento pianificato per uno dei seguenti oggetti, viene creata una campagna corrispondente come segnaposto e il _[!UICONTROL Scheduled Changes]_nella parte superiore della pagina. La campagna segnaposto ha una data di inizio, ma non una data di fine. Puoi pianificare gli aggiornamenti ai contenuti come parte di una campagna, quindi visualizzare in anteprima e condividere le modifiche per data, ora o visualizzazione archivio. Dopo aver creato una nuova campagna per un oggetto, puoi assegnarla come aggiornamento pianificato per altri oggetti.

- [Prodotti](../catalog/product-scheduled-changes.md)
- [Categorie](../catalog/category-scheduled-changes.md)
- [Regole prezzo catalogo](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [Regole prezzo carrello](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [Pagine CMS](pages-workspace.md#scheduled-changes)
- [Blocchi CMS](blocks.md)

## Flusso di lavoro di staging dei contenuti

1. **Creare il contenuto della baseline**

   La linea di base è il contenuto di una risorsa senza una campagna e include tutto ciò che si trova sotto _[!UICONTROL Scheduled Changes]_nella parte superiore della pagina. Il contenuto della linea di base viene sempre utilizzato, a meno che non sia presente una campagna attiva con le modifiche pianificate per tale posizione nella timeline.

1. **Creare la prima campagna**

   Crea la prima campagna con le date di inizio e fine necessarie. Per rendere la campagna aperta, lascia vuota la data di fine. Al termine della prima campagna, viene ripristinato il contenuto della linea di base originale.

   >[!NOTE]
   >
   >Le date di inizio e di fine della campagna devono essere definite utilizzando **_predefinito_** Fuso orario amministratore, convertito dal fuso orario locale di ciascun sito Web. Prendi in considerazione un esempio in cui hai più siti web in fusi orari diversi, ma desideri avviare una campagna basata su un fuso orario negli Stati Uniti. In questo caso, è necessario pianificare un aggiornamento separato per ogni fuso orario locale e impostare **[!UICONTROL Start Date]** e **[!UICONTROL End Date]** in convertito da ogni fuso orario del sito Web locale al fuso orario predefinito dell’amministratore.

1. **Aggiungi una seconda campagna**

   Crea la seconda campagna, con le date di inizio e fine necessarie. La seconda campagna può essere assegnata a un periodo di tempo completamente diverso. Quando crei più campagne per la stessa risorsa, le campagne non possono sovrapporsi. Puoi creare tutte le campagne necessarie.

   >[!NOTE]
   >
   >Tutti gli aggiornamenti pianificati vengono applicati consecutivamente, il che significa che qualsiasi entità può avere un solo aggiornamento pianificato alla volta. Qualsiasi aggiornamento pianificato viene applicato a tutte le visualizzazioni dello store entro il relativo intervallo di tempo. Di conseguenza, un’entità non può avere un aggiornamento pianificato diverso per diverse visualizzazioni dello store contemporaneamente. Tutti i valori degli attributi di entità all’interno di tutte le visualizzazioni archivio, che non sono influenzati dall’aggiornamento pianificato corrente, vengono presi dai valori predefiniti e non dal precedente aggiornamento pianificato.

1. **Ripristinare il contenuto della linea di base**

   Se tutte le campagne hanno date di fine, il contenuto previsto viene ripristinato ogni volta che tutte le campagne attive terminano.

>[!NOTE]
>
>Mentre per un’entità è attivo un aggiornamento dell’area di gestione temporanea, la modifica dell’entità sta modificando l’aggiornamento dell’area di gestione temporanea attivo corrente. Non influisce sul contenuto della linea di base, che viene ripristinato al termine dell’aggiornamento della gestione temporanea.

## [!UICONTROL Content Staging] dashboard

Il [!UICONTROL Content Staging] [dashboard](content-staging-dashboard.md) fornisce visibilità su tutte le modifiche e gli aggiornamenti pianificati per il sito. È possibile visualizzare in anteprima e condividere con altri qualsiasi giorno, intervallo di date o periodo di tempo di una campagna.

![Dashboard di staging](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## Demo di staging dei contenuti

Per informazioni sulla gestione temporanea dei contenuti, guarda questo video:

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12)

## Risorse per la risoluzione dei problemi

Per assistenza nella risoluzione dei problemi di staging dei contenuti, vedi quanto segue [!DNL Commerce] Articoli della Knowledge Base:

- [Errore 404 su tutte le pagine a causa di un problema di staging del contenuto](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [Gli aggiornamenti pianificati per la gestione temporanea dei contenuti non vengono visualizzati con la cache Fastly non aggiornata](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [Posso pianificare gli aggiornamenti di Gestione temporanea dei contenuti per i prezzi in un catalogo condiviso?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)
