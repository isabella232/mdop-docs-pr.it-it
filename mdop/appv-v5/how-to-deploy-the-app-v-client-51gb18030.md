---
title: Come distribuire il client App-V
description: Come distribuire il client App-V
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805493"
---
# <span data-ttu-id="756fb-103">Come distribuire il client App-V</span><span class="sxs-lookup"><span data-stu-id="756fb-103">How to Deploy the App-V Client</span></span>


<span data-ttu-id="756fb-104">Usare la procedura seguente per installare il client di Microsoft Application Virtualization (App-V) 5,1 e il client di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="756fb-104">Use the following procedure to install the Microsoft Application Virtualization (App-V) 5.1 client and Remote Desktop Services client.</span></span> <span data-ttu-id="756fb-105">È necessario installare la versione del client che corrisponde al sistema operativo del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-105">You must install the version of the client that matches the operating system of the target computer.</span></span>

<a href="" id="bkmk-clt-install-prereqs"></a>**<span data-ttu-id="756fb-106">Operazioni da eseguire prima di iniziare</span><span class="sxs-lookup"><span data-stu-id="756fb-106">What to do before you start</span></span>**

1. <span data-ttu-id="756fb-107">Rivedere e installare i prerequisiti software:</span><span class="sxs-lookup"><span data-stu-id="756fb-107">Review and install the software prerequisites:</span></span>

   <span data-ttu-id="756fb-108">Installare il software prerequisito che corrisponde alla versione di App-V che si sta installando:</span><span class="sxs-lookup"><span data-stu-id="756fb-108">Install the prerequisite software that corresponds to the version of App-V that you are installing:</span></span>

   -   [<span data-ttu-id="756fb-109">Informazioni su App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="756fb-109">About App-V 5.1</span></span>](about-app-v-51.md)

   -   [<span data-ttu-id="756fb-110">Prerequisiti di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="756fb-110">App-V 5.1 Prerequisites</span></span>](app-v-51-prerequisites.md)

2. <span data-ttu-id="756fb-111">Esaminare gli scenari di coesistenza client e non supportati, in applicazione dell'installazione:</span><span class="sxs-lookup"><span data-stu-id="756fb-111">Review the client coexistence and unsupported scenarios, as applicable to your installation:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-112">Distribuzione di client App-V coesistenti</span><span class="sxs-lookup"><span data-stu-id="756fb-112">Deploying coexisting App-V clients</span></span></p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)"><span data-ttu-id="756fb-113">Pianificazione della distribuzione di App-V 5.1 Sequencer e del client</span><span class="sxs-lookup"><span data-stu-id="756fb-113">Planning for the App-V 5.1 Sequencer and Client Deployment</span></span></a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-114">Scenari di installazione non supportati o limitati</span><span class="sxs-lookup"><span data-stu-id="756fb-114">Unsupported or limited installation scenarios</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-115">Vedere la sezione client nelle <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configurazioni supportate in App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="756fb-115">See the client section in <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">App-V 5.1 Supported Configurations</span></span></a></p></td>
   </tr>
   </tbody>
   </table>



