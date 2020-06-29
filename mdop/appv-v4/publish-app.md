---
title: PUBLISH APP
description: PUBLISH APP
author: dansimp
ms.assetid: f25f06a8-ca23-435b-a0c2-16a5f39b6b97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2ccb19255786ee47a8356feef14be1c4d9b4fb2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815816"
---
# <span data-ttu-id="2fdbf-103">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="2fdbf-103">PUBLISH APP</span></span>


<span data-ttu-id="2fdbf-104">Pubblica un collegamento a un'applicazione nel menu Start dell'utente, nel desktop o in un'altra posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-104">Publishes an application shortcut to the user's Start menu, desktop, or other specified location.</span></span>

`SFTMIME PUBLISH APP:application                 {/DESKTOP | /START | /TARGET target-path} [/ICON icon-pathname]                 [/DISPLAY display-name] [/ARGS command-args...]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="2fdbf-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="2fdbf-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="2fdbf-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fdbf-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fdbf-107">APPLICAZIONE: &lt; applicazione&gt;</span><span class="sxs-lookup"><span data-stu-id="2fdbf-107">APPLICATION:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-108">Nome e versione (facoltativa) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-108">The name and version (optional) of the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fdbf-109">/DESKTOP</span><span class="sxs-lookup"><span data-stu-id="2fdbf-109">/DESKTOP</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-110">Pubblica un collegamento al desktop dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-110">Publishes a shortcut to the user's desktop.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fdbf-111">/START</span><span class="sxs-lookup"><span data-stu-id="2fdbf-111">/START</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-112">Pubblica un collegamento alla cartella Application Virtualization Applications nella cartella Programs del menu Start.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-112">Publishes a shortcut to the Application Virtualization Applications folder in the Programs folder of the Start menu.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fdbf-113">/TARGET &lt; target-Path&gt;</span><span class="sxs-lookup"><span data-stu-id="2fdbf-113">/TARGET &lt;target-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-114">Percorso assoluto in cui deve essere pubblicato il collegamento.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-114">The absolute path where the shortcut should be published.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fdbf-115">&lt;Icona/icona-percorso&gt;</span><span class="sxs-lookup"><span data-stu-id="2fdbf-115">/ICON &lt;icon-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-116">Il percorso o l'URL per il file dell'icona.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-116">The path or URL for the icon file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fdbf-117">/DISPLAY &lt; -nome visualizzato&gt;</span><span class="sxs-lookup"><span data-stu-id="2fdbf-117">/DISPLAY &lt;display-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-118">Nome visualizzato per il collegamento.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-118">The display name for the shortcut.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fdbf-119">&lt;Comando/args-args&gt;</span><span class="sxs-lookup"><span data-stu-id="2fdbf-119">/ARGS &lt;command-args&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-120">Parametri da passare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-120">Parameters to be passed to the application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fdbf-121">/LOG</span><span class="sxs-lookup"><span data-stu-id="2fdbf-121">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-122">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-122">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fdbf-123">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="2fdbf-123">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-124">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="2fdbf-124">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="2fdbf-125">/GUI</span><span class="sxs-lookup"><span data-stu-id="2fdbf-125">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-126">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-126">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="2fdbf-127">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-127">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="2fdbf-128">/LOGU</span><span class="sxs-lookup"><span data-stu-id="2fdbf-128">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="2fdbf-129">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="2fdbf-129">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="2fdbf-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2fdbf-130">Related topics</span></span>


[<span data-ttu-id="2fdbf-131">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="2fdbf-131">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





