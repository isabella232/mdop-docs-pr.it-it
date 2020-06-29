---
title: Come gestire le esenzioni della crittografia BitLocker dell'utente
description: Come gestire le esenzioni della crittografia BitLocker dell'utente
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826795"
---
# <span data-ttu-id="b1b1d-103">Come gestire le esenzioni della crittografia BitLocker dell'utente</span><span class="sxs-lookup"><span data-stu-id="b1b1d-103">How to Manage User BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="b1b1d-104">Microsoft BitLocker Administration and Monitoring (MBAM) consente di esonerare gli utenti dai requisiti di crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-104">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="b1b1d-105">Per esonerare gli utenti dalla protezione di BitLocker, è necessario:</span><span class="sxs-lookup"><span data-stu-id="b1b1d-105">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b1b1d-106">Attività</span><span class="sxs-lookup"><span data-stu-id="b1b1d-106">Task</span></span></th>
<th align="left"><span data-ttu-id="b1b1d-107">Dettagli</span><span class="sxs-lookup"><span data-stu-id="b1b1d-107">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1b1d-108">Creare un'infrastruttura per supportare gli utenti esentati.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-108">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1b1d-109">Gli esempi di questa infrastruttura includono fornire agli utenti un numero di telefono di contatto, una pagina Web o un indirizzo di posta elettronica che possono usare per richiedere un'esenzione.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-109">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1b1d-110">Aggiungere l'utente esentato a un gruppo di sicurezza per un oggetto Criteri di gruppo configurato in modo specifico per gli utenti esentati.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-110">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1b1d-111">Quando i membri di questo gruppo di sicurezza si iscrivono a un computer, l'impostazione di criteri di gruppo dell'utente esonera l'utente dalla protezione BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-111">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="b1b1d-112">L'impostazione di criteri di gruppo dell'utente sovrascrive i criteri del computer e il computer rimarrà esentato dalla crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-112">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b1b1d-113">Nota</span><span class="sxs-lookup"><span data-stu-id="b1b1d-113">Note</span></span></strong><br/><p><span data-ttu-id="b1b1d-114">MBAM non emana i criteri di crittografia se il computer è già protetto da BitLocker e l'utente è esonerato.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-114">MBAM does not enact the encryption policy if the computer is already BitLocker-protected and the user is exempted.</span></span> <span data-ttu-id="b1b1d-115">Tuttavia, se un altro utente che non è esonerato dai criteri di crittografia accede al computer, verrà applicata la crittografia.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-115">However, if another user who is not exempt from the encryption policy signs in to the computer, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b1b1d-116">I passaggi seguenti descrivono ciò che accade quando gli utenti finali richiedono un'esenzione dal processo di esenzione dalla crittografia unità BitLocker tramite il client MBAM o attraverso qualsiasi processo usato dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-116">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="b1b1d-117">È necessario configurare le impostazioni dei criteri di gruppo di MBAM per consentire agli utenti finali di richiedere un'esenzione dalla crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-117">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="b1b1d-118">Quando gli utenti finali accedono a un computer che deve essere crittografato, ricevono una notifica per cui il computer verrà crittografato.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-118">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="b1b1d-119">Possono selezionare l' **esenzione dalla richiesta** e posticipare la crittografia selezionando **rinvia**oppure selezionare **Avvia crittografia** per accettare la crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-119">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="b1b1d-120">Nota</span><span class="sxs-lookup"><span data-stu-id="b1b1d-120">Note</span></span>**  
    <span data-ttu-id="b1b1d-121">Selezionando **esenzione dalla richiesta** rinvia la protezione di BitLocker fino al tempo massimo impostato nei criteri di esenzione dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-121">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="b1b1d-122">Se gli utenti finali selezionano **esenzione dalla richiesta**, ricevono una notifica che informa loro di contattare il gruppo di amministrazione BitLocker dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-122">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="b1b1d-123">A seconda della configurazione dei **criteri di esenzione** per l'utente, gli utenti vengono forniti con uno o più dei metodi di contatto seguenti:</span><span class="sxs-lookup"><span data-stu-id="b1b1d-123">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="b1b1d-124">Numero di telefono</span><span class="sxs-lookup"><span data-stu-id="b1b1d-124">Phone number</span></span>

    -   <span data-ttu-id="b1b1d-125">URL della pagina Web</span><span class="sxs-lookup"><span data-stu-id="b1b1d-125">Webpage URL</span></span>

    -   <span data-ttu-id="b1b1d-126">Indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="b1b1d-126">Mailing address</span></span>

