---
title: Note sulla versione di App-V 4.6 SP1
description: Note sulla versione di App-V 4.6 SP1
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819836"
---
# Note sulla versione di App-V 4.6 SP1


Per cercare queste note sulla versione, premere CTRL + F.

**Importante**  Leggere accuratamente queste note sulla versione prima di installare il sistema di gestione di Microsoft Application Virtualization (App-V). Queste note sulla versione contengono informazioni che consentono di installare correttamente Application Virtualization (App-V) 4.6 SP1. Questo documento contiene informazioni che non sono disponibili nella documentazione del prodotto. Se c'è una differenza tra queste note sulla versione e altre documentazioni di App-V, la modifica più recente deve essere considerata autorevole.

 

## Protezione da vulnerabilità e virus della sicurezza


Per proteggere le vulnerabilità e i virus della sicurezza, è importante installare gli ultimi aggiornamenti della sicurezza disponibili per qualsiasi nuovo software da installare. Per altre informazioni, vedere il [sito Web Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemi noti di Application Virtualization 4.6 SP1


Questa sezione fornisce le informazioni più aggiornate sui problemi relativi a Microsoft Application Virtualization (App-V) 4.6 SP1. Questi problemi non vengono visualizzati nella documentazione del prodotto e in alcuni casi potrebbe essere contraddetta la documentazione del prodotto esistente. Quando è possibile, questi problemi verranno risolti in versioni successive.

### Il percorso di SPRT viene perso se non termina con Slash (/)

Quando il percorso in un HREF in un modello di progetto non termina con una barra ( **/** ), l'oggetto href generato non include il percorso. Questo problema si verifica quando l'utente modifica manualmente il file **sprt** . Se usi il sequencer, la barra () viene sempre aggiunta **/** dopo il percorso.

SOLUZIONE verificare che l'HREF abbia una barra di avanzamento finale ( **/** ).

### Il nome della cartella utente non corrisponde al nome del pacchetto

Le cartelle che contengono file utente e Global. pkg non includono più il nome del pacchetto. In precedenza, il client App-V usato per usare la cartella radice del pacchetto 8,3 nome breve come parte del nome della cartella. Questo consente di identificarlo facilmente. Quando usi il sequencer App-V 4,6 SP1, la cartella radice del pacchetto 8,3 nomi brevi è ora stringhe casuali. In questo modo è difficile identificare le cartelle che contengono i file con **estensione pkg** del pacchetto nel computer in cui è in uso App-V client.

SOLUZIONE usare uno dei metodi seguenti per identificare più facilmente queste cartelle di pacchetti:

1.  Quando si crea il pacchetto usando il sequencer, specificare il nome di una cartella che segue la convenzione di denominazione di 8,3 per la cartella dell'applicazione principale. Questo nome verrà quindi usato come parte del nome della cartella utente, come nel caso di App-V 4,6.

2.  Il file con estensione SPRJ ora contiene un tag che visualizza la stringa usata come inizio del nome della cartella utente. Puoi usare l'elemento **ShortName** dell'elemento **PACKAGEROOTFOLDER** per determinare il nome.

### In uso App-V 4,6 SP1 nei computer con più di 64 processori

Quando si esegue App-V 4,6 SP1 nei computer in cui sono installati più processori 64, il client App-V non riesce.

SOLUZIONE alternativa nessuna. Questa configurazione non è supportata. È necessario eseguire App-V 4,6 SP1on computer con meno di 64 processori.

### L'aggiornamento di Application Virtualization 4,6 SP1 non è disponibile in tutte le impostazioni locali che usano Microsoft Update

Quando si usa Microsoft Update, l'aggiornamento per App-V 4,6 SP1 non è disponibile per le impostazioni locali della lingua seguenti:

-   Kazaco

-   Hindi

-   Serbo-cirillico

SOLUZIONE alternativa se si usa Microsoft Windows Server Update Services (WSUS), usare la versione in lingua inglese dell'aggiornamento o scaricare l'aggiornamento dal catalogo Microsoft Update.

### Dopo l'espansione del pacchetto padre, non è possibile eseguire la sequenza di un plug-in con componenti affiancati

Quando si espande un pacchetto padre usando **strumenti**  /  **Espandi pacchetto nel sistema locale** nella console App-V Sequencer e si sequenzia un plug-in con componenti affiancati, viene restituito un errore di installazione. Ad esempio:

-   **HRESULT 0x80073712**

Questo problema si verifica quando il Sequencer scrive il componente affiancato al registro di sistema, ma non cancella il valore per la chiave del registro di sistema seguente:

HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty

SOLUZIONE alternativa dopo l'espansione del pacchetto padre nel computer che sta eseguendo il sequencer, è necessario eliminare il valore per la chiave del registro di sistema seguente:

HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty

Dopo aver eliminato il valore, sequenziare il plug-in.

### Informazioni sul copyright delle note sulla versione

Questo documento viene fornito "così com'è". Le informazioni e le visualizzazioni espresse in questo documento, ad esempio URL e altri riferimenti al sito Web Internet, possono essere modificate senza preavviso. Si rischia di usarlo.

Alcuni esempi descritti in questo documento sono forniti solo per le illustrazioni e sono fittizi. Nessuna associazione o connessione reale è destinata o deve essere dedotta.

Il presente documento non implica la concessione di alcun diritto di proprietà intellettuale in relazione ai prodotti Microsoft. È possibile copiare e usare questo documento per fini di riferimento interno. È possibile modificare questo documento per gli scopi interni e di riferimento.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server e Windows Vista sono marchi di fabbrica del gruppo Microsoft di società.

Tutti gli altri marchi sono proprietà dei rispettivi proprietari.

 

 





