---
title: ADD PACKAGE
description: ADD PACKAGE
author: dansimp
ms.assetid: aa83928d-a234-4395-831e-2a7ef786ff53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 925349ce5bdf041b6a8768b5413692966e1cfc1e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822396"
---
# <span data-ttu-id="36234-103">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="36234-103">ADD PACKAGE</span></span>


<span data-ttu-id="36234-104">Aggiunge un record del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="36234-104">Adds a package record.</span></span> <span data-ttu-id="36234-105">Se il pacchetto esiste già, questo comando aggiornerà la configurazione del pacchetto esistente.</span><span class="sxs-lookup"><span data-stu-id="36234-105">If the package already exists, this command will update the configuration of the existing package.</span></span>

`SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                 [/OVERRIDEURL url [/AUTOLOADONREFRESH] [/AUTOLOADONLOGIN]                 [/AUTOLOADONLAUNCH] [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="36234-106">Parametro</span><span class="sxs-lookup"><span data-stu-id="36234-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="36234-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36234-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36234-108">PACCHETTO: &lt; nome pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="36234-108">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-109">Nome utente-visibile e user-friendly per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="36234-109">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36234-110">&lt;Percorso manifesto/manifest&gt;</span><span class="sxs-lookup"><span data-stu-id="36234-110">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-111">Percorso del file manifesto che elenca le applicazioni incluse nel pacchetto e tutte le relative informazioni di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="36234-111">The path of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36234-112">&lt;URL/OVERRIDEURL&gt;</span><span class="sxs-lookup"><span data-stu-id="36234-112">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-113">Posizione del file SFT del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="36234-113">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36234-114">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="36234-114">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-115">Il caricamento in background viene eseguito dopo un aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="36234-115">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36234-116">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="36234-116">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-117">Il caricamento in background viene eseguito quando un utente effettua l'accesso.</span><span class="sxs-lookup"><span data-stu-id="36234-117">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36234-118">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="36234-118">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-119">Il caricamento in background viene eseguito dopo che un utente avvia un'applicazione dal pacchetto.</span><span class="sxs-lookup"><span data-stu-id="36234-119">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36234-120">Destinazione/AUTOLOADTARGET</span><span class="sxs-lookup"><span data-stu-id="36234-120">/AUTOLOADTARGET target</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-121">Indica quali applicazioni del pacchetto verranno caricate di carico.</span><span class="sxs-lookup"><span data-stu-id="36234-121">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36234-122">NESSUNO</span><span class="sxs-lookup"><span data-stu-id="36234-122">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-123">Non verrà eseguito alcun caricamento del carico, nonostante la presenza di eventuali flag/AUTOLOADONxxx.</span><span class="sxs-lookup"><span data-stu-id="36234-123">No autoloading will be performed, despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36234-124">TUTTI</span><span class="sxs-lookup"><span data-stu-id="36234-124">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-125">Se è abilitato un trigger di autoload, tutte le applicazioni nel pacchetto verranno caricate nella cache indipendentemente dal fatto che siano o meno già avviate.</span><span class="sxs-lookup"><span data-stu-id="36234-125">If an autoload trigger is enabled, all applications in the package will be loaded into cache whether or not they have been previously started.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36234-126">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="36234-126">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-127">Se è abilitato un trigger di autoload, il pacchetto verrà caricato se le applicazioni di questo pacchetto sono state avviate in precedenza da un utente.</span><span class="sxs-lookup"><span data-stu-id="36234-127">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36234-128">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="36234-128">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-129">Se presente, il pacchetto sarà disponibile per tutti gli utenti di questo computer.</span><span class="sxs-lookup"><span data-stu-id="36234-129">If present, the package will be available for all users on this computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36234-130">/LOG</span><span class="sxs-lookup"><span data-stu-id="36234-130">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-131">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="36234-131">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36234-132">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="36234-132">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-133">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="36234-133">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="36234-134">/GUI</span><span class="sxs-lookup"><span data-stu-id="36234-134">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-135">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="36234-135">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="36234-136">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="36234-136">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="36234-137">/LOGU</span><span class="sxs-lookup"><span data-stu-id="36234-137">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="36234-138">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="36234-138">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="36234-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="36234-139">Related topics</span></span>


[<span data-ttu-id="36234-140">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="36234-140">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





