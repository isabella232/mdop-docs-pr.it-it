---
title: Come gestire i ruoli di amministrazione di MBAM
description: Come gestire i ruoli di amministrazione di MBAM
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825116"
---
# <span data-ttu-id="f302c-103">Come gestire i ruoli di amministrazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="f302c-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="f302c-104">Dopo che la configurazione di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) è stata completata per tutte le funzionalità del server, agli utenti amministrativi dovrà essere concesso l'accesso.</span><span class="sxs-lookup"><span data-stu-id="f302c-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users will have to be granted access to them.</span></span> <span data-ttu-id="f302c-105">Come procedura consigliata, gli amministratori che gestiscono o usano le caratteristiche di amministrazione e monitoraggio di Microsoft BitLocker devono essere assegnati ai gruppi di sicurezza dei servizi di dominio e quindi tali gruppi devono essere aggiunti al gruppo di amministrazione locale di MBAM appropriato.</span><span class="sxs-lookup"><span data-stu-id="f302c-105">As a best practice, administrators who will manage or use Microsoft BitLocker Administration and Monitoring Server features should be assigned to Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="f302c-106">Per gestire le appartenenze al ruolo di amministratore di MBAM</span><span class="sxs-lookup"><span data-stu-id="f302c-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="f302c-107">Assegnare utenti amministrativi ai gruppi di sicurezza in servizi di dominio di ActiveDirectory.</span><span class="sxs-lookup"><span data-stu-id="f302c-107">Assign administrative users to security groups in ActiveDirectory Domain Services.</span></span>

2.  <span data-ttu-id="f302c-108">Aggiungere gruppi di sicurezza di ActiveDirectory ai ruoli per MBAM Administrative Groups Local sul server MBAM per le rispettive caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="f302c-108">Add ActiveDirectory security groups to the roles for MBAM administrative local groups on the MBAM server for the respective features.</span></span>

    -   <span data-ttu-id="f302c-109">Gli **amministratori di sistema di mbam** hanno accesso a tutte le caratteristiche di MBAM nel sito Web di amministrazione e monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="f302c-109">**MBAM System Administrators** have access to all MBAM features in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="f302c-110">**Gli utenti di mbam helpdesk** hanno accesso alle opzioni Gestisci TPM e ripristino unità nel sito Web di amministrazione e monitoraggio di mbam, ma devono compilare tutti i campi quando usano un'opzione qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="f302c-110">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="f302c-111">**Report mbam gli utenti** possono accedere ai report di conformità e controllo nel sito Web di amministrazione e monitoraggio di mbam.</span><span class="sxs-lookup"><span data-stu-id="f302c-111">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM Administration and Monitoring website.</span></span>

    -   <span data-ttu-id="f302c-112">**Gli utenti di mbam Advanced helpdesk** hanno accesso alle opzioni Gestisci TPM e ripristino unità nel sito Web di amministrazione e monitoraggio di mbam, ma non sono obbligati a compilare tutti i campi quando usano un'opzione qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="f302c-112">**MBAM Advanced Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM Administration and Monitoring website, but are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="f302c-113">Per altre informazioni sui ruoli per l'amministrazione e il monitoraggio di Microsoft BitLocker, vedere [pianificazione dei ruoli di amministratore di MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="f302c-113">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 2.0 Administrator Roles](planning-for-mbam-20-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="f302c-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f302c-114">Related topics</span></span>


[<span data-ttu-id="f302c-115">Amministrazione delle funzionalità di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f302c-115">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





