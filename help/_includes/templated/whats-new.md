---
source-git-commit: 78d6e7fa263246e8fa52aa0386b35e4bb39553ad
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 2%

---
# Nuovo modello

## Novità

Questa sezione contiene le modifiche apportate negli ultimi 60 giorni. Da questo elenco sono esclusi tutti gli aggiornamenti minori, ad esempio la modifica della copia.

### 10 febbraio 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrizione</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Aggiornamenti alla documentazione per l'amministratore per la versione di febbraio di Adobe Commerce as a Cloud Service:<br />- Aggiunta documentazione per <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/order-management/invoices#custom-capture-amounts">importi di acquisizione personalizzati</a> durante la creazione di fatture nell'API REST, che consente agli esercenti di acquisire importi personalizzati durante la creazione di fatture per acquisizioni parziali e scenari di pagamento specializzati.<br />- Indica quali report nel <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/start/reporting/reports-menu">menu Report</a> sono ora solo PaaS.</p>
</td>
      <td>
        Aggiornamento principale
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/0c602db5a7291b95d725bce59df53923490d6b96">commit</a></td>
    </tr>
  </tbody>
</table>

### 2 febbraio 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrizione</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Aggiornamento di <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law">Conformità alle normative sui cookie</a> per aggiungere la chiave localStorage <code class="language-plaintext highlighter-rouge">mage-cache-timeout</code> mancante e convertire l'elenco dei cookie esenti in un formato tabella.</p>
</td>
      <td>
        Tecnico, feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/ebb6348c6b5a30f5de4025f39bae0061b397a4b9">commit</a></td>
    </tr>
    <tr>
      <td><p>[!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Si applica solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} Sono stati aggiornati i prerequisiti per la configurazione dell’integrazione IMS per Adobe Commerce, al fine di fornire informazioni sulla richiesta di accesso a Adobe Admin Console.</p>
</td>
      <td>
        Tecnico, feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/8ea546c5e1cc9296c8b056ea7e25984a66d43851">commit</a></td>
    </tr>
  </tbody>
</table>

### 31 gennaio 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrizione</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>È stato aggiornato il <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-groups">Gruppo di clienti</a> nella Guida di gestione clienti per chiarire che gli utenti amministratori non possono modificare il Gruppo di clienti di un cliente dopo che il cliente è stato assegnato a una società.</p>
</td>
      <td>
        Tecnico
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/pull/81">richiesta pull</a></td>
    </tr>
  </tbody>
</table>

### 20 gennaio 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrizione</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>I riferimenti ai prodotti sono stati modificati da "Adobe Sensei" a "Adobe AI" per riflettere gli aggiornamenti di branding di Adobe.</p>
</td>
      <td>
        Feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/4077b922dae0ed9a9050a5f6160143a636646daa">commit</a></td>
    </tr>
  </tbody>
</table>

### 16 gennaio 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrizione</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>È stata aggiunta una precisazione quando sono disponibili <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/config/sales/sales-emails#order-ready-for-pickup-in-store">e-mail pronte per il ritiro nello store</a>.</p>
</td>
      <td>
        Feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/65fd67dcd3c14daddfc0f36493dc6da3630898a1">commit</a></td>
    </tr>
  </tbody>
</table>

### 15 gennaio 2026

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrizione</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>Sono state aggiunte le seguenti funzionalità ad Adobe Commerce as a Cloud Service:<br />- È stato aggiunto il supporto per <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/captcha/security-google-recaptcha-enterprise">Google reCAPTCHA Enterprise</a>, che fornisce protezione avanzata da bot con funzionalità di analisi dei rischi adattivi e machine learning.<br />- Trasforma i numeri di registrazione spedizione inclusi nelle e-mail dei clienti da testo normale in collegamenti cliccabili <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/delivery/shipping-settings#shipment-tracking-urls">abilitando gli URL di tracciamento personalizzati</a>. Questa funzione è supportata per USPS, UPS, FedEx e DHL.<br />- È ora possibile combinare gli sconti per prezzi su più livelli con gli sconti per le regole del catalogo utilizzando <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/pricing/product-price-tier#enable-tier-pricing-for-catalog-price-rules">regole prezzo catalogo</a>. Questo miglioramento consente di creare strategie di prezzo più dinamiche e competitive.</p>
</td>
      <td>
        Aggiornamento principale, nuovo argomento
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/70e73b47c4b0342ade3deab64dbe39f29b82191f">commit</a></td>
    </tr>
  </tbody>
</table>

### 17 dicembre 2025

<table style="table-layout:auto;">
  <thead>
    <tr>
      <th>Descrizione</th>
      <th>Tipo</th>
      <th>Source</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><p>È stato aggiornato l'argomento <a href="https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty">Premi e fedeltà</a> per chiarire come vengono calcolate le imposte quando i clienti utilizzano punti premio o memorizzano il credito durante l'acquisto.</p>
</td>
      <td>
        Feedback
      </td>
      <td><a href="https://github.com/AdobeDocs/commerce-admin.en/commit/1154cd5ced746ac6dfd609946528f281774bbaaa">commit</a></td>
    </tr>
  </tbody>
</table>
