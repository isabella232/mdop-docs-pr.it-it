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
# Note sulla versione di MBAM 2.0


Per cercare queste note sulla versione, premere CTRL + F.

Leggere accuratamente queste note sulla versione prima di installare Microsoft BitLockerAdministration e monitoraggio (MBAM) 2.0. Queste note sulla versione contengono informazioni necessarie per installare correttamente BitLockerAdministration e il monitoraggio 2.0 e contengono informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altre documentazioni di MBAM 2.0, l'ultima modifica dovrebbe essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## <a href="" id="---------mbam-2-0-known-issues"></a> Problemi noti di MBAM 2.0


Questa sezione contiene le note sulla versione per MBAM 2.0.

### Il campo nome computer potrebbe non comparire nella conformità al computer di BitLocker e nei report dettagli conformità di BitLocker Enterprise quando si esegue MBAM con Microsoft System Center Configuration Manager 2007

Quando si usa MBAM con Configuration Manager 2007, il campo nome computer potrebbe essere vuoto nei report relativi ai dettagli relativi alla conformità con il computer e alla conformità di BitLocker Enterprise.

SOLUZIONE alternativa: None.

### Il report conformità aziendale non viene aggiornato dopo l'aggiornamento dell'infrastruttura server di MBAM autonoma

Se si usa la topologia autonoma di MBAM e si aggiorna l'infrastruttura del server dalla versione 1,0 a 2,0, non è possibile aggiornare il report conformità aziendale.

SOLUZIONE alternativa: dopo l'aggiornamento, eseguire lo script seguente nel database di conformità e controllo:

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

### I report nel portale help desk visualizzano un avviso se SSL non è configurato in SSRS

Se SQL Server Reporting Services (SSRS) non è stato configurato per l'uso di Secure Socket Layer (SSL), l'URL per i report verrà impostato su HTTP invece che su HTTPS quando si installa il server MBAM. Se si passa al portale help desk e si seleziona un report, viene visualizzato il messaggio seguente: "viene visualizzato solo il contenuto protetto".

SOLUZIONE alternativa: per visualizzare il report, fare clic su **Mostra tutto il contenuto**. Per risolvere il problema, passare al computer MBAM in cui è installato SQL Server Reporting Services, eseguire **Gestione configurazione di Reporting Services**e quindi fare clic su **URL servizio Web**. Selezionare il certificato SSL appropriato per il server, immettere la porta SSL appropriata (la porta predefinita è 443) e quindi fare clic su **applica**.

### Le istanze non predefinite del database di Configuration Manager non sono supportate

MBAM Cerca solo l'istanza predefinita del database di Configuration Manager in Configuration Manager 2007 e SystemCenter2012 ConfigurationManager. Se si usa un'istanza non predefinita, non è possibile installare MBAM.

SOLUZIONE alternativa: None.

### <a href="" id="clicking--back--in-the-compliance-summary-report-might-throw-an-error"></a>Se si fa clic su "back" nel report di riepilogo conformità, potrebbe essere generato un errore

Se si esegue il drill-down in un report di riepilogo conformità e quindi si fa clic sul collegamento a **ritroso** nel report SSRS, potrebbe essere generato un errore.

SOLUZIONE alternativa: None.

### Solo spazio usato la crittografia non funziona correttamente

Se si crittografa un computer per la prima volta dopo l'installazione del client MBAM e si imposta un oggetto Criteri di gruppo per implementare la crittografia solo spazio usato, MBAM crittografa erroneamente l'intero disco invece di crittografare solo lo spazio usato del disco. Se un computer è già crittografato quando si installa il client MBAM e si imposta lo stesso oggetto Criteri di gruppo, la crittografia funziona correttamente e crittografa solo lo spazio su disco usato nel computer.

SOLUZIONE alternativa: None.

### La forza di cifratura viene visualizzata in modo non corretto nel report conformità computer

Se non si imposta un valore di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di criteri di gruppo forza di crittografia, il report conformità computer nella topologia di integrazione di Configuration Manager Visualizza sempre "sconosciuto" per il livello di cifratura, anche quando l'intensità della cifratura usa l'impostazione predefinita della crittografia a 128 bit. Il report Visualizza il livello di crittografia corretto se si imposta uno specifico livello di crittografia nell'oggetto Criteri di gruppo.

SOLUZIONE alternativa: impostare sempre un livello di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di gruppo forza di cifratura.

### La distribuzione dello stato di conformità tramite il tipo di unità Visualizza dati obsoleti dopo l'aggiornamento degli elementi di configurazione

Dopo aver aggiornato gli elementi di configurazione di MBAM in SystemCenter2012 ConfigurationManager, la distribuzione dello stato di conformità tramite il grafico a barre del tipo di unità nel dashboard conformità Enterprise di BitLocker Mostra i dati basati sulle informazioni di versioni precedenti degli elementi di configurazione.

SOLUZIONE alternativa: None. La modifica degli elementi di configurazione di MBAM non è supportata e il report potrebbe non essere visualizzato come previsto.

