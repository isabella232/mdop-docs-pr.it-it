---
title: Note sulla versione di MBAM 2.0 SP1
description: Note sulla versione di MBAM 2.0 SP1
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825585"
---
# Note sulla versione di MBAM 2.0 SP1


Per cercare queste note sulla versione, premere CTRL + F.

Leggere queste note sulla versione accuratamente prima di installare Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1). Queste note sulla versione contengono informazioni necessarie per installare correttamente l'amministrazione e il monitoraggio di BitLocker di 2,0 SP1 e contengono informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altre documentazioni di MBAM 2,0 SP1, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> Problemi noti di MBAM 2,0 SP1


Questa sezione contiene problemi noti per MBAM 2,0 SP1.

### L'aggiornamento di MBAM con la topologia integrata di Configuration Manager per MBAM 2,0 SP1 richiede la rimozione manuale degli oggetti di Configuration Manager

Se si usa MBAM con Configuration Manager e si vuole eseguire l'aggiornamento a MBAM 2,0 SP1, è necessario rimuovere manualmente tutti gli oggetti di Configuration Manager installati in Configuration Manager come parte dell'installazione di MBAM. Gli oggetti che è necessario rimuovere manualmente sono i report di MBAM, la raccolta di computer supportati MBAM e la previsione di configurazione della protezione BitLocker e gli elementi di configurazione associati.

**Soluzione alternativa**: aggiornare gli oggetti di Configuration Manager completando i passaggi seguenti:

1.  Eseguire il backup dei dati di conformità esistenti in un file esterno, come descritto nella procedura seguente.

    **Nota**  Tutti i dati di conformità di BitLocker esistenti verranno eliminati quando si elimina la previsione esistente in Gestione configurazione. I dati verranno rigenerati nel tempo, ma è consigliabile salvare una copia dei dati nel caso siano necessari i dati di conformità per un determinato computer prima che i dati di conformità vengano rigenerati.

     

    1.  Per salvare i dati cronologici relativi alla conformità di BitLocker, aprire il report **Dettagli conformità di BitLocker Enterprise** .

    2.  Fare clic sull'icona **Salva** nel report e selezionare **Excel**.

        Il report salvato conterrà dati come il nome del computer, il nome di dominio, lo stato di conformità, l'esenzione, gli utenti del dispositivo, i dettagli dello stato di conformità e la data/ora dell'ultimo contatto. Alcune informazioni, ad esempio informazioni dettagliate sul volume e forza di crittografia, non vengono salvate.

2.  Disinstallare **mbam** dal server tramite il programma di installazione di **mbam** .

3.  Eliminare manualmente gli oggetti seguenti da Configuration Manager:

    -   Raccolta di computer supportati MBAM

    -   Previsione protezione BitLocker

    -   Elemento di configurazione protezione unità sistema operativo BitLocker

    -   Elemento di configurazione della protezione delle unità dati fisse di BitLocker

4.  Eliminare manualmente la cartella di MBAM Reports nel sito di SQL Server Reporting Services di Configuration Manager. A tale scopo, effettua le seguenti operazioni:

    1.  Usare Internet Explorer per passare al punto di Reporting Services, ad esempio http:// &lt; yourcmserver &gt; /Reports.

    2.  Fare clic sul collegamento codice sito di Configuration Manager appropriato.

    3.  Eliminare la cartella MBAM.

5.  Usare il programma di installazione di MBAM server per reinstallare gli oggetti di integrazione di Configuration Manager. I computer client inizieranno a caricare di nuovo i dati di conformità di BitLocker nel tempo.

### Il pulsante Invia in Self-Service Portal non funziona in Internet Explorer10

Quando si usa Internet Explorer10 per accedere al sito Web di amministrazione e monitoraggio, il pulsante **Invia** nel sito Web non funziona.

**Soluzione alternativa**: nel server in cui è stato installato il sito Web di amministrazione e monitoraggio installare l' [hotfix per i file di definizione del browser ASP.NET](https://go.microsoft.com/fwlink/?LinkId=317798).

### I nomi di dominio internazionali non sono supportati

MBAM 2,0 SP1 non supporta i nomi di dominio internazionali.

**Soluzione alternativa**: None.

### I report nel sito Web amministrazione e monitoraggio visualizzano un avviso se SSL non è configurato in SSRS

Se SQLServer Reporting Services (SSRS) non è stato configurato per l'uso di Secure Socket Layer (SSL), l'URL per i report verrà impostato su HTTP invece che su HTTPS quando si installa il server MBAM. Se si passa al sito Web amministrazione e monitoraggio e si seleziona un report, viene visualizzato il messaggio seguente: "viene visualizzato solo il contenuto protetto".

**Soluzione alternativa**: per risolvere il problema, configurare SSL in **Gestione configurazione di Reporting Services** nel server mbam in cui è installato SqlServer Reporting Services. Disinstallare e quindi reinstallare il sito Web di amministrazione e monitoraggio Server.

### Se si fa clic di nuovo nel report di riepilogo conformità, potrebbe essere visualizzato un errore

Se si esegue il drill-down in un report di riepilogo conformità e quindi si fa clic sul collegamento a **ritroso** nel report SSRS, potrebbe verificarsi un errore.

**Soluzione alternativa**: None.

