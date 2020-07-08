---
title: Note sulla versione di MBAM 2.5 SP1
description: Note sulla versione di MBAM 2.5 SP1
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824986"
---
# Note sulla versione di MBAM 2.5 SP1


Per cercare queste note sulla versione, premere CTRL + F.

Leggere accuratamente queste note sulla versione prima di installare Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1. Queste note sulla versione contengono informazioni necessarie per installare correttamente MBAM e possono contenere informazioni che non sono disponibili nella documentazione del prodotto. Se queste note sulla versione si differenziano da altre documentazioni di MBAM 2,5 SP1, tenere presente che la modifica più recente è autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> Problemi noti di MBAM 2,5 SP1


Questa sezione contiene le note sulla versione per MBAM 2,5 SP1.

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a>I cmdlet di PowerShell Read-AD \ * non consentono di inviare commenti e suggerimenti se l'utente non dispone di diritti sufficienti

Se un utente che prova a usare i cmdlet di PowerShell Read-AD \ * per il server MBAM non ha diritti utente per leggere le informazioni di ripristino di Active Directory o per leggere le informazioni sul TPM, i cmdlet non forniranno all'utente alcun errore o avviso.

**Soluzione alternativa:** Usare i cmdlet di PowerShell Read-AD \ * solo se si hanno i diritti utente necessari.

### I cmdlet di migrazione di MBAM Active Directory (AD) non recuperano le informazioni sul ripristino del volume

I cmdlet di migrazione di MBAM Active Directory (AD) non riescono a recuperare le informazioni di ripristino del volume per i computer in unità organizzative (OU) se il carattere barra (/) fa parte del nome dell'unità organizzativa. Le estrazioni degli annunci ripetute avranno esito negativo con un errore di terminazione della pipeline quando viene rilevato questo errore.

**Dettagli tecnici:** Questo errore verrà visualizzato quando si eseguirà il comando:

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

Inoltre, l'analisi dello stack dell'eccezione `Error[0].Exception.StackTrace` avrà un aspetto simile al seguente:

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

**Soluzione alternativa:** Eseguire una di queste attività per risolvere la situazione:

-   Rinominare l'unità organizzativa per rimuovere il carattere barra di inoltro e quindi eseguire lo script.

-   Per escludere un'unità organizzativa problematica dal processo di backup, trovare un elenco delle unità organizzative i cui nomi non contengono il carattere barra di inoltro. Eseguire lo script in queste unità organizzative, una OU alla volta.

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> MBAM non riesce a crittografare un volume e segnala un errore se si imposta una protezione TPM + PIN in un dispositivo Tablet

Se gli utenti finali provano a impostare una protezione TPM + PIN in un dispositivo tablet, MBAM non riesce a crittografare e segnala un errore. Questo problema si verifica perché i dispositivi tablet non dispongono di una tastiera dell'ambiente di avvio preliminare.

**Soluzione alternativa:** Abilitare l' **uso dell'autenticazione di BitLocker che richiede l'immissione di Preboot da tastiera nell'impostazione di criteri di gruppo Tablet** . Questa impostazione è un'impostazione di criteri di gruppo di BitLocker e non è disponibile nei modelli di criteri di gruppo di MBAM.

### Il nome dell'entità utente è obbligatorio per tutti gli account del servizio

Il nome dell'entità utente (UPN) deve essere impostato per tutti gli account del servizio in MBAM. Se non si riesce a creare un UPN per un account, durante il processo di configurazione viene visualizzato un messaggio di errore che indica che non è stato possibile trovare l'utente o il gruppo in Active Directory.

**Soluzione alternativa:** Aggiungere l'UPN all'account del servizio.

### Il portale self-service e il sito Web di amministrazione e monitoraggio non si aprono dopo l'aggiornamento di IIS a .NET Framework 4,5

Quando si aggiorna Internet Information Services (IIS) a Microsoft .NET Framework 4,5, il portale self-service e il sito Web di amministrazione e monitoraggio non si aprono.

**Soluzione alternativa:** Vedere l'articolo [messaggio di errore dopo l'installazione di .NET Framework 4,0: "Impossibile caricare il tipo" System. ServiceModel. Activation. HttpModule "](https://go.microsoft.com/fwlink/?LinkId=393568).

### Il sito Web di amministrazione e monitoraggio Visualizza un messaggio di errore "Impossibile trovare il report" quando i report non sono configurati

Se si configura il sito Web amministrazione e monitoraggio e quindi si prova a visualizzare un report senza configurare prima la caratteristica report, viene visualizzato un messaggio di errore che indica che non è possibile trovare il report.

**Soluzione alternativa:** Configurare la caratteristica report prima di configurare le applicazioni Web.

### I report nel sito Web amministrazione e monitoraggio visualizzano un avviso se SSL non è configurato in SSRS

Se SQL Server Reporting Services (SSRS) non è stato configurato per l'uso di Secure Socket Layer (SSL), l'URL della caratteristica report verrà impostato su HTTP anziché su HTTPS quando si configura il server MBAM. Se si apre il sito Web amministrazione e monitoraggio e si seleziona un report, viene visualizzato il messaggio di errore seguente: "viene visualizzato solo il contenuto protetto".

