---
title: Come lavorare online o offline con Application Virtualization
description: Come lavorare online o offline con Application Virtualization
author: dansimp
ms.assetid: aa532b37-8a00-4db4-9b51-e1e8354b2495
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0dfdd315fe607156135247c4a34d0248ef8fbdd9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816376"
---
# <span data-ttu-id="ab507-103">Come lavorare online o offline con Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="ab507-103">How to Work Offline or Online with Application Virtualization</span></span>


<span data-ttu-id="ab507-104">Se si prevede di essere disconnessi dalla rete per un periodo di tempo prolungato, è possibile lavorare in modalità offline per eliminare eventuali ritardi quando il client di virtualizzazione dell'applicazione tenta di comunicare con il server.</span><span class="sxs-lookup"><span data-stu-id="ab507-104">If you plan to be disconnected from the network for an extended period of time, you can work in offline mode to eliminate possible delays when the Application Virtualization client attempts to communicate with the server.</span></span> <span data-ttu-id="ab507-105">In modalità offline l'Application Virtualization Client non tenterà di comunicare con il server di pubblicazione, quindi le applicazioni devono essere completamente memorizzate nella cache prima di abilitare la modalità offline.</span><span class="sxs-lookup"><span data-stu-id="ab507-105">In offline mode, the Application Virtualization client will not attempt to communicate with the publishing server, so applications must be fully cached before enabling offline mode.</span></span> <span data-ttu-id="ab507-106">Le applicazioni non verranno recuperate dalla condivisione di contenuto, anche se sono nel disco locale nel computer.</span><span class="sxs-lookup"><span data-stu-id="ab507-106">Applications will not be retrieved from the content share even if they are on the local disk on the computer.</span></span> <span data-ttu-id="ab507-107">È possibile usare la procedura client Application Virtualization seguente per passare dalla modalità offline a quella online.</span><span class="sxs-lookup"><span data-stu-id="ab507-107">You can use the following Application Virtualization Client procedure to toggle between working offline and online.</span></span>

<span data-ttu-id="ab507-108">**Nota**  Per impostazione predefinita, il **lavoro offline** è disabilitato per il client per Servizi Desktop remoto (in precedenza Servizi terminal).</span><span class="sxs-lookup"><span data-stu-id="ab507-108">**Note** By default, **Work Offline** is disabled for the Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="ab507-109">L'amministratore di sistema deve modificare le autorizzazioni utente per consentire l'uso di questa impostazione in un client per Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="ab507-109">Your system administrator must change your user permissions to allow you to use this setting on a Client for Remote Desktop Services.</span></span>

 

**<span data-ttu-id="ab507-110">Per lavorare offline</span><span class="sxs-lookup"><span data-stu-id="ab507-110">To work offline</span></span>**

-   <span data-ttu-id="ab507-111">Fare clic con il pulsante destro del mouse sull'icona del sistema di virtualizzazione dell'applicazione nell'area di notifica e scegliere **lavora offline** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="ab507-111">Right-click the Application Virtualization System icon in the notification area, and select **Work Offline** from the pop-up menu.</span></span>

**<span data-ttu-id="ab507-112">Per lavorare online</span><span class="sxs-lookup"><span data-stu-id="ab507-112">To work online</span></span>**

-   <span data-ttu-id="ab507-113">Fare clic con il pulsante destro del mouse sull'icona del sistema di virtualizzazione dell'applicazione nell'area di notifica e scegliere **lavora online** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="ab507-113">Right-click the Application Virtualization System icon in the notification area, and select **Work Online** from the pop-up menu.</span></span>

## <span data-ttu-id="ab507-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab507-114">Related topics</span></span>


[<span data-ttu-id="ab507-115">Come usare l'area di notifica del desktop per Application Virtualization Client Management</span><span class="sxs-lookup"><span data-stu-id="ab507-115">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





