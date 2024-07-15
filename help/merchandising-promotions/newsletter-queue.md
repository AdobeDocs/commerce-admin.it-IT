---
title: Code newsletter
description: Scopri come gestire le code di newsletter per inviare più batch di newsletter.
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Code newsletter

Per gestire il carico sul server, le newsletter con molti abbonati vengono inviate in una coda di più batch. Puoi controllare periodicamente la coda delle newsletter per verificarne lo stato e vedere quanti sono stati elaborati. Eventuali problemi che si verificano durante la trasmissione vengono visualizzati nel report _Problema newsletter_.

## Inviare una newsletter

1. Nel menu _Amministratore_, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. Nella griglia trovare il [modello di newsletter](newsletter-template.md) da inviare e impostare la colonna **[!UICONTROL Action]** su `Queue Newsletter`.

1. Per **[!UICONTROL Queue Date Start]**, selezionare la data di inizio della trasmissione dal calendario (![icona Calendario](../assets/icon-calendar.png)).

1. Per **[!UICONTROL Subscribers From]**, selezionare ogni visualizzazione dello store da includere nell&#39;esplosione dell&#39;e-mail.

1. Completa le informazioni sull’intestazione dell’e-mail:

   - Immettere una breve descrizione della newsletter per la riga **[!UICONTROL Subject]** dell&#39;intestazione e-mail.

   - Immettere **[!UICONTROL Sender Name]**.

   - Per **[!UICONTROL Sender Email]**, immettere l&#39;indirizzo di posta elettronica del mittente.

     Il nome e l’indirizzo e-mail predefiniti del mittente sono specificati nella configurazione.

     ![Informazioni coda newsletter](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. Se applicabile, immettere una nota nella casella **[!UICONTROL Message]** sopra le istruzioni per annullare l&#39;abbonamento.

   >[!NOTE]
   >
   >Non rimuovere le istruzioni, che sono richieste dalla legge in molte giurisdizioni.

1. Per applicare stili personalizzati a una newsletter, aggiungili nel campo **[!UICONTROL Newsletter Styles]**.

1. Al termine, fare clic su **[!UICONTROL Save and Resume]**.

   La newsletter viene visualizzata nella coda in attesa di elaborazione.

## Verifica la presenza di problemi

Nel menu _Amministratore_, vai a **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## Barra dei pulsanti

| Pulsante | Descrizione |
|--- |--- |
| **[!UICONTROL Back]** | Torna alla pagina Modelli newsletter senza salvare le modifiche. |
| **[!UICONTROL Reset]** | Ripristina i valori precedenti delle modifiche non salvate nel modulo di informazioni coda. |
| **[!UICONTROL Preview Template]** | Apre una pagina di anteprima in una scheda separata. |
| **[!UICONTROL Save and Resume]** | Salva tutte le modifiche apportate. Mette in coda la newsletter. |
| **[!UICONTROL Save Newsletter]** | Salva tutte le modifiche apportate. Mette in coda la newsletter. |

{style="table-layout:auto"}

## Colonne

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL ID] | Un identificatore numerico univoco assegnato a ciascun modello di newsletter. |
| [!UICONTROL Queue Start] | La data in cui è stata inviata la newsletter. |
| [!UICONTROL Queue End] | La data in cui la newsletter ha terminato l’invio. |
| [!UICONTROL Subject] | Oggetto del modello di newsletter. |
| [!UICONTROL Status] | Indica lo stato dell’invio della newsletter. Valori possibili: `Sent`, `Canceled`, `Not Sent`, `Sending` o `Paused`. |
| [!UICONTROL Processed] | Indica quante newsletter sono state inviate. |
| [!UICONTROL Recipients] | Indica quante newsletter sono state ricevute dagli abbonati. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**: apre una finestra separata per l&#39;anteprima del modello. |

{style="table-layout:auto"}
