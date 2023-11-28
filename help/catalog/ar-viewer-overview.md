---
title: '[!DNL AR Viewer] per Adobe Commerce'
description: Scopri come [!DNL AR Viewer] potrebbero trarre vantaggio dalla tua istanza di Adobe Commerce e da come integrare e configurare correttamente l’estensione.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!DNL AR Viewer] per Adobe Commerce

La realtà aumentata (AR) descrive le esperienze degli utenti che aggiungono elementi 2D o 3D alla vista dal vivo dalla fotocamera di un dispositivo in modo tale che questi elementi sembrano abitare il mondo reale.

Il [!DNL AR Viewer] per Adobe Commerce, l’estensione offre all’utente un’esperienza fluida progettata per visualizzare immagini 3D di rendering.

Le informazioni contenute in questa guida forniscono una panoramica dell’esperienza di onboarding per [!DNL AR Viewer] in Adobe Commerce e come [!DNL AR Viewer] offre vantaggi all’utente, nonché best practice da seguire lungo tale percorso.

Sviluppato da Pixar, [Descrizione scena universale (USD)](https://www.pixar.com/usd){target=_blank} è il primo software open-source in grado di intercambiare in modo solido e scalabile scene 3D che possono essere composte da molte risorse, sorgenti e animazioni diverse, promuovendo al contempo flussi di lavoro altamente collaborativi. Questo USD viene utilizzato in `.USDZ` file. Questo `.USDZ` consente di distribuire contenuti AR e 3D ai dispositivi dell&#39;utente.

>[!NOTE]
>
> Il [!DNL AR Viewer] supporta solo `.USDZ` file.

## [!DNL AR Viewer] requisiti

Il [!DNL AR Viewer] è compatibile con entrambi [!DNL Magento Open Source] e Adobe Commerce. Consulta [Ciclo di vita](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} per ulteriori informazioni sulle versioni supportate.

Consulta [Installare [!DNL AR Viewer] estensione](../catalog/ar-viewer-setup.md) per ulteriori informazioni.

Per utilizzare [!DNL AR Viewer], per la tua istanza devi disporre dei seguenti elementi:

* PHP 8.1.0
* Adobe Commerce versione 2.4.4 e successive
* Magento Open Source (CE) versione 2.4.x

## Limiti di compatibilità

[!DNL AR Viewer] limitazioni di compatibilità esistenti:

* `.USDZ` Solo per: questa funzione supporta solo `.USDZ` file.
* `qr-code`: Richiede `endroid/qr-code` versione 4.5.
* `Catalog module`: Richiede `magento/module-catalog` versione 104.0.0.
