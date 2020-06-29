---
title: Pianificazione dei ruoli di amministrazione di MBAM 2.0
description: Pianificazione dei ruoli di amministrazione di MBAM 2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824895"
---
# <span data-ttu-id="8125e-103">Pianificazione dei ruoli di amministrazione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8125e-103">Planning for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="8125e-104">Questo argomento elenca e descrive i ruoli di amministratore disponibili disponibili in Microsoft BitLocker Administration and Monitoring (MBAM), nonché i percorsi del server in cui vengono creati i gruppi locali.</span><span class="sxs-lookup"><span data-stu-id="8125e-104">This topic lists and describes the available administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM) as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="8125e-105">Ruoli di amministratore di MBAM</span><span class="sxs-lookup"><span data-stu-id="8125e-105">MBAM Administrator Roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="8125e-106">Amministratori di sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="8125e-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="8125e-107">Gli amministratori di questo ruolo hanno accesso a tutte le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8125e-107">Administrators in this role have access to all Microsoft BitLocker Administration and Monitoring features.</span></span> <span data-ttu-id="8125e-108">Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="8125e-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="8125e-109">Utenti di MBAM helpdesk</span><span class="sxs-lookup"><span data-stu-id="8125e-109">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="8125e-110">Gli amministratori di questo ruolo hanno accesso alle funzionalità dell'help desk di MBAM.</span><span class="sxs-lookup"><span data-stu-id="8125e-110">Administrators in this role have access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="8125e-111">Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="8125e-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-report-users"></a> **<span data-ttu-id="8125e-112">Utenti di report MBAM</span><span class="sxs-lookup"><span data-stu-id="8125e-112">MBAM Report Users</span></span>**  
<span data-ttu-id="8125e-113">Gli amministratori di questo ruolo hanno accesso ai report di conformità e controllo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="8125e-113">Administrators in this role have access to the Compliance and Audit Reports from MBAM.</span></span> <span data-ttu-id="8125e-114">Il gruppo locale per questo ruolo è installato nel database di amministrazione e monitoraggio Server, conformità e controllo e nel server che ospita i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="8125e-114">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **<span data-ttu-id="8125e-115">MBAM Advanced helpdesk utenti</span><span class="sxs-lookup"><span data-stu-id="8125e-115">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="8125e-116">Gli amministratori in questo ruolo hanno aumentato l'accesso alle funzionalità dell'help desk di MBAM.</span><span class="sxs-lookup"><span data-stu-id="8125e-116">Administrators in this role have increased access to the Help Desk features from MBAM.</span></span> <span data-ttu-id="8125e-117">Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="8125e-117">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="8125e-118">Se un utente è un membro di entrambi gli utenti di MBAM helpdesk e MBAM Advanced helpdesk utenti, le autorizzazioni di MBAM Advanced helpdesk utenti eseguiranno l'override delle autorizzazioni utente di MBAM helpdesk.</span><span class="sxs-lookup"><span data-stu-id="8125e-118">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will override the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="8125e-119">**Importante**  Per visualizzare i report, un utente di amministrazione deve essere un membro del gruppo di sicurezza degli **utenti del report mbam** nel database di amministrazione e monitoraggio Server, conformità e controllo e nel server che ospita la funzionalità report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="8125e-119">**Important** To view reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports feature.</span></span> <span data-ttu-id="8125e-120">Come procedura consigliata, creare un gruppo di sicurezza in servizi di dominio Active Directory con diritti sul gruppo di sicurezza Local **report degli utenti di mbam** nel server di amministrazione e monitoraggio e nel server che ospita i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="8125e-120">As a best practice, create a security group in Active Directory Domain Services with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and the server that hosts the Compliance and Audit Reports.</span></span>

 

## <span data-ttu-id="8125e-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8125e-121">Related topics</span></span>


[<span data-ttu-id="8125e-122">Preparazione dell'ambiente per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="8125e-122">Preparing your Environment for MBAM 2.0</span></span>](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





