---
title: Come eseguire la migrazione del database SQL di App-V in un server SQL diverso
description: Come eseguire la migrazione del database SQL di App-V in un server SQL diverso
author: dansimp
ms.assetid: 353892a1-9327-4489-a19c-4ec7bd1b736f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e3d84b0cb328873db3722ad3eb9af6a2b442fdcf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817075"
---
# <span data-ttu-id="ef420-103">Come eseguire la migrazione del database SQL di App-V in un server SQL diverso</span><span class="sxs-lookup"><span data-stu-id="ef420-103">How to Migrate the App-V SQL Database to a Different SQL Server</span></span>


<span data-ttu-id="ef420-104">Le procedure seguenti descrivono in dettaglio come eseguire la migrazione del database SQL del server di gestione di Microsoft Application Virtualization (App-V) a un server SQL diverso.</span><span class="sxs-lookup"><span data-stu-id="ef420-104">The following procedures describe in detail how to migrate the SQL database of the Microsoft Application Virtualization (App-V) Management Server to a different SQL Server.</span></span>

<span data-ttu-id="ef420-105">**Importante**  Questa procedura richiede che il servizio App-V Server venga interrotto e questo impedirà agli utenti finali di usare le proprie applicazioni.</span><span class="sxs-lookup"><span data-stu-id="ef420-105">**Important** This procedure requires that the App-V server service is stopped and this will prevent end-users from using their applications.</span></span>

 

**<span data-ttu-id="ef420-106">Per eseguire il backup del database SQL di App-V</span><span class="sxs-lookup"><span data-stu-id="ef420-106">To back up the App-V SQL database</span></span>**

1.  <span data-ttu-id="ef420-107">Aprire il programma Services. msc e arrestare il servizio App-V Management Server in tutti i server di gestione che usano il database di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="ef420-107">Open the Services.msc program and stop the App-V Management Server service on all Management Servers that use the database to be migrated.</span></span>

2.  <span data-ttu-id="ef420-108">Nel computer in cui si trova il database di App-V aprire SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="ef420-108">On the computer where the App-V database is located, open SQL Server Management Studio.</span></span>

3.  <span data-ttu-id="ef420-109">Espandere il nodo **database** e individuare il database App-V (il nome predefinito è APPVIRT).</span><span class="sxs-lookup"><span data-stu-id="ef420-109">Expand the **Databases** node and locate the App-V database (default name is APPVIRT).</span></span>

4.  <span data-ttu-id="ef420-110">Fare clic con il pulsante destro del mouse sul database e scegliere **attività** e quindi selezionare **backup**.</span><span class="sxs-lookup"><span data-stu-id="ef420-110">Right-click the database and select **Tasks** and then select **Back Up**.</span></span>

5.  <span data-ttu-id="ef420-111">Verificare che il **modello di recupero** sia impostato su **semplice** e che il **tipo di backup** sia impostato su **completo**.</span><span class="sxs-lookup"><span data-stu-id="ef420-111">Verify that **Recovery model** is set to **SIMPLE** and the **Backup type** is set to **Full**.</span></span> <span data-ttu-id="ef420-112">Se necessario, modificare le impostazioni di **set di backup** e di **destinazione** .</span><span class="sxs-lookup"><span data-stu-id="ef420-112">Change the **Backup set** and **Destination** settings if it is necessary.</span></span>

6.  <span data-ttu-id="ef420-113">Fare clic su **OK** per eseguire il backup del database.</span><span class="sxs-lookup"><span data-stu-id="ef420-113">Click **OK** to back up the database.</span></span> <span data-ttu-id="ef420-114">Dopo che il backup è stato completato correttamente, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef420-114">After the backup has completed successfully, click **OK**.</span></span>

7.  <span data-ttu-id="ef420-115">Aprire Esplora risorse e passare alla cartella che contiene il file di backup del database, ad esempio APPVIRT. BAK.</span><span class="sxs-lookup"><span data-stu-id="ef420-115">Open Windows Explorer and browse to the folder that contains the database backup file, for example APPVIRT.BAK.</span></span> <span data-ttu-id="ef420-116">Copiare il file di backup del database nel computer di destinazione in cui è in uso SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ef420-116">Copy the database backup file to the destination computer that is running SQL Server.</span></span>

**<span data-ttu-id="ef420-117">Per ripristinare il database SQL di App-V nel computer di destinazione</span><span class="sxs-lookup"><span data-stu-id="ef420-117">To restore the App-V SQL database to the destination computer</span></span>**

