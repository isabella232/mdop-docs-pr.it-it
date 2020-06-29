---
title: Architettura di alto livello
description: Architettura di alto livello
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827295"
---
# <span data-ttu-id="dac6c-103">Architettura di alto livello</span><span class="sxs-lookup"><span data-stu-id="dac6c-103">High-Level Architecture</span></span>


<span data-ttu-id="dac6c-104">Questa sezione descrive l'architettura di sistema di alto livello e la progettazione di componenti di Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="dac6c-104">This section describes the high-level system architecture and component design of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="dac6c-105">Architettura di sistema</span><span class="sxs-lookup"><span data-stu-id="dac6c-105">System Architecture</span></span>


<span data-ttu-id="dac6c-106">MED-V migliora Windows Virtual PC per l'esecuzione di due sistemi operativi su un dispositivo, l'aggiunta del recapito delle immagini virtuali, il provisioning basato su criteri di gruppo e la gestione centralizzata.</span><span class="sxs-lookup"><span data-stu-id="dac6c-106">MED-V enhances Windows Virtual PC to run two operating systems on one device, adding virtual image delivery, Group Policy-based provisioning, and centralized management.</span></span> <span data-ttu-id="dac6c-107">Con MED-V puoi configurare, distribuire e gestire facilmente le immagini di PC virtuali di Windows aziendali in qualsiasi desktop basato su Windows che esegua Windows 7 Professional, Enterprise o Windows 7 Ultimate.</span><span class="sxs-lookup"><span data-stu-id="dac6c-107">By using MED-V, you can easily configure, deploy, and manage corporate Windows Virtual PC images on any Windows-based desktop running Windows 7 Professional, Enterprise, or Windows 7 Ultimate.</span></span> <span data-ttu-id="dac6c-108">La soluzione MED-V include i componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="dac6c-108">The MED-V solution includes the following components:</span></span>

<a href="" id="---------------med-v-host"></a> **<span data-ttu-id="dac6c-109">Host MED-V</span><span class="sxs-lookup"><span data-stu-id="dac6c-109">MED-V Host</span></span>**  
<span data-ttu-id="dac6c-110">Un ambiente Windows 7 che include un agente host MED-V, un sistema ESD (Electronic Software Distribution), un sistema di gestione del registro e un guest MED-V.</span><span class="sxs-lookup"><span data-stu-id="dac6c-110">A Windows 7 environment that includes a MED-V Host Agent, an electronic software distribution (ESD) system, a registry management system, and a MED-V guest.</span></span> <span data-ttu-id="dac6c-111">L'host MED-V interagisce con l'ospite MED-V in modo che sia possibile elaborare alcune funzioni di configurazione e le informazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="dac6c-111">The MED-V host interacts with the MED-V guest so that certain setup functions and system information can be processed.</span></span>

<a href="" id="-------------------med-v-host-agent"></a> **<span data-ttu-id="dac6c-112">Agente host MED-V</span><span class="sxs-lookup"><span data-stu-id="dac6c-112">MED-V Host Agent</span></span>**  
<span data-ttu-id="dac6c-113">Il software MED-V contenuto nell'host MED-V che fornisce un canale per comunicare con l'ospite MED-V.</span><span class="sxs-lookup"><span data-stu-id="dac6c-113">The MED-V software contained in the MED-V host that provides a channel to communicate with the MED-V guest.</span></span> <span data-ttu-id="dac6c-114">Offre anche funzionalità come la configurazione e la pubblicazione delle applicazioni prima volta.</span><span class="sxs-lookup"><span data-stu-id="dac6c-114">It also provides functionality such as first time setup and application publishing.</span></span>

<span data-ttu-id="dac6c-115">**Nota**  Dopo aver installato MED-V e i relativi componenti necessari, è necessario configurarlo.</span><span class="sxs-lookup"><span data-stu-id="dac6c-115">**Note** After MED-V and its required components are installed MED-V must be configured.</span></span> <span data-ttu-id="dac6c-116">La configurazione di MED-V viene indicata come configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="dac6c-116">The configuration of MED-V is referred to as first time setup.</span></span>

 

<a href="" id="esd-system"></a>**<span data-ttu-id="dac6c-117">Sistema ESD</span><span class="sxs-lookup"><span data-stu-id="dac6c-117">ESD System</span></span>**  
<span data-ttu-id="dac6c-118">Il metodo di distribuzione del software esistente che consente di distribuire e installare i file del pacchetto dell'area di lavoro MED-V creati da MED-V.</span><span class="sxs-lookup"><span data-stu-id="dac6c-118">Your existing software distribution method that lets you deploy and install the MED-V workspace package files that MED-V creates.</span></span>

