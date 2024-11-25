---
title: '[!DNL AR Viewer] per Adobe Commerce'
description: Scopri i vantaggi che  [!DNL AR Viewer]  può offrire alla tua istanza di Adobe Commerce e come integrare e configurare correttamente l'estensione.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# [!DNL AR Viewer] per Adobe Commerce

La realtà aumentata (AR) descrive le esperienze degli utenti che aggiungono elementi 2D o 3D alla vista dal vivo dalla fotocamera di un dispositivo in modo tale che questi elementi sembrano abitare il mondo reale.

L&#39;estensione [!DNL AR Viewer] per Adobe Commerce offre all&#39;utente un&#39;esperienza perfetta progettata per visualizzare immagini 3D sottoposte a rendering.

Le informazioni contenute in questa guida forniscono una panoramica dell&#39;esperienza di onboarding per [!DNL AR Viewer] in Adobe Commerce e dei vantaggi che [!DNL AR Viewer] offre all&#39;utente, nonché delle best practice da seguire in tale percorso.

Sviluppato da Pixar, [Universal Scene Description (USD)](https://openusd.org/release/index.html){target=_blank} è il primo software open-source in grado di interscambiare in modo robusto e scalabile scene 3D che possono essere composte da molte risorse, sorgenti e animazioni diverse, promuovendo al contempo flussi di lavoro altamente collaborativi. Questo USD viene utilizzato all&#39;interno di `.USDZ` file. Questo file `.USDZ` distribuisce contenuto AR e 3D ai dispositivi dell&#39;utente.

>[!NOTE]
>
> [!DNL AR Viewer] supporta solo `.USDZ` file.

## [!DNL AR Viewer] requisiti

[!DNL AR Viewer] è compatibile con [!DNL Magento Open Source] e Adobe Commerce. Per ulteriori informazioni sulle versioni supportate, vedere [Criteri del ciclo di vita](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank}.

Per ulteriori informazioni, vedere [Installare l&#39;estensione [!DNL AR Viewer] extension](../catalog/ar-viewer-setup.md).

Per utilizzare [!DNL AR Viewer], è necessario disporre dei seguenti elementi per l&#39;istanza:

* PHP 8.1.0
* Adobe Commerce versione 2.4.4 e successive
* Magento Open Source (CE) versione 2.4.x

## Limiti di compatibilità

[!DNL AR Viewer] limitazioni di compatibilità esistenti:

* Solo `.USDZ`: questa funzionalità supporta solo `.USDZ` file.
* `qr-code`: richiede `endroid/qr-code` versione 4.5.
* `Catalog module`: richiede `magento/module-catalog` versione 104.0.0.
