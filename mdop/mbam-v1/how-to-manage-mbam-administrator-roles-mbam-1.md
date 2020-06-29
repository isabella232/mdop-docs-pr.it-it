---
title: Come gestire i ruoli di amministrazione di MBAM
description: Come gestire i ruoli di amministrazione di MBAM
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804624"
---
# <span data-ttu-id="54ee8-103">Come gestire i ruoli di amministrazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="54ee8-103">How to Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="54ee8-104">Dopo la configurazione di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) per tutte le funzionalità del server, agli utenti amministrativi deve essere concesso l'accesso a queste funzionalità del server.</span><span class="sxs-lookup"><span data-stu-id="54ee8-104">After Microsoft BitLocker Administration and Monitoring (MBAM) Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="54ee8-105">Come procedura consigliata, gli amministratori che gestiscono o usano le caratteristiche di MBAM server devono essere assegnati a gruppi di sicurezza di Active Directory e quindi tali gruppi devono essere aggiunti al gruppo locale amministrativo di MBAM appropriato.</span><span class="sxs-lookup"><span data-stu-id="54ee8-105">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

**<span data-ttu-id="54ee8-106">Per gestire le appartenenze al ruolo di amministratore di MBAM</span><span class="sxs-lookup"><span data-stu-id="54ee8-106">To manage MBAM Administrator Role memberships</span></span>**

1.  <span data-ttu-id="54ee8-107">Assegnare utenti amministrativi ai gruppi di sicurezza in Servizi ActiveDirectoryDomain.</span><span class="sxs-lookup"><span data-stu-id="54ee8-107">Assign administrative users to security groups in ActiveDirectoryDomain Services.</span></span>

2.  <span data-ttu-id="54ee8-108">Aggiungere gruppi di sicurezza di ActiveDirectoryDomain Services ai ruoli per MBAM Administrative Groups Local nel server di amministrazione e monitoraggio di Microsoft BitLocker per le rispettive funzionalità.</span><span class="sxs-lookup"><span data-stu-id="54ee8-108">Add ActiveDirectoryDomain Services security groups to the roles for MBAM administrative local groups on the Microsoft BitLocker Administration and Monitoring server for the respective features.</span></span> <span data-ttu-id="54ee8-109">I ruoli utente sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="54ee8-109">The user roles are as follows:</span></span>

    -   <span data-ttu-id="54ee8-110">Gli **amministratori di sistema di mbam** hanno accesso a tutte le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="54ee8-110">**MBAM System Administrators** have access to all Microsoft BitLocker Administration and Monitoring features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="54ee8-111">**Gli utenti di mbam hardware** hanno accesso alle funzionalità di compatibilità hardware nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="54ee8-111">**MBAM Hardware Users** have access to the Hardware Compatibility features in the MBAM administration website.</span></span>

    -   <span data-ttu-id="54ee8-112">**Gli utenti di mbam helpdesk** hanno accesso alle opzioni Gestisci TPM e ripristino unità nel sito Web di amministrazione di mbam, ma devono compilare tutti i campi quando usano un'opzione qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="54ee8-112">**MBAM Helpdesk Users** have access to the Manage TPM and Drive Recovery options in the MBAM administration website, but must fill in all fields when they use either option.</span></span>

    -   <span data-ttu-id="54ee8-113">**Report mbam gli utenti** possono accedere ai report di conformità e controllo nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="54ee8-113">**MBAM Report Users** have access to the Compliance and Audit reports in the MBAM administration website.</span></span>

    -   <span data-ttu-id="54ee8-114">**Mbam Advanced helpdesk USA** consente di accedere alle opzioni Gestisci TPM e ripristino unità nel sito Web di amministrazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="54ee8-114">**MBAM Advanced Helpdesk Uses** have access to the Manage TPM and Drive Recovery options in the MBAM administration website.</span></span> <span data-ttu-id="54ee8-115">Questi utenti non sono tenuti a compilare tutti i campi quando usano un'opzione qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="54ee8-115">These users are not required to fill in all fields when they use either option.</span></span>

    <span data-ttu-id="54ee8-116">Per altre informazioni sui ruoli per l'amministrazione e il monitoraggio di Microsoft BitLocker, vedere [pianificazione dei ruoli di amministratore di MBAM 1,0](planning-for-mbam-10-administrator-roles.md).</span><span class="sxs-lookup"><span data-stu-id="54ee8-116">For more information about roles for Microsoft BitLocker Administration and Monitoring, see [Planning for MBAM 1.0 Administrator Roles](planning-for-mbam-10-administrator-roles.md).</span></span>

## <span data-ttu-id="54ee8-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="54ee8-117">Related topics</span></span>


[<span data-ttu-id="54ee8-118">Amministrazione delle funzionalità di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="54ee8-118">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





