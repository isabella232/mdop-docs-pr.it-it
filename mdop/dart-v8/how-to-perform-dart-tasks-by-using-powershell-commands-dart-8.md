---
title: Come eseguire attività di DaRT usando i comandi di PowerShell
description: Come eseguire attività di DaRT usando i comandi di PowerShell
author: dansimp
ms.assetid: bc788b00-38c7-4f57-a832-916b68264d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f8ff87aa09555b93ca04a6ec7fa5dd4ba8504514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824305"
---
# <span data-ttu-id="b74f5-103">Come eseguire attività di DaRT usando i comandi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="b74f5-103">How to Perform DaRT Tasks by Using PowerShell Commands</span></span>


<span data-ttu-id="b74f5-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 offre il set di cmdlet di Windows PowerShell seguente.</span><span class="sxs-lookup"><span data-stu-id="b74f5-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="b74f5-105">Gli amministratori possono usare questi cmdlet di PowerShell per eseguire varie attività del server DaRT 8,0 dal prompt dei comandi invece che dalla creazione guidata immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="b74f5-105">Administrators can use these PowerShell cmdlets to perform various DaRT 8.0 server tasks from the command prompt rather than from the DaRT Recovery Image wizard.</span></span>

## <span data-ttu-id="b74f5-106">Per amministrare il dardo usando i comandi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="b74f5-106">To administer DaRT by using PowerShell commands</span></span>


<span data-ttu-id="b74f5-107">Usare i cmdlet di PowerShell descritti qui per amministrare il dardo.</span><span class="sxs-lookup"><span data-stu-id="b74f5-107">Use the PowerShell cmdlets described here to administer DaRT.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b74f5-108">Nome</span><span class="sxs-lookup"><span data-stu-id="b74f5-108">Name</span></span></th>
<th align="left"><span data-ttu-id="b74f5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b74f5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b74f5-110">Copy-DartImage</span><span class="sxs-lookup"><span data-stu-id="b74f5-110">Copy-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="b74f5-111">Brucia una ISO in un CD, un DVD o un'unità USB.</span><span class="sxs-lookup"><span data-stu-id="b74f5-111">Burns an ISO to a CD, DVD, or USB drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b74f5-112">Export-DartImage</span><span class="sxs-lookup"><span data-stu-id="b74f5-112">Export-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="b74f5-113">Consente di convertire in un file ISO il file WIM di origine, che contiene un'immagine dardo.</span><span class="sxs-lookup"><span data-stu-id="b74f5-113">Allows the source WIM file, which contains a DaRT image, to be converted into an ISO file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b74f5-114">New-DartConfiguration</span><span class="sxs-lookup"><span data-stu-id="b74f5-114">New-DartConfiguration</span></span></p></td>
<td align="left"><p><span data-ttu-id="b74f5-115">Crea un oggetto di configurazione DaRT necessario per applicare un set di strumenti DaRT a un'immagine Windows.</span><span class="sxs-lookup"><span data-stu-id="b74f5-115">Creates a DaRT configuration object that is needed to apply a DaRT toolset to a Windows Image.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b74f5-116">Set-DartImage</span><span class="sxs-lookup"><span data-stu-id="b74f5-116">Set-DartImage</span></span></p></td>
<td align="left"><p><span data-ttu-id="b74f5-117">Applica un oggetto DartConfiguration a un'immagine di Windows montata.</span><span class="sxs-lookup"><span data-stu-id="b74f5-117">Applies a DartConfiguration object to a mounted Windows Image.</span></span> <span data-ttu-id="b74f5-118">Questo include l'aggiunta di tutti i file, la configurazione e le dipendenze tra pacchetti.</span><span class="sxs-lookup"><span data-stu-id="b74f5-118">This includes adding all files, configuration, and package dependencies.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b74f5-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b74f5-119">Related topics</span></span>


[<span data-ttu-id="b74f5-120">Amministrazione di DaRT 8.0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="b74f5-120">Administering DaRT 8.0 Using PowerShell</span></span>](administering-dart-80-using-powershell-dart-8.md)

 

 





