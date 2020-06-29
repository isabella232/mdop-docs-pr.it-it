---
title: DELETE OBJ
description: DELETE OBJ
author: dansimp
ms.assetid: fb17a261-f378-4ce6-a538-ab2f0ada0f2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d74fc1ac098d7dc4dd2f28633e9ca58d4211d74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821705"
---
# <span data-ttu-id="4263c-103">DELETE OBJ</span><span class="sxs-lookup"><span data-stu-id="4263c-103">DELETE OBJ</span></span>


<span data-ttu-id="4263c-104">Rimuove tutti i record dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4263c-104">Removes all of your application records.</span></span>

`SFTMIME DELETE OBJ:APP [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="4263c-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="4263c-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="4263c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4263c-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4263c-107">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="4263c-107">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="4263c-108">Se specificato, tutte le applicazioni vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="4263c-108">If specified, all applications are removed.</span></span> <span data-ttu-id="4263c-109">Per impostazione predefinita, vengono rimosse solo le applicazioni a cui l'utente corrente ha accesso.</span><span class="sxs-lookup"><span data-stu-id="4263c-109">By default, only applications the current user has access to are removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4263c-110">/LOG</span><span class="sxs-lookup"><span data-stu-id="4263c-110">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="4263c-111">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="4263c-111">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4263c-112">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="4263c-112">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="4263c-113">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="4263c-113">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="4263c-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="4263c-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="4263c-115">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="4263c-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="4263c-116">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="4263c-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="4263c-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="4263c-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="4263c-118">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4263c-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="4263c-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4263c-119">Related topics</span></span>


[<span data-ttu-id="4263c-120">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="4263c-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





