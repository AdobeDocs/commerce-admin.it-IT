---
title: Configura elenchi di desideri
description: Scopri come configurare la funzionalità della lista dei desideri per i clienti del tuo negozio.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Configura elenchi di desideri

La configurazione della lista dei desideri abilita le liste dei desideri e determina il modello di e-mail e il mittente dei messaggi e-mail utilizzati quando una lista dei desideri viene condivisa.

## Abilita funzionalità lista desideri

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Wish List]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL General Options]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - impostazioni generali della lista dei desideri](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - Attiva **[!UICONTROL Enabled]** su `Yes`, che attiva il modulo Elenco desideri per l&#39;archivio.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) attiva **[!UICONTROL Enable Multiple Wish Lists]** su `Yes`, che consente ai clienti di creare e gestire più elenchi di desideri.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Per limitare il numero di elenchi di desideri che i clienti possono avere associati al proprio account, immetti il valore per **[!UICONTROL Number of Multiple Wish Lists]**.

   - Attiva **[!UICONTROL Show in Sidebar]** su `Yes`, per visualizzare gli elenchi dei desideri nella barra laterale.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Share Options]** ed effettuare le seguenti operazioni:

   ![Configurazione clienti - opzioni di condivisione elenco dei desideri](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - Impostare **[!UICONTROL Email Sender]** sul contatto dell&#39;archivio che deve essere visualizzato come mittente del messaggio. Opzioni: Contatto Generale, Rappresentante Commerciale, Assistenza Clienti, E-Mail Personalizzata.

   - Imposta **[!UICONTROL Email Template]** da utilizzare quando un cliente condivide una lista dei desideri.

   - Per limitare il numero totale di e-mail che un cliente può inviare, immetti un valore **[!UICONTROL Max Emails Allowed to be Sent]**. Il valore predefinito è 10 e il massimo consentito è 10.000.

   - Per limitare la dimensione del messaggio, immettere il valore per **[!UICONTROL Email Text Length Limit]**. Il valore predefinito è 255.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) della sezione **[!UICONTROL My Wish List Link]** e impostare **[!UICONTROL Display Wish List Summary]** su uno dei seguenti elementi:

   - `Display number of items in wish list`
   - `Display item quantities`

   ![Configurazione clienti - visualizzazione elenco desideri](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Aggiungi ricerca lista dei desideri

![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce)

È possibile trovare qualsiasi elenco dei desideri pubblico utilizzando il widget di ricerca [elenco dei desideri](../content-design/widgets.md). Il widget consente a un cliente di effettuare ricerche in base al nome o all’indirizzo e-mail del proprietario della lista dei desideri. I clienti del negozio possono trovare elenchi di desideri che appartengono ad altri clienti, visualizzarli e ordinare prodotti da loro, o aggiungere i prodotti ai propri elenchi di desideri. Se un articolo viene acquistato da una lista dei desideri pubblica da un altro cliente, non viene rimosso dalla lista dei desideri originale. Il widget _Ricerca lista desideri_ può essere aggiunto a qualsiasi pagina del tuo store per facilitare ai clienti la ricerca delle liste dei desideri di amici e familiari.

![Esempio di vetrina - ricerca nella lista dei desideri](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add Widget]**.

1. Nella scheda _[!UICONTROL Settings]_eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Type]** su `Wish List Search`.

   - Imposta **[!UICONTROL Design Theme]** sul tema dell&#39;archivio in cui viene aggiunto l&#39;elenco dei desideri.

   - Fare clic su **[!UICONTROL Continue]**.

1. Completa _[!UICONTROL Storefront Properties]_:

   - Immettere **[!UICONTROL Widget Title]**.

   - Impostare **[!UICONTROL Assign to Store Views]** sulla visualizzazione o sul sito Web in cui verrà utilizzato il widget.

   - Per **[!UICONTROL Sort Order]**, immettere un numero per determinare la posizione del widget all&#39;interno del relativo contenitore.

     `0` = primo (predefinito), `1` = secondo, `2` = terzo e così via.

1. Nella sezione _[!UICONTROL Layout Updates]_, fare clic su **[!UICONTROL Add Layout Update]**e impostare **[!UICONTROL Display on]**su uno dei seguenti elementi:

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

1. Nell&#39;elenco **[!UICONTROL Container]** scegliere l&#39;area del layout di pagina in cui deve essere posizionato.

   ![Widget ricerca elenco desideri - layout](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. Nel pannello a sinistra, scegli **[!UICONTROL Widget Options]**.

1. Imposta **[!UICONTROL Quick Search Form Types]** su uno dei seguenti:

   - `All Forms` - I clienti possono eseguire ricerche in base a tutti i parametri disponibili.
   - `Owner Name` - I clienti possono cercare elenchi di desideri in base al nome del proprietario.
   - `Owner Email` - I clienti possono cercare le liste dei desideri in base all&#39;indirizzo e-mail del proprietario.

   >[!NOTE]
   >
   >Gli indirizzi di spedizione non sono inclusi nelle liste dei desideri.

1. Configura le proprietà widget rimanenti in base alle esigenze, seguendo le [istruzioni](../content-design/widget-create.md) standard.

1. Al termine, fare clic su **[!UICONTROL Save]**.

1. Quando richiesto, aggiorna tutte le cache non valide.
