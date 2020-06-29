---
title: DELETE SERVER
description: DELETE SERVER
author: dansimp
ms.assetid: 4c929639-1c1d-47c3-9225-cc4d7a8736f0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92af31a818174fb4b0e82a11c918af2484ac2bce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821695"
---
# <span data-ttu-id="58f8e-103">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="58f8e-103">DELETE SERVER</span></span>


<span data-ttu-id="58f8e-104">Rimuove un server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="58f8e-104">Removes a publishing server.</span></span>

<span data-ttu-id="58f8e-105">**Nota**  Questo comando non rimuove le applicazioni o i pacchetti pubblicati nel client dal server.</span><span class="sxs-lookup"><span data-stu-id="58f8e-105">**Note** This command does not remove any applications or packages published to the client by the server.</span></span> <span data-ttu-id="58f8e-106">Per ogni applicazione, usa il comando SFTMIME **Clear app** seguito dal comando **Elimina pacchetto** per rimuovere completamente le applicazioni e i pacchetti dal client.</span><span class="sxs-lookup"><span data-stu-id="58f8e-106">For each application, use the SFTMIME **CLEAR APP** command followed by the **DELETE PACKAGE** command to completely remove those applications and packages from the client.</span></span>

 

`SFTMIME DELETE SERVER:server-name [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="58f8e-107">Parametro</span><span class="sxs-lookup"><span data-stu-id="58f8e-107">Parameter</span></span></th>
<th align="left"><span data-ttu-id="58f8e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58f8e-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="58f8e-109">SERVER: &lt; nome server&gt;</span><span class="sxs-lookup"><span data-stu-id="58f8e-109">SERVER:&lt;server-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="58f8e-110">Nome visualizzato del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="58f8e-110">The display name of the publishing server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="58f8e-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="58f8e-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="58f8e-112">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="58f8e-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="58f8e-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="58f8e-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="58f8e-114">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="58f8e-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="58f8e-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="58f8e-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="58f8e-116">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="58f8e-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="58f8e-117">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="58f8e-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="58f8e-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="58f8e-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="58f8e-119">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="58f8e-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="58f8e-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58f8e-120">Related topics</span></span>


[<span data-ttu-id="58f8e-121">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="58f8e-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





