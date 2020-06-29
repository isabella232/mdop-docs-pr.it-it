---
title: UNLOAD PACKAGE
description: UNLOAD PACKAGE
author: dansimp
ms.assetid: a076eb5a-ce3d-49e4-ac7a-4d4df10e3477
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fbee040f97bf5675ace7e873741a4270a993a911
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815146"
---
# <span data-ttu-id="72ab3-103">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="72ab3-103">UNLOAD PACKAGE</span></span>


<span data-ttu-id="72ab3-104">Scarica il pacchetto dalla cache del file System.</span><span class="sxs-lookup"><span data-stu-id="72ab3-104">Unloads the package from the file system cache.</span></span>

`SFTMIME UNLOAD PACKAGE:package-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="72ab3-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="72ab3-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="72ab3-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72ab3-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72ab3-107">PACCHETTO: &lt; nome pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="72ab3-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="72ab3-108">Nome del pacchetto da scaricare.</span><span class="sxs-lookup"><span data-stu-id="72ab3-108">The name of the package to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72ab3-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="72ab3-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="72ab3-110">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="72ab3-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72ab3-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="72ab3-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="72ab3-112">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="72ab3-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="72ab3-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="72ab3-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="72ab3-114">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="72ab3-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="72ab3-115">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="72ab3-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="72ab3-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="72ab3-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="72ab3-117">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="72ab3-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="72ab3-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72ab3-118">Related topics</span></span>


[<span data-ttu-id="72ab3-119">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="72ab3-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





