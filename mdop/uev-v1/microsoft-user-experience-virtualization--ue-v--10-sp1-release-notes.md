---
title: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0 SP1
description: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0 SP1
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804263"
---
# Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0 SP1


Per cercare le note sulla versione di Microsoft User Experience Virtualization (UE-V) 1,0 Service Pack 1, premere CTRL + F.

Prima di installare UE-V, leggere accuratamente queste note sulla versione. Le note sulla versione contengono informazioni necessarie per installare correttamente la virtualizzazione dell'esperienza utente e contengono informazioni aggiuntive che non sono disponibili nella documentazione del prodotto. Se sono presenti differenze tra queste note sulla versione e altre documentazioni UE-V, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Problemi noti di UE-V


Questa sezione contiene note sulla versione per la virtualizzazione dell'esperienza utente 1,0 SP1.

### Le impostazioni del registro di sistema non riescono a eseguire la sincronizzazione tra App-V e le applicazioni native nello stesso computer

Quando un computer dispone di un'applicazione disponibile sia con l'applicazione Application Virtualization (App-V) che con un'applicazione di installazione nativa installata con un Windows Installer (file con estensione msi), le impostazioni basate sul Registro di sistema non vengono sincronizzate tra le tecnologie.

SOLUZIONE alternativa: per risolvere il problema, eseguire l'applicazione selezionando una delle due tecnologie, ma non entrambe.

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a>La sincronizzazione delle impostazioni di Windows 8 non riesce quando la condivisione di rete è esterna al dominio dell'utente

Quando Windows® 8 tenta la sincronizzazione delle impostazioni del sistema operativo, synchrnization non riesce con il messaggio di errore seguente: **Boost:: filesystem:: exists:: nome utente o password non corretti**. Questo errore può indicare che la condivisione di rete è esterna al dominio dell'utente. Per verificare la visualizzazione di eventi del log operativo, aprire il **Visualizzatore eventi** e passare a **applicazioni e servizi registra**la registrazione della  /  **Microsoft**  /  **virtualizzazione dell'esperienza utente**Microsoft  /  **Logging**  /  **Operational**. Le condivisioni di rete usate per i percorsi di archiviazione delle impostazioni di UE-V dovrebbero risiedere nello stesso dominio Active Directory dell'utente.

SOLUZIONE alternativa: usare le condivisioni di rete dello stesso dominio Active Directory dell'utente. .

### Firma di posta elettronica in roaming per Outlook 2010

UE-V sposterà i file di firma di Outlook 2010 tra i dispositivi. Tuttavia, le opzioni di firma predefinite per i nuovi messaggi e le risposte/inoltri non vengono visualizzate in roaming. Queste due impostazioni sono archiviate nel profilo di Outlook, che UE-V non esegue il roaming.

SOLUZIONE alternativa: None.

### Le impostazioni di sincronizzazione non vengono sincronizzate nell'intervallo previsto durante l'uso in modalità di collegamento lento

In condizioni normali i percorsi di archiviazione delle impostazioni devono essere disponibili tramite una connessione di rete a collegamento veloce. In modalità di collegamento lento la sincronizzazione si verificherà solo su base periodica. Per impostazione predefinita, la pianificazione della sincronizzazione della modalità di collegamento lenta è impostata su ogni 360 minuti.

SOLUZIONE alternativa: per cambiare la frequenza della sincronizzazione in background per i computer in modalità di collegamento lento, è possibile configurare i criteri di gruppo per i criteri di sincronizzazione in background per **i file offline**.

### I caratteri speciali non vengono sincronizzati

Alcuni caratteri, ad esempio i simboli di valuta, non vengono sincronizzati tra i computer Windows 7 e Windows 8 che eseguono l'agente UE-V.

SOLUZIONE alternativa: None.

### UE-V non supporta le impostazioni di roaming tra le versioni a 32 bit e 64 bit di Microsoft Office

È consigliabile installare la versione a 32 bit di Microsoft Office per sistemi operativi a 32 e 64 bit. Per scegliere la versione di Microsoft Office di cui si ha bisogno, fare clic qui ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ). UE-V supporta le impostazioni di roaming tra le versioni di Office con architettura identica. Ad esempio, le impostazioni di Office di 32 bit andranno in roaming tra tutte le istanze di Office a 32 bit. UE-V non supporta le impostazioni di roaming tra le versioni di Office a 32 bit e 64 bit.

SOLUZIONE alternativa: None

### <a href="" id="msi-s-are-not-localized"></a>I file MSI non sono localizzati