3.  <span data-ttu-id="b1b1d-127">Dopo aver ricevuto la richiesta di esenzione, l'amministratore di MBAM decide se aggiungere l'utente al gruppo servizi di dominio Active Directory (AD DS) di esenzione per BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-127">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="b1b1d-128">Dopo che un utente finale invia una richiesta di esenzione, il client MBAM segnala l'utente come "temporaneamente esenti".</span><span class="sxs-lookup"><span data-stu-id="b1b1d-128">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="b1b1d-129">Il client attende quindi un numero specificato di giorni, che gli amministratori IT configurano, prima di verificare di nuovo la conformità del computer.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-129">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="b1b1d-130">Se l'amministratore di MBAM respinge la richiesta di esenzione, l'opzione per la richiesta di esenzione è disattivata, che impedisce che l'utente richieda l'esenzione.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-130">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

<span data-ttu-id="b1b1d-131">Microsoft BitLocker Administration and Monitoring (MBAM) consente di esonerare gli utenti dai requisiti di crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-131">Microsoft BitLocker Administration and Monitoring (MBAM) enables you to exempt users from BitLocker Drive Encryption requirements.</span></span>

<span data-ttu-id="b1b1d-132">Per esonerare gli utenti dalla protezione di BitLocker, è necessario:</span><span class="sxs-lookup"><span data-stu-id="b1b1d-132">To exempt users from BitLocker protection, you have to:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b1b1d-133">Attività</span><span class="sxs-lookup"><span data-stu-id="b1b1d-133">Task</span></span></th>
<th align="left"><span data-ttu-id="b1b1d-134">Dettagli</span><span class="sxs-lookup"><span data-stu-id="b1b1d-134">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1b1d-135">Creare un'infrastruttura per supportare gli utenti esentati.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-135">Create an infrastructure to support exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1b1d-136">Gli esempi di questa infrastruttura includono fornire agli utenti un numero di telefono di contatto, una pagina Web o un indirizzo di posta elettronica che possono usare per richiedere un'esenzione.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-136">Examples of this infrastructure include providing users with a contact telephone number, webpage, or mailing address that they can use to request an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1b1d-137">Aggiungere l'utente esentato a un gruppo di sicurezza per un oggetto Criteri di gruppo configurato in modo specifico per gli utenti esentati.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-137">Add the exempted user to a security group for a Group Policy Object that is configured specifically for exempted users.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1b1d-138">Quando i membri di questo gruppo di sicurezza si iscrivono a un computer, l'impostazione di criteri di gruppo dell'utente esonera l'utente dalla protezione BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-138">When members of this security group sign in to a computer, the user’s Group Policy setting exempts the user from BitLocker protection.</span></span> <span data-ttu-id="b1b1d-139">L'impostazione di criteri di gruppo dell'utente sovrascrive i criteri del computer e il computer rimarrà esentato dalla crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-139">The user’s Group Policy setting overwrites the computer policy, and the computer will remain exempt from BitLocker encryption.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b1b1d-140">Nota</span><span class="sxs-lookup"><span data-stu-id="b1b1d-140">Note</span></span></strong><br/><p><span data-ttu-id="b1b1d-141">Se il computer è già protetto da BitLocker, il criterio di esenzione dall'utente non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-141">If the computer is already BitLocker-protected, the User Exemption Policy has no effect.</span></span> <span data-ttu-id="b1b1d-142">Inoltre, se un altro utente accede a un computer che non è esentato dai criteri di crittografia, verrà applicata la crittografia.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-142">In addition, if another user signs in to a computer that is not exempt from the encryption policy, encryption will take place.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b1b1d-143">I passaggi seguenti descrivono ciò che accade quando gli utenti finali richiedono un'esenzione dal processo di esenzione dalla crittografia unità BitLocker tramite il client MBAM o attraverso qualsiasi processo usato dall'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-143">The following steps describe what occurs when end users request an exemption from the BitLocker Drive Encryption exemption process through the MBAM Client or through whatever process your organization uses.</span></span> <span data-ttu-id="b1b1d-144">È necessario configurare le impostazioni dei criteri di gruppo di MBAM per consentire agli utenti finali di richiedere un'esenzione dalla crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-144">You must configure MBAM Group Policy settings to allow end users to request an exemption from BitLocker Drive Encryption.</span></span>

