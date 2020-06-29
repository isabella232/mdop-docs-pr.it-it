---
title: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.1 convertito per tutti gli utenti in un computer specifico
description: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.1 convertito per tutti gli utenti in un computer specifico
author: dansimp
ms.assetid: 4ef823a5-3106-44c5-aecc-29edf69c2fbb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 7bac244804b46309a0e0a75cb3742dfe22e92e8f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805308"
---
# <span data-ttu-id="efdb2-103">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.1 convertito per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="efdb2-103">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>


<span data-ttu-id="efdb2-104">Usare la procedura seguente per eseguire la migrazione di punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5,1 usando il file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="efdb2-104">Use the following procedure to migrate extension points from an App-V4.6 package to a App-V 5.1 package using the deployment configuration file.</span></span>

<span data-ttu-id="efdb2-105">**Nota**  Questa procedura presuppone che si esegua l'ultima versione di App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="efdb2-105">**Note** This procedure assumes that you are running the latest version of App-V 4.6.</span></span>  
<span data-ttu-id="efdb2-106">La procedura seguente non richiede un server di gestione di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="efdb2-106">The following procedure does not require an App-V 5.1 management server.</span></span>

 

**<span data-ttu-id="efdb2-107">Per eseguire la migrazione di punti di estensione da un pacchetto da un pacchetto App-V 4.6 a un pacchetto convertito App-V 5,1 usando il file di configurazione della distribuzione</span><span class="sxs-lookup"><span data-stu-id="efdb2-107">To migrate extension points from a package from an App-V4.6 package to a converted App-V 5.1 package using the deployment configuration file</span></span>**

1. <span data-ttu-id="efdb2-108">Individuare la directory che contiene il file di configurazione della distribuzione per il pacchetto che si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="efdb2-108">Locate the directory that contains the deployment configuration file for the package you want to migrate.</span></span> <span data-ttu-id="efdb2-109">Per impostare il criterio, eseguire l'aggiornamento seguente alla sezione **userConfiguration** :</span><span class="sxs-lookup"><span data-stu-id="efdb2-109">To set the policy, make the following update to the **userConfiguration** section:</span></span>

   **<span data-ttu-id="efdb2-110">ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="efdb2-110">ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;</span></span>**

   <span data-ttu-id="efdb2-111">Di seguito è riportato un esempio di contenuto di un file di configurazione della distribuzione:</span><span class="sxs-lookup"><span data-stu-id="efdb2-111">The following is an example of content from a deployment configuration file:</span></span>

   <span data-ttu-id="efdb2-112">&lt;? XML version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="efdb2-112">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="efdb2-113">&lt;DeploymentConfiguration</span><span class="sxs-lookup"><span data-stu-id="efdb2-113">&lt;DeploymentConfiguration</span></span>

   <span data-ttu-id="efdb2-114">xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageID = &lt; ID pacchetto &gt; DisplayName = &lt; nome visualizzato&gt;</span><span class="sxs-lookup"><span data-stu-id="efdb2-114">xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration>" PackageId=&lt;Package ID&gt; DisplayName=&lt;Display Name&gt;</span></span>

   <span data-ttu-id="efdb2-115">&lt;MachineConfiguration/&gt;</span><span class="sxs-lookup"><span data-stu-id="efdb2-115">&lt;MachineConfiguration/&gt;</span></span>

   <span data-ttu-id="efdb2-116">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="efdb2-116">&lt;UserConfiguration&gt;</span></span>

   <span data-ttu-id="efdb2-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="efdb2-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="efdb2-118">PackageName = &lt; ID pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="efdb2-118">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="efdb2-119">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="efdb2-119">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="efdb2-120">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="efdb2-120">&lt;/DeploymentConfiguration&gt;</span></span>

2. <span data-ttu-id="efdb2-121">Per aggiungere il pacchetto App-V 5,1, in un tipo di prompt dei comandi di PowerShell con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="efdb2-121">To add the App-V 5.1 package, in an elevated PowerShell command prompt type:</span></span>

   <span data-ttu-id="efdb2-122">PS &gt; **$pkg = Add-AppvClientPackage** **-** path path &lt; to package location &gt;  - **DynamicDeploymentConfiguration** &lt; percorso del file di configurazione della distribuzione&gt;</span><span class="sxs-lookup"><span data-stu-id="efdb2-122">PS&gt;**$pkg= Add-AppvClientPackage** **–Path** &lt;Path to package location&gt; -**DynamicDeploymentConfiguration** &lt;Path to the deployment configuration file&gt;</span></span>

   <span data-ttu-id="efdb2-123">PS &gt; **Publish-AppVClientPackage $pkg**</span><span class="sxs-lookup"><span data-stu-id="efdb2-123">PS&gt;**Publish-AppVClientPackage $pkg**</span></span>

3. <span data-ttu-id="efdb2-124">Per testare la migrazione, Apri l'applicazione virtuale usando le accordi o i tasti di scelta rapida associati.</span><span class="sxs-lookup"><span data-stu-id="efdb2-124">To test the migration, open the virtual application using associated FTAs or shortcuts.</span></span> <span data-ttu-id="efdb2-125">L'applicazione si apre con App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="efdb2-125">The application opens with App-V 5.1.</span></span> <span data-ttu-id="efdb2-126">Sia il pacchetto App-V 4,6 che il pacchetto convertito App-V 5,1 vengono pubblicati per l'utente, ma i accordi e i tasti di scelta rapida per le applicazioni sono stati assunti dal pacchetto App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="efdb2-126">Both, the App-V 4.6 package and the converted App-V 5.1 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.1 package.</span></span>

   <span data-ttu-id="efdb2-127">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="efdb2-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="efdb2-128">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="efdb2-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="efdb2-129">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="efdb2-129">Got an App-V issue?</span></span>** <span data-ttu-id="efdb2-130">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="efdb2-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="efdb2-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="efdb2-131">Related topics</span></span>


[<span data-ttu-id="efdb2-132">Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="efdb2-132">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="efdb2-133">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="efdb2-133">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





