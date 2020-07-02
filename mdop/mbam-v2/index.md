---
title: Guida dell'amministratore di amministrazione e monitoraggio di Microsoft BitLocker 2
description: Guida dell'amministratore di amministrazione e monitoraggio di Microsoft BitLocker 2
author: dansimp
ms.assetid: fdb43f62-960a-4811-8802-50efdf04b4af
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: dd6deb6fb91c64ac8609b54114e0dd417497034a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795751"
---
# <span data-ttu-id="76d0d-103">Guida dell'amministratore di amministrazione e monitoraggio di Microsoft BitLocker 2</span><span class="sxs-lookup"><span data-stu-id="76d0d-103">Microsoft BitLocker Administration and Monitoring 2 Administrator's Guide</span></span>

<span data-ttu-id="76d0d-104">Microsoft BitLockerAdministration and Monitoring (MBAM) 2.0 offre un'interfaccia amministrativa semplificata che è possibile usare per gestire la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="76d0d-104">Microsoft BitLockerAdministration and Monitoring(MBAM)2.0 provides a simplified administrative interface that you can use to manage BitLocker drive encryption.</span></span> <span data-ttu-id="76d0d-105">In BitLockerAdministration e monitoraggio 2.0 è possibile selezionare le opzioni di crittografia unità BitLocker appropriate per l'organizzazione e quindi utilizzarle per monitorare la conformità dei client a tali criteri.</span><span class="sxs-lookup"><span data-stu-id="76d0d-105">In BitLockerAdministration and Monitoring2.0, you can select BitLocker drive encryption policy options that are appropriate for your enterprise, and then use them to monitor client compliance with those policies.</span></span> <span data-ttu-id="76d0d-106">È anche possibile segnalare lo stato di crittografia di un singolo computer e dell'intera organizzazione.</span><span class="sxs-lookup"><span data-stu-id="76d0d-106">You can also report on the encryption status of an individual computer and on the enterprise as a whole.</span></span> <span data-ttu-id="76d0d-107">Inoltre, è possibile accedere alle informazioni chiave di ripristino quando gli utenti dimenticano il PIN o la password o quando cambia il BIOS o il record di avvio.</span><span class="sxs-lookup"><span data-stu-id="76d0d-107">In addition, you can access recovery key information when users forget their PIN or password or when their BIOS or boot record changes.</span></span>

## <span data-ttu-id="76d0d-108">Struttura</span><span class="sxs-lookup"><span data-stu-id="76d0d-108">Outline</span></span>

- [<span data-ttu-id="76d0d-109">Attività iniziali di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-109">Getting Started with MBAM 2.0</span></span>](getting-started-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-110">Informazioni su MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-110">About MBAM 2.0</span></span>](about-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-111">Note sulla versione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-111">Release Notes for MBAM 2.0</span></span>](release-notes-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-112">Informazioni su MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="76d0d-112">About MBAM 2.0 SP1</span></span>](about-mbam-20-sp1.md)
  - [<span data-ttu-id="76d0d-113">Note sulla versione di MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="76d0d-113">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)
  - [<span data-ttu-id="76d0d-114">Valutazione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-114">Evaluating MBAM 2.0</span></span>](evaluating-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-115">Architettura di alto livello per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-115">High-Level Architecture for MBAM 2.0</span></span>](high-level-architecture-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-116">Accessibilità per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-116">Accessibility for MBAM 2.0</span></span>](accessibility-for-mbam-20-mbam-2.md)
- [<span data-ttu-id="76d0d-117">Pianificazione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-117">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-118">Preparazione dell'ambiente per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-118">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-119">Prerequisiti per la distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-119">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)
  - [<span data-ttu-id="76d0d-120">Pianificazione della distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-120">Planning to Deploy MBAM 2.0</span></span>](planning-to-deploy-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-121">Configurazioni supportate di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-121">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)
  - [<span data-ttu-id="76d0d-122">Elenco di controllo per la pianificazione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-122">MBAM 2.0 Planning Checklist</span></span>](mbam-20-planning-checklist-mbam-2.md)
- [<span data-ttu-id="76d0d-123">Distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-123">Deploying MBAM 2.0</span></span>](deploying-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-124">Distribuzione dell'infrastruttura server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-124">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)
  - [<span data-ttu-id="76d0d-125">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-125">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)
  - [<span data-ttu-id="76d0d-126">Distribuzione del client MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-126">Deploying the MBAM 2.0 Client</span></span>](deploying-the-mbam-20-client-mbam-2.md)
  - [<span data-ttu-id="76d0d-127">Elenco di controllo per la distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-127">MBAM 2.0 Deployment Checklist</span></span>](mbam-20-deployment-checklist-mbam-2.md)
  - [<span data-ttu-id="76d0d-128">Aggiornamento da versioni precedenti di MBAM</span><span class="sxs-lookup"><span data-stu-id="76d0d-128">Upgrading from Previous Versions of MBAM</span></span>](upgrading-from-previous-versions-of-mbam.md)
- [<span data-ttu-id="76d0d-129">Operazioni relative a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-129">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-130">Uso di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="76d0d-130">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)
  - [<span data-ttu-id="76d0d-131">Amministrazione delle funzionalità di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-131">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)
  - [<span data-ttu-id="76d0d-132">Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-132">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-133">Gestione di BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="76d0d-133">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)
  - [<span data-ttu-id="76d0d-134">Manutenzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-134">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-135">Sicurezza e privacy per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-135">Security and Privacy for MBAM 2.0</span></span>](security-and-privacy-for-mbam-20-mbam-2.md)
  - [<span data-ttu-id="76d0d-136">Amministrazione di MBAM 2.0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="76d0d-136">Administering MBAM 2.0 Using PowerShell</span></span>](administering-mbam-20-using-powershell-mbam-2.md)
- [<span data-ttu-id="76d0d-137">Risoluzione dei problemi relativi a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="76d0d-137">Troubleshooting MBAM 2.0</span></span>](troubleshooting-mbam-20-mbam-2.md)

## <span data-ttu-id="76d0d-138">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="76d0d-138">More Information</span></span>

- [<span data-ttu-id="76d0d-139">Esperienza di informazioni su MDOP</span><span class="sxs-lookup"><span data-stu-id="76d0d-139">MDOP Information Experience</span></span>](index.md)

  <span data-ttu-id="76d0d-140">Trovare documentazione, video e altre risorse per le tecnologie MDOP.</span><span class="sxs-lookup"><span data-stu-id="76d0d-140">Find documentation, videos, and other resources for MDOP technologies.</span></span>

 

 





