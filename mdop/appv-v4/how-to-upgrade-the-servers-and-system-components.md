---
title: Come aggiornare i server e i componenti del sistema
description: Come aggiornare i server e i componenti del sistema
author: dansimp
ms.assetid: 7d8374fe-5897-452e-923e-556a854b2024
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 61f8742a2f5e3c17083a77b839dfbee85ea00e24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816425"
---
# <span data-ttu-id="f6547-103">Come aggiornare i server e i componenti del sistema</span><span class="sxs-lookup"><span data-stu-id="f6547-103">How to Upgrade the Servers and System Components</span></span>


<span data-ttu-id="f6547-104">Usare la procedura seguente per aggiornare i componenti software installati in tutti i computer di sistema per la virtualizzazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f6547-104">Use the following procedure to upgrade software components installed on all Application Virtualization System computers.</span></span> <span data-ttu-id="f6547-105">I servizi di sistema di virtualizzazione delle applicazioni verranno riavviati automaticamente in ogni computer dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="f6547-105">Application Virtualization System services will be restarted automatically on each computer after it has been upgraded.</span></span>

**<span data-ttu-id="f6547-106">Nota</span><span class="sxs-lookup"><span data-stu-id="f6547-106">Note</span></span>**  
-   <span data-ttu-id="f6547-107">Il processo di aggiornamento Arresta tutti i servizi di sistema di virtualizzazione delle applicazioni, eliminando così il sistema dal servizio.</span><span class="sxs-lookup"><span data-stu-id="f6547-107">The upgrade process stops all Application Virtualization System services, thereby taking the system out of service.</span></span> <span data-ttu-id="f6547-108">Le sessioni utente devono essere interrotte prima di iniziare il processo di aggiornamento ed è consigliabile arrestare tutti i servizi Application Virtualization Server nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="f6547-108">User sessions should be shut down before you begin the upgrade process, and you should stop all Application Virtualization Server services in your environment.</span></span>

-   <span data-ttu-id="f6547-109">Se si hanno più server che condividono l'accesso al database di virtualizzazione dell'applicazione, è necessario che tutti questi server vengano disattivati durante l'aggiornamento del database.</span><span class="sxs-lookup"><span data-stu-id="f6547-109">If you have more than one server that is sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="f6547-110">È consigliabile seguire le normali procedure aziendali per l'aggiornamento del database, ma è consigliabile testare l'aggiornamento del database usando una copia di backup del database per la prima volta in un server di test.</span><span class="sxs-lookup"><span data-stu-id="f6547-110">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="f6547-111">Devi quindi selezionare uno dei server per il primo aggiornamento, che aggiornerà lo schema del database.</span><span class="sxs-lookup"><span data-stu-id="f6547-111">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="f6547-112">Dopo che il database di produzione è stato aggiornato correttamente, è possibile aggiornare gli altri server.</span><span class="sxs-lookup"><span data-stu-id="f6547-112">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

-   <span data-ttu-id="f6547-113">È possibile eseguire l'aggiornamento a Microsoft Application Virtualization (App-V) 4.5 solo da Microsoft Application Virtualization (App-V) 4.1 o 4.1 SP1.</span><span class="sxs-lookup"><span data-stu-id="f6547-113">You can upgrade to Microsoft Application Virtualization (App-V)4.5 only from Microsoft Application Virtualization (App-V)4.1 or4.1 SP1.</span></span> <span data-ttu-id="f6547-114">App-V 4.0 e versioni precedenti devono essere disinstallate o aggiornate in 4.1 o 4.1 SP1 prima di eseguire l'aggiornamento a App-V 4.5.</span><span class="sxs-lookup"><span data-stu-id="f6547-114">App-V4.0 and earlier must be uninstalled or upgraded to4.1 or4.1 SP1 before upgrading to App-V4.5.</span></span>

 

**<span data-ttu-id="f6547-115">Per aggiornare i componenti software nei computer dei sistemi di virtualizzazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="f6547-115">To upgrade software components on Application Virtualization System computers</span></span>**

1.  <span data-ttu-id="f6547-116">Passare al percorso del programma di installazione nella rete, eseguire il programma dalla rete oppure copiarne la directory nel computer di destinazione e quindi fare doppio clic sul file Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="f6547-116">Navigate to the location of the Setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click the Setup.exe file.</span></span>

2.  <span data-ttu-id="f6547-117">Nella pagina di **benvenuto** dell'installazione guidata fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f6547-117">On the **Welcome** page of the Installation Wizard, click **Next**.</span></span>

3.  <span data-ttu-id="f6547-118">Nella pagina **contratto di licenza** leggere il contratto di licenza, verificare **di accettare i termini del contratto di licenza**e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f6547-118">On the **License Agreement** page, read the license agreement, check **I accept the terms in the license agreement**, and click **Next**.</span></span>

4.  <span data-ttu-id="f6547-119">Quando si apre la pagina **software installata** e viene visualizzato un elenco dei componenti del sistema di virtualizzazione delle applicazioni installati e della versione di ogni componente, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f6547-119">When the **Installed Software** page opens and displays a list of the installed Application Virtualization System components and the version of each component, click **Next**.</span></span>

