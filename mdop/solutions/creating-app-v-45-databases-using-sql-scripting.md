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
# <span data-ttu-id="d3cc9-103">Creazione di database App-V 4.5 con script SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-103">Creating App-V 4.5 Databases Using SQL Scripting</span></span>


**<span data-ttu-id="d3cc9-104">Per chi è destinata questa soluzione?</span><span class="sxs-lookup"><span data-stu-id="d3cc9-104">Who is this solution intended for?</span></span>** <span data-ttu-id="d3cc9-105">Professionisti della tecnologia dell'informazione che gestiscono i database di Application Virtualization (App-V) 4,5.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-105">Information technology professionals who manage Application Virtualization (App-V) 4.5 databases.</span></span>

**<span data-ttu-id="d3cc9-106">Come può aiutarti questa guida?</span><span class="sxs-lookup"><span data-stu-id="d3cc9-106">How can this guide help you?</span></span>** <span data-ttu-id="d3cc9-107">Questa soluzione spiega e documenta la procedura per installare Microsoft Application Virtualization Server quando l'installazione dell'amministratore non ha privilegi di "sysadmin" per SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-107">This solution explains and documents the procedure to install the Microsoft Application Virtualization Server when the administrator installing does not have “sysadmin” privileges to the SQL Server.</span></span>

## <span data-ttu-id="d3cc9-108">Panoramica</span><span class="sxs-lookup"><span data-stu-id="d3cc9-108">Overview</span></span>


<span data-ttu-id="d3cc9-109">Una delle sfide dell'installazione di Microsoft Application Virtualization 4,5 (App-V) consiste nel fatto che il programma di installazione presuppone che l'utente che installa le funzionalità del server non sia solo un amministratore del computer locale, ma disponga anche dei privilegi di amministratore di SQL Server che ospitano l'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-109">One of the challenges of installing Microsoft Application Virtualization 4.5 (App-V) is that the install program assumes that the user installing the server features will not only be a local computer administrator, but also have SQL administrator privileges on the SQL server that will host the Data Store.</span></span> <span data-ttu-id="d3cc9-110">Questo requisito si basa sul fatto che il database, nonché i ruoli e le autorizzazioni appropriati, vengono creati come parte dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-110">This requirement is based on the fact that the database, as well as the appropriate roles and permissions, are created as part of the install.</span></span> <span data-ttu-id="d3cc9-111">Tuttavia, nella maggior parte delle aziende, i server SQL vengono gestiti separatamente dal team dell'infrastruttura che installerà App-V.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-111">However, in most enterprises, SQL servers are managed separately from the infrastructure team who will be installing App-V.</span></span> <span data-ttu-id="d3cc9-112">Questi requisiti di sicurezza renderanno difficile ottenere agli amministratori SQL l'obbligo per l'amministratore dell'infrastruttura di installare App-V diritti adeguati; allo stesso modo, gli amministratori SQL non avranno i privilegi necessari per installare il prodotto per il team dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-112">These security requirements will make it difficult to get SQL administrators to give the infrastructure administrator installing App-V adequate rights; similarly, the SQL administrators will not have the required privileges to install the product for the infrastructure team.</span></span>

<span data-ttu-id="d3cc9-113">Attualmente, un amministratore che prova l'installazione di App-V deve avere privilegi di SQL "sysadmin".</span><span class="sxs-lookup"><span data-stu-id="d3cc9-113">Currently, an administrator attempting the installation of App-V must have SQL “sysadmin” privileges.</span></span> <span data-ttu-id="d3cc9-114">Nelle versioni precedenti del prodotto la configurazione consentiva agli amministratori SQL di creare un account "sysadmin" temporaneo o di essere presente durante l'installazione per fornire le credenziali con i privilegi di "sysadmin".</span><span class="sxs-lookup"><span data-stu-id="d3cc9-114">In previous versions of the product the setup allowed for the SQL administrators to either create a temporary “sysadmin” account or be present during installation to provide credentials with “sysadmin” privileges.</span></span> <span data-ttu-id="d3cc9-115">In questa versione gli script vengono forniti nel prodotto rilasciato per tutti gli amministratori da usare per l'implementazione dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-115">In this release, scripts are provided in the released product for all administrators to use when implementing their infrastructure.</span></span>

