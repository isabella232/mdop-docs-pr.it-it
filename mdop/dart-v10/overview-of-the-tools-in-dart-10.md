---
title: Panoramica degli strumenti di DaRT 10
description: Panoramica degli strumenti di DaRT 10
author: dansimp
ms.assetid: 752467dd-b646-4335-82ce-9090d4651f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8bef2b92e998bebffae526d4288c76be081fe0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822995"
---
# Panoramica degli strumenti di DaRT 10


Dalla finestra del **set di strumenti di diagnostica e recupero** in Microsoft Diagnostics and Recovery Toolset (DART) 10, puoi iniziare uno dei singoli strumenti che Includi quando crei l'immagine di ripristino di Dart 10. Per informazioni su come accedere alla finestra del **set di strumenti di diagnostica e ripristino** , vedere [come recuperare i computer locali usando l'immagine di ripristino DaRT](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md).

Se è disponibile, è possibile usare la **creazione guidata soluzione** nella finestra del **set di strumenti di diagnostica e ripristino** per selezionare lo strumento più adatto per risolvere il problema specifico, in base a una breve intervista fornita dalla procedura guidata.

## Esplorazione degli strumenti DaRT


Segue una descrizione degli strumenti di DaRT 10.

### Gestione computer

**Gestione computer** è una raccolta di strumenti di amministrazione di Windows che consentono di risolvere i problemi di un computer. È possibile usare gli strumenti di gestione dei computer in DaRT per visualizzare le informazioni di sistema e i registri eventi, gestire i dischi, eseguire l'esecuzione di elenchi **automatizzati** e gestire servizi e driver. La console di **Gestione computer** è personalizzata per facilitare la diagnosi e il ripristino di problemi che potrebbero impedire l'avvio del sistema operativo Windows.

**Nota**  Il recupero dei dischi dinamici con dardo non è supportato.

 

### Analizzatore crash

Usare la **procedura guidata Analizzatore crash** per determinare rapidamente la causa di un errore del computer analizzando il file di dump della memoria nel sistema operativo Windows che si sta ripristinando. **Analizzatore crash** esamina il file di dump della memoria per il driver che ha causato il failover di un computer. Puoi quindi disabilitare il driver di dispositivo problema usando il nodo **Servizi e driver** nello strumento **Gestione computer** .

La **procedura guidata Analizzatore crash** richiede gli strumenti di debug per Windows e i file di simboli per il sistema operativo da ripristinare. Puoi includere entrambi i requisiti quando crei l'immagine di ripristino DaRT. Se non sono inclusi nell'immagine di ripristino e non è possibile accedervi nel computer in cui si sta effettuando il ripristino, è sufficiente copiare il file di dump della memoria in un altro computer e usare la versione autonoma di **Crash Analyzer** per diagnosticare il problema.

L' **analizzatore di crash** in uso è una buona idea anche se si prevede di rieseguire l'immagine del computer. L'immagine potrebbe avere un driver difettoso che causa problemi nell'ambiente. Eseguendo **analizzatore crash**è possibile identificare i driver dei problemi e migliorare la stabilità delle immagini.

Per altre informazioni su **Crash Analyzer**, vedere [diagnostica degli errori di sistema con Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md).

### Disk Commander

**Disk Commander** consente di recuperare e ripristinare partizioni o volumi di dischi usando uno dei processi di ripristino seguenti:

-   Ripristinare il record di avvio Master (MBR)

-   Recuperare uno o più volumi persi

-   Ripristinare le tabelle delle partizioni da **Disk Commander** backup

-   Salvare le tabelle delle partizioni in **Disk Commander** backup

**Avviso**  È consigliabile eseguire il backup di un disco prima di usare **Disk Commander** per ripristinarlo. Usando **Disk Commander**, puoi potenzialmente danneggiare i volumi e renderli inaccessibili. Inoltre, le modifiche apportate a un volume possono influire su altri volumi perché i volumi in un disco condividono una tabella di partizioni.

 

**Nota**  Il recupero dei dischi dinamici con dardo non è supportato.

 

### Cancellazione disco

È possibile usare il **wipe del disco** per eliminare tutti i dati da un disco o da un volume, anche i dati rimasti dopo la riformattazione di un'unità disco rigido. La **cancellazione del disco** consente di selezionare una sovrascrittura a passaggio singolo o una sovrascrittura a quattro passaggi, che soddisfa gli attuali standard del dipartimento della difesa degli Stati Uniti.

**Avviso**  Dopo aver asciugato un disco o un volume, non è possibile recuperare i dati. Verificare le dimensioni e l'etichetta di un volume prima di cancellarlo.

 

### Explorer

