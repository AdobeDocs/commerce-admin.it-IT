---
title: Imposta sul valore aggiunto
description: descrizione qui&gt;
exl-id: 20dbcb86-e558-47f2-968d-b5c9ec5f665b
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 0%

---

# Imposta sul valore aggiunto

Alcuni paesi applicano un&#39;imposta sul valore aggiunto, o IVA, su beni e servizi. Ci possono essere diverse aliquote IVA a seconda della fase nel processo di produzione o distribuzione, materiali o servizi che si vendono ai clienti. È possibile applicare più di un&#39;aliquota IVA per calcolare correttamente l&#39;imposta dovuta.

Commerce può essere configurato per addebitare un&#39;imposta sul valore aggiunto in base all&#39;indirizzo dell&#39;esercente o del cliente, se entrambi si trovano nello stesso paese. I calcoli IVA si basano in genere sulla destinazione della spedizione, anziché sul punto di origine. Per la maggior parte degli scenari è sufficiente un&#39;impostazione di configurazione che calcola l&#39;IVA in base all&#39;indirizzo di spedizione del cliente.

## Scenari di esempio

- Nel caso di un&#39;impresa soggetta all&#39;IVA in un paese dell&#39;UE che fornisce beni a un privato in un altro paese dell&#39;UE, l&#39;IVA è calcolata come &quot;vendita a distanza&quot; in base all&#39;ubicazione dell&#39;esercente.

- Un&#39;azienda nei Paesi Bassi che effettua un acquisto da un negozio nel Regno Unito che spedisce a un indirizzo nel Regno Unito è tenuta a pagare le aliquote IVA del Regno Unito.

- Per la vendita di [prodotti scaricabili](../catalog/product-create-downloadable.md), o _beni digitali_, l&#39;aliquota IVA si basa sulla destinazione di spedizione, anziché sull&#39;ubicazione dell&#39;esercente. Vedere [Luogo di fornitura per i beni digitali](taxes.md#place-of-supply-for-digital-goods-eu).

>[!TIP]
>
>Alcune spedizioni transfrontaliere e B2B hanno requisiti fiscali più complessi. Per espandere le funzionalità native dell&#39;installazione di Commerce, è consigliabile aggiungere una soluzione di gestione delle imposte dal [Marketplace](https://marketplace.magento.com/extensions/accounting-finance/taxes.html).

## Configura IVA

Le istruzioni seguenti includono una procedura di esempio per impostare un&#39;IVA del 20% nel Regno Unito per le vendite ai clienti al dettaglio. Per altre aliquote e altri paesi, seguire la procedura generale ma inserire informazioni specifiche che corrispondono al paese, all&#39;aliquota IVA, ai tipi di cliente e così via.

>[!NOTE]
>
>Prima di procedere, assicurati di scoprire quali regole e regolamenti si applicano all&#39;IVA nella tua zona.

In talune operazioni tra imprese, l’IVA non viene calcolata. Commerce può convalidare l&#39;ID IVA di un cliente per garantire che l&#39;IVA sia valutata correttamente (o meno). Consulta [Convalida ID IVA](#vat-id-validation).

### Passaggio 1: impostare le classi imposta cliente

Il processo di creazione di una regola fiscale inizia con l&#39;aggiunta di un&#39;aliquota.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   ![Imposta classi imposta cliente](./assets/vat-zones.png){width="600" zoomable="yes"}

1. Assicurati che esista una classe fiscale cliente appropriata da utilizzare con l’IVA.

   Per questo esempio, accertati che esista una classe fiscale cliente denominata _Cliente al dettaglio_. Se la classe fiscale non esiste, fare clic su **[!UICONTROL Add New Tax Rate]**.

1. Immettere **[!UICONTROL Tax Identifier]** per la nuova classe fiscale.

   Tutte le aliquote vengono visualizzate nel campo _Aliquota_ in _Informazioni sulle regole fiscali_ quando si creano le regole fiscali.

1. Per impostare l&#39;intervallo di codici postali (da / a), selezionare la casella di controllo **[!UICONTROL Zip/Post is Range]**.

1. Scegliere **[!UICONTROL Country]** in cui applicare l&#39;aliquota.

1. Immettere **[!UICONTROL Rate Percent]** da utilizzare per il calcolo dell&#39;aliquota all&#39;acquisto.

1. Al termine, fare clic su **[!UICONTROL Save Rate]**.

In base all&#39;aliquota fiscale sottomessa, è possibile creare regole fiscali successive. In assenza di aliquote fiscali, la creazione di norme fiscali diventa impossibile.

