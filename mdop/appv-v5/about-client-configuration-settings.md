---
title: Informazioni sulle impostazioni di configurazione client
description: Informazioni sulle impostazioni di configurazione client
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806105"
---
# <span data-ttu-id="b9cbb-103">Informazioni sulle impostazioni di configurazione client</span><span class="sxs-lookup"><span data-stu-id="b9cbb-103">About Client Configuration Settings</span></span>


<span data-ttu-id="b9cbb-104">Il client di Microsoft Application Virtualization (App-V) 5,0 archivia la configurazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-104">The Microsoft Application Virtualization (App-V) 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="b9cbb-105">Se si conosce il formato dei dati nel registro di sistema, è possibile raccogliere informazioni utili sul client.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="b9cbb-106">È anche possibile configurare molte azioni client modificando le voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="b9cbb-107">Questo argomento elenca le impostazioni di configurazione del client App-V 5,0 e spiega i loro usi.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-107">This topic lists the App-V 5.0 Client configuration settings and explains their uses.</span></span> <span data-ttu-id="b9cbb-108">È possibile usare PowerShell per modificare le impostazioni di configurazione del client.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-108">You can use PowerShell to modify the client configuration settings.</span></span> <span data-ttu-id="b9cbb-109">Per altre informazioni sull'uso di PowerShell e App-V 5,0, vedere [amministrazione di App-v tramite PowerShell](administering-app-v-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="b9cbb-109">For more information about using PowerShell and App-V 5.0 see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> <span data-ttu-id="b9cbb-110">Impostazioni di configurazione client App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="b9cbb-110">App-V 5.0 Client Configuration Settings</span></span>


