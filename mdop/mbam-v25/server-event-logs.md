---
title: Registri eventi del server
description: Registri eventi del server
author: dansimp
ms.assetid: 04e724d2-28cc-4fa8-86a1-0d4ab0234b11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 269e9b4bc2644fae4dc5796652c7587bb0ef6076
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823385"
---
# Registri eventi del server


Le tabelle in questa sezione contengono informazioni sugli ID eventi di MBAM server log.

## Configurazione


La tabella seguente contiene i messaggi e le informazioni sulla risoluzione dei problemi per gli ID evento che possono verificarsi nel server MBAM durante la configurazione.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ID evento</th>
<th align="left">Source</th>
<th align="left">Simbolo dell'evento</th>
<th align="left">Messaggio</th>
<th align="left">Risoluzione dei problemi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/operativo</p></td>
<td align="left"><p>VssRegistrationException</p></td>
<td align="left"><p>È stata generata un'eccezione durante la registrazione VSS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/operativo</p></td>
<td align="left"><p>VssDeregistrationException</p></td>
<td align="left"><p>È stata generata un'eccezione durante l'annullamento della registrazione di VSS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>300</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>CmdletError</p></td>
<td align="left"><p>Errore nella rimozione della cartella.</p></td>
<td align="left"><p>Indica che si è verificato un errore di terminazione durante l'esecuzione di un'attività. Controlla altri messaggi di evento nel log per diagnosticare ulteriormente la configurazione di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>301</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>cmdletUnexpectedError</p></td>
<td align="left"><p>Errore del cmdlet imprevisto.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>302</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>CmdletWarning</p></td>
<td align="left"><p>Avviso cmdlet.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>303</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/operativo</p></td>
<td align="left"><p>CmdletInformation</p></td>
<td align="left"><p>Informazioni sui cmdlet.</p></td>
<td align="left"><p>Solo informativo; non è necessario alcun intervento di risoluzione dei problemi. L'evento indica che un'attività è in esecuzione dai cmdlet, ad esempio enabling\disabling, o annullamento di un'operazione.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>400</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>ConfiguratorError</p></td>
<td align="left"><p>Errore configuratore.</p></td>
<td align="left"><p>Indica che si è verificato un errore durante l'avvio di MBAM Configurator. Assicurarsi che l'utente disponga di privilegi adeguati per avviare MBAM Configurator.</p></td>
</tr>
<tr class="even">
<td align="left"><p>401</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>ConfiguratorUnexpectedError</p></td>
<td align="left"><p>Errore configuratore imprevisto.</p></td>
<td align="left"><p>Indica che si è verificato un errore di terminazione durante l'esecuzione di un'attività di MBAM Configurator. Il messaggio di errore conterrà altri dettagli sull'errore. Controlla altri messaggi di errore nel log eventi per diagnosticare ulteriormente la configurazione di MBAM. Gli errori noti includono:</p>
<ul>
<li><p>Errore di recupero o convalida di un certificato selezionato dall'utente</p></li>
<li><p>Errore di analisi dell'URL dei report</p></li>
<li><p>Errore di apertura dei log eventi per l'utente</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>402</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>ConfiguratorWarning</p></td>
<td align="left"><p>Avviso configuratore.</p></td>
<td align="left"><p>Indica che un'attività di MBAM Configurator non è completa come previsto, ma non ha superato completamente. Le attività note includono un certificato mancante nello Store LocalMachine\My configurato nella caratteristica applicazione Web oppure un timeout per un'attività in sospeso.</p></td>
</tr>
<tr class="even">
<td align="left"><p>410</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/operativo</p></td>
<td align="left"><p>ConfiguratorInformation</p></td>
<td align="left"><p>Informazioni configuratore.</p></td>
<td align="left"><p>Solo informativo; non è necessario alcun intervento di risoluzione dei problemi. L'evento indica che un'attività viene richiamata da MBAM Configurator. Le attività note includono:</p>
<ul>
<li><p>Avvio del configuratore</p></li>
<li><p>Controllo dei prerequisiti software per una caratteristica di MBAM</p></li>
<li><p>Convalida dei parametri per una caratteristica di MBAM</p></li>
<li><p>Enabling\disabling\committing una caratteristica di MBAM</p></li>
<li><p>Generazione di uno script di PowerShell dal configuratore</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>500</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>WebProviderUnexpectedError</p></td>
<td align="left"><p>Errore imprevisto del provider di applicazioni Web.</p></td>
<td align="left"><p>Indica che si è verificato un errore durante l'abilitazione e la configurazione di un sito Web o di un servizio Web di MBAM in IIS. Gli errori noti includono:</p>
<ul>
<li><p>Errore nella ricerca della cartella radice di IIS WWW</p></li>
<li><p>Errore di accesso alla configurazione di IIS in web.config a causa di file non validi o di impostazioni mancanti</p></li>
<li><p>Errore di creazione o rimozione di un'applicazione Web</p></li>
<li><p>Violazione di accesso a IIS</p></li>
</ul>
<p>Questo errore viene registrato anche se MBAM non può accedere a Active Directory (AD) per convalidare gli account utente. Verificare che IIS sia installato, configurato correttamente e che il servizio IIS sia in funzione. Verificare che tutti i controlli dei prerequisiti software di MBAM vengano superati. Verificare che l'utente disponga delle autorizzazioni corrette per creare applicazioni Web nell'istanza di IIS. Verificare che l'utente abbia accesso alla lettura degli oggetti dell'account utente in Active Directory.</p></td>
</tr>
<tr class="even">
<td align="left"><p>501</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>WebProviderError</p></td>
<td align="left"><p>Errore imprevisto del provider di applicazioni Web.</p></td>
<td align="left"><p>Indica che si è verificato un errore durante l'abilitazione, la disattivazione o la configurazione di un sito Web o un servizio Web di MBAM in IIS. Gli errori noti includono:</p>
<ul>
<li><p>Errore di lettura delle informazioni di binding di base o WSHttp da IIS</p></li>
<li><p>Sezione identità mancante o voce DNS nella sezione identità nei file di configurazione di IIS</p></li>
<li><p>Errore di apertura della chiave del registro di sistema HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>Errore di lettura del valore PathWWWRoot dalla chiave del registro di sistema HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>L'utente sta provando a specificare un nome di directory virtuale con un nome riservato per MBAM</p></li>
</ul>
<p>Verificare che IIS sia installato e configurato correttamente. Verificare che la chiave del registro di sistema HKLM\SOFTWARE\Microsoft\InetStp: PathWWWRoot esista e sia accessibile. Verificare che le informazioni di binding in IIS non siano danneggiate.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>502</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>WebProviderWarning</p></td>
<td align="left"><p>Avviso del provider di applicazioni Web.</p></td>
<td align="left"><p>Indica che si è verificato un errore non fatale durante l'abilitazione di un sito Web o di un servizio Web MBAM. Gli errori noti includono:</p>
<ul>
<li><p>Errore di accesso ad Active Directory per convalidare il nome dell'entità servizio (SPN) nell'account del pool di app</p></li>
<li><p>Errore di convalida del nome SPN perché assegnato a più account in Active Directory</p></li>
<li><p>Errore di registrazione di un nome SPN nell'account del pool di app in Active Directory</p></li>
<li><p>Il nome SPN è registrato su un account diverso dal pool di app in Active Directory</p></li>
<li><p>Errore di rimozione di SPN dall'account del pool di app in Active Directory durante un'operazione di rollback</p></li>
<li><p>Non è possibile verificare se al gruppo IIS_IUSRS è stato concesso il privilegio di accesso come batch nel server IIS</p></li>
</ul>
<p>Il messaggio dell'evento conterrà ulteriori informazioni sull'errore specifico. Verificare che l'annuncio sia raggiungibile dal server in cui è in corso la configurazione di MBAM. Verificare che l'utente che ha eseguito la configurazione di MBAM disponga delle autorizzazioni di lettura per l'account del pool di app in Active Directory. Se un nome SPN è già registrato nell'account del pool di app in AD, assicurati che non sia registrato in altri account.</p></td>
</tr>
<tr class="even">
<td align="left"><p>503</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/operativo</p></td>
<td align="left"><p>WebProviderInformation</p></td>
<td align="left"><p>Informazioni sul provider di applicazioni Web. Descrizione</p></td>
<td align="left"><p>Solo informativo; non è necessario alcun intervento di risoluzione dei problemi. L'evento indica che un'attività viene richiamata dalla configurazione di MBAM. Le attività note includono la configurazione di IIS, ad esempio le informazioni di binding e il sito radice, e la configurazione del nome dell'entità servizio (SPN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>600</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>SetupUnexpectedError</p></td>
<td align="left"><p>Errore di configurazione imprevisto.</p></td>
<td align="left"><p>Indica che si è verificato un errore di terminazione durante la enabling\disabling o la configurazione di una caratteristica di MBAM. Gli errori noti includono:</p>
<ul>
<li><p>Errore durante il rollback di un'attività dopo un errore</p></li>
<li><p>Errore di lettura dal registro di sistema</p></li>
<li><p>Errore di creare o eliminare una cartella nel file System</p></li>
<li><p>Errore di lettura delle informazioni sulla versione SQL</p></li>
<li><p>Errore di registrazione di writer VSS in SQL</p></li>
</ul>
<p>Il messaggio dell'evento conterrà ulteriori informazioni sull'errore specifico. Verificare che tutti i controlli prerequisito del software MBAM passino. Verificare che il percorso del registro di sistema MBAM, se esistente, HKEY_LOCAL_MACHINE server \SOFTWARE\Microsoft\MBAM e tutte le sottochiavi siano leggibili. Verificare che l'annuncio sia raggiungibile dal server in cui è in corso la configurazione di MBAM. Verificare che l'utente che ha eseguito la configurazione di MBAM disponga delle autorizzazioni di lettura in Active Directory.</p>
<p>Per una registrazione di VSS writer di successo, verificare che sia installata una versione supportata di SQL e che un'istanza sia accessibile all'utente che sta usando la configurazione di MBAM. Se la disabilitazione di una caratteristica MBAM o la disinstallazione di MBAM verificare che tutti i file, ad esempio i file di log e i file di web.config, vengano chiusi in modo che MBAM possa rimuovere i siti Web e i servizi Web.</p></td>
</tr>
<tr class="even">
<td align="left"><p>601</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>SetupError</p></td>
<td align="left"><p>Errore di installazione.</p></td>
<td align="left"><p>Indica che si è verificato un errore di terminazione durante la enabling\disabling o la configurazione di una caratteristica di MBAM. Gli errori noti includono:</p>
<ul>
<li><p>Errore di lettura della configurazione di MBAM in IIS</p></li>
<li><p>Sezione appSettings corrotta in configurazione IIS o impostazioni non configurate correttamente</p></li>
<li><p>Errore di convalida del nome host</p></li>
<li><p>Errore di lettura delle informazioni sulla versione SQL</p></li>
<li><p>Errore di registrazione di writer VSS in SQL</p></li>
</ul>
<p>Il messaggio dell'evento conterrà ulteriori informazioni sull'errore specifico. Verificare che IIS sia installato e configurato in modo corretto. Verificare che tutti i controlli prerequisito del software MBAM passino. Per una registrazione di VSS writer di successo, verificare che sia installata una versione supportata di SQL e che un'istanza sia accessibile all'utente che sta usando la configurazione di MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>602</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>SetupWarning</p></td>
<td align="left"><p>Avviso di configurazione.</p></td>
<td align="left"><p>Indica che si è verificato un errore non fatale durante l'enabling\disabling o la configurazione di una caratteristica di MBAM come l'integrazione di Configuration Manager (CM) o l'applicazione Web MBAM. Gli errori noti includono: la mancata eliminazione di report MBAM dal punto di ruolo SRS nel CM e la mancata risoluzione di un nome host dal controller di dominio. Il messaggio dell'evento conterrà ulteriori informazioni sull'errore specifico.</p>
<p>Verificare che l'annuncio sia raggiungibile dal server in cui è in corso la configurazione di MBAM. Verificare che l'utente che ha eseguito la configurazione di MBAM disponga delle autorizzazioni di rimozione per l'istanza di SSRS configurata come punto di ruolo SRS in CM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>603</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/operativo</p></td>
<td align="left"><p>SetupInformation</p></td>
<td align="left"><p>Informazioni sulla configurazione.</p></td>
<td align="left"><p>Solo informativo; non è necessario alcun intervento di risoluzione dei problemi.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>605</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>WebProviderSoftwareCheckFailure</p></td>
<td align="left"><p>L'applicazione Web non può essere abilitata perché non vengono soddisfatte una o più dipendenze del software.</p></td>
<td align="left"><p>Durante l'installazione di MBAM sito Web/servizio Web, la configurazione di MBAM verifica se sono presenti prerequisiti necessari. Questo messaggio indica che MBAM non è riuscito a installare il sito Web o il servizio Web richiesto perché manca il presupposto necessario. Vedere i messaggi di errore che precedono questo messaggio per ottenere altre informazioni sui prerequisiti mancanti.</p></td>
</tr>
<tr class="even">
<td align="left"><p>606</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>SetupParameterValidationFailure</p></td>
<td align="left"><p>Il parametro necessario per abilitare la caratteristica del server non è stato specificato o non ha superato la convalida.</p></td>
<td align="left"><p>Indica che il parametro necessario per configurare una caratteristica di MBAM non è stato specificato o non ha superato la convalida.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>607</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>SetupParameterValidationFailureWithError</p></td>
<td align="left"><p>Errore riscontrato durante il tentativo di convalidare il parametro specificato necessario per abilitare la funzionalità del server.</p></td>
<td align="left"><p>Indica che si è verificato un errore durante il tentativo di convalidare il parametro specificato necessario per abilitare la funzionalità del server.</p></td>
</tr>
<tr class="even">
<td align="left"><p>700</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>DbProviderUnexpectedError</p></td>
<td align="left"><p>Errore imprevisto del provider DB.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>701</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>DbProviderError</p></td>
<td align="left"><p>Errore del provider DB.</p></td>
<td align="left"><p>Il messaggio contenuto nella sezione EventDetails deve contenere ulteriori informazioni sull'errore effettivo. Queste sono alcune delle aree da verificare:</p>
<ul>
<li><p>La configurazione di MBAM non è riuscita a connettersi al database usando le informazioni di connessione fornite. Verificare i dettagli della stringa di connessione forniti per la configurazione di MBAM.</p></li>
<li><p>La configurazione di MBAM non può connettersi al database specificato usando le credenziali dell'account di dominio specificato. Verificare che il nome utente e la password dell'account di dominio siano validi.</p></li>
<li><p>La configurazione di MBAM non può connettersi al database specificato usando le credenziali dell'account di dominio specificato. Verificare che l'account di dominio fornito disponga delle autorizzazioni necessarie per connettersi al database MBAM.</p></li>
<li><p>MBAM DAC PAC non riuscirà se è già installata una versione più recente di database MBAM. Verificare che non esista una nuova versione di MBAM DBs nel server SQL specifico.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>702</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>DbProviderWarning</p></td>
<td align="left"><p>Avviso provider DB.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>703</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/operativo</p></td>
<td align="left"><p>DbProviderInformation</p></td>
<td align="left"><p>Informazioni sul provider DB.</p></td>
<td align="left"><p>Solo informativo; non è necessario alcun intervento di risoluzione dei problemi.</p></td>
</tr>
<tr class="even">
<td align="left"><p>704</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>DbProviderDacError</p></td>
<td align="left"><p>Si è verificato un errore durante la distribuzione dell'applicazione a livello dati.</p></td>
<td align="left"><p>MBAM impacchetta i suoi database come applicazioni a livello dati e prova a registrarli usando Microsoft. SqlServer. DAC. DacServices. Il messaggio di errore nel contesto viene segnalato dal servizio DAC. L'evento deve contenere informazioni dettagliate sulle cause. Leggere le informazioni contenute nel messaggio di errore per risolvere i problemi e risolvere il problema.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>705</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>DbProviderDacWarning</p></td>
<td align="left"><p>Si è verificato un avviso durante la distribuzione dell'applicazione a livello dati.</p></td>
<td align="left"><p>MBAM impacchetta i suoi database come applicazione a livello dati e prova a registrarli usando Microsoft. SqlServer. DAC. DacServices. Il messaggio di avviso nel contesto viene segnalato dal servizio DAC. L'evento deve contenere informazioni dettagliate sulle cause. Leggere le informazioni contenute nel messaggio di avviso per risolvere i problemi e risolvere il problema.</p></td>
</tr>
<tr class="even">
<td align="left"><p>706</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/operativo</p></td>
<td align="left"><p>DbProviderDacInformation</p></td>
<td align="left"><p>È stato generato un messaggio durante la distribuzione dell'applicazione a livello dati.</p></td>
<td align="left"><p>Solo informativo; non è necessario alcun intervento di risoluzione dei problemi.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>800</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>ReportProviderUnexpectedError</p></td>
<td align="left"><p>Errore imprevisto del provider di report.</p></td>
<td align="left"><p>Errore imprevisto del provider di report. Descrizione {exceptionDetails} Questi sono alcuni dei dettagli di eccezione possibili:</p>
<p><strong>Si è verificato un errore durante l'ottenimento del nome della directory &#39; {DirectoryName} &#39;</strong></p>
<p><strong>Si è verificata un'eccezione durante l'ottenimento di file per la directory &#39; {DirectoryName} &#39;</strong></p>
<p><strong>Si è verificata un'eccezione durante l'enumerazione delle directory nella directory &#39; {DirectoryName} &#39;</strong></p>
<p><strong>Si è verificata un'eccezione durante la lettura di tutti i byte per il file &#39; {nomefile} &#39;</strong></p>
<p>Durante l'installazione di MBAM, la configurazione di MBAM decomprime tutti i file di report nel percorso di installazione specificato. Come parte dell'installazione di report, installa modulo Cerca di accedere ai file di report decompressi in percorso di installazione e comunica con SQL Reporting Services per pubblicare i file di report. Gli errori di cui sopra si verificano quando MBAM non riesce ad accedere ai file/cartelle in un percorso di installazione decompresso. Ecco alcuni suggerimenti per risolvere il problema:</p>
<ul>
<li><p>Verificare che MBAM sia installato.</p></li>
<li><p>Verificare che RegKey HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\InstallationPath sia presente e accessibile all'utente in esecuzione.</p></li>
<li><p>Verificare che il percorso dei file di report in MBAM InstallationPath non superi i caratteri di 248.</p></li>
<li><p>Verificare che la cartella di installazione di MBAM o i file contenuti nel percorso di installazione di MBAM non siano stati modificati dopo l'installazione.</p></li>
<li><p>Verificare che l'utente che ha eseguito la configurazione sia autorizzato a leggere da/a scrivere nella cartella di installazione di MBAM.</p></li>
</ul>
<p><strong>Connettività di Reporting Services non riuscita. {exceptionDetails}</strong></p>
<p>Durante l'installazione di MBAM Reports, Modules cerca di comunicare con i servizi Web di SSRS per creare cartelle e pubblicare report. Il messaggio precedente indica che MBAM non è riuscito a trovare o comunicare con i servizi Web SSRS. Ecco alcuni suggerimenti per risolvere il problema:</p>
<ul>
<li><p>Verificare che SSRS sia installato nel computer specificato.</p></li>
<li><p>Uso della console SSRS verificare che SSRS sia abilitato ed in uso.</p></li>
<li><p>Verificare che l'utente che ha eseguito la configurazione sia autorizzato ad accedere a SSRS.</p></li>
</ul>
<p><strong>Non è possibile rimuovere i report di MBAM usando l'URL dell'istanza di Reporting Services &#39; {SSRSInstanceUrl} &#39;. Verificare che l'istanza di SSRS necessaria per i report MBAM sia in uso e configurata correttamente.</strong></p>
<p>Quando l'installazione di MBAM non riesce o quando gli utenti disabilitano le funzionalità di segnalazione di MBAM, il modulo di configurazione rimuove i report SSRS. Il messaggio precedente indica che MBAM non è riuscito a rimuovere i report SSRS. Ecco alcuni suggerimenti per risolvere il problema:</p>
<ul>
<li><p>Verificare che SSRS sia installato nel computer specificato.</p></li>
<li><p>Uso della console SSRS verificare che SSRS sia abilitato ed in uso.</p></li>
<li><p>Verificare che l'utente che ha eseguito la configurazione sia autorizzato ad accedere a SSRS.</p></li>
</ul>
<p><strong>Si è verificato un errore durante la pubblicazione di report. {exceptionDetails}.</strong></p>
<p>Durante l'installazione di MBAM Reports, Modules cerca di comunicare con i servizi Web di SSRS per creare cartelle e pubblicare report. Il messaggio precedente indica che il servizio Web SSRS è stato segnalato ed eccezione durante la pubblicazione di report. Ecco alcuni suggerimenti per risolvere il problema:</p>
<ul>
<li><p>Uso della console SSRS verificare che SSRS sia abilitato ed in uso.</p></li>
<li><p>Verificare che l'utente che ha eseguito la configurazione sia autorizzato ad accedere/pubblicare report in SSRS.</p></li>
</ul>
<p><strong>Un criterio per il gruppo nome utente &#39; {nomeutente} &#39; esiste già. Se non è corretto, modificare manualmente il servizio di Reporting per i criteri duplicati o non validi.</strong></p>
<p>Dopo la pubblicazione di report MBAM, MBAM Setup cerca di creare un report MBAM utenti Roles (se non esiste già) e imposta i criteri utente corrispondenti. L'errore precedente indica che il servizio Web SSRS ha generato un'eccezione durante la configurazione dei criteri di ruolo degli utenti del report. Seguire le istruzioni nel messaggio dell'evento e fare riferimento a &quot; <a href="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;ProdVer=8.00&amp;EvtID=rsInvalidPolicyDefinition&amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;LCID=1033&amp;quot" data-raw-source="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;amp;ProdVer=8.00&amp;amp;EvtID=rsInvalidPolicyDefinition&amp;amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;amp;LCID=1033&amp;quot"> https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp ; ProdVer = 8.00 &amp; EvtID = rsInvalidPolicyDefinition &amp; EvtSrc = Microsoft. ReportingServices. Diagnostics. ErrorStrings. resources. Strings &amp; LCID = 1033&quot </a> ; per altre informazioni.</p>
<p><strong>Si è verificato un errore durante la convalida dell'accesso a SSRS {exceptionDetails}.</strong></p>
<p>Come parte del controllo dei prerequisiti, MBAM setup verifica se l'utente ha le autorizzazioni necessarie per accedere/creare una cartella in SSRS. Il messaggio di errore indica che si è verificata un'eccezione durante la verifica dell'accesso a SSRS. Vedere i dettagli dell'eccezione per i suggerimenti per il debug.</p>
<p><strong>Si è verificato un errore SOAP durante il controllo dell'URL SSRS. {exceptionDetails}</strong></p>
<p><strong>Si è verificato un errore Web durante il controllo dell'URL SSRS. {exceptionDetails}</strong></p>
<p><strong>Si è verificato un errore HTTP/HTTPS durante il controllo dell'URL SSRS. {exceptionDetails}</strong></p>
<p><strong>Si è verificato un errore durante il controllo dell'URL SSRS. {exceptionDetails}</strong></p>
<p>Come parte del controllo dei prerequisiti, la configurazione di MBAM recupera gli URL associati all'istanza SSRS fornita e prova a comunicare con il servizio Web SSRS. Il messaggio di errore precedente indica che il servizio Web SSRS nell'URL assegnato ha generato un'eccezione, fare riferimento a Dettagli eccezione per altre informazioni. Questi sono alcuni suggerimenti per risolvere i problemi di comunicazione SSRS.</p>
<ul>
<li><p>Verificare che SSRS sia installato nel computer specificato.</p></li>
<li><p>Uso della console SSRS verificare che SSRS sia abilitato ed in uso.</p></li>
<li><p>Verificare che l'utente che ha eseguito la configurazione sia autorizzato ad accedere a SSRS.</p></li>
</ul>
<p><strong>Si è verificato un errore durante il recupero della versione SSRS. {exceptionDetails}</strong></p>
<p>Come parte del controllo dei prerequisiti, MBAM Setup esegue una query in WMI per recuperare il numero di versione associato all'istanza di SSRS fornita. Il messaggio di errore precedente indica che si è verificata un'eccezione durante l'esecuzione di query su WMI. Per altre informazioni, vedere exceptionDetails. Ecco alcuni controlli che è possibile eseguire:</p>
<ul>
<li><p>Verificare che SSRS con il nome dell'istanza specificato sia installato nel computer specificato.</p></li>
<li><p>Uso della console SSRS verificare che SSRS sia abilitato ed in uso.</p></li>
<li><p>Verificare che l'utente che esegue la configurazione sia autorizzato a eseguire query sulla classe SSRS in spazio dei nomi WMI.</p></li>
</ul>
<p><strong>L'utente corrente non è autorizzato ad accedere allo spazio dei nomi WMI &#39; {ssrsWMINamespace} &#39;.</strong></p>
<p><strong>Si è verificato un errore durante l'enumerazione dello spazio dei nomi &#39; {ssrsWMINamespace} &#39;. Il server RPC per il provider WMI SSRS nell'host locale non viene trovato.</strong></p>
<p><strong>Si è verificato un errore durante l'enumerazione dello spazio dei nomi &#39; {ssrsNamespace} &#39;. Non è possibile trovare un'istanza di SSRS nell'host locale.</strong></p>
<p><strong>Si è verificato un errore durante l'accesso a WMI. Il server RPC ad esempio &#39; {ssrsInstance} &#39; non è stato trovato.</strong></p>
<p><strong>Si è verificato un errore durante l'accesso a WMI. Il nome dell'istanza &#39; {ssrsInstanceName} &#39; non è corretto.</strong></p>
<p><strong>Si è verificato un errore durante l'accesso a WMI. Non è possibile trovare l'istanza &#39; {ssrsInstanceName} &#39; nell'host locale.</strong></p>
<p>Come parte del controllo dei prerequisiti, MBAM Setup esegue una query in WMI per recuperare lo spazio dei nomi WMI associato all'istanza specificata. Il messaggio di errore precedente indica che si è verificato l'eccezione durante l'esecuzione di query su WMI. Per altre informazioni, vedere exceptionDetails. Ecco alcuni controlli che è possibile eseguire:</p>
<ul>
<li><p>Verificare che SSRS con il nome dell'istanza specificato sia installato nel computer specificato.</p></li>
<li><p>Uso della console SSRS verificare che SSRS sia abilitato ed in uso.</p></li>
<li><p>Verificare che l'utente che esegue la configurazione sia autorizzato ad accedere alla classe SSRS o query in uno spazio dei nomi WMI.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>801</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>ReportProviderError</p></td>
<td align="left"><p>Errore imprevisto del provider di report.</p></td>
<td align="left"><p>In base al nome dell'istanza di SQL Server Reporting Services, MBAM prova a trovare lo spazio dei nomi WMI corrispondente all'istanza di Reporting e a connettersi. Questo errore si verifica se MBAM incontra un'eccezione quando MBAM Cerca o tenta di connettersi allo spazio dei nomi WMI di SSRS. Leggere le informazioni contenute nei messaggi di errore registrati nel canale di configurazione di MBAM prima di questo messaggio per ottenere altri dettagli. Ecco alcuni aspetti che puoi verificare:</p>
<ul>
<li><p>Verificare che SSRS con il nome dell'istanza specificato sia attivo e in uso</p></li>
<li><p>Verificare che l'account utente che esegue l'installazione di MBAM disponga delle autorizzazioni necessarie per eseguire query/connettersi allo spazio dei nomi WMI di SSRS</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>802</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>ReportProviderWarning</p></td>
<td align="left"><p>Avviso del provider di report.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>803</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/operativo</p></td>
<td align="left"><p>ReportProviderInformation</p></td>
<td align="left"><p>Informazioni sul provider di report.</p></td>
<td align="left"><p>Solo informativo; non è necessario alcun intervento di risoluzione dei problemi.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>900</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>CMProviderUnexpectedError</p></td>
<td align="left"><p>Errore previsto del provider CM.</p></td>
<td align="left"><p>Indica che si è verificato un errore di terminazione durante la enabling\disabling o la configurazione della funzionalità di integrazione di Configuration Manager (CM) in MBAM. Gli errori noti includono:</p>
<ul>
<li><p>Errore di connessione al server del sito CM tramite il provider SMS</p></li>
<li><p>Errore di lettura dal registro di sistema</p></li>
<li><p>Errore di creare o eliminare una cartella nel file System</p></li>
<li><p>Errore di individuazione dell'installazione della console di Configuration Manager nel computer locale</p></li>
<li><p>Errore nel recupero di informazioni per l'istanza di SSRS configurata come punto di ruolo SRS in CM</p></li>
</ul>
<p>Il messaggio dell'evento conterrà ulteriori informazioni sull'errore specifico. Verificare che tutti i controlli prerequisito del software MBAM passino. Verificare che il percorso del registro di sistema MBAM, se esistente, HKEY_LOCAL_MACHINE server \SOFTWARE\Microsoft\MBAM e tutte le sottochiavi siano leggibili. Verificare che MBAM sia integrato con una versione supportata di Configuration Manager. Verificare che la console di Configuration Manager sia installata nel computer in cui viene richiamata la configurazione di MBAM e che la console possa essere usata per la connessione al server del sito target CM. Verificare che un'istanza di SSRS valida sia configurata come punto di ruolo SRS in CM e che l'utente che sta usando la configurazione di MBAM disponga delle autorizzazioni di Read\Write per l'istanza di SSRS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>901</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/admin</p></td>
<td align="left"><p>CMProviderError</p></td>
<td align="left"><p>Errore previsto del provider CM.</p></td>
<td align="left"><p>Indica che si è verificato un errore di terminazione durante la enabling\disabling o la configurazione della funzionalità di integrazione di Configuration Manager (CM) in MBAM. Gli errori noti includono:</p>
<ul>
<li><p>errore di connessione al server del sito CM tramite il provider SMS</p></li>
<li><p>errore di lettura dal registro di sistema</p></li>
<li><p>errore di creare o eliminare una cartella nel file System</p></li>
<li><p>errore di individuazione dell'installazione della console di Configuration Manager nel computer locale</p></li>
<li><p>cartella ConfigMgr mancante in SSRS come cartella radice per i report del punto di ruolo SRS</p></li>
<li><p>origine dati condivisa ConfigMgr mancante in SSRS</p></li>
<li><p>errore di distribuzione dei report SSRS nell'istanza di SSRS configurata come punto di ruolo SRS in CM</p></li>
<li><p>errore di creazione di elementi di configurazione e previsioni in CM</p></li>
</ul>
<p>Il messaggio dell'evento conterrà ulteriori informazioni sull'errore specifico. Verificare che tutti i controlli prerequisito del software MBAM passino. Verificare che il percorso del registro di sistema MBAM, se esistente, HKEY_LOCAL_MACHINE server \SOFTWARE\Microsoft\MBAM e tutte le sottochiavi siano leggibili. Verificare che MBAM sia integrato con una versione supportata di Configuration Manager. Verificare che la console di Configuration Manager sia installata nel computer in cui viene richiamata la configurazione di MBAM e che la console possa essere usata per la connessione al server del sito target CM. Verificare che l'utente disponga delle autorizzazioni di Read\Write necessarie per creare elementi di configurazione, previsioni e raccolte in CM. Verificare che un'istanza di SSRS valida sia configurata come punto di ruolo SRS in CM e che l'utente che sta usando la configurazione di MBAM disponga delle autorizzazioni di Read\Write per l'istanza di SSRS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>902</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>CMProviderWarning</p></td>
<td align="left"><p>Avviso del provider CM.</p></td>
<td align="left"><p>Indica che si è verificato un errore non fatale durante l'abilitazione della funzionalità di integrazione di Configuration Manager (CM). Gli errori noti includono: non è necessario eseguire il commit delle regole di raccolta nella raccolta di computer supportati MBAM in CM e in altri errori di SSRS e correlati alla rete.</p>
<p>Il messaggio dell'evento conterrà ulteriori informazioni sull'errore specifico. Alcune operazioni che hanno causato l'avviso vengono ritirate dopo l'avviso. Se dopo diversi tentativi l'errore persiste, MBAM potrebbe terminare con un errore effettivo. Controlla altri messaggi di evento nel log per diagnosticare ulteriormente la configurazione di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>903</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-server/operativo</p></td>
<td align="left"><p>CMProviderInformation</p></td>
<td align="left"><p>Informazioni sul provider di CM.</p></td>
<td align="left"><p>Solo informativo; non è necessario alcun intervento di risoluzione dei problemi.</p></td>
</tr>
</tbody>
</table>

 

