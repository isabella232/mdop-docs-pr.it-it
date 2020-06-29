---
title: Come distribuire il client di MBAM usando una riga di comando
description: Come distribuire il client di MBAM usando una riga di comando
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824486"
---
# <span data-ttu-id="b8ddc-103">Come distribuire il client di MBAM usando una riga di comando</span><span class="sxs-lookup"><span data-stu-id="b8ddc-103">How to Deploy the MBAM Client by Using a Command Line</span></span>


<span data-ttu-id="b8ddc-104">È possibile usare una riga di comando per distribuire il software client di amministrazione e monitoraggio di Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="b8ddc-104">You can use a command line to deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software.</span></span>

## <span data-ttu-id="b8ddc-105">Riga di comando per distribuire il software del client MBAM</span><span class="sxs-lookup"><span data-stu-id="b8ddc-105">Command Line to deploy the MBAM Client software</span></span>


<span data-ttu-id="b8ddc-106">Digitare il comando seguente al prompt dei comandi per accettare automaticamente il contratto di licenza con l'utente finale quando si distribuisce il software client MBAM.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-106">Type the following command at the command prompt to automatically accept the end user license agreement when deploying the MBAM Client software.</span></span>

**<span data-ttu-id="b8ddc-107">MBAMClientSetup.exe/acceptEula = Yes</span><span class="sxs-lookup"><span data-stu-id="b8ddc-107">MBAMClientSetup.exe /acceptEula=Yes</span></span>**

<span data-ttu-id="b8ddc-108">**Nota**  Le opzioni della riga di comando **/Ju** e **/JM** non sono supportate e non possono essere usate per installare il software client mbam.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-108">**Note** The **/ju** and **/jm** command-line options are not supported and cannot be used to install the MBAM Client software.</span></span>

 

<span data-ttu-id="b8ddc-109">Digitare il comando seguente al prompt dei comandi per estrarre e installare l'MSP:</span><span class="sxs-lookup"><span data-stu-id="b8ddc-109">Type the following command at the command prompt to extract and install the MSP:</span></span>

**<span data-ttu-id="b8ddc-110">MBAMClientSetup.exe &lt; percorso di/Extract per estrarre MSI &gt; /AcceptEula = Yes</span><span class="sxs-lookup"><span data-stu-id="b8ddc-110">MBAMClientSetup.exe /extract &lt;path to extract MSI&gt; /acceptEula=Yes</span></span>**

<span data-ttu-id="b8ddc-111">Installare quindi il file MSI in modo invisibile all'utente eseguendo il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="b8ddc-111">Then, install the MSI silently by running the following command:</span></span>

**<span data-ttu-id="b8ddc-112">msiexec/i &lt; path to Estratto MSI &gt; /qb ALLUSERS = 1 REBOOT = ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="b8ddc-112">msiexec /i &lt;path to extracted MSI&gt; /qb ALLUSERS=1 REBOOT=ReallySuppress</span></span>**

<span data-ttu-id="b8ddc-113">**Nota**  A partire da MBAM 2,5 SP1, un file MSI separato non è più incluso nel prodotto MBAM.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-113">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="b8ddc-114">È tuttavia possibile estrarre l'MSI dal file eseguibile (con estensione exe) incluso nel prodotto, dopo aver accettato l'EULA.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-114">However, you can extract the MSI from the executable file (.exe) that is included with the product, after accepting the EULA.</span></span>

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a><span data-ttu-id="b8ddc-115">OPTIn \ _FOR \ _MICROSOFT \ _UPDATES = 1 opzione della riga di comando</span><span class="sxs-lookup"><span data-stu-id="b8ddc-115">OPTIN\_FOR\_MICROSOFT\_UPDATES=1 command-line option</span></span>


<span data-ttu-id="b8ddc-116">Facoltativamente, è possibile specificare l'opzione della riga `OPTIN_FOR_MICROSOFT_UPDATES=1` di comando durante l'installazione del software client per installare automaticamente gli aggiornamenti Microsoft nei computer client.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-116">You can optionally specify the command-line option `OPTIN_FOR_MICROSOFT_UPDATES=1` during the Client software installation to automatically install Microsoft Updates on client computers.</span></span> <span data-ttu-id="b8ddc-117">Se specifichi questa opzione, Microsoft Update avvia automaticamente la ricerca degli aggiornamenti disponibili dopo il completamento dell'installazione del software client.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-117">Specifying this option makes Microsoft Update automatically start and search for available updates to install after the Client software installation finishes.</span></span>

<span data-ttu-id="b8ddc-118">Puoi usare questa opzione della riga di comando con uno dei metodi di installazione seguenti.</span><span class="sxs-lookup"><span data-stu-id="b8ddc-118">You can use this command-line option with either of the following installation methods.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8ddc-119">Installare il software del client MBAM usando</span><span class="sxs-lookup"><span data-stu-id="b8ddc-119">Install the MBAM Client software by using</span></span></th>
<th align="left"><span data-ttu-id="b8ddc-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="b8ddc-120">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="b8ddc-121">MBAMClientSetup.exe</span><span class="sxs-lookup"><span data-stu-id="b8ddc-121">MBAMClientSetup.exe</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b8ddc-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="b8ddc-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="b8ddc-123">msiexec/i MBAMClient.msi</span><span class="sxs-lookup"><span data-stu-id="b8ddc-123">msiexec /i MBAMClient.msi</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="b8ddc-124">msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="b8ddc-124">msiexec /i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="b8ddc-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8ddc-125">Related topics</span></span>


[<span data-ttu-id="b8ddc-126">Distribuzione del client di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="b8ddc-126">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="b8ddc-127">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="b8ddc-127">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="b8ddc-128">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="b8ddc-128">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="b8ddc-129">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="b8ddc-129">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




