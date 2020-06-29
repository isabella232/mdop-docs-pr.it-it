---
title: Informazioni su App-V 5.0 SP3
description: Informazioni su App-V 5.0 SP3
author: dansimp
ms.assetid: 67b5268b-edc1-4027-98b0-b3937dd70a6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: bc72f3f72c2b06470287dfe4ba3ed22abcc6068b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814975"
---
# <span data-ttu-id="6784b-103">Informazioni su App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6784b-103">About App-V 5.0 SP3</span></span>


<span data-ttu-id="6784b-104">Usare le sezioni seguenti per esaminare le informazioni sulle modifiche significative che si applicano a Microsoft Application Virtualization (App-V) 5,0 SP3:</span><span class="sxs-lookup"><span data-stu-id="6784b-104">Use the following sections to review information about significant changes that apply to Microsoft Application Virtualization (App-V) 5.0 SP3:</span></span>

-   [<span data-ttu-id="6784b-105">Prerequisiti software App-V 5,0 SP3 e configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="6784b-105">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>](#bkmk-sp3-prereq-configs)

-   [<span data-ttu-id="6784b-106">Migrazione a App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6784b-106">Migrating to App-V 5.0 SP3</span></span>](#bkmk-migrate-to-50sp3)

-   [<span data-ttu-id="6784b-107">Il file XML del gruppo di connessioni creato manualmente richiede l'aggiornamento allo schema</span><span class="sxs-lookup"><span data-stu-id="6784b-107">Manually created connection group xml file requires update to schema</span></span>](#bkmk-update-schema-cg)

-   [<span data-ttu-id="6784b-108">Miglioramenti apportati ai gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="6784b-108">Improvements to connection groups</span></span>](#bkmk-cg-improvements)

-   [<span data-ttu-id="6784b-109">Gli amministratori possono pubblicare e annullare la pubblicazione di pacchetti per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="6784b-109">Administrators can publish and unpublish packages for a specific user</span></span>](#bkmk-usersid-pub-pkgs-specf-user)

-   [<span data-ttu-id="6784b-110">Consentire solo agli amministratori di pubblicare e annullare la pubblicazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="6784b-110">Enable only administrators to publish and unpublish packages</span></span>](#bkmk-admins-only-pub-unpub-pkgs)

-   [<span data-ttu-id="6784b-111">La chiave del registro di sistema RunVirtual supporta i pacchetti pubblicati per l'utente</span><span class="sxs-lookup"><span data-stu-id="6784b-111">RunVirtual registry key supports packages that are published to the user</span></span>](#bkmk-runvirtual-reg-key)

-   [<span data-ttu-id="6784b-112">Guida di nuovi cmdlet di PowerShell e cmdlet aggiornabile</span><span class="sxs-lookup"><span data-stu-id="6784b-112">New PowerShell cmdlets and updateable cmdlet help</span></span>](#bkmk-posh-cmdlets-help)

-   [<span data-ttu-id="6784b-113">La directory delle applicazioni virtuali primarie (PVAD) è nascosta ma può essere attivata</span><span class="sxs-lookup"><span data-stu-id="6784b-113">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>](#bkmk-pvad-hidden)

-   [<span data-ttu-id="6784b-114">ClientVersion è necessario per visualizzare i metadati di pubblicazione di App-V</span><span class="sxs-lookup"><span data-stu-id="6784b-114">ClientVersion is required to view App-V publishing metadata</span></span>](#bkmk-pub-metadata-clientversion)

-   [<span data-ttu-id="6784b-115">I registri eventi App-V sono stati consolidati</span><span class="sxs-lookup"><span data-stu-id="6784b-115">App-V event logs have been consolidated</span></span>](#bkmk-event-logs-moved)

## <a href="" id="bkmk-sp3-prereq-configs"></a><span data-ttu-id="6784b-116">Prerequisiti software App-V 5,0 SP3 e configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="6784b-116">App-V 5.0 SP3 software prerequisites and supported configurations</span></span>


<span data-ttu-id="6784b-117">Vedere i collegamenti seguenti per i prerequisiti software App-V 5,0 SP3 e le configurazioni supportate.</span><span class="sxs-lookup"><span data-stu-id="6784b-117">See the following links for the App-V 5.0 SP3 software prerequisites and supported configurations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-118">Collegamenti ai prerequisiti e alle configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="6784b-118">Links to prerequisites and supported configurations</span></span></th>
<th align="left"><span data-ttu-id="6784b-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6784b-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-50-sp3-prerequisites.md" data-raw-source="[App-V 5.0 SP3 Prerequisites](app-v-50-sp3-prerequisites.md)"><span data-ttu-id="6784b-120">Prerequisiti di App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6784b-120">App-V 5.0 SP3 Prerequisites</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="6784b-121">Software prerequisito che è necessario installare prima di avviare l'installazione di App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6784b-121">Prerequisite software that you must install before starting the App-V 5.0 SP3 installation</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-50-sp3-supported-configurations.md" data-raw-source="[App-V 5.0 SP3 Supported Configurations](app-v-50-sp3-supported-configurations.md)"><span data-ttu-id="6784b-122">Configurazioni supportate da App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6784b-122">App-V 5.0 SP3 Supported Configurations</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="6784b-123">Requisiti hardware e sistemi operativi supportati per i componenti App-V Server, sequencer e client</span><span class="sxs-lookup"><span data-stu-id="6784b-123">Supported operating systems and hardware requirements for the App-V Server, Sequencer, and Client components</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-migrate-to-50sp3"></a><span data-ttu-id="6784b-124">Migrazione a App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6784b-124">Migrating to App-V 5.0 SP3</span></span>


<span data-ttu-id="6784b-125">Usare le informazioni seguenti per eseguire l'aggiornamento a App-V 5,0 SP3 da versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="6784b-125">Use the following information to upgrade to App-V 5.0 SP3 from earlier versions.</span></span>

### <span data-ttu-id="6784b-126">Prima di iniziare l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6784b-126">Before you start the upgrade</span></span>

<span data-ttu-id="6784b-127">Prima di iniziare l'aggiornamento, esaminare le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6784b-127">Review the following information before you start the upgrade:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-128">Elementi da rivedere prima dell'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6784b-128">Items to review before upgrading</span></span></th>
<th align="left"><span data-ttu-id="6784b-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6784b-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-130">Componenti da aggiornare</span><span class="sxs-lookup"><span data-stu-id="6784b-130">Components to upgrade</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="6784b-131">App-V Server</span><span class="sxs-lookup"><span data-stu-id="6784b-131">App-V Server</span></span></p></li>
<li><p><span data-ttu-id="6784b-132">Sequencer</span><span class="sxs-lookup"><span data-stu-id="6784b-132">Sequencer</span></span></p></li>
<li><p><span data-ttu-id="6784b-133">App-V client o client RDS (Remote Desktop Services) App-V</span><span class="sxs-lookup"><span data-stu-id="6784b-133">App-V client or App-V Remote Desktop Services (RDS) client</span></span></p></li>
<li><p><span data-ttu-id="6784b-134">Gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="6784b-134">Connection groups</span></span></p></li>
</ol>
<div class="alert">
<strong><span data-ttu-id="6784b-135">Nota</span><span class="sxs-lookup"><span data-stu-id="6784b-135">Note</span></span></strong><br/><p><span data-ttu-id="6784b-136">Per usare l'interfaccia utente del client App-V, Scarica la versione esistente dall' <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> applicazione Microsoft Application Virtualization 5,0 client </a> .</span><span class="sxs-lookup"><span data-stu-id="6784b-136">To use the App-V client user interface, download the existing version from <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Microsoft Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)">Microsoft Application Virtualization 5.0 Client UI Application</a>.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-137">Aggiornamento da App-V 4. x</span><span class="sxs-lookup"><span data-stu-id="6784b-137">Upgrading from App-V 4.x</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-138">Devi prima eseguire l'aggiornamento a App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="6784b-138">You must first upgrade to App-V 5.0.</span></span> <span data-ttu-id="6784b-139">Non è possibile eseguire l'aggiornamento direttamente da App-V 4. x a App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="6784b-139">You cannot upgrade directly from App-V 4.x to App-V 5.0 SP3.</span></span></p>
<p><span data-ttu-id="6784b-140">Per altre informazioni, vedi:</span><span class="sxs-lookup"><span data-stu-id="6784b-140">For more information, see:</span></span></p>
<ul>
<li><p><a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"><span data-ttu-id="6784b-141">Informazioni su App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="6784b-141">About App-V 5.0</span></span></a> </p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)"><span data-ttu-id="6784b-142">Pianificazione per la migrazione da una versione precedente di App-V</span><span class="sxs-lookup"><span data-stu-id="6784b-142">Planning for Migrating from a Previous Version of App-V</span></span></a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-143">Aggiornamento da App-V 5,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6784b-143">Upgrading from App-V 5.0 or later</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-144">È possibile eseguire l'aggiornamento a App-V 5,0 SP3 direttamente da una delle versioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6784b-144">You can upgrade to App-V 5.0 SP3 directly from any of the following versions:</span></span></p>
<ul>
<li><p><span data-ttu-id="6784b-145">App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="6784b-145">App-V 5.0</span></span></p></li>
<li><p><span data-ttu-id="6784b-146">App-V 5,0 SP1</span><span class="sxs-lookup"><span data-stu-id="6784b-146">App-V 5.0 SP1</span></span></p></li>
<li><p><span data-ttu-id="6784b-147">App-V 5,0 SP2</span><span class="sxs-lookup"><span data-stu-id="6784b-147">App-V 5.0 SP2</span></span></p></li>
</ul>
<p><span data-ttu-id="6784b-148">Per eseguire l'aggiornamento a App-V 5,0 SP3, seguire la procedura descritta nelle sezioni rimanenti di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="6784b-148">To upgrade to App-V 5.0 SP3, follow the steps in the remaining sections of this article.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-149">Modifiche necessarie ai pacchetti e ai gruppi di connessioni dopo l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6784b-149">Required changes to packages and connection groups after upgrade</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-150">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="6784b-150">None.</span></span> <span data-ttu-id="6784b-151">I pacchetti e i gruppi di connessioni continueranno a funzionare al momento.</span><span class="sxs-lookup"><span data-stu-id="6784b-151">Packages and connection groups will continue to work as they currently do.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a><span data-ttu-id="6784b-152">Procedura per aggiornare l'infrastruttura di App-V</span><span class="sxs-lookup"><span data-stu-id="6784b-152">Steps to upgrade the App-V infrastructure</span></span>

<span data-ttu-id="6784b-153">Completare i passaggi seguenti per aggiornare ogni componente dell'infrastruttura App-V in App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="6784b-153">Complete the following steps to upgrade each component of the App-V infrastructure to App-V 5.0 SP3.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-154">Passaggio</span><span class="sxs-lookup"><span data-stu-id="6784b-154">Step</span></span></th>
<th align="left"><span data-ttu-id="6784b-155">Per altre informazioni</span><span class="sxs-lookup"><span data-stu-id="6784b-155">For more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-156">Passaggio 1: aggiornare l'App-V Server.</span><span class="sxs-lookup"><span data-stu-id="6784b-156">Step 1: Upgrade the App-V Server.</span></span></p>
<p><span data-ttu-id="6784b-157">Se non si usa App-V Server, ignorare questo passaggio e passare al passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="6784b-157">If you are not using the App-V Server, skip this step and go to the next step.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6784b-158">Nota</span><span class="sxs-lookup"><span data-stu-id="6784b-158">Note</span></span></strong><br/><p><span data-ttu-id="6784b-159">Il client App-V 5,0 SP3 è compatibile con il server App-V 5,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="6784b-159">The App-V 5.0 SP3 client is compatible with the App-V 5.0 SP1 Server.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="6784b-160">Segui questa procedura: </span><span class="sxs-lookup"><span data-stu-id="6784b-160">Follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="6784b-161">Esaminare le <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)"> Note sulla versione per App-v 5,0 SP3 </a> per problemi che possono influire sull'installazione di App-v Server.</span><span class="sxs-lookup"><span data-stu-id="6784b-161">Review the <a href="release-notes-for-app-v-50-sp3.md" data-raw-source="[Release Notes for App-V 5.0 SP3](release-notes-for-app-v-50-sp3.md)">Release Notes for App-V 5.0 SP3</a> for issues that may affect the App-V Server installation.</span></span></p></li>
<li><p><span data-ttu-id="6784b-162">Eseguire una delle operazioni seguenti, a seconda del metodo usato per aggiornare il database di gestione e/o il database di report:</span><span class="sxs-lookup"><span data-stu-id="6784b-162">Do one of the following, depending on the method you are using to upgrade the Management database and/or Reporting database:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-163">Metodo di aggiornamento del database</span><span class="sxs-lookup"><span data-stu-id="6784b-163">Database upgrade method</span></span></th>
<th align="left"><span data-ttu-id="6784b-164">Passaggio</span><span class="sxs-lookup"><span data-stu-id="6784b-164">Step</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-165">Windows Installer</span><span class="sxs-lookup"><span data-stu-id="6784b-165">Windows Installer</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-166">Ignorare questo passaggio e passare al passaggio 3, "Se si esegue l'aggiornamento del server App-V..."</span><span class="sxs-lookup"><span data-stu-id="6784b-166">Skip this step and go to step 3, “If you are upgrading the App-V Server...”</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-167">Script SQL</span><span class="sxs-lookup"><span data-stu-id="6784b-167">SQL scripts</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6784b-168">Database di gestione</span><span class="sxs-lookup"><span data-stu-id="6784b-168">Management database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6784b-169">Per installare o aggiornare, vedere <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> gli script SQL per installare o aggiornare il database del server di gestione di App-V 5,0 SP3 Fail </a> .</span><span class="sxs-lookup"><span data-stu-id="6784b-169">To install or upgrade, see <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)">SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6784b-170">Database di report</span><span class="sxs-lookup"><span data-stu-id="6784b-170">Reporting database</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6784b-171">Seguire i passaggi descritti in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> come distribuire i database di App-V tramite gli script SQL </a> .</span><span class="sxs-lookup"><span data-stu-id="6784b-171">Follow the steps in <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)">How to Deploy the App-V Databases by Using SQL Scripts</a>.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>
<p> </p></li>
<li><p><span data-ttu-id="6784b-172">Se si sta aggiornando il pacchetto di hotfix App-v 5,0 SP1 3 o versione successiva, eseguire la procedura descritta nella sezione <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)"> controllare le chiavi del registro di sistema dopo l'installazione del server App-v 5,0 SP3 </a> .</span><span class="sxs-lookup"><span data-stu-id="6784b-172">If you are upgrading the App-V Server from App-V 5.0 SP1 Hotfix Package 3 or later, complete the steps in section <a href="#bkmk-check-reg-key-svr" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](#bkmk-check-reg-key-svr)">Check registry keys after installing the App-V 5.0 SP3 Server</a>.</span></span></p></li>
<li><p><span data-ttu-id="6784b-173">Seguire la procedura descritta in <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)"> come distribuire il server App-V 5,0 </a> .</span><span class="sxs-lookup"><span data-stu-id="6784b-173">Follow the steps in <a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">How to Deploy the App-V 5.0 Server</a>.</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-174">Passaggio 2: aggiornare l'App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="6784b-174">Step 2: Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-175">Vedere <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> come installare il sequencer </a> .</span><span class="sxs-lookup"><span data-stu-id="6784b-175">See <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)">How to Install the Sequencer</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-176">Passaggio 3: aggiornare il client App-V o client RDS App-v.</span><span class="sxs-lookup"><span data-stu-id="6784b-176">Step 3: Upgrade the App-V client or App-V RDS client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-177">Scopri <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> come distribuire il client App-V </a> .</span><span class="sxs-lookup"><span data-stu-id="6784b-177">See <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">How to Deploy the App-V Client</a>.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-check-reg-key-svr"></a><span data-ttu-id="6784b-178">Controllare le chiavi del registro di sistema prima di installare il server App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6784b-178">Check registry keys before installing the App-V 5.0 SP3 Server</span></span>

<span data-ttu-id="6784b-179">Questo è il passaggio 3 della tabella precedente.</span><span class="sxs-lookup"><span data-stu-id="6784b-179">This is step 3 from the previous table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6784b-180">Quando è necessario eseguire questo passaggio</span><span class="sxs-lookup"><span data-stu-id="6784b-180">When this step is required</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6784b-181">Si esegue l'aggiornamento da App-V SP1 con tutti i pacchetti di hotfix successivi installati usando un file msp.</span><span class="sxs-lookup"><span data-stu-id="6784b-181">You are upgrading from App-V SP1 with any subsequent Hotfix Packages that you installed by using an .msp file.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6784b-182">Quali componenti richiedono di eseguire questo passaggio</span><span class="sxs-lookup"><span data-stu-id="6784b-182">Which components require that you do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6784b-183">Solo i componenti di App-V Server che si stanno aggiornando.</span><span class="sxs-lookup"><span data-stu-id="6784b-183">Only the App-V Server components that you are upgrading.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6784b-184">Quando è necessario eseguire questo passaggio</span><span class="sxs-lookup"><span data-stu-id="6784b-184">When you need to do this step</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6784b-185">Prima di aggiornare l'App-V Server a App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6784b-185">Before you upgrade the App-V Server to App-V 5.0 SP3</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6784b-186">Cosa è necessario fare</span><span class="sxs-lookup"><span data-stu-id="6784b-186">What you need to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6784b-187">Usando le informazioni nelle tabelle seguenti, aggiornare ogni valore della chiave del registro <code>HKLM\Software\Microsoft\AppV\Server</code> di sistema in con il valore specificato nell'installazione del server originale.</span><span class="sxs-lookup"><span data-stu-id="6784b-187">Using the information in the following tables, update each registry key value under <code>HKLM\Software\Microsoft\AppV\Server</code> with the value that you provided in your original server installation.</span></span> <span data-ttu-id="6784b-188">Il completamento di questo passaggio ripristina i valori del registro di sistema che potrebbero essere stati rimossi quando sono stati installati i pacchetti di hotfix di App-V SP1.</span><span class="sxs-lookup"><span data-stu-id="6784b-188">Completing this step restores registry values that may have been removed when App-V SP1 Hotfix Packages were installed.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="6784b-189">Tasto ManagementDatabase</span><span class="sxs-lookup"><span data-stu-id="6784b-189">ManagementDatabase key</span></span>**

<span data-ttu-id="6784b-190">Se si sta installando il database di gestione, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase` .</span><span class="sxs-lookup"><span data-stu-id="6784b-190">If you are installing the Management database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-191">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="6784b-191">Key name</span></span></th>
<th align="left"><span data-ttu-id="6784b-192">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6784b-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="6784b-193">IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-194">Descrive se è necessario un account di accesso pubblico per accedere ai database di gestione non locali.</span><span class="sxs-lookup"><span data-stu-id="6784b-194">Describes whether a public access account is required to access non-local management databases.</span></span> <span data-ttu-id="6784b-195">Il valore è impostato su "1" se necessario.</span><span class="sxs-lookup"><span data-stu-id="6784b-195">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-196">MANAGEMENT_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6784b-196">MANAGEMENT_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-197">Nome del database di gestione.</span><span class="sxs-lookup"><span data-stu-id="6784b-197">Name of the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6784b-198">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-199">Account usato per l'accesso in lettura (pubblico) al database di gestione.</span><span class="sxs-lookup"><span data-stu-id="6784b-199">Account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="6784b-200">Usato quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="6784b-200">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="6784b-201">MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-202">Identificatore sicuro (SID) dell'account usato per l'accesso in lettura (pubblico) al database di gestione.</span><span class="sxs-lookup"><span data-stu-id="6784b-202">Secure identifier (SID) of the account used for read (public) access to the Management database.</span></span></p>
<p><span data-ttu-id="6784b-203">Usato quando <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="6784b-203">Used when <code>IS_MANAGEMENT_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-204">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6784b-204">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-205">Istanza di SQL Server per il database di gestione.</span><span class="sxs-lookup"><span data-stu-id="6784b-205">SQL Server instance for the Management database.</span></span></p>
<p><span data-ttu-id="6784b-206">Se il valore è vuoto, viene usata l'istanza di database predefinita.</span><span class="sxs-lookup"><span data-stu-id="6784b-206">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6784b-207">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-208">Account usato per l'accesso in scrittura (amministratore) al database di gestione.</span><span class="sxs-lookup"><span data-stu-id="6784b-208">Account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="6784b-209">MANAGEMENT_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-210">Identificatore sicuro (SID) dell'account usato per l'accesso in scrittura (amministratore) al database di gestione.</span><span class="sxs-lookup"><span data-stu-id="6784b-210">Secure identifier (SID) of the account used for write (administrator) access to the Management database.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6784b-211">MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-212">Account del computer remoto di Management Server (dominio\account).</span><span class="sxs-lookup"><span data-stu-id="6784b-212">Management server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6784b-213">MANAGEMENT_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-214">Account di accesso dell'amministratore dell'installazione per il server di gestione (dominio\account).</span><span class="sxs-lookup"><span data-stu-id="6784b-214">Installation administrator login for the Management server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6784b-215">MANAGEMENT_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-216">Valori validi:</span><span class="sxs-lookup"><span data-stu-id="6784b-216">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="6784b-217">1 </strong> -il servizio di gestione si trova nel computer locale, ovvero MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT è vuoto.</span><span class="sxs-lookup"><span data-stu-id="6784b-217">1</strong> – the Management service is on the local computer, that is, MANAGEMENT_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="6784b-218">0 </strong> - il servizio di gestione si trova in un computer diverso dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="6784b-218">0</strong> - the Management service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="6784b-219">Tasto ManagementService</span><span class="sxs-lookup"><span data-stu-id="6784b-219">ManagementService key</span></span>**

<span data-ttu-id="6784b-220">Se si sta installando il server di gestione, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ManagementService` .</span><span class="sxs-lookup"><span data-stu-id="6784b-220">If you are installing the Management server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ManagementService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-221">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="6784b-221">Key name</span></span></th>
<th align="left"><span data-ttu-id="6784b-222">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6784b-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-223">MANAGEMENT_ADMINACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6784b-223">MANAGEMENT_ADMINACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-224">Gruppo o account Active Directory Domain Services (AD DS) autorizzato a gestire App-V (dominio\account).</span><span class="sxs-lookup"><span data-stu-id="6784b-224">Active Directory Domain Services (AD DS) group or account that is authorized to manage App-V (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-225">MANAGEMENT_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6784b-225">MANAGEMENT_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-226">Istanza di SQL Server che contiene il database di gestione.</span><span class="sxs-lookup"><span data-stu-id="6784b-226">SQL server instance that contains the Management database.</span></span></p>
<p><span data-ttu-id="6784b-227">Se il valore è vuoto, viene usata l'istanza di database predefinita.</span><span class="sxs-lookup"><span data-stu-id="6784b-227">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-228">MANAGEMENT_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="6784b-228">MANAGEMENT_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-229">Nome del server SQL remoto con il database di gestione.</span><span class="sxs-lookup"><span data-stu-id="6784b-229">Name of the remote SQL server with the Management database.</span></span></p>
<p><span data-ttu-id="6784b-230">Se il valore è vuoto, viene usato il computer locale.</span><span class="sxs-lookup"><span data-stu-id="6784b-230">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="6784b-231">Tasto ReportingDatabase</span><span class="sxs-lookup"><span data-stu-id="6784b-231">ReportingDatabase key</span></span>**

<span data-ttu-id="6784b-232">Se si sta installando il database delle relazioni, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase` .</span><span class="sxs-lookup"><span data-stu-id="6784b-232">If you are installing the Reporting database, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingDatabase`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-233">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="6784b-233">Key name</span></span></th>
<th align="left"><span data-ttu-id="6784b-234">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6784b-234">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span><span class="sxs-lookup"><span data-stu-id="6784b-235">IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-236">Descrive se è necessario un account di accesso pubblico per accedere a database di report non locali.</span><span class="sxs-lookup"><span data-stu-id="6784b-236">Describes whether a public access account is required to access non-local reporting databases.</span></span> <span data-ttu-id="6784b-237">Il valore è impostato su "1" se necessario.</span><span class="sxs-lookup"><span data-stu-id="6784b-237">Value is set to “1” if it is required.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-238">REPORTING_DB_NAME</span><span class="sxs-lookup"><span data-stu-id="6784b-238">REPORTING_DB_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-239">Nome del database di report.</span><span class="sxs-lookup"><span data-stu-id="6784b-239">Name of the Reporting database.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6784b-240">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-241">Account usato per l'accesso in lettura (pubblico) al database di report.</span><span class="sxs-lookup"><span data-stu-id="6784b-241">Account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="6784b-242">Usato quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="6784b-242">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="6784b-243">REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-244">Identificatore sicuro (SID) dell'account usato per l'accesso in lettura (pubblico) al database di report.</span><span class="sxs-lookup"><span data-stu-id="6784b-244">Secure identifier (SID) of the account used for read (public) access to the Reporting database.</span></span></p>
<p><span data-ttu-id="6784b-245">Usato quando <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> è impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="6784b-245">Used when <code>IS_REPORTING_DB_PUBLIC_ACCESS_ACCOUNT_REQUIRED</code> is set to 1.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-246">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6784b-246">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-247">Istanza di SQL Server per il database di report.</span><span class="sxs-lookup"><span data-stu-id="6784b-247">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="6784b-248">Se il valore è vuoto, viene usata l'istanza di database predefinita.</span><span class="sxs-lookup"><span data-stu-id="6784b-248">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6784b-249">REPORTING_DB_WRITE_ACCESS_ACCOUNT</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span><span class="sxs-lookup"><span data-stu-id="6784b-250">REPORTING_DB_WRITE_ACCESS_ACCOUNT_SID</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6784b-251">REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-252">Account del computer remoto di Reporting Server (dominio\account).</span><span class="sxs-lookup"><span data-stu-id="6784b-252">Reporting server remote computer account (domain\account).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span><span class="sxs-lookup"><span data-stu-id="6784b-253">REPORTING_SERVER_INSTALL_ADMIN_ACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-254">Account di accesso dell'amministratore dell'installazione per il server di report (dominio\account).</span><span class="sxs-lookup"><span data-stu-id="6784b-254">Installation administrator login for the Reporting server (domain\account).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6784b-255">REPORTING_SERVER_MACHINE_USE_LOCAL</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-256">Valori validi:</span><span class="sxs-lookup"><span data-stu-id="6784b-256">Valid values are:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="6784b-257">1 </strong> -il servizio Reporting si trova nel computer locale, ovvero REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT è vuoto.</span><span class="sxs-lookup"><span data-stu-id="6784b-257">1</strong> – the Reporting service is on the local computer, that is, REPORTING_REMOTE_SERVER_MACHINE_ACCOUNT is blank.</span></span></p></li>
<li><p><strong><span data-ttu-id="6784b-258">0 </strong> - il servizio Reporting si trova in un computer diverso dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="6784b-258">0</strong> - the Reporting service is on a different computer from the local computer.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="6784b-259">Tasto ReportingService</span><span class="sxs-lookup"><span data-stu-id="6784b-259">ReportingService key</span></span>**

<span data-ttu-id="6784b-260">Se si sta installando il server di Reporting, impostare le chiavi del registro di sistema in `HKLM\Software\Microsoft\AppV\Server\ReportingService` .</span><span class="sxs-lookup"><span data-stu-id="6784b-260">If you are installing the Reporting server, set these registry keys under `HKLM\Software\Microsoft\AppV\Server\ReportingService`.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-261">Nome chiave</span><span class="sxs-lookup"><span data-stu-id="6784b-261">Key name</span></span></th>
<th align="left"><span data-ttu-id="6784b-262">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6784b-262">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-263">REPORTING_DB_SQL_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="6784b-263">REPORTING_DB_SQL_INSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-264">Istanza di SQL Server per il database di report.</span><span class="sxs-lookup"><span data-stu-id="6784b-264">SQL Server instance for the Reporting database.</span></span></p>
<p><span data-ttu-id="6784b-265">Se il valore è vuoto, viene usata l'istanza di database predefinita.</span><span class="sxs-lookup"><span data-stu-id="6784b-265">If the value is blank, the default database instance is used.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-266">REPORTING_DB_SQL_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="6784b-266">REPORTING_DB_SQL_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-267">Nome del server SQL remoto con il database di report.</span><span class="sxs-lookup"><span data-stu-id="6784b-267">Name of the remote SQL server with the Reporting database.</span></span></p>
<p><span data-ttu-id="6784b-268">Se il valore è vuoto, viene usato il computer locale.</span><span class="sxs-lookup"><span data-stu-id="6784b-268">If the value is blank, the local computer is used.</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-update-schema-cg"></a><span data-ttu-id="6784b-269">Il file XML del gruppo di connessioni creato manualmente richiede l'aggiornamento allo schema</span><span class="sxs-lookup"><span data-stu-id="6784b-269">Manually created connection group xml file requires update to schema</span></span>


<span data-ttu-id="6784b-270">Se si crea manualmente il file XML del gruppo di connessioni e si vogliono usare le nuove funzionalità "pacchetti facoltativi" e "Usa qualsiasi versione" descritte in [miglioramenti ai gruppi di connessioni](#bkmk-cg-improvements), è necessario specificare lo schema seguente nel file XML:</span><span class="sxs-lookup"><span data-stu-id="6784b-270">If you are manually creating the connection group XML file, and want to use the new “optional packages” and “use any version” features that are described in [Improvements to connection groups](#bkmk-cg-improvements), you must specify the following schema in the XML file:</span></span>

`xmlns="http://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"`

<span data-ttu-id="6784b-271">Per esempi e altre informazioni, vedere [informazioni sul file del gruppo di connessioni](about-the-connection-group-file.md).</span><span class="sxs-lookup"><span data-stu-id="6784b-271">For examples and more information, see [About the Connection Group File](about-the-connection-group-file.md).</span></span>

## <a href="" id="bkmk-cg-improvements"></a><span data-ttu-id="6784b-272">Miglioramenti apportati ai gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="6784b-272">Improvements to connection groups</span></span>


<span data-ttu-id="6784b-273">Puoi gestire i gruppi di connessioni più facilmente usando pacchetti facoltativi e altri miglioramenti che sono stati aggiunti in App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="6784b-273">You can manage connection groups more easily by using optional packages and other improvements that have been added in App-V 5.0 SP3.</span></span> <span data-ttu-id="6784b-274">Nella tabella seguente sono riepilogate le attività che è possibile eseguire con le nuove caratteristiche dei gruppi di connessioni e i collegamenti a informazioni più dettagliate su ogni attività.</span><span class="sxs-lookup"><span data-stu-id="6784b-274">The following table summarizes the tasks that you can perform by using the new connection group features, and links to more detailed information about each task.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-275">Attività/funzionalità</span><span class="sxs-lookup"><span data-stu-id="6784b-275">Task/feature</span></span></th>
<th align="left"><span data-ttu-id="6784b-276">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6784b-276">Description</span></span></th>
<th align="left"><span data-ttu-id="6784b-277">Collegamenti ad altre informazioni</span><span class="sxs-lookup"><span data-stu-id="6784b-277">Links to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-278">Abilitare un gruppo di connessioni per includere pacchetti facoltativi</span><span class="sxs-lookup"><span data-stu-id="6784b-278">Enable a connection group to include optional packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-279">L'inclusione di pacchetti facoltativi in un gruppo di connessioni consente di determinare in modo dinamico quali applicazioni verranno incluse nell'ambiente virtuale del gruppo di connessioni, in base alle applicazioni a cui gli utenti hanno diritto.</span><span class="sxs-lookup"><span data-stu-id="6784b-279">Including optional packages in a connection group enables you to dynamically determine which applications will be included in the connection group’s virtual environment, based on the applications that users are entitled to.</span></span></p>
<p><span data-ttu-id="6784b-280">Non è necessario gestire il numero di gruppi di connessioni perché è possibile combinare pacchetti facoltativi e non facoltativi nello stesso gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6784b-280">You don’t need to manage as many connection groups because you can mix optional and non-optional packages in the same connection group.</span></span> <span data-ttu-id="6784b-281">La combinazione di pacchetti consente a diversi gruppi di utenti di usare lo stesso gruppo di connessioni, anche se gli utenti potrebbero avere un solo pacchetto in comune.</span><span class="sxs-lookup"><span data-stu-id="6784b-281">Mixing packages allows different groups of users to use the same connection group, even though users might have only one package in common.</span></span></p>
<p><strong><span data-ttu-id="6784b-282">Esempio </strong> : è possibile abilitare un pacchetto con Microsoft Office per tutti gli utenti, ma abilitare diversi pacchetti facoltativi, che contengono diversi plug-in di Office, per i diversi sottoinsiemi di utenti.</span><span class="sxs-lookup"><span data-stu-id="6784b-282">Example</strong>: You can enable a package with Microsoft Office for all users, but enable different optional packages, which contain different Office plug-ins, to different subsets of users.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="6784b-283">Come usare i pacchetti facoltativi nei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="6784b-283">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-284">Annullare la pubblicazione o eliminare un pacchetto facoltativo senza modificare il gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="6784b-284">Unpublish or delete an optional package without changing the connection group</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-285">Annullare la pubblicazione o eliminare o annullare la pubblicazione e pubblicare di nuovo un pacchetto facoltativo, che si trova in un gruppo di connessioni, senza dover disabilitare o riabilitare il gruppo di connessioni nel client App-V.</span><span class="sxs-lookup"><span data-stu-id="6784b-285">Unpublish or delete, or unpublish and republish an optional package, which is in a connection group, without having to disable or re-enable the connection group on the App-V client.</span></span></p></td>
<td align="left"><p><a href="how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups.md#bkmk-apps-plugs-optional)"><span data-ttu-id="6784b-286">Come usare i pacchetti facoltativi nei gruppi di connessione</span><span class="sxs-lookup"><span data-stu-id="6784b-286">How to Use Optional Packages in Connection Groups</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-287">Pubblicare i gruppi di connessioni che contengono i pacchetti pubblicati dall'utente e pubblicati globalmente</span><span class="sxs-lookup"><span data-stu-id="6784b-287">Publish connection groups that contain user-published and globally published packages</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-288">Creare un gruppo di connessioni pubblicato dall'utente che contiene i pacchetti pubblicati dall'utente e pubblicati globalmente.</span><span class="sxs-lookup"><span data-stu-id="6784b-288">Create a user-published connection group that contains user-published and globally published packages.</span></span></p></td>
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="6784b-289">Come creare un gruppo di connessione con pacchetti pubblicati dall'utente e pubblicati globalmente</span><span class="sxs-lookup"><span data-stu-id="6784b-289">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-290">Creare un gruppo di connessioni ignorare la versione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="6784b-290">Make a connection group ignore the package version</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-291">Configurare un gruppo di connessioni per accettare qualsiasi versione di un pacchetto, che consente di aggiornare un pacchetto senza dover disabilitare il gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6784b-291">Configure a connection group to accept any version of a package, which enables you to upgrade a package without having to disable the connection group.</span></span> <span data-ttu-id="6784b-292">Inoltre, se c'è un pacchetto facoltativo con una versione non corretta nel gruppo di connessioni, il pacchetto viene ignorato e non bloccherà l'ambiente virtuale del gruppo di connessioni da creare.</span><span class="sxs-lookup"><span data-stu-id="6784b-292">In addition, if there is an optional package with an incorrect version in the connection group, the package is ignored and won’t block the connection group’s virtual environment from being created.</span></span></p></td>
<td align="left"><p><a href="how-to-make-a-connection-group-ignore-the-package-version.md" data-raw-source="[How to Make a Connection Group Ignore the Package Version](how-to-make-a-connection-group-ignore-the-package-version.md)"><span data-ttu-id="6784b-293">Come impostare un gruppo di connessione in modo che ignori la versione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="6784b-293">How to Make a Connection Group Ignore the Package Version</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-294">Limitare le funzionalità di pubblicazione degli utenti finali</span><span class="sxs-lookup"><span data-stu-id="6784b-294">Limit end users’ publishing capabilities</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-295">Consente solo agli amministratori (non agli utenti finali) di pubblicare pacchetti e di abilitare i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6784b-295">Enable only administrators (not end users) to publish packages and to enable connection groups.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-296">Per informazioni sui gruppi di connessioni, vedere <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)"> come consentire solo agli amministratori di abilitare i gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="6784b-296">For information about connection groups, see <a href="how-to-allow-only-administrators-to-enable-connection-groups.md" data-raw-source="[How to Allow Only Administrators to Enable Connection Groups](how-to-allow-only-administrators-to-enable-connection-groups.md)">How to Allow Only Administrators to Enable Connection Groups</span></span></a></p>
<p><span data-ttu-id="6784b-297">Per informazioni sui pacchetti, vedere gli articoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="6784b-297">For information about packages, see the following articles:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-298">Metodo</span><span class="sxs-lookup"><span data-stu-id="6784b-298">Method</span></span></th>
<th align="left"><span data-ttu-id="6784b-299">Collegamento ad altre informazioni</span><span class="sxs-lookup"><span data-stu-id="6784b-299">Link to more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-300">Console di gestione</span><span class="sxs-lookup"><span data-stu-id="6784b-300">Management console</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-50.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-50.md)"><span data-ttu-id="6784b-301">Come pubblicare un pacchetto tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="6784b-301">How to Publish a Package by Using the Management Console</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-302">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6784b-302">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admin-only-posh-topic-cg)"><span data-ttu-id="6784b-303">Come gestire i gruppi di connessione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="6784b-303">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-304">Sistema di distribuzione elettronica software di terze parti</span><span class="sxs-lookup"><span data-stu-id="6784b-304">Third-party electronic software delivery system</span></span></p></td>
<td align="left"><p><a href="how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md" data-raw-source="[How to Enable Only Administrators to Publish Packages by Using an ESD](how-to-enable-only-administrators-to-publish-packages-by-using-an-esd.md)"><span data-ttu-id="6784b-305">Come consentire solo agli amministratori di pubblicare i pacchetti con ESD</span><span class="sxs-lookup"><span data-stu-id="6784b-305">How to Enable Only Administrators to Publish Packages by Using an ESD</span></span></a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-306">Abilitare o disabilitare un gruppo di connessioni per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="6784b-306">Enable or disable a connection group for a specific user</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-307">Gli amministratori possono abilitare o disabilitare un gruppo di connessioni per un utente specifico usando il <strong> parametro facoltativo-UserSID </strong> con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="6784b-307">Administrators can enable or disable a connection group for a specific user by using the optional <strong>–UserSID</strong> parameter with the following cmdlets:</span></span></p>
<ul>
<li><p><span data-ttu-id="6784b-308">Enable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="6784b-308">Enable-AppVClientConnectionGroup</span></span></p></li>
<li><p><span data-ttu-id="6784b-309">Disable-AppVClientConnectionGroup</span><span class="sxs-lookup"><span data-stu-id="6784b-309">Disable-AppVClientConnectionGroup</span></span></p></li>
</ul></td>
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell.md#bkmk-enable-cg-for-user-poshtopic)"><span data-ttu-id="6784b-310">Come gestire i gruppi di connessione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="6784b-310">How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-311">Unione di percorsi di pacchetto identici in una directory virtuale in gruppi di connessioni</span><span class="sxs-lookup"><span data-stu-id="6784b-311">Merging identical package paths into one virtual directory in connection groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-312">Se due o più pacchetti in un gruppo di connessioni contengono percorsi di directory identici, i percorsi vengono uniti in un'unica directory virtuale all'interno dell'ambiente virtuale del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6784b-312">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span></p>
<p><span data-ttu-id="6784b-313">Questa unione di percorsi consente a un'applicazione in un pacchetto di accedere ai file che si trovano in un pacchetto diverso.</span><span class="sxs-lookup"><span data-stu-id="6784b-313">This merging of paths allows an application in one package to access files that are in a different package.</span></span></p></td>
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md#bkmk-merged-root-ve-exp)"><span data-ttu-id="6784b-314">Informazioni sull'ambiente virtuale del gruppo di connessione</span><span class="sxs-lookup"><span data-stu-id="6784b-314">About the Connection Group Virtual Environment</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-usersid-pub-pkgs-specf-user"></a><span data-ttu-id="6784b-315">Gli amministratori possono pubblicare e annullare la pubblicazione di pacchetti per un utente specifico</span><span class="sxs-lookup"><span data-stu-id="6784b-315">Administrators can publish and unpublish packages for a specific user</span></span>


<span data-ttu-id="6784b-316">Gli amministratori possono usare i cmdlet seguenti per pubblicare o annullare la pubblicazione di pacchetti per un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="6784b-316">Administrators can use the following cmdlets to publish or unpublish packages for a specific user.</span></span> <span data-ttu-id="6784b-317">Per usare i cmdlet, immettere il parametro **– UserSID** , seguito dall'identificatore di sicurezza dell'utente (SID).</span><span class="sxs-lookup"><span data-stu-id="6784b-317">To use the cmdlets, enter the **–UserSID** parameter, followed by the user’s security identifier (SID).</span></span> <span data-ttu-id="6784b-318">Per altre informazioni, vedi:</span><span class="sxs-lookup"><span data-stu-id="6784b-318">For more information, see:</span></span>

-   [<span data-ttu-id="6784b-319">Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="6784b-319">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-pub-pkg-a-user-standalone-posh)

-   [<span data-ttu-id="6784b-320">Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="6784b-320">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span>](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-unpub-pkg-specfc-use)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-321">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6784b-321">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="6784b-322">Esempi</span><span class="sxs-lookup"><span data-stu-id="6784b-322">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-323">Publish-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6784b-323">Publish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-324">Publish-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="6784b-324">Publish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-325">Annulla pubblicazione-AppvClientPackage</span><span class="sxs-lookup"><span data-stu-id="6784b-325">Unpublish-AppvClientPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-326">UNPUBLISH-AppvClientPackage "ContosoApplication"-UserSID S-1-2-34-56789012-3456789012-345678901-2345</span><span class="sxs-lookup"><span data-stu-id="6784b-326">Unpublish-AppvClientPackage “ContosoApplication” -UserSID S-1-2-34-56789012-3456789012-345678901-2345</span></span></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-admins-only-pub-unpub-pkgs"></a><span data-ttu-id="6784b-327">Consentire solo agli amministratori di pubblicare e annullare la pubblicazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="6784b-327">Enable only administrators to publish and unpublish packages</span></span>


<span data-ttu-id="6784b-328">È possibile abilitare solo gli amministratori (non gli utenti finali) a pubblicare e annullare la pubblicazione di pacchetti usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6784b-328">You can enable only administrators (not end users) to publish and unpublish packages by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-329">Metodo</span><span class="sxs-lookup"><span data-stu-id="6784b-329">Method</span></span></th>
<th align="left"><span data-ttu-id="6784b-330">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="6784b-330">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-331">Impostazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6784b-331">Group Policy setting</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-332">Passare al nodo oggetto Criteri di gruppo seguente:</span><span class="sxs-lookup"><span data-stu-id="6784b-332">Navigate to the following Group Policy Object node:</span></span></p>
<p><strong><span data-ttu-id="6784b-333">Criteri di configurazione del computer &gt; &gt; modelli amministrativi &gt; &gt; App-V &gt; Publishing </strong> .</span><span class="sxs-lookup"><span data-stu-id="6784b-333">Computer Configuration &gt; Policies &gt; Administrative Templates &gt; System &gt; App-V &gt; Publishing</strong>.</span></span></p>
<p><span data-ttu-id="6784b-334">Abilitare l' <strong> impostazione Richiedi i criteri di gruppo pubblica come amministratore </strong> .</span><span class="sxs-lookup"><span data-stu-id="6784b-334">Enable the <strong>Require publish as administrator</strong> Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-335">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6784b-335">PowerShell</span></span></p></td>
<td align="left"><p><a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md#bkmk-admins-pub-pkgs)"><span data-ttu-id="6784b-336">Come gestire i pacchetti App-V 5.0 in esecuzione in un computer autonomo con PowerShell</span><span class="sxs-lookup"><span data-stu-id="6784b-336">How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell</span></span></a></p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-runvirtual-reg-key"></a><span data-ttu-id="6784b-337">La chiave del registro di sistema RunVirtual supporta i pacchetti pubblicati per l'utente</span><span class="sxs-lookup"><span data-stu-id="6784b-337">RunVirtual registry key supports packages that are published to the user</span></span>


<span data-ttu-id="6784b-338">App-V 5,0 SP3 aggiunge il supporto per l'uso della chiave del registro di sistema **RunVirtual** con le applicazioni virtualizzate presenti nei pacchetti pubblicati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="6784b-338">App-V 5.0 SP3 adds support for using the **RunVirtual** registry key with virtualized applications that are in user-published packages.</span></span> <span data-ttu-id="6784b-339">La chiave del registro di sistema **RunVirtual** consente di eseguire un'applicazione installata localmente in un ambiente virtuale, insieme alle applicazioni virtualizzate tramite App-V.</span><span class="sxs-lookup"><span data-stu-id="6784b-339">The **RunVirtual** registry key lets you run a locally installed application in a virtual environment, along with applications that have been virtualized by using App-V.</span></span>

<span data-ttu-id="6784b-340">In precedenza, le applicazioni virtualizzate nei pacchetti App-V dovevano essere pubblicate globalmente.</span><span class="sxs-lookup"><span data-stu-id="6784b-340">Previously, the virtualized applications in App-V packages had to be published globally.</span></span> <span data-ttu-id="6784b-341">Per altre informazioni su **RunVirtual** e su altri metodi di gestione delle applicazioni installate localmente in un ambiente virtuale con applicazioni virtualizzate, vedere [eseguire un'applicazione installata localmente in un ambiente virtuale con applicazioni virtualizzate](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span><span class="sxs-lookup"><span data-stu-id="6784b-341">For more about **RunVirtual** and about other methods of running locally installed applications in a virtual environment with virtualized applications, see [Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md).</span></span>

## <a href="" id="bkmk-posh-cmdlets-help"></a><span data-ttu-id="6784b-342">Guida di nuovi cmdlet di PowerShell e cmdlet aggiornabile</span><span class="sxs-lookup"><span data-stu-id="6784b-342">New PowerShell cmdlets and updateable cmdlet help</span></span>


<span data-ttu-id="6784b-343">I nuovi cmdlet di PowerShell e la guida per i cmdlet aggiornabili sono inclusi in App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="6784b-343">New PowerShell cmdlets and updateable cmdlet help are included in App-V 5.0 SP3.</span></span> <span data-ttu-id="6784b-344">Per scaricare i moduli cmdlet, vedere [come caricare i cmdlet di PowerShell e ottenere la guida per i cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span><span class="sxs-lookup"><span data-stu-id="6784b-344">To download the cmdlet modules, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md#bkmk-load-cmdlets).</span></span>

### <span data-ttu-id="6784b-345">Nuovi cmdlet di PowerShell per server App-V 5,0 SP3</span><span class="sxs-lookup"><span data-stu-id="6784b-345">New App-V 5.0 SP3 Server PowerShell cmdlets</span></span>

<span data-ttu-id="6784b-346">Sono stati aggiunti nuovi cmdlet di Windows PowerShell per App-V Server per gestire i gruppi di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6784b-346">New Windows PowerShell cmdlets for the App-V Server have been added to help you manage connection groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-347">Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6784b-347">Cmdlet</span></span></th>
<th align="left"><span data-ttu-id="6784b-348">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6784b-348">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-349">Add-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="6784b-349">Add-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-350">Accoda un pacchetto alla fine di un gruppo di connessioni&#39;elenco di pacchetti s e consente di configurare il pacchetto come facoltativo e/o senza una versione all'interno del gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6784b-350">Appends a package to the end of a connection group&#39;s package list and enables you to configure the package as optional and/or with no version within the connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-351">Set-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="6784b-351">Set-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-352">Consente di modificare i dettagli del pacchetto del gruppo di connessioni, ad esempio se è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6784b-352">Enables you to edit details about the connection group package, such as whether it is optional.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-353">Remove-AppvServerConnectionGroupPackage</span><span class="sxs-lookup"><span data-stu-id="6784b-353">Remove-AppvServerConnectionGroupPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-354">Rimuove un pacchetto da un gruppo di connessioni.</span><span class="sxs-lookup"><span data-stu-id="6784b-354">Removes a package from a connection group.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-get-cmdlet-help"></a><span data-ttu-id="6784b-355">Ottenere assistenza per i cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="6784b-355">Getting help for the PowerShell cmdlets</span></span>

<span data-ttu-id="6784b-356">La guida per i cmdlet è disponibile nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="6784b-356">Cmdlet help is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-357">Formato</span><span class="sxs-lookup"><span data-stu-id="6784b-357">Format</span></span></th>
<th align="left"><span data-ttu-id="6784b-358">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6784b-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-359">Come modulo scaricabile</span><span class="sxs-lookup"><span data-stu-id="6784b-359">As a downloadable module</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-360">Per ottenere la guida più recente dopo il download del modulo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="6784b-360">To get the latest help after downloading the cmdlet module:</span></span></p>
<ol>
<li><p><span data-ttu-id="6784b-361">Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="6784b-361">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span></p></li>
<li><p><span data-ttu-id="6784b-362">Digitare uno dei comandi seguenti per caricare i cmdlet per il modulo desiderato:</span><span class="sxs-lookup"><span data-stu-id="6784b-362">Type one of the following commands to load the cmdlets for the module you want:</span></span></p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-363">Componente App-V</span><span class="sxs-lookup"><span data-stu-id="6784b-363">App-V component</span></span></th>
<th align="left"><span data-ttu-id="6784b-364">Comando per digitare</span><span class="sxs-lookup"><span data-stu-id="6784b-364">Command to type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-365">App-V Server</span><span class="sxs-lookup"><span data-stu-id="6784b-365">App-V Server</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-366">Update-Guida-modulo AppvServer</span><span class="sxs-lookup"><span data-stu-id="6784b-366">Update-Help-Module AppvServer</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-367">Sequencer App-V</span><span class="sxs-lookup"><span data-stu-id="6784b-367">App-V Sequencer</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-368">Update-Guida-modulo AppvSequencer</span><span class="sxs-lookup"><span data-stu-id="6784b-368">Update-Help-Module AppvSequencer</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-369">Client App-V</span><span class="sxs-lookup"><span data-stu-id="6784b-369">App-V client</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-370">Update-Guida-modulo AppvClient</span><span class="sxs-lookup"><span data-stu-id="6784b-370">Update-Help-Module AppvClient</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-371">In TechNet come pagine Web</span><span class="sxs-lookup"><span data-stu-id="6784b-371">On TechNet as web pages</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-372">Vedere il nodo App-V in <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automazione di Microsoft Desktop Optimization Pack con Windows PowerShell </a> .</span><span class="sxs-lookup"><span data-stu-id="6784b-372">See the App-V node under <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)">Microsoft Desktop Optimization Pack Automation with Windows PowerShell</a>.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="6784b-373">Per altre informazioni, vedere [come caricare i cmdlet di PowerShell e ottenere la guida per i cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span><span class="sxs-lookup"><span data-stu-id="6784b-373">For more information, see [How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-50-sp3.md).</span></span>

## <a href="" id="bkmk-pvad-hidden"></a><span data-ttu-id="6784b-374">La directory delle applicazioni virtuali primarie (PVAD) è nascosta ma può essere attivata</span><span class="sxs-lookup"><span data-stu-id="6784b-374">Primary virtual application directory (PVAD) is hidden but can be turned on</span></span>


<span data-ttu-id="6784b-375">La directory delle applicazioni virtuali primarie (PVAD) è nascosta in App-V 5,0 SP3, ma è possibile riattivarla e renderla visibile usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6784b-375">The primary virtual application directory (PVAD) is hidden in App-V 5.0 SP3, but you can turn it back on and make it visible by using one of the following methods:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-376">Metodo</span><span class="sxs-lookup"><span data-stu-id="6784b-376">Method</span></span></th>
<th align="left"><span data-ttu-id="6784b-377">Passaggi</span><span class="sxs-lookup"><span data-stu-id="6784b-377">Steps</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6784b-378">Usare un parametro della riga di comando</span><span class="sxs-lookup"><span data-stu-id="6784b-378">Use a command line parameter</span></span></p></td>
<td align="left"><p><span data-ttu-id="6784b-379">Passare il <strong> parametro – EnablePVADControl </strong> al <strong>Sequencer.exe</strong> .</span><span class="sxs-lookup"><span data-stu-id="6784b-379">Pass the <strong>–EnablePVADControl</strong> parameter to the <strong>Sequencer.exe</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6784b-380">Creare una sottochiave del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="6784b-380">Create a registry subkey</span></span></p></td>
<td align="left"><ol>
<li><p><span data-ttu-id="6784b-381">Nell'editor del registro di sistema passare a:</span><span class="sxs-lookup"><span data-stu-id="6784b-381">In the Registry Editor, navigate to:</span></span> <code>HKLM\SOFTWARE\Microsoft\AppV\Sequencer\Compatibility</code></p>
<div class="alert">
<strong><span data-ttu-id="6784b-382">Nota</span><span class="sxs-lookup"><span data-stu-id="6784b-382">Note</span></span></strong><br/><p><span data-ttu-id="6784b-383">Se la <code>Compatibility</code> sottochiave non esiste, è necessario crearla.</span><span class="sxs-lookup"><span data-stu-id="6784b-383">If the <code>Compatibility</code> subkey doesn’t exist, you must create it.</span></span></p>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="6784b-384">Crea un valore DWORD denominato <strong> EnablePVADControl </strong> e imposta il valore su <strong> 1 </strong> .</span><span class="sxs-lookup"><span data-stu-id="6784b-384">Create a DWORD Value named <strong>EnablePVADControl</strong>, and set the value to <strong>1</strong>.</span></span></p>
<p><span data-ttu-id="6784b-385">Un valore pari a <strong> 0 </strong> indica che PVAD è nascosto.</span><span class="sxs-lookup"><span data-stu-id="6784b-385">A value of <strong>0</strong> means that PVAD is hidden.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>



<span data-ttu-id="6784b-386">**Altre informazioni su PVAD:** Quando si usa sequencer per creare un pacchetto, è possibile immettere qualsiasi percorso di installazione per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6784b-386">**More about PVAD:** When you use the Sequencer to create a package, you can enter any installation path for the package.</span></span> <span data-ttu-id="6784b-387">Nelle versioni precedenti di App-V era necessario specificare la directory dell'applicazione virtuale primaria (PVAD) dell'applicazione come percorso.</span><span class="sxs-lookup"><span data-stu-id="6784b-387">In past versions of App-V, you were required to specify the primary virtual application directory (PVAD) of the application as the path.</span></span> <span data-ttu-id="6784b-388">PVAD è la directory in cui in genere si installa un'applicazione nel computer locale se non si usa l'App-V.</span><span class="sxs-lookup"><span data-stu-id="6784b-388">PVAD is the directory to which you would typically install an application on your local computer if you weren’t using App-V.</span></span> <span data-ttu-id="6784b-389">Ad esempio, se si sta installando Office in un computer, il PVAD in genere sarebbe C:\\Programmi \\Programmi\\microsoft Office\\.</span><span class="sxs-lookup"><span data-stu-id="6784b-389">For example, if you were installing Office on a computer, the PVAD typically would be C:\\Program Files\\Microsoft Office\\.</span></span>

## <a href="" id="bkmk-pub-metadata-clientversion"></a><span data-ttu-id="6784b-390">ClientVersion è necessario per visualizzare i metadati di pubblicazione di App-V</span><span class="sxs-lookup"><span data-stu-id="6784b-390">ClientVersion is required to view App-V publishing metadata</span></span>


<span data-ttu-id="6784b-391">In App-V 5,0 SP3 è necessario specificare i valori seguenti nell'indirizzo quando si esegue una query sul server di pubblicazione App-V per i metadati:</span><span class="sxs-lookup"><span data-stu-id="6784b-391">In App-V 5.0 SP3, you must provide the following values in the address when you query the App-V Publishing server for metadata:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6784b-392">Value</span><span class="sxs-lookup"><span data-stu-id="6784b-392">Value</span></span></th>
<th align="left"><span data-ttu-id="6784b-393">Ulteriori dettagli</span><span class="sxs-lookup"><span data-stu-id="6784b-393">Additional details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="6784b-394">ClientVersion</span><span class="sxs-lookup"><span data-stu-id="6784b-394">ClientVersion</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6784b-395">Se si omette il <strong> </strong> parametro ClientVersion dalla query, i metadati escludono le nuove funzionalità App-V 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="6784b-395">If you omit the <strong>ClientVersion</strong> parameter from the query, the metadata excludes the new App-V 5.0 SP3 features.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="6784b-396">Clientos</span><span class="sxs-lookup"><span data-stu-id="6784b-396">ClientOS</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="6784b-397">È necessario specificare questo valore solo se si selezionano sistemi operativi client specifici quando si sequenzia il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6784b-397">You have to provide this value only if you select specific client operating systems when you sequence the package.</span></span> <span data-ttu-id="6784b-398">Se si seleziona l'impostazione predefinita (tutti i sistemi operativi), non specificare questo valore nella query.</span><span class="sxs-lookup"><span data-stu-id="6784b-398">If you select the default (all operating systems), do not specify this value in the query.</span></span></p>
<p><span data-ttu-id="6784b-399">Se si omette il <strong> parametro clientos </strong> dalla query, solo i pacchetti sequenziati per supportare qualsiasi sistema operativo verranno visualizzati nei metadati.</span><span class="sxs-lookup"><span data-stu-id="6784b-399">If you omit the <strong>ClientOS</strong> parameter from the query, only the packages that were sequenced to support any operating system appear in the metadata.</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="6784b-400">Per la sintassi e gli esempi di questa query, vedere [visualizzazione dei metadati di pubblicazione di App-V Server](viewing-app-v-server-publishing-metadata.md).</span><span class="sxs-lookup"><span data-stu-id="6784b-400">For syntax and examples of this query, see [Viewing App-V Server Publishing Metadata](viewing-app-v-server-publishing-metadata.md).</span></span>

## <a href="" id="bkmk-event-logs-moved"></a><span data-ttu-id="6784b-401">I registri eventi App-V sono stati consolidati</span><span class="sxs-lookup"><span data-stu-id="6784b-401">App-V event logs have been consolidated</span></span>


<span data-ttu-id="6784b-402">I registri eventi seguenti, precedentemente presenti nei **registri delle applicazioni e dei servizi/Microsoft/appv/ &lt; app- &gt; V Component**, sono stati spostati in **registri applicazioni e servizi/Microsoft/appv/ServiceLog**.</span><span class="sxs-lookup"><span data-stu-id="6784b-402">The following event logs, previously located at **Applications and Services Logs/Microsoft/AppV/&lt;App-V component&gt;**, have been moved to **Applications and Services Logs/Microsoft/AppV/ServiceLog**.</span></span>

<span data-ttu-id="6784b-403">Per visualizzare i registri, selezionare Visualizza **Mostra** i &gt; **registri analitici e di debug** nell'applicazione Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="6784b-403">To view the logs, select **View** &gt; **Show Analytic and Debug Logs** in the Event Viewer application.</span></span>

<span data-ttu-id="6784b-404">Client per il catalogo client-client di integrazione-client di orchestrazione-client di PackageConfig-client di scripting-client di servizi-Vemgr client-VFSC FilesystemMetadataLibrary ManifestLibrary sottosistemi PolicyLibrary-sottosistemi ActiveX-sottosistemi di sistema-sottosistemi-com-FTA</span><span class="sxs-lookup"><span data-stu-id="6784b-404">Client-Catalog Client-Integration Client-Orchestration Client-PackageConfig Client-Scripting Client-Service Client-Vemgr Client-VFSC FilesystemMetadataLibrary ManifestLibrary PolicyLibrary Subsystems-ActiveX Subsystems-AppPath Subsystems-Com Subsystems-fta</span></span>

## <span data-ttu-id="6784b-405">Come ottenere le tecnologie MDOP</span><span class="sxs-lookup"><span data-stu-id="6784b-405">How to Get MDOP Technologies</span></span>


<span data-ttu-id="6784b-406">App-V fa parte di Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="6784b-406">App-V is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="6784b-407">MDOP fa parte di Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="6784b-407">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="6784b-408">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="6784b-408">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>






## <span data-ttu-id="6784b-409">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6784b-409">Related topics</span></span>


[<span data-ttu-id="6784b-410">Note sulla versione di App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6784b-410">Release Notes for App-V 5.0 SP3</span></span>](release-notes-for-app-v-50-sp3.md)









