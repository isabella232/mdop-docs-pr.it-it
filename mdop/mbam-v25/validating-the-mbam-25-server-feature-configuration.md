---
title: Convalida della configurazione delle funzionalità del server di MBAM 2.5
description: Convalida della configurazione delle funzionalità del server di MBAM 2.5
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827085"
---
# Convalida della configurazione delle funzionalità del server di MBAM 2.5


Al termine della distribuzione della funzionalità del server di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5, è consigliabile convalidare la distribuzione per verificare che tutte le funzionalità siano state configurate correttamente. Usare la procedura che corrisponde alla topologia (autonoma o integrazione di System Center Configuration Manager) distribuita.

## Convalida della distribuzione di MBAM server con la topologia autonoma


Eseguire la procedura seguente per convalidare la distribuzione di MBAM server con la topologia autonoma.

**Per convalidare una distribuzione autonoma di MBAM server**

1.  In ogni server in cui è distribuita una caratteristica di **Control Panel** mbam, fare clic su &gt; **Programs** &gt; **programmi e funzionalità**del pannello di controllo. Verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati nell'elenco **programmi e funzionalità** .

    **Nota**  
    Per eseguire la convalida, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.



2.  Nel server in cui è configurato il database di ripristino, aprire SQL Server Management Studio e verificare che il database **di mbam Recovery e hardware** sia configurato.

3.  Nel server in cui è configurato il database di conformità e controllo, aprire SQL Server Management Studio e verificare che il **database dello stato di conformità di mbam** sia configurato.

4.  Nel server in cui è configurata la caratteristica report aprire un Web browser con credenziali amministrative e passare alla Home page del sito di SQL Server Reporting Services.

    La posizione principale predefinita di un'istanza del sito di SQL Server Reporting Services è:

    http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *porta* &gt; /Reports.aspx

    Per trovare l'URL effettivo, usare lo strumento Gestione configurazione di Reporting Services e selezionare le istanze specificate durante l'installazione.

5.  Verificare che una cartella report denominata **amministrazione e monitoraggio di Microsoft BitLocker** contenga un'origine dati denominata **MaltaDataSource** e le cartelle della lingua. L'origine dati contiene cartelle con nomi che rappresentano le lingue, ad esempio en-US. I report si trovano nelle cartelle della lingua.

    **Nota**  
    Se SQL Server Reporting Services (SSRS) è stato configurato come istanza denominata, l'URL dovrebbe essere simile al seguente: http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *porta* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. Nel server in cui è configurata la caratteristica sito Web amministrazione e monitoraggio eseguire **Server Manager**, passare a **ruoli**e quindi selezionare **Web Server (IIS)** &gt; **Gestione Internet Information Services (IIS)**.

7. In **connessioni**passare al * &lt; nome &gt; del computer* e selezionare **siti** di &gt; **amministrazione e monitoraggio di Microsoft BitLocker**. Verificare che siano elencati i seguenti elementi:

   -   **MBAMAdministrationService**

   -   **MBAMComplianceStatusService**

   -   **MBAMRecoveryAndHardwareService**

8. Nel server in cui sono configurati il sito Web di amministrazione e monitoraggio e il portale self-service, aprire un Web browser con credenziali amministrative.

