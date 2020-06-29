---
ms.reviewer: ''
title: Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per un utente specifico
description: Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per un utente specifico
ms.assetid: f1d2ab1f-0831-4976-b49f-169511d3382a
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 2a0660024734806c508043cc2db030c96cfd16a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805205"
---
# <span data-ttu-id="67e92-103">Come ripristinare i punti di estensione da un pacchetto App-V 5.0 a un pacchetto App-V 4.6 per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="67e92-103">How to Revert Extension Points From an App-V 5.0 Package to an App-V 4.6 Package for a Specific User</span></span>

<span data-ttu-id="67e92-104">*Nota:*\* App-V 4,6 è uscito dal supporto mainstream.</span><span class="sxs-lookup"><span data-stu-id="67e92-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="67e92-105">Usare la procedura seguente per ripristinare un pacchetto App-V 5,0 nel formato di file App-V usando il file di configurazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="67e92-105">Use the following procedure to revert an App-V 5.0 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="67e92-106">Per ripristinare un pacchetto</span><span class="sxs-lookup"><span data-stu-id="67e92-106">To revert a package</span></span>**

1.  <span data-ttu-id="67e92-107">Assicurati che il pacchetto App-V 4,6 venga pubblicato dagli utenti, ma i accordi e i tasti di scelta rapida sono stati assunti dal pacchetto App-V 5,0 usando il metodo di migrazione seguente, [come eseguire la migrazione dei punti di estensione da un pacchetto App-v 4,6 a App-v 5,0 per un utente specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="67e92-107">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.0 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span></span>

    <span data-ttu-id="67e92-108">Nella sezione **userConfiguration** del file di configurazione della distribuzione per il pacchetto convertito, per impostare il criterio, eseguire l'aggiornamento seguente alla sezione **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; pacchetto**</span><span class="sxs-lookup"><span data-stu-id="67e92-108">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="67e92-109">Da un prompt dei comandi con privilegi elevati digitare:</span><span class="sxs-lookup"><span data-stu-id="67e92-109">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="67e92-110">PS &gt; **Publish-AppVClientPackage $pkg** -percorso DynamicUserConfigurationPath del &lt; file di configurazione utente&gt;</span><span class="sxs-lookup"><span data-stu-id="67e92-110">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="67e92-111">Eseguire un aggiornamento della pubblicazione o attendere il prossimo aggiornamento della pubblicazione pianificata per l'App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="67e92-111">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="67e92-112">Aprire l'applicazione usando accordi o i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="67e92-112">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="67e92-113">L'applicazione deve ora aprirsi usando App-V 4,6 SP2.</span><span class="sxs-lookup"><span data-stu-id="67e92-113">The Application should now open using App-V 4.6 SP2.</span></span>

    **<span data-ttu-id="67e92-114">Nota</span><span class="sxs-lookup"><span data-stu-id="67e92-114">Note</span></span>**  
    <span data-ttu-id="67e92-115">Se non è più necessario il pacchetto App-V 5,0, è possibile annullare la pubblicazione del pacchetto App-V 5,0 e i punti di estensione verranno ripristinati automaticamente in App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="67e92-115">If you do not need the App-V 5.0 package anymore, you can unpublish the App-V 5.0 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="67e92-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67e92-116">Related topics</span></span>


[<span data-ttu-id="67e92-117">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="67e92-117">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)












