---
title: Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico
description: Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico
ms.assetid: 2a43ca1b-6847-4dd1-ade2-336ac4ac6af0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 62542e5cd0b9dcb55f6e8f3db4d4f43c011a2839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805194"
---
# <span data-ttu-id="544f4-103">Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="544f4-103">How to Revert Extension Points from an App-V 5.0 Package to an App-V 4.6 Package For All Users on a Specific Computer</span></span>

<span data-ttu-id="544f4-104">*Nota:*\* App-V 4,6 è uscito dal supporto mainstream.</span><span class="sxs-lookup"><span data-stu-id="544f4-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="544f4-105">Il seguente presuppone che il client App-V 4,6 SP3 sia già installato.</span><span class="sxs-lookup"><span data-stu-id="544f4-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="544f4-106">Usare la procedura seguente per ripristinare i punti di estensione da un pacchetto App-V 5,0 al formato di file App-V 4,6 usando il file di configurazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="544f4-106">Use the following procedure to revert extension points from an App-V 5.0 package to the App-V 4.6 file format using the deployment configuration file.</span></span>

**<span data-ttu-id="544f4-107">Per ripristinare un pacchetto</span><span class="sxs-lookup"><span data-stu-id="544f4-107">To revert a package</span></span>**

1.  <span data-ttu-id="544f4-108">Assicurati che il pacchetto App-V 4,6 venga pubblicato dagli utenti, ma i accordi e i tasti di scelta rapida sono stati assunti dal pacchetto App-V 5,0 usando il metodo di migrazione seguente, [come eseguire la migrazione dei punti di estensione da un pacchetto App-v 4,6 a un pacchetto di App-v 5,0 convertito per tutti gli utenti di un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span><span class="sxs-lookup"><span data-stu-id="544f4-108">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md).</span></span>

    <span data-ttu-id="544f4-109">Nella sezione **userConfiguration** del file di configurazione della distribuzione per il pacchetto convertito, per impostare il criterio, eseguire l'aggiornamento seguente alla sezione **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; pacchetto**</span><span class="sxs-lookup"><span data-stu-id="544f4-109">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="544f4-110">Da un prompt dei comandi con privilegi elevati digitare:</span><span class="sxs-lookup"><span data-stu-id="544f4-110">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="544f4-111">PS &gt; **set-AppvClientPackage $pkg** -percorso DynamicDeploymentConfiguration del &lt; file di configurazione della distribuzione&gt;</span><span class="sxs-lookup"><span data-stu-id="544f4-111">PS&gt;**Set-AppvClientPackage $pkg –DynamicDeploymentConfiguration** &lt;path to deployment configuration file&gt;</span></span>

    <span data-ttu-id="544f4-112">PS &gt; **Publish-AppVClientPackage $pkg-DynamicUserConfigurationType useDeploymentConfiguration**</span><span class="sxs-lookup"><span data-stu-id="544f4-112">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationType useDeploymentConfiguration**</span></span>

3.  <span data-ttu-id="544f4-113">Eseguire un aggiornamento della pubblicazione o attendere il prossimo aggiornamento della pubblicazione pianificata per il pacchetto App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="544f4-113">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6 SP2 package.</span></span>

    <span data-ttu-id="544f4-114">Aprire l'applicazione usando accordi o i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="544f4-114">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="544f4-115">L'applicazione deve ora aprirsi usando App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="544f4-115">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="544f4-116">Nota</span><span class="sxs-lookup"><span data-stu-id="544f4-116">Note</span></span>**  
    <span data-ttu-id="544f4-117">Se non è più necessario il pacchetto App-V 5,0, è possibile annullare la pubblicazione del pacchetto App-V 5,0 e i punti di estensione verranno ripristinati automaticamente in App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="544f4-117">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="544f4-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="544f4-118">Related topics</span></span>


[<span data-ttu-id="544f4-119">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="544f4-119">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)









