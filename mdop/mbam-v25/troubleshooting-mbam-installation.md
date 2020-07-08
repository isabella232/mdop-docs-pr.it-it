---
title: Risoluzione dei problemi di installazione di MBAM 2.5
description: Introduzione alla risoluzione dei problemi di installazione di MBAM 2,5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804546"
---
# Risoluzione dei problemi di installazione di MBAM 2.5

Questo articolo illustra come risolvere i problemi di installazione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 in una configurazione autonoma.

## Riferimenti ai file di log di MBAM per la risoluzione dei problemi

MBAM include la registrazione per l'installazione del server, l'installazione del client e gli eventi. Questa registrazione deve essere definita per la risoluzione dei problemi. 
 
### File di log di installazione di MBAM server

MBAMServerSetup.exe genera i file di log seguenti nella cartella% Temp% dell'utente durante l'installazione di MBAM:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 numeri>. log**

MBAMServerSetup.exe registra le azioni intraprese durante l'installazione di MBAM Setup e MBAM server:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log**

MBAMServerSetup.exe registra altre azioni acquisite durante l'installazione.

### File di log di installazione del client MBAM

L'installazione del client viene registrata nel file di log seguente nella cartella% Temp% (o in una posizione personalizzata, a seconda del modo in cui il client è stato installato): <br />**MSI \<five random characters\> . log**

Questo log contiene le azioni che vengono eseguite durante l'installazione di MBAM client.
 
### Evento client MBAM-canale di registrazione

MBAM include canali di registrazione eventi distinti. I file di log amministratore, analitico e operativo si trovano nel Visualizzatore eventi, in **applicazioni e servizi**di  >  **Microsoft**  >  **Windows**  >  **mbam**.

La tabella seguente fornisce una breve descrizione di ogni log eventi.
 
|Registro eventi| Descrizione|
|----------|-------|
|Microsoft-Windows-MBAM/admin|  Contiene messaggi di errore|
|Microsoft-Windows-MBAM/analitica|   Contiene informazioni di registrazione avanzate|
|Microsoft-Windows-MBAM/Operational|    Contiene messaggi di successo|

### Evento server MBAM-canale di registrazione

I file di log si trovano nel Visualizzatore eventi, in **Application and Services logs**di  >  **Microsoft**  >  **Windows**  >  **mbam**. La tabella seguente include i registri eventi del server introdotti in MBAM 2,5:

|Registro eventi| Descrizione|
|--------|-------------|
|Microsoft-Windows-MBAM/admin|  Contiene messaggi di errore|
|Microsoft-Windows-MBAM/analitica|   Contiene informazioni di registrazione avanzate|
|Microsoft-Windows-MBAM/Operational|    Contiene messaggi di successo|

### Registri del servizio Web MBAM

Ogni log del servizio Web MBAM scrive le informazioni di registrazione in un file SVCLOG. Per impostazione predefinita, ogni servizio Web scrive il file di traccia in una cartella che usa il proprio nome nella cartella C:\inetpub\Microsoft di gestione di BitLocker Solution\Logs.

È possibile usare lo strumento Visualizzatore di tracce del servizio (parte di Microsoft Visual Studio) per esaminare le tracce di svclog.

## Risoluzione dei problemi di crittografia e segnalazione

Questa sezione contiene informazioni sulla risoluzione dei problemi relativi a funzionalità server, funzionalità client, impostazioni di configurazione e problemi noti:
 
### Installazione del client MBAM, impostazioni di criteri di gruppo

Determinare se l'agente MBAM è installato nel computer client. Quando MBAM è installato, crea un servizio denominato servizio client di Gestione BitLocker. Questo servizio è configurato per l'avvio automatico. Determinare se il servizio è in corso.

Verificare che nel computer client vengano applicate le impostazioni dei criteri di gruppo di MBAM. La sottochiave del registro di sistema seguente viene creata se sono state applicate le impostazioni di criteri di gruppo nel computer client: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**

