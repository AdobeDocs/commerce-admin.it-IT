---
title: Amministratore Commerce in Adobe Unified Experience
description: Scopri in che modo i clienti di Adobe Commerce as a Cloud Service possono accedere e navigare nell’amministrazione di Commerce in Adobe Unified Experience e tornare all’interfaccia classica.
feature: Admin Workspace
role: Admin, User
level: Beginner
badgeSaas: label="Solo SaaS" type="Positive" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce as a Cloud Service (infrastruttura SaaS gestita da Adobe)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
    internal-label: Admin tools and workspace
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
    internal-label: Admin workspace
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: e10d4cd8b48e1714c0f32b6c6733524eaac0aa8c
workflow-type: tm+mt
source-wordcount: '1451'
ht-degree: 0%
---
# Amministratore Commerce in Adobe Unified Experience

L’amministratore di Commerce per Adobe Commerce as a Cloud Service si apre in Adobe Unified Experience quando selezioni un nome di istanza in Commerce Cloud Manager.

L’interfaccia di Adobe Unified Experience fornisce la navigazione superiore condivisa utilizzata tra i prodotti Adobe, una navigazione a sinistra aggiornata e uno stile di pagina amministratore aggiornato.

Puoi cambiare organizzazioni, prodotti e istanze di Commerce e accedere ad Aiuto, notifiche e preferenze account dalla navigazione in alto. Le autorizzazioni per il ruolo Commerce esistenti continuano a determinare a quali voci del menu Amministratore puoi accedere.

