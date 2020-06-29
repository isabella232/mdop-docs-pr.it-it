---
title: Determinare il motivo per cui un dispositivo riceve un messaggio di non conformità
description: Determinare il motivo per cui un dispositivo riceve un messaggio di non conformità
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824575"
---
# <span data-ttu-id="25bdf-103">Determinare il motivo per cui un dispositivo riceve un messaggio di non conformità</span><span class="sxs-lookup"><span data-stu-id="25bdf-103">Determining why a Device Receives a Noncompliance Message</span></span>


<span data-ttu-id="25bdf-104">I codici di nonconformità seguenti sono forniti da WMI e descrivono i motivi per cui un determinato dispositivo viene segnalato da MBAM come non conforme.</span><span class="sxs-lookup"><span data-stu-id="25bdf-104">The following noncompliance codes are provided by WMI and describe the reasons why a particular device is reported by MBAM as noncompliant.</span></span>

<span data-ttu-id="25bdf-105">Puoi usare il metodo preferito per visualizzare WMI.</span><span class="sxs-lookup"><span data-stu-id="25bdf-105">You can use your preferred method to view WMI.</span></span> <span data-ttu-id="25bdf-106">Se si usa PowerShell, eseguire `gwmi -class mbam_volume -Namespace root\microsoft\mbam` da un prompt di PowerShell e cercare ReasonsForNoncompliance.</span><span class="sxs-lookup"><span data-stu-id="25bdf-106">If you use PowerShell, run `gwmi -class mbam_volume -Namespace root\microsoft\mbam` from a PowerShell prompt and search for ReasonsForNoncompliance.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="25bdf-107">Codice di non conformità</span><span class="sxs-lookup"><span data-stu-id="25bdf-107">Non-Compliance Code</span></span></th>
<th align="left"><span data-ttu-id="25bdf-108">Motivo della mancata conformità</span><span class="sxs-lookup"><span data-stu-id="25bdf-108">Reason for Non-Compliance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="25bdf-109">0</span><span class="sxs-lookup"><span data-stu-id="25bdf-109">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-110">Non crittografare l'AES 256.</span><span class="sxs-lookup"><span data-stu-id="25bdf-110">Cipher strength not AES 256.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="25bdf-111">1</span><span class="sxs-lookup"><span data-stu-id="25bdf-111">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-112">MBAM Policy richiede che il volume sia crittografato, ma non lo è.</span><span class="sxs-lookup"><span data-stu-id="25bdf-112">MBAM Policy requires this volume to be encrypted but it is not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="25bdf-113">2</span><span class="sxs-lookup"><span data-stu-id="25bdf-113">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-114">I criteri di MBAM richiedono che il volume non venga crittografato, ma lo è.</span><span class="sxs-lookup"><span data-stu-id="25bdf-114">MBAM Policy requires this volume to NOT be encrypted, but it is.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="25bdf-115">3</span><span class="sxs-lookup"><span data-stu-id="25bdf-115">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-116">I criteri di MBAM richiedono che questo volume usi un Protector TPM, ma non lo fa.</span><span class="sxs-lookup"><span data-stu-id="25bdf-116">MBAM Policy requires this volume use a TPM protector, but it does not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="25bdf-117">4</span><span class="sxs-lookup"><span data-stu-id="25bdf-117">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-118">I criteri di MBAM richiedono che questo volume usi un TPM + PIN Protector, ma non lo fa.</span><span class="sxs-lookup"><span data-stu-id="25bdf-118">MBAM Policy requires this volume use a TPM+PIN protector, but it does not.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="25bdf-119">5</span><span class="sxs-lookup"><span data-stu-id="25bdf-119">5</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-120">I criteri di MBAM non consentono di segnalare i computer non TPM come conformi.</span><span class="sxs-lookup"><span data-stu-id="25bdf-120">MBAM Policy does not allow non TPM machines to report as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="25bdf-121">6</span><span class="sxs-lookup"><span data-stu-id="25bdf-121">6</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-122">Il volume include un Protector TPM, ma il TPM non è visibile (viene avviato con il tasto recupera dopo la disattivazione del TPM nel BIOS?).</span><span class="sxs-lookup"><span data-stu-id="25bdf-122">Volume has a TPM protector but the TPM is not visible (booted with recover key after disabling TPM in BIOS?).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="25bdf-123">7</span><span class="sxs-lookup"><span data-stu-id="25bdf-123">7</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-124">I criteri di MBAM richiedono che questo volume usi una password Protector, ma non ne ha una.</span><span class="sxs-lookup"><span data-stu-id="25bdf-124">MBAM Policy requires this volume use a password protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="25bdf-125">8</span><span class="sxs-lookup"><span data-stu-id="25bdf-125">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-126">I criteri di MBAM richiedono che il volume non usi una password Protector, ma ne abbia una.</span><span class="sxs-lookup"><span data-stu-id="25bdf-126">MBAM Policy requires this volume NOT use a password protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="25bdf-127">9</span><span class="sxs-lookup"><span data-stu-id="25bdf-127">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-128">I criteri di MBAM richiedono che questo volume usi un Protector di sblocco automatico, ma non ne ha una.</span><span class="sxs-lookup"><span data-stu-id="25bdf-128">MBAM Policy requires this volume use an auto-unlock protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="25bdf-129">10</span><span class="sxs-lookup"><span data-stu-id="25bdf-129">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-130">I criteri di MBAM richiedono che questo volume non usi un Protector di sblocco automatico, ma ne ha una.</span><span class="sxs-lookup"><span data-stu-id="25bdf-130">MBAM Policy requires this volume NOT use an auto-unlock protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="25bdf-131">11</span><span class="sxs-lookup"><span data-stu-id="25bdf-131">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-132">Conflitto di criteri rilevato impedendo a MBAM di segnalare il volume come conforme.</span><span class="sxs-lookup"><span data-stu-id="25bdf-132">Policy conflict detected preventing MBAM from reporting this volume as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="25bdf-133">12</span><span class="sxs-lookup"><span data-stu-id="25bdf-133">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-134">È necessario un volume di sistema per crittografare il volume del sistema operativo, ma non è presente.</span><span class="sxs-lookup"><span data-stu-id="25bdf-134">A system volume is needed to encrypt the OS volume but it is not present.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="25bdf-135">13</span><span class="sxs-lookup"><span data-stu-id="25bdf-135">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-136">La protezione viene sospesa per il volume.</span><span class="sxs-lookup"><span data-stu-id="25bdf-136">Protection is suspended for the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="25bdf-137">14</span><span class="sxs-lookup"><span data-stu-id="25bdf-137">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-138">Autounlock non sicuro a meno che il volume del sistema operativo non sia crittografato.</span><span class="sxs-lookup"><span data-stu-id="25bdf-138">AutoUnlock unsafe unless the OS volume is encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="25bdf-139">15</span><span class="sxs-lookup"><span data-stu-id="25bdf-139">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-140">I criteri richiedono una forza di codifica minima è XTS-AES-128 bit, la forza di Cypher effettiva è più debole.</span><span class="sxs-lookup"><span data-stu-id="25bdf-140">Policy requires minimum cypher strength is XTS-AES-128 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="25bdf-141">16</span><span class="sxs-lookup"><span data-stu-id="25bdf-141">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="25bdf-142">I criteri richiedono una forza di codifica minima è XTS-AES-256 bit, la forza di Cypher effettiva è più debole.</span><span class="sxs-lookup"><span data-stu-id="25bdf-142">Policy requires minimum cypher strength is XTS-AES-256 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="25bdf-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25bdf-143">Related topics</span></span>


[<span data-ttu-id="25bdf-144">Documentazione tecnica per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="25bdf-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="25bdf-145">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="25bdf-145">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## <span data-ttu-id="25bdf-146">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="25bdf-146">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="25bdf-147">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="25bdf-147">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="25bdf-148">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="25bdf-148">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