<span data-ttu-id="b9cbb-111">La tabella seguente mostra le informazioni sulle impostazioni di configurazione del client App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="b9cbb-111">The following table displays information about the App-V 5.0 client configuration settings:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b9cbb-112">Impostazione del nome</span><span class="sxs-lookup"><span data-stu-id="b9cbb-112">Setting Name</span></span></th>
<th align="left"><span data-ttu-id="b9cbb-113">Contrassegno imposta</span><span class="sxs-lookup"><span data-stu-id="b9cbb-113">Setup Flag</span></span></th>
<th align="left"><span data-ttu-id="b9cbb-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9cbb-114">Description</span></span></th>
<th align="left"><span data-ttu-id="b9cbb-115">Opzioni di impostazione</span><span class="sxs-lookup"><span data-stu-id="b9cbb-115">Setting Options</span></span></th>
<th align="left"><span data-ttu-id="b9cbb-116">Valore della chiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b9cbb-116">Registry Key Value</span></span></th>
<th align="left"><span data-ttu-id="b9cbb-117">Chiavi e valori di stato dei criteri disabilitati</span><span class="sxs-lookup"><span data-stu-id="b9cbb-117">Disabled Policy State Keys and Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-118">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="b9cbb-118">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-119">PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="b9cbb-119">PACKAGEINSTALLATIONROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-120">Specifica la directory in cui verranno installate tutte le nuove applicazioni e gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-120">Specifies directory where all new applications and updates will be installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-121">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-121">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-122">Streaming\PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="b9cbb-122">Streaming\PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-123">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-123">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-124">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="b9cbb-124">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-125">PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="b9cbb-125">PACKAGESOURCEROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-126">Sostituisce la posizione di origine per scaricare il contenuto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-126">Overrides source location for downloading package content.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-127">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-127">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-128">Streaming\PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="b9cbb-128">Streaming\PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-129">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-129">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-130">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="b9cbb-130">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-131">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-131">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-132">Questa impostazione controlla se le applicazioni virtualizzate vengono avviate in computer con Windows 8 collegati tramite una connessione di rete a consumo (ad esempio 4G).</span><span class="sxs-lookup"><span data-stu-id="b9cbb-132">This setting controls whether virtualized applications are launched on Windows 8 machines connected via a metered network connection (For example, 4G).</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-133">True (abilitato); False (stato disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-133">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-134">Streaming\AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="b9cbb-134">Streaming\AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-135">0</span><span class="sxs-lookup"><span data-stu-id="b9cbb-135">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-136">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="b9cbb-136">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-137">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-137">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-138">Specifica il numero di tentativi di una sessione eliminata.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-138">Specifies the number of times to retry a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-139">Numero intero (0-99)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-139">Integer (0-99)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-140">Streaming\ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="b9cbb-140">Streaming\ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-141">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-141">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-142">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="b9cbb-142">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-143">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-143">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-144">Specifica il numero di secondi tra i tentativi di ristabilire una sessione eliminata.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-144">Specifies the number of seconds between attempts to reestablish a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-145">Numero intero (0-3600)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-145">Integer (0-3600)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-146">Streaming\ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="b9cbb-146">Streaming\ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-147">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-147">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-148">AutoLoad</span><span class="sxs-lookup"><span data-stu-id="b9cbb-148">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-149">AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="b9cbb-149">AUTOLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-150">Specifica il modo in cui i nuovi pacchetti devono essere caricati automaticamente da App-V in un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-150">Specifies how new packages should be loaded automatically by App-V on a specific computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-151">(0x0) None; (0x1) usato in precedenza; (0x2) tutti</span><span class="sxs-lookup"><span data-stu-id="b9cbb-151">(0x0) None; (0x1) Previously used; (0x2) All</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-152">Streaming\AutoLoad</span><span class="sxs-lookup"><span data-stu-id="b9cbb-152">Streaming\AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-153">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-153">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-154">LocationProvider</span><span class="sxs-lookup"><span data-stu-id="b9cbb-154">LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-155">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-155">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-156">Specifica il CLSID per un'implementazione compatibile dell'interfaccia IAppvPackageLocationProvider.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-156">Specifies the CLSID for a compatible implementation of the IAppvPackageLocationProvider interface.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-157">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-157">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-158">Streaming\LocationProvider</span><span class="sxs-lookup"><span data-stu-id="b9cbb-158">Streaming\LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-159">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-159">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-160">CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="b9cbb-160">CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-161">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-161">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-162">Specifica il percorso di un certificato valido nell'archivio certificati.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-162">Specifies the path to a valid certificate in the certificate store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-163">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-163">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-164">Streaming\CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="b9cbb-164">Streaming\CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-165">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-165">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-166">VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="b9cbb-166">VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-167">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-167">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-168">Verifica lo stato di revoca del certificato del server prima della vaporizzazione tramite HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-168">Verifies Server certificate revocation status before steaming using HTTPS.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-169">True (abilitato); False (stato disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-169">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-170">Streaming\VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="b9cbb-170">Streaming\VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-171">0</span><span class="sxs-lookup"><span data-stu-id="b9cbb-171">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-172">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="b9cbb-172">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-173">SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="b9cbb-173">SHAREDCONTENTSTOREMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-174">Specifica che il contenuto del pacchetto in streaming non verrà salvato nel disco rigido locale.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-174">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-175">True (abilitato); False (stato disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-175">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-176">Streaming\SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="b9cbb-176">Streaming\SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-177">0</span><span class="sxs-lookup"><span data-stu-id="b9cbb-177">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-178">Nome</span><span class="sxs-lookup"><span data-stu-id="b9cbb-178">Name</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-179">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-179">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-180">Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-180">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b9cbb-181">Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-181">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-182">PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="b9cbb-182">PUBLISHINGSERVERNAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-183">Visualizza il nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-183">Displays the name of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-184">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-184">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-185">Publishing\Servers {serverId} \ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b9cbb-185">Publishing\Servers{serverId}\FriendlyName</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-186">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-186">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-187">URL</span><span class="sxs-lookup"><span data-stu-id="b9cbb-187">URL</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-188">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-188">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-189">Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-189">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b9cbb-190">Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-190">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-191">PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="b9cbb-191">PUBLISHINGSERVERURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-192">Visualizza l'URL del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-192">Displays the URL of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-193">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-193">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-194">Publishing\Servers {serverId} \ URL</span><span class="sxs-lookup"><span data-stu-id="b9cbb-194">Publishing\Servers{serverId}\URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-195">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-195">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-196">GlobalRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="b9cbb-196">GlobalRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-197">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-197">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-198">Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-198">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b9cbb-199">Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-199">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-200">GLOBALREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="b9cbb-200">GLOBALREFRESHENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-201">Abilita l'aggiornamento della pubblicazione globale (booleano)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-201">Enables global publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-202">True (abilitato); False (stato disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-202">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-203">Publishing\Servers {serverId} \ GlobalEnabled</span><span class="sxs-lookup"><span data-stu-id="b9cbb-203">Publishing\Servers{serverId}\GlobalEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-204">False</span><span class="sxs-lookup"><span data-stu-id="b9cbb-204">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-205">GlobalRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="b9cbb-205">GlobalRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-206">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-206">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-207">Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-207">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b9cbb-208">Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-208">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-209">GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="b9cbb-209">GLOBALREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-210">Attiva un aggiornamento della pubblicazione globale all'accesso.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-210">Triggers a global publishing refresh on logon.</span></span> <span data-ttu-id="b9cbb-211">Boolean</span><span class="sxs-lookup"><span data-stu-id="b9cbb-211">( Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-212">True (abilitato); False (stato disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-212">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-213">Publishing\Servers {serverId} \ GlobalLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="b9cbb-213">Publishing\Servers{serverId}\GlobalLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-214">False</span><span class="sxs-lookup"><span data-stu-id="b9cbb-214">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-215">GlobalRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b9cbb-215">GlobalRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-216">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-216">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-217">Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-217">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b9cbb-218">Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-218">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-219">GLOBALREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="b9cbb-219">GLOBALREFRESHINTERVAL</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="b9cbb-220">Specifica l'intervallo di aggiornamento della pubblicazione con GlobalRefreshIntervalUnit.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-220">Specifies the publishing refresh interval using the GlobalRefreshIntervalUnit.</span></span> <span data-ttu-id="b9cbb-221">Per disabilitare l'aggiornamento del pacchetto, selezionare 0.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-221">To disable package refresh, select 0.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-222">Numero intero (0-744</span><span class="sxs-lookup"><span data-stu-id="b9cbb-222">Integer (0-744</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-223">Publishing\Servers {serverId} \ GlobalPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b9cbb-223">Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-224">0</span><span class="sxs-lookup"><span data-stu-id="b9cbb-224">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-225">GlobalRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b9cbb-225">GlobalRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-226">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-226">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-227">Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-227">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b9cbb-228">Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-228">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-229">GLOBALREFRESHINTERVALUNI</span><span class="sxs-lookup"><span data-stu-id="b9cbb-229">GLOBALREFRESHINTERVALUNI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-230">Specifica l'unità di intervallo (ora 0-23, giorno 0-31).</span><span class="sxs-lookup"><span data-stu-id="b9cbb-230">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="b9cbb-231">0 per ora, 1 per giorno</span><span class="sxs-lookup"><span data-stu-id="b9cbb-231">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-232">Publishing\Servers {serverId} \ GlobalPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b9cbb-232">Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-233">1</span><span class="sxs-lookup"><span data-stu-id="b9cbb-233">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-234">UserRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="b9cbb-234">UserRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-235">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-235">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-236">Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-236">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b9cbb-237">Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-237">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-238">USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="b9cbb-238">USERREFRESHENABLED</span></span> </p></td>
<td align="left"><p><span data-ttu-id="b9cbb-239">Abilita l'aggiornamento della pubblicazione degli utenti (Boolean)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-239">Enables user publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-240">True (abilitato); False (stato disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-240">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-241">Publishing\Servers {serverId} \ UserEnabled</span><span class="sxs-lookup"><span data-stu-id="b9cbb-241">Publishing\Servers{serverId}\UserEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-242">False</span><span class="sxs-lookup"><span data-stu-id="b9cbb-242">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-243">UserRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="b9cbb-243">UserRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-244">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-244">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-245">Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-245">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b9cbb-246">Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-246">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-247">USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="b9cbb-247">USERREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-248">Attiva un aggiornamento della pubblicazione degli utenti ONLOGON.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-248">Triggers a user publishing refresh onlogon.</span></span> <span data-ttu-id="b9cbb-249">Boolean</span><span class="sxs-lookup"><span data-stu-id="b9cbb-249">( Boolean)</span></span></p>
<p><span data-ttu-id="b9cbb-250">Conteggio parole (con spazi): 60</span><span class="sxs-lookup"><span data-stu-id="b9cbb-250">Word count (with spaces): 60</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-251">True (abilitato); False (stato disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-251">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-252">Publishing\Servers {serverId} \ UserLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="b9cbb-252">Publishing\Servers{serverId}\UserLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-253">False</span><span class="sxs-lookup"><span data-stu-id="b9cbb-253">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-254">UserRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b9cbb-254">UserRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-255">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-255">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-256">Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-256">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b9cbb-257">Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-257">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-258">USERREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="b9cbb-258">USERREFRESHINTERVAL</span></span>     </p></td>
<td align="left"><p><span data-ttu-id="b9cbb-259">Specifica l'intervallo di aggiornamento della pubblicazione con UserRefreshIntervalUnit.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-259">Specifies the publishing refresh interval using the UserRefreshIntervalUnit.</span></span> <span data-ttu-id="b9cbb-260">Per disabilitare l'aggiornamento del pacchetto, selezionare 0.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-260">To disable package refresh, select 0.</span></span></p>
<p><span data-ttu-id="b9cbb-261">Conteggio parole (con spazi): 85</span><span class="sxs-lookup"><span data-stu-id="b9cbb-261">Word count (with spaces): 85</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-262">Numero intero (0-744 ore)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-262">Integer (0-744 Hours)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-263">Publishing\Servers {serverId} \ UserPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="b9cbb-263">Publishing\Servers{serverId}\UserPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-264">0</span><span class="sxs-lookup"><span data-stu-id="b9cbb-264">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-265">UserRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b9cbb-265">UserRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-266">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-266">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-267">Questa impostazione non può essere modificata usando il <strong> cmdLet set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-267">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="b9cbb-268">Devi usare il <strong> cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-268">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-269">USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="b9cbb-269">USERREFRESHINTERVALUNIT</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="b9cbb-270">Specifica l'unità di intervallo (ora 0-23, giorno 0-31).</span><span class="sxs-lookup"><span data-stu-id="b9cbb-270">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="b9cbb-271">0 per ora, 1 per giorno</span><span class="sxs-lookup"><span data-stu-id="b9cbb-271">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-272">Publishing\Servers {serverId} \ UserPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="b9cbb-272">Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-273">1</span><span class="sxs-lookup"><span data-stu-id="b9cbb-273">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-274">MigrationMode</span><span class="sxs-lookup"><span data-stu-id="b9cbb-274">MigrationMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-275">MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="b9cbb-275">MIGRATIONMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-276">La modalità di migrazione consente al client App-V di modificare i tasti di scelta rapida e FTA per i pacchetti creati con una versione precedente di App-V.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-276">Migration mode allows the App-V client to modify shortcuts and FTA’s for packages created using a previous version of App-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-277">True (stato abilitato); False (stato disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-277">True(enabled state); False (disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-278">Coexistence\MigrationMode</span><span class="sxs-lookup"><span data-stu-id="b9cbb-278">Coexistence\MigrationMode</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-279">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="b9cbb-279">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-280">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="b9cbb-280">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-281">Consente al computer che usa il client App-V 5,0 di raccogliere e restituire determinate informazioni sull'utilizzo per consentire di migliorare ulteriormente l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-281">Allows the computer running the App-V 5.0 Client to collect and return certain usage information to help allow us to further improve the application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-282">0 per disabilitato; 1 per abilitato</span><span class="sxs-lookup"><span data-stu-id="b9cbb-282">0 for disabled; 1 for enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-283">SOFTWARE/Microsoft/AppV/analisi utilizzo software/CEIPEnable</span><span class="sxs-lookup"><span data-stu-id="b9cbb-283">SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-284">0</span><span class="sxs-lookup"><span data-stu-id="b9cbb-284">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-285">EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="b9cbb-285">EnablePackageScripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-286">ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="b9cbb-286">ENABLEPACKAGESCRIPTS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-287">Abilita gli script definiti nel manifesto del pacchetto di file di configurazione che deve essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-287">Enables scripts defined in the package manifest of configuration files that should run.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-288">True (abilitato); False (stato disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-288">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-289">\Scripting\EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="b9cbb-289">\Scripting\EnablePackageScripts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-290">RoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="b9cbb-290">RoamingFileExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-291">ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="b9cbb-291">ROAMINGFILEEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-292">Specifica i percorsi di file relativi a% USERPROFILE% che non sono in roaming con un profilo utente&#39;s.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-292">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="b9cbb-293">Esempio di utilizzo:/ROAMINGFILEEXCLUSIONS =&#39;desktop; immagini personali&#39;</span><span class="sxs-lookup"><span data-stu-id="b9cbb-293">Example usage:  /ROAMINGFILEEXCLUSIONS=&#39;desktop;my pictures&#39;</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-294">RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="b9cbb-294">RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-295">ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="b9cbb-295">ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-296">Specifica i percorsi del registro di sistema che non sono in roaming con un profilo utente.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-296">Specifies the registry paths that do not roam with a user profile.</span></span> <span data-ttu-id="b9cbb-297">Esempio di utilizzo:/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</span><span class="sxs-lookup"><span data-stu-id="b9cbb-297">Example usage: /ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-298">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-298">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-299">Integration\RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="b9cbb-299">Integration\RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-300">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-300">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-301">IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="b9cbb-301">IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-302">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-302">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-303">Specifica la posizione in cui creare collegamenti simbolici associati alla versione corrente di un pacchetto pubblicato per utente.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-303">Specifies the location to create symbolic links associated with the current version of a per-user published package.</span></span> <span data-ttu-id="b9cbb-304">tutte le estensioni delle applicazioni virtuali, ad esempio le scelte rapide da tastiera e le associazioni di tipi di file, puntano al percorso.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-304">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="b9cbb-305">Se non specifichi un percorso, i collegamenti simbolici non verranno usati quando pubblichi il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-305">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="b9cbb-306">Ad esempio:%localappdata%\Microsoft\AppV\Client\Integration.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-306">For example: %localappdata%\Microsoft\AppV\Client\Integration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-307">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-307">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-308">Integration\IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="b9cbb-308">Integration\IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-309">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-309">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-310">IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="b9cbb-310">IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-311">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-311">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-312">Specifica la posizione in cui creare collegamenti simbolici associati alla versione corrente di un pacchetto pubblicato globalmente.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-312">Specifies the location to create symbolic links associated with the current version of a globally published package.</span></span> <span data-ttu-id="b9cbb-313">tutte le estensioni delle applicazioni virtuali, ad esempio le scelte rapide da tastiera e le associazioni di tipi di file, puntano al percorso.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-313">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="b9cbb-314">Se non specifichi un percorso, i collegamenti simbolici non verranno usati quando pubblichi il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-314">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="b9cbb-315">Ad esempio:%allusersprofile%\Microsoft\AppV\Client\Integration</span><span class="sxs-lookup"><span data-stu-id="b9cbb-315">For example: %allusersprofile%\Microsoft\AppV\Client\Integration</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-316">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-316">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-317">Integration\IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="b9cbb-317">Integration\IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-318">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-318">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-319">VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="b9cbb-319">VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-320">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-320">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-321">Un elenco delimitato da virgole delle estensioni di file che possono essere usate per determinare se un'applicazione installata localmente può essere eseguita nell'ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-321">A comma -delineated list of file name extensions that can be used to determine if a locally installed application can be run in the virtual environment.</span></span></p>
<p><span data-ttu-id="b9cbb-322">Quando si creano tasti di scelta rapida, accordi e altri punti di estensione durante la pubblicazione, App-V confronterà l'estensione del nome file all'elenco se l'applicazione associata al punto di estensione è installata localmente.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-322">When shortcuts, FTAs, and other extension points are created during publishing, App-V will compare the file name extension to the list if the application that is associated with the extension point is locally installed.</span></span> <span data-ttu-id="b9cbb-323">Se si trova l'estensione, <strong> </strong> verrà aggiunto il parametro della riga di comando RunVirtual e l'applicazione verrà eseguita virtualmente.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-323">If the extension is located, the <strong>RunVirtual</strong> command line parameter will be added, and the application will run virtually.</span></span></p>
<p><span data-ttu-id="b9cbb-324">Per altre informazioni sul <strong> parametro RunVirtual </strong> , vedere <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> eseguire un'applicazione installata localmente in un ambiente virtuale con applicazioni virtualizzate </a> .</span><span class="sxs-lookup"><span data-stu-id="b9cbb-324">For more information about the <strong>RunVirtual</strong> parameter, see <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</a>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-325">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-325">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-326">Integration\VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="b9cbb-326">Integration\VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-327">Valore criterio non scritto</span><span class="sxs-lookup"><span data-stu-id="b9cbb-327">Policy value not written</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-328">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="b9cbb-328">ReportingEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-329">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-329">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-330">Consente al client di restituire informazioni a un server di report.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-330">Enables the client to return information to a reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-331">True (abilitato); False (stato disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-331">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-332">Reporting\EnableReporting</span><span class="sxs-lookup"><span data-stu-id="b9cbb-332">Reporting\EnableReporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-333">False</span><span class="sxs-lookup"><span data-stu-id="b9cbb-333">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-334">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="b9cbb-334">ReportingServerURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-335">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-335">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-336">Specifica la posizione nel server di report in cui vengono salvate le informazioni sul client.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-336">Specifies the location on the reporting server where client information is saved.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-337">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-337">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-338">Reporting\ReportingServer</span><span class="sxs-lookup"><span data-stu-id="b9cbb-338">Reporting\ReportingServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-339">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-339">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-340">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="b9cbb-340">ReportingDataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-341">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-341">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-342">Specifica la dimensione massima in megabyte (MB) della cache XML per l'archiviazione delle informazioni di report.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-342">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="b9cbb-343">Le dimensioni si applicano alla cache in memoria.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-343">The size applies to the cache in memory.</span></span> <span data-ttu-id="b9cbb-344">Quando viene raggiunto il limite, il file di log verrà ribaltato.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-344">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="b9cbb-345">Imposta tra 0 e 1024.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-345">Set between 0 and 1024.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-346">Numero intero [0-1024]</span><span class="sxs-lookup"><span data-stu-id="b9cbb-346">Integer [0-1024]</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-347">Reporting\DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="b9cbb-347">Reporting\DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-348">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-348">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-349">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="b9cbb-349">ReportingDataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-350">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-350">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-351">Specifica la dimensione massima in byte da trasmettere al server per la segnalazione delle richieste di caricamento.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-351">Specifies the maximum size in bytes to transmit to the server for reporting upload requests.</span></span> <span data-ttu-id="b9cbb-352">Ciò consente di evitare errori di trasmissione permanenti quando il log ha raggiunto una dimensione significativa.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-352">This can help avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="b9cbb-353">Impostato tra 1024 e illimitato.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-353">Set between 1024 and unlimited.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-354">Numero intero [1024-illimitato]</span><span class="sxs-lookup"><span data-stu-id="b9cbb-354">Integer [1024 - Unlimited]</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-355">Reporting\DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="b9cbb-355">Reporting\DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-356">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-356">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-357">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="b9cbb-357">ReportingStartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-358">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-358">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-359">Specifica il momento in cui avviare il client per inviare dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-359">Specifies the time to initiate the client to send data to the reporting server.</span></span> <span data-ttu-id="b9cbb-360">È necessario specificare un numero intero valido compreso tra 0-23 corrispondente all'ora del giorno.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-360">You must specify a valid integer between 0-23 corresponding to the hour of the day.</span></span> <span data-ttu-id="b9cbb-361">Per impostazione predefinita, il ReportingStartTime inizierà <strong> </strong> il giorno corrente alle 10 P. M. o 22.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-361">By default the <strong>ReportingStartTime</strong> will start on the current day at 10 P.M.or 22.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-362">Nota</span><span class="sxs-lookup"><span data-stu-id="b9cbb-362">Note</span></span></strong><br/><p><span data-ttu-id="b9cbb-363">Devi configurare questa impostazione in un momento in cui i computer che eseguono il client App-V 5,0 sono meno probabili di essere offline.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-363">You should configure this setting to a time when computers running the App-V 5.0 client are least likely to be offline.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-364">Numero intero (0-23)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-364">Integer (0 – 23)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-365">Report \ StartTime</span><span class="sxs-lookup"><span data-stu-id="b9cbb-365">Reporting\ StartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-366">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-366">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-367">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="b9cbb-367">ReportingInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-368">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-368">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-369">Specifica l'intervallo di tentativi che il client userà per rinviare i dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-369">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-370">Integer</span><span class="sxs-lookup"><span data-stu-id="b9cbb-370">Integer</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-371">Reporting\RetryInterval</span><span class="sxs-lookup"><span data-stu-id="b9cbb-371">Reporting\RetryInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-372">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-372">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-373">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="b9cbb-373">ReportingRandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-374">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-374">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-375">Specifica il ritardo massimo (in minuti) per l'invio dei dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-375">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="b9cbb-376">Quando l'attività pianificata viene avviata, il client genera un ritardo casuale compreso tra 0 e <strong> ReportingRandomDelay </strong> e attenderà la durata specificata prima di inviare i dati.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-376">When the scheduled task is started, the client generates a random delay between 0 and <strong>ReportingRandomDelay</strong> and will wait the specified duration before sending data.</span></span> <span data-ttu-id="b9cbb-377">Questo può aiutare a prevenire collisioni nel server.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-377">This can help to prevent collisions on the server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-378">Numero intero [0-ReportingRandomDelay]</span><span class="sxs-lookup"><span data-stu-id="b9cbb-378">Integer [0 - ReportingRandomDelay]</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-379">Reporting\RandomDelay</span><span class="sxs-lookup"><span data-stu-id="b9cbb-379">Reporting\RandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-380">Valore criterio non scritto (uguale a non configurato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-380">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-381">EnableDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="b9cbb-381">EnableDynamicVirtualization</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-382">Importante</span><span class="sxs-lookup"><span data-stu-id="b9cbb-382">Important</span></span></strong><br/><p><span data-ttu-id="b9cbb-383">Questa impostazione è disponibile solo con App-V 5,0 SP2 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-383">This setting is available only with App-V 5.0 SP2 or later.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-384">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-384">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-385">Abilita le estensioni della shell supportate, gli oggetti helper del browser e i controlli attivi X per essere virtualizzati ed eseguiti con le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-385">Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-386">1 (abilitato), 0 (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-386">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-387">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</span><span class="sxs-lookup"><span data-stu-id="b9cbb-387">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Virtualization</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-388">EnablePublishingRefreshUI</span><span class="sxs-lookup"><span data-stu-id="b9cbb-388">EnablePublishingRefreshUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-389">Importante</span><span class="sxs-lookup"><span data-stu-id="b9cbb-389">Important</span></span></strong><br/><p><span data-ttu-id="b9cbb-390">Questa impostazione è disponibile solo con App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-390">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-391">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-391">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-392">Abilita la barra di stato dell'aggiornamento della pubblicazione per il computer in cui è in esecuzione il client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-392">Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-393">1 (abilitato), 0 (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-393">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-394">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</span><span class="sxs-lookup"><span data-stu-id="b9cbb-394">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Publishing</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b9cbb-395">HideUI</span><span class="sxs-lookup"><span data-stu-id="b9cbb-395">HideUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b9cbb-396">Importante</span><span class="sxs-lookup"><span data-stu-id="b9cbb-396">Important</span></span></strong><br/><p><span data-ttu-id="b9cbb-397">Questa impostazione è disponibile solo con App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-397">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="b9cbb-398">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-398">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-399">Nasconde la barra di stato dell'aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-399">Hides the publishing refresh progress bar.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-400">1 (abilitato), 0 (disabilitato)</span><span class="sxs-lookup"><span data-stu-id="b9cbb-400">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b9cbb-401">ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="b9cbb-401">ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-402">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-402">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-403">Specifica un elenco di percorsi di processo (che possono contenere caratteri jolly), che sono candidati per l'uso della virtualizzazione dinamica (estensioni della shell supportate, oggetti helper del browser e controlli ActiveX).</span><span class="sxs-lookup"><span data-stu-id="b9cbb-403">Specifies a list of process paths (that may contain wildcards), which are candidates for using dynamic virtualization (supported shell extensions, browser helper objects, and ActiveX controls).</span></span> <span data-ttu-id="b9cbb-404">Solo i processi il cui percorso completo corrisponde a uno di questi elementi possono usare la virtualizzazione dinamica.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-404">Only processes whose full path matches one of these items can use dynamic virtualization.</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-405">String</span><span class="sxs-lookup"><span data-stu-id="b9cbb-405">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-406">Virtualization\ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="b9cbb-406">Virtualization\ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="b9cbb-407">Stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="b9cbb-407">Empty string.</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="b9cbb-408">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9cbb-408">Related topics</span></span>


[<span data-ttu-id="b9cbb-409">Distribuzione di App-V 5.0 Sequencer e del client</span><span class="sxs-lookup"><span data-stu-id="b9cbb-409">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

[<span data-ttu-id="b9cbb-410">Come modificare la configurazione del client App-V 5.0 usando il modello ADMX e Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="b9cbb-410">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[<span data-ttu-id="b9cbb-411">Come distribuire il client App-V</span><span class="sxs-lookup"><span data-stu-id="b9cbb-411">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)









