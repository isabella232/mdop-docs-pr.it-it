---
title: Come installare il server di report in un computer autonomo e connetterlo al database
description: Come installare il server di report in un computer autonomo e connetterlo al database
author: dansimp
ms.assetid: 11f07750-4045-4c8d-a583-7d70c9e9aa7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67866714ff6ae60097d9b368fd0eaf361b08eec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805379"
---
# <span data-ttu-id="99e05-103">Come installare il server di report in un computer autonomo e connetterlo al database</span><span class="sxs-lookup"><span data-stu-id="99e05-103">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>

<span data-ttu-id="99e05-104">Usare la procedura seguente per installare il server di report in un computer autonomo e connetterlo al database.</span><span class="sxs-lookup"><span data-stu-id="99e05-104">Use the following procedure to install the reporting server on a standalone computer and connect it to the database.</span></span>

<span data-ttu-id="99e05-105">**Importante** Prima di eseguire la procedura seguente, è necessario leggere e comprendere [informazioni sui report di App-V 5,1](about-app-v-51-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="99e05-105">**Important** Before performing the following procedure you should read and understand [About App-V 5.1 Reporting](about-app-v-51-reporting.md).</span></span>

## <span data-ttu-id="99e05-106">Per installare il server di report in un computer autonomo e connetterlo al database</span><span class="sxs-lookup"><span data-stu-id="99e05-106">To install the reporting server on a standalone computer and connect it to the database</span></span>

1. <span data-ttu-id="99e05-107">Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="99e05-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="99e05-108">Per avviare l'installazione del server App-V 5,1, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore.</span><span class="sxs-lookup"><span data-stu-id="99e05-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="99e05-109">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="99e05-109">Click **Install**.</span></span>

2. <span data-ttu-id="99e05-110">Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="99e05-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="99e05-111">In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).**</span><span class="sxs-lookup"><span data-stu-id="99e05-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="99e05-112">Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="99e05-112">To disable Microsoft updates, select **I don't want to use Microsoft Update**.</span></span> <span data-ttu-id="99e05-113">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="99e05-113">Click **Next**.</span></span>

4. <span data-ttu-id="99e05-114">Nella pagina **Selezione funzionalità** selezionare la casella di controllo del **Server dei report** e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="99e05-114">On the **Feature Selection** page, select the **Reporting Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="99e05-115">Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="99e05-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="99e05-116">Nella pagina **Configura database di report esistente** selezionare **Usa un server SQL remoto**e digitare il nome del computer che ha eseguito Microsoft SQL Server, ad esempio **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="99e05-116">On the **Configure Existing Reporting Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL Server, for example **SqlServerMachine**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="99e05-117">Se Microsoft SQL Server è distribuito nello stesso server, selezionare **Usa SQL Server locale**.</span><span class="sxs-lookup"><span data-stu-id="99e05-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>

    <span data-ttu-id="99e05-118">Per l'istanza di SQL Server, selezionare **Usa l'istanza predefinita**.</span><span class="sxs-lookup"><span data-stu-id="99e05-118">For the SQL Server Instance, select **Use the default instance**.</span></span> <span data-ttu-id="99e05-119">Se si usa un'istanza di Microsoft SQL Server personalizzata, è necessario selezionare **Usa un'istanza personalizzata** e quindi digitare il nome dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="99e05-119">If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.</span></span>

    <span data-ttu-id="99e05-120">Specificare il **nome del database di SQL Server** che verrà usato da questo server di report, ad esempio **AppvReporting**.</span><span class="sxs-lookup"><span data-stu-id="99e05-120">Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.</span></span>

7. <span data-ttu-id="99e05-121">Nella pagina **configura configurazione del server di Reporting** .</span><span class="sxs-lookup"><span data-stu-id="99e05-121">On the **Configure Reporting Server Configuration** page.</span></span>

   - <span data-ttu-id="99e05-122">Specificare il nome del sito Web che si vuole usare per il servizio di creazione di report.</span><span class="sxs-lookup"><span data-stu-id="99e05-122">Specify the Website Name that you want to use for the Reporting Service.</span></span> <span data-ttu-id="99e05-123">Se non si ha un nome personalizzato, lasciarlo invariato.</span><span class="sxs-lookup"><span data-stu-id="99e05-123">Leave the default unchanged if you do not have a custom name.</span></span>

   - <span data-ttu-id="99e05-124">Per il **Binding della porta**, specifica un numero di porta univoco che verrà usato da App-V 5,1, ad esempio **55555**.</span><span class="sxs-lookup"><span data-stu-id="99e05-124">For the **Port binding**, specify a unique port number that will be used by App-V 5.1, for example **55555**.</span></span> <span data-ttu-id="99e05-125">Devi anche assicurarti che la porta specificata non venga usata da un altro sito Web.</span><span class="sxs-lookup"><span data-stu-id="99e05-125">You should also ensure that the port specified is not being used by another website.</span></span>

8. <span data-ttu-id="99e05-126">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="99e05-126">Click **Install**.</span></span>

**<span data-ttu-id="99e05-127">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="99e05-127">Got an App-V issue?</span></span>** <span data-ttu-id="99e05-128">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="99e05-128">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="99e05-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99e05-129">Related topics</span></span>

[<span data-ttu-id="99e05-130">Informazioni sulla creazione di report in App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="99e05-130">About App-V 5.1 Reporting</span></span>](about-app-v-51-reporting.md)

[<span data-ttu-id="99e05-131">Distribuzione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="99e05-131">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="99e05-132">Come abilitare la creazione di report nel client App-V 5.1 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="99e05-132">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)
