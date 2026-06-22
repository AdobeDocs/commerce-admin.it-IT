---
title: '[!DNL AR Viewer] per Adobe Commerce'
description: Scopri i vantaggi che  [!DNL AR Viewer]  può offrire alla tua istanza di Adobe Commerce e come integrare e configurare correttamente l'estensione.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
TQID: https://experienceleague.adobe.com/ofebqdDS0exPDKJMLB-mpE0eVjRKT5ck91Fm2-7CVjA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# [!DNL AR Viewer] per Adobe Commerce

La realtà aumentata (AR) descrive le esperienze degli utenti che aggiungono elementi 2D o 3D alla vista dal vivo dalla fotocamera di un dispositivo in modo tale che questi elementi sembrano abitare il mondo reale.

L&#39;estensione [!DNL AR Viewer] per Adobe Commerce offre all&#39;utente un&#39;esperienza perfetta progettata per visualizzare immagini 3D sottoposte a rendering.

Le informazioni contenute in questa guida forniscono una panoramica dell&#39;esperienza di onboarding per [!DNL AR Viewer] in Adobe Commerce e dei vantaggi che [!DNL AR Viewer] offre all&#39;utente, nonché delle best practice da seguire in tale percorso.

Sviluppato da Pixar, [Universal Scene Description (USD)](https://openusd.org/release/index.html){target=_blank} è il primo software open-source in grado di interscambiare in modo robusto e scalabile scene 3D che possono essere composte da numerose risorse, origini e animazioni diverse, promuovendo al contempo flussi di lavoro altamente collaborativi. Questo USD viene utilizzato all&#39;interno di `.USDZ` file. Questo file `.USDZ` distribuisce contenuto AR e 3D ai dispositivi dell&#39;utente.

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