3. <span data-ttu-id="756fb-116">Esaminare le posizioni per informazioni sul Registro di sistema, il log e la risoluzione dei problemi del client:</span><span class="sxs-lookup"><span data-stu-id="756fb-116">Review the locations for client registry, log, and troubleshooting information:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="756fb-117">Informazioni sul Registro di sistema client</span><span class="sxs-lookup"><span data-stu-id="756fb-117">Client registry information</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="756fb-118">Per impostazione predefinita, dopo l'installazione del client App-V 5,1, le informazioni sul client sono archiviate nel registro di sistema nella chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="756fb-118">By default, after you install the App-V 5.1 client, the client information is stored in the registry in the following registry key:</span></span></p>
<p><strong><span data-ttu-id="756fb-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</span><span class="sxs-lookup"><span data-stu-id="756fb-119">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT</span></span></strong></p></li>
<li><p><span data-ttu-id="756fb-120">Quando si distribuisce un pacchetto virtualizzato in un computer che sta eseguendo il client App-V, i dati del pacchetto associati vengono archiviati nella posizione seguente:</span><span class="sxs-lookup"><span data-stu-id="756fb-120">When you deploy a virtualized package to a computer that is running the App-V client, the associated package data is stored in the following location:</span></span></p>
<p><strong><span data-ttu-id="756fb-121">C: \ ProgramData \ App-V</span><span class="sxs-lookup"><span data-stu-id="756fb-121">C: \ ProgramData \ App-V</span></span></strong></p>
<p><span data-ttu-id="756fb-122">È tuttavia possibile riconfigurare la posizione con la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="756fb-122">However, you can reconfigure this location with the following registry key:</span></span></p>
<p><strong><span data-ttu-id="756fb-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="756fb-123">HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="756fb-124">File di log client</span><span class="sxs-lookup"><span data-stu-id="756fb-124">Client log files</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="756fb-125">Per informazioni sul file di log associato al client App-V 5,1, eseguire una ricerca nel log seguente:</span><span class="sxs-lookup"><span data-stu-id="756fb-125">For log file information that is associated with the App-V 5.1 Client, search in the following log:</span></span></p>
<p><strong><span data-ttu-id="756fb-126">Registri eventi/registri applicazioni e servizi/Microsoft/AppV</span><span class="sxs-lookup"><span data-stu-id="756fb-126">Event logs / Applications and Services Logs / Microsoft / AppV</span></span></strong></p></li>
<li><p><span data-ttu-id="756fb-127">In App-V 5,0 SP3 alcuni registri sono stati consolidati e spostati nella posizione seguente:</span><span class="sxs-lookup"><span data-stu-id="756fb-127">In App-V 5.0 SP3, some logs were consolidated and moved to the following location:</span></span></p>
<p><strong><span data-ttu-id="756fb-128">Registri eventi/registri applicazioni e servizi/Microsoft/AppV/ServiceLog</span><span class="sxs-lookup"><span data-stu-id="756fb-128">Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</span></span></strong></p>
<p><span data-ttu-id="756fb-129">Per un elenco dei registri spostati, vedere <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> informazioni su App-V 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="756fb-129">For a list of the moved logs, see <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)">About App-V 5.0 SP3</a>.</span></span></p></li>
<li><p><span data-ttu-id="756fb-130">I pacchetti attualmente archiviati nei computer che eseguono il client App-V 5,1 vengono salvati nella posizione seguente:</span><span class="sxs-lookup"><span data-stu-id="756fb-130">Packages that are currently stored on computers that run the App-V 5.1 Client are saved to the following location:</span></span></p>
<p><strong><span data-ttu-id="756fb-131">C:\ProgramData\App-V &amp; lt; ID pacchetto &gt; &amp; lt; ID versione&gt;</span><span class="sxs-lookup"><span data-stu-id="756fb-131">C:\ProgramData\App-V&amp;lt;package id&gt;&amp;lt;version id&gt;</span></span></strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="756fb-132">Informazioni sulla risoluzione dei problemi di installazione client</span><span class="sxs-lookup"><span data-stu-id="756fb-132">Client installation troubleshooting information</span></span></p></td>
<td align="left"><p><span data-ttu-id="756fb-133">Vedere il log degli errori nella <strong> cartella% Temp% </strong> .</span><span class="sxs-lookup"><span data-stu-id="756fb-133">See the error log in the <strong>%temp%</strong> folder.</span></span> <span data-ttu-id="756fb-134">Per rivedere i file di log, fare clic sul pulsante <strong> Start </strong> , digitare <strong> % temp% </strong> e quindi cercare il <strong> log appv_ </strong> .</span><span class="sxs-lookup"><span data-stu-id="756fb-134">To review the log files, click <strong>Start</strong>, type <strong>%temp%</strong>, and then look for the <strong>appv_ log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="756fb-135">Per installare il client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="756fb-135">To install the App-V 5.1 Client</span></span>**

1.  <span data-ttu-id="756fb-136">Copiare il file di installazione del client App-V 5,1 nel computer in cui verrà installato.</span><span class="sxs-lookup"><span data-stu-id="756fb-136">Copy the App-V 5.1 client installation file to the computer on which it will be installed.</span></span> <span data-ttu-id="756fb-137">Scegliere tra i tipi di client seguenti:</span><span class="sxs-lookup"><span data-stu-id="756fb-137">Choose from the following client types:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="756fb-138">Tipo di client</span><span class="sxs-lookup"><span data-stu-id="756fb-138">Client type</span></span></th>
    <th align="left"><span data-ttu-id="756fb-139">File da usare</span><span class="sxs-lookup"><span data-stu-id="756fb-139">File to use</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="756fb-140">Versione standard del client</span><span class="sxs-lookup"><span data-stu-id="756fb-140">Standard version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="756fb-141">appv_client_setup.exe</span><span class="sxs-lookup"><span data-stu-id="756fb-141">appv_client_setup.exe</span></span></strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="756fb-142">Versione Servizi Desktop remoto del client</span><span class="sxs-lookup"><span data-stu-id="756fb-142">Remote Desktop Services version of the client</span></span></p></td>
    <td align="left"><p><strong><span data-ttu-id="756fb-143">appv_client_setup_rds.exe</span><span class="sxs-lookup"><span data-stu-id="756fb-143">appv_client_setup_rds.exe</span></span></strong></p></td>
    </tr>
    </tbody>
    </table>



