---
title: Informazioni su User Experience Virtualization 1.0
description: Informazioni su User Experience Virtualization 1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822715"
---
# <span data-ttu-id="e6bb7-103">Informazioni su User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="e6bb7-103">About User Experience Virtualization 1.0</span></span>


<span data-ttu-id="e6bb7-104">Microsoft User Experience Virtualization (UE-V) monitora le modifiche apportate dagli utenti alle impostazioni delle applicazioni e alle impostazioni del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="e6bb7-104">Microsoft User Experience Virtualization (UE-V) monitors the changes that are made by users to application settings and Windows operating system settings.</span></span> <span data-ttu-id="e6bb7-105">Le impostazioni utente vengono acquisite e centralizzate in una posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="e6bb7-105">The user settings are captured and centralized to a settings storage location.</span></span> <span data-ttu-id="e6bb7-106">Queste impostazioni possono quindi essere applicate ai diversi computer a cui l'utente ha eseguito l'accesso, inclusi i computer desktop, i computer portatili e le sessioni VDI (Virtual Desktop Infrastructure).</span><span class="sxs-lookup"><span data-stu-id="e6bb7-106">These settings can then be applied to the different computers that are accessed by the user, including desktop computers, laptop computers, and virtual desktop infrastructure (VDI) sessions.</span></span>

<span data-ttu-id="e6bb7-107">User Experience Virtualization usa i modelli di posizione delle impostazioni per specificare quali applicazioni e impostazioni di Windows nei computer degli utenti vengono monitorate e centralizzate.</span><span class="sxs-lookup"><span data-stu-id="e6bb7-107">User Experience Virtualization uses settings location templates to specify what applications and Windows settings on the user computers are monitored and centralized.</span></span> <span data-ttu-id="e6bb7-108">Il modello di posizione delle impostazioni è un file XML che specifica quali posizioni di file e del registro di sistema sono associate a ogni applicazione o impostazione di sistemi operativi.</span><span class="sxs-lookup"><span data-stu-id="e6bb7-108">The settings location template is an XML file that specifies which file and registry locations are associated with each application or operating system setting.</span></span> <span data-ttu-id="e6bb7-109">Il modello non contiene valori per le impostazioni; contiene solo le posizioni delle impostazioni da monitorare.</span><span class="sxs-lookup"><span data-stu-id="e6bb7-109">The template does not contain values for the settings; it contains only the locations of the settings that are to be monitored.</span></span>

<span data-ttu-id="e6bb7-110">Le impostazioni dell'applicazione e le impostazioni di Windows vengono monitorate da UE-V quando gli utenti stanno lavorando ai loro computer.</span><span class="sxs-lookup"><span data-stu-id="e6bb7-110">The application settings and Windows settings are monitored by UE-V when users are working on their computers.</span></span> <span data-ttu-id="e6bb7-111">I valori per le impostazioni dell'applicazione sono archiviati nel server di archiviazione delle impostazioni quando l'utente chiude l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e6bb7-111">The values for the application settings are stored on the settings storage server when the user closes the application.</span></span> <span data-ttu-id="e6bb7-112">I valori per le impostazioni di Windows vengono archiviati quando l'utente si disconnette, quando il computer è bloccato o quando si disconnette in remoto da un computer.</span><span class="sxs-lookup"><span data-stu-id="e6bb7-112">The values for the Windows settings are stored when the user logs off, when the computer is locked, or when they disconnect remotely from a computer.</span></span>

<span data-ttu-id="e6bb7-113">Un amministratore può creare un modello di posizione delle impostazioni di UE-V per specificare quali impostazioni dell'applicazione aziendale andranno in roaming.</span><span class="sxs-lookup"><span data-stu-id="e6bb7-113">An administrator can create a UE-V settings location template to specify which enterprise application settings will roam.</span></span> <span data-ttu-id="e6bb7-114">UE-V include un set di modelli di posizione delle impostazioni per alcune applicazioni Microsoft e le impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="e6bb7-114">UE-V includes a set of settings location templates for some Microsoft applications and Windows settings.</span></span> <span data-ttu-id="e6bb7-115">Per un elenco delle applicazioni e delle impostazioni predefinite in UE-V, vedere [pianificazione delle applicazioni da sincronizzare con UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="e6bb7-115">For a list of default applications and settings in UE-V, see [Planning Which Applications to Synchronize with UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md).</span></span>

## <span data-ttu-id="e6bb7-116">Note sulla versione di UEV 1,0</span><span class="sxs-lookup"><span data-stu-id="e6bb7-116">UEV 1.0 Release Notes</span></span>


<span data-ttu-id="e6bb7-117">Per altre informazioni e per le ultime notizie che non hanno reso disponibile la documentazione, vedere [Note sulla versione di Microsoft User Experience Virtualization (UE-V) 1,0](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="e6bb7-117">For more information, and for late-breaking news that did not make it into the documentation, see [Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).</span></span>

## <span data-ttu-id="e6bb7-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6bb7-118">Related topics</span></span>


[<span data-ttu-id="e6bb7-119">Attività iniziali di User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="e6bb7-119">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="e6bb7-120">Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="e6bb7-120">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="e6bb7-121">Architettura di alto livello per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="e6bb7-121">High-Level Architecture for UE-V 1.0</span></span>](high-level-architecture-for-ue-v-10.md)

 

 