1.  <span data-ttu-id="ef420-118">Nel computer di destinazione aprire SQL Server Management Studio, fare clic con il pulsante destro del mouse sul nodo **database** e scegliere **Ripristina database**.</span><span class="sxs-lookup"><span data-stu-id="ef420-118">On the destination computer, open SQL Server Management Studio, right-click the **Databases** node and select **Restore Database**.</span></span>

2.  <span data-ttu-id="ef420-119">In **origine per ripristino**scegliere **da dispositivo** e quindi fare clic su "**...**"</span><span class="sxs-lookup"><span data-stu-id="ef420-119">Under **Source for Restore**, choose **From device** and then click the “**…**”</span></span> <span data-ttu-id="ef420-120">.</span><span class="sxs-lookup"><span data-stu-id="ef420-120">button.</span></span>

3.  <span data-ttu-id="ef420-121">Nella finestra di dialogo **specifica backup** verificare che il supporto di **backup** sia impostato su **file** e quindi fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="ef420-121">In the **Specify Backup** dialog box, make sure that the **Backup Media** is set to **File** and then click **Add**.</span></span>

4.  <span data-ttu-id="ef420-122">Selezionare il file di backup copiato dal computer originale in cui è in uso SQL Server e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef420-122">Select the backup file that you copied from the original computer that is running SQL Server, and then click **OK**.</span></span>

5.  <span data-ttu-id="ef420-123">Fare clic su **OK** e quindi su per selezionare il set di backup da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="ef420-123">Click **OK** and then click to select the backup set to restore.</span></span>

6.  <span data-ttu-id="ef420-124">In **destinazione per il ripristino**fare clic sull'elenco a discesa per il **database** e selezionare il nome del database App-V, ad esempio APPVIRT.</span><span class="sxs-lookup"><span data-stu-id="ef420-124">Under **Destination for restore**, click the drop-down for **To database** and select the App-V database name, for example APPVIRT.</span></span>

7.  <span data-ttu-id="ef420-125">Fare clic su **OK** per avviare il ripristino.</span><span class="sxs-lookup"><span data-stu-id="ef420-125">Click **OK** to start the restore.</span></span> <span data-ttu-id="ef420-126">Dopo che il ripristino è stato completato correttamente, fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef420-126">After the restore has completed successfully, click **OK**.</span></span>

8.  <span data-ttu-id="ef420-127">Espandere il nodo di **sicurezza** , fare clic con il pulsante destro del mouse su **account di accesso** e scegliere **nuovo accesso**.</span><span class="sxs-lookup"><span data-stu-id="ef420-127">Expand the **Security** node, right-click **Logins** and select **New Login**.</span></span>

9.  <span data-ttu-id="ef420-128">Nel campo **nome login** immettere i dettagli dell'account del servizio di rete per l'App-V Management Server nel formato DOMAIN\\SERVERNAME $.</span><span class="sxs-lookup"><span data-stu-id="ef420-128">In the **Login Name** field, enter the Network Service account details for the App-V Management Server in the format of DOMAIN\\SERVERNAME$.</span></span>

10. <span data-ttu-id="ef420-129">Nella pagina **generale** in **database predefinito** Selezionare il nome del database App-V, ad esempio APPVIRT, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef420-129">On the **General** page under **Default database** select the App-V database name, for example, APPVIRT, and then click **OK**.</span></span>

11. <span data-ttu-id="ef420-130">In **Seleziona una pagina**fare clic su per selezionare la pagina di **mapping utente** .</span><span class="sxs-lookup"><span data-stu-id="ef420-130">Under **Select a page**, click to select the **User Mapping** page.</span></span> <span data-ttu-id="ef420-131">In **utenti mappati a questo account di accesso**fare clic sulla casella di controllo nella colonna **mappa** per selezionare il database App-V.</span><span class="sxs-lookup"><span data-stu-id="ef420-131">Under **Users mapped to this login**, click the check box in the **Map** column to select the App-V database.</span></span>

12. <span data-ttu-id="ef420-132">In \*\*appartenenza a ruoli del database per: &lt; appvdatabasename &gt; \*\*, fare clic per selezionare **SFTEveryone** e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef420-132">Under **Database role membership for: &lt;appvdatabasename&gt;**, click to select **SFTEveryone** and then click **OK**.</span></span>

