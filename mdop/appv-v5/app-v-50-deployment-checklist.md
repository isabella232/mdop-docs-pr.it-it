---
title: Elenco di controllo per la distribuzione di App-V 5.0
description: Elenco di controllo per la distribuzione di App-V 5.0
author: dansimp
ms.assetid: d6d93152-82b4-4b02-8b11-ed21d3331f00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f213271a6d4b90961846b49553c07f1eb6e4c03
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806033"
---
# <span data-ttu-id="f1975-103">Elenco di controllo per la distribuzione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f1975-103">App-V 5.0 Deployment Checklist</span></span>


<span data-ttu-id="f1975-104">Questo elenco di controllo può essere usato per aiutarti durante la distribuzione di Microsoft Application Virtualization (App-V) 5,0.</span><span class="sxs-lookup"><span data-stu-id="f1975-104">This checklist can be used to help you during Microsoft Application Virtualization (App-V) 5.0 deployment.</span></span>

**<span data-ttu-id="f1975-105">Nota</span><span class="sxs-lookup"><span data-stu-id="f1975-105">Note</span></span>**  
<span data-ttu-id="f1975-106">Questo elenco di controllo illustra la procedura consigliata e un elenco di elementi di alto livello da tenere in considerazione durante la distribuzione delle caratteristiche di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f1975-106">This checklist outlines the recommended steps and a high-level list of items to consider when deploying App-V 5.0 features.</span></span> <span data-ttu-id="f1975-107">È consigliabile copiare questo elenco di controllo in un foglio di calcolo e personalizzarlo per l'uso.</span><span class="sxs-lookup"><span data-stu-id="f1975-107">It is recommended that you copy this checklist into a spreadsheet program and customize it for your use.</span></span>



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
<th align="left"><span data-ttu-id="f1975-108">Attività</span><span class="sxs-lookup"><span data-stu-id="f1975-108">Task</span></span></th>
<th align="left"><span data-ttu-id="f1975-109">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="f1975-109">References</span></span></th>
<th align="left"><span data-ttu-id="f1975-110">Note</span><span class="sxs-lookup"><span data-stu-id="f1975-110">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1975-111">Completare la fase di pianificazione per preparare l'ambiente di elaborazione per la distribuzione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f1975-111">Complete the planning phase to prepare the computing environment for App-V 5.0 deployment.</span></span></p></td>
<td align="left"><p><a href="app-v-50-planning-checklist.md" data-raw-source="[App-V 5.0 Planning Checklist](app-v-50-planning-checklist.md)"><span data-ttu-id="f1975-112">Elenco di controllo per la pianificazione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f1975-112">App-V 5.0 Planning Checklist</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1975-113">Esaminare le informazioni sulle configurazioni supportate in App-V 5,0 per verificare che i computer client e server selezionati siano supportati per l'installazione di funzionalità di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="f1975-113">Review the App-V 5.0 supported configurations information to make sure selected client and server computers are supported for App-V 5.0 feature installation.</span></span></p></td>
<td align="left"><p><a href="app-v-50-supported-configurations.md" data-raw-source="[App-V 5.0 Supported Configurations](app-v-50-supported-configurations.md)"><span data-ttu-id="f1975-114">Configurazioni supportate di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f1975-114">App-V 5.0 Supported Configurations</span></span></a></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p><span data-ttu-id="f1975-115">Eseguire l'installazione di App-V 5,0 per distribuire le funzionalità di App-V 5,0 necessarie per l'ambiente.</span><span class="sxs-lookup"><span data-stu-id="f1975-115">Run App-V 5.0 Setup to deploy the required App-V 5.0 features for your environment.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f1975-116">Nota</span><span class="sxs-lookup"><span data-stu-id="f1975-116">Note</span></span></strong><br/><p><span data-ttu-id="f1975-117">Tenere traccia dei nomi dei server e dell'URL associato creato durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="f1975-117">Keep track of the names of the servers and associated URL’s created during installation.</span></span> <span data-ttu-id="f1975-118">Queste informazioni verranno usate durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="f1975-118">This information will be used throughout the installation process.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p></p>
<ul>
<li><p><a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"><span data-ttu-id="f1975-119">Come installare Sequencer</span><span class="sxs-lookup"><span data-stu-id="f1975-119">How to Install the Sequencer</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"><span data-ttu-id="f1975-120">Come distribuire il client App-V</span><span class="sxs-lookup"><span data-stu-id="f1975-120">How to Deploy the App-V Client</span></span></a></p></li>
<li><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"><span data-ttu-id="f1975-121">Come distribuire il server App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f1975-121">How to Deploy the App-V 5.0 Server</span></span></a></p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="f1975-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1975-122">Related topics</span></span>


[<span data-ttu-id="f1975-123">Distribuzione di App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="f1975-123">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)