Verificare che questa chiave esista e venga popolata usando i valori per le impostazioni dei criteri di gruppo.

### Agente MBAM nel periodo di ritardo iniziale

Il client MBAM non avvia l'operazione immediatamente dopo l'installazione. C'è un ritardo casuale iniziale di 1-18 minuti prima che l'agente MBAM inizi l'operazione. Oltre al ritardo iniziale, c'è un ritardo di almeno 90 minuti. Il ritardo dipende dalle impostazioni dei criteri di gruppo configurate per la frequenza di controllo dello stato del client. Di conseguenza, il ritardo totale prima dell'avvio di un'operazione del client è il ritardo della frequenza di *avvio casuale*del  +  *client*.

Se i registri eventi operativi e amministrativi sono vuoti, il client non ha ancora avviato l'operazione e si trova nel periodo di ritardo menzionato in precedenza. Se si vuole ignorare il ritardo, eseguire le operazioni seguenti:
 
1. Arrestare il servizio di servizio client di Gestione BitLocker.

2. Nella sottochiave **HKEY_LOCAL_MACHINE \software\microsoft\mbam** del registro di sistema creare il valore del registro di sistema **NoStartupDelay** , impostarne il tipo su **REG_DWORD**e quindi impostarne il valore su **1**.

3. In **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**impostare i valori di **ClientWakeupFrequency** e **StatusReportingFrequency** su **1**. Questi valori ritorneranno alle impostazioni originali dopo il computer per gli aggiornamenti dei criteri di gruppo.

4. Avviare il servizio di servizio client di Gestione BitLocker.

Dopo l'avvio del servizio, se si accede localmente nel computer e non sono presenti errori, è necessario ricevere una richiesta di crittografia del computer entro un minuto. Se non si riceve una richiesta, è necessario rivedere i log di amministrazione di MBAM per eventuali voci di errore.

### Il computer non ha un dispositivo TPM o il dispositivo TPM non è abilitato nel BIOS

Esaminare il log eventi dell'amministratore di MBAM. Verrà visualizzata la voce di un evento simile alla seguente nel log eventi dell'amministratore di MBAM:

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

Aprire Gestione TPM (TPM. msc) e verificare che il computer disponga di un dispositivo TPM. Se TPM. msc non mostra un dispositivo, aprire Gestione dispositivi (devmgmt. msc) e verificare la visualizzazione di un modulo Trusted Platform in dispositivi di sicurezza. Se non si vede un dispositivo Trusted Platform Module, potrebbe essere vero per uno dei motivi seguenti:

* Il sistema non ha un dispositivo Trusted Platform Module (TPM/sicurezza).

* Il dispositivo TPM è disabilitato nel BIOS.

* Il dispositivo TPM è abilitato nel BIOS, ma la gestione del dispositivo TPM dall'impostazione del sistema operativo è disabilitata nel BIOS.

* Non si usa un driver Microsoft per il dispositivo TPM. Esaminare i dispositivi elencati in gestione dispositivi per identificare il driver di dispositivo TPM Microsoft.

Se il dispositivo TPM non usa il driver C:\Windows\System32\tpm.sys, è necessario aggiornare il driver selezionando il file C:\Windows\Inf\tpm.inf.

### Il computer non ha una partizione di sistema valida

Esaminare il log eventi dell'amministratore di MBAM. Verrà visualizzata la voce di un evento simile alla seguente nel log eventi dell'amministratore di MBAM:

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

