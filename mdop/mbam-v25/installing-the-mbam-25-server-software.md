---
title: Installazione del software per il server di MBAM 2.5
description: Installazione del software per il server di MBAM 2.5
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823395"
---
# <span data-ttu-id="e7a19-103">Installazione del software per il server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e7a19-103">Installing the MBAM 2.5 Server Software</span></span>


<span data-ttu-id="e7a19-104">Questo argomento descrive come installare il software per server di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,5 usando la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker o usando i parametri della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="e7a19-104">This topic describes how to install the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard or by using command-line parameters.</span></span> <span data-ttu-id="e7a19-105">Ripetere il processo di installazione del server per ogni server in cui si stanno configurando le caratteristiche del server MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="e7a19-105">Repeat the server installation process for each server on which you are configuring MBAM 2.5 Server features.</span></span> <span data-ttu-id="e7a19-106">Dopo aver completato l'installazione, vedere [configurazione delle funzionalità del server MBAM 2,5](configuring-the-mbam-25-server-features.md) per la procedura relativa alla configurazione delle funzionalità del server.</span><span class="sxs-lookup"><span data-stu-id="e7a19-106">After you finish the installation, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md) for steps about configuring the Server features.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e7a19-107">Prima di iniziare</span><span class="sxs-lookup"><span data-stu-id="e7a19-107">Before you start</span></span></th>
<th align="left"><span data-ttu-id="e7a19-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7a19-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7a19-109">Esaminare le informazioni sulla pianificazione di MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="e7a19-109">Review the MBAM 2.5 planning information</span></span></p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)"><span data-ttu-id="e7a19-110">Prerequisiti del server di MBAM 2.5 per le topologie di integrazione autonome e di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="e7a19-110">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span></a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)"><span data-ttu-id="e7a19-111">Configurazioni supportate di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e7a19-111">MBAM 2.5 Supported Configurations</span></span></a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)"><span data-ttu-id="e7a19-112">Architettura di alto livello per MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e7a19-112">High-Level Architecture for MBAM 2.5</span></span></a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7a19-113">Informazioni su come recuperare i file di log</span><span class="sxs-lookup"><span data-stu-id="e7a19-113">Read how to get log files</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7a19-114">Per impostazione predefinita, i file di log vengono creati nella cartella% Temp% del computer locale.</span><span class="sxs-lookup"><span data-stu-id="e7a19-114">By default, log files are created in the local computer’s %temp% folder.</span></span> <span data-ttu-id="e7a19-115">Per scrivere i file di log in una posizione specifica anziché nella <strong> cartella% Temp </strong> %, usare l' <strong> </strong> &lt; <em> argomento posizione/log </em> &gt; .</span><span class="sxs-lookup"><span data-stu-id="e7a19-115">To write the log files to a specific location rather than to the <strong>%temp</strong>% folder, use the <strong>/log</strong> &lt;<em>location</em>&gt; argument.</span></span></p>
<p><span data-ttu-id="e7a19-116">Altri eventi potrebbero essere registrati nel Visualizzatore eventi nei <strong> nodi di mbam-setup </strong> o <strong> mbam-Web in </strong> <strong> applicazioni e servizi per i registri di &gt; Microsoft &gt; Windows </strong> .</span><span class="sxs-lookup"><span data-stu-id="e7a19-116">Additional events might be logged in Event Viewer in the <strong>MBAM-Setup</strong> or <strong>MBAM-Web</strong> nodes under <strong>Applications and Services Logs &gt; Microsoft &gt; Windows</strong>.</span></span> <span data-ttu-id="e7a19-117">Ad esempio, se si disinstalla MBAM, il programma di disinstallazione disinstallerà anche MBAM-Setup e MBAM-web logs in EventViewer.</span><span class="sxs-lookup"><span data-stu-id="e7a19-117">For example, if you uninstall MBAM, the uninstaller will also uninstall the MBAM-Setup and MBAM-Web logs in EventViewer.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="e7a19-118">Installazione del software MBAM 2,5 Server tramite la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker</span><span class="sxs-lookup"><span data-stu-id="e7a19-118">Installing the MBAM 2.5 Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard</span></span>


