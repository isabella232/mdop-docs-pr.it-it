---
title: Progettare l'infrastruttura del server MED-V
description: Progettare l'infrastruttura del server MED-V
author: dansimp
ms.assetid: 2781040f-880e-4e16-945d-a38c0adb4151
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4ba4c38328c5484b7daa292f9fc33a4e59824327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824185"
---
# Progettare l'infrastruttura del server MED-V


In questo argomento verrà progettata l'infrastruttura server per ogni istanza MED-V. Ciò include la determinazione della presenza dell'istanza di SQL Server nel server MED-V o in un server remoto, oltre alle dimensioni del database di SQL Server. Verrà anche determinato il percorso della console di gestione.

## Progettare e posizionare il server per ogni istanza di MED-V


Il server MED-V implementa i criteri e archivia i dati relativi allo stato e alla cronologia relativi ai client.

### Fattore di forma

MED-V consiglia l'uso di un server CPU dual core da 2,8 GHz con 2GB di RAM. Questa raccomandazione si basa sul presupposto che il server MED-V verrà eseguito su un computer dedicato e che SQL Server e la console di gestione MED-V verranno eseguiti in computer distinti.

In base a questo carico di lavoro, il server MED-V deve essere caricato in un numero relativamente leggero. In assenza di indicazioni specifiche per l'architettura sul fattore di forma del server, progettare il server usando la raccomandazione MED-V, con la memoria che corrisponde al fattore di forma standard dell'organizzazione. Il server MED-V può essere eseguito in una macchina virtuale (VM) in Windows Server2008 Hyper-V. Se viene usata una VM, verificare che abbia accesso alle risorse della CPU e della memoria equivalenti a quelle specificate per un computer fisico.

La capacità del disco che il server MED-V richiede deve essere sufficiente per archiviare i file di configurazione dell'area di lavoro MED-V. Un'area di lavoro MED-V può usare solo una VM e un criterio per uno o più utenti. Di conseguenza, il numero di aree di lavoro MED-V che devono essere archiviate dipende dalla misura in cui sono necessari diversi criteri per diversi utenti della stessa VM, oltre al numero di VM che verranno usati. I file XML dell'area di lavoro MED-V sono di circa 30KB dimensioni per una tipica area di lavoro MED-V. Per determinare la capacità del disco necessaria, moltiplicare 30 KB per il numero di aree di lavoro MED-V che verranno archiviate dal server MED-V.

Le connessioni di rete più importanti del server MED-V sono i collegamenti ai client, quindi posizionare il server in un percorso di rete che fornisce la larghezza di banda più disponibile e i collegamenti più affidabili ai client.

### Tolleranza di errore

Può essere presente un solo server MED-V attivo in un'istanza di MED-V e MED-V non include funzionalità standard per inserire il server in un cluster di Microsoft Cluster Server (MSCS) per ottenere la tolleranza d'errore. Un server di backup passivo può essere configurato manualmente.

Per stabilire se un server di backup passivo deve essere configurato manualmente per l'istanza MED-V, determinare se gli utenti saranno autorizzati a usare le immagini MED-V in modalità offline. Per informazioni sulla modalità offline, vedere [come configurare un utente o un gruppo di dominio](how-to-configure-a-domain-user-or-groupmedvv2.md). Se gli utenti non possono lavorare offline, non saranno in grado di continuare a lavorare in caso di errore di un server MED-V, anche se l'area di lavoro MED-V è già stata avviata nel client. Se è consentito il lavoro offline, per ogni area di lavoro MED-V determinare per quanto tempo il client può lavorare offline prima che debba eseguire l'autenticazione. Questa è la quantità massima di tempo in cui il server non può essere disponibile.

## Progettare e posizionare il database di SQL Server


Il server MED-V usa il database di SQL Server per archiviare lo stato e gli eventi del client. È possibile installare il database di SQL Server nello stesso computer del server MED-V oppure inserirlo in un server separato in cui è in uso SQL Server, che può essere facoltativamente remoto. È possibile condividere il database con altre istanze di MED-V, in questo caso gli eventi e gli avvisi provenienti da tali istanze verranno archiviati nello stesso database e i report includeranno eventi di tutte le istanze. È possibile installare il database in un'istanza di SQL Server esistente e i database di altri server MED-V possono trovarsi nella stessa istanza.

Se si posiziona il server di database in una posizione remota dal server MED-V, tra i collegamenti di rete che non dispongono di larghezza di banda sufficiente, i report potrebbero essere lenti per il caricamento nella console e potrebbero non visualizzare i dati più recenti dai client. Fare riferimento alle aspettative del livello di servizio dell'organizzazione determinate in [definire l'ambito del progetto](define-the-project-scope.md) e usare queste informazioni per decidere dove posizionare il database di SQL Server.

### Fattore di forma

