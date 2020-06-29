---
title: Come installare il server di report in un computer autonomo e connetterlo al database
description: Come installare il server di report in un computer autonomo e connetterlo al database
author: dansimp
ms.assetid: d186bdb7-e522-4124-bc6d-7d5a41ba8266
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f20f1ce16c3f0168d1c797efd816d4125c0f1f53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805386"
---
# <span data-ttu-id="9b570-103">Come installare il server di report in un computer autonomo e connetterlo al database</span><span class="sxs-lookup"><span data-stu-id="9b570-103">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="9b570-104">Usare la procedura seguente per installare il server di report in un computer autonomo e connetterlo al database.</span><span class="sxs-lookup"><span data-stu-id="9b570-104">Use the following procedure to install the reporting server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="9b570-105">Importante</span><span class="sxs-lookup"><span data-stu-id="9b570-105">Important</span></span>**  
<span data-ttu-id="9b570-106">Prima di eseguire la procedura seguente, è necessario leggere e comprendere [informazioni sui report di App-V 5,0](about-app-v-50-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="9b570-106">Before performing the following procedure you should read and understand [About App-V 5.0 Reporting](about-app-v-50-reporting.md).</span></span>



**<span data-ttu-id="9b570-107">Per installare il server di report in un computer autonomo e connetterlo al database</span><span class="sxs-lookup"><span data-stu-id="9b570-107">To install the reporting server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="9b570-108">Copiare i file di installazione del server App-V 5,0 nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="9b570-108">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="9b570-109">Per avviare l'installazione del server App-V 5,0, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore.</span><span class="sxs-lookup"><span data-stu-id="9b570-109">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="9b570-110">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="9b570-110">Click **Install**.</span></span>

2.  <span data-ttu-id="9b570-111">Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="9b570-111">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="9b570-112">In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).**</span><span class="sxs-lookup"><span data-stu-id="9b570-112">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="9b570-113">Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="9b570-113">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="9b570-114">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="9b570-114">Click **Next**.</span></span>

4.  <span data-ttu-id="9b570-115">Nella pagina **Selezione funzionalità** selezionare la casella di controllo del **Server dei report** e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="9b570-115">On the **Feature Selection** page, select the **Reporting Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="9b570-116">Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="9b570-116">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="9b570-117">Nella pagina **Configura database di report esistente** selezionare **Usa un server SQL remoto**e digitare il nome del computer che ha eseguito Microsoft SQL Server, ad esempio **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="9b570-117">On the **Configure Existing Reporting Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL Server, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="9b570-118">Nota</span><span class="sxs-lookup"><span data-stu-id="9b570-118">Note</span></span>**  
    <span data-ttu-id="9b570-119">Se Microsoft SQL Server è distribuito nello stesso server, selezionare **Usa SQL Server locale**.</span><span class="sxs-lookup"><span data-stu-id="9b570-119">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this reporting server will use, for example **AppvReporting**.
~~~

7. <span data-ttu-id="9b570-120">Nella pagina **configura configurazione del server di Reporting** .</span><span class="sxs-lookup"><span data-stu-id="9b570-120">On the **Configure Reporting Server Configuration** page.</span></span>

   -   <span data-ttu-id="9b570-121">Specificare il nome del sito Web che si vuole usare per il servizio di creazione di report.</span><span class="sxs-lookup"><span data-stu-id="9b570-121">Specify the Website Name that you want to use for the Reporting Service.</span></span> <span data-ttu-id="9b570-122">Se non si ha un nome personalizzato, lasciarlo invariato.</span><span class="sxs-lookup"><span data-stu-id="9b570-122">Leave the default unchanged if you do not have a custom name.</span></span>

   -   <span data-ttu-id="9b570-123">Per il **Binding della porta**, specifica un numero di porta univoco che verrà usato da App-V 5,0, ad esempio **55555**.</span><span class="sxs-lookup"><span data-stu-id="9b570-123">For the **Port binding**, specify a unique port number that will be used by App-V 5.0, for example **55555**.</span></span> <span data-ttu-id="9b570-124">Devi anche assicurarti che la porta specificata non venga usata da un altro sito Web.</span><span class="sxs-lookup"><span data-stu-id="9b570-124">You should also ensure that the port specified is not being used by another website.</span></span>

8. <span data-ttu-id="9b570-125">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="9b570-125">Click **Install**.</span></span>

   <span data-ttu-id="9b570-126">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="9b570-126">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9b570-127">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9b570-127">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9b570-128">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="9b570-128">Got an App-V issue?</span></span>** <span data-ttu-id="9b570-129">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9b570-129">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9b570-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b570-130">Related topics</span></span>


[<span data-ttu-id="9b570-131">Informazioni sulla creazione di report in App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="9b570-131">About App-V 5.0 Reporting</span></span>](about-app-v-50-reporting.md)

[<span data-ttu-id="9b570-132">Distribuzione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="9b570-132">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="9b570-133">Come abilitare la creazione di report nel client App-V 5.0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9b570-133">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)









