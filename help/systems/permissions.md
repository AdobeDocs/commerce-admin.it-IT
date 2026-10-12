---
title: Autorizzazioni amministratore
description: Scopri gli account utente amministratore e come i ruoli vengono utilizzati per concedere l’accesso alle funzioni di gestione dello store.
exl-id: 54e4a322-4747-4472-b60b-cfe84c109f86
role: Admin
feature: Admin Workspace, Roles/Permissions, User Account, Security
TQID: 'https://experienceleague.adobe.com/7xyouYohAbOKbwVCxZPamD-7gEiqGrqEAAg9FDm8z-U'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: e439352c-5b67-587d-b34e-d2a0aa5a0242
    internal-label: Roles/Permissions
  - id: 4560f5f5-d00c-5b5d-b61b-369d85ef7a26
    internal-label: User Account
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
    internal-label: Admin tools and workspace
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
    internal-label: Admin workspace
role_v2:
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
source-wordcount: '260'
ht-degree: 0%
---
# Autorizzazioni amministratore

Adobe Commerce e Magento Open Source utilizzano ruoli e autorizzazioni per creare diversi livelli di accesso all’amministratore. La prima volta che il tuo archivio viene configurato, ricevi un set di credenziali di accesso per il ruolo Amministratore con autorizzazioni complete. Tuttavia, puoi limitare il livello delle autorizzazioni in base alla necessità di sapere per altre persone che lavorano sul tuo sito. Ad esempio, a un membro del team di progettazione può essere consentito l’accesso solo agli strumenti di progettazione del contenuto, ma non alle aree con informazioni su clienti e ordini.

Inoltre, puoi limitare ulteriormente l’accesso come amministratore a un solo sito specifico o a un insieme di siti e ai relativi dati associati. Se disponi di più marchi o business unit con negozi separati sulla stessa installazione di Commerce, puoi fornire all’amministratore l’accesso a ogni business unit, ma nascondere e proteggere i dati da altri utenti amministratori.

Quando l’accesso di un utente amministratore è limitato a un sito web o a un archivio specifico, quelli in cui non è autorizzato non sono visibili o sono visualizzati in grigio. Per l’utente vengono visualizzati solo i dati di vendita e altri dati per siti web e store consentiti.

- ![Adobe Commerce](../assets/adobe-logo.svg) (solo Adobe Commerce) Per impostazione predefinita, il sistema registra (registra) automaticamente tutte le azioni eseguite da un utente quando applica le modifiche a un archivio. Le azioni di amministrazione possono essere riviste nel [Rapporto Registri azioni](action-log-report.md). Configura la registrazione in [Registrazione azioni amministratore](action-log.md) nelle impostazioni di amministrazione avanzate del tuo archivio.

![Amministratore - tutti gli account utente](./assets/users-all.png){width="700" zoomable="yes"}
