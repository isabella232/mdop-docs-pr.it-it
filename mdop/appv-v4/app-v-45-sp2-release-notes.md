---
title: Note sulla versione di App-V 4.5 SP2
description: Note sulla versione di App-V 4.5 SP2
author: dansimp
ms.assetid: 1b3a8a83-4523-4634-9f75-29bc22ca5815
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 35cff3b2a2c110a4d8beba883a4cf9332381ea60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819855"
---
# Note sulla versione di App-V 4.5 SP2


Per cercare queste note sulla versione, premere CTRL + F.

**Importante**  Leggere accuratamente queste note sulla versione prima di installare Microsoft Application Virtualization Management System. Queste note sulla versione contengono informazioni necessarie per installare correttamente il sistema di gestione della virtualizzazione dell'applicazione. Queste note sulla versione contengono informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una discrepanza tra queste note sulla versione e la documentazione del sistema di gestione della virtualizzazione delle applicazioni, l'ultima modifica deve essere considerata autorevole.

 

Per informazioni aggiornate sui problemi noti, visitare la raccolta Microsoft TechNet nelle [Note sulla versione di App-V 4,5 SP2](https://go.microsoft.com/fwlink/?LinkId=184640) ( https://go.microsoft.com/fwlink/?LinkId=184640) .

## Informazioni su Microsoft Application Virtualization 4,5 Service Pack 2


Queste note sulla versione sono state aggiornate per riflettere le modifiche introdotte con Microsoft Application Virtualization (App-V) 4.5 Service Pack2 (SP2). Questo Service Pack contiene le modifiche seguenti:

-   Supporto per Office 2010: App-V 4.5 SP2 ora supporta la virtualizzazione di Microsoft Office 2010. Per indicazioni prescrittivi per la sequenziazione di Microsoft Office 2010 con App-V 4,5 SP2, vedere [istruzioni per la sequenziazione di office 2010 in Microsoft App-V 4,6](https://go.microsoft.com/fwlink/?LinkId=191539) ( https://go.microsoft.com/fwlink/?LinkId=191539) .

-   Supporto per il mirroring del database: App-V 4.5 SP2 ora supporta il mirroring del database di Microsoft SQL Server. Per altre informazioni sulla configurazione del mirroring del database nell'ambiente App-V, vedere [come configurare il supporto per il mirroring di Microsoft SQL Server per App-v](https://go.microsoft.com/fwlink/?LinkId=190880) ( https://go.microsoft.com/fwlink/?LinkId=190880) .

-   Feedback dei clienti e aggiornamento rapido cumulativo: App-V 4.5 SP2 include anche un rollup di correzioni per risolvere i problemi trovati dopo il rilascio di App-V 4.5 SP1. Gli aggiornamenti affrontano una combinazione di problemi noti e feedback dei clienti da team, partner e clienti interni Microsoft che usano App-V 4.5. Per un elenco completo degli aggiornamenti, vedere l'articolo 980847 della Microsoft Knowledge base (KB) alla [Descrizione di Microsoft Application Virtualization 4,5 Service Pack 2](https://go.microsoft.com/fwlink/?LinkId=191540) ( https://go.microsoft.com/fwlink/?LinkId=191540) .

## Informazioni sulla documentazione del prodotto


La documentazione completa per Application Virtualization (App-V) è disponibile su Microsoft TechNet nella [raccolta di Application Virtualization TechCenter](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) . La documentazione di TechNet include la guida online per l'Application Virtualization Sequencer, i client di virtualizzazione delle applicazioni e il server di virtualizzazione dell'applicazione. Include anche la guida alla pianificazione e distribuzione di Application Virtualization e la Guida alle operazioni di virtualizzazione dell'applicazione.

## Protezione da vulnerabilità e virus della sicurezza


Per proteggere le vulnerabilità e i virus della sicurezza, è consigliabile installare gli ultimi aggiornamenti della sicurezza disponibili per qualsiasi nuovo software da installare. Per altre informazioni, vedere [Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Inviare commenti e suggerimenti


È possibile inviare commenti e suggerimenti o segnalare un problema con il sistema di gestione di Microsoft Application Virtualization (App-V) tramite il forum della community nel [Forum della documentazione App-v](https://go.microsoft.com/fwlink/?LinkId=122917) di Application Virtualization TechCenter ( https://go.microsoft.com/fwlink/?LinkId=122917) .

È anche possibile inviare il feedback della documentazione direttamente al team di documentazione di App-V <appvdocs@microsoft.com> .

## Problemi noti di Application Virtualization 4.5 SP2


Questa sezione fornisce le informazioni più aggiornate sui problemi relativi a Microsoft Application Virtualization (App-V) 4.5 SP2. Questi problemi non vengono visualizzati nella documentazione del prodotto e in alcuni casi potrebbe essere contraddetta la documentazione del prodotto esistente. Quando possibile, questi problemi verranno risolti in versioni successive del software.

### Linee guida per l'installazione di Server Management Console

Se è necessario installare il software di gestione su sistemi diversi dal server di pubblicazione e streaming di Application Virtualization principale, l'installazione del server supporta l'installazione di Application Virtualization Management Console e Application Virtualization Management Web Service su server distinti dal server di gestione di App-V principale. Per distribuire i componenti di gestione in più server, la delega Kerberos deve essere abilitata nel server in cui è installato il servizio Web Application Virtualization. Per informazioni su come abilitare questo supporto, vedere [come configurare il server in modo che sia attendibile per la delega](https://go.microsoft.com/fwlink/?LinkId=166682) ( https://go.microsoft.com/fwlink/?LinkId=166682) .

### Linee guida per l'installazione o l'aggiornamento dei client a App-V 4.5 SP2 tramite Setup.msi

Quando si installano o si aggiornano i client App-V in App-V 4,5 SP2 usando Setup.msi, i prerequisiti non vengono installati automaticamente.

WORKAROUNDYou deve installare manualmente i prerequisiti prima di installare o aggiornare i client App-V in App-V 4.5 SP2. Per le procedure dettagliate su come installare i prerequisiti e il client App-V, vedere [come installare il client tramite la riga di comando](https://go.microsoft.com/fwlink/?LinkId=144106) ( https://go.microsoft.com/fwlink/?LinkId=144106) .

Al termine, installare i client App-V 4,5 SP2 usando Setup.msi con credenziali amministrative. Questo file è disponibile nel supporto per la versione di App-V 4,5 SP2 nella cartella Installers\\Client.

Durante l'installazione della segnalazione degli errori delle applicazioni Microsoft, usare il comando seguente se si sta installando o eseguendo l'aggiornamento al client Desktop App-V 4,5 SP2:

**msiexec/i dw20shared.msi APPGUID = {C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D} ALLUSERS = 1 reboot = Elimina reinstallazione = tutti REINSTALLMODE = vomus**

In alternativa, se si sta eseguendo l'installazione o l'aggiornamento al client App-V 4,5 SP2 per Servizi Desktop remoto (in precedenza Servizi terminal), usare il comando seguente:

**msiexec/i dw20shared.msi APPGUID = {ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5} ALLUSERS = 1 reboot = Elimina reinstallazione = tutti REINSTALLMODE = vomus**

**Nota**  
-   Il parametro APPGUID fa riferimento al codice prodotto dei client App-V che si installano o si aggiornano. Il codice prodotto è univoco per ogni Setup.msi. È possibile usare l'editor di database Orca o uno strumento simile per esaminare i file di Windows Installer e determinare il codice prodotto. Questo passaggio è necessario per tutte le installazioni o gli aggiornamenti per App-V 4,5 SP2.

-   Questo passaggio non è necessario se si esegue l'aggiornamento e in precedenza è stato installato Dw20shared.msi.

 

### Migliorare le prestazioni durante la sequenziazione di .NET Framework

Durante la sequenziazione di Microsoft .NET Framework, è possibile che si verifichino prestazioni di sistema ridotte perché il servizio NGEN di .NET Framework tenta di precompilare gli assembly come attività in background.

WORKAROUNDWhen sequenziazione di .NET Framework, disattiva il servizio NGEN .NET Framework (Mscorsvw.exe) dopo aver completato la fase di monitoraggio. Devi usare la scheda **Servizi virtuali** nell'App-V Sequencer e cambiare il tipo di avvio in **disabled**.

### Quando si disinstalla il client Microsoft Application Virtualization, le impostazioni utente associate all'utente che esegue la disinstallazione vengono eliminate

Quando si disinstalla il client App-V, Windows Installer rimuove le impostazioni di virtualizzazione delle applicazioni dal profilo dell'utente corrente. Se il computer usa profili mobili, non usare l'account di rete personale per disinstallare il client perché rimuoverà le impostazioni per le applicazioni virtuali in tutti i computer.

WORKAROUNDYou deve disinstallare il client App-V con un account amministrativo che non viene usato per l'uso di applicazioni virtuali.

### Le modifiche apportate nel file system virtuale e nelle schede del registro di sistema virtuale devono essere salvate durante l'esecuzione della sequenziazione guidata

Se si apre un pacchetto per eseguire un aggiornamento o se è già stata eseguita la sequenziazione guidata con un nuovo pacchetto e si apportano modifiche al pacchetto nelle schede Virtual File System o Virtual Registry, le modifiche non vengono salvate automaticamente.

WORKAROUNDSave le modifiche prima di eseguire nuovamente la procedura guidata, per verificare che vengano riflesse nell'ambiente virtuale della procedura guidata.

### Il sequencer della riga di comando deve essere eseguito da un prompt dei comandi con privilegi elevati

Quando si usa il sequencer della riga di comando, non viene richiesto l'elevazione.

WORKAROUNDRun il sequencer della riga di comando usando un prompt dei comandi con privilegi elevati.

### I nomi di variabile del percorso breve nei file OSD possono causare errori

Se si riceve un errore 450478-1F702339-0000010B "il nome della directory non è valido" quando si avvia un'applicazione virtuale nel client, è possibile che la variabile nell'OSD sia impostata in modo non corretto. Questo problema può verificarsi se il programma di installazione dell'applicazione imposta un nome di percorso breve durante la sequenziazione.

WORKAROUNDRemove la tilde finale da qualsiasi variabile CSIDL esistente nel file OSD.

### <a href="" id="correct-syntax-for-decodepath-parameter-for-command-line-sequencer-"></a>Sintassi corretta per il parametro DECODEPATH per il sequencer della riga di comando

Nel sequencer della riga di comando, quando si apre un pacchetto per l'aggiornamento e lo decodifica nella radice dell'unità Q, la sintassi per il parametro *DECODEPATH* non dovrebbe includere una barra finale.

WORKAROUNDYou può usare **Q:** invece di **Q:\\** (omettendo il carattere finale "\ \").

### <a href="" id="when-upgrading-app-v-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a>Quando i pacchetti di upgradingAPP-V 4,2 si verificano problemi causati dai file di Windows Installer nel file system virtuale

Quando si aggiorna un pacchetto da APP-V 4.2, è possibile che si verifichino problemi relativi a una mancata corrispondenza dei file di sistema di Windows Installer inclusi per impostazione predefinita in APP-V 4.2 e nelle librerie di Windows Installer installate localmente nella workstation di sequenziazione. I file seguenti si trovano in CSIDL \ _SYSTEM \ \:

Cabinet.dll

Msi.dll

Msiexec.exe

Msihnd.dll

Msimsg.dlll

WORKAROUNDDelete tutti i file precedenti dal pacchetto. Eliminare i mapping nella scheda **VFS** e i file effettivi nella cartella CSIDL \ _SYSTEM nel percorso di decodifica.

### <a href="" id="on-windows-xp--by-default--client-installation-logging-is-not-enabled-"></a>In WindowsXP, per impostazione predefinita, la registrazione dell'installazione client non è abilitata

Durante l'installazione del client, per verificare che gli eventuali errori di installazione vengano acquisiti per la risoluzione dei problemi, è necessario abilitare la registrazione usando la riga di comando.

WORKAROUNDAdd il parametro */l\ * VX! log.txt* alla riga di comando, come illustrato nell'esempio seguente:

**setup.exe/s/v "/qn/l\ * VX! log.txt "**

**msiexec.exe/i setup.msi/Qn/l\ * VX! log.txt**

In alternativa, è possibile impostare la chiave del registro di sistema sul valore seguente:

**\ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies\\Microsoft\\Windows\\Installer\] "Logging" = "voicewarmupx!"**

### Per il funzionamento dell'autenticazione Kerberos, i nomi principali di servizio (SPN) devono essere registrati per IIS

Quando si usa Internet Information Services (IIS) 6.0 orIIS 7.0 per l'icona o il recupero dei file OSD e lo streaming di pacchetti, per abilitare l'autenticazione Kerberos, i nomi SPN devono essere registrati nel modo seguente:

-   Nel server IIS eseguire i comandi seguenti usando lo strumento SETSPN.EXE Resource Kit. Deve essere usato il nome di dominio completo del server (FQDN).

    **&lt;Nome di dominio completo di SoftGrid&gt;**

    **Nome di dominio completo di Setspn-r HTTP/ &lt; Server&gt;**

Per altre informazioni, Vedi [autenticazione integrata di Windows (IIS 6,0)](https://go.microsoft.com/fwlink/?LinkId=131407) ( https://go.microsoft.com/fwlink/?LinkId=131407) .

### Modifiche alla compatibilità di .NET

Microsoft Application Virtualization (App-V) cumulativo Update1 o versioni successive supporta la sequenziazione di .NET Framework in WindowsXP SP2 o versioni successive. Le routine di sequenziazione per le applicazioni .NET scritte per SoftGrid 4.2 potrebbero essere aggiornate quando vengono usate con il sequencer App-V 4,5. Per informazioni dettagliate e soluzioni alternative, vedere l'articolo su Application Virtualization TechCenter di [supporto per .NET in Microsoft Application virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=123412) ( https://go.microsoft.com/fwlink/?LinkId=123412) .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Dopo l'aggiornamento del client da App-V 4.2, alcune applicazioni non vengono visualizzate

Verificare l'errore seguente nel log: "il client di virtualizzazione dell'applicazione non ha potuto analizzare il file OSD". Il client App-V 4,5 filtra le applicazioni con un file OSD che contiene un tag OS vuoto ( &lt; OS &gt; &lt; /OS &gt; ).

WORKAROUNDDelete il tag OS vuoto dal file OSD.

### Il server App-V richiede esenzioni nel firewall per determinati processi

Per il server per la trasmissione corretta delle applicazioni, i processi principali del server, incluso il dispatcher, richiedono l'accesso tramite il firewall.

WORKAROUNDSet esenzioni nel firewall del server per i processi seguenti: Sghwsvr.exe e Sghwdsptr.exe. Questo vale per l'App-V Management Server e per l'App-V Streaming Server.

### Quando il programma di installazione del server viene eseguito in modalità invisibile all'utente, non controlla correttamente la MSXML6

Il server di gestione di App-V dipende da MSXML6. Tuttavia, se si esegue il programma di installazione in modalità silenziosa, ad esempio tramite il comando **msiexec-i setup.msi/Qn** in un sistema in cui MSXML6 non è già installato, il programma di installazione non rileva la dipendenza mancante e si installa comunque. Di conseguenza, quando i client tentano di aggiornare le informazioni di pubblicazione da App-V Management Server, riceveranno errori.

WORKAROUNDVerify che MSXML6 sia installato nel sistema prima di provare un'installazione invisibile al server di gestione di App-V.

### Codice di errore 000C800 quando si tenta di connettersi alla console di gestione di Application Virtualization

Un amministratore di Application Virtualization che non è un amministratore locale nel server del servizio Web di gestione App-V riceve un errore (codice di errore: 000C800) durante il tentativo di connessione alla console di gestione di App-V e la voce Sftmmc. log indica che l'accesso a SftMgmt. UDL viene negato. Per connettersi correttamente alla console di gestione di App-V, un amministratore che non dispone dei diritti di amministratore locale per l'App-V Management Web Service Server deve avere almeno le autorizzazioni di lettura ed esecuzione per il file SftMgmt. udl.

Gli amministratori della virtualizzazione delle applicazioni devono avere le autorizzazioni di lettura ed esecuzione per il file SftMgmt. UDL nella cartella%systemdrive%\\Program \\Programmi\\microsoft System Center App Virt Management Server\\App Virt Management Service.

### I parametri della riga di comando del programma di installazione client vengono ignorati quando vengono usati in combinazione con KEEPCURRENTSETTINGS = 1

Se usato in combinazione con KEEPCURRENTSETTINGS = 1, i parametri della riga di comando del programma di installazione client seguenti vengono ignorati: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA e REQUIRESECURECONNECTION.

WORKAROUNDIf si desidera mantenere le impostazioni, usare KEEPCURRENTSETTINGS = 1 e quindi impostare gli altri parametri dopo la distribuzione. Il modello ADM App-V può essere usato per impostare le impostazioni client seguenti: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES e ALLOWINDEPENDENTFILESTREAMING. È possibile scaricare il modello ADM dall'area DownLoad Microsoft in [Microsoft Application Virtualization Administrative Template (modello ADM)](https://go.microsoft.com/fwlink/?LinkId=121835) ( https://go.microsoft.com/fwlink/?LinkId=121835) .

### Informazioni sul copyright delle note sulla versione

Questo documento viene fornito "così com'è". Le informazioni e le opinioni espresse nel presente documento, inclusi gli URL e altri riferimenti a siti Web Internet, sono soggette a modifiche senza preavviso. Si rischia di usarlo.

Alcuni esempi descritti in questo documento sono forniti solo per le illustrazioni e sono fittizi.Nessuna associazione o connessione reale è destinata o deve essere dedotta.

Il presente documento non implica la concessione di alcun diritto di proprietà intellettuale in relazione ai prodotti Microsoft. È possibile copiare e usare questo documento per fini di riferimento interno. È possibile modificare questo documento per gli scopi interni e di riferimento.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer e Windows Vista sono marchi di fabbrica del gruppo Microsoft di società.

Tutti gli altri marchi sono proprietà dei rispettivi proprietari.

 

 





