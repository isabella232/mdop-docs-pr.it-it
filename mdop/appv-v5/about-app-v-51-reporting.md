---
title: Informazioni sulla creazione di report in App-V 5.1
description: Informazioni sulla creazione di report in App-V 5.1
author: dansimp
ms.assetid: 385dca00-7178-4e35-8d86-c58867ebd65c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 827343d538238ca638b57a74ae5d2d74bc6c5968
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814955"
---
# <span data-ttu-id="8e3ed-103">Informazioni sulla creazione di report in App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="8e3ed-103">About App-V 5.1 Reporting</span></span>

<span data-ttu-id="8e3ed-104">Microsoft Application Virtualization (App-V) 5,1 include una funzionalità di Reporting predefinita che consente di raccogliere informazioni sui computer che eseguono il client App-V 5,1 e informazioni sull'utilizzo del pacchetto di applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-104">Microsoft Application Virtualization (App-V) 5.1 includes a built-in reporting feature that helps you collect information about computers running the App-V 5.1 client as well as information about virtual application package usage.</span></span> <span data-ttu-id="8e3ed-105">Puoi usare queste informazioni per generare report da un database centralizzato.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-105">You can use this information to generate reports from a centralized database.</span></span>

## <a href="" id="---------app-v-5-1-reporting-overview"></a> <span data-ttu-id="8e3ed-106">Panoramica delle relazioni di App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="8e3ed-106">App-V 5.1 Reporting Overview</span></span>

<span data-ttu-id="8e3ed-107">Nell'elenco seguente viene visualizzato il flusso di lavoro di alto livello end-to-end per la creazione di report in App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-107">The following list displays the end–to-end high-level workflow for reporting in App-V 5.1.</span></span>

1. <span data-ttu-id="8e3ed-108">Il server di report App-V 5,1 ha i prerequisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-108">The App-V 5.1 Reporting server has the following prerequisites:</span></span>

    - <span data-ttu-id="8e3ed-109">Ruolo del server Web Internet Information Service (IIS)</span><span class="sxs-lookup"><span data-stu-id="8e3ed-109">Internet Information Service (IIS) web server role</span></span>

    - <span data-ttu-id="8e3ed-110">Ruolo di autenticazione di Windows (in **IIS/sicurezza**)</span><span class="sxs-lookup"><span data-stu-id="8e3ed-110">Windows Authentication role (under **IIS / Security**)</span></span>

    - <span data-ttu-id="8e3ed-111">SQL Server installato ed eseguito con SQL Server Reporting Services (SSRS)</span><span class="sxs-lookup"><span data-stu-id="8e3ed-111">SQL Server installed and running with SQL Server Reporting Services (SSRS)</span></span>

    <span data-ttu-id="8e3ed-112">Per verificare che SQL Server Reporting Services sia in uso, visualizzare `http://localhost/Reports` in un Web browser come amministratore nel server che ospiterà la creazione di report di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-112">To confirm SQL Server Reporting Services is running, view `http://localhost/Reports` in a web browser as administrator on the server that will host App-V 5.1 Reporting.</span></span> <span data-ttu-id="8e3ed-113">La Home page di SQL Server Reporting Services dovrebbe essere visualizzata.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-113">The SQL Server Reporting Services Home page should display.</span></span>

2. <span data-ttu-id="8e3ed-114">Installare il server di report App-V 5,1 e il database associato.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-114">Install the App-V 5.1 reporting server and associated database.</span></span> <span data-ttu-id="8e3ed-115">Per altre informazioni sull'installazione di Reporting Server, vedere [come installare il server di report in un computer autonomo e connetterlo al database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ed-115">For more information about installing the reporting server see [How to install the Reporting Server on a Standalone Computer and Connect it to the Database](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md).</span></span> <span data-ttu-id="8e3ed-116">Configurare l'ora in cui il computer che ha eseguito il client App-V 5,1 deve inviare i dati al server di report.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-116">Configure the time when the computer running the App-V 5.1 client should send data to the reporting server.</span></span>

3. <span data-ttu-id="8e3ed-117">Se non si usa un sistema di distribuzione software elettronico, ad esempio Configuration Manager, per visualizzare i report, è possibile definire i report in SQL Server Reporting Service.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-117">If you are not using an electronic software distribution system such as Configuration Manager to view reports then you can define reports in SQL Server Reporting Service.</span></span> <span data-ttu-id="8e3ed-118">Scaricare i report SSRS predefiniti dall' [area download](https://go.microsoft.com/fwlink/?LinkId=397255).</span><span class="sxs-lookup"><span data-stu-id="8e3ed-118">Download predefined SSRS Reports from the [Download Center](https://go.microsoft.com/fwlink/?LinkId=397255).</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e3ed-119">Se si usa l'integrazione di Configuration Manager con App-V 5,1, la maggior parte dei report viene generata da Configuration Manager invece che da App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-119">If you are using the Configuration Manager integration with App-V 5.1, most reports are generated from Configuration Manager rather than from App-V 5.1.</span></span>