BitLocker richiede una partizione di sistema per abilitare la crittografia ([crittografia unità BitLocker in Windows 7: domande frequenti](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).

MBAM non crea automaticamente la partizione di sistema. È possibile usare l'utilità preparazione unità BitLocker (bdehdcfg.exe) per creare la partizione di sistema e trasferire i file di avvio necessari.

Ad esempio, puoi usare il comando **% windir% \system32\bdeHdCfg.exe-destinazione 300-dimensione predefinita-tranquilla** per preparare l'unità in modo invisibile all'utente prima di distribuire mbam per crittografare le unità. Questo richiede un riavvio. Se necessario, è anche possibile eseguire lo script dell'azione. Il documento seguente descrive lo strumento di preparazione unità BitLocker:

[Descrizione dello strumento di preparazione unità BitLocker](https://support.microsoft.com/help/933246)

### Le unità non sono formattate per avere un file system compatibile

Vedere l' [articolo di TechNet per i requisiti di file System per BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).

### Conflitto di criteri di gruppo

Verrà visualizzata la voce di un evento simile alla seguente nel log eventi dell'amministratore di MBAM:

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

Verificare le impostazioni di criteri di gruppo per assicurarsi di non avere un'impostazione in conflitto tra le impostazioni dei criteri di gruppo di MBAM.

È consigliabile configurare criteri di gruppo usando il modello MBAM di MDOP e non il modello di crittografia unità BitLocker.

Ad esempio:

In impostazioni di crittografia unità sistema operativo è stato selezionato TPM come Protector ed è stato selezionato Consenti anche **PIN avanzati per l'avvio**. Si tratta di impostazioni in conflitto, perché la protezione solo TPM non richiede un PIN. Devi quindi disabilitare l'impostazione dei PIN avanzati.

### L'utente può richiedere un'esenzione

Se è stata abilitata l'impostazione Configurazione computer\Modelli Amministrativi\componenti di Components\MDOP MBAM (BitLocker Management) \Client Management\Configure criteri di esenzione dall'utente, agli utenti verrà offerta la possibilità di richiedere un'esenzione.

Per impostazione predefinita, se l'utente richiede un'esenzione, l'esenzione sarà valida per 7 giorni e l'utente non riceverà le richieste di crittografia durante questo periodo. Il valore predefinito può essere aumentato o ridotto durante la configurazione dei criteri. Una volta terminato il periodo di esenzione, viene chiesto di crittografare l'utente.

Verrà visualizzata la voce seguente nel log eventi dell'amministratore di MBAM quando un computer è in esenzione dall'utente:

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

Se si vuole ignorare manualmente l'esenzione dall'utente per un computer, eseguire le operazioni seguenti:
 
1. Imposta il valore AllowUserExemption su **0** nella sottochiave del registro di sistema seguente: <br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. Eliminare tutti i valori del registro di sistema sotto la sottochiave del registro di sistema seguente, ad eccezione di **AgentVersion**, **EncodedComputerName**e **installato**:<br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM**

    **Nota** Per applicare le modifiche, è necessario riavviare l'agente MBAM.

Tenere presente che dopo l'applicazione di criteri di gruppo al computer, questi valori possono tornare alle impostazioni originali.

### Problema WMI

MBAM usa i metodi della classe win32_encryptablevolume per gestire BitLocker. Se questo modulo non è registrato o è corrotto, il client MBAM non funzionerà correttamente e verrà visualizzata la voce dell'evento seguente nel log eventi dell'amministratore di MBAM:

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

Si potrebbe inoltre notare che i criteri di ripristino e hardware non si applicano con il codice di errore 0x8007007e. Questo significa che non è stato possibile trovare il modulo specificato.

Per risolvere il problema, è necessario registrare nuovamente la classe **Win32_EncryptableVolume** usando il comando seguente:

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## Risoluzione dei problemi relativi alle comunicazioni di MBAM Agent

Questa sezione contiene informazioni per la risoluzione dei problemi seguenti correlate alla comunicazione tra gli agenti di MBAM:

### URL del servizio MBAM non corretto

Se il valore del servizio di stato o del ripristino e del servizio hardware di MBAM Compliance non è corretto, verrà visualizzata una voce di evento simile alla seguente nel registro eventi di amministrazione di MBAM nel computer client:

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

Verificare i valori di **KeyRecoveryServiceEndPoint** e **StatusReportingServiceEndpoint** sotto la sottochiave del registro di sistema seguente nel computer client: <br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Per impostazione predefinita, l'URL per KeyRecoveryServiceEndPoint (MBAM Recovery and hardware service endpoint) è il formato seguente: <br />
**http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

Per impostazione predefinita, l'URL per StatusReportingServiceEndpoint (l'endpoint del servizio di segnalazione dello stato di MBAM) è il formato seguente:<br />
**http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> L'URL non deve contenere spazi.

Se l'URL del servizio non è corretto, è consigliabile correggere l'URL del servizio nell'impostazione di criteri di gruppo seguente:

**Configurazione computer**  >  **Criteri**  >  **Modelli amministrativi**  >  **Componenti**  >  di Windows **MDOP mbam (Gestione BitLocker)**  >  **Gestione client**  >  **Configurare i servizi mbam**

### Problema di connettività che influisce sul server di amministrazione MBAM

L'agente MBAM non sarà in grado di pubblicare gli aggiornamenti del database se esistono problemi di connettività tra l'agente client e il server di amministrazione MBAM. In questo caso, noterai le voci di errore di connettività nel log eventi dell'amministratore di MBAM nel computer client:

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

* Verificare la connettività di base eseguendo il ping del server di amministrazione MBAM per nome e IP. Verificare se è possibile connettersi al sito Web o alla porta di servizio di MBAM Administration tramite Telnet o Portqry.

* Verificare che il servizio IIS sia in uso nel server di amministrazione e monitoraggio di MBAM e che il servizio Web MBAM sia in ascolto sulla stessa porta configurata nel computer client MBAM ( `netstat –ano | find "portnumber"` ).

* Verificare che il numero di porta configurato per il sito Web di MBAM usi IIS Manager (inetmgr). Verificare che il numero di porta sia uguale al numero di porta in cui il client sta ascoltando. Verificare che il numero di porta non sia condiviso da un'altra applicazione. Ad esempio, un'altra applicazione sul server non deve usare la stessa porta.

* Se è presente un firewall, verificare che la porta sia aperta nel firewall o nel server proxy.

* Se la comunicazione tra client e server è sicura, verificare che si stia usando un certificato SSL valido.

* Verificare la connettività di rete tra il server Web e il server di database a cui vengono inviati i dati per l'inserimento. È possibile controllare la connettività del database dal server Web al server di database usando l'amministratore dell'origine dati ODBC. Informazioni dettagliate sulla risoluzione dei problemi di connessione a SQL Server sono disponibili in [modalità di risoluzione dei problemi di connessione al motore di database di SQL Server](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).

#### Risoluzione dei problemi relativi al problema della connettività

Verificare che l'URL del servizio configurato nel client sia corretto. Copiare il valore dell'URL per KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) dal registro di sistema e aprirlo in Internet Explorer.

