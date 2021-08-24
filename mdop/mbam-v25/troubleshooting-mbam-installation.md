---
title: Risoluzione dei problemi di installazione di MBAM 2.5
description: Introduzione alla risoluzione dei problemi di installazione di MBAM 2.5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 6ea152792801c630fa365f37d1668d1a4d84b3a5
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910631"
---
# <a name="troubleshooting-mbam-25-installation-problems"></a>Risoluzione dei problemi di installazione di MBAM 2.5

In questo articolo viene illustrato come risolvere i problemi di installazione di Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 in una configurazione autonoma.

## <a name="referring-mbam-log-files-for-troubleshooting"></a>Riferimento ai file di registro MBAM per la risoluzione dei problemi

MBAM include la registrazione per l'installazione del server, l'installazione client e gli eventi. Questa registrazione deve essere indicata per la risoluzione dei problemi. 
 
### <a name="mbam-server-installation-log-files"></a>File di registro di installazione del server MBAM

MBAMServerSetup.exe durante l'installazione di MBAM vengono generati i seguenti file di registro nella cartella %temp% dell'utente:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 numeri>.log**

MBAMServerSetup.exe registra le azioni eseguite durante l'installazione di MBAM e dell'installazione delle funzionalità del server MBAM:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log**

MBAMServerSetup.exe registra le azioni aggiuntive eseguite durante l'installazione.

### <a name="mbam-client-installation-log-file"></a>File di registro dell'installazione del client MBAM

L'installazione del client viene registrata nel file di registro seguente nella cartella %temp% (o in un percorso personalizzato, a seconda di come è stato installato il client): <br />**MSI \<five random characters\> .log**

Questo registro contiene le azioni eseguite durante l'installazione del client MBAM.
 
### <a name="mbam-client-event-logging-channel"></a>Canale di registrazione eventi del client MBAM

MBAM dispone di canali di registrazione eventi separati. I file di registro amministratore, analitico e operativo si trovano nel Visualizzatore eventi, in **Registri**applicazioni e servizi  >  **Microsoft**  >  **Windows**  >  **MBAM.**

Nella tabella seguente viene fornita una breve descrizione di ogni registro eventi.
 
|Registro eventi| Descrizione|
|----------|-------|
|Microsoft-Windows-MBAM/Admin|  Contiene messaggi di errore|
|Microsoft-Windows-MBAM/Analitico|   Contiene informazioni di registrazione avanzate|
|Microsoft-Windows-MBAM/Operational|    Contiene i messaggi di esito positivo|

### <a name="mbam-server-event-logging-channel"></a>Canale di registrazione eventi del server MBAM

I file di registro si trovano nel Visualizzatore eventi, in **Registri**applicazioni e servizi  >  **Microsoft**  >  **Windows**  >  **MBAM**. Nella tabella seguente sono inclusi i registri eventi del server introdotti in MBAM 2.5:

|Registro eventi| Descrizione|
|--------|-------------|
|Microsoft-Windows-MBAM/Admin|  Contiene messaggi di errore|
|Microsoft-Windows-MBAM/Analitico|   Contiene informazioni di registrazione avanzate|
|Microsoft-Windows-MBAM/Operational|    Contiene i messaggi di esito positivo|

### <a name="mbam-web-service-logs"></a>Log del servizio Web MBAM

Ogni registro del servizio Web MBAM scrive le informazioni di registrazione in un file SVCLOG. Per impostazione predefinita, ogni servizio Web scrive il file di traccia in una cartella che ne utilizza il nome nella cartella C:\inetpub\Microsoft BitLocker Management Solution\Logs.

È possibile utilizzare lo strumento visualizzatore di traccia del servizio (parte Microsoft Visual Studio) per esaminare le tracce svclog.

## <a name="troubleshooting-encryption-and-reporting-issues"></a>Risoluzione dei problemi di crittografia e segnalazione

In questa sezione sono contenute informazioni sulla risoluzione dei problemi relativi a funzionalità server, funzionalità client, impostazioni di configurazione e problemi noti:
 
### <a name="mbam-client-installation-group-policy-settings"></a>Installazione client MBAM, impostazioni di Criteri di gruppo

Determinare se l'agente MBAM è installato nel computer client. Quando MBAM viene installato, crea un servizio denominato Servizio client di gestione BitLocker. Questo servizio è configurato per l'avvio automatico. Determinare se il servizio è in esecuzione.

