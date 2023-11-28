---
title: Termini e condizioni per il pagamento
description: Scopri i termini e le condizioni configurabili per il tuo store.
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# Termini e condizioni per il pagamento

Quando manuale _Termini e condizioni_ se questa funzionalità è abilitata, i clienti devono accettare i termini e le condizioni della vendita prima che l’acquisto sia finalizzato. I Termini e Condizioni della vendita di solito includono informazioni di divulgazione che potrebbero essere richieste dalla legge per i siti B2C o B2B e delineano i diritti dell&#39;acquirente e del venditore. Il messaggio Termini e condizioni viene visualizzato dopo le informazioni sul pagamento, immediatamente prima del _Inserisci ordine_ pulsante.

![Termini e condizioni al pagamento](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## Passaggio 1: abilitare termini e condizioni per il pagamento

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Checkout Options]** sezione.

   ![Opzioni di pagamento](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. Verifica che **[!UICONTROL Enable Onepage Checkout]** è impostato su `Yes`.

1. Imposta **[!UICONTROL Enable Terms and Conditions]** a `Yes`.

1. Clic **[!UICONTROL Save Config]**.

## Passaggio 2: aggiungere le informazioni sui termini e le condizioni

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**.

   ![Griglia termini e condizioni](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add New Condition]**.

1. Inserisci il **[!UICONTROL Condition Name]** per riferimento interno.

   ![Nuova condizione](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Status]** a `Enabled`.

1. Imposta **[!UICONTROL Applied]** a uno dei seguenti elementi:

   - `Automatically` - Le condizioni vengono accettate automaticamente al momento del pagamento.
   - `Manually` - I clienti devono accettare manualmente le condizioni per effettuare un ordine.

1. Imposta **[!UICONTROL Show Content as]** a uno dei seguenti elementi:

   - `Text` - Visualizza i termini e le condizioni come testo non formattato.
   - `HTML` - Visualizza il contenuto come HTML che può essere formattato.

1. Seleziona ciascuno **[!UICONTROL Store View]** dove si desidera utilizzare questi Termini e Condizioni.

1. Scorri verso il basso e completa le informazioni da visualizzare:

   - Inserisci il **[!UICONTROL Checkbox Text]** da utilizzare come testo per il collegamento Termini e condizioni. Ad esempio, `I understand and accept the terms and conditions of the sale`.

   - In **[!UICONTROL Content]** inserisci il testo completo dei termini e delle condizioni della vendita.

1. (Facoltativo) Inserisci il **[!UICONTROL Content Height (css)]** in pixel per determinare l&#39;altezza della casella di testo in cui viene visualizzata l&#39;istruzione relativa ai termini e alle condizioni durante l&#39;estrazione.

   Ad esempio, per fare in modo che la casella di testo sia alta 1 pollice su uno schermo da 96 dpi, immettete `96`. Se il contenuto si estende oltre l&#39;altezza della casella, viene visualizzata una barra di scorrimento.

1. Clic **[!UICONTROL Save Condition]**.
