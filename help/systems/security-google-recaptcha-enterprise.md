---
title: Google reCAPTCHA Enterprise
description: Scopri come configurare Google reCAPTCHA Enterprise per proteggere la vetrina Adobe Commerce as a Cloud Service da bot e attività fraudolente.
role: Admin
feature: Configuration, Security
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce as a Cloud Service (infrastruttura SaaS gestita da Adobe)."
exl-id: 2c88488c-8ff1-41db-b81b-89ad164e134d
TQID: https://experienceleague.adobe.com/oMZleuJsp2QiDD7IsMDV647LWKm938lNvY4--o6G3c8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eb30f47f-d87a-400f-8f78-63ce7979ff56id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) fornisce protezione avanzata da bot per la vetrina Adobe Commerce as a Cloud Service utilizzando l&#39;analisi adattiva dei rischi e l&#39;apprendimento automatico per distinguere utenti umani e bot. Questo aiuta a prevenire attività fraudolente, spam e abusi sul tuo sito.

>[!NOTE]
>
>Questa funzione NON fornisce il supporto reCAPTCHA per l’amministratore.

L&#39;[integrazione reCAPTCHA](https://experienceleague.adobe.com/developer/commerce/storefront/dropins/user-auth/recaptcha/) descrive come aggiungere il supporto per reCAPTCHA Enterprise nella vetrina.

Vedere [Google reCAPTCHA V3 e V2](security-google-recaptcha.md) per informazioni sulla configurazione di altre versioni di Google reCAPTCHA.

## Funzioni

Google reCAPTCHA Enterprise include le seguenti funzionalità:

- **Rilevamento avanzato bot**: utilizza i modelli di apprendimento automatico di Google Cloud per il rilevamento avanzato dei bot
- **Analisi del punteggio di rischio**: fornisce punteggi di rischio dettagliati (0,0-1,0) per ogni interazione
- **Soglie configurabili**: imposta i punteggi minimi di rischio accettabili per tenant
- **Supporto multi-tenant**: configurazione per tenant con progetti Google Cloud isolati
- **Credenziali crittografate**: credenziali dell&#39;account del servizio archiviate crittografate in un database
- **Protezione modulo**: protegge tutti i moduli Commerce standard, inclusi accesso, pagamento, recensioni dei prodotti e altro ancora.

## Prerequisiti

Prima di configurare Google reCAPTCHA Enterprise per la vetrina Adobe Commerce as a Cloud Service sono necessarie le seguenti risorse:

- Un account Google Cloud attivo con reCAPTCHA Enterprise abilitato.
- Accedi alla console Google Cloud per creare e gestire le chiavi aziendali reCAPTCHA.

Nelle installazioni Adobe Commerce as a Cloud Service con più tenant, ogni tenant deve disporre del proprio progetto Google Cloud e delle chiavi aziendali reCAPTCHA.

## Passaggio 1: configurare Google reCAPTCHA Enterprise

Segui questi passaggi generali per configurare Google reCAPTCHA Enterprise per la vetrina. Per istruzioni dettagliate, consulta la [documentazione aziendale di Google reCAPTCHA](https://docs.cloud.google.com/recaptcha/docs/overview).

1. [Crea un progetto Google Cloud](https://developers.google.com/workspace/guides/create-project) per l&#39;implementazione reCAPTCHA Enterprise.

1. Abilita l&#39;API aziendale [reCAPTCHA](https://docs.cloud.google.com/recaptcha/docs/prepare-environment).

1. Crea una [chiave del sito](https://docs.cloud.google.com/recaptcha/docs/choose-key-type) dell&#39;organizzazione reCAPTCHA basata su punteggio.

1. Creare un account di servizio con il ruolo IAM `roles/recaptchaenterprise.admin`.

1. Scarica il file della chiave JSON dell’account di servizio, che contiene le credenziali necessarie per autenticare la vetrina Adobe Commerce as a Cloud Service con Google reCAPTCHA Enterprise.

## Passaggio 2: configurare Google reCAPTCHA per la vetrina

1. Nella barra laterale di Adobe Commerce _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Espandere _[!UICONTROL Security]_e scegliere **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Scorri verso il basso fino alla sezione **[!UICONTROL reCAPTCHA Enterprise]** e completa la configurazione come segue.

   - Per **[!UICONTROL Site Key]**, copia e incolla la chiave del sito aziendale reCAPTCHA dalla console Google Cloud.

   - Per **[!UICONTROL Google Cloud Project ID]**, copia e incolla l&#39;ID progetto dal tuo progetto Google Cloud.

   - Per **[!UICONTROL Service Account JSON]**, copiare il contenuto del file di chiave JSON dell&#39;account del servizio scaricato in [Passaggio 1: configurare Google reCAPTCHA Enterprise](#step-1-set-up-google-recaptcha-enterprise).

   - Per **[!UICONTROL Minimum Score Threshold]**, immetti il punteggio minimo (0,0-1,0) per identificare quando un&#39;interazione dell&#39;utente viene segnalata come rischio potenziale. Un punteggio di 1,0 è una tipica interazione dell’utente e 0,0 è probabilmente un bot.

   - Per **[!UICONTROL Badge Position]**, scegli la posizione del badge reCAPTCHA invisibile su ogni pagina. Opzioni: `Inline` / `Bottom Right` / `Bottom Left`.

   - Per **[!UICONTROL Theme]**, scegliere `Light Theme` (impostazione predefinita) o `Dark Theme` per determinare lo stile della casella reCAPTCHA di Google.

   - Per **[!UICONTROL Language Code]**, immetti un [codice a due caratteri](https://developers.google.com/recaptcha/docs/language) che specifica il linguaggio utilizzato per il testo e i messaggi reCAPTCHA di Google.

   - Per **[!UICONTROL Validation Failure Message]**, è possibile modificare il messaggio visualizzato nella vetrina quando la convalida non ha esito positivo.


1. Espandere la sezione **[!UICONTROL Storefront]** e impostare ogni modulo della vetrina che si desidera proteggere su **[!UICONTROL reCAPTCHA Enterprise]**.

   {{recaptcha-forms-list}}

   ![Configurazione opzioni storefront](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Passaggio 3: salvare la configurazione

1. Al termine delle impostazioni di configurazione, fare clic su **[!UICONTROL Save Config]**.

1. Nel messaggio nella parte superiore dell&#39;area di lavoro, fare clic su **[!UICONTROL Cache Management]** e aggiornare ogni cache non valida.
