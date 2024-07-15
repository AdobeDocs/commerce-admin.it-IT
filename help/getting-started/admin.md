---
title: Che cos’è l’amministratore?
description: Scopri l’ [!DNL Commerce] Amministratore, il luogo in cui i commercianti configurano prodotti e promozioni, gestiscono gli ordini ed eseguono altre attività amministrative.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Che cos’è l’amministratore?

Il tuo store _Admin_ è il back office protetto da password in cui, in qualità di commerciante, puoi impostare prodotti e promozioni, gestire gli ordini ed eseguire altre attività amministrative. Tutte le attività di configurazione di base e le operazioni di gestione degli archivi vengono eseguite da _Admin_.

Per ulteriore sicurezza, l&#39;accesso _Admin_ è protetto da [autenticazione a due fattori](../systems/security-two-factor-authentication.md) e può essere configurato per richiedere un [CAPTCHA](../systems/security-captcha.md). Per ulteriori informazioni, vai a [Configurazione di Admin Security](../systems/security-admin.md).

![Barra laterale di amministrazione e dashboard](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Le credenziali di accesso [iniziali](admin-signin.md) sono state configurate durante l&#39;installazione di Adobe Commerce o di Magento Open Source. Se dimentichi la password, puoi inviare una password temporanea all’indirizzo e-mail associato all’account. Per aumentare la sicurezza, configura il tuo archivio in modo che richieda un nome utente con distinzione tra maiuscole e minuscole e una password complessa.

Oltre all&#39;account utente Amministratore predefinito, la tua azienda può creare tutti i [account aggiuntivi](../systems/permissions-users-all.md) necessari per gestire gli account cliente dello store e del supporto. Ogni account può essere associato a un [ruolo](../systems/permissions-user-roles.md) specifico e al livello di accesso, in base all&#39;azienda _che deve sapere_. L’indirizzo e-mail associato a ciascun account utente amministratore deve essere univoco.

{{ims-admin-note}}

## Raccolta dati di utilizzo

La prima volta che accedi a _Admin_, ti viene richiesto di concedere l&#39;autorizzazione di Adobe per raccogliere i dati di utilizzo per tutti gli utenti Admin. Adobe Consentendo la raccolta dei dati di utilizzo da parte dell’amministratore, puoi contribuire a migliorare l’esperienza di utilizzo dell’amministratore Adobe Commerce e dei prodotti e servizi correlati.

![Consenti raccolta dati di utilizzo amministratore](./assets/admin-usage-data.png){width="600"}

I singoli utenti non sono identificati nei dati di utilizzo. L&#39;impostazione della raccolta dati può essere modificata in qualsiasi momento dalla configurazione [Utilizzo amministratore](../configuration-reference/advanced/admin.md#admin-usage).

Per Adobe Commerce, l&#39;abilitazione della raccolta dati abilita anche la _guida interna al prodotto_, progettata per portare contenuto interattivo all&#39;_amministratore_. Fornisce aiuto, descrizioni, guide dettagliate, informazioni sull’onboarding, annunci sulle funzioni e altro ancora.
