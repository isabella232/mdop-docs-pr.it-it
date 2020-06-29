---
title: Risoluzione dei problemi di MED-V con il toolkit di amministrazione
description: Risoluzione dei problemi di MED-V con il toolkit di amministrazione
author: dansimp
ms.assetid: 6c096a1c-b9ce-4ec7-8dfd-5286e3b9a617
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1eaa493e5603e8a1275a6ff5f189739b168f319
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825375"
---
# <span data-ttu-id="ecb43-103">Risoluzione dei problemi di MED-V con il toolkit di amministrazione</span><span class="sxs-lookup"><span data-stu-id="ecb43-103">Troubleshooting MED-V by Using the Administration Toolkit</span></span>


<span data-ttu-id="ecb43-104">Usare il Toolkit di amministrazione MED-V per risolvere alcuni problemi di un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="ecb43-104">Use the MED-V Administration Toolkit to troubleshoot certain problems in a MED-V workspace.</span></span> <span data-ttu-id="ecb43-105">Il Toolkit di amministrazione MED-V consente di accedere e configurare i registri eventi, riavviare o reimpostare l'area di lavoro MED-V e visualizzare le applicazioni pubblicate e gli indirizzi Web reindirizzati nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="ecb43-105">The MED-V Administration Toolkit lets you access and configure event logs, restart or reset the MED-V workspace, and view the published applications and redirected web addresses in the MED-V workspace.</span></span> <span data-ttu-id="ecb43-106">È anche possibile usare il Toolkit di amministrazione MED-V per aprire la macchina virtuale dell'area di lavoro MED-V in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="ecb43-106">You can also use the MED-V Administration Toolkit to open the MED-V workspace virtual machine in full-screen mode.</span></span>

## <span data-ttu-id="ecb43-107">Per aprire il Toolkit di amministrazione di MED-V</span><span class="sxs-lookup"><span data-stu-id="ecb43-107">To Open the MED-V Administration Toolkit</span></span>


<span data-ttu-id="ecb43-108">Per aprire il Toolkit di amministrazione di MED-V, eseguire la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="ecb43-108">Perform the following steps to open the MED-V Administration Toolkit:</span></span>

1.  <span data-ttu-id="ecb43-109">Nel computer host che contiene l'area di lavoro MED-V che si sta risolvendo, aprire una finestra del prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="ecb43-109">On the host computer that contains the MED-V workspace you are troubleshooting, open a Command Prompt window.</span></span>

2.  <span data-ttu-id="ecb43-110">Passare a%systemdrive%\\Program \\Programmi\\microsoft Enterprise Desktop Virtualization.</span><span class="sxs-lookup"><span data-stu-id="ecb43-110">Browse to %systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization.</span></span>

3.  <span data-ttu-id="ecb43-111">Al prompt dei comandi digitare **MedvHost/Toolkit**.</span><span class="sxs-lookup"><span data-stu-id="ecb43-111">At the command prompt, type **MedvHost /toolkit**.</span></span>

<span data-ttu-id="ecb43-112">Dopo l'apertura del Toolkit di amministrazione di MED-V, è possibile usare il Toolkit per risolvere i problemi nell'area di lavoro MED-V trovata durante la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="ecb43-112">After the MED-V Administration Toolkit opens, you can use the toolkit to help resolve issues in the MED-V workspace found during troubleshooting.</span></span>

## <span data-ttu-id="ecb43-113">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ecb43-113">In this Section</span></span>


<a href="" id="viewing-and-configuring-med-v-logs"></a>[<span data-ttu-id="ecb43-114">Visualizzazione e configurazione dei log MED-V</span><span class="sxs-lookup"><span data-stu-id="ecb43-114">Viewing and Configuring MED-V Logs</span></span>](viewing-and-configuring-med-v-logs.md)  
<span data-ttu-id="ecb43-115">Descrive come usare il Toolkit di amministrazione MED-V per raccogliere e gestire i registri eventi MED-V nel computer host e nella macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="ecb43-115">Describes how to use the MED-V Administration Toolkit to collect and manage MED-V event logs in the host computer and the guest virtual machine.</span></span>

<a href="" id="restarting-and-resetting-a-med-v-workspace"></a>[<span data-ttu-id="ecb43-116">Riavvio e ripristino di un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="ecb43-116">Restarting and Resetting a MED-V Workspace</span></span>](restarting-and-resetting-a-med-v-workspace.md)  
<span data-ttu-id="ecb43-117">Descrive come riavviare e reimpostare le aree di lavoro MED-V usando il Toolkit di amministrazione MED-V.</span><span class="sxs-lookup"><span data-stu-id="ecb43-117">Describes how to restart and reset MED-V workspaces by using the MED-V Administration Toolkit.</span></span>

<a href="" id="viewing-med-v-workspace-configurations"></a>[<span data-ttu-id="ecb43-118">Visualizzazione delle configurazioni dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="ecb43-118">Viewing MED-V Workspace Configurations</span></span>](viewing-med-v-workspace-configurations.md)  
<span data-ttu-id="ecb43-119">Descrive come usare il Toolkit di amministrazione MED-V per visualizzare le applicazioni pubblicate e gli indirizzi Web reindirizzati in un'area di lavoro MED-V e come aprire la macchina virtuale dell'area di lavoro MED-V in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="ecb43-119">Describes how to use the MED-V Administration Toolkit to view the published applications and redirected web addresses in a MED-V workspace and how to open the MED-V workspace virtual machine in full-screen mode.</span></span>

## <span data-ttu-id="ecb43-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ecb43-120">Related topics</span></span>


[<span data-ttu-id="ecb43-121">Messaggi del registro eventi MED-V</span><span class="sxs-lookup"><span data-stu-id="ecb43-121">MED-V Event Log Messages</span></span>](med-v-event-log-messages.md)

[<span data-ttu-id="ecb43-122">Risoluzione dei problemi di MED-V</span><span class="sxs-lookup"><span data-stu-id="ecb43-122">Troubleshooting MED-V</span></span>](troubleshooting-med-vmedv2.md)

 

 