<span data-ttu-id="e7a19-119">Seguire questa procedura per installare il software MBAM server usando la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e7a19-119">Use these steps to install the MBAM Server software by using the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

**<span data-ttu-id="e7a19-120">Per installare il software del server MBAM 2,5 tramite la procedura guidata</span><span class="sxs-lookup"><span data-stu-id="e7a19-120">To install the MBAM 2.5 Server software by using the wizard</span></span>**

1.  <span data-ttu-id="e7a19-121">Nel server in cui si vuole installare MBAM eseguire **MBAMserversetup.exe** per avviare la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e7a19-121">On the server where you want to install MBAM, run **MBAMserversetup.exe** to start the Microsoft BitLocker Administration and Monitoring Setup wizard.</span></span>

2.  <span data-ttu-id="e7a19-122">Nella pagina di **benvenuto** fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e7a19-122">On the **Welcome** page, click **Next**.</span></span>

3.  <span data-ttu-id="e7a19-123">Leggere e accettare il contratto di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e7a19-123">Read and accept the Microsoft Software License Agreement, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="e7a19-124">Scegliere se usare Microsoft Update quando si controllano gli aggiornamenti e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e7a19-124">Choose whether to use Microsoft Update when you check for updates, and then click **Next**.</span></span>

5.  <span data-ttu-id="e7a19-125">Scegliere se partecipare al programma Analisi utilizzo software e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="e7a19-125">Choose whether to participate in the Customer Experience Improvement Program, and then click **Next**.</span></span>

6.  <span data-ttu-id="e7a19-126">Per avviare l'installazione, fare clic su **Installa**.</span><span class="sxs-lookup"><span data-stu-id="e7a19-126">To start the installation, click **Install**.</span></span>

7.  <span data-ttu-id="e7a19-127">Per configurare le caratteristiche del server dopo l'installazione del software MBAM server, selezionare la casella di controllo **Esegui la configurazione del server mbam dopo la chiusura della procedura guidata** .</span><span class="sxs-lookup"><span data-stu-id="e7a19-127">To configure the server features after the MBAM Server software finishes installing, select the **Run MBAM Server Configuration after the wizard closes** check box.</span></span> <span data-ttu-id="e7a19-128">In alternativa, è possibile configurare MBAM in seguito usando il collegamento di **configurazione del server mbam** creato dall'installazione del server nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="e7a19-128">Alternatively, you can configure MBAM later by using the **MBAM Server Configuration** shortcut that the server installation creates on your **Start** menu.</span></span>

8.  <span data-ttu-id="e7a19-129">Fai clic su **Fine**.</span><span class="sxs-lookup"><span data-stu-id="e7a19-129">Click **Finish**.</span></span>

## <span data-ttu-id="e7a19-130">Installazione del software del server MBAM 2,5 tramite una finestra del prompt dei comandi</span><span class="sxs-lookup"><span data-stu-id="e7a19-130">Installing the MBAM 2.5 Server software by using a Command Prompt window</span></span>


<span data-ttu-id="e7a19-131">Al prompt dei comandi digitare un comando simile al comando seguente per installare il software del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="e7a19-131">At a command prompt, type a command similar to the following command to install the MBAM Server software.</span></span>

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

