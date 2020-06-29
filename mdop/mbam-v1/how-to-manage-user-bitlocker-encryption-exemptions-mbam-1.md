---
title: Come gestire le esenzioni della crittografia BitLocker dell'utente
description: Come gestire le esenzioni della crittografia BitLocker dell'utente
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804623"
---
# <span data-ttu-id="79169-103">Come gestire le esenzioni della crittografia BitLocker dell'utente</span><span class="sxs-lookup"><span data-stu-id="79169-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="79169-104">Microsoft BitLocker Administration and Monitoring (MBAM) può essere usato per gestire la protezione di BitLocker esentando gli utenti che non hanno bisogno o vogliono crittografare le unità.</span><span class="sxs-lookup"><span data-stu-id="79169-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to manage BitLocker protection by exempting users who do not need or want their drives encrypted.</span></span>

<span data-ttu-id="79169-105">Per esonerare gli utenti dalla protezione di BitLocker, un'organizzazione deve prima di tutto creare un'infrastruttura per supportare tali esenzioni.</span><span class="sxs-lookup"><span data-stu-id="79169-105">To exempt users from BitLocker protection, an organization must first create an infrastructure to support such exemptions.</span></span> <span data-ttu-id="79169-106">L'infrastruttura di supporto può includere un numero di telefono di contatto, una pagina Web o un indirizzo di posta elettronica per richiedere l'esenzione.</span><span class="sxs-lookup"><span data-stu-id="79169-106">The supporting infrastructure might include a contact telephone number, webpage, or mailing address to request exemption.</span></span> <span data-ttu-id="79169-107">Inoltre, tutti gli utenti esenti dovranno essere aggiunti a un gruppo di sicurezza per i criteri di gruppo creati in modo specifico per gli utenti esentati.</span><span class="sxs-lookup"><span data-stu-id="79169-107">Also, any exempt user will have to be added to a security group for Group Policy created specifically for exempted users.</span></span> <span data-ttu-id="79169-108">Quando i membri di questo gruppo di sicurezza accedono a un computer, i criteri di gruppo degli utenti indicano che l'utente è esonerato dalla protezione da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="79169-108">When members of this security group log on to a computer, the user Group Policy shows that the user is exempted from BitLocker protection.</span></span> <span data-ttu-id="79169-109">Il criterio utente sovrascrive i criteri del computer e il computer rimarrà esentato dalla crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="79169-109">The user policy overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span>

<span data-ttu-id="79169-110">**Nota**  Se il computer è già protetto da BitLocker, il criterio di esenzione dall'utente non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="79169-110">**Note** If the computer is already BitLocker-protected, the user exemption policy has no effect.</span></span>

 

<span data-ttu-id="79169-111">Nella tabella seguente viene illustrato il modo in cui viene applicata la protezione BitLocker in base al modo in cui vengono impostate le esenzioni.</span><span class="sxs-lookup"><span data-stu-id="79169-111">The following table shows how BitLocker protection is applied based on how exemptions are set.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="79169-112">Stato utente</span><span class="sxs-lookup"><span data-stu-id="79169-112">User Status</span></span></th>
<th align="left"><span data-ttu-id="79169-113">Computer non esonerato</span><span class="sxs-lookup"><span data-stu-id="79169-113">Computer Not Exempt</span></span></th>
<th align="left"><span data-ttu-id="79169-114">Computer esenti</span><span class="sxs-lookup"><span data-stu-id="79169-114">Computer Exempt</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="79169-115">L'utente non è esonerato</span><span class="sxs-lookup"><span data-stu-id="79169-115">User not exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79169-116">La protezione di BitLocker viene applicata nel computer.</span><span class="sxs-lookup"><span data-stu-id="79169-116">BitLocker protection is enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="79169-117">La protezione di BitLocker non viene applicata nel computer.</span><span class="sxs-lookup"><span data-stu-id="79169-117">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="79169-118">Esenzione dall'utente</span><span class="sxs-lookup"><span data-stu-id="79169-118">User exempt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="79169-119">La protezione di BitLocker non viene applicata nel computer.</span><span class="sxs-lookup"><span data-stu-id="79169-119">BitLocker protection is not enforced on the computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="79169-120">La protezione di BitLocker non viene applicata nel computer.</span><span class="sxs-lookup"><span data-stu-id="79169-120">BitLocker protection is not enforced on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="79169-121">Per esonerare un utente dalla crittografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="79169-121">To exempt a user from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="79169-122">Creare un gruppo di sicurezza di ActiveDirectoryDomainServices che verrà usato per gestire le esenzioni dagli utenti dalla crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="79169-122">Create an ActiveDirectoryDomainServices security group that will be used to manage user exemptions from BitLocker encryption.</span></span>

