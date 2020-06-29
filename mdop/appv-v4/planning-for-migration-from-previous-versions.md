---
title: Pianificazione della migrazione da versioni precedenti
description: Pianificazione della migrazione da versioni precedenti
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815926"
---
# <span data-ttu-id="f7e7b-103">Pianificazione della migrazione da versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="f7e7b-103">Planning for Migration from Previous Versions</span></span>


<span data-ttu-id="f7e7b-104">Prima di provare a eseguire l'aggiornamento a Microsoft Application Virtualization 4.5 o versioni successive, è necessario aggiornare una versione precedente a 4.1 alla versione 4.1.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-104">Before attempting to upgrade to Microsoft Application Virtualization4.5 or later versions, any version prior to4.1 must be upgraded to version4.1.</span></span> <span data-ttu-id="f7e7b-105">È consigliabile pianificare prima di tutto aggiornare i client e quindi aggiornare i componenti del server.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-105">You should plan to upgrade your clients first, and then upgrade the server components.</span></span> <span data-ttu-id="f7e7b-106">I client che sono stati aggiornati a 4.5 continueranno a funzionare con i server di virtualizzazione delle applicazioni che non sono ancora stati aggiornati.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-106">Clients that have been upgraded to4.5 will continue to work with Application Virtualization servers that have not yet been upgraded.</span></span> <span data-ttu-id="f7e7b-107">Le versioni precedenti del client non sono supportate nei server che sono stati aggiornati a 4.5.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-107">Earlier versions of the client are not supported on servers that have been upgraded to4.5.</span></span> <span data-ttu-id="f7e7b-108">Per altre informazioni sull'aggiornamento dei componenti di sistema, vedere [considerazioni sulla distribuzione e l'aggiornamento della virtualizzazione delle applicazioni](application-virtualization-deployment-and-upgrade-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="f7e7b-108">For more information about upgrading the system components, see [Application Virtualization Deployment and Upgrade Considerations](application-virtualization-deployment-and-upgrade-considerations.md).</span></span>

<span data-ttu-id="f7e7b-109">Per garantire una migrazione efficace, i componenti del sistema di virtualizzazione dell'applicazione devono essere aggiornati nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="f7e7b-109">To help ensure a successful migration, the Application Virtualization system components should be upgraded in the following order:</span></span>

1.  **<span data-ttu-id="f7e7b-110">Client di Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-110">Microsoft Application Virtualization Clients.</span></span>** <span data-ttu-id="f7e7b-111">Per istruzioni dettagliate sull'aggiornamento, vedere [come aggiornare l'Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md).</span><span class="sxs-lookup"><span data-stu-id="f7e7b-111">For step-by-step upgrade instructions, see [How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md).</span></span>

2.  **<span data-ttu-id="f7e7b-112">Server e database di Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-112">Microsoft Application Virtualization Servers and Database.</span></span>** <span data-ttu-id="f7e7b-113">Per istruzioni dettagliate sull'aggiornamento, vedere [come aggiornare i server e i componenti di sistema](how-to-upgrade-the-servers-and-system-components.md).</span><span class="sxs-lookup"><span data-stu-id="f7e7b-113">For step-by-step upgrade instructions, see [How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md).</span></span>

    <span data-ttu-id="f7e7b-114">**Nota**  Se si dispone di più di un server per l'accesso alla rete di virtualizzazione dell'applicazione, è necessario che tutti questi server vengano disattivati durante l'aggiornamento del database.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-114">**Note** If you have more than one server sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="f7e7b-115">È consigliabile seguire le normali procedure aziendali per l'aggiornamento del database, ma è consigliabile testare l'aggiornamento del database usando una copia di backup del database per la prima volta in un server di test.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-115">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="f7e7b-116">Devi quindi selezionare uno dei server per il primo aggiornamento, che aggiornerà lo schema del database.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="f7e7b-117">Dopo che il database di produzione è stato aggiornato correttamente, è possibile aggiornare gli altri server.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-117">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

     

3.  **<span data-ttu-id="f7e7b-118">Servizio Web Microsoft Application Virtualization Management.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-118">Microsoft Application Virtualization Management Web Service.</span></span>** <span data-ttu-id="f7e7b-119">Questo passaggio si applica solo se il servizio Web di gestione si trova in un server distinto, che richiede l'esecuzione del programma di installazione del server nel server separato per l'aggiornamento del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-119">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Web service.</span></span> <span data-ttu-id="f7e7b-120">In caso contrario, il passaggio di aggiornamento del server precedente aggiornerà automaticamente il servizio Web di gestione.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-120">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span>

4.  **<span data-ttu-id="f7e7b-121">Microsoft Application Virtualization Management Console.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-121">Microsoft Application Virtualization Management Console.</span></span>** <span data-ttu-id="f7e7b-122">Questo passaggio si applica solo se la console di gestione si trova in un computer separato, per cui è necessario eseguire il programma di installazione del server in tale computer separato per aggiornare la console.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-122">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="f7e7b-123">In caso contrario, il passaggio di aggiornamento del server precedente aggiornerà la console di gestione.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-123">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span>

5.  **<span data-ttu-id="f7e7b-124">Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-124">Microsoft Application Virtualization Sequencer.</span></span>** <span data-ttu-id="f7e7b-125">Per istruzioni dettagliate, vedere [come installare Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="f7e7b-125">For step-by-step instructions, see [How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span></span> <span data-ttu-id="f7e7b-126">Tutti i pacchetti di applicazioni virtuali sequenziati nella versione 4.2 non dovranno essere risequenziati per l'uso con la versione 4.5.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-126">Any virtual application packages sequenced in version4.2 will not have to be re-sequenced for use with version4.5.</span></span> <span data-ttu-id="f7e7b-127">Tuttavia, è consigliabile aggiornare i pacchetti virtuali al formato Microsoft Application Virtualization 4.5 se si desidera applicare elenchi di controllo di accesso (ACL) predefiniti o generare un file di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-127">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization4.5 format if you would like to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="f7e7b-128">Si tratta di un processo semplice e richiede solo che il pacchetto di applicazione virtuale esistente venga aperto e salvato con il sequencer 4.5.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-128">This is a simple process and requires only that the existing virtual application package be opened and saved with the4.5 Sequencer.</span></span> <span data-ttu-id="f7e7b-129">Questo può essere automatizzato usando l'interfaccia della riga di comando di Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-129">This can be automated by using the Application Virtualization Sequencer command-line interface.</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="f7e7b-130">Supporto del pacchetto client App-V 4.6</span><span class="sxs-lookup"><span data-stu-id="f7e7b-130">App-V4.6 Client Package Support</span></span>


<span data-ttu-id="f7e7b-131">Puoi distribuire pacchetti creati in versioni precedenti di client App-V a App-V 4.6.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-131">You can deploy packages created in previous versions of App-V to App-V4.6 Clients.</span></span> <span data-ttu-id="f7e7b-132">È tuttavia necessario modificare il file **OSD** associato in modo che includa le informazioni appropriate per il sistema operativo e l'architettura di chip.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-132">However, you must modify the associated **.osd** file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="f7e7b-133">Usare i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-133">Use the following values.</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f7e7b-134">Valore OS</span><span class="sxs-lookup"><span data-stu-id="f7e7b-134">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7e7b-135">&lt;VALORE OS = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-135">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7e7b-136">&lt;VALORE OS = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-136">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7e7b-137">&lt;VALORE OS = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-137">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7e7b-138">&lt;VALORE OS = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-138">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7e7b-139">&lt;VALORE OS = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-139">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7e7b-140">&lt;VALORE OS = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-140">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7e7b-141">&lt;VALORE OS = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-141">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7e7b-142">&lt;VALORE OS = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-142">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7e7b-143">&lt;VALORE OS = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-143">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7e7b-144">&lt;VALORE OS = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-144">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7e7b-145">&lt;VALORE OS = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="f7e7b-145">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f7e7b-146">Per eseguire un pacchetto di 32 bit appena creato, è necessario sequenziare l'applicazione in un computer che esegue un sistema operativo a 32 bit con l'App-V 4.6 Sequencer installato.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-146">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V4.6 Sequencer installed.</span></span> <span data-ttu-id="f7e7b-147">Dopo aver sequenziato l'applicazione, nella console sequencer selezionare la scheda **distribuzione** e quindi specificare il sistema operativo appropriato e l'architettura di chip in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-147">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="f7e7b-148">**Importante**  Le applicazioni sequenziate in un computer che eseguono un sistema operativo a 64 bit devono essere distribuite nei computer che eseguono un sistema operativo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-148">**Important** Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="f7e7b-149">I nuovi pacchetti a 32 bit creati con l'App-V 4.6 Sequencer non verranno eseguiti nei computer che eseguono il client App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-149">New 32-bit packages created by using the App-V4.6 Sequencer will not run on computers running the App-V 4.5 Client.</span></span>

 

<span data-ttu-id="f7e7b-150">Per eseguire nuovi pacchetti a 64 bit nel client App-V 4.6, è necessario sequenziare l'applicazione in un computer che esegue App-V 4.6 Sequencer e che esegue un sistema operativo a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-150">To run new 64-bit packages on the App-V4.6 Client, you must sequence the application on a computer running the App-V4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="f7e7b-151">Dopo aver sequenziato l'applicazione, nella console sequencer selezionare la scheda **distribuzione** e quindi specificare il sistema operativo appropriato e l'architettura di chip in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-151">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="f7e7b-152">La tabella seguente elenca le versioni client in cui verranno eseguiti i pacchetti creati con le varie versioni del sequencer.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-152">The following table lists which client versions will run packages created by using the various versions of the Sequencer.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="f7e7b-153">Sequenziato tramite l'App-V 4,2 Sequencer</span><span class="sxs-lookup"><span data-stu-id="f7e7b-153">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="f7e7b-154">Sequenziato tramite l'App-V 4,5 Sequencer</span><span class="sxs-lookup"><span data-stu-id="f7e7b-154">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="f7e7b-155">Sequenziato tramite l'app 32 bit-V 4,6 Sequencer</span><span class="sxs-lookup"><span data-stu-id="f7e7b-155">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="f7e7b-156">Sequenziato tramite l'app 64 bit-V 4,6 Sequencer</span><span class="sxs-lookup"><span data-stu-id="f7e7b-156">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="f7e7b-157">Sequenziato tramite il sequencer App-V 4,6 SP1 di 32 bit</span><span class="sxs-lookup"><span data-stu-id="f7e7b-157">Sequenced by using the 32-bit App-V 4.6 SP1 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="f7e7b-158">Sequenziato tramite il sequencer App-V 4,6 SP1 di 64 bit</span><span class="sxs-lookup"><span data-stu-id="f7e7b-158">Sequenced by using the 64-bit App-V 4.6 SP1 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7e7b-159">Client di 4,2</span><span class="sxs-lookup"><span data-stu-id="f7e7b-159">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-160">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-160">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-161">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-161">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-162">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-162">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-163">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-164">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-164">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-165">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-165">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7e7b-166">4,5 client ¹</span><span class="sxs-lookup"><span data-stu-id="f7e7b-166">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-167">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-167">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-168">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-168">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-169">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-170">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-170">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-171">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-171">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-172">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-172">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7e7b-173">Client di 4,6 (32 bit)</span><span class="sxs-lookup"><span data-stu-id="f7e7b-173">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-174">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-174">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-175">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-175">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-176">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-176">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-177">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-177">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-178">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-179">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-179">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7e7b-180">Client di 4,6 (64 bit)</span><span class="sxs-lookup"><span data-stu-id="f7e7b-180">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-181">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-182">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-182">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-183">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-184">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-185">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-185">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-186">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f7e7b-187">Client SP1 di 4,6</span><span class="sxs-lookup"><span data-stu-id="f7e7b-187">4.6 SP1 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-188">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-189">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-190">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-191">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-191">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-192">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-192">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-193">No</span><span class="sxs-lookup"><span data-stu-id="f7e7b-193">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f7e7b-194">Client di 4,6 SP1 (64 bit)</span><span class="sxs-lookup"><span data-stu-id="f7e7b-194">4.6 SP1 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-195">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-196">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-197">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-197">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-198">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-199">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-199">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="f7e7b-200">Sì</span><span class="sxs-lookup"><span data-stu-id="f7e7b-200">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f7e7b-201">¹ si applica a tutte le versioni del client App-V 4.5, tra cui App-V 4.5, App-V 4.5 CU1 e App-V 4.5 SP1.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-201">¹Applies to all versions of the App-V4.5 Client, including App-V4.5, App-V4.5CU1 and App-V4.5 SP1.</span></span>

## <span data-ttu-id="f7e7b-202">Considerazioni aggiuntive sulla migrazione</span><span class="sxs-lookup"><span data-stu-id="f7e7b-202">Additional Migration Considerations</span></span>


<span data-ttu-id="f7e7b-203">Una delle caratteristiche dell'App-V 4.5 Sequencer è la possibilità di creare file di Windows Installer (con estensione msi) come punti di controllo per l'interoperabilità dei pacchetti di applicazioni virtuali con sistemi ESD (Electronic Software Distribution), come Microsoft endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-203">One of the features of the App-V4.5 Sequencer is the ability to create Windows Installer files (.msi) as control points for virtual application package interoperability with electronic software distribution (ESD) systems such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="f7e7b-204">I file di Windows Installer precedenti creati con lo strumento MSI per la virtualizzazione delle applicazioni installati in un client App-V 4.1 o 4.2 che viene successivamente aggiornato a 4.5 continueranno a funzionare, anche se non possono essere installati nel client 4.5.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-204">Previous Windows Installer files created with the .msi tool for Application Virtualization that were installed on a App-V4.1 or4.2 Client that is subsequently upgraded to4.5 continue to work, although they cannot be installed on the4.5 Client.</span></span> <span data-ttu-id="f7e7b-205">Tuttavia, non possono essere rimossi o aggiornati a meno che non vengano aggiornati nel sequencer 4.5.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-205">However, they cannot be removed or upgraded unless they are upgraded in the4.5 Sequencer.</span></span> <span data-ttu-id="f7e7b-206">Il pacchetto di applicazione virtuale pre-4,5 originale deve essere aperto nel sequencer 4.5 e quindi salvato come file di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-206">The original pre-4.5 virtual application package would need to be opened in the4.5 Sequencer and then saved as a Windows Installer File.</span></span>

<span data-ttu-id="f7e7b-207">**Nota**  Se il client App-V 4.2 è già stato aggiornato a 4.5, è possibile usare lo script come soluzione alternativa per conservare i 4.2 pacchetti in 4,5 client e consentire loro di gestirli.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-207">**Note** If the App-V4.2 Client has already been upgraded to4.5, it is possible to use script as a workaround to preserve the4.2 packages on4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="f7e7b-208">Questo script deve copiare due file, msvcp71.dll e msvcr71.dll, nella cartella di installazione di App-V e impostare i valori della chiave del registro di sistema seguenti nella chiave del registro di sistema \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="f7e7b-208">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key \[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

<span data-ttu-id="f7e7b-209">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="f7e7b-209">"ClientVersion"="4.2.1.20"</span></span>

<span data-ttu-id="f7e7b-210">"GlobalDataDirectory" = "C:\\\\Documents e Settings\\\\All Users\\\\Documents\\\\" (una posizione di scrittura globale)</span><span class="sxs-lookup"><span data-stu-id="f7e7b-210">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>

 

<span data-ttu-id="f7e7b-211">I file di Windows Installer generati dall'App-V 4,5 Sequencer visualizzano il messaggio di errore "questo pacchetto richiede Microsoft Application Virtualization Client 4,5 o versione successiva" quando si tenta di eseguirli in un client App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-211">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when you try to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="f7e7b-212">Aprire il vecchio pacchetto con l'App-V 4,5 SP1 Sequencer o l'App-V 4,6 Sequencer e generare un nuovo file MSI per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-212">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi for the package.</span></span>

<span data-ttu-id="f7e7b-213">Tutti i report 4.2 creati e salvati verranno sovrascritti quando il server viene aggiornato a 4.5.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-213">Any4.2 reports that were created and saved will be overwritten when the server is upgraded to4.5.</span></span> <span data-ttu-id="f7e7b-214">Se è necessario conservare questi report, è necessario salvare una copia di backup del file SftMMC. msc che si trova nella cartella di SoftGrid Management Console nel server e usare tale copia per sostituire il nuovo SftMMC. msc installato durante l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="f7e7b-214">If you need to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

<span data-ttu-id="f7e7b-215">Per altre informazioni sull'aggiornamento dalle versioni precedenti, vedere [aggiornamento alle domande frequenti su Microsoft Application Virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="f7e7b-215">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <span data-ttu-id="f7e7b-216">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f7e7b-216">Related topics</span></span>


[<span data-ttu-id="f7e7b-217">Pianificazione della distribuzione del sistema Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="f7e7b-217">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





