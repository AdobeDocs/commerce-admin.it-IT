---
title: Riscrittura dell'URL della pagina del contenuto
description: Scopri come utilizzare la riscrittura dell’URL della pagina dei contenuti per reindirizzare i collegamenti all’URL di un’altra pagina dei contenuti nel tuo store di Commerce.
exl-id: e29c45fd-cf25-4b51-a8ae-9e188dc2a61c
feature: Page Content, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Riscrittura dell&#39;URL della pagina del contenuto

Prima di iniziare, assicurati di comprendere esattamente cosa deve essere realizzato il reindirizzamento. Pensa in termini di _destinazione_ / _origine_ o _reindirizzamento a_ / _reindirizzamento da_. Anche se le persone possono ancora passare alla pagina precedente da motori di ricerca o collegamenti obsoleti, il reindirizzamento fa sì che il tuo negozio passi alla nuova destinazione.

![Riscritture URL - pagina CMS](./assets/url-rewrite-cms-page.png){width="700" zoomable="yes"}

## Passaggio 1: Pianificare la riscrittura

Per evitare errori, prendere nota della chiave URL del _reindirizzamento a_ pagina e del _reindirizzamento da_ pagina.

In caso di dubbi, apri ogni pagina del tuo Negozio e copia il percorso dalla barra degli indirizzi del browser.

### Percorso pagina CMS

Reindirizza a: `new-page`

Reindirizzamento da: `old-page`

## Passaggio 2: Creare la riscrittura

{{url-rewrite-params}}

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Prima di procedere, eseguire le operazioni seguenti per verificare che il percorso della richiesta sia disponibile.

   - Nel filtro di ricerca nella parte superiore della colonna **[!UICONTROL Request Path]**, immettere la chiave URL della pagina da reindirizzare e fare clic su **[!UICONTROL Search]**.

   - Se esistono più record di reindirizzamento per la pagina, individua quello che corrisponde alla visualizzazione store applicabile e aprilo in modalità di modifica.

   - Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Delete]**. Quando richiesto, fare clic su **[!UICONTROL OK]** per confermare.

1. Quando si torna alla pagina URL riscrive, fare clic su **[!UICONTROL Add URL Rewrite]**.

1. Imposta **[!UICONTROL Create URL Rewrite]** su `for CMS page`.

1. Trova la nuova pagina di destinazione nella griglia e apri in modalità di modifica.

   ![Aggiungi riscrittura URL - per pagina CMS](./assets/url-rewrite-cms-page-add.png){width="700" zoomable="yes"}

1. In Informazioni di riscrittura URL eseguire le operazioni seguenti:

   - Se sono presenti più visualizzazioni dello store, selezionare **[!UICONTROL Store]** a cui applicare la riscrittura.

   - Per **[!UICONTROL Request Path]**, immetti la chiave URL della pagina originale richiesta dal cliente. Questo è il _reindirizzamento da_ pagina.

     >[!NOTE]
     >
     >Il percorso della richiesta deve essere univoco per l’archivio specificato. Se esiste già un reindirizzamento che utilizza lo stesso percorso di richiesta, quando tenti di salvare il reindirizzamento riceverai un errore. Prima di poterne creare uno, devi eliminare il reindirizzamento precedente.

   - Imposta **[!UICONTROL Redirect]** su uno dei seguenti:

      - `Temporary (302)`
      - `Permanent (301)`

   - Per il riferimento, immettere una breve descrizione della riscrittura.

   ![Informazioni di riscrittura URL](./assets/url-rewrite-cms-page-information.png){width="600" zoomable="yes"}

1. Prima di salvare il reindirizzamento, verifica quanto segue:

   - Il collegamento nell’angolo in alto a sinistra mostra il nome della pagina di destinazione.
   - Il percorso della richiesta contiene il percorso per il reindirizzamento _originale da_ pagina.

1. Al termine, fare clic su **[!UICONTROL Save]**.

   La nuova riscrittura viene visualizzata nella griglia nella parte superiore dell&#39;elenco.

## Passaggio 3: Verifica il risultato

1. Vai alla pagina principale del tuo negozio.

1. Effettuare una delle seguenti operazioni:

   - Passa alla pagina _reindirizzamento originale da_.
   - Nella barra degli indirizzi del browser, immetti il nome del _reindirizzamento originale da_ pagina subito dopo l&#39;URL dell&#39;archivio e premi **Invio**.

   Viene visualizzata la nuova pagina di destinazione invece della richiesta della pagina originale.

## Descrizioni dei campi

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Indica il tipo di riscrittura. Impossibile modificare il tipo dopo la creazione della riscrittura. Opzioni: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Pagina CMS da reindirizzare. Il percorso della richiesta deve essere univoco e non può essere utilizzato da un altro reindirizzamento. Se ricevi un messaggio di errore indicante che il percorso della richiesta esiste, elimina il reindirizzamento esistente e riprova. |
| [!UICONTROL Target Path] | Percorso interno utilizzato dal sistema per puntare alla destinazione. Il percorso di destinazione è disattivato e non può essere modificato. |
| [!UICONTROL Redirect] | Determina il tipo di reindirizzamento. Opzioni: <br/>**[!UICONTROL No]**- Nessun reindirizzamento specificato.<br/>**[!UICONTROL Temporary (302)]** - Indica ai motori di ricerca che la riscrittura ha una durata limitata. I motori di ricerca generalmente non conservano le informazioni sul rango delle pagine per le riscritture temporanee. <br/>**[!UICONTROL Permanent (301)]**- Indica ai motori di ricerca che la riscrittura è permanente. I motori di ricerca in genere conservano le informazioni sulla classificazione delle pagine per le riscritture permanenti. |
| [!UICONTROL Description] | Descrive lo scopo della riscrittura per riferimento interno. |

{style="table-layout:auto"}
