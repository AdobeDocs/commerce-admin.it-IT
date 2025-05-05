---
title: Riscritture URL prodotto
description: Scopri come utilizzare le riscritture dell’URL del prodotto per reindirizzare i collegamenti all’URL di un altro prodotto nel tuo store di Commerce.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# Riscritture URL prodotto

Prima di iniziare, assicurati di comprendere esattamente cosa deve essere realizzato dal reindirizzamento. Pensa in termini di _destinazione_ / _richiesta originale_ o _reindirizzamento a_ / _reindirizzamento da_. Anche se le persone possono ancora passare alla pagina precedente da motori di ricerca o collegamenti obsoleti, il reindirizzamento fa sì che il tuo negozio passi alla nuova destinazione.

Se per l&#39;archivio sono abilitati [reindirizzamenti automatici](url-redirect-product-automatic.md), non è necessario creare una riscrittura quando viene modificato un codice Product Key[URL](../catalog/catalog-urls.md).

{{url-rewrite-skip}}

## Passaggio 1: Pianificare la riscrittura

Per evitare errori, prendere nota del percorso _reindirizza a_ e del percorso _reindirizza da_ e includere la chiave e il suffisso dell&#39;URL (se applicabile).

Se non sei sicuro, apri ogni pagina di prodotto nel tuo store e copia il percorso dalla barra degli indirizzi del browser. Durante la creazione di un reindirizzamento di prodotto, puoi includere o escludere il [percorso categoria](../catalog/catalog-urls.md). Per questo esempio, creiamo un reindirizzamento di prodotto senza un percorso di categoria.

### Prodotto con percorso categoria

Reindirizza a: `gear/bags/impulse-duffle.html`

Reindirizzamento da: `gear/bags/overnight-duffle.html`

### Prodotto senza percorso categoria

Reindirizza a: `impulse-duffle.html`

Reindirizzamento da: `overnight-duffle.html`

## Passaggio 2: Creare la riscrittura

{{url-rewrite-params}}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Prima di procedere, eseguire le operazioni seguenti per verificare che il percorso della richiesta sia disponibile.

   - Nel filtro di ricerca nella parte superiore della colonna **[!UICONTROL Request Path]**, immettere la chiave URL della pagina da reindirizzare e fare clic su **[!UICONTROL Search]**.

   - Se esistono più record di reindirizzamento per la pagina, individua quello che corrisponde alla visualizzazione store applicabile e aprilo in modalità di modifica.

   - Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Delete]**. Quando richiesto, fare clic su **[!UICONTROL OK]** per confermare.

1. Nell&#39;angolo superiore destro della pagina URL riscritture fare clic su **Aggiungi URL riscrittura**.

1. Imposta **[!UICONTROL Create URL Rewrite]** su `For product`.

