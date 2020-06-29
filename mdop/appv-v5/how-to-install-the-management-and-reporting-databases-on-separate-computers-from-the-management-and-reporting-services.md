---
title: Come installare i database di gestione e creazione di report in computer distinti dai servizi di gestione e creazione di report
description: Come installare i database di gestione e creazione di report in computer distinti dai servizi di gestione e creazione di report
author: dansimp
ms.assetid: 02afd6d6-4c33-4c0b-bd88-ae167b786fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1522045fced411164ac4fd36af41d46ab61ad6f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805416"
---
# <span data-ttu-id="35342-103">Come installare i database di gestione e creazione di report in computer distinti dai servizi di gestione e creazione di report</span><span class="sxs-lookup"><span data-stu-id="35342-103">How to Install the Management and Reporting Databases on Separate Computers from the Management and Reporting Services</span></span>


<span data-ttu-id="35342-104">Usare la procedura seguente per installare il server di database e il server di gestione in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="35342-104">Use the following procedure to install the database server and management server on different computers.</span></span> <span data-ttu-id="35342-105">Il computer in cui si prevede di installare il server di database deve eseguire una versione supportata di Microsoft SQL o l'installazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="35342-105">The computer you plan to install the database server on must be running a supported version of Microsoft SQL or the installation will fail.</span></span>

**<span data-ttu-id="35342-106">Nota</span><span class="sxs-lookup"><span data-stu-id="35342-106">Note</span></span>**  
<span data-ttu-id="35342-107">Dopo aver completato la distribuzione, il nome di **Microsoft SQL Server**, il nome dell' **istanza** e il nome del **database** verranno richiesti dall'amministratore che installa il servizio per potersi connettere a questi database.</span><span class="sxs-lookup"><span data-stu-id="35342-107">After you complete the deployment, the **Microsoft SQL Server name**, **instance name** and **database name** will be required by the administrator installing the service to be able to connect to these databases.</span></span>



**<span data-ttu-id="35342-108">Per installare il database di gestione e il server di gestione in computer separati</span><span class="sxs-lookup"><span data-stu-id="35342-108">To install the management database and the management server on separate computers</span></span>**

1.  <span data-ttu-id="35342-109">Copiare i file di installazione del server App-V 5,0 nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="35342-109">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="35342-110">Per avviare l'installazione del server App-V 5,0, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore.</span><span class="sxs-lookup"><span data-stu-id="35342-110">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="35342-111">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="35342-111">Click **Install**.</span></span>

2.  <span data-ttu-id="35342-112">Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="35342-112">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="35342-113">In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).**</span><span class="sxs-lookup"><span data-stu-id="35342-113">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="35342-114">Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="35342-114">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="35342-115">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="35342-115">Click **Next**.</span></span>

4.  <span data-ttu-id="35342-116">Nella pagina **Selezione funzionalità** selezionare i componenti che si desidera installare selezionando la casella di **controllo database server di gestione** e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="35342-116">On the **Feature Selection** page, select the components you want to install by selecting the **Management Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="35342-117">Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="35342-117">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="35342-118">Nella **pagina Crea nuovo database del server di gestione**iniziale accettare le selezioni predefinite, se necessario, e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="35342-118">On the initial **Create New Management Server Database page**, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="35342-119">Se si usa un'istanza di SQL Server personalizzata, selezionare **Usa un'istanza personalizzata** e digitare il nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="35342-119">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="35342-120">Se si usa un nome di database personalizzato, selezionare **configurazione personalizzata** e digitare il nome del database.</span><span class="sxs-lookup"><span data-stu-id="35342-120">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="35342-121">Nella pagina **Crea nuovo database del server di gestione** selezionare **Usa un computer remoto**e digitare l'account del computer remoto usando il formato seguente: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="35342-121">On the next **Create New Management Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="35342-122">Nota</span><span class="sxs-lookup"><span data-stu-id="35342-122">Note</span></span>**  
    <span data-ttu-id="35342-123">Se si prevede di distribuire il server di gestione nello stesso computer, è necessario selezionare **Usa questo computer locale**.</span><span class="sxs-lookup"><span data-stu-id="35342-123">If you plan to deploy the management server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the management server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="35342-124">Per avviare l'installazione, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="35342-124">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="35342-125">Per installare il database delle relazioni e il server di report in computer separati</span><span class="sxs-lookup"><span data-stu-id="35342-125">To install the reporting database and the reporting server on separate computers</span></span>**

1.  <span data-ttu-id="35342-126">Copiare i file di installazione del server App-V 5,0 nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="35342-126">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="35342-127">Per avviare l'installazione del server App-V 5,0, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore.</span><span class="sxs-lookup"><span data-stu-id="35342-127">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="35342-128">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="35342-128">Click **Install**.</span></span>

2.  <span data-ttu-id="35342-129">Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="35342-129">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="35342-130">In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).**</span><span class="sxs-lookup"><span data-stu-id="35342-130">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="35342-131">Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="35342-131">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="35342-132">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="35342-132">Click **Next**.</span></span>

