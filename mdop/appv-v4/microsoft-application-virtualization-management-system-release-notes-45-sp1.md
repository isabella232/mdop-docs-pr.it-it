---
title: Note sulla versione di Microsoft Application Virtualization Management System 4,5 SP1
description: Note sulla versione di Microsoft Application Virtualization Management System 4,5 SP1
author: dansimp
ms.assetid: 5d6b11ea-7b87-4084-9a7c-0d831f247aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c24d2e98ad09460ca22e4b29d75ae2b9c72d0bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816156"
---
# Note sulla versione di Microsoft Application Virtualization Management System 4,5 SP1


Per cercare queste note sulla versione, premere CTRL + F.

**Importante**  Leggere accuratamente queste note sulla versione prima di installare il sistema di gestione della virtualizzazione dell'applicazione. Queste note sulla versione contengono informazioni necessarie per installare correttamente il sistema di gestione della virtualizzazione dell'applicazione. Queste note sulla versione contengono informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una discrepanza tra queste note sulla versione e la documentazione del sistema di gestione della virtualizzazione delle applicazioni, l'ultima modifica deve essere considerata autorevole.

 

Per informazioni aggiornate sui problemi noti, visitare la raccolta Microsoft TechNet <https://go.microsoft.com/fwlink/?LinkId=122918> .

## Informazioni su Microsoft Application Virtualization 4,5 Service Pack 1


Queste note sulla versione sono state aggiornate per riflettere le modifiche introdotte con Microsoft Application Virtualization (App-V) 4.5 Service Pack1 (SP1). Questo Service Pack contiene le modifiche seguenti:

-   Supporto per Windows 7 e Windows Server 2008 R2: App-V 4,5 SP1 offre il supporto per Windows 7 e Windows Server 2008 R2, incluso il supporto per le funzionalità di Windows 7, ad esempio la barra delle applicazioni, AppLocker, BranchCache e BitLocker da usare.Il supporto di Windows Server 2008 R2 è solo per l'Application Virtualization Server. Per altre informazioni sul supporto di AppLocker in Windows 7, vedere <https://go.microsoft.com/fwlink/?LinkID=156732> .

-   Supporto per i regni Kerberos di terze parti: App-V 4,5 SP1 offre il supporto per gli ambienti che hanno una relazione di trust e gli account utente mappati tra un dominio Windows e un ambito Kerberos MIT, che è uno scenario comune in molte università. Per informazioni su come abilitare questo supporto, visitare la raccolta Microsoft TechNet <https://go.microsoft.com/fwlink/?LinkId=166004> .

-   Supporto migliorato per la pubblicazione e lo streaming delle applicazioni tramite HTTP/HTTPS: App-V 4,5 SP1 offre il supporto per la pubblicazione e lo streaming delle applicazioni tramite i protocolli HTTP/HTTPS per Windows XP Home Edition, Windows Vista Home Basic e Windows 7 Home Basic.

-   Feedback dei clienti e rollup hotfix: App-V 4.5 SP1 include anche un rollup di correzioni per risolvere i problemi riscontrati in seguito alla versione di Microsoft Application Virtualization (App-V) 4.5 CU1 release. Gli aggiornamenti sono il risultato di una combinazione di problemi noti e feedback dei clienti dei team, partner e clienti interni che usano App-V 4.5. Per un elenco completo degli aggiornamenti, vedere l'articolo della Knowledge <https://go.microsoft.com/fwlink/?LinkId=167121> .

## Informazioni sulla documentazione del prodotto


La documentazione completa per Application Virtualization (App-V) è disponibile su Microsoft TechNet nell'Application Virtualization (App-V) TechCenter at <https://go.microsoft.com/fwlink/?LinkId=122939> . La documentazione di TechNet include la guida online per Application Virtualization Sequencer, Application Virtualization Client e Application Virtualization Server. Include anche la guida alla pianificazione e distribuzione di Application Virtualization e la Guida alle operazioni di virtualizzazione dell'applicazione.

## Protezione da vulnerabilità e virus della sicurezza


Per proteggere le vulnerabilità e i virus della sicurezza, è consigliabile installare gli ultimi aggiornamenti della sicurezza disponibili per qualsiasi nuovo software da installare. Per altre informazioni, vedere il sito Web Microsoft Security at <https://go.microsoft.com/fwlink/?LinkId=3482> .

