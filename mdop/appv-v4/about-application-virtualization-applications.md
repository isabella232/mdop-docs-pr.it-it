---
title: Informazioni sulle applicazioni di Application Virtualization
description: Informazioni sulle applicazioni di Application Virtualization
author: dansimp
ms.assetid: 3bf833b7-d172-4eef-a9e8-4b4f0c7eb15b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4eeea7a0ec4454aefcdde5196ae15ed029da45b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820086"
---
# <span data-ttu-id="4a8d6-103">Informazioni sulle applicazioni di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="4a8d6-103">About Application Virtualization Applications</span></span>


<span data-ttu-id="4a8d6-104">Nella virtualizzazione delle applicazioni un' *applicazione* è un programma eseguibile, ad esempio Microsoft Visio, che viene trasmesso al client Desktop Application Virtualization o al client per Servizi Desktop remoto (in precedenza Servizi terminal) da un Application Virtualization Management Server.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-104">In Application Virtualization, an *application* is an executable program, such as Microsoft Visio, that is streamed to the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) from an Application Virtualization Management Server.</span></span> <span data-ttu-id="4a8d6-105">Prima di poter eseguire il flusso di un'applicazione a un client, l'applicazione deve essere preparata per il flusso tramite l'elaborazione con Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-105">Before an application can be streamed to a client, the application must be prepared for streaming by processing it with the Application Virtualization Sequencer.</span></span>

## <span data-ttu-id="4a8d6-106">Gestione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="4a8d6-106">Managing Applications</span></span>


<span data-ttu-id="4a8d6-107">È necessario aggiungere applicazioni al sistema prima di rendere le applicazioni disponibili per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-107">You must add applications to the system before you can make the applications available to users.</span></span> <span data-ttu-id="4a8d6-108">Il metodo più comune per l'aggiunta di applicazioni al sistema consiste nell'importarli.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-108">The most common method for adding applications to the system is to import them.</span></span> <span data-ttu-id="4a8d6-109">Per accedere a questa caratteristica, fare clic con il pulsante destro del mouse sul nodo **applicazioni** nella console di gestione di Application Virtualization Server e scegliere **Importa applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-109">To access this feature, right-click the **Applications** node in the Application Virtualization Server Management Console and choose **Import Applications**.</span></span>

<span data-ttu-id="4a8d6-110">È possibile importare contemporaneamente più file OSD (Open Software Descriptor) oppure importare un file di progetto sequencer (SPRJ) che può contenere più file OSD.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-110">You can import more than one Open Software Descriptor (OSD) file at the same time, or you can import a Sequencer Project file (SPRJ) that can contain multiple OSD files.</span></span> <span data-ttu-id="4a8d6-111">Questa funzionalità consente di configurare le applicazioni correlate in modo simile.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-111">This functionality enables you to configure related applications similarly.</span></span>

<span data-ttu-id="4a8d6-112">È anche possibile usare le caratteristiche seguenti per gestire le applicazioni:</span><span class="sxs-lookup"><span data-stu-id="4a8d6-112">You can also use the following features to help you manage your applications:</span></span>

-   <span data-ttu-id="4a8d6-113">**Gruppi**di applicazioni: consente di creare gruppi logici di applicazioni per la gestione semplificata.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-113">**Application Groups**—Enables you to create logical groups of applications for simplified management.</span></span> <span data-ttu-id="4a8d6-114">Quando si apportano modifiche a un gruppo (ad esempio le autorizzazioni di accesso), le modifiche vengono applicate a tutte le applicazioni del gruppo.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-114">When changes are made to a group (for example, access permissions), the changes are applied to all applications in the group.</span></span> <span data-ttu-id="4a8d6-115">Le applicazioni di un gruppo possono provenire da pacchetti diversi.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-115">Applications in a group can come from different packages.</span></span>

-   <span data-ttu-id="4a8d6-116">**Selezione multipla**: consente di selezionare più applicazioni contemporaneamente tenendo premuto il tasto CTRL quando si fa clic su un'applicazione per modificare le proprietà dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-116">**Multi Select**—Enables you to select multiple applications at once by holding the CTRL key when you click an application to modify the application properties.</span></span> <span data-ttu-id="4a8d6-117">Tuttavia, se si vuole mantenere una relazione tra le applicazioni, è necessario creare un gruppo di applicazioni per contenere le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-117">However, if you want to maintain a relationship between the applications, you should create an application group to hold the applications.</span></span>

-   <span data-ttu-id="4a8d6-118">**Copia Cross System**: consente di copiare le applicazioni da un ambiente a un altro ambiente in cui è in esecuzione la stessa versione di App-V in un unico passaggio.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-118">**Cross System Copy**—Enables you to copy applications from one environment to another environment that is running the same version of App-V in one step.</span></span> <span data-ttu-id="4a8d6-119">Ad esempio, potresti avere un ambiente di test di accettazione degli utenti in cui devi inizialmente distribuire e configurare le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-119">For example, you might have a user acceptance test environment where you initially deploy and configure applications.</span></span> <span data-ttu-id="4a8d6-120">Dopo aver terminato la fase di test, è consigliabile replicare lo stesso set di applicazioni (incluse le autorizzazioni) nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="4a8d6-120">After you finish your testing phase, you might want to replicate the same set of applications (including permissions) to the production environment.</span></span>

## <span data-ttu-id="4a8d6-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a8d6-121">Related topics</span></span>


[<span data-ttu-id="4a8d6-122">Informazioni sui pacchetti di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="4a8d6-122">About Application Virtualization Packages</span></span>](about-application-virtualization-packages.md)

[<span data-ttu-id="4a8d6-123">Informazioni su Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="4a8d6-123">About the Application Virtualization Server Management Console</span></span>](about-the-application-virtualization-server-management-console.md)

[<span data-ttu-id="4a8d6-124">Come gestire i gruppi di applicazioni in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="4a8d6-124">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="4a8d6-125">Come gestire le applicazioni in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="4a8d6-125">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





