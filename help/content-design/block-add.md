---
title: Aggiungere blocchi di contenuto
description: Crea blocchi di contenuto personalizzati che puoi riutilizzare in qualsiasi pagina o all’interno di un altro blocco.
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# Aggiungere blocchi di contenuto

È possibile creare blocchi di contenuto personalizzati e quindi aggiungerli a qualsiasi pagina, gruppo di pagine o persino a un altro blocco. Ad esempio, è possibile inserire un cursore immagine in un blocco e quindi posizionare il blocco nella home page. L’area di lavoro Blocchi utilizza lo stesso [controlli di base](pages-workspace.md) come _Pagine_ Workspace per trovare i blocchi disponibili ed eseguire la manutenzione ordinaria. Una volta completato il blocco, puoi utilizzare [Widget](widget-static-block.md) per posizionarlo su pagine specifiche del tuo negozio.

![Nella pagina Blocchi viene visualizzata una griglia dei blocchi esistenti](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## Creare un blocco

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Nell’angolo superiore destro, fai clic su **Aggiungi nuovo blocco**.

   ![Nella pagina Nuovo blocco vengono visualizzate le opzioni e uno spazio dei contenuti](./assets/block-detail.png){width="500" zoomable="yes"}

1. Se desideri modificare lo stato di attivazione predefinito del nuovo blocco, imposta **Abilita blocco** a `No`.

1. Assegna un **Titolo blocco** per riferimento interno.

1. Assegna un univoco **Identificatore** per il blocco.

   Utilizza tutti i caratteri minuscoli con il carattere di sottolineatura anziché gli spazi.

1. Seleziona ciascuno **[!UICONTROL Store View]** dove desideri che il blocco sia disponibile.

1. Aggiungi il contenuto per il blocco utilizzando il set di strumenti di contenuto visualizzato:

   - Se [Page Builder](../page-builder/introduction.md) è attivato, seleziona **[!UICONTROL Edit with Page Builder]** per utilizzare gli strumenti Page Builder nel contenuto [workspace](../page-builder/workspace.md).

     ![Area di lavoro di Page Builder](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >Per informazioni sull’aggiunta di blocchi con Page Builder, consulta [Tutorial 2: blocchi](../page-builder/2-blocks.md).

   - Utilizza il [editor](editor.md) per formattare il testo, creare collegamenti e aggiungere tabelle, immagini, video e audio.

     Se preferisci lavorare con codice HTML, fai clic su **Mostra/Nascondi editor**.

     ![Editor blocchi (nascosto)](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save]** freccia e scegli **[!UICONTROL Save & Close]**.

   Il nuovo blocco viene visualizzato nella parte inferiore dell&#39;elenco nella griglia Blocchi.

1. Utilizza il [Widget](widget-static-block.md) per posizionare il blocco completato su una pagina specifica del negozio.

## Eliminare un blocco

Esistono due modi per rimuovere un blocco personalizzato. Puoi rimuoverlo dal _Blocchi_ o dalla pagina modifica blocco.

### Metodo 1: rimuovere un blocco dalla griglia Blocchi

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Individua i blocchi utilizzando i filtri sopra la griglia e seleziona la casella di controllo per uno o più blocchi da eliminare.
1. Nell&#39;angolo superiore sinistro dell&#39;elenco, impostare **[!UICONTROL Actions]** a `Delete`.
1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.

### Metodo 2: rimuovere un blocco dalla pagina di modifica

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Trova il blocco da eliminare.
1. In _Azioni_ per il blocco, fai clic su **[!UICONTROL Select]** e scegli **[!UICONTROL Edit]**.
1. Nella barra dei menu, fai clic su **[!UICONTROL Delete Block]**.
1. Per confermare l’azione, fai clic su **[!UICONTROL OK]**.

## Menu Salva

| Comando | Descrizione |
|----------|----------- |
| [!UICONTROL Save] | Salva il blocco corrente e continua a lavorare. |
| [!UICONTROL Save & Duplicate] | Salva e chiudi il blocco corrente e apri una nuova copia duplicata. |
| [!UICONTROL Save & Close] | Salvare e chiudere il blocco corrente e tornare alla griglia Blocchi. |

{style="table-layout:auto"}

## Aggiungere un lightbox o un cursore

- È facile aggiungere una [cursore](../page-builder/slider.md) al tuo negozio con [[!DNL Page Builder]](../page-builder/introduction.md). Il dispositivo di scorrimento può essere impostato per la riproduzione automatica o controllato manualmente con i pulsanti di navigazione.

  ![Cursore Page Builder](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  È inoltre disponibile un ampio assortimento di lightbox per immagini basate su jQuery su [[!DNL Commerce Marketplace]][1], e alcuni sono gratuiti.

- Puoi scaricare un’estensione anche da [!DNL Commerce Marketplace]. Per ulteriori informazioni, consulta la documentazione fornita dallo sviluppatore dell’estensione.

[1]: https://marketplace.magento.com/extensions.html?q=lightbox