## Invio di commenti e suggerimenti


È possibile inviare commenti e suggerimenti o segnalare un problema con il sistema di gestione di Microsoft Application Virtualization (App-V) tramite un forum della community su Microsoft Application Virtualization TechCenter ( <https://go.microsoft.com/fwlink/?LinkId=122917> ).

È anche possibile inviare commenti e suggerimenti sulla documentazione direttamente al team di documentazione di App-V. Inviare il feedback della documentazione a appvdocs@microsoft.com.

## Problemi noti di Application Virtualization 4.5 SP1


Questa sezione fornisce le informazioni più aggiornate sui problemi relativi a Microsoft Application Virtualization (App-V) 4.5 SP1. Questi problemi non vengono visualizzati nella documentazione del prodotto e in alcuni casi potrebbe essere contraddetta la documentazione del prodotto esistente. Quando possibile, questi problemi verranno risolti in versioni successive del software.

### Linee guida per l'installazione di Server Management Console

Se è necessario installare il software di gestione su sistemi diversi da quelli della pubblicazione e del server di flusso di virtualizzazione delle applicazioni primarie, l'installazione del server supporta l'installazione della console di gestione e del servizio Web di gestione in server distinti dal server di gestione di App-V principale. Per distribuire i componenti di gestione in più server, la delega Kerberos deve essere abilitata nel server in cui è installato il servizio Web. Per informazioni su come abilitare questo supporto, visitare la raccolta Microsoft TechNet all'indirizzo <https://go.microsoft.com/fwlink/?LinkId=166682>

### Linee guida per l'installazione o l'aggiornamento dei client a App-V 4.5 SP1 con setup.msi

Quando si installano o si aggiornano i client App-V in App-V 4,5 SP1 usando setup.msi, i prerequisiti non vengono installati automaticamente.

WORKAROUNDYou deve installare manualmente i prerequisiti prima di installare o aggiornare l'App-V client toApp-V 4,5 SP1. Per le procedure dettagliate per l'installazione dei prerequisiti e del client App-V, vedere <https://go.microsoft.com/fwlink/?LinkId=144106> .

Al termine, installare il client App-V 4,5 SP1 usando setup.msi con privilegi elevati. Questo file è disponibile nel supporto per la versione di App-V 4,5 SP1 nella cartella Installers\\Client.

Durante l'installazione della segnalazione degli errori delle applicazioni Microsoft, usare il comando seguente se si sta installando o eseguendo l'aggiornamento al client Desktop App-V 4,5 SP1:

    msiexec /i dw20shared.msi APPGUID={93468B43-C19D-44F9-8BCC-114076DB0443}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

In alternativa, se si sta eseguendo l'installazione o l'aggiornamento al client App-V 4,5 SP1 per Servizi Desktop remoto (in precedenza Servizi terminal), usare il comando seguente:

    msiexec /i dw20shared.msi APPGUID={0042AD3C-99A4-4E58-B5F0-744D5AD96E1C} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

**Nota**  Il parametro APPGUID fa riferimento al codice prodotto del client App-V installato o aggiornato. Il codice prodotto è univoco per ogni setup.msi. È possibile usare l'editor di database Orca o uno strumento simile per esaminare i file di Windows Installer e determinare il codice prodotto. Questo passaggio è necessario per tutte le installazioni o gli aggiornamenti per App-V 4,5 SP1.

 

### Migliorare le prestazioni durante la sequenziazione di .NET Framework

Quando si sequenziano .NET Framework, è possibile che si verifichino prestazioni di sistema ridotte perché il servizio NGEN di Microsoft .NET Framework tenta di precompilare gli assembly come attività in background.

WORKAROUNDWhen sequenziazione di .NET Framework, disabilitare il servizio NGEN di Microsoft .NET Framework (mscorsvw.exe) dopo aver completato la fase di monitoraggio. Devi usare la scheda **Servizi virtuali** nel sequencer e cambiare il tipo di avvio in disabled.

### Quando si disinstalla il client Microsoft Application Virtualization, le impostazioni utente associate all'utente che esegue la disinstallazione verranno eliminate

Quando disinstalli il client App-V, Windows Installer rimuoverà le impostazioni di virtualizzazione delle applicazioni dal profilo dell'utente corrente. Se il computer usa profili mobili, non usare l'account di rete personale per disinstallare il client perché rimuoverà le impostazioni per le applicazioni virtuali in tutti i computer.

WORKAROUNDYou deve eseguire la disinstallazione del client App-V con un account amministrativo che non viene usato per l'esecuzione di applicazioni virtuali.

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

### <a href="" id="when-upgrading-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a>Quando si aggiornano 4.2 pacchetti, si verificano problemi causati dai file di Windows Installer nel file system virtuale

Quando si aggiorna un pacchetto da 4.2, è possibile che si verifichino problemi relativi a una mancata corrispondenza dei file di sistema di Windows Installer inclusi per impostazione predefinita in 4.2 e nelle librerie di Windows Installer installate localmente nella workstation di sequenziazione. I file seguenti si trovano in CSIDL \ _SYSTEM \ \:

cabinet.dll

msi.dll

msiexec.exe

msihnd.dll

msimsg.dlll

WORKAROUNDDelete tutti i file precedenti dal pacchetto. Eliminare i mapping nella scheda **VFS** e i file effettivi nella cartella CSIDL \ _SYSTEM nel percorso di decodifica.

### <a href="" id="on-windows-xp--client-install-logging-is-not-enabled-by-default-"></a>In WindowsXP, la registrazione di installazione client non è abilitata per impostazione predefinita

Durante l'installazione del client, per verificare che gli eventuali errori di installazione vengano acquisiti per scopi di risoluzione dei problemi, è necessario abilitare la registrazione usando la riga di comando.

WORKAROUNDAdd il parametro */l\ * VX! log.txt* alla riga di comando, come illustrato nell'esempio seguente:

setup.exe/s/v "/qn/l\ * VX! log.txt "

msiexec.exe/i setup.msi/Qn/l\ * VX! log.txt

In alternativa, è possibile impostare la chiave del registro di sistema sul valore seguente:

\ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies\\Microsoft\\Windows\\Installer\] "Logging" = "voicewarmupx!"

