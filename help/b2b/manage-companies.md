---
title: Gestione società
description: Amministrazione e gestione semplificate delle organizzazioni B2B con modelli operativi complessi.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Gestione società

La gestione aziendale in Adobe Commerce fornisce agli amministratori strumenti completi per organizzare, configurare e supervisionare le relazioni aziendali B2B. Questa funzione è essenziale per le aziende che lavorano con più clienti aziendali, filiali o strutture organizzative complesse.

La gestione aziendale consente di:

* **Organizza relazioni commerciali**: crea e gestisci account aziendali individuali per i clienti B2B
* **Creare gerarchie organizzative**: strutturare le relazioni padre-figlio che rispecchiano le organizzazioni aziendali reali
* **Amministrazione centralizzata**: gestione di più società e delle relative impostazioni da un&#39;unica interfaccia amministrativa
* **Operazioni semplificate**: applicazione di configurazioni e criteri coerenti tra società correlate
* **Supporto di strutture complesse**: gestione di filiali, franchising, attività multisito e divisioni aziendali

Gli utenti amministratori possono creare una gerarchia di società per rispecchiare un’organizzazione B2B assegnando le società a una società madre designata. Questa assegnazione consente all&#39;amministratore della società madre di visualizzare e gestire le società all&#39;interno dell&#39;organizzazione.

Avvia le attività di gestione società dalla visualizzazione *[!UICONTROL Companies]*. Dall&#39;amministratore, passa a **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Griglia gestione società B2B](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Prerequisiti

Prima di gestire le aziende, assicurati che:

* Le funzioni B2B sono abilitate nell’installazione di Adobe Commerce
* Si dispone dell&#39;accesso amministrativo con le autorizzazioni di gestione della società
* Gli account aziendali sono configurati correttamente con le informazioni aziendali necessarie
* I ruoli utente e le autorizzazioni vengono definiti per gli amministratori e gli utenti della società

## Casi d’uso

La gestione aziendale è ideale per:

* **Aziende con più sedi** con centralizzazione degli acquisti ma esigenze specifiche della sede
* **Operazioni di affiliazione** che richiedono supervisione aziendale e autonomia locale
* **Società affiliate** con criteri condivisi ma operazioni indipendenti
* **Grandi aziende** con più divisioni o unità aziendali
* **Reti di distribuzione** con rivenditori, rivenditori o partner di canale

## Informazioni sulla gerarchia e sui tipi di società

La gerarchia aziendale struttura le relazioni commerciali organizzando più società sotto un&#39;unica società madre. Questa funzione rispecchia le strutture organizzative del mondo reale, consentendo al contempo la gestione centralizzata e preservando le identità delle singole aziende.

### Tipi di società

La colonna *[!UICONTROL Company Type]* nella griglia Aziende mostra il modo in cui ogni società si inserisce all&#39;interno dell&#39;organizzazione B2B:

* **Principale** - Hub centrale con una o più società assegnate
   * Controlla più società figlie ma non può essere assegnato a un altro padre
   * **Caso d&#39;uso**: sede centrale, organizzazione principale di affiliazione o società holding

* **Figlio**—Società assegnata a un&#39;organizzazione padre
   * Funziona secondo la governance principale e può ereditare le configurazioni
   * Può appartenere a un solo elemento padre alla volta
   * **Caso d&#39;uso**: filiali, sedi in franchising o divisioni regionali

* **Società**—Società singola indipendente
   * Funziona indipendentemente senza relazioni gerarchiche
   * Può essere convertito in padre (assegnando società) o figlio (assegnando a padre)
   * **Caso d&#39;uso**: singoli clienti aziendali o client autonomi

### Conversione di tipi di società

* **Società singola → padre**. Assegnare altre società
* **Società singola → figlio**. Assegnarla a una società padre esistente
* **Singolo → figlio** - Annulla l&#39;assegnazione della società figlio dal padre
* **Padre → Figlio**. Impossibile rimuovere prima tutte le società assegnate

### Gestione delle gerarchie aziendali

Quando si modificano società all&#39;interno di una gerarchia, espandere *[!UICONTROL Company Hierarchy]* per visualizzare tutte le società correlate. Un flag `Current` indica la società in fase di modifica.

![Griglia gerarchia società B2B](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

Per istruzioni dettagliate, consulta [Gestire la gerarchia aziendale](manage-company-hierarchy.md).

## Attività di gestione società

Durante la gestione delle società dalla griglia società, gli amministratori possono eseguire le attività seguenti dalla griglia *[!UICONTROL Company Hierarchy]*:

* **Visualizza e gestisci relazioni aziendali**
   * **Visualizza società associate**—Visualizza tutte le società collegate a un&#39;organizzazione padre in un&#39;unica vista centralizzata
   * **Monitora stato società** - Tieni traccia delle società attive, in sospeso e inattive all&#39;interno della gerarchia
   * **Accedi ai dettagli della società**—Passa direttamente alle singole pagine di configurazione della società

* **Creare e modificare gerarchie**
   * **Assegna società** - Aggiungi società esistenti a un&#39;organizzazione padre dalla pagina dei dettagli della società
   * **Creare relazioni padre-figlio**: strutturare le società in modo che riflettano le relazioni commerciali reali
   * **Riorganizza strutture**—Sposta le aziende tra organizzazioni padre diverse in base alle esigenze aziendali.

* **Gestione della configurazione in blocco**
   * **Applica impostazioni tra società**—Aggiorna impostazioni avanzate per più società contemporaneamente utilizzando il controllo [!UICONTROL Actions] nella griglia società
   * **Standardizzare le configurazioni**: garantire la coerenza dei criteri tra le organizzazioni correlate
   * **Sovrascrivi singole impostazioni** - Invia le configurazioni della società padre alle società figlio selezionate

* **Azioni amministrative**
   * **Rimuovi relazioni aziendali**. Utilizzare l&#39;azione *[!UICONTROL Unassign from parent]* per sciogliere le relazioni organizzative
   * **Gestisci l&#39;accesso alla società**: controlla quali amministratori possono visualizzare e modificare le relazioni aziendali
   * **Monitorare le modifiche alla gerarchia**—Tenere traccia delle modifiche alle strutture organizzative

## Best practice

Quando gestisci le aziende, considera le seguenti best practice:

* **Creazione di gerarchie aziendali**: durante la gestione di strutture aziendali complesse, pianifica la gerarchia in modo che corrisponda alle relazioni aziendali reali, mantenendo al contempo le strutture semplici per evitare confusione da parte degli utenti. Documenta tutte le relazioni aziendali e le relative connessioni commerciali per riferimento futuro.

* **Gestione della configurazione**: verifica le modifiche alla configurazione delle singole società prima di applicarle alle gerarchie intere e documenta sempre le impostazioni correnti prima di apportare modifiche in blocco. Comunica in anticipo le modifiche pianificate agli amministratori aziendali interessati.

* **Sicurezza** - Limita le autorizzazioni di gestione della società solo agli amministratori attendibili, effettua revisioni regolari delle relazioni aziendali e delle autorizzazioni di accesso e monitora tutte le modifiche della gerarchia a scopo di controllo.

>[!MORELIKETHIS]
>
>* [Crea un account società](account-company-create.md)
>* [Gestione gerarchie società](manage-company-hierarchy.md)
>* [Ruoli e autorizzazioni società](account-company-roles-permissions.md)
>* [Gestione crediti aziendali](credit-company.md)
>* [Abilita funzionalità B2B](enable-basic-features.md)