Analogamente, copiare il valore dell'URL per StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) e aprirlo in Internet Explorer.

> [!Note]
> Se non è possibile passare all'URL dal computer client, è consigliabile testare la connettività di rete di base dal client al server che sta usando IIS. Vedere i punti 1, 2, 3 e 4 nella sezione precedente.

Esaminare inoltre i registri dell'applicazione nel server di amministrazione e monitoraggio per eventuali errori.

È possibile creare una traccia di rete simultanea tra il client e il server e rivedere la traccia per determinare la causa dell'errore di connessione tra l'agente client e il server di amministrazione MBAM.

> [!Note]
> Se è possibile passare agli URL del servizio dal computer client e sono presenti voci di errore di connettività nei registri degli eventi di amministrazione di MBAM, potrebbe essere dovuto a un errore di connettività tra l'Administration Server e il server di database.

Se è possibile passare a entrambi gli URL del servizio e la connettività tra il client e il server in cui è in corso, IIS sta funzionando. Tuttavia, potrebbe essersi verificato un problema di comunicazione tra il server che sta usando IIS e il server di database.

I servizi MBAM potrebbero non essere in grado di connettersi al server di database a causa di un problema di rete o di un'impostazione di stringa di connessione database non corretta. Esaminare i registri dell'applicazione nel server di amministrazione e monitoraggio. È possibile che vengano visualizzate voci di errore o avvisi da ASP.NET di origine 2.0.50727.0 simili alla voce di log seguente:

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

