---
title: Come abilitare la creazione di report nel client App-V 5.0 con PowerShell
description: Come abilitare la creazione di report nel client App-V 5.0 con PowerShell
author: dansimp
ms.assetid: a7aaf553-0f83-4cd0-8df8-93a5f1ebe497
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c004b4900a9814a11cb2706659a2edb99de6cc1b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805464"
---
# <span data-ttu-id="bd61a-103">Come abilitare la creazione di report nel client App-V 5.0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd61a-103">How to Enable Reporting on the App-V 5.0 Client by Using PowerShell</span></span>


<span data-ttu-id="bd61a-104">Usare la procedura seguente per configurare l'App V 5,0 per la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="bd61a-104">Use the following procedure to configure the App-V 5.0 for reporting.</span></span>

**<span data-ttu-id="bd61a-105">Per configurare il computer in cui è in uso il client App-V 5,0 per la creazione di report</span><span class="sxs-lookup"><span data-stu-id="bd61a-105">To configure the computer running the App-V 5.0 client for reporting</span></span>**

1. <span data-ttu-id="bd61a-106">Installare il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="bd61a-106">Install the App-V 5.0 client.</span></span> <span data-ttu-id="bd61a-107">Per altre informazioni sull'installazione del client [, vedere come distribuire il client App-V](how-to-deploy-the-app-v-client-gb18030.md).</span><span class="sxs-lookup"><span data-stu-id="bd61a-107">For more information about installing the client see [How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md).</span></span>