2.  <span data-ttu-id="79169-123">Creare un'impostazione di un oggetto Criteri di gruppo usando il modello di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="79169-123">Create a Group Policy Object setting by using the MBAM Group Policy template.</span></span> <span data-ttu-id="79169-124">Associa l'oggetto Criteri di gruppo al gruppo di Active Directory creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="79169-124">Associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="79169-125">Per altre informazioni sulle impostazioni dei criteri necessarie per consentire agli utenti di richiedere l'esenzione dalla crittografia BitLocker, vedere la sezione configurare i criteri di esenzione dall'utente nella [pianificazione per i requisiti di criteri di gruppo di MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="79169-125">For more information about the necessary policy settings to enable users to request exemption from BitLocker encryption, see the Configure User Exemption Policy section in [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md).</span></span>

3.  <span data-ttu-id="79169-126">Dopo aver creato un gruppo di sicurezza per gli utenti esentati da BitLocker, aggiungere al gruppo i nomi degli utenti che chiedono l'esenzione.</span><span class="sxs-lookup"><span data-stu-id="79169-126">After creating a security group for BitLocker-exempted users, add to this group the names of the users who are requesting exemption.</span></span> <span data-ttu-id="79169-127">Quando un utente accede a un computer controllato da BitLocker, il client MBAM verificherà l'impostazione di criteri di esenzione dall'utente e sospenderà la protezione a seconda che l'utente faccia parte del gruppo di sicurezza per l'esenzione da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="79169-127">When a user logs on to a computer controlled by BitLocker, the MBAM client will check the User Exemption Policy setting and will suspend protection based on whether the user is part of the BitLocker exemption security group.</span></span>

    <span data-ttu-id="79169-128">**Nota**  Gli scenari di computer condivisi richiedono una particolare considerazione per quanto riguarda l'esenzione dall'utente.</span><span class="sxs-lookup"><span data-stu-id="79169-128">**Note** Shared computer scenarios require special consideration regarding user exemption.</span></span> <span data-ttu-id="79169-129">Se un utente non esenta accede a un computer condiviso con un utente esentasse, il computer potrebbe essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="79169-129">If a non-exempt user logs on to a computer shared with an exempt user, the computer may be encrypted.</span></span>

     

**<span data-ttu-id="79169-130">Per consentire agli utenti di richiedere l'esenzione dalla crittografia BitLocker</span><span class="sxs-lookup"><span data-stu-id="79169-130">To enable users to request exemption from BitLocker Encryption</span></span>**

1.  <span data-ttu-id="79169-131">Dopo aver configurato i criteri di esenzione dall'utente usingwith il modello di MBAM Policy, un utente può richiedere l'esenzione dalla protezione di BitLocker tramite il client MBAM.</span><span class="sxs-lookup"><span data-stu-id="79169-131">After you have configured user-exemption policies by usingwith the MBAM Policy template, a user can request exemption from BitLocker protection through the MBAM client.</span></span>

2.  <span data-ttu-id="79169-132">Quando un utente accede a un computer contrassegnato come **compatibile** nell'elenco di compatibilità hardware di mbam, il sistema presenta all'utente una notifica che il computer verrà crittografato.</span><span class="sxs-lookup"><span data-stu-id="79169-132">When a user logs on to a computer that is marked as **Compatible** in the MBAM Hardware Compatibility list, the system presents the user with a notification that the computer is going to be encrypted.</span></span> <span data-ttu-id="79169-133">L'utente può selezionare **esenzione dalla richiesta** e rinviare la crittografia selezionando **più avanti**oppure selezionare **inizia** per accettare la crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="79169-133">The user can select **Request Exemption** and postpone the encryption by selecting **Later**, or select **Start** to accept the BitLocker encryption.</span></span>

    <span data-ttu-id="79169-134">**Nota**  Selezionando **esenzione dalla richiesta** verrà rinviata la protezione di BitLocker fino al tempo massimo impostato nei criteri di esenzione dall'utente.</span><span class="sxs-lookup"><span data-stu-id="79169-134">**Note** Selecting **Request Exemption** will postpone the BitLocker protection until the maximum time set in the User Exemption Policy.</span></span>

     

3.  <span data-ttu-id="79169-135">Quando un utente seleziona la **richiesta di esenzione**, l'utente riceve una notifica per contattare il gruppo di amministrazione BitLocker dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="79169-135">When a user selects **Request Exemption**, the user is notified to contact the organization's BitLocker administration group.</span></span> <span data-ttu-id="79169-136">A seconda della configurazione dei criteri di esenzione per l'utente, gli utenti vengono forniti con uno o più dei metodi di contatto seguenti:</span><span class="sxs-lookup"><span data-stu-id="79169-136">Depending on how the Configure User Exemption Policy is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="79169-137">Numero di telefono</span><span class="sxs-lookup"><span data-stu-id="79169-137">Phone Number</span></span>

    -   <span data-ttu-id="79169-138">URL della pagina Web</span><span class="sxs-lookup"><span data-stu-id="79169-138">Webpage URL</span></span>

    -   <span data-ttu-id="79169-139">Indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="79169-139">Mailing Address</span></span>

    <span data-ttu-id="79169-140">Dopo l'invio della richiesta, l'amministratore di MBAM può decidere se è appropriato aggiungere l'utente al gruppo Active Directory di esenzione da BitLocker.</span><span class="sxs-lookup"><span data-stu-id="79169-140">After submittal of the request, the MBAM Administrator can decide if it is appropriate to add the user to the BitLocker Exemption Active Directory group.</span></span>

    <span data-ttu-id="79169-141">**Nota**  Quando il limite di tempo di posticipazione dei criteri di esenzione dall'utente è scaduto, gli utenti non vedranno l'opzione per richiedere l'esenzione ai criteri di crittografia.</span><span class="sxs-lookup"><span data-stu-id="79169-141">**Note** Once the postpone time limit from the User Exemption Policy has expired, users will not see the option to request exemption to the encryption policy.</span></span> <span data-ttu-id="79169-142">A questo punto, gli utenti devono contattare direttamente l'amministratore di MBAM per ricevere l'esenzione dalla protezione di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="79169-142">At this point, users must contact the MBAM administrator directly in order to receive exemption from BitLocker Protection.</span></span>

     

## <span data-ttu-id="79169-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79169-143">Related topics</span></span>


[<span data-ttu-id="79169-144">Amministrazione delle funzionalità di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="79169-144">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





