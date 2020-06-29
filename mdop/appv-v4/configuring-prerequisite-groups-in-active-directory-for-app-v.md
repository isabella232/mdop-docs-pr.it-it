---
title: Configurazione dei gruppi di prerequisiti in Active Directory per App-V
description: Configurazione dei gruppi di prerequisiti in Active Directory per App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821865"
---
# <span data-ttu-id="db7b8-103">Configurazione dei gruppi di prerequisiti in Active Directory per App-V</span><span class="sxs-lookup"><span data-stu-id="db7b8-103">Configuring Prerequisite Groups in Active Directory for App-V</span></span>


<span data-ttu-id="db7b8-104">Prima di installare il server di gestione di Microsoft Application Virtualization (App-V), è necessario creare gli oggetti seguenti in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db7b8-104">Before you install the Microsoft Application Virtualization (App-V) Management Server, you must create the following objects in Active Directory.</span></span> <span data-ttu-id="db7b8-105">App-V usa i gruppi di Active Directory per controllare l'accesso alle applicazioni e alle funzioni amministrative.</span><span class="sxs-lookup"><span data-stu-id="db7b8-105">App-V uses Active Directory groups to control access to applications and administrative functions.</span></span> <span data-ttu-id="db7b8-106">Si utilizzeranno questi gruppi durante il processo di installazione del server e quando si pubblicano le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="db7b8-106">You will use these groups during the server installation process and when publishing applications.</span></span>

## <span data-ttu-id="db7b8-107">Configurazione dei gruppi prerequisiti in Active Directory per la virtualizzazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="db7b8-107">Configuring Prerequisite Groups in Active Directory for Application Virtualization</span></span>


<span data-ttu-id="db7b8-108">Questa tabella elenca i gruppi di Active Directory necessari per l'installazione di App-V.</span><span class="sxs-lookup"><span data-stu-id="db7b8-108">This table lists the Active Directory groups that are required for installing App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db7b8-109">Oggetto</span><span class="sxs-lookup"><span data-stu-id="db7b8-109">Object</span></span></th>
<th align="left"><span data-ttu-id="db7b8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db7b8-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db7b8-111">Unità organizzativa (OU)</span><span class="sxs-lookup"><span data-stu-id="db7b8-111">Organizational Unit (OU)</span></span></p></td>
<td align="left"><p><span data-ttu-id="db7b8-112">Creare un'unità organizzativa in Active Directory per i gruppi specifici necessari per App-V.</span><span class="sxs-lookup"><span data-stu-id="db7b8-112">Create an OU in Active Directory for the specific groups required for App-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db7b8-113">Gruppo amministrativo App-V</span><span class="sxs-lookup"><span data-stu-id="db7b8-113">App-V Administrative Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="db7b8-114">Durante l'installazione di App-V Management Server devi selezionare un gruppo di Active Directory da usare come gruppo amministratori di App-V per controllare l'accesso amministrativo alla console di gestione.</span><span class="sxs-lookup"><span data-stu-id="db7b8-114">During installation of the App-V Management Server, you must select an Active Directory group to use as the App-V Administrators group to control administrative access to the Management Console.</span></span> <span data-ttu-id="db7b8-115">Creare un gruppo di sicurezza per gli amministratori di App-V e aggiungere a questo gruppo ogni utente che deve usare la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="db7b8-115">Create a security group for App-V administrators, and add to this group every user who needs to use the Management Console.</span></span> <span data-ttu-id="db7b8-116">Non è possibile creare questo gruppo direttamente dal programma di installazione di App-V Management Server.</span><span class="sxs-lookup"><span data-stu-id="db7b8-116">You cannot create this group directly from the App-V Management Server installer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db7b8-117">Gruppo utenti App-V</span><span class="sxs-lookup"><span data-stu-id="db7b8-117">App-V Users Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="db7b8-118">App-V richiede che ogni account utente che accede alle funzioni App-V sia membro di un criterio di provider associato a un singolo gruppo per l'accesso alla piattaforma generale.</span><span class="sxs-lookup"><span data-stu-id="db7b8-118">App-V requires that every User account that accesses App-V functions be a member of a provider policy associated with a single group for general platform access.</span></span> <span data-ttu-id="db7b8-119">Usare un gruppo esistente; ad esempio, gli utenti di dominio, se tutti gli utenti devono avere accesso a App-V o creare un nuovo gruppo.</span><span class="sxs-lookup"><span data-stu-id="db7b8-119">Use an existing group; for example, Domain Users, if all users are to have access to App-V, or create a new group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db7b8-120">Gruppi di applicazioni</span><span class="sxs-lookup"><span data-stu-id="db7b8-120">Application Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="db7b8-121">App-V associa il diritto di usare una singola applicazione con un gruppo di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db7b8-121">App-V associates the right to use an individual application with an Active Directory group.</span></span> <span data-ttu-id="db7b8-122">Crea un gruppo di Active Directory per ogni applicazione e assegna gli utenti a questi gruppi in base alle esigenze per controllare l'accesso degli utenti alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="db7b8-122">Create an Active Directory group for each application, and assign users to these groups as needed to control user access to the applications.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="db7b8-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db7b8-123">Related topics</span></span>


[<span data-ttu-id="db7b8-124">Requisiti per la distribuzione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="db7b8-124">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="db7b8-125">Come configurare Windows Server 2008 per i server di gestione di App-V</span><span class="sxs-lookup"><span data-stu-id="db7b8-125">How to Configure Windows Server 2008 for App-V Management Servers</span></span>](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





