---
title: Creazione di database App-V 4.5 con script SQL
description: Creazione di database App-V 4.5 con script SQL
author: dansimp
ms.assetid: 6cd0b180-163e-463f-a658-939ab9a7cfa1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ab2c102a43701bfdeaac49359b4ca3c4a063fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825976"
---
# Creazione di database App-V 4.5 con script SQL


**Per chi è destinata questa soluzione?** Professionisti della tecnologia dell'informazione che gestiscono i database di Application Virtualization (App-V) 4,5.

**Come può aiutarti questa guida?** Questa soluzione spiega e documenta la procedura per installare Microsoft Application Virtualization Server quando l'installazione dell'amministratore non ha privilegi di "sysadmin" per SQL Server.

## Panoramica


Una delle sfide dell'installazione di Microsoft Application Virtualization 4,5 (App-V) consiste nel fatto che il programma di installazione presuppone che l'utente che installa le funzionalità del server non sia solo un amministratore del computer locale, ma disponga anche dei privilegi di amministratore di SQL Server che ospitano l'archivio dati. Questo requisito si basa sul fatto che il database, nonché i ruoli e le autorizzazioni appropriati, vengono creati come parte dell'installazione. Tuttavia, nella maggior parte delle aziende, i server SQL vengono gestiti separatamente dal team dell'infrastruttura che installerà App-V. Questi requisiti di sicurezza renderanno difficile ottenere agli amministratori SQL l'obbligo per l'amministratore dell'infrastruttura di installare App-V diritti adeguati; allo stesso modo, gli amministratori SQL non avranno i privilegi necessari per installare il prodotto per il team dell'infrastruttura.

Attualmente, un amministratore che prova l'installazione di App-V deve avere privilegi di SQL "sysadmin". Nelle versioni precedenti del prodotto la configurazione consentiva agli amministratori SQL di creare un account "sysadmin" temporaneo o di essere presente durante l'installazione per fornire le credenziali con i privilegi di "sysadmin". In questa versione gli script vengono forniti nel prodotto rilasciato per tutti gli amministratori da usare per l'implementazione dell'infrastruttura.

Questo whitepaper illustra lo scenario in cui l'installazione dovrà essere divisa in due attività separate: creazione del database SQL e installazione delle funzionalità di App-V Server. Gli amministratori di SQL sarebbero in grado di esaminare gli script SQL e apportare modifiche per risolvere eventuali conflitti con altri database o per supportare l'integrazione con altri strumenti. Il risultato degli script è consentire agli amministratori SQL di preparare il database in modo che gli amministratori dell'infrastruttura non debbano concedere diritti avanzati a SQL Server. Questo è importante in ambienti in cui i criteri di sicurezza lo vieteranno.

### Processo di creazione di database SQL

Gli script SQL consentono agli amministratori SQL di creare il database richiesto e di configurare i privilegi per gli amministratori di App-V per installare e gestire correttamente l'ambiente. I passaggi per il completamento di queste attività sono elencati più avanti in questo documento.

Questo processo separa le azioni di creazione e configurazione del database dall'installazione effettiva di App-V.

**Informazioni da fornire agli amministratori SQL**

-   Nome del gruppo di annunci che sarà l'amministratore dell'App-V

-   Nome del server in cui verrà installato App-V Management Server

**Informazioni da restituire agli amministratori dell'infrastruttura**

-   Nome del server di database o dell'istanza e il nome del database App-V

Dopo aver preparato il database, gli amministratori di App-V possono eseguire l'installazione di App-V senza privilegi di amministratore SQL.

### Uso degli script di configurazione SQL

**Requisiti**

Di seguito è riportato un elenco di requisiti per l'uso degli script che si trovano nella cartella support\\createdb nella radice della posizione di estrazione selezionata.

-   Gli script devono essere copiati in una posizione scrivibile nel computer in cui verranno eseguiti (assicurarsi di rimuovere l'attributo di sola lettura da questi script dopo la copia) e gli strumenti client SQL devono essere caricati nel computer (osql è necessario solo per l'esecuzione dei file batch di esempio nel computer locale).

-   SQL Server deve supportare l'autenticazione di Windows.

-   Verificare che l'istanza di SQL Server e il servizio agente SQL siano in uso.

-   Accedere con un account di dominio che è un amministratore SQL (sysadmin) nel computer in cui verranno eseguiti gli script.

Gli script vengono eseguiti sotto le credenziali di dominio dell'utente connesso.

**Creazione di database con script SQL**

**Attività che devono essere eseguite dagli amministratori di SQL:**

