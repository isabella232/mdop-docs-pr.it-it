---
title: UNPUBLISH PACKAGE
description: UNPUBLISH PACKAGE
author: dansimp
ms.assetid: 1651427c-72a5-4701-bb57-71e14a7a3803
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7704fb3ed03be4864a837767d9e890d28b63f175
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815135"
---
# <span data-ttu-id="a0d25-103">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="a0d25-103">UNPUBLISH PACKAGE</span></span>


<span data-ttu-id="a0d25-104">Consente di rimuovere i tasti di scelta rapida e i tipi di file per un intero pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a0d25-104">Enables you to remove the shortcuts and file types for an entire package.</span></span>

`SFTMIME UNPUBLISH PACKAGE:package-name [/CLEAR] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a0d25-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="a0d25-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="a0d25-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0d25-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0d25-107">PACCHETTO: &lt; nome pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="a0d25-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0d25-108">Nome del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a0d25-108">The name of the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0d25-109">/CLEAR</span><span class="sxs-lookup"><span data-stu-id="a0d25-109">/CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0d25-110">Se presente, verranno rimosse anche le impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="a0d25-110">If present, user settings will also be removed.</span></span> <span data-ttu-id="a0d25-111">Per altre informazioni, vedere la nota importante più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="a0d25-111">(For more information, see the Important note later in this topic.)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0d25-112">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="a0d25-112">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0d25-113">Se presente, il pacchetto sarà non pubblicato per tutti gli utenti di questo computer.</span><span class="sxs-lookup"><span data-stu-id="a0d25-113">If present, the package will be unpublished for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0d25-114">/LOG</span><span class="sxs-lookup"><span data-stu-id="a0d25-114">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0d25-115">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="a0d25-115">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0d25-116">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="a0d25-116">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0d25-117">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="a0d25-117">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0d25-118">/GUI</span><span class="sxs-lookup"><span data-stu-id="a0d25-118">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0d25-119">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="a0d25-119">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a0d25-120">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="a0d25-120">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0d25-121">/LOGU</span><span class="sxs-lookup"><span data-stu-id="a0d25-121">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0d25-122">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="a0d25-122">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a0d25-123">**Importante**  Prima di poter eseguire il comando **UNPUBLISH PACKAGE** , il pacchetto deve essere già stato aggiunto al client Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="a0d25-123">**Important** Before you can run the **UNPUBLISH PACKAGE** command, the package must already have been added to the Application Virtualization Client.</span></span>

<span data-ttu-id="a0d25-124">Per usare il pacchetto **globale**, l'annullamento della **pubblicazione** deve essere eseguito come amministratore locale. in caso contrario, è necessaria solo l'autorizzazione **ClearApp** .</span><span class="sxs-lookup"><span data-stu-id="a0d25-124">To use **GLOBAL**, **UNPUBLISH PACKAGE** must be run as local Administrator; otherwise, only **ClearApp** permission is needed.</span></span>

<span data-ttu-id="a0d25-125">L'uso di **UNPUBLISH PACKAGE** with **Global** rimuove tutti i tipi di file globali e i tasti di scelta rapida per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a0d25-125">Using **UNPUBLISH PACKAGE** with **GLOBAL** removes any global file types and shortcuts for the package.</span></span> <span data-ttu-id="a0d25-126">**Clear** non è applicabile.</span><span class="sxs-lookup"><span data-stu-id="a0d25-126">**CLEAR** is not applicable.</span></span>

<span data-ttu-id="a0d25-127">L'uso di **UNPUBLISH PACKAGE** without **Global** rimuove i tasti di scelta rapida e i tipi di file per il pacchetto e, se **Clear** è impostato, rimuove anche le impostazioni utente e arresta i carichi in background nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a0d25-127">Using **UNPUBLISH PACKAGE** without **GLOBAL** removes the user shortcuts and file types for the package and, if **CLEAR** is set, also removes user settings and stops background loads under the user’s context.</span></span>

<span data-ttu-id="a0d25-128">**UNPUBLISH PACKAGE** funziona con le applicazioni dello stesso nome del pacchetto o GUID usato come ID di origine per il pacchetto di **aggiunta**, **modifica**e **pubblicazione**.</span><span class="sxs-lookup"><span data-stu-id="a0d25-128">**UNPUBLISH PACKAGE** works on applications from the same package name or GUID that was used as the source ID for **ADD**, **EDIT**, and **PUBLISH PACKAGE**.</span></span>

<span data-ttu-id="a0d25-129">Annulla **pubblicazione pacchetto** Cancella sempre tutte le impostazioni utente, i collegamenti e i tipi di file indipendentemente dall'uso dell'opzione/Clear.</span><span class="sxs-lookup"><span data-stu-id="a0d25-129">**UNPUBLISH PACKAGE** always clears all the user settings, shortcuts, and file types regardless of the use of the /CLEAR switch.</span></span>

 

## <span data-ttu-id="a0d25-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0d25-130">Related topics</span></span>


[<span data-ttu-id="a0d25-131">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="a0d25-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





