---
title: Pianificazione per l'uso del reindirizzamento delle cartelle con App-V
description: Pianificazione per l'uso del reindirizzamento delle cartelle con App-V
author: dansimp
ms.assetid: 2a4deeed-fdc0-465c-b88a-3a2fbbf27436
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b25b3531faa495275bf4e478389f44790d8eed9a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804935"
---
# <span data-ttu-id="57311-103">Pianificazione per l'uso del reindirizzamento delle cartelle con App-V</span><span class="sxs-lookup"><span data-stu-id="57311-103">Planning to Use Folder Redirection with App-V</span></span>


<span data-ttu-id="57311-104">App-V 5,0 SP2 supporta l'uso del reindirizzamento delle cartelle, una funzionalità che consente agli utenti e agli amministratori di reindirizzare il percorso di una cartella in una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="57311-104">App-V 5.0 SP2 supports the use of folder redirection, a feature that enables users and administrators to redirect the path of a folder to a new location.</span></span>

<span data-ttu-id="57311-105">Questo argomento contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="57311-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="57311-106">Requisiti per l'uso del reindirizzamento delle cartelle</span><span class="sxs-lookup"><span data-stu-id="57311-106">Requirements for using folder redirection</span></span>](#bkmk-folder-redir-reqs)

-   [<span data-ttu-id="57311-107">Come configurare il reindirizzamento delle cartelle per l'uso con App-V</span><span class="sxs-lookup"><span data-stu-id="57311-107">How to configure folder redirection for use with App-V</span></span>](#bkmk-folder-redir-cfg)

-   [<span data-ttu-id="57311-108">Funzionamento del reindirizzamento delle cartelle con App-V</span><span class="sxs-lookup"><span data-stu-id="57311-108">How folder redirection works with App-V</span></span>](#bkmk-folder-redir-works)

-   [<span data-ttu-id="57311-109">Panoramica del reindirizzamento delle cartelle</span><span class="sxs-lookup"><span data-stu-id="57311-109">Overview of folder redirection</span></span>](#bkmk-folder-redir-overview)

## <a href="" id="bkmk-folder-redir-reqs"></a><span data-ttu-id="57311-110">Requisiti e scenari non supportati per l'uso del reindirizzamento delle cartelle</span><span class="sxs-lookup"><span data-stu-id="57311-110">Requirements and unsupported scenarios for using folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57311-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57311-111">Requirements</span></span></p></td>
<td align="left"><p><span data-ttu-id="57311-112">Per usare il reindirizzamento delle cartelle% AppData%, è necessario:</span><span class="sxs-lookup"><span data-stu-id="57311-112">To use %AppData% folder redirection, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="57311-113">Avere un pacchetto di App-V che include una cartella di file system virtuale AppData.</span><span class="sxs-lookup"><span data-stu-id="57311-113">Have an App-V package that has an AppData virtual file system (VFS) folder.</span></span></p></li>
<li><p><span data-ttu-id="57311-114">Abilitare il reindirizzamento delle cartelle e reindirizzare le cartelle degli utenti a una cartella condivisa, in genere una cartella di rete.</span><span class="sxs-lookup"><span data-stu-id="57311-114">Enable folder redirection and redirect users’ folders to a shared folder, typically a network folder.</span></span></p></li>
<li><p><span data-ttu-id="57311-115">Eseguire il roaming sia o nessuna delle opzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="57311-115">Roam both or neither of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="57311-116">File in%appdata%\Microsoft\AppV\Client\Catalog</span><span class="sxs-lookup"><span data-stu-id="57311-116">Files under %appdata%\Microsoft\AppV\Client\Catalog</span></span></p></li>
<li><p><span data-ttu-id="57311-117">Impostazioni del registro di sistema in HKEY_CURRENT_USER \Software\Microsoft\AppV\Client\Packages</span><span class="sxs-lookup"><span data-stu-id="57311-117">Registry settings under HKEY_CURRENT_USER\Software\Microsoft\AppV\Client\Packages</span></span></p>
<p><span data-ttu-id="57311-118">Per altre informazioni, Vedi <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)"> pubblicazione delle applicazioni e interazione tra client </a> .</span><span class="sxs-lookup"><span data-stu-id="57311-118">For more detail, see <a href="application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs" data-raw-source="[Application Publishing and Client Interaction](application-publishing-and-client-interaction.md#bkmk-clt-inter-roam-reqs)">Application Publishing and Client Interaction</a>.</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="57311-119">Verificare che le cartelle seguenti siano disponibili per ogni utente che accede al computer in cui è in uso il client App-V 5,0 SP2 o versione successiva:</span><span class="sxs-lookup"><span data-stu-id="57311-119">Ensure that the following folders are available to each user who logs into the computer that is running the App-V 5.0 SP2 or later client:</span></span></p>
<ul>
<li><p><span data-ttu-id="57311-120">% AppData% è configurato per il percorso di rete desiderato (con o senza <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)"> supporto per i file offline </a> ).</span><span class="sxs-lookup"><span data-stu-id="57311-120">%AppData% is configured to the desired network location (with or without <a href="https://technet.microsoft.com/library/cc780552.aspx" data-raw-source="[Offline Files](https://technet.microsoft.com/library/cc780552.aspx)">Offline Files</a> support).</span></span></p></li>
<li><p><span data-ttu-id="57311-121">% LocalAppData% è configurato nella cartella locale desiderata.</span><span class="sxs-lookup"><span data-stu-id="57311-121">%LocalAppData% is configured to the desired local folder.</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57311-122">Scenari non supportati</span><span class="sxs-lookup"><span data-stu-id="57311-122">Unsupported scenarios</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="57311-123">Configurazione di% LocalAppData% come unità di rete.</span><span class="sxs-lookup"><span data-stu-id="57311-123">Configuring %LocalAppData% as a network drive.</span></span></p></li>
<li><p><span data-ttu-id="57311-124">Reindirizzamento del menu Start a una singola cartella per più utenti.</span><span class="sxs-lookup"><span data-stu-id="57311-124">Redirecting the Start menu to a single folder for multiple users.</span></span></p></li>
<li><p><span data-ttu-id="57311-125">Se il roaming AppData (% AppData%) viene reindirizzato a una condivisione di rete non disponibile, le applicazioni App-V non verranno avviate nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="57311-125">If roaming AppData (%AppData%) is redirected to a network share that is not available, App-V applications will fail to launch as follows:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57311-126">Versione App-V</span><span class="sxs-lookup"><span data-stu-id="57311-126">App-V version</span></span></th>
<th align="left"><span data-ttu-id="57311-127">Descrizione scenario</span><span class="sxs-lookup"><span data-stu-id="57311-127">Scenario description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57311-128">In App-V 5,0 tramite App-V 5,0 SP2 Plus hotfix</span><span class="sxs-lookup"><span data-stu-id="57311-128">In App-V 5.0 through App-V 5.0 SP2 plus hotfixes</span></span></p></td>
<td align="left"><p><span data-ttu-id="57311-129">Questo errore si verificherà indipendentemente dal fatto che i file offline siano abilitati.</span><span class="sxs-lookup"><span data-stu-id="57311-129">This failure will occur regardless of whether Offline Files is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57311-130">In App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="57311-130">In App-V 5.0 SP3</span></span></p></td>
<td align="left"><p><span data-ttu-id="57311-131">Se la condivisione di rete non disponibile è stata abilitata per i file offline, l'applicazione App-V verrà avviata correttamente.</span><span class="sxs-lookup"><span data-stu-id="57311-131">If the unavailable network share has been enabled for Offline Files, the App-V application will start successfully.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-cfg"></a><span data-ttu-id="57311-132">Come configurare il reindirizzamento delle cartelle per l'uso con App-V</span><span class="sxs-lookup"><span data-stu-id="57311-132">How to configure folder redirection for use with App-V</span></span>


<span data-ttu-id="57311-133">Il reindirizzamento delle cartelle può essere applicato a cartelle diverse, ad esempio desktop, documenti personali, immagini personali e così via. Tuttavia, l'unica cartella che influisce sull'uso delle applicazioni App-V è la cartella AppData Roaming dell'utente (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="57311-133">Folder redirection can be applied to different folders, such as Desktop, My Documents, My Pictures, etc. However, the only folder that impacts the use of App-V applications is the user’s roaming AppData folder (%AppData%).</span></span> <span data-ttu-id="57311-134">Puoi applicare il reindirizzamento delle cartelle a qualsiasi altra cartella supportata senza influire su App-V.</span><span class="sxs-lookup"><span data-stu-id="57311-134">You can apply folder redirection to any other supported folders without impacting App-V.</span></span>

## <a href="" id="bkmk-folder-redir-works"></a><span data-ttu-id="57311-135">Funzionamento del reindirizzamento delle cartelle con App-V</span><span class="sxs-lookup"><span data-stu-id="57311-135">How folder redirection works with App-V</span></span>


<span data-ttu-id="57311-136">La tabella seguente descrive il funzionamento del reindirizzamento delle cartelle quando% AppData% viene reindirizzato a una rete e dopo aver soddisfatto i requisiti elencati in precedenza in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="57311-136">The following table describes how folder redirection works when %AppData% is redirected to a network and when you have met the requirements listed earlier in this article.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="57311-137">Stato ambiente virtuale</span><span class="sxs-lookup"><span data-stu-id="57311-137">Virtual environment state</span></span></th>
<th align="left"><span data-ttu-id="57311-138">Azione che si verifica</span><span class="sxs-lookup"><span data-stu-id="57311-138">Action that occurs</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57311-139">Quando l'ambiente virtuale viene avviato</span><span class="sxs-lookup"><span data-stu-id="57311-139">When the virtual environment starts</span></span></p></td>
<td align="left"><p><span data-ttu-id="57311-140">La cartella AppData di Virtual File System (VFS) viene mappata alla cartella AppData locale (% LocalAppData%) invece della cartella AppData mobile dell'utente (% AppData%).</span><span class="sxs-lookup"><span data-stu-id="57311-140">The virtual file system (VFS) AppData folder is mapped to the local AppData folder (%LocalAppData%) instead of to the user’s roaming AppData folder (%AppData%).</span></span></p>
<ul>
<li><p><span data-ttu-id="57311-141">LocalAppData contiene una cache locale della cartella AppData mobile dell'utente per il pacchetto in uso.</span><span class="sxs-lookup"><span data-stu-id="57311-141">LocalAppData contains a local cache of the user’s roaming AppData folder for the package in use.</span></span> <span data-ttu-id="57311-142">La cache locale si trova in:</span><span class="sxs-lookup"><span data-stu-id="57311-142">The local cache is located under:</span></span></p>
<p><code>%LocalAppData%\Microsoft\AppV\Client\VFS\PackageGUID\AppData</code></p></li>
<li><p><span data-ttu-id="57311-143">Gli ultimi dati della cartella AppData Roaming dell'utente vengono copiati e sostituiti dai dati attualmente presenti nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="57311-143">The latest data from the user’s roaming AppData folder is copied to and replaces the data currently in the local cache.</span></span></p></li>
<li><p><span data-ttu-id="57311-144">Mentre l'ambiente virtuale è in esecuzione, i dati continueranno a essere salvati nella cache locale.</span><span class="sxs-lookup"><span data-stu-id="57311-144">While the virtual environment is running, data continues to be saved to the local cache.</span></span> <span data-ttu-id="57311-145">I dati vengono serviti solo in% LocalAppData% e non vengono spostati o sincronizzati con% AppData% fino a quando l'utente finale non arresta il computer.</span><span class="sxs-lookup"><span data-stu-id="57311-145">Data is served only out of %LocalAppData% and is not moved or synchronized with %AppData% until the end user shuts down the computer.</span></span></p></li>
<li><p><span data-ttu-id="57311-146">Le voci nella cartella AppData vengono effettuate usando il contesto utente e non il contesto di sistema.</span><span class="sxs-lookup"><span data-stu-id="57311-146">Entries to the AppData folder are made using the user context, not the system context.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="57311-147">Nota</span><span class="sxs-lookup"><span data-stu-id="57311-147">Note</span></span></strong><br/><p><span data-ttu-id="57311-148">Il reindirizzamento delle cartelle client App-V a volte non riesce a trasferire i file da% AppData% a% LocalAppData%.</span><span class="sxs-lookup"><span data-stu-id="57311-148">The App-V client folder redirection sometimes fails to move files from %AppData% to %LocalAppData%.</span></span> <span data-ttu-id="57311-149">Vedere <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)"> Note sulla versione per App-V 5,0 SP2 </a> .</span><span class="sxs-lookup"><span data-stu-id="57311-149">See <a href="release-notes-for-app-v-50-sp2.md#bkmk-folderredirection" data-raw-source="[Release Notes for App-V 5.0 SP2](release-notes-for-app-v-50-sp2.md#bkmk-folderredirection)">Release Notes for App-V 5.0 SP2</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57311-150">Quando l'ambiente virtuale si arresta</span><span class="sxs-lookup"><span data-stu-id="57311-150">When the virtual environment shuts down</span></span></p></td>
<td align="left"><p><span data-ttu-id="57311-151">I dati memorizzati nella cache locale in AppData (roaming) vengono compressi e copiati nella cartella AppData di roaming "reale" in% AppData%.</span><span class="sxs-lookup"><span data-stu-id="57311-151">The local cached data in AppData (roaming) is zipped up and copied to the “real” roaming AppData folder in %AppData%.</span></span> <span data-ttu-id="57311-152">Un indicatore di data e ora, che indica l'ultimo caricamento noto, viene salvato contemporaneamente come chiave del registro di sistema in:</span><span class="sxs-lookup"><span data-stu-id="57311-152">A time stamp, which indicates the last known upload, is simultaneously saved as a registry key under:</span></span></p>
<p><code>HKCU\Software\Microsoft\AppV\Client\Packages&amp;lt;PACKAGE_GUID&gt;\AppDataTime</code></p>
<p><span data-ttu-id="57311-153">Per ottenere la ridondanza, App-V 5,0 mantiene le tre copie più recenti dei dati compressi in% AppData%.</span><span class="sxs-lookup"><span data-stu-id="57311-153">To provide redundancy, App-V 5.0 keeps the three most recent copies of the compressed data under %AppData%.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-folder-redir-overview"></a><span data-ttu-id="57311-154">Panoramica del reindirizzamento delle cartelle</span><span class="sxs-lookup"><span data-stu-id="57311-154">Overview of folder redirection</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57311-155">Scopo</span><span class="sxs-lookup"><span data-stu-id="57311-155">Purpose</span></span></p></td>
<td align="left"><p><span data-ttu-id="57311-156">Consente agli utenti finali di lavorare con i file, che sono stati reindirizzati a un'altra cartella, come se i file fossero ancora presenti nell'unità locale.</span><span class="sxs-lookup"><span data-stu-id="57311-156">Enables end users to work with files, which have been redirected to another folder, as if the files still existed on the local drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57311-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57311-157">Description</span></span></p></td>
<td align="left"><p><span data-ttu-id="57311-158">Il reindirizzamento delle cartelle consente agli utenti e agli amministratori di reindirizzare il percorso di una cartella a un percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="57311-158">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="57311-159">I documenti nella cartella sono disponibili per l'utente da qualsiasi computer della rete.</span><span class="sxs-lookup"><span data-stu-id="57311-159">The documents in the folder are available to the user from any computer on the network.</span></span></p>
<ul>
<li><p><span data-ttu-id="57311-160">Il reindirizzamento delle cartelle consente agli utenti e agli amministratori di reindirizzare il percorso di una cartella a un percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="57311-160">Folder redirection allows users and administrators to redirect the path of a folder to a network location.</span></span> <span data-ttu-id="57311-161">I documenti nella cartella sono disponibili per l'utente da qualsiasi computer della rete.</span><span class="sxs-lookup"><span data-stu-id="57311-161">The documents in the folder are available to the user from any computer on the network.</span></span></p></li>
<li><p><span data-ttu-id="57311-162">Il nuovo percorso può essere una cartella nel computer locale o una cartella in una rete condivisa.</span><span class="sxs-lookup"><span data-stu-id="57311-162">The new location can be a folder on the local computer or a folder on a shared network.</span></span></p></li>
<li><p><span data-ttu-id="57311-163">Il reindirizzamento delle cartelle aggiorna immediatamente i file, mentre i dati mobili vengono in genere sincronizzati quando l'utente accede o disconnette.</span><span class="sxs-lookup"><span data-stu-id="57311-163">Folder redirection updates the files immediately, whereas roaming data is typically synchronized when the user logs in or logs off.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="57311-164">Esempio di utilizzo</span><span class="sxs-lookup"><span data-stu-id="57311-164">Usage example</span></span></p></td>
<td align="left"><p><span data-ttu-id="57311-165">È possibile reindirizzare la cartella documenti, che in genere viene archiviata nel disco rigido locale del computer&#39;s, in un percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="57311-165">You can redirect the Documents folder, which is usually stored on the computer&#39;s local hard disk, to a network location.</span></span> <span data-ttu-id="57311-166">L'utente può accedere ai documenti nella cartella da qualsiasi computer della rete.</span><span class="sxs-lookup"><span data-stu-id="57311-166">The user can access the documents in the folder from any computer on the network.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="57311-167">Altre risorse</span><span class="sxs-lookup"><span data-stu-id="57311-167">More resources</span></span></p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/cc778976.aspx" data-raw-source="[Folder redirection overview](https://technet.microsoft.com/library/cc778976.aspx)"><span data-ttu-id="57311-168">Panoramica del reindirizzamento delle cartelle</span><span class="sxs-lookup"><span data-stu-id="57311-168">Folder redirection overview</span></span></a></p></td>
</tr>
</tbody>
</table>
