Assicurarsi che le impostazioni di Criteri di gruppo MBAM siano applicate al computer client. Se nel computer client sono state applicate le impostazioni di Criteri di gruppo, viene creata la sottochiave del Registro di sistema ** seguente:HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Verificare che questa chiave esista e che sia popolata utilizzando i valori per le impostazioni di Criteri di gruppo.

### <a name="mbam-agent-in-the-initial-delay-period"></a>Agente MBAM nel periodo di ritardo iniziale

Il client MBAM non avvia l'operazione subito dopo l'installazione. Si verifica un ritardo casuale iniziale di 1-18 minuti prima che l'agente MBAM inizi l'operazione. Oltre al ritardo iniziale, si verifica un ritardo di almeno 90 minuti. Il ritardo dipende dalle impostazioni di Criteri di gruppo configurate per la frequenza di controllo dello stato del client. Di conseguenza, il ritardo totale prima dell'avvio di un'operazione del client è *il*ritardo casuale del  +  *controllo della frequenza del client.*

Se i registri eventi operativi e di amministrazione sono vuoti, il client non ha ancora avviato l'operazione ed è nel periodo di ritardo menzionato in precedenza. Se si desidera ignorare il ritardo, attenersi alla seguente procedura:
 
1. Arrestare il servizio Servizio client di gestione BitLocker.

2. Nella sottochiave **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** del Registro di sistema creare il valore del Registro di sistema **NoStartupDelay,** impostarne il tipo **su REG_DWORD**e quindi impostarne il valore su **1.**

3. In **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**impostare i valori **ClientWakeupFrequency** e **StatusReportingFrequency** su **1.** Questi valori ripristinano le impostazioni originali dopo gli aggiornamenti di Criteri di gruppo nel computer.

4. Avviare il servizio Servizio client di gestione BitLocker.

Dopo l'avvio del servizio, se si accede localmente al computer e non si verificano errori, è consigliabile ricevere una richiesta di crittografia del computer entro un minuto. Se non si riceve una richiesta, è consigliabile esaminare i registri di amministrazione di MBAM per eventuali voci di errore.

### <a name="computer-does-not-have-a-tpm-device-or-the-tpm-device-is-not-enabled-in-the-bios"></a>Il computer non dispone di un dispositivo TPM oppure il dispositivo TPM non è abilitato nel BIOS

Esaminare il registro eventi di amministrazione di MBAM. Nel registro eventi di amministrazione di MBAM verrà visualizzata una voce di evento simile alla seguente:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

Aprire Gestione TPM (tpm.msc) e verificare se il computer dispone di un dispositivo TPM. Se tpm.msc non mostra un dispositivo, apri Gestione dispositivi (devmgmt.msc) e verifica la presenza di un modulo di piattaforma attendibile in Dispositivi di sicurezza. Se non viene visualizzato un dispositivo Trusted Platform Module, ciò potrebbe essere vero per uno dei motivi seguenti:

* Il sistema non dispone di un dispositivo Trusted Platform Module (TPM/Security).

* Il dispositivo TPM è disabilitato nel BIOS.

* Il dispositivo TPM è abilitato nel BIOS, ma la gestione del dispositivo TPM dal sistema operativo è disabilitata nel BIOS.

* Non stai usando un driver Microsoft per il dispositivo TPM. Esaminare i dispositivi elencati in Gestione dispositivi per identificare il driver di dispositivo TPM Microsoft.

Se il dispositivo TPM non utilizza il driver C:\Windows\System32\tpm.sys, è consigliabile aggiornare il driver selezionando il file C:\Windows\Inf\tpm.inf.

### <a name="computer-does-not-have-a-valid-system-partition"></a>Il computer non dispone di una partizione SYSTEM valida

Esaminare il registro eventi di amministrazione di MBAM. Nel registro eventi di amministrazione di MBAM verrà visualizzata una voce di evento simile alla seguente:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

