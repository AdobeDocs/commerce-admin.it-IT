---
title: Che cos’è l’amministratore?
description: Scopri l’ [!DNL Commerce] Amministratore, il luogo in cui i commercianti configurano prodotti e promozioni, gestiscono gli ordini ed eseguono altre attività amministrative.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
TQID: https://experienceleague.adobe.com/A0DuYohA907-EHXQ6fyy2Sz83Y6cFZ7PDY5SmtBa14Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 0%

---

# Che cos’è l’amministratore?

Il tuo store _Admin_ è il back office protetto da password in cui, in qualità di commerciante, puoi impostare prodotti e promozioni, gestire gli ordini ed eseguire altre attività amministrative. Tutte le attività di configurazione di base e le operazioni di gestione degli archivi vengono eseguite da _Admin_.

Per ulteriore sicurezza, l&#39;accesso _Admin_ è protetto da [autenticazione a due fattori](../systems/security-two-factor-authentication.md) e può essere configurato per richiedere un [CAPTCHA](../systems/security-captcha.md). Per ulteriori informazioni, vai a [Configurazione di Admin Security](../systems/security-admin.md).

![Barra laterale di amministrazione e dashboard](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Le credenziali di accesso [iniziali](admin-signin.md) sono state configurate durante l&#39;installazione di Adobe Commerce o Magento Open Source. Se dimentichi la password, puoi inviare una password temporanea all’indirizzo e-mail associato all’account. Per aumentare la sicurezza, configura il tuo archivio in modo che richieda un nome utente con distinzione tra maiuscole e minuscole e una password complessa.

Oltre all&#39;account utente Amministratore predefinito, la tua azienda può creare tutti i [account aggiuntivi](../systems/permissions-users-all.md) necessari per gestire gli account cliente dello store e del supporto. Ogni account può essere associato a un [ruolo](../systems/permissions-user-roles.md) specifico e al livello di accesso, in base all&#39;azienda _che deve sapere_. L’indirizzo e-mail associato a ciascun account utente amministratore deve essere univoco.

{{ims-admin-note}}

## Raccolta dati di utilizzo

La prima volta che accedi a _Admin_, ti viene richiesto di concedere l&#39;autorizzazione Adobe per raccogliere i dati di utilizzo per tutti gli utenti Admin. Consentendo la raccolta dei dati di utilizzo da parte dell’amministratore, puoi aiutare Adobe a migliorare l’esperienza di utilizzo dell’amministratore Adobe Commerce e dei prodotti e servizi correlati.

![Consenti raccolta dati di utilizzo amministratore](./assets/admin-usage-data.png){width="600"}

I singoli utenti non sono identificati nei dati di utilizzo. L&#39;impostazione della raccolta dati può essere modificata in qualsiasi momento dalla configurazione [Utilizzo amministratore](../configuration-reference/advanced/admin.md#admin-usage).

Per Adobe Commerce, l&#39;abilitazione della raccolta dati abilita anche la _guida interna al prodotto_, progettata per portare contenuto interattivo all&#39;_amministratore_. Fornisce aiuto, descrizioni, guide dettagliate, informazioni sull’onboarding, annunci sulle funzioni e altro ancora.