2. <span data-ttu-id="bd61a-108">Dopo aver installato il client App-V 5,0, usare la versione **set-AppvClientConfiguration** di PowerShell per configurare le impostazioni di configurazione della creazione di report appropriate:</span><span class="sxs-lookup"><span data-stu-id="bd61a-108">After you have installed the App-V 5.0 client, use the **Set-AppvClientConfiguration** PowerShell to configure appropriate Reporting Configuration settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="bd61a-109">Impostazione</span><span class="sxs-lookup"><span data-stu-id="bd61a-109">Setting</span></span></th>
   <th align="left"><span data-ttu-id="bd61a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd61a-110">Description</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="bd61a-111">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="bd61a-111">ReportingEnabled</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd61a-112">Consente al client di restituire informazioni a un server di report.</span><span class="sxs-lookup"><span data-stu-id="bd61a-112">Enables the client to return information to a reporting server.</span></span> <span data-ttu-id="bd61a-113">Questa impostazione è necessaria per il client per raccogliere i dati dei report nel client.</span><span class="sxs-lookup"><span data-stu-id="bd61a-113">This setting is required for the client to collect the reporting data on the client.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="bd61a-114">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="bd61a-114">ReportingServerURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd61a-115">Specifica la posizione nel server di report in cui vengono salvate le informazioni sul client.</span><span class="sxs-lookup"><span data-stu-id="bd61a-115">Specifies the location on the reporting server where client information is saved.</span></span> <span data-ttu-id="bd61a-116">Ad esempio, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</span><span class="sxs-lookup"><span data-stu-id="bd61a-116">For example, http://&lt;reportingservername&gt;:&lt;reportingportnumber&gt;.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="bd61a-117">Nota</span><span class="sxs-lookup"><span data-stu-id="bd61a-117">Note</span></span></strong><br/><p><span data-ttu-id="bd61a-118">Questo è il numero di porta assegnato durante la configurazione del server di Reporting</span><span class="sxs-lookup"><span data-stu-id="bd61a-118">This is the port number that was assigned during the Reporting Server setup</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="bd61a-119">Ora di inizio della segnalazione</span><span class="sxs-lookup"><span data-stu-id="bd61a-119">Reporting Start Time</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd61a-120">Questa operazione è impostata per pianificare il client per inviare automaticamente i dati al server.</span><span class="sxs-lookup"><span data-stu-id="bd61a-120">This is set to schedule the client to automatically send the data to the server.</span></span> <span data-ttu-id="bd61a-121">Questa impostazione indicherà l'ora in cui inizieranno a inviare i dati dei report.</span><span class="sxs-lookup"><span data-stu-id="bd61a-121">This setting will indicate the hour at which the reporting data will start to send.</span></span> <span data-ttu-id="bd61a-122">È nel formato 24 ore e prenderà un numero compreso tra 0-23.</span><span class="sxs-lookup"><span data-stu-id="bd61a-122">It is in the 24 hour format and will take a number between 0-23.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="bd61a-123">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="bd61a-123">ReportingRandomDelay</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd61a-124">Specifica il ritardo massimo (in minuti) per l'invio dei dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="bd61a-124">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="bd61a-125">Quando l'attività pianificata viene avviata, il client genera un ritardo casuale compreso tra 0 e ReportingRandomDelay e attenderà la durata specificata prima di inviare i dati.</span><span class="sxs-lookup"><span data-stu-id="bd61a-125">When the scheduled task is started, the client generates a random delay between 0 and ReportingRandomDelay and will wait the specified duration before sending data.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="bd61a-126">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="bd61a-126">ReportingInterval</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd61a-127">Specifica l'intervallo di tentativi che il client userà per rinviare i dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="bd61a-127">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="bd61a-128">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="bd61a-128">ReportingDataCacheLimit</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd61a-129">Specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report.</span><span class="sxs-lookup"><span data-stu-id="bd61a-129">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="bd61a-130">Le dimensioni si applicano alla cache in memoria.</span><span class="sxs-lookup"><span data-stu-id="bd61a-130">The size applies to the cache in memory.</span></span> <span data-ttu-id="bd61a-131">Quando viene raggiunto il limite, il file di log verrà ribaltato.</span><span class="sxs-lookup"><span data-stu-id="bd61a-131">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="bd61a-132">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="bd61a-132">ReportingDataBlockSize</span></span></p></td>
   <td align="left"><p><span data-ttu-id="bd61a-133">Specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report.</span><span class="sxs-lookup"><span data-stu-id="bd61a-133">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="bd61a-134">Le dimensioni si applicano alla cache in memoria.</span><span class="sxs-lookup"><span data-stu-id="bd61a-134">The size applies to the cache in memory.</span></span> <span data-ttu-id="bd61a-135">Quando viene raggiunto il limite, il file di log verrà ribaltato.</span><span class="sxs-lookup"><span data-stu-id="bd61a-135">When the limit is reached, the log file will roll over.</span></span></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="bd61a-136">Dopo aver configurato le impostazioni appropriate, il computer che gestisce il client App-V 5,0 raccoglierà automaticamente i dati e invierà i dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="bd61a-136">After the appropriate settings have been configured, the computer running the App-V 5.0 client will automatically collect data and will send the data back to the reporting server.</span></span>

   <span data-ttu-id="bd61a-137">Gli amministratori possono inoltre restituire manualmente i dati in modo su richiesta usando il cmdlet di PowerShell **Send-AppvClientReport** .</span><span class="sxs-lookup"><span data-stu-id="bd61a-137">Additionally, administrators can manually send the data back in an on-demand manner using the **Send-AppvClientReport** PowerShell cmdlet.</span></span>

   <span data-ttu-id="bd61a-138">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="bd61a-138">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="bd61a-139">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="bd61a-139">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="bd61a-140">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="bd61a-140">Got an App-V issue?</span></span>** <span data-ttu-id="bd61a-141">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="bd61a-141">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="bd61a-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd61a-142">Related topics</span></span>


[<span data-ttu-id="bd61a-143">Amministrazione di App-V con PowerShell</span><span class="sxs-lookup"><span data-stu-id="bd61a-143">Administering App-V by Using PowerShell</span></span>](administering-app-v-by-using-powershell.md)









