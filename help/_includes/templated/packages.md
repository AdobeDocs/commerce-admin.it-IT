---
source-git-commit: a37e67c332140fbba7609db8cc5e22a3625a1c9d
workflow-type: tm+mt
source-wordcount: '2387'
ht-degree: 0%

---
# Adobe Commerce con pacchetti B2B

<!-- The 'packages' variable contains the 'packages' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'packages-dev' variable contains the 'packages-dev' node of the '_data/codebase/b2b/composer_lock.json' file
 -->

<!-- The 'product' variable contains data of the 'magento/product-enterprise-edition' package
 -->

<!-- The edition variable contains `commerce-b2b` value from the _data/names.yml file
 -->

Adobe Commerce B2B utilizza Composer per gestire i pacchetti PHP.

Il file `composer.json` dichiara l&#39;elenco dei pacchetti, mentre il file `composer.lock` memorizza un elenco completo dei pacchetti (una versione completa di ciascun pacchetto e delle relative dipendenze) utilizzati per creare un&#39;installazione di Adobe Commerce B2B.

La seguente documentazione di riferimento è generata dal file `composer.lock` e riguarda i pacchetti richiesti inclusi in Adobe Commerce B2B 1.5.2.

## Dipendenze

`magento/extension-b2b 1.5.2` ha le seguenti dipendenze:

