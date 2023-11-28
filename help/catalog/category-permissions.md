---
title: Autorizzazioni categoria
description: Scopri come utilizzare le categorie per controllare la visualizzazione dei prezzi dei prodotti, determinare quali gruppi di clienti possono aggiungere prodotti al carrello e specificare la pagina di destinazione.
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# Autorizzazioni categoria

{{ee-feature}}

L’accesso alle categorie può essere limitato a specifici gruppi di clienti o limitato completamente. Puoi controllare la visualizzazione dei prezzi dei prodotti, determinare quali gruppi di clienti possono aggiungere prodotti al carrello e specificare la pagina di destinazione.

>[!NOTE]
>
>Le autorizzazioni per categoria hanno un ambito globale e, se abilitate, limitano l’accesso a ogni categoria in base alle singole autorizzazioni. Per impostazione predefinita, le autorizzazioni per le categorie non sono abilitate.

Ad esempio, se vendi solo a clienti grossisti, puoi consentire a chiunque di sfogliare il catalogo, ma visualizzare i prezzi e consentire gli acquisti solo per gli acquirenti nel _Commercio all&#39;ingrosso_ gruppo di clienti. Nell’esempio seguente, solo gli utenti connessi hanno accesso alla categoria &quot;Raccolte&quot;. Per gli ospiti, l&#39;opzione &quot;Raccolte&quot; non viene visualizzata nel menu principale.

![Utenti connessi Vedere la categoria &quot;Raccolte&quot;](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

Quando questa opzione è attivata, viene _[!UICONTROL Category Permissions]_nella pagina Categoria, che consente di applicare l&#39;accesso necessario per ogni categoria. Puoi aggiungere più regole di autorizzazione a ogni categoria per diversi siti web e gruppi di clienti.

## Passaggio 1: configurare le autorizzazioni per le categorie

>[!IMPORTANT]
>
>Tutti gli esistenti [impostazioni delle autorizzazioni del gruppo](../configuration-reference/catalog/catalog.md#category-permissions) vengono ignorati da **_tutto_** categorie nel catalogo quando **_[!UICONTROL Shared Catalog]_** la funzione è abilitata. [!UICONTROL Shared Catalog] controlla completamente tutte le autorizzazioni di categoria nel catalogo quando questo è abilitato.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Category Permissions]** sezione.

   ![Autorizzazioni categoria](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedi [Autorizzazioni categoria](../configuration-reference/catalog/catalog.md#category-permissions) nel _Riferimento configurazione_.

1. Imposta **[!UICONTROL Enable]** a `Yes`.

1. Completa le altre opzioni in base a ciò che desideri consentire o limitare sul tuo store (vedi le sezioni seguenti).

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando viene richiesto di aggiornare la cache, fare clic su **[!UICONTROL Cache Management]** nel messaggio di sistema e seguire le istruzioni per aggiornare la cache.

### [!UICONTROL Allow Browsing Category]

Questa opzione si applica a tutte le categorie in [sito web](../getting-started/websites-stores-views.md).

Per consentire ai membri di un **_gruppo di clienti specifico_** per sfogliare i prodotti delle categorie, effettuare le seguenti operazioni:

1. Imposta **[!UICONTROL Allow Browsing Category]** a `Specified Customer Groups`.

1. In **[!UICONTROL Customer Groups]** selezionare ogni gruppo a cui è consentito sfogliare i prodotti della categoria.

   Per selezionare più gruppi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) mentre si fa clic su ogni gruppo.

   ![Consenti navigazione per gruppo di clienti all’ingrosso](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

A **_limitare l’accesso e il reindirizzamento a una pagina di destinazione_**, eseguire le operazioni seguenti:

1. Imposta **[!UICONTROL Allow Browsing Category]** a `No, Redirect to Landing Page`.

1. Scegli la **[!UICONTROL Landing Page]** dove i visitatori vengono reindirizzati.

   ![Reindirizza alla home page](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Anche se il _[!UICONTROL Allow Browsing Category]_si applica a tutte le categorie del sito web, puoi configurare una pagina di destinazione diversa per ogni visualizzazione store.

### [!UICONTROL Display Product Prices]

Questa opzione si applica a tutte le categorie in [sito web](../getting-started/websites-stores-views.md).

Per consentire solo i membri di **_gruppi di clienti specifici_** per visualizzare il prezzo dei prodotti della categoria, eseguire le operazioni seguenti:

1. Imposta **[!UICONTROL Display Product Prices]** a `Yes, for Specified Customer Groups`.

1. In **[!UICONTROL Customer Groups]** selezionare ogni gruppo che può visualizzare il prezzo dei prodotti della categoria.

   Per selezionare più gruppi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) mentre si fa clic su ogni gruppo.)

   ![Solo il gruppo di clienti all’ingrosso può vedere i prezzi](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

Questa opzione si applica a tutte le categorie in [sito web](../getting-started/websites-stores-views.md).

Per consentire solo i membri di **_gruppi di clienti specifici_** per inserire prodotti di categoria nel carrello, eseguire le operazioni seguenti:

1. Imposta **[!UICONTROL Allow Adding to Cart]** a `Yes, for Specified Customer Groups`.

1. In **[!UICONTROL Customer Groups]** selezionare ogni gruppo che può aggiungere prodotti della categoria al carrello.

   Per selezionare più gruppi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) mentre si fa clic su ogni gruppo.

   ![Solo il gruppo di clienti all’ingrosso può mettere il prodotto nel carrello](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

Imposta questa opzione per impedire ai membri di un gruppo di clienti specifico di utilizzare la funzione Ricerca nel catalogo. Si applica a tutte le categorie [sito web](../getting-started/websites-stores-views.md).

- Per consentire **_solo clienti connessi_** per utilizzare Ricerca nel catalogo, seleziona `NOT LOGGED IN`.

- Per consentire **_solo gruppi di clienti specifici_** per utilizzare Ricerca nel catalogo, seleziona ogni gruppo da escludere dall’utilizzo di Ricerca per categoria.

  Per selezionare più gruppi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) mentre si fa clic su ogni gruppo.

  ![Ricerca nel catalogo non consentita per gruppo clienti generale](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## Passaggio 2: applicare le autorizzazioni per le categorie

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Nell&#39;albero delle categorie selezionare la categoria di destinazione.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** sulla pagina ed eseguire le operazioni seguenti:

   - Per creare una regola di autorizzazioni, fai clic su **[!UICONTROL New Permission]**.

     ![Sezione Autorizzazioni categoria](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - Scegli la applicabile **[!UICONTROL Website]** e **[!UICONTROL Customer Group]**.

   - Imposta le singole autorizzazioni in base alle esigenze.

   >[!NOTE]
   >
   >Quando `Browsing Category` = `Deny` è impostata l&#39;autorizzazione per qualsiasi categoria padre, non viene visualizzata nella [Breadcrumb Trail](navigation-breadcrumb-trail.md) nella pagina categoria figlio.

1. Al termine, fai clic su **[!UICONTROL Save]**.

>[!NOTE]
>
>Se presente **_Consenti_** autorizzazioni impostate per `Root Category`, quindi queste autorizzazioni vengono applicate automaticamente a tutte le sottocategorie e a tutti i prodotti all&#39;interno del `Catalog`. Se un prodotto è assegnato a più categorie e dispone di **_Consenti_** per almeno una categoria, ha automaticamente lo stesso **_Consenti_** autorizzazioni per tutte le categorie assegnate.
