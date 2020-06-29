---
title: Autorizzazioni di accesso utente in Application Virtualization Client
description: Autorizzazioni di accesso utente in Application Virtualization Client
author: dansimp
ms.assetid: 7459374c-810c-45e3-b205-fdd1f8514f80
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083faffb48aa58a0ee0c81b58fae307e53548b8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815116"
---
# <span data-ttu-id="7faab-103">Autorizzazioni di accesso utente in Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="7faab-103">User Access Permissions in Application Virtualization Client</span></span>


<span data-ttu-id="7faab-104">Nella scheda **autorizzazioni** della finestra di dialogo **Proprietà** , accessibile facendo clic con il pulsante destro del mouse sul nodo **Application Virtualization** in Application Virtualization Client Management Console, gli amministratori possono concedere agli utenti le autorizzazioni per l'utilizzo delle varie funzioni client.</span><span class="sxs-lookup"><span data-stu-id="7faab-104">On the **Permissions** tab on the **Properties** dialog box, accessible by right-clicking the **Application Virtualization** node in the Application Virtualization Client Management Console, administrators can grant users permissions to use the various client functions.</span></span>

<span data-ttu-id="7faab-105">**Nota**  Prima di modificare le autorizzazioni degli utenti, verificare che le modifiche apportate alle autorizzazioni siano coerenti con le linee guida dell'organizzazione per la concessione delle autorizzazioni utente.</span><span class="sxs-lookup"><span data-stu-id="7faab-105">**Note** Before changing users permissions, ensure that any permissions changes are consistent with the organization's guidelines for granting user permissions.</span></span>

 