2.  <span data-ttu-id="756fb-144">Fare doppio clic sul file di installazione e fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="756fb-144">Double-click the installation file, and click **Install**.</span></span> <span data-ttu-id="756fb-145">Prima che l'installazione venga avviata, il programma di installazione controlla il computer per tutti i [prerequisiti di App-V 5,1](app-v-51-prerequisites.md)mancanti.</span><span class="sxs-lookup"><span data-stu-id="756fb-145">Before the installation begins, the installer checks the computer for any missing [App-V 5.1 Prerequisites](app-v-51-prerequisites.md).</span></span>

3.  <span data-ttu-id="756fb-146">Rivedere e accettare le condizioni di licenza software, scegliere se usare Microsoft Update e se partecipare al programma Microsoft Customer Experience Improvement e fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="756fb-146">Review and accept the Software License Terms, choose whether to use Microsoft Update and whether to participate in the Microsoft Customer Experience Improvement Program, and click **Install**.</span></span>

4.  <span data-ttu-id="756fb-147">Nella pagina **installazione completata** fare clic su **Chiudi**.</span><span class="sxs-lookup"><span data-stu-id="756fb-147">On the **Setup completed successfully** page, click **Close**.</span></span>

    <span data-ttu-id="756fb-148">L'installazione crea le voci seguenti per il client App-V nei **programmi**:</span><span class="sxs-lookup"><span data-stu-id="756fb-148">The installation creates the following entries for the App-V client in **Programs**:</span></span>

    -   **<span data-ttu-id="756fb-149">.exe</span><span class="sxs-lookup"><span data-stu-id="756fb-149">.exe</span></span>**

    -   **<span data-ttu-id="756fb-150">.msi</span><span class="sxs-lookup"><span data-stu-id="756fb-150">.msi</span></span>**

    -   **<span data-ttu-id="756fb-151">Language Pack</span><span class="sxs-lookup"><span data-stu-id="756fb-151">language pack</span></span>**

        **<span data-ttu-id="756fb-152">Nota</span><span class="sxs-lookup"><span data-stu-id="756fb-152">Note</span></span>**  
        <span data-ttu-id="756fb-153">Dopo l'installazione, è possibile disinstallare solo il file exe.</span><span class="sxs-lookup"><span data-stu-id="756fb-153">After the installation, only the .exe file can be uninstalled.</span></span>



**<span data-ttu-id="756fb-154">Per installare il client App-V 5,1 con uno script</span><span class="sxs-lookup"><span data-stu-id="756fb-154">To install the App-V 5.1 client using a script</span></span>**

1. <span data-ttu-id="756fb-155">Installare tutti i prerequisiti software necessari nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-155">Install all of the required prerequisite software on the target computers.</span></span> <span data-ttu-id="756fb-156">Vedere [cosa fare prima di iniziare](#bkmk-clt-install-prereqs).</span><span class="sxs-lookup"><span data-stu-id="756fb-156">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="756fb-157">Se si installa il client usando un file con estensione msi, l'installazione non riuscirà se mancano i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="756fb-157">If you install the client by using an .msi file, the installation will fail if any prerequisites are missing.</span></span>

