---
title: Come abilitare la creazione di report nel client App-V 5.1 con PowerShell
description: Come abilitare la creazione di report nel client App-V 5.1 con PowerShell
author: dansimp
ms.assetid: c4c58be6-cc50-44f6-bf4f-8346fc5d0c0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1d8c0d5e1930020ed1ce354f806f8917a9644e02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805452"
---
# <span data-ttu-id="9a43f-103">Come abilitare la creazione di report nel client App-V 5.1 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9a43f-103">How to Enable Reporting on the App-V 5.1 Client by Using PowerShell</span></span>


<span data-ttu-id="9a43f-104">Usare la procedura seguente per configurare l'App V 5,1 per la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="9a43f-104">Use the following procedure to configure the App-V 5.1 for reporting.</span></span>

**<span data-ttu-id="9a43f-105">Per configurare il computer in cui è in uso il client App-V 5,1 per la creazione di report</span><span class="sxs-lookup"><span data-stu-id="9a43f-105">To configure the computer running the App-V 5.1 client for reporting</span></span>**

1. <span data-ttu-id="9a43f-106">Installare il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="9a43f-106">Install the App-V 5.1 client.</span></span> <span data-ttu-id="9a43f-107">Per altre informazioni sull'installazione del client [, vedere come distribuire il client App-V](how-to-deploy-the-app-v-client-51gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="9a43f-107">For more information about installing the client see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md).</span></span>

