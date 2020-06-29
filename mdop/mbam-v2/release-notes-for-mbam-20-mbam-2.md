---
title: Note sulla versione di MBAM 2.0
description: Note sulla versione di MBAM 2.0
author: dansimp
ms.assetid: c3f16cf3-94f2-47ac-b3a4-3dc505c6a8dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d5d3c7d539cf2828d28c1844321bc34ab7736ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825586"
---
# <span data-ttu-id="858fa-103">Note sulla versione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="858fa-103">Release Notes for MBAM 2.0</span></span>


<span data-ttu-id="858fa-104">Per cercare queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="858fa-104">To search these release notes, press Ctrl+F.</span></span>

<span data-ttu-id="858fa-105">Leggere accuratamente queste note sulla versione prima di installare Microsoft BitLockerAdministration e monitoraggio (MBAM) 2.0.</span><span class="sxs-lookup"><span data-stu-id="858fa-105">Read these release notes thoroughly before you install Microsoft BitLockerAdministration and Monitoring(MBAM)2.0.</span></span> <span data-ttu-id="858fa-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente BitLockerAdministration e il monitoraggio 2.0 e contengono informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="858fa-106">These release notes contain information that is required to successfully install BitLockerAdministration and Monitoring2.0 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="858fa-107">Se c'è una differenza tra queste note sulla versione e altre documentazioni di MBAM 2.0, l'ultima modifica dovrebbe essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="858fa-107">If there is a difference between these release notes and other MBAM2.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="858fa-108">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="858fa-108">These release notes supersede the content that is included with this product.</span></span>

## <a href="" id="---------mbam-2-0-known-issues"></a> <span data-ttu-id="858fa-109">Problemi noti di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="858fa-109">MBAM2.0 Known Issues</span></span>


<span data-ttu-id="858fa-110">Questa sezione contiene le note sulla versione per MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="858fa-110">This section contains release notes for MBAM2.0.</span></span>

### <span data-ttu-id="858fa-111">Il campo nome computer potrebbe non comparire nella conformità al computer di BitLocker e nei report dettagli conformità di BitLocker Enterprise quando si esegue MBAM con Microsoft System Center Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="858fa-111">Computer Name field may not appear in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007</span></span>

<span data-ttu-id="858fa-112">Quando si usa MBAM con Configuration Manager 2007, il campo nome computer potrebbe essere vuoto nei report relativi ai dettagli relativi alla conformità con il computer e alla conformità di BitLocker Enterprise.</span><span class="sxs-lookup"><span data-stu-id="858fa-112">The Computer Name field may be blank in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you use MBAM with Configuration Manager 2007.</span></span>

<span data-ttu-id="858fa-113">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="858fa-113">WORKAROUND: None.</span></span>

### <span data-ttu-id="858fa-114">Il report conformità aziendale non viene aggiornato dopo l'aggiornamento dell'infrastruttura server di MBAM autonoma</span><span class="sxs-lookup"><span data-stu-id="858fa-114">Enterprise Compliance Report fails to update after you upgrade the Stand-alone MBAM server infrastructure</span></span>

<span data-ttu-id="858fa-115">Se si usa la topologia autonoma di MBAM e si aggiorna l'infrastruttura del server dalla versione 1,0 a 2,0, non è possibile aggiornare il report conformità aziendale.</span><span class="sxs-lookup"><span data-stu-id="858fa-115">If you are using the MBAM Stand-alone topology, and you upgrade the server infrastructure from version 1.0 to 2.0, the Enterprise Compliance Report fails to update.</span></span>

<span data-ttu-id="858fa-116">SOLUZIONE alternativa: dopo l'aggiornamento, eseguire lo script seguente nel database di conformità e controllo:</span><span class="sxs-lookup"><span data-stu-id="858fa-116">WORKAROUND: After the upgrade, run the following script on the Compliance and Audit Database:</span></span>