- magento/framework: >=103.0.6 &lt;103.0.9
- magento/magento2-b2b-base: 1.5.2
- [magento/module-b2b](https://developer.adobe.com/commerce/php/module-reference/module-b2b/): 100.5.2
- [magento/module-bundle-NEGOTIable-quote](https://developer.adobe.com/commerce/php/module-reference/module-bundle-negotiable-quote/): 100.5.1
- [magento/module-bundle-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list/): 100.5.1
- [magento/module-bundle-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-bundle-requisition-list-graph-ql/): 1.5.1
- [magento/module-bundle-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-bundle-shared-catalog/): 100.5.1
- [magento/module-checkout-address-search-NEGOTIable-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-address-search-negotiable-quote/): 100.5.1
- [magento/module-checkout-agreements-NEGOTIable-quote](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-negotiable-quote/): 100.5.1
- [magento/module-checkout-agreements-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-checkout-agreements-purchase-order/): 1.5.1
- [magento/module-company](https://developer.adobe.com/commerce/php/module-reference/module-company/): 102.0.2
- [magento/module-company-asynchronous-operations](https://developer.adobe.com/commerce/php/module-reference/module-company-asynchronous-operations/): 1.5.1
- [magento/module-company-credit](https://developer.adobe.com/commerce/php/module-reference/module-company-credit/): 100.5.2
- [magento/module-company-credit-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-credit-graph-ql/): 1.5.1
- [magento/module-company-customer-import-export](https://developer.adobe.com/commerce/php/module-reference/module-company-customer-import-export/): 1.5.0
- [magento/module-company-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-graph-ql/): 1.5.2
- [magento/module-company-NEGOTIable-quote](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote/): 1.5.1
- [magento/module-company-NEGOTIable-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-company-negotiable-quote-template/): 1.5.1
- [magento/module-company-payment](https://developer.adobe.com/commerce/php/module-reference/module-company-payment/): 100.5.1
- [magento/module-company-quote](https://developer.adobe.com/commerce/php/module-reference/module-company-quote/): 1.5.2
- [magento/module-company-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-company-quote-graph-ql/): 1.5.2
- [magento/module-company-relation](https://developer.adobe.com/commerce/php/module-reference/module-company-relation/): 1.5.2
- [magento/module-company-relation-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-company-relation-shared-catalog/): 1.5.1
- [magento/module-company-shipping](https://developer.adobe.com/commerce/php/module-reference/module-company-shipping/): 1.5.1
- [magento/module-configurable-NEGOTIable-quote](https://developer.adobe.com/commerce/php/module-reference/module-configurable-negotiable-quote/): 100.5.1
- [magento/module-configurable-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list/): 100.5.1
- [magento/module-configurable-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-configurable-requisition-list-graph-ql/): 1.5.1
- [magento/module-configurable-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-configurable-shared-catalog/): 100.5.1
- [magento/module-downloadable-company](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-company/): 1.5.1
- [magento/module-downloadable-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-downloadable-requisition-list-graph-ql/): 1.5.1
- [magento/module-gift-card-NEGOTIable-quote](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-negotiable-quote/): 100.5.1
- [magento/module-gift-card-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list/): 100.5.1
- [magento/module-gift-card-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-requisition-list-graph-ql/): 1.5.1
- [magento/module-gift-card-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-gift-card-shared-catalog/): 100.5.1
- [magento/module-grouped-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-grouped-requisition-list/): 100.5.1
- [magento/module-grouped-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-grouped-shared-catalog/): 100.5.1
- [magento/module-tradable-quote](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote/): 101.0.2
- [magento/module-tradable-quote-async-order](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-async-order/): 1.5.1
- [magento/module-tradable-quote-duplicate](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate/): 1.5.2
- [magento/module-tradable-quote-duplicate-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-duplicate-graph-ql/): 1.5.1
- [magento/module-tradable-quote-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-graph-ql/): 1.5.1
- [magento/module-tradable-quote-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list/): 1.5.1
- [magento/module-tradable-quote-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-requisition-list-graph-ql/): 1.5.1
- [magento/module-tradable-quote-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-shared-catalog/): 100.5.1
- [magento/module-tradable-quote-template](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template/): 1.5.2
- [magento/module-tradable-quote-template-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-graph-ql/): 1.5.2
- [magento/module-tradable-quote-template-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-template-shared-catalog/): 1.5.1
- [magento/module-tradable-quote-weee](https://developer.adobe.com/commerce/php/module-reference/module-negotiable-quote-weee/): 100.5.1
- [magento/module-order-history-search](https://developer.adobe.com/commerce/php/module-reference/module-order-history-search/): 100.5.2
- [magento/module-paypal-NEGOTIable-quote](https://developer.adobe.com/commerce/php/module-reference/module-paypal-negotiable-quote/): 1.5.1
- [magento/module-paypal-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-paypal-purchase-order/): 1.5.1
- [magento/module-purchase-order](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order/): 100.5.2
- [magento/module-purchase-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-graph-ql/): 1.5.1
- [magento/module-purchase-order-rule](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule/): 100.5.2
- [magento/module-purchase-order-rule-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-purchase-order-rule-graph-ql/): 1.5.1
- [magento/module-quick-order](https://developer.adobe.com/commerce/php/module-reference/module-quick-order/): 100.5.1
- [magento/module-quick-order-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-quick-order-graph-ql/): 1.5.1
- [magento/module-requisition-list](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list/): 100.5.2
- [magento/module-requisition-list-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-requisition-list-graph-ql/): 1.5.1
- [magento/module-shared-catalog](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog/): 100.5.2
- [magento/module-shared-catalog-graph-ql](https://developer.adobe.com/commerce/php/module-reference/module-shared-catalog-graph-ql/): 1.5.1
- magento/security-package-b2b: 1.0.6

## Licenze di terze parti

### Apache-2.0, solo LGPL-2.1

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/opensearch-project/opensearch-php">opensearch-project/opensearch-php</a>
    </td>
    <td>Libreria</td>
    <td>Client PHP per OpenSearch</td>
  </tr>
  </tbody>
</table>

### Apache-2.0

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/adobe/stock-api-libphp">astock/stock-api-libphp</a>
    </td>
    <td>Libreria</td>
    <td>Libreria API di Adobe Stock</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/awslabs/aws-crt-php">aws/aws-crt-php</a>
    </td>
    <td>Libreria</td>
    <td>Common Runtime di AWS per PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/aws/aws-sdk-php">aws/aws-sdk-php</a>
    </td>
    <td>Libreria</td>
    <td>AWS SDK per PHP - Utilizzare Amazon Web Services nel progetto PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/api">open-telemetry/api</a>
    </td>
    <td>Libreria</td>
    <td>API per OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/opentelemetry-php/context">telemetria aperta/contesto</a>
    </td>
    <td>Libreria</td>
    <td>Implementazione contestuale per OpenTelemetry PHP.</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree
    </td>
    <td>Metapackage</td>
    <td>Braintree Magento</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/wikimedia/less.php">wikimedia/less.php</a>
    </td>
    <td>Libreria</td>
    <td>Porta PHP del processore LESS</td>
  </tr>
  </tbody>
</table>

### Clausola BSD-2

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/Bacon/BaconQrCode">bacon/bacon-qr-code</a>
    </td>
    <td>Libreria</td>
    <td>BaconQrCode è un generatore di codici QR per PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/DASPRiD/Enum">dasprid/enum</a>
    </td>
    <td>Libreria</td>
    <td>Implementazione PHP 7.1 enum</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webimpress/safe-writer">webimpress/safe-writer</a>
    </td>
    <td>Libreria</td>
    <td>Strumento per scrivere i file in modo sicuro, per evitare race condition</td>
  </tr>
  </tbody>
</table>

### Clausola BSD-3

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_File">colinmollenhour/cache-backend-file</a>
    </td>
    <td>Modulo Magento</td>
    <td>Il backend Zend_Cache_Backend_File di magazzino ha prestazioni estremamente scadenti per la pulizia da parte dei tag, rendendolo inutilizzabile con l’aumento del numero di elementi memorizzati in cache. Questo back-end apporta molte modifiche che determinano un notevole miglioramento delle prestazioni, in particolare per la pulizia dei tag.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/php-redis-session-abstract">colinmollenhour/php-redis-session-abstract</a>
    </td>
    <td>Libreria</td>
    <td>Un gestore di sessione basato su Redis con blocco ottimistico</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/duosecurity/duo_universal_php">duosecurity/duo_universal_php</a>
    </td>
    <td>Libreria</td>
    <td>Un'implementazione PHP del Duo Universal SDK.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/firebase/php-jwt">firebase/php-jwt</a>
    </td>
    <td>Libreria</td>
    <td>Una semplice libreria per codificare e decodificare i token web JSON (JWT) in PHP. Deve essere conforme alla specifica corrente.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-captcha">laminas/laminas-captcha</a>
    </td>
    <td>Libreria</td>
    <td>Generare e convalidare i CAPTCHA utilizzando figure, immagini, ReCaptcha e altro ancora</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-code">laminas/laminas-code</a>
    </td>
    <td>Libreria</td>
    <td>Estensioni dell'API PHP Reflection, scansione del codice statico e generazione del codice</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-config">laminas/laminas-config</a>
    </td>
    <td>Libreria</td>
    <td>fornisce un'interfaccia utente basata su proprietà di oggetto nidificato per accedere ai dati di configurazione nel codice dell'applicazione</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-di">laminas/laminas-di</a>
    </td>
    <td>Libreria</td>
    <td>Iniezione di dipendenza automatica per contenitori PSR-11</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-escaper">laminas/laminas-escape</a>
    </td>
    <td>Libreria</td>
    <td>Escape sicuro e protetto di HTML, attributi HTML, JavaScript, CSS e URL</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-eventmanager">laminas/laminas-eventmanager</a>
    </td>
    <td>Libreria</td>
    <td>Attivare e ascoltare gli eventi all'interno di un'applicazione PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-feed">laminas/laminas-feed</a>
    </td>
    <td>Libreria</td>
    <td>fornisce funzionalità per creare e utilizzare feed RSS e Atom</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-filter">laminas/laminas-filter</a>
    </td>
    <td>Libreria</td>
    <td>Filtrare e normalizzare a livello di programmazione dati e file</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-http">laminas/laminas-http</a>
    </td>
    <td>Libreria</td>
    <td>Interfaccia semplice per l'esecuzione di richieste HTTP (Hyper-Text Transfer Protocol)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-i18n">laminas/laminas-i18n</a>
    </td>
    <td>Libreria</td>
    <td>Fornisci le traduzioni per la tua applicazione, e filtra e convalida i valori internazionalizzati</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-json">laminas/laminas-json</a>
    </td>
    <td>Libreria</td>
    <td>fornisce metodi di convenienza per serializzare da PHP nativo a JSON e decodificare da JSON a PHP nativo</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-loader">laminas/laminas-loader</a>
    </td>
    <td>Libreria</td>
    <td>Strategie di caricamento automatico e plug-in</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-modulemanager">laminas/laminas-modulemanager</a>
    </td>
    <td>Libreria</td>
    <td>Sistema modulare per applicazioni laminas-mvc</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-mvc">laminas/laminas-mvc</a>
    </td>
    <td>Libreria</td>
    <td>Livello MVC basato su eventi di Laminas, incluse applicazioni MVC, controller e plug-in</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-permissions-acl">laminas/laminas-permissions-acl</a>
    </td>
    <td>Libreria</td>
    <td>Implementazione di un elenco di controllo di accesso (ACL) leggero e flessibile per la gestione dei privilegi</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-recaptcha">laminas/laminas-recaptcha</a>
    </td>
    <td>Libreria</td>
    <td>Wrapper OOP per il servizio Web ReCaptcha</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-router">laminas/laminas-router</a>
    </td>
    <td>Libreria</td>
    <td>Sistema di routing flessibile per applicazioni HTTP e console</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-server">laminas/laminas-server</a>
    </td>
    <td>Libreria</td>
    <td>Creazione di server RPC basati su riflessioni</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-servicemanager">laminas/laminas-servicemanager</a>
    </td>
    <td>Libreria</td>
    <td>Contenitore Di Iniezione Di Dipendenza Basato Su Fabbrica</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-session">laminas/laminas-session</a>
    </td>
    <td>Libreria</td>
    <td>Interfaccia orientata agli oggetti per sessioni PHP e storage</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-soap">laminati/sapone laminato</a>
    </td>
    <td>Libreria</td>
    <td></td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-stdlib">laminas/laminas-stdlib</a>
    </td>
    <td>Libreria</td>
    <td>Estensioni SPL, utility di array, gestori di errori e altro ancora</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-text">laminas/laminas-text</a>
    </td>
    <td>Libreria</td>
    <td>Creare i file FIGlet e le tabelle basate su testo</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-translator">laminas/laminas-translator</a>
    </td>
    <td>Libreria</td>
    <td>Interfacce per il componente Translator del laminas-i18n</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-uri">laminas/laminas-uri</a>
    </td>
    <td>Libreria</td>
    <td>Componente che facilita la manipolazione e la convalida degli URI (Uniform Resource Identifiers)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-validator">laminas/laminas-validator</a>
    </td>
    <td>Libreria</td>
    <td>Classi di convalida per un'ampia gamma di domini e possibilità di concatenare le convalide per creare criteri di convalida complessi</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/laminas/laminas-view">laminas/laminas-view</a>
    </td>
    <td>Libreria</td>
    <td>Livello di vista flessibile che supporta e fornisce più livelli di vista, helper e altro ancora</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/marc-mabe/php-enum">marc-mabe/php-enum</a>
    </td>
    <td>Libreria</td>
    <td>Implementazione semplice e rapida delle enumerazioni con PHP nativo</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/nikic/PHP-Parser">nikic/php-parser</a>
    </td>
    <td>Libreria</td>
    <td>Un parser PHP scritto in PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpfui/recaptcha">phpfui/recaptcha</a>
    </td>
    <td>Libreria</td>
    <td>Libreria client per reCAPTCHA di Google per PHP 8.4 e versioni successive</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tedious/JShrink">tedivm/jshrink</a>
    </td>
    <td>Libreria</td>
    <td>PHP integrato nel minifier JavaScript</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/tubalmartin/YUI-CSS-compressor-PHP-port">tubalmartin/cssmin</a>
    </td>
    <td>Libreria</td>
    <td>Porta PHP del compressore CSS YUI</td>
  </tr>
  </tbody>
</table>

### Modifica clausola BSD-3

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/Cm_Cache_Backend_Redis">colinmollenhour/cache-backend-redis</a>
    </td>
    <td>Modulo Magento</td>
    <td>Zend_Cache back-end che utilizza Redis con supporto completo per i tag.</td>
  </tr>
  </tbody>
</table>

### ISC

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/paragonie/sodium_compat">paragonie/sodio_compat</a>
    </td>
    <td>Libreria</td>
    <td>Pura implementazione PHP di libsodium; utilizza l’estensione PHP, se presente</td>
  </tr>
  </tbody>
</table>

### LGPL-2.1-or-later

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/ezyang/htmlpurifier">ezyang/htmlpurificer</a>
    </td>
    <td>Libreria</td>
    <td>Filtro HTML conforme agli standard scritto in PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-amqplib/php-amqplib">php-amqplib/php-amqplib</a>
    </td>
    <td>Libreria</td>
    <td>Ex videlalvaro/php-amqplib.  Questa libreria è un’implementazione PHP pura del protocollo AMQP. È stato testato contro RabbitMQ.</td>
  </tr>
  </tbody>
</table>

### MIT

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/braintree/braintree_php">albero del cervello/albero del cervello_php</a>
    </td>
    <td>Libreria</td>
    <td>Libreria client Braintree PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/math">brick/matematica</a>
    </td>
    <td>Libreria</td>
    <td>Libreria aritmetica di precisione arbitraria</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/brick/varexporter">brick/varexporter</a>
    </td>
    <td>Libreria</td>
    <td>Una potente alternativa a var_export(), che può esportare chiusure e oggetti senza __set_state()</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ChristianRiesen/base32">cristiano-riesen/base32</a>
    </td>
    <td>Libreria</td>
    <td>Codificatore/decodificatore Base32 secondo RFC 4648</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/colinmollenhour/credis">colinmollenhour/credis</a>
    </td>
    <td>Libreria</td>
    <td>Credis è un’interfaccia leggera dell’archivio Redis di valori chiave che racchiude la libreria phpredis quando disponibile per prestazioni migliori.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/ca-bundle">compositore/ca-bundle</a>
    </td>
    <td>Libreria</td>
    <td>Consente di trovare un percorso per il bundle CA di sistema e include un fallback al bundle CA di Mozilla.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/class-map-generator">compositore/class-map-generator</a>
    </td>
    <td>Libreria</td>
    <td>Utilità per scansionare il codice PHP e generare mappe di classe.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/composer">compositore/compositore</a>
    </td>
    <td>Libreria</td>
    <td>Composer consente di dichiarare, gestire e installare le dipendenze dei progetti PHP. Ti garantisce di avere la giusta pila ovunque.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/metadata-minifier">compositore/minificatore metadati</a>
    </td>
    <td>Libreria</td>
    <td>Piccola libreria di utilità che gestisce la minimizzazione e l'espansione dei metadati.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/pcre">compositore/pcre</a>
    </td>
    <td>Libreria</td>
    <td>Libreria di wrapping PCRE che offre sostituzioni preg_* di tipo sicuro.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/semver">compositore/semver</a>
    </td>
    <td>Libreria</td>
    <td>Libreria semver che offre utility, analisi e convalida dei vincoli di versione.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/spdx-licenses">licenze compositore/spdx</a>
    </td>
    <td>Libreria</td>
    <td>Elenco licenze SPDX e libreria di convalida.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/composer/xdebug-handler">compositore/xdebug-handler</a>
    </td>
    <td>Libreria</td>
    <td>Riavvia un processo senza Xdebug.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/doctrine/lexer">dottrina/lexer</a>
    </td>
    <td>Libreria</td>
    <td>Libreria parser PHP Doctrine Lexer che può essere utilizzata nei parser discendenti ricorsivi top-down.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/egulias/EmailValidator">egulias/email-validator</a>
    </td>
    <td>Libreria</td>
    <td>Libreria per la convalida delle e-mail rispetto a diverse RFC</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elastic-transport-php">elastico/trasporto</a>
    </td>
    <td>Libreria</td>
    <td>Libreria PHP per trasporto HTTP per prodotti elastici</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/elastic/elasticsearch-php">elasticsearch/elasticsearch</a>
    </td>
    <td>Libreria</td>
    <td>Client PHP per Elasticsearch</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/endroid/qr-code">endroid/qr-code</a>
    </td>
    <td>Libreria</td>
    <td>Codice QR Endroid</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/guzzlestreams">ezimuel/guzzlestreams</a>
    </td>
    <td>Libreria</td>
    <td>Forcella di guzzle/ruscelli (abbandonati) da utilizzare con elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ezimuel/ringphp">ezimuel/ringphp</a>
    </td>
    <td>Libreria</td>
    <td>Forchetta di guzzle/RingPHP (abbandonato) da utilizzare con elasticsearch-php</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/guzzle">guzzlehttp/guzzle</a>
    </td>
    <td>Libreria</td>
    <td>Guzzle è una libreria client HTTP PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/promises">guzzlehttp/promise</a>
    </td>
    <td>Libreria</td>
    <td>Libreria Guzzle promesse</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/guzzle/psr7">guzzlehttp/psr7</a>
    </td>
    <td>Libreria</td>
    <td>Implementazione del messaggio PSR-7 che fornisce anche metodi di utilità comuni</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jsonrainbow/json-schema">justinrainbow/json-schema</a>
    </td>
    <td>Libreria</td>
    <td>Libreria per convalidare uno schema JSON.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem">lega/flysystem</a>
    </td>
    <td>Libreria</td>
    <td>Estrazione archiviazione file per PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-aws-s3-v3">league/flysystem-aws-s3-v3</a>
    </td>
    <td>Libreria</td>
    <td>Scheda di file system AWS S3 per Flysystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/flysystem-local">lega/flysystem-locale</a>
    </td>
    <td>Libreria</td>
    <td>Adattatore di file system locale per Flysystem.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/thephpleague/mime-type-detection">league/mime-type-detection</a>
    </td>
    <td>Libreria</td>
    <td>Rilevamento del tipo MIME per Flysystem</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/monolog">monologo/monologo</a>
    </td>
    <td>Libreria</td>
    <td>Invia i registri a file, socket, caselle in entrata, database e vari servizi web</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/jmespath/jmespath.php">mtdowling/jmespath.php</a>
    </td>
    <td>Libreria</td>
    <td>Specificare in modo dichiarativo come estrarre elementi da un documento JSON</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/constant_time_encoding">paragonie/constant_time_encoding</a>
    </td>
    <td>Libreria</td>
    <td>Implementazioni a tempo costante della codifica RFC 4648 (Base-64, Base-32, Base-16)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/paragonie/random_compat">paragonie/random_compat</a>
    </td>
    <td>Libreria</td>
    <td>polyfill PHP 5.x per random_bytes() e random_int() da PHP 7</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/emogrifier">pelago/emoglificatore</a>
    </td>
    <td>Libreria</td>
    <td>Converte gli stili CSS in attributi di stile in linea nel codice HTML</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/discovery">php-http/discovery</a>
    </td>
    <td>Composer-plugin</td>
    <td>Trova e installa le implementazioni PSR-7, PSR-17, PSR-18 e HTTPlug</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/httplug">php-http/httplug</a>
    </td>
    <td>Libreria</td>
    <td>HTTPlug, astrazione del client HTTP per PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-http/promise">php-http/promise</a>
    </td>
    <td>Libreria</td>
    <td>Promessa utilizzata per le richieste HTTP asincrone</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/CssXPath">phpgt/cssxpath</a>
    </td>
    <td>Libreria</td>
    <td>Converti selettori CSS in query XPath.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/Dom">phpgt/dom</a>
    </td>
    <td>Libreria</td>
    <td>API DOM moderna.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/PhpGt/PropFunc">phpgt/propfunc</a>
    </td>
    <td>Libreria</td>
    <td>Funzioni della funzione di accesso alle proprietà e del mutatore.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/mcrypt_compat">phpseclib/mcrypt_compat</a>
    </td>
    <td>Libreria</td>
    <td>Poliriempimento PHP 5.x-8.x per estensione mcrypt</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/phpseclib/phpseclib">phpseclib/phpseclib</a>
    </td>
    <td>Libreria</td>
    <td>Libreria PHP Secure Communications: implementazioni Pure-PHP di RSA, AES, SSH2, SFTP, X.509 ecc.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/cache">psr/cache</a>
    </td>
    <td>Libreria</td>
    <td>Interfaccia comune per il caching delle librerie</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/clock">psr/clock</a>
    </td>
    <td>Libreria</td>
    <td>Interfaccia comune per la lettura dell'orologio.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/container">psr/container</a>
    </td>
    <td>Libreria</td>
    <td>Interfaccia comune dei contenitori (PHP FIG PSR-11)</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/event-dispatcher">psr/event-dispatcher</a>
    </td>
    <td>Libreria</td>
    <td>Interfacce standard per la gestione degli eventi.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-client">psr/http-client</a>
    </td>
    <td>Libreria</td>
    <td>Interfaccia comune per i client HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-factory">psr/http-factory</a>
    </td>
    <td>Libreria</td>
    <td>PSR-17: interfacce comuni per i message factory HTTP PSR-7</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/http-message">psr/http-message</a>
    </td>
    <td>Libreria</td>
    <td>Interfaccia comune per i messaggi HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/php-fig/log">psr/log</a>
    </td>
    <td>Libreria</td>
    <td>Interfaccia comune per le librerie di registrazione</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ralouphie/getallheaders">ralouphie/getallheaders</a>
    </td>
    <td>Libreria</td>
    <td>Un polyfill per getallheaders.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/collection">ramsey/collection</a>
    </td>
    <td>Libreria</td>
    <td>Libreria PHP per la rappresentazione e la manipolazione delle raccolte.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/ramsey/uuid">ramsey/uuid</a>
    </td>
    <td>Libreria</td>
    <td>Libreria PHP per la generazione e l’utilizzo di identificatori universalmente univoci (UUID).</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/reactphp/promise">react/promise</a>
    </td>
    <td>Libreria</td>
    <td>Implementazione leggera di CommonJS Promises/A per PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/MyIntervals/PHP-CSS-Parser">sabberworm/php-css-parser</a>
    </td>
    <td>Libreria</td>
    <td>Parser per file CSS scritti in PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/jsonlint">seld/jsonlint</a>
    </td>
    <td>Libreria</td>
    <td>Linter JSON</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/phar-utils">seld/phar-utils</a>
    </td>
    <td>Libreria</td>
    <td>PHAR formato file utilità, per quando PHP phars si up</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Seldaek/signal-handler">seld/signal-handler</a>
    </td>
    <td>Libreria</td>
    <td>Semplice gestore di segnali unix che genera un errore silenzioso quando i segnali non sono supportati per un facile sviluppo su più piattaforme</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/aes-key-wrap">spomky-labs/aes-key-wrap</a>
    </td>
    <td>Libreria</td>
    <td>Key Wrap AES per PHP.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/otphp">spomky-labs/otphp</a>
    </td>
    <td>Libreria</td>
    <td>Libreria PHP per la generazione di password monouso secondo l'RFC 4226 (HOTP Algorithm) e l'RFC 6238 (TOTP Algorithm) e compatibile con Google Authenticator</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/Spomky-Labs/pki-framework">spomky-labs/pki-framework</a>
    </td>
    <td>Libreria</td>
    <td>Un framework PHP per la gestione dell'infrastruttura a chiave pubblica. Comprende certificati a chiave pubblica X.509, certificati di attributi, richieste di certificazione e convalida del percorso di certificazione.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/config">symfony/config</a>
    </td>
    <td>Libreria</td>
    <td>Consente di trovare, caricare, combinare, riempire automaticamente e convalidare i valori di configurazione di qualsiasi tipo</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/console">symfony/console</a>
    </td>
    <td>Libreria</td>
    <td>Semplifica la creazione di interfacce per riga di comando belle e testabili</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/css-selector">symfony/css-selector</a>
    </td>
    <td>Libreria</td>
    <td>Converte i selettori CSS in espressioni XPath</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/dependency-injection">symfony/dependency-injection</a>
    </td>
    <td>Libreria</td>
    <td>Consente di standardizzare e centralizzare il modo in cui gli oggetti vengono costruiti nell'applicazione</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/deprecation-contracts">symfony/deprecation-CONTRACTS</a>
    </td>
    <td>Libreria</td>
    <td>Funzione e convenzione generiche per attivare gli avvisi di deprecazione</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/error-handler">symfony/error-handler</a>
    </td>
    <td>Libreria</td>
    <td>Fornisce strumenti per gestire gli errori e facilitare il debug del codice PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher">symfony/event-dispatcher</a>
    </td>
    <td>Libreria</td>
    <td>Fornisce strumenti che consentono ai componenti dell'applicazione di comunicare tra loro inviando eventi e ascoltandoli</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/event-dispatcher-contracts">symfony/event-dispatcher-CONTRACTS</a>
    </td>
    <td>Libreria</td>
    <td>Astrazioni generiche correlate all’evento dispatching</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/filesystem">symfony/filesystem</a>
    </td>
    <td>Libreria</td>
    <td>Fornisce utilità di base per il file system</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/finder">symfony/finder</a>
    </td>
    <td>Libreria</td>
    <td>Trova file e directory tramite un'interfaccia intuitiva</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client">symfony/http-client</a>
    </td>
    <td>Libreria</td>
    <td>Fornisce potenti metodi per recuperare le risorse HTTP in modo sincrono o asincrono</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-client-contracts">symfony/http-client-CONTRACTS</a>
    </td>
    <td>Libreria</td>
    <td>Astrazioni generiche correlate ai client HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-foundation">symfony/http-foundation</a>
    </td>
    <td>Libreria</td>
    <td>Definisce un livello orientato agli oggetti per la specifica HTTP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/http-kernel">symfony/http-kernel</a>
    </td>
    <td>Libreria</td>
    <td>Fornisce un processo strutturato per convertire una richiesta in una risposta</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/intl">symfony/intl</a>
    </td>
    <td>Libreria</td>
    <td>Consente di accedere ai dati di localizzazione della libreria ICU</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mailer">symfony/mailer</a>
    </td>
    <td>Libreria</td>
    <td>Aiuta a inviare e-mail</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/mime">symfony/mime</a>
    </td>
    <td>Libreria</td>
    <td>Consente la manipolazione dei messaggi MIME</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-ctype">symfony/polyfill-ctype</a>
    </td>
    <td>Libreria</td>
    <td>Symfony polyfill per funzioni di tipo</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-grapheme">symfony/polyfill-intl-grapheme</a>
    </td>
    <td>Libreria</td>
    <td>Symfony polyfill per le funzioni grapheme_* di intl</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-idn">symfony/polyfill-intl-idn</a>
    </td>
    <td>Libreria</td>
    <td>Symfony polyfill per le funzioni intl idn_to_ascii e idn_to_utf8</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-intl-normalizer">symfony/polyfill-intl-normalizer</a>
    </td>
    <td>Libreria</td>
    <td>Symfony polyfill per la classe Normalizer di intl e funzioni correlate</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-mbstring">symfony/polyfill-mbstring</a>
    </td>
    <td>Libreria</td>
    <td>Symfony polyfill per l’estensione Mbstring</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php73">symfony/polyfill-php73</a>
    </td>
    <td>Libreria</td>
    <td>Symfony polyfill supporta alcune funzioni PHP 7.3+ per ridurre le versioni PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php80">symfony/polyfill-php80</a>
    </td>
    <td>Libreria</td>
    <td>Symfony polyfill supporta alcune funzioni PHP 8.0+ per ridurre le versioni PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php81">symfony/polyfill-php81</a>
    </td>
    <td>Libreria</td>
    <td>Symfony polyfill supporta alcune funzioni PHP 8.1+ per ridurre le versioni PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php82">symfony/polyfill-php82</a>
    </td>
    <td>Libreria</td>
    <td>Symfony polyfill supporta alcune funzioni PHP 8.2+ per ridurre le versioni PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/polyfill-php83">symfony/polyfill-php83</a>
    </td>
    <td>Libreria</td>
    <td>Symfony polyfill supporta alcune funzioni PHP 8.3+ per ridurre le versioni PHP</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/process">symfony/process</a>
    </td>
    <td>Libreria</td>
    <td>Esegue comandi nei sottoprocessi</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/service-contracts">symfony/service-CONTRACTS</a>
    </td>
    <td>Libreria</td>
    <td>Astrazioni generiche relative ai servizi di scrittura</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/string">symfony/string</a>
    </td>
    <td>Libreria</td>
    <td>Fornisce un’API orientata agli oggetti per stringhe e tratta byte, punti di codice UTF-8 e cluster di grafemi in modo unificato</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-dumper">symfony/var-dumper</a>
    </td>
    <td>Libreria</td>
    <td>Fornisce meccanismi per passare attraverso qualsiasi variabile PHP arbitraria</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/var-exporter">symfony/var-exporter</a>
    </td>
    <td>Libreria</td>
    <td>Consente l'esportazione di qualsiasi struttura di dati PHP serializzabile nel codice PHP normale</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/symfony/yaml">symfony/yaml</a>
    </td>
    <td>Libreria</td>
    <td>Carica ed esegue il dump dei file YAML</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/web-token/jwt-framework">web-token/jwt-framework</a>
    </td>
    <td>Symfony-bundle</td>
    <td>Libreria di firma di oggetti e crittografia JSON per PHP e Symfony Bundle.</td>
  </tr>
  <tr>
    <td>
      <a href="https://github.com/webonyx/graphql-php">webonyx/graphql-php</a>
    </td>
    <td>Libreria</td>
    <td>Una porta PHP dell'implementazione di riferimento GraphQL</td>
  </tr>
  </tbody>
</table>

### OSL-3.0, AFL-3.0

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-customer-balance
    </td>
    <td>Modulo Magento2</td>
    <td>N/D</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card
    </td>
    <td>Modulo Magento2</td>
    <td>N/D</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-card-account
    </td>
    <td>Modulo Magento2</td>
    <td>N/D</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-gift-wrapping
    </td>
    <td>Modulo Magento2</td>
    <td>N/D</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-graph-ql
    </td>
    <td>Modulo Magento2</td>
    <td>N/D</td>
  </tr>
  <tr>
    <td>
      paypal/module-braintree-reward
    </td>
    <td>Modulo Magento2</td>
    <td>N/D</td>
  </tr>
  </tbody>
</table>

### OSL-3.0

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### PHP

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      <a href="https://github.com/2tvenom/CBOREncode">2tvenom/cborencode</a>
    </td>
    <td>Libreria</td>
    <td>Codificatore CBOR per PHP</td>
  </tr>
  </tbody>
</table>

### Proprietario

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>

### proprietario

<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Tipo</th>
      <th>Descrizione</th>
    </tr>
  </thead>
  <tbody>
  <tr>
    <td>
      paypal/module-braintree-core
    </td>
    <td>Modulo Magento2</td>
    <td>Effettua il forking dal modulo Magento Braintree 2.2.0 di Gene Commerce per PayPal.</td>
  </tr>
  </tbody>
</table>
