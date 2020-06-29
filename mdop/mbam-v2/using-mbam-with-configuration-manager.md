---
title: Uso di MBAM con Configuration Manager
description: Uso di MBAM con Configuration Manager
author: dansimp
ms.assetid: 03868717-4aa7-4897-8166-9a3df5e9519e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e3c5dd199010ac758ab701b0753d913ea323efd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823786"
---
# <span data-ttu-id="7a0ec-103">Uso di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a0ec-103">Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="7a0ec-104">Quando si installa Microsoft BitLocker Administration and Monitoring (MBAM), è possibile scegliere un'installazione che integri l'amministrazione e il monitoraggio di Microsoft BitLocker con System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7a0ec-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM), you can choose an installation that integrates Microsoft BitLocker Administration and Monitoring with System Center Configuration Manager.</span></span> <span data-ttu-id="7a0ec-105">Per un elenco delle versioni supportate di Configuration Manager, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="7a0ec-105">For a list of the supported versions of Configuration Manager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="7a0ec-106">Questa integrazione Sposta l'infrastruttura di amministrazione e monitoraggio della conformità e della creazione di report di Microsoft BitLocker nell'ambiente nativo di Microsoft System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7a0ec-106">This integration moves the Microsoft BitLocker Administration and Monitoring compliance and reporting infrastructure into the native environment of Microsoft System Center Configuration Manager.</span></span> <span data-ttu-id="7a0ec-107">Con la topologia di Configuration Manager, gli amministratori IT possono visualizzare i report e lo stato di conformità della propria azienda dalla console di gestione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7a0ec-107">With the Configuration Manager topology, IT administrators can view reports and the compliance status of their enterprise from the Configuration Manager Management Console.</span></span>

<span data-ttu-id="7a0ec-108">**Importante**  Windows to go non è supportato quando si installa la topologia integrata di MBAM con Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="7a0ec-108">**Important** Windows To Go is not supported when you install the integrated topology of MBAM with Configuration Manager 2007.</span></span>

 

## <a href="" id="getting-started---using-mbam-with-configuration-manager"></a><span data-ttu-id="7a0ec-109">Guida introduttiva: usare MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a0ec-109">Getting Started – Using MBAM with Configuration Manager</span></span>


<span data-ttu-id="7a0ec-110">Questa sezione descrive come funziona MBAM con Configuration Manager e spiega l'architettura consigliata per la distribuzione di MBAM con la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7a0ec-110">This section describes how MBAM works with Configuration Manager and explains the recommended architecture for deploying MBAM with the Configuration Manager Integration topology.</span></span>

[<span data-ttu-id="7a0ec-111">Attività iniziali: uso di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a0ec-111">Getting Started - Using MBAM with Configuration Manager</span></span>](getting-started---using-mbam-with-configuration-manager.md)

## <span data-ttu-id="7a0ec-112">Pianificazione della distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a0ec-112">Planning to Deploy MBAM with Configuration Manager</span></span>


<span data-ttu-id="7a0ec-113">Questa sezione descrive i prerequisiti di installazione, le configurazioni supportate e i requisiti hardware e software che è necessario prendere in considerazione prima di installare MBAM con la topologia di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7a0ec-113">This section describes the installation prerequisites, supported configurations, and hardware and software requirements that you need to consider before you install MBAM with the Configuration Manager topology.</span></span>

[<span data-ttu-id="7a0ec-114">Pianificazione della distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a0ec-114">Planning to Deploy MBAM with Configuration Manager</span></span>](planning-to-deploy-mbam-with-configuration-manager-2.md)

## <span data-ttu-id="7a0ec-115">Distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a0ec-115">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="7a0ec-116">Questa sezione descrive come distribuire MBAM con Configuration Manager e include istruzioni per l'installazione e la configurazione di MBAM nel server di amministrazione e monitoraggio Server e Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7a0ec-116">This section describes how to deploy MBAM with Configuration Manager, and includes instructions for installing and configuring the MBAM on the Administration and Monitoring Server and Configuration Manager Server.</span></span>

[<span data-ttu-id="7a0ec-117">Distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a0ec-117">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

## <span data-ttu-id="7a0ec-118">Informazioni sui report di MBAM in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a0ec-118">Understanding MBAM Reports in Configuration Manager</span></span>


<span data-ttu-id="7a0ec-119">In questa sezione vengono descritti i report di MBAM che è possibile eseguire da Configuration Manager per mostrare la conformità della propria azienda e la conformità dei singoli computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7a0ec-119">This section describes the MBAM reports that you can run from Configuration Manager to show the compliance of your enterprise and compliance of individual computers in your enterprise.</span></span>

[<span data-ttu-id="7a0ec-120">Informazioni sui report di MBAM in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7a0ec-120">Understanding MBAM Reports in Configuration Manager</span></span>](understanding-mbam-reports-in-configuration-manager.md)

## <span data-ttu-id="7a0ec-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a0ec-121">Related topics</span></span>


[<span data-ttu-id="7a0ec-122">Operazioni relative a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="7a0ec-122">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





