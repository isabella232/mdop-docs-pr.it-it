---
title: Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer
description: Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805529"
---
# <span data-ttu-id="0408d-103">Come distribuire l'App-V 4,6 e il client App-V 5,1 nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="0408d-103">How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer</span></span>

<span data-ttu-id="0408d-104">**Nota:** App-V 4,6 è uscito dal supporto mainstream.</span><span class="sxs-lookup"><span data-stu-id="0408d-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span>

<span data-ttu-id="0408d-105">Usare le informazioni seguenti per installare il client di Microsoft Application Virtualization (App-V) 5,1 (preferibilmente con i Service Pack più recenti e gli hotfix) e il client App-V 4.6 SP2 o il client App-V 4.6 S3 nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="0408d-105">Use the following information to install the Microsoft Application Virtualization (App-V) 5.1 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP2 client or the App-V 4.6S3 client on the same computer.</span></span> <span data-ttu-id="0408d-106">Per le versioni supportate, i requisiti e altre informazioni sulla pianificazione, vedere [pianificazione della migrazione da una versione precedente di App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span><span class="sxs-lookup"><span data-stu-id="0408d-106">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).</span></span>

**<span data-ttu-id="0408d-107">Per distribuire client App-V 5,1 e client App-V 4,6 nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="0408d-107">To deploy the App-V 5.1 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="0408d-108">Installare la versione seguente del client App-V nel computer in cui è in esecuzione App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="0408d-108">Install the following version of the App-V client on the computer that is running App-V 4.6.</span></span>

    -   [<span data-ttu-id="0408d-109">Microsoft Application Virtualization 4,6 Service Pack 3</span><span class="sxs-lookup"><span data-stu-id="0408d-109">Microsoft Application Virtualization 4.6 Service Pack 3</span></span>](https://www.microsoft.com/download/details.aspx?id=41187)

2.  <span data-ttu-id="0408d-110">Installare il client App-V 5,1 nel computer in cui è in esecuzione la versione App-V 4,6 SP3 del client.</span><span class="sxs-lookup"><span data-stu-id="0408d-110">Install the App-V 5.1 client on the computer that is running the App-V 4.6 SP3 version of the client.</span></span> <span data-ttu-id="0408d-111">Per ottenere risultati ottimali, è consigliabile installare tutti gli aggiornamenti disponibili per il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="0408d-111">For best results, we recommend that you install all available updates to the App-V 5.1 client.</span></span>

3.  <span data-ttu-id="0408d-112">Convertire o rieseguire la sequenza graduale dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="0408d-112">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="0408d-113">Per convertire i pacchetti, usa il convertitore di pacchetti App-V 5,1 e Converti i pacchetti necessari nel formato di file App-V 5,1 (**. AppV**).</span><span class="sxs-lookup"><span data-stu-id="0408d-113">To convert the packages, use the App-V 5.1 package converter and convert the required packages to the App-V 5.1 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="0408d-114">Per risequenziare i pacchetti, è consigliabile usare la versione più recente del sequencer per ottenere risultati ottimali.</span><span class="sxs-lookup"><span data-stu-id="0408d-114">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="0408d-115">Per altre informazioni sulla pubblicazione di pacchetti, vedere [come pubblicare un pacchetto tramite la console di gestione](how-to-publish-a-package-by-using-the-management-console-51.md).</span><span class="sxs-lookup"><span data-stu-id="0408d-115">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md).</span></span>

4.  <span data-ttu-id="0408d-116">Distribuire pacchetti ai computer client.</span><span class="sxs-lookup"><span data-stu-id="0408d-116">Deploy packages to the client computers.</span></span>

5.  <span data-ttu-id="0408d-117">Convertire i punti di estensione, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="0408d-117">Convert extension points, as needed.</span></span> <span data-ttu-id="0408d-118">Per altre informazioni, vedi le risorse seguenti:</span><span class="sxs-lookup"><span data-stu-id="0408d-118">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="0408d-119">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.1 convertito per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="0408d-119">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.1 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="0408d-120">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.1 per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="0408d-120">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.1 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [<span data-ttu-id="0408d-121">Come convertire un pacchetto creato in una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="0408d-121">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  <span data-ttu-id="0408d-122">Verificare che i pacchetti dell'App-V 5,1 abbiano esito positivo e quindi rimuovere i pacchetti 4,6.</span><span class="sxs-lookup"><span data-stu-id="0408d-122">Test that your App-V 5.1 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="0408d-123">Per controllare lo stato dell'utente dei computer client, è consigliabile usare la [virtualizzazione dell'esperienza utente](https://technet.microsoft.com/library/dn458947.aspx) o un altro strumento di gestione dell'ambiente utente.</span><span class="sxs-lookup"><span data-stu-id="0408d-123">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="0408d-124">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="0408d-124">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="0408d-125">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="0408d-125">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="0408d-126">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="0408d-126">Got an App-V issue?</span></span>** <span data-ttu-id="0408d-127">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="0408d-127">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="0408d-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0408d-128">Related topics</span></span>


[<span data-ttu-id="0408d-129">Pianificazione per la migrazione da una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="0408d-129">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[<span data-ttu-id="0408d-130">Distribuzione di App-V 5.1 Sequencer e del client</span><span class="sxs-lookup"><span data-stu-id="0408d-130">Deploying the App-V 5.1 Sequencer and Client</span></span>](deploying-the-app-v-51-sequencer-and-client.md)

 

 





