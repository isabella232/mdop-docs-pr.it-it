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
ms.openlocfilehash: c119f1d43a70cce04dd6151697318f7cf6a8d1f2
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910591"
---
# <a name="creating-app-v-45-databases-using-sql-scripting"></a>Creazione di database App-V 4.5 con script SQL


**Who è destinata a questa soluzione?** Professionisti dell'information technology che gestiscono i database di Application Virtualization (App-V) 4.5.

**Come può essere utile questa guida?** Questa soluzione illustra e documenta la procedura per installare Microsoft Application Virtualization Server quando l'amministratore che esegue l'installazione non dispone dei privilegi "sysadmin" per l'SQL Server.

## <a name="overview"></a>Panoramica


Una delle sfide dell'installazione di Microsoft Application Virtualization 4.5 (App-V) è che il programma di installazione presuppone che l'utente che installa le funzionalità del server non sarà solo un amministratore del computer locale, ma avrà anche privilegi di amministratore di SQL sul server SQL che ospiterà l'archivio dati. Questo requisito si basa sul fatto che il database, nonché i ruoli e le autorizzazioni appropriati, vengono creati come parte dell'installazione. Tuttavia, nella maggior parte delle SQL i server vengono gestiti separatamente dal team dell'infrastruttura che installerà App-V. Questi requisiti di sicurezza renderanno difficile ottenere agli amministratori SQL di concedere all'amministratore dell'infrastruttura l'installazione di App-V diritti adeguati; analogamente, gli amministratori SQL non avranno i privilegi necessari per installare il prodotto per il team dell'infrastruttura.

Attualmente, un amministratore che tenta l'installazione di App-V deve disporre SQL privilegi "sysadmin". Nelle versioni precedenti del prodotto l'installazione consentiva agli amministratori di SQL di creare un account "sysadmin" temporaneo o di essere presenti durante l'installazione per fornire le credenziali con privilegi "sysadmin". In questa versione, gli script vengono forniti nel prodotto rilasciato da tutti gli amministratori per l'implementazione dell'infrastruttura.

In questo white paper viene illustrato lo scenario in cui l'installazione dovrà essere suddivisa in due attività distinte: la creazione del database di SQL e l'installazione delle funzionalità del server App-V. Gli SQL possono esaminare gli script di SQL e apportare modifiche per risolvere eventuali conflitti con altri database o per supportare l'integrazione con altri strumenti. Il risultato degli script è consentire agli amministratori SQL di preparare il database in modo che agli amministratori dell'infrastruttura non sia necessario concedere diritti avanzati sul server SQL. Questo è importante negli ambienti in cui i criteri di sicurezza lo proibiscono.

### <a name="sql-database-creation-process"></a>database SQL Processo di creazione

Gli SQL consentono agli amministratori SQL di creare il database necessario e di impostare i privilegi per gli amministratori di App-V per installare e gestire correttamente l'ambiente. I passaggi per il completamento di queste attività sono elencati più avanti in questo documento.

Questo processo separa le azioni di creazione e configurazione del database dall'installazione effettiva di App-V.

**Informazioni da SQL amministratori**

-   Nome del gruppo di Active Directory che sarà l'amministratore di App-V

-   Nome del server in cui verrà installato il server di gestione di App-V

**Informazioni da restituire agli amministratori dell'infrastruttura**

-   Nome del server o dell'istanza di database e nome del database App-V

Dopo aver preparato il database, gli amministratori di App-V possono eseguire l'installazione di App-V senza SQL privilegi di amministratore.

### <a name="using-the-sql-setup-scripts"></a>Utilizzo degli SQL di installazione

**Requisiti**

Di seguito è riportato un elenco dei requisiti per l'utilizzo degli script che si trovano nella cartella support\\createdb nella radice del percorso di estrazione selezionato.

-   Gli script devono essere copiati in un percorso scrivibile nel computer in cui verranno eseguiti (assicurarsi di rimuovere l'attributo di sola lettura da questi script dopo che sono stati copiati) e gli strumenti client di SQL devono essere caricati nel computer (osql è necessario solo per l'esecuzione dei file batch di esempio nel computer locale).

-   Il SQL Server deve supportare l'Windows autenticazione.

-   Verificare che il servizio SQL Server e SQL Agent siano in esecuzione.

-   Eseguire l'accesso con un account di dominio SQL amministratore di sistema (sysadmin) nel computer in cui verranno eseguiti gli script.

Gli script vengono eseguiti con le credenziali di dominio dell'utente connesso.

**Creazione di database tramite SQL script**

**Attività da eseguire dagli SQL amministratori:**