<span data-ttu-id="d3cc9-116">Questo whitepaper illustra lo scenario in cui l'installazione dovrà essere divisa in due attività separate: creazione del database SQL e installazione delle funzionalità di App-V Server.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-116">This whitepaper discusses the scenario in which the install will need to be divided into two separate tasks: creating the SQL database, and installing the App-V server features.</span></span> <span data-ttu-id="d3cc9-117">Gli amministratori di SQL sarebbero in grado di esaminare gli script SQL e apportare modifiche per risolvere eventuali conflitti con altri database o per supportare l'integrazione con altri strumenti.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-117">The SQL administrators would be able to review the SQL scripts and make modifications to resolve any conflicts with other databases, or to support integration with other tools.</span></span> <span data-ttu-id="d3cc9-118">Il risultato degli script è consentire agli amministratori SQL di preparare il database in modo che gli amministratori dell'infrastruttura non debbano concedere diritti avanzati a SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-118">The result of the scripts is to allow SQL administrators to prepare the database so that the infrastructure administrators do not have to be granted any advanced rights on the SQL server.</span></span> <span data-ttu-id="d3cc9-119">Questo è importante in ambienti in cui i criteri di sicurezza lo vieteranno.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-119">This is important in environments where security policies would prohibit this.</span></span>

### <span data-ttu-id="d3cc9-120">Processo di creazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-120">SQL Database Creation Process</span></span>

<span data-ttu-id="d3cc9-121">Gli script SQL consentono agli amministratori SQL di creare il database richiesto e di configurare i privilegi per gli amministratori di App-V per installare e gestire correttamente l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-121">The SQL scripts allow for SQL administrators to create the required database and also set up the privileges for the App-V administrators to successfully install and manage the environment.</span></span> <span data-ttu-id="d3cc9-122">I passaggi per il completamento di queste attività sono elencati più avanti in questo documento.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-122">The steps for completing these tasks are listed later in this document.</span></span>

<span data-ttu-id="d3cc9-123">Questo processo separa le azioni di creazione e configurazione del database dall'installazione effettiva di App-V.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-123">This process separates the database creation and configuration actions from the actual App-V installation.</span></span>

**<span data-ttu-id="d3cc9-124">Informazioni da fornire agli amministratori SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-124">Information to be provided to SQL administrators</span></span>**

-   <span data-ttu-id="d3cc9-125">Nome del gruppo di annunci che sarà l'amministratore dell'App-V</span><span class="sxs-lookup"><span data-stu-id="d3cc9-125">Name of AD group that is going to be the App-V admin’s</span></span>

-   <span data-ttu-id="d3cc9-126">Nome del server in cui verrà installato App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="d3cc9-126">Name of the server where App-V Management Server will be installed</span></span>

**<span data-ttu-id="d3cc9-127">Informazioni da restituire agli amministratori dell'infrastruttura</span><span class="sxs-lookup"><span data-stu-id="d3cc9-127">Information to be returned to the Infrastructure administrators</span></span>**

-   <span data-ttu-id="d3cc9-128">Nome del server di database o dell'istanza e il nome del database App-V</span><span class="sxs-lookup"><span data-stu-id="d3cc9-128">Name of the database server or instance and the name of the App-V database</span></span>

<span data-ttu-id="d3cc9-129">Dopo aver preparato il database, gli amministratori di App-V possono eseguire l'installazione di App-V senza privilegi di amministratore SQL.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-129">Once the database has been prepared, the App-V administrators can run the App-V installation without SQL administrator privileges.</span></span>

### <span data-ttu-id="d3cc9-130">Uso degli script di configurazione SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-130">Using the SQL Setup Scripts</span></span>

**<span data-ttu-id="d3cc9-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3cc9-131">Requirements</span></span>**

<span data-ttu-id="d3cc9-132">Di seguito è riportato un elenco di requisiti per l'uso degli script che si trovano nella cartella support\\createdb nella radice della posizione di estrazione selezionata.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-132">The following is a list of requirements for using the scripts which are located in the support\\createdb folder at the root of the selected extract location.</span></span>

