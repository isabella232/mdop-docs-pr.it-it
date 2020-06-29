---
title: Come installare il server di pubblicazione in un computer remoto
description: Come installare il server di pubblicazione in un computer remoto
author: dansimp
ms.assetid: 37970706-54ff-4799-9485-b9b49fd50f37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d711fa51ade856b3ac5880ba60a19315c358734
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805397"
---
# <span data-ttu-id="c8b7f-103">Come installare il server di pubblicazione in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="c8b7f-103">How to Install the Publishing Server on a Remote Computer</span></span>


<span data-ttu-id="c8b7f-104">Usare la procedura seguente per installare il server di pubblicazione in un computer separato.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-104">Use the following procedure to install the publishing server on a separate computer.</span></span> <span data-ttu-id="c8b7f-105">Prima di eseguire la procedura seguente, verificare che il database e il server di gestione siano disponibili.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-105">Before you perform the following procedure, ensure the database and management server are available.</span></span>

**<span data-ttu-id="c8b7f-106">Per installare il server di pubblicazione in un computer separato</span><span class="sxs-lookup"><span data-stu-id="c8b7f-106">To install the publishing server on a separate computer</span></span>**

1. <span data-ttu-id="c8b7f-107">Copiare i file di installazione del server App-V 5,0 nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-107">Copy the App-V 5.0 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="c8b7f-108">Per avviare l'installazione del server App-V 5,0, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-108">To start the App-V 5.0 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="c8b7f-109">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-109">Click **Install**.</span></span>

2. <span data-ttu-id="c8b7f-110">Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="c8b7f-111">In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).**</span><span class="sxs-lookup"><span data-stu-id="c8b7f-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="c8b7f-112">Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-112">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="c8b7f-113">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-113">Click **Next**.</span></span>

4. <span data-ttu-id="c8b7f-114">Nella pagina **Selezione funzionalità** selezionare la casella di controllo **server di pubblicazione** e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-114">On the **Feature Selection** page, select the **Publishing Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="c8b7f-115">Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="c8b7f-116">Nella pagina **configura configurazione server di pubblicazione** specificare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8b7f-116">On the **Configure Publishing Server Configuration** page, specify the following items:</span></span>

   -   <span data-ttu-id="c8b7f-117">URL per il servizio di gestione a cui il server di pubblicazione si connette.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-117">The URL for the management service that the publishing server will connect to.</span></span> <span data-ttu-id="c8b7f-118">Ad esempio, **http://ManagementServerName:12345** .</span><span class="sxs-lookup"><span data-stu-id="c8b7f-118">For example, **http://ManagementServerName:12345**.</span></span>

   -   <span data-ttu-id="c8b7f-119">Specificare il nome del sito Web che si vuole usare per il servizio di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-119">Specify the website name that you want to use for the publishing service.</span></span> <span data-ttu-id="c8b7f-120">Accettare l'impostazione predefinita se non si dispone di un nome personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-120">Accept the default if you do not have a custom name.</span></span>

   -   <span data-ttu-id="c8b7f-121">Per il **Binding della porta**, specifica un numero di porta univoco che verrà usato da App-V 5,0, ad esempio **54321**.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-121">For the **Port Binding**, specify a unique port number that will be used by App-V 5.0, for example **54321**.</span></span>

7. <span data-ttu-id="c8b7f-122">Nella pagina **pronto per l'installazione** fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-122">On the **Ready to Install** page, click **Install**.</span></span>

8. <span data-ttu-id="c8b7f-123">Al termine dell'installazione, il server di pubblicazione deve essere registrato con il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-123">After the installation is complete, the publishing server must be registered with the management server.</span></span> <span data-ttu-id="c8b7f-124">Nella console di gestione di App-V 5,0, eseguire la procedura seguente per registrare il server:</span><span class="sxs-lookup"><span data-stu-id="c8b7f-124">In the App-V 5.0 management console, use the following steps to register the server:</span></span>

   1.  <span data-ttu-id="c8b7f-125">Aprire la console del server di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-125">Open the App-V 5.0 management server console.</span></span>

   2.  <span data-ttu-id="c8b7f-126">Nel riquadro sinistro selezionare **Server**e quindi **Registra nuovo server**.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-126">In the left pane, select **Servers**, and then select **Register New Server**.</span></span>

   3.  <span data-ttu-id="c8b7f-127">Digitare il nome del server e una descrizione (se necessario) e fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-127">Type the name of this server and a description (if required) and click **Add**.</span></span>

9. <span data-ttu-id="c8b7f-128">Per verificare se il server di pubblicazione è in uso correttamente, è consigliabile importare un pacchetto nel server di gestione, autorizzare il pacchetto a un gruppo di annunci e pubblicare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c8b7f-128">To verify if the publishing server is running correctly, you should import a package to the management server, entitle the package to an AD group, and publish the package.</span></span> <span data-ttu-id="c8b7f-129">Con un browser Internet aprire l'URL seguente: <strong> http://publishingserver:pubport </strong> .</span><span class="sxs-lookup"><span data-stu-id="c8b7f-129">Using an internet browser, open the following URL: <strong>http://publishingserver:pubport</strong>.</span></span> <span data-ttu-id="c8b7f-130">Se il server sta eseguendo correttamente le informazioni simili a quelle seguenti verranno visualizzate:</span><span class="sxs-lookup"><span data-stu-id="c8b7f-130">If the server is running correctly information similar to the following will be displayed:</span></span>

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   <span data-ttu-id="c8b7f-131">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="c8b7f-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="c8b7f-132">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="c8b7f-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="c8b7f-133">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="c8b7f-133">Got an App-V issue?</span></span>** <span data-ttu-id="c8b7f-134">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="c8b7f-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="c8b7f-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8b7f-135">Related topics</span></span>


[<span data-ttu-id="c8b7f-136">Distribuzione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="c8b7f-136">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

 

 





