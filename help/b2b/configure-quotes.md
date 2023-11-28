---
title: Configurare le virgolette
description: Scopri la configurazione delle virgolette, che controlla la quantità minima di ordini richiesta per le richieste di virgolette, la durata delle virgolette e gli allegati dei file.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Configurare le virgolette

Se le virgolette sono abilitate nel [Funzioni B2B](enable-basic-features.md), è possibile configurare il supporto per le offerte in Admin. La configurazione delle virgolette determina la quantità minima richiesta per le richieste di virgolette, la durata delle virgolette e i formati di file supportati per i file allegati.

>[!NOTE]
>
>Le opzioni di configurazione dei preventivi e la possibilità di utilizzare le funzioni di negoziazione dei preventivi sono controllate mediante [risorse ruolo](../systems/permissions-user-roles.md#role-resources). Queste risorse ruolo devono essere selezionate per il ruolo utente Amministratore assegnato all&#39;account utente Amministratore. Per concedere l&#39;accesso alle funzioni di preventivo nell&#39;amministratore, passare a **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, selezionare il ruolo e passare a [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] nel_ Risorse per il ruolo _albero.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Quotes]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL General]** ed effettuare le seguenti operazioni:

   ![Configurazione preventivi di vendita - Generale](./assets/quotes-general.png){width="700" zoomable="yes"}

   Consulta [Virgolette](../configuration-reference/sales/quotes.md) nel _Riferimento configurazione_ per un elenco completo delle opzioni della funzionalità Virgolette e delle relative funzioni.

   - Inserisci il **[!UICONTROL Minimum Amount]** nel carrello che deve essere soddisfatto prima di poter inviare una richiesta di preventivo.

   - Per **[!UICONTROL Minimum Amount Message]**, inserisci il messaggio da visualizzare quando il totale del carrello non soddisfa la quantità minima richiesta.

   - Per **[!UICONTROL Default Expiration Period]**, immettere il numero di **[!UICONTROL days]**, **[!UICONTROL weeks]**, o **[!UICONTROL months]** che un preventivo deve rimanere valido.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Attached files]** ed effettuare le seguenti operazioni:

   - Per **[!UICONTROL File formats for upload]**, immettere il suffisso di ogni tipo di file supportato per i file allegati a un preventivo.

     Immetti ogni suffisso di file in minuscolo e separato da una virgola.

     Per impostazione predefinita, sono supportati i seguenti formati: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`, e `jpeg`

   - Per **[!UICONTROL Maximum file size]**, immettere la dimensione massima in megabyte di un file allegato.

     Il valore immesso potrebbe essere sostituito dall&#39;impostazione del server.

     ![Configurazione offerte di vendita - file allegati](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