1.  Copiare gli script contenuti nella cartella support\\createdb dalla radice del percorso di estrazione selezionato nel computer in cui verranno eseguiti gli script. I file seguenti sono necessari per la corretta esecuzione degli script e devono essere chiamati nell'ordine indicato di seguito.

    -   database.sql

    -   roles.sql

    -   table\_CODES.sql

    -   functions\_before\_tables.sql

    -   tables.sql

    -   functions.sql

    -   views.sql

    -   procedures.sql

    -   triggers.sql

    -   data\_codes.sql

    -   data\_messages.sql

    -   data\_defaults.sql

    -   alerts\_jobs.sql

    -   dbversion.sql

2.  Esaminare e modificare, se necessario, il `database.sql` file. Le impostazioni predefinite denoeranno il database "APPVIRTDB".

    -   Se necessario, sostituire `APPVIRTDB` le istanze di con quella che verrà `database name` utilizzata.

    -   Modificare la proprietà nello script con il percorso appropriato per il SQL Server `FILENAME` in cui verrà creato il database.

3.  Esaminare e modificare, se necessario, il contenuto del `database name [APPVIRTDB]` file utilizzato nel file `roles.sql` database.sql.

****

### <a name="example-of-how-to-automate-the-process-using-batch-files"></a>Esempio di come automatizzare il processo utilizzando file batch

Se utilizzati, i due file batch di esempio forniti eseguono SQL script nel modo seguente:

1.  **Create\_schema.bat (1)**

    -   database.sql

    -   roles.sql

2.  **Create\_tables.bat (2)**

    -   table\_CODES.sql

    -   functions\_before\_tables.sql

    -   tables.sql

    -   functions.sql

    -   views.sql

    -   procedures.sql

    -   triggers.sql

    -   data\_codes.sql

    -   data\_messages.sql

    -   data\_defaults.sql

    -   alerts\_jobs.sql

    -   dbversion.sql

**Nota**  
È necessario prestare particolare attenzione quando si modificano gli script e devono essere eseguiti solo da persone con le conoscenze appropriate. Inoltre, dei file di esempio presentati devono essere modificati solo gli elementi seguenti: **create\_schema.bat**, **create\_tables.bat**, **database.sql**e **roles.sql**. Tutti gli altri file non devono essere modificati in alcun modo in quanto ciò potrebbe causare la creazione non corretta del database, causando l'errore di installazione dei servizi App-V.



I due file batch di esempio devono essere posizionati nella stessa directory in cui sono stati copiati gli altri script SQL nel computer.

1.  Eseguire il file ** dicreate\_schema.bat** di esempio per creare il database. Il completamento dello script potrebbe richiedere alcuni secondi e non deve essere interrotto.

    -   Eseguire il file di schema.bat dalla directory in cui è stato copiato. La sintassi è: `SQLSERVERNAME` "Create\_schema.bat"

        ![AppV46SQLcreatebat.](images/appv46sqlcreatebat.bmp)

    -   Se questo script ha esito negativo durante la creazione del nuovo database "APPVIRTDB", controllare il registro come indicato per correggere il problema. Sarà necessario eliminare il database creato con un'esecuzione parziale degli script per garantire che i tentativi successivi funzionino correttamente.

2.  Eseguire il `create_tables.bat` file per creare le tabelle nel database. Il completamento dello script potrebbe richiedere alcuni secondi e non deve essere interrotto.

    -   Eseguire il create\_tables.bat file dalla directory in cui è stato copiato. La sintassi è: `SQLSERVERNAME DBNAME` "create\_tables.bat"

        ![app-v 4.6 sql create\-table.bat.](images/appv46sqlcreate-tablebat.gif)

        Se lo script ha esito negativo durante la creazione delle tabelle, controllare il registro come indicato per correggere il problema. Sarà necessario eliminare il database ed eseguire create\_schema.bat prima di tentare di eseguire il file create\_tables.bat in tutti i tentativi successivi.

### <a name="setting-permissions-on-the-app-v-database"></a>Impostazione delle autorizzazioni per il database di App-V

Gli account seguenti dovranno essere creati nel server SQL con autorizzazioni e ruoli specifici per il nuovo database per l'installazione, la distribuzione e l'amministrazione continua dell'ambiente App-V.

-   Creare un account di accesso per il gruppo di amministratori di App-V nel SQL Server e nel database APPVIRTDB per "domain\\App-V Admins" (dove "dominio" e "App-V Admins" verranno modificati per riflettere il proprio ambiente) e aggiungerli al ruolo del database SFTAdmin e SFTEveryone.

    ![app-v 4.6 sql script set permissions and roles.](images/appv46sqlscriptsetpermsroles.gif)

