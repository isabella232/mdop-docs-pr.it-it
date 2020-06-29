---
title: Pianificazione dei ruoli di amministrazione di MBAM 1.0
description: Pianificazione dei ruoli di amministrazione di MBAM 1.0
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825886"
---
# <span data-ttu-id="96ef4-103">Pianificazione dei ruoli di amministrazione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="96ef4-103">Planning for MBAM 1.0 Administrator Roles</span></span>


<span data-ttu-id="96ef4-104">Questo argomento include e descrive i ruoli di amministratore disponibili in Microsoft BitLocker Administration and Monitoring (MBAM), nonché i percorsi del server in cui vengono creati i gruppi locali.</span><span class="sxs-lookup"><span data-stu-id="96ef4-104">This topic includes and describes the administrator roles that are available in Microsoft BitLocker Administration and Monitoring (MBAM), as well as the server locations where the local groups are created.</span></span>

## <span data-ttu-id="96ef4-105">Ruoli di amministratore di MBAM</span><span class="sxs-lookup"><span data-stu-id="96ef4-105">MBAM Administrator roles</span></span>


<a href="" id="---------------mbam-system-administrators"></a> **<span data-ttu-id="96ef4-106">Amministratori di sistema MBAM</span><span class="sxs-lookup"><span data-stu-id="96ef4-106">MBAM System Administrators</span></span>**  
<span data-ttu-id="96ef4-107">Gli amministratori di questo ruolo hanno accesso a tutte le caratteristiche di MBAM.</span><span class="sxs-lookup"><span data-stu-id="96ef4-107">Administrators in this role have access to all MBAM features.</span></span> <span data-ttu-id="96ef4-108">Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="96ef4-108">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-hardware-users"></a> **<span data-ttu-id="96ef4-109">Utenti di hardware MBAM</span><span class="sxs-lookup"><span data-stu-id="96ef4-109">MBAM Hardware Users</span></span>**  
<span data-ttu-id="96ef4-110">Gli amministratori di questo ruolo hanno accesso alle funzionalità di funzionalità hardware di MBAM.</span><span class="sxs-lookup"><span data-stu-id="96ef4-110">Administrators in this role have access to the Hardware Capability features from MBAM.</span></span> <span data-ttu-id="96ef4-111">Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="96ef4-111">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam-helpdesk-users"></a> **<span data-ttu-id="96ef4-112">Utenti di MBAM helpdesk</span><span class="sxs-lookup"><span data-stu-id="96ef4-112">MBAM Helpdesk Users</span></span>**  
<span data-ttu-id="96ef4-113">Gli amministratori di questo ruolo hanno accesso alle funzionalità dell'helpdesk da MBAM.</span><span class="sxs-lookup"><span data-stu-id="96ef4-113">Administrators in this role have access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="96ef4-114">Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="96ef4-114">The local group for this role is installed on the Administration and Monitoring Server.</span></span>

<a href="" id="---------------mbam--report-users"></a> **<span data-ttu-id="96ef4-115">Utenti di report MBAM</span><span class="sxs-lookup"><span data-stu-id="96ef4-115">MBAM Report Users</span></span>**  
<span data-ttu-id="96ef4-116">Gli amministratori di questo ruolo hanno accesso alla caratteristica conformità e rapporti di controllo da MBAM.</span><span class="sxs-lookup"><span data-stu-id="96ef4-116">Administrators in this role have access to the Compliance and Audit Reports feature from MBAM.</span></span> <span data-ttu-id="96ef4-117">Il gruppo locale per questo ruolo è installato nel database di amministrazione e monitoraggio Server, conformità e controllo e nel server che ospita i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="96ef4-117">The local group for this role is installed on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Audit Reports.</span></span>

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **<span data-ttu-id="96ef4-118">MBAM Advanced helpdesk utenti</span><span class="sxs-lookup"><span data-stu-id="96ef4-118">MBAM Advanced Helpdesk Users</span></span>**  
<span data-ttu-id="96ef4-119">Gli amministratori di questo ruolo hanno aumentato l'accesso alle funzionalità dell'helpdesk da MBAM.</span><span class="sxs-lookup"><span data-stu-id="96ef4-119">Administrators in this role have increased access to the Helpdesk features from MBAM.</span></span> <span data-ttu-id="96ef4-120">Il gruppo locale per questo ruolo è installato nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="96ef4-120">The local group for this role is installed on the Administration and Monitoring Server.</span></span> <span data-ttu-id="96ef4-121">Se un utente è un membro di entrambi gli utenti di MBAM helpdesk e MBAM Advanced helpdesk utenti, le autorizzazioni di MBAM Advanced helpdesk utenti sovrascriveranno le autorizzazioni utente di MBAM helpdesk.</span><span class="sxs-lookup"><span data-stu-id="96ef4-121">If a user is a member of both MBAM Helpdesk Users and MBAM Advanced Helpdesk Users, the MBAM Advanced Helpdesk Users permissions will overwrite the MBAM Helpdesk User permissions.</span></span>

<span data-ttu-id="96ef4-122">**Importante**  Per visualizzare i report, un utente di amministrazione deve essere un membro del gruppo di sicurezza degli **utenti del report mbam** nel database di amministrazione e monitoraggio Server, conformità e controllo e nel server che ospita la funzionalità conformità e report.</span><span class="sxs-lookup"><span data-stu-id="96ef4-122">**Important** To view the reports, an administrative user must be a member of the **MBAM Report Users** security group on the Administration and Monitoring Server, Compliance and Audit Database, and on the server that hosts the Compliance and Reports feature.</span></span> <span data-ttu-id="96ef4-123">Come procedura consigliata, creare un gruppo di sicurezza in Active Directory con i diritti sul gruppo di sicurezza Local **report degli utenti di mbam** nel server di amministrazione e monitoraggio e nel server che ospita la conformità e i report.</span><span class="sxs-lookup"><span data-stu-id="96ef4-123">As a best practice, create a security group in Active Directory with rights on the local **MBAM Report Users** security group on both the Administration and Monitoring Server and on the server that hosts the Compliance and Reports.</span></span>

 

## <span data-ttu-id="96ef4-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96ef4-124">Related topics</span></span>


[<span data-ttu-id="96ef4-125">Preparazione dell'ambiente per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="96ef4-125">Preparing your Environment for MBAM 1.0</span></span>](preparing-your-environment-for-mbam-10.md)

 

 





