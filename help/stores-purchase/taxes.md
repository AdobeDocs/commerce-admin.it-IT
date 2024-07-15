---
title: Imposte
description: Scopri come configurare il tuo negozio per calcolare le imposte in base ai requisiti della tua lingua.
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# Imposte

Configura il tuo store per calcolare le tasse secondo i requisiti della tua lingua. Puoi impostare [classi fiscali](tax-class.md) per prodotti e gruppi di clienti e creare [regole fiscali](tax-rules.md) che combinano classi di prodotti e clienti, aree fiscali e aliquote. Commerce fornisce inoltre impostazioni di configurazione per imposte sui prodotti fisse, imposte composte e visualizzazione dei prezzi oltre i confini internazionali. Se devi riscuotere una [imposta sul valore aggiunto](vat.md), puoi impostare lo store per calcolare automaticamente l&#39;importo appropriato con la convalida.

>[!NOTE]
>
>Le versioni da 2.4.0 a 2.4.3 di Adobe Commerce e Magento Open Source includevano l’estensione sviluppata dal fornitore Vertex utilizzata per l’integrazione con Vertex Cloud al fine di fornire gestione fiscale e pulizia degli indirizzi. A partire dalla versione 2.4.4, questa estensione non è più inclusa nella versione di base e deve essere installata e aggiornata dalla versione di Commerce Marketplace o direttamente dal fornitore. [Contattare il vertice](https://marketplace.magento.com/partner/vertex_inc) per informazioni sull&#39;estensione e sulla documentazione.<br><br>
>
>Se l’estensione in bundle è abilitata e configurata, devi aggiornare il file compositore.json come parte del processo di aggiornamento 2.4.4 e gestire gli aggiornamenti delle estensioni in futuro. Consulta [Moduli di aggiornamento](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) nella _Guida all&#39;aggiornamento_.

## Riferimento rapido

Alcune impostazioni di imposta dispongono di una scelta di opzioni che determinano il modo in cui l&#39;imposta viene calcolata e presentata al cliente. Per ulteriori informazioni, vedere [Linee guida internazionali sulle imposte](international-tax-guidelines.md).

Utilizzare le tabelle seguenti come riferimento per la configurazione delle impostazioni di calcolo delle imposte:

### Metodi di calcolo delle imposte

Le opzioni del metodo di calcolo delle imposte includono [!UICONTROL Unit Price], [!UICONTROL Row Total] e [!UICONTROL Total]. Nella tabella seguente viene illustrato come viene gestito l&#39;arrotondamento (a due cifre) per impostazioni diverse.

| Impostazione | Calcolo e visualizzazione |
|--- |--- |
| [!UICONTROL Unit Price] | Commerce calcola l&#39;imposta per ciascun articolo e visualizza i prezzi comprensivi di imposte. Per calcolare il totale dell&#39;imposta, viene arrotondata l&#39;imposta per ogni elemento e quindi viene sommata. |
| [!UICONTROL Row Total] | Commerce calcola l&#39;imposta per ogni riga. Per calcolare il totale dell&#39;imposta, viene arrotondata l&#39;imposta per ogni voce di riga e quindi viene sommata. |
| [!UICONTROL Total] | Commerce calcola l&#39;imposta per ciascun articolo e aggiunge tali valori per calcolare l&#39;importo totale dell&#39;imposta non arrotondato per l&#39;ordine. Applica quindi la modalità di arrotondamento specificata all&#39;imposta totale per determinare l&#39;imposta totale per l&#39;ordine. |

{style="table-layout:auto"}

### Prezzi catalogo con o senza imposte

I possibili campi di visualizzazione variano a seconda del metodo di calcolo e del fatto che i prezzi del catalogo includano o escludano le imposte. I campi di visualizzazione hanno precisione a due decimali nei calcoli normali. Alcune combinazioni di impostazioni di prezzo visualizzano i prezzi che includono ed escludono l&#39;imposta. Quando entrambi compaiono sullo stesso elemento di riga, i clienti possono essere confusi e viene attivato un [avviso](taxes.md#warning-messages).

| Impostazione | Calcolo e visualizzazione |
|--- |--- |
| [!UICONTROL Excluding Tax] | Utilizzando questa impostazione, il prezzo dell&#39;articolo di base viene utilizzato nel momento in cui viene immesso e vengono applicati i metodi di calcolo dell&#39;imposta. |
| [!UICONTROL IncludingTax] | Utilizzando questa impostazione, viene calcolato per primo il prezzo dell&#39;articolo di base al netto delle imposte. Questo valore viene utilizzato come prezzo base e vengono applicati i metodi di calcolo dell&#39;imposta. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Vi sono modifiche rispetto alle versioni precedenti per gli esercenti dell&#39;UE o altri commercianti IVA che espongono i prezzi, comprese le imposte, e operano in diversi paesi con più punti di vendita. Se si caricano i prezzi con più di due cifre di precisione, Commerce arrotonda automaticamente tutti i prezzi a due cifre per garantire che venga presentato un prezzo coerente agli acquirenti.

### Prezzi di spedizione con o senza imposte

| Impostazione | Visualizzazione | Calcolo |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | Appare senza imposte. | Calcolo normale. La spedizione viene aggiunta al totale del carrello, in genere visualizzato come un articolo separato. |
| [!UICONTROL Including Tax] | Può essere un&#39;imposta inclusa oppure può essere visualizzata separatamente. | La spedizione viene trattata come un altro articolo nel carrello con le imposte, utilizzando gli stessi calcoli. |

{style="table-layout:auto"}

### Importi imposta come voci

Per visualizzare due diversi importi di imposta come voci di riga separate, ad esempio GST e PST per i negozi canadesi, è necessario impostare priorità diverse per le regole fiscali correlate. Tuttavia, nei calcoli fiscali precedenti, le imposte con priorità diverse sarebbero automaticamente composte. Per visualizzare correttamente importi di imposta separati senza una composizione errata degli importi di imposta, è possibile impostare priorità diverse e selezionare la casella di controllo _Calcola solo subtotale_. Questa impostazione produce importi di imposta calcolati correttamente che vengono visualizzati come voci separate.

## Messaggi di avvertenza

Alcune combinazioni di opzioni relative alle imposte potrebbero confondere i clienti e generare un avviso. Queste condizioni possono verificarsi quando il metodo di calcolo dell&#39;imposta è impostato su `Row` o `Total` e al cliente vengono presentati prezzi che escludono e includono l&#39;imposta. Può anche verificarsi quando nel carrello è presente un’imposta per articolo. Poiché il calcolo dell&#39;imposta viene arrotondato, l&#39;importo visualizzato nel carrello potrebbe essere diverso dall&#39;importo che il cliente prevede di pagare.

Se il calcolo dell&#39;imposta si basa su una configurazione problematica, vengono visualizzate le seguenti avvertenze:

![Punto esclamativo](../assets/icon-warning.png) **Avviso**. `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![Punto esclamativo](../assets/icon-warning.png) **Avviso**. `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## Luogo di cessione di beni digitali (UE)

Gli esercenti dell&#39;Unione europea (UE) devono segnalare i beni digitali venduti trimestralmente a ciascun paese membro. I beni digitali vengono tassati in base all’indirizzo di spedizione del cliente. La legge impone agli esercenti di eseguire una dichiarazione fiscale e di identificare gli importi delle imposte pertinenti per i beni digitali, anziché per i beni fisici.

I commercianti devono segnalare tutti i beni digitali venduti dai paesi membri dell&#39;UE su base trimestrale a un&#39;amministrazione fiscale centrale, insieme al pagamento dovuto per le imposte riscosse durante il periodo.

I commercianti che non hanno ancora raggiunto la soglia (50.000/100.000 euro di volume d&#39;affari annuo) devono continuare a segnalare i beni fisici venduti agli Stati membri dell&#39;UE in cui hanno registrato numeri di partita IVA.

I commercianti sottoposti a revisione per le imposte pagate per i beni digitali devono fornire due informazioni di supporto per stabilire il luogo di residenza del cliente.

- Per stabilire il luogo di residenza del cliente, è possibile utilizzare l&#39;indirizzo di spedizione del cliente e la registrazione di una transazione di pagamento riuscita. Il pagamento viene accettato solo se l&#39;indirizzo di spedizione corrisponde alle informazioni del provider di pagamenti.
- Le informazioni possono anche essere acquisite direttamente dall’archivio dati nelle tabelle del database di Commerce.

_**Per raccogliere informazioni sull&#39;imposta sui beni digitali:**_

1. Caricare le aliquote fiscali per tutti i paesi membri dell&#39;UE.

1. Crea una classe fiscale per prodotti digitali.

1. Assegna tutti i tuoi beni digitali alla classe fiscale dei prodotti di beni digitali.

1. Crea [regole fiscali](tax-rules.md) per i beni fisici, utilizzando le classi fiscali dei prodotti fisici, e associale alle aliquote fiscali appropriate.

1. Creare regole fiscali per i beni digitali, utilizzando la classe di imposta prodotto per i beni digitali, e associarle alle aliquote fiscali appropriate per i paesi membri dell&#39;UE.

1. Eseguire il rapporto sulle imposte per il periodo appropriato e raccogliere le informazioni sui beni digitali richieste.

1. Esporta gli importi delle imposte correlati alle aliquote per la classe fiscale dei prodotti digitali.

Risorse aggiuntive:

- [Unione fiscale e doganale della Commissione europea][1]
- [Modifiche al luogo di fornitura di EU 1015][2]

[1]: https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm
[2]: https://www2.deloitte.com/global/en/services/tax.html