```sql
-- =============================================
-- Script Template
-- =============================================

DECLARE @DatabaseName nvarchar(255);
SET @DatabaseName = DB_NAME()

USE msdb;

DECLARE @JobID BINARY(16)
SELECT @JobID = job_id
FROM msdb.dbo.sysjobs
WHERE (name = N'CreateCache')

if (@JobID IS NOT NULL)
BEGIN
    EXEC dbo.sp_delete_job
         @job_name = N'CreateCache';
END

EXEC dbo.sp_add_job
    @job_name = N'CreateCache',
    @enabled = 1;

EXEC dbo.sp_add_jobstep
     @job_name = N'CreateCache',
     @step_name = N'Copy Data',
     @subsystem = N'TSQL',
     @command = N'EXEC [ComplianceCore].UpdateCache',
     @database_name = @DatabaseName,
     @retry_attempts = 5,
     @retry_interval = 5;


EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 010000,
     @active_end_time = 020000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7am',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 070000,
     @active_end_time = 080000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7am';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule1pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 130000,
     @active_end_time = 140000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule1pm';

EXEC dbo.sp_add_jobschedule
     @job_name = N'CreateCache',
     @name = N'ReportCacheSchedule7pm',
     @freq_type = 4,
     @freq_interval = 1,
     @active_start_time = 190000,
     @active_end_time = 200000;

EXEC dbo.sp_attach_schedule
     @job_name = N'CreateCache',
     @schedule_name = N'ReportCacheSchedule7pm';

EXEC dbo.sp_add_jobserver
     @job_name = N'CreateCache';
```

### <span data-ttu-id="858fa-117">I report nel portale help desk visualizzano un avviso se SSL non è configurato in SSRS</span><span class="sxs-lookup"><span data-stu-id="858fa-117">Reports in the Help Desk Portal display a warning if SSL is not configured in SSRS</span></span>

<span data-ttu-id="858fa-118">Se SQL Server Reporting Services (SSRS) non è stato configurato per l'uso di Secure Socket Layer (SSL), l'URL per i report verrà impostato su HTTP invece che su HTTPS quando si installa il server MBAM.</span><span class="sxs-lookup"><span data-stu-id="858fa-118">If SQL Server Reporting Services (SSRS) was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="858fa-119">Se si passa al portale help desk e si seleziona un report, viene visualizzato il messaggio seguente: "viene visualizzato solo il contenuto protetto".</span><span class="sxs-lookup"><span data-stu-id="858fa-119">If you then browse to the Help Desk Portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span>

<span data-ttu-id="858fa-120">SOLUZIONE alternativa: per visualizzare il report, fare clic su **Mostra tutto il contenuto**.</span><span class="sxs-lookup"><span data-stu-id="858fa-120">WORKAROUND: To show the report, click **Show All Content**.</span></span> <span data-ttu-id="858fa-121">Per risolvere il problema, passare al computer MBAM in cui è installato SQL Server Reporting Services, eseguire **Gestione configurazione di Reporting Services**e quindi fare clic su **URL servizio Web**.</span><span class="sxs-lookup"><span data-stu-id="858fa-121">To address this issue, go to the MBAM computer where SQL Server Reporting Services is installed, run **Reporting Services Configuration Manager**, and then click **Web Service URL**.</span></span> <span data-ttu-id="858fa-122">Selezionare il certificato SSL appropriato per il server, immettere la porta SSL appropriata (la porta predefinita è 443) e quindi fare clic su **applica**.</span><span class="sxs-lookup"><span data-stu-id="858fa-122">Select the appropriate SSL certificate for the server, enter the appropriate SSL port (the default port is 443), and then click **Apply**.</span></span>

### <span data-ttu-id="858fa-123">Le istanze non predefinite del database di Configuration Manager non sono supportate</span><span class="sxs-lookup"><span data-stu-id="858fa-123">Non-default instances of the Configuration Manager database are not supported</span></span>

<span data-ttu-id="858fa-124">MBAM Cerca solo l'istanza predefinita del database di Configuration Manager in Configuration Manager 2007 e SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="858fa-124">MBAM looks only for the default instance of the Configuration Manager database in Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span> <span data-ttu-id="858fa-125">Se si usa un'istanza non predefinita, non è possibile installare MBAM.</span><span class="sxs-lookup"><span data-stu-id="858fa-125">If you use a non-default instance, you cannot install MBAM.</span></span>