-   <span data-ttu-id="d3cc9-133">Gli script devono essere copiati in una posizione scrivibile nel computer in cui verranno eseguiti (assicurarsi di rimuovere l'attributo di sola lettura da questi script dopo la copia) e gli strumenti client SQL devono essere caricati nel computer (osql è necessario solo per l'esecuzione dei file batch di esempio nel computer locale).</span><span class="sxs-lookup"><span data-stu-id="d3cc9-133">Scripts must be copied to a writeable location on the computer where they will be run (be sure to remove the read only attribute from these scripts after they have been copied) and SQL client tools must be loaded on that computer (osql is only required for running the sample batch files on the local computer).</span></span>

-   <span data-ttu-id="d3cc9-134">SQL Server deve supportare l'autenticazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-134">The SQL Server must support Windows Authentication.</span></span>

-   <span data-ttu-id="d3cc9-135">Verificare che l'istanza di SQL Server e il servizio agente SQL siano in uso.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-135">Ensure that the SQL Server Instance and SQL Agent Service are running.</span></span>

-   <span data-ttu-id="d3cc9-136">Accedere con un account di dominio che è un amministratore SQL (sysadmin) nel computer in cui verranno eseguiti gli script.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-136">Log on with a domain account that is a SQL administrator (sysadmin) on the computer where the scripts will be done.</span></span>

<span data-ttu-id="d3cc9-137">Gli script vengono eseguiti sotto le credenziali di dominio dell'utente connesso.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-137">The scripts runs under the logged-on user’s domain credentials.</span></span>

**<span data-ttu-id="d3cc9-138">Creazione di database con script SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-138">Database Creation Using SQL Scripts</span></span>**

**<span data-ttu-id="d3cc9-139">Attività che devono essere eseguite dagli amministratori di SQL:</span><span class="sxs-lookup"><span data-stu-id="d3cc9-139">Tasks to be performed by SQL administrators:</span></span>**

1.  <span data-ttu-id="d3cc9-140">Copiare gli script contenuti nella cartella support\\createdb dalla radice della posizione di estrazione selezionata al computer in cui verranno eseguiti gli script.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-140">Copy the scripts contained in the support\\createdb folder from the root of the selected extract location to the computer where the scripts will be run.</span></span> <span data-ttu-id="d3cc9-141">I file seguenti sono obbligatori per l'esecuzione corretta degli script e devono essere chiamati nell'ordine presentato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-141">The following files are required for the scripts to run properly and must be called in the order presented below.</span></span>

    -   <span data-ttu-id="d3cc9-142">database. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-142">database.sql</span></span>

    -   <span data-ttu-id="d3cc9-143">Roles. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-143">roles.sql</span></span>

    -   <span data-ttu-id="d3cc9-144">tabella \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-144">table\_CODES.sql</span></span>

    -   <span data-ttu-id="d3cc9-145">funzioni \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-145">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="d3cc9-146">Tables. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-146">tables.sql</span></span>

    -   <span data-ttu-id="d3cc9-147">functions. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-147">functions.sql</span></span>

    -   <span data-ttu-id="d3cc9-148">views. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-148">views.sql</span></span>

    -   <span data-ttu-id="d3cc9-149">procedure. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-149">procedures.sql</span></span>

    -   <span data-ttu-id="d3cc9-150">Triggers. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-150">triggers.sql</span></span>

    -   <span data-ttu-id="d3cc9-151">dati \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-151">data\_codes.sql</span></span>

    -   <span data-ttu-id="d3cc9-152">dati \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-152">data\_messages.sql</span></span>

    -   <span data-ttu-id="d3cc9-153">dati \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-153">data\_defaults.sql</span></span>

    -   <span data-ttu-id="d3cc9-154">avvisi \ _jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-154">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="d3cc9-155">DBVERSION. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-155">dbversion.sql</span></span>

