---
title: Google reCAPTCHA Enterprise
description: Scopri come configurare Google reCAPTCHA Enterprise per proteggere la vetrina Adobe Commerce as a Cloud Service da bot e attività fraudolente.
role: Admin
feature: Configuration, Security
source-git-commit: 5181e6dcbffdca87dd6c376c36f7c9d0a3fbc015
workflow-type: tm+mt
source-wordcount: '526'
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) fornisce protezione avanzata da bot per la vetrina Adobe Commerce as a Cloud Service utilizzando l&#39;analisi adattiva dei rischi e l&#39;apprendimento automatico per distinguere utenti umani e bot. Questo aiuta a prevenire attività fraudolente, spam e abusi sul tuo sito.

>[!NOTE]
>
>Questa funzione NON fornisce il supporto reCAPTCHA per l’amministratore.

Vedere [Google reCAPTCHA V3 e V2](security-google-recaptcha.md) per informazioni sulla configurazione di altre versioni di Google reCAPTCHA.

## Funzioni

Google reCAPTCHA Enterprise include le seguenti funzionalità:

- **Rilevamento avanzato bot**: utilizza i modelli di apprendimento automatico di Google Cloud per il rilevamento avanzato dei bot
- **Analisi del punteggio di rischio**: fornisce punteggi di rischio dettagliati (0,0-1,0) per ogni interazione
- **Soglie configurabili**: imposta i punteggi minimi di rischio accettabili per tenant
- **Supporto multi-tenant**: configurazione per tenant con progetti Google Cloud isolati
- **Credenziali crittografate**: credenziali dell&#39;account del servizio archiviate crittografate nel database
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

1. Nel pannello a sinistra in _[!UICONTROL Security]_, scegli **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Completare la sezione **[!UICONTROL reCAPTCHA Enterprise]** come segue.

   - Per **[!UICONTROL Site Key]**, copia e incolla la chiave del sito reCAPTCHA Enterprise dalla console Google Cloud.

   - Per **[!UICONTROL Google Cloud Project ID]**, copia e incolla l&#39;ID progetto dal tuo progetto Google Cloud.

   - Per **[!UICONTROL Service Account JSON]**, copiare il contenuto del file di chiave JSON dell&#39;account del servizio scaricato in [Passaggio 1: configurare Google reCAPTCHA Enterprise](#step-1-set-up-google-recaptcha-enterprise).

   - Per **[!UICONTROL Minimum Score Threshold]**, immettere il punteggio minimo (0,0-1,0) per identificare quando un&#39;interazione utente viene contrassegnata come rischio potenziale; dove 1,0 è un&#39;interazione utente tipica e 0,0 è probabilmente un bot.

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