**Soluzione alternativa:** Per visualizzare il report, fare clic su **Mostra tutto il contenuto**. Per risolvere il problema, passare al computer MBAM in cui è installato SQL Server Reporting Services, eseguire **Gestione configurazione di Reporting Services**e quindi fare clic su **URL servizio Web**. Selezionare il certificato SSL appropriato per il server, immettere la porta SSL appropriata (la porta predefinita è 443) e quindi fare clic su **applica**.

### Se si fa clic su "back" nel report Riepilogo conformità di BitLocker, potrebbe essere generato un errore

Se si esegue il drill-down in un report di riepilogo conformità di BitLocker e quindi si fa clic sul collegamento a **ritroso** nel report SSRS, potrebbe essere generato un errore.

**Soluzione alternativa:** Nessuno.

### La forza di crittografia viene visualizzata in modo non corretto nel report conformità computer BitLocker

Se non si imposta un valore di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di criteri di gruppo forza di crittografia, il report conformità computer BitLocker nella topologia di integrazione di Configuration Manager Visualizza sempre "sconosciuto" per il livello di cifratura, anche quando l'intensità della cifratura usa l'impostazione predefinita della crittografia a 128 bit. Il report Visualizza il livello di crittografia corretto se si imposta uno specifico livello di crittografia nell'oggetto Criteri di gruppo.

**Soluzione alternativa:** Imposta sempre un livello di crittografia specifico nell'oggetto **Scegli il metodo di crittografia dell'unità e** il criterio di gruppo forza di crittografia.

### La distribuzione dello stato di conformità tramite il tipo di unità Visualizza dati obsoleti dopo l'aggiornamento degli elementi di configurazione

Dopo aver aggiornato gli elementi di configurazione di MBAM in SystemCenter2012 ConfigurationManager, la distribuzione dello stato di conformità tramite il grafico a barre del tipo di unità nel dashboard conformità Enterprise di BitLocker Mostra i dati basati sulle informazioni di versioni precedenti degli elementi di configurazione.

**Soluzione alternativa:** Nessuno. La modifica degli elementi di configurazione di MBAM non è supportata e il report potrebbe non essere visualizzato come previsto.

### La configurazione di sicurezza avanzata può causare la visualizzazione errata di un messaggio di errore

Se la configurazione di sicurezza avanzata di Internet Explorer (ESC) è attivata, potrebbe essere visualizzato un messaggio di errore "accesso negato" quando si prova a visualizzare i report nel server MBAM. Per impostazione predefinita, ESC è attivato per proteggere il server diminuendo l'esposizione del server a potenziali attacchi che possono verificarsi tramite il contenuto Web e gli script delle applicazioni.

**Soluzione alternativa:** Se viene visualizzato il messaggio di errore "accesso negato" quando si prova a visualizzare i report nel server MBAM, è possibile impostare un oggetto Criteri di gruppo o modificare manualmente l'impostazione predefinita nell'immagine per disabilitare la configurazione di sicurezza avanzata. È anche possibile visualizzare in alternativa i report di un altro computer in cui ESC non è abilitato.

### Supporto per l'algoritmo di crittografia BitLocker XTS-AES
BitLocker ha aggiunto il supporto per l'algoritmo di crittografia XTS-AES in Windows 10, versione 1511. Con HF02, MBAM ha aggiunto il supporto client per l'opzione BitLocker e in HF04 è stato aggiunto il supporto lato server. Tuttavia, esiste un limite noto:

* I clienti devono usare la stessa forza di crittografia per il sistema operativo e i volumi di dati nello stesso computer.
Se vengono usati diversi punti di forza per la crittografia, MBAM riporterà la macchina come **non conforme**.

### Il portale self-service aggiunge automaticamente "-" alla voce ID chiave
A partire da HF02, il portale self-service di MBAM aggiunge automaticamente la voce "-" all'ID chiave.  
**Nota:** Il server deve essere riconfigurato per il fatto che il codice JavaScript abbia effetto.

### I report di MBAM 2,5 SP1 non funzionano/eseguono correttamente il rendering
La pagina report non esegue il rendering correttamente quando SSRS è ospitato in SQL Server 2016 Edition. 
Ad esempio, passando all'helpdesk-facendo clic sui report-(la parte evidenziata contiene "x" su di essa), questa operazione viene ulteriormente eseguita con Fiddler, che ha l'aspetto di una volta che si fa clic su report, che chiama la pagina SSRS con il formato di rendering HTML 4,0.

**Soluzione alternativa:** Guardando il codice sito. master e notato che la modalità X-UA è stata dettata come IE8. Il modo in cui IE8 supera la fine della vita e il cliente usa IE11. Aggiornare l'impostazione al codice seguente. Questo consente al sito di usare le tecnologie di rendering di IE11

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

L'impostazione originale è: 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


Questo è il motivo per cui il problema non è stato visto con altri browser come Chrome, Firefox e così via.



## Argomenti correlati


[Informazioni su MBAM 2.5](about-mbam-25.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