<span data-ttu-id="858fa-126">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="858fa-126">WORKAROUND: None.</span></span>

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a><span data-ttu-id="858fa-127">Se si fa clic su "back" nel report di riepilogo conformità, potrebbe essere generato un errore</span><span class="sxs-lookup"><span data-stu-id="858fa-127">Clicking “Back” in the Compliance Summary report might throw an error</span></span>

<span data-ttu-id="858fa-128">Se si esegue il drill-down in un report di riepilogo conformità e quindi si fa clic sul collegamento a **ritroso** nel report SSRS, potrebbe essere generato un errore.</span><span class="sxs-lookup"><span data-stu-id="858fa-128">If you drill down into a Compliance Summary report, and then click the **Back** link in the SSRS report, an error might be thrown.</span></span>

<span data-ttu-id="858fa-129">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="858fa-129">WORKAROUND: None.</span></span>

### <span data-ttu-id="858fa-130">Solo spazio usato la crittografia non funziona correttamente</span><span class="sxs-lookup"><span data-stu-id="858fa-130">Used Space Only Encryption does not work correctly</span></span>

<span data-ttu-id="858fa-131">Se si crittografa un computer per la prima volta dopo l'installazione del client MBAM e si imposta un oggetto Criteri di gruppo per implementare la crittografia solo spazio usato, MBAM crittografa erroneamente l'intero disco invece di crittografare solo lo spazio usato del disco.</span><span class="sxs-lookup"><span data-stu-id="858fa-131">If you encrypt a computer for the first time after you install the MBAM Client, and you have set a Group Policy Object to implement Used Space Only encryption, MBAM erroneously encrypts the entire disk instead of encrypting only the disk’s used space.</span></span> <span data-ttu-id="858fa-132">Se un computer è già crittografato quando si installa il client MBAM e si imposta lo stesso oggetto Criteri di gruppo, la crittografia funziona correttamente e crittografa solo lo spazio su disco usato nel computer.</span><span class="sxs-lookup"><span data-stu-id="858fa-132">If a computer is already encrypted when you install the MBAM Client, and you have set the same Group Policy Object, the encryption works correctly and encrypts only the used disk space on your computer.</span></span>

<span data-ttu-id="858fa-133">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="858fa-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="858fa-134">La forza di cifratura viene visualizzata in modo non corretto nel report conformità computer</span><span class="sxs-lookup"><span data-stu-id="858fa-134">Cipher strength displays incorrectly on the Computer Compliance report</span></span>

<span data-ttu-id="858fa-135">Se non si imposta un valore di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di criteri di gruppo forza di crittografia, il report conformità computer nella topologia di integrazione di Configuration Manager Visualizza sempre "sconosciuto" per il livello di cifratura, anche quando l'intensità della cifratura usa l'impostazione predefinita della crittografia a 128 bit.</span><span class="sxs-lookup"><span data-stu-id="858fa-135">If you do not set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object, the Computer Compliance report in the Configuration Manager Integration topology always displays “unknown” for the cipher strength, even when the cipher strength uses the default of 128-bit encryption.</span></span> <span data-ttu-id="858fa-136">Il report Visualizza il livello di crittografia corretto se si imposta uno specifico livello di crittografia nell'oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="858fa-136">The report displays the correct cipher strength if you set a specific cipher strength in the Group Policy Object.</span></span>

<span data-ttu-id="858fa-137">SOLUZIONE alternativa: impostare sempre un livello di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di gruppo forza di cifratura.</span><span class="sxs-lookup"><span data-stu-id="858fa-137">WORKAROUND: Always set a specific cipher strength in the **Choose drive encryption method and cipher strength** Group Policy Object.</span></span>

### <span data-ttu-id="858fa-138">La distribuzione dello stato di conformità tramite il tipo di unità Visualizza dati obsoleti dopo l'aggiornamento degli elementi di configurazione</span><span class="sxs-lookup"><span data-stu-id="858fa-138">Compliance Status Distribution By Drive Type displays old data after you update configuration items</span></span>

<span data-ttu-id="858fa-139">Dopo aver aggiornato gli elementi di configurazione di MBAM in SystemCenter2012 ConfigurationManager, la distribuzione dello stato di conformità tramite il grafico a barre del tipo di unità nel dashboard conformità Enterprise di BitLocker Mostra i dati basati sulle informazioni di versioni precedenti degli elementi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="858fa-139">After you update MBAM configuration items in SystemCenter2012 ConfigurationManager, the Compliance Status Distribution By Drive Type bar chart on the BitLocker Enterprise Compliance Dashboard shows data that is based on information from old versions of the configuration items.</span></span>