2. <span data-ttu-id="756fb-158">Per usare uno script per installare il client App-V 5,1, usare i parametri seguenti con **appv\_client\_setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="756fb-158">To use a script to install the App-V 5.1 client, use the following parameters with **appv\_client\_setup.exe**.</span></span>

   **<span data-ttu-id="756fb-159">Nota</span><span class="sxs-lookup"><span data-stu-id="756fb-159">Note</span></span>**  
   <span data-ttu-id="756fb-160">Il client Windows Installer (con estensione msi) supporta lo stesso set di opzioni, fatta eccezione per il parametro **/log** .</span><span class="sxs-lookup"><span data-stu-id="756fb-160">The client Windows Installer (.msi) supports the same set of switches, except for the **/LOG** parameter.</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-161">/INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="756fb-161">/INSTALLDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-162">Specifica la directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-162">Specifies the installation directory.</span></span> <span data-ttu-id="756fb-163">Esempio di utilizzo: <strong> /INSTALLDIR = C:\Program Files\AppV client</span><span class="sxs-lookup"><span data-stu-id="756fb-163">Example usage: <strong>/INSTALLDIR=C:\Program Files\AppV Client</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-164">/CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="756fb-164">/CEIPOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-165">Consente la partecipazione al programma Analisi utilizzo software.</span><span class="sxs-lookup"><span data-stu-id="756fb-165">Enables participation in the Customer Experience Improvement Program.</span></span> <span data-ttu-id="756fb-166">Esempio di utilizzo: <strong> /CEIPOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-166">Example usage: <strong>/CEIPOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-167">/MUOPTIN</span><span class="sxs-lookup"><span data-stu-id="756fb-167">/MUOPTIN</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-168">Abilita Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="756fb-168">Enables Microsoft Update.</span></span> <span data-ttu-id="756fb-169">Esempio di utilizzo: <strong> /MUOPTIN = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-169">Example usage: <strong>/MUOPTIN=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-170">/PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="756fb-170">/PACKAGEINSTALLATIONROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-171">Specifica la directory in cui installare tutte le nuove applicazioni e gli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="756fb-171">Specifies the directory in which to install all new applications and updates.</span></span> <span data-ttu-id="756fb-172">Esempio di utilizzo: <strong> /PACKAGEINSTALLATIONROOT =&#39;C:\app-V packages&#39;</span><span class="sxs-lookup"><span data-stu-id="756fb-172">Example usage: <strong>/PACKAGEINSTALLATIONROOT=&#39;C:\App-V Packages&#39;</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-173">/PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="756fb-173">/PACKAGESOURCEROOT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-174">Sostituisce la posizione di origine per il download del contenuto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="756fb-174">Overrides the source location for downloading package content.</span></span> <span data-ttu-id="756fb-175">Esempio di utilizzo: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</span><span class="sxs-lookup"><span data-stu-id="756fb-175">Example usage: <strong>/PACKAGESOURCEROOT=&#39;<a href="http://packageStore" data-raw-source="http://packageStore">http://packageStore</a>&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-176">/AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="756fb-176">/AUTOLOAD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-177">Specifica il modo in cui i nuovi pacchetti verranno caricati da App-V 5,1 in un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="756fb-177">Specifies how new packages will be loaded by App-V 5.1 on a specific computer.</span></span> <span data-ttu-id="756fb-178">Le opzioni seguenti sono abilitate: [1]; caricare automaticamente tutti i pacchetti [2]; o caricare automaticamente nessun pacchetto [0]. <strong> Esempio di utilizzo:/AUTOLOAD = [0 | 1 | 2]</span><span class="sxs-lookup"><span data-stu-id="756fb-178">The following options are enabled: [1]; automatically load all packages [2]; or automatically load no packages [0].<strong>Example usage: /AUTOLOAD=[0|1|2]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-179">/SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="756fb-179">/SHAREDCONTENTSTOREMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-180">Specifica che il contenuto del pacchetto in streaming non verrà salvato nel disco rigido locale.</span><span class="sxs-lookup"><span data-stu-id="756fb-180">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span> <span data-ttu-id="756fb-181">Esempio di utilizzo: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-181">Example usage: <strong>/SHAREDCONTENTSTOREMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-182">/MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="756fb-182">/MIGRATIONMODE</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-183">Consente al client App-V 5,1 di modificare i tasti di scelta rapida e i accordi associati ai pacchetti creati con una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="756fb-183">Allows the App-V 5.1 client to modify the shortcuts and FTAs that are associated with the packages that are created with a previous version.</span></span> <span data-ttu-id="756fb-184">Esempio di utilizzo: <strong> /MIGRATIONMODE = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-184">Example usage: <strong>/MIGRATIONMODE=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-185">/ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="756fb-185">/ENABLEPACKAGESCRIPTS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-186">Abilita gli script definiti nel file manifesto del pacchetto o nei file di configurazione che devono essere eseguiti.</span><span class="sxs-lookup"><span data-stu-id="756fb-186">Enables the scripts that are defined in the package manifest file or configuration files that should run.</span></span> <span data-ttu-id="756fb-187">Esempio di utilizzo: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-187">Example usage: <strong>/ENABLEPACKAGESCRIPTS=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-188">/ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="756fb-188">/ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-189">Specifica i percorsi del registro di sistema che non andranno in roaming con un profilo utente.</span><span class="sxs-lookup"><span data-stu-id="756fb-189">Specifies the registry paths that will not roam with a user profile.</span></span> <span data-ttu-id="756fb-190">Esempio di utilizzo: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</span><span class="sxs-lookup"><span data-stu-id="756fb-190">Example usage: <strong>/ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-191">/ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="756fb-191">/ROAMINGFILEEXCLUSIONS</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-192">Specifica i percorsi di file relativi a% USERPROFILE% che non sono in roaming con un profilo utente&#39;s.</span><span class="sxs-lookup"><span data-stu-id="756fb-192">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="756fb-193">Esempio di utilizzo: <strong> /ROAMINGFILEEXCLUSIONS &#39;desktop; immagini personali&#39;</span><span class="sxs-lookup"><span data-stu-id="756fb-193">Example usage: <strong>/ROAMINGFILEEXCLUSIONS &#39;desktop;my pictures&#39;</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-194">/S [1-5] PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="756fb-194">/S[1-5]PUBLISHINGSERVERNAME</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-195">Visualizza il nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-195">Displays the name of the publishing server.</span></span> <span data-ttu-id="756fb-196">Esempio di utilizzo: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</span><span class="sxs-lookup"><span data-stu-id="756fb-196">Example usage: <strong>/S2PUBLISHINGSERVERNAME=MyPublishingServer</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-197">/S [1-5] PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="756fb-197">/S[1-5]PUBLISHINGSERVERURL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-198">Visualizza l'URL del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-198">Displays the URL of the publishing server.</span></span> <span data-ttu-id="756fb-199">Esempio di utilizzo: <strong> /S2PUBLISHINGSERVERURL = \pubserver</span><span class="sxs-lookup"><span data-stu-id="756fb-199">Example usage: <strong>/S2PUBLISHINGSERVERURL=\pubserver</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-200">/S [1-5] GLOBALREFRESHENABLED-</span><span class="sxs-lookup"><span data-stu-id="756fb-200">/S[1-5]GLOBALREFRESHENABLED -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-201">Abilita un aggiornamento globale della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-201">Enables a global publishing refresh.</span></span> <span data-ttu-id="756fb-202">Esempio di utilizzo: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-202">Example usage: <strong>/S2GLOBALREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-203">/S [1-5] GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="756fb-203">/S[1-5]GLOBALREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-204">Avvia un aggiornamento della pubblicazione globale quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="756fb-204">Initiates a global publishing refresh when a user logs on.</span></span> <span data-ttu-id="756fb-205">Esempio di utilizzo: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-205">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-206">/S [1-5] GLOBALREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="756fb-206">/S[1-5]GLOBALREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-207">Specifica l'intervallo di aggiornamento della pubblicazione, dove <strong> 0 </strong> indica che non viene aggiornato periodicamente.</span><span class="sxs-lookup"><span data-stu-id="756fb-207">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="756fb-208">Esempio di utilizzo: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="756fb-208">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-209">/S [1-5] GLOBALREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="756fb-209">/S[1-5]GLOBALREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-210">Specifica l'unità di intervallo (ore [0], giorni [1]).</span><span class="sxs-lookup"><span data-stu-id="756fb-210">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="756fb-211">Esempio di utilizzo: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-211">Example usage: <strong>/S2GLOBALREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-212">/S [1-5] USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="756fb-212">/S[1-5]USERREFRESHENABLED</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-213">Consente di aggiornare la pubblicazione degli utenti.</span><span class="sxs-lookup"><span data-stu-id="756fb-213">Enables user publishing refresh.</span></span> <span data-ttu-id="756fb-214">Esempio di utilizzo: <strong> /S2USERREFRESHENABLED = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-214">Example usage: <strong>/S2USERREFRESHENABLED=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-215">/S [1-5] USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="756fb-215">/S[1-5]USERREFRESHONLOGON</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-216">Avvia un aggiornamento della pubblicazione degli utenti quando un utente esegue l'accesso.</span><span class="sxs-lookup"><span data-stu-id="756fb-216">Initiates a user publishing refresh when a user logs on.</span></span> <span data-ttu-id="756fb-217">Esempio di utilizzo: <strong> /S2LOGONREFRESH = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-217">Example usage: <strong>/S2LOGONREFRESH=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-218">/S [1-5] USERREFRESHINTERVAL-</span><span class="sxs-lookup"><span data-stu-id="756fb-218">/S[1-5]USERREFRESHINTERVAL -</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-219">Specifica l'intervallo di aggiornamento della pubblicazione, dove <strong> 0 </strong> indica che non viene aggiornato periodicamente.</span><span class="sxs-lookup"><span data-stu-id="756fb-219">Specifies the publishing refresh interval, where <strong>0</strong> indicates do not periodically refresh.</span></span> <span data-ttu-id="756fb-220">Esempio di utilizzo: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</span><span class="sxs-lookup"><span data-stu-id="756fb-220">Example usage: <strong>/S2PERIODICREFRESHINTERVAL=[0-744]</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-221">/S [1-5] USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="756fb-221">/S[1-5]USERREFRESHINTERVALUNIT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-222">Specifica l'unità di intervallo (ore [0], giorni [1]).</span><span class="sxs-lookup"><span data-stu-id="756fb-222">Specifies the interval unit (Hours[0], Days[1]).</span></span> <span data-ttu-id="756fb-223">Esempio di utilizzo: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</span><span class="sxs-lookup"><span data-stu-id="756fb-223">Example usage: <strong>/S2USERREFRESHINTERVALUNIT=[0|1]</span></span></strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-224">/Log</span><span class="sxs-lookup"><span data-stu-id="756fb-224">/Log</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-225">Specifica un percorso in cui vengono salvate le informazioni sul log.</span><span class="sxs-lookup"><span data-stu-id="756fb-225">Specifies a location where the log information is saved.</span></span> <span data-ttu-id="756fb-226">La posizione predefinita è% Temp%.</span><span class="sxs-lookup"><span data-stu-id="756fb-226">The default location is %Temp%.</span></span> <span data-ttu-id="756fb-227">Esempio di utilizzo: <strong> /log C:\logs\log.log</span><span class="sxs-lookup"><span data-stu-id="756fb-227">Example usage: <strong>/log C:\logs\log.log</span></span></strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-228">/nocancel/q</span><span class="sxs-lookup"><span data-stu-id="756fb-228">/q</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-229">Specifica un'installazione automatica.</span><span class="sxs-lookup"><span data-stu-id="756fb-229">Specifies an unattended installation.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-230">/REPAIR</span><span class="sxs-lookup"><span data-stu-id="756fb-230">/REPAIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-231">Ripristina un'installazione precedente del client.</span><span class="sxs-lookup"><span data-stu-id="756fb-231">Repairs a previous client installation.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-232">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="756fb-232">/NORESTART</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-233">Impedisce il riavvio del computer dopo l'installazione del client.</span><span class="sxs-lookup"><span data-stu-id="756fb-233">Prevents the computer from rebooting after the client installation.</span></span></p>
   <p><span data-ttu-id="756fb-234">Il parametro impedisce il riavvio del computer per gli utenti finali dopo l'installazione di ogni aggiornamento e consente di programmare la reinstallazione in base alle proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="756fb-234">The parameter prevents the end-user computer from rebooting after each update is installed and lets you schedule the reboot at your convenience.</span></span> <span data-ttu-id="756fb-235">Ad esempio, è possibile installare App-V 5,1 e quindi installare il pacchetto di hotfix Y senza riavviare il sistema dopo l'installazione del Service Pack.</span><span class="sxs-lookup"><span data-stu-id="756fb-235">For example, you can install App-V 5.1 and then install Hotfix Package Y without rebooting after the Service Pack installation.</span></span> <span data-ttu-id="756fb-236">Dopo l'installazione, è necessario riavviare prima di iniziare a usare app-V.</span><span class="sxs-lookup"><span data-stu-id="756fb-236">After the installation, you must reboot before you start using App-V.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-237">/UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="756fb-237">/UNINSTALL</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-238">Disinstalla il client.</span><span class="sxs-lookup"><span data-stu-id="756fb-238">Uninstalls the client.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-239">/ACCEPTEULA</span><span class="sxs-lookup"><span data-stu-id="756fb-239">/ACCEPTEULA</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-240">Accetta il contratto di licenza.</span><span class="sxs-lookup"><span data-stu-id="756fb-240">Accepts the license agreement.</span></span> <span data-ttu-id="756fb-241">Questa operazione è necessaria per un'installazione automatica.</span><span class="sxs-lookup"><span data-stu-id="756fb-241">This is required for an unattended installation.</span></span> <span data-ttu-id="756fb-242">Esempio di utilizzo: <strong> /AcceptEula </strong> o <strong> /ACCEPTEULA = 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="756fb-242">Example usage: <strong>/ACCEPTEULA</strong> or <strong>/ACCEPTEULA=1</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-243">/LAYOUT</span><span class="sxs-lookup"><span data-stu-id="756fb-243">/LAYOUT</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-244">Specifica l'azione di layout associata.</span><span class="sxs-lookup"><span data-stu-id="756fb-244">Specifies the associated layout action.</span></span> <span data-ttu-id="756fb-245">Estrae anche Windows Installer (. msi) e i file di script in una cartella senza installare App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="756fb-245">It also extracts the Windows Installer (.msi) and script files to a folder without installing App-V 5.1.</span></span> <span data-ttu-id="756fb-246">Nessun valore previsto.</span><span class="sxs-lookup"><span data-stu-id="756fb-246">No value is expected.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="756fb-247">/LAYOUTDIR</span><span class="sxs-lookup"><span data-stu-id="756fb-247">/LAYOUTDIR</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-248">Specifica la directory del layout.</span><span class="sxs-lookup"><span data-stu-id="756fb-248">Specifies the layout directory.</span></span> <span data-ttu-id="756fb-249">Richiede un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="756fb-249">Requires a string value.</span></span> <span data-ttu-id="756fb-250">Esempio di utilizzo: <strong> /LAYOUTDIR = "client di virtualizzazione C:\Application" </strong> .</span><span class="sxs-lookup"><span data-stu-id="756fb-250">Example usage: <strong>/LAYOUTDIR=”C:\Application Virtualization Client”</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="756fb-251">/?,/h,/Help</span><span class="sxs-lookup"><span data-stu-id="756fb-251">/?, /h, /help</span></span></p></td>
   <td align="left"><p><span data-ttu-id="756fb-252">Richiede informazioni sui parametri di installazione precedenti.</span><span class="sxs-lookup"><span data-stu-id="756fb-252">Requests help about the previous installation parameters.</span></span></p></td>
   </tr>
   </tbody>
   </table>



