---
title: Creare regole per il marchio di arricchimento del catalogo
description: Scopri come creare e gestire regole di governance del brand per l’arricchimento del catalogo, definire i requisiti per la copia del prodotto e applicare le regole ai processi di arricchimento del catalogo.
role: Admin, User, Leader
source-git-commit: 9d7a4f4e98fe2d2d51261d96a2e072c28925babd
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%
---
# Creare regole del marchio per l’arricchimento dei cataloghi

Le regole di governance dei marchi e dei marchi sono disponibili solo per l’arricchimento dei cataloghi. Non si applicano all’arricchimento della PDP. Queste regole definiscono i requisiti per i nomi e le descrizioni dei prodotti generati da [!DNL Commerce Catalog Agent]. Modifica o configura una regola predefinita per gli standard del brand predefiniti, quindi crea regole personalizzate per campagne, categorie di prodotto o marchi secondari specifici. Selezionare una regola quando si crea un processo [Arricchimento catalogo](catalog-enrichment.md).

## Governance del brand aperto

1. In Amministrazione, passa a **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**.
1. Apri la scheda **[!UICONTROL Brand Governance]**.

La scheda **Governance del brand** contiene la regola predefinita ed eventuali regole personalizzate create. Puoi cercare le regole o filtrare l’indice delle regole.

Per ogni riga vengono visualizzati **Nome regola**, **Campi**, **Tono**, **Ultima modifica** e **Stato**. La regola predefinita è contrassegnata **[!UICONTROL Default]**.

Nell&#39;area **[!UICONTROL Needs your attention]** sono evidenziate le regole che richiedono lavoro, ad esempio le bozze che richiedono configurazione o le regole con conflitti. Rivedere i dettagli della regola e utilizzare l&#39;azione disponibile, ad esempio **[!UICONTROL Finish setup]** o **[!UICONTROL Fix conflict]**.

## Comprendere i tipi di regole

L’arricchimento del catalogo supporta una regola predefinita e regole personalizzate.

### Regola predefinita

Ogni istanza di [!DNL Adobe Commerce] dispone esattamente di una regola predefinita. [!DNL Adobe Commerce] crea questa regola con campi vuoti. Il nome è fisso come **[!UICONTROL Global]**. Puoi modificare la regola, ma non eliminarla.

[!DNL Adobe Commerce] applica la regola predefinita per impostazione predefinita quando si crea un processo di arricchimento del catalogo senza selezionare una regola personalizzata. La regola predefinita fornisce la governance di base per l’arricchimento del catalogo.

### Regole personalizzate

Puoi creare un numero qualsiasi di regole personalizzate per una campagna, una categoria di prodotto o un marchio secondario. Una regola personalizzata non viene applicata automaticamente. Selezionala durante la creazione di un processo di arricchimento del catalogo.

Una regola personalizzata non eredita i valori dalla regola predefinita. Quando crei una regola personalizzata, puoi copiare i valori correnti della regola predefinita come punto di partenza unico. Le modifiche successive alla regola predefinita non aggiornano la regola personalizzata.

Utilizza la Regola predefinita per gli standard da applicare quando un utente non seleziona una regola personalizzata. Crea una regola personalizzata per una campagna o una categoria con requisiti diversi. Aggiungi eventuali requisiti globali necessari anche per la regola personalizzata, perché le regole personalizzate non ereditano i valori globali.

## Creare una regola personalizzata

In questa sezione imparerai a creare una regola di governance del brand.

![Crea regola per la governance del brand](./assets/brand-gov-create-rule.png)

1. Nella scheda **Governance del marchio**, fai clic su **[!UICONTROL Create Rule]**.
1. Scegli come avviare la regola:
   - **[!UICONTROL Blank]**: imposta tutti i valori autonomamente.
   - **[!UICONTROL Copy Global enrichment]**: inizia con i valori della regola predefinita correnti come copia monouso.
   - **[!UICONTROL Draft with AI]**: (**Disponibile a breve**) Descrivi la tua voce del brand per ottenere i valori delle regole suggeriti.
1. Immetti un **Nome regola** che ne identifichi lo scopo, ad esempio una campagna, una categoria o un marchio secondario.
1. In **Campi da migliorare**, configura il nome del prodotto e i requisiti di descrizione del prodotto.

   Configura separatamente nomi e descrizioni dei prodotti. Ogni campo ha i propri requisiti di attivazione e governance.

1. Imposta **Lunghezza nome prodotto**.

   Imposta l’intervallo di lunghezza minima e massima del nome per un nome di prodotto arricchito. Ad esempio, una regola può richiedere un minimo di 20 caratteri e un massimo di 200 caratteri.

1. Imposta l&#39;opzione **Maiuscole**:

   - **[!UICONTROL Sentence case]**: `Waterproof hiking boots`
   - **[!UICONTROL Title Case]**: `Waterproof Hiking Boots`
   - **[!UICONTROL As written]**: mantiene le iniziali maiuscole nel testo di origine.

1. Descrivi il **Tono marchio**. Consulta [impostare il tono del brand](#set-brand-tone) per maggiori informazioni.
1. Impostare le frasi richieste ed escluse

   Aggiungere una frase **[!UICONTROL Must include]**.
   Aggiungere una frase **[!UICONTROL Never use]**.

1. Fare clic su **[!UICONTROL Save as draft]** per terminare in un secondo momento oppure fare clic su **[!UICONTROL Publish rule]** per rendere la regola disponibile per la selezione durante la creazione di una regola di arricchimento catalogo. Fare clic su **[!UICONTROL Cancel]** per uscire senza salvare.

1. È ora possibile applicare la regola a un processo [Arricchimento catalogo](catalog-enrichment.md).

### Imposta il tono del brand

Immettere le istruzioni nel campo **[!UICONTROL Brand tone]** multiriga per descrivere la voce e lo stile del nome arricchito.

Di seguito sono riportati alcuni esempi del tono che è possibile utilizzare per la **Descrizione**:

- **B2B industriale**: `Write for the operator and the buyer. Open with what the unit does and where it fits in the kitchen, then throughput, utility requirements, footprint, and certifications. Plain, technical language. Mention cleaning and maintenance, because total cost of ownership drives the decision. No lifestyle language.`
- **Moda di lusso**: `Quiet confidence. Lead with craftsmanship and provenance (atelier, tannery, technique), then how the piece wears and ages. Short, measured sentences. Sensory detail is fine. Never compare to other brands or mention price or value.`
- **Elettronica di consumo**: `Clear and benefit-led. Turn every spec into what it does for the user. Scannable short paragraphs or bullets. Put compatibility and what's in the box up front. Don't make performance claims without a source, and don't use comparative claims like "fastest"`
- **Alimenti speciali e generi alimentari**: `Warm and appetizing, but honest. Describe taste, texture, and aroma in concrete terms, then origin and how it's made, then serving ideas. Plain, friendly language. Put allergens and dietary attributes in a consistent closing line. Don't make health claims.`
- **Arredamento domestico**: `Inviting and practical. Open with how the piece is used, then dimensions, materials, and care. Help the shopper picture it in their space without overselling. Always mention assembly, delivery, and weight, since those drive returns.`