<span data-ttu-id="858fa-140">SOLUZIONE alternativa: None.</span><span class="sxs-lookup"><span data-stu-id="858fa-140">WORKAROUND: None.</span></span> <span data-ttu-id="858fa-141">La modifica degli elementi di configurazione di MBAM non è supportata e il report potrebbe non essere visualizzato come previsto.</span><span class="sxs-lookup"><span data-stu-id="858fa-141">Modification of the MBAM configuration items is not supported, and the report might not appear as expected.</span></span>

### <span data-ttu-id="858fa-142">La configurazione di sicurezza avanzata può causare la visualizzazione non corretta di report</span><span class="sxs-lookup"><span data-stu-id="858fa-142">Enhanced Security Configuration may cause reports to display incorrectly</span></span>

<span data-ttu-id="858fa-143">Se la configurazione di sicurezza avanzata di Internet Explorer (ESC) è attivata, potrebbe essere visualizzato un messaggio di "accesso negato" quando si prova a visualizzare i report nel server MBAM.</span><span class="sxs-lookup"><span data-stu-id="858fa-143">If Internet Explorer Enhanced Security Configuration (ESC) is turned on, an “Access Denied” message might appear when you try to view reports on the MBAM Server.</span></span> <span data-ttu-id="858fa-144">Per impostazione predefinita, ESC è attivato per proteggere il server diminuendo l'esposizione del server a potenziali attacchi che possono verificarsi tramite il contenuto Web e gli script delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="858fa-144">By default, ESC is turned on to protect the server by decreasing the server’s exposure to potential attacks that can occur through web content and application scripts.</span></span>

<span data-ttu-id="858fa-145">SOLUZIONE alternativa: se viene visualizzato il messaggio "accesso negato" quando si prova a visualizzare i report nel server MBAM, è possibile impostare un oggetto Criteri di gruppo o modificare manualmente l'impostazione predefinita nell'immagine per disabilitare la configurazione di sicurezza avanzata.</span><span class="sxs-lookup"><span data-stu-id="858fa-145">WORKAROUND: If the “Access Denied” message appears when you try to view reports on the MBAM Server, you can set a Group Policy Object or change the default manually in your image to disable Enhanced Security Configuration.</span></span> <span data-ttu-id="858fa-146">È anche possibile visualizzare in alternativa i report di un altro computer in cui ESC non è abilitato.</span><span class="sxs-lookup"><span data-stu-id="858fa-146">You can also alternatively view the reports from another computer on which ESC is not enabled.</span></span>

### <span data-ttu-id="858fa-147">L'installazione di MBAM server non riesce quando si esegue l'aggiornamento da SQL Server 2008 a SQL Server 2012</span><span class="sxs-lookup"><span data-stu-id="858fa-147">MBAM Server installation fails when you upgrade from SQL Server 2008 to SQL Server 2012</span></span>

<span data-ttu-id="858fa-148">Se si esegue l'aggiornamento da SQL Server 2008 a SQL Server 2012 e si prova a installare il database di conformità e controllo o il database di ripristino, l'installazione non riesce e viene eseguito il rollback.</span><span class="sxs-lookup"><span data-stu-id="858fa-148">If you upgrade from SQL Server 2008 to SQL Server 2012, and then try to install the Compliance and Audit Database or the Recovery Database, the installation fails and rolls back.</span></span> <span data-ttu-id="858fa-149">Il problema si verifica perché il file SQLCMD.exe obbligatorio è stato rimosso durante l'aggiornamento di SQL e non può essere trovato dal programma di installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="858fa-149">The failure occurs because the required SQLCMD.exe file was removed during the SQL upgrade and cannot be found by the MBAM installer.</span></span> <span data-ttu-id="858fa-150">Le righe del file di log MSI possono avere un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="858fa-150">The MSI log file lines may look similar to the following:</span></span>