9. Individuare i siti Web seguenti per verificare che vengano caricati correttamente:

   -   HTTPS (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /helpdesk/-confermare tutti i collegamenti per gli spostamenti e i report

   -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /selfservice/

   **Nota**  
   Si presuppone che siano state configurate le caratteristiche del server nella porta predefinita senza crittografia di rete. Se sono state configurate le caratteristiche del server in una porta o una directory virtuale diversa, modificare gli URL per includere la porta appropriata, ad esempio:

   http (s):// &lt; *nome host* &gt; : &lt; *porta* &gt; /helpdesk/

   http (s):// &lt; *nome host* &gt; : &lt; *porta* &gt; / &lt; *VirtualDirectory*&gt;/

   Se le caratteristiche del server sono state configurate con crittografia di rete, cambiare http://in https://.



10. Individuare i servizi Web seguenti per verificare che vengano caricati correttamente. Verrà visualizzata una pagina per indicare che il servizio è in corso, ma la pagina non Visualizza i metadati.

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMAdministrationService/AdministrationService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMUserSupportService/UserSupportService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMComplianceStatusService/StatusReportingService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *porta* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc

## Convalida della distribuzione di MBAM server con la topologia di integrazione di Configuration Manager


Usare la procedura seguente per convalidare la distribuzione di MBAM con la topologia di integrazione di Configuration Manager. Completare i passaggi di convalida che corrispondono alla versione di Configuration Manager in uso.

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a>Convalida della distribuzione di MBAM server con System Center 2012 Configuration Manager

Seguire questa procedura per convalidare la distribuzione di MBAM server quando si usa MBAM con System Center 2012 Configuration Manager.

**Per convalidare una distribuzione di Configuration Manager Integration MBAM Server-System Center 2012 Configuration Manager**

1.  Nel server in cui è distribuito System Center 2012 Configuration Manager, aprire **programmi e funzionalità** nel **Pannello di controllo**e verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati.

    **Nota**  
    Per convalidare la configurazione, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.



2.  Nella console di Configuration Manager fare clic su **assets and Compliance** &gt; **Device**Workspace e verificare che venga visualizzata una nuova raccolta denominata **computer supportati mbam** .

3.  Nella console di Configuration Manager fare clic su **Monitoring** &gt; **Reporting** &gt; **Reports** &gt; **mbam**report Reporting Workspace.

4.  Verificare che la cartella **mbam** contenga sottocartelle, con nomi che rappresentano lingue diverse e che i report seguenti siano elencati in ogni sottocartella della lingua:

    -   Conformità al computer BitLocker

    -   Dashboard di conformità di BitLocker Enterprise

    -   Dettagli di conformità di BitLocker Enterprise

    -   Riepilogo conformità di BitLocker Enterprise

5.  Nella console di Configuration Manager fare clic sulle previsioni di configurazione delle impostazioni di conformità per l'area **risorse e conformità** &gt; **Compliance Settings** &gt; **Configuration Baselines**e verificare che sia elencata la **protezione BitLocker** della previsione di configurazione.

6.  Nella console di Configuration Manager fare clic sugli elementi di configurazione **assets and Compliance** Workspace &gt; **Compliance Settings** &gt; **Configuration Items**e verificare che siano visualizzati i nuovi elementi di configurazione seguenti:

    -   Protezione delle unità dati fisse di BitLocker

    -   Protezione unità sistema operativo BitLocker

### Convalida della distribuzione di MBAM server con Configuration Manager 2007

Seguire questa procedura per convalidare la distribuzione di MBAM server quando si usa MBAM con Configuration Manager 2007.

**Per convalidare una distribuzione di Configuration Manager Integration MBAM Server-Configuration Manager 2007**

1.  Nel server in cui è distribuito Configuration Manager 2007 aprire **programmi e funzionalità** nel **Pannello di controllo** e verificare che l' **amministrazione e il monitoraggio di Microsoft BitLocker** vengano visualizzati.

    **Nota**  
    Per convalidare la configurazione, è necessario usare un account di dominio che disponga delle credenziali amministrative del computer locale per ogni server.



2.  Nella console di Configuration Manager fare clic su **database del sito &lt; codicesito &gt;  -  &lt; NomeServer &gt; , &lt; nomesito &gt; ), Gestione computer**e verificare che venga visualizzata una nuova raccolta denominata **computer supportati mbam** .

3.  Nella console di Configuration Manager fare clic su **Reporting** &gt; **Services** &gt; ** \\\\ &lt; NomeServer &gt; ** &gt; **cartelle di report** &gt; **MBAM**.

    Verificare che la cartella **mbam** contenga sottocartelle, con nomi che rappresentano lingue diverse e che i report seguenti siano elencati in ogni sottocartella della lingua:

    -   Conformità al computer BitLocker

    -   Dashboard di conformità di BitLocker Enterprise

    -   Dettagli di conformità di BitLocker Enterprise

    -   Riepilogo conformità di BitLocker Enterprise

4.  Nella console di Configuration Manager fare clic su previsioni di configurazione per la **gestione della configurazione desiderata** &gt; **Configuration Baselines**e verificare che sia elencata la **protezione BitLocker** della configurazione di base.

5.  Nella console di Configuration Manager fare clic su elementi di configurazione della **gestione della configurazione desiderati** &gt; **Configuration Items**e verificare che siano visualizzati i nuovi elementi di configurazione seguenti:

    -   Protezione delle unità dati fisse di BitLocker

    -   Protezione unità sistema operativo BitLocker



## Argomenti correlati


[Configurazione delle funzionalità server di MBAM 2.5](configuring-the-mbam-25-server-features.md)


## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