<span data-ttu-id="7faab-106">La tabella seguente elenca e descrive le autorizzazioni che possono essere concesse agli utenti.</span><span class="sxs-lookup"><span data-stu-id="7faab-106">The following table lists and describes the permissions that can be granted to users.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7faab-107">Nome autorizzazione</span><span class="sxs-lookup"><span data-stu-id="7faab-107">Permission Name</span></span></th>
<th align="left"><span data-ttu-id="7faab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7faab-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7faab-109">Aggiungere applicazioni</span><span class="sxs-lookup"><span data-stu-id="7faab-109">Add applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-110">Registrare nuove applicazioni passando un nuovo file OSD al client usando sfttray.exe, sftmime.exe o MMC.</span><span class="sxs-lookup"><span data-stu-id="7faab-110">Register new applications by passing a new OSD file to the client by using sfttray.exe, sftmime.exe or the MMC.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7faab-111">Modificare le dimensioni della cache del file System</span><span class="sxs-lookup"><span data-stu-id="7faab-111">Change file system cache size</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-112">Aumentare le dimensioni della cache del file System.</span><span class="sxs-lookup"><span data-stu-id="7faab-112">Increase the size of the file system cache.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7faab-113">Cambiare l'unità del file System</span><span class="sxs-lookup"><span data-stu-id="7faab-113">Change file system drive</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-114">Selezionare una lettera di unità preferita diversa per il file System.</span><span class="sxs-lookup"><span data-stu-id="7faab-114">Select a different preferred drive letter for the file system.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7faab-115">Modificare le impostazioni del log</span><span class="sxs-lookup"><span data-stu-id="7faab-115">Change log settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-116">Modificare il livello di log o il percorso del log per il file di log del client.</span><span class="sxs-lookup"><span data-stu-id="7faab-116">Change the log level or the log path for the client log file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7faab-117">Modificare i file OSD</span><span class="sxs-lookup"><span data-stu-id="7faab-117">Change OSD files</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-118">Modificare i file OSD per le applicazioni registrate e passarli al client.</span><span class="sxs-lookup"><span data-stu-id="7faab-118">Modify OSD files for registered applications and pass them into the client.</span></span> <span data-ttu-id="7faab-119">Questo non ha alcun effetto sull'aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="7faab-119">This does not affect publishing refresh.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7faab-120">Cancellare le impostazioni dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="7faab-120">Clear application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-121">Eliminare tipi di file, tasti di scelta rapida e qualsiasi configurazione per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="7faab-121">Delete file types, shortcuts and any configurations for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7faab-122">Eliminare le applicazioni</span><span class="sxs-lookup"><span data-stu-id="7faab-122">Delete applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-123">Rimuovere tutti i riferimenti a un'applicazione dal file System e dalla cache OSD per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="7faab-123">Remove all references to an application from the file system and OSD cache for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7faab-124">Importare applicazioni nella cache</span><span class="sxs-lookup"><span data-stu-id="7faab-124">Import applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-125">Caricare i dati dell'applicazione direttamente da un file SFT specificato nella cache del file System.</span><span class="sxs-lookup"><span data-stu-id="7faab-125">Load application data directly from a specified SFT file into the file system cache.</span></span> <span data-ttu-id="7faab-126">Questo problema interessa tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="7faab-126">This affects all users.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7faab-127">Caricare le applicazioni nella cache</span><span class="sxs-lookup"><span data-stu-id="7faab-127">Load applications into the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-128">Avviare un caricamento del file SFT per un'applicazione dall'origine configurata, ad esempio un App-V Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="7faab-128">Start a load of the SFT file for an application from the configured source, such as an App-V Streaming Server.</span></span> <span data-ttu-id="7faab-129">In questo articolo viene caricata l'applicazione per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="7faab-129">This loads the application for all users on the computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7faab-130">Bloccare e sbloccare le applicazioni nella cache</span><span class="sxs-lookup"><span data-stu-id="7faab-130">Lock and unlock applications in the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-131">Impedire o consentire la scaricamento delle applicazioni dalla cache del file System.</span><span class="sxs-lookup"><span data-stu-id="7faab-131">Prevent or allow applications from being unloaded from the file system cache.</span></span> <span data-ttu-id="7faab-132">Questo problema interessa tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="7faab-132">This affects all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7faab-133">Gestire le associazioni di tipi di file</span><span class="sxs-lookup"><span data-stu-id="7faab-133">Manage file type associations</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-134">Aggiungere, modificare o eliminare associazioni di tipi di file solo per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="7faab-134">Add, modify, or delete file type associations for the current user only.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7faab-135">Gestire le impostazioni di aggiornamento della pubblicazione</span><span class="sxs-lookup"><span data-stu-id="7faab-135">Manage publishing refresh settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-136">Modificare le impostazioni che controllano l'intervallo di pubblicazione degli aggiornamenti per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="7faab-136">Change settings that control the timing of publishing refreshes for all users on the computer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7faab-137">Gestire i server di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="7faab-137">Manage publishing servers</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-138">Aggiungere, modificare o eliminare i server di pubblicazione per tutti gli utenti del computer.</span><span class="sxs-lookup"><span data-stu-id="7faab-138">Add, modify, or delete publishing servers for all users on the computer.</span></span> <span data-ttu-id="7faab-139">Questa autorizzazione include implicitamente le autorizzazioni per la gestione delle impostazioni di aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="7faab-139">This permission implicitly includes permission to manage publishing refresh settings.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7faab-140">Pubblicare i tasti di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="7faab-140">Publish shortcuts</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-141">Creare nuovi collegamenti alle applicazioni registrate.</span><span class="sxs-lookup"><span data-stu-id="7faab-141">Create new shortcuts to registered applications.</span></span> <span data-ttu-id="7faab-142">L'utente deve anche avere l'autorizzazione per creare file nel file system locale.</span><span class="sxs-lookup"><span data-stu-id="7faab-142">The user must also have permission to create files in the local file system.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7faab-143">Ripristinare le applicazioni</span><span class="sxs-lookup"><span data-stu-id="7faab-143">Repair applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-144">Rimuovere le configurazioni specifiche dell'applicazione per l'utente corrente senza rimuovere i collegamenti o le associazioni di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="7faab-144">Remove application specific configurations for the current user without removing shortcuts or file type associations.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7faab-145">Avviare un aggiornamento della pubblicazione</span><span class="sxs-lookup"><span data-stu-id="7faab-145">Start a publishing refresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-146">Avviare un aggiornamento della pubblicazione non pianificato per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="7faab-146">Start an unscheduled publishing refresh for the current user.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7faab-147">Attivare o disattivare la modalità offline</span><span class="sxs-lookup"><span data-stu-id="7faab-147">Toggle offline mode</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-148">Cambiare l'intero client dalla modalità online a quella offline per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="7faab-148">Change the entire client from online to offline mode for all users.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7faab-149">Scaricare le applicazioni dalla cache</span><span class="sxs-lookup"><span data-stu-id="7faab-149">Unload applications from the cache</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-150">Cancellare i dati dell'applicazione dalla cache del file System per tutti gli utenti senza rimuovere le impostazioni specifiche per l'utente, i collegamenti o le associazioni di tipi di file.</span><span class="sxs-lookup"><span data-stu-id="7faab-150">Clear application data from the file system cache for all users without removing user-specific settings, shortcuts, or file type associations.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7faab-151">Visualizzare tutte le applicazioni</span><span class="sxs-lookup"><span data-stu-id="7faab-151">View all applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="7faab-152">Consentire all'utente di visualizzare le applicazioni virtuali per tutti gli utenti registrati nel computer.</span><span class="sxs-lookup"><span data-stu-id="7faab-152">Allow the user to see the virtual applications for all users registered on the computer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="7faab-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7faab-153">Related topics</span></span>


[<span data-ttu-id="7faab-154">Come modificare le autorizzazioni di accesso utente</span><span class="sxs-lookup"><span data-stu-id="7faab-154">How to Change User Access Permissions</span></span>](how-to-change-user-access-permissions.md)

 

 





