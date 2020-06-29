---
title: QUERY OBJ
description: QUERY OBJ
author: dansimp
ms.assetid: 55abf0d1-c779-4172-8357-552ab010933b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328e9feb96c70080531cbbc666d8ff1b86045ba5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815736"
---
# <span data-ttu-id="8f86e-103">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="8f86e-103">QUERY OBJ</span></span>


<span data-ttu-id="8f86e-104">Restituisce un elenco delimitato da tabulazioni di applicazioni correnti, pacchetti, associazioni di tipi di file o server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="8f86e-104">Returns a tab-delimited list of current applications, packages, file type associations, or publishing servers.</span></span>

`SFTMIME QUERY OBJ:{APP|PACKAGE|TYPE|SERVER} [/SHORT] [/GLOBAL]                 [/LOG log-pathname | /CONSOLE ]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8f86e-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="8f86e-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="8f86e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f86e-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8f86e-107">APP</span><span class="sxs-lookup"><span data-stu-id="8f86e-107">APP</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f86e-108">Restituisce un elenco di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8f86e-108">Returns a list of applications.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8f86e-109">PACCHETTO</span><span class="sxs-lookup"><span data-stu-id="8f86e-109">PACKAGE</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f86e-110">Restituisce un elenco di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8f86e-110">Returns a list of packages.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8f86e-111">TYPE</span><span class="sxs-lookup"><span data-stu-id="8f86e-111">TYPE</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f86e-112">Restituisce un elenco di associazioni di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="8f86e-112">Returns a list of file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8f86e-113">SERVER</span><span class="sxs-lookup"><span data-stu-id="8f86e-113">SERVER</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f86e-114">Restituisce un elenco di server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="8f86e-114">Returns a list of publishing servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8f86e-115">/SHORT</span><span class="sxs-lookup"><span data-stu-id="8f86e-115">/SHORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f86e-116">Senza visualizzare le proprietà complete di ognuna, restituisce un elenco di nomi di applicazioni, pacchetti, associazioni o nomi di server.</span><span class="sxs-lookup"><span data-stu-id="8f86e-116">Without displaying the full properties of each, returns a list of application names, packages, associations, or server names.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8f86e-117">/GLOBAL</span><span class="sxs-lookup"><span data-stu-id="8f86e-117">/GLOBAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f86e-118">Per le applicazioni, restituisce tutte le applicazioni note anziché solo quelle a cui l'utente corrente ha accesso.</span><span class="sxs-lookup"><span data-stu-id="8f86e-118">For applications, returns all known applications instead of only the ones the current user has access to.</span></span> <span data-ttu-id="8f86e-119">Per i pacchetti, restituisce tutti i pacchetti noti anziché solo quelli a cui l'utente corrente ha accesso.</span><span class="sxs-lookup"><span data-stu-id="8f86e-119">For packages, returns all known packages instead of only the ones the current user has access to.</span></span> <span data-ttu-id="8f86e-120">Per le associazioni, restituisce solo le associazioni che si applicano a tutti gli utenti, non quelli specifici dell'utente.</span><span class="sxs-lookup"><span data-stu-id="8f86e-120">For associations, returns only associations that apply to all users, not user-specific ones.</span></span> <span data-ttu-id="8f86e-121">Non valido per i server.</span><span class="sxs-lookup"><span data-stu-id="8f86e-121">Not valid for servers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8f86e-122">/LOG</span><span class="sxs-lookup"><span data-stu-id="8f86e-122">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f86e-123">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="8f86e-123">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8f86e-124">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="8f86e-124">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f86e-125">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="8f86e-125">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8f86e-126">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="8f86e-126">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8f86e-127">/LOGU</span><span class="sxs-lookup"><span data-stu-id="8f86e-127">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f86e-128">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="8f86e-128">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8f86e-129">**Nota**  Nella versione 4,6 è stata aggiunta una nuova colonna all'output della QUERY SFTMIME OBJ: APP \ [/GLOBAL\].</span><span class="sxs-lookup"><span data-stu-id="8f86e-129">**Note** In version 4.6, a new column has been added to the output of SFTMIME QUERY OBJ:APP \[/GLOBAL\].</span></span> <span data-ttu-id="8f86e-130">L'ultima colonna dell'output è un valore numerico che indica se un'applicazione viene pubblicata o meno.</span><span class="sxs-lookup"><span data-stu-id="8f86e-130">The last column of the output is a numeric value that indicates whether an application is published or not.</span></span>

<span data-ttu-id="8f86e-131">PUBLISHED = 1 indica che l'applicazione è stata pubblicata da un aggiornamento del server di pubblicazione, installando l'applicazione usando un file di Windows Installer (. MSI) oppure eseguendo un pacchetto di aggiunta di SFTMIME, configura il comando pacchetto o pubblica pacchetto usando un manifesto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="8f86e-131">PUBLISHED=1 means the application was published by a Publishing Server refresh, by installing the application by using a Windows Installer file (.MSI), or by running an SFTMIME ADD PACKAGE, CONFIGURE PACKAGE or PUBLISH PACKAGE command by using a package manifest.</span></span>

<span data-ttu-id="8f86e-132">PUBLISHED = 0 indica che l'applicazione non è stata pubblicata o non è più pubblicata come risultato dell'esecuzione di un'operazione Clear o dell'esecuzione di un comando SFTMIME UNPUBLISH.</span><span class="sxs-lookup"><span data-stu-id="8f86e-132">PUBLISHED=0 means the application has not been published or it is no longer published as a result of performing a Clear operation or running an SFTMIME UNPUBLISH command.</span></span>

<span data-ttu-id="8f86e-133">Se si usa il parametro/GLOBAL, lo stato pubblicato sarà 1 per le applicazioni pubblicate globalmente e 0 per le applicazioni pubblicate in contesti utente.</span><span class="sxs-lookup"><span data-stu-id="8f86e-133">If you use the /GLOBAL parameter, the PUBLISHED state will be 1 for applications that were published globally and 0 for those applications that were published under user contexts.</span></span> <span data-ttu-id="8f86e-134">Senza il parametro/GLOBAL, viene restituito uno stato pubblicato di 1 per le applicazioni pubblicate nel contesto dell'utente che esegue il comando e viene restituito uno stato di 0 per le applicazioni pubblicate globalmente.</span><span class="sxs-lookup"><span data-stu-id="8f86e-134">Without the /GLOBAL parameter, a PUBLISHED state of 1 is returned for applications published in the context of the user running the command, and a state of 0 is returned for those applications that are published globally.</span></span>

 

<span data-ttu-id="8f86e-135">Il comando SFTMIME QUERY OBJ può essere usato per richiedere informazioni su tutti gli oggetti visualizzati sopra: applicazioni, pacchetti, associazioni di tipi di file e server.</span><span class="sxs-lookup"><span data-stu-id="8f86e-135">The SFTMIME QUERY OBJ command can be used to query for information on all of the objects shown above—applications, packages, file type associations, and servers.</span></span><span data-ttu-id="8f86e-136">Per mostrare come usare il comando SFTMIME QUERY OBJ nelle normali attività operative, nell'esempio seguente viene illustrato il processo da seguire se si vuole impostare il valore del parametro OVERRIDEURL per un pacchetto specifico per specificare un nuovo percorso per il contenuto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="8f86e-136">To show how you might use the SFTMIME QUERY OBJ command in your normal operations tasks, the following example demonstrates the process you would follow if you wanted to set the OVERRIDEURL parameter value for a specific package to specify a new path to the package content.</span></span> 

1.  <span data-ttu-id="8f86e-137">Per trovare il pacchetto che si vuole configurare, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="8f86e-137">To find the package that you want to configure, run the following command:</span></span>

    `SFTMIME QUERY OBJ:PACKAGE`

    <span data-ttu-id="8f86e-138">Questo comando restituisce ogni nome di pacchetto individuato come GUID nella prima colonna di output, ad esempio {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span><span class="sxs-lookup"><span data-stu-id="8f86e-138">This command returns each discovered package name as a GUID in the first column of output—for example, {AF78ABE1-57D4-4297-89DE-C308684AEDD6}.</span></span>

2.  <span data-ttu-id="8f86e-139">Per impostare il valore del parametro OVERRIDEURL, è possibile usare il comando [Configura pacchetto](configure-package.md) di SFTMIME.</span><span class="sxs-lookup"><span data-stu-id="8f86e-139">To set the OVERRIDEURL parameter value, you use the SFTMIME [CONFIGURE PACKAGE](configure-package.md) command.</span></span> <span data-ttu-id="8f86e-140">Ad esempio, per impostare il valore di OVERRIDEURL per il pacchetto su un valore di *\\\\server\\share\\mypackage.SFT*, usa il comando SFTMIME Configura pacchetto e assegnagli il GUID del pacchetto selezionato dall'output del comando SFTMIME query obj nel passaggio 1, seguito dal parametro OVERRIDEURL e dal relativo nuovo valore, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8f86e-140">For example, to set the OVERRIDEURL value for this package to a value of *\\\\server\\share\\mypackage.sft*, use the SFTMIME CONFIGURE PACKAGE command and give it the selected package GUID from the output of the SFTMIME QUERY OBJ command in step 1, followed by the OVERRIDEURL parameter and its new value, as follows:</span></span>

    `SFTMIME CONFIGURE PACKAGE:"{AF78ABE1-57D4-4297-89DE-C308684AEDD6}" /OVERRIDEURL "\\\\server\\share\\mypackage.sft "`

<span data-ttu-id="8f86e-141">Per la versione 4.6 SP2 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="8f86e-141">For version4.6 SP2, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8f86e-142">/NO-UPDATE-FTA-SHORTCUT</span><span class="sxs-lookup"><span data-stu-id="8f86e-142">/NO-UPDATE-FTA-SHORTCUT</span></span></p></td>
<td align="left"><p><span data-ttu-id="8f86e-143">Indica lo stato corrente del flag/NO-UPDATE-FTA-SHORTCUT.</span><span class="sxs-lookup"><span data-stu-id="8f86e-143">Indicates the current state of the /NO-UPDATE-FTA-SHORTCUT flag.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="8f86e-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f86e-144">Related topics</span></span>


[<span data-ttu-id="8f86e-145">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="8f86e-145">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