Se SQL Server viene eseguito nello stesso server di MED-V e se SQL Server viene usato solo per archiviare i dati per il server, iniziare con la raccomandazione MED-V e aggiungere risorse per il caricamento di SQL Server. Se SQL Server archivierà eventi e avvisi da più istanze di MED-V, per informazioni su come ridimensionare il fattore di forma del server, vedere la guida alla [pianificazione e alla progettazione di Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) (http://go.Microsoft.com/fwlink/?LinkId=163302).

Le dimensioni del database variano a seconda del numero di eventi client che verranno archiviati nel database. Gli eventi vengono creati tramite il normale funzionamento del client, ad esempio quando viene avviata un'area di lavoro MED-V o quando si verifica un errore nell'area di lavoro MED-V. L'intervallo predefinito in cui il client invia gli eventi è di 1 minuto.

Per stimare le dimensioni del database, determinare le operazioni seguenti:

-   Numero di client nell'istanza MED-V. Il valore massimo è 5.000.

-   Tasso di arrivo tipico dell'evento. Questa tariffa dipende dal comportamento di utilizzo del client, ma è di circa 15-20 eventi al giorno per ogni cliente.

-   Dimensione evento. Le dimensioni sono in genere intorno a 200 byte.

-   Importo dello spazio di archiviazione. Numero di giorni per cui verranno archiviati gli eventi.

Moltiplicare questi valori per calcolare le dimensioni dell'archivio dati obbligatorio in byte e quindi aggiungere un fattore di sicurezza per tenere conto delle operazioni seguenti:

-   Errori, che potrebbero creare un numero elevato di eventi da un client in un breve periodo di tempo.

-   Tabella di database e spazio organizzativo.

Per approssimare il requisito per l'ottimizzazione dell'infrastruttura al secondo (IOPs), usare i valori sopra riportati, moltiplicando il tasso di arrivo dell'evento tipico per il numero di client nell'istanza. Questo restituisce il numero di record che possono essere scritti ogni giorno. Dividere il numero per 86.400 per derivare il numero di record scritti al secondo. Se le operazioni di scrittura possono essere equiparate a un'operazione IO (Single Infrastructure Optimization), questo numero è necessario per la scrittura di IOPs. Aggiungere un buffer a tale attività per la creazione di report. Questa operazione è difficile da determinare, ma dipende dal numero di console in uso con l'istanza e dalla frequenza con cui vengono usati per generare report.

### Tolleranza di errore

Quando il client MED-V è in funzione, se il server non è disponibile, il backup degli eventi verrà eseguito sul client e i report non saranno disponibili nella console di gestione. Fare riferimento alle aspettative del livello di servizio dell'organizzazione determinate in [definire l'ambito del progetto](define-the-project-scope.md) per decidere se la progettazione di un'infrastruttura SQL Server a tolleranza d'errore è necessaria.

MED-V non offre il supporto per l'uso di SQL Server in un cluster MSCS. Per garantire la modalità di standby caldo e per evitare perdite di dati in caso di errore, è possibile inserire SQL Server in una configurazione di log shipping. Per informazioni sulla distribuzione del log, vedere la guida alla [pianificazione e alla progettazione dell'infrastruttura Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) ( https://go.microsoft.com/fwlink/?LinkId=163302) .

## Progettare la console di gestione


Parte della funzionalità della console di gestione di MED-V consiste nel testare le VM prima che vengano imballate per la distribuzione nei client MED-V. Di conseguenza, la console di gestione deve essere progettata con un fattore di forma simile, il più vicino possibile, al fattore di forma di un tipico computer client MED-V.

L'applicazione console di gestione viene installata insieme al client MED-V e USA Microsoft Virtual PC2007 SP1 con l'hotfix descritto nell'articolo 974918 della Microsoft Knowledge base. Deve essere usato un sistema operativo client; la console di gestione MED-V non può essere eseguita nello stesso sistema del server MED-V.

Non è possibile condividere una console di gestione con più istanze del server MED-V. L'indirizzo del server MED-V viene specificato durante l'installazione del client MED-V della console di gestione; Questa operazione può essere modificata dopo l'installazione, ma in qualsiasi momento la console di gestione può funzionare solo con un solo server MED-V.

È possibile usare più console di gestione con un singolo server MED-V. Per evitare conflitti, è disponibile un meccanismo che informa gli altri utenti della console quando una console ha apportato modifiche a un'area di lavoro MED-V.

Per ogni istanza MED-V, determinare quante console di gestione saranno necessarie e dove verranno inserite. Selezionare un fattore di modulo client MED-V tipico da usare per la console di gestione.

## Argomenti correlati


[Configurazioni supportate di MED-V 1.0 SP1](med-v-10-sp1-supported-configurationsmedv-10-sp1.md)

[Configurazione del server MED-V per la modalità cluster](configuring-med-v-server-for-cluster-mode.md)

[Come installare il client MED-V e MED-V Management Console](how-to-install-med-v-client-and-med-v-management-console.md)

[Uso dell'interfaccia utente di MED-V Management Console](using-the-med-v-management-console-user-interface.md)

 

 





