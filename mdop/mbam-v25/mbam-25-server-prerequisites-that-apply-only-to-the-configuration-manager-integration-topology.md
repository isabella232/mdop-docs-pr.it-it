---
title: Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager
description: Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804323"
---
# <span data-ttu-id="ae0c6-103">Prerequisiti del server di MBAM 2.5 che si applicano solo alla topologia di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ae0c6-103">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>


<span data-ttu-id="ae0c6-104">Se si sta installando Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 usando la funzionalità di integrazione di System Center Configuration Manager, è necessario completare i prerequisiti descritti in questo argomento, oltre a quelli nei [prerequisiti di MBAM 2,5 Server per le topologie di integrazione di gestione autonoma e configurazione](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="ae0c6-104">If you are installing Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 by using the System Center Configuration Manager Integration feature, you must complete the prerequisites described in this topic, in addition to those in [MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md).</span></span> <span data-ttu-id="ae0c6-105">È inoltre necessario creare o modificare i file MOF necessari per la topologia di integrazione di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ae0c6-105">You must also create or modify .mof files that are needed for the Configuration Manager Integration topology.</span></span>

## <span data-ttu-id="ae0c6-106">Prerequisiti per la funzionalità di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ae0c6-106">Prerequisites for the Configuration Manager Integration Feature</span></span>


<span data-ttu-id="ae0c6-107">Se si sta configurando MBAM con la topologia di integrazione di System Center Configuration Manager, è necessario completare i prerequisiti aggiuntivi necessari per Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ae0c6-107">If you are configuring MBAM with the System Center Configuration Manager Integration topology, you must complete additional prerequisites that are required for Configuration Manager.</span></span>

[<span data-ttu-id="ae0c6-108">Prerequisiti per la funzionalità di integrazione di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ae0c6-108">Prerequisites for the Configuration Manager Integration Feature</span></span>](prerequisites-for-the-configuration-manager-integration-feature.md)

## <span data-ttu-id="ae0c6-109">Modificare il file Configuration. mof</span><span class="sxs-lookup"><span data-stu-id="ae0c6-109">Edit the Configuration.mof file</span></span>


<span data-ttu-id="ae0c6-110">Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker tramite i report di MBAM Configuration Manager, è necessario modificare il file Configuration. mof per SystemCenter2012 ConfigurationManager e Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="ae0c6-110">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager Reports, you have to edit the Configuration.mof file for SystemCenter2012 ConfigurationManager and Microsoft System Center Configuration Manager 2007.</span></span>

[<span data-ttu-id="ae0c6-111">Modificare il file Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="ae0c6-111">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="ae0c6-112">Creare o modificare il file SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="ae0c6-112">Create or edit the Sms\_def.mof file</span></span>


<span data-ttu-id="ae0c6-113">Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker nei report di MBAM Configuration Manager, è necessario creare o modificare il file SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="ae0c6-113">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager Reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="ae0c6-114">Se si usa il ConfigurationManager di SystemCenter2012, è necessario creare il file.</span><span class="sxs-lookup"><span data-stu-id="ae0c6-114">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="ae0c6-115">In Configuration Manager 2007 il file esiste già, quindi è necessario modificare, ma non sovrascrivere, il file esistente.</span><span class="sxs-lookup"><span data-stu-id="ae0c6-115">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span>

[<span data-ttu-id="ae0c6-116">Creare o modificare il file SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="ae0c6-116">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file-mbam-25.md)


## <span data-ttu-id="ae0c6-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ae0c6-117">Related topics</span></span>


[<span data-ttu-id="ae0c6-118">Preparazione dell'ambiente per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ae0c6-118">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="ae0c6-119">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ae0c6-119">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="ae0c6-120">Pianificazione della distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="ae0c6-120">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="ae0c6-121">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="ae0c6-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="ae0c6-122">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="ae0c6-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="ae0c6-123">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="ae0c6-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




