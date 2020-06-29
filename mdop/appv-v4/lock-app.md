---
title: LOCK APP
description: LOCK APP
author: dansimp
ms.assetid: 30673433-4364-499f-8116-cb135fe2716f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 319271640c2550fc94479e876a59b30d3b2bf7ae
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816245"
---
# <span data-ttu-id="2f3f4-103">LOCK APP</span><span class="sxs-lookup"><span data-stu-id="2f3f4-103">LOCK APP</span></span>


<span data-ttu-id="2f3f4-104">Blocca l'applicazione specificata nella cache del file System.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-104">Locks the application specified in the file system cache.</span></span>

`SFTMIME LOCK APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2f3f4-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="2f3f4-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="2f3f4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f3f4-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f3f4-107">APP: &lt; applicazione&gt;</span><span class="sxs-lookup"><span data-stu-id="2f3f4-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f3f4-108">Nome e versione (facoltativa) dell'applicazione da bloccare.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-108">The name and version (optional) of the application to lock.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f3f4-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="2f3f4-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f3f4-110">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f3f4-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="2f3f4-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f3f4-112">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="2f3f4-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2f3f4-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="2f3f4-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f3f4-114">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2f3f4-115">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2f3f4-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="2f3f4-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="2f3f4-117">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="2f3f4-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2f3f4-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f3f4-118">Related topics</span></span>


[<span data-ttu-id="2f3f4-119">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="2f3f4-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