13. <span data-ttu-id="ef420-133">Assicurarsi che Windows Firewall nel nuovo computer in cui è in corso SQL Server sia configurato per consentire l'accesso al sistema da parte di App-V Management Server.</span><span class="sxs-lookup"><span data-stu-id="ef420-133">Make sure that the Windows Firewall on the new computer that is running SQL Server is configured to allow the App-V Management Server to access the system.</span></span> <span data-ttu-id="ef420-134">In **strumenti di amministrazione**usare il programma **Windows Firewall con sicurezza avanzata** per creare una **regola in entrata** per la porta utilizzata da SQL Server (il valore predefinito è la porta 1433).</span><span class="sxs-lookup"><span data-stu-id="ef420-134">Under **Administrative Tools**, use the **Windows Firewall with Advanced Security** program to create an **Inbound Rule** for the port that is used by SQL Server (default is port 1433).</span></span>

**<span data-ttu-id="ef420-135">Per eseguire la migrazione dei processi di SQL Server Agent di App-V</span><span class="sxs-lookup"><span data-stu-id="ef420-135">To migrate the App-V SQL Server Agent jobs</span></span>**

1.  <span data-ttu-id="ef420-136">Nel computer originale in cui è in uso SQL Server, in SQL Server Management Studio espandere il nodo **agente SQL Server** e quindi espandere il nodo **processi** .</span><span class="sxs-lookup"><span data-stu-id="ef420-136">On the original computer that is running SQL Server, in SQL Server Management Studio, expand the **SQL Server Agent** node, and then expand the **Jobs** node.</span></span>

2.  <span data-ttu-id="ef420-137">Fare clic con il pulsante destro del mouse sui quattro processi di App-V seguenti e scegliere **processo script come | Crea in | File**e salvare ogni script in una cartella e assegnare a ogni script un nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="ef420-137">Right-click the following four App-V jobs and select **Script Job as | CREATE to | File**, and save each script to a folder and give each script a descriptive name.</span></span>

    -   **<span data-ttu-id="ef420-138">Database di SoftGrid (appvdbname) controlla Cronologia utilizzo</span><span class="sxs-lookup"><span data-stu-id="ef420-138">Softgrid Database (appvdbname) Check Usage History</span></span>**

    -   **<span data-ttu-id="ef420-139">Database di SoftGrid (appvdbname) Chiudi sessioni orfane</span><span class="sxs-lookup"><span data-stu-id="ef420-139">Softgrid Database (appvdbname) Close Orphaned Sessions</span></span>**

    -   **<span data-ttu-id="ef420-140">Database SoftGrid (appvdbname) applicare il limite di dimensione</span><span class="sxs-lookup"><span data-stu-id="ef420-140">Softgrid Database (appvdbname) Enforce Size Limit</span></span>**

    -   **<span data-ttu-id="ef420-141">Database di SoftGrid (appvdbname) monitor Alert/stato processo</span><span class="sxs-lookup"><span data-stu-id="ef420-141">Softgrid Database (appvdbname) Monitor Alert/Job Status</span></span>**

3.  <span data-ttu-id="ef420-142">Copiare i quattro file di script (con estensione SQL) nel computer di destinazione in cui è in esecuzione SQL Server e aprire SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="ef420-142">Copy the four script files (.sql) to the destination computer that is running SQL Server and open SQL Server Management Studio.</span></span>

4.  <span data-ttu-id="ef420-143">In Esplora risorse fare clic con il pulsante destro del mouse su ogni file con estensione SQL e quindi scegliere **Esegui**.</span><span class="sxs-lookup"><span data-stu-id="ef420-143">In Windows Explorer, right-click each .sql file and then click **Run**.</span></span> <span data-ttu-id="ef420-144">Ogni script viene aperto in una finestra di query in SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="ef420-144">Each script will open in a query window in SQL Server Management Studio.</span></span> <span data-ttu-id="ef420-145">Fare clic su **Esegui** per ogni script e verificare che ogni operazione sia stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="ef420-145">Click **Execute** for each script and verify that each is completed successfully.</span></span>

5.  <span data-ttu-id="ef420-146">Aggiornare il nodo **processi** nel nodo **agente SQL Server** e verificare che i quattro processi vengano creati correttamente.</span><span class="sxs-lookup"><span data-stu-id="ef420-146">Refresh the **Jobs** node under the **SQL Server Agent** node and confirm that the four jobs are created successfully.</span></span>