#### Possibili cause

##### Causa 1

L'amministratore potrebbe avere specificato un nome di istanza di database non valido o un cognome di database durante l'installazione di componenti server di amministrazione e monitoraggio.

È possibile verificare e correggere le stringhe di connessione del database tramite la console di gestione di IIS. A questo scopo, aprire Gestione IIS e passare a amministrazione e monitoraggio di Microsoft BitLocker. Per ogni servizio elencato sul lato sinistro, eseguire la procedura seguente per modificare le stringhe di connessione del database:

1. In **visualizzazione funzionalità**fare doppio clic su **stringhe di connessione**.

2. Nella pagina **stringhe di connessione** selezionare la stringa di connessione che si vuole modificare.

3. Nel riquadro **azioni** selezionare **modifica**.

4. Nella finestra di dialogo **Modifica stringa di connessione** modificare le proprietà che si desidera modificare e quindi scegliere **OK**.

##### Causa 2

Porta di SQL Server bloccata nel firewall. Verificare il numero di porta in cui SQL Server è configurato per l'ascolto e verificare che la porta sia aperta nel firewall tra il server di amministrazione e il server di database.

##### Causa 3

Binding TCP/IP non corretti di SQL Server. Verificare i binding TCP/IP SQL in Gestione configurazione SQL Server nel server di database. MBAM richiede che i protocolli TCP/IP e named pipe siano abilitati per la connessione al database.

##### Causa 4

L'account del servizio NT Authority\Network o l'account del computer del server di amministrazione MBAM non dispone delle autorizzazioni necessarie per connettersi al database SQL.

Durante l'installazione di componenti di database nel server di database, il programma di installazione crea due gruppi locali: controllo di conformità di MBAM per l'accesso DB e recupero di MBAM e accesso DB hardware.

L'account del servizio NT Authority\Network, l'account del computer di MBAM Administration Server e l'utente che installa i componenti del database vengono aggiunti automaticamente a questi gruppi.

A questi gruppi vengono concesse le autorizzazioni necessarie per il database durante l'installazione. Tutti gli utenti che fanno parte di questo gruppo ricevono automaticamente le autorizzazioni necessarie per il database.

Il servizio Web potrebbe non connettersi al server di database a causa di un problema di autorizzazioni se una o più delle condizioni seguenti sono vere:

* I gruppi menzionati in precedenza vengono rimossi dai gruppi locali nel server di database.

* L'account del servizio NT Authority\Network e l'account del computer di MBAM Administration Server non sono membri di questi gruppi.

* Questi gruppi non dispongono delle autorizzazioni necessarie per il database.

Si noteranno errori relativi alle autorizzazioni nei registri dell'applicazione nel server di amministrazione e monitoraggio di MBAM se una delle condizioni precedenti è vera. In questo caso, devi aggiungere manualmente l'account del servizio NT Authority\Network e l'account del computer del server di amministrazione di MBAM e concedere loro un ruolo pubblico a livello di server nel server di database SQL che usa SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .

#### Esaminare i registri del servizio Web

Se nessun evento viene registrato nei registri dell'applicazione nel server di amministrazione MBAM, è il momento di esaminare i registri del servizio Web (con estensione svclog) del servizio Web di MBAM ospitati nel server di amministrazione e monitoraggio di mbam. Per visualizzare il file di log, sarà necessario usare lo strumento Visualizzatore di tracce di servizio (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx .

Dovresti studiare principalmente i log di traccia del servizio di RecoveryandHardwareService e ComplianceStatusService. Per impostazione predefinita, i registri dei servizi Web si trovano nella cartella di gestione di C:\inetpub\Microsoft BitLocker Solution\Logs. Ogni servizio scrive il proprio file con estensione svclog nella relativa cartella.