2.  <span data-ttu-id="d3cc9-156">Rivedere e modificare, se necessario, il `database.sql` file.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-156">Review and modify, if necessary, the `database.sql` file.</span></span> <span data-ttu-id="d3cc9-157">Le impostazioni predefinite denominano il database "APPVIRTDB".</span><span class="sxs-lookup"><span data-stu-id="d3cc9-157">The default settings will name the database “APPVIRTDB.”</span></span>

    -   <span data-ttu-id="d3cc9-158">Se necessario, Sostituisci `APPVIRTDB` le istanze con il `database name` che verrà usato.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-158">If necessary replace instances of `APPVIRTDB` with the `database name` that will be used.</span></span>

    -   <span data-ttu-id="d3cc9-159">Modificare la `FILENAME` proprietà nello script con il percorso appropriato per SQL Server in cui verrà creato il database.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-159">Modify the `FILENAME` property in the script with the appropriate path for the SQL Server where the database will be created.</span></span>

3.  <span data-ttu-id="d3cc9-160">Rivedere e modificare, se necessario, `database name [APPVIRTDB]` nel `roles.sql` file usato nel file database. SQL.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-160">Review and modify, if necessary, the `database name [APPVIRTDB]` in the `roles.sql` file that was used in the database.sql file.</span></span>

****

### <span data-ttu-id="d3cc9-161">Esempio di come automatizzare il processo con i file batch</span><span class="sxs-lookup"><span data-stu-id="d3cc9-161">Example of how to automate the process using batch files</span></span>

<span data-ttu-id="d3cc9-162">Se usato, i due file batch di esempio forniti eseguono gli script SQL nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="d3cc9-162">If used, the two sample batch files provided run the SQL scripts in the following manner:</span></span>

1.  **<span data-ttu-id="d3cc9-163">Create\_schema.bat (1)</span><span class="sxs-lookup"><span data-stu-id="d3cc9-163">Create\_schema.bat (1)</span></span>**

    -   <span data-ttu-id="d3cc9-164">database. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-164">database.sql</span></span>

    -   <span data-ttu-id="d3cc9-165">Roles. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-165">roles.sql</span></span>

2.  **<span data-ttu-id="d3cc9-166">Create\_tables.bat (2)</span><span class="sxs-lookup"><span data-stu-id="d3cc9-166">Create\_tables.bat (2)</span></span>**

    -   <span data-ttu-id="d3cc9-167">tabella \ _CODES. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-167">table\_CODES.sql</span></span>

    -   <span data-ttu-id="d3cc9-168">funzioni \ _before \ _tables. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-168">functions\_before\_tables.sql</span></span>

    -   <span data-ttu-id="d3cc9-169">Tables. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-169">tables.sql</span></span>

    -   <span data-ttu-id="d3cc9-170">functions. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-170">functions.sql</span></span>

    -   <span data-ttu-id="d3cc9-171">views. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-171">views.sql</span></span>

    -   <span data-ttu-id="d3cc9-172">procedure. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-172">procedures.sql</span></span>

    -   <span data-ttu-id="d3cc9-173">Triggers. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-173">triggers.sql</span></span>

    -   <span data-ttu-id="d3cc9-174">dati \ _codes. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-174">data\_codes.sql</span></span>

    -   <span data-ttu-id="d3cc9-175">dati \ _messages. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-175">data\_messages.sql</span></span>

    -   <span data-ttu-id="d3cc9-176">dati \ _defaults. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-176">data\_defaults.sql</span></span>

    -   <span data-ttu-id="d3cc9-177">avvisi \ _jobs. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-177">alerts\_jobs.sql</span></span>

    -   <span data-ttu-id="d3cc9-178">DBVERSION. SQL</span><span class="sxs-lookup"><span data-stu-id="d3cc9-178">dbversion.sql</span></span>