4. <span data-ttu-id="8e3ed-120">Dopo aver importato il modulo di PowerShell App-V 5,1 usando `Import-Module AppvClient` come amministratore, abilitare il client App-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-120">After importing the App-V 5.1 PowerShell module using `Import-Module AppvClient` as administrator, enable the App-V 5.1 client.</span></span> <span data-ttu-id="8e3ed-121">Questo cmdlet di PowerShell di esempio Abilita la creazione di report App-V 5,1:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-121">This sample PowerShell cmdlet enables App-V 5.1 reporting:</span></span>

    ```powershell
    Set-AppvClientConfiguration –reportingserverurl <url>:<port> -reportingenabled 1 – ReportingStartTime <0-23> - ReportingRandomDelay <#min>
    ```

    <span data-ttu-id="8e3ed-122">Per inviare immediatamente i dati del report di App-V 5,1, eseguire `Send-AppvClientReport` il client App-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-122">To immediately send App-V 5.1 report data, run `Send-AppvClientReport` on the App-V 5.1 client.</span></span>

    <span data-ttu-id="8e3ed-123">Per altre informazioni sull'installazione del client App-V 5,1 con i report abilitati, vedere [informazioni sulle impostazioni di configurazione del client](about-client-configuration-settings51.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ed-123">For more information about installing the App-V 5.1 client with reporting enabled see [About Client Configuration Settings](about-client-configuration-settings51.md).</span></span> <span data-ttu-id="8e3ed-124">Per amministrare la creazione di report di App-V 5,1 con Windows PowerShell, vedere [come abilitare la creazione di report nel client App-v 5,1 usando PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ed-124">To administer App-V 5.1 Reporting with Windows PowerShell, see [How to Enable Reporting on the App-V 5.1 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md).</span></span>

5. <span data-ttu-id="8e3ed-125">Dopo che il server di Reporting riceve i dati dal client App-V 5,1, invia i dati al database di report.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-125">After the reporting server receives the data from the App-V 5.1 client it sends the data to the reporting database.</span></span> <span data-ttu-id="8e3ed-126">Quando il database riceve ed elabora i dati client, viene inviata una risposta corretta al server di report e quindi viene inviata una notifica al client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-126">When the database receives and processes the client data, a successful reply is sent to the reporting server and then a notification is sent to the App-V 5.1 client.</span></span>

6. <span data-ttu-id="8e3ed-127">Quando il client App-V 5,1 riceve la notifica di successo, svuota la cache di dati per risparmiare spazio.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-127">When the App-V 5.1 client receives the success notification, it empties the data cache to conserve space.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8e3ed-128">Per impostazione predefinita, la cache viene deselezionata dopo che il server ha confermato la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-128">By default the cache is cleared after the server confirms receipt of data.</span></span> <span data-ttu-id="8e3ed-129">È possibile configurare manualmente il client per salvare la cache di dati.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-129">You can manually configure the client to save the data cache.</span></span>

<span data-ttu-id="8e3ed-130">Se il dispositivo client App-V 5,1 non riceve una notifica di successo dal server, mantiene i dati nella cache e cerca di rinviare i dati all'intervallo configurato successivo.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-130">If the App-V 5.1 client device does not receive a success notification from the server, it retains data in the cache and tries to resend data at the next configured interval.</span></span> <span data-ttu-id="8e3ed-131">I client continuano a raccogliere dati e a aggiungerli alla cache.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-131">Clients continue to collect data and add it to the cache.</span></span>

### <a href="" id="-------------app-v-5-1-reporting-server-frequently-asked-questions"></a> <span data-ttu-id="8e3ed-132">Domande frequenti su App-V 5,1 Reporting Server</span><span class="sxs-lookup"><span data-stu-id="8e3ed-132">App-V 5.1 reporting server frequently asked questions</span></span>

