---
title: Come configurare il client per ricevere aggiornamenti dei gruppi di pacchetti e connessioni dal server di pubblicazione
description: Come configurare il client per ricevere aggiornamenti dei gruppi di pacchetti e connessioni dal server di pubblicazione
author: dansimp
ms.assetid: f5dfd96d-4b63-468c-8d93-9dfdf47c28fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e9df1f8b324430449d8d1dd3624d9f1157968a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805691"
---
# <span data-ttu-id="f7a74-103">Come configurare il client per ricevere aggiornamenti dei gruppi di pacchetti e connessioni dal server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="f7a74-103">How to Configure the Client to Receive Package and Connection Groups Updates From the Publishing Server</span></span>


<span data-ttu-id="f7a74-104">La distribuzione di pacchetti e gruppi di connessioni tramite il server di pubblicazione App-V 5,0 è utile perché offre una gestione a punti singoli e una elevata scalabilità.</span><span class="sxs-lookup"><span data-stu-id="f7a74-104">Deploying packages and connection groups using the App-V 5.0 publishing server is helpful because it offers single-point management and high scalability.</span></span>

<span data-ttu-id="f7a74-105">Usare la procedura seguente per configurare il client App-V 5,0 per ricevere gli aggiornamenti dal server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="f7a74-105">Use the following steps to configure the App-V 5.0 client to receive updates from the publishing server.</span></span>

<span data-ttu-id="f7a74-106">**Nota**  Per le procedure seguenti, il server di gestione è stato installato in un computer denominato **MyMgmtSrv**e il server di pubblicazione è stato installato in un computer denominato **MyPubSrv**.</span><span class="sxs-lookup"><span data-stu-id="f7a74-106">**Note** For the following procedures the management server was installed on a computer named **MyMgmtSrv**, and the publishing server was installed on a computer named **MyPubSrv**.</span></span>

 

**<span data-ttu-id="f7a74-107">Per configurare il client App-V 5,0 per ricevere gli aggiornamenti dal server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="f7a74-107">To configure the App-V 5.0 client to receive updates from the publishing server</span></span>**

1.  <span data-ttu-id="f7a74-108">Distribuire i server di gestione e pubblicazione di App-V 5,0 e aggiungere i pacchetti e i gruppi di connessioni necessari.</span><span class="sxs-lookup"><span data-stu-id="f7a74-108">Deploy the App-V 5.0 management and publishing servers, and add the required packages and connection groups.</span></span> <span data-ttu-id="f7a74-109">Per altre informazioni sull'aggiunta di pacchetti e di gruppi di connessioni, vedere [come aggiungere o aggiornare pacchetti tramite la console di gestione](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) e [come creare un gruppo di connessioni](how-to-create-a-connection-group.md).</span><span class="sxs-lookup"><span data-stu-id="f7a74-109">For more information about adding packages and connection groups, see [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Create a Connection Group](how-to-create-a-connection-group.md).</span></span>

2.  <span data-ttu-id="f7a74-110">Per aprire la console di gestione, fare clic sul collegamento seguente, aprire un browser e digitare quanto segue: http://MyMgmtSrv/AppvManagement/Console.html in un Web browser e importare, pubblicare e autorizzare tutti i pacchetti e i gruppi di connessioni che saranno necessari per un determinato set di utenti.</span><span class="sxs-lookup"><span data-stu-id="f7a74-110">To open the management console click the following link, open a browser and type the following: http://MyMgmtSrv/AppvManagement/Console.html in a web browser, and import, publish, and entitle all the packages and connection groups which will be necessary for a particular set of users.</span></span>