UE-V 1,0 SP1 include un programma di configurazione localizzato per l'agente UE-V e per il generatore di UE-V. Questi file MSI sono ancora disponibili, ma l'interfaccia utente viene ridotta a icona e l'MSI viene visualizzato solo in inglese. Nonostante il file sia in inglese, il programma di installazione installa tutte le lingue supportate durante l'installazione.

SOLUZIONE alternativa: None

### Altre cartelle della condivisione con il percorso di archiviazione delle impostazioni non sono disponibili in modalità di connessione lenta

Le condivisioni dell'archivio delle impostazioni non devono trovarsi in una condivisione di rete usata per altre cartelle che devono sempre essere disponibili. Quando la condivisione di rete che ospita il percorso di archiviazione dell'impostazione entra in modalità di connessione lenta, l'unica cartella disponibile è la cartella della posizione di archiviazione delle impostazioni. Le altre cartelle della condivisione non sono disponibili in modalità di connessione lenta.

Soluzione alternativa: None

### Le favicon associate ai Preferiti di Internet Explorer 9 non vanno in roaming

Le favicon associate ai Preferiti di Internet Explorer 9 non vengono visualizzate in roaming dalla virtualizzazione dell'esperienza utente e non compaiono quando i Preferiti vengono visualizzati per la prima volta in un nuovo computer.

SOLUZIONE alternativa: le favicon verranno visualizzate con i Preferiti associati una volta che il segnalibro viene usato e memorizzato nella cache nel browser Internet Explorer 9.

### I percorsi delle impostazioni dei file sono archiviati nel registro di sistema

Alcune impostazioni dell'applicazione archiviano i percorsi dei file di configurazione e delle impostazioni come valori nel registro di sistema. I file a cui si fa riferimento come percorsi nel registro di sistema devono essere sincronizzati quando si esegue il roaming delle impostazioni tra i computer.

SOLUZIONE alternativa: usare il reindirizzamento delle cartelle o altre tecnologie per assicurarsi che tutti i file a cui si fa riferimento come percorsi di impostazioni file siano presenti e posizionati nella stessa posizione in tutti i computer in cui le impostazioni si aggirano.

### I percorsi di archiviazione delle impostazioni lunghe possono causare un errore

Mantieni il più breve possibile i percorsi di archiviazione delle impostazioni. I percorsi lunghi potrebbero impedire la risoluzione o la sincronizzazione. UE-V usa il percorso di archiviazione delle impostazioni come parte del percorso calcolato per archiviare le impostazioni. Questo percorso viene calcolato nel modo seguente: percorso di archiviazione delle impostazioni + "SettingsPackages" + dir pacchetto (ID modello) + nome pacchetto (ID modello). Se il percorso calcolato supera i 260 caratteri, lo spazio di archiviazione del pacchetto non riesce e genera il messaggio di errore seguente nel log eventi operativo della UE-V:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Per controllare gli eventi del log operativo, aprire il Visualizzatore eventi e passare a registri applicazioni e servizi/Microsoft/esperienza utente per la virtualizzazione/registrazione/operativo.

SOLUZIONE alternativa: None.

### UE-V Agent ritardi al logout o all'accesso

Se si verifica un accesso o un logout prima che i file offline abbiano stabilito che un collegamento lento è in posizione, la disconnessione o l'accesso potrebbero essere ritardati. La funzionalità file offline può richiedere fino a tre minuti per rilevare lo stato corrente della rete. Se l'accesso o l'arresto si verifica prima che i file offline abbiano determinato che il computer è connesso a un collegamento lento, il pacchetto di impostazioni UE-V verrà inviato al server invece della cache locale.

SOLUZIONE alternativa: None.

### Conflitto di impostazioni quando si prova a eseguire il roaming delle impostazioni del sistema operativo in Windows 8

In Windows 8 se la sincronizzazione dell'account Microsoft è abilitata insieme a UE-V per le impostazioni del sistema operativo, le impostazioni applicate potrebbero non essere coerenti.

SOLUZIONE alternativa: eseguire una delle operazioni seguenti:

-   Disabilitare la sincronizzazione dell'account Microsoft se si usa UE-V per aggirare le impostazioni del sistema operativo

-   Disabilitare UE-V per le impostazioni del sistema operativo

### Alcune impostazioni del sistema operativo si aggirano solo tra le versioni del sistema operativo

Le impostazioni del sistema operativo per l'Assistente vocale e i caratteri di valuta specifici per le impostazioni locali si aggirano solo tra le versioni del sistema operativo di Windows. Ad esempio, i caratteri di valuta verranno spostati solo da Windows 7 a Windows 7.

SOLUZIONE alternativa: None

 

 