<span data-ttu-id="e7a19-132">La tabella seguente descrive i parametri della riga di comando per l'installazione del software del server MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="e7a19-132">The following table describes the command-line parameters for installing the MBAM 2.5 Server software.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e7a19-133">Parametro</span><span class="sxs-lookup"><span data-stu-id="e7a19-133">Parameter</span></span></th>
<th align="left"><span data-ttu-id="e7a19-134">Valore di parametro</span><span class="sxs-lookup"><span data-stu-id="e7a19-134">Parameter value</span></span></th>
<th align="left"><span data-ttu-id="e7a19-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7a19-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7a19-136">CEIPENABLED</span><span class="sxs-lookup"><span data-stu-id="e7a19-136">CEIPENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7a19-137">True false</span><span class="sxs-lookup"><span data-stu-id="e7a19-137">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7a19-138">Vero-partecipare al programma di Customer Improvement Experience, che consente a Microsoft di identificare quali funzionalità di MBAM migliorare.</span><span class="sxs-lookup"><span data-stu-id="e7a19-138">True - participate in the Customer Improvement Experience Program, which helps Microsoft identify which MBAM features to improve.</span></span></p>
<p><span data-ttu-id="e7a19-139">Falso: non partecipare al programma esperienza di miglioramento del cliente.</span><span class="sxs-lookup"><span data-stu-id="e7a19-139">False – do not participate in the Customer Improvement Experience Program.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7a19-140">OPTIN_FOR_MICROSOFT_UPDATES</span><span class="sxs-lookup"><span data-stu-id="e7a19-140">OPTIN_FOR_MICROSOFT_UPDATES</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7a19-141">True false</span><span class="sxs-lookup"><span data-stu-id="e7a19-141">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7a19-142">True: usare Microsoft Update per proteggere il computer e aggiornarlo per Windows e altri prodotti Microsoft, tra cui MBAM.</span><span class="sxs-lookup"><span data-stu-id="e7a19-142">True - use Microsoft Update to keep your computer secure and up-to-date for Windows and other Microsoft products, including MBAM.</span></span></p>
<p><span data-ttu-id="e7a19-143">Falso: non usare Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="e7a19-143">False – do not use Microsoft Update</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e7a19-144">INSTALLDIR</span><span class="sxs-lookup"><span data-stu-id="e7a19-144">INSTALLDIR</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7a19-145">&lt;Percorso&gt;</span><span class="sxs-lookup"><span data-stu-id="e7a19-145">&lt;Path&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7a19-146">Posizione in cui si vuole installare MBAM.</span><span class="sxs-lookup"><span data-stu-id="e7a19-146">Location where you want to install MBAM.</span></span></p>
<p><span data-ttu-id="e7a19-147">Esempio:</span><span class="sxs-lookup"><span data-stu-id="e7a19-147">Example:</span></span></p>
<p><span data-ttu-id="e7a19-148">INSTALLDIR = c:\mbaminstall</span><span class="sxs-lookup"><span data-stu-id="e7a19-148">INSTALLDIR=c:\mbaminstall</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e7a19-149">FORCE_UNINSTALL</span><span class="sxs-lookup"><span data-stu-id="e7a19-149">FORCE_UNINSTALL</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7a19-150">True false</span><span class="sxs-lookup"><span data-stu-id="e7a19-150">True False</span></span></p></td>
<td align="left"><p><span data-ttu-id="e7a19-151">Vero-continuare la procedura di disinstallazione di MBAM, anche se le caratteristiche non vengono rimosse.</span><span class="sxs-lookup"><span data-stu-id="e7a19-151">True - continue the process of uninstalling MBAM, even if any features fail to be removed.</span></span></p>
<p><span data-ttu-id="e7a19-152">False (impostazione predefinita) se l'azione di disinstallazione personalizzata non riesce a rimuovere una caratteristica aggiunta di MBAM server, la disinstallazione non riesce e MBAM rimane installato.</span><span class="sxs-lookup"><span data-stu-id="e7a19-152">False (default) if the uninstallation custom action fails to remove an added MBAM Server feature, the uninstallation fails, and MBAM remains installed.</span></span></p>
<p><span data-ttu-id="e7a19-153">In entrambi i casi, tutte le funzionalità che sono state rimosse correttamente durante il tentativo di disinstallare MBAM rimangono rimosse.</span><span class="sxs-lookup"><span data-stu-id="e7a19-153">In both instances, any features that were successfully removed during the attempt to uninstall MBAM stay removed.</span></span></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="e7a19-154">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7a19-154">Related topics</span></span>


[<span data-ttu-id="e7a19-155">Distribuzione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e7a19-155">Deploying MBAM 2.5</span></span>](deploying-mbam-25.md)

[<span data-ttu-id="e7a19-156">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e7a19-156">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

 

## <span data-ttu-id="e7a19-157">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="e7a19-157">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e7a19-158">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="e7a19-158">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e7a19-159">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="e7a19-159">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





