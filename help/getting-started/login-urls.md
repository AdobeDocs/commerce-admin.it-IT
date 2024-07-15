---
title: Credenziali di accesso e URL
description: Scopri gli URL di Commerce e le credenziali dell’account utilizzati per accedere all’amministratore e alla vetrina.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '334'
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

In Adobe viene fornito un set di dati di esempio che include un archivio di campioni con più di 250 prodotti (di cui circa 200 configurabili), categorie, regole di prezzo promozionali, pagine CMS, banner e così via. I dati di esempio utilizzano il tema _Luma_ nella vetrina. [L&#39;installazione di questi dati di esempio](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) è facoltativa, ma può essere utile per testare e sviluppare personalizzazioni per le attività di eCommerce.
