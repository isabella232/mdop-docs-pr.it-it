---
title: Note sulla versione di App-V 5.0 SP2
description: Note sulla versione di App-V 5.0 SP2
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804894"
---
# Note sulla versione di App-V 5.0 SP2


**Per cercare un problema specifico in queste note sulla versione, premere CTRL + F.**

Leggere accuratamente queste note sulla versione prima di installare App-V 5,0 SP2.

Queste note sulla versione contengono informazioni necessarie per installare correttamente App-V 5,0 SP2. Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto. Se sono presenti differenze tra queste note sulla versione e altre documentazioni di App-V 5,0, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Informazioni sulla documentazione del prodotto


Per informazioni sulla documentazione di App-V 5,0, vedere la Home page di App-V 5,0 in Microsoft TechNet.

## Inviare commenti e suggerimenti


Siamo interessati a ricevere commenti e suggerimenti su App-V 5,0. È possibile inviare il proprio feedback <mdopdocs@microsoft.com> .

**Nota**  Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future nella documentazione e nei rilasci del prodotto.

 

Per le informazioni più aggiornate su MDOP e sulle risorse di formazione aggiuntive, vedere la pagina relativa all' [esperienza di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Per altre informazioni sui nuovi aggiornamenti o per inviare commenti e suggerimenti, seguici su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemi noti del pacchetto hotfix 4 per Application Virtualization 5,0 SP2


### I pacchetti smettono di funzionare dopo la disinstallazione del pacchetto hotfix 4 per Application Virtualization 5,0 SP2

Pacchetti pubblicati quando il pacchetto hotfix 4 per Application Virtualization 5,0 SP2 viene applicato smette di funzionare quando viene rimosso il pacchetto hotfix 4 per Application Virtualization 5,0 SP2.

SOLUZIONE

Se la cartella seguente esiste, è necessario eliminarla:

**% LocalAppData%**  \\  **Microsoft**  \\  **Appv**  \\  **Client**  \\  **VFS**  \\  ** &lt; ID &gt; pacchetto** per ogni pacchetto pubblicato.

**Nota**  Per eliminare la cartella, è necessario disporre di privilegi elevati.

 

Per usare uno script, per ogni account utente nel computer e per ogni ID pacchetto pubblicato dopo l'installazione del pacchetto hotfix 4 per Application Virtualization 5,0 SP2:

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   I tasti di scelta rapida rimarranno con le sessioni utente anche dopo l'eliminazione della cartella dalla directory nella sezione precedente, quindi è possibile fare clic sul collegamento per eseguire di nuovo l'applicazione. Non è necessario pubblicare di nuovo l'applicazione.

-   Questo problema si verifica sia per i pacchetti pubblicati dall'utente che per quelli a livello globale, ad esempio Microsoft Office2013. La cartella deve essere eliminata per entrambi i tipi di pacchetti.

-   Non è necessario eliminare la cartella VFS nei dati dell'app roaming (**% AppData%**). Solo la **% LocalAppData%** deve essere eliminata.

### Punti di integrazione di Microsoft Office nella posizione errata del file System

Punti di integrazione di Microsoft Office nella posizione errata del file System (Groove.exe messaggio di errore).

SOLUZIONE

Usare uno dei metodi seguenti:

1.  Eliminare il collegamento nella cartella di avvio dopo l'aggiornamento.

2.  Modificare il collegamento nella cartella di avvio con uno script.

3.  Usa il file di configurazione della distribuzione per specificare la destinazione di collegamento alla radice di integrazione.

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> Pacchetto hotfix 4 per il programma di installazione di Application Virtualization 5,0 SP2 può richiedere molto tempo

Il pacchetto hotfix 4 per il programma di installazione di Application Virtualization 5,0 SP2 può richiedere molto tempo a seconda del numero di file archiviati nella cache del pacchetto esistente.

L'aggiornamento dei descrittori di sicurezza dei pacchetti associati durante il pacchetto di hotfix 4 per l'installazione di Application Virtualization 5,0 SP2 ha un impatto significativo sul tempo necessario per l'installazione. In precedenza, l'installazione è stata standard in Duration. Tuttavia, ora dipende dal numero di file che sono stati inscenati nella cache del pacchetto.

SOLUZIONE alternativa: None

### La disinstallazione del pacchetto hotfix 4 per Application Virtualization 5,0 SP2 non riesce se è in uso il pacchetto JIT-V

Se si installa il pacchetto di hotfix 4 per Application Virtualization 5,0 SP2 e quindi si prova a disinstallare l'hotfix quando viene usata la virtualizzazione JIT (just-in-Time), l'operazione non riesce se si verificano tutte le condizioni seguenti:

-   È stato installato usando un file di Windows Installer (con estensione msi) e quindi si applicano gli aggiornamenti usando un file di patch di Microsoft Installer (con estensione msp).

-   Si prova a disinstallare un aggiornamento usando l'elemento Aggiungi o Rimuovi programmi nel pannello di controllo.

-   Nel computer è in uso un pacchetto abilitato per V JIT.

SOLUZIONE alternativa: completare la procedura seguente:

1.  Aprire Windows PowerShell ed eseguire i comandi seguenti:

    -   **Import-Module appvclient**

    -   **Get-AppvClientPackage | Stop-AppvClientPackage**

2.  Disinstallare l'aggiornamento usando Aggiungi o Rimuovi programmi.

## Problemi noti di App-V 5,0 SP2


### <a href="" id="bkmk-folderredirection"></a>Il reindirizzamento delle cartelle client App-V a volte non riesce a trasferire i file da% AppData% a% LocalAppData%

Quando% AppData% è una cartella di rete condivisa configurata per il reindirizzamento delle cartelle, le modifiche apportate agli utenti finali a AppData (roaming) possono essere perse quando si cambia computer o quando il loro AppData locale viene deselezionato quando si disconnette e quindi si riattiva. Questo errore si verifica perché la chiave del registro di sistema (AppDataTime), che indica l'ultimo caricamento noto, esce dalla sincronizzazione con il AppData memorizzato nella cache locale.

SOLUZIONE alternativa: eliminare manualmente la chiave del registro di sistema seguente per ogni pacchetto pertinente quando un utente finale effettua l'accesso o la disattivazione:

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

La prima volta che gli utenti finali avviano un'applicazione nel pacchetto dopo l'accesso, App-V impone il download della compressione% AppData%, anche se% LocalAppData% è già aggiornato.

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> App-V 5,0 Service Pack 2 (App-V 5,0 SP2) non include una nuova versione di App-V Server

App-V 5.0 SP2 non include una nuova versione del server App-V. Se si distribuiscono client App-V 5,0 SP2 che usano Windows 8,1 nell'ambiente e si prevede di gestire i client con l'infrastruttura App-V, è necessario installare il [pacchetto hotfix 2 per Microsoft Application Virtualization 5,0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634). (https://go.microsoft.com/fwlink/?LinkId=386634)

Se si esegue e si gestiscono client App-V 5,0 SP2 con uno dei metodi seguenti, non è necessario alcun aggiornamento client:

-   Modalità autonoma

-   Configuration Manager.

-   ESD di terze parti.

Il client App-V 5,0 SP2 è completamente compatibile con Windows 8,1

SOLUZIONE alternativa: None.

## Informazioni sul copyright delle note sulla versione


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società. Tutti gli altri marchi sono proprietà dei rispettivi proprietari.








## Argomenti correlati


[Informazioni su App-V 5.0 SP2](about-app-v-50-sp2.md)

 

 