Esaminare l'attività nel log di traccia dei servizi per eventuali voci di errore o di avviso. Per impostazione predefinita, le voci di errore vengono evidenziate in rosso. Selezionare la descrizione dell'errore nel riquadro destro del Visualizzatore di traccia per visualizzare informazioni dettagliate sulla voce di errore. Di seguito è riportata una voce di errore di esempio dal log di traccia:

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

## Re-installazione o riconfigurazione dell'infrastruttura MBAM

Per reinstallare o riconfigurare l'infrastruttura MBAM, è necessario conoscere le operazioni seguenti:

* Account del pool di applicazioni

* Gruppi di MBAM (helpdesk, Advanced, gruppo report utenti)

* URL report MBAM

* Nomi di database e nome di SQL Server

* Account di MBAM ReadWrite e ReadOnly

### Account del pool di applicazioni

Per trovare l'account del pool di applicazioni, accedere al server Web MBAM, aprire **Gestione Internet Information Services (IIS)** e quindi selezionare **pool di applicazioni**:

![pool di applicazioni](images/troubleshooting-MBAM-installation-1.png)

Il nome dell'entità servizio (SPN) deve essere impostato in questo account. Questa impostazione è molto importante per la funzionalità di MBAM.

### Gruppi di MBAM (helpdesk, Advanced, report Users Group e reports URL)

![Gruppi di MBAM](images/troubleshooting-MBAM-installation-2.png)

In questo modo vengono fornite informazioni come il gruppo helpdesk, il gruppo helpdesk avanzato, il gruppo report utenti e l'URL report MBAM. L'URL di report MBAM deve essere fornito nella configurazione di MBAM e dovrebbe essere letto come: http (s)://servername/ReportServer.

### Nomi di database e nome di SQL Server (DB)

Per trovare i nomi e le istanze di SQL Server che ospitano MBAM DBs, accedere al server Web MBAM (IIS) e passare alla sottochiave del registro di sistema folowing:

**HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web**

![Regedit](images/troubleshooting-MBAM-installation-3.png)

Le parti evidenziate sono stringhe di connessione. Dovrebbero avere il nome di SQL Server, i nomi di database e le istanze (se denominati).

### Account di MBAM ReadWrite e ReadOnly

Queste informazioni si trovano nel database di SQL Server, per cui è già stato trovato il nome dal server Web.

#### Account di ReadWrite

1. Accedere a SQL Management Studio.

2. Fare clic con il pulsante destro del mouse su **mbam Recovery and hardware**, scegliere **Proprietà**e quindi selezionare **autorizzazioni**.

Ad esempio, il nome dell'account Lab è **MBAMWrite**. Il pool di applicazioni e gli account di ReadWrite sono impostati come uguali.

![SQL DB](images/troubleshooting-MBAM-installation-4.png)

![Proprietà DB](images/troubleshooting-MBAM-installation-5.png)

Passare alla pagina **sicurezza** e quindi **accedere** a SQL Management Studio. Passare all'account visualizzato nella schermata precedente.

![Sicurezza SQL](images/troubleshooting-MBAM-installation-6.png)

Fare clic con il pulsante destro del mouse sugli account, scegliere **Proprietà mapping utenti**e individuare il database di mbam Recovery and hardware:

![Mapping degli utenti](images/troubleshooting-MBAM-installation-7.png)

#### Account di sola lettura

Aprire Gestione configurazione di SQL Server Reporting Services nel server SSRS. Selezionare **URL Gestione report**e quindi esplorare gli **URL**:

![Gestione report](images/troubleshooting-MBAM-installation-8.png)

Selezionare **amministrazione e monitoraggio di Microsoft BitLocker**:

![Amministrazione e monitoraggio di BitLocker](images/troubleshooting-MBAM-installation-9.png)

Selezionare **MaltaDatasource**:

![DBs](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

MaltaDataSource dovrebbe avere il nome dell'account ReadOnly e dovrebbe essere usato nella configurazione di MBAM.

## Riferimento

Per informazioni, vedi gli articoli seguenti:

[Distribuzione di MBAM 2,5 in una configurazione autonoma](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
