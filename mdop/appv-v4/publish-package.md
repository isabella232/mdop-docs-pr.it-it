---
title: PUBLISH PACKAGE
description: PUBLISH PACKAGE
author: dansimp
ms.assetid: a33e72dd-194f-4283-8e99-4584ab13de53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00b63389986f495d9405939245a50575bae453f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815815"
---
# <span data-ttu-id="c4463-103">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="c4463-103">PUBLISH PACKAGE</span></span>


<span data-ttu-id="c4463-104">Pubblica il contenuto di un intero pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c4463-104">Publishes the contents of an entire package.</span></span>

`SFTMIME PUBLISH PACKAGE:package-name /MANIFEST manifest-path [/GLOBAL]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c4463-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="c4463-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="c4463-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4463-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4463-107">PACCHETTO: &lt; nome pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="c4463-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4463-108">Nome utente-visibile e user-friendly per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c4463-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4463-109">&lt;Percorso manifesto/manifest&gt;</span><span class="sxs-lookup"><span data-stu-id="c4463-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4463-110">Il percorso o l'URL del file manifesto che elenca le applicazioni incluse nel pacchetto e tutte le relative informazioni di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c4463-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4463-111">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="c4463-111">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4463-112">Se presente, il pacchetto sarà disponibile per tutti gli utenti di questo computer.</span><span class="sxs-lookup"><span data-stu-id="c4463-112">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4463-113">/LOG</span><span class="sxs-lookup"><span data-stu-id="c4463-113">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4463-114">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="c4463-114">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4463-115">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="c4463-115">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4463-116">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="c4463-116">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c4463-117">/GUI</span><span class="sxs-lookup"><span data-stu-id="c4463-117">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4463-118">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="c4463-118">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c4463-119">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="c4463-119">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c4463-120">/LOGU</span><span class="sxs-lookup"><span data-stu-id="c4463-120">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="c4463-121">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="c4463-121">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c4463-122">**Importante**  Il pacchetto deve essere già stato aggiunto al client Application Virtualization e il file manifesto è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c4463-122">**Important** The package must already have been added to the Application Virtualization Client, and the manifest file is required.</span></span>

<span data-ttu-id="c4463-123">Per usare il parametro **Global** , il comando pubblica pacchetto deve essere eseguito come amministratore locale. in caso contrario, sono necessarie solo le autorizzazioni **ManageTypes** e **PublishShortcut** .</span><span class="sxs-lookup"><span data-stu-id="c4463-123">To use the **GLOBAL** parameter, the PUBLISH PACKAGE command must be run as local Administrator; otherwise, only **ManageTypes** and **PublishShortcut** permissions are needed.</span></span>

<span data-ttu-id="c4463-124">La pubblicazione senza il parametro **globale** concede all'utente l'accesso alle applicazioni nel pacchetto e pubblica i tipi di file e i tasti di scelta rapida elencati nel manifesto nel profilo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c4463-124">Publishing without the **GLOBAL** parameter grants the user access to the applications in the package and publishes the file types and shortcuts listed in the manifest to the user’s profile.</span></span>

<span data-ttu-id="c4463-125">La pubblicazione con il parametro **Global** aggiunge i tipi di file e i tasti di scelta rapida elencati nel manifesto al profilo "tutti gli utenti".</span><span class="sxs-lookup"><span data-stu-id="c4463-125">Publishing with the **GLOBAL** parameter adds the file types and shortcuts listed in the manifest to the “All Users” profile.</span></span>

<span data-ttu-id="c4463-126">Se il pacchetto non è globale prima della chiamata e viene usato il parametro **globale** , il pacchetto viene reso globale e disponibile per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="c4463-126">If the package is not global before the call and the **GLOBAL** parameter is used, the package is made global and available to all users.</span></span>

 

## <span data-ttu-id="c4463-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4463-127">Related topics</span></span>


[<span data-ttu-id="c4463-128">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="c4463-128">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