5.  <span data-ttu-id="f6547-120">Nella pagina **avviso di perdita della sessione** leggere il messaggio visualizzato e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f6547-120">On the **Session Loss Warning** page, read the displayed message and click **Next**.</span></span>

6.  <span data-ttu-id="f6547-121">Nella pagina **Connetti a database di configurazione** esaminare il contenuto della pagina e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f6547-121">On the **Connect to Configuration Database** page, review the content on the page and click **Next**.</span></span>

7.  <span data-ttu-id="f6547-122">Se viene visualizzata la pagina di **aggiornamento del database** , è necessario un aggiornamento del database.</span><span class="sxs-lookup"><span data-stu-id="f6547-122">If the **Database Upgrade Required** page is displayed, a database upgrade is required.</span></span> <span data-ttu-id="f6547-123">Immettere le credenziali amministrative del database e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f6547-123">Enter the database administrative credentials, and then click **Next**.</span></span> <span data-ttu-id="f6547-124">Se questa pagina non è visualizzata, passare al passaggio 9.</span><span class="sxs-lookup"><span data-stu-id="f6547-124">If this page is not displayed, skip to Step 9.</span></span>

8.  <span data-ttu-id="f6547-125">Nella pagina **Database Configuration backup** selezionare le caselle appropriate per eseguire il backup ed esportarlo in una posizione esistente e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f6547-125">On the **Backup Configuration Database** page, check the appropriate boxes to perform the backup and export it to an existing location, and then click **Next**.</span></span>

    <span data-ttu-id="f6547-126">**Importante**  Per poter eseguire il rollback alla versione precedente in caso di errore di aggiornamento, verificare di aver **eseguito il backup della casella database di configurazione oppure di** perdere i dati di configurazione.</span><span class="sxs-lookup"><span data-stu-id="f6547-126">**Important** If you want to be able to roll back to the previous version in the event of an upgrade failure, make sure you check the **Perform a backup of the configuration database** box, or you will lose the configuration data.</span></span>

    <span data-ttu-id="f6547-127">Quando si vuole ripristinare un database con VSS, è necessario prima di tutto arrestare il servizio App-V Server nel server di gestione.</span><span class="sxs-lookup"><span data-stu-id="f6547-127">When you want to restore a database with VSS, you must first stop the App-V Server Service on the Management Server.</span></span> <span data-ttu-id="f6547-128">Questa operazione deve essere eseguita in ogni server di gestione se sono presenti più server connessi allo stesso database.</span><span class="sxs-lookup"><span data-stu-id="f6547-128">This should be done on every Management server if there is more than one server connected to the same database.</span></span>

     

9.  <span data-ttu-id="f6547-129">Nella prima pagina di **convalida del pacchetto** leggere il contenuto e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f6547-129">On the first **Package Validation** page, read the content and then click **Next**.</span></span>

10. <span data-ttu-id="f6547-130">Nella seconda pagina di **convalida del pacchetto** è possibile visualizzare i dettagli della convalida del pacchetto in una finestra del blocco note.</span><span class="sxs-lookup"><span data-stu-id="f6547-130">On the second **Package Validation** page, you have the option of displaying the details of the package validation in a Notepad window.</span></span> <span data-ttu-id="f6547-131">Per visualizzare i dettagli, fare clic su **Dettagli**; in caso contrario, fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f6547-131">To see the details, click **Details**; otherwise, click **Next**.</span></span>

11. <span data-ttu-id="f6547-132">Nella pagina **pronto per l'aggiornamento della programmazione** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f6547-132">On the **Ready to Upgrade the Program** page, click **Next**.</span></span>

12. <span data-ttu-id="f6547-133">Nella pagina **installazione guidata completare** fare clic su **fine**.</span><span class="sxs-lookup"><span data-stu-id="f6547-133">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

13. <span data-ttu-id="f6547-134">Ripetere i passaggi da 1 a 12 in tutti gli altri computer in cui è stata installata l'Application Virtualization Management Console o il componente software Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="f6547-134">Repeat steps 1–12 on all other computers where you installed the Application Virtualization Management Console or the Application Virtualization Server software component.</span></span>

    <span data-ttu-id="f6547-135">Dopo l'aggiornamento dell'archivio dati, è possibile riprendere il normale funzionamento.</span><span class="sxs-lookup"><span data-stu-id="f6547-135">After upgrading the data store, you can resume normal operation.</span></span> <span data-ttu-id="f6547-136">L'aggiornamento dell'archivio dati viene aggiornato quando si aggiorna un server o il servizio Web di gestione App-V.</span><span class="sxs-lookup"><span data-stu-id="f6547-136">(The data store is upgraded when you upgrade any server or the App-V Management Web Service.)</span></span>

## <span data-ttu-id="f6547-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6547-137">Related topics</span></span>


[<span data-ttu-id="f6547-138">Considerazioni sull'aggiornamento e la distribuzione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f6547-138">Application Virtualization Deployment and Upgrade Considerations</span></span>](application-virtualization-deployment-and-upgrade-considerations.md)

 

 





