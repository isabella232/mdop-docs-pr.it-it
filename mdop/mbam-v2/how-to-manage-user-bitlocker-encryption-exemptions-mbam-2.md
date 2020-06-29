---
title: Come gestire le esenzioni della crittografia BitLocker dell'utente
description: Come gestire le esenzioni della crittografia BitLocker dell'utente
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825075"
---
# <span data-ttu-id="106b4-103">Come gestire le esenzioni della crittografia BitLocker dell'utente</span><span class="sxs-lookup"><span data-stu-id="106b4-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="106b4-104">Microsoft BitLocker Administration and Monitoring (MBAM) può essere usato per gestire la protezione di BitLocker esentando gli utenti se sono presenti utenti che non hanno bisogno o vogliono crittografare le unità.</span><span class="sxs-lookup"><span data-stu-id="106b4-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users if there are users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="106b4-105">Per esonerare gli utenti dalla protezione di BitLocker, un'organizzazione dovrà creare un'infrastruttura per supportare gli utenti esentati, ad esempio per consentire all'utente di usare un numero di telefono di contatto, una pagina Web o un indirizzo di posta elettronica per richiedere un'esenzione.</span><span class="sxs-lookup"><span data-stu-id="106b4-105">To exempt users from BitLocker protection, an organization will have to create an infrastructure to support exempted users, such as giving the user a contact telephone number, webpage, or mailing address to use to request an exemption.</span></span> <span data-ttu-id="106b4-106">Inoltre, un utente esonerato dovrà essere aggiunto a un gruppo di sicurezza per un oggetto Criteri di gruppo creato in modo specifico per gli utenti esentati.</span><span class="sxs-lookup"><span data-stu-id="106b4-106">Also, an exempt user will have to be added to a security group for a Group Policy Object that was created specifically for exempted users.</span></span> <span data-ttu-id="106b4-107">Quando i membri di questo gruppo di sicurezza accedono a un computer, l'impostazione di criteri di gruppo dell'utente indica che l'utente è esonerato dalla protezione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="106b4-107">When members of this security group log on to a computer, the user’s Group Policy setting shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="106b4-108">L'impostazione di criteri di gruppo dell'utente sovrascrive i criteri del computer e il computer rimarrà esentato dalla crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="106b4-108">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="106b4-109">**Nota**  Se il computer è già protetto da BitLocker, il criterio di esenzione dall'utente non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="106b4-109">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="106b4-110">Nella tabella seguente viene illustrato il modo in cui viene applicata la protezione BitLocker in base al modo in cui vengono impostate le esenzioni.</span><span class="sxs-lookup"><span data-stu-id="106b4-110">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="106b4-111">Stato utente</span><span class="sxs-lookup"><span data-stu-id="106b4-111">User Status</span></span></th>
<th align="left"><span data-ttu-id="106b4-112">Computer non esonerato</span><span class="sxs-lookup"><span data-stu-id="106b4-112">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="106b4-113">Computer esenti</span><span class="sxs-lookup"><span data-stu-id="106b4-113">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="106b4-114">L'utente non è esonerato</span><span class="sxs-lookup"><span data-stu-id="106b4-114">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="106b4-115">La protezione di BitLocker viene applicata al computer</span><span class="sxs-lookup"><span data-stu-id="106b4-115">BitLocker protection is enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="106b4-116">La protezione BitLocker non viene applicata al computer</span><span class="sxs-lookup"><span data-stu-id="106b4-116">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="106b4-117">Esenzione dall'utente</span><span class="sxs-lookup"><span data-stu-id="106b4-117">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="106b4-118">La protezione BitLocker non viene applicata al computer</span><span class="sxs-lookup"><span data-stu-id="106b4-118">BitLocker protection is not enforced on computer</span></span></p></td>
<td align="left"><p><span data-ttu-id="106b4-119">La protezione BitLocker non viene applicata al computer</span><span class="sxs-lookup"><span data-stu-id="106b4-119">BitLocker protection is not enforced on computer</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="106b4-120">Per esonerare un utente dalla crittografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="106b4-120">To exempt a user from BitLocker encryption</span></span>**

1.  <span data-ttu-id="106b4-121">Creare un gruppo di sicurezza di ActiveDirectoryDomainServices che verrà usato per gestire le esenzioni dagli utenti dai requisiti di crittografia di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="106b4-121">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="106b4-122">Creare un'impostazione di un oggetto Criteri di gruppo usando il modello di criteri di gruppo amministrazione e monitoraggio di Microsoft BitLocker e associarlo al gruppo di Active Directory creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="106b4-122">Create a Group Policy Object setting by using the Microsoft BitLocker Administration and Monitoring Group Policy template and associate it with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="106b4-123">Le impostazioni dei criteri per gli utenti esenti possono essere trovate in **UserConfiguration\\Administrative Templates\\Windows COMPONENTS\\MDOP mbam (Gestione BitLocker)**.</span><span class="sxs-lookup"><span data-stu-id="106b4-123">The policy settings to exempt users can be found under **UserConfiguration\\Administrative Templates\\Windows Components\\MDOP MBAM (BitLocker Management)**.</span></span>