### Per il funzionamento dell'autenticazione Kerberos, i nomi principali di servizio (SPN) devono essere registrati per IIS

Quando si usa IIS 6.0 o 7.0 per il recupero di file di icone o OSD e lo streaming di pacchetti, per consentire l'autenticazione Kerberos, è necessario che i nomi SPN vengano registrati nel modo seguente:

-   Nel server IIS eseguire i comandi seguenti usando lo strumento SETSPN.EXE Resource Kit. Deve essere usato il nome di dominio completo del server (FQDN).

    &lt;Nome di dominio completo di SoftGrid&gt;

    Nome di dominio completo di Setspn-r HTTP/ &lt; Server&gt;

Per altre informazioni, vedi <https://go.microsoft.com/fwlink/?LinkId=131407>.

### Modifiche alla compatibilità di .NET

Microsoft Application Virtualization (App-V) cumulativo Update1 o versioni successive supporta la sequenziazione di .NET Framework in WindowsXP (SP2 o versioni successive). Potrebbe essere necessario aggiornare le routine di sequenziazione per le applicazioni .NET scritte per SoftGrid 4.2 quando vengono usate con l'App-V 4,5 Sequencer. Per informazioni dettagliate e soluzioni alternative, vedere l'articolo della Knowledge base <https://go.microsoft.com/fwlink/?LinkId=123412> .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Dopo l'aggiornamento del client da App-V 4.2, alcune applicazioni non vengono visualizzate

Verificare l'errore seguente nel log: "il client di virtualizzazione dell'applicazione non ha potuto analizzare il file OSD". Il client App-V 4,5 filtra le applicazioni che contengono un file OSD contenente un tag OS vuoto ( &lt; OS &gt; &lt; /OS &gt; ).

WORKAROUNDDelete il tag OS vuoto dal file OSD.

### Il server App-V richiede esenzioni nel firewall per determinati processi

Per il server per la trasmissione corretta delle applicazioni, i processi principali del server, incluso il dispatcher, devono accedere tramite il firewall.

WORKAROUNDSet esenzioni nel firewall del server per i processi seguenti: sghwsvr.exe e sghwdsptr.exe. Questo vale per l'App-V Management Server e per l'App-V Streaming Server.