**<span data-ttu-id="756fb-253">Per installare il client App-V 5,1 usando il file di Windows Installer (con estensione msi)</span><span class="sxs-lookup"><span data-stu-id="756fb-253">To install the App-V 5.1 client by using the Windows Installer (.msi) file</span></span>**

1.  <span data-ttu-id="756fb-254">Installare i prerequisiti necessari nei computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-254">Install the required prerequisites on the target computers.</span></span> <span data-ttu-id="756fb-255">Vedere [cosa fare prima di iniziare](#bkmk-clt-install-prereqs).</span><span class="sxs-lookup"><span data-stu-id="756fb-255">See [What to do before you start](#bkmk-clt-install-prereqs).</span></span> <span data-ttu-id="756fb-256">Se i prerequisiti non sono soddisfatti, l'installazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="756fb-256">If any prerequisites are not met, the installation will fail.</span></span>

2.  <span data-ttu-id="756fb-257">Assicurarsi che i computer di destinazione non abbiano un riavvio in sospeso prima di installare il client con i file di Windows Installer (MSI) di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="756fb-257">Ensure that the target computers do not have any pending restarts before you install the client using the App-V 5.1 Windows Installer (.msi) files.</span></span> <span data-ttu-id="756fb-258">I file di Windows Installer non contrassegnano un riavvio in sospeso.</span><span class="sxs-lookup"><span data-stu-id="756fb-258">The Windows Installer files do not flag a pending restart.</span></span>

