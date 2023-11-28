---
title: '[!DNL Google Content Experiments]'
description: Scopri come utilizzare [!DNL Google Content Experiments] per impostare un test A/B di prodotti, categorie o pagine di contenuti Commerce.
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

L’esempio seguente mostra come impostare un test A/B di prodotti, categorie o pagine di contenuto utilizzando Esperimenti di contenuto Google Analytics. Ti consigliamo di tenere aperte due schede del browser mentre segui le istruzioni, perché devi effettuare un salto avanti e indietro tra l’amministratore di Commerce e il tuo [!DNL Google Analytics] account.

>[!NOTE]
>
>[!DNL Google Content Experiments] è stato dichiarato obsoleto e deve essere sostituito da [Google Optimize](https://support.google.com/optimize/answer/7084762?hl=en).

## Passaggio 1: Abilita esperimenti di contenuto (Commerce)

1. Accedi all’amministratore dell’installazione di Commerce.

1. Segui le istruzioni per abilitare [Google Analytics](google-analytics.md) con Content Experiments nella configurazione Commerce.

   ![Configurazione delle vendite - API Google - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## Passaggio 2: Impostare le varianti (Commerce)

Crea più varianti dello stesso prodotto, categoria o pagina.

- Ogni variante deve avere un [Chiave URL](../catalog/catalog-urls.md).
- Ogni variante deve avere lo stesso [visualizzazione store](../getting-started/websites-stores-views.md#scope-settings) selezionato.

Puoi creare fino a dieci varianti di ogni entità da testare. Per i prodotti, utilizzare [Salva e duplica](../catalog/product-workspace.md) per risparmiare tempo.

## Passaggio 3: Configurare l’esperimento (Google)

>[!NOTE]
>
>Per creare un esperimento devi disporre delle autorizzazioni appropriate per l’account Google.

1. Apri un’altra scheda del browser e accedi al tuo [Google Analytics][2] account.

   Se necessario, passare al **[!UICONTROL Account]** e **[!UICONTROL Property]**.

1. Nella barra laterale a sinistra, scegli **[!UICONTROL Admin]** e utilizza uno dei seguenti metodi:

   **Metodo 1:** Scegli una vista esistente

   Nell’intestazione della sezione _[!UICONTROL View]_, fare clic sulla freccia rivolta verso il basso e scegliere la vista che deve fornire i dati per l&#39;esperimento.

   **Metodo 2:** Creare una nuova visualizzazione di reporting

   - Nell’intestazione della sezione _Visualizza_ , fare clic su **[!UICONTROL Create View]** ed effettuare le seguenti operazioni:

      - Identifica la posizione dell’esperimento come `Website` o `Mobile app`.

      - Inserisci un valore descrittivo **[!UICONTROL Reporting View Name]**.

      - Specifica la **[!UICONTROL Reporting Time Zone]**.

   - Al termine, fai clic su **[!UICONTROL Create View]** e quindi fare clic sulla freccia indietro per tornare alla pagina precedente.

1. Nel pannello a sinistra sotto _[!UICONTROL Reports]_, scegli **[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**.

1. Clic **[!UICONTROL Create experiment]** ed effettuare le seguenti operazioni:

   - Specifica la percentuale di traffico da reindirizzare.

   - Specifica la **[!UICONTROL Original Page URL]** e gli URL di ciascuno **[!UICONTROL page variation]** che vuoi testare.

   - Completa le altre opzioni.

1. Una volta configurato l’esperimento, fai clic su **[!UICONTROL Manually Insert the Code]** e copia il frammento di codice.

## Passaggio 4: Incolla frammento di codice (Commerce)

1. Torna all’amministratore dell’installazione di Commerce e apri la versione originale del prodotto, della categoria o della pagina in modalità di modifica.

1. Espandi **[!UICONTROL View Optimization]** per il prodotto, la categoria o la pagina.

1. Incolla lo snippet di codice copiato dalle Google Analytics in **[!UICONTROL Experiment Code]** casella di testo.

   >[!NOTE]
   >
   >Non incollare il frammento di codice in nessuna delle varianti.

   ![Ottimizzazione della visualizzazione prodotto](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save]**.

## Passaggio 5: rivedere e avviare l’esperimento (Google)

1. Torna al tuo [Google Analytics][2] account.

1. Controlla le impostazioni dell’esperimento.

1. Per iniziare, fai clic su **[!UICONTROL Start Experiment]**.

   In caso contrario, fare clic su **[!UICONTROL Save for Later]**.


[2]: https://analytics.google.com/