### Quando il programma di installazione del server viene eseguito in modalità invisibile all'utente, non controlla correttamente la MSXML6

Il server di gestione di App-V dipende da MSXML6. Tuttavia, se si esegue il programma di installazione in modalità silenziosa, ad esempio usando il comando "msiexec-i setup.msi/qn" in un sistema in cui MSXML6 non è già installato, il programma di installazione non rileva la dipendenza mancante e si installa comunque. Di conseguenza, quando i client tentano di aggiornare le informazioni di pubblicazione dal server di gestione di App-V, vedranno gli errori.

WORKAROUNDVerify che MSXML6 sia installato nel sistema prima di provare un'installazione silenziosa di App-V Management Server.

### Codice di errore 000C800 quando si tenta di connettersi alla console di gestione di Application Virtualization

Un amministratore di Application Virtualization che non è un amministratore locale di App-V Management Web Service Server riceverà un errore (codice di errore: 000C800) durante il tentativo di connessione alla console di gestione di App-V e la voce Sftmmc. log indicherà che l'accesso a SftMgmt. UDL viene negato. Per connettersi correttamente alla console di gestione di App-V, un amministratore che non dispone dei diritti di amministratore locale per l'App-V Management Web Service Server deve avere almeno le autorizzazioni di lettura ed esecuzione per il file SftMgmt. udl.

Agli amministratori della virtualizzazione delle applicazioni deve essere assegnata l'autorizzazione di lettura ed esecuzione per il file SftMgmt. UDL in%systemdrive%\\Program \\Programmi\\microsoft System Center App Virt Management Server\\App Virt Management Service.

### I parametri della riga di comando del programma di installazione client vengono ignorati quando vengono usati in combinazione con KEEPCURRENTSETTINGS = 1

Se usato in combinazione con KEEPCURRENTSETTINGS = 1, i parametri della riga di comando del programma di installazione client seguenti vengono ignorati: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA e REQUIRESECURECONNECTION.

WORKAROUNDIf si desidera mantenere le impostazioni, usare KEEPCURRENTSETTINGS = 1 e quindi impostare gli altri parametri dopo la distribuzione. Il modello ADM App-V può essere usato per impostare le impostazioni client seguenti: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES e ALLOWINDEPENDENTFILESTREAMING. È possibile trovare il modello ADM <https://go.microsoft.com/fwlink/?LinkId=121835> .

## Informazioni sul copyright delle note sulla versione


Le informazioni contenute in questo documento, incluso l'URL e altri riferimenti a siti Web Internet, sono soggette a modifiche senza preavviso e vengono fornite solo a scopo informativo. L'intero rischio dell'uso o dei risultati dell'uso di questo documento rimane con l'utente e Microsoft Corporation non rilascia alcuna garanzia, espressa o implicita. Se non diversamente specificato, le società, le organizzazioni, i prodotti, i nomi di dominio, gli indirizzi di posta elettronica, i loghi, le persone, i luoghi e gli eventi descritti in questi esempi sono fittizi. Nessuna associazione con una società, un'organizzazione, un prodotto, un nome di dominio, un indirizzo di posta elettronica, un logo, una persona, un luogo o un evento reali è destinato o dovrebbe essere dedotto. Rispettare tutte le leggi sul copyright applicabili è responsabilità dell'utente. Senza limitare i diritti in diritto d'autore, nessuna parte di questo documento può essere riprodotta, archiviata o introdotta in un sistema di recupero o trasmessa in qualsiasi forma o con qualsiasi mezzo (elettronica, meccanica, fotocopie, registrazione o altro) o per qualsiasi scopo, senza l'espressa autorizzazione scritta di Microsoft Corporation.

Microsoft può avere brevetti, applicazioni di brevetto, marchi, copyright o altri diritti di proprietà intellettuale che coprono argomenti in questo documento. Fatta eccezione per quanto espressamente specificato in un contratto di licenza scritta da Microsoft, l'arredamento di questo documento non offre alcuna licenza per questi brevetti, marchi, copyright o altre proprietà intellettuali.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer e Windows Vista sono marchi di fabbrica del gruppo Microsoft di società.

Tutti gli altri marchi sono proprietà dei rispettivi proprietari.

 

 





