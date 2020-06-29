---
title: UNLOAD APP
description: UNLOAD APP
author: dansimp
ms.assetid: f0d729ae-8772-498b-be11-1a4b35499c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1ae30f5b8c788f8763c2c2b9d1c1956182750d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815155"
---
# <span data-ttu-id="65be6-103">UNLOAD APP</span><span class="sxs-lookup"><span data-stu-id="65be6-103">UNLOAD APP</span></span>


<span data-ttu-id="65be6-104">Scarica l'applicazione e tutte le altre applicazioni nel pacchetto dalla cache del file System.</span><span class="sxs-lookup"><span data-stu-id="65be6-104">Unloads the application and all other applications in the package from the file system cache.</span></span>

`SFTMIME UNLOAD APP:application [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="65be6-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="65be6-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="65be6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65be6-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65be6-107">APP: &lt; applicazione&gt;</span><span class="sxs-lookup"><span data-stu-id="65be6-107">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="65be6-108">Nome e versione (facoltativa) dell'applicazione da scaricare.</span><span class="sxs-lookup"><span data-stu-id="65be6-108">The name and version (optional) of the application to unload.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="65be6-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="65be6-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="65be6-110">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="65be6-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65be6-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="65be6-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="65be6-112">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="65be6-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="65be6-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="65be6-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="65be6-114">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="65be6-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="65be6-115">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="65be6-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="65be6-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="65be6-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="65be6-117">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="65be6-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="65be6-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="65be6-118">Related topics</span></span>


[<span data-ttu-id="65be6-119">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="65be6-119">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





