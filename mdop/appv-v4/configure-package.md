---
title: CONFIGURE PACKAGE
description: CONFIGURE PACKAGE
author: dansimp
ms.assetid: acc7eaa8-6ada-47b9-a655-2ca2537605b9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dc8b315b68349cc9834316786b0bf15d4ac3c5cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819346"
---
# <span data-ttu-id="07b35-103">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="07b35-103">CONFIGURE PACKAGE</span></span>


<span data-ttu-id="07b35-104">Consente all'utente di modificare un file manifesto del pacchetto, un'origine pacchetto, tipi di trigger di caricamento o destinazione di caricamento per un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="07b35-104">Enables the user to change a package manifest file, package source, load trigger types, or load target for a package.</span></span>

`SFTMIME CONFIGURE PACKAGE:package-name [/MANIFEST manifest-path]                 [/OVERRIDEURL url] [/AUTOLOADNEVER] [/AUTOLOADONREFRESH]                 [/AUTOLOADONLOGIN] [/AUTOLOADONLAUNCH]                 [/AUTOLOADTARGET {NONE|ALL|PREVUSED}]                 [/LOG log-pathname | /CONSOLE | /GUI]                 [/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="07b35-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="07b35-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="07b35-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07b35-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b35-107">PACCHETTO: &lt; nome pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="07b35-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-108">Nome utente-visibile e user-friendly per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="07b35-108">User-visible and user-friendly name for the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07b35-109">&lt;Percorso manifesto/manifest&gt;</span><span class="sxs-lookup"><span data-stu-id="07b35-109">/MANIFEST &lt;manifest-path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-110">Il percorso o l'URL del file manifesto che elenca le applicazioni incluse nel pacchetto e tutte le relative informazioni di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="07b35-110">The path or URL of the manifest file that lists the applications included in the package and all of their publishing information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b35-111">&lt;URL/OVERRIDEURL&gt;</span><span class="sxs-lookup"><span data-stu-id="07b35-111">/OVERRIDEURL &lt;URL&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-112">Posizione del file SFT del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="07b35-112">The location of the package's SFT file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07b35-113">/AUTOLOADNEVER</span><span class="sxs-lookup"><span data-stu-id="07b35-113">/AUTOLOADNEVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-114">Il caricamento in background è disattivato per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="07b35-114">Background loading is turned off for the package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b35-115">/AUTOLOADONREFRESH</span><span class="sxs-lookup"><span data-stu-id="07b35-115">/AUTOLOADONREFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-116">Il caricamento in background viene eseguito dopo un aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="07b35-116">Background loading is performed after a publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07b35-117">/AUTOLOADONLOGIN</span><span class="sxs-lookup"><span data-stu-id="07b35-117">/AUTOLOADONLOGIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-118">Il caricamento in background viene eseguito quando un utente effettua l'accesso.</span><span class="sxs-lookup"><span data-stu-id="07b35-118">Background loading is performed when a user logs in.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b35-119">/AUTOLOADONLAUNCH</span><span class="sxs-lookup"><span data-stu-id="07b35-119">/AUTOLOADONLAUNCH</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-120">Il caricamento in background viene eseguito dopo che un utente avvia un'applicazione dal pacchetto.</span><span class="sxs-lookup"><span data-stu-id="07b35-120">Background loading is performed after a user starts an application from the package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07b35-121">&lt;Destinazione/AUTOLOADTARGET&gt;</span><span class="sxs-lookup"><span data-stu-id="07b35-121">/AUTOLOADTARGET &lt;target&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-122">Indica quali applicazioni del pacchetto verranno caricate di carico.</span><span class="sxs-lookup"><span data-stu-id="07b35-122">Indicates which applications from the package will be autoloaded.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b35-123">NESSUNO</span><span class="sxs-lookup"><span data-stu-id="07b35-123">NONE</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-124">Non verranno eseguiti carichi di carica automatici, nonostante la presenza di eventuali flag/AUTOLOADONxxx.</span><span class="sxs-lookup"><span data-stu-id="07b35-124">No autoloading will be performed despite the presence of any /AUTOLOADONxxx flags.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07b35-125">TUTTI</span><span class="sxs-lookup"><span data-stu-id="07b35-125">ALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-126">Se è abilitato un trigger di autoload, tutte le applicazioni nel pacchetto verranno caricate nella cache, indipendentemente dal fatto che siano state avviate.</span><span class="sxs-lookup"><span data-stu-id="07b35-126">If an autoload trigger is enabled, all applications in the package will be loaded into cache regardless of whether they have ever been launched.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b35-127">PREVUSED</span><span class="sxs-lookup"><span data-stu-id="07b35-127">PREVUSED</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-128">Se è abilitato un trigger di autoload, il pacchetto verrà caricato se le applicazioni di questo pacchetto sono state avviate in precedenza da un utente.</span><span class="sxs-lookup"><span data-stu-id="07b35-128">If an autoload trigger is enabled, the package will load if any applications in this package have previously been started by a user.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07b35-129">/LOG</span><span class="sxs-lookup"><span data-stu-id="07b35-129">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-130">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="07b35-130">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b35-131">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="07b35-131">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-132">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="07b35-132">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07b35-133">/GUI</span><span class="sxs-lookup"><span data-stu-id="07b35-133">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-134">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="07b35-134">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="07b35-135">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="07b35-135">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b35-136">/LOGU</span><span class="sxs-lookup"><span data-stu-id="07b35-136">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-137">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="07b35-137">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="07b35-138">Per la versione 4.6 SP2 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="07b35-138">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="07b35-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE | FALSE} {/GLOBAL}]</span><span class="sxs-lookup"><span data-stu-id="07b35-139">[/NO-UPDATE-FTA-SHORTCUT {TRUE|FALSE} {/GLOBAL}]</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-140">Se impostato su TRUE, viene creato un valore del registro di sistema per il pacchetto, per ogni utente o a livello globale, se è specificato il flag/GLOBAL.</span><span class="sxs-lookup"><span data-stu-id="07b35-140">If set to TRUE, a registry value is created for the package, either per user, or globally if the /GLOBAL flag is specified.</span></span></p>
<p><span data-ttu-id="07b35-141">Se impostato su FALSE, il valore del registro di sistema viene rimosso e le associazioni di tipi di file (FTA) per il pacchetto vengono reinstallate.</span><span class="sxs-lookup"><span data-stu-id="07b35-141">If set to FALSE, the registry value is removed and the file type associations (FTA) for the package are reinstalled.</span></span></p>
<p><span data-ttu-id="07b35-142">Se non specificato, si verifica un comportamento normale di FTA e di pubblicazione rapida.</span><span class="sxs-lookup"><span data-stu-id="07b35-142">If not specified, normal FTA and shortcut publishing behavior occurs.</span></span> <span data-ttu-id="07b35-143">Se si eseguono le operazioni successive di aggiornamento delle pubblicazioni nel client App-V 4,6 SP2, le scelte rapide e accordi per i pacchetti che hanno questo set di valori del registro di sistema non verranno modificate e i tasti di scelta rapida e accordi non verranno registrati all'avvio o all'accesso dell'utente, a meno che non si reimposti il contrassegno.</span><span class="sxs-lookup"><span data-stu-id="07b35-143">If you perform any subsequent publishing refresh operations on the App-V 4.6 SP2 client, the shortcuts and FTAs for packages that have this registry value set will not be changed, and the shortcuts and FTAs will not be registered at system startup or user login unless you reset the flag.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="07b35-144">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="07b35-144">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="07b35-145">Funziona in combinazione con il flag/NO-UPDATE-FTA-SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="07b35-145">Works in conjunction with the /NO-UPDATE-FTA-SHORTCUT flag.</span></span> <span data-ttu-id="07b35-146">Se il contrassegno/GLOBAL è presente, indica che verrà creato un valore del registro di sistema per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="07b35-146">If the /GLOBAL flag is present, it indicates that a registry value will be created for that package for all users.</span></span> <span data-ttu-id="07b35-147">Per impostazione predefinita, il valore del registro di sistema viene creato solo per l'utente.</span><span class="sxs-lookup"><span data-stu-id="07b35-147">By default, the registry value is created only for this user.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="07b35-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07b35-148">Related topics</span></span>


[<span data-ttu-id="07b35-149">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="07b35-149">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





