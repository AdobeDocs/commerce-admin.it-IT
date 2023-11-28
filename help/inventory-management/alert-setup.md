---
title: Avvisi sui prodotti
description: Scopri gli avvisi sui prodotti e come utilizzarli per informare i clienti sullo stato delle scorte e sulle modifiche dei prezzi dei prodotti.
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# Avvisi sui prodotti

I clienti possono abbonarsi a due tipi di avvisi tramite e-mail: avvisi di modifica del prezzo e avvisi in-stock. Per ogni tipo di avviso, puoi determinare se i clienti sono in grado di iscriversi, selezionare il modello di e-mail utilizzato e identificare il mittente dell’e-mail.

![Registrati per ricevere un avviso sui prodotti](assets/product-alert-setting.png){width="600" zoomable="yes"}

## Avvisi sulla variazione di prezzo

Quando gli avvisi di modifica del prezzo sono attivati, _Avvisa quando il prezzo scende_ Il collegamento viene visualizzato in ogni pagina del prodotto. I clienti possono fare clic sul collegamento per iscriversi agli avvisi relativi al prodotto. Agli ospiti viene richiesto di aprire un account con il tuo negozio. Ogni volta che il prezzo cambia o il prodotto diventa speciale, tutti coloro che si sono iscritti all’avviso ricevono un avviso e-mail.

## Avvisi in-stock

L’avviso di magazzino crea un collegamento denominato _Avvisa quando il prodotto è disponibile_ per ogni prodotto esaurito. I clienti possono fare clic sul collegamento per iscriversi all’avviso. Quando il prodotto è di nuovo disponibile, i clienti ricevono una notifica via e-mail che indica che il prodotto è disponibile. I prodotti con avvisi hanno un _Avvisi sui prodotti_ nel pannello Informazioni prodotto, che elenca i clienti che si sono abbonati a un avviso.

![Elenco delle sottoscrizioni di prodotti e prezzi segnalati](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## Configurare gli avvisi sui prodotti

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Fai clic per espandere _[!UICONTROL Product Alerts]_ed effettuare le seguenti operazioni:

   ![Avvisi sui prodotti](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - Per inviare avvisi sui cambiamenti di prezzo ai clienti, impostare **[!UICONTROL Allow Alert When Product Price Changes]** a `Yes`.

   - Imposta **[!UICONTROL Price Alert Email Template]** al modello che si desidera utilizzare per le notifiche di avviso prezzi.

   - Per inviare avvisi quando i prodotti esauriti diventano nuovamente disponibili, imposta **[!UICONTROL Allow Alert When Product Comes Back in Stock]** a `Yes`.

     >[!NOTE]
     >
     >Il _Avvisa quando il prodotto è disponibile_ il messaggio viene visualizzato solo quando **[!UICONTROL Display Out of Stock Products]** è impostato su `Yes` (nella Configurazione all’indirizzo [!UICONTROL Catalog] > [!UICONTROL Inventory]).

   - Imposta **[!UICONTROL Stock Alert Email Template]** al modello che desideri utilizzare per gli avvisi sul stock di prodotto.

   - Imposta **[!UICONTROL Alert Email Sender]** al [contatto store](../getting-started/store-details.md#store-email-addresses){target="_blank"} that you want to appear as the sender of the email alert. Learn more about [store email addresses](../configuration-reference/general/store-email-addresses.md){target="_blank"} nella guida utente di base.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Configurare i modelli e-mail per gli avvisi sui prodotti

Quindi, configura, aggiungi o modifica il modello e-mail per l’avviso di prezzo. Puoi modificare le configurazioni dell’avviso di prezzo dopo aver creato modelli aggiuntivi.

Per informazioni più dettagliate sull’utilizzo dei messaggi e-mail, consulta [Modelli di messaggio](../systems/email-template-custom.md#message-templates) nel _Guida ai sistemi di amministrazione_.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Clic **[!UICONTROL Add New Template]**.

1. Sotto _Carica modello predefinito_, scegli il **[!UICONTROL Template]** che desideri personalizzare.

   È possibile scegliere il modello di avviso incluso nel tema. Oppure puoi selezionare `Price Alert` o `Stock Alert` modelli in _[!UICONTROL Magento_PriceAlert]_.

1. Clic **[!UICONTROL Load Template]**.

1. Immetti un **[!UICONTROL Template Name]**.

   È possibile selezionare questo nome nel _Avvisi prezzi_ configurazione.

1. Leggi il contenuto esistente e apporta le modifiche necessarie per:

   | Campo | Descrizione |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | Questo testo viene visualizzato nella riga dell’oggetto di un messaggio e-mail. |
   | [!UICONTROL Template Content] | Questo testo viene visualizzato nel contenuto completo dell’e-mail inviata. |

1. Per aggiungere le informazioni generate da [!DNL Commerce] dati, utilizza **[!UICONTROL Insert Variable]** per utilizzare un elenco di variabili disponibili.

1. Clic **[!UICONTROL Save Template]**.

## Impostazioni di esecuzione degli avvisi sui prodotti

Queste impostazioni consentono di selezionare la frequenza [!DNL Commerce] verifica la presenza di modifiche che richiedono l&#39;invio di avvisi. Puoi anche selezionare il destinatario, il mittente e il modello per le e-mail inviate se l’invio degli avvisi non riesce.

![Impostazioni di esecuzione degli avvisi sui prodotti](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Product Alerts Run Settings]** sezione.

1. Per determinare la frequenza con cui vengono inviati gli avvisi sui prodotti, imposta **[!UICONTROL Frequency]** a uno dei seguenti elementi:

   - `Daily`
   - `Weekly`
   - `Monthly`

1. Per determinare l’ora dell’invio degli avvisi sui prodotti, imposta **[!UICONTROL Start Time]** all&#39;ora, al minuto e al secondo.

   >[!NOTE]
   >
   >Gli avvisi sui prodotti vengono inviati dal consumatore &quot;product_alert&quot;.

1. Per **[!UICONTROL Error Email Recipient]**, inserisci l’e-mail della persona da contattare in caso di errore.

1. Per **[!UICONTROL Error Email Sender]**, selezionare l&#39;identità dell&#39;archivio visualizzata come mittente della notifica di errore.

1. Imposta **[!UICONTROL Error Email Template]** al modello e-mail transazionale da utilizzare per la notifica di errore.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
