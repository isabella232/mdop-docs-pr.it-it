---
title: Aggiornamento di MED-V 2.0
description: Aggiornamento di MED-V 2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823735"
---
# <span data-ttu-id="cbdfb-103">Aggiornamento di MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="cbdfb-103">Updating MED-V 2.0</span></span>


<span data-ttu-id="cbdfb-104">Proteggere il sistema applicando gli aggiornamenti di sicurezza appropriati per Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="cbdfb-104">Help secure your system by applying the appropriate security updates for Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="cbdfb-105">Aggiornamento di MED-V</span><span class="sxs-lookup"><span data-stu-id="cbdfb-105">Updating MED-V</span></span>


<span data-ttu-id="cbdfb-106">Puoi aggiornare MED-V in modo interattivo, dall'utente finale o in silenzio usando un sistema di distribuzione elettronica del software.</span><span class="sxs-lookup"><span data-stu-id="cbdfb-106">You can update MED-V interactively, by the end user, or silently by using an electronic software distribution system.</span></span> <span data-ttu-id="cbdfb-107">L'installazione dell'agente host MED-V aggiorna l'agente host MED-V e quindi aggiorna l'area di lavoro MED-V, se necessario.</span><span class="sxs-lookup"><span data-stu-id="cbdfb-107">Installation of the MED-V Host Agent upgrades the MED-V Host Agent and then updates the MED-V workspace if required.</span></span> <span data-ttu-id="cbdfb-108">L'agente host MED-V e l'agente guest continuano a essere sincronizzati. Se le applicazioni sono in esecuzione dall'area di lavoro MED-V mentre viene aggiornato l'agente host MED-V, è necessario riavviare il computer host per completare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="cbdfb-108">The MED-V Host Agent and Guest Agent keep in sync. If applications are running from the MED-V workspace while the MED-V Host Agent is being updated, a restart of the host computer is required to complete the update.</span></span> <span data-ttu-id="cbdfb-109">Se non sono in uso applicazioni, MED-V viene riavviato automaticamente e l'aggiornamento viene completato senza riavviare il computer host.</span><span class="sxs-lookup"><span data-stu-id="cbdfb-109">If no applications are running, MED-V is restarted automatically and the upgrade is completed without a restart of the host computer.</span></span>

<span data-ttu-id="cbdfb-110">Se si aggiorna MED-V usando un sistema di distribuzione elettronica del software, è possibile controllare il comportamento di riavvio.</span><span class="sxs-lookup"><span data-stu-id="cbdfb-110">If you are updating MED-V by using an electronic software distribution system, you can control the restart behavior.</span></span> <span data-ttu-id="cbdfb-111">Per eseguire questa operazione, eliminare il riavvio digitando **Riavvia = "ReallySuppress"** al prompt dei comandi durante l'installazione di MED-V\_HostAgent\_Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="cbdfb-111">To do this, suppress the restart by typing **REBOOT=”ReallySuppress”** at the command prompt when installing MED-V\_HostAgent\_Setup.exe.</span></span> <span data-ttu-id="cbdfb-112">Configura quindi il sistema di distribuzione elettronica del software per acquisire il codice restituito di 3010 (che segnala che è necessario riavviare il computer) ed eseguire il comportamento set restart.</span><span class="sxs-lookup"><span data-stu-id="cbdfb-112">Then, configure the electronic software distribution system to capture the 3010 return code (which signals that a restart is required) and perform the set restart behavior.</span></span>

## <span data-ttu-id="cbdfb-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cbdfb-113">Related topics</span></span>


[<span data-ttu-id="cbdfb-114">Documentazione tecnica su MED-V</span><span class="sxs-lookup"><span data-stu-id="cbdfb-114">Technical Reference for MED-V</span></span>](technical-reference-for-med-v.md)

 

 





