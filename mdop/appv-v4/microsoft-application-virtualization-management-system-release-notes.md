---
title: Note sulla versione di Microsoft Application Virtualization Management System
description: Note sulla versione di Microsoft Application Virtualization Management System
author: dansimp
ms.assetid: e1a4d5ee-53c7-4b48-814c-a34ce0e698dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c34abab9a49bd69f760a9b531d0950cc581253c1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816165"
---
# Note sulla versione di Microsoft Application Virtualization Management System


Per cercare queste note sulla versione, premere CTRL + F.

**Importante**  Leggere accuratamente queste note sulla versione prima di installare il sistema di gestione della virtualizzazione dell'applicazione. Queste note sulla versione contengono informazioni necessarie per installare correttamente il sistema di gestione della virtualizzazione dell'applicazione. Questo documento contiene informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una discrepanza tra queste note sulla versione e la documentazione del sistema di gestione della virtualizzazione delle applicazioni, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

 

Per informazioni aggiornate sui problemi noti, visitare la raccolta Microsoft TechNet <https://go.microsoft.com/fwlink/?LinkId=122918> .

## Informazioni sull'aggiornamento cumulativo 1 di Microsoft Application Virtualization 4,5


Queste note sulla versione sono state aggiornate per riflettere le modifiche introdotte con Microsoft Application Virtualization 4.5 Update1 cumulativo (App-V 4.5 CU1), che fornisce gli aggiornamenti più recenti di Application Virtualization (App-V) 4.5. Questo aggiornamento cumulativo contiene le modifiche seguenti:

-   Supporto per Windows7 beta e Windows Server2008R2 beta: App-V 4.5 CU1 risolve i problemi di compatibilità con Windows7 beta e Windows Server2008R2 beta. Verrà fornito supporto per il blocco dei problemi che impediscono l'uso di App-V 4.5 CU1 in un ambiente di test nelle versioni precedenti alla versione RTM di Windows7. Ciò consentirà di verificare che le applicazioni virtuali possano essere eseguite correttamente in un ambiente di test in cui è necessaria la compatibilità tra client App-V 4.5 e versione beta di Windows7.

    **Importante**  L'esecuzione di App-V 4.5 CU1 in qualsiasi versione di Windows7 o Windows Server2008R2 in un ambiente operativo live non è supportata.

     

-   Supporto migliorato per la sequenziazione di .NET Framework: App-V 4.5 CU1 risolve i problemi precedenti relativi alla sequenziazione di .NET Framework 3.5 e versioni precedenti in WindowsXP (SP2 o versioni successive). Per altre informazioni sulle nuove funzionalità, vedere l'articolo su TechNet <https://go.microsoft.com/fwlink/?LinkId=123412> .

-   Feedback dei clienti e aggiornamento rapido cumulativo: App-V 4.5 CU1 include anche un rollup di correzioni per risolvere i problemi riscontrati in seguito alla versione RTM di App-V 4.5. Questo include una combinazione di problemi noti e feedback dei clienti dei team, partner e clienti interni che usano App-V 4.5. Per un elenco completo degli aggiornamenti inclusi, vedere l'articolo della Knowledge <https://go.microsoft.com/fwlink/?LinkId=141258> .

## Informazioni sulla documentazione del prodotto


La documentazione completa per Application Virtualization (App-V) è disponibile su Microsoft TechNet nell'Application Virtualization (App-V) TechCenter at <https://go.microsoft.com/fwlink/?LinkId=122939> . La documentazione di TechNet include la guida online per Application Virtualization Sequencer, Application Virtualization Client e Application Virtualization Server. Include anche la guida alla pianificazione e distribuzione di Application Virtualization e la Guida alle operazioni di virtualizzazione dell'applicazione.

## Protezione da vulnerabilità e virus della sicurezza


Per proteggere le vulnerabilità e i virus della sicurezza, è importante installare gli ultimi aggiornamenti della sicurezza disponibili per qualsiasi nuovo software da installare. Per altre informazioni, vedere il sito Web Microsoft Security at <https://go.microsoft.com/fwlink/?LinkId=3482> .

