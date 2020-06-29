---
title: HELP
description: HELP
author: dansimp
ms.assetid: 0ddb5f18-0c0a-45ea-b7c7-2d4749e3d35d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 395e6199529ccbe708aa7d1ac6673ea6f9494ae4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821465"
---
# <span data-ttu-id="1ac82-103">HELP</span><span class="sxs-lookup"><span data-stu-id="1ac82-103">HELP</span></span>


<span data-ttu-id="1ac82-104">Visualizza le informazioni sui vari comandi di SFTMIME che possono essere usati in Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="1ac82-104">Displays information about the various SFTMIME commands that can be used in Application Virtualization (App-V).</span></span>

## <span data-ttu-id="1ac82-105">HELP</span><span class="sxs-lookup"><span data-stu-id="1ac82-105">HELP</span></span>


`SFTMIME [/? | /HELP [VERB:<verb>]]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1ac82-106">Parametro</span><span class="sxs-lookup"><span data-stu-id="1ac82-106">Parameter</span></span></th>
<th align="left"><span data-ttu-id="1ac82-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ac82-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-108">/?,/HELP</span><span class="sxs-lookup"><span data-stu-id="1ac82-108">/?, /HELP</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-109">Visualizza le informazioni sull'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="1ac82-109">Displays usage information.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ac82-110">verbo</span><span class="sxs-lookup"><span data-stu-id="1ac82-110">verb</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-111">Comando da eseguire, ad esempio Aggiungi, Aggiorna, guida o Rimuovi.</span><span class="sxs-lookup"><span data-stu-id="1ac82-111">The command to run, such as ADD, REFRESH, HELP or REMOVE.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-112">oggetto</span><span class="sxs-lookup"><span data-stu-id="1ac82-112">object</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-113">Il comando si applica a, ad esempio APP: &quot; applicazione predefinita.&quot;</span><span class="sxs-lookup"><span data-stu-id="1ac82-113">What the command applies to, such as APP:&quot;Default Application.&quot;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ac82-114">parametri</span><span class="sxs-lookup"><span data-stu-id="1ac82-114">parameters</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-115">Parametri facoltativi per il verbo e l'oggetto specificati.</span><span class="sxs-lookup"><span data-stu-id="1ac82-115">Optional parameters for the specified verb and object.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-116">/LOG</span><span class="sxs-lookup"><span data-stu-id="1ac82-116">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-117">Registrare l'output nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="1ac82-117">Log output to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ac82-118">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="1ac82-118">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-119">Visualizza l'output nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="1ac82-119">Displays output in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-120">/GUI</span><span class="sxs-lookup"><span data-stu-id="1ac82-120">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-121">Visualizza gli errori in una finestra di dialogo (non valido per le query).</span><span class="sxs-lookup"><span data-stu-id="1ac82-121">Displays errors in a dialog box (not valid for queries).</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1ac82-122">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="1ac82-122">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-123">/LOGU</span><span class="sxs-lookup"><span data-stu-id="1ac82-123">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-124">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="1ac82-124">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1ac82-125">Sono supportati i verbi descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1ac82-125">The verbs described in the following table are supported.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-126">ADD</span><span class="sxs-lookup"><span data-stu-id="1ac82-126">ADD</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-127">Aggiunge una nuova applicazione, un pacchetto, un'associazione di tipi di file o un server di pubblicazione al client App-V.</span><span class="sxs-lookup"><span data-stu-id="1ac82-127">Adds a new application, package, file type association, or publishing server to the App-V Client.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ac82-128">CONFIGURARE</span><span class="sxs-lookup"><span data-stu-id="1ac82-128">CONFIGURE</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-129">Modifica la configurazione di un'applicazione, di un pacchetto, di un'associazione di tipi di file o di un server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="1ac82-129">Changes the configuration of an application, a package, a file type association, or a publishing server.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-130">DELETE</span><span class="sxs-lookup"><span data-stu-id="1ac82-130">DELETE</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-131">Rimuove le applicazioni, i pacchetti, le associazioni di tipi di file o i server.</span><span class="sxs-lookup"><span data-stu-id="1ac82-131">Removes applications, packages, file type associations, or servers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ac82-132">CARICARE</span><span class="sxs-lookup"><span data-stu-id="1ac82-132">LOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-133">Carica un pacchetto nella cache del file System.</span><span class="sxs-lookup"><span data-stu-id="1ac82-133">Loads a package into the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-134">RIPRISTINARE</span><span class="sxs-lookup"><span data-stu-id="1ac82-134">REPAIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-135">Reimposta le impostazioni personali per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1ac82-135">Resets your personal settings for an application.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ac82-136">REFRESH</span><span class="sxs-lookup"><span data-stu-id="1ac82-136">REFRESH</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-137">Attiva un aggiornamento del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="1ac82-137">Triggers a publishing server refresh.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-138">PUBBLICARE</span><span class="sxs-lookup"><span data-stu-id="1ac82-138">PUBLISH</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-139">Pubblica un collegamento a un'applicazione nel menu Start, nel desktop o in un'altra posizione specificata dell'utente o può essere usato per pubblicare il contenuto di un intero pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1ac82-139">Publishes an application shortcut to the user's Start menu, desktop, or other specified location, or can be used to publish the contents of an entire package.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ac82-140">ANNULLARE la pubblicazione</span><span class="sxs-lookup"><span data-stu-id="1ac82-140">UNPUBLISH</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-141">Rimuove i tasti di scelta rapida e i tipi di file per un intero pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1ac82-141">Removes the shortcuts and file types for an entire package.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-142">QUERY</span><span class="sxs-lookup"><span data-stu-id="1ac82-142">QUERY</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-143">Ottiene un elenco corrente di applicazioni, pacchetti, associazioni di tipi di file o server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="1ac82-143">Gets a current list of applications, packages, file type associations, or publishing servers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ac82-144">CHIARO</span><span class="sxs-lookup"><span data-stu-id="1ac82-144">CLEAR</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-145">Rimuove le impostazioni personali e le configurazioni desktop per una o più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ac82-145">Removes your personal settings and desktop configurations for one or more applications.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-146">SCARICARE</span><span class="sxs-lookup"><span data-stu-id="1ac82-146">UNLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-147">Scarica un pacchetto dalla cache del file System.</span><span class="sxs-lookup"><span data-stu-id="1ac82-147">Unloads a package from the file system cache.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1ac82-148">BLOCCARE</span><span class="sxs-lookup"><span data-stu-id="1ac82-148">LOCK</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-149">Blocca l'applicazione specificata nella cache del file System.</span><span class="sxs-lookup"><span data-stu-id="1ac82-149">Locks the application specified in the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1ac82-150">SBLOCCARE</span><span class="sxs-lookup"><span data-stu-id="1ac82-150">UNLOCK</span></span></p></td>
<td align="left"><p><span data-ttu-id="1ac82-151">Sblocca l'applicazione specificata nella cache del file System.</span><span class="sxs-lookup"><span data-stu-id="1ac82-151">Unlocks the application specified in the file system cache.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1ac82-152">Per altre informazioni sulle azioni precedenti, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="1ac82-152">For more information about the preceding actions, use the following command:</span></span>

`SFTMIME /HELP VERB:verb`

<span data-ttu-id="1ac82-153">Ad esempio, il comando seguente visualizzerà le informazioni per il verbo di aggiunta:</span><span class="sxs-lookup"><span data-stu-id="1ac82-153">For example, the following command will display information for the ADD verb:</span></span>

`SFTMIME /HELP VERB:ADD`

## <span data-ttu-id="1ac82-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ac82-154">Related topics</span></span>


[<span data-ttu-id="1ac82-155">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="1ac82-155">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





