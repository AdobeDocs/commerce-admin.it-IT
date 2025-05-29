---
title: Recensioni prodotto
description: Scopri in che modo le recensioni dei prodotti possono migliorare il tuo negozio e portare più credibilità ai tuoi prodotti.
exl-id: 82f96b24-626f-4b2d-be42-3d655d08dfda
feature: Merchandising, Products
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Recensioni prodotto

Le recensioni dei prodotti aiutano a creare un senso di comunità, e sono considerate più credibili di qualsiasi altro denaro pubblicitario possa comprare. Infatti, alcuni motori di ricerca danno ai siti con recensioni di prodotti una classificazione più alta rispetto a quelli senza. Per coloro che trovano il tuo sito cercando un prodotto specifico, una recensione del prodotto è essenzialmente la pagina di destinazione del tuo negozio. Le recensioni dei prodotti aiutano le persone a trovare il tuo negozio, tenerli coinvolti e spesso portare alle vendite.

Commerce include una funzionalità nativa di valutazione del prodotto che puoi gestire dall’amministratore. È inoltre possibile utilizzare un&#39;estensione di [Commerce Marketplace](../getting-started/commerce-marketplace.md) per utilizzare un sistema di gestione delle revisioni ospitato.

>[!NOTE]
>
>Le versioni da 2.4.0 a 2.4.3 di Adobe Commerce e Magento Open Source includevano l’estensione sviluppata dal fornitore Yotpo. A partire dalla versione 2.4.4, questa estensione non è più inclusa nella versione core e deve essere installata e aggiornata da Commerce Marketplace. Il Marketplace fornisce anche accesso alla documentazione corrente fornita dallo sviluppatore dell’estensione.
>><br><br>
>>Se l’estensione in bundle è abilitata e configurata, devi aggiornare il file compositore.json come parte del processo di aggiornamento 2.4.4 e gestire gli aggiornamenti delle estensioni in futuro. Per ulteriori informazioni, vedere [Moduli di aggiornamento](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) nella _Guida all&#39;aggiornamento_.

## Recensioni di prodotto sul vetrina

Quando la funzione nativa Revisioni prodotto è abilitata, i clienti possono scrivere recensioni per qualsiasi prodotto nel catalogo. Le recensioni possono essere scritte dalla pagina del prodotto facendo clic su:

- **Aggiungi la tua recensione** per i prodotti con recensioni esistenti.

- **Rivedi per primo questo prodotto** per i prodotti senza revisioni esistenti.

La scheda [!UICONTROL Reviews] elenca tutte le revisioni correnti e il modulo utilizzato per inviare una revisione.

La configurazione determina se i clienti devono aprire un account con il tuo negozio prima di scrivere le recensioni dei prodotti o se possono inviare le recensioni come ospiti. L’obbligo per i revisori di aprire un account impedisce la presentazione anonima e migliora la qualità delle recensioni.

![Esempio di vetrina - Aggiungi la tua recensione](./assets/storefront-review-this-product.png){width="700" zoomable="yes"}

Il numero di stelle indica il livello di soddisfazione del prodotto. I visitatori possono fare clic sul collegamento per leggere le recensioni e scriverne una propria. Come incentivo, i clienti possono ricevere punti premio per la presentazione di una revisione. Quando una revisione viene inviata, viene inviata all&#39;Amministratore per la moderazione. Una volta approvata, la recensione viene pubblicata nel tuo store.

![Vetrina di esempio - scheda Recensioni](./assets/storefront-reviews-tab.png){width="700" zoomable="yes"}

### [!UICONTROL My Product Reviews]

Nella sezione _[!UICONTROL My Product Reviews]_del dashboard account cliente sono elencate tutte le revisioni inviate dal cliente e approvate per la pubblicazione. Ogni riepilogo di revisione include la data di invio della revisione, i collegamenti alla pagina del prodotto e i dettagli della revisione.

![Recensioni dei miei prodotti](./assets/account-dashboard-my-product-reviews.png){width="700" zoomable="yes"}

1. Nella barra laterale del proprio account, il cliente sceglie **[!UICONTROL My Product Reviews]**.

1. Per visualizzare la revisione completa, fare clic su **[!UICONTROL See Details]**.

   ![Dettagli revisione](./assets/account-dashboard-my-product-reviews-details.png){width="700" zoomable="yes"}

## Abilitare le funzioni di revisione del prodotto

La funzione Revisioni prodotto di Commerce è attivata per impostazione predefinita.

>[!NOTE]
>
>Per impostare questi campi su `No` e disabilitare le recensioni di prodotti Commerce, è necessario deselezionare le caselle di controllo **Usa valore di sistema**.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e seleziona **[!UICONTROL Catalog]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Product Reviews]**.

   ![Configurazione del catalogo - Recensioni prodotti Commerce](../configuration-reference/catalog/assets/catalog-product-reviews.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enabled]** su `Yes`.

   Questa è l’impostazione predefinita che abilita le revisioni dei prodotti.

1. Imposta **[!UICONTROL Allow Guests to Write Reviews]** su `Yes`.

   Questa è l’impostazione predefinita che determina se i clienti devono aprire un account con il tuo negozio per poter scrivere recensioni di prodotti.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

## Creare valutazioni personalizzate

Con le Revisioni dei prodotti Commerce, i clienti possono assegnare valutazioni quando inviano una revisione del prodotto. Le valutazioni predefinite sono qualità, prezzo e valore. Oltre a questi, puoi aggiungere le tue valutazioni personalizzate. Le valutazioni a cinque stelle visualizzate nelle pagine del catalogo vengono calcolate in media per ogni prodotto.

![Esempio di vetrina - valutazioni personalizzate](./assets/attribute-custom-ratings-review.png){width="700" zoomable="yes"}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Rating]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add New Rating]**.

   ![Amministratore - Valutazioni](./assets/product-reviews-rating.png){width="700" zoomable="yes"}

1. Nella sezione _[!UICONTROL Rating Title]_, immetti **[!UICONTROL Default Value]**per la nuova valutazione.

   Se applicabile, inserisci anche la traduzione per ogni visualizzazione store.

   ![Impostazioni titolo valutazione](./assets/product-rating-title.png){width="600" zoomable="yes"}

1. Nella sezione _Visibilità valutazione_, impostare **[!UICONTROL Visibility In]** sulla visualizzazione dello store in cui deve essere utilizzata la valutazione.

   Per selezionare più visualizzazioni dello store, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ogni elemento.

   >[!NOTE]
   >
   >Le valutazioni non sono visibili a meno che non siano assegnate a una visualizzazione archivio.

1. Per **[!UICONTROL Sort Order]**, immettere un numero per determinare l&#39;ordine di questa valutazione quando elencato con altri.

1. Se si desidera visualizzare la propria valutazione nella vetrina, selezionare la casella di controllo **[!UICONTROL Is Active]**.

   ![Impostazioni visibilità valutazione](./assets/product-rating-visibility.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Rating]**.

   La valutazione media per tutte le recensioni viene visualizzata per ogni prodotto nella pagina della griglia del catalogo dei prodotti.

   ![Pagina catalogo](./assets/catalog-rating-page.png){width="700" zoomable="yes"}