BitLocker richiede una partizione SYSTEM per abilitare la crittografia ( Crittografia unità[BitLocker in Windows 7: Domande frequenti](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).

MBAM non crea automaticamente la partizione di sistema. È possibile utilizzare l'utilità di preparazione dell'unità BitLocker (bdehdcfg.exe) per creare la partizione di sistema e spostare i file di avvio necessari.

Ad esempio, è possibile utilizzare il comando **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** per preparare l'unità in modo invisibile all'utente prima di distribuire MBAM per crittografare le unità. A tale scopo, è necessario riavviare il sistema. Se necessario, è inoltre possibile eseguire lo script dell'azione. Nel documento seguente viene descritto lo strumento di preparazione dell'unità BitLocker:

[Descrizione dello strumento preparazione unità BitLocker](https://support.microsoft.com/help/933246)

### <a name="drives-are-not-formatted-to-have-a-compatible-file-system"></a>Le unità non sono formattate per avere un file system compatibile

Vedere [l'articolo techNet per i requisiti del file system per BitLocker.](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements)

### <a name="group-policy-conflict"></a>Conflitto di Criteri di gruppo

Nel registro eventi di amministrazione di MBAM verrà visualizzata una voce di evento simile alla seguente:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

Verificare le impostazioni di Criteri di gruppo per assicurarsi di non disporre di un'impostazione in conflitto tra le impostazioni di Criteri di gruppo di MBAM.

È consigliabile configurare Criteri di gruppo utilizzando il modello MDOP MBAM e non il modello Crittografia unità BitLocker.

Ad esempio:

In Impostazioni crittografia unità del sistema operativo è stato selezionato TPM come protettore e è stato anche selezionato Consenti **PIN avanzato per l'avvio.** Si tratta di impostazioni in conflitto perché la protezione solo TPM non richiede un PIN. Di conseguenza, è consigliabile disabilitare l'impostazione pin avanzato.

### <a name="user-may-have-requested-an-exemption"></a>L'utente potrebbe aver richiesto un'esenzione

Se è stata abilitata l'impostazione di Criteri di gruppo Configurazione computer\Modelli amministrativi\Componenti di Windows\MDOP MBAM (Gestione BitLocker)\Gestione client\Configura criteri di esenzione utente, agli utenti verrà offerta la possibilità di richiedere un'esenzione.

Per impostazione predefinita, se l'utente richiede un'esenzione, l'esenzione sarà valida per 7 giorni e l'utente non riceverà richieste di crittografia durante questo periodo. Il valore predefinito può essere aumentato o diminuito durante la configurazione dei criteri. Al termine del periodo di esenzione, all'utente viene richiesto di crittografare.

Quando un computer è in esenzione dall'utente, nel registro eventi di amministrazione di MBAM verrà visualizzata la voce seguente:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

Se si desidera sostituire manualmente l'esenzione utente per un computer, attenersi alla seguente procedura:
 
1. Impostare il valore AllowUserExemption su **0** nella seguente sottochiave del Registro di sistema: <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. Eliminare tutti i valori del Registro di sistema nella seguente sottochiave del Registro di sistema ad eccezione di **AgentVersion,** **EncodedComputerName**e **Installed**:<br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM**

    **Nota** È necessario riavviare l'agente MBAM per l'applicazione delle modifiche.

Tenere presente che, dopo aver applicato Criteri di gruppo al computer, questi valori potrebbero ripristinare le impostazioni originali.

### <a name="wmi-issue"></a>Problema WMI

MBAM usa i metodi della classe win32_encryptablevolume per gestire BitLocker. Se il modulo non è registrato o è danneggiato, il client MBAM non funzionerà correttamente e nel registro eventi di amministrazione di MBAM verrà visualizzata la voce di evento seguente:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

Inoltre, è possibile notare che i criteri di ripristino e hardware non si applicano con codice di errore 0x8007007e. Si traduce in "Impossibile trovare il modulo specificato".

Per risolvere questo problema, è necessario registrare di nuovo la **classe win32_encryptablevolume** utilizzando il comando seguente:

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <a name="troubleshooting-mbam-agent-communication-issues"></a>Risoluzione dei problemi di comunicazione dell'agente MBAM

In questa sezione sono contenute informazioni sulla risoluzione dei problemi correlati alla comunicazione con gli agenti MBAM:

### <a name="incorrect-mbam-service-url"></a>URL del servizio MBAM non corretto

Se il valore di Servizio stato di conformità MBAM o Ripristino e servizio hardware non è corretto, nel registro eventi di amministrazione di MBAM nel computer client verrà visualizzata una voce di evento simile alla seguente:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

Verificare i valori **di KeyRecoveryServiceEndPoint** e **StatusReportingServiceEndpoint** nella sottochiave del Registro di sistema seguente nel computer client: <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Per impostazione predefinita, l'URL per KeyRecoveryServiceEndPoint (endpoint del servizio di ripristino MBAM e hardware) è nel formato seguente: <br />
**http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

Per impostazione predefinita, l'URL per StatusReportingServiceEndpoint (endpoint del servizio di segnalazione dello stato MBAM) è nel formato seguente:<br />
**http:// : \<servername\> \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> L'URL non deve contenere spazi.

Se l'URL del servizio non è corretto, è necessario correggere l'URL del servizio nell'impostazione di Criteri di gruppo seguente:

**Configurazione computer**  >  **Criteri**  >  **Modelli amministrativi**  >  **Windows componenti**  >  **MDOP MBAM (Gestione BitLocker)**  >  **Gestione client**  >  **Configurare i servizi MBAM**

### <a name="connectivity-issue-that-affects-the-mbam-administration-server"></a>Problema di connettività che interessa il server di amministrazione di MBAM

L'agente MBAM non sarà in grado di inviare aggiornamenti al database se sono presenti problemi di connettività tra l'agente client e il server di amministrazione di MBAM. In questo caso, si noteranno voci di errore di connettività nel registro eventi di amministrazione di MBAM nel computer client:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

Controlli di base:

* Verificare la connettività di base eseguendo il ping del server di amministrazione di MBAM in base al nome e all'IP. Verificare se è possibile connettersi al sito Web di amministrazione di MBAM o alla porta del servizio tramite telnet o portqry.

* Verificare che il servizio IIS sia in esecuzione nel server di amministrazione e monitoraggio MBAM e che il servizio Web MBAM sia in ascolto sulla stessa porta configurata nel computer client MBAM ( `netstat –ano | find "portnumber"` ).

* Verificare che il numero di porta configurato per il sito Web MBAM utilizzi Gestione IIS (inetmgr). Assicurarsi che il numero di porta sia lo stesso del numero di porta su cui il client è in attesa. Assicurarsi che il numero di porta non sia condiviso da un'altra applicazione. Ad esempio, un'altra applicazione sul server non deve utilizzare la stessa porta.

* Se è presente un firewall, assicurarsi che la porta sia aperta nel firewall o nel server proxy.

* Se la comunicazione tra client e server è sicura, assicurarsi di utilizzare un certificato SSL valido.

* Verificare la connettività di rete tra il server Web e il server di database a cui vengono inviati i dati per l'inserimento. È possibile verificare la connettività del database dal server Web al server database utilizzando Amministrazione origine dati ODBC. Informazioni dettagliate SQL Server risoluzione dei problemi di connessione sono disponibili in [How to Troubleshoot Connecting to the SQL Server motore di database](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).

#### <a name="troubleshooting-the-connectivity-issue"></a>Risoluzione del problema di connettività

Verificare che l'URL del servizio configurato nel client sia corretto. Copiare il valore dell'URL per KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) dal Registro di sistema e aprirlo in Internet Explorer.

Analogamente, copiare il valore dell'URL per StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) e aprirlo in Internet Explorer.

> [!Note]
> Se non è possibile accedere all'URL dal computer client, è consigliabile testare la connettività di rete di base dal client al server che esegue IIS. Vedere i punti 1, 2, 3 e 4 nella sezione precedente.

Esaminare inoltre i registri applicazioni nel server di amministrazione e di monitoraggio per verificare la presenza di eventuali errori.

È possibile creare una traccia di rete simultanea tra il client e il server ed esaminare la traccia per determinare la causa dell'errore di connessione tra l'agente client e il server di amministrazione di MBAM.

> [!Note]
> Se è possibile accedere agli URL del servizio dal computer client e sono presenti voci di errore di connettività nei registri eventi di amministrazione di MBAM, ciò potrebbe essere dovuto a un errore di connettività tra il server di amministrazione e il server di database.

Se è possibile accedere a entrambi gli URL del servizio ed è presente connettività tra il client e il server in esecuzione, IIS funziona. Tuttavia, potrebbe verificarsi un problema di comunicazione tra il server che esegue IIS e il server di database.

I servizi MBAM potrebbero non essere in grado di connettersi al server di database a causa di un problema di rete o di un'impostazione errata della stringa di connessione al database. Esaminare i registri applicazioni nel server di amministrazione e di monitoraggio. È possibile che vengano visualizzati errori o avvisi dall'origine ASP.NET 2.0.50727.0 simili alla voce di registro seguente:

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### <a name="possible-causes"></a>Possibili cause

##### <a name="cause-1"></a>Causa 1

È possibile che l'amministratore abbia specificato un nome di istanza di database/nome di database non valido durante l'installazione dei componenti del server di amministrazione e monitoraggio.

È possibile verificare e correggere le stringhe di connessione al database utilizzando la console di gestione IIS. A tale scopo, aprire Gestione IIS e passare a Amministrazione e monitoraggio di Microsoft BitLocker. Per ogni servizio elencato a sinistra, eseguire la procedura seguente per modificare le stringhe di connessione al database:

1. In **Visualizzazione caratteristiche**selezionare due volte Stringhe di **connessione.**

2. Nella pagina **Stringhe di** connessione selezionare la stringa di connessione che si desidera modificare.

3. Nel riquadro **Azioni** selezionare **Modifica.**

4. Nella finestra **di dialogo Modifica stringa** di connessione modificare le proprietà che si desidera modificare e quindi selezionare **OK.**

##### <a name="cause-2"></a>Causa 2

SQL Server porta bloccata nel firewall. Verificare il numero di porta SQL Server configurato per l'ascolto e verificare che la porta sia aperta nel firewall tra il server di amministrazione e il server di database.

##### <a name="cause-3"></a>Causa 3

Binding TCP/IP SQL server non corretti. Verificare SQL binding TCP/IP in Gestione configurazione SQL Server nel server di database. MBAM richiede che i protocolli TCP/IP e Named Pipes siano abilitati per la connessione al database.

##### <a name="cause-4"></a>Causa 4

L'account NT Authority\Network Service o l'account computer del server di amministrazione MBAM non dispone delle autorizzazioni necessarie per connettersi al database SQL database.

Durante l'installazione dei componenti di database nel server di database, il programma di installazione crea due gruppi locali: MBAM Compliance Auditing DB Access e MBAM Recovery e Hardware DB Access.

L'account NT Authority\Network Service, l'account computer del server di amministrazione MBAM e l'utente che installa i componenti di database vengono aggiunti automaticamente a questi gruppi.

A questi gruppi vengono concesse le autorizzazioni necessarie per il database durante l'installazione. Tutti gli utenti che fanno parte di questo gruppo ricevono automaticamente le autorizzazioni necessarie per il database.

Il servizio Web potrebbe non connettersi al server di database a causa di un problema di autorizzazioni se si verifica una o più delle condizioni seguenti:

* I gruppi menzionati in precedenza vengono rimossi dai gruppi locali nel server di database.

* L'account NT Authority\Network Service e l'account computer del server di amministrazione MBAM non sono membri di questi gruppi.

* Questi gruppi non dispongono delle autorizzazioni necessarie per il database.

Si noteranno errori relativi alle autorizzazioni nei registri applicazioni nel server di amministrazione e monitoraggio MBAM se una delle condizioni precedenti è vera. In tal caso, è necessario aggiungere manualmente l'account NT Authority\Network Service e l'account computer del server di amministrazione MBAM e concedere loro un ruolo pubblico a livello di server nel server database di SQL che utilizza SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .

#### <a name="review-the-web-service-logs"></a>Esaminare i log del servizio Web

Se non viene registrato alcun evento nei registri applicazioni nel server di amministrazione di MBAM, è necessario esaminare i registri del servizio Web (con estensione svclog) del servizio Web MBAM ospitato nel server di amministrazione e monitoraggio MBAM. Sarà necessario utilizzare lo strumento Visualizzatore traccia servizio (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx per visualizzare il file di registro.

È consigliabile analizzare principalmente i registri di traccia del servizio di RecoveryandHardwareService e ComplianceStatusService. Per impostazione predefinita, i log del servizio Web si trovano nella cartella C:\inetpub\Microsoft BitLocker Management Solution\Logs. In questo caso, ogni servizio scrive il relativo file svclog nella propria cartella.

Esaminare l'attività nel registro di traccia del servizio per eventuali voci di errore o avviso. Per impostazione predefinita, le voci di errore sono evidenziate in rosso. Selezionare la descrizione dell'errore nel riquadro destro del visualizzatore di traccia per visualizzare informazioni dettagliate sulla voce di errore. Di seguito è riportata una voce di errore di esempio dal registro di traccia:

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## <a name="re-installation-or-reconfiguration-of-mbam-infrastructure"></a>Riconfigurazione o riconfigurazione dell'infrastruttura MBAM

Per installare di nuovo o riconfigurare l'infrastruttura MBAM, è necessario conoscere gli aspetti seguenti:

* Account pool di applicazioni

* Gruppi MBAM (Helpdesk, Advanced, Report Users Group)

* URL report MBAM

* SQL Server nomi di database e nomi di database

* Account MBAM ReadWrite e ReadOnly

### <a name="application-pool-account"></a>Account pool di applicazioni

Per trovare l'account del pool di applicazioni, accedere al server Web MBAM, **aprire Gestione Internet Information Services (IIS)** e quindi selezionare **Pool di applicazioni**:

![pool di applicazioni.](images/troubleshooting-MBAM-installation-1.png)

Il nome dell'entità servizio (SPN) deve essere impostato in questo account. Questa impostazione è molto importante per le funzionalità di MBAM.

### <a name="mbam-groups-helpdesk-advanced-report-users-group-and-reports-url"></a>Gruppi MBAM (Helpdesk, Advanced, Report Users Group and Reports URL)

![Gruppi MBAM.](images/troubleshooting-MBAM-installation-2.png)

In questo modo vengono fornite informazioni quali Gruppo helpdesk, Gruppo helpdesk avanzato, Gruppo Utenti report e URL report MBAM. L'URL dei rapporti MBAM deve essere specificato nell'installazione di MBAM e deve essere letto come: http(s)://nomeserver/ReportServer.

### <a name="sql-server-name-and-database-db-names"></a>SQL Server nomi di database e nomi di database

Per trovare i nomi SQL Server e le istanze che ospitano i database MBAM, accedere al server Web MBAM (IIS) e passare alla sottochiave del Registro di sistema folowing:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web**

![Regedit.](images/troubleshooting-MBAM-installation-3.png)

Le parti evidenziate sono stringhe di connessione. Devono avere il nome SQL Server, i nomi di database e le istanze (se denominati).

### <a name="mbam-readwrite-and-readonly-accounts"></a>Account MBAM ReadWrite e ReadOnly

Queste informazioni saranno contenute nel database SQL Server, per il quale è già stato trovato il nome dal server Web.

#### <a name="readwrite-account"></a>Account ReadWrite

1. Accedere al SQL Management Studio.

2. Fare clic con il pulsante destro del mouse su Ripristino **e hardware di MBAM,** **scegliere Proprietà**e quindi **Autorizzazioni.**

Ad esempio, il nome dell'account lab è **MBAMWrite.** Gli account Pool di applicazioni e ReadWrite sono impostati per essere uguali.

![SQL DB.](images/troubleshooting-MBAM-installation-4.png)

![Proprietà db.](images/troubleshooting-MBAM-installation-5.png)

Passare a **Sicurezza** e quindi **Account di** accesso in SQL Management Studio. Passare all'account mostrato nella schermata precedente.

![SQL Sicurezza.](images/troubleshooting-MBAM-installation-6.png)

Fare clic con il pulsante destro del mouse sull'account, scegliere Proprietà **Mapping utenti**e individuare il database hardware e ripristino MBAM:

![Mapping utenti.](images/troubleshooting-MBAM-installation-7.png)

#### <a name="readonly-account"></a>Account ReadOnly

Aprire SQL Server Reporting Services Configuration Manager nel server SSRS. Selezionare **URL Gestione report**e quindi sfogliare gli **URL**:

![Gestione report.](images/troubleshooting-MBAM-installation-8.png)

Selezionare **Amministrazione e monitoraggio di Microsoft Bitlocker**:

![Amministrazione e monitoraggio di Bitlocker.](images/troubleshooting-MBAM-installation-9.png)

Selezionare **MaltaDatasource**:

![DBs.](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource.](images/troubleshooting-MBAM-installation-11.png)

MaltaDataSource deve avere il nome account ReadOnly e deve essere usato nella configurazione di MBAM.

## <a name="reference"></a>Riferimento

Per ulteriori informazioni, vedere gli articoli seguenti:

[Distribuzione di MBAM 2.5 in una configurazione autonoma](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
