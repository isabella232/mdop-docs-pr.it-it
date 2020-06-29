---
title: Scenario di distribuzione end-to-end per MED-V 2.0
description: Scenario di distribuzione end-to-end per MED-V 2.0
author: dansimp
ms.assetid: 91bb5a9a-5fb1-4743-8494-9d4dee2ec222
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6d56e70ad359ebf2d76cf3f30f54f73cd9ca1c66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826175"
---
# <span data-ttu-id="d86b1-103">Scenario di distribuzione end-to-end per MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="d86b1-103">End-to-End Deployment Scenario for MED-V 2.0</span></span>


<span data-ttu-id="d86b1-104">Questo scenario di esempio per Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 consente di distribuire i componenti MED-V nell'organizzazione usando più scenari da capo a fine.</span><span class="sxs-lookup"><span data-stu-id="d86b1-104">This sample scenario for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 helps you deploy the MED-V components in your enterprise by using multiple scenarios end-to-end.</span></span> <span data-ttu-id="d86b1-105">Questo scenario di esempio può essere considerato un caso di studio che consente di inserire i singoli scenari e le singole procedure nel contesto.</span><span class="sxs-lookup"><span data-stu-id="d86b1-105">You can think of this sample scenario as a case study that helps put the individual scenarios and procedures in context.</span></span>

<span data-ttu-id="d86b1-106">Questa sezione fornisce informazioni di base e indicazioni per la distribuzione di componenti MED-V come soluzione end-to-end nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="d86b1-106">This section provides basic information and directions for deploying MED-V components as an end-to-end solution in your enterprise.</span></span>

## <span data-ttu-id="d86b1-107">Scenario dettagliato di distribuzione di MED-V</span><span class="sxs-lookup"><span data-stu-id="d86b1-107">MED-V Deployment Step-by-step Scenario</span></span>


<span data-ttu-id="d86b1-108">Gli argomenti di questo scenario dettagliato includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="d86b1-108">The topics in this step-by-step scenario include the following:</span></span>

-   <span data-ttu-id="d86b1-109">Le [configurazioni supportate in Med-v 2,0](med-v-20-supported-configurations.md) illustrano i requisiti necessari per installare ed eseguire Microsoft Enterprise Desktop VIRTUALIZATION (MED-v) 2.0 nell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="d86b1-109">[MED-V 2.0 Supported Configurations](med-v-20-supported-configurations.md) discusses the requirements that you must have to install and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0in your environment.</span></span> <span data-ttu-id="d86b1-110">In questo argomento vengono specificati i requisiti del sistema operativo, i requisiti di configurazione e i requisiti dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="d86b1-110">This topic specifies the operating system requirements, configuration requirements, and MED-V workspace requirements.</span></span> <span data-ttu-id="d86b1-111">Questo argomento include anche informazioni sulla localizzazione sulle lingue supportate da MED-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="d86b1-111">This topic also includes localization information about the languages that MED-V 2.0 supports.</span></span>

-   <span data-ttu-id="d86b1-112">[Panoramica sulla distribuzione di Med-v 2,0](med-v-20-deployment-overview.md) illustra informazioni generali e istruzioni per l'installazione e la distribuzione di Med-v in tutta l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="d86b1-112">[MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md) discusses general information and instructions to help you install and deploy MED-V throughout your enterprise.</span></span> <span data-ttu-id="d86b1-113">I componenti MED-V sono basati su client e vengono recapitati e gestiti usando l'infrastruttura e i processi esistenti dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="d86b1-113">The MED-V components are client-based and are delivered and managed by using your existing enterprise infrastructure and processes.</span></span> <span data-ttu-id="d86b1-114">Questo argomento offre una panoramica della soluzione MED-V che include informazioni sui file di installazione di MED-V e sui componenti MED-V distribuiti.</span><span class="sxs-lookup"><span data-stu-id="d86b1-114">This topic provides an overview of the MED-V solution that includes information about the MED-V installation files and the MED-V components that you deploy.</span></span> <span data-ttu-id="d86b1-115">Questo argomento offre anche una panoramica di alto livello sul processo di installazione e distribuzione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="d86b1-115">This topic also provides a high-level overview of the MED-V installation and deployment process.</span></span>

