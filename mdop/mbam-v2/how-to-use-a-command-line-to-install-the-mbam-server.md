---
title: Come usare una riga di comando per installare il server MBAM
description: Come usare una riga di comando per installare il server MBAM
author: dansimp
ms.assetid: 6ffc6d41-a793-42c2-b997-95ba47550648
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a689a2df77300300073b2731281004feac87305f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825645"
---
# <span data-ttu-id="bc3a4-103">Come usare una riga di comando per installare il server MBAM</span><span class="sxs-lookup"><span data-stu-id="bc3a4-103">How to Use a Command Line to Install the MBAM Server</span></span>


<span data-ttu-id="bc3a4-104">È possibile usare una riga di comando per installare il server MBAM con la topologia autonoma o Gestione configurazione.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-104">You can use a command line to install the MBAM Server with either the Stand-alone or Configuration Manager topology.</span></span> <span data-ttu-id="bc3a4-105">L'esempio della riga di comando seguente è per la distribuzione di MBAM in un singolo server, che è un'architettura che deve essere usata solo in un ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-105">The following command line example is for deploying MBAM on a single server, which is an architecture that should be used only in a test environment.</span></span> <span data-ttu-id="bc3a4-106">Sarà necessario cambiare la riga di comando di conseguenza quando si distribuisce MBAM in un ambiente di produzione, che dovrebbe avere più server.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-106">You will need to change the command line accordingly when you deploy MBAM to a production environment, which should have multiple servers.</span></span>

## <span data-ttu-id="bc3a4-107">Riga di comando per la distribuzione del server MBAM 2.0 con la topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="bc3a4-107">Command Line for Deploying the MBAM2.0 Server with the Stand-alone Topology</span></span>


<span data-ttu-id="bc3a4-108">È possibile usare una riga di comando simile alla seguente per installare il server MBAM con la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-108">You can use a command line that is similar to the following to install the MBAM Server with the Stand-alone topology.</span></span>

