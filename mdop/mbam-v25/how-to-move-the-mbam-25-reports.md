---
title: Come spostare i report di MBAM 2.5
description: Come spostare i report di MBAM 2.5
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804192"
---
# <span data-ttu-id="7388d-103">Come spostare i report di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7388d-103">How to Move the MBAM 2.5 Reports</span></span>


<span data-ttu-id="7388d-104">Usare queste procedure per trasferire la caratteristica report da un computer a un altro, ovvero per trasferire la caratteristica report dal server a al server B.</span><span class="sxs-lookup"><span data-stu-id="7388d-104">Use these procedures to move the Reports feature from one computer to another, that is, to move the Reports feature from Server A to Server B.</span></span>

<span data-ttu-id="7388d-105">I passaggi di alto livello per lo spostamento della caratteristica report sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7388d-105">The high-level steps for moving the Reports feature are:</span></span>

1.  <span data-ttu-id="7388d-106">Arrestare tutte le istanze del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7388d-106">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="7388d-107">Installare il software MBAM 2,5 Server sul server B e configurare la caratteristica report nel server B.</span><span class="sxs-lookup"><span data-stu-id="7388d-107">Install the MBAM 2.5 Server software on Server B and configure the Reports feature on Server B.</span></span>

3.  <span data-ttu-id="7388d-108">Aggiornare i dati di connessione dei report nei server di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7388d-108">Update the reports connection data on the MBAM Administration and Monitoring servers.</span></span>

4.  <span data-ttu-id="7388d-109">Riprendere l'istanza del sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7388d-109">Resume the instance of the MBAM Administration and Monitoring Website.</span></span>

<span data-ttu-id="7388d-110">**Nota**  Per eseguire gli script di Windows PowerShell di esempio in questo argomento, è necessario aggiornare i criteri di esecuzione di Windows PowerShell per consentire l'esecuzione di script.</span><span class="sxs-lookup"><span data-stu-id="7388d-110">**Note** To run the example Windows PowerShell scripts in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="7388d-111">Per istruzioni, vedere [eseguire script di Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7388d-111">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

 

**<span data-ttu-id="7388d-112">Arrestare il sito Web di amministrazione e monitoraggio di MBAM</span><span class="sxs-lookup"><span data-stu-id="7388d-112">Stop the MBAM Administration and Monitoring Website</span></span>**

-   <span data-ttu-id="7388d-113">Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per arrestare il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7388d-113">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="7388d-114">Per automatizzare questa procedura, è possibile usare Windows PowerShell per immettere un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="7388d-114">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**<span data-ttu-id="7388d-115">Installare il software MBAM server ed eseguire la configurazione guidata server MBAM sul server B</span><span class="sxs-lookup"><span data-stu-id="7388d-115">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>**