<a href="" id="registry-management-system"></a>**<span data-ttu-id="dac6c-119">Sistema di gestione del registro</span><span class="sxs-lookup"><span data-stu-id="dac6c-119">Registry Management System</span></span>**  
<span data-ttu-id="dac6c-120">Metodo esistente per la gestione delle impostazioni e delle preferenze dei criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="dac6c-120">Your existing method of managing Group Policy settings and preferences.</span></span>

<a href="" id="windows-virtual-pc-image"></a>**<span data-ttu-id="dac6c-121">Immagine di un PC virtuale Windows</span><span class="sxs-lookup"><span data-stu-id="dac6c-121">Windows Virtual PC Image</span></span>**  
<span data-ttu-id="dac6c-122">Una macchina virtuale definita dall'amministratore che contiene i componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="dac6c-122">An administrator-defined virtual machine that contains the following components:</span></span>

<a href="" id="corporate-operating-system"></a>**<span data-ttu-id="dac6c-123">Sistema operativo aziendale</span><span class="sxs-lookup"><span data-stu-id="dac6c-123">Corporate Operating System</span></span>**  
<span data-ttu-id="dac6c-124">Sistema operativo aziendale standard.</span><span class="sxs-lookup"><span data-stu-id="dac6c-124">Your standard corporate operating system.</span></span>

<a href="" id="management-and-security-tools"></a>**<span data-ttu-id="dac6c-125">Strumenti di gestione e sicurezza</span><span class="sxs-lookup"><span data-stu-id="dac6c-125">Management and Security Tools</span></span>**  
<span data-ttu-id="dac6c-126">Gli strumenti di gestione e sicurezza standard, ad esempio la protezione da virus.</span><span class="sxs-lookup"><span data-stu-id="dac6c-126">Your standard management and security tools, such as virus protection.</span></span>

<a href="" id="-----------------------med-v-guest"></a> **<span data-ttu-id="dac6c-127">Guest MED-V</span><span class="sxs-lookup"><span data-stu-id="dac6c-127">MED-V Guest</span></span>**  
<span data-ttu-id="dac6c-128">Un ambiente Windows XP SP3, come parte di un PC virtuale Windows in uso in Windows 7 che contiene i componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="dac6c-128">A Windows XP SP3 environment, as part of a Windows Virtual PC running on Windows 7 that contains the following components:</span></span>

<a href="" id="---------------------------med-v-guest-agent"></a> **<span data-ttu-id="dac6c-129">Agente guest MED-V</span><span class="sxs-lookup"><span data-stu-id="dac6c-129">MED-V Guest Agent</span></span>**  
<span data-ttu-id="dac6c-130">Il software MED-V contenuto nell'guest MED-V che fornisce un canale per comunicare con l'host MED-V.</span><span class="sxs-lookup"><span data-stu-id="dac6c-130">The MED-V software contained in the MED-V guest that provides a channel to communicate with the MED-V host.</span></span> <span data-ttu-id="dac6c-131">Supporta inoltre l'agente host MED-V con funzioni come l'esecuzione della configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="dac6c-131">It also supports the MED-V Host Agent with functions like performing first time setup.</span></span>

<span data-ttu-id="dac6c-132">**Nota**  L'agente guest MED-V viene installato automaticamente durante la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="dac6c-132">**Note** The MED-V Guest Agent is installed automatically during first time setup.</span></span>

 

<a href="" id="esd-client"></a>**<span data-ttu-id="dac6c-133">Client ESD</span><span class="sxs-lookup"><span data-stu-id="dac6c-133">ESD Client</span></span>**  
<span data-ttu-id="dac6c-134">Una parte facoltativa del sistema ESD che installa pacchetti software e segnala lo stato al sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="dac6c-134">An optional part of your ESD system that installs software packages and reports status to the ESD system.</span></span>

## <span data-ttu-id="dac6c-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dac6c-135">Related topics</span></span>


[<span data-ttu-id="dac6c-136">Pianificazione per la compatibilità del sistema operativo dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="dac6c-136">Planning for Application Operating System Compatibility</span></span>](planning-for-application-operating-system-compatibility.md)

[<span data-ttu-id="dac6c-137">Preparare l'ambiente di distribuzione per MED-V</span><span class="sxs-lookup"><span data-stu-id="dac6c-137">Prepare the Deployment Environment for MED-V</span></span>](prepare-the-deployment-environment-for-med-v.md)

 

 





