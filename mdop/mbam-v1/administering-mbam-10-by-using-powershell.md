---
title: Amministrazione di MBAM 1.0 con PowerShell
description: Amministrazione di MBAM 1.0 con PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825136"
---
# <span data-ttu-id="1ff45-103">Amministrazione di MBAM 1.0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ff45-103">Administering MBAM 1.0 by Using PowerShell</span></span>


<span data-ttu-id="1ff45-104">Microsoft BitLocker Administration and Monitoring (MBAM) fornisce il seguente set di cmdlet di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1ff45-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="1ff45-105">Gli amministratori possono usare questi cmdlet di PowerShell per eseguire varie attività di MBAM server dal prompt dei comandi invece che dal sito Web di amministrazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ff45-105">Administrators can use these PowerShell cmdlets to perform various MBAM server tasks from the command prompt rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="1ff45-106">Come amministrare MBAM usando PowerShell</span><span class="sxs-lookup"><span data-stu-id="1ff45-106">How to administer MBAM by using PowerShell</span></span>


<span data-ttu-id="1ff45-107">Usare i cmdlet di PowerShell descritti qui per amministrare MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ff45-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ff45-108">Nome</span><span class="sxs-lookup"><span data-stu-id="1ff45-108">Name</span></span></th>
<th align="left"><span data-ttu-id="1ff45-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ff45-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ff45-110">Add-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="1ff45-110">Add-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ff45-111">Aggiunge un nuovo modello hardware all'inventario hardware di MBAM.</span><span class="sxs-lookup"><span data-stu-id="1ff45-111">Adds a new hardware model to the MBAM hardware inventory.</span></span> <span data-ttu-id="1ff45-112">Questo cmdlet può anche specificare se l'hardware è supportato o non supporta la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1ff45-112">This cmdlet can also specify whether the hardware is supported or unsupported for BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ff45-113">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="1ff45-113">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ff45-114">Richiede una chiave di ripristino MBAM che consentirà a un utente di sbloccare un computer o un'unità crittografata.</span><span class="sxs-lookup"><span data-stu-id="1ff45-114">Requests an MBAM recovery key that will enable a user to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ff45-115">Get-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="1ff45-115">Get-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ff45-116">Ottiene un inventario hardware master che contiene dati che indicano se i modelli hardware sono compatibili o non sono compatibili con la crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1ff45-116">Gets a master hardware inventory that contains data that indicates whether hardware models are compatible or incompatible with BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ff45-117">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="1ff45-117">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ff45-118">Fornisce una password del proprietario del TPM per un utente per gestire l'accesso al TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="1ff45-118">Provides a TPM owner password for a user to manage their TPM (Trusted Platform Module) access.</span></span> <span data-ttu-id="1ff45-119">Consente agli utenti quando il TPM li ha bloccati e non accetterà più il PIN.</span><span class="sxs-lookup"><span data-stu-id="1ff45-119">Helps users when TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ff45-120">Installare-Mbam</span><span class="sxs-lookup"><span data-stu-id="1ff45-120">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ff45-121">Installa le caratteristiche di MBAM che includono strumenti avanzati per criteri di gruppo, crittografia, recupero di chiavi e report di conformità.</span><span class="sxs-lookup"><span data-stu-id="1ff45-121">Installs MBAM features that provide advanced group policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ff45-122">Remove-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="1ff45-122">Remove-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ff45-123">Rimuove i modelli hardware dall'inventario hardware.</span><span class="sxs-lookup"><span data-stu-id="1ff45-123">Removes the hardware models from the hardware inventory.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ff45-124">Set-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="1ff45-124">Set-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ff45-125">Consente la gestione di un inventario hardware master per indicare se i modelli hardware sono in grado o non possono eseguire la crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1ff45-125">Allows management of a master hardware inventory to designate whether or not hardware models are capable or incapable to perform BitLocker encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ff45-126">Disinstallare-mbam</span><span class="sxs-lookup"><span data-stu-id="1ff45-126">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ff45-127">Rimuove le caratteristiche di MBAM installate in precedenza che includono strumenti avanzati per i criteri, la crittografia, il recupero delle chiavi e i report di conformità.</span><span class="sxs-lookup"><span data-stu-id="1ff45-127">Removes previously installed MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="1ff45-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ff45-128">Related topics</span></span>


[<span data-ttu-id="1ff45-129">Operazioni relative a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1ff45-129">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