-   Concedere a questo gruppo l'autorizzazione "VIEW ANY DEFINITION" a livello globale (in questo modo il processo di installazione di Microsoft Application Virtualization Management Server consente di verificare che l'account di accesso del server di gestione esista già). In MS-SQL 2005 e successive sono state aggiunte restrizioni di accesso ai metadati contenuti in master.db. Per impostazione predefinita, l'utente creato nel passaggio precedente non dispone dei diritti necessari per l'installazione del server. Aprire le proprietà dell'account di accesso creato in precedenza, Proprietà di accesso- &gt; A protezione diretta. Aggiungi l'istanza del database e abilita "GRANT" per "Visualizza qualsiasi definizione", come mostrato nella schermata seguente.

    ![app-v 4.6 sql script grant perm for view any def.](images/appv46sqlscriptviewanydef.gif)

-   Aggiungere un ruolo alla tabella ROLE\_ASSIGNMENTS per l'account di accesso creato nel passaggio precedente per consentire agli amministratori di App-V di accedere a Application Virtualization Management Console, con ruolo = "ADMIN" e group\_ref = "domain\\App-V Admins" (dove "domain" e "App-V Admins" verranno modificati per riflettere il proprio ambiente).

    ![assegnazione del ruolo dello script sql app-v 4.6.](images/appv46sqlscriptroleassign.gif)

-   Creare l'account SQL Server e il database App-V per il server di gestione. Questo account viene utilizzato da Microsoft Application Virtualization Management Server per connettersi all'archivio dati ed è responsabile della manutenzione delle richieste client per le applicazioni in streaming. Esistono due opzioni, a seconda della posizione SQL Server e del server di gestione:

    1.  Se Management Server e SQL Server verranno installati nello stesso computer, aggiungere un account di accesso per NT AUTHORITY\\NETWORK SERVICE e aggiungerlo ai ruoli del database SFTUser e SFTEveryone.

    2.  Se il server di gestione e il SQL Server devono essere installati in computer diversi, aggiungere un account di accesso per "dominio\\Nome server App-V$" (dove "Nome server App-V" è il nome del server in cui verrà installato il server di gestione App-V) e aggiungerlo ai ruoli del database SFTUser e SFTEveryone.

-   Aprire la finestra della query nella finestra SQL ed eseguire le operazioni SQL:

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    Dove APPVIRTDB è il nome del database App-V creato nel SQL Server nel passaggio precedente e l'utente che sta per eseguire l'installazione del server App-v deve essere membro di "domain\\App-V Admins" (dove "dominio" e "App-V Admins" verranno modificati per riflettere il proprio ambiente).

### <a name="tasks-to-be-performed-by-the-infrastructure-administrators"></a>Attività che devono essere eseguite dagli amministratori dell'infrastruttura

1.  L'amministratore nel gruppo "App-V Admins" deve installare App-V.

    Utilizzare le informazioni degli SQL per selezionare il SQL Server e il database creati nei passaggi precedenti.

2.  L'amministratore nel gruppo "App-V Admins" accede a Application Virtualization Management Console ed elimina gli oggetti seguenti dalla console di gestione.

    **Warning**  
    Questa operazione è necessaria perché il programma di installazione tradizionale popola determinati record nel database che non vengono popolati se si esegue l'installazione in un database già esistente. Eliminare gli oggetti seguenti:

    -   In "Gruppi di server", "Gruppo di server predefinito", eliminare "Application Virtualization Management Server"

    -   In "Gruppi di server" eliminare "Gruppo di server predefinito"

    -   In "Criteri provider" eliminare "Provider predefinito"



3.  L'amministratore nel gruppo di amministratori di App-V deve quindi creare:

    -   In "Criteri provider" crea un nuovo criterio provider

    -   Creare un "gruppo di server predefinito"

        **Nota**  
        È necessario creare un gruppo "Server predefinito" anche se non si verrà utilizzati. Il programma di installazione del server cerca solo il "Gruppo di server predefinito" quando tenta di aggiungere il server.  Se non è presente alcun "Gruppo di server predefinito", l'installazione avrà esito negativo. Se si prevede di utilizzare gruppi di server diversi da quelli predefiniti, è sufficiente conservare il "Gruppo di server predefinito" se si prevede di aggiungere i successivi server di gestione App-V all'infrastruttura.



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <a name="conclusion"></a>Conclusione


In conclusione, le informazioni contenute in questo documento consentono a un amministratore di collaborare con gli amministratori di SQL per sviluppare un percorso di distribuzione che funzioni per le divisioni di sicurezza e amministrative di un'organizzazione. Dopo aver letto questo documento e aver testato le attività documentate, un amministratore deve essere pronto per implementare l'infrastruttura App-V in questo tipo di ambiente.









