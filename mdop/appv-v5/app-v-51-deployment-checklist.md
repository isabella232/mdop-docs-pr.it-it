---
title: Elenco di controllo per la distribuzione di App-V 5.1
description: Elenco di controllo per la distribuzione di App-V 5.1
author: dansimp
ms.assetid: 44bed85a-e4f5-49d7-a308-a2b681f76372
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0864335e505996a3ea379b09de6a1aaa7fbe1676
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805979"
---
# <span data-ttu-id="04b71-103">Elenco di controllo per la distribuzione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="04b71-103">App-V 5.1 Deployment Checklist</span></span>


<span data-ttu-id="04b71-104">Questo elenco di controllo può essere usato per aiutarti durante la distribuzione di Microsoft Application Virtualization (App-V) 5,1.</span><span class="sxs-lookup"><span data-stu-id="04b71-104">This checklist can be used to help you during Microsoft Application Virtualization (App-V) 5.1 deployment.</span></span>

**<span data-ttu-id="04b71-105">Nota</span><span class="sxs-lookup"><span data-stu-id="04b71-105">Note</span></span>**  
<span data-ttu-id="04b71-106">Questo elenco di controllo illustra la procedura consigliata e un elenco di elementi di alto livello da tenere in considerazione durante la distribuzione delle caratteristiche di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="04b71-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying App-V 5.1 features.</span></span> <span data-ttu-id="04b71-107">È consigliabile copiare questo elenco di controllo in un foglio di calcolo e personalizzarlo per l'uso.</span><span class="sxs-lookup"><span data-stu-id="04b71-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="04b71-108">Attività</span><span class="sxs-lookup"><span data-stu-id="04b71-108">Task</span></span></th>
<th align="left"><span data-ttu-id="04b71-109">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="04b71-109">References</span></span></th>
<th align="left"><span data-ttu-id="04b71-110">Note</span><span class="sxs-lookup"><span data-stu-id="04b71-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="04b71-111">Completare la fase di pianificazione per preparare l'ambiente di elaborazione per la distribuzione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="04b71-111">Complete the planning phase to prepare the computing environment for App-V 5.1 deployment.</span></span></p></td>
<td align="left"><p><a href="app-v-51-planning-checklist.md" data-raw-source="[App-V 5.1 Planning Checklist](app-v-51-planning-checklist.md)"><span data-ttu-id="04b71-112">Elenco di controllo per la pianificazione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="04b71-112">App-V 5.1 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="04b71-113">Esaminare le informazioni sulle configurazioni supportate in App-V 5,1 per verificare che i computer client e server selezionati siano supportati per l'installazione di funzionalità di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="04b71-113">Review the App-V 5.1 supported configurations information to make sure selected client and server computers are supported for App-V 5.1 feature installation.</span></span></p></td>
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"><span data-ttu-id="04b71-114">Configurazioni supportate di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="04b71-114">App-V 5.1 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="04b71-115">Eseguire l'installazione di App-V 5,1 per distribuire le funzionalità di App-V 5,1 necessarie per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="04b71-115">Run App-V 5.1 Setup to deploy the required App-V 5.1 features for your environment.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="04b71-116">Nota</span><span class="sxs-lookup"><span data-stu-id="04b71-116">Note</span></span></strong><br/><p><span data-ttu-id="04b71-117">Tenere traccia dei nomi dei server e dell'URL associato creato durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="04b71-117">Keep track of the names of the servers and associated URL’s created during installation.</span></span> <span data-ttu-id="04b71-118">Queste informazioni verranno usate durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="04b71-118">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p></p>
<ul>
<li><p><a href="how-to-install-the-sequencer-51beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-51beta-gb18030.md)"><span data-ttu-id="04b71-119">Come installare Sequencer</span><span class="sxs-lookup"><span data-stu-id="04b71-119">How to Install the Sequencer</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)"><span data-ttu-id="04b71-120">Come distribuire il client App-V</span><span class="sxs-lookup"><span data-stu-id="04b71-120">How to Deploy the App-V Client</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"><span data-ttu-id="04b71-121">Come distribuire il server App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="04b71-121">How to Deploy the App-V 5.1 Server</span></span></a></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="04b71-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04b71-122">Related topics</span></span>


[<span data-ttu-id="04b71-123">Distribuzione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="04b71-123">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)