1.  Copiare gli script contenuti nella cartella support\\createdb dalla radice della posizione di estrazione selezionata al computer in cui verranno eseguiti gli script. I file seguenti sono obbligatori per l'esecuzione corretta degli script e devono essere chiamati nell'ordine presentato di seguito.

    -   database. SQL

    -   Roles. SQL

    -   tabella \ _CODES. SQL

    -   funzioni \ _before \ _tables. SQL

    -   Tables. SQL

    -   functions. SQL

    -   views. SQL

    -   procedure. SQL

    -   Triggers. SQL

    -   dati \ _codes. SQL

    -   dati \ _messages. SQL

    -   dati \ _defaults. SQL

    -   avvisi \ _jobs. SQL

    -   DBVERSION. SQL

2.  Rivedere e modificare, se necessario, il `database.sql` file. Le impostazioni predefinite denominano il database "APPVIRTDB".

    -   Se necessario, Sostituisci `APPVIRTDB` le istanze con il `database name` che verrà usato.

    -   Modificare la `FILENAME` proprietà nello script con il percorso appropriato per SQL Server in cui verrà creato il database.

3.  Rivedere e modificare, se necessario, `database name [APPVIRTDB]` nel `roles.sql` file usato nel file database. SQL.

****

### Esempio di come automatizzare il processo con i file batch

Se usato, i due file batch di esempio forniti eseguono gli script SQL nel modo seguente:

1.  **Create\_schema.bat (1)**

    -   database. SQL

    -   Roles. SQL

2.  **Create\_tables.bat (2)**

    -   tabella \ _CODES. SQL

    -   funzioni \ _before \ _tables. SQL

    -   Tables. SQL

    -   functions. SQL

    -   views. SQL

    -   procedure. SQL

    -   Triggers. SQL

    -   dati \ _codes. SQL

    -   dati \ _messages. SQL

    -   dati \ _defaults. SQL

    -   avvisi \ _jobs. SQL

    -   DBVERSION. SQL

**Nota**  
Una considerazione accurata quando si modificano gli script deve essere eseguita solo da un utente con le informazioni appropriate. Inoltre, per i file di esempio presentati è necessario modificare solo le operazioni seguenti: **create\_schema.bat**, **create\_tables.bat**, **database. SQL**e **Roles. SQL**. Tutti gli altri file non devono essere modificati in alcun modo perché questo potrebbe causare la creazione non corretta del database, che consentirà di installare l'errore dei servizi App-V.



I due file batch di esempio devono essere posizionati nella stessa directory in cui sono stati copiati tutti gli altri script SQL nel computer.

1.  Eseguire il file di esempio **create\_schema.bat** per creare il database. Questo script impiegano diversi secondi per completare l'operazione e non devono essere interrotti.

    -   Eseguire il file crea schema.bat dalla directory in cui è stato copiato. La sintassi è: "Create\_schema.bat `SQLSERVERNAME` "

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   Se questo script non riesce durante la creazione del nuovo database "APPVIRTDB", selezionare il log come indicato per correggere il problema. Sarà necessario eliminare il database creato con un parziale funzionamento degli script, in modo da assicurarti che i successivi tentativi funzionino correttamente.

2.  Eseguire il `create_tables.bat` file per creare le tabelle nel database. Questo script impiegano diversi secondi per completare l'operazione e non devono essere interrotti.

    -   Eseguire il file create\_tables.bat dalla directory in cui è stato copiato. La sintassi è: "create\_tables.bat `SQLSERVERNAME DBNAME` "

        ![App-v 4,6 SQL create\-table.bat](images/appv46sqlcreate-tablebat.gif)

        Se lo script non riesce durante la creazione delle tabelle, selezionare il log come indicato per correggere il problema. Sarà necessario eliminare il database ed eseguire create\_schema.bat prima di provare a eseguire il file di create\_tables.bat in tutti i tentativi successivi.

### Impostazione delle autorizzazioni per il database App-V

Gli account seguenti dovranno essere creati in SQL Server con autorizzazioni e ruoli specifici per il nuovo database per l'installazione, la distribuzione e l'amministrazione continua dell'ambiente App-V.

-   Creare un account di accesso per il gruppo amministratori App-V in SQL Server e il database APPVIRTDB per gli amministratori di domain\\App-V (dove "Domain" e "App-V Admins" verranno modificati per riflettere il proprio ambiente) e aggiungerli al ruolo del database SFTAdmin e SFTEveryone.

    ![App-v 4,6 script SQL impostare le autorizzazioni e i ruoli](images/appv46sqlscriptsetpermsroles.gif)