<span data-ttu-id="8e3ed-133">La tabella seguente mostra le risposte alle domande più frequenti sulla creazione di report di App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="8e3ed-133">The following table displays answers to common questions about App-V 5.1 reporting</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8e3ed-134">Domanda</span><span class="sxs-lookup"><span data-stu-id="8e3ed-134">Question</span></span></th>
<th align="left"><span data-ttu-id="8e3ed-135">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="8e3ed-135">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e3ed-136">Qual è la frequenza con cui vengono inviate le informazioni di segnalazione al database delle relazioni?</span><span class="sxs-lookup"><span data-stu-id="8e3ed-136">What is the frequency that reporting information is sent to the reporting database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e3ed-137">La frequenza dipende dal modo in cui l'attività di creazione di report è configurata nel computer in cui è in uso il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-137">The frequency depends on how the reporting task is configured on the computer running the App-V 5.1 client.</span></span> <span data-ttu-id="8e3ed-138">È necessario configurare la frequenza/intervallo per l'invio dei dati di report.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-138">You must configure the frequency / interval for sending the reporting data.</span></span> <span data-ttu-id="8e3ed-139">La creazione di report di App-V 5,1 non è abilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-139">App-V 5.1 Reporting is not enabled by default.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8e3ed-140">Quali informazioni sono archiviate nel database del server di Reporting?</span><span class="sxs-lookup"><span data-stu-id="8e3ed-140">What information is stored in the reporting server database?</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e3ed-141">Nell'elenco seguente vengono visualizzati gli elementi archiviati nel database delle relazioni:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-141">The following list displays what is stored in the reporting database:</span></span></p>
<ul>
<li><p><span data-ttu-id="8e3ed-142">Il sistema operativo in esecuzione nel computer che gestisce il client App-V 5,1: nome host, versione, Service Pack, tipo-client/server, architettura del processore.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-142">The operating system running on the computer running the App-V 5.1 client: host name, version, service pack, type - client/server, processor architecture.</span></span></p></li>
<li><p><span data-ttu-id="8e3ed-143">Informazioni client App-V 5,1: versione.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-143">App-V 5.1 Client information: version.</span></span></p></li>
<li><p><span data-ttu-id="8e3ed-144">Elenco di pacchetti pubblicati: GUID, versione GUID, nome.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-144">Published package list: GUID, version GUID, name.</span></span></p></li>
<li><p><span data-ttu-id="8e3ed-145">Informazioni sull'uso delle applicazioni: nome, versione, server di streaming, utente (dominio\alias), GUID della versione del pacchetto, stato di avvio e ora, ora di arresto.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-145">Application usage information: name, version, streaming server, user (domain\alias), package version GUID, launch status and time, shutdown time.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e3ed-146">Qual è il volume medio di informazioni inviate al server di report?</span><span class="sxs-lookup"><span data-stu-id="8e3ed-146">What is the average volume of information that is sent to the reporting server?</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e3ed-147">Dipende.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-147">It depends.</span></span> <span data-ttu-id="8e3ed-148">Nell'elenco seguente vengono visualizzati i tre set di dati inviati al server di report:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-148">The following list displays the three sets of the data sent to the reporting server:</span></span></p>
<ol>
<li><p><span data-ttu-id="8e3ed-149">Sistema operativo e informazioni client di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-149">Operating system, and App-V 5.1 client information.</span></span> <span data-ttu-id="8e3ed-150">~ 150 byte, ogni volta che vengono inviati questi dati.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-150">~150 Bytes, every time this data is sent.</span></span></p></li>
<li><p><span data-ttu-id="8e3ed-151">Elenco di pacchetti pubblicati.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-151">Published package list.</span></span> <span data-ttu-id="8e3ed-152">~ 7 KB per 30 pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-152">~7 KB for 30 packages.</span></span> <span data-ttu-id="8e3ed-153">Viene inviato solo quando l'elenco di pacchetti viene aggiornato con un aggiornamento della pubblicazione, che viene eseguito raramente. Se non è presente alcuna modifica, queste informazioni non vengono inviate.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-153">This is sent only when the package list is updated with a publishing refresh, which is done infrequently; if there is no change, this information is not sent.</span></span></p></li>
<li><p><span data-ttu-id="8e3ed-154">Informazioni sull'utilizzo delle applicazioni virtuali-circa 0,25 KB per ogni evento.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-154">Virtual application usage information – about 0.25KB per event.</span></span> <span data-ttu-id="8e3ed-155">L'apertura e la chiusura contano come un evento se si verificano entrambi prima di inviare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-155">Opening and closing count as one event if both occur before sending the information.</span></span> <span data-ttu-id="8e3ed-156">Durante l'invio con un'attività pianificata, solo i dati dopo l'ultimo caricamento riuscito vengono inviati al server.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-156">When sending using a scheduled task, only the data since the last successful upload is sent to the server.</span></span> <span data-ttu-id="8e3ed-157">Se l'invio manuale viene eseguito tramite il cmdlet di PowerShell, esiste un argomento facoltativo che controlla se i dati devono essere inviati nuovamente la prossima volta, ovvero che l'argomento è <strong> DeleteOnSuccess </strong> .</span><span class="sxs-lookup"><span data-stu-id="8e3ed-157">If sending manually through the PowerShell cmdlet, there is an optional argument that controls if the data needs to be re-sent next time around – that argument is <strong>DeleteOnSuccess</strong>.</span></span></p>
<p></p>
<p><span data-ttu-id="8e3ed-158">Ad esempio, se venti applicazioni vengono aperte e chiuse e le informazioni di segnalazione vengono inviate giornalmente, il traffico giornaliero tipico dovrebbe essere di circa 0,15 KB + 20 x 0,25 KB o su 5KB/utente</span><span class="sxs-lookup"><span data-stu-id="8e3ed-158">So for example, if twenty applications are opened and closed and reporting information is scheduled to be sent daily, the typical daily traffic should be about 0.15KB + 20 x 0.25KB, or about 5KB/user</span></span></p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8e3ed-159">I report possono essere pianificati?</span><span class="sxs-lookup"><span data-stu-id="8e3ed-159">Can reporting be scheduled?</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e3ed-160">Sì.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-160">Yes.</span></span> <span data-ttu-id="8e3ed-161">Oltre a inviare manualmente i report usando i cmdlet di PowerShell ( <strong> Send-AppvClientReport </strong> ), l'attività può essere programmata in modo che avvenga automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-161">Besides manually sending reporting using PowerShell Cmdlets (<strong>Send-AppvClientReport</strong>), the task can be scheduled so it will happen automatically.</span></span> <span data-ttu-id="8e3ed-162">Esistono due modi per pianificare la creazione di report:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-162">There are two ways to schedule the reporting:</span></span></p>
<ol>
<li><p><span data-ttu-id="8e3ed-163">Usare i cmdlet di PowerShell- <strong> set-AppvClientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="8e3ed-163">Using PowerShell cmdlets - <strong>Set-AppvClientConfiguration</strong>.</span></span> <span data-ttu-id="8e3ed-164">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-164">For example:</span></span></p>
<p><span data-ttu-id="8e3ed-165">Set-AppvClientConfiguration-ReportingEnabled 1-ReportingServerURL<a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span><span class="sxs-lookup"><span data-stu-id="8e3ed-165">Set-AppvClientConfiguration -ReportingEnabled 1 - ReportingServerURL <a href="http://any.com/appv-reporting" data-raw-source="http://any.com/appv-reporting">http://any.com/appv-reporting</span></span></a></p>
<p></p>
<p><span data-ttu-id="8e3ed-166">Per un elenco completo delle impostazioni di configurazione del client, vedere <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)"> informazioni sulle impostazioni di configurazione del client </a> e cercare le voci seguenti: <strong> ReportingEnabled </strong> , <strong> ReportingServerURL </strong> , <strong> ReportingDataCacheLimit </strong> , <strong> ReportingDataBlockSize </strong> , <strong> ReportingStartTime </strong> , <strong> ReportingRandomDelay </strong> , <strong> ReportingInterval </strong> .</span><span class="sxs-lookup"><span data-stu-id="8e3ed-166">For a complete list of client configuration settings see <a href="about-client-configuration-settings51.md" data-raw-source="[About Client Configuration Settings](about-client-configuration-settings51.md)">About Client Configuration Settings</a> and look for the following entries: <strong>ReportingEnabled</strong>, <strong>ReportingServerURL</strong>, <strong>ReportingDataCacheLimit</strong>, <strong>ReportingDataBlockSize</strong>, <strong>ReportingStartTime</strong>, <strong>ReportingRandomDelay</strong>, <strong>ReportingInterval</strong>.</span></span></p>
<p></p></li>
<li><p><span data-ttu-id="8e3ed-167">Tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-167">By using Group Policy.</span></span> <span data-ttu-id="8e3ed-168">Se distribuiti con il controller di dominio, le impostazioni sono le stesse elencate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-168">If distributed using the domain controller, the settings are the same as previously listed.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8e3ed-169">Nota</span><span class="sxs-lookup"><span data-stu-id="8e3ed-169">Note</span></span></strong><br/><p><span data-ttu-id="8e3ed-170">Le impostazioni dei criteri di gruppo eseguono l'override delle impostazioni locali configurate tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="8e3ed-170">Group Policy settings override local settings configured using PowerShell.</span></span></p>
</div>
<div>
</div></li>
</ol></td>
</tr>
</tbody>
</table>