1.  <span data-ttu-id="b1b1d-145">Quando gli utenti finali accedono a un computer che deve essere crittografato, ricevono una notifica per cui il computer verrà crittografato.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-145">When end users sign in to a computer that is required to be encrypted, they receive a notification that their computer is going to be encrypted.</span></span> <span data-ttu-id="b1b1d-146">Possono selezionare l' **esenzione dalla richiesta** e posticipare la crittografia selezionando **rinvia**oppure selezionare **Avvia crittografia** per accettare la crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-146">They can select **Request Exemption** and postpone the encryption by selecting **Postpone**, or they can select **Start Encryption** to accept the BitLocker encryption.</span></span>

    **<span data-ttu-id="b1b1d-147">Nota</span><span class="sxs-lookup"><span data-stu-id="b1b1d-147">Note</span></span>**  
    <span data-ttu-id="b1b1d-148">Selezionando **esenzione dalla richiesta** rinvia la protezione di BitLocker fino al tempo massimo impostato nei criteri di esenzione dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-148">Selecting **Request Exemption** postpones the BitLocker protection until the maximum time that is set in the User Exemption Policy.</span></span>



2.  <span data-ttu-id="b1b1d-149">Se gli utenti finali selezionano **esenzione dalla richiesta**, ricevono una notifica che informa loro di contattare il gruppo di amministrazione BitLocker dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-149">If end users select **Request Exemption**, they receive a notification telling them to contact the organization’s BitLocker administration group.</span></span> <span data-ttu-id="b1b1d-150">A seconda della configurazione dei **criteri di esenzione** per l'utente, gli utenti vengono forniti con uno o più dei metodi di contatto seguenti:</span><span class="sxs-lookup"><span data-stu-id="b1b1d-150">Depending on how the **Configure User Exemption Policy** is configured, users are provided with one or more of the following contact methods:</span></span>

    -   <span data-ttu-id="b1b1d-151">Numero di telefono</span><span class="sxs-lookup"><span data-stu-id="b1b1d-151">Phone number</span></span>

    -   <span data-ttu-id="b1b1d-152">URL della pagina Web</span><span class="sxs-lookup"><span data-stu-id="b1b1d-152">Webpage URL</span></span>

    -   <span data-ttu-id="b1b1d-153">Indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="b1b1d-153">Mailing address</span></span>

3.  <span data-ttu-id="b1b1d-154">Dopo aver ricevuto la richiesta di esenzione, l'amministratore di MBAM decide se aggiungere l'utente al gruppo servizi di dominio Active Directory (AD DS) di esenzione per BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-154">After the exemption request is received, the MBAM administrator decides whether to add the user to the BitLocker Exemption Active Directory Domain Services (AD DS) group.</span></span>

4.  <span data-ttu-id="b1b1d-155">Dopo che un utente finale invia una richiesta di esenzione, il client MBAM segnala l'utente come "temporaneamente esenti".</span><span class="sxs-lookup"><span data-stu-id="b1b1d-155">After an end user submits an exemption request, the MBAM Client reports the user as “Temporarily exempt.”</span></span> <span data-ttu-id="b1b1d-156">Il client attende quindi un numero specificato di giorni, che gli amministratori IT configurano, prima di verificare di nuovo la conformità del computer.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-156">The Client then waits a specified number of days, which IT administrators configure, before it checks the computer’s compliance again.</span></span> <span data-ttu-id="b1b1d-157">Se l'amministratore di MBAM respinge la richiesta di esenzione, l'opzione per la richiesta di esenzione è disattivata, che impedisce che l'utente richieda l'esenzione.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-157">If the MBAM administrator rejects the exemption request, the exemption request option is deactivated, which prevents the user from requesting the exemption again.</span></span>

