---
title: Come installare il server di pubblicazione in un computer remoto
description: Come installare il server di pubblicazione in un computer remoto
author: dansimp
ms.assetid: 1c903f78-0558-458d-a149-d5f6fb55aefb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a085d68305057538228599e35dd9500957342ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805385"
---
# <span data-ttu-id="57bc6-103">Come installare il server di pubblicazione in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="57bc6-103">How to Install the Publishing Server on a Remote Computer</span></span>


<span data-ttu-id="57bc6-104">Usare la procedura seguente per installare il server di pubblicazione in un computer separato.</span><span class="sxs-lookup"><span data-stu-id="57bc6-104">Use the following procedure to install the publishing server on a separate computer.</span></span> <span data-ttu-id="57bc6-105">Prima di eseguire la procedura seguente, verificare che il database e il server di gestione siano disponibili.</span><span class="sxs-lookup"><span data-stu-id="57bc6-105">Before you perform the following procedure, ensure the database and management server are available.</span></span>

**<span data-ttu-id="57bc6-106">Per installare il server di pubblicazione in un computer separato</span><span class="sxs-lookup"><span data-stu-id="57bc6-106">To install the publishing server on a separate computer</span></span>**

1. <span data-ttu-id="57bc6-107">Copiare i file di installazione del server App-V 5,1 nel computer in cui si vuole installarlo.</span><span class="sxs-lookup"><span data-stu-id="57bc6-107">Copy the App-V 5.1 server installation files to the computer on which you want to install it on.</span></span> <span data-ttu-id="57bc6-108">Per avviare l'installazione del server App-V 5,1, fare clic con il pulsante destro del mouse ed eseguire **appv\_server\_setup.exe** come amministratore.</span><span class="sxs-lookup"><span data-stu-id="57bc6-108">To start the App-V 5.1 server installation right-click and run **appv\_server\_setup.exe** as an administrator.</span></span> <span data-ttu-id="57bc6-109">Fai clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="57bc6-109">Click **Install**.</span></span>

2. <span data-ttu-id="57bc6-110">Nella pagina **Guida introduttiva** rivedere e accettare le condizioni di licenza e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="57bc6-110">On the **Getting Started** page, review and accept the license terms, and click **Next**.</span></span>

3. <span data-ttu-id="57bc6-111">In **usare Microsoft Update per semplificare la protezione del computer e** la pagina aggiornata, per abilitare gli aggiornamenti Microsoft, selezionare **Usa Microsoft Update quando si verificano gli aggiornamenti (scelta consigliata).**</span><span class="sxs-lookup"><span data-stu-id="57bc6-111">On the **Use Microsoft Update to help keep your computer secure and up-to-date** page, to enable Microsoft updates, select **Use Microsoft Update when I check for updates (recommended).**</span></span> <span data-ttu-id="57bc6-112">Per disabilitare gli aggiornamenti Microsoft, selezionare **non si vuole usare Microsoft Update**.</span><span class="sxs-lookup"><span data-stu-id="57bc6-112">To disable Microsoft updates, select **I don’t want to use Microsoft Update**.</span></span> <span data-ttu-id="57bc6-113">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="57bc6-113">Click **Next**.</span></span>

4. <span data-ttu-id="57bc6-114">Nella pagina **Selezione funzionalità** selezionare la casella di controllo **server di pubblicazione** e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="57bc6-114">On the **Feature Selection** page, select the **Publishing Server** checkbox and click **Next**.</span></span>

5. <span data-ttu-id="57bc6-115">Nella pagina **posizione di installazione** accettare il percorso predefinito e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="57bc6-115">On the **Installation Location** page, accept the default location and click **Next**.</span></span>

