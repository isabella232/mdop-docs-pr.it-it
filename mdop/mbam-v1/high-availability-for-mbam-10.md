---
title: Disponibilità elevata per MBAM 1.0
description: Disponibilità elevata per MBAM 1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825365"
---
# <span data-ttu-id="5e6e8-103">Disponibilità elevata per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5e6e8-103">High Availability for MBAM 1.0</span></span>


<span data-ttu-id="5e6e8-104">Questo argomento descrive come configurare un'installazione a elevata disponibilità di Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="5e6e8-104">This topic describes how to configure a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

## <span data-ttu-id="5e6e8-105">Scenari di disponibilità elevata per MBAM</span><span class="sxs-lookup"><span data-stu-id="5e6e8-105">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="5e6e8-106">L'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) sono progettati per essere a tolleranza d'errore.</span><span class="sxs-lookup"><span data-stu-id="5e6e8-106">Microsoft BitLocker Administration and Monitoring (MBAM) is designed to be fault-tolerant.</span></span> <span data-ttu-id="5e6e8-107">Se un server diventa non disponibile, gli utenti non devono essere colpiti negativamente.</span><span class="sxs-lookup"><span data-stu-id="5e6e8-107">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="5e6e8-108">Ad esempio, se l'agente MBAM non riesce a connettersi al server Web MBAM, gli utenti non devono essere richieste di azione.</span><span class="sxs-lookup"><span data-stu-id="5e6e8-108">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="5e6e8-109">Quando si pianifica l'installazione di MBAM, prendere in considerazione i seguenti problemi che possono influenzare la disponibilità del servizio MBAM:</span><span class="sxs-lookup"><span data-stu-id="5e6e8-109">When you plan your MBAM installation, consider the following concerns that can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="5e6e8-110">Crittografia unità e password di ripristino: se non è possibile escrowE una password di ripristino, la crittografia non viene avviata nel computer client.</span><span class="sxs-lookup"><span data-stu-id="5e6e8-110">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption will not start on the client computer.</span></span>

-   <span data-ttu-id="5e6e8-111">Caricamento dei dati sullo stato di conformità: se il server che ospita il servizio report stato conformità non è disponibile, i dati di conformità non rimarranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="5e6e8-111">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data will not remain current.</span></span>

-   <span data-ttu-id="5e6e8-112">Help desk Recovery Key Access-se l'help desk non può accedere alle informazioni sul database MBAM, non sarà in grado di fornire chiavi di ripristino agli utenti.</span><span class="sxs-lookup"><span data-stu-id="5e6e8-112">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, they will be unable to provide recovery keys to users.</span></span>

-   <span data-ttu-id="5e6e8-113">Disponibilità dei report: i report non saranno disponibili se il server che ospita i report di conformità e controllo non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="5e6e8-113">Availability of reports – Reports will not be available if the server that hosts the Compliance and Audit Reports is not available.</span></span>

<span data-ttu-id="5e6e8-114">La principale preoccupazione per MBAM High Availability è la disponibilità del ripristino della chiave BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5e6e8-114">The main concern for MBAM high availability is BitLocker key recovery availability.</span></span> <span data-ttu-id="5e6e8-115">Se il supporto tecnico non è in grado di fornire chiavi di ripristino, gli utenti bloccati non riescono a sbloccare i computer.</span><span class="sxs-lookup"><span data-stu-id="5e6e8-115">If the help desk cannot provide recovery keys, users who are locked out cannot unlock their computers.</span></span> <span data-ttu-id="5e6e8-116">Per evitare questo problema, è consigliabile implementare server Web ridondanti e database per garantire un'elevata disponibilità.</span><span class="sxs-lookup"><span data-stu-id="5e6e8-116">To avoid this problem, consider implementing redundant web servers and databases to ensure high availability.</span></span>

<span data-ttu-id="5e6e8-117">Per altre informazioni sulla scalabilità e l'elevata disponibilità di MBAM, vedi la [scalabilità di mbam white paper](https://go.microsoft.com/fwlink/p/?LinkId=229025) ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .</span><span class="sxs-lookup"><span data-stu-id="5e6e8-117">For more information about MBAM scalability and high availability, see the [MBAM Scalability White Paper](https://go.microsoft.com/fwlink/p/?LinkId=229025) (https://go.microsoft.com/fwlink/p/?LinkId=229025).</span></span>

<span data-ttu-id="5e6e8-118">Per informazioni generali sull'elevata disponibilità per Microsoft SQL Server, vedere [disponibilità elevata](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .</span><span class="sxs-lookup"><span data-stu-id="5e6e8-118">For general guidance on high availability for Microsoft SQL Server, see [High Availability](https://go.microsoft.com/fwlink/p/?LinkId=221504) (https://go.microsoft.com/fwlink/p/?LinkId=221504).</span></span>

<span data-ttu-id="5e6e8-119">Per indicazioni generali sulla disponibilità e scalabilità per i server Web, vedere [disponibilità e scalabilità](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .</span><span class="sxs-lookup"><span data-stu-id="5e6e8-119">For general guidance on availability and scalability for web servers, see [Availability and Scalability](https://go.microsoft.com/fwlink/p/?LinkId=221503) (https://go.microsoft.com/fwlink/p/?LinkId=221503).</span></span>

## <span data-ttu-id="5e6e8-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5e6e8-120">Related topics</span></span>


[<span data-ttu-id="5e6e8-121">Manutenzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5e6e8-121">Maintaining MBAM 1.0</span></span>](maintaining-mbam-10.md)

 

 





