---
title: Gestire le chiavi di accesso con restrizioni in Commerce
description: Creare, assegnare ed eliminare le chiavi di accesso con restrizioni che proteggono le viste di catalogo condivise B2B sincronizzate con Adobe Commerce Optimizer.
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 0%
---

# Gestire le chiavi di accesso con restrizioni

Utilizzare la pagina Chiavi di accesso limitate per gestire le chiavi di accesso per le visualizzazioni di catalogo privato create da [!DNL Adobe Commerce Optimizer Connector for B2B]. Il connettore sincronizza le configurazioni del catalogo condiviso B2B da Adobe Commerce a Adobe Commerce Optimizer.

>[!NOTE]
>
>Per le chiavi create manualmente e utilizzate per gestire cataloghi privati in scenari non B2B, ad esempio portali partner, gestire le chiavi da [[!DNL Adobe Commerce Optimizer Studio]](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"}.

## Pubblico e disponibilità {#audience}

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud Infrastructure e on-premise."}

La pagina [!UICONTROL Restricted Access Keys] è disponibile per i commercianti Adobe Commerce on Cloud Infrastructure e on-premise che utilizzano cataloghi condivisi B2B con [!DNL Adobe Commerce Optimizer Connector for B2B]. Il connettore installa e abilita automaticamente la pagina.

Quando si crea una vista catalogo per un catalogo condiviso, il connettore genera e assegna automaticamente un tasto. Utilizzare questa pagina per visualizzare tale chiave e per creare, assegnare o eliminare chiavi aggiuntive.

## Accedere alla pagina Chiavi di accesso limitate {#access-restricted-access-keys-page}

Dall&#39;area di amministrazione, passare a **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Restricted Access Keys]**.

![Chiavi di accesso con restrizioni pagina elenco chiavi e relative viste catalogo assegnate](assets/restricted-access-keys.png){width="600" zoomable="yes"}

Questa pagina elenca tutte le chiavi, a prescindere dal fatto che siano assegnate a una vista catalogo. Per assegnare una chiave a una visualizzazione catalogo specifica, utilizzare l&#39;azione [!UICONTROL Edit Restricted Access Keys] in tale visualizzazione catalogo. Vedi [Assegnare le chiavi a una visualizzazione catalogo](#assign-keys-to-a-catalog-view).

## Riepilogo chiavi di accesso limitate {#restricted-access-keys-summary}

La griglia contiene una chiave per riga.

| Campo | Descrizione |
| --- | --- |
| **ID chiave** | L’identificatore di chiave univoco. |
| **Titolo** | Etichetta fornita per identificare la chiave. |
| **Visualizzazioni catalogo assegnate** | Visualizzazioni di catalogo a cui è attualmente assegnata questa chiave. |
| **Scade Alle** | La data di scadenza della chiave. |
| **Azioni** | Azioni a livello di riga. Vedi [Gestione chiavi](#manage-keys). |

## Gestione chiavi {#manage-keys}

- **[!UICONTROL Create Key]** - Genera una nuova coppia di chiavi non assegnata. Commerce genera la coppia di chiavi e memorizza la chiave privata. La chiave pubblica non viene registrata con [!DNL Adobe Commerce Optimizer] finché non si assegna la chiave a una visualizzazione catalogo.
- **[!UICONTROL View Public Key]** - Apre una visualizzazione di sola lettura della chiave pubblica, in modo da poterla copiare per registrare di nuovo o sincronizzare di nuovo la chiave, se necessario. La chiave privata non viene mai visualizzata.
- **[!UICONTROL Delete]** - Rimuove la chiave e ne revoca la registrazione remota in [!DNL Adobe Commerce Optimizer]. I token Storefront già rilasciati con questa chiave rimangono validi fino alla scadenza. Questa azione non può essere annullata.

>[!NOTE]
>
>Una chiave scaduta può essere eliminata solo. Impossibile assegnare o annullare l&#39;assegnazione di una chiave scaduta.

## Creare una chiave

Nella pagina [!UICONTROL Restricted Access Keys], creare una chiave selezionando **[!UICONTROL Create Key]**.

Commerce genera una nuova coppia di chiavi e memorizza la chiave privata. La tabella Chiavi di accesso con restrizioni viene aggiornata con una nuova voce di chiave che mostra l&#39;ID di chiave univoco. Utilizzare [!UICONTROL Key ID] quando si assegna la chiave a una visualizzazione catalogo.

La chiave pubblica non è registrata con [!DNL Adobe Commerce Optimizer] finché non viene assegnata a una visualizzazione catalogo. Dopo la registrazione, la voce della tabella Chiavi di accesso con restrizioni viene aggiornata per mostrare l&#39;assegnazione del catalogo e la data di scadenza.

## Assegnare o rimuovere le chiavi di accesso con restrizioni {#assign-keys-to-a-catalog-view}

{{$include /help/_includes/edit-restricted-access-keys.md}}

## Selezione dei tasti e rotazione {#key-selection-and-rotation}

Quando a una visualizzazione catalogo vengono assegnate più chiavi, [!DNL Adobe Commerce] utilizza automaticamente la chiave non scaduta assegnata con la data di scadenza più recente per firmare i token.

>[!IMPORTANT]
>
>La rotazione automatica dei tasti non è ancora disponibile. Le chiavi hanno per impostazione predefinita un periodo di scadenza lungo. Per ruotare manualmente una chiave, creane una nuova, assegnala alla vista catalogo insieme a quella esistente. Dopo aver verificato che la nuova chiave è in uso, elimina la chiave precedente.

Per modificare il periodo di scadenza predefinito applicato alle chiavi appena create, passare a **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Restricted Access Keys]** > **[!UICONTROL Provisioning]** > **[!UICONTROL Default key lifetime (days)]**. Consulta [Servizi > Chiavi di accesso con restrizioni ACO](../configuration-reference/services/aco-restricted-access-keys.md).

## Limitazioni note {#known-limitations}

- Nessun indicatore di stato attivo o attivo nella griglia principale [!UICONTROL Restricted Access Keys].

  È possibile visualizzare lo stato del collegamento nella pagina [!UICONTROL Edit Restricted Access Keys]. Utilizza il menu a discesa per visualizzare le chiavi disponibili e il loro stato. Se a una vista catalogo viene assegnata una chiave, questa viene collegata. Se non è assegnato, non ha uno stato. Puoi assegnare tali chiavi alla vista catalogo che stai modificando.

  Nella pagina [!UICONTROL Catalog View Sync Status] è possibile visualizzare le chiavi collegate a una visualizzazione catalogo dalla pagina dei dettagli della visualizzazione catalogo (azione **[!UICONTROL View details]**). La pagina dei dettagli mostra anche la cronologia delle chiavi, compreso il momento in cui è stata assegnata o revocata l’assegnazione dalla vista catalogo.

- La rotazione automatica dei tasti non è ancora disponibile.

>[!MORELIKETHIS]
>
> - [Gestisci configurazione visualizzazione catalogo](/help/b2b/catalog-views-manage.md) — Assegna queste chiavi dall&#39;account condiviso del catalogo o dell&#39;azienda
> - [Monitoraggio dello stato di sincronizzazione della visualizzazione del catalogo](catalog-view-sync-status.md) — Controlla e riconcilia le visualizzazioni del catalogo protette da queste chiavi
> - [Servizi > Chiavi di accesso con restrizioni ACO](../configuration-reference/services/aco-restricted-access-keys.md) — Configura il periodo di scadenza della chiave predefinita
> - [Servizi > Visualizzazione catalogo ACO](../configuration-reference/services/aco-catalog-view.md) — Configura la durata del token di accesso della vetrina e abilita o disabilita la pubblicazione
> - [Gestire le chiavi di accesso con restrizioni](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/restricted-access-keys){target="_blank"} nella *Guida di Adobe Commerce Optimizer Connector*: scopri come queste chiavi si adattano alla sincronizzazione di cataloghi condivisi B2B
> - [Chiavi di accesso limitate](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} nella *Guida di Adobe Commerce Optimizer*: il flusso di chiavi manuale basato su ACO Studio per i casi di utilizzo non B2B