**<span data-ttu-id="d3cc9-179">Nota</span><span class="sxs-lookup"><span data-stu-id="d3cc9-179">Note</span></span>**  
<span data-ttu-id="d3cc9-180">Una considerazione accurata quando si modificano gli script deve essere eseguita solo da un utente con le informazioni appropriate.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-180">Careful consideration when modifying the scripts must be taken and should only be done by someone with the appropriate knowledge.</span></span> <span data-ttu-id="d3cc9-181">Inoltre, per i file di esempio presentati è necessario modificare solo le operazioni seguenti: **create\_schema.bat**, **create\_tables.bat**, **database. SQL**e **Roles. SQL**.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-181">Also, of the sample files presented only the following should be changed: **create\_schema.bat**, **create\_tables.bat**, **database.sql**, and **roles.sql**.</span></span> <span data-ttu-id="d3cc9-182">Tutti gli altri file non devono essere modificati in alcun modo perché questo potrebbe causare la creazione non corretta del database, che consentirà di installare l'errore dei servizi App-V.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-182">All other files should not be modified in any way as this could cause the database to be created incorrectly, which will lead to the failure of App-V services to be installed.</span></span>



<span data-ttu-id="d3cc9-183">I due file batch di esempio devono essere posizionati nella stessa directory in cui sono stati copiati tutti gli altri script SQL nel computer.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-183">The two sample batch files must be placed in the same directory where the rest of the SQL scripts were copied to on the computer.</span></span>

1.  <span data-ttu-id="d3cc9-184">Eseguire il file di esempio **create\_schema.bat** per creare il database.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-184">Run the sample **create\_schema.bat** file to create the database.</span></span> <span data-ttu-id="d3cc9-185">Questo script impiegano diversi secondi per completare l'operazione e non devono essere interrotti.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-185">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="d3cc9-186">Eseguire il file crea schema.bat dalla directory in cui è stato copiato.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-186">Run the create schema.bat file from the directory where it was copied to.</span></span> <span data-ttu-id="d3cc9-187">La sintassi è: "Create\_schema.bat `SQLSERVERNAME` "</span><span class="sxs-lookup"><span data-stu-id="d3cc9-187">Syntax is: “Create\_schema.bat `SQLSERVERNAME`”</span></span>

        ![AppV46SQLcreatebat](images/appv46sqlcreatebat.bmp)

    -   <span data-ttu-id="d3cc9-189">Se questo script non riesce durante la creazione del nuovo database "APPVIRTDB", selezionare il log come indicato per correggere il problema.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-189">If this script fails during the creation of the new “APPVIRTDB” database, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="d3cc9-190">Sarà necessario eliminare il database creato con un parziale funzionamento degli script, in modo da assicurarti che i successivi tentativi funzionino correttamente.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-190">It will be necessary to delete the database that was created with a partial running of the scripts in order to ensure that subsequent attempts will work properly.</span></span>

2.  <span data-ttu-id="d3cc9-191">Eseguire il `create_tables.bat` file per creare le tabelle nel database.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-191">Run the `create_tables.bat` file to create the tables in the database.</span></span> <span data-ttu-id="d3cc9-192">Questo script impiegano diversi secondi per completare l'operazione e non devono essere interrotti.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-192">This script will take several seconds to complete and should not be interrupted.</span></span>

    -   <span data-ttu-id="d3cc9-193">Eseguire il file create\_tables.bat dalla directory in cui è stato copiato.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-193">Run the create\_tables.bat file from the directory where it was copied.</span></span> <span data-ttu-id="d3cc9-194">La sintassi è: "create\_tables.bat `SQLSERVERNAME DBNAME` "</span><span class="sxs-lookup"><span data-stu-id="d3cc9-194">Syntax is: “create\_tables.bat `SQLSERVERNAME DBNAME`”</span></span>

        ![App-v 4,6 SQL create\-table.bat](images/appv46sqlcreate-tablebat.gif)

        <span data-ttu-id="d3cc9-196">Se lo script non riesce durante la creazione delle tabelle, selezionare il log come indicato per correggere il problema.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-196">If the script fails during the creation of the tables, check the log as indicated to correct the issue.</span></span> <span data-ttu-id="d3cc9-197">Sarà necessario eliminare il database ed eseguire create\_schema.bat prima di provare a eseguire il file di create\_tables.bat in tutti i tentativi successivi.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-197">It will be necessary to delete the database and run create\_schema.bat before attempting to run the create\_tables.bat file on all subsequent attempts.</span></span>

### <span data-ttu-id="d3cc9-198">Impostazione delle autorizzazioni per il database App-V</span><span class="sxs-lookup"><span data-stu-id="d3cc9-198">Setting permissions on the App-V database</span></span>

