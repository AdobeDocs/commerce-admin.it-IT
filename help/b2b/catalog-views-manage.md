---
title: Gestisci configurazione vista catalogo
description: Scopri come rivedere le viste di catalogo Adobe Commerce Optimizer create per i cataloghi condivisi B2B e assegnare le chiavi di accesso con restrizioni che li proteggono.
feature: B2B, Companies, Catalog Management
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: f9f21f675d5c608547db790f33d1aa9be90a36eb
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%
---
# Gestire la configurazione della vista catalogo

Con l&#39;estensione [!DNL Adobe Commerce Optimizer Connector for B2B] installata, nella pagina Visualizzazioni catalogo sono elencate le [!DNL Adobe Commerce Optimizer] [proiezioni della visualizzazione catalogo](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"} create per il catalogo condiviso personalizzato.  Una _proiezione_ è la visualizzazione catalogo creata quando il connettore sincronizza i dati del catalogo condiviso con [!DNL Adobe Commerce Optimizer]. Il connettore crea una proiezione separata per ogni visualizzazione store nel catalogo condiviso, in modo che un catalogo condiviso possa avere più visualizzazioni catalogo. Nelle esperienze storefront, queste visualizzazioni catalogo sono accessibili solo alle aziende assegnate al catalogo condiviso associato.

Supponiamo ad esempio che Acme Industrial sia assegnata a un catalogo condiviso, EU Business, che appartiene al sito web dell’UE. Il sito web presenta due visualizzazioni dello store:

- `English (UK)`

- `German (Germany)`

Il connettore proietta il catalogo condiviso in due [!DNL Adobe Commerce Optimizer] visualizzazioni catalogo:

- `EU Business – English (UK)`

- `EU Business – German (Germany)`

L&#39;azienda dispone di visualizzazioni catalogo in inglese e tedesco, ma solo di un&#39;assegnazione catalogo condivisa. Ogni vista store visualizza i dati dalla vista catalogo corrispondente.

Entrambe le visualizzazioni catalogo possono condividere lo stesso listino prezzi quando utilizzano lo stesso sito Web e lo stesso ambito di determinazione prezzi per gruppo di clienti.

## Autenticazione visualizzazione catalogo

Il connettore protegge le visualizzazioni del catalogo con tasti di accesso limitato. Adobe Commerce utilizza la chiave privata per firmare un token di accesso per un acquirente autorizzato. Prima di restituire i dati del catalogo protetto, [!DNL Adobe Commerce Optimizer] convalida il token in base alla chiave pubblica corrispondente associata alla visualizzazione del catalogo richiesta.

Per configurare la durata del token o disabilitare il rilascio del token, vedi [Servizi > Visualizzazione catalogo ACO](/help/configuration-reference/services/aco-catalog-view.md).

È possibile esaminare queste visualizzazioni catalogo e gestire le chiavi assegnate dalla scheda _[!UICONTROL Catalog Views]_del catalogo condiviso o dalla sezione_[!UICONTROL Catalog Views]_ della società associata. Entrambi elencano le stesse visualizzazioni catalogo e le assegnazioni chiave correnti. Vedere [Modifica chiavi di accesso con restrizioni](#edit-restricted-access-keys) per l&#39;esatto percorso di navigazione da ogni posizione.

Per monitorare la sincronizzazione dei dati del catalogo condiviso con [!DNL Adobe Commerce Optimizer], vedere [Monitoraggio dello stato di sincronizzazione della visualizzazione del catalogo](/help/systems/catalog-view-sync-status.md).

## Riferimento visualizzazioni catalogo

{{$include /help/_includes/catalog-views-reference-table.md}}

## Modifica chiavi di accesso con restrizioni

{{$include /help/_includes/edit-restricted-access-keys.md}}

Per ulteriori dettagli, vedere [Gestire le chiavi di accesso con restrizioni](/help/systems/restricted-access-keys.md).

>[!MORELIKETHIS]
>
> - [Proiezione catalogo condiviso B2B](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}
> - [Servizi > Visualizzazione catalogo ACO](/help/configuration-reference/services/aco-catalog-view.md)
> - [Monitoraggio stato sincronizzazione visualizzazione catalogo](/help/systems/catalog-view-sync-status.md)
> - [Gestione dei cataloghi condivisi](catalog-shared-manage.md)
> - [Gestisci account società](account-company-manage.md)