>[!NOTE]
>
>L’amministratore di Commerce in Adobe Unified Experience è disponibile solo per Adobe Commerce as a Cloud Service. I clienti Adobe Commerce on cloud infrastructure e Adobe Commerce on-premise continuano a utilizzare la [interfaccia utente classica dell&#39;amministratore di Commerce](admin.md).

![Dashboard di amministrazione di Commerce con navigazione superiore Unified Experience e navigazione sinistra Commerce](./assets/admin-unified-experience-overview.png){width="800" zoomable="yes" border="light"}

## Apri Commerce Admin.

Dopo aver effettuato l&#39;accesso ad [Adobe Experience Cloud](https://experience.adobe.com/){target="_blank"}, apri Commerce Cloud Manager. Quindi, seleziona un’istanza per aprire Admin in Unified Experience (Amministrazione in esperienza unificata).

Il flusso di accesso consente di spostarsi tra le istanze di Commerce senza accedere separatamente a ciascuna istanza.
Puoi passare dai prodotti Adobe alle istanze Commerce senza ulteriori richieste di accesso.

Per la procedura di accesso, vedere [Accedere a un&#39;istanza](https://experienceleague.adobe.com/it/docs/commerce/cloud-service/getting-started#access-an-instance){target="_blank"} nella _Guida di Adobe Commerce as a Cloud Service_.

>[!BEGINTABS]

>[!TAB Apri l&#39;amministratore da Commerce Cloud Manager]

![Apri l&#39;amministratore](./assets/admin-uex-seamless-login-cloud-manager-to-instance.png){width="800" zoomable="yes" border="light"}

>[!TAB Visualizza in azione]

![Apri l&#39;amministratore da Commerce Cloud Manager](./assets/admin-uex-seamless-login-cloud-manager-to-instance.gif){width="800" zoomable="yes" border="light"}

>[!ENDTABS]

### Scegli un’interfaccia amministratore {#classic-ui}

Per la versione iniziale dell’amministratore di Commerce in Unified Experience, Adobe Commerce as a Cloud Service supporta due esperienze amministratore di Commerce, Adobe Unified Experience e l’interfaccia classica.

Per impostazione predefinita, quando selezioni un’istanza di Commerce in Commerce Cloud Manager, l’amministratore di Commerce si apre in Adobe Unified Experience. Per tornare all’interfaccia classica, utilizza un segnalibro esistente o individua l’URL per l’interfaccia classica. Vedi [Apri interfaccia classica](#open-classic-ui).

I collegamenti per l’esperienza unificata e l’interfaccia utente classica sono disponibili nel pannello dei dettagli dell’istanza in Commerce Cloud Manager.

| Collegamento | Esperienza |
| --- | --- |
| **[!UICONTROL Admin URL (Unified Shell UI)]** | Apre Admin in Unified Experience (Amministrazione in esperienza unificata). |
| **[!UICONTROL Admin URL (Classic UI)]** | Apre la precedente interfaccia di amministrazione. |

![Illustrazione dei dettagli dell&#39;istanza di Commerce Cloud Manager che mostra i collegamenti all&#39;URL amministratore (interfaccia utente di Unified Shell) e all&#39;URL amministratore (interfaccia classica)](./assets/admin-unified-experience-cloud-manager-instance-details.png){width="800" zoomable="yes" border="light"}

_Illustrazione basata sulla schermata dell&#39;elenco delle istanze e sulla progettazione aggiornata dei dettagli delle istanze. Gli URL visualizzati utilizzano gli host di gestione temporanea._

#### Formati URL

| Esperienza | Schema URL |
| --- | --- |
| Esperienza unificata | `https://<experience-cloud-host>/#/@<organization>/in:<instance-id>/commerce/cloud-service/admin` |
| Interfaccia classica | `https://<commerce-admin-host>/<instance-id>/admin/` |

Unified Experience identifica l&#39;organizzazione dopo `@` e l&#39;istanza dopo `in:`. L’interfaccia classica inserisce l’ID istanza direttamente dopo il nome host.

Ad esempio, questi URL di staging aprono la stessa istanza:

- **Esperienza unificata**: `https://experience-stage.adobe.com/#/@adobe-commerce-uex/in:<instance-id>/commerce/cloud-service/admin`
- **Interfaccia classica**: `https://na1-stage.admin.commerce.adobe.com/<instance-id>/admin/`

Questi nomi host di staging non sono URL di produzione. Utilizza sempre i collegamenti delle istanze da Commerce Cloud Manager anziché costruire URL.

#### Apri interfaccia classica

Per aprire l’interfaccia classica:

- Utilizza un segnalibro o un URL Classic Admin esistente. Questi URL aprono solo l’interfaccia classica e non vengono reindirizzati a Unified Experience (Esperienza unificata).
- Selezionare **[!UICONTROL Admin URL (Classic UI)]** nei dettagli istanza di Commerce Cloud Manager.

L&#39;amministratore non dispone di un commutatore di interfaccia. Se necessario, utilizza Commerce Cloud Manager o un URL amministratore salvato per tornare all’interfaccia classica.

## Identificare l’organizzazione e l’istanza

Prima di apportare modifiche, controlla l’organizzazione e l’istanza in cui stai lavorando:

- Il menu dell’account mostra l’organizzazione corrente.
- Il commutatore di istanza nella navigazione superiore mostra il nome dell&#39;istanza e un badge **[!UICONTROL Production]** o **[!UICONTROL Sandbox]**.

Utilizza il badge ambiente per distinguere un’istanza di produzione da una sandbox quando passi da un’istanza all’altra.

## Cambiare organizzazioni, prodotti e istanze

La navigazione in alto fornisce controlli separati per cambiare il contesto di lavoro.

### Cambiare organizzazione

Utilizza il selettore organizzazione nella navigazione superiore per spostarti tra le organizzazioni a cui hai accesso.

1. Nella navigazione in alto, seleziona il nome dell’organizzazione.

1. Seleziona un’organizzazione dall’elenco.

   L’elenco mostra le organizzazioni a cui hai accesso. Un segno di spunta identifica l’organizzazione in cui si lavora.

>[!BEGINTABS]

>[!TAB Commutatore organizzazione]

![Commutatore organizzazione](./assets/admin-uex-org-switcher.png){width="800" zoomable="yes" border="light"}

>[!TAB Visualizza in azione]

![Commutatore organizzazione](./assets/admin-uex-org-switcher.gif){width="800" zoomable="yes" border="light"}

>[!ENDTABS]

Il menu Account mostra anche l’organizzazione in cui stai lavorando. Seleziona l&#39;immagine del tuo profilo (![Account](./assets/admin-unified-experience-icon-account.png){width="24"}) nella navigazione superiore, quindi controlla la riga **[!UICONTROL Organization]**.

![Menu dell&#39;account con l&#39;organizzazione corrente](./assets/admin-uex-account-menu-organization.png){width="800" zoomable="yes" border="light"}

Le istanze che è possibile aprire appartengono all&#39;organizzazione in cui si sta lavorando. Per modificare le istanze, vedere [Cambiare le istanze di Commerce](#switch-commerce-instances).

### Cambia prodotti

Utilizza il commutatore prodotto (![Commutatore prodotto](./assets/admin-unified-experience-icon-product-switcher.png){width="24"}) nella navigazione superiore per cambiare le applicazioni in qualsiasi momento. Funziona allo stesso modo di altri prodotti Adobe.

- **Admin Console**: apri Adobe Admin Console dal commutatore del prodotto per gestire gli utenti e il loro accesso (**[!UICONTROL Administer]** > **[!UICONTROL Users]**). Non è necessario ricordare l’URL. Adobe Admin Console è separato dall&#39;amministratore Commerce, dove gestisci il tuo store.
- **Adobe Exchange**: trova estensioni di terze parti, plug-in, script e integrazioni Enterprise in Adobe Creative Cloud, Adobe Experience Cloud e Adobe Document Cloud.
- **Altri prodotti**: apri prodotti come Coworker.

>[!BEGINTABS]

>[!TAB Menu del selettore prodotti]

![Menu del selettore prodotti](./assets/admin-uex-product-dropdown.png){width="800" zoomable="yes" border="light"}

>[!TAB Visualizza in azione]

![Menu del selettore prodotti](./assets/admin-uex-product-dropdown.gif){width="800" zoomable="yes" border="light"}

>[!ENDTABS]

Per la gestione degli utenti e dei ruoli di Adobe Commerce as a Cloud Service, consulta [Gestione utenti](https://experienceleague.adobe.com/it/docs/commerce/cloud-service/user-management){target="_blank"}.

### Cambia istanze Commerce

La navigazione superiore include un pulsante per cambiare istanza. Mostra sempre il badge **[!UICONTROL Production]** o **[!UICONTROL Sandbox]** e il nome dell&#39;istanza in cui ti trovi.

1. Nella navigazione in alto, seleziona il selettore di istanze che visualizza il nome dell’istanza corrente e il badge dell’ambiente.

1. Seleziona un’istanza dall’elenco.

   L’elenco contiene le istanze di Adobe Commerce as a Cloud Service a cui puoi accedere nell’organizzazione corrente. Non è necessario tornare a Commerce Cloud Manager per cambiare le istanze, in modo da poter spostarsi avanti e indietro tra le istanze.

1. Prima di continuare, controlla il nome dell’istanza e il badge dell’ambiente.

L’istanza fa parte dell’URL della pagina, quindi puoi aggiungere un segnalibro o condividere un collegamento che apre un’istanza specifica. Se apri l’amministratore senza un’istanza nel collegamento, viene caricata l’ultima istanza utilizzata.

## Utilizza il pannello di navigazione a sinistra

Il menu Amministratore di Commerce viene visualizzato nella barra di navigazione a sinistra di Adobe Unified Experience. Espandere o comprimere le sezioni di menu per trovare gli strumenti necessari oppure digitare per passare a una voce di menu.

Il menu è specifico per l’istanza in cui stai lavorando. Quando cambi istanza, la barra di navigazione a sinistra viene aggiornata di conseguenza.

Le autorizzazioni del ruolo esistenti vengono riportate. Vengono visualizzate solo le voci di menu consentite dal ruolo.

Continua a utilizzare la Guida per l’amministratore per attività quali la gestione di prodotti, ordini, clienti e configurazione. Le pagine amministratore hanno uno stile aggiornato, quindi il loro aspetto può differire dalle schermate dell’interfaccia classica in questa guida.

>[!BEGINTABS]

>[!TAB Navigazione sinistra amministratore Commerce]

![Navigazione sinistra amministratore Commerce](./assets/admin-uex-left-navigation.png){width="800" zoomable="yes" border="light"}

>[!TAB Visualizza in azione]

![Navigazione sinistra amministratore Commerce](./assets/admin-uex-left-navigation.gif){width="800" zoomable="yes" border="light"}

>[!ENDTABS]

## Ottieni aiuto e fornisci feedback

Per accedere alle risorse senza uscire dall&#39;amministratore di Commerce, apri il pannello della guida utilizzando l&#39;icona della guida (![icona Guida](./assets/admin-unified-experience-icon-help.png){width="24"}) nella navigazione superiore.

- **Guida**: cerca la documentazione in Adobe Experience League direttamente dal pannello.
- **Supporto**: accedi ai forum della community e ad altre risorse di apprendimento e trova il tuo ticket di supporto su Adobe Experience League.
- **Feedback**: invia feedback ad Adobe dallo stesso pannello.

Aiuto, supporto e feedback sono disponibili nel contesto. Rimani nel tuo Commerce Admin e non perdere il posto.

>[!BEGINTABS]

>[!TAB Pannello della Guida]

![Pannello della Guida](./assets/admin-uex-help-search.png){width="800" zoomable="yes" border="light"}

>[!TAB Visualizza in azione]

![Pannello della Guida](./assets/admin-uex-help-search.gif){width="800" zoomable="yes" border="light"}

>[!ENDTABS]

## Visualizza notifiche {#view-notifications}

Per visualizzare notifiche, richieste e annunci di prodotti nel contesto, apri il pannello delle notifiche utilizzando l&#39;icona a forma di campanello (![Notifiche](./assets/admin-unified-experience-icon-notifications.png){width="24"}) nella navigazione superiore.

Il pannello riunisce **[!UICONTROL Requests]**, **[!UICONTROL Notifications]** e **[!UICONTROL Announcements]** in un&#39;unica posizione. Non è necessario uscire dall’amministratore di Commerce per visualizzare uno di questi messaggi.

Utilizza l’icona a forma di campana nella navigazione superiore di Unified Experience per questo pannello, anziché il controllo di notifica all’interno dell’intestazione della pagina Commerce. Per istruzioni sui messaggi di posta in arrivo dell&#39;amministratore di Commerce, vedere [Posta in arrivo messaggio](admin-message-inbox.md).

>[!BEGINTABS]

>[!TAB Pannello Notifiche]

![Pannello Notifiche](./assets/admin-uex--notifications-bell.png){width="800" zoomable="yes" border="light"}

>[!TAB Visualizza in azione]

![Pannello Notifiche](./assets/admin-uex--notifications-bell.gif){width="800" zoomable="yes" border="light"}

>[!ENDTABS]

## Gestire le preferenze account

Seleziona l&#39;immagine del tuo profilo (![Account](./assets/admin-unified-experience-icon-account.png){width="24"}) nella navigazione superiore per aprire il menu dell&#39;account. Da questo menu puoi:

- Visualizzare l&#39;organizzazione in cui si sta lavorando.
- Attiva la modalità scura con l&#39;interruttore **[!UICONTROL Dark theme]**.
- Apri le preferenze utente.

>[!BEGINTABS]

>[!TAB Menu account con modalità scura]

![Menu account con modalità scura](./assets/admin-uex-dark-mode.png){width="800" zoomable="yes" border="light"}

>[!TAB Visualizza in azione]

![Menu account con modalità scura](./assets/admin-uex-dark-mode.gif){width="800" zoomable="yes" border="light"}

>[!ENDTABS]

## Stile pagina aggiornato

Le pagine dell’amministratore di Commerce hanno un aspetto aggiornato che corrisponde all’esperienza unificata di Adobe. Per le versioni successive è pianificato un ulteriore restyling.

>[!MORELIKETHIS]
>
>[Guida all&#39;amministrazione e all&#39;interfaccia di Adobe CX Enterprise](https://experienceleague.adobe.com/it/docs/core-services/interface/experience-cloud)
