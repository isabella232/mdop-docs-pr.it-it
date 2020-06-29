---
title: Come distribuire l'App-V 4,6 e il client App-V 5,0 nello stesso computer
description: Come distribuire l'App-V 4,6 e il client App-V 5,0 nello stesso computer
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805535"
---
# <span data-ttu-id="138f2-103">Come distribuire l'App-V 4,6 e il client App-V 5,0 nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="138f2-103">How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer</span></span>

<span data-ttu-id="138f2-104">**Nota:** App-V 4,6 è uscito dal supporto mainstream.</span><span class="sxs-lookup"><span data-stu-id="138f2-104">**Note:** App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="138f2-105">Il seguente presuppone che il client App-V 4,6 SP3 sia già installato.</span><span class="sxs-lookup"><span data-stu-id="138f2-105">The following assumes that the App-V 4.6 SP3 client is already installed.</span></span>

<span data-ttu-id="138f2-106">Usare le informazioni seguenti per installare il client App-V 5,0 (preferibilmente con i Service Pack più recenti e gli hotfix) e il client App-V 4.6 SP3 nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="138f2-106">Use the following information to install the App-V 5.0 client (preferably, with the latest Service Packs and hotfixes) and the App-V 4.6SP3 client on the same computer.</span></span> <span data-ttu-id="138f2-107">Per le versioni supportate, i requisiti e altre informazioni sulla pianificazione, vedere [pianificazione della migrazione da una versione precedente di App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span><span class="sxs-lookup"><span data-stu-id="138f2-107">For supported versions, requirements, and other planning information, see [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).</span></span>

**<span data-ttu-id="138f2-108">Per distribuire client App-V 5,0 e client App-V 4,6 nello stesso computer</span><span class="sxs-lookup"><span data-stu-id="138f2-108">To deploy the App-V 5.0 client and App-V 4.6 client on the same computer</span></span>**

1.  <span data-ttu-id="138f2-109">Installare il client App-V 5,0 SP3 nel computer in cui è in esecuzione la versione App-V 4,6 del client.</span><span class="sxs-lookup"><span data-stu-id="138f2-109">Install the App-V 5.0 SP3 client on the computer that is running the App-V 4.6 version of the client.</span></span> <span data-ttu-id="138f2-110">Per ottenere risultati ottimali, è consigliabile installare tutti gli aggiornamenti disponibili per il client App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="138f2-110">For best results, we recommend that you install all available updates to the App-V 5.0 SP3 client.</span></span>

2.  <span data-ttu-id="138f2-111">Convertire o rieseguire la sequenza graduale dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="138f2-111">Convert or re-sequence the packages gradually.</span></span>

    -   <span data-ttu-id="138f2-112">Per convertire i pacchetti, usa il convertitore di pacchetti App-V 5,0 e Converti i pacchetti necessari nel formato di file App-V 5,0 (**. AppV**).</span><span class="sxs-lookup"><span data-stu-id="138f2-112">To convert the packages, use the App-V 5.0 package converter and convert the required packages to the App-V 5.0 (**.appv**) file format.</span></span>

    -   <span data-ttu-id="138f2-113">Per risequenziare i pacchetti, è consigliabile usare la versione più recente del sequencer per ottenere risultati ottimali.</span><span class="sxs-lookup"><span data-stu-id="138f2-113">To re-sequence the packages, consider using the latest version of the Sequencer for best results.</span></span>

    <span data-ttu-id="138f2-114">Per altre informazioni sulla pubblicazione di pacchetti, vedere [come pubblicare un pacchetto tramite la console di gestione](how-to-publish-a-package-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="138f2-114">For more information about publishing packages, see [How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md).</span></span>

3.  <span data-ttu-id="138f2-115">Distribuire pacchetti ai computer client.</span><span class="sxs-lookup"><span data-stu-id="138f2-115">Deploy packages to the client computers.</span></span>

4.  <span data-ttu-id="138f2-116">Convertire i punti di estensione, in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="138f2-116">Convert extension points, as needed.</span></span> <span data-ttu-id="138f2-117">Per altre informazioni, vedi le risorse seguenti:</span><span class="sxs-lookup"><span data-stu-id="138f2-117">For more information, see the following resources:</span></span>

    -   [<span data-ttu-id="138f2-118">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 a un pacchetto App-V 5.0 convertito per tutti gli utenti in un computer specifico</span><span class="sxs-lookup"><span data-stu-id="138f2-118">How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [<span data-ttu-id="138f2-119">Come eseguire la migrazione dei punti di estensione da un pacchetto App-V 4.6 ad App-V 5.0 per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="138f2-119">How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User</span></span>](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [<span data-ttu-id="138f2-120">Come convertire un pacchetto creato in una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="138f2-120">How to Convert a Package Created in a Previous Version of App-V</span></span>](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  <span data-ttu-id="138f2-121">Verificare che i pacchetti dell'App-V 5,0 abbiano esito positivo e quindi rimuovere i pacchetti 4,6.</span><span class="sxs-lookup"><span data-stu-id="138f2-121">Test that your App-V 5.0 packages are successful, and then remove the 4.6 packages.</span></span> <span data-ttu-id="138f2-122">Per controllare lo stato dell'utente dei computer client, è consigliabile usare la [virtualizzazione dell'esperienza utente](https://technet.microsoft.com/library/dn458947.aspx) o un altro strumento di gestione dell'ambiente utente.</span><span class="sxs-lookup"><span data-stu-id="138f2-122">To check the user state of your client computers, we recommend that you use [User Experience Virtualization](https://technet.microsoft.com/library/dn458947.aspx) or another user environment management tool.</span></span>

    <span data-ttu-id="138f2-123">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="138f2-123">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="138f2-124">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="138f2-124">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="138f2-125">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="138f2-125">Got an App-V issue?</span></span>** <span data-ttu-id="138f2-126">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="138f2-126">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="138f2-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="138f2-127">Related topics</span></span>


[<span data-ttu-id="138f2-128">Pianificazione per la migrazione da una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="138f2-128">Planning for Migrating from a Previous Version of App-V</span></span>](planning-for-migrating-from-a-previous-version-of-app-v.md)

[<span data-ttu-id="138f2-129">Distribuzione di App-V 5.0 Sequencer e del client</span><span class="sxs-lookup"><span data-stu-id="138f2-129">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

 

 