3.  <span data-ttu-id="756fb-259">Distribuire uno dei file di Windows Installer seguenti nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-259">Deploy one of the following Windows Installer files to the target computer.</span></span> <span data-ttu-id="756fb-260">Il file specificato deve corrispondere alla configurazione del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-260">The file that you specify must match the configuration of the target computer.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="756fb-261">Tipo di distribuzione</span><span class="sxs-lookup"><span data-stu-id="756fb-261">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="756fb-262">Distribuire il file</span><span class="sxs-lookup"><span data-stu-id="756fb-262">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="756fb-263">Il computer sta usando un sistema operativo Microsoft Windows a 32 bit</span><span class="sxs-lookup"><span data-stu-id="756fb-263">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="756fb-264">appv_client_MSI_x86.msi</span><span class="sxs-lookup"><span data-stu-id="756fb-264">appv_client_MSI_x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="756fb-265">Il computer sta usando un sistema operativo Microsoft Windows a 64 bit</span><span class="sxs-lookup"><span data-stu-id="756fb-265">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="756fb-266">appv_client_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="756fb-266">appv_client_MSI_x64.msi</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="756fb-267">Si sta distribuendo il client Servizi Desktop remoto App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="756fb-267">You are deploying the App-V 5.1 Remote Desktop Services client</span></span></p></td>
    <td align="left"><p><span data-ttu-id="756fb-268">appv_client_rds_MSI_x64.msi</span><span class="sxs-lookup"><span data-stu-id="756fb-268">appv_client_rds_MSI_x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="756fb-269">Usando le informazioni nella tabella seguente, selezionare il Language Pack **. msi** appropriato da installare, in base alla lingua desiderata per il computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-269">Using the information in the following table, select the appropriate language pack **.msi** to install, based on the desired language for the target computer.</span></span> <span data-ttu-id="756fb-270">Il **xxxx** nella tabella fa riferimento alle impostazioni locali di destinazione del Language Pack.</span><span class="sxs-lookup"><span data-stu-id="756fb-270">The **xxxx** in the table refers to the target locale of the language pack.</span></span>

    **<span data-ttu-id="756fb-271">Informazioni da conoscere prima di iniziare:</span><span class="sxs-lookup"><span data-stu-id="756fb-271">What to know before you start:</span></span>**

    -   <span data-ttu-id="756fb-272">I Language Pack sono comuni sia al client standard App-V 5,1 che alla versione Servizi Desktop remoto del client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="756fb-272">The language packs are common to both the standard App-V 5.1 client and the Remote Desktop Services version of the App-V 5.1 client.</span></span>

    -   <span data-ttu-id="756fb-273">Se si installa il client App-V 5,1 usando il **. exe**, il programma di installazione distribuirà solo il Language Pack che corrisponde al sistema operativo in uso nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="756fb-273">If you install the App-V 5.1 client using the **.exe**, the installer will deploy only the language pack that matches the operating system running on the target computer.</span></span>

    -   <span data-ttu-id="756fb-274">Per distribuire altri Language Pack in un computer di destinazione, usare la procedura **per installare il client App-V 5,1 usando il file di Windows Installer (con estensione msi)**.</span><span class="sxs-lookup"><span data-stu-id="756fb-274">To deploy additional language packs on a target computer, use the procedure **To install the App-V 5.1 client by using Windows Installer (.msi) file**.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="756fb-275">Tipo di distribuzione</span><span class="sxs-lookup"><span data-stu-id="756fb-275">Type of deployment</span></span></th>
    <th align="left"><span data-ttu-id="756fb-276">Distribuire il file</span><span class="sxs-lookup"><span data-stu-id="756fb-276">Deploy this file</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="756fb-277">Il computer sta usando un sistema operativo Microsoft Windows a 32 bit</span><span class="sxs-lookup"><span data-stu-id="756fb-277">Computer is running a 32-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="756fb-278">appv_client_LP_xxxx_ x86.msi</span><span class="sxs-lookup"><span data-stu-id="756fb-278">appv_client_LP_xxxx_ x86.msi</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="756fb-279">Il computer sta usando un sistema operativo Microsoft Windows a 64 bit</span><span class="sxs-lookup"><span data-stu-id="756fb-279">Computer is running a 64-bit Microsoft Windows operating system</span></span></p></td>
    <td align="left"><p><span data-ttu-id="756fb-280">appv_client_LP_xxxx_ x64.msi</span><span class="sxs-lookup"><span data-stu-id="756fb-280">appv_client_LP_xxxx_ x64.msi</span></span></p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## <span data-ttu-id="756fb-281">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="756fb-281">Related topics</span></span>


[<span data-ttu-id="756fb-282">Distribuzione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="756fb-282">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="756fb-283">Informazioni sulle impostazioni di configurazione client</span><span class="sxs-lookup"><span data-stu-id="756fb-283">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

[<span data-ttu-id="756fb-284">Come disinstallare il client App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="756fb-284">How to Uninstall the App-V 5.1 Client</span></span>](how-to-uninstall-the-app-v-51-client.md)









