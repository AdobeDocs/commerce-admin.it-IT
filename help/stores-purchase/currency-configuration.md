---
title: Configurazione della valuta
description: Scopri come impostare l’ambito della valuta di base e come specificare le valute accettate e la valuta da utilizzare per la visualizzazione del prezzo.
exl-id: ba78095f-36eb-4e38-a6e8-72d85e0cf980
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Configurazione della valuta

Prima di impostare i singoli tassi di valuta, è necessario impostare l&#39;ambito del [valuta di base](../configuration-reference/general/currency-setup.md). È impostata su globale per impostazione predefinita, che applica l&#39;impostazione della valuta di base all&#39;intero [gerarchia store](../getting-started/websites-stores-views.md). Se si dispone di un&#39;installazione Adobe Commerce multisito o di Magento Open Source, è possibile gestire più valute di base impostando l&#39;ambito a livello di sito Web.

È inoltre possibile specificare le valute accettate e la valuta da utilizzare per la visualizzazione [prezzi](../catalog/catalog-price-scope.md) nel tuo negozio. Nel diagramma seguente, l&#39;ambito della valuta di base viene impostato a livello di sito Web, in modo che ogni sito Web possa avere una valuta di base diversa.

![Diagramma ambito valuta](./assets/scope-currency-config.svg){width="600" zoomable="yes"}

## Passaggio 1: scegliere le divise accettate

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nell&#39;angolo in alto a sinistra, imposta **[!UICONTROL Scope]** alla vista store in cui si applica la configurazione.

