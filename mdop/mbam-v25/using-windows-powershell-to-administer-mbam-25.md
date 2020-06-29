---
title: Uso di Windows PowerShell per l'amministrazione di MBAM 2.5
description: Uso di Windows PowerShell per l'amministrazione di MBAM 2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804450"
---
# <span data-ttu-id="8b474-103">Uso di Windows PowerShell per l'amministrazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8b474-103">Using Windows PowerShell to Administer MBAM 2.5</span></span>


<span data-ttu-id="8b474-104">Questo argomento descrive i cmdlet di Windows PowerShell per l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) correlati al recupero di computer o unità quando gli utenti vengono bloccati.</span><span class="sxs-lookup"><span data-stu-id="8b474-104">This topic describes Windows PowerShell cmdlets for Microsoft BitLocker Administration and Monitoring (MBAM) that relate to recovering computers or drives when users get locked out.</span></span>

<span data-ttu-id="8b474-105">Per i cmdlet che si usano per configurare le caratteristiche di MBAM server, vedere [configurazione delle caratteristiche del server mbam 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="8b474-105">For cmdlets that you use to configure MBAM Server features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a><span data-ttu-id="8b474-106">Cmdlet per il recupero di computer o unità gestite da MBAM</span><span class="sxs-lookup"><span data-stu-id="8b474-106">Cmdlets for recovering computers or drives that are managed by MBAM</span></span>


<span data-ttu-id="8b474-107">Usare i cmdlet di Windows PowerShell seguenti per recuperare i computer o le unità gestite da MBAM.</span><span class="sxs-lookup"><span data-stu-id="8b474-107">Use the following Windows PowerShell cmdlets to recover computers or drives that are managed by MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b474-108">Nome</span><span class="sxs-lookup"><span data-stu-id="8b474-108">Name</span></span></th>
<th align="left"><span data-ttu-id="8b474-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b474-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b474-110">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="8b474-110">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b474-111">Richiede una chiave di ripristino MBAM che consente agli utenti di sbloccare un computer o un'unità crittografata.</span><span class="sxs-lookup"><span data-stu-id="8b474-111">Requests an MBAM recovery key that enables users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b474-112">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="8b474-112">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b474-113">Fornisce agli utenti una password del proprietario del TPM che possono usare per sbloccare un TPM (Trusted Platform Module) quando il TPM li ha bloccati e non accetterà più il PIN.</span><span class="sxs-lookup"><span data-stu-id="8b474-113">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> <span data-ttu-id="8b474-114">Guida per i cmdlet di MBAM</span><span class="sxs-lookup"><span data-stu-id="8b474-114">MBAM cmdlet Help</span></span>


<span data-ttu-id="8b474-115">La Guida di Windows PowerShell per i cmdlet MBAM è disponibile nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="8b474-115">Windows PowerShell Help for MBAM cmdlets is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8b474-116">Formato della Guida di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b474-116">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="8b474-117">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="8b474-117">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b474-118">In un prompt dei comandi di Windows PowerShell digitare <strong> Get-Help </strong> &lt; <em> cmdlet</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="8b474-118">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="8b474-119">Per caricare i più recenti cmdlet di Windows PowerShell, seguire le istruzioni visualizzate nella pagina <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b474-119">To upload the latest Windows PowerShell cmdlets, follow the instructions in <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b474-120">In TechNet come pagine Web</span><span class="sxs-lookup"><span data-stu-id="8b474-120">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8b474-121">Nell'area download come file di Word. docx</span><span class="sxs-lookup"><span data-stu-id="8b474-121">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8b474-122">Nell'area download come file PDF</span><span class="sxs-lookup"><span data-stu-id="8b474-122">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="8b474-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8b474-123">Related topics</span></span>


[<span data-ttu-id="8b474-124">Amministrazione delle funzionalità di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="8b474-124">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="8b474-125">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b474-125">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## <span data-ttu-id="8b474-126">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="8b474-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8b474-127">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8b474-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8b474-128">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8b474-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





