---
title: Elenco di controllo pre-installazione di App-V
description: Elenco di controllo pre-installazione di App-V
author: dansimp
ms.assetid: 3af609b1-2c09-4edb-b083-b913b6d5e8c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 70e71d3dea02daeadedb4cff78c58302ac743dda
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819786"
---
# <span data-ttu-id="69732-103">Elenco di controllo pre-installazione di App-V</span><span class="sxs-lookup"><span data-stu-id="69732-103">App-V Pre-Installation Checklist</span></span>


<span data-ttu-id="69732-104">L'elenco di controllo seguente ha lo scopo di specificare un alto livello di elementi da tenere in considerazione e illustrare i passaggi da eseguire prima di installare i server di Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="69732-104">The following checklist is intended to provide a high-level list of items to consider and outlines the steps you should take before you install the Microsoft Application Virtualization (App-V) servers.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69732-105">Passaggio</span><span class="sxs-lookup"><span data-stu-id="69732-105">Step</span></span></th>
<th align="left"><span data-ttu-id="69732-106">Riferimento</span><span class="sxs-lookup"><span data-stu-id="69732-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69732-107">Verificare che l'ambiente di elaborazione soddisfi le configurazioni supportate necessarie per App-V.</span><span class="sxs-lookup"><span data-stu-id="69732-107">Ensure your computing environment meets the supported configurations required for App-V.</span></span></p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)"><span data-ttu-id="69732-108">Requisiti per la distribuzione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="69732-108">Application Virtualization Deployment Requirements</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69732-109">Configurare i gruppi e gli account di Active Directory necessari.</span><span class="sxs-lookup"><span data-stu-id="69732-109">Configure the necessary Active Directory groups and accounts.</span></span></p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)"><span data-ttu-id="69732-110">Configurazione dei gruppi di prerequisiti in Active Directory per App-V</span><span class="sxs-lookup"><span data-stu-id="69732-110">Configuring Prerequisite Groups in Active Directory for App-V</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69732-111">Configurare le impostazioni di Internet Information Services (IIS) nel server in cui è in uso IIS.</span><span class="sxs-lookup"><span data-stu-id="69732-111">Configure the Internet Information Services (IIS) settings on the server that is running IIS.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)"><span data-ttu-id="69732-112">Come configurare Windows Server 2008 per i server di gestione di App-V</span><span class="sxs-lookup"><span data-stu-id="69732-112">How to Configure Windows Server 2008 for App-V Management Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69732-113">Configurare il server che utilizza IIS per essere considerato attendibile per la delega.</span><span class="sxs-lookup"><span data-stu-id="69732-113">Configure the server that is running IIS to be trusted for delegation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="69732-114">Nota</span><span class="sxs-lookup"><span data-stu-id="69732-114">Note</span></span></strong><br/><p><span data-ttu-id="69732-115">Questa operazione è necessaria solo se si sta installando App-V Management Server utilizzando un'architettura di sistema distribuita, ovvero se si installa App-V Management Console, il servizio Web di gestione e il database in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="69732-115">This is required only if you are installing the App-V Management Server by using a distributed system architecture, that is, if you install the App-V Management Console, the Management Web Service, and the database on different computers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)"><span data-ttu-id="69732-116">Come configurare il server in modo che sia attendibile per la delega</span><span class="sxs-lookup"><span data-stu-id="69732-116">How to Configure the Server to be Trusted for Delegation</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69732-117">Installare Microsoft SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="69732-117">Install Microsoft SQL Server 2008.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)"><span data-ttu-id="69732-118">Installare SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</span><span class="sxs-lookup"><span data-stu-id="69732-118">Install SQL Server 2008</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924">https://go.microsoft.com/fwlink/?LinkId=181924</a>).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="69732-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69732-119">Related topics</span></span>


[<span data-ttu-id="69732-120">Elenchi di controllo per la distribuzione e l'aggiornamento di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="69732-120">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

[<span data-ttu-id="69732-121">Elenco di controllo installazione di App-V</span><span class="sxs-lookup"><span data-stu-id="69732-121">App-V Installation Checklist</span></span>](app-v-installation-checklist.md)









