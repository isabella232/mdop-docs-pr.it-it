---
title: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico
description: Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805307"
---
# <span data-ttu-id="debc2-103">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="debc2-103">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>

<span data-ttu-id="debc2-104">*Nota:*\* App-V 4,6 è uscito dal supporto mainstream.</span><span class="sxs-lookup"><span data-stu-id="debc2-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="debc2-105">Usare la procedura seguente per eseguire la migrazione dei pacchetti creati con App-V usando il file di configurazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="debc2-105">Use the following procedure to migrate packages created with App-V using the user configuration file.</span></span>

**<span data-ttu-id="debc2-106">Per convertire un pacchetto</span><span class="sxs-lookup"><span data-stu-id="debc2-106">To convert a package</span></span>**

1. <span data-ttu-id="debc2-107">Individuare il file di configurazione dell'utente per il pacchetto che si vuole convertire.</span><span class="sxs-lookup"><span data-stu-id="debc2-107">Locate the user configuration file for the package you want to convert.</span></span> <span data-ttu-id="debc2-108">Per impostare il criterio, eseguire gli aggiornamenti seguenti nella sezione **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="debc2-108">To set the policy, perform the following updates in the **userConfiguration** section: **ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName=&lt;Package ID&gt;**.</span></span>

   <span data-ttu-id="debc2-109">Di seguito è riportato un esempio di file di configurazione utente:</span><span class="sxs-lookup"><span data-stu-id="debc2-109">The following is an example of a user configuration file:</span></span>

   <span data-ttu-id="debc2-110">&lt;? XML version = "1.0"?&gt;</span><span class="sxs-lookup"><span data-stu-id="debc2-110">&lt;?xml version="1.0" ?&gt;</span></span>

   <span data-ttu-id="debc2-111">&lt;UserConfiguration PackageId = &lt; ID pacchetto &gt; DisplayName = &lt; nome del pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="debc2-111">&lt;UserConfiguration PackageId=&lt;Package ID&gt; DisplayName=&lt;Name of the Package&gt;</span></span>

   <span data-ttu-id="debc2-112">xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"</span><span class="sxs-lookup"><span data-stu-id="debc2-112">xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>; &lt;ManagingAuthority TakeoverExtensionPointsFrom46="true"</span></span>

   <span data-ttu-id="debc2-113">PackageName = &lt; ID pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="debc2-113">PackageName=&lt;Package ID&gt;</span></span>

   <span data-ttu-id="debc2-114">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="debc2-114">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="debc2-115">Per aggiungere il pacchetto App-V 5,0, digitare quanto segue in un prompt dei comandi di PowerShell con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="debc2-115">To add the App-V 5.0 package type the following in an elevated PowerShell command prompt:</span></span>

   <span data-ttu-id="debc2-116">PS &gt; **$pkg = Add-AppvClientPackage-** percorso percorso della &lt; posizione del pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="debc2-116">PS&gt;**$pkg= Add-AppvClientPackage –Path** &lt;Path to package location&gt;</span></span>

   <span data-ttu-id="debc2-117">PS &gt; **Publish-AppVClientPackage $pkg-percorso DynamicUserConfiguration** &lt; del file di configurazione utente&gt;</span><span class="sxs-lookup"><span data-stu-id="debc2-117">PS&gt;**Publish-AppVClientPackage $pkg -DynamicUserConfiguration** &lt;Path to the user configuration file&gt;</span></span>

3. <span data-ttu-id="debc2-118">Aprire l'applicazione usando accordi o i tasti di scelta rapida ora.</span><span class="sxs-lookup"><span data-stu-id="debc2-118">Open the application using FTAs or shortcuts now.</span></span> <span data-ttu-id="debc2-119">L'applicazione deve essere aperta usando App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="debc2-119">The application should open using App-V 5.0.</span></span>

   <span data-ttu-id="debc2-120">Il pacchetto App-V SP2 e il pacchetto convertito App-V 5,0 vengono pubblicati per l'utente, ma i accordi e i tasti di scelta rapida per le applicazioni sono stati assunti dal pacchetto App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="debc2-120">The App-V SP2 package and the converted App-V 5.0 package are published to the user, but the FTAs and shortcuts for the applications have been assumed by the App-V 5.0 package.</span></span>

   <span data-ttu-id="debc2-121">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="debc2-121">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="debc2-122">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="debc2-122">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="debc2-123">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="debc2-123">Got an App-V issue?</span></span>** <span data-ttu-id="debc2-124">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="debc2-124">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="debc2-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="debc2-125">Related topics</span></span>


[<span data-ttu-id="debc2-126">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="debc2-126">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