4.  <span data-ttu-id="35342-133">Nella pagina **Selezione funzionalità** selezionare i componenti da installare selezionando la casella di controllo **database server report** e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="35342-133">On the **Feature Selection** page, select the components you want to install by selecting the **Reporting Server Database** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="35342-134">Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="35342-134">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="35342-135">Nella pagina iniziale **Crea nuovo database del server di Reporting** accettare le selezioni predefinite, se necessario, e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="35342-135">On the initial **Create New Reporting Server Database** page, accept the default selections if appropriate, and click **Next**.</span></span>

    <span data-ttu-id="35342-136">Se si usa un'istanza di SQL Server personalizzata, selezionare **Usa un'istanza personalizzata** e digitare il nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="35342-136">If you are using a custom SQL Server instance, then select **Use a custom instance** and type the name of the instance.</span></span>

    <span data-ttu-id="35342-137">Se si usa un nome di database personalizzato, selezionare **configurazione personalizzata** e digitare il nome del database.</span><span class="sxs-lookup"><span data-stu-id="35342-137">If you are using a custom database name, then select **Custom configuration** and type the database name.</span></span>

7.  <span data-ttu-id="35342-138">Nella pagina **Crea nuovo database del server di Reporting** selezionare **Usa un computer remoto**e digitare l'account del computer remoto usando il formato seguente: **Domain\\MachineAccount**.</span><span class="sxs-lookup"><span data-stu-id="35342-138">On the next **Create New Reporting Server Database** page, select **Use a remote computer**, and type the remote machine account using the following format: **Domain\\MachineAccount**.</span></span>

    **<span data-ttu-id="35342-139">Nota</span><span class="sxs-lookup"><span data-stu-id="35342-139">Note</span></span>**  
    <span data-ttu-id="35342-140">Se si prevede di distribuire il server di report nello stesso computer, è necessario selezionare **Usa questo computer locale**.</span><span class="sxs-lookup"><span data-stu-id="35342-140">If you plan to deploy the reporting server on the same computer you must select **Use this local computer**.</span></span>



~~~
Specify the user name for the reporting server **Install Administrator** using the following format: **Domain\\AdministratorLoginName**. Click **Next**.
~~~

8. <span data-ttu-id="35342-141">Per avviare l'installazione, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="35342-141">To start the installation, click **Install**.</span></span>

**<span data-ttu-id="35342-142">Per installare i database di gestione e Reporting usando gli script di database di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="35342-142">To install the management and reporting databases using App-V 5.0 database scripts</span></span>**

1.  <span data-ttu-id="35342-143">Copiare i file di installazione del server App-V 5,0 nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="35342-143">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span>

2.  <span data-ttu-id="35342-144">Per estrarre gli script di database di App-V 5,0, aprire un prompt dei comandi e specificare il percorso in cui vengono salvati i file di installazione ed eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="35342-144">To extract the App-V 5.0 database scripts, open a command prompt and specify the location where the installation files are saved and run the following command:</span></span>

    <span data-ttu-id="35342-145">**appv\_server\_setup.exe** **/layout** **/LAYOUTDIR = "InstallationExtractionLocation"**.</span><span class="sxs-lookup"><span data-stu-id="35342-145">**appv\_server\_setup.exe** **/LAYOUT** **/LAYOUTDIR=”InstallationExtractionLocation”**.</span></span>

3.  <span data-ttu-id="35342-146">Dopo aver completato l'estrazione, per accedere agli script di database di App-V 5,0 e al file Leggimi delle istruzioni:</span><span class="sxs-lookup"><span data-stu-id="35342-146">After the extraction has been completed, to access the App-V 5.0 database scripts and instructions readme file:</span></span>

    -   <span data-ttu-id="35342-147">Gli script di database di gestione di App-V 5,0 e le istruzioni Leggimi si trovano nella cartella seguente: database di gestione degli script di database **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Management Database**.</span><span class="sxs-lookup"><span data-stu-id="35342-147">The App-V 5.0 Management Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Management Database**.</span></span>

    -   <span data-ttu-id="35342-148">I file di script e istruzioni del database di report App-V 5,0 si trovano nella cartella seguente: database di report degli script di database **InstallationExtractionLocation**  \\  **Database Scripts**  \\  **Reporting Database**.</span><span class="sxs-lookup"><span data-stu-id="35342-148">The App-V 5.0 Reporting Database scripts and instructions readme are located in the following folder: **InstallationExtractionLocation** \\ **Database Scripts** \\ **Reporting Database**.</span></span>

4.  <span data-ttu-id="35342-149">Per ogni database, copiare gli script in una condivisione e modificarli seguendo le istruzioni nel file Leggimi.</span><span class="sxs-lookup"><span data-stu-id="35342-149">For each database, copy the scripts to a share and modify them following the instructions in the readme file.</span></span>

    **<span data-ttu-id="35342-150">Nota</span><span class="sxs-lookup"><span data-stu-id="35342-150">Note</span></span>**  
    <span data-ttu-id="35342-151">Per altre informazioni sulla modifica dei SID necessari contenuti negli script, vedere [come installare i database di App-V e convertire gli identificatori di sicurezza associati tramite PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="35342-151">For more information about modifying the required SIDs contained in the scripts see, [How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell.md).</span></span>



5.  <span data-ttu-id="35342-152">Eseguire gli script nel computer che esegue Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="35342-152">Run the scripts on the computer running Microsoft SQL Server.</span></span>

    <span data-ttu-id="35342-153">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="35342-153">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="35342-154">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="35342-154">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="35342-155">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="35342-155">Got an App-V issue?</span></span>** <span data-ttu-id="35342-156">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="35342-156">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="35342-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35342-157">Related topics</span></span>


[<span data-ttu-id="35342-158">Distribuzione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="35342-158">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









