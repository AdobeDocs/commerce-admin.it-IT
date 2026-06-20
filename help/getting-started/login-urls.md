---
title: Credenziali di accesso e URL
description: Scopri gli URL di Commerce e le credenziali dell’account utilizzati per accedere all’amministratore e alla vetrina.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
TQID: https://experienceleague.adobe.com/8IGacP581jwpVtFnCFXRrG5vuIwCJaAUnbliitMHuf8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: d41d3a54-9721-475c-abd6-295bebfba9e4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 373
ht-degree: 0%

---

# Credenziali di accesso e URL

Prima di procedere con la configurazione e la configurazione, assicurati di disporre delle informazioni necessarie per accedere all’amministratore del tuo store e al tuo account Commerce.

## URL vetrina

L&#39;indirizzo per [storefront](storefront.md) è in genere il dominio assegnato al tuo indirizzo IP. Alcuni archivi vengono installati nella directory principale o nella directory più in alto. Altri vengono installati in una directory sotto la radice. L’archivio potrebbe trovarsi all’interno di un sottodominio associato a un dominio primario. L&#39;URL del tuo archivio potrebbe essere simile a uno dei seguenti:

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx` s

Se non disponi ancora di un dominio, l&#39;URL dello store include una serie di quattro numeri, ciascuno separato da un punto nella notazione _dotted quad_.

## URL amministratore

L&#39;indirizzo dell&#39;archivio [Admin](admin.md) è configurato durante l&#39;installazione. L&#39;indirizzo predefinito è lo stesso del tuo archivio, ma con `/admin` alla fine. Sebbene gli esempi in questa guida utilizzino la directory predefinita, è consigliabile eseguire l’amministratore da una posizione univoca dell’archivio.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## Account [!DNL Commerce]

Il tuo account [Commerce](commerce-account-create.md) ti consente di accedere a informazioni su prodotti e servizi, impostazioni account, cronologia di fatturazione e risorse di supporto. Per accedere al tuo account, vai al sito principale di Commerce e fai clic su **[!UICONTROL My Account]** in alto a destra.

## Account cliente

Mentre stai apprendendo a spostarti all&#39;interno del negozio, assicurati di impostare un [account cliente](../customers/account-dashboard.md) di prova, in modo da poter sperimentare il processo di archiviazione e pagamento dal punto di vista del cliente.

## Dati di esempio

[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."}

Adobe fornisce un set di dati di esempio che include un archivio di campioni con più di 250 prodotti (di cui circa 200 configurabili), categorie, regole di prezzo promozionali, pagine CMS, banner e così via. I dati di esempio utilizzano il tema _Luma_ nella vetrina. [L&#39;installazione di questi dati di esempio](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html?lang=it) è facoltativa, ma può essere utile per testare e sviluppare personalizzazioni per le attività di eCommerce.
