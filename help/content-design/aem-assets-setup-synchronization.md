---
title: Configurare il servizio di sincronizzazione
description: '"Scopri come collegare i progetti Adobe Commerce e Experience Manager Assets con il servizio Assets Rule Engine per abilitare la sincronizzazione delle risorse tra questi due sistemi".'
feature: CMS, Media
source-git-commit: 9d7b1b58b472a99196213e5ab109142bc57b1692
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---


# Configurare il servizio di sincronizzazione

Il servizio motore di regole delle risorse (ARES) è un servizio multi-tenant che integra AEM Assets con Adobe Commerce. Questo servizio sincronizza le risorse tra Adobe Commerce e Experience Manager. Il servizio ARES associa automaticamente le risorse dell’AEM ai prodotti di Adobe Commerce in base allo SKU o ad altri attributi chiave. Inoltre, assicura che le risorse e le varianti di prodotto più recenti siano sempre disponibili sul sito di e-commerce.

Per configurare il servizio, è necessario registrare l’ID tenant utilizzando l’API ARES GraphQL e selezionare la regola corrispondente per la sincronizzazione delle risorse.

## Scegli una strategia di corrispondenza

L’integrazione di AEM Assets per Commerce supporta due strategie di corrispondenza per la sincronizzazione delle risorse tra Adobe Commerce e AEM Assets.

- **MatchBySku**-Questa è la regola di corrispondenza predefinita che corrisponde alle risorse in base allo SKU (Stock Keeping Unit) del prodotto. Lo SKU è un identificatore univoco per ciascun prodotto. Questa regola associa lo SKU nei metadati della risorsa allo SKU del prodotto Commerce per garantire che le risorse siano associate ai prodotti corretti.

- **ExternalMatcher**-Questa regola di corrispondenza è per scenari più complessi o requisiti aziendali specifici che richiedono una logica di corrispondenza personalizzata. Per utilizzare questa regola, è necessario che in Adobe Developer App Builder sia implementato un codice personalizzato che definisca la corrispondenza tra le risorse e i prodotti.

Per l&#39;onboarding iniziale, utilizza la strategia `MatchBySku`. Se necessario, puoi modificare la strategia di corrispondenza in un secondo momento.

## Registrare un tenant

>[!BEGINSHADEBOX]

**Prerequisito**

- [Il progetto AEM Assets è stato configurato con i metadati Commerce necessari per la mappatura delle risorse](aem-assets-configure-aem.md).