<span data-ttu-id="d3cc9-199">Gli account seguenti dovranno essere creati in SQL Server con autorizzazioni e ruoli specifici per il nuovo database per l'installazione, la distribuzione e l'amministrazione continua dell'ambiente App-V.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-199">The following accounts will need to be created on the SQL server with specific permissions and roles to the new database for the installation, deployment and ongoing administration of the App-V environment.</span></span>

-   <span data-ttu-id="d3cc9-200">Creare un account di accesso per il gruppo amministratori App-V in SQL Server e il database APPVIRTDB per gli amministratori di domain\\App-V (dove "Domain" e "App-V Admins" verranno modificati per riflettere il proprio ambiente) e aggiungerli al ruolo del database SFTAdmin e SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-200">Create a login for the App-V administrators group on the SQL Server and the APPVIRTDB database for the “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment) and add them to the SFTAdmin and SFTEveryone database role.</span></span>

    ![App-v 4,6 script SQL impostare le autorizzazioni e i ruoli](images/appv46sqlscriptsetpermsroles.gif)

-   <span data-ttu-id="d3cc9-202">Concedere a questo gruppo l'autorizzazione "Visualizza qualsiasi definizione" a livello globale (questo consente al processo di configurazione del server di gestione di Microsoft Application Virtualization Management di verificare che l'accesso al server di gestione esista già).</span><span class="sxs-lookup"><span data-stu-id="d3cc9-202">Grant this group “VIEW ANY DEFINITION” permission at the global level (This allows the Microsoft Application Virtualization Management Server setup process to verify that the Management Server login already exists).</span></span> <span data-ttu-id="d3cc9-203">In MS-SQL 2005 e sopra le restrizioni di accesso ai metadati contenuti in master. DB sono stati aggiunti.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-203">Under MS-SQL 2005 and above access restrictions to the metadata contained in master.db were added.</span></span> <span data-ttu-id="d3cc9-204">L'utente creato nel passaggio precedente non avrà per impostazione predefinita i diritti necessari per l'installazione del server.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-204">The user created in the previous step will by default not have the rights needed by the server installation.</span></span> <span data-ttu-id="d3cc9-205">Aprire le proprietà dell'account di accesso creato in precedenza, proprietà di login- &gt; entità a protezione diretta.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-205">Open the properties of the previously created login, Login Properties-&gt;Securables.</span></span> <span data-ttu-id="d3cc9-206">Aggiungere l'istanza del database e abilitare "GRANT" per "Visualizza qualsiasi definizione", come illustrato nella schermata seguente.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-206">Add the Database instance and enable “GRANT” for “View any definition” as shown in the screenshot below.</span></span>

    ![App-v 4,6 SQL script Grant Perm per la visualizzazione di qualsiasi def](images/appv46sqlscriptviewanydef.gif)

-   <span data-ttu-id="d3cc9-208">Aggiungere un ruolo alla tabella ROLE \ _ASSIGNMENTS per l'account di accesso creato nel passaggio precedente per consentire agli amministratori di App-V di accedere alla console di gestione di Application Virtualization, con role = "ADMIN" e Group \ _ref = "domain\\App-V Admins" (dove "Domain" e "App-V Admins" verranno modificati per riflettere il proprio ambiente).</span><span class="sxs-lookup"><span data-stu-id="d3cc9-208">Add a role to the ROLE\_ASSIGNMENTS table for the login created in the previous step to allow App-V administrators access to the Application Virtualization Management Console, with role = “ADMIN” and group\_ref = “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

    ![assegnazione di ruoli di script SQL di App-v 4,6](images/appv46sqlscriptroleassign.gif)

