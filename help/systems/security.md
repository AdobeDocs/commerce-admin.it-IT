---
title: Sicurezza
description: Scopri gli strumenti disponibili per proteggere archivi e dati e le linee guida per un piano d’azione sulla sicurezza se noti un compromesso.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: 671ec7015c37b24ca0acc615ae3715b8b870a453
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# Sicurezza

Esistono diversi modi per proteggere il tuo archivio e mantenere la sicurezza dei dati:

- Configurazione [autenticazione a due fattori](security-two-factor-authentication.md)
- Implementare [CAPTCHA](security-captcha.md) o [reCAPTCHA](security-google-recaptcha.md)
- Configurare un [Security Scan](security-scan.md) per ciascun dominio nell’installazione di Adobe Commerce o di Magento Open Source.

Visita il [Centro sicurezza](https://helpx.adobe.com/security.html){:target=&quot;_blank&quot;} e iscriviti al registro degli avvisi di sicurezza per ottenere le ultime notizie su potenziali vulnerabilità. Per informazioni sulle procedure consigliate per la protezione, vedere [Proteggere il sito e l’infrastruttura di Commerce](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) nel _Playbook di implementazione_.

>[!NOTE]
>
>Archivi che hanno abilitato [!DNL Adobe Identity Management Services] Per l’autenticazione IMS, Adobe Commerce nativo e Magento Open Source 2FA sono disabilitati. Gli utenti amministratori che hanno effettuato l’accesso alla propria istanza Commerce con le credenziali di Adobe non devono ripetere l’autenticazione per molte attività di amministrazione. L’autenticazione viene gestita da Adobe IMS quando l’utente amministratore accede alla sessione corrente. Consulta [[!DNL Adobe Identity Management Service] Panoramica dell’integrazione di (IMS)](../getting-started/adobe-ims-integration-overview.md).

![Centro sicurezza](./assets/product-security-home.png){width="700" zoomable="yes"}

## Piano d&#39;azione sulla sicurezza

Se pensi che il tuo sito Adobe Commerce o di Magento Open Source sia compromesso, segui questo piano d’azione senza indugio.

1. **Diagnostica**: esegui un’analisi per stabilire lo stato di sicurezza dell’archivio Commerce. Commerce [Security Scan](security-scan.md) è un servizio gratuito offerto da Adobe che ti consente di monitorare i siti Commerce per individuare rischi di sicurezza noti e malware e di ricevere notifiche di sicurezza.

1. **Pulisci**: noleggia un [consulente qualificato](https://solutionpartners.adobe.com/s/directory/?partner_type=1) o servizio online per pulire il tuo sito da tutto il codice dannoso. Alcuni membri della community di Commerce consigliano [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). Controlla la `/media` cartella per il codice eseguibile rimanente. Rimuovi tutti gli utenti Admin sconosciuti e reimposta tutte le password Admin.

1. **Protect**: aggiorna l’installazione di Commerce con la versione più recente. Se si utilizza una versione precedente, applicare tutte le patch di sicurezza non appena diventano disponibili. Rivedi e segui [Best practice per la sicurezza di Commerce](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). Iscriviti a [Avvisi sulla sicurezza di Commerce](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **Report**: se pensi di aver trovato una vulnerabilità specifica in Commerce, [apri un problema con un Adobe](https://hackerone.com/adobe?type=team) e includere dettagli tecnici.

1. **Aggiorna**: per garantire la massima tranquillità con il supporto 24 ore su 24, 7 giorni su 7, pianifica l’aggiornamento a [Adobe Commerce sull’architettura cloud](https://business.adobe.com/products/magento/cloud-delivery.html) ora.