## Invio di commenti e suggerimenti


È possibile inviare commenti e suggerimenti o segnalare un problema con il sistema di gestione di Microsoft Application Virtualization (App-V) tramite un forum della community su Microsoft Application Virtualization TechCenter ( <https://go.microsoft.com/fwlink/?LinkId=122917> ).

È anche possibile inviare commenti e suggerimenti sulla documentazione direttamente al team di documentazione di App-V. Inviare il feedback della documentazione a appvdocs@microsoft.com.

## Problemi noti di Application Virtualization 4.5 CU1


Questa sezione fornisce le informazioni più aggiornate sui problemi relativi a Microsoft Application Virtualization (App-V) 4.5 CU1. Questi problemi non vengono visualizzati nella documentazione del prodotto e in alcuni casi potrebbe essere contraddetta la documentazione del prodotto esistente. Quando possibile, questi problemi verranno risolti in versioni successive.

### Linee guida per l'installazione o l'aggiornamento dei client a App-V 4.5 CU1 con setup.msi

Quando si installano o si aggiornano i client App-V in App-V 4.5 CU1 usando setup.msi, i prerequisiti non vengono installati automaticamente.

WORKAROUNDYou deve installare manualmente i prerequisiti prima di installare o aggiornare il client App-V a 4.5 CU1. Per le procedure dettagliate per l'installazione dei prerequisiti e del client App-V, vedere <https://go.microsoft.com/fwlink/?LinkId=144106> .

Al termine, installare il client App-V 4.5 CU1 usando setup.msi con privilegi elevati. Questo file è disponibile nell'App-V 4.5 CU1 Release media nella cartella Installers\\Client.

Durante l'installazione della segnalazione degli errori delle applicazioni Microsoft, usare il comando seguente se si sta installando o eseguendo l'aggiornamento al client Desktop App-V 4.5 CU1:

    msiexec /i dw20shared.msi APPGUID={FE495DBC-6D42-4698-B61F-86E655E0796D}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

In alternativa, se si sta eseguendo l'installazione o l'aggiornamento al client di Servizi terminal App-V 4,5 CU1, usare il comando seguente:

    msiexec /i dw20shared.msi APPGUID={8A97C241-D92A-47DC-B360-E716C1AAA929} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

**Nota**  Il parametro APPGUID fa riferimento al codice prodotto del client App-V di cui si esegue l'installazione o l'aggiornamento. Il codice prodotto è univoco per ogni setup.msi. Puoi usare l'editor di database Orca o uno strumento simile per esaminare i file di Windows Installer e determinare il codice del prodotto. Questo passaggio è necessario per tutte le installazioni o gli aggiornamenti a App-V 4.5 CU1.

 

### <a href="" id="some-applications-might-fail-to-install-during-the-monitoring-phase-when-sequencing-on-windows-7-beta--"></a>Alcune applicazioni potrebbero non riuscire a installare durante la fase di monitoraggio durante la sequenziazione in versione beta di Windows7

Durante la sequenziazione in versione beta di Windows7 o in un computer con Windows Installer 5.0, è possibile che alcune applicazioni non vengano installate durante la fase di monitoraggio.

WORKAROUNDYou deve concedere manualmente le autorizzazioni di controllo completo del gruppo Everyone alla chiave del registro di sistema seguente:

    HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\SystemGuard

**Importante**  È necessario usare il pulsante **Avanzate** per impostare l'opzione "Includi autorizzazioni ereditabili dall'elemento padre dell'oggetto".

 

### Non è possibile salvare i pacchetti durante la sequenziazione in versione beta di Windows7

Durante la sequenziazione in versione beta di Windows7, potrebbe non essere possibile salvare il pacchetto sequenziato a causa di una violazione della condivisione.

SOLUZIONI alternative specificate nella sezione procedure consigliate della Guida alla sequenziazione di Microsoft Application Virtualization 4.5 (vedere <https://go.microsoft.com/fwlink/?LinkId=144108> ) è necessario arrestare e disabilitare i programmi software seguenti prima di iniziare la sequenziazione:

-   Windows Defender

-   Software antivirus

-   Software di deframmentazione del disco

-   Windows Search

-   Qualsiasi sessione di Esplora risorse di Windows aperta

Inoltre, se si usa Microsoft Update in esecuzione nella stazione di sequenziazione per acquisire gli aggiornamenti durante il processo di aggiornamento del pacchetto, prima di iniziare la sequenziazione sarà necessario aggiungere "C:\\Windows\\SoftwareDistribution" come VFS Esclusion.

### Migliorare le prestazioni durante la sequenziazione di .NET Framework

Quando si sequenziano .NET Framework, è possibile che si verifichino prestazioni di sistema ridotte perché il servizio NGEN di Microsoft .NET Framework tenta di precompilare gli assembly come attività in background.

WORKAROUNDWhen sequenziazione di .NET Framework, disabilitare il servizio NGEN di Microsoft .NET Framework (mscorsvw.exe) dopo aver completato la fase di monitoraggio. Devi usare la scheda **Servizi virtuali** nel sequencer e cambiare il tipo di avvio in disabled.

### Problemi di interoperabilità con la barra delle applicazioni Windows7

Quando si esegue l'Application Virtualization Client in Windows7, la barra delle applicazioni di Windows7 non comprime più istanze di un'applicazione virtuale in un singolo pulsante della barra delle applicazioni. Inoltre, gli elenchi Jump non vengono visualizzati quando si fa clic con il pulsante destro del mouse su una barra delle applicazioni virtuale, a meno che l'applicazione non sia stata bloccata alla barra delle applicazioni di Windows7.

### Quando si disinstalla il client Microsoft Application Virtualization, le impostazioni utente associate all'utente che esegue la disinstallazione verranno eliminate

Quando si disinstalla Microsoft Application Virtualization Client, Windows Installer rimuove le impostazioni di virtualizzazione delle applicazioni dal profilo dell'utente corrente. Se il computer usa profili mobili, non usare l'account di rete personale per disinstallare il client perché rimuoverà le impostazioni per le applicazioni virtuali in tutti i computer.

WORKAROUNDYou deve eseguire la disinstallazione del client App-V con un account amministrativo che non viene usato per l'esecuzione di applicazioni virtuali.

### Le modifiche apportate nel file system virtuale e nelle schede del registro di sistema virtuale devono essere salvate durante l'esecuzione della sequenziazione guidata

Se si apre un pacchetto per eseguire un aggiornamento o se è già stata eseguita la sequenziazione guidata con un nuovo pacchetto e si apportano modifiche al pacchetto nelle schede Virtual File System o Virtual Registry, le modifiche non vengono salvate automaticamente.

WORKAROUNDSave le modifiche prima di eseguire nuovamente la procedura guidata, per verificare che vengano riflesse nell'ambiente virtuale della procedura guidata.

### Il sequencer della riga di comando deve essere eseguito da un prompt dei comandi con privilegi elevati

Quando si usa il sequencer della riga di comando, non viene richiesto l'elevazione.

WORKAROUNDRun il sequencer della riga di comando usando un prompt dei comandi con privilegi elevati.

### Configurazione della console di gestione server in ambienti distribuiti

Se è necessario installare i componenti di gestione su sistemi diversi da quelli della pubblicazione e del server di flusso di virtualizzazione delle applicazioni primarie, l'installazione del server supporta l'installazione della console di gestione e del servizio Web su server distinti dal server di virtualizzazione dell'applicazione principale quando è configurato correttamente.

Per distribuire i componenti di gestione in più server, la delega Kerberos deve essere abilitata nel server in cui è installato il servizio Web.

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

### Durante l'aggiornamento da RC, le autorizzazioni predefinite per i registri client non consentono agli utenti non amministratori di accedere ai log per la risoluzione dei problemi e il supporto

Le autorizzazioni predefinite per i registri client per il client VirtualizationRC applicazione non consentono l'accesso non per l'amministratore ai file di log e le modifiche manuali alle autorizzazioni del log sono state ripristinate quando i client sono stati riavviati. Questa operazione è stata corretta nella versione RTM per le nuove installazioni del client, ma durante l'aggiornamento da RC le autorizzazioni personalizzate per i file di log esistenti non vengono reimpostate. Tuttavia, quando vengono creati nuovi log o dopo la reimpostazione del log, i file avranno le nuove autorizzazioni predefinite.

WORKAROUNDAfter l'aggiornamento, Reimposta i registri client esistenti o modifica manualmente le autorizzazioni.

### Modifiche alla compatibilità di .NET

Microsoft Application Virtualization Update1 cumulativo supporta la sequenziazione di .NET Framework in WindowsXP (SP2 o versioni successive). Potrebbe essere necessario aggiornare le routine di sequenziazione per le applicazioni .NET scritte per SoftGrid 4.2 quando vengono usate con l'App-V 4.5 Sequencer. Per informazioni dettagliate e soluzioni alternative, vedere l'articolo della Knowledge base <https://go.microsoft.com/fwlink/?LinkId=123412> .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Dopo l'aggiornamento del client da App-V 4.2, alcune applicazioni non vengono visualizzate

Verificare l'errore seguente nel log: "il client di virtualizzazione dell'applicazione non ha potuto analizzare il file OSD". Il client Microsoft Application Virtualization 4.5 filtra le applicazioni che includono un file OSD contenente un tag OS vuoto ( &lt; OS &gt; &lt; /OS &gt; ).

WORKAROUNDDelete il tag OS vuoto dal file OSD.

### Il server App-V richiede esenzioni nel firewall per determinati processi

Per il server per la trasmissione corretta delle applicazioni, i processi principali del server, incluso il dispatcher, devono accedere tramite il firewall.

WORKAROUNDSet esenzioni nel firewall del server per i processi seguenti: sghwsvr.exe e sghwdsptr.exe. Questo vale per l'App-V Management Server e per l'App-V Streaming Server.

### La sequenziazione di pacchetti che richiedono nuovi runtime di Visual Basic potrebbe non riuscire

Se si sequenzia un pacchetto che usa una versione più recente di un runtime di Visual Basic (VB) in un sistema in cui è installata una versione precedente di VBruntime, è possibile che venga visualizzato un arresto anomalo o un altro comportamento imprevisto quando si prova a usare il pacchetto. Ad esempio, se provi a sequenziare Microsoft Money2007, che usa la versione 6.00.9782 di VBruntime, in un sistema WindowsXP con la versione 6.00.9690 del VBruntime, potresti vedere un arresto anomalo in progettazione fattura quando provi a eseguire l'esecuzione in un altro sistema di WindowsXP con quel vecchio VBruntime.

WORKAROUNDAfter l'installazione dell'applicazione nel computer di sequenziazione, pur monitorando, copiare la VBruntime corretta (più recente) nella directory del pacchetto da cui è stato avviato l'eseguibile. Ciò consente all'applicazione sequenziata di trovare la versione prevista di VBruntime quando viene avviata.

**Importante**  Questo problema è stato risolto in Microsoft Application Virtualization 4.5 Update1 cumulativo.

 

### Quando il programma di installazione del server viene eseguito in modalità invisibile all'utente, non controlla correttamente la MSXML6

Il server di gestione di App-V dipende da MSXML6. Tuttavia, se Esegui il programma di installazione in modalità silenziosa, ad esempio usando il comando "msiexec-i setup.msi/qn" in un sistema in cui MSXML6 non è già installato, il programma di installazione non nota la dipendenza mancante e si installa comunque. Il risultato più comune è che quando i client tentano di aggiornare le informazioni di pubblicazione da App-V Management Server, vedranno gli errori.

WORKAROUNDVerify che MSXML6 sia installato nel sistema prima di provare un'installazione silenziosa di App-V Management Server.

### Codice di errore 000C800 quando si tenta di connettersi alla console di gestione di Application Virtualization

Un amministratore di Application Virtualization che non è un amministratore locale nel server del servizio di gestione della virtualizzazione dell'applicazione riceverà un errore (codice di errore: 000C800) durante il tentativo di connessione alla console di gestione della virtualizzazione dell'applicazione e la voce Sftmmc. log indicherà che l'accesso a SftMgmt. UDL viene negato. Per connettersi correttamente alla console di gestione di Application Virtualization, un amministratore di Application Virtualization che non è un amministratore locale nel server del servizio di gestione della virtualizzazione dell'applicazione deve avere almeno l'accesso in lettura ed esecuzione al file SftMgmt. udl.

Agli amministratori della virtualizzazione delle applicazioni deve essere assegnata l'autorizzazione di lettura ed esecuzione per il file SftMgmt. UDL in%systemdrive%\\Program \\Programmi\\microsoft System Center App Virt Management Server\\App Virt Management Service.

### I parametri della riga di comando del programma di installazione client vengono ignorati quando vengono usati in combinazione con KEEPCURRENTSETTINGS = 1

Se usato in combinazione con KEEPCURRENTSETTINGS = 1, i parametri della riga di comando del programma di installazione client seguenti vengono ignorati: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA e REQUIRESECURECONNECTION.

WORKAROUNDIf si desidera mantenere le impostazioni, usare KEEPCURRENTSETTINGS = 1 e quindi impostare gli altri parametri dopo la distribuzione. Il modello ADM App-V può essere usato per impostare le impostazioni client seguenti: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES e ALLOWINDEPENDENTFILESTREAMING. È possibile trovare il modello ADM <https://go.microsoft.com/fwlink/?LinkId=121835> .

### Errore durante l'inizializzazione delle applicazioni virtuali con Symantec Endpoint Protection

Quando si usa Symantec Endpoint Protection con l'applicazione e la caratteristica di controllo del dispositivo abilitata, le applicazioni virtuali potrebbero non riuscire a iniziare, con l'errore "l'applicazione non è stata inizializzata correttamente (0xc000007b)". Per informazioni dettagliate e soluzioni alternative, vedere l'articolo della Knowledge base <https://go.microsoft.com/fwlink/?LinkId=125851> .

**Importante**  Questo problema è stato risolto in Microsoft Application Virtualization 4.5 Update1 cumulativo.

 

## Informazioni sul copyright delle note sulla versione


Le informazioni contenute in questo documento, incluso l'URL e altri riferimenti a siti Web Internet, sono soggette a modifiche senza preavviso e vengono fornite solo a scopo informativo. L'intero rischio dell'uso o dei risultati dell'uso di questo documento rimane con l'utente e Microsoft Corporation non rilascia alcuna garanzia, espressa o implicita. Nell'esempio le aziende, le organizzazioni, i prodotti, gli utenti e gli eventi descritti in questo documento sono fittizi. Nessuna associazione con una società, un'organizzazione, un prodotto, una persona o un evento reale è intesa o deve essere dedotta. Rispettare tutte le leggi sul copyright applicabili è responsabilità dell'utente. Senza limitare i diritti in diritto d'autore, nessuna parte di questo documento può essere riprodotta, archiviata o introdotta in un sistema di recupero o trasmessa in qualsiasi forma o con qualsiasi mezzo (elettronica, meccanica, fotocopie, registrazione o altro) o per qualsiasi scopo, senza l'espressa autorizzazione scritta di Microsoft Corporation.

Microsoft può avere brevetti, applicazioni di brevetto, marchi, copyright o altri diritti di proprietà intellettuale che coprono argomenti in questo documento. Fatta eccezione per quanto espressamente specificato in un contratto di licenza scritta da Microsoft, l'arredamento di questo documento non offre alcuna licenza per questi brevetti, marchi, copyright o altre proprietà intellettuali.



Microsoft, MS-DOS, Windows, WindowsServer, Windows Vista, Active Directory e ActiveSync sono marchi registrati o marchi commerciali di MicrosoftCorporation negli Stati Uniti e/o in altri paesi.

I nomi delle società e dei prodotti effettivamente menzionati nel presente documento possono essere i marchi dei rispettivi proprietari.

 

 





