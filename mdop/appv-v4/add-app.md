---
title: ADD APP
description: ADD APP
author: dansimp
ms.assetid: 329fd0c8-a795-49be-b0fd-1367c5b4a34b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac83c0cf130e8de1d34d42d74e946716e4503246
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819896"
---
# <span data-ttu-id="f5f44-103">ADD APP</span><span class="sxs-lookup"><span data-stu-id="f5f44-103">ADD APP</span></span>


<span data-ttu-id="f5f44-104">Aggiunge un record dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5f44-104">Adds an application record.</span></span>

`SFTMIME ADD APP:application /OSD osd-pathname [/ICON icon-pathname] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f5f44-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="f5f44-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="f5f44-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5f44-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5f44-107">APP: &lt; applicazione&gt;</span><span class="sxs-lookup"><span data-stu-id="f5f44-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5f44-108">Nome e versione (facoltativa) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f5f44-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5f44-109">/OSD &lt; OSD-PathName&gt;</span><span class="sxs-lookup"><span data-stu-id="f5f44-109">/OSD &lt;osd-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5f44-110">Il percorso o l'URL per il file OSD.</span><span class="sxs-lookup"><span data-stu-id="f5f44-110">The path or URL for the OSD file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5f44-111">&lt;Icona/icona-percorso&gt;</span><span class="sxs-lookup"><span data-stu-id="f5f44-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5f44-112">Il percorso o l'URL per il file dell'icona.</span><span class="sxs-lookup"><span data-stu-id="f5f44-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5f44-113">/LOG</span><span class="sxs-lookup"><span data-stu-id="f5f44-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5f44-114">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="f5f44-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5f44-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="f5f44-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5f44-116">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="f5f44-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f5f44-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="f5f44-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5f44-118">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="f5f44-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f5f44-119">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="f5f44-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5f44-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="f5f44-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="f5f44-121">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="f5f44-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f5f44-122">**Nota**  Il nome risultante dell'applicazione verrà ricavato dal file OSD e non dal nome fornito in APP: &lt; applicazione &gt; .</span><span class="sxs-lookup"><span data-stu-id="f5f44-122">**Note** The resulting name of the application will be taken from the OSD file and not from the name provided in APP:&lt;application&gt;.</span></span>

 

## <span data-ttu-id="f5f44-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5f44-123">Related topics</span></span>


[<span data-ttu-id="f5f44-124">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="f5f44-124">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