## <a href="" id="---------app-v-5-1-client-reporting"></a> <span data-ttu-id="8e3ed-171">Report client App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="8e3ed-171">App-V 5.1 Client Reporting</span></span>

<span data-ttu-id="8e3ed-172">Per usare la creazione di report di App-V 5,1, è necessario installare e configurare il client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-172">To use App-V 5.1 reporting you must install and configure the App-V 5.1 client.</span></span> <span data-ttu-id="8e3ed-173">Dopo l'installazione del client, usare il cmdlet **set-AppVClientConfiguration** di PowerShell o il **modello ADMX** per configurare la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-173">After the client has been installed, use the **Set-AppVClientConfiguration** PowerShell cmdlet or the **ADMX Template** to configure reporting.</span></span> <span data-ttu-id="8e3ed-174">I cmdlet delle funzionalità di creazione di report sono disponibili tramite il collegamento seguente e sono preimpostati per la **creazione di report**.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-174">The reporting feature cmdlets are available by using the following link and are prefaced by **Reporting**.</span></span> <span data-ttu-id="8e3ed-175">Per un elenco completo delle impostazioni di configurazione del client, vedere [informazioni sulle impostazioni di configurazione del client](about-client-configuration-settings51.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ed-175">For a complete list of client configuration settings see [About Client Configuration Settings](about-client-configuration-settings51.md).</span></span> <span data-ttu-id="8e3ed-176">La sezione seguente contiene esempi di configurazione della creazione di report client App-V 5,1 tramite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-176">The following section provides examples of App-V 5.1 client reporting configuration using PowerShell.</span></span>

