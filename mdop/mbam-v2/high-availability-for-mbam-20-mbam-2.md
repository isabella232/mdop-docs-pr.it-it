---
title: Disponibilità elevata per MBAM 2.0
description: Disponibilità elevata per MBAM 2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824726"
---
# <span data-ttu-id="9fa0b-103">Disponibilità elevata per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9fa0b-103">High Availability for MBAM 2.0</span></span>


<span data-ttu-id="9fa0b-104">Questo argomento fornisce informazioni di base su un'installazione a elevata disponibilità di Microsoft BitLocker Administration and Monitoring (MBAM).</span><span class="sxs-lookup"><span data-stu-id="9fa0b-104">This topic provides basic information about a highly available installation of Microsoft BitLocker Administration and Monitoring (MBAM).</span></span> <span data-ttu-id="9fa0b-105">Gli scenari di disponibilità elevata non sono completamente supportati in questa versione di MBAM, quindi non sono descritti qui.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-105">High-availability scenarios are not fully supported in this version of MBAM, so they are not described here.</span></span> <span data-ttu-id="9fa0b-106">Si consiglia di cercare i Blog e i forum correlati, in cui gli utenti descrivono come hanno configurato correttamente l'elevata disponibilità per MBAM nei loro ambienti.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-106">It is recommended that you search related blogs and forums, where users describe how they have successfully configured high availability for MBAM in their environments.</span></span>

## <span data-ttu-id="9fa0b-107">Scenari di disponibilità elevata per MBAM</span><span class="sxs-lookup"><span data-stu-id="9fa0b-107">High Availability Scenarios for MBAM</span></span>


<span data-ttu-id="9fa0b-108">L'amministrazione e il monitoraggio di Microsoft BitLocker sono progettati per essere a tolleranza d'errore.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-108">Microsoft BitLocker Administration and Monitoring is designed to be fault-tolerant.</span></span> <span data-ttu-id="9fa0b-109">Se un server diventa non disponibile, gli utenti non devono essere interessati negativamente.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-109">If a server becomes unavailable, users should not be negatively affected.</span></span> <span data-ttu-id="9fa0b-110">Ad esempio, se l'agente MBAM non riesce a connettersi al server Web MBAM, gli utenti non devono essere richieste di azione.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-110">For example, if the MBAM agent cannot connect to the MBAM web server, users should not be prompted for action.</span></span>

<span data-ttu-id="9fa0b-111">Quando si pianifica l'installazione di MBAM, prendere in considerazione gli elementi seguenti, che possono influire sulla disponibilità del servizio MBAM:</span><span class="sxs-lookup"><span data-stu-id="9fa0b-111">When you plan your MBAM installation, consider the following items, which can affect the availability of the MBAM service:</span></span>

-   <span data-ttu-id="9fa0b-112">Crittografia unità e password di ripristino: se non è possibile escrowE una password di ripristino, la crittografia non viene avviata nel computer client.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-112">Drive encryption and recovery password – If a recovery password cannot be escrowed, the encryption does not start on the client computer.</span></span>

-   <span data-ttu-id="9fa0b-113">Caricamento dei dati sullo stato di conformità: se il server che ospita il servizio report stato conformità non è disponibile, i dati di conformità non rimangono aggiornati.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-113">Compliance status data upload – If the server that hosts the compliance status report service is not available, the compliance data does not remain current.</span></span>

-   <span data-ttu-id="9fa0b-114">Help desk Recovery Key Access-se il supporto tecnico non è in grado di accedere alle informazioni sul database MBAM, il supporto tecnico non può fornire chiavi di ripristino agli utenti.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-114">Help Desk recovery key access - If the Help Desk cannot access MBAM database information, the Help Desk cannot provide recovery keys to users.</span></span>

-   <span data-ttu-id="9fa0b-115">Disponibilità dei report: se il server che ospita i report di conformità e controllo non è disponibile, i report non saranno disponibili.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-115">Availability of reports –If the server that hosts the Compliance and Audit Reports is not available, reports will not be available.</span></span>

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a><span data-ttu-id="9fa0b-116">In che modo il backup di MBAM usa il servizio Copia Shadow del volume (VSS)</span><span class="sxs-lookup"><span data-stu-id="9fa0b-116">How the MBAM Backup Uses the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="9fa0b-117">MBAM 2.0 offre un writer del servizio Copia Shadow del volume (VSS), denominato Microsoft BitLocker Administration and Management writer, che facilita il backup del database di conformità e audit e del database di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-117">MBAM2.0 provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer, which facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="9fa0b-118">Il server di Windows Installer di MBAM registra MBAM VSS writer.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-118">The MBAM Server Windows Installer registers the MBAM VSS Writer.</span></span> <span data-ttu-id="9fa0b-119">Qualsiasi errore durante la registrazione di VSS Writer fa sì che l'installazione di MBAM server venga ritirata.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-119">Any failure during the VSS writer registration causes the MBAM Server installation to roll back.</span></span> <span data-ttu-id="9fa0b-120">In una topologia in cui il database di conformità e controllo e il database di ripristino sono installati in server diversi, è registrata un'istanza distinta di MBAM VSS Writer in ogni server.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-120">In a topology where the Compliance and Audit Database and the Recovery Database are installed on different servers, a separate instance of MBAM VSS Writer is registered on each server.</span></span> <span data-ttu-id="9fa0b-121">MBAM VSS Writer dipende da SQL Server VSS writer.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-121">The MBAM VSS Writer is dependent on the SQL Server VSS Writer.</span></span> <span data-ttu-id="9fa0b-122">SQL Server VSS writer viene registrato come parte dell'installazione di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-122">The SQL Server VSS Writer is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="9fa0b-123">Qualsiasi tecnologia di backup che usa writer VSS per eseguire il backup può individuare il writer di MBAM VSS.</span><span class="sxs-lookup"><span data-stu-id="9fa0b-123">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS Writer.</span></span>

## <span data-ttu-id="9fa0b-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9fa0b-124">Related topics</span></span>


[<span data-ttu-id="9fa0b-125">Manutenzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="9fa0b-125">Maintaining MBAM 2.0</span></span>](maintaining-mbam-20-mbam-2.md)

 

 





