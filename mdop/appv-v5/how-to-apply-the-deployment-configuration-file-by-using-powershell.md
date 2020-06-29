---
title: Come applicare il file di configurazione della distribuzione con PowerShell
description: Come applicare il file di configurazione della distribuzione con PowerShell
author: dansimp
ms.assetid: 5df5d5bc-6c72-4087-8b93-d6d4b502a1f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6764f07dfe8cff1fb30c354937a405202468428
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805733"
---
# <span data-ttu-id="9e75a-103">Come applicare il file di configurazione della distribuzione con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e75a-103">How to Apply the Deployment Configuration File by Using PowerShell</span></span>


<span data-ttu-id="9e75a-104">Il file di configurazione della distribuzione dinamica viene applicato quando un pacchetto viene aggiunto o impostato su un computer che gestisce il client App-V 5,0 prima che il pacchetto sia stato pubblicato.</span><span class="sxs-lookup"><span data-stu-id="9e75a-104">The dynamic deployment configuration file is applied when a package is added or set to a computer running the App-V 5.0 client before the package has been published.</span></span> <span data-ttu-id="9e75a-105">Il file configura le impostazioni predefinite per il pacchetto per tutti gli utenti nel computer che gestisce il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="9e75a-105">The file configures the default settings for package for all users on the computer running the App-V 5.0 client.</span></span> <span data-ttu-id="9e75a-106">Questa sezione descrive i passaggi usati per usare un file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="9e75a-106">This section describes the steps used to use a deployment configuration file.</span></span> <span data-ttu-id="9e75a-107">La procedura si basa sull'esempio seguente e presuppone che il pacchetto e i file di configurazione seguenti siano presenti in un computer:</span><span class="sxs-lookup"><span data-stu-id="9e75a-107">The procedure is based on the following example and assumes the following package and configuration files exist on a computer:</span></span>

**<span data-ttu-id="9e75a-108">c:\\Packages\\Contoso\\MyApp.appv</span><span class="sxs-lookup"><span data-stu-id="9e75a-108">c:\\Packages\\Contoso\\MyApp.appv</span></span>**

**<span data-ttu-id="9e75a-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="9e75a-109">c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

**<span data-ttu-id="9e75a-110">Per applicare il file di configurazione della distribuzione tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="9e75a-110">To Apply the Deployment Configuration File Using PowerShell</span></span>**

-   <span data-ttu-id="9e75a-111">Per specificare un nuovo set predefinito di configurazioni per tutti gli utenti che eseguiranno il pacchetto in un computer specifico, usando una console di PowerShell, digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="9e75a-111">To specify a new default set of configurations for all users who will run the package on a specific computer, using a PowerShell console type the following:</span></span>

    **<span data-ttu-id="9e75a-112">Add-AppVClientPackage – path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="9e75a-112">Add-AppVClientPackage –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**

    **<span data-ttu-id="9e75a-113">Nota</span><span class="sxs-lookup"><span data-stu-id="9e75a-113">Note</span></span>**  
    <span data-ttu-id="9e75a-114">Questo comando acquisisce l'oggetto risultante in $pkg.</span><span class="sxs-lookup"><span data-stu-id="9e75a-114">This command captures the resulting object into $pkg.</span></span> <span data-ttu-id="9e75a-115">Se il pacchetto è già presente nel computer, è possibile usare il cmdlet **set-AppVclientPackage** per applicare il documento di configurazione della distribuzione:</span><span class="sxs-lookup"><span data-stu-id="9e75a-115">If the package is already present on the computer, the **Set-AppVclientPackage** cmdlet can be used to apply the deployment configuration document:</span></span>

    **<span data-ttu-id="9e75a-116">Set-AppVClientPackage-Name MyApp-path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span><span class="sxs-lookup"><span data-stu-id="9e75a-116">Set-AppVClientPackage –Name Myapp –Path c:\\Packages\\Contoso\\MyApp.appv -DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml</span></span>**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="9e75a-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9e75a-117">Related topics</span></span>


[<span data-ttu-id="9e75a-118">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="9e75a-118">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