-   <span data-ttu-id="d3cc9-210">Creare un account di accesso per SQL Server e un database App-V per il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-210">Create login for SQL Server and App-V database for the Management Server.</span></span> <span data-ttu-id="d3cc9-211">Questo account viene usato da Microsoft Application Virtualization Management Server per connettersi all'archivio dati ed è responsabile della manutenzione delle richieste client per le applicazioni in streaming.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-211">This account is used by the Microsoft Application Virtualization Management Server to connect to the data store and is responsible for servicing client requests for streamed applications.</span></span> <span data-ttu-id="d3cc9-212">A seconda della posizione in cui devono essere installati il server SQL e il server di gestione, sono disponibili due opzioni:</span><span class="sxs-lookup"><span data-stu-id="d3cc9-212">There are two options, depending on where the SQL Server and Management Server are to be installed:</span></span>

    1.  <span data-ttu-id="d3cc9-213">Se server di gestione e SQL Server verranno installati nello stesso computer, aggiungere un account di accesso per NT AUTHORITY\\NETWORK SERVICE e aggiungerlo ai ruoli di database di SFTUser e SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-213">If Management Server and SQL Server are going to be installed on the same computer, add a login for NT AUTHORITY\\NETWORK SERVICE and add it to the SFTUser and SFTEveryone database roles.</span></span>

    2.  <span data-ttu-id="d3cc9-214">Se il server di gestione e SQL Server devono essere installati in computer diversi, aggiungere un account di accesso per "domain\\App-V Server Name $" (dove "App-V Server Name" è il nome del server in cui verrà installato l'App-V Management Server) e aggiungerlo ai ruoli di database di SFTUser e SFTEveryone.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-214">If the Management Server and SQL Server are to be installed on different computers, add a login for “domain\\App-V Server Name$” (where “App-V Server Name” is the name of the server where the App-V Management Server will be installed) and add it to the SFTUser and SFTEveryone database roles.</span></span>

-   <span data-ttu-id="d3cc9-215">Aprire la finestra della query nella finestra SQL ed eseguire il codice SQL seguente:</span><span class="sxs-lookup"><span data-stu-id="d3cc9-215">Open the query window on the SQL window and run the following SQL:</span></span>

    ``` syntax
    USE APPVIRTDB
    GRANT ALTER ON ROLE::SFTuser TO “domain\App-V Admins”
    ```

    <span data-ttu-id="d3cc9-216">Dove APPVIRTDB è il nome del database App-V creato in SQL Server nel passaggio precedente e l'utente che sta per eseguire l'installazione di App-v server deve essere un membro di "domain\\App-V Admins" (dove "Domain" e "App-V Admins" verranno modificati per riflettere il proprio ambiente).</span><span class="sxs-lookup"><span data-stu-id="d3cc9-216">Where the APPVIRTDB is the name of the App-V Database created on the SQL Server in the previous step, and the user who is going to do the install of the App-v server needs to be a member of “domain\\App-V Admins” (where “domain” and “App-V Admins” will be changed to reflect your own environment).</span></span>

### <span data-ttu-id="d3cc9-217">Attività che devono essere eseguite dagli amministratori dell'infrastruttura</span><span class="sxs-lookup"><span data-stu-id="d3cc9-217">Tasks to be performed by the Infrastructure administrators</span></span>

1.  <span data-ttu-id="d3cc9-218">L'amministratore del gruppo "App-V Admins" dovrebbe installare App-V.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-218">Administrator in the “App-V Admins” group should install App-V.</span></span>

    <span data-ttu-id="d3cc9-219">Usare le informazioni degli amministratori di SQL per selezionare SQL Server e il database creato nei passaggi precedenti.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-219">Use information from the SQL administrators for selecting the SQL Server and database created in the previous steps.</span></span>

2.  <span data-ttu-id="d3cc9-220">L'amministratore del gruppo "App-V Admins" accede a Application Virtualization Management Console ed Elimina gli oggetti seguenti dalla console di gestione.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-220">Administrator in the “App-V Admins” group logs in to Application Virtualization Management Console and deletes the following objects from the Management Console.</span></span>

    **<span data-ttu-id="d3cc9-221">Warning</span><span class="sxs-lookup"><span data-stu-id="d3cc9-221">Warning</span></span>**  
    <span data-ttu-id="d3cc9-222">Ciò è necessario perché la configurazione tradizionale popola alcuni record nel database che non vengono popolati se si esegue l'installazione in un database già esistente.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-222">This is required as the traditional setup populates certain records in the database that are not populated if you run the install against an already existing database.</span></span> <span data-ttu-id="d3cc9-223">Eliminare gli oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="d3cc9-223">Delete the following objects:</span></span>

    -   <span data-ttu-id="d3cc9-224">In "gruppi di server", "gruppo server predefinito", eliminare "Application Virtualization Management Server"</span><span class="sxs-lookup"><span data-stu-id="d3cc9-224">Under “Server Groups,” “Default Server Group,” delete “Application Virtualization Management Server”</span></span>

    -   <span data-ttu-id="d3cc9-225">In "gruppi di server" eliminare "gruppo server predefinito"</span><span class="sxs-lookup"><span data-stu-id="d3cc9-225">Under “Server Groups,” delete “Default Server Group”</span></span>

    -   <span data-ttu-id="d3cc9-226">In "criteri provider" Elimina "provider predefinito"</span><span class="sxs-lookup"><span data-stu-id="d3cc9-226">Under “Provider Policies,” delete “Default Provider”</span></span>



3.  <span data-ttu-id="d3cc9-227">L'amministratore del gruppo amministratori App-V deve quindi creare:</span><span class="sxs-lookup"><span data-stu-id="d3cc9-227">Administrator in the App-V admins group should then create:</span></span>

    -   <span data-ttu-id="d3cc9-228">In "criteri provider" creare un nuovo criterio per il provider</span><span class="sxs-lookup"><span data-stu-id="d3cc9-228">Under “Provider Policies,” create a New Provider Policy</span></span>

    -   <span data-ttu-id="d3cc9-229">Creare un "gruppo di server predefinito"</span><span class="sxs-lookup"><span data-stu-id="d3cc9-229">Create a “Default Server Group”</span></span>

        **<span data-ttu-id="d3cc9-230">Nota</span><span class="sxs-lookup"><span data-stu-id="d3cc9-230">Note</span></span>**  
        <span data-ttu-id="d3cc9-231">È necessario creare un gruppo "server predefinito" anche se non verrà usato.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-231">You must create a “Default Server” group even if you will not be used.</span></span> <span data-ttu-id="d3cc9-232">Il programma di installazione del server Cerca solo il "gruppo server predefinito" quando si prova ad aggiungere il server.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-232">The server installer only looks for the "Default Server Group" when trying to add the server.</span></span>  <span data-ttu-id="d3cc9-233">Se non è presente alcun "gruppo server predefinito", l'installazione non riuscirà.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-233">If there is no "Default Server Group" then the installation will fail.</span></span> <span data-ttu-id="d3cc9-234">Se si prevede di usare gruppi di server diversi da quelli predefiniti, è sufficiente mantenere il "gruppo di server predefinito" Se si prevede di aggiungere i successivi server di gestione di App-V all'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-234">If you plan on using server groups other than the default that is fine, it’s just necessary to retain the "Default Server Group" if you plan on adding subsequent App-V Management Servers to your infrastructure.</span></span>



~~~
-   Assign the App-V Users Group to the New Provider Policy created above

-   Under “Server Groups,” create a New Server Group, specifying the New Provider Policy

-   Under the New Server group, create a New Application Virtualization Management Server

    **Important**  
    Do not restart the service before completing all of the above steps!



-   Administrator restarts the Application Virtualization Management Server service.
~~~

## <span data-ttu-id="d3cc9-235">Conclusione</span><span class="sxs-lookup"><span data-stu-id="d3cc9-235">Conclusion</span></span>


<span data-ttu-id="d3cc9-236">In conclusione, le informazioni contenute in questo documento consentono a un amministratore di collaborare con gli amministratori SQL per sviluppare un percorso di distribuzione che funzioni per le divisioni di sicurezza e amministrative di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-236">In conclusion, the information in this document allows an administrator to work with the SQL administrators to develop a deployment path that works for the security and administrative divisions in an organization.</span></span> <span data-ttu-id="d3cc9-237">Dopo aver letto il documento e aver testato le attività documentate, è necessario che un amministratore sia pronto per implementare l'infrastruttura App-V in questo tipo di ambiente.</span><span class="sxs-lookup"><span data-stu-id="d3cc9-237">After reading this document and testing the tasks documented, an administrator should be ready to implement their App-V infrastructure in this type of environment.</span></span>









