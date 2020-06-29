---
title: DELETE TYPE
description: DELETE TYPE
author: dansimp
ms.assetid: f2852723-c894-49f3-a3c5-56f9648bb9ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0df68c0a0efcd0e269410d1580f7b0a82301c46d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821686"
---
# <span data-ttu-id="0fbcd-103">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="0fbcd-103">DELETE TYPE</span></span>


<span data-ttu-id="0fbcd-104">Rimuove l'associazione di tipi di file specificata.</span><span class="sxs-lookup"><span data-stu-id="0fbcd-104">Removes the specified file type association.</span></span>

`SFTMIME DELETE TYPE:file-extension [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0fbcd-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="0fbcd-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="0fbcd-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fbcd-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0fbcd-107">DIGITARE: &lt; File-Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="0fbcd-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="0fbcd-108">Estensione del nome file da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0fbcd-108">The file name extension to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0fbcd-109">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="0fbcd-109">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="0fbcd-110">Se specificato, indica che l'associazione globale per l'estensione del nome file deve essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="0fbcd-110">If specified, indicates that the global association for the file name extension should be removed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0fbcd-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="0fbcd-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="0fbcd-112">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="0fbcd-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0fbcd-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="0fbcd-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="0fbcd-114">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="0fbcd-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0fbcd-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="0fbcd-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="0fbcd-116">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="0fbcd-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0fbcd-117">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="0fbcd-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0fbcd-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="0fbcd-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="0fbcd-119">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="0fbcd-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="0fbcd-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0fbcd-120">Related topics</span></span>


[<span data-ttu-id="0fbcd-121">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="0fbcd-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





