---
title: Come applicare il file di configurazione utente con PowerShell
description: Come applicare il file di configurazione utente con PowerShell
author: dansimp
ms.assetid: f7d7c595-4fdd-4096-b53d-9eead111c339
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95ae5840f5eee04a29431716a956ddec7d0487aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805727"
---
# <span data-ttu-id="2afdd-103">Come applicare il file di configurazione utente con PowerShell</span><span class="sxs-lookup"><span data-stu-id="2afdd-103">How to Apply the User Configuration File by Using PowerShell</span></span>


<span data-ttu-id="2afdd-104">Il file di configurazione dell'utente dinamico viene applicato quando un pacchetto viene pubblicato in un utente specifico e determina il modo in cui verrà eseguito il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2afdd-104">The dynamic user configuration file is applied when a package is published to a specific user and determines how the package will run.</span></span>

<span data-ttu-id="2afdd-105">Usare la procedura seguente per specificare un file di configurazione specifico dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2afdd-105">Use the following procedure to specify a user-specific configuration file.</span></span> <span data-ttu-id="2afdd-106">La procedura seguente si basa sull'esempio:</span><span class="sxs-lookup"><span data-stu-id="2afdd-106">The following procedure is based on the example:</span></span>

**<span data-ttu-id="2afdd-107">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="2afdd-107">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="2afdd-108">Per applicare un file di configurazione utente</span><span class="sxs-lookup"><span data-stu-id="2afdd-108">To apply a user Configuration file</span></span>**

1.  <span data-ttu-id="2afdd-109">Per aggiungere il pacchetto al computer usando la console di PowerShell, digitare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="2afdd-109">To add the package to the computer using the PowerShell console type the following command:</span></span>

    <span data-ttu-id="2afdd-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.AppV**.</span><span class="sxs-lookup"><span data-stu-id="2afdd-110">**Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**.</span></span>

2.  <span data-ttu-id="2afdd-111">Usare il comando seguente per pubblicare il pacchetto nell'utente e specificare il file di configurazione dell'utente dinamico aggiornato:</span><span class="sxs-lookup"><span data-stu-id="2afdd-111">Use the following command to publish the package to the user and specify the updated the dynamic user configuration file:</span></span>

    **<span data-ttu-id="2afdd-112">Publish-AppVClientPackage $pkg-DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span><span class="sxs-lookup"><span data-stu-id="2afdd-112">Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml</span></span>**

    <span data-ttu-id="2afdd-113">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="2afdd-113">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2afdd-114">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="2afdd-114">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2afdd-115">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="2afdd-115">Got an App-V issue?</span></span>** <span data-ttu-id="2afdd-116">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2afdd-116">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2afdd-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2afdd-117">Related topics</span></span>


[<span data-ttu-id="2afdd-118">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="2afdd-118">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