### <span data-ttu-id="8e3ed-177">Configurazione della creazione di report client App-V tramite PowerShell</span><span class="sxs-lookup"><span data-stu-id="8e3ed-177">Configuring App-V Client reporting using PowerShell</span></span>

<span data-ttu-id="8e3ed-178">Gli esempi seguenti illustrano come i parametri di PowerShell possono configurare le funzionalità di creazione di report del client App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-178">The following examples show how PowerShell parameters can configure the reporting features of the App-V 5.1 client.</span></span>

> [!NOTE]
> <span data-ttu-id="8e3ed-179">L'attività di configurazione seguente può essere configurata anche usando le impostazioni dei criteri di gruppo nel modello ADMX di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-179">The following configuration task can also be configured using Group Policy settings in the App-V 5.1 ADMX template.</span></span> <span data-ttu-id="8e3ed-180">Per altre informazioni sull'uso del modello ADMX, vedere [come modificare la configurazione del client App-V 5,1 usando il modello ADMX e i criteri di gruppo](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).</span><span class="sxs-lookup"><span data-stu-id="8e3ed-180">For more information about using the ADMX template, see [How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md).</span></span>

<span data-ttu-id="8e3ed-181">**Per abilitare la creazione di report e avviare la raccolta dei dati nel computer che gestisce il client App-V 5,1**:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-181">**To enable reporting and to initiate data collection on the computer running the App-V 5.1 client**:</span></span>

```powershell
Set-AppVClientConfiguration –ReportingEnabled 1
```

<span data-ttu-id="8e3ed-182">**Per configurare il client per l'invio automatico di dati a un server di report specifico**:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-182">**To configure the client to automatically send data to a specific reporting server**:</span></span>

```powershell
Set-AppVClientConfiguration –ReportingServerURL http://MyReportingServer:MyPort/ -ReportingStartTime 20 -ReportingInterval 1 -ReportingRandomDelay 30 -ReportingInterval 1 -ReportingRandomDelay 30
```

<span data-ttu-id="8e3ed-183">Questo esempio configura il client per inviare automaticamente i dati dei report all'URL del server di report **http://MyReportingServer:MyPort/** .</span><span class="sxs-lookup"><span data-stu-id="8e3ed-183">This example configures the client to automatically send the reporting data to the reporting server URL **http://MyReportingServer:MyPort/**.</span></span> <span data-ttu-id="8e3ed-184">I dati dei report verranno inoltre inviati giornalmente tra 8:00 e 8:30 PM, a seconda del ritardo casuale generato per la sessione.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-184">Additionally, the reporting data will be sent daily between 8:00 and 8:30 PM, depending on the random delay generated for the session.</span></span>

<span data-ttu-id="8e3ed-185">**Per limitare le dimensioni della cache dei dati nel client**:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-185">**To limit the size of the data cache on the client**:</span></span>

```powershell
Set-AppvClientConfiguration –ReportingDataCacheLimit 100
```

<span data-ttu-id="8e3ed-186">Configura le dimensioni massime della cache dei report nel computer in cui è in uso il client App-V 5,1 per 100 MB.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-186">Configures the maximum size of the reporting cache on the computer running the App-V 5.1 client to 100 MB.</span></span> <span data-ttu-id="8e3ed-187">Se il limite della cache viene raggiunto prima che i dati vengano inviati al server, il log viene riposizionato e i dati verranno sovrascritti, se necessario.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-187">If the cache limit is reached before the data is sent to the server, then the log rolls over and data will be overwritten as necessary.</span></span>

<span data-ttu-id="8e3ed-188">**Per configurare le dimensioni del blocco dati trasmesse attraverso la rete tra il client e il server**:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-188">**To configure the data block size transmitted across the network between the client and the server**:</span></span>

```powershell
Set-AppvClientConfiguration –ReportingDataBlockSize 10240
```

<span data-ttu-id="8e3ed-189">Specifica il blocco di dati massimo inviato dal client a 10240 MB.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-189">Specifies the maximum data block that the client sends to 10240 MB.</span></span>

### <span data-ttu-id="8e3ed-190">Tipi di dati raccolti</span><span class="sxs-lookup"><span data-stu-id="8e3ed-190">Types of data collected</span></span>