3.  <span data-ttu-id="f7a74-111">Nel computer che esegue il client App-V 5,0 aprire un prompt dei comandi di PowerShell con privilegi elevati, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f7a74-111">On the computer running the App-V 5.0 client, open an elevated PowerShell command prompt, run the following command:</span></span>

    **<span data-ttu-id="f7a74-112">Add-AppvPublishingServer-Name ABC-URL http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="f7a74-112">Add-AppvPublishingServer -Name ABC -URL http:// MyPubSrv/AppvPublishing</span></span>**

    <span data-ttu-id="f7a74-113">Questo comando consente di configurare il server di pubblicazione specificato.</span><span class="sxs-lookup"><span data-stu-id="f7a74-113">This command will configure the specified publishing server.</span></span> <span data-ttu-id="f7a74-114">Dovrebbe essere visualizzato l'output simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="f7a74-114">You should see output similar to the following:</span></span>

    <span data-ttu-id="f7a74-115">ID: 1</span><span class="sxs-lookup"><span data-stu-id="f7a74-115">Id : 1</span></span>

    <span data-ttu-id="f7a74-116">SetByGroupPolicy: false</span><span class="sxs-lookup"><span data-stu-id="f7a74-116">SetByGroupPolicy : False</span></span>

    <span data-ttu-id="f7a74-117">Nome: ABC</span><span class="sxs-lookup"><span data-stu-id="f7a74-117">Name : ABC</span></span>

    <span data-ttu-id="f7a74-118">URL: http://MyPubSrv/AppvPublishing</span><span class="sxs-lookup"><span data-stu-id="f7a74-118">URL : http:// MyPubSrv/AppvPublishing</span></span>

    <span data-ttu-id="f7a74-119">GlobalRefreshEnabled: false</span><span class="sxs-lookup"><span data-stu-id="f7a74-119">GlobalRefreshEnabled : False</span></span>

    <span data-ttu-id="f7a74-120">GlobalRefreshOnLogon: false</span><span class="sxs-lookup"><span data-stu-id="f7a74-120">GlobalRefreshOnLogon : False</span></span>

    <span data-ttu-id="f7a74-121">GlobalRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="f7a74-121">GlobalRefreshInterval : 0</span></span>

    <span data-ttu-id="f7a74-122">GlobalRefreshIntervalUnit: giorno</span><span class="sxs-lookup"><span data-stu-id="f7a74-122">GlobalRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="f7a74-123">UserRefreshEnabled: vero</span><span class="sxs-lookup"><span data-stu-id="f7a74-123">UserRefreshEnabled : True</span></span>

    <span data-ttu-id="f7a74-124">UserRefreshOnLogon: vero</span><span class="sxs-lookup"><span data-stu-id="f7a74-124">UserRefreshOnLogon : True</span></span>

    <span data-ttu-id="f7a74-125">UserRefreshInterval: 0</span><span class="sxs-lookup"><span data-stu-id="f7a74-125">UserRefreshInterval : 0</span></span>

    <span data-ttu-id="f7a74-126">UserRefreshIntervalUnit: giorno</span><span class="sxs-lookup"><span data-stu-id="f7a74-126">UserRefreshIntervalUnit : Day</span></span>

    <span data-ttu-id="f7a74-127">ID restituito: in questo caso 1</span><span class="sxs-lookup"><span data-stu-id="f7a74-127">The returned Id – in this case 1</span></span>

4.  <span data-ttu-id="f7a74-128">Nel computer che gestisce il client App-V 5,0 aprire un prompt dei comandi di PowerShell e digitare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f7a74-128">On the computer running the App-V 5.0 client, open a PowerShell command prompt, and type the following command:</span></span>

    **<span data-ttu-id="f7a74-129">Sincronizzazione-AppvPublishingServer-ServerId 1</span><span class="sxs-lookup"><span data-stu-id="f7a74-129">Sync-AppvPublishingServer -ServerId 1</span></span>**

    <span data-ttu-id="f7a74-130">Il comando esegue una query sul server di pubblicazione per i pacchetti e i gruppi di connessioni che devono essere aggiunti o rimossi per questo particolare client in base ai diritti per i pacchetti e i gruppi di connessioni configurati nel server di gestione.</span><span class="sxs-lookup"><span data-stu-id="f7a74-130">The command will query the publishing server for the packages and connection groups that need to be added or removed for this particular client based on the entitlements for the packages and connection groups as configured on the management server.</span></span>

    <span data-ttu-id="f7a74-131">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="f7a74-131">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="f7a74-132">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="f7a74-132">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="f7a74-133">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="f7a74-133">Got an App-V issue?</span></span>** <span data-ttu-id="f7a74-134">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="f7a74-134">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="f7a74-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7a74-135">Related topics</span></span>


[<span data-ttu-id="f7a74-136">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f7a74-136">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





