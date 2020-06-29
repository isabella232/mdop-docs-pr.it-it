---
title: CONFIGURE TYPE
description: CONFIGURE TYPE
author: dansimp
ms.assetid: 2caf9433-5449-486f-ab94-83ee8e44d7f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b70cdd1b27eba0109183f1eb9cfb42f08b3f341
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821936"
---
# <span data-ttu-id="d315d-103">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="d315d-103">CONFIGURE TYPE</span></span>


<span data-ttu-id="d315d-104">Consente all'utente di modificare le impostazioni per un'associazione di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="d315d-104">Enables the user to change settings for a file type association.</span></span>

`SFTMIME CONFIGURE TYPE:file-extension [/GLOBAL] [/APP application]                 [/ICON icon-pathname] [/DESCRIPTION type-desc]                 [/CONTENT-TYPE content-type] [/PERCEIVED-TYPE perceived-type]                 [/PROGID progid] [/CONFIRMOPEN {YES|NO}]                 [/SHOWEXT {YES|NO}] [/NEWMENU {YES|NO}]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="d315d-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="d315d-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="d315d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d315d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d315d-107">DIGITARE: &lt; File-Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="d315d-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-108">Estensione del nome file da configurare.</span><span class="sxs-lookup"><span data-stu-id="d315d-108">The file name extension to be configured.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d315d-109">&lt;Applicazione/App&gt;</span><span class="sxs-lookup"><span data-stu-id="d315d-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-110">Nome e versione (facoltativa) dell'applicazione per associare il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="d315d-110">The name and version (optional) of the application to associate this file type with.</span></span> <span data-ttu-id="d315d-111">Non può essere specificato con PROGID.</span><span class="sxs-lookup"><span data-stu-id="d315d-111">Cannot be specified with PROGID.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d315d-112">&lt;Icona/icona-percorso&gt;</span><span class="sxs-lookup"><span data-stu-id="d315d-112">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-113">Il percorso o l'URL per il file dell'icona.</span><span class="sxs-lookup"><span data-stu-id="d315d-113">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d315d-114">&lt;Tipo di/Description-DESC&gt;</span><span class="sxs-lookup"><span data-stu-id="d315d-114">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-115">Nome descrittivo dell'utente per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="d315d-115">The user-friendly name for the file type.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d315d-116">&lt;Tipo di contenuto/Content-Type&gt;</span><span class="sxs-lookup"><span data-stu-id="d315d-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-117">Tipo di contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="d315d-117">The content type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d315d-118">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="d315d-118">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-119">Se presente, indica che l'associazione che si applica a tutti gli utenti deve essere modificata, non quella specifica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d315d-119">If present, indicates that the association that applies to all users should be edited, not the user-specific one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d315d-120">&lt;Tipo di/perceived-Type percepito&gt;</span><span class="sxs-lookup"><span data-stu-id="d315d-120">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-121">Tipo di file percepito.</span><span class="sxs-lookup"><span data-stu-id="d315d-121">The perceived type of the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d315d-122">/PROGID &lt; ProgID&gt;</span><span class="sxs-lookup"><span data-stu-id="d315d-122">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-123">Indica che l'estensione deve essere associata a un tipo di file diverso.</span><span class="sxs-lookup"><span data-stu-id="d315d-123">Indicates that the extension should be associated with a different file type.</span></span> <span data-ttu-id="d315d-124">Il tipo di file precedente non viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="d315d-124">The previous file type is not deleted.</span></span> <span data-ttu-id="d315d-125">Non è possibile specificare l'APP, l'icona, la descrizione, CONFIRMOPEN o SHOWEXT.</span><span class="sxs-lookup"><span data-stu-id="d315d-125">Cannot be specified with APP, ICON, DESCRIPTION, CONFIRMOPEN, or SHOWEXT.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d315d-126">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="d315d-126">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-127">Indica se gli utenti che scaricano un file di questo tipo devono essere chiesti se aprire o salvare il file.</span><span class="sxs-lookup"><span data-stu-id="d315d-127">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d315d-128">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="d315d-128">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-129">Indica se l'estensione del file deve essere sempre visualizzata, anche se l'utente ha richiesto che tutte le estensioni vengano nascoste.</span><span class="sxs-lookup"><span data-stu-id="d315d-129">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d315d-130">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="d315d-130">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-131">Indica se una voce deve essere aggiunta al <strong> nuovo menu della shell </strong> .</span><span class="sxs-lookup"><span data-stu-id="d315d-131">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d315d-132">/LOG</span><span class="sxs-lookup"><span data-stu-id="d315d-132">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-133">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="d315d-133">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d315d-134">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="d315d-134">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-135">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="d315d-135">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="d315d-136">/GUI</span><span class="sxs-lookup"><span data-stu-id="d315d-136">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-137">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="d315d-137">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="d315d-138">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="d315d-138">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="d315d-139">/LOGU</span><span class="sxs-lookup"><span data-stu-id="d315d-139">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="d315d-140">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d315d-140">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="d315d-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d315d-141">Related topics</span></span>


[<span data-ttu-id="d315d-142">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="d315d-142">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





