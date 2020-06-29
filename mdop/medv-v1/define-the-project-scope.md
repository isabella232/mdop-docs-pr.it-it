---
title: Definire l'ambito di progetto
description: Definire l'ambito di progetto
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823645"
---
# <span data-ttu-id="717a6-103">Definire l'ambito di progetto</span><span class="sxs-lookup"><span data-stu-id="717a6-103">Define the Project Scope</span></span>


<span data-ttu-id="717a6-104">Quando si definisce l'ambito del progetto, determinare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="717a6-104">When defining the project scope, determine the following:</span></span>

1.  <span data-ttu-id="717a6-105">Utenti finali di MED-V: la posizione e il numero di utenti finali vengono usati per determinare la posizione delle installazioni client MED-V e il numero di istanze di MED-V, nonché il numero e la posizione dei repository di immagini MED-V.</span><span class="sxs-lookup"><span data-stu-id="717a6-105">The MED-V end users—the location and number of end users are used in determining the location of MED-V client installations and the number of MED-V instances, as well as the number and placement of MED-V image repositories.</span></span>

2.  <span data-ttu-id="717a6-106">Le immagini della macchina virtuale (VM) che devono essere gestite da MED-V per determinare il metodo di distribuzione delle immagini e la posizione dei repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="717a6-106">The virtual machine (VM) images to be managed by MED-V—to determine the method of distributing images and placement of image repositories.</span></span>

3.  <span data-ttu-id="717a6-107">Le aspettative del livello di servizio dell'organizzazione, per determinare i requisiti di prestazioni e tolleranza d'errore per il server e il database MED-V, nonché per il repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="717a6-107">The organization’s service level expectations—to determine the performance and fault-tolerance requirements for the MED-V server and database as well as the image repository.</span></span>

4.  <span data-ttu-id="717a6-108">Convalidare con l'azienda: verificare che l'infrastruttura pianificata influenzi l'azienda in modo completo.</span><span class="sxs-lookup"><span data-stu-id="717a6-108">Validate with the business—ensure there is a complete understanding of how the planned infrastructure affects the business.</span></span>

## <span data-ttu-id="717a6-109">Definire gli utenti finali di MED-V</span><span class="sxs-lookup"><span data-stu-id="717a6-109">Define the MED-V End Users</span></span>


<span data-ttu-id="717a6-110">Prima di tutto, determinare dove si trovano gli utenti finali, nonché il numero di utenti in ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="717a6-110">First, determine where the end users are located, as well as the number of users in each location.</span></span> <span data-ttu-id="717a6-111">In secondo luogo, ottenere un diagramma di infrastruttura di rete che visualizza le posizioni utente e la larghezza di banda disponibile per tali posizioni.</span><span class="sxs-lookup"><span data-stu-id="717a6-111">Second, obtain a network infrastructure diagram that displays the user locations and the available bandwidth to those locations.</span></span> <span data-ttu-id="717a6-112">In terzo luogo, scoprire se gli utenti viaggiano tra le posizioni.</span><span class="sxs-lookup"><span data-stu-id="717a6-112">Third, find out if users travel between locations.</span></span> <span data-ttu-id="717a6-113">Se gli utenti viaggiano, potrebbero essere necessarie ulteriori capacità nella progettazione dell'infrastruttura server e dei repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="717a6-113">If users travel, additional capacity may be required in the design of the server infrastructure and image repositories.</span></span>

## <span data-ttu-id="717a6-114">Determinare le immagini MED-V da gestire con MED-V</span><span class="sxs-lookup"><span data-stu-id="717a6-114">Determine the MED-V Images to Be Managed by MED-V</span></span>


<span data-ttu-id="717a6-115">Dopo avere definito gli utenti finali di MED-V, determinare quali VM verranno gestite da MED-V per gli utenti in ogni posizione.</span><span class="sxs-lookup"><span data-stu-id="717a6-115">After the MED-V end users have been defined, determine which VMs will be managed by MED-V for the users in each location.</span></span>

<span data-ttu-id="717a6-116">Se una delle macchine virtuali è archiviata in una raccolta centralizzata, determinare la posizione della raccolta in modo che possa essere valutata per l'uso come repository MED-V.</span><span class="sxs-lookup"><span data-stu-id="717a6-116">If any of the VMs are stored in a centralized library, determine the location of the library so that it may be evaluated for use as a MED-V repository.</span></span>

## <a href="" id="determine-the-organization-s-service-level-expectations"></a><span data-ttu-id="717a6-117">Determinare le aspettative del livello di servizio dell'organizzazione</span><span class="sxs-lookup"><span data-stu-id="717a6-117">Determine the Organization’s Service Level Expectations</span></span>


<span data-ttu-id="717a6-118">Per ogni area di lavoro MED-V, nota il periodo di tempo accettabile per il caricamento di una nuova immagine e per la distribuzione dei tempi per gli aggiornamenti critici.</span><span class="sxs-lookup"><span data-stu-id="717a6-118">For each MED-V workspace, note the acceptable time for a new image to load and the timeframe for critical updates to be deployed.</span></span>

<span data-ttu-id="717a6-119">Se applicabile, registrare le aspettative del livello di servizio per i report MED-V, da usare nella progettazione dell'infrastruttura server.</span><span class="sxs-lookup"><span data-stu-id="717a6-119">If applicable, record the service level expectations for MED-V reporting, to be used in the design of the server infrastructure.</span></span>

## <span data-ttu-id="717a6-120">Convalidare con il business</span><span class="sxs-lookup"><span data-stu-id="717a6-120">Validate with the Business</span></span>


<span data-ttu-id="717a6-121">Chiedere agli stakeholder aziendali e ai proprietari delle applicazioni le seguenti domande:</span><span class="sxs-lookup"><span data-stu-id="717a6-121">Ask business stakeholders and application owners the following questions:</span></span>

-   <span data-ttu-id="717a6-122">Esistono immagini esistenti che possono essere combinate?</span><span class="sxs-lookup"><span data-stu-id="717a6-122">Are there any existing images that can be combined?</span></span> <span data-ttu-id="717a6-123">Ad esempio, se l'applicazione A su WindowsXP è un'immagine VPC e l'applicazione B su WindowsXP è un'altra immagine VPC, forse una singola immagine può contenere entrambe le applicazioni, riducendo così lo spazio del repository e la larghezza di banda necessaria per il download delle immagini.</span><span class="sxs-lookup"><span data-stu-id="717a6-123">For example, if application A on WindowsXP is one VPC image and application B on WindowsXP is another VPC image, perhaps a single image can contain both applications, thereby reducing repository space and bandwidth required for image download.</span></span>

-   <span data-ttu-id="717a6-124">Le applicazioni in ambito licenziabili e supportate possono essere distribuite in una VM da MED-V?</span><span class="sxs-lookup"><span data-stu-id="717a6-124">Are the in-scope applications licensable and supportable if delivered in a VM by MED-V?</span></span> <span data-ttu-id="717a6-125">Verificare che il fornitore dell'applicazione assicuri che le condizioni di licenza e supporto tecnico non vengano violate consegnando l'applicazione tramite MED-V.</span><span class="sxs-lookup"><span data-stu-id="717a6-125">Check with the application supplier to ensure that licensing and support terms will not be violated by delivering the application through MED-V.</span></span>

 

 





