---
title: Chiave di crittografia
description: Scopri come generare automaticamente o aggiungere la tua chiave di crittografia, che deve essere modificata regolarmente per migliorare la sicurezza.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 21be3c7a56cb72d685b2b3605bc27266e8e55f37
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Chiave di crittografia

Adobe Commerce e il Magento Open Source utilizzano una chiave di crittografia per proteggere le password e altri dati sensibili. Viene utilizzato un algoritmo [!DNL ChaCha20-Poly1305] standard del settore con una chiave a 256 bit per crittografare tutti i dati che richiedono la crittografia. Ciò include i dati della carta di credito e le password di integrazione (modulo di pagamento e spedizione). Inoltre, viene utilizzato un forte algoritmo di hash sicuro (SHA-256) per eseguire l’hashing di tutti i dati che non richiedono decrittografia.

Durante l&#39;installazione iniziale, viene richiesto di consentire a Commerce di generare una chiave di crittografia o di immetterne una propria. Lo strumento per la chiave di crittografia consente di modificare la chiave in base alle esigenze. La chiave di crittografia deve essere cambiata regolarmente per migliorare la sicurezza e in qualsiasi momento la chiave originale potrebbe essere compromessa. Ogni volta che la chiave viene modificata, tutti i dati legacy vengono codificati nuovamente utilizzando la nuova chiave.

Per informazioni tecniche, vedere [Installazione locale avanzata](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) nella _Guida all&#39;installazione_.

## Passaggio 1: rendere il file scrivibile

Per modificare la chiave di crittografia, verificare che il seguente file sia scrivibile: `[your store]/app/etc/env.php`

## Passaggio 2: modificare la chiave di crittografia

1. Nella barra laterale _Admin_, passa a **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**.

   ![Chiave di crittografia del sistema](./assets/encryption-key.png){width="700" zoomable="yes"}

1. Effettuare una delle seguenti operazioni:

   - Per generare una nuova chiave, impostare **[!UICONTROL Auto-generate Key]** su `Yes`.
   - Per utilizzare una chiave diversa, impostare **[!UICONTROL Auto-generate Key]** su `No`. Quindi nel campo **[!UICONTROL New Key]**, immettere o incollare la chiave che si desidera utilizzare.

1. Fare clic su **[!UICONTROL Change Encryption Key]**.

1. Conserva un record della nuova chiave in un luogo sicuro.

   È necessario per decrittografare i dati, se si verificano problemi con i file.