-   <span data-ttu-id="d86b1-116">[Preparare l'ambiente di distribuzione per MED-v](prepare-the-deployment-environment-for-med-v.md) descrive come preparare l'ambiente per una distribuzione di 2,0 Med-v.</span><span class="sxs-lookup"><span data-stu-id="d86b1-116">[Prepare the Deployment Environment for MED-V](prepare-the-deployment-environment-for-med-v.md) discusses how to prepare your environment for a MED-V 2.0 deployment.</span></span> <span data-ttu-id="d86b1-117">In questa sezione vengono descritti i prerequisiti necessari per l'ambiente MED-V, ad esempio Microsoft Windows 7 e un'infrastruttura Active Directory in cui si usano i criteri di gruppo per consentire la gestione e la configurazione centralizzata di sistemi operativi, applicazioni e impostazioni degli utenti.</span><span class="sxs-lookup"><span data-stu-id="d86b1-117">This section describes the prerequisites that are required for the MED-V environment, such as Microsoft Windows 7 and an Active Directory infrastructure in which you use Group Policy to provide centralized management and configuration of operating systems, applications, and users' settings.</span></span> <span data-ttu-id="d86b1-118">Questa sezione descrive anche i prerequisiti che è necessario avere per l'installazione e la distribuzione di MED-V 2,0 in tutta l'organizzazione, ad esempio Windows Virtual PC e l'aggiornamento di Windows Virtual PC richiesto.</span><span class="sxs-lookup"><span data-stu-id="d86b1-118">This section also describes the prerequisites that you must have for installing and deploying MED-V 2.0 throughout your enterprise, such as Windows Virtual PC and the required Windows Virtual PC update.</span></span>

-   <span data-ttu-id="d86b1-119">[Distribuire i componenti Med-v](deploy-the-med-v-components.md) descrive i diversi modi in cui è possibile installare tutti i file di installazione necessari e i componenti Med-v in tutta l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="d86b1-119">[Deploy the MED-V Components](deploy-the-med-v-components.md) discusses the different ways you can install all of the necessary installation files and MED-V components throughout your enterprise.</span></span> <span data-ttu-id="d86b1-120">Per installare e distribuire MED-V, eseguire in genere le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="d86b1-120">To install and deploy MED-V, you typically follow these steps:</span></span>

    1.  <span data-ttu-id="d86b1-121">Installare il **Packager area di lavoro MED-v** nel computer amministratore che verrà usato per compilare i pacchetti dell'area di lavoro MED-v.</span><span class="sxs-lookup"><span data-stu-id="d86b1-121">Install the **MED-V Workspace Packager** on the administrator computer that you will use to build the MED-V workspace packages.</span></span> <span data-ttu-id="d86b1-122">Per altre informazioni, vedere [come installare il Packager area di lavoro MED-V](how-to-install-the-med-v-workspace-packager.md).</span><span class="sxs-lookup"><span data-stu-id="d86b1-122">For more information, see [How to Install the MED-V Workspace Packager](how-to-install-the-med-v-workspace-packager.md).</span></span>

    2.  <span data-ttu-id="d86b1-123">Creare e testare i pacchetti dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="d86b1-123">Create and test your MED-V workspace packages.</span></span> <span data-ttu-id="d86b1-124">Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-v](create-a-med-v-workspace-package.md) e [testare il pacchetto area di lavoro MED-v](testing-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="d86b1-124">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md) and [Testing the MED-V Workspace Package](testing-the-med-v-workspace-package.md).</span></span>

    3.  <span data-ttu-id="d86b1-125">Distribuire MED-V in tutta l'organizzazione usando il metodo esistente della società per la distribuzione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d86b1-125">Deploy MED-V throughout your enterprise by using your company’s existing method for deploying applications.</span></span> <span data-ttu-id="d86b1-126">Per altre informazioni, vedere [distribuzione del pacchetto area di lavoro MED-V](deploying-the-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="d86b1-126">For more information, see [Deploying the MED-V Workspace Package](deploying-the-med-v-workspace-package.md).</span></span>

## <span data-ttu-id="d86b1-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d86b1-127">Related topics</span></span>


[<span data-ttu-id="d86b1-128">Distribuzione di MED-V</span><span class="sxs-lookup"><span data-stu-id="d86b1-128">Deployment of MED-V</span></span>](deployment-of-med-v.md)

[<span data-ttu-id="d86b1-129">Scenario di pianificazione end-to-end per MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="d86b1-129">End-to-End Planning Scenario for MED-V 2.0</span></span>](end-to-end-planning-scenario-for-med-v-20.md)

[<span data-ttu-id="d86b1-130">Scenario di operazioni end-to-end per MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="d86b1-130">End-to-End Operations Scenario for MED-V 2.0</span></span>](end-to-end-operations-scenario-for-med-v-20.md)

 

 





