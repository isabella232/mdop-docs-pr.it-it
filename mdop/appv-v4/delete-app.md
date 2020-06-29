---
title: DELETE APP
description: DELETE APP
author: dansimp
ms.assetid: 2f89c0c0-373b-4389-a26d-67b3f9712957
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c27c70ef3227ebaf6b16bcb1fbb4b4e65b7cb7f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821716"
---
# <span data-ttu-id="5f4e2-103">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="5f4e2-103">DELETE APP</span></span>


<span data-ttu-id="5f4e2-104">Rimuove un record dell'applicazione dalla cache del file System per renderlo non più visibile.</span><span class="sxs-lookup"><span data-stu-id="5f4e2-104">Removes an application record from the file system cache to make it no longer visible.</span></span> <span data-ttu-id="5f4e2-105">I collegamenti degli utenti e le associazioni di tipi di file sono nascosti ma non eliminati.</span><span class="sxs-lookup"><span data-stu-id="5f4e2-105">Users’ shortcuts and file type associations are hidden but not deleted.</span></span> <span data-ttu-id="5f4e2-106">Nessuna impostazione utente viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="5f4e2-106">No user settings are removed.</span></span>

`SFTMIME DELETE APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5f4e2-107">Parametro</span><span class="sxs-lookup"><span data-stu-id="5f4e2-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="5f4e2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f4e2-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f4e2-109">APP: &lt; applicazione&gt;</span><span class="sxs-lookup"><span data-stu-id="5f4e2-109">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f4e2-110">Nome e versione (facoltativa) dell'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5f4e2-110">The name and version (optional) of the application to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f4e2-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="5f4e2-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f4e2-112">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="5f4e2-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f4e2-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="5f4e2-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f4e2-114">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="5f4e2-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="5f4e2-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="5f4e2-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f4e2-116">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="5f4e2-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="5f4e2-117">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="5f4e2-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5f4e2-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="5f4e2-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="5f4e2-119">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="5f4e2-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="5f4e2-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f4e2-120">Related topics</span></span>


[<span data-ttu-id="5f4e2-121">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="5f4e2-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





