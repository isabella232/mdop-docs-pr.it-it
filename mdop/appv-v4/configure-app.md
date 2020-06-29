---
title: CONFIGURE APP
description: CONFIGURE APP
author: dansimp
ms.assetid: fcfb4f86-8b7c-4208-bca3-955fd067079f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 42ff17e180df262deed3fe79674ad6fda6f0be4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819376"
---
# <span data-ttu-id="c7370-103">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="c7370-103">CONFIGURE APP</span></span>


<span data-ttu-id="c7370-104">Consente all'utente di modificare l'icona associata a un'applicazione ma non di aggiornare l'icona in collegamenti o associazioni di tipi di file esistenti.</span><span class="sxs-lookup"><span data-stu-id="c7370-104">Enables the user to change the icon associated with an application but does not update the icon on existing shortcuts or file type associations.</span></span>

`SFTMIME CONFIGURE APP:application /ICON icon-pathname                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c7370-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="c7370-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="c7370-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7370-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7370-107">APP: &lt; applicazione&gt;</span><span class="sxs-lookup"><span data-stu-id="c7370-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7370-108">Nome e versione (facoltativa) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c7370-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7370-109">&lt;Icona/icona-percorso&gt;</span><span class="sxs-lookup"><span data-stu-id="c7370-109">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7370-110">Il percorso o l'URL per il file dell'icona.</span><span class="sxs-lookup"><span data-stu-id="c7370-110">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7370-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="c7370-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7370-112">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="c7370-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c7370-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="c7370-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7370-114">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="c7370-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7370-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="c7370-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7370-116">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="c7370-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c7370-117">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="c7370-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c7370-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="c7370-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="c7370-119">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c7370-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="c7370-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c7370-120">Related topics</span></span>


[<span data-ttu-id="c7370-121">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="c7370-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