<span data-ttu-id="8e3ed-191">La tabella seguente mostra i tipi di informazioni che è possibile raccogliere usando la creazione di report di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-191">The following table displays the types of information you can collect by using App-V 5.1 reporting.</span></span>

|<span data-ttu-id="8e3ed-192">Informazioni sul client</span><span class="sxs-lookup"><span data-stu-id="8e3ed-192">Client Information</span></span>  |<span data-ttu-id="8e3ed-193">Informazioni sul pacchetto</span><span class="sxs-lookup"><span data-stu-id="8e3ed-193">Package Information</span></span>  |<span data-ttu-id="8e3ed-194">Utilizzo dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="8e3ed-194">Application Usage</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="8e3ed-195">Nome host</span><span class="sxs-lookup"><span data-stu-id="8e3ed-195">Host Name</span></span> |<span data-ttu-id="8e3ed-196">Nome pacchetto</span><span class="sxs-lookup"><span data-stu-id="8e3ed-196">Package Name</span></span>|<span data-ttu-id="8e3ed-197">Orari di inizio e fine</span><span class="sxs-lookup"><span data-stu-id="8e3ed-197">Start and End Times</span></span>|
|<span data-ttu-id="8e3ed-198">Versione client di App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="8e3ed-198">App-V 5.1 Client Version</span></span> |<span data-ttu-id="8e3ed-199">Versione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="8e3ed-199">Package Version</span></span>|<span data-ttu-id="8e3ed-200">Stato esecuzione</span><span class="sxs-lookup"><span data-stu-id="8e3ed-200">Run Status</span></span>|
|<span data-ttu-id="8e3ed-201">Architettura del processore</span><span class="sxs-lookup"><span data-stu-id="8e3ed-201">Processor Architecture</span></span> |<span data-ttu-id="8e3ed-202">Origine pacchetto</span><span class="sxs-lookup"><span data-stu-id="8e3ed-202">Package Source</span></span>|<span data-ttu-id="8e3ed-203">Stato arresto</span><span class="sxs-lookup"><span data-stu-id="8e3ed-203">Shutdown State</span></span>|
|<span data-ttu-id="8e3ed-204">Versione del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8e3ed-204">Operating System Version</span></span>|<span data-ttu-id="8e3ed-205">Percentuale di cache</span><span class="sxs-lookup"><span data-stu-id="8e3ed-205">Percent Cached</span></span>|<span data-ttu-id="8e3ed-206">Nome applicazione</span><span class="sxs-lookup"><span data-stu-id="8e3ed-206">Application Name</span></span>|
|<span data-ttu-id="8e3ed-207">Livello di Service Pack</span><span class="sxs-lookup"><span data-stu-id="8e3ed-207">Service Pack Level</span></span>| |<span data-ttu-id="8e3ed-208">Versione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="8e3ed-208">Application Version</span></span>|
|<span data-ttu-id="8e3ed-209">Tipo di sistema operativo</span><span class="sxs-lookup"><span data-stu-id="8e3ed-209">Operating System Type</span></span>| |<span data-ttu-id="8e3ed-210">Nome utente</span><span class="sxs-lookup"><span data-stu-id="8e3ed-210">Username</span></span>|
| | |<span data-ttu-id="8e3ed-211">Gruppo di connessioni</span><span class="sxs-lookup"><span data-stu-id="8e3ed-211">Connection Group</span></span>|

<span data-ttu-id="8e3ed-212">Il client raccoglie e salva questi dati in un formato **XML** .</span><span class="sxs-lookup"><span data-stu-id="8e3ed-212">The client collects and saves this data in an **.xml** format.</span></span> <span data-ttu-id="8e3ed-213">La cache di dati è nascosta per impostazione predefinita e richiede i diritti di amministratore per aprire il file XML.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-213">The data cache is hidden by default and requires administrator rights to open the XML file.</span></span>

### <span data-ttu-id="8e3ed-214">Invio di dati al server</span><span class="sxs-lookup"><span data-stu-id="8e3ed-214">Sending data to the server</span></span>

<span data-ttu-id="8e3ed-215">Puoi configurare il computer che sta usando il client App-V 5,1 per inviare automaticamente i dati al server di report specificato.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-215">You can configure the computer that is running the App-V 5.1 client to automatically send data to the specified reporting server.</span></span> <span data-ttu-id="8e3ed-216">Per specificare il server, usare il cmdlet **set-AppvClientConfiguration** con le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-216">To specify the server use the **Set-AppvClientConfiguration** cmdlet with the following settings:</span></span>

- <span data-ttu-id="8e3ed-217">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="8e3ed-217">ReportingEnabled</span></span>
- <span data-ttu-id="8e3ed-218">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="8e3ed-218">ReportingServerURL</span></span>
- <span data-ttu-id="8e3ed-219">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="8e3ed-219">ReportingStartTime</span></span>
- <span data-ttu-id="8e3ed-220">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="8e3ed-220">ReportingInterval</span></span>
- <span data-ttu-id="8e3ed-221">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="8e3ed-221">ReportingRandomDelay</span></span>

