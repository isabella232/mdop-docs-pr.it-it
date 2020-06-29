---
title: Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico
description: Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico
author: dansimp
ms.assetid: 64640b8e-de6b-4006-a33e-353d285af15e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: ce8d5cc0e79be46fd9680a3bea0236bbeb93ea83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805193"
---
# <span data-ttu-id="cec94-103">Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="cec94-103">How to Revert Extension Points from an App-V 5.1 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>


<span data-ttu-id="cec94-104">Usare la procedura seguente per ripristinare i punti di estensione da un pacchetto App-V 5,1 al formato di file App-V 4,6 usando il file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="cec94-104">Use the following procedure to revert extension points from an App-V 5.1 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="cec94-105">Per ripristinare un pacchetto</span><span class="sxs-lookup"><span data-stu-id="cec94-105">To revert a package</span></span>**

1.  <span data-ttu-id="cec94-106">Assicurati che il pacchetto App-V 4,6 venga pubblicato dagli utenti, ma i accordi e i tasti di scelta rapida sono stati assunti dal pacchetto App-V 5,1 usando il metodo di migrazione seguente, [come eseguire la migrazione dei punti di estensione da un pacchetto App-v 4,6 a un pacchetto di App-v 5,1 convertito per tutti gli utenti di un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="cec94-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="cec94-107">Nella sezione **userConfiguration** del file di configurazione della distribuzione per il pacchetto convertito, per impostare il criterio, eseguire l'aggiornamento seguente alla sezione **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; pacchetto**</span><span class="sxs-lookup"><span data-stu-id="cec94-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="cec94-108">Da un prompt dei comandi con privilegi elevati digitare:</span><span class="sxs-lookup"><span data-stu-id="cec94-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="cec94-109">PS &gt; **set-AppvClientPackage $pkg** -percorso DynamicDeploymentConfiguration del &lt; file di configurazione della distribuzione&gt;</span><span class="sxs-lookup"><span data-stu-id="cec94-109">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="cec94-110">PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="cec94-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="cec94-111">Eseguire un aggiornamento della pubblicazione o attendere il prossimo aggiornamento della pubblicazione pianificata per il pacchetto App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="cec94-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 package.</span></span>

    <span data-ttu-id="cec94-112">Aprire l'applicazione usando accordi o i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="cec94-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="cec94-113">L'applicazione deve ora aprirsi usando App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="cec94-113">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="cec94-114">Nota</span><span class="sxs-lookup"><span data-stu-id="cec94-114">Note</span></span>**  
    <span data-ttu-id="cec94-115">Se non è più necessario il pacchetto App-V 5,1, è possibile annullare la pubblicazione del pacchetto App-V 5,1 e i punti di estensione verranno ripristinati automaticamente in App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="cec94-115">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="cec94-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cec94-116">Related topics</span></span>


[<span data-ttu-id="cec94-117">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="cec94-117">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