1. Nella griglia, individua il prodotto che è la destinazione (destinazione) del reindirizzamento e fai clic sulla riga.

   ![Riscritture URL - prodotto](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. Sotto l&#39;albero delle categorie fare clic su **[!UICONTROL Skip Category Selection]**.

   In questo esempio, il reindirizzamento non include una categoria.

   ![Riscrittura URL prodotto - ignora selezione categoria](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   Nella pagina Aggiungi riscrittura URL per un prodotto, nell’angolo in alto a sinistra, viene visualizzato un collegamento alla destinazione e nel campo Percorso di destinazione viene visualizzata la versione di sistema del percorso, che non può essere modificata. Inizialmente, nel campo Percorso di reindirizzamento viene visualizzato anche il percorso di destinazione.

   - Se sono presenti più visualizzazioni dello store, impostare **[!UICONTROL Store]** sulla visualizzazione in cui si applica la riscrittura. In caso contrario, viene creata una riscrittura per ogni vista.

   - Per **[!UICONTROL Request Path]**, sostituisci il valore predefinito immettendo la chiave URL e il suffisso (se applicabile) della richiesta di prodotto originale. Si tratta del prodotto _reindirizzamento da_ identificato nel passaggio di pianificazione.

     >[!NOTE]
     >
     >Il percorso della richiesta deve essere univoco per l’archivio specificato. Se esiste già un reindirizzamento che utilizza lo stesso percorso di richiesta, quando tenti di salvare il reindirizzamento riceverai un errore. Prima di poterne creare uno, devi eliminare il reindirizzamento precedente.

   - Imposta **[!UICONTROL Redirect Type]** su uno dei seguenti:

      - `Temporary (302)`
      - `Permanent (301)`

   - Per riferimento personale, immettere un breve **[!UICONTROL Description]** della riscrittura.

   ![Riscrittura URL prodotto - informazioni](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. Prima di salvare il reindirizzamento, verifica quanto segue:

   - Il collegamento in alto a sinistra mostra il nome del prodotto di destinazione.
   - Il percorso della richiesta contiene il percorso per il reindirizzamento _originale dal prodotto_.

1. Al termine, fare clic su **[!UICONTROL Save]**.

   La nuova riscrittura del prodotto viene ora visualizzata nella parte superiore della griglia URL riscritture.

## Passaggio 3: Verifica il risultato

1. Vai alla pagina principale del tuo negozio.

1. Effettuare una delle seguenti operazioni:

   - Passa alla pagina di richiesta del prodotto _reindirizzamento originale da_.
   - Nella barra degli indirizzi del browser, immetti il percorso del _reindirizzamento originale dal_ prodotto subito dopo l&#39;URL dell&#39;archivio e premi **Invio**.

   Viene visualizzato il nuovo prodotto di destinazione invece della richiesta di prodotto originale.

## Descrizioni dei campi

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indica il tipo di riscrittura. Impossibile modificare il tipo dopo la creazione della riscrittura. Opzioni: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Prodotto da reindirizzare. A seconda della configurazione, il percorso della richiesta potrebbe includere il suffisso `.html` o `.htm` e la categoria. Il percorso della richiesta deve essere univoco e non può essere utilizzato da un altro reindirizzamento. Se ricevi un errore che indica che il percorso della richiesta esiste, elimina il reindirizzamento esistente e riprova. |
| [!UICONTROL Target Path] | Percorso interno utilizzato dal sistema per puntare alla destinazione del reindirizzamento. Il percorso di destinazione è disattivato e non può essere modificato. |
| [!UICONTROL Redirect] | Determina il tipo di reindirizzamento. Opzioni: <br/>**[!UICONTROL No]**- Nessun reindirizzamento specificato. Molte operazioni creano richieste di reindirizzamento di questo tipo. Ad esempio, ogni volta che si aggiungono prodotti a una categoria, viene creato un reindirizzamento del tipo `No` per ogni visualizzazione store.<br/>**[!UICONTROL Temporary (302)]** - Indica ai motori di ricerca che la riscrittura ha una durata limitata. I motori di ricerca generalmente non conservano le informazioni sul rango delle pagine per le riscritture temporanee. <br/>**[!UICONTROL Permanent (301)]**- Indica ai motori di ricerca che la riscrittura è permanente. I motori di ricerca in genere conservano le informazioni sulla classificazione delle pagine per le riscritture permanenti. |
| [!UICONTROL Description] | Descrive lo scopo della riscrittura per riferimento interno. |

{style="table-layout:auto"}

## Riscritture di più URL

Puoi aggiornare rapidamente e contemporaneamente le riscritture URL per più o tutti i prodotti, seguendo la procedura riportata di seguito.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Seleziona tutti i prodotti per i quali desideri aggiornare le riscritture URL.

1. In _[!UICONTROL Actions]_, scegliere **[!UICONTROL Update attributes]**&#x200B;per aggiornare più o tutte le riscritture.

1. In _[!UICONTROL PRODUCTS INFORMATION]_, fare clic sulla scheda **[!UICONTROL Websites]**.

1. Nella sezione _[!UICONTROL Add Product To Websites]_&#x200B;selezionare tutti i siti Web per i quali si desidera ripristinare le riscritture URL.

1. Al termine dell&#39;aggiornamento, fare clic su **[!UICONTROL Save]**.

>[!NOTE]
>
>Tutti i prodotti selezionati vengono letti sui siti web selezionati e le riscritture URL vengono rigenerate.

![Aggiorna attributi - aggiorna più riscritture URL](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
