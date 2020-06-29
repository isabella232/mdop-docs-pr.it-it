---
title: Configurare i prerequisiti di ambiente
description: Configurare i prerequisiti di ambiente
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826446"
---
# <span data-ttu-id="95b81-103">Configurare i prerequisiti di ambiente</span><span class="sxs-lookup"><span data-stu-id="95b81-103">Configure Environment Prerequisites</span></span>


<span data-ttu-id="95b81-104">Prima di poter distribuire ed eseguire Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, è necessario assicurarsi che l'ambiente soddisfi i prerequisiti minimi seguenti.</span><span class="sxs-lookup"><span data-stu-id="95b81-104">Before you can deploy and run Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, you must ensure that your environment meets the following minimum prerequisites.</span></span>

**<span data-ttu-id="95b81-105">Windows 7</span><span class="sxs-lookup"><span data-stu-id="95b81-105">Windows 7</span></span>**

<span data-ttu-id="95b81-106">L'agente host MED-V e il Packager area di lavoro MED-V sono supportati solo in Windows 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="95b81-106">The MED-V Host Agent and the MED-V Workspace Packager are only supported in Windows 7 or newer.</span></span>

**<span data-ttu-id="95b81-107">Windows XP SP3</span><span class="sxs-lookup"><span data-stu-id="95b81-107">Windows XP SP3</span></span>**

<span data-ttu-id="95b81-108">L'agente guest MED-V è supportato solo in Windows XP SP3.</span><span class="sxs-lookup"><span data-stu-id="95b81-108">The MED-V Guest Agent is only supported in Windows XP SP3.</span></span>

**<span data-ttu-id="95b81-109">.NET Framework 3,5 SP1</span><span class="sxs-lookup"><span data-stu-id="95b81-109">.NET Framework 3.5 SP1</span></span>**

<span data-ttu-id="95b81-110">Gli agenti Guest e host MED-V e Packager area di lavoro MED-V richiedono Microsoft .NET Framework 3,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="95b81-110">The MED-V Host and Guest agents and the MED-V Workspace Packager require the Microsoft .NET Framework 3.5 SP1.</span></span>

<span data-ttu-id="95b81-111">**Importante**  È inoltre necessario installare l'aggiornamento [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) https://go.microsoft.com/fwlink/?LinkId=204950) , che affronta diversi problemi noti di compatibilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="95b81-111">**Important** You must also install the update [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (https://go.microsoft.com/fwlink/?LinkId=204950), which addresses several known application compatibility issues.</span></span>

 

<span data-ttu-id="95b81-112">**Nota**  È necessario installare manualmente .NET Framework 3,5 SP1 e l'aggiornamento di KB959209 nell'immagine di Windows Virtual PC preparata per l'uso con MED-V.</span><span class="sxs-lookup"><span data-stu-id="95b81-112">**Note** You must manually install the .NET Framework 3.5 SP1 and the update KB959209 into the Windows Virtual PC image that you prepare for use with MED-V.</span></span> <span data-ttu-id="95b81-113">Per impostazione predefinita, tuttavia, Microsoft .NET Framework 3,5 SP1 e l'aggiornamento sono inclusi quando si installa Windows 7 nel computer host.</span><span class="sxs-lookup"><span data-stu-id="95b81-113">However, by default, the Microsoft .NET Framework 3.5 SP1 and the update are included when you install Windows 7 on the host computer.</span></span>

 

**<span data-ttu-id="95b81-114">Infrastruttura di Active Directory</span><span class="sxs-lookup"><span data-stu-id="95b81-114">An Active Directory Infrastructure</span></span>**

<span data-ttu-id="95b81-115">Criteri di gruppo offre la gestione centralizzata e la configurazione di sistemi operativi, applicazioni e impostazioni degli utenti in un ambiente Active Directory.</span><span class="sxs-lookup"><span data-stu-id="95b81-115">Group Policy provides the centralized management and configuration of operating systems, applications, and users' settings in an Active Directory environment.</span></span>

## <span data-ttu-id="95b81-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="95b81-116">Related topics</span></span>


[<span data-ttu-id="95b81-117">Configurare i prerequisiti di installazione</span><span class="sxs-lookup"><span data-stu-id="95b81-117">Configure Installation Prerequisites</span></span>](configure-installation-prerequisites.md)

[<span data-ttu-id="95b81-118">Architettura di alto livello</span><span class="sxs-lookup"><span data-stu-id="95b81-118">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="95b81-119">Configurazioni supportate di MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="95b81-119">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





