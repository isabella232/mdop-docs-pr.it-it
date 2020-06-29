---
title: Configurazione del firewall per i server App-V
description: Configurazione del firewall per i server App-V
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821816"
---
# <span data-ttu-id="907cb-103">Configurazione del firewall per i server App-V</span><span class="sxs-lookup"><span data-stu-id="907cb-103">Configuring the Firewall for the App-V Servers</span></span>


<span data-ttu-id="907cb-104">Dopo aver installato Microsoft Application Virtualization (App-V) Management Server o streaming server e averlo configurato per l'uso del protocollo RTSP o RTSPs, è necessario creare eccezioni del firewall per i programmi App-V.</span><span class="sxs-lookup"><span data-stu-id="907cb-104">After you install the Microsoft Application Virtualization (App-V) Management Server or Streaming Server and configure it to use the RTSP or RTSPS protocol, you must create firewall exceptions for the App-V programs.</span></span>

## <span data-ttu-id="907cb-105">Configurazione delle eccezioni del firewall per Application Virtualization Management Server</span><span class="sxs-lookup"><span data-stu-id="907cb-105">Configuring Firewall Exceptions for Application Virtualization Management Server</span></span>


<span data-ttu-id="907cb-106">Creare un'eccezione del firewall per **sghwdsptr.exe** e **sghwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="907cb-106">Create a firewall exception for **sghwdsptr.exe** and **sghwsvr.exe**.</span></span> <span data-ttu-id="907cb-107">Questi programmi si trovano nella cartella C:\\Programmi \\Programmi\\microsoft System Center App Virt Management Server\\App Virt Management Server\\bin in un sistema operativo a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="907cb-107">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="907cb-108">Se si usa una versione del sistema operativo a 64 bit, la cartella si trova in file C:\\Programmi (x86) \\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="907cb-108">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Management Server\\App Virt Management Server\\bin.</span></span>

## <span data-ttu-id="907cb-109">Configurazione delle eccezioni del firewall per Application Virtualization Streaming Server</span><span class="sxs-lookup"><span data-stu-id="907cb-109">Configuring Firewall Exceptions for Application Virtualization Streaming Server</span></span>


<span data-ttu-id="907cb-110">Creare un'eccezione del firewall per **sglwdsptr.exe** e **sglwsvr.exe**.</span><span class="sxs-lookup"><span data-stu-id="907cb-110">Create a firewall exception for **sglwdsptr.exe** and **sglwsvr.exe**.</span></span> <span data-ttu-id="907cb-111">Questi programmi si trovano nella cartella C:\\Programmi \\Programmi\\microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin in un sistema operativo a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="907cb-111">These programs are found in the folder C:\\Program Files\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin on a 32-bit operating system.</span></span> <span data-ttu-id="907cb-112">Se si usa una versione del sistema operativo a 64 bit, la cartella si trova in file C:\\Programmi (x86) \\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.</span><span class="sxs-lookup"><span data-stu-id="907cb-112">If you are using a 64-bit operating system version, the folder is located under C:\\Program Files (x86)\\Microsoft System Center App Virt Streaming Server\\App Virt Streaming Server\\bin.</span></span>

## <span data-ttu-id="907cb-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="907cb-113">Related topics</span></span>


[<span data-ttu-id="907cb-114">Come configurare i server per la distribuzione basata su server</span><span class="sxs-lookup"><span data-stu-id="907cb-114">How to Configure Servers for Server-Based Deployment</span></span>](how-to-configure-servers-for-server-based-deployment.md)

[<span data-ttu-id="907cb-115">Come installare e configurare l'applicazione predefinita</span><span class="sxs-lookup"><span data-stu-id="907cb-115">How to Install and Configure the Default Application</span></span>](how-to-install-and-configure-the-default-application.md)

 

 




