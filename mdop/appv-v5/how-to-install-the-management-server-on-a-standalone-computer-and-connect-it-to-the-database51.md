---
title: Come installare il server di gestione in un computer autonomo e connetterlo al database
description: Come installare il server di gestione in un computer autonomo e connetterlo al database
author: dansimp
ms.assetid: 3f83c335-d976-4abd-b8f8-d7f5e50b4318
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2cce96f914f65e7432b5ed9e7c5ecb1a6306990
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805409"
---
# <span data-ttu-id="f8044-103">Come installare il server di gestione in un computer autonomo e connetterlo al database</span><span class="sxs-lookup"><span data-stu-id="f8044-103">How to install the Management Server on a Standalone Computer and Connect it to the Database</span></span>


<span data-ttu-id="f8044-104">Usare la procedura seguente per installare il server di gestione in un computer autonomo e connetterlo al database.</span><span class="sxs-lookup"><span data-stu-id="f8044-104">Use the following procedure to install the management server on a standalone computer and connect it to the database.</span></span>

**<span data-ttu-id="f8044-105">Per installare il server di gestione in un computer autonomo e connetterlo al database</span><span class="sxs-lookup"><span data-stu-id="f8044-105">To install the management server on a standalone computer and connect it to the database</span></span>**

1.  <span data-ttu-id="f8044-106">Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="f8044-106">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="f8044-107">Per avviare l'installazione del server App-V 5,1, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore.</span><span class="sxs-lookup"><span data-stu-id="f8044-107">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="f8044-108">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="f8044-108">Click **Install**.</span></span>

2.  <span data-ttu-id="f8044-109">Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f8044-109">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3.  <span data-ttu-id="f8044-110">In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).**</span><span class="sxs-lookup"><span data-stu-id="f8044-110">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="f8044-111">Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="f8044-111">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="f8044-112">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f8044-112">Click **Next**.</span></span>

4.  <span data-ttu-id="f8044-113">Nella pagina **Selezione funzionalità** selezionare la casella di **controllo server di gestione** e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f8044-113">On the **Feature Selection** page, select the **Management Server** checkbox and click **Next**.</span></span>

5.  <span data-ttu-id="f8044-114">Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="f8044-114">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6.  <span data-ttu-id="f8044-115">Nella pagina **Configura database di gestione esistente** selezionare **Usa un server SQL remoto**e digitare il nome del computer che ha eseguito Microsoft SQL SQL, ad esempio **SqlServerMachine**.</span><span class="sxs-lookup"><span data-stu-id="f8044-115">On the **Configure Existing Management Database** page, select **Use a remote SQL Server**, and type the machine name of the computer running Microsoft SQL SQL, for example **SqlServerMachine**.</span></span>

    **<span data-ttu-id="f8044-116">Nota</span><span class="sxs-lookup"><span data-stu-id="f8044-116">Note</span></span>**  
    <span data-ttu-id="f8044-117">Se Microsoft SQL Server è distribuito nello stesso server, selezionare **Usa SQL Server locale**.</span><span class="sxs-lookup"><span data-stu-id="f8044-117">If the Microsoft SQL Server is deployed on the same server, select **Use local SQL Server**.</span></span>



~~~
For the SQL Server Instance, select **Use the default instance**. If you are using a custom Microsoft SQL Server instance, you must select **Use a custom instance** and then type the name of the instance.

Specify the **SQL Server Database name** that this management server will use, for example **AppvManagement**.
~~~

7. <span data-ttu-id="f8044-118">Nella pagina **configura configurazione server di gestione** specificare il gruppo di annunci o l'account che si connetterà alla console di gestione per scopi amministrativi, ad esempio **MyDomain\\MyUser** o **MyDomain\\AdminGroup**.</span><span class="sxs-lookup"><span data-stu-id="f8044-118">On the **Configure Management Server Configuration** page, specify the AD group or account that will connect to the management console for administrative purposes for example **MyDomain\\MyUser** or **MyDomain\\AdminGroup**.</span></span> <span data-ttu-id="f8044-119">L'account o il gruppo di annunci specificato verrà abilitato per la gestione del server tramite la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="f8044-119">The account or AD group you specify will be enabled to manage the server through the management console.</span></span> <span data-ttu-id="f8044-120">Dopo l'installazione, è possibile aggiungere altri utenti o gruppi tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="f8044-120">You can add additional users or groups using the management console after installation</span></span>

   <span data-ttu-id="f8044-121">Specificare il **nome del sito Web** che si vuole usare per il servizio di gestione.</span><span class="sxs-lookup"><span data-stu-id="f8044-121">Specify the **Website Name** that you want to use for the management service.</span></span> <span data-ttu-id="f8044-122">Accettare l'impostazione predefinita se non si dispone di un nome personalizzato.</span><span class="sxs-lookup"><span data-stu-id="f8044-122">Accept the default if you do not have a custom name.</span></span> <span data-ttu-id="f8044-123">Per il **Binding della porta**, specificare un numero di porta univoco da usare, ad esempio **12345**.</span><span class="sxs-lookup"><span data-stu-id="f8044-123">For the **Port Binding**, specify a unique port number to be used, for example **12345**.</span></span>

8. <span data-ttu-id="f8044-124">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="f8044-124">Click **Install**.</span></span>

9. <span data-ttu-id="f8044-125">Per verificare che il programma di installazione sia stato completato correttamente, aprire un Web browser e digitare l'URL seguente: http://managementserver:portnumber/Console .</span><span class="sxs-lookup"><span data-stu-id="f8044-125">To confirm that the setup has completed successfully, open a web browser, and type the following URL: http://managementserver:portnumber/Console.</span></span> <span data-ttu-id="f8044-126">Se l'installazione è stata eseguita correttamente, la **console di gestione** verrà visualizzata senza messaggi di errore o avvisi visualizzati.</span><span class="sxs-lookup"><span data-stu-id="f8044-126">If the installation was successful, you should see the **Management Console** appear without any error messages or warnings being displayed.</span></span>

   <span data-ttu-id="f8044-127">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="f8044-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f8044-128">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="f8044-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f8044-129">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="f8044-129">Got an App-V issue?</span></span>** <span data-ttu-id="f8044-130">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f8044-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f8044-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8044-131">Related topics</span></span>


[<span data-ttu-id="f8044-132">Distribuzione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="f8044-132">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)