<span data-ttu-id="8e3ed-222">Dopo aver configurato le impostazioni precedenti, è necessario creare un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-222">After you configure the previous settings, you must create a scheduled task.</span></span> <span data-ttu-id="8e3ed-223">L'attività pianificata contatterà il server specificato dall'impostazione **ReportingServerURL** e avvierà il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-223">The scheduled task will contact the server specified by the **ReportingServerURL** setting and will initiate the transfer.</span></span> <span data-ttu-id="8e3ed-224">Se si vogliono inviare manualmente dati al di fuori dell'orario programmato, usare il cmdlet di PowerShell seguente:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-224">If you want to manually send data outside of the scheduled times, use the following PowerShell cmdlet:</span></span>

```powershell
Send-AppVClientReport –URL http://MyReportingServer:MyPort/ -DeleteOnSuccess
```

<span data-ttu-id="8e3ed-225">Se il server di report è stato configurato in precedenza, il parametro **– URL** può essere omesso.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-225">If the reporting server has been previously configured, then the **–URL** parameter can be omitted.</span></span> <span data-ttu-id="8e3ed-226">In alternativa, se i dati devono essere inviati a una posizione alternativa, specificare un URL diverso per eseguire l'override del **ReportingServerURL** configurato per la raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-226">Alternatively, if the data should be sent to an alternate location, specify a different URL to override the configured **ReportingServerURL** for this data collection.</span></span>

<span data-ttu-id="8e3ed-227">Il parametro **-DeleteOnSuccess** indica che se il trasferimento ha esito positivo, la cache di dati viene deselezionata.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-227">The **-DeleteOnSuccess** parameter indicates that if the transfer is successful, then the data cache is cleared.</span></span> <span data-ttu-id="8e3ed-228">Se non viene specificato, la cache non verrà deselezionata.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-228">If this is not specified, then the cache will not be cleared.</span></span>

### <span data-ttu-id="8e3ed-229">Raccolta dati manuale</span><span class="sxs-lookup"><span data-stu-id="8e3ed-229">Manual Data Collection</span></span>

<span data-ttu-id="8e3ed-230">Puoi anche usare il cmdlet **Send-AppVClientReport** per raccogliere manualmente i dati.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-230">You can also use the **Send-AppVClientReport** cmdlet to manually collect data.</span></span> <span data-ttu-id="8e3ed-231">Questa soluzione è utile con o senza un server di report esistente.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-231">This solution is helpful with or without an existing reporting server.</span></span> <span data-ttu-id="8e3ed-232">Nell'elenco seguente vengono visualizzate informazioni sulla raccolta di dati con o senza un server di report.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-232">The following list displays information about collecting data with or without a reporting server.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8e3ed-233">Con un server di report</span><span class="sxs-lookup"><span data-stu-id="8e3ed-233">With a Reporting Server</span></span></th>
<th align="left"><span data-ttu-id="8e3ed-234">Senza un server di report</span><span class="sxs-lookup"><span data-stu-id="8e3ed-234">Without a Reporting Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8e3ed-235">Se si dispone di un server di report App-V 5,1 esistente, creare un'attività pianificata personalizzata o uno script.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-235">If you have an existing App-V 5.1 reporting Server, create a customized scheduled task or script.</span></span> <span data-ttu-id="8e3ed-236">Specifica che il client invia i dati nella posizione specificata con la frequenza desiderata.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-236">Specify that the client send the data to the specified location with the desired frequency.</span></span></p></td>
<td align="left"><p><span data-ttu-id="8e3ed-237">Se non si dispone di un server di report App-V 5,1 esistente, usare il <strong> parametro – URL </strong> per inviare i dati a una condivisione specificata.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-237">If you do not have an existing App-V 5.1 reporting Server, use the <strong>–URL</strong> parameter to send the data to a specified share.</span></span> <span data-ttu-id="8e3ed-238">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-238">For example:</span></span></p>
<p><code>Send-AppVClientReport –URL \Myshare\MyData\ -DeleteOnSuccess</code></p>
<p><span data-ttu-id="8e3ed-239">L'esempio precedente invierà i dati di report <strong> nella &lt; posizione di \MyShare\MyData/Strong &gt; indicata dal <strong> parametro-URL </strong> .</span><span class="sxs-lookup"><span data-stu-id="8e3ed-239">The previous example will send the reporting data to <strong>\MyShare\MyData&lt;/strong&gt; location indicated by the <strong>-URL</strong> parameter.</span></span> <span data-ttu-id="8e3ed-240">Dopo che i dati sono stati inviati, la cache viene deselezionata.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-240">After the data has been sent, the cache is cleared.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8e3ed-241">Nota</span><span class="sxs-lookup"><span data-stu-id="8e3ed-241">Note</span></span></strong><br/><p><span data-ttu-id="8e3ed-242">Se viene specificata una posizione diversa da quella del server di Reporting, i dati vengono inviati tramite il <strong> </strong> formato XML senza ulteriori elaborazioni.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-242">If a location other than the Reporting Server is specified, the data is sent using <strong>.xml</strong> format with no additional processing.</span></span></p>
</div>
<div>
</div></td>
</tr>
</tbody>
</table>