- [Installa e configura l&#39;integrazione Experience Manager Assets in Adobe Commerce](aem-assets-configure-commerce.md).

>[!ENDSHADEBOX]

## Raccogli le credenziali

Per autenticare e collegare l’ambiente di progetto Commerce e l’ambiente di progetto AEM Assets con i servizi SaaS di Commerce sono necessarie le seguenti credenziali.

| Dati richiesti | Source | Dove trovarlo |
| ---------- | ------ | ------------- |
| Chiave API dall’account di Magento | Commerce | Fornisci la chiave API pubblica per l’ambiente Commerce in uso, di staging o produzione. Le chiavi API per gli ambienti di produzione e staging sono disponibili nella pagina [Configurazione connettore di servizio Commerce](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) in Amministrazione oppure nella pagina [!UICONTROL My Account] nella sezione [!UICONTROL API Portal]. |
| Identificatore progetto Commerce SaaS <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Amministratore Commerce | Questi valori identificano l’ambiente Commerce, lo spazio dati SaaS e il progetto a cui connettersi. I valori provengono dalla [configurazione dell&#39;identificatore SaaS di Commerce Services Connector].(aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| AEM `programId`<br>`environmentId` | [Ambiente di authoring di AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | Aprire la pagina AEM Sites e selezionare **[!UICONTROL Assets]**.  Copia gli ID del progetto e dell&#39;ambiente dall&#39;URL: `https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/` |
| baseURL | vetrina Commerce | L&#39;[URL di base](../stores-purchase/store-urls.md) per la vetrina Commerce. |
| Credenziali OAuth per accesso API | Amministratore Commerce | Queste credenziali sono disponibili nelle impostazioni di configurazione di Commerce [per l&#39;integrazione di Assets](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release). |

## Registra tenant

Completa la registrazione del tenant inviando una richiesta al servizio Motore regole di Assets per aggiungere credenziali di autenticazione e ID tenant. La richiesta include le credenziali e gli identificatori di progetto necessari per stabilire le connessioni tra il servizio, il progetto Commerce e il progetto Experience Manager Assets.

Invia la richiesta utilizzando un client GraphQL o cURL.

>[!BEGINTABS]

>[!TAB Richiesta GraphQL]

Utilizzare un client GraphQL per inviare una richiesta POST all&#39;endpoint API `https://commerce.adobe.io/assets-integration/graphql`

**Intestazioni richieste**

Specifica le seguenti intestazioni HTTP per la richiesta:

- `x-api-key`: chiave API dall&#39;account di Magento
- `magento-environment-Id`: Identificatore SaaS
- `x-gw-signature`: token JWT associato al MAGEID

**Richiesta:**

**Sintassi**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

**Esempio di utilizzo**

Registra un tenant e seleziona la regola `matchBySku` per mappare le risorse tra Adobe Commerce e il progetto AEM Assets.

**Richiesta:**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "***",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "rule": {
            "type": "matchBySKU"
            "matchBySkuRule": {
               "metadataField": "commerce:skus"
            }
         }
      }
   }
```

**Risposta**

```graphql
{
    "data": {
        "registerTenant": {
            "tenantId": "b65d5da7-2756-46a1-9ff1-14fb5d925fee",
            "userErrors": []
        }
    }
}
```

>[!TAB richiesta cURL]

```shell
curl --request POST \
  --url https://commerce.adobe.io/assets-integration/graphql \
  --header 'Content-Type: application/json' \
  --header 'Magento-Environment-Id: ****' \
  --header 'x-api-key: ****' \
  --header 'x-gw-signature: *****' \
  --data '{"query":"mutation registerTenant($tenantInput: TenantInput!) {\n\tregisterTenant(tenantInput: $tenantInput) {\n\t\ttenantId\n\t\tuserErrors {\n\t\t\tmessage\n\t\t\tpath\n\t\t}\n\t}\n}\n","operationName":"registerTenant","variables":{"tenantInput":{"enabled":true,"threshold":100,"projectId":"5d6faa03-e200-4623-9008-da144e4eefd8","aem":{"programId":"***","environmentId":"***"},"commerce":{"version":"2.4.6-p2","extensionVersion":"0.0.1","baseUrl":"***","credentials":{"consumerKey":"***","consumerSecret":"***","accessToken":"***","accessTokenSecret":"***"}},"rule":{"type":"matchBySKU","matchBySkuRule":{"metadataField":"commerce:skus"}}}}}'
```

>[!ENDTABS]

### Campi di input

#### AemInput

Identifica l’istanza di AEM Assets per l’archiviazione delle risorse Commerce. È possibile ottenere queste informazioni dalla vista Programmi personali di Cloud Manager o dall&#39;URL di authoring dei contenuti.

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| `programId` | Stringa! | Identificatore univoco del progetto in AEM Cloud Service |
| `environmentId` | Stringa! | ID per l’ambiente del progetto in uso, ad esempio Produzione, Staging o Sviluppo |

#### CommerceInput

Questo campo di input fornisce le credenziali di autenticazione OAuth per l’accesso API al catalogo Commerce. Queste credenziali sono disponibili nelle impostazioni di configurazione di Commerce [per l&#39;integrazione di Assets](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| `baseUrl` | Stringa | L&#39;[URL di base](../stores-purchase/store-urls.md) per la vetrina Commerce. |
| `credentials` | [InputCredenzialiCommerce](#commercecredentialsinput). | Specifica le credenziali per accedere all’istanza di Commerce. |
| `extensionVersion` | Stringa | Facoltativo. Versione dell’integrazione AEM Assets per l’estensione Commerce installata nell’istanza Commerce. |
| `version` | Stringa | Facoltativo. Versione dell&#39;applicazione Commerce installata nell&#39;istanza Commerce. |

#### CommerceCredentialsInput

Questo campo di input fornisce le credenziali OAuth per l’accesso API al catalogo Commerce. Queste credenziali sono disponibili nelle impostazioni di configurazione di Commerce [per l&#39;integrazione di Assets](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release).

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| `accessToken` | Stringa! | Il token di accesso generato per l’integrazione Assets. |
| `accessTokenSecret` | Stringa! | Il segreto del token di accesso generato per l’integrazione Assets. |
| `consumerKey` | Stringa! | La chiave consumer generata per l’integrazione di Assets. |
| `consumerSecret` | Stringa! | Segreto consumer generato per l’integrazione Assets. |

#### ExternalMatcherInput

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| assetToProductUrl | Stringa! | <!--Add field description--> |
| productToAssetUrl | Stringa! | <!--Add field description--> |
| credenziali | [ExternalMatcherCredentialsInput](#externalmatchercredentials). | Credenziali per accedere al progetto App Builder per l’integrazione AEM Assets per Commerce. |

#### ExternalMatcherCredentials

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| `oauthServerUrl` | Stringa! |    |
| `clientId` | Stringa! |      |
| `clientSecret` | Stringa! |    |
| `imsOrgId` | Stringa! | L’organizzazione IMS in cui viene eseguito il provisioning di AEM Assets e Adobe Commerce. |

#### MatchBySkuRuleInput

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| metadataField | Stringa! | Specifica il campo di metadati delle risorse da utilizzare per la corrispondenza. Usa `commerce:skus` |

#### RuleInput

Specifica la regola di corrispondenza da utilizzare per la sincronizzazione delle risorse tra Adobe Commerce e AEM Assets.

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| externalMatcher | [ExternalMatcherInput](#externalmatcherinput) | Seleziona la regola externalMatcher per la corrispondenza delle risorse e specifica i dati necessari per utilizzarla. |
| MatchBySkuRule | [MatchBySkuRuleInput](#matchbyskuruleinput) | Seleziona MatchBySkuRule per la corrispondenza delle risorse e specifica i dati necessari per utilizzarla. |

#### RuleTypeInput

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| TipoRegola | enum | Specifica un elenco di regole di corrispondenza risorse disponibili per l’integrazione AEM Assets per Commerce. I valori disponibili sono `matchBySKU` o `externalMatcher`. |

#### TenantInput

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| `aem` | [InputAem!](#aeminput) | Identifica l’istanza di AEM Assets all’interno di AEM Cloud Service in cui memorizzi le risorse Commerce. |
| `commerce` | [CommerceInput!](#commerceinput) | Fornisce informazioni sul progetto Commerce e credenziali per l&#39;accesso API |
| `enabled` | Booleano! | Abilita o disabilita la sincronizzazione delle risorse tra Adobe Commerce e AEM Assets. |
| `projectId` | Stringa! | ID progetto SaaS dalla configurazione dell&#39;identificatore SaaS del connettore dei servizi Commerce [](aem-assets-configure-commerce.md#configure-the-commerce-services-connector). |
| `rule` | [InputRegola!](#ruleinput) | Specifica la regola di corrispondenza da utilizzare per la sincronizzazione delle risorse tra Adobe Commerce e AEM Assets. Specificare `[matchBySkuRule](#matchbyskuruleinput)` o `[externalMatcher](#externalmatcherinput)`. |

### Campi di output

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| dati | [registerTenant] | Restituisce le informazioni di registrazione del tenant ed eventuali messaggi di errore provenienti dal server. |

#### RegisterTenantResponse

| Campo | Tipo di dati | Descrizione |
| ----- | --------- | ----------- |
| tenantId | Stringa! | Restituisce l&#39;ID tenant registrato. Questo ID assicura che i dati per l’integrazione di AEM Assets per Commerce vengano memorizzati e recuperati dallo spazio dati SaaS associato all’ambiente Commerce. |
| userErrors | [[userError!]!](#usererror) | Restituisce qualsiasi messaggio di errore generato dalla richiesta. |

#### UserError

| Errore | Descrizione |
|:------|:------------|
| `IMS Org ID not associated to this Commerce` | Questo errore si verifica se l&#39;ID ambiente specificato nell&#39;intestazione `Magento-Environment-Id` non è assegnato all&#39;account IMS. Questo errore può verificarsi perché l&#39;account IMS non è stato connesso quando [Commerce Services Connector](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) è stato configurato per l&#39;istanza di Commerce. |
| `Client ID is invalid` | L&#39;intestazione `x-api-key` non è corretta. |
| `Client ID is missing` | Intestazione `x-api-key` non fornita. |
| `JWT is required` | Intestazione `x-gw-signature` non fornita. |
| `JWT is invalid` | Intestazione `x-gw-signature` non fornita. |
| `Tenant already exists` | Un tenant con `mageID` specificato (tratto dal token JWT) e `saasId` (fornito dall&#39;intestazione `Magento-Environment-Id`) era già registrato. |
| `Unexpected error when connecting with AEM Assets` | Questo errore si verifica a causa di valori `programId` o `environmentId` non validi o inesistenti. |
| `Unable to connect with AEM Assets` | Questo errore può essere dovuto a due motivi:<br>1. L’account delle risorse dell’AEM è associato a un ID organizzazione IMS diverso da quello fornito per Adobe Commerce.<br>2. I metadati `commerce:isCommerce` non esistono in AEM Assets, a indicare che non sono presenti risorse approvate da inviare da AEM Assets all&#39;istanza di Commerce. |
| `Unexpected error when connecting with Commerce` | Questo errore si verifica quando viene fornito un commerce non valido `baseURL`. |
| `Unable to connect with Commerce, unauthorized` | Sono state fornite credenziali commerce non valide, con conseguente accesso non autorizzato. |
| `Invalid rule. The value must be matchBySKU or externalMatcher` | Il campo `Rule` contiene un valore errato. Per la richiesta RegisterTenant, i tipi di regole disponibili sono definiti dall&#39;enum [RuleTypeInput](#ruletypeinput). |

## Abilitare l’integrazione con Experience Manager Assets

Dopo aver registrato il tenant, l’ultimo passaggio del processo di onboarding consiste nell’abilitare l’estensione Experience Manager Assets Integration for Commerce nell’amministratore.

1. Abilita l&#39;estensione.

   1. Vai a **Archivi** > Impostazioni > **Configurazione** > **Catalogo**.

   1. Aprire la configurazione del catalogo selezionando **[!UICONTROL Catalog]**.

   1. Espandere **[!UICONTROL AEM Assets integration]**.

   1. Imposta **[!UICONTROL Integration enabled]** su `yes`.

      ![Integrazione di AEM Assets per la configurazione dell&#39;amministratore di Commerce](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}
