---
title: ADD TYPE
description: ADD TYPE
author: dansimp
ms.assetid: 8f1d3978-9977-4851-9f46-fee6aefa3535
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d2dcfb24a32dc733aa91b5534e0011090ef12b9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822385"
---
# <span data-ttu-id="6370b-103">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="6370b-103">ADD TYPE</span></span>


<span data-ttu-id="6370b-104">Aggiunge l'associazione di tipi di file specificata.</span><span class="sxs-lookup"><span data-stu-id="6370b-104">Adds the specified file type association.</span></span>

`SFTMIME ADD TYPE:file-extension /APP application [/ICON icon-pathname]                 [/DESCRIPTION type-desc] [/CONTENT-TYPE content-type] [/GLOBAL]                 [/PERCEIVED-TYPE perceived-type] [/PROGID progid]                 [/CONFIRMOPEN {YES|NO}] [/SHOWEXT {YES|NO}]                 [/NEWMENU {YES|NO}]  [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6370b-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="6370b-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="6370b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6370b-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6370b-107">DIGITARE: &lt; File-Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="6370b-107">TYPE:&lt;file-extension&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-108">Estensione del nome di file che verrà associata all'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="6370b-108">The file name extension that will be associated with the application specified.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6370b-109">&lt;Applicazione/App&gt;</span><span class="sxs-lookup"><span data-stu-id="6370b-109">/APP &lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-110">Nome e versione (facoltativa) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6370b-110">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6370b-111">&lt;Icona/icona-percorso&gt;</span><span class="sxs-lookup"><span data-stu-id="6370b-111">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-112">Il percorso o l'URL per il file dell'icona.</span><span class="sxs-lookup"><span data-stu-id="6370b-112">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6370b-113">&lt;Tipo di/Description-DESC&gt;</span><span class="sxs-lookup"><span data-stu-id="6370b-113">/DESCRIPTION &lt;type-desc&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-114">Nome descrittivo dell'utente per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="6370b-114">The user-friendly name for the file type.</span></span> <span data-ttu-id="6370b-115">Impostazione predefinita per il &quot; file di estensione.&quot;</span><span class="sxs-lookup"><span data-stu-id="6370b-115">Defaults to &quot;EXTENSION File.&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6370b-116">&lt;Tipo di contenuto/Content-Type&gt;</span><span class="sxs-lookup"><span data-stu-id="6370b-116">/CONTENT-TYPE &lt;content-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-117">Tipo di contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="6370b-117">The content type of the file.</span></span> <span data-ttu-id="6370b-118">Impostazione predefinita per &quot; application/softricity-extension.&quot;</span><span class="sxs-lookup"><span data-stu-id="6370b-118">Defaults to &quot;application/softricity-extension.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6370b-119">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="6370b-119">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-120">Se presente, il pacchetto sarà disponibile per tutti gli utenti di questo computer.</span><span class="sxs-lookup"><span data-stu-id="6370b-120">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6370b-121">&lt;Tipo di/perceived-Type percepito&gt;</span><span class="sxs-lookup"><span data-stu-id="6370b-121">/PERCEIVED-TYPE &lt;perceived-type&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-122">Tipo di file percepito.</span><span class="sxs-lookup"><span data-stu-id="6370b-122">The perceived type of the file.</span></span> <span data-ttu-id="6370b-123">Il valore predefinito è Nothing.</span><span class="sxs-lookup"><span data-stu-id="6370b-123">Defaults to nothing.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6370b-124">/PROGID &lt; ProgID&gt;</span><span class="sxs-lookup"><span data-stu-id="6370b-124">/PROGID &lt;progid&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-125">Identificatore a livello di codice per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="6370b-125">The programmatic identifier for the file type.</span></span> <span data-ttu-id="6370b-126">Per impostazione predefinita, l'App Virt. Extension. file.</span><span class="sxs-lookup"><span data-stu-id="6370b-126">Defaults to App Virt.extension.File.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6370b-127">/CONFIRMOPEN</span><span class="sxs-lookup"><span data-stu-id="6370b-127">/CONFIRMOPEN</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-128">Indica se gli utenti che scaricano un file di questo tipo devono essere chiesti se aprire o salvare il file.</span><span class="sxs-lookup"><span data-stu-id="6370b-128">Indicates whether users downloading a file of this type should be asked whether to open or save the file.</span></span> <span data-ttu-id="6370b-129">Il valore predefinito è sì.</span><span class="sxs-lookup"><span data-stu-id="6370b-129">Defaults to YES.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6370b-130">/SHOWEXT</span><span class="sxs-lookup"><span data-stu-id="6370b-130">/SHOWEXT</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-131">Indica se l'estensione del file deve essere sempre visualizzata, anche se l'utente ha richiesto che tutte le estensioni vengano nascoste.</span><span class="sxs-lookup"><span data-stu-id="6370b-131">Indicates whether the file's extension should always be shown, even if the user has requested that all extensions be hidden.</span></span> <span data-ttu-id="6370b-132">Il valore predefinito è NO.</span><span class="sxs-lookup"><span data-stu-id="6370b-132">Defaults to NO.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6370b-133">/NEWMENU</span><span class="sxs-lookup"><span data-stu-id="6370b-133">/NEWMENU</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-134">Indica se una voce deve essere aggiunta al <strong> nuovo menu della shell </strong> .</span><span class="sxs-lookup"><span data-stu-id="6370b-134">Indicates whether an entry should be added to the shell's <strong>New</strong> menu.</span></span> <span data-ttu-id="6370b-135">Il valore predefinito è NO.</span><span class="sxs-lookup"><span data-stu-id="6370b-135">Defaults to NO.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6370b-136">/LOG</span><span class="sxs-lookup"><span data-stu-id="6370b-136">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-137">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="6370b-137">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6370b-138">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="6370b-138">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-139">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="6370b-139">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6370b-140">/GUI</span><span class="sxs-lookup"><span data-stu-id="6370b-140">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-141">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="6370b-141">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6370b-142">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="6370b-142">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6370b-143">/LOGU</span><span class="sxs-lookup"><span data-stu-id="6370b-143">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="6370b-144">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="6370b-144">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="6370b-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6370b-145">Related topics</span></span>


[<span data-ttu-id="6370b-146">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="6370b-146">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