-   Concedere a questo gruppo l'autorizzazione "Visualizza qualsiasi definizione" a livello globale (questo consente al processo di configurazione del server di gestione di Microsoft Application Virtualization Management di verificare che l'accesso al server di gestione esista già). In MS-SQL 2005 e sopra le restrizioni di accesso ai metadati contenuti in master. DB sono stati aggiunti. L'utente creato nel passaggio precedente non avrà per impostazione predefinita i diritti necessari per l'installazione del server. Aprire le proprietà dell'account di accesso creato in precedenza, proprietà di login- &gt; entità a protezione diretta. Aggiungere l'istanza del database e abilitare "GRANT" per "Visualizza qualsiasi definizione", come illustrato nella schermata seguente.

    ![App-v 4,6 SQL script Grant Perm per la visualizzazione di qualsiasi def](images/appv46sqlscriptviewanydef.gif)

-   Aggiungere un ruolo alla tabella ROLE \ _ASSIGNMENTS per l'account di accesso creato nel passaggio precedente per consentire agli amministratori di App-V di accedere alla console di gestione di Application Virtualization, con role = "ADMIN" e Group \ _ref = "domain\\App-V Admins" (dove "Domain" e "App-V Admins" verranno modificati per riflettere il proprio ambiente).

    ![assegnazione di ruoli di script SQL di App-v 4,6](images/appv46sqlscriptroleassign.gif)

-   Creare un account di accesso per SQL Server e un database App-V per il server di gestione. Questo account viene usato da Microsoft Application Virtualization Management Server per connettersi all'archivio dati ed è responsabile della manutenzione delle richieste client per le applicazioni in streaming. A seconda della posizione in cui devono essere installati il server SQL e il server di gestione, sono disponibili due opzioni:

    1.  Se server di gestione e SQL Server verranno installati nello stesso computer, aggiungere un account di accesso per NT AUTHORITY\\NETWORK SERVICE e aggiungerlo ai ruoli di database di SFTUser e SFTEveryone.

    2.  Se il server di gestione e SQL Server devono essere installati in computer diversi, aggiungere un account di accesso per "domain\\App-V Server Name $" (dove "App-V Server Name" è il nome del server in cui verrà installato l'App-V Management Server) e aggiungerlo ai ruoli di database di SFTUser e SFTEveryone.

-   Aprire la finestra della query nella finestra SQL ed eseguire il codice SQL seguente:

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    Dove APPVIRTDB è il nome del database App-V creato in SQL Server nel passaggio precedente e l'utente che sta per eseguire l'installazione di App-v server deve essere un membro di "domain\\App-V Admins" (dove "Domain" e "App-V Admins" verranno modificati per riflettere il proprio ambiente).

### Attività che devono essere eseguite dagli amministratori dell'infrastruttura

1.  L'amministratore del gruppo "App-V Admins" dovrebbe installare App-V.

    Usare le informazioni degli amministratori di SQL per selezionare SQL Server e il database creato nei passaggi precedenti.

2.  L'amministratore del gruppo "App-V Admins" accede a Application Virtualization Management Console ed Elimina gli oggetti seguenti dalla console di gestione.

    **Warning**  
    Ciò è necessario perché la configurazione tradizionale popola alcuni record nel database che non vengono popolati se si esegue l'installazione in un database già esistente. Eliminare gli oggetti seguenti:

    -   In "gruppi di server", "gruppo server predefinito", eliminare "Application Virtualization Management Server"

    -   In "gruppi di server" eliminare "gruppo server predefinito"

    -   In "criteri provider" Elimina "provider predefinito"



3.  L'amministratore del gruppo amministratori App-V deve quindi creare:

    -   In "criteri provider" creare un nuovo criterio per il provider

    -   Creare un "gruppo di server predefinito"

        **Nota**  
        È necessario creare un gruppo "server predefinito" anche se non verrà usato. Il programma di installazione del server Cerca solo il "gruppo server predefinito" quando si prova ad aggiungere il server.  Se non è presente alcun "gruppo server predefinito", l'installazione non riuscirà. Se si prevede di usare gruppi di server diversi da quelli predefiniti, è sufficiente mantenere il "gruppo di server predefinito" Se si prevede di aggiungere i successivi server di gestione di App-V all'infrastruttura.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## Conclusione


In conclusione, le informazioni contenute in questo documento consentono a un amministratore di collaborare con gli amministratori SQL per sviluppare un percorso di distribuzione che funzioni per le divisioni di sicurezza e amministrative di un'organizzazione. Dopo aver letto il documento e aver testato le attività documentate, è necessario che un amministratore sia pronto per implementare l'infrastruttura App-V in questo tipo di ambiente.