<span data-ttu-id="858fa-151">RunDbInstallScript recupero DB CA: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript recupero DB CA: dbInstance-xxxxxx\\I01RunDbInstallScript Recovery DB CA: SqlScript-C:\\Programmi Files\\Microsoft\\Microsoft BitLocker Administration e Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recupero DB CA: defaultFileName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recupero DB CA: PercorsoDatiPredefinito-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript recupero DB CA: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recupero DB CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Programmi Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" PercorsoDatiPredefinito = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript recupero DB CA: iniziare a eseguire l'installazione del database di ripristino scriptRunDbInstallScript recupero DB CA: il file di log sqlcmd si trova in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript recupero DB eccezione CA: installare l'eccezione di output della riga di comando dell'azione personalizzata del database di ripristino: il sistema non riesce a trovare il file specificato</span><span class="sxs-lookup"><span data-stu-id="858fa-151">RunDbInstallScript Recovery Db CA: BinDir - E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript Recovery Db CA: dbInstance - xxxxxx\\I01RunDbInstallScript Recovery Db CA: sqlScript- C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery Db CA: dbName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultFileName- MBAM\_Recovery\_and\_HardwareRunDbInstallScript Recovery Db CA: defaultDataPath- F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\RunDbInstallScript Recovery Db CA: defaultLogPath- K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\RunDbInstallScript Recovery Db CA: scriptLogPath - C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e -E -S xxxxxxx\\I01 -i "C:\\Program Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql" -v DatabaseName="MBAM\_Recovery\_and\_Hardware" DefaultFileName="MBAM\_Recovery\_and\_Hardware" DefaultDataPath="F:\\MSSQL\\MSSQL10.I01\\MSSQL\\DATA\\" DefaultLogPath="K:\\MSSQL\\MSSQL10.I01\\MSSQL\\Data\\" -o "C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log"RunDbInstallScript Recovery Db CA:Starting to run the Recovery database install scriptRunDbInstallScript Recovery Db CA: Sqlcmd log file is located in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript Recovery Db CA Exception: Install Recovery database Custom Action command line output Exception: The system cannot find the file specified</span></span>

<span data-ttu-id="858fa-152">Il server di Windows Installer di MBAM è hardcoded per trovare il percorso SQLCMD.exe cercando nel valore stringa Path nel registro di sistema in HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span><span class="sxs-lookup"><span data-stu-id="858fa-152">The MBAM Server Windows Installer is hardcoded to find the SQLCMD.exe path by looking in the Path string value in the registry under HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup.</span></span> <span data-ttu-id="858fa-153">La chiave è ancora presente durante la migrazione da SQL Server 2008 a SQL Server 2012, ma il percorso a cui fa riferimento il valore dei dati non contiene il file SQLCMD.exe, perché il processo di aggiornamento di SQL ha rimosso il file.</span><span class="sxs-lookup"><span data-stu-id="858fa-153">The key is still present during the migration from SQL Server 2008 to SQL Server 2012, but the path that is referenced by the data value does not contain the SQLCMD.exe file, because the SQL upgrade process removed the file.</span></span>

<span data-ttu-id="858fa-154">SOLUZIONE alternativa: rinominare temporaneamente il valore della stringa Path di HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup in **path \ _old**e quindi eseguire di nuovo il programma di installazione di Windows Installer di mbam server.</span><span class="sxs-lookup"><span data-stu-id="858fa-154">WORKAROUND: Temporarily rename the HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup Path string value to **Path\_old**, and then re-run the MBAM Server Windows Installer.</span></span> <span data-ttu-id="858fa-155">Una volta completata l'installazione e creato i database in SQL Server 2012, rinominare il **percorso \ _old** valore in **path**.</span><span class="sxs-lookup"><span data-stu-id="858fa-155">When the installation completes successfully and creates the databases in SQL Server 2012, rename the **Path\_old** value to **Path**.</span></span>

## <span data-ttu-id="858fa-156">Aggiornamenti rapidi e articoli della Knowledge base per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="858fa-156">Hotfixes and Knowledge Base articles for MBAM2.0</span></span>


