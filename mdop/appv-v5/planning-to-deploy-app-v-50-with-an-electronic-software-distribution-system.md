---
title: Pianificazione della distribuzione di App-V 5.0 con un sistema di distribuzione elettronica del software
description: Pianificazione della distribuzione di App-V 5.0 con un sistema di distribuzione elettronica del software
author: dansimp
ms.assetid: 8cd3f1fb-b84e-4260-9e72-a14d01e7cadf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ca441820be7e6759e65902aea18b2db7f989e8f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804953"
---
# <span data-ttu-id="1ea03-103">Pianificazione della distribuzione di App-V 5.0 con un sistema di distribuzione elettronica del software</span><span class="sxs-lookup"><span data-stu-id="1ea03-103">Planning to Deploy App-V 5.0 with an Electronic Software Distribution System</span></span>


<span data-ttu-id="1ea03-104">Se si usa un sistema di distribuzione del software elettronico per distribuire pacchetti App-V, vedere le considerazioni seguenti sulla pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1ea03-104">If you are using an electronic software distribution system to deploy App-V packages, review the following planning considerations.</span></span> <span data-ttu-id="1ea03-105">Per informazioni sull'uso di System Center Configuration Manager per distribuire App-V, vedere [Introduzione alla gestione delle applicazioni in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span><span class="sxs-lookup"><span data-stu-id="1ea03-105">For information about using System Center Configuration Manager to deploy App-V, see [Introduction to Application Management in Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).</span></span>

<span data-ttu-id="1ea03-106">Esaminare le opzioni di requisiti per il componente e l'architettura seguenti che si applicano quando si usa un ESD per distribuire pacchetti App-V:</span><span class="sxs-lookup"><span data-stu-id="1ea03-106">Review the following component and architecture requirements options that apply when you use an ESD to deploy App-V packages:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ea03-107">Requisito o opzione di distribuzione</span><span class="sxs-lookup"><span data-stu-id="1ea03-107">Deployment requirement or option</span></span></th>
<th align="left"><span data-ttu-id="1ea03-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ea03-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ea03-109">App-V Management Server, database di gestione e server di pubblicazione non sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="1ea03-109">The App-V Management server, Management database, and Publishing server are not required.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ea03-110">Queste funzioni vengono gestite dalla soluzione ESD implementata.</span><span class="sxs-lookup"><span data-stu-id="1ea03-110">These functions are handled by the implemented ESD solution.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ea03-111">Puoi distribuire l'App-V Reporting Server e il database di report affiancati all'ESD.</span><span class="sxs-lookup"><span data-stu-id="1ea03-111">You can deploy the App-V Reporting server and Reporting database side by side with the ESD.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ea03-112">La distribuzione affiancata consente di raccogliere dati e generare report.</span><span class="sxs-lookup"><span data-stu-id="1ea03-112">The side-by-side deployment lets you to collect data and generate reports.</span></span></p>
<p><span data-ttu-id="1ea03-113">Se si Abilita il client App-V per inviare informazioni sul report e non si usa l'App-V Reporting Server, i dati dei report vengono archiviati nei file XML associati.</span><span class="sxs-lookup"><span data-stu-id="1ea03-113">If you enable the App-V client to send report information, and you are not using the App-V Reporting server, the reporting data is stored in associated .xml files.</span></span></p></td>
</tr>
</tbody>
</table>

 






 

 