### <span data-ttu-id="8e3ed-243">Creazione di report</span><span class="sxs-lookup"><span data-stu-id="8e3ed-243">Creating Reports</span></span>

<span data-ttu-id="8e3ed-244">Per recuperare le informazioni sul report e creare report tramite App-V 5,1 è necessario usare uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-244">To retrieve report information and create reports using App-V 5.1 you must use one of the following methods:</span></span>

- <span data-ttu-id="8e3ed-245">**Microsoft SQL Server Reporting Services (SSRS)** -Microsoft SQL Server Reporting Services è disponibile con Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-245">**Microsoft SQL Server Reporting Services (SSRS)** - Microsoft SQL Server Reporting Services is available with Microsoft SQL Server.</span></span> <span data-ttu-id="8e3ed-246">SSRS non viene installato quando si installa il server di report App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-246">SSRS is not installed when you install the App-V 5.1 reporting server.</span></span> <span data-ttu-id="8e3ed-247">Deve essere distribuito separatamente per generare i report associati.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-247">It must be deployed separately to generate the associated reports.</span></span>

    <span data-ttu-id="8e3ed-248">Per altre informazioni sull'uso di [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596), usare il collegamento seguente.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-248">Use the following link for more information about using [Microsoft SQL Server Reporting Services](https://go.microsoft.com/fwlink/?LinkId=285596).</span></span>

- <span data-ttu-id="8e3ed-249">**Scripting** : è possibile generare report tramite scripting direttamente sul database di report di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-249">**Scripting** – You can generate reports by scripting directly against the App-V 5.1 reporting database.</span></span> <span data-ttu-id="8e3ed-250">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-250">For example:</span></span>

    **<span data-ttu-id="8e3ed-251">Stored procedure:</span><span class="sxs-lookup"><span data-stu-id="8e3ed-251">Stored Procedure:</span></span>**

    <span data-ttu-id="8e3ed-252">**spProcessClientReport** è programmato per l'esecuzione a mezzanotte o 12:00 AM.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-252">**spProcessClientReport** is scheduled to run at midnight or 12:00 AM.</span></span>

    <span data-ttu-id="8e3ed-253">Per eseguire la stored procedure pianificata di Microsoft SQL Server, è necessario che Microsoft SQL Server Agent sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-253">To run the Microsoft SQL Server Scheduled Stored procedure, the Microsoft SQL Server Agent must be running.</span></span> <span data-ttu-id="8e3ed-254">Devi verificare che Microsoft SQL Server Agent sia impostato su **autostart**.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-254">You should ensure that the Microsoft SQL Server Agent is set to **AutoStart**.</span></span> <span data-ttu-id="8e3ed-255">Per altre informazioni, vedere [autostart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span><span class="sxs-lookup"><span data-stu-id="8e3ed-255">For more information see [Autostart SQL Server Agent (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=287045).</span></span>

    <span data-ttu-id="8e3ed-256">La stored procedure viene creata anche quando si usano gli script di database App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-256">The stored procedure is also created when using the App-V 5.1 database scripts.</span></span>

<span data-ttu-id="8e3ed-257">Devi anche assicurarti che le **connessioni simultanee massime** del servizio di Reporting Server Web siano impostate su un valore che il server potrà gestire senza influire sulla disponibilità.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-257">You should also ensure that the reporting server web service's **Maximum Concurrent Connections** is set to a value that the server will be able to manage without impacting availability.</span></span> <span data-ttu-id="8e3ed-258">Il numero consigliato di **connessioni simultanee massime** per il **servizio Web Reporting** è **10.000**.</span><span class="sxs-lookup"><span data-stu-id="8e3ed-258">The recommended number of **Maximum Concurrent Connections** for the **Reporting Web Service** is **10,000**.</span></span>

## <span data-ttu-id="8e3ed-259">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e3ed-259">Related topics</span></span>

[<span data-ttu-id="8e3ed-260">Distribuzione del server App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="8e3ed-260">Deploying the App-V 5.1 Server</span></span>](deploying-the-app-v-51-server.md)

[<span data-ttu-id="8e3ed-261">Come installare il server di report in un computer autonomo e connetterlo al database</span><span class="sxs-lookup"><span data-stu-id="8e3ed-261">How to install the Reporting Server on a Standalone Computer and Connect it to the Database</span></span>](how-to-install-the-reporting-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)