### Passaggio 2: impostare le classi di imposta prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Fare clic su **[!UICONTROL Add New Tax Rule]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Additional Settings]**.

   ![Imposta classi imposta prodotto](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. In _Classe imposta prodotto_, fare clic su **[!UICONTROL Add New Tax Class]**.

1. Per aggiungere la nuova classe all&#39;elenco delle classi di imposta sui prodotti disponibili e creare tre nuove classi, immettere il **[!UICONTROL Name]** della nuova classe di imposta e fare clic sul segno di spunta:

   - `VAT Standard`
   - `VAT Reduced`
   - `VAT Zero`

1. Fare clic su **[!UICONTROL Save Class]** per ogni nuova classe aggiunta.

1. Fare clic su **[!UICONTROL Save Rule]**.

### Passaggio 3: Impostare aree e aliquote fiscali

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   In questo esempio è possibile rimuovere le aliquote fiscali statunitensi o lasciarle invariate.

1. Fare clic su **[!UICONTROL Add New Tax Rate]**.

   ![Impostare aree e aliquote fiscali](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

1. Definisci i nuovi tassi come segue:

   **IVA standard**

   - Identificatore imposta: `VAT Standard`
   - Paese e stato: `United Kingdom`
   - Percentuale tasso: `20.00`

   **IVA ridotta**

   - Identificatore imposta: `VAT Reduced`
   - Paese e stato: `United Kingdom`
   - Percentuale tasso: `5.00`

1. Fare clic su **[!UICONTROL Save Rate]** per ogni tariffa.

### Passaggio 4: Impostare le regole fiscali

Una regola fiscale è una combinazione di una classe fiscale cliente, una classe fiscale prodotto e un&#39;aliquota.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. Aggiungere nuove regole fiscali come segue:

   **IVA standard**

   - Nome: `VAT Standard`
   - Classe imposta cliente: `Retail Customer`
   - Classe imposta prodotto: `VAT Standard`
   - Aliquota: `VAT Standard Rate`

   **Iva Ridotta**

   - Nome: `VAT Reduced`
   - Classe imposta cliente: `Retail Customer`
   - Classe imposta prodotto: `VAT Reduced`
   - Aliquota: `VAT Reduced Rate`

1. Fare clic su **[!UICONTROL Save Rule]** per ogni tariffa.

### Passaggio 5: applicare le classi di imposta ai prodotti

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Manage Products]**.

1. Apri un prodotto dal catalogo in modalità di modifica.

1. Nella pagina _Generale_, individua l&#39;opzione **[!UICONTROL Tax Class]** e seleziona **[!UICONTROL VAT Class]** applicabile al prodotto.

1. Al termine, fare clic su **[!UICONTROL Save]**.

   ![Applica classi imposta ai prodotti](./assets/vat-apply-classes.png){width="600" zoomable="yes"}

## Descrizioni dei campi

### Informazioni archivio

Commerce utilizza le seguenti [impostazioni di configurazione delle informazioni di archiviazione](../configuration-reference/general/general.md#store-information) per calcolare l&#39;IVA in base alle informazioni sul commerciante.

**[!UICONTROL VAT Number]** - Codice IVA assegnato al commerciante.

**[!UICONTROL Validate VAT Number]** - [Convalida IVA](#vat-id-validation) conferma che la partita IVA corrisponde al record corrispondente nel database [Commissione europea](https://ec.europa.eu/taxation_customs/vies/).

### Informazioni cliente

Commerce utilizza i campi seguenti per calcolare l&#39;IVA in base a [informazioni sul cliente](../customers/account-dashboard-account-information.md)).

#### Informazioni account

**[!UICONTROL Tax/VAT Number]** - Se applicabile, la partita IVA o la partita IVA assegnata al cliente.

#### Indirizzi

**[!UICONTROL VAT Number]** - Se applicabile, la partita IVA associata a un indirizzo di fatturazione o spedizione specifico del cliente. Per la vendita di [beni digitali](taxes.md#place-of-supply-for-digital-goods-eu)) all&#39;interno dell&#39;UE, l&#39;importo dell&#39;IVA si basa sulla destinazione della spedizione.

### Account cliente

Commerce utilizza le [impostazioni di configurazione cliente](../customers/account-options-new.md) seguenti per calcolare l&#39;IVA.

**[!UICONTROL Show VAT Number on Storefront]** - Determina se il campo Partita IVA cliente è incluso nella Rubrica disponibile nel conto cliente.

**[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]** - L&#39;ID IVA è un identificatore interno per il numero IVA del cliente quando viene utilizzato nella convalida IVA. Durante la convalida IVA, Commerce conferma che il numero corrisponde al database [Commissione europea](https://ec.europa.eu/taxation_customs/vies/). I clienti possono essere assegnati automaticamente a uno dei quattro gruppi predefiniti in base ai risultati della convalida.

## Convalida ID IVA

_Convalida ID IVA_ calcola automaticamente l&#39;imposta richiesta per le transazioni B2B che si svolgono all&#39;interno dell&#39;Unione Europea (UE), in base alle impostazioni locali del cliente e dell&#39;esercente. Commerce esegue la convalida dell&#39;ID IVA utilizzando i servizi Web del server [Commissione europea][1].

>[!NOTE]
>
>Le norme fiscali relative all’IVA non influiscono su altre norme fiscali e non impediscono l’applicazione di altre norme fiscali. È possibile applicare una sola regola fiscale alla volta.

- L&#39;IVA viene addebitata se l&#39;esercente e il cliente si trovano nello stesso paese dell&#39;UE.
- L&#39;IVA non viene addebitata se il commerciante e il cliente si trovano in paesi dell&#39;UE diversi ed entrambe le parti sono imprese registrate nell&#39;UE.

L&#39;amministratore del negozio crea più di un gruppo di clienti predefinito che può essere assegnato automaticamente al cliente durante la creazione dell&#39;account, la creazione o l&#39;aggiornamento degli indirizzi e il pagamento. Ne consegue che le vendite all&#39;interno del paese (nazionale) e all&#39;interno dell&#39;UE sono soggette a norme fiscali diverse.

>[!IMPORTANT]
>
>Se vendi prodotti virtuali o scaricabili che non richiedono la spedizione, l’aliquota IVA del paese di ubicazione di un cliente deve essere utilizzata sia per le vendite intra-unionali che per quelle nazionali. Creare singole regole fiscali aggiuntive per le classi imposta prodotto corrispondenti ai prodotti virtuali.

### Flusso di lavoro di registrazione cliente

Se la convalida dell&#39;ID IVA è abilitata, dopo la registrazione a ciascun cliente viene proposto di inserire il numero di partita IVA. Tuttavia, solo gli acquirenti che sono clienti IVA registrati sono tenuti a compilare questo campo.

Quando un cliente specifica il numero di partita IVA e altri campi di indirizzo e sceglie di salvare, il sistema salva l&#39;indirizzo e invia la richiesta di convalida del codice IVA al server della Commissione europea. In base ai risultati della convalida, a un cliente viene assegnato uno dei gruppi predefiniti. Questo gruppo può essere modificato se un cliente o un amministratore modifica l&#39;ID IVA dell&#39;indirizzo predefinito o l&#39;intero indirizzo predefinito. A volte, il gruppo può essere modificato temporaneamente (la modifica del gruppo viene emulata) durante il checkout di una pagina.

Se questa opzione è abilitata, è possibile sostituire la convalida dell&#39;ID IVA per i singoli clienti selezionando la casella di controllo nella pagina _[!UICONTROL Customer Information]_.

### Flusso di lavoro di cassa

Se la convalida IVA di un cliente viene eseguita durante il pagamento, l&#39;identificativo della richiesta IVA e la data della richiesta IVA vengono salvati nella sezione Cronologia commenti dell&#39;ordine.

Il comportamento del sistema relativo alla convalida dell&#39;ID IVA e alla modifica del gruppo di clienti durante l&#39;estrazione dipende dalla configurazione delle impostazioni Convalida per ogni transazione e Disattiva modifica automatica gruppo. Questa sezione descrive l&#39;implementazione della funzionalità di convalida dell&#39;ID IVA per l&#39;estrazione sul front-end.

Se il cliente utilizza Google Express Checkout, PayPal Express Checkout o un altro metodo di pagamento esterno, il pagamento viene eseguito completamente sul lato del gateway dei pagamenti esterno. Per questo scenario, non è possibile applicare l&#39;impostazione _Convalida su ogni transazione_ e il gruppo di clienti non può cambiare durante l&#39;estrazione.

![Flusso di lavoro estrazione convalida IVA](./assets/vat-id-validation2.png){width="550" zoomable="yes"}

### Configura convalida ID IVA

Per configurare la convalida dell&#39;ID IVA, è innanzitutto necessario impostare i gruppi di clienti necessari e creare le classi di imposta, le aliquote e le regole correlate. Quindi, abilita la convalida dell’ID IVA per l’archivio e completa la configurazione.

Gli esempi seguenti mostrano come le classi e le aliquote fiscali vengono utilizzate per la convalida dell&#39;ID IVA. Rivedi gli esempi e segui le istruzioni per l’impostazione delle classi e delle regole fiscali necessarie per il tuo Negozio.

#### Esempio: regole fiscali minime richieste per la convalida dell&#39;ID IVA

| Regola fiscale #1 |  |
|--- |--- |
| Classe imposta cliente | Le classi di imposta cliente devono includere: <br />Una classe per i clienti nazionali. <br />Classe per clienti con ID IVA formattati in modo errato.<br />Classe per i clienti la cui convalida dell&#39;ID IVA non è riuscita. |
| Classe imposta prodotto | Le classi di imposta prodotto devono includere una classe per i prodotti di tutti i tipi, ad eccezione di bundle e virtual. |
| Aliquota fiscale | L&#39;aliquota deve includere l&#39;aliquota IVA del paese dell&#39;esercente. |

{style="table-layout:auto"}

| Regola fiscale #2 |   |
|--- |--- |
| Classe imposta cliente | Una classe per clienti intra-unione. |
| Classe imposta prodotto | Una classe per prodotti di tutti i tipi, eccetto virtuale. |
| Aliquota fiscale | Aliquote IVA per tutti i paesi dell&#39;UE, ad eccezione del paese dell&#39;esercente. Attualmente questo tasso è dello 0%. |

{style="table-layout:auto"}

| Regola fiscale #3 | (Richiesto per prodotti virtuali e scaricabili) |
|--- |--- |
| Classe imposta cliente | Le classi IVA cliente devono includere: <br/>Una classe per clienti nazionali <br/>Una classe per clienti con ID IVA A non valido per clienti per i quali la convalida dell&#39;ID IVA non è riuscita |
| Classe imposta prodotto | Classe per prodotti virtuali. |
| Aliquota fiscale | Aliquota IVA del paese dell&#39;esercente. |

{style="table-layout:auto"}

| Regola fiscale #4 | (Richiesto per prodotti virtuali e scaricabili) |
|--- |--- |
| Classe imposta cliente | Una classe per clienti intra-unione. |
| Classe imposta prodotto | Classe per prodotti virtuali. |
| Aliquota fiscale | Aliquote IVA per tutti i paesi dell&#39;UE, ad eccezione del paese dell&#39;esercente. Attualmente questo tasso è dello 0%. |

{style="table-layout:auto"}

#### Passaggio 1: creare gruppi di clienti correlati all&#39;IVA

La convalida ID IVA assegna automaticamente uno dei quattro gruppi di clienti predefiniti ai clienti in base ai risultati della convalida ID IVA:

- Residenti nazionali
- intra-UE
- ID IVA non valido
- Errore di convalida

Puoi creare gruppi di clienti per la convalida dell&#39;ID IVA o utilizzare gruppi esistenti, se conformi alla logica aziendale. Quando si configura la convalida dell&#39;ID IVA, è necessario assegnare ciascuno dei gruppi di clienti creati come impostazione predefinita per i clienti con risultati di convalida dell&#39;ID IVA appropriati.

#### Passaggio 2: creare classi, aliquote e regole relative all&#39;IVA

Ogni regola fiscale è definita da tre entità:

- Classi imposta cliente
- Classi imposta prodotto
- Aliquote fiscali

Crea le [regole fiscali](tax-rules.md) per utilizzare correttamente la convalida ID IVA.

- Le regole fiscali includono le aliquote e [le classi fiscali](tax-class.md).
- Le classi di imposta sono assegnate a [gruppi di clienti](../customers/customer-groups.md).

#### Passaggio 3: abilitare e configurare la convalida dell’ID IVA

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Se necessario, impostare **[!UICONTROL Store View]** per la configurazione.

1. Nel pannello a sinistra, espandi **[!UICONTROL Customers]** e scegli **[!UICONTROL Customer Configuration]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Create New Account Options]**.

   Nell&#39;esempio seguente, le impostazioni generali del cliente non correlate alla convalida dell&#39;IVA sono dim.

   ![Crea nuove opzioni account](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enable Automatic Assignment to Customer Group]** su `Yes` e completa i campi seguenti in base alle esigenze.

   - **[!UICONTROL Default Group]**
   - **[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]**
   - **[!UICONTROL Show VAT Number on Storefront]**

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

#### Passaggio 4: imposta l&#39;ID IVA e il paese di ubicazione

1. Nel pannello a sinistra, espandi **[!UICONTROL General]** e scegli **[!UICONTROL General]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Store Information]**.

   ![Informazioni archivio](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. Seleziona **[!UICONTROL Country]**.

1. Immetti **[!UICONTROL VAT Number]** e fai clic su **[!UICONTROL Validate VAT Number]**.

   Il risultato viene visualizzato immediatamente.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

#### Passaggio 5: verificare l&#39;elenco dei paesi membri dell&#39;UE

1. Continuando nella pagina di configurazione _Generale_, espandere ![Selettore di espansione](../assets/icon-display-expand.png) la sezione **[!UICONTROL Countries Options]**.

   ![Opzioni paesi](../configuration-reference/general/assets/general-country-options.png){width="600" zoomable="yes"}

1. Nell&#39;elenco **[!UICONTROL European Union Countries]** verificare che sia selezionato ogni paese membro dell&#39;UE.

   Per modificare l&#39;impostazione predefinita, deselezionare la casella di controllo **Usa valori di sistema**. Tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ogni paese che si desidera aggiungere o rimuovere.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.


[1]: https://ec.europa.eu/taxation_customs/vies/