1.  <span data-ttu-id="7388d-116">Installare il software MBAM server sul server B. Per istruzioni, vedere [installazione del software server MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="7388d-116">Install the MBAM Server software on Server B. For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="7388d-117">Nel server B avviare la configurazione guidata di MBAM server, fare clic su **Aggiungi nuove funzionalità**e quindi selezionare solo la caratteristica **report** .</span><span class="sxs-lookup"><span data-stu-id="7388d-117">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Reports** feature.</span></span>

    <span data-ttu-id="7388d-118">In alternativa, puoi usare il cmdlet di Windows PowerShell **Enable-MbamReport** per configurare i report.</span><span class="sxs-lookup"><span data-stu-id="7388d-118">Alternatively, you can use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span>

    <span data-ttu-id="7388d-119">Per istruzioni su come configurare i report, vedere [come configurare i report di MBAM 2,5](how-to-configure-the-mbam-25-reports.md).</span><span class="sxs-lookup"><span data-stu-id="7388d-119">For instructions on how to configure the Reports, see [How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md).</span></span>

**<span data-ttu-id="7388d-120">Aggiornare i dati di connessione dei report nel server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="7388d-120">Update the reports connection data on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="7388d-121">Nel server in cui è in corso la caratteristica report utilizzare la console di gestione di Internet Information Services (IIS) per aggiornare l'URL dei report.</span><span class="sxs-lookup"><span data-stu-id="7388d-121">On the server that is running the Reports feature, use the Internet Information Services (IIS) Manager console to update the Reports URL.</span></span>

2.  <span data-ttu-id="7388d-122">Espandere **amministrazione e monitoraggio di Microsoft BitLocker**e quindi selezionare il nodo **helpdesk** .</span><span class="sxs-lookup"><span data-stu-id="7388d-122">Expand **Microsoft BitLocker Administration and Monitoring**, and then select the **HelpDesk** node.</span></span>

3.  <span data-ttu-id="7388d-123">Nella sezione **gestione** della **visualizzazione funzionalità**selezionare **editor di configurazione**.</span><span class="sxs-lookup"><span data-stu-id="7388d-123">In the **Management** section of the **Features View**, select **Configuration Editor**.</span></span>

4.  <span data-ttu-id="7388d-124">Nel campo **sezione** selezionare **appSettings**.</span><span class="sxs-lookup"><span data-stu-id="7388d-124">In the **Section** field, select **appSettings**.</span></span>

5.  <span data-ttu-id="7388d-125">Selezionare la riga della **raccolta** e quindi fare clic sul pulsante "ellissi" **(...)** all'estrema destra del riquadro per aprire l' **Editor della raccolta**.</span><span class="sxs-lookup"><span data-stu-id="7388d-125">Select the **Collection** row, and then click the "ellipses" button **(…)** at the far right of the pane to open the **Collection Editor**.</span></span>

6.  <span data-ttu-id="7388d-126">Nell' **Editor della raccolta**seleziona la riga che contiene **Microsoft. mbam. Reports. URL**e aggiorna il valore per **Microsoft. mbam. Reports. URL** per riflettere il nome del server per il server B.</span><span class="sxs-lookup"><span data-stu-id="7388d-126">In the **Collection Editor**, select the row that contains **Microsoft.Mbam.Reports.Url**, and update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B.</span></span>

    <span data-ttu-id="7388d-127">Se la caratteristica report è stata precedentemente configurata in un'istanza denominata di SQL Server Reporting Services, aggiungere o aggiornare il nome dell'istanza all'URL, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="7388d-127">If you previously configured the Reports feature on a named instance of SQL Server Reporting Services, add or update the name of the instance to the URL, for example:</span></span>

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  <span data-ttu-id="7388d-128">Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando nel server di amministrazione e monitoraggio simile all'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="7388d-128">To automate this procedure, you can use Windows PowerShell to run a command on the Administration and Monitoring Server that is similar to the following code example.</span></span>

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    <span data-ttu-id="7388d-129">Usando le descrizioni nella tabella seguente, Sostituisci i valori nell'esempio di codice con i valori corrispondenti all'ambiente.</span><span class="sxs-lookup"><span data-stu-id="7388d-129">Using the descriptions in the following table, replace the values in the code example with values that match your environment.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="7388d-130">Parametro</span><span class="sxs-lookup"><span data-stu-id="7388d-130">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="7388d-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7388d-131">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="7388d-132">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="7388d-132">$SERVERNAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7388d-133">Nome del server a cui sono stati spostati i report.</span><span class="sxs-lookup"><span data-stu-id="7388d-133">Name of the server to which the Reports were moved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="7388d-134">$SRSINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="7388d-134">$SRSINSTANCENAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="7388d-135">Nome dell'istanza di SQL Server Reporting Services a cui sono stati spostati i report.</span><span class="sxs-lookup"><span data-stu-id="7388d-135">Name of the instance of SQL Server Reporting Services to which the Reports were moved.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="7388d-136">Riprendere l'istanza del sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="7388d-136">Resume the instance of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="7388d-137">Nel server che gestisce il sito Web di amministrazione e monitoraggio usare la console di gestione di Internet Information Services (IIS) per avviare il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7388d-137">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="7388d-138">Per automatizzare questa procedura, è possibile usare Windows PowerShell per eseguire un comando simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="7388d-138">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    <span data-ttu-id="7388d-139">**Nota**  Per eseguire questo comando, è necessario aggiungere il modulo IIS per Windows PowerShell all'istanza corrente di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7388d-139">**Note** To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

     



## <span data-ttu-id="7388d-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7388d-140">Related topics</span></span>


[<span data-ttu-id="7388d-141">Come configurare i report di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7388d-141">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="7388d-142">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7388d-142">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="7388d-143">Spostamento delle funzionalità di MBAM 2.5 a un altro server</span><span class="sxs-lookup"><span data-stu-id="7388d-143">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 
## <span data-ttu-id="7388d-144">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="7388d-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="7388d-145">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="7388d-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="7388d-146">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="7388d-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





