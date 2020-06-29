---
title: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico
description: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico
ms.assetid: 3ae9996f-71d9-4ca1-9aab-25b599158e55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3c53104907448edeb894cf4eb9dbb0a24d3229e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805313"
---
# <span data-ttu-id="bd940-103">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="bd940-103">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>

<span data-ttu-id="bd940-104">**Nota:** App-V 4,6 è uscito dal supporto mainstream.</span><span class="sxs-lookup"><span data-stu-id="bd940-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="bd940-105">Usare la procedura seguente per eseguire la migrazione di punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5,0 usando il file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="bd940-105">Use the following procedure to migrate extension points from an App-V4.6package to a App-V 5.0 package using the deployment configuration file.</span></span>

<span data-ttu-id="bd940-106">**Nota**  La procedura seguente non richiede un server di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="bd940-106">**Note** The following procedure does not require an App-V 5.0 management server.</span></span>

 

**<span data-ttu-id="bd940-107">Per eseguire la migrazione di punti di estensione da un pacchetto da un pacchetto App-V 4.6 a un pacchetto convertito App-V 5,0 usando il file di configurazione della distribuzione</span><span class="sxs-lookup"><span data-stu-id="bd940-107">To migrate extension points from a package from an App-V4.6 package to a converted App-V 5.0 package using the deployment configuration file</span></span>**

1. <span data-ttu-id="bd940-108">Individuare la directory che contiene il file di configurazione della distribuzione per il pacchetto che si vuole eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="bd940-108">Locate the directory that contains the deployment configuration file for the package you want to migrate.</span></span> <span data-ttu-id="bd940-109">Per impostare il criterio, eseguire l'aggiornamento seguente alla sezione **userConfiguration** :</span><span class="sxs-lookup"><span data-stu-id="bd940-109">To set the policy, make the following update to the **userConfiguration** section:</span></span>

   **<span data-ttu-id="bd940-110">ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="bd940-110">ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;</span></span>**

   <span data-ttu-id="bd940-111">Di seguito è riportato un esempio di contenuto di un file di configurazione della distribuzione:</span><span class="sxs-lookup"><span data-stu-id="bd940-111">The following is an example of content from a deployment configuration file:</span></span>

   <span data-ttu-id="bd940-112">&lt;? XML version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="bd940-112">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="bd940-113">&lt;DeploymentConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd940-113">&lt;DeploymentConfiguration</span></span>

   <span data-ttu-id="bd940-114">xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageID = &lt; ID pacchetto &gt; DisplayName = &lt; nome visualizzato&gt;</span><span class="sxs-lookup"><span data-stu-id="bd940-114">xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration>" PackageId=&lt;Package ID&gt; DisplayName=&lt;Display Name&gt;</span></span>

   <span data-ttu-id="bd940-115">&lt;MachineConfiguration/&gt;</span><span class="sxs-lookup"><span data-stu-id="bd940-115">&lt;MachineConfiguration/&gt;</span></span>

   <span data-ttu-id="bd940-116">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="bd940-116">&lt;UserConfiguration&gt;</span></span>

   <span data-ttu-id="bd940-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="bd940-117">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="bd940-118">PackageName = &lt; ID pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="bd940-118">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="bd940-119">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="bd940-119">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="bd940-120">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="bd940-120">&lt;/DeploymentConfiguration&gt;</span></span>

2. <span data-ttu-id="bd940-121">Per aggiungere il pacchetto App-V 5,0, in un tipo di prompt dei comandi di PowerShell con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="bd940-121">To add the App-V 5.0 package, in an elevated PowerShell command prompt type:</span></span>

   <span data-ttu-id="bd940-122">PS &gt; **$pkg = Add-AppvClientPackage** **-** path path &lt; to package location &gt;  - **DynamicDeploymentConfiguration** &lt; percorso del file di configurazione della distribuzione&gt;</span><span class="sxs-lookup"><span data-stu-id="bd940-122">PS&gt;**$pkg= Add-AppvClientPackage** **–Path** &lt;Path to package location&gt; -**DynamicDeploymentConfiguration** &lt;Path to the deployment configuration file&gt;</span></span>

   <span data-ttu-id="bd940-123">PS &gt; **Publish-AppVClientPackage $pkg**</span><span class="sxs-lookup"><span data-stu-id="bd940-123">PS&gt;**Publish-AppVClientPackage $pkg**</span></span>

3. <span data-ttu-id="bd940-124">Per testare la migrazione, Apri l'applicazione virtuale usando le accordi o i tasti di scelta rapida associati.</span><span class="sxs-lookup"><span data-stu-id="bd940-124">To test the migration, open the virtual application using associated FTAs or shortcuts.</span></span> <span data-ttu-id="bd940-125">L'applicazione si apre con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="bd940-125">The application opens with App-V 5.0.</span></span> <span data-ttu-id="bd940-126">Sia il pacchetto App-V 4,6 che il pacchetto convertito App-V 5,0 vengono pubblicati per l'utente, ma i accordi e i tasti di scelta rapida per le applicazioni sono stati assunti dal pacchetto App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="bd940-126">Both, the App-V 4.6 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="bd940-127">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="bd940-127">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="bd940-128">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="bd940-128">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="bd940-129">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="bd940-129">Got an App-V issue?</span></span>** <span data-ttu-id="bd940-130">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="bd940-130">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="bd940-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd940-131">Related topics</span></span>


[<span data-ttu-id="bd940-132">Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="bd940-132">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[<span data-ttu-id="bd940-133">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="bd940-133">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