1. Nel pannello a sinistra sotto _Generale_, scegli **[!UICONTROL Currency Setup]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Currency Options]** e impostare le seguenti opzioni:

   - **[!UICONTROL Base Currency]** — Imposta sulla valuta principale utilizzata per le transazioni in linea.

   - **[!UICONTROL Default Display Currency]** — Imposta sulla valuta utilizzata per visualizzare i prezzi nella visualizzazione punto vendita.

   - **[!UICONTROL Allowed Currencies]** — Selezionare tutte le valute accettate come pagamento nella visualizzazione punto vendita. Assicurati anche di selezionare la valuta principale.

     Per più valute, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   ![Configurazione generale - Opzioni di valuta](../configuration-reference/general/assets/currency-setup-currency-options.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedi [Opzioni valuta](../configuration-reference/general/currency-setup.md) nel _Guida di riferimento alla configurazione_.

1. Quando viene richiesto di aggiornare la cache, fare clic su _Chiudi_ ( ![Chiudi casella](../assets/icon-close-x.png) ) nell&#39;angolo superiore destro del messaggio di sistema.

   È possibile [aggiorna la cache](../systems/cache-management.md) più tardi.

1. Definire l&#39;ambito della valuta di base:

   - Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

   - Scorri verso il basso ed espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Price]** sezione. Questa sezione viene visualizzata solo se l&#39;ambito è impostato come **[!UICONTROL Store View:]** _Configurazione predefinita_.)

   - Imposta **[!UICONTROL Catalog Price Scope]** a `Global` o `Website`.

   ![Configurazione del catalogo - Opzioni di prezzo](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

## Passaggio 2: configurare la connessione di importazione

1. Scorri fino alla parte superiore della pagina.

1. Nel pannello a sinistra, espandi **[!UICONTROL General]** e scegli **[!UICONTROL Currency Setup]**.

1. Configurare la connessione al servizio valuta:

   Sono disponibili tre opzioni di assistenza: _[!UICONTROL Fixer.io (legacy)]_,_[!UICONTROL Fixer Api (APILayer)]_, e _[!UICONTROL Currency Converter API]_

   >[!IMPORTANT]
   >
   >A partire dalla versione 2.4.6 di, le [[!DNL Fixer.io]](https://fixer.io/) il servizio è obsoleto e sostituito con il [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) servizio. Si consiglia vivamente di utilizzare un account APILayer invece di un account obsoleto [!DNL Fixer.io] account.

   - _Per connettersi al [servizio fixer.io](https://fixer.io/):_

      - Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Fixer.io]** sezione.

      - Inserisci il file fixer.io **[!UICONTROL API key]**.

      - Per **[!UICONTROL Connection Timeout in Seconds]**, inserisci il numero di secondi di inattività consentiti prima che la connessione si interrompa.

     ![Configurazione generale - Impostazione valuta - Opzioni Fixer.io](../configuration-reference/general/assets/currency-setup-fixer.png){width="600" zoomable="yes"}

   - _Per connettersi al [[!DNL Fixer Api (APILayer)] servizio](https://apilayer.com/):_

      - Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Fixer Api (APILayer)]** sezione.

      - Immetti il [!DNL APILayer] **[!UICONTROL API key]**.

      - Per **[!UICONTROL Connection Timeout in Seconds]**, inserisci il numero di secondi di inattività consentiti prima che la connessione si interrompa.

     ![Configurazione generale - Impostazione valuta - Opzioni API Fixer (APILayer)](../configuration-reference/general/assets/currency-setup-fixer-api.png){width="600" zoomable="yes"}

   - _Per connettersi al [[!DNL Currency Convertor API] servizio](https://free.currencyconverterapi.com/):_

      - Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Currency Convertor API]** sezione.

      - Inserire il convertitore di valuta **[!UICONTROL API key]**.

      - Per **[!UICONTROL Connection Timeout in Seconds]**, inserisci il numero di secondi di inattività consentiti prima che la connessione si interrompa.

     ![Configurazione generale - Impostazione valuta - Opzioni API di Convertitore valuta](../configuration-reference/general/assets/currency-setup-converter.png){width="600" zoomable="yes"}

## Passaggio 3: configurare le impostazioni di importazione pianificate

1. Continuando con l&#39;impostazione della valuta, espandere ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Scheduled Import Settings]** sezione.

   ![Configurazione generale - impostazioni importazione pianificata valuta](../configuration-reference/general/assets/currency-setup-scheduled-import-settings.png){width="600" zoomable="yes"}

1. Per aggiornare automaticamente i tassi di cambio, impostare **[!UICONTROL Enabled]** a `Yes`.

1. Impostare le opzioni di aggiornamento:

   - **[!UICONTROL Service]** — Imposta sul provider di tariffe. Il valore predefinito è `Fixer.io (legacy)`.

   - **[!UICONTROL Start Time]** — Impostare su ora, minuto e secondo l&#39;aggiornamento delle tariffe in base alla pianificazione.

   - **[!UICONTROL Frequency]** — Per determinare la frequenza con cui vengono aggiornati i tassi, impostare una delle seguenti opzioni:

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]** — Immettere l&#39;indirizzo di posta elettronica della persona che deve ricevere la notifica e-mail se si verifica un errore durante il processo di importazione.

     Per immettere più indirizzi e-mail, separali con una virgola.

   - **[!UICONTROL Error Email Sender]** — Imposta su [contatto store](../getting-started/store-details.md#store-email-addresses) che viene visualizzato come mittente della notifica di errore.

   - **[!UICONTROL Error Email Template]** — Imposta sul modello di e-mail utilizzato per la notifica di errore.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando viene richiesto di aggiornare la cache, fare clic su **[!UICONTROL Cache Management]** collega e aggiorna la cache non valida.

   ![Messaggio di sistema - aggiorna la cache non valida](./assets/msg-cache-management.png){width="600" zoomable="yes"}

## Passaggio 4: aggiornare i tassi di valuta

I tassi di cambio devono essere aggiornati con i valori correnti prima che diventino effettivi. [Aggiornare le tariffe](currency-update.md) manualmente o per importare automaticamente le tariffe.

## Passaggio 5: personalizzare i simboli di valuta (facoltativo)

La gestione dei simboli di valuta consente di personalizzare il simbolo associato a ciascuna valuta accettata come pagamento nel Negozio.

![Simboli di valuta](./assets/stores-currency-symbols.png){width="600" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Symbols]**.

   Ogni valuta abilitata per il tuo archivio viene visualizzata nel _[!UICONTROL Currency]_elenco.

1. Modificare le impostazioni nell&#39;elenco in base alle esigenze:

   - Immettere un simbolo personalizzato per ogni valuta che si desidera utilizzare oppure selezionare **[!UICONTROL Use Standard]** casella di controllo per ciascuna valuta.

   - Per ignorare il simbolo di default, deselezionate _[!UICONTROL Use Standard]_e immettere il simbolo che si desidera utilizzare.

   >[!NOTE]
   >
   >Non è possibile modificare l&#39;allineamento del simbolo di valuta da sinistra a destra.

1. Al termine, fai clic su **[!UICONTROL Save Currency Symbols]**.

1. Quando viene richiesto di aggiornare la cache, fare clic su **[!UICONTROL Cache Management]** collega e aggiorna eventuali cache non valide.
