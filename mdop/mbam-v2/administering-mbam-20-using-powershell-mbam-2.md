---
title: Amministrazione di MBAM 2.0 con PowerShell
description: Amministrazione di MBAM 2.0 con PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823505"
---
# <span data-ttu-id="633ed-103">Amministrazione di MBAM 2.0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="633ed-103">Administering MBAM 2.0 Using PowerShell</span></span>


<span data-ttu-id="633ed-104">Microsoft BitLocker Administration and Monitoring (MBAM) fornisce il seguente set di cmdlet di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="633ed-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="633ed-105">Gli amministratori possono usare questi cmdlet di PowerShell per eseguire varie attività di amministrazione e monitoraggio di Microsoft BitLocker dalla riga di comando invece che dal sito Web di amministrazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="633ed-105">Administrators can use these PowerShell cmdlets to perform various Microsoft BitLocker Administration and Monitoring server tasks from the command line rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="633ed-106">Come amministrare MBAM usando PowerShell</span><span class="sxs-lookup"><span data-stu-id="633ed-106">How to Administer MBAM Using PowerShell</span></span>


<span data-ttu-id="633ed-107">Usare i cmdlet di PowerShell descritti qui per amministrare MBAM.</span><span class="sxs-lookup"><span data-stu-id="633ed-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="633ed-108">Nome</span><span class="sxs-lookup"><span data-stu-id="633ed-108">Name</span></span></th>
<th align="left"><span data-ttu-id="633ed-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="633ed-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="633ed-110">Installare-Mbam</span><span class="sxs-lookup"><span data-stu-id="633ed-110">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="633ed-111">Installa le caratteristiche di MBAM che includono criteri avanzati, crittografia, ripristino delle chiavi e report di conformità.</span><span class="sxs-lookup"><span data-stu-id="633ed-111">Installs the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="633ed-112">Disinstallare-mbam</span><span class="sxs-lookup"><span data-stu-id="633ed-112">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="633ed-113">Rimuove le caratteristiche di MBAM che consentono di usare criteri avanzati, crittografia, recupero chiavi e strumenti per la creazione di report di conformità.</span><span class="sxs-lookup"><span data-stu-id="633ed-113">Removes the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="633ed-114">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="633ed-114">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="633ed-115">Richiede una chiave di ripristino MBAM che consentirà agli utenti di sbloccare un computer o un'unità crittografata.</span><span class="sxs-lookup"><span data-stu-id="633ed-115">Requests an MBAM recovery key that will enable users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="633ed-116">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="633ed-116">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="633ed-117">Fornisce agli utenti una password del proprietario del TPM che possono usare per sbloccare un TPM (Trusted Platform Module) quando il TPM li ha bloccati e non accetterà più il PIN.</span><span class="sxs-lookup"><span data-stu-id="633ed-117">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="633ed-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="633ed-118">Related topics</span></span>


[<span data-ttu-id="633ed-119">Operazioni relative a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="633ed-119">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





