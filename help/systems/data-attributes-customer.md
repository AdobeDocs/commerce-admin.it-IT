---
title: Riferimento attributi dati cliente
description: Utilizzare questo riferimento degli attributi dei dati del cliente quando si utilizzano importazioni ed esportazioni di dati del cliente.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Riferimento attributi dati cliente

Nelle tabelle seguenti sono elencati gli attributi di un&#39;esportazione tipica del file principale e degli indirizzi dei clienti. L’installazione utilizzata per esportare questi dati dispone di due siti web e diverse visualizzazioni store, con i dati di esempio installati.

Ogni attributo, o campo, è rappresentato nel file CSV come una colonna e i record dei clienti sono rappresentati da righe. Le colonne che iniziano con un carattere di sottolineatura sono entità di servizio che contengono proprietà o dati complessi.

## File principale clienti

| Attributo | Descrizione |
|--- |--- |
| `email` | Indirizzo e-mail del cliente. |
| `_website` |  |
| `_store` |  |
| `confirmation` | Flag di conferma. |
| `created_at` | Data di creazione dell&#39;account cliente. |
| `created_in` | La vista del negozio in cui è stato creato l’account. |
| `disable_auto_group_change` | Determina se i gruppi di clienti possono essere assegnati in modo dinamico durante la convalida dell&#39;ID IVA. |
| `dob` | La data di nascita del cliente. <br><br>**_Importante:_**&#x200B;In linea con le attuali best practice per la sicurezza e la privacy, controlla l&#39;archiviazione e l&#39;elaborazione della data di nascita completa dei clienti (mese, giorno, anno). Se raccolto con altri identificatori personali (ad esempio_nome completo _), potrebbe rappresentare un rischio legale e di sicurezza. Consigliamo di limitare la memorizzazione delle date di nascita complete dei clienti e di utilizzare invece l’anno di nascita del cliente come alternativa. |
| `firstname` | Il nome del cliente. |
| `gender` | Il genere del cliente. |
| `group_id` | ID del gruppo di clienti a cui è assegnato il cliente. |
| `lastname` | Cognome del cliente. |
| `middlename` | Secondo nome o secondo nome iniziale del cliente. |
| `password_hash` | Hash password |
| `prefix` | Qualsiasi prefisso utilizzato con il nome del cliente (ad esempio `Mr.`, `Ms.`, `Mrs.` e `Dr.`). |
| `rp_token` | Reimposta token password. |
| `rp_token_created_at` | Data di reimpostazione della password. |
| `store_id` | ID store |
| `suffix` | Qualsiasi suffisso utilizzato con il nome del cliente (ad esempio `Jr.`, `Sr.` e `Esquire`). |
| `taxvat` |  |
| `website_id` | ID sito Web del sito in cui è stato creato l&#39;account del cliente. |
| `password` | La password del cliente. |

{style="table-layout:auto"}

## Indirizzi dei clienti

| Attributo | Descrizione |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | La città in cui si trova l’indirizzo del cliente. |
| `company` | Il nome della società, se applicabile per questo indirizzo. |
| `country_id` | L’ID paese in cui si trova l’indirizzo del cliente. |
| `fax` | Numero di fax del cliente, se applicabile. |
| `firstname` | Il nome del cliente. |
| `lastname` | Cognome del cliente. |
| `middlename` | Secondo nome o secondo nome iniziale del cliente. |
| `postcode` | Il codice postale o ZIP in cui si trova l’indirizzo del cliente. |
| `prefix` | Qualsiasi prefisso utilizzato con il nome del cliente (ad esempio `Mr.`, `Ms.`, `Mrs.` e `Dr.`). |
| `region` | L’area geografica in cui si trova l’indirizzo del cliente. |
| `region_id` | ID regione |
| `street` | Indirizzo del cliente. Se specificata nella configurazione, è disponibile una seconda riga dell’indirizzo stradale. |
| `suffix` | Se utilizzato, il suffisso associato al nome del cliente (ad esempio `Jr.`, `Sr.` o `III`). |
| `telephone` | Numero di telefono del cliente associato all&#39;indirizzo. |
| `vat_id` | L’ID IVA è un identificatore interno del numero di IVA del cliente quando viene utilizzato nella convalida dell’IVA. |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | Identifica l’indirizzo di fatturazione predefinito. Il valore `1` indica che l&#39;indirizzo è l&#39;indirizzo di fatturazione predefinito del cliente. Valori: 1 / 0 |
| `_address_default_shipping_` | Identifica l&#39;indirizzo di spedizione predefinito. Il valore `1` indica che l&#39;indirizzo è l&#39;indirizzo di spedizione predefinito del cliente. Valori: `1` / `0` |

{style="table-layout:auto"}
