---
title: Disattivare l’integrazione dell’amministratore di Commerce con Adobe ID
description: Segui questa procedura facoltativa per disabilitare l’integrazione Amministratore Adobe Commerce con Adobe IMS.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/KL6Cx3ymElo7ROx5SUJtlqtKivnw7-heqPWGksGP-pg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 351
ht-degree: 0%

---

# Disattivare l’integrazione dell’amministratore di Commerce con Adobe ID

{{ee-feature}}

I commercianti che hanno integrato la loro istanza di Commerce con il flusso di lavoro di autenticazione Adobe IMS potrebbero dover disabilitare questa integrazione opzionale.

Dopo la disabilitazione dell’integrazione IMS, le distribuzioni di Commerce tornano al flusso di lavoro e ai criteri per le password di autenticazione di Commerce predefiniti. Solo i flussi di lavoro degli utenti amministratori sono interessati quando questa integrazione è abilitata o disabilitata.

Per una panoramica dell&#39;accesso dell&#39;amministratore di Commerce, vedere [Account amministratore](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html).

## Passaggio 1: disabilitare l’integrazione

Non puoi disabilitare questa integrazione dall’Amministratore. Per disabilitare l’integrazione Adobe IMS con Commerce e ripristinare l’autenticazione Commerce allo stato predefinito, è necessario disabilitare l’integrazione dall’interfaccia della riga di comando.

Per disabilitare l’integrazione:

```bash
bin/magento admin:adobe-ims:disable
```

In caso di esito positivo, Adobe Commerce visualizza il seguente messaggio:

```
Admin Adobe IMS integration is disabled.
```

## Passaggio 2: creare o recuperare la password Commerce

Dopo aver disabilitato l’integrazione, gli utenti amministratore devono utilizzare una password Commerce per accedere all’amministratore.

* Gli utenti amministratore di Commerce che ricordano la propria password Commerce preesistente (ovvero una password Commerce creata prima dell’integrazione IMS) possono utilizzarla per accedere all’amministratore.

* Gli utenti amministratori di Commerce che non hanno una password Commerce preesistente o l’hanno dimenticata devono creare una nuova password. Per creare una nuova password, gli utenti amministratori possono utilizzare la funzionalità [!UICONTROL Forgot your password?] nella pagina di accesso di Commerce per creare una nuova password. Consulta [Reimpostare le password dei clienti](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce non accetta un campo password vuoto.

## Dopo aver disabilitato l’integrazione

Il flusso di lavoro di autenticazione predefinito di Commerce riprende dopo la disabilitazione dell’integrazione IMS e viene nuovamente richiesta la password agli utenti amministratori.

La disabilitazione dell&#39;integrazione IMS comporta l&#39;eliminazione delle credenziali immesse quando l&#39;integrazione è stata abilitata (`Organization ID`, `Client ID` e `Client Secret` valori) dai file di configurazione di Commerce.