``` syntax
MbamSetup.exe /qb /l*v MaltaServerInstall.log TOPOLOGY=0 I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 ADDLOCAL=KeyDatabase,ReportsDatabase,Reports,AdministrationMonitoringServer,SelfServiceServer,PolicyTemplate,REPORTS_USERACCOUNT=[UserDomain]\[UserName1] REPORTS_USERACCOUNTPW=[UserPwd1] COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="bc3a4-109">La tabella seguente descrive i parametri della riga di comando per la distribuzione del server MBAM con la topologia autonoma.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-109">The following table describes the command line parameters for deploying the MBAM Server with the Stand-alone topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc3a4-110">Parametro</span><span class="sxs-lookup"><span data-stu-id="bc3a4-110">Parameter</span></span></th>
<th align="left"><span data-ttu-id="bc3a4-111">Valore di parametro</span><span class="sxs-lookup"><span data-stu-id="bc3a4-111">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="bc3a4-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc3a4-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc3a4-113">TOPOLOGIA</span><span class="sxs-lookup"><span data-stu-id="bc3a4-113">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-114">0</span><span class="sxs-lookup"><span data-stu-id="bc3a4-114">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-115">0-topologia autonoma</span><span class="sxs-lookup"><span data-stu-id="bc3a4-115">0 – Stand-alone topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc3a4-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="bc3a4-116">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-117">01</span><span class="sxs-lookup"><span data-stu-id="bc3a4-117">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-118">0-non accettare la licenza agreement1-accettare il contratto di licenza</span><span class="sxs-lookup"><span data-stu-id="bc3a4-118">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc3a4-119">ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="bc3a4-119">ADDLOCAL</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-120">Caratteristiche da installare nel server</span><span class="sxs-lookup"><span data-stu-id="bc3a4-120">Features to be installed on the Server</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-121">Database</span><span class="sxs-lookup"><span data-stu-id="bc3a4-121">KeyDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-122">Database di ripristino</span><span class="sxs-lookup"><span data-stu-id="bc3a4-122">Recovery Database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-123">ReportsDatabase</span><span class="sxs-lookup"><span data-stu-id="bc3a4-123">ReportsDatabase</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-124">Database dei report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="bc3a4-124">Compliance and Audit Reports Database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-125">Rapporti</span><span class="sxs-lookup"><span data-stu-id="bc3a4-125">Reports</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-126">Report di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="bc3a4-126">Compliance and Audit Reports</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-127">AdministrationMonitoringServer</span><span class="sxs-lookup"><span data-stu-id="bc3a4-127">AdministrationMonitoringServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-128">Sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="bc3a4-128">Administration and Monitoring website</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-129">SelfServiceServer</span><span class="sxs-lookup"><span data-stu-id="bc3a4-129">SelfServiceServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-130">Portale self-service</span><span class="sxs-lookup"><span data-stu-id="bc3a4-130">Self-Service Portal</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-131">PolicyTemplate</span><span class="sxs-lookup"><span data-stu-id="bc3a4-131">PolicyTemplate</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-132">Modello di criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="bc3a4-132">MBAM Group Policy template</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc3a4-133">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc3a4-133">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-134">UserDomain [UserName1]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-134">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-135">Dominio e account utente dell'account del servizio Reporting Services che accede al database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="bc3a4-135">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc3a4-136">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="bc3a4-136">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-137">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-137">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-138">Password dell'account del servizio Reporting Services che accederà al database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="bc3a4-138">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc3a4-139">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc3a4-139">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-140">ComputerName</span><span class="sxs-lookup"><span data-stu-id="bc3a4-140">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-141">Nome istanza di SQL Server per il database di conformità e controllo: Sostituisci <strong> % nomecomputer% </strong> con il nome del computer</span><span class="sxs-lookup"><span data-stu-id="bc3a4-141">SQL Server instance name for the Compliance and Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc3a4-142">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc3a4-142">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-143">ComputerName</span><span class="sxs-lookup"><span data-stu-id="bc3a4-143">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-144">Nome istanza di SQL Server per il database di ripristino: Sostituisci <strong> % nomecomputer% </strong> con il nome del computer</span><span class="sxs-lookup"><span data-stu-id="bc3a4-144">SQL Server instance name for the Recovery Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc3a4-145">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="bc3a4-145">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-146">ComputerName</span><span class="sxs-lookup"><span data-stu-id="bc3a4-146">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-147">Istanza di SQL Server Reporting Server in cui verranno installati i report di conformità e controllo-Sostituisci <strong> % nomecomputer% </strong> con il nome del computer</span><span class="sxs-lookup"><span data-stu-id="bc3a4-147">SQL Server Reporting Server instance where the Compliance and Audit reports will be installed – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc3a4-148">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="bc3a4-148">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-149">83</span><span class="sxs-lookup"><span data-stu-id="bc3a4-149">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-150">Porta per il sito Web di amministrazione e monitoraggio; "83" è solo un esempio</span><span class="sxs-lookup"><span data-stu-id="bc3a4-150">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc3a4-151">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="bc3a4-151">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-152">83</span><span class="sxs-lookup"><span data-stu-id="bc3a4-152">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-153">Porta per il sito Web portale self-service; "83" è solo un esempio</span><span class="sxs-lookup"><span data-stu-id="bc3a4-153">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="bc3a4-154">Riga di comando per la distribuzione del server MBAM 2.0 con la topologia di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bc3a4-154">Command Line for Deploying the MBAM2.0 Server with the Configuration Manager Topology</span></span>


<span data-ttu-id="bc3a4-155">Per installare il server MBAM con la topologia di Configuration Manager, è possibile usare una riga di comando simile alla seguente.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-155">You can use a command line that is similar to the following to install the MBAM Server with the Configuration Manager topology.</span></span>

``` syntax
MbamSetup.exe /qn /l*v MaltaServerInstall.log I_ACCEPT_ENDUSER_LICENSE_AGREEMENT=1 TOPOLOGY=1 COMPLIDB_SQLINSTANCE=%computername% RECOVERYANDHWDB_SQLINSTANCE=%computername% SRS_INSTANCENAME=%computername% REPORTS_USERACCOUNT=[UserDomain]\[UserName] REPORTS_USERACCOUNTPW=[UserPwd] ADMINANDMON_WEBSITE_PORT=83 WEBSITE_PORT=83
```

<span data-ttu-id="bc3a4-156">La tabella seguente descrive i parametri della riga di comando per l'installazione del server MBAM 2.0 con la topologia di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="bc3a4-156">The following table describes the command line parameters for installing the MBAM2.0 Server with the Configuration Manager topology.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bc3a4-157">Parametro</span><span class="sxs-lookup"><span data-stu-id="bc3a4-157">Parameter</span></span></th>
<th align="left"><span data-ttu-id="bc3a4-158">Valore di parametro</span><span class="sxs-lookup"><span data-stu-id="bc3a4-158">Parameter Value</span></span></th>
<th align="left"><span data-ttu-id="bc3a4-159">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc3a4-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc3a4-160">TOPOLOGIA</span><span class="sxs-lookup"><span data-stu-id="bc3a4-160">TOPOLOGY</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-161">1</span><span class="sxs-lookup"><span data-stu-id="bc3a4-161">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-162">1-topologia di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="bc3a4-162">1 – Configuration Manager topology</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc3a4-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span><span class="sxs-lookup"><span data-stu-id="bc3a4-163">I_ACCEPT_ENDUSER_LICENSE_AGREEMENT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-164">01</span><span class="sxs-lookup"><span data-stu-id="bc3a4-164">01</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-165">0-non accettare la licenza agreement1-accettare il contratto di licenza</span><span class="sxs-lookup"><span data-stu-id="bc3a4-165">0 – do not accept the license agreement1 – accept the license agreement</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc3a4-166">COMPLIDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc3a4-166">COMPLIDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-167">ComputerName</span><span class="sxs-lookup"><span data-stu-id="bc3a4-167">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-168">Nome istanza di SQL Server per il database di controllo: Sostituisci <strong> % nomecomputer% </strong> con il nome del computer</span><span class="sxs-lookup"><span data-stu-id="bc3a4-168">SQL Server instance name for the Audit Database – replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc3a4-169">RECOVERYANDHWDB_SQLINSTANCE</span><span class="sxs-lookup"><span data-stu-id="bc3a4-169">RECOVERYANDHWDB_SQLINSTANCE</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-170">ComputerName</span><span class="sxs-lookup"><span data-stu-id="bc3a4-170">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-171">Nome istanza di SQL Server per il database di ripristino-sostituire <strong> % nomecomputer% </strong> con il nome del computer</span><span class="sxs-lookup"><span data-stu-id="bc3a4-171">SQL Server instance name for the Recovery Database - replace <strong>%computername%</strong> with the computer name</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc3a4-172">SRS_INSTANCENAME</span><span class="sxs-lookup"><span data-stu-id="bc3a4-172">SRS_INSTANCENAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-173">ComputerName</span><span class="sxs-lookup"><span data-stu-id="bc3a4-173">%computername%</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-174">Istanza di SQL Server Reporting Server in cui verranno installati i report di controllo, sostituire% NomeComputer% con il nome del computer</span><span class="sxs-lookup"><span data-stu-id="bc3a4-174">SQL Server Reporting Server instance where the Audit reports will be installed – replace %computername% with the computer name</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc3a4-175">REPORTS_USERACCOUNT</span><span class="sxs-lookup"><span data-stu-id="bc3a4-175">REPORTS_USERACCOUNT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-176">UserDomain [UserName1]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-176">[UserDomain][UserName1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-177">Dominio e account utente dell'account del servizio Reporting Services che accede al database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="bc3a4-177">Domain and user account of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc3a4-178">REPORTS_USERACCOUNTPW</span><span class="sxs-lookup"><span data-stu-id="bc3a4-178">REPORTS_USERACCOUNTPW</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-179">[UserPwd1]</span><span class="sxs-lookup"><span data-stu-id="bc3a4-179">[UserPwd1]</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-180">Password dell'account del servizio Reporting Services che accederà al database di conformità e controllo</span><span class="sxs-lookup"><span data-stu-id="bc3a4-180">Password of the Reporting Services service account that will access the Compliance and Audit database</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bc3a4-181">ADMINANDMON_WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="bc3a4-181">ADMINANDMON_WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-182">83</span><span class="sxs-lookup"><span data-stu-id="bc3a4-182">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-183">Porta per il sito Web di amministrazione e monitoraggio; "83" è solo un esempio</span><span class="sxs-lookup"><span data-stu-id="bc3a4-183">Port for the Administration and Monitoring website; “83” is only an example</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bc3a4-184">WEBSITE_PORT</span><span class="sxs-lookup"><span data-stu-id="bc3a4-184">WEBSITE_PORT</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-185">83</span><span class="sxs-lookup"><span data-stu-id="bc3a4-185">83</span></span></p></td>
<td align="left"><p><span data-ttu-id="bc3a4-186">Porta per il sito Web portale self-service; "83" è solo un esempio</span><span class="sxs-lookup"><span data-stu-id="bc3a4-186">Port for the Self-Service Portal website; “83” is only an example</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="bc3a4-187">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bc3a4-187">Related topics</span></span>


[<span data-ttu-id="bc3a4-188">Distribuzione dell'infrastruttura server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="bc3a4-188">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





