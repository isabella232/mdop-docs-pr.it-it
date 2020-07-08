---
title: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0
description: Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0
author: dansimp
ms.assetid: 920f3fae-e9b5-4b94-beda-32c19d31e94b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9f9942eef7ea84cf7010a0c0173427827a512216
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804264"
---
# Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1.0


Per eseguire ricerche nelle note sulla versione di Microsoft User Experience Virtualization (UE-V), premere CTRL + F.

Prima di installare UE-V, leggere accuratamente queste note sulla versione. Le note sulla versione contengono informazioni necessarie per installare correttamente la virtualizzazione dell'esperienza utente e contengono informazioni aggiuntive che non sono disponibili nella documentazione del prodotto. Se sono presenti differenze tra queste note sulla versione e altre documentazioni UE-V, l'ultima modifica deve essere considerata autorevole. Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.

## Commenti e suggerimenti


Spiegaci cosa ne pensi della nostra documentazione per MDOP fornendoci feedback e commenti. Inviare il feedback della documentazione a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Problemi noti di UE-V


Questa sezione contiene note sulla versione per la virtualizzazione dell'esperienza utente.

### Le impostazioni del registro di sistema non riescono a eseguire la sincronizzazione tra App-V e le applicazioni native nello stesso computer

Quando un computer dispone di un'applicazione disponibile sia con l'applicazione Application Virtualization (App-V) che con un'applicazione di installazione nativa (installata con un file MSI), le impostazioni basate sul Registro di sistema non vengono sincronizzate tra le tecnologie.

SOLUZIONE alternativa: per risolvere il problema, eseguire l'applicazione selezionando una delle due tecnologie, ma non entrambe.

### La sincronizzazione delle impostazioni di Windows 8 non riesce con errore: "Boost:: filesystem:: exists:: nome utente o password non corretto"

La sincronizzazione delle impostazioni del sistema operativo Windows® 8 non riesce con il messaggio di errore seguente: **Boost:: filesystem:: exists:: nome utente o password non corretti**. Per verificare la visualizzazione di eventi del log operativo, aprire il **Visualizzatore eventi** e passare a **applicazioni e servizi registra**la registrazione della  /  **Microsoft**  /  **virtualizzazione dell'esperienza utente**Microsoft  /  **Logging**  /  **Operational**. Le condivisioni di rete usate per i percorsi di archiviazione delle impostazioni di UE-V dovrebbero risiedere nello stesso dominio Active Directory dell'utente. In caso contrario, potrebbe verificarsi l'errore seguente: "nome utente o password errati".

SOLUZIONE alternativa: usare le condivisioni di rete dello stesso dominio Active Directory dell'utente. .

### Firma di posta elettronica in roaming per Outlook 2010

UE-V sposterà i file di firma di Outlook 2010 tra i dispositivi. Tuttavia, le opzioni di firma predefinite per i nuovi messaggi e le risposte/inoltri non lo sono.Queste due impostazioni sono archiviate nel profilo di Outlook, che UE-Vdoes non è in roaming.

SOLUZIONE alternativa: None.

### Le impostazioni di sincronizzazione non vengono sincronizzate nell'intervallo previsto durante l'uso in modalità di collegamento lento

In condizioni normali i percorsi di archiviazione delle impostazioni devono essere disponibili tramite una connessione di rete a collegamento veloce. In modalità di collegamento lento la sincronizzazione si verificherà solo su base periodica. Per impostazione predefinita, la pianificazione della sincronizzazione della modalità di collegamento lenta è impostata su ogni 360 minuti.

SOLUZIONE alternativa: per cambiare la frequenza della sincronizzazione in background per i computer in modalità di collegamento lento, è possibile configurare i criteri di gruppo per i criteri di sincronizzazione in background per **i file offline**.

### I caratteri speciali non vengono sincronizzati

Alcuni caratteri, ad esempio i simboli di valuta, non vengono sincronizzati tra i computer Windows 7 e Windows 8 che eseguono l'agente UE-V.

SOLUZIONE alternativa: None.

### UE-V non supporta le impostazioni di roaming tra le versioni a 32 bit e 64 bit di Microsoft Office

È consigliabile installare la versione a 32 bit di Microsoft Office per sistemi operativi a 32 e 64 bit. Per scegliere la versione di Microsoft Office di cui si ha bisogno, fare clic qui. ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)). UE-V supporta le impostazioni di roaming tra le versioni di Office con architettura identica. Ad esempio, le impostazioni di Office di 32 bit andranno in roaming tra tutte le istanze di Office a 32 bit. UE-V non supporta le impostazioni di roaming tra le versioni di Office a 32 bit e 64 bit.

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

### I percorsi più lunghi di 260 caratteri non sono supportati

I percorsi di archiviazione delle impostazioni con più di 260 caratteri non sono supportati. La copia dei pacchetti di impostazioni UE-V in percorsi di archiviazione delle impostazioni che superano i 260 caratteri non riesce e genera il messaggio di eccezione seguente nel log eventi operativo UE-V: **\ [Boost:: filesystem:: Copy \ _file: il sistema non riesce a trovare il percorso specificato \]**. Per verificare la visualizzazione di eventi del log operativo, aprire il **Visualizzatore eventi** e passare a **applicazioni e servizi registra**la registrazione della  /  **Microsoft**  /  **virtualizzazione dell'esperienza utente**Microsoft  /  **Logging**  /  **Operational**.

I percorsi delle impostazioni dei file con più di 260 caratteri non sono attualmente supportati. Le impostazioni dei file a cui si fa riferimento nei modelli di posizione delle impostazioni di UE-V non possono essere posizionate in un percorso di directory che supera i 260 caratteri.

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

### I segnalibri di Internet Explorer non vengono visualizzati in Internet Explorer SmartBar

Quando i segnalibri di Internet Explorer si spostano da un computer a un altro, l'indice nel secondo computer non può essere aggiornato, quindi quando si digita la barra degli indirizzi, il favorito non viene visualizzato come risultato di ricerca nel computer 2.

SOLUZIONE alternativa: None

 

 