**<span data-ttu-id="ef420-147">Per aggiornare la configurazione di App-V Management Server</span><span class="sxs-lookup"><span data-stu-id="ef420-147">To update the configuration of the App-V Management Server</span></span>**

1.  <span data-ttu-id="ef420-148">Nel server di gestione di App-V modificare le chiavi del registro di sistema seguenti:</span><span class="sxs-lookup"><span data-stu-id="ef420-148">On the App-V Management Server, modify the following registry keys:</span></span>

    -   <span data-ttu-id="ef420-149">**Sqlservername**  =  &lt; newservername&gt;</span><span class="sxs-lookup"><span data-stu-id="ef420-149">**SQLServerName** = &lt;newservername&gt;</span></span>

    -   <span data-ttu-id="ef420-150">**SQLServerPort**  =  SQLServerPort &lt; newserverport&gt;</span><span class="sxs-lookup"><span data-stu-id="ef420-150">**SQLServerPort** = &lt;newserverport&gt;</span></span>

    <span data-ttu-id="ef420-151">Riavvia quindi il servizio App-V Server.</span><span class="sxs-lookup"><span data-stu-id="ef420-151">Then restart the App-V server service.</span></span>

2.  <span data-ttu-id="ef420-152">Individuare il file SftMgmt. udl nella directory di installazione di App-V Management Server (l'impostazione predefinita è C:\\Programmi \\Programmi\\microsoft System Center App Virt Management Server\\App Virt Management Service).</span><span class="sxs-lookup"><span data-stu-id="ef420-152">Browse to find the file SftMgmt.udl under the App-V Management Server installation directory (default is C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Service).</span></span> <span data-ttu-id="ef420-153">Fare clic con il pulsante destro del mouse sul file e scegliere **Apri**.</span><span class="sxs-lookup"><span data-stu-id="ef420-153">Right-click the file and select **Open**.</span></span>

3.  <span data-ttu-id="ef420-154">Nella scheda **connessione** immettere il nome del computer di destinazione in cui è in uso SQL Server e quindi fare clic su **Test connessione**.</span><span class="sxs-lookup"><span data-stu-id="ef420-154">On the **Connection** tab, enter the name of the destination computer that is running SQL Server, and then click **Test Connection**.</span></span> <span data-ttu-id="ef420-155">Quando il test ha esito positivo, fare di nuovo clic su **OK** e quindi su **OK** .</span><span class="sxs-lookup"><span data-stu-id="ef420-155">When the test is successful, click **OK** and then click **OK** again.</span></span>

4.  <span data-ttu-id="ef420-156">Per le versioni di App-V Management Server prima di 4,5 SP2, è necessario aggiornare le impostazioni di registrazione SQL.</span><span class="sxs-lookup"><span data-stu-id="ef420-156">For App-V Management Server versions before 4.5 SP2, you must update the SQL Logging settings.</span></span> <span data-ttu-id="ef420-157">In **gruppi di server**fare clic con il pulsante destro del mouse sul gruppo server a cui è associato il server e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="ef420-157">Under **Server Groups**, right-click the server group the server is a member of and select **Properties**.</span></span>

5.  <span data-ttu-id="ef420-158">Nella scheda **registrazione** fare clic per selezionare la voce del **database SQL** e quindi fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="ef420-158">On the **Logging** tab click to select the **SQL Database** entry and then click **Edit**.</span></span>

6.  <span data-ttu-id="ef420-159">Cambiare il **nome host DNS** nel nome host del nuovo computer in cui è in uso SQL Server e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef420-159">Change the **DNS Host Name** to the host name of the new computer that is running SQL Server and then click **OK**.</span></span> <span data-ttu-id="ef420-160">Fare clic su **OK** due volte di più e quindi riavviare il servizio App-V Server.</span><span class="sxs-lookup"><span data-stu-id="ef420-160">Click **OK** two times more, and then restart the App-V server service.</span></span>

7.  <span data-ttu-id="ef420-161">Aprire la console di gestione di App-V, fare clic con il pulsante destro del mouse sul nodo delle **applicazioni** e scegliere **Aggiorna**.</span><span class="sxs-lookup"><span data-stu-id="ef420-161">Open the App-V Management Console, right-click the **Applications** node and select **Refresh**.</span></span> <span data-ttu-id="ef420-162">L'elenco delle applicazioni deve essere visualizzato come prima.</span><span class="sxs-lookup"><span data-stu-id="ef420-162">The list of applications should be displayed as before.</span></span>

 

 





