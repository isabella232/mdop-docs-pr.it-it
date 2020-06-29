---
title: DELETE PACKAGE
description: DELETE PACKAGE
author: dansimp
ms.assetid: 8f7a4598-610d-490e-a224-426acce01a9f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a0051967ca308e88d143b8116330f5d770d6086d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821696"
---
# <span data-ttu-id="b8c60-103">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="b8c60-103">DELETE PACKAGE</span></span>


<span data-ttu-id="b8c60-104">Rimuove un record del pacchetto e le applicazioni a cui è associato.</span><span class="sxs-lookup"><span data-stu-id="b8c60-104">Removes a package record and the applications associated with it.</span></span>

`SFTMIME DELETE PACKAGE:package-name                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8c60-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="b8c60-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="b8c60-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8c60-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8c60-107">PACCHETTO: &lt; nome pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="b8c60-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8c60-108">Nome del pacchetto da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b8c60-108">The name of the package to be removed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8c60-109">/LOG</span><span class="sxs-lookup"><span data-stu-id="b8c60-109">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8c60-110">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="b8c60-110">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8c60-111">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="b8c60-111">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8c60-112">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="b8c60-112">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8c60-113">/GUI</span><span class="sxs-lookup"><span data-stu-id="b8c60-113">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8c60-114">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="b8c60-114">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b8c60-115">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="b8c60-115">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8c60-116">/LOGU</span><span class="sxs-lookup"><span data-stu-id="b8c60-116">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8c60-117">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b8c60-117">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b8c60-118">**Importante**  Il comando Elimina pacchetto esegue sempre un'eliminazione globale del pacchetto ed Elimina solo i tipi di file globali e i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="b8c60-118">**Important** The DELETE PACKAGE command always performs a global delete of the package and deletes only global file types and shortcuts.</span></span>

<span data-ttu-id="b8c60-119">Se il pacchetto è globale, questo comando deve essere eseguito come amministratore locale. in caso contrario, è necessaria solo l'autorizzazione **Deleteapp** .</span><span class="sxs-lookup"><span data-stu-id="b8c60-119">If the package is global, this command must be run as local Administrator; otherwise, only **DeleteApp** permission is needed.</span></span>

 

## <span data-ttu-id="b8c60-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8c60-120">Related topics</span></span>


[<span data-ttu-id="b8c60-121">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="b8c60-121">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