6. <span data-ttu-id="57bc6-116">Nella pagina **configura configurazione server di pubblicazione** specificare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="57bc6-116">On the **Configure Publishing Server Configuration** page, specify the following items:</span></span>

   -   <span data-ttu-id="57bc6-117">URL per il servizio di gestione a cui il server di pubblicazione si connette.</span><span class="sxs-lookup"><span data-stu-id="57bc6-117">The URL for the management service that the publishing server will connect to.</span></span> <span data-ttu-id="57bc6-118">Ad esempio, **http://ManagementServerName:12345** .</span><span class="sxs-lookup"><span data-stu-id="57bc6-118">For example, **http://ManagementServerName:12345**.</span></span>

   -   <span data-ttu-id="57bc6-119">Specificare il nome del sito Web che si vuole usare per il servizio di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="57bc6-119">Specify the website name that you want to use for the publishing service.</span></span> <span data-ttu-id="57bc6-120">Accettare l'impostazione predefinita se non si dispone di un nome personalizzato.</span><span class="sxs-lookup"><span data-stu-id="57bc6-120">Accept the default if you do not have a custom name.</span></span>

   -   <span data-ttu-id="57bc6-121">Per il **Binding della porta**, specifica un numero di porta univoco che verrà usato da App-V 5,1, ad esempio **54321**.</span><span class="sxs-lookup"><span data-stu-id="57bc6-121">For the **Port Binding**, specify a unique port number that will be used by App-V 5.1, for example **54321**.</span></span>

7. <span data-ttu-id="57bc6-122">Nella pagina **pronto per l'installazione** fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="57bc6-122">On the **Ready to Install** page, click **Install**.</span></span>

8. <span data-ttu-id="57bc6-123">Al termine dell'installazione, il server di pubblicazione deve essere registrato con il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="57bc6-123">After the installation is complete, the publishing server must be registered with the management server.</span></span> <span data-ttu-id="57bc6-124">Nella console di gestione di App-V 5,1, eseguire la procedura seguente per registrare il server:</span><span class="sxs-lookup"><span data-stu-id="57bc6-124">In the App-V 5.1 management console, use the following steps to register the server:</span></span>

   1.  <span data-ttu-id="57bc6-125">Aprire la console del server di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="57bc6-125">Open the App-V 5.1 management server console.</span></span>

   2.  <span data-ttu-id="57bc6-126">Nel riquadro sinistro selezionare **Server**e quindi **Registra nuovo server**.</span><span class="sxs-lookup"><span data-stu-id="57bc6-126">In the left pane, select **Servers**, and then select **Register New Server**.</span></span>

   3.  <span data-ttu-id="57bc6-127">Digitare il nome del server e una descrizione (se necessario) e fare clic su **Aggiungi**.</span><span class="sxs-lookup"><span data-stu-id="57bc6-127">Type the name of this server and a description (if required) and click **Add**.</span></span>

9. <span data-ttu-id="57bc6-128">Per verificare se il server di pubblicazione è in uso correttamente, è consigliabile importare un pacchetto nel server di gestione, autorizzare il pacchetto a un gruppo di annunci e pubblicare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="57bc6-128">To verify if the publishing server is running correctly, you should import a package to the management server, entitle the package to an AD group, and publish the package.</span></span> <span data-ttu-id="57bc6-129">Con un browser Internet aprire l'URL seguente: <strong> http://publishingserver:pubport </strong> .</span><span class="sxs-lookup"><span data-stu-id="57bc6-129">Using an internet browser, open the following URL: <strong>http://publishingserver:pubport</strong>.</span></span> <span data-ttu-id="57bc6-130">Se il server sta eseguendo correttamente le informazioni simili a quelle seguenti verranno visualizzate:</span><span class="sxs-lookup"><span data-stu-id="57bc6-130">If the server is running correctly information similar to the following will be displayed:</span></span>

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

   <span data-ttu-id="57bc6-131">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="57bc6-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="57bc6-132">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="57bc6-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="57bc6-133">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="57bc6-133">Got an App-V issue?</span></span>** <span data-ttu-id="57bc6-134">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="57bc6-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="57bc6-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57bc6-135">Related topics</span></span>


[<span data-ttu-id="57bc6-136">Distribuzione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="57bc6-136">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

 

 





