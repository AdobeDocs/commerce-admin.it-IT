---
title: Chiave di crittografia
description: Scopri come modificare la propria chiave di crittografia, operazione che dovrebbe essere eseguita regolarmente per migliorare la sicurezza.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 48f3431faa5db50f896b7a8e3db59421c639185b
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Chiave di crittografia

>[!NOTE]
>
>Se si è tentato di completare questi passaggi e si verificano problemi, vedere l&#39;articolo [della Knowledge Base Risoluzione dei problemi relativi alla rotazione delle chiavi di crittografia: CVE-2024-34102](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/troubleshooting-encryption-key-rotation-cve-2024-34102) .

Adobe Systems Commerce e Magento Open Source utilizzano una chiave di crittografia per proteggere password e altri dati sensibili. Un algoritmo standard [!DNL ChaCha20-Poly1305] del settore viene utilizzato con una chiave a 256 bit per crittografare tutti i dati che richiedono la crittografia. Ciò include dati di scheda di credito e password di integrazione (modulo di pagamento e spedizione). Inoltre, viene utilizzato un forte algoritmo Secure Hash (SHA-256) per eseguire l&#39;hashing di tutti i dati che non richiedono la decrittografia.

Durante l&#39;installazione iniziale, viene richiesto di consentire a Commerce di generare una chiave di crittografia o di immetterne una personalizzata. La chiave di crittografia consente strumento di modificare la chiave in base alle esigenze. La chiave di crittografia deve essere cambiata regolarmente per migliorare la sicurezza e in qualsiasi momento la chiave originale potrebbe essere compromessa.

Per informazioni tecniche, vedere [Avanzate&#39;installazione](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) locale nella Guida _all&#39;installazione_ e [Crittografia](https://developer.adobe.com/commerce/php/development/security/data-encryption/) dei dati nella _Guida per sviluppatori_ PHP.

>[!IMPORTANT]
>
>- Prima di seguire queste istruzioni per modificare la chiave di crittografia, assicurarsi che il seguente file sia scrivibile: `[your store]/app/etc/env.php`
>- La funzione di modifica della chiave di crittografia nelle impostazioni di amministrazione è deprecata ed è stata rimossa nella versione 2.4.8. È necessario utilizzare il comando CLI descritto in questa pagina per modificare la chiave di crittografia dopo l&#39;aggiornamento alla versione 2.4.8.

**Per modificare una chiave di crittografia:**

Le seguenti istruzioni richiedono accesso a un terminale.

1. Abilita [la modalità](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode) di manutenzione.

   ```bash
   bin/magento maintenance:enable
   ```

1. Disattiva cron job.

   _Progetti di infrastruttura cloud:_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _Progetti locali_

   ```bash
   crontab -e
   ```

1. Modificare la chiave di crittografia utilizzando uno dei seguenti metodi.

   +++CLI, comando

   Esegui il seguente comando CLI e assicurati che venga completato senza errori. Se è necessario crittografare nuovamente determinati valori di configurazione del sistema o campi di pagamento, vedere la guida dettagliata [sulla ri-crittografia](https://developer.adobe.com/commerce/php/development/security/data-encryption/) nella _PHP Develop Guide_.

   ```bash
   bin/magento encryption:key:change
   ```

   +++

   +++Impostazioni Amministratore

   >[!IMPORTANT]
   >
   >Questa funzione è stata deprecata ed è stata rimossa nella versione 2.4.8. Adobe Systems consiglia di modificare le chiavi di crittografia con l&#39;interfaccia della riga di comando.

   1. _Nella barra laterale Amministratore_, vai a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

      ![Chiave di crittografia del sistema](./assets/encryption-key.png){width="700" zoomable="yes"}

   1. Esegui una delle operazioni seguenti:

      - Per generare una nuova chiave, impostare **[!UICONTROL Auto-generate Key]** su `Yes`.
      - Per utilizzare una chiave diversa, impostare **[!UICONTROL Auto-generate Key]** su `No`. Quindi, immettere o incollare nel **[!UICONTROL New Key]** campo la chiave che si desidera utilizzare.

   1. Fare clic su **[!UICONTROL Change Encryption Key]**.

      >[!NOTE]
      >
      >Conservare una registrazione della nuova chiave in un luogo sicuro. È necessario per decrittografare i dati, se si verificano problemi con i file.

   +++

1. Svuota la cache.

   _Progetti di infrastruttura cloud:_

   ```bash
   magento-cloud cc
   ```

   _Progetti locali:_

   ```bash
   bin/magento cache:flush
   ```

1. Abilita cron job.

   _Progetti di infrastruttura cloud:_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _Progetti locali:_

   ```bash
   crontab -e
   ```

1. Disattiva la modalità di manutenzione.

   ```bash
   bin/magento maintenance:disable
   ```