3.  <span data-ttu-id="106b4-124">Dopo aver creato un gruppo di sicurezza per gli utenti esentati da BitLocker, aggiungere a questo gruppo i nomi degli utenti che chiedono un'esenzione.</span><span class="sxs-lookup"><span data-stu-id="106b4-124">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting an exemption.</span></span> <span data-ttu-id="106b4-125">Quando gli utenti accedono a un computer controllato da BitLocker, il client MBAM verificherà l'impostazione dei criteri di esenzione dall'utente e sospenderà la protezione a seconda che l'utente faccia parte del gruppo di sicurezza dell'esenzione per BitLocker.</span><span class="sxs-lookup"><span data-stu-id="106b4-125">When users log on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="106b4-126">**Importante**  Gli scenari di computer condivisi richiedono una particolare considerazione quando si usano le esenzioni dall'utente.</span><span class="sxs-lookup"><span data-stu-id="106b4-126">**Important** Shared computer scenarios require special consideration when using user exemptions.</span></span> <span data-ttu-id="106b4-127">Se un utente non esenta accede a un computer condiviso con un utente esentasse, il computer potrebbe essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="106b4-127">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="106b4-128">Per consentire agli utenti di richiedere un'esenzione dalla crittografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="106b4-128">To enable users to request an exemption from BitLocker encryption</span></span>**

1.  <span data-ttu-id="106b4-129">Se sono stati configurati criteri di esenzione dall'utente usando il modello di criteri di MBAM, un utente può richiedere un'esenzione dalla protezione di BitLocker tramite il client MBAM.</span><span class="sxs-lookup"><span data-stu-id="106b4-129">If you have configured user exemption policies by using the MBAM policy template, a user can request an exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="106b4-130">Quando gli utenti accedono a un computer che deve essere crittografato, ricevono una notifica per cui il computer verrà crittografato.</span><span class="sxs-lookup"><span data-stu-id="106b4-130">When users log on to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="106b4-131">Possono selezionare **esenzione richiesta** e posticipare la crittografia selezionando **più avanti**oppure selezionare **inizia** per accettare la crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="106b4-131">They can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="106b4-132">**Nota**  Selezionando **esenzione dalla richiesta** rinvia la protezione di BitLocker fino al tempo massimo impostato nei criteri di esenzione dall'utente.</span><span class="sxs-lookup"><span data-stu-id="106b4-132">**Note** Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="106b4-133">Se gli utenti selezionano **esenzione dalla richiesta**, ricevono una notifica per comunicare loro di contattare il gruppo di amministrazione BitLocker dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="106b4-133">If users select **Request Exemption**, they receive a notification telling them to contact your organization’s BitLocker administration group.</span></span> <span data-ttu-id="106b4-134">A seconda della configurazione dei criteri di esenzione per l'utente, gli utenti vengono forniti con uno o più dei metodi di contatto seguenti:</span><span class="sxs-lookup"><span data-stu-id="106b4-134">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="106b4-135">Numero di telefono</span><span class="sxs-lookup"><span data-stu-id="106b4-135">Phone Number</span></span>

    -   <span data-ttu-id="106b4-136">URL della pagina Web</span><span class="sxs-lookup"><span data-stu-id="106b4-136">Webpage URL</span></span>

    -   <span data-ttu-id="106b4-137">Indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="106b4-137">Mailing Address</span></span>

    <span data-ttu-id="106b4-138">Dopo la ricezione della richiesta di esenzione, l'amministratore di MBAM può decidere se è appropriato aggiungere l'utente al gruppo Active Directory di esenzione da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="106b4-138">After the exemption request is received, the MBAM Administrator can take decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="106b4-139">**Nota**  Quando un utente invia una richiesta di esenzione, l'agente MBAM segnala l'utente come "temporaneamente esonerato" e quindi attende un numero configurabile di giorni prima di verificare di nuovo la conformità del computer.</span><span class="sxs-lookup"><span data-stu-id="106b4-139">**Note** Once a user submits an exemption request, the MBAM agent reports the user as “temporarily exempt” and then waits a configurable number of days before it checks the computer’s compliance again.</span></span> <span data-ttu-id="106b4-140">Se l'amministratore di MBAM respinge la richiesta di esenzione, l'opzione per la richiesta di esenzione è disattivata, impedendo che l'utente possa richiedere di nuovo l'esenzione.</span><span class="sxs-lookup"><span data-stu-id="106b4-140">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from being able to request the exemption again.</span></span>

     

## <span data-ttu-id="106b4-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="106b4-141">Related topics</span></span>


[<span data-ttu-id="106b4-142">Amministrazione delle funzionalità di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="106b4-142">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