### Solo spazio usato la crittografia non funziona correttamente

Se si crittografa un computer per la prima volta dopo l'installazione del client MBAM e si imposta un oggetto Criteri di gruppo per implementare la crittografia solo spazio usato, MBAM crittografa erroneamente l'intero disco invece di crittografare solo lo spazio usato del disco. Se un computer è già crittografato con la crittografia solo spazio usato prima di installare il client MBAM ed è stato impostato lo stesso oggetto Criteri di gruppo crittografia solo spazio usato, MBAM riconosce l'impostazione e segnala correttamente la crittografia nei report di conformità.

**Soluzione alternativa**: None.

### La forza di cifratura viene visualizzata in modo non corretto nel report conformità computer

Se non si imposta un valore di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di criteri di gruppo della forza di cifratura, il report conformità computer nella topologia integrata di Configuration Manager Visualizza sempre **sconosciuto** per il livello di cifratura, anche quando l'intensità di cifratura usa il valore predefinito della crittografia a 128 bit. Il report Visualizza il livello di crittografia corretto se si imposta uno specifico livello di crittografia nell'oggetto Criteri di gruppo.

**Soluzione alternativa**: impostare sempre un livello di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di gruppo forza di cifratura.

### La distribuzione dello stato di conformità tramite il tipo di unità Visualizza dati obsoleti dopo l'aggiornamento degli elementi di configurazione

Dopo aver aggiornato gli elementi di configurazione di MBAM in SystemCenter2012 ConfigurationManager, la distribuzione dello stato di conformità tramite il grafico a barre del tipo di unità nel dashboard conformità Enterprise di BitLocker Mostra i dati basati sulle informazioni di versioni precedenti degli elementi di configurazione.

**Soluzione alternativa**: None. La modifica degli elementi di configurazione di MBAM non è supportata e il report potrebbe non essere visualizzato come previsto.

### La configurazione di sicurezza avanzata può causare la visualizzazione non corretta di report

Se la configurazione di sicurezza avanzata di Internet Explorer (ESC) è attivata, potrebbe essere visualizzato un messaggio di **Access denied** quando si prova a visualizzare i report nel server mbam. Per impostazione predefinita, la configurazione di sicurezza avanzata viene attivata per proteggere il server diminuendo l'esposizione del server a potenziali attacchi che possono verificarsi tramite il contenuto Web e gli script delle applicazioni.

**Soluzione alternativa**: se il messaggio di **accesso negato** viene visualizzato quando si prova a visualizzare i report nel server mbam, è possibile impostare un oggetto Criteri di gruppo o modificare manualmente l'impostazione predefinita nell'immagine per disabilitare la configurazione di sicurezza avanzata. È anche possibile visualizzare in alternativa i report di un altro computer in cui la configurazione di sicurezza avanzata non è abilitata.

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> L'installazione di MBAM server non riesce quando si esegue l'aggiornamento da SQLServer2008 a SQLServer2012

Se si esegue l'aggiornamento da SQLServer2008 a SQLServer2012 e quindi si prova a installare il database di conformità e di controllo o il database di ripristino, l'installazione non riesce e viene eseguito il rollback. Il problema si verifica perché il file SQLCMD.exe obbligatorio è stato rimosso durante l'aggiornamento di SQLServer e non può essere trovato dal programma di installazione di MBAM. Le righe del file di log MSI possono avere un aspetto simile al seguente:

RunDbInstallScript recupero DB CA: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript recupero DB CA: dbInstance-xxxxxx\\I01RunDbInstallScript Recovery DB CA: SqlScript-C:\\Programmi Files\\Microsoft\\Microsoft BitLocker Administration e Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB CA: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recupero DB CA: defaultFileName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript recupero DB CA: PercorsoDatiPredefinito-F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\RunDbInstallScript recupero DB CA: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recupero DB CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Programmi Files\\Microsoft\\Microsoft BitLocker Administration and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" PercorsoDatiPredefinito = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript recupero DB CA: iniziare a eseguire l'installazione del database di ripristino scriptRunDbInstallScript recupero DB CA: il file di log sqlcmd si trova in C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript recupero DB eccezione CA: installare l'eccezione di output della riga di comando dell'azione personalizzata del database di ripristino: il sistema non riesce a trovare il file specificato

Il server di Windows Installer di MBAM è hardcoded per trovare il percorso SQLCMD.exe guardando il valore della stringa Path nel registro di sistema in HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup. La chiave è ancora presente durante la migrazione da SQLServer2008 a SQLServer2012, ma il percorso a cui fa riferimento il valore dei dati non contiene il file SQLCMD.exe, perché il processo SqlUpgrade ha rimosso il file.

**Soluzione alternativa**: rinominare temporaneamente il valore stringa Path di HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup in **path \ _old**e quindi eseguire di nuovo Windows Installer sul server mbam. Dopo aver completato l'installazione e creato i database in SQLServer2012, rinominare **path \ _old** su **path**.

## Aggiornamenti rapidi e articoli della Knowledge base per MBAM 2,0 SP1


Questa sezione contiene gli aggiornamenti rapidi e gli articoli della KB per MBAM 2,0 SP1.

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


[Informazioni su MBAM 2.0 SP1](about-mbam-20-sp1.md)

 

 





