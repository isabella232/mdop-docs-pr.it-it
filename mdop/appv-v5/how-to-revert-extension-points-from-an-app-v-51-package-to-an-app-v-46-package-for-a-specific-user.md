---
title: Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per un utente specifico
description: Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per un utente specifico
author: dansimp
ms.assetid: bd53c5d6-7fd2-4816-b03b-d59da0a35819
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a69d6fb5b180161f39aa89e03b52227f32ce4879
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805199"
---
# <span data-ttu-id="2c129-103">Come ripristinare i punti di estensione da un pacchetto App-V 5.1 a un pacchetto App-V 4.6 per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="2c129-103">How to Revert Extension Points From an App-V 5.1 Package to an App-V 4.6 Package for a Specific User</span></span>


<span data-ttu-id="2c129-104">Usare la procedura seguente per ripristinare un pacchetto App-V 5,1 nel formato di file App-V usando il file di configurazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2c129-104">Use the following procedure to revert an App-V 5.1 package to the App-V file format using the user configuration file.</span></span>

**<span data-ttu-id="2c129-105">Per ripristinare un pacchetto</span><span class="sxs-lookup"><span data-stu-id="2c129-105">To revert a package</span></span>**

1.  <span data-ttu-id="2c129-106">Assicurati che il pacchetto App-V 4,6 venga pubblicato dagli utenti, ma i accordi e i tasti di scelta rapida sono stati assunti dal pacchetto App-V 5,1 usando il metodo di migrazione seguente, [come eseguire la migrazione dei punti di estensione da un pacchetto App-v 4,6 a App-v 5,1 per un utente specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="2c129-106">Ensure that App-V 4.6 package is published to the users but the FTAs and shortcuts have been assumed by App-V 5.1 package using the following migration method, [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).</span></span>

    <span data-ttu-id="2c129-107">Nella sezione **userConfiguration** del file di configurazione della distribuzione per il pacchetto convertito, per impostare il criterio, eseguire l'aggiornamento seguente alla sezione **UserConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "false" PackageName = &lt; ID &gt; pacchetto**</span><span class="sxs-lookup"><span data-stu-id="2c129-107">In the **userConfiguration** section of the deployment configuration file for the converted package, to set the policy, make the following update to the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="false" PackageName=&lt;Package ID&gt;**</span></span>

2.  <span data-ttu-id="2c129-108">Da un prompt dei comandi con privilegi elevati digitare:</span><span class="sxs-lookup"><span data-stu-id="2c129-108">From an elevated command prompt, type:</span></span>

    <span data-ttu-id="2c129-109">PS &gt; **Publish-AppVClientPackage $pkg** -percorso DynamicUserConfigurationPath del &lt; file di configurazione utente&gt;</span><span class="sxs-lookup"><span data-stu-id="2c129-109">PS&gt;**Publish-AppVClientPackage $pkg –DynamicUserConfigurationPath** &lt;path to user configuration file&gt;</span></span>

3.  <span data-ttu-id="2c129-110">Eseguire un aggiornamento della pubblicazione o attendere il prossimo aggiornamento della pubblicazione pianificata per l'App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="2c129-110">Perform a publishing refresh, or wait for the next scheduled publishing refresh for the App-V 4.6.</span></span> <span data-ttu-id="2c129-111">Aprire l'applicazione usando accordi o i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="2c129-111">Open the application using FTAs or shortcuts.</span></span> <span data-ttu-id="2c129-112">L'applicazione deve ora aprirsi usando App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="2c129-112">The Application should now open using App-V 4.6.</span></span>

    **<span data-ttu-id="2c129-113">Nota</span><span class="sxs-lookup"><span data-stu-id="2c129-113">Note</span></span>**  
    <span data-ttu-id="2c129-114">Se non è più necessario il pacchetto App-V 5,1, è possibile annullare la pubblicazione del pacchetto App-V 5,1 e i punti di estensione verranno ripristinati automaticamente in App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="2c129-114">If you do not need the App-V 5.1 package anymore, you can unpublish the App-V 5.1 package and the extension points will automatically revert to App-V 4.6.</span></span>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="2c129-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2c129-115">Related topics</span></span>


[<span data-ttu-id="2c129-116">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2c129-116">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)









