---
title: Configurare le virgolette
description: Scopri la configurazione delle virgolette, che controlla la quantità minima di ordini richiesta per le richieste di virgolette, la durata delle virgolette e gli allegati dei file.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
TQID: https://experienceleague.adobe.com/RenH7-cnfF8qVEqFQc7IPMVsIp0alug5OgvYlr5piTM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 0%

---

# Configurare le virgolette

Se le virgolette sono abilitate nelle [funzionalità B2B generali](enable-basic-features.md), è possibile configurare il supporto per le virgolette in Amministrazione. La configurazione delle virgolette determina la quantità minima richiesta per le richieste di virgolette, la durata delle virgolette e i formati di file supportati per i file allegati.

>[!NOTE]
>
>Le opzioni di configurazione dei preventivi e la possibilità di utilizzare le funzioni di negoziazione dei preventivi sono controllate utilizzando le [risorse ruolo](../systems/permissions-user-roles.md#role-resources). Queste risorse ruolo devono essere selezionate per il ruolo utente Amministratore assegnato all&#39;account utente Amministratore. Per concedere l&#39;accesso alle funzioni di preventivo nell&#39;amministratore, passare a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, selezionare il ruolo e passare a [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] nell&#39;albero_ Risorse ruolo _.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Quotes]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL General]** ed effettuare le seguenti operazioni:

   ![Configurazione offerte di vendita - Generale](./assets/quotes-general.png){width="700" zoomable="yes"}

   Per un elenco completo delle opzioni della funzionalità Quotes e delle relative funzioni, vedere [Quotes](../configuration-reference/sales/quotes.md) nel _Riferimento configurazione_.

   - Immettere **[!UICONTROL Minimum Amount]** nel carrello che deve essere soddisfatto prima di poter inviare una richiesta di preventivo.

   - Per **[!UICONTROL Minimum Amount Message]**, immettere il messaggio che si desidera visualizzare quando il totale del carrello acquisti non soddisfa la quantità minima richiesta.

   - Per **[!UICONTROL Default Expiration Period]**, immettere il numero di **[!UICONTROL days]**, **[!UICONTROL weeks]** o **[!UICONTROL months]** che un preventivo deve rimanere valido.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Attached files]** ed effettuare le seguenti operazioni:

   - Per **[!UICONTROL File formats for upload]**, immettere il suffisso di ogni tipo di file supportato per i file allegati a virgolette.

     Immetti ogni suffisso di file in minuscolo e separato da una virgola.

     Per impostazione predefinita, sono supportati i seguenti formati: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` e `jpeg`

   - Per **[!UICONTROL Maximum file size]**, immettere la dimensione massima in megabyte di un file allegato.

     Il valore immesso potrebbe essere sostituito dall&#39;impostazione del server.

     ![Configurazione offerte di vendita - file allegati](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