## Operazione


La tabella seguente contiene i messaggi e le informazioni sulla risoluzione dei problemi per gli ID evento che possono verificarsi durante l'esecuzione di MBAM.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ID evento</th>
<th align="left">Source</th>
<th align="left">Simbolo dell'evento</th>
<th align="left">Messaggio</th>
<th align="left">Risoluzione dei problemi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>1</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>WebAppSpnError</p></td>
<td align="left"><p>Applicazione: {nomesito} {VirtualDirectory} mancano i seguenti nomi di entità servizio (SPN): {ListOfSpns} registrare gli SPN obbligatori nell'account: {ExecutionAccount}.</p></td>
<td align="left"><p>Per l'autenticazione integrata di Windows per avere esito positivo, occorre che i nomi SPN necessari siano a posto. Questo messaggio indica che l'SPN richiesto per l'applicazione MBAM non è stato configurato correttamente. I dettagli contenuti in questo evento devono contenere ulteriori informazioni.</p>
<p>Vedere "nome dell'entità servizio (SPN)" nei <a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams)"> prerequisiti di MBAM 2,5 Server per le topologie di integrazione di gestione autonoma e configurazione </a> per altre informazioni.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Operational</p></td>
<td align="left"><p>PerformanceCounterError</p></td>
<td align="left"><p>Si è verificato un errore durante il recupero di un contatore delle prestazioni.</p>
<p>Messaggio: {EventMessage} Category: {CategoryOfPerformanceCounter} contatore delle prestazioni: {NameOfPerformanceCounter} instance: {nome dell'istanza di categoria del contatore delle prestazioni} eccezione: {ExceptionThrown}</p>
<p>Il messaggio di traccia conterrà il messaggio di eccezione effettivo, alcuni dei quali sono descritti di seguito:</p>
<p><strong>ArgumentNullException </strong> : questa eccezione viene generata se la categoria, il contatore o l'istanza del contatore delle prestazioni richiesto non è valido.</p>
<p><strong>System. InvalidOperationException </strong> : CategoryName è una stringa vuota ( &quot; &quot; ).-o-counterName è una stringa vuota ( &quot; &quot; ).</p>
<p>-oppure-l'impostazione di autorizzazione di lettura/scrittura richiesta non è valida per questo contatore.</p>
<p>-oppure-la categoria specificata non esiste (se readOnly è true).</p>
<p>-oppure-la categoria specificata non è una categoria personalizzata di .NET Framework (se readOnly è false).</p>
<p>-oppure-la categoria specificata è contrassegnata come a più istanze e richiede il contatore delle prestazioni da creare con un nome di istanza.</p>
<p>-oppure-instanceName è maggiore di 127 caratteri.</p>
<p>-oppure-CategoryName e counterName sono stati localizzati in lingue diverse.</p>
<p><strong>System. ComponentModel. Win32exception </strong> : si è verificato un errore durante l'accesso a un'API di sistema.</p>
<p><strong>System. PlatformNotSupportedException </strong> : la piattaforma è windows 98 o Windows Millennium Edition (me), che non supporta i contatori delle prestazioni.</p>
<p><strong>System. UnauthorizedAccessException </strong> : il codice in esecuzione senza privilegi amministrativi ha tentato di leggere un contatore delle prestazioni.</p></td>
<td align="left"><p>Il messaggio contenuto nell'evento fornirà altri dettagli intorno all'eccezione generata. Se è stata generata un'eccezione System. UnauthorizedAccessException, verificare che l'account di esecuzione di MBAM (pool di app) abbia accesso alle API del contatore delle prestazioni.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>100</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>AdminServiceRecoveryDbError</p></td>
<td align="left"><p><strong>GetMachineUsers </strong> : si è verificato un errore durante l'ottenimento delle informazioni utente dal database. Messaggio: {messaggio}-oppure-</p>
<p><strong>GetRecoveryKey </strong> : si è verificato un errore durante l'ottenimento della chiave di ripristino dal database. Messaggio: {messaggio}-oppure-</p>
<p><strong>GetRecoveryKey </strong> : si è verificato un errore durante l'ottenimento delle informazioni utente dal database. Messaggio: {messaggio}-oppure-</p>
<p><strong>GetRecoveryKeyIds </strong> : si è verificato un errore durante l'ottenimento degli ID chiave di ripristino dal database. Messaggio: {messaggio}-oppure-</p>
<p><strong>GetTpmHashForUser </strong> : si è verificato un errore durante l'ottenimento dei dati hash TPM dal database di ripristino. Messaggio: {messaggio}-oppure-</p>
<p><strong>GetTpmHashForUser </strong> : si è verificato un errore durante l'ottenimento dei dati hash TPM dal database di ripristino. Messaggio: {messaggio}-oppure-</p>
<p><strong>QueryDriveRecoveryData </strong> : si è verificato un errore durante l'ottenimento dei dati di ripristino dell'unità dal database. Messaggio: {messaggio}-oppure-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : si è verificato un errore durante l'ottenimento degli ID chiave di ripristino dal database. Messaggio: {messaggio}-oppure-</p>
<p><strong>QueryVolumeUsers </strong> : si è verificato un errore durante l'ottenimento delle informazioni utente dal database.</p></td>
<td align="left"><p>Questo messaggio viene registrato ogni volta che si verifica un'eccezione durante la comunicazione con il database di ripristino di MBAM. Leggere le informazioni contenute nella traccia per ottenere dettagli specifici sull'eccezione.</p>
<p>Per istruzioni dettagliate sulla risoluzione dei problemi, vedere l'articolo <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> su come risolvere i problemi di connessione al motore di database di SQL Server </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>101</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>AdminServiceComplianceDbError</p></td>
<td align="left"><p><strong>GetRecoveryKey </strong> : si è verificato un errore durante la registrazione di un evento di controllo nel database di conformità. Messaggio: {messaggio}-oppure-</p>
<p><strong>GetRecoveryKeyIds </strong> : si è verificato un errore durante la registrazione di un evento di controllo nel database di conformità. Messaggio: {messaggio}-oppure-</p>
<p><strong>GetTpmHashForUser </strong> : si è verificato un errore durante la registrazione di un evento di controllo nel database di conformità. Messaggio: {messaggio}-oppure-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : si è verificato un errore durante la registrazione di un evento di controllo nel database di conformità. Messaggio: {messaggio}-oppure-</p>
<p><strong>QueryDriveRecoveryData </strong> : si è verificato un errore durante la registrazione di un evento di controllo nel database di conformità. Messaggio: {messaggio}</p></td>
<td align="left"><p>Questo messaggio viene registrato ogni volta che si verifica un'eccezione durante la comunicazione del database di conformità di MBAM. Leggere le informazioni contenute nella traccia per ottenere dettagli specifici sull'eccezione.</p>
<p>Per istruzioni dettagliate sulla risoluzione dei problemi, vedere l'articolo <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> su come risolvere i problemi di connessione al motore di database di SQL Server </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>102</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>AgentServiceRecoveryDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Questo messaggio indica un'eccezione quando il servizio di MBAM Agent prova a comunicare con il database di ripristino. Leggere il messaggio contenuto nell'evento per ottenere informazioni specifiche sull'eccezione.</p>
<p>Vedere l'articolo <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> di TechNet come risolvere i problemi di connessione al motore di database di SQL Server </a> per verificare se l'account del pool mbam app ha le autorizzazioni necessarie per la connessione o l'esecuzione sul database di ripristino di mbam.</p></td>
</tr>
<tr class="even">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>AgentServiceError</p></td>
<td align="left"><p>Non è possibile rilevare l'account utente del computer client o la migrazione dei dati. -oppure-</p>
<p>La verifica dell'account non è riuscita per identità chiamante.</p></td>
<td align="left"><p>Ogni volta che viene effettuata una chiamata &quot; ai &quot; &quot; metodi Web PostKeyRecoveryInfo, IsRecoveryKeyResetRequired &quot; , &quot; CommitRecoveryKeyRest &quot; o &quot; GetTpmHash &quot; nei servizi di agente di mbam, viene recuperato il contesto del chiamante per ottenere le credenziali del chiamante. Se il contesto del chiamante è null o è vuoto, i log dei servizi di MBAM Agent &quot; non riescono a rilevare l'account del computer client o la migrazione dei dati.&quot;</p>
<p>La verifica dell'account del messaggio non &quot; riuscita per l'identità del chiamante &quot; viene registrata se il metodo Web si aspetta che il chiamante sia un account di computer e il chiamante non è un account del computer oppure se il metodo Web fa eccezione per il chiamante come account utente e il chiamante non è un account utente o un membro dell'account del gruppo di migrazione dei dati.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>StatusServiceComplianceDbConfigError</p></td>
<td align="left"><p>&quot;La stringa di connessione al database di conformità nel registro di sistema è vuota.&quot;</p></td>
<td align="left"><p>Questo messaggio viene registrato ogni volta che la stringa di connessione DB di conformità non è valida.</p>
<p>Verificare il valore nella chiave del registro di sistema HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString</p></td>
</tr>
<tr class="even">
<td align="left"><p>105</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>StatusServiceComplianceDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Questo messaggio di errore indica che i siti Web/servizi Internet di MBAM non erano in grado di connettersi al database di MBAMCompliance.</p>
<p>Vedere l'articolo <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> di TechNet come risolvere i problemi di connessione al motore di database di SQL Server </a> per verificare che l'account del pool di app IIS possa connettersi al database di mbam Compliance.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>106</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>HelpdeskError</p></td>
<td align="left"><p>La richiesta di URL {URL} ha causato un errore interno. -oppure-</p>
<p>Si è verificato un errore durante l'ottenimento delle informazioni sul contesto di esecuzione. Non è possibile verificare la registrazione del nome dell'entità servizio (SPN). -oppure-</p>
<p>Si è verificato un errore durante la verifica della registrazione del nome dell'entità servizio (SPN).</p></td>
<td align="left"><p>Indica che è stata generata un'eccezione non gestita nell'applicazione Helpdesk. Esaminare le voci di log nel canale operativo di MBAM admin per trovare l'eccezione specifica. o</p>
<p>Durante l'operazione di caricamento del sito Web iniziale dell'helpdesk viene eseguito un controllo SPN. Per verificare l'SPN, il supporto tecnico richiede le informazioni sull'account di esecuzione, IIS SiteName e ApplicationVirtualPath corrispondente al sito Web dell'helpdesk. Questo messaggio di errore viene registrato quando uno o più di questi messaggi non sono validi o mancanti. o</p>
<p>Questo messaggio indica che viene generata un'eccezione di sicurezza durante l'esecuzione della verifica dell'SPN. Fare riferimento all'eccezione contenuta nella sezione Dettagli evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>107</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>SelfServicePortalError</p></td>
<td align="left"><p>Si è verificato un errore durante l'ottenimento della chiave di ripristino per un utente. EventDetails: {ExceptionMessage}-oppure-</p>
<p>Si è verificato un errore durante l'ottenimento delle informazioni sul contesto di esecuzione. Non è possibile verificare la registrazione del nome dell'entità servizio (SPN). EventDetails: utente: {nomeutente identità} applicazione: {SiteName\ApplicationVirtualPath}-oppure-</p>
<p>Si è verificato un errore durante la verifica della registrazione del nome dell'entità servizio (SPN). EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>Indica che è stata generata un'eccezione imprevista quando è stata eseguita una richiesta di recupero della chiave di ripristino. Fare riferimento al messaggio di eccezione contenuto nella sezione Dettagli evento. Se l'analisi è abilitata in MBAM helpdesk, vedere i dati di traccia per ottenere messaggi di eccezione dettagliati. o</p>
<p>Durante un'operazione di caricamento iniziale, il portale self-service (SSP) recupera le informazioni sull'account di esecuzione, IIS nomesito e ApplicationVirtualPath che corrispondono al sito Web self-service per verificare il nome SPN. Questo messaggio di errore viene registrato quando uno o più di questi non sono validi. o</p>
<p>Questo messaggio indica che è stata generata un'eccezione di sicurezza durante l'esecuzione della verifica dell'SPN. Fare riferimento all'eccezione contenuta nella sezione Dettagli evento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>108</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>DomainControllerError</p></td>
<td align="left"><p>Si è verificato un errore durante la risoluzione del nome di dominio {NomeDominio}, si è verificato un errore di allocazione della memoria. -oppure-</p>
<p>Impossibile richiamare il metodo DsGetDcName. EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>Per risolvere il nome di dominio, MBAM sfrutta l' &quot; &quot; API di Windows DsGetDcName. Questo messaggio viene registrato quando &quot; DsGetDcName &quot; restituisce &quot; ERROR_NOT_ENOUGH_MEMORY &quot; che indica un errore di allocazione della memoria. o</p>
<p>Questo messaggio indica che &quot; &quot; il metodo API DsGetDcName non è disponibile nel sistema di hosting.</p></td>
</tr>
<tr class="even">
<td align="left"><p>109</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>WebAppRecoveryDbError</p></td>
<td align="left"><p>Si è verificato un errore durante la lettura della configurazione del database di ripristino. La stringa di connessione al database di ripristino non è configurata. Messaggio: {messaggio}-oppure-</p>
<p><strong>DoesUserHaveMatchingRecoveryKey </strong> : si è verificato un errore durante l'ottenimento degli ID chiave di ripristino per un utente. Messaggio: {messaggio}-oppure-</p>
<p><strong>QueryDriveRecoveryData </strong> : si è verificato un errore durante l'ottenimento dei dati di ripristino dell'unità. Messaggio: {messaggio}-oppure-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : si è verificato un errore durante l'ottenimento degli ID chiave di ripristino per un utente. Messaggio: {messaggio}-oppure-</p>
<p>Si è verificato un errore durante l'ottenimento dell'hash della password del TPM dal database di ripristino. EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>Questo messaggio indica che le informazioni della stringa di connessione al database di ripristino in &quot; HKLM\Software\Microsoft\MBAM Server\Web\RecoveryDBConnectionString &quot; non sono valide. Verificare il valore della chiave del registro di sistema specificata. o</p>
<p>Se viene registrato uno dei messaggi rimanenti, vedere la sezione risoluzione dei problemi illustrata nell'articolo di TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> come risolvere i problemi di connessione al motore di database di SQL Server </a> per verificare se una connessione può essere eseguita nel database di ripristino di mbam dal server IIS usando le credenziali del pool di app.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>110</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>WebAppComplianceDbError</p></td>
<td align="left"><p>Si è verificato un errore durante la lettura della configurazione del database di conformità. La stringa di connessione al database di conformità non è configurata. -oppure-</p>
<p><strong>GetRecoveryKeyForCurrentUser </strong> : si è verificato un errore durante la registrazione di un evento di controllo nel database di conformità. Messaggio: {messaggio}-oppure-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : si è verificato un errore durante la registrazione di un evento di controllo nel database di conformità. Messaggio: {messaggio}-oppure-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : si è verificato un errore durante la registrazione di un evento di controllo nel database di conformità. Messaggio: {messaggio}</p></td>
<td align="left"><p>Questo messaggio indica che le informazioni sulla stringa di connessione DB di conformità in &quot; HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString &quot; non sono valide. Verificare il valore corrispondente alla chiave del registro di sistema sopra riportata. o</p>
<p>Se viene registrato uno dei messaggi rimanenti, vedere la procedura di risoluzione dei problemi illustrata nell'articolo di TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> come risolvere i problemi di connessione al motore di database di SQL Server </a> per verificare se una connessione può essere effettuata al database di mbam Compliance dal server IIS usando le credenziali del pool di app.</p></td>
</tr>
<tr class="even">
<td align="left"><p>111</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>WebAppDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Questi errori indicano una delle due condizioni seguenti</p>
<ul>
<li><p>I siti Web di MBAM/WebServices non sono stati in grado di connettersi al database di MBAMCompliance o MBAMRecovery</p></li>
<li><p>Siti Web MBAM/account di esecuzione WebServices (account del pool di app) non è stato possibile eseguire la stored procedure GetVersion in MBAMCompliance o MBAMRecovery database</p></li>
</ul>
<p>Il messaggio contenuto nell'evento fornirà ulteriori dettagli sull'eccezione.</p>
<p>Fare riferimento alle procedure per la risoluzione dei problemi elencate nell'articolo di TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> come risolvere i problemi di connessione al motore di database di SQL Server </a> per verificare che l'account di esecuzione di mbam (account del pool app) possa connettersi al database di mbam Compliance/Recovery e disponga delle autorizzazioni necessarie per eseguire la stored procedure GetVersion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>112</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/admin</p></td>
<td align="left"><p>WebAppError</p></td>
<td align="left"><p>Si è verificato un errore durante la verifica della registrazione del nome dell'entità servizio (SPN). EventDetails: {ExceptionMessage}</p></td>
<td align="left"><p>Per eseguire la verifica dell'SPN, MBAM esegue una query in Active Directory per recuperare un elenco di account di esecuzione mappati di SPN. MBAM interroga anche il &quot;ApplicationHost.config&quot; per ottenere i binding del sito Web di mbam. Questo messaggio di errore indica che MBAM non è riuscito a comunicare con Active Directory oppure che non è stato possibile caricare il file applicationHost.config.</p>
<p>Verificare che l'account di esecuzione (account del pool di app) disponga delle autorizzazioni per la query AD o il file ApplicationHost.config. Verificare inoltre le voci di binding del sito in ApplicationHost.config file.</p></td>
</tr>
<tr class="even">
<td align="left"><p>200</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Operational</p></td>
<td align="left"><p>HelpDeskInformation</p></td>
<td align="left"><p>L'applicazione del sito Web di amministrazione è stata trovata e connessa a una versione supportata del database di ripristino. -oppure-</p>
<p>L'applicazione del sito Web di amministrazione è stata trovata e connessa a una versione supportata del database di conformità.</p></td>
<td align="left"><p>Indica il successo della connessione al database di ripristino/conformità dal sito Web di MBAM helpdesk.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>201</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Operational</p></td>
<td align="left"><p>SelfServicePortalInformation</p></td>
<td align="left"><p>L'applicazione portale self-service è stata trovata e connessa a una versione supportata del database di ripristino. -oppure-</p>
<p>L'applicazione portale self-service è stata trovata e connessa a una versione supportata del database di conformità.</p></td>
<td align="left"><p>Indica il successo della connessione al database di ripristino/conformità dal portale self-service di MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>202</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Web/Operational</p></td>
<td align="left"><p>WebAppInformation</p></td>
<td align="left"><p>L'applicazione ha i nomi SPN registrati correttamente.</p></td>
<td align="left"><p>Indica che i nomi SPN necessari per il sito Web dell'helpdesk di MBAM sono correttamente registrati in base all'account in esecuzione.</p></td>
</tr>
</tbody>
</table>

 


## Argomenti correlati


[Documentazione tecnica per MBAM 2.5](technical-reference-for-mbam-25.md)

[Registri eventi del client](client-event-logs.md)

 
## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





