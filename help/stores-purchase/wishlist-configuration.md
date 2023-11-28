---
title: Configura elenchi di desideri
description: Scopri come configurare la funzionalità della lista dei desideri per i clienti del tuo negozio.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Configura elenchi di desideri

La configurazione della lista dei desideri abilita le liste dei desideri e determina il modello di e-mail e il mittente dei messaggi e-mail utilizzati quando una lista dei desideri viene condivisa.

## Abilita funzionalità lista desideri

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Wish List]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL General Options]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - Impostazioni generali elenco desideri](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - Attiva/Disattiva **[!UICONTROL Enabled]** a `Yes`, che attiva il modulo della lista dei desideri per il negozio.

   - ![Adobe Commerce](../assets/adobe-logo.svg) Attiva/disattiva (solo Adobe Commerce) **[!UICONTROL Enable Multiple Wish Lists]** a `Yes`, che consente ai clienti di creare e gestire più elenchi di desideri.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Solo per Adobe Commerce) Per limitare il numero di elenchi di desideri che i clienti possono avere associati al proprio account, immetti un valore per **[!UICONTROL Number of Multiple Wish Lists]**.

   - Attiva/Disattiva **[!UICONTROL Show in Sidebar]** a `Yes`, che visualizza gli elenchi dei desideri nella barra laterale.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Share Options]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti: opzioni di condivisione della lista dei desideri](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - Imposta il **[!UICONTROL Email Sender]** al contatto del punto vendita che deve apparire come mittente del messaggio. Opzioni: Contatto Generale, Rappresentante Commerciale, Assistenza Clienti, E-Mail Personalizzata.

   - Imposta il **[!UICONTROL Email Template]** da utilizzare quando un cliente condivide una lista dei desideri.

   - Per limitare il numero totale di e-mail che un cliente può inviare, inserisci un **[!UICONTROL Max Emails Allowed to be Sent]** valore. Il valore predefinito è 10 e il massimo consentito è 10.000.

   - Per limitare la dimensione del messaggio, immetti un valore per **[!UICONTROL Email Text Length Limit]**. Il valore predefinito è 255.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL My Wish List Link]** sezione e set **[!UICONTROL Display Wish List Summary]** a uno dei seguenti elementi:

   - `Display number of items in wish list`
   - `Display item quantities`

   ![Configurazione clienti - Visualizzazione elenco desideri](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Aggiungi ricerca lista dei desideri

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

Qualsiasi lista dei desideri pubblica può essere trovata utilizzando la Ricerca lista dei desideri [widget](../content-design/widgets.md). Il widget consente a un cliente di effettuare ricerche in base al nome o all’indirizzo e-mail del proprietario della lista dei desideri. I clienti del negozio possono trovare elenchi di desideri che appartengono ad altri clienti, visualizzarli e ordinare prodotti da loro, o aggiungere i prodotti ai propri elenchi di desideri. Se un articolo viene acquistato da una lista dei desideri pubblica da un altro cliente, non viene rimosso dalla lista dei desideri originale. Il _Ricerca elenco desideri_ Il widget può essere aggiunto a qualsiasi pagina del tuo negozio per rendere facile per i clienti di trovare le liste dei desideri di amici e familiari.

![Esempio di vetrina: ricerca nella lista dei desideri](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Widget]**.

1. In _[!UICONTROL Settings]_, eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Type]** a `Wish List Search`.

   - Imposta **[!UICONTROL Design Theme]** al tema del negozio in cui viene aggiunta la lista dei desideri.

   - Clic **[!UICONTROL Continue]**.

1. Completa il _[!UICONTROL Storefront Properties]_:

   - Inserisci il **[!UICONTROL Widget Title]**.

   - Imposta **[!UICONTROL Assign to Store Views]** alla visualizzazione o al sito Web in cui deve essere utilizzato il widget.

   - Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la posizione del widget all&#39;interno del relativo contenitore.

     `0` = first (valore predefinito), `1` = secondo, `2` = terzo e così via.

1. In _[!UICONTROL Layout Updates]_, fare clic su **[!UICONTROL Add Layout Update]**e imposta **[!UICONTROL Display on]**a uno dei seguenti elementi:

   - _[!UICONTROL Categories]_

      - `Anchor Categories`
      - `Non-Anchor Categories`

   - _[!UICONTROL Products]_

      - `All Product Type`
      - `Simple Product`
      - `Virtual Product`
      - `Bundle Product`
      - `Configurable Product`
      - `Downloadable Product`
      - `Gift Card`
      - `Grouped Product`

   - _[!UICONTROL Generic Page]_

      - `All Pages`
      - `Specified Page`
      - `Page Layouts`

1. In **[!UICONTROL Container]** , scegliere l&#39;area del layout di pagina in cui deve essere posizionato.

   ![Widget ricerca elenco desideri - layout](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. Nel pannello a sinistra, scegli **[!UICONTROL Widget Options]**.

1. Imposta **[!UICONTROL Quick Search Form Types]** a uno dei seguenti elementi:

   - `All Forms` - I clienti possono effettuare ricerche in base a tutti i parametri disponibili.
   - `Owner Name` - I clienti possono cercare le liste dei desideri in base al nome del proprietario.
   - `Owner Email` - I clienti possono cercare le liste dei desideri in base all&#39;indirizzo e-mail del proprietario.

   >[!NOTE]
   >
   >Gli indirizzi di spedizione non sono inclusi nelle liste dei desideri.

1. Configura le proprietà widget rimanenti secondo necessità, seguendo lo standard [istruzioni](../content-design/widget-create.md).

1. Al termine, fai clic su **[!UICONTROL Save]**.

1. Quando richiesto, aggiorna tutte le cache non valide.