2. <span data-ttu-id="9a43f-108">Dopo aver installato il client App-V 5,1, usare la versione **set-AppvClientConfiguration** di PowerShell per configurare le impostazioni di configurazione della creazione di report appropriate:</span><span class="sxs-lookup"><span data-stu-id="9a43f-108">After you have installed the App-V 5.1 client, use the **Set-AppvClientConfiguration** PowerShell to configure appropriate Reporting Configuration settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="9a43f-109">Impostazione</span><span class="sxs-lookup"><span data-stu-id="9a43f-109">Setting</span></span></th>
   <th align="left"><span data-ttu-id="9a43f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a43f-110">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="9a43f-111">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="9a43f-111">ReportingEnabled</span></span></p></td>
   <td align="left"><p><span data-ttu-id="9a43f-112">Consente al client di restituire informazioni a un server di report.</span><span class="sxs-lookup"><span data-stu-id="9a43f-112">Enables the client to return information to a reporting server.</span></span> <span data-ttu-id="9a43f-113">Questa impostazione è necessaria per il client per raccogliere i dati dei report nel client.</span><span class="sxs-lookup"><span data-stu-id="9a43f-113">This setting is required for the client to collect the reporting data on the client.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="9a43f-114">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="9a43f-114">ReportingServerURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="9a43f-115">Specifica la posizione nel server di report in cui vengono salvate le informazioni sul client.</span><span class="sxs-lookup"><span data-stu-id="9a43f-115">Specifies the location on the reporting server where client information is saved.</span></span> <span data-ttu-id="9a43f-116">Ad esempio, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</span><span class="sxs-lookup"><span data-stu-id="9a43f-116">For example, http://&lt;reportingservername&gt;:&lt;reportingportnumber&gt;.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="9a43f-117">Nota</span><span class="sxs-lookup"><span data-stu-id="9a43f-117">Note</span></span></strong><br/><p><span data-ttu-id="9a43f-118">Questo è il numero di porta assegnato durante la configurazione del server di Reporting</span><span class="sxs-lookup"><span data-stu-id="9a43f-118">This is the port number that was assigned during the Reporting Server setup</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="9a43f-119">Ora di inizio della segnalazione</span><span class="sxs-lookup"><span data-stu-id="9a43f-119">Reporting Start Time</span></span></p></td>
   <td align="left"><p><span data-ttu-id="9a43f-120">Questa operazione è impostata per pianificare il client per inviare automaticamente i dati al server.</span><span class="sxs-lookup"><span data-stu-id="9a43f-120">This is set to schedule the client to automatically send the data to the server.</span></span> <span data-ttu-id="9a43f-121">Questa impostazione indicherà l'ora in cui inizieranno a inviare i dati dei report.</span><span class="sxs-lookup"><span data-stu-id="9a43f-121">This setting will indicate the hour at which the reporting data will start to send.</span></span> <span data-ttu-id="9a43f-122">È nel formato 24 ore e prenderà un numero compreso tra 0-23.</span><span class="sxs-lookup"><span data-stu-id="9a43f-122">It is in the 24 hour format and will take a number between 0-23.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="9a43f-123">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="9a43f-123">ReportingRandomDelay</span></span></p></td>
   <td align="left"><p><span data-ttu-id="9a43f-124">Specifica il ritardo massimo (in minuti) per l'invio dei dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="9a43f-124">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="9a43f-125">Quando l'attività pianificata viene avviata, il client genera un ritardo casuale compreso tra 0 e ReportingRandomDelay e attenderà la durata specificata prima di inviare i dati.</span><span class="sxs-lookup"><span data-stu-id="9a43f-125">When the scheduled task is started, the client generates a random delay between 0 and ReportingRandomDelay and will wait the specified duration before sending data.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="9a43f-126">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="9a43f-126">ReportingInterval</span></span></p></td>
   <td align="left"><p><span data-ttu-id="9a43f-127">Specifica l'intervallo di tentativi che il client userà per rinviare i dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="9a43f-127">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="9a43f-128">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="9a43f-128">ReportingDataCacheLimit</span></span></p></td>
   <td align="left"><p><span data-ttu-id="9a43f-129">Specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report.</span><span class="sxs-lookup"><span data-stu-id="9a43f-129">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="9a43f-130">Le dimensioni si applicano alla cache in memoria.</span><span class="sxs-lookup"><span data-stu-id="9a43f-130">The size applies to the cache in memory.</span></span> <span data-ttu-id="9a43f-131">Quando viene raggiunto il limite, il file di log verrà ribaltato.</span><span class="sxs-lookup"><span data-stu-id="9a43f-131">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="9a43f-132">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="9a43f-132">ReportingDataBlockSize</span></span></p></td>
   <td align="left"><p><span data-ttu-id="9a43f-133">Specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report.</span><span class="sxs-lookup"><span data-stu-id="9a43f-133">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="9a43f-134">Le dimensioni si applicano alla cache in memoria.</span><span class="sxs-lookup"><span data-stu-id="9a43f-134">The size applies to the cache in memory.</span></span> <span data-ttu-id="9a43f-135">Quando viene raggiunto il limite, il file di log verrà ribaltato.</span><span class="sxs-lookup"><span data-stu-id="9a43f-135">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="9a43f-136">Dopo aver configurato le impostazioni appropriate, il computer che gestisce il client App-V 5,1 raccoglierà automaticamente i dati e invierà i dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="9a43f-136">After the appropriate settings have been configured, the computer running the App-V 5.1 client will automatically collect data and will send the data back to the reporting server.</span></span>

   <span data-ttu-id="9a43f-137">Gli amministratori possono inoltre restituire manualmente i dati in modo su richiesta usando il cmdlet di PowerShell **Send-AppvClientReport** .</span><span class="sxs-lookup"><span data-stu-id="9a43f-137">Additionally, administrators can manually send the data back in an on-demand manner using the **Send-AppvClientReport** PowerShell cmdlet.</span></span>

   <span data-ttu-id="9a43f-138">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="9a43f-138">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="9a43f-139">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="9a43f-139">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="9a43f-140">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="9a43f-140">Got an App-V issue?</span></span>** <span data-ttu-id="9a43f-141">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="9a43f-141">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="9a43f-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a43f-142">Related topics</span></span>


[<span data-ttu-id="9a43f-143">Amministrazione di App-V 5.1 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9a43f-143">Administering App-V 5.1 by Using PowerShell</span></span>](administering-app-v-51-by-using-powershell.md)









