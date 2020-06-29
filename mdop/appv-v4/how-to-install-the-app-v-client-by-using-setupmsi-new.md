---
title: Come installare il client App-V con Setup.msi
description: Come installare il client App-V con Setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817335"
---
# <span data-ttu-id="c0319-103">Come installare il client App-V con Setup.msi</span><span class="sxs-lookup"><span data-stu-id="c0319-103">How to Install the App-V Client by Using Setup.msi</span></span>


<span data-ttu-id="c0319-104">Questo argomento descrive come installare il client App-V usando il programma setup.msi.</span><span class="sxs-lookup"><span data-stu-id="c0319-104">This topic describes how to install the App-V client by using the setup.msi program.</span></span> <span data-ttu-id="c0319-105">Prima di installare il client App-V tramite il programma setup.msi, è necessario determinare prima di tutto se è necessario installare un software prerequisito e quindi è necessario installarlo.</span><span class="sxs-lookup"><span data-stu-id="c0319-105">Before you install the App-V client using the setup.msi program, you must first determine if any prerequisite software must be installed, and then you must install it.</span></span> <span data-ttu-id="c0319-106">Per installare il software prerequisito, vedere la sezione [installazione del software prerequisito](#prereq-sw) di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="c0319-106">To install the prerequisite software, see the [Installing Prerequisite Software](#prereq-sw) section of this topic.</span></span> <span data-ttu-id="c0319-107">Per installare il software client, vedere [installazione del client App-V tramite la sezione Setup.msi Program](#msi-setup) di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="c0319-107">To install the client software, see the [Installing the App-V Client Using the Setup.msi Program](#msi-setup) section of this topic.</span></span>

## <a href="" id="prereq-sw"></a><span data-ttu-id="c0319-108">Installazione del software prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c0319-108">Installing Prerequisite Software</span></span>


<span data-ttu-id="c0319-109">Per installare il software prerequisito, è possibile usare le procedure seguenti.</span><span class="sxs-lookup"><span data-stu-id="c0319-109">You can use the following procedures to install the prerequisite software.</span></span> <span data-ttu-id="c0319-110">Puoi creare un file di comando ed eseguire i comandi dal prompt dei comandi oppure puoi usare un linguaggio di scripting come VBScript o Windows PowerShell per eseguire i comandi.</span><span class="sxs-lookup"><span data-stu-id="c0319-110">You can create a command file and run the commands from the command prompt, or you can use a scripting language such as VBScript or Windows PowerShell to run the commands.</span></span>

<span data-ttu-id="c0319-111">**Nota**  Le versioni x86 del software seguente sono necessarie per le versioni x86 e x64 del client App-V.</span><span class="sxs-lookup"><span data-stu-id="c0319-111">**Note** The x86 versions of the following software are required for both x86 and x64 versions of the App-V client.</span></span>

 

**<span data-ttu-id="c0319-112">Per installare Microsoft VisualC + + 2005SP1 Redistributable Package (x86)</span><span class="sxs-lookup"><span data-stu-id="c0319-112">To install Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>**

1. <span data-ttu-id="c0319-113">Scaricare il pacchetto software [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) dall'area download Microsoft ( <https://go.microsoft.com/fwlink/?LinkId=119961> ).</span><span class="sxs-lookup"><span data-stu-id="c0319-113">Download the [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) software package from the Microsoft Download Center (<https://go.microsoft.com/fwlink/?LinkId=119961>).</span></span> <span data-ttu-id="c0319-114">\ [Modello di token value \] per la versione 4,5 SP2 e versioni successive del client App-V, Scarica vcredist\_x86.exe da [Microsoft Visual C++ 2005 Service Pack 1 ridistribuibile pacchetto di sicurezza ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [modello di token value \]</span><span class="sxs-lookup"><span data-stu-id="c0319-114">\[Template Token Value\] For version 4.5 SP2 and later of the App-V client, download vcredist\_x86.exe from [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360) (https://go.microsoft.com/fwlink/?LinkId=169360).\[Template Token Value\]</span></span>

2. <span data-ttu-id="c0319-115">Per eseguire l'installazione in modo invisibile all'utente, usare l'opzione della riga di comando "/Q" con vcredist\_x86.exe, ad esempio **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="c0319-115">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

3. <span data-ttu-id="c0319-116">Per installare il software usando il file vcredist\_x86.msi, usare l'opzione della riga di comando "/C/T: &lt; fullpathtofolder &gt; " per estrarre i file vcredist.msi e vcredis1.cab da vcredist\_x86.exe in una cartella temporanea.</span><span class="sxs-lookup"><span data-stu-id="c0319-116">To install the software by using the vcredist\_x86.msi file, use the command-line option “/C /T:&lt;fullpathtofolder&gt;” to extract the files vcredist.msi and vcredis1.cab from vcredist\_x86.exe to a temporary folder.</span></span> <span data-ttu-id="c0319-117">Per eseguire l'installazione in modo invisibile all'utente, usare l'opzione della riga di comando/quiet, ad esempio **msiexec/i vcredist.msi** /quiet.</span><span class="sxs-lookup"><span data-stu-id="c0319-117">To install silently, use the command-line option /quiet—for example, **msiexec /i vcredist.msi** /quiet.</span></span>

### <span data-ttu-id="c0319-118">Per installare Microsoft VisualC + + 2008SP1 Redistributable Package (x86)</span><span class="sxs-lookup"><span data-stu-id="c0319-118">To install Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

<span data-ttu-id="c0319-119">**Importante**  Per la versione 4.6 e successive del client App-V, è necessario installare anche l'aggiornamento della protezione ATL pacchetto ridistribuibile di Microsoft Visual C++ 2008 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c0319-119">**Important** For version4.6 and later of the App-V client, you must also install the Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update.</span></span>

 

****

1.  <span data-ttu-id="c0319-120">Scaricare il pacchetto software di [aggiornamento della sicurezza ATL pacchetto di Microsoft Visual C++ 2008 Service Pack 1 ridistribuibile](https://go.microsoft.com/fwlink/?LinkId=150700) dall'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=150700) .</span><span class="sxs-lookup"><span data-stu-id="c0319-120">Download the [Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=150700) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=150700).</span></span>

2.  <span data-ttu-id="c0319-121">Per eseguire l'installazione in modo invisibile all'utente, usare l'opzione della riga di comando "/Q" con vcredist\_x86.exe, ad esempio **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="c0319-121">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

### <span data-ttu-id="c0319-122">Per installare Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="c0319-122">To install Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

****

1.  <span data-ttu-id="c0319-123">Scaricare il pacchetto software [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) dall'area download Microsoft ( https://go.microsoft.com/fwlink/?LinkId=63266) .</span><span class="sxs-lookup"><span data-stu-id="c0319-123">Download the [Microsoft Core XML Services (MSXML)6.0SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=63266).</span></span>

2.  <span data-ttu-id="c0319-124">Per eseguire l'installazione in modo invisibile all'utente, usare l'opzione della riga di comando/quiet, ad esempio **msiexec/i msxml6\_x86.msi/quiet**.</span><span class="sxs-lookup"><span data-stu-id="c0319-124">To install silently, use the command-line option /quiet—for example, **msiexec /i msxml6\_x86.msi /quiet**.</span></span>

### <span data-ttu-id="c0319-125">Per installare segnalazione errori applicazione Microsoft</span><span class="sxs-lookup"><span data-stu-id="c0319-125">To install Microsoft Application Error Reporting</span></span>

<span data-ttu-id="c0319-126">Durante l'installazione della segnalazione errori applicazione Microsoft, è necessario usare il parametro *appGUID* per specificare il codice Product App-V.</span><span class="sxs-lookup"><span data-stu-id="c0319-126">When installing Microsoft Application Error Reporting, you must use the *APPGUID* parameter to specify the App-V product code.</span></span> <span data-ttu-id="c0319-127">Il codice prodotto è univoco per ogni tipo e versione client App-V.</span><span class="sxs-lookup"><span data-stu-id="c0319-127">The product code is unique for each App-V client type and version.</span></span> <span data-ttu-id="c0319-128">Selezionare il codice prodotto corretto dalla tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c0319-128">Select the correct product code from the following table.</span></span>

<span data-ttu-id="c0319-129">**Importante**  Per App-V 4.6 SP2 e versioni successive, non è più necessario installare segnalazione errori applicazioni Microsoft (dw20shared.msi).</span><span class="sxs-lookup"><span data-stu-id="c0319-129">**Important** For App-V4.6SP2 and later, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="c0319-130">App-V ora usa la segnalazione degli errori Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c0319-130">App-V now uses Microsoft Error Reporting.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0319-131">Versione</span><span class="sxs-lookup"><span data-stu-id="c0319-131">Version</span></span></th>
<th align="left"><span data-ttu-id="c0319-132">Codice prodotto per client desktop</span><span class="sxs-lookup"><span data-stu-id="c0319-132">Product Code for Desktop Client</span></span></th>
<th align="left"><span data-ttu-id="c0319-133">Codice prodotto per client per Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="c0319-133">Product Code for Client for Remote Desktop Services</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0319-134">App-V 4,5 CU1</span><span class="sxs-lookup"><span data-stu-id="c0319-134">App-V 4.5 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span><span class="sxs-lookup"><span data-stu-id="c0319-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span><span class="sxs-lookup"><span data-stu-id="c0319-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0319-137">App-V 4,5 SP1</span><span class="sxs-lookup"><span data-stu-id="c0319-137">App-V 4.5 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-138">93468B43-C19D-44F9-8BCC-114076DB0443</span><span class="sxs-lookup"><span data-stu-id="c0319-138">93468B43-C19D-44F9-8BCC-114076DB0443</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span><span class="sxs-lookup"><span data-stu-id="c0319-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0319-140">App-V 4,5 SP2</span><span class="sxs-lookup"><span data-stu-id="c0319-140">App-V 4.5 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span><span class="sxs-lookup"><span data-stu-id="c0319-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span><span class="sxs-lookup"><span data-stu-id="c0319-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0319-143">App-V 4,6 x86</span><span class="sxs-lookup"><span data-stu-id="c0319-143">App-V 4.6 x86</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span><span class="sxs-lookup"><span data-stu-id="c0319-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-145">439FAC21-B423-41D4-8126-54F9FCB70039</span><span class="sxs-lookup"><span data-stu-id="c0319-145">439FAC21-B423-41D4-8126-54F9FCB70039</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0319-146">App-V 4,6 x64</span><span class="sxs-lookup"><span data-stu-id="c0319-146">App-V 4.6 x64</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span><span class="sxs-lookup"><span data-stu-id="c0319-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span><span class="sxs-lookup"><span data-stu-id="c0319-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0319-149">App-V 4,6 x86 ¹</span><span class="sxs-lookup"><span data-stu-id="c0319-149">App-V 4.6 x86 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span><span class="sxs-lookup"><span data-stu-id="c0319-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-151">9915D911-CC73-4122-AF4F-564F89454655</span><span class="sxs-lookup"><span data-stu-id="c0319-151">9915D911-CC73-4122-AF4F-564F89454655</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0319-152">App-V 4,6 x64 ¹</span><span class="sxs-lookup"><span data-stu-id="c0319-152">App-V 4.6 x64 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span><span class="sxs-lookup"><span data-stu-id="c0319-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span><span class="sxs-lookup"><span data-stu-id="c0319-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0319-155">App-V 4,6 x86 SP1</span><span class="sxs-lookup"><span data-stu-id="c0319-155">App-V 4.6 x86 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span><span class="sxs-lookup"><span data-stu-id="c0319-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-157">1354855A-2298-4C73-9022-EF0686C65991</span><span class="sxs-lookup"><span data-stu-id="c0319-157">1354855A-2298-4C73-9022-EF0686C65991</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0319-158">App-V 4,6 x64 SP1</span><span class="sxs-lookup"><span data-stu-id="c0319-158">App-V 4.6 x64 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span><span class="sxs-lookup"><span data-stu-id="c0319-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0319-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span><span class="sxs-lookup"><span data-stu-id="c0319-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c0319-161">¹ App-V "lingue" rilascio.</span><span class="sxs-lookup"><span data-stu-id="c0319-161">¹App-V “Languages” release.</span></span>

<span data-ttu-id="c0319-162">**Nota**  Se è necessario trovare il codice prodotto, è possibile usare l'Orca.exe editor di database o uno strumento simile per esaminare i file di Windows Installer per trovare il valore della proprietà *ProductCode* .</span><span class="sxs-lookup"><span data-stu-id="c0319-162">**Note** If you need to find the product code, you can use the Orca.exe database editor or a similar tool to examine Windows Installer files to find the value of the *ProductCode* property.</span></span> <span data-ttu-id="c0319-163">Per altre informazioni sull'uso di Orca.exe, vedere [strumenti di sviluppo di Windows Installer](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .</span><span class="sxs-lookup"><span data-stu-id="c0319-163">For more information about using Orca.exe, see [Windows Installer Development Tools](https://go.microsoft.com/fwlink/?LinkId=150008) (https://go.microsoft.com/fwlink/?LinkId=150008).</span></span>

 

****

1.  <span data-ttu-id="c0319-164">Individuare il programma di installazione della segnalazione degli errori delle applicazioni Microsoft, dw20shared.msi, che si trova nella cartella **Support\\Watson** del supporto di rilascio.</span><span class="sxs-lookup"><span data-stu-id="c0319-164">Locate the Microsoft Application Error Reporting install program, dw20shared.msi, which can be found in the **Support\\Watson** folder on the release media.</span></span>

2.  <span data-ttu-id="c0319-165">Per installare il software, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="c0319-165">To install the software, run the following command:</span></span>

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a><span data-ttu-id="c0319-166">Installazione del client App-V tramite il programma Setup.msi</span><span class="sxs-lookup"><span data-stu-id="c0319-166">Installing the App-V Client by Using the Setup.msi Program</span></span>


<span data-ttu-id="c0319-167">Usare la procedura seguente per installare il client App-V.</span><span class="sxs-lookup"><span data-stu-id="c0319-167">Use the following procedure to install the App-V client.</span></span> <span data-ttu-id="c0319-168">Verificare che sia stato installato il software necessario per i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="c0319-168">Ensure that any necessary prerequisite software has been installed.</span></span> <span data-ttu-id="c0319-169">\ [Template token value \] per la versione 4.6 e successive del client App-V, il programma setup.msi controlla il sistema e se il software prerequisito non è installato, viene generato un messaggio di errore che indica che l'installazione non può continuare.</span><span class="sxs-lookup"><span data-stu-id="c0319-169">\[Template Token Value\] For version4.6 and later of the App-V client, the setup.msi program checks the system and if prerequisite software is not installed, it generates an error message indicating that installation cannot continue.</span></span> <span data-ttu-id="c0319-170">\ [Valore token modello \]</span><span class="sxs-lookup"><span data-stu-id="c0319-170">\[Template Token Value\]</span></span>

**<span data-ttu-id="c0319-171">Per installare il client di virtualizzazione dell'applicazione usando Setup.msi</span><span class="sxs-lookup"><span data-stu-id="c0319-171">To install the Application Virtualization Client by Using Setup.msi</span></span>**

1.  <span data-ttu-id="c0319-172">Verificare di avere effettuato l'accesso con un account che disponga dei diritti di amministratore nel computer.</span><span class="sxs-lookup"><span data-stu-id="c0319-172">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="c0319-173">Aprire una finestra del prompt dei comandi utilizzando diritti elevati e quindi modificare la directory nella cartella che contiene i file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="c0319-173">Open a Command Prompt window by using elevated rights, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="c0319-174">Quando si installa la versione 4.6 o una versione successiva del client App-V, è necessario usare il programma di installazione corretto per il sistema operativo del computer, 32 bit o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="c0319-174">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="c0319-175">L'installazione non riesce e verrà visualizzato un messaggio di errore se si usa il programma di installazione errato.</span><span class="sxs-lookup"><span data-stu-id="c0319-175">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="c0319-176">Immettere la stringa di comando installa al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="c0319-176">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="c0319-177">In alternativa, è possibile creare un file di comando ed eseguirlo dal prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="c0319-177">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="c0319-178">Puoi anche usare un linguaggio di scripting come VBScript o Windows PowerShell per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="c0319-178">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="c0319-179">Nell'esempio della riga di comando seguente viene illustrato il modo in cui setup.msi può essere usato con una serie di parametri facoltativi.</span><span class="sxs-lookup"><span data-stu-id="c0319-179">The following command-line example shows how setup.msi can be used with a number of optional parameters.</span></span> <span data-ttu-id="c0319-180">Per altre informazioni su questi parametri, vedere [parametri della riga di comando di Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c0319-180">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="c0319-181">msiexec.exe/i "setup.msi" SWICACHESIZE = "10240" SWIPUBSVRDISPLAY = "sistema di produzione" SWIPUBSVRTYPE = "HTTP/Secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "on" SWIGLOBALDATA = "D:\\AppVirt\\Global" SWIUSERDATA = "^% LOCALAPPDATA ^%\\Windows\\Application client di virtualizzazione" SWIFSDRIVE = "S"/q</span><span class="sxs-lookup"><span data-stu-id="c0319-181">msiexec.exe /i "setup.msi" SWICACHESIZE="10240" SWIPUBSVRDISPLAY="Production System" SWIPUBSVRTYPE="HTTP /secure" SWIPUBSVRHOST="PRODSYS" SWIPUBSVRPORT="443" SWIPUBSVRPATH="/AppVirt/appsntype.xml" SWIPUBSVRREFRESH="on" SWIGLOBALDATA="D:\\AppVirt\\Global" SWIUSERDATA="^% LOCALAPPDATA^%\\Windows\\Application Virtualization Client" SWIFSDRIVE="S" /q</span></span>**

    **<span data-ttu-id="c0319-182">Importante</span><span class="sxs-lookup"><span data-stu-id="c0319-182">Important</span></span>**  
    -   <span data-ttu-id="c0319-183">L'opzione "**/q**" di Windows Installer consente di eseguire l'installazione invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="c0319-183">The Windows Installer switch "**/q**" is used to make this a silent installation.</span></span>

    -   <span data-ttu-id="c0319-184">I **%** caratteri "" in "**% HOMEDRIVE%**" devono essere preceduti dal carattere di **^** escape "".</span><span class="sxs-lookup"><span data-stu-id="c0319-184">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="c0319-185">In caso contrario, la shell dei comandi di Windows imposta il valore su quello dell'utente che sta eseguendo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="c0319-185">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="c0319-186">Per attivare la registrazione dell'installazione, usare lo switch msiexec **/l\ \* v filename. log**.</span><span class="sxs-lookup"><span data-stu-id="c0319-186">To turn on installation logging, use the msiexec switch **/l\*v filename.log**.</span></span>

     

## <span data-ttu-id="c0319-187">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0319-187">Related topics</span></span>


[<span data-ttu-id="c0319-188">Come installare il client usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="c0319-188">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