<span data-ttu-id="858fa-157">Questa sezione contiene gli aggiornamenti rapidi e gli articoli della KB per MBAM 2.0.</span><span class="sxs-lookup"><span data-stu-id="858fa-157">This section contains hotfixes and KB articles for MBAM2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="858fa-158">Articolo KB</span><span class="sxs-lookup"><span data-stu-id="858fa-158">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="858fa-159">Title</span><span class="sxs-lookup"><span data-stu-id="858fa-159">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="858fa-160">Link</span><span class="sxs-lookup"><span data-stu-id="858fa-160">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="858fa-161">2831166</span><span class="sxs-lookup"><span data-stu-id="858fa-161">2831166</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-162">L'installazione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 non riesce con &quot; gli oggetti di System Center cm già installati&quot;</span><span class="sxs-lookup"><span data-stu-id="858fa-162">Installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 fails with &quot;System Center CM Objects Already Installed&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)"><span data-ttu-id="858fa-163">support.microsoft.com/kb/2831166/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-163">support.microsoft.com/kb/2831166/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="858fa-164">2870849</span><span class="sxs-lookup"><span data-stu-id="858fa-164">2870849</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-165">Gli utenti non possono recuperare la chiave di ripristino di BitLocker usando il portale self service di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="858fa-165">Users cannot retrieve BitLocker Recovery key using MBAM2.0 Self Service Portal</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)"><span data-ttu-id="858fa-166">support.microsoft.com/kb/2870849/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-166">support.microsoft.com/kb/2870849/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="858fa-167">2756402</span><span class="sxs-lookup"><span data-stu-id="858fa-167">2756402</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-168">Il client MBAM fallirebbe con l'ID evento 4 e il codice di errore 0x8004100E nella descrizione dell'evento</span><span class="sxs-lookup"><span data-stu-id="858fa-168">MBAM client would fail with Event ID 4 and error code 0x8004100E in the Event description</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)"><span data-ttu-id="858fa-169">support.microsoft.com/kb/2756402/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-169">support.microsoft.com/kb/2756402/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="858fa-170">2620287</span><span class="sxs-lookup"><span data-stu-id="858fa-170">2620287</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-171">Messaggio di errore "errore del server nell'applicazione"/Reports "quando si fa clic sulla scheda report in MBAM</span><span class="sxs-lookup"><span data-stu-id="858fa-171">Error Message “Server Error in ‘/Reports’ Application” When You Click Reports Tab in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)"><span data-ttu-id="858fa-172">support.microsoft.com/kb/2620287/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-172">support.microsoft.com/kb/2620287/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="858fa-173">2639518</span><span class="sxs-lookup"><span data-stu-id="858fa-173">2639518</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-174">Errore durante l'apertura di report di conformità Enterprise o computer in MBAM</span><span class="sxs-lookup"><span data-stu-id="858fa-174">Error opening Enterprise or Computer Compliance Reports in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)"><span data-ttu-id="858fa-175">support.microsoft.com/kb/2639518/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-175">support.microsoft.com/kb/2639518/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="858fa-176">2620269</span><span class="sxs-lookup"><span data-stu-id="858fa-176">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-177">I report di MBAM Enterprise non vengono aggiornati</span><span class="sxs-lookup"><span data-stu-id="858fa-177">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="858fa-178">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-178">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="858fa-179">2712461</span><span class="sxs-lookup"><span data-stu-id="858fa-179">2712461</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-180">L'installazione di MBAM in un controller di dominio non è supportata</span><span class="sxs-lookup"><span data-stu-id="858fa-180">Installing MBAM on a Domain Controller is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)"><span data-ttu-id="858fa-181">support.microsoft.com/kb/2712461/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-181">support.microsoft.com/kb/2712461/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="858fa-182">2876732</span><span class="sxs-lookup"><span data-stu-id="858fa-182">2876732</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-183">Viene visualizzato il codice di errore 0x80071a90 durante la configurazione dell'integrazione di MBAM 2.0 standalone o Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="858fa-183">You receive error code 0x80071a90 during Standalone or Configuration Manager Integration setup of MBAM2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)"><span data-ttu-id="858fa-184">support.microsoft.com/kb/2876732/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-184">support.microsoft.com/kb/2876732/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="858fa-185">2754259</span><span class="sxs-lookup"><span data-stu-id="858fa-185">2754259</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-186">MBAM e comunicazioni di rete sicure</span><span class="sxs-lookup"><span data-stu-id="858fa-186">MBAM and Secure Network Communication</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)"><span data-ttu-id="858fa-187">support.microsoft.com/kb/2754259/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-187">support.microsoft.com/kb/2754259/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="858fa-188">2870842</span><span class="sxs-lookup"><span data-stu-id="858fa-188">2870842</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-189">La configurazione di MBAM 2.0 non riesce durante lo scenario di integrazione di Configuration Manager con SQL Server 2008</span><span class="sxs-lookup"><span data-stu-id="858fa-189">MBAM2.0 Setup fails during Configuration Manager Integration Scenario with SQL Server 2008</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)"><span data-ttu-id="858fa-190">support.microsoft.com/kb/2870842/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-190">support.microsoft.com/kb/2870842/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="858fa-191">2668533</span><span class="sxs-lookup"><span data-stu-id="858fa-191">2668533</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-192">La configurazione di MBAM non riesce se SQL SSRS non è configurato correttamente</span><span class="sxs-lookup"><span data-stu-id="858fa-192">MBAM Setup fails if SQL SSRS is not configured properly</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)"><span data-ttu-id="858fa-193">support.microsoft.com/kb/2668533/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-193">support.microsoft.com/kb/2668533/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="858fa-194">2870847</span><span class="sxs-lookup"><span data-stu-id="858fa-194">2870847</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-195">La configurazione di MBAM 2,0 non riesce con l' &quot; errore di recupero delle impostazioni del ruolo del server di Configuration Manager per &#39;ruolo&#39; del punto di Reporting Services&quot;</span><span class="sxs-lookup"><span data-stu-id="858fa-195">MBAM 2.0 Setup fails with &quot;Error retrieving Configuration Manager Server role settings for &#39;Reporting Services Point&#39; role&quot;</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)"><span data-ttu-id="858fa-196">support.microsoft.com/kb/2870847/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-196">support.microsoft.com/kb/2870847/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="858fa-197">2870839</span><span class="sxs-lookup"><span data-stu-id="858fa-197">2870839</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-198">I report di MBAM 2.0 Enterprise non vengono aggiornati nella topologia standalone di MBAM 2.0 a causa di un errore di CreateCache processo SQL</span><span class="sxs-lookup"><span data-stu-id="858fa-198">MBAM2.0 Enterprise Reports are not refreshed in MBAM2.0 Standalone topology due to SQL job CreateCache failure</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)"><span data-ttu-id="858fa-199">support.microsoft.com/kb/2870839/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-199">support.microsoft.com/kb/2870839/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="858fa-200">2620269</span><span class="sxs-lookup"><span data-stu-id="858fa-200">2620269</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-201">I report di MBAM Enterprise non vengono aggiornati</span><span class="sxs-lookup"><span data-stu-id="858fa-201">MBAM Enterprise Reporting Not Getting Updated</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)"><span data-ttu-id="858fa-202">support.microsoft.com/kb/2620269/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-202">support.microsoft.com/kb/2620269/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="858fa-203">2935997</span><span class="sxs-lookup"><span data-stu-id="858fa-203">2935997</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-204">I computer supportati da MBAM Reporting di conformità non corretto include i prodotti non supportati</span><span class="sxs-lookup"><span data-stu-id="858fa-204">MBAM Supported Computers compliance reporting incorrectly includes unsupported products</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)"><span data-ttu-id="858fa-205">support.microsoft.com/kb/2935997/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-205">support.microsoft.com/kb/2935997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="858fa-206">2612822</span><span class="sxs-lookup"><span data-stu-id="858fa-206">2612822</span></span></p></td>
<td align="left"><p><span data-ttu-id="858fa-207">Il record del computer viene rifiutato in MBAM</span><span class="sxs-lookup"><span data-stu-id="858fa-207">Computer Record is Rejected in MBAM</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)"><span data-ttu-id="858fa-208">support.microsoft.com/kb/2612822/EN-US</span><span class="sxs-lookup"><span data-stu-id="858fa-208">support.microsoft.com/kb/2612822/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="858fa-209">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="858fa-209">Related topics</span></span>


[<span data-ttu-id="858fa-210">Informazioni su MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="858fa-210">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)

 

 





