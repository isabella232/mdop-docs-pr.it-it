---
title: Come distribuire i database App-V con script SQL
description: Come distribuire i database App-V con script SQL
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805482"
---
# <span data-ttu-id="8cf28-103">Come distribuire i database App-V con script SQL</span><span class="sxs-lookup"><span data-stu-id="8cf28-103">How to Deploy the App-V Databases by Using SQL Scripts</span></span>


<span data-ttu-id="8cf28-104">Seguire le istruzioni seguenti per usare gli script SQL, invece di Windows Installer, per:</span><span class="sxs-lookup"><span data-stu-id="8cf28-104">Use the following instructions to use SQL scripts, rather than the Windows Installer, to:</span></span>

-   <span data-ttu-id="8cf28-105">Installare i database di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="8cf28-105">Install the App-V 5.0 databases</span></span>

-   <span data-ttu-id="8cf28-106">Aggiornare i database di 5,0 a una versione successiva</span><span class="sxs-lookup"><span data-stu-id="8cf28-106">Upgrade the 5.0 databases to a later version</span></span>

**<span data-ttu-id="8cf28-107">Come installare i database di App-V usando gli script SQL</span><span class="sxs-lookup"><span data-stu-id="8cf28-107">How to install the App-V databases by using SQL scripts</span></span>**

1. <span data-ttu-id="8cf28-108">Prima di installare gli script di database, rivedere e conservare una copia delle condizioni di licenza di App-V.</span><span class="sxs-lookup"><span data-stu-id="8cf28-108">Before you install the database scripts, review and keep a copy of the App-V license terms.</span></span> <span data-ttu-id="8cf28-109">Eseguendo gli script del database si accettano le condizioni di licenza.</span><span class="sxs-lookup"><span data-stu-id="8cf28-109">By running the database scripts, you are agreeing to the license terms.</span></span> <span data-ttu-id="8cf28-110">Se non è possibile accettarli, non usare questo software.</span><span class="sxs-lookup"><span data-stu-id="8cf28-110">If you do not accept them, you should not use this software.</span></span>

2. <span data-ttu-id="8cf28-111">Copiare il **appv\_server\_setup.exe** dal supporto per la versione di App-V in un percorso temporaneo.</span><span class="sxs-lookup"><span data-stu-id="8cf28-111">Copy the **appv\_server\_setup.exe** from the App-V release media to a temporary location.</span></span>

3. <span data-ttu-id="8cf28-112">Da un prompt dei comandi eseguire **appv\_server\_setup.exe** e specificare una posizione temporanea per l'estrazione degli script di database.</span><span class="sxs-lookup"><span data-stu-id="8cf28-112">From a command prompt, run **appv\_server\_setup.exe** and specify a temporary location for extracting the database scripts.</span></span>

   <span data-ttu-id="8cf28-113">Esempio: appv\_server\_setup.exe/layout c:\\ &lt; percorso temporaneo&gt;</span><span class="sxs-lookup"><span data-stu-id="8cf28-113">Example: appv\_server\_setup.exe /layout c:\\&lt;temporary location path&gt;</span></span>

4. <span data-ttu-id="8cf28-114">Passare al percorso temporaneo creato, aprire la cartella **DatabaseScripts** estratta e rivedere il file Readme.txt appropriato per le istruzioni:</span><span class="sxs-lookup"><span data-stu-id="8cf28-114">Browse to the temporary location that you created, open the extracted **DatabaseScripts** folder, and review the appropriate Readme.txt file for instructions:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="8cf28-115">Database</span><span class="sxs-lookup"><span data-stu-id="8cf28-115">Database</span></span></th>
   <th align="left"><span data-ttu-id="8cf28-116">Posizione del file Readme.txt da usare</span><span class="sxs-lookup"><span data-stu-id="8cf28-116">Location of Readme.txt file to use</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="8cf28-117">Database di gestione</span><span class="sxs-lookup"><span data-stu-id="8cf28-117">Management database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="8cf28-118">Sottocartella ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="8cf28-118">ManagementDatabase subfolder</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="8cf28-119">Importante</span><span class="sxs-lookup"><span data-stu-id="8cf28-119">Important</span></span></strong><br/><p><span data-ttu-id="8cf28-120">Se si esegue l'aggiornamento o l'installazione del database di gestione di App-V 5,0 SP3, vedere <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> script SQL per installare o aggiornare il database del server di gestione di App-v 5,0 SP3 Fail </a> .</span><span class="sxs-lookup"><span data-stu-id="8cf28-120">If you are upgrading to or installing the App-V 5.0 SP3 Management database, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="8cf28-121">Database di report</span><span class="sxs-lookup"><span data-stu-id="8cf28-121">Reporting database</span></span></p></td>
   <td align="left"><p><span data-ttu-id="8cf28-122">Sottocartella ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="8cf28-122">ReportingDatabase subfolder</span></span></p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="8cf28-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8cf28-123">Related topics</span></span>


[<span data-ttu-id="8cf28-124">Distribuzione del server App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="8cf28-124">Deploying the App-V 5.0 Server</span></span>](deploying-the-app-v-50-server.md)

[<span data-ttu-id="8cf28-125">Come distribuire il server App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="8cf28-125">How to Deploy the App-V 5.0 Server</span></span>](how-to-deploy-the-app-v-50-server-50sp3.md)









