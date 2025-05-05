---
title: L’URL della categoria viene riscritto
description: Scopri come utilizzare la riscrittura dell’URL della categoria per reindirizzare i collegamenti all’URL di un’altra categoria nel tuo store di Commerce.
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# L’URL della categoria viene riscritto

Se una categoria viene rimossa dal catalogo, puoi riscriverla per reindirizzare i collegamenti all’URL di un’altra categoria nel tuo store. Pensa in termini di _destinazione_ / _richiesta originale_ o _reindirizzamento a_ / _reindirizzamento da_. Anche se le persone possono ancora passare alla pagina precedente da motori di ricerca o collegamenti obsoleti, il reindirizzamento fa sì che il tuo negozio passi alla nuova destinazione.

Se per l&#39;archivio sono abilitati [reindirizzamenti automatici](url-redirect-product-automatic.md), non è necessario creare una riscrittura quando viene modificata una chiave [URL](../catalog/catalog-urls.md) della categoria.

{{url-rewrite-skip}}

## Passaggio 1: Pianificare la riscrittura

Per evitare errori, prendere nota del percorso _reindirizza a_ e del percorso _reindirizza da_ e includere la chiave e il suffisso dell&#39;URL (se applicabile).

Se non sei sicuro, apri ogni pagina di categoria nel tuo store e copia il percorso dalla barra degli indirizzi del browser.

**Esempio:**

Reindirizza a: `gear/backpacks-and-bags.html`

Reindirizzamento da: `gear/bags.html`

## Passaggio 2: Creare la riscrittura

{{url-rewrite-params}}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Prima di procedere, eseguire le operazioni seguenti per verificare che il percorso della richiesta sia disponibile:

   - Nel filtro di ricerca nella parte superiore della colonna **[!UICONTROL Request Path]**, immettere la chiave URL della categoria da reindirizzare e fare clic su **[!UICONTROL Search]**.

   - Se esistono più record di reindirizzamento per la pagina, individua quello che corrisponde alla visualizzazione store applicabile e apri il record di reindirizzamento in modalità di modifica.

   - Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Delete]**. Quando richiesto, fare clic su **[!UICONTROL OK]** per confermare.

1. Quando si torna alla pagina _[!UICONTROL URL Rewrites]_, fare clic su **[!UICONTROL Add URL Rewrite]**.

1. Impostare **[!UICONTROL Create URL Rewrite]** su `For category` e scegliere la categoria di destinazione nell&#39;albero di destinazione del reindirizzamento.

   ![Riscrittura URL - scegli categoria](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. Nella sezione _URL Rewrite_ eseguire le operazioni seguenti:

   - Se sono presenti più archivi, selezionare **[!UICONTROL Store]** in cui applicare la riscrittura.

   - Per **[!UICONTROL Request Path]**, immettere la chiave URL della categoria richiesta dal cliente. Categoria _reindirizzamento da_.

     >[!NOTE]
     >
     >Il percorso della richiesta deve essere univoco per l’archivio specificato. Se esiste già un reindirizzamento che utilizza lo stesso percorso di richiesta, quando tenti di salvare il reindirizzamento riceverai un errore. Prima di poterne creare uno, devi eliminare il reindirizzamento precedente.

   - Imposta **[!UICONTROL Redirect]** su uno dei seguenti:

      - `Temporary (302)`
      - `Permanent (301)`

   - Per il riferimento, immettere una breve descrizione della riscrittura.

   ![Aggiungi riscrittura URL per categoria](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. Prima di salvare il reindirizzamento, verifica quanto segue:

   - Il collegamento nell’angolo in alto a sinistra mostra il nome della categoria di destinazione.
   - Il percorso della richiesta contiene il percorso per il reindirizzamento _originale dalla categoria_.

1. Al termine, fare clic sul pulsante **[!UICONTROL Save]**.

   La nuova categoria riscrittura viene visualizzata nella parte superiore della griglia URL riscritture.

## Passaggio 3: Verifica il risultato

1. Vai alla pagina principale del tuo negozio.

1. Effettuare una delle seguenti operazioni:

   - Passa alla categoria _reindirizzamento originale da_.
   - Nella barra degli indirizzi del browser, immetti il percorso della categoria _reindirizzamento originale da_ subito dopo l&#39;URL dell&#39;archivio e premi **[!UICONTROL Enter]**.

   Viene visualizzata la nuova categoria di destinazione invece della richiesta della categoria originale.

## Descrizioni dei campi

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indica il tipo di riscrittura. Impossibile modificare il tipo dopo la creazione della riscrittura. Opzioni: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Categoria da reindirizzare. A seconda della configurazione, il percorso della richiesta potrebbe includere il suffisso .html o .htm e la categoria padre. Il percorso della richiesta deve essere univoco e non può essere utilizzato da un altro reindirizzamento. Se ricevi un errore che indica che il percorso della richiesta esiste, elimina il reindirizzamento esistente e riprova. |
| [!UICONTROL Target Path] | Percorso interno utilizzato dal sistema per puntare alla destinazione del reindirizzamento. Il percorso di destinazione è disattivato e non può essere modificato. |
| [!UICONTROL Redirect] | Determina il tipo di reindirizzamento. Opzioni: <br/>**[!UICONTROL No]**- Nessun reindirizzamento specificato. Molte operazioni creano richieste di reindirizzamento di questo tipo. Ad esempio, ogni volta che si aggiungono prodotti a una categoria, viene creato un reindirizzamento del tipo `No` per ogni visualizzazione store.<br/>**[!UICONTROL Temporary (302)]** - Indica ai motori di ricerca che la riscrittura ha una durata limitata. I motori di ricerca generalmente non conservano le informazioni sul rango delle pagine per le riscritture temporanee. <br/>**[!UICONTROL Permanent (301)]**- Indica ai motori di ricerca che la riscrittura è permanente. I motori di ricerca in genere conservano le informazioni sulla classificazione delle pagine per le riscritture permanenti. |
| [!UICONTROL Description] | Descrive lo scopo della riscrittura per riferimento interno. |

{style="table-layout:auto"}
