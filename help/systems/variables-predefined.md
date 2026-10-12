---
title: Usa variabili predefinite
description: Scopri le variabili predefinite e come aggiungerle in un modello e-mail.
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
TQID: 'https://experienceleague.adobe.com/TKhaNVRFLc3VK0iDkCpqoWSnvFRJmDWAIw1uBPzlh00'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8d0b446f-5b16-5a10-b272-01143504a11c
    internal-label: System
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
  - id: bb03f6c4-cab9-560e-9d02-5816e1808d17
    internal-label: Communications
subfeature_v2:
  - id: 2191e157-828a-5358-ad69-ebcaa8402915
    internal-label: Variables
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%
---
# Usa variabili predefinite

Le variabili [Predefined](variables-predefined.md) semplificano la personalizzazione dei modelli [email](email-templates.md) e [newsletter](../merchandising-promotions/newsletters.md) e di altri tipi di contenuto. L&#39;elenco delle variabili [predefinite](variables-predefined.md) consentite viene visualizzato quando si fa clic sul pulsante Inserisci variabile. Come mostrato nell’immagine seguente, l’elenco delle variabili disponibili per un modello e-mail specifico è determinato dai dati associati al modello. Per un elenco dei modelli e-mail utilizzati di frequente e delle relative variabili associate, vedere [Riferimento variabile](variables-reference.md).

![Variabili predefinite per modello e-mail](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## Aggiungere una variabile a un modello e-mail

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. Effettuare una delle seguenti operazioni:

   - Per aggiungere la variabile a un modello esistente, fai clic sul modello nell’elenco per aprirlo in modalità di modifica.

   - Per utilizzare la variabile in un nuovo modello, fare clic su **[!UICONTROL Add New Template]** e personalizzare il codice del modello predefinito. Vedi [Modelli di messaggio](email-template-custom.md#message-templates).

1. In _[!UICONTROL Load default template]_scegliere **[!UICONTROL Template]**che si desidera personalizzare.

1. Per applicare un modello, scegliere **[!UICONTROL Load Template]**.

   Nel campo _[!UICONTROL Currently used for]_viene visualizzato il percorso di configurazione per il modello._[!UICONTROL Template Subject]_ e _[!UICONTROL Template Content]_vengono generati automaticamente in relazione al modello selezionato.

   - **[!UICONTROL Template Subject]** - Il testo viene visualizzato nella riga dell&#39;oggetto di un&#39;e-mail.

   - **[!UICONTROL Template Content]** - Questo testo viene visualizzato nel contenuto completo dell&#39;e-mail inviata.

   ![Contenuto modello e-mail](./assets/email-template-content.png){width="600" zoomable="yes"}

1. Immetti **[!UICONTROL Template Name]**.

1. Per un elenco delle [variabili predefinite](variables-predefined.md) che possono essere utilizzate con questo modello di posta elettronica, fare clic su **[!UICONTROL Insert Variable]**.

   Determinare la variabile da inserire nel modello. Quindi, fai clic su _Chiudi_ (X) nell&#39;angolo superiore destro. (Tornerai su questo più tardi.)

1. Per visualizzare un modello del modello, fare clic su **[!UICONTROL Preview Template]** nella barra dei pulsanti.

   Quando l’anteprima viene aperta in una nuova scheda, determina dove posizionare la variabile in relazione all’altro contenuto. Quindi torna alla scheda originale per continuare.

   ![Anteprima modello](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. Nella casella **[!UICONTROL Template Content]**, posizionare il punto di inserimento dove si desidera visualizzare la variabile e fare clic su **[!UICONTROL Insert Variable...]**.

1. Nell’elenco delle variabili disponibili, fai clic su quella che desideri inserire nel modello.

1. Al termine, fare clic su **[!UICONTROL Save Template]**.

## Convertire il modello in testo normale

1. Apri un modello in modalità di modifica.

1. Nella parte superiore della pagina, fare clic su **[!UICONTROL Convert to Plain Text]**.

1. Quando viene richiesto di rimuovere i tag, fare clic su **[!UICONTROL OK]**.

1. Per salvare la versione in testo normale, fare clic su **[!UICONTROL Save Template]**.

## Ripristina la versione di HTML

1. Nella parte superiore della pagina, fare clic su **[!UICONTROL Return HTML Version]**.

1. Per salvare la versione HTML del modello, fare clic su **[!UICONTROL Save Template]**.
