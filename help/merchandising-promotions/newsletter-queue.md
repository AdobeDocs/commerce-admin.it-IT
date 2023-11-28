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

Per gestire il carico sul server, le newsletter con molti abbonati vengono inviate in una coda di più batch. Puoi controllare periodicamente la coda delle newsletter per verificarne lo stato e vedere quanti sono stati elaborati. Eventuali problemi che si verificano durante la trasmissione vengono visualizzati sul _Problema newsletter_ rapporto.

## Inviare una newsletter

1. Il giorno _Amministratore_ menu, vai a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. Nella griglia, individua [modello newsletter](newsletter-template.md) da inviare e impostare **[!UICONTROL Action]** colonna a `Queue Newsletter`.

1. Per **[!UICONTROL Queue Date Start]**, seleziona la data di inizio della trasmissione dal calendario (![Icona Calendario](../assets/icon-calendar.png)).

1. Per **[!UICONTROL Subscribers From]**, seleziona ogni visualizzazione del negozio da includere nell’esplosione dell’e-mail.

1. Completa le informazioni sull’intestazione dell’e-mail:

   - Immetti una breve descrizione della newsletter per **[!UICONTROL Subject]** dell’intestazione e-mail.

   - Inserisci il **[!UICONTROL Sender Name]**.

   - Per **[!UICONTROL Sender Email]**, immetti l&#39;indirizzo e-mail del mittente.

     Il nome e l’indirizzo e-mail predefiniti del mittente sono specificati nella configurazione.

     ![Informazioni coda newsletter](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. Se applicabile, inserire una nota nella sezione **[!UICONTROL Message]** sopra le istruzioni per annullare l’abbonamento.

   >[!NOTE]
   >
   >Non rimuovere le istruzioni, che sono richieste dalla legge in molte giurisdizioni.

1. Per applicare stili personalizzati a una newsletter, aggiungili nella **[!UICONTROL Newsletter Styles]** campo.

1. Al termine, fai clic su **[!UICONTROL Save and Resume]**.

   La newsletter viene visualizzata nella coda in attesa di elaborazione.

## Verifica la presenza di problemi

Il giorno _Amministratore_ menu, vai a **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

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
| [!UICONTROL Status] | Indica lo stato dell’invio della newsletter. Valori possibili: `Sent`, `Canceled`, `Not Sent`, `Sending`, o `Paused`. |
| [!UICONTROL Processed] | Indica quante newsletter sono state inviate. |
| [!UICONTROL Recipients] | Indica quante newsletter sono state ricevute dagli abbonati. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**: apre una finestra separata per visualizzare in anteprima il modello. |

{style="table-layout:auto"}