**<span data-ttu-id="b1b1d-158">Per esonerare un utente dalla crittografia unità BitLocker</span><span class="sxs-lookup"><span data-stu-id="b1b1d-158">To exempt a user from BitLocker Drive Encryption</span></span>**

1.  <span data-ttu-id="b1b1d-159">Creare un gruppo di sicurezza di servizi di dominio Active Directory che verrà usato per gestire le esenzioni dagli utenti dai requisiti di crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-159">Create an AD DS security group that will be used to manage user exemptions from BitLocker encryption requirements.</span></span>

2.  <span data-ttu-id="b1b1d-160">Creare un oggetto Criteri di gruppo usando i modelli di criteri di gruppo per l'amministrazione e il monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-160">Create a Group Policy Object by using the Microsoft BitLocker Administration and Monitoring Group Policy Templates.</span></span>

3.  <span data-ttu-id="b1b1d-161">Associa l'oggetto Criteri di gruppo al gruppo di servizi di dominio Active Directory creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-161">Associate the Group Policy Object with the AD DS group that you created in the previous step.</span></span> <span data-ttu-id="b1b1d-162">Le impostazioni dei criteri per gli utenti esenti si trovano in: **UserConfiguration** &gt; **modelli amministrativi** di &gt; **Windows Components** &gt; **MDOP mbam (BitLocker Management)**.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-162">The policy settings to exempt users are located at: **UserConfiguration** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (BitLocker Management)**.</span></span>

4.  <span data-ttu-id="b1b1d-163">Per il gruppo di sicurezza creato per gli utenti esentati da BitLocker, aggiungere i nomi degli utenti che chiedono un'esenzione.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-163">To the security group you created for BitLocker exempted users, add the names of the users who are requesting an exemption.</span></span>

    <span data-ttu-id="b1b1d-164">Quando un utente accede a un computer controllato da BitLocker, il client MBAM controlla l'impostazione dei criteri di esenzione dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-164">When a user signs in to a computer controlled by BitLocker, the MBAM Client checks the User Exemption Policy setting.</span></span> <span data-ttu-id="b1b1d-165">Se il computer è già crittografato, la protezione di BitLocker non viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-165">If the computer is already encrypted, BitLocker protection is not suspended.</span></span> <span data-ttu-id="b1b1d-166">Se il computer non è crittografato, MBAM non chiede all'utente di crittografarlo.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-166">If the computer is not encrypted, MBAM does not prompt the user to encrypt.</span></span>

    **<span data-ttu-id="b1b1d-167">Importante</span><span class="sxs-lookup"><span data-stu-id="b1b1d-167">Important</span></span>**  
    <span data-ttu-id="b1b1d-168">Gli scenari di computer condivisi richiedono una particolare considerazione quando si usano le esenzioni degli utenti di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-168">Shared computer scenarios require special consideration when you are using BitLocker user exemptions.</span></span> <span data-ttu-id="b1b1d-169">Se un utente non esonerato accede a un computer condiviso con un utente esenta, il computer potrebbe essere crittografato.</span><span class="sxs-lookup"><span data-stu-id="b1b1d-169">If a non-exempt user signs in to a computer that is shared with an exempt user, the computer may be encrypted.</span></span>




## <span data-ttu-id="b1b1d-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b1b1d-170">Related topics</span></span>


[<span data-ttu-id="b1b1d-171">Amministrazione delle funzionalità di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b1b1d-171">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="b1b1d-172">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b1b1d-172">Planning for MBAM 2.5 Group Policy Requirements</span></span>](planning-for-mbam-25-group-policy-requirements.md)




## <span data-ttu-id="b1b1d-173">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="b1b1d-173">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b1b1d-174">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="b1b1d-174">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b1b1d-175">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b1b1d-175">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