Lo strumento **Esplora risorse** consente di esplorare il file System e le condivisioni di rete del computer in modo da poter rimuovere i dati importanti archiviati dall'utente nell'unità locale prima di provare a ripristinare o riutilizzare il computer. Poiché è possibile eseguire il mapping delle lettere delle unità alle condivisioni di rete, è possibile copiare e trasferire facilmente i file dal computer alla rete per la sicurezza o dalla rete al computer per ripristinarli.

### Ripristino file

Il **ripristino dei file** consente di provare a ripristinare i file che sono stati eliminati accidentalmente o che erano troppo grandi per essere inseriti nel Cestino. Il **ripristino dei file** non è limitato ai normali volumi di disco, ma può trovare e ripristinare i file in volumi persi o in volumi crittografati da BitLocker.

**Nota**  Il recupero dei dischi dinamici con dardo non è supportato.

 

### Ricerca di file

Prima di ricreare un computer, è importante recuperare i file dal disco rigido locale, in particolare quando l'utente potrebbe non avere eseguito il backup o archiviare i file in un'altra posizione.

Lo strumento di **ricerca** apre una finestra di **ricerca file** che può essere usata per trovare i documenti quando non si conosce il percorso del file o per cercare tipi generali di file in tutti i dischi rigidi locali. È possibile cercare modelli di nomi di file specifici in percorsi specifici. Puoi anche limitare i risultati a un intervallo di date o a un intervallo di dimensioni.

### Disinstallazione hotfix

La **procedura guidata per la disinstallazione dell'hotfix** consente di rimuovere gli hotfix o i Service Pack dal sistema operativo Windows nel computer che si sta riparando. Usare questo strumento quando si sospetta che sia previsto un hotfix o un Service Pack per impedire l'avvio del sistema operativo.

Ti consigliamo di disinstallare solo un hotfix alla volta, anche se lo strumento ti consente di disinstallare più di uno.

**Importante**  Le applicazioni installate o aggiornate dopo l'installazione di un hotfix potrebbero non funzionare correttamente dopo la disinstallazione di un hotfix.

 

### Fabbro

La **procedura guidata fabbro** consente di impostare o modificare la password per qualsiasi account locale nel sistema operativo Windows che si sta analizzando o ripristinando. Non è necessario conoscere la password corrente. La password impostata deve tuttavia essere conforme ai requisiti definiti da un oggetto Criteri di gruppo locale. Include la lunghezza e la complessità della password.

È possibile usare **fabbro** quando la password di un account locale, ad esempio l'account di amministratore locale, non è nota. Non è possibile usare **fabbro** per impostare le password per gli account di dominio.

### Editor del Registro di sistema

È possibile usare l' **Editor del registro** di sistema per accedere e modificare il registro di sistemi operativo Windows che si sta analizzando o riparando. Ciò include l'aggiunta, la rimozione e la modifica di chiavi e valori e l'importazione di file del registro di sistema (con estensione reg).

**Avviso**  Se si modifica il registro di sistema in modo non corretto utilizzando l' **Editor del registro di sistema**, si verificano problemi gravi. Questi problemi potrebbero richiedere di reinstallare il sistema operativo. Prima di apportare modifiche al registro di sistema, è consigliabile eseguire il backup di tutti i dati valutati nel computer. Cambiare il registro di sistema a proprio rischio.

 

### Analisi SFC

Lo strumento di **Analisi SFC** avvia la **procedura guidata di ripristino dei file di sistema** e consente di ripristinare i file di sistema che impediscono l'avvio del sistema operativo Windows installato. La **procedura guidata di ripristino dei file di sistema** può ripristinare automaticamente i file di sistema danneggiati o mancanti oppure può richiedere l'assistenza prima di eseguire eventuali riparazioni.

### Creazione guidata soluzione

La **creazione guidata soluzione** presenta una serie di domande e quindi consiglia lo strumento migliore per la situazione, in base alle proprie risposte. Questa procedura guidata consente di determinare lo strumento da usare quando non si ha familiarità con gli strumenti di DaRT.

### Configurazione TCP/IP

Quando si avvia un computer con problemi in DaRT, è impostato per ottenere automaticamente la configurazione TCP/IP (indirizzo IP e server DNS) dal protocollo DHCP (Dynamic Host Configuration Protocol). Se DHCP non è disponibile, è possibile configurare manualmente TCP/IP usando lo strumento di **configurazione TCP/IP** . Prima di tutto selezionare una scheda di rete e quindi configurare l'indirizzo IP e il server DNS per tale adapter.

## Argomenti correlati


[Attività iniziali di DaRT 10](getting-started-with-dart-10.md)

 

 