### La configurazione di sicurezza avanzata può causare la visualizzazione non corretta di report

Se la configurazione di sicurezza avanzata di Internet Explorer (ESC) è attivata, potrebbe essere visualizzato un messaggio di "accesso negato" quando si prova a visualizzare i report nel server MBAM. Per impostazione predefinita, ESC è attivato per proteggere il server diminuendo l'esposizione del server a potenziali attacchi che possono verificarsi tramite il contenuto Web e gli script delle applicazioni.

SOLUZIONE alternativa: se viene visualizzato il messaggio "accesso negato" quando si prova a visualizzare i report nel server MBAM, è possibile impostare un oggetto Criteri di gruppo o modificare manualmente l'impostazione predefinita nell'immagine per disabilitare la configurazione di sicurezza avanzata. È anche possibile visualizzare in alternativa i report di un altro computer in cui ESC non è abilitato.

### L'installazione di MBAM server non riesce quando si esegue l'aggiornamento da SQL Server 2008 a SQL Server 2012

Se si esegue l'aggiornamento da SQL Server 2008 a SQL Server 2012 e si prova a installare il database di conformità e controllo o il database di ripristino, l'installazione non riesce e viene eseguito il rollback. Il problema si verifica perché il file SQLCMD.exe obbligatorio è stato rimosso durante l'aggiornamento di SQL e non può essere trovato dal programma di installazione di MBAM. Le righe del file di log MSI possono avere un aspetto simile al seguente:

RunDbInstallScript recupero DB CA: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript recupero DB CA: dbInstance-xxxxxx\\I01RunDbInstallScript Recovery DB CA: SqlScript-C:\\Programmi Files\\Microsoft\\Microsoft BitLocker Administration e Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recupero DB CA: defaultFileName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recupero DB CA: PercorsoDatiPredefinito-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript recupero DB CA: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recupero DB CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Programmi Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" PercorsoDatiPredefinito = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript recupero DB CA: iniziare a eseguire l'installazione del database di ripristino scriptRunDbInstallScript recupero DB CA: il file di log sqlcmd si trova in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript recupero DB eccezione CA: installare l'eccezione di output della riga di comando dell'azione personalizzata del database di ripristino: il sistema non riesce a trovare il file specificato

Il server di Windows Installer di MBAM è hardcoded per trovare il percorso SQLCMD.exe cercando nel valore stringa Path nel registro di sistema in HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup. La chiave è ancora presente durante la migrazione da SQL Server 2008 a SQL Server 2012, ma il percorso a cui fa riferimento il valore dei dati non contiene il file SQLCMD.exe, perché il processo di aggiornamento di SQL ha rimosso il file.

SOLUZIONE alternativa: rinominare temporaneamente il valore della stringa Path di HKLM\\Software\\Microsoft\\Microsoft SQL Server\\100\\Tools\\ClientSetup in **path \ _old**e quindi eseguire di nuovo il programma di installazione di Windows Installer di mbam server. Una volta completata l'installazione e creato i database in SQL Server 2012, rinominare il **percorso \ _old** valore in **path**.

## Aggiornamenti rapidi e articoli della Knowledge base per MBAM 2.0


Questa sezione contiene gli aggiornamenti rapidi e gli articoli della KB per MBAM 2.0.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Articolo KB</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>L'installazione di Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 non riesce con &quot; gli oggetti di System Center cm già installati&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>Gli utenti non possono recuperare la chiave di ripristino di BitLocker usando il portale self service di MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>Il client MBAM fallirebbe con l'ID evento 4 e il codice di errore 0x8004100E nella descrizione dell'evento</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>Messaggio di errore "errore del server nell'applicazione"/Reports "quando si fa clic sulla scheda report in MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Errore durante l'apertura di report di conformità Enterprise o computer in MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>I report di MBAM Enterprise non vengono aggiornati</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>L'installazione di MBAM in un controller di dominio non è supportata</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>Viene visualizzato il codice di errore 0x80071a90 durante la configurazione dell'integrazione di MBAM 2.0 standalone o Configuration Manager</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM e comunicazioni di rete sicure</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>La configurazione di MBAM 2.0 non riesce durante lo scenario di integrazione di Configuration Manager con SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>La configurazione di MBAM non riesce se SQL SSRS non è configurato correttamente</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>La configurazione di MBAM 2,0 non riesce con l' &quot; errore di recupero delle impostazioni del ruolo del server di Configuration Manager per &#39;ruolo&#39; del punto di Reporting Services&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>I report di MBAM 2.0 Enterprise non vengono aggiornati nella topologia standalone di MBAM 2.0 a causa di un errore di CreateCache processo SQL</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>I report di MBAM Enterprise non vengono aggiornati</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>I computer supportati da MBAM Reporting di conformità non corretto include i prodotti non supportati</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>Il record del computer viene rifiutato in MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Informazioni su MBAM 2.0](about-mbam-20-mbam-2.md)

 

 





