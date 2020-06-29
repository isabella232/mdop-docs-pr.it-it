---
title: Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell
description: Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell
author: dansimp
ms.assetid: 826429fd-29bb-44be-b47e-5f5c7d20dd1d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f350a9eb96a20f50644cfdc1965b7f72741a2c29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822836"
---
# <span data-ttu-id="944fe-103">Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="944fe-103">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>


<span data-ttu-id="944fe-104">Dopo aver installato il software del server MBAM 2,5, è possibile usare le funzionalità configura MBAM 2,5 server usando i cmdlet di Windows PowerShell o la configurazione guidata server di MBAM.</span><span class="sxs-lookup"><span data-stu-id="944fe-104">After you install the MBAM 2.5 Server software, you can use configure MBAM 2.5 Server features by using Windows PowerShell cmdlets or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="944fe-105">Questo argomento descrive come configurare MBAM 2,5 usando i cmdlet di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="944fe-105">This topic describes how to configure MBAM 2.5 by using the Windows PowerShell cmdlets.</span></span> <span data-ttu-id="944fe-106">Per usare la procedura guidata, vedere [configurazione delle funzionalità del server MBAM 2,5](configuring-the-mbam-25-server-features.md).</span><span class="sxs-lookup"><span data-stu-id="944fe-106">To use the wizard instead, see [Configuring the MBAM 2.5 Server Features](configuring-the-mbam-25-server-features.md).</span></span>

## <span data-ttu-id="944fe-107">Contenuto dell'argomento</span><span class="sxs-lookup"><span data-stu-id="944fe-107">In this topic</span></span>


<span data-ttu-id="944fe-108">Questo argomento include le informazioni seguenti sull'uso di Windows PowerShell per configurare MBAM:</span><span class="sxs-lookup"><span data-stu-id="944fe-108">This topic includes the following information about using Windows PowerShell to configure MBAM:</span></span>

-   [<span data-ttu-id="944fe-109">Come caricare la Guida di Windows PowerShell per MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="944fe-109">How to load Windows PowerShell Help for MBAM 2.5</span></span>](#bkmk-load-posh-help)

-   [<span data-ttu-id="944fe-110">Come ottenere assistenza per un cmdlet di Windows PowerShell di MBAM</span><span class="sxs-lookup"><span data-stu-id="944fe-110">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>](#bkmk-help-specific-cmdlet)

-   [<span data-ttu-id="944fe-111">Configurazioni che è possibile eseguire solo con Windows PowerShell, ma non con la configurazione guidata del server MBAM</span><span class="sxs-lookup"><span data-stu-id="944fe-111">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>](#bkmk-config-only-posh)

-   [<span data-ttu-id="944fe-112">Prerequisiti e requisiti per l'uso di Windows PowerShell per configurare le caratteristiche del server MBAM</span><span class="sxs-lookup"><span data-stu-id="944fe-112">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>](#bkmk-prereqs-posh-mbamsvr)

-   [<span data-ttu-id="944fe-113">Uso di Windows PowerShell per configurare MBAM in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="944fe-113">Using Windows PowerShell to configure MBAM on a remote computer</span></span>](#bkmk-remote-config)

-   [<span data-ttu-id="944fe-114">Account obbligatori e parametri del cmdlet di Windows PowerShell corrispondenti</span><span class="sxs-lookup"><span data-stu-id="944fe-114">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>](#bkmk-reqd-posh-accts)

<span data-ttu-id="944fe-115">Per informazioni sui cmdlet **Get-MbamBitLockerRecoveryKey** e **Get-MbamTPMOwnerPassword** di Windows PowerShell, che vengono usati per amministrare mbam, vedere [uso di Windows powershell per amministrare MBAM 2,5](using-windows-powershell-to-administer-mbam-25.md).</span><span class="sxs-lookup"><span data-stu-id="944fe-115">For information about the **Get-MbamBitLockerRecoveryKey** and **Get-MbamTPMOwnerPassword** Windows PowerShell cmdlets, which are used to administer MBAM, see [Using Windows PowerShell to Administer MBAM 2.5](using-windows-powershell-to-administer-mbam-25.md).</span></span>

## <a href="" id="bkmk-load-posh-help"></a><span data-ttu-id="944fe-116">Come caricare la Guida di Windows PowerShell per MBAM 2,5</span><span class="sxs-lookup"><span data-stu-id="944fe-116">How to load Windows PowerShell Help for MBAM 2.5</span></span>


<span data-ttu-id="944fe-117">Per un elenco dei cmdlet di Windows PowerShell in TechNet, vedere [automazione di Microsoft Desktop Optimization Pack con Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span><span class="sxs-lookup"><span data-stu-id="944fe-117">For a list of the Windows PowerShell cmdlets on TechNet, see [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=392816).</span></span>

**<span data-ttu-id="944fe-118">Per caricare la Guida di MBAM 2,5 per i cmdlet di Windows PowerShell dopo l'installazione del software del server MBAM</span><span class="sxs-lookup"><span data-stu-id="944fe-118">To load the MBAM 2.5 Help for Windows PowerShell cmdlets after installing the MBAM Server software</span></span>**

1.  <span data-ttu-id="944fe-119">Aprire Windows PowerShell o Windows PowerShell Integrated Scripting Environment (ISE).</span><span class="sxs-lookup"><span data-stu-id="944fe-119">Open Windows PowerShell or Windows PowerShell Integrated Scripting Environment (ISE).</span></span>

2.  <span data-ttu-id="944fe-120">Digitare **Update-Guida-modulo Microsoft. mbam**.</span><span class="sxs-lookup"><span data-stu-id="944fe-120">Type **Update-Help –Module Microsoft.MBAM**.</span></span>

## <a href="" id="bkmk-help-specific-cmdlet"></a><span data-ttu-id="944fe-121">Come ottenere assistenza per un cmdlet di Windows PowerShell di MBAM</span><span class="sxs-lookup"><span data-stu-id="944fe-121">How to get Help about an MBAM Windows PowerShell cmdlet</span></span>


<span data-ttu-id="944fe-122">La Guida di Windows PowerShell per MBAM è disponibile nei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="944fe-122">Windows PowerShell Help for MBAM is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="944fe-123">Formato della Guida di Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="944fe-123">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="944fe-124">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="944fe-124">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-125">In un prompt dei comandi di Windows PowerShell digitare <strong> Get-Help </strong> &lt; <em> cmdlet</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="944fe-125">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="944fe-126">Per caricare i più recenti cmdlet di Windows PowerShell, seguire le istruzioni della sezione precedente su come caricare la Guida di Windows PowerShell per MBAM.</span><span class="sxs-lookup"><span data-stu-id="944fe-126">To upload the latest Windows PowerShell cmdlets, follow the instructions in the previous section on how to load Windows PowerShell Help for MBAM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="944fe-127">In TechNet come pagine Web</span><span class="sxs-lookup"><span data-stu-id="944fe-127">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-128">Nell'area download come file di Word. docx</span><span class="sxs-lookup"><span data-stu-id="944fe-128">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="944fe-129">Nell'area download come file PDF</span><span class="sxs-lookup"><span data-stu-id="944fe-129">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-config-only-posh"></a><span data-ttu-id="944fe-130">Configurazioni che è possibile eseguire solo con Windows PowerShell, ma non con la configurazione guidata del server MBAM</span><span class="sxs-lookup"><span data-stu-id="944fe-130">Configurations that you can do only with Windows PowerShell but not with the MBAM Server Configuration wizard</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="944fe-131">Configurazioni che è possibile eseguire solo con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="944fe-131">Configurations that you can do only by using Windows PowerShell</span></span></th>
<th align="left"><span data-ttu-id="944fe-132">Dettagli</span><span class="sxs-lookup"><span data-stu-id="944fe-132">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-133">Installare i servizi Web in un computer separato dalle applicazioni Web.</span><span class="sxs-lookup"><span data-stu-id="944fe-133">Install the web services on a separate computer from the web applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="944fe-134">Usando la procedura guidata, è necessario installare i servizi Web e le applicazioni Web nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="944fe-134">Using the wizard, you must install the web services and web applications on the same computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="944fe-135">Abilitare i report in un punto distinto di Reporting Services senza installare tutti gli oggetti di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="944fe-135">Enable reports on a separate reporting services point without installing all of the Configuration Manager objects.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-136">Eliminare tutti gli oggetti da Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="944fe-136">Delete all of the objects from Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="944fe-137">L'eliminazione degli oggetti a sua volta Elimina tutti i dati di conformità da Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="944fe-137">Deleting the objects in turn deletes all of the compliance data from Configuration Manager.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="944fe-138">Immettere una stringa di connessione personalizzata per i database.</span><span class="sxs-lookup"><span data-stu-id="944fe-138">Enter a custom connection string for the databases.</span></span></p></td>
<td align="left"><p><span data-ttu-id="944fe-139">Esempio: per configurare le applicazioni Web in modo che funzionino con il mirroring, devi usare il <strong> cmdlet Enable-MbamWebApplication </strong> per specificare la sintassi appropriata per i partner di failover nella stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="944fe-139">Example: To configure the web applications to work with mirroring, you must use the <strong>Enable-MbamWebApplication</strong> cmdlet to specify the appropriate failover partner syntax in the connection string.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-140">Ignorare la convalida e configurare una caratteristica anche se il controllo dei prerequisiti non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="944fe-140">Skip validation and configure a feature even though the prerequisite check failed.</span></span></p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="944fe-141">**Nota**  Non è possibile disabilitare i database MBAM con un cmdlet di Windows PowerShell o con la configurazione guidata del server MBAM.</span><span class="sxs-lookup"><span data-stu-id="944fe-141">**Note** You cannot disable the MBAM databases with a Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="944fe-142">Per impedire la rimozione accidentale dei dati di conformità e di controllo, gli amministratori di database devono rimuovere manualmente i database.</span><span class="sxs-lookup"><span data-stu-id="944fe-142">To prevent the accidental removal of your compliance and audit data, database administrators must remove databases manually.</span></span>

 

## <a href="" id="bkmk-prereqs-posh-mbamsvr"></a><span data-ttu-id="944fe-143">Prerequisiti e requisiti per l'uso di Windows PowerShell per configurare le caratteristiche del server MBAM</span><span class="sxs-lookup"><span data-stu-id="944fe-143">Prerequisites and requirements for using Windows PowerShell to configure MBAM Server features</span></span>


<span data-ttu-id="944fe-144">Prima di avviare la configurazione, completare i prerequisiti seguenti.</span><span class="sxs-lookup"><span data-stu-id="944fe-144">Before starting the configuration, complete the following prerequisites.</span></span>

**<span data-ttu-id="944fe-145">Prerequisiti relativi agli account</span><span class="sxs-lookup"><span data-stu-id="944fe-145">Account-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="944fe-146">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="944fe-146">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="944fe-147">Dettagli o altre informazioni</span><span class="sxs-lookup"><span data-stu-id="944fe-147">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-148">Creare gli account necessari.</span><span class="sxs-lookup"><span data-stu-id="944fe-148">Create the required accounts.</span></span></p></td>
<td align="left"><p><span data-ttu-id="944fe-149">Vedere <strong> la sezione account necessari e i parametri del cmdlet di Windows PowerShell corrispondenti </strong> più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="944fe-149">See section <strong>Required accounts and corresponding Windows PowerShell cmdlet parameters</strong> later in this topic.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="944fe-150">Gli account utente e i gruppi passati come parametri ai cmdlet di Windows PowerShell devono essere account validi nel dominio.</span><span class="sxs-lookup"><span data-stu-id="944fe-150">User accounts and groups that you pass as parameters to the Windows PowerShell cmdlets must be valid accounts in the domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="944fe-151">Non è possibile usare gli account locali.</span><span class="sxs-lookup"><span data-stu-id="944fe-151">You cannot use local accounts.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-152">Specificare gli account nel formato di livello più basso.</span><span class="sxs-lookup"><span data-stu-id="944fe-152">Specify accounts in the down-level format.</span></span></p></td>
<td align="left"><p><span data-ttu-id="944fe-153">Esempi:</span><span class="sxs-lookup"><span data-stu-id="944fe-153">Examples:</span></span></p>
<p><span data-ttu-id="944fe-154">domainNetBiosName\userdomainNetBiosName\group</span><span class="sxs-lookup"><span data-stu-id="944fe-154">domainNetBiosName\userdomainNetBiosName\group</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="944fe-155">Prerequisiti relativi alle autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="944fe-155">Permission-related prerequisites</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="944fe-156">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="944fe-156">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="944fe-157">Dettagli o altre informazioni</span><span class="sxs-lookup"><span data-stu-id="944fe-157">Details or additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-158">È necessario essere un amministratore nel computer locale in cui si sta configurando la caratteristica MBAM.</span><span class="sxs-lookup"><span data-stu-id="944fe-158">You must be an administrator on the local computer where you are configuring the MBAM feature.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="944fe-159">Usare un prompt dei comandi di Windows PowerShell con privilegi elevati per eseguire tutti i cmdlet di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="944fe-159">Use an elevated Windows PowerShell command prompt to run all Windows PowerShell cmdlets.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-160">Solo per il <strong> cmdlet Enable-MbamDatabase </strong> :</span><span class="sxs-lookup"><span data-stu-id="944fe-160">For the <strong>Enable-MbamDatabase</strong> cmdlet only:</span></span></p>
<p><span data-ttu-id="944fe-161">&quot; &quot; Per l'istanza del database di Microsoft SQL Server di destinazione è necessario aver creato le autorizzazioni per il database.</span><span class="sxs-lookup"><span data-stu-id="944fe-161">You must have &quot;create any database&quot; permissions on the instance of the target Microsoft SQL Server database.</span></span></p>
<p><span data-ttu-id="944fe-162">Questo account utente deve far parte del gruppo Administrators locale o del gruppo Backup Operators per registrare il writer del servizio Copia Shadow del volume di MBAM (VSS).</span><span class="sxs-lookup"><span data-stu-id="944fe-162">This user account must be a part of the local administrators group or the Backup Operators group to register the MBAM Volume Shadow Copy Service (VSS) Writer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="944fe-163">Per impostazione predefinita, l'amministratore del database o l'amministratore di sistema ha le autorizzazioni necessarie per &quot; creare qualsiasi database &quot; .</span><span class="sxs-lookup"><span data-stu-id="944fe-163">By default, the database administrator or system administrator has the required &quot;create any database&quot; permissions.</span></span></p>
<p></p>
<p><span data-ttu-id="944fe-164">Per altre informazioni su VSS Writer, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)"> servizio Copia Shadow del volume </a> .</span><span class="sxs-lookup"><span data-stu-id="944fe-164">For more information about VSS Writer, see <a href="https://go.microsoft.com/fwlink/?LinkId=392814" data-raw-source="[Volume Shadow Copy Service](https://go.microsoft.com/fwlink/?LinkId=392814)">Volume Shadow Copy Service</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="944fe-165">Solo per la <strong> funzionalità di integrazione di System Center Configuration Manager </strong> :</span><span class="sxs-lookup"><span data-stu-id="944fe-165">For the <strong>System Center Configuration Manager Integration</strong> feature only:</span></span></p>
<p><span data-ttu-id="944fe-166">L'utente che abilita questa funzionalità deve avere questi diritti in Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="944fe-166">The user who enables this feature must have these rights in Configuration Manager:</span></span></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="944fe-167">Tipo di diritti in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="944fe-167">Type of rights in Configuration Manager</span></span></th>
<th align="left"><span data-ttu-id="944fe-168">Diritti obbligatori</span><span class="sxs-lookup"><span data-stu-id="944fe-168">Required rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-169">Diritti sito di Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="944fe-169">Configuration Manager Site rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="944fe-170">Read</span><span class="sxs-lookup"><span data-stu-id="944fe-170">Read</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="944fe-171">Diritti di raccolta di Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="944fe-171">Configuration Manager Collection rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="944fe-172">Crea-Elimina-leggi-modifica-Distribuisci elementi di configurazione</span><span class="sxs-lookup"><span data-stu-id="944fe-172">Create- Delete- Read- Modify- Deploy Configuration Items</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="944fe-173">Diritti degli elementi di configurazione di Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="944fe-173">Configuration Manager Configuration item rights:</span></span></p></td>
<td align="left"><p>- <span data-ttu-id="944fe-174">Crea-Elimina-leggi</span><span class="sxs-lookup"><span data-stu-id="944fe-174">Create- Delete- Read</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p>
<p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-remote-config"></a><span data-ttu-id="944fe-175">Uso di Windows PowerShell per configurare MBAM in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="944fe-175">Using Windows PowerShell to configure MBAM on a remote computer</span></span>


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="944fe-176">Quando usare questa funzionalità</span><span class="sxs-lookup"><span data-stu-id="944fe-176">When to use this capability</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="944fe-177">Quando si vogliono configurare le caratteristiche del server MBAM 2,5 in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="944fe-177">When you want to configure the MBAM 2.5 Server features on a remote computer.</span></span> <span data-ttu-id="944fe-178">I cmdlet di Windows PowerShell sono in uso in un computer e si configurano le caratteristiche in un computer remoto diverso.</span><span class="sxs-lookup"><span data-stu-id="944fe-178">The Windows PowerShell cmdlets are running on one computer, and you are configuring the features on a different, remote computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="944fe-179">Operazioni da eseguire</span><span class="sxs-lookup"><span data-stu-id="944fe-179">What you have to do</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="944fe-180">Per usare Windows PowerShell per configurare le caratteristiche del server MBAM 2,5 in un computer remoto, è necessario:</span><span class="sxs-lookup"><span data-stu-id="944fe-180">To use Windows PowerShell to configure MBAM 2.5 Server features on a remote computer, you must:</span></span></p>
<ul>
<li><p><span data-ttu-id="944fe-181">Verificare che il software MBAM 2,5 Server sia stato installato nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="944fe-181">Ensure that the MBAM 2.5 Server software has been installed on the remote computer.</span></span></p></li>
<li><p><span data-ttu-id="944fe-182">Usare il protocollo CredSSP (Credential Security Support Provider) per aprire la sessione di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="944fe-182">Use the Credential Security Support Provider (CredSSP) Protocol to open the Windows PowerShell session.</span></span></p></li>
<li><p><span data-ttu-id="944fe-183">Abilitare Gestione remota Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="944fe-183">Enable Windows Remote Management (WinRM).</span></span> <span data-ttu-id="944fe-184">Se non si riesce a abilitare WinRM e a configurarlo correttamente, il <strong> cmdlet New-PSSession </strong> descritto in questa tabella mostra un errore e descrive come risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="944fe-184">If you fail to enable WinRM and to configure it correctly, the <strong>New-PSSession</strong> cmdlet that is described in this table displays an error and describes how to fix the issue.</span></span> <span data-ttu-id="944fe-185">Per altre informazioni su WinRM, vedere <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)"> uso di gestione remota di Windows </a> .</span><span class="sxs-lookup"><span data-stu-id="944fe-185">For more information about WinRM, see <a href="https://go.microsoft.com/fwlink/?LinkId=393064" data-raw-source="[Using Windows Remote Management](https://go.microsoft.com/fwlink/?LinkId=393064)">Using Windows Remote Management</a>.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="944fe-186">Perché è necessario farlo</span><span class="sxs-lookup"><span data-stu-id="944fe-186">Why you have to do it</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="944fe-187">Questo protocollo consente ai cmdlet di Windows PowerShell di connettersi a servizi di dominio Active Directory utilizzando le credenziali amministrative dell'utente.</span><span class="sxs-lookup"><span data-stu-id="944fe-187">This protocol enables the Windows PowerShell cmdlets to connect to Active Directory Domain Services by using the user’s administrative credentials.</span></span> <span data-ttu-id="944fe-188">Potrebbe essere visualizzato un errore di convalida se si avvia la sessione di Windows PowerShell senza questo protocollo.</span><span class="sxs-lookup"><span data-stu-id="944fe-188">You might get a validation error if you start the Windows PowerShell session without this protocol.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="944fe-189">Come avviare una sessione di Windows PowerShell con il protocollo CredSSP</span><span class="sxs-lookup"><span data-stu-id="944fe-189">How to start a Windows PowerShell session with the CredSSP protocol</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="944fe-190">Digitare il codice seguente al prompt di Windows PowerShell:</span><span class="sxs-lookup"><span data-stu-id="944fe-190">Type the following code at the Windows PowerShell prompt:</span></span></p>
<p><code>$s = New-PSSession -ComputerName xxx -Authentication Credssp -Credential xxx</code></p>
<p><span data-ttu-id="944fe-191">Il codice seguente mostra un esempio.</span><span class="sxs-lookup"><span data-stu-id="944fe-191">The following code shows an example.</span></span></p>
<p><code>$session = New-PSSession -ComputerName &lt;MBAM_server_name&gt; -Authentication Credssp -Credential (Get-Credential)</code></p>
<p><code>Enter-PSSession $session</code></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqd-posh-accts"></a><span data-ttu-id="944fe-192">Account obbligatori e parametri del cmdlet di Windows PowerShell corrispondenti</span><span class="sxs-lookup"><span data-stu-id="944fe-192">Required accounts and corresponding Windows PowerShell cmdlet parameters</span></span>


<span data-ttu-id="944fe-193">La tabella seguente descrive gli account necessari per configurare le caratteristiche del server MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="944fe-193">The following table describes the accounts that are required to configure MBAM 2.5 Server features.</span></span> <span data-ttu-id="944fe-194">Vengono inoltre elencati i cmdlet e il parametro di Windows PowerShell corrispondente per cui è necessario specificare l'account durante la configurazione.</span><span class="sxs-lookup"><span data-stu-id="944fe-194">It also lists the corresponding Windows PowerShell cmdlet and parameter for which you have to specify the account during configuration.</span></span>

<span data-ttu-id="944fe-195">Tipo di parametro cmdlet (utente o gruppo) Descrizione Enable-MBAMDatabase</span><span class="sxs-lookup"><span data-stu-id="944fe-195">Cmdlet Parameter Type (User or Group) Description Enable-MBAMDatabase</span></span>

<span data-ttu-id="944fe-196">AccessAccount</span><span class="sxs-lookup"><span data-stu-id="944fe-196">AccessAccount</span></span>

<span data-ttu-id="944fe-197">Utente o gruppo</span><span class="sxs-lookup"><span data-stu-id="944fe-197">User or Group</span></span>

<span data-ttu-id="944fe-198">Specificare un utente o un gruppo di dominio che disponga dell'autorizzazione di lettura/scrittura per il database per consentire alle applicazioni Web di accedere ai dati e ai report nel database.</span><span class="sxs-lookup"><span data-stu-id="944fe-198">Specify a domain user or group that has read/write permission to this database to give the web applications access to data and reports in this database.</span></span> <span data-ttu-id="944fe-199">Se il valore è un utente di dominio, il parametro **WebServiceApplicationPoolCredential** usato quando si usa il cmdlet **Enable-MbamWebApplication** deve usare lo stesso account utente.</span><span class="sxs-lookup"><span data-stu-id="944fe-199">If the value is a domain user, then the **WebServiceApplicationPoolCredential** parameter that is used when running the **Enable-MbamWebApplication** cmdlet must use the same user account.</span></span> <span data-ttu-id="944fe-200">Se il valore è un gruppo Domain Users, l'account di dominio usato dal parametro **WebServiceApplicationPoolCredential** deve essere un membro di questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="944fe-200">If the value is a domain Users group, then the domain account that is used by the **WebServiceApplicationPoolCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="944fe-201">ReportAccount</span><span class="sxs-lookup"><span data-stu-id="944fe-201">ReportAccount</span></span>

<span data-ttu-id="944fe-202">Utente o gruppo</span><span class="sxs-lookup"><span data-stu-id="944fe-202">User or Group</span></span>

<span data-ttu-id="944fe-203">Specificare un utente o un gruppo di utenti di dominio che disponga dell'autorizzazione di sola lettura per il database per consentire ai report di MBAM di accedere ai dati di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="944fe-203">Specify a domain user or Users group that has read-only permission to this database to provide the MBAM reports access to the compliance and audit data.</span></span> <span data-ttu-id="944fe-204">Se il valore è un utente di dominio, il parametro **ComplianceAndAuditDBCredential** del cmdlet **Enable-MbamReport** deve usare lo stesso account utente.</span><span class="sxs-lookup"><span data-stu-id="944fe-204">If the value is a domain user, then the **ComplianceAndAuditDBCredential** parameter of the **Enable-MbamReport** cmdlet must use the same user account.</span></span> <span data-ttu-id="944fe-205">Se il valore è un gruppo Domain Users, l'account di dominio usato dal parametro **ComplianceAndAuditDBCredential** deve essere un membro di questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="944fe-205">If the value is a domain Users group, then the domain account that is used by the **ComplianceAndAuditDBCredential** parameter must be a member of this group.</span></span>

<span data-ttu-id="944fe-206">Enable-MbamReport</span><span class="sxs-lookup"><span data-stu-id="944fe-206">Enable-MbamReport</span></span>

<span data-ttu-id="944fe-207">ComplianceAndAuditDBCredential</span><span class="sxs-lookup"><span data-stu-id="944fe-207">ComplianceAndAuditDBCredential</span></span>

<span data-ttu-id="944fe-208">Utente</span><span class="sxs-lookup"><span data-stu-id="944fe-208">User</span></span>

<span data-ttu-id="944fe-209">Specifica le credenziali amministrative usate dall'istanza SSRS locale per connettersi al database di controllo e conformità di MBAM.</span><span class="sxs-lookup"><span data-stu-id="944fe-209">Specifies the administrative credential that the local SSRS instance uses to connect to the MBAM Compliance and Audit Database.</span></span> <span data-ttu-id="944fe-210">L'utente del dominio nelle credenziali amministrative deve essere uguale all'account utente usato per il parametro **ReportAccount** , che viene usato durante l'esecuzione del cmdlet **Enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="944fe-210">The domain user in the administrative credential must be the same as the user account that is used for the **ReportAccount** parameter, which is used while running the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="944fe-211">Se un gruppo Domain Users è stato usato con il parametro **ReportAccount** , questo account deve essere un membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="944fe-211">If a domain Users group was used with the **ReportAccount** parameter, this account should be a member of that group.</span></span>

<span data-ttu-id="944fe-212">**Importante**  L'account specificato nelle credenziali amministrative deve avere diritti utente limitati per migliorare la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="944fe-212">**Important** The account specified in the administrative credentials should have limited user rights for improved security.</span></span> <span data-ttu-id="944fe-213">La password dell'account deve inoltre essere impostata su not expire.</span><span class="sxs-lookup"><span data-stu-id="944fe-213">Also, the password of the account should be set to not expire.</span></span>

 

<span data-ttu-id="944fe-214">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="944fe-214">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="944fe-215">Gruppo</span><span class="sxs-lookup"><span data-stu-id="944fe-215">Group</span></span>

<span data-ttu-id="944fe-216">Specifica il gruppo di utenti del dominio con autorizzazioni di lettura per i report.</span><span class="sxs-lookup"><span data-stu-id="944fe-216">Specifies the domain user group that has read permissions to the reports.</span></span> <span data-ttu-id="944fe-217">Il gruppo specificato deve essere lo stesso gruppo usato per il parametro **ReportsReadOnlyAccessGroup** nel cmdlet **Enable-MbamWebApplication** .</span><span class="sxs-lookup"><span data-stu-id="944fe-217">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamWebApplication** cmdlet.</span></span>

<span data-ttu-id="944fe-218">Enable-MBAMWebApplication</span><span class="sxs-lookup"><span data-stu-id="944fe-218">Enable-MBAMWebApplication</span></span>

<span data-ttu-id="944fe-219">AdvancedHelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="944fe-219">AdvancedHelpdeskAccessGroup</span></span>

<span data-ttu-id="944fe-220">Gruppo</span><span class="sxs-lookup"><span data-stu-id="944fe-220">Group</span></span>

<span data-ttu-id="944fe-221">Specifica il gruppo Domain Users che ha accesso a tutte le aree del sito Web di amministrazione e monitoraggio, ad eccezione dell'area report.</span><span class="sxs-lookup"><span data-stu-id="944fe-221">Specifies the domain Users group that has access to all areas of the Administration and Monitoring Website except the Reports area.</span></span>

<span data-ttu-id="944fe-222">HelpdeskAccessGroup</span><span class="sxs-lookup"><span data-stu-id="944fe-222">HelpdeskAccessGroup</span></span>

<span data-ttu-id="944fe-223">Gruppo</span><span class="sxs-lookup"><span data-stu-id="944fe-223">Group</span></span>

<span data-ttu-id="944fe-224">Specifica il gruppo Domain Users che ha accesso alle aree di **Gestione TPM** e **recupero unità** del sito Web amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="944fe-224">Specifies the domain Users group that has access to the **Manage TPM** and **Drive Recovery** areas of the Administration and Monitoring Website.</span></span>

<span data-ttu-id="944fe-225">ReportsReadOnlyAccessGroup</span><span class="sxs-lookup"><span data-stu-id="944fe-225">ReportsReadOnlyAccessGroup</span></span>

<span data-ttu-id="944fe-226">Gruppo</span><span class="sxs-lookup"><span data-stu-id="944fe-226">Group</span></span>

<span data-ttu-id="944fe-227">Specifica il gruppo Domain Users che ha l'autorizzazione di lettura per l'area **report** del sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="944fe-227">Specifies the domain Users group that has read permission to the **Reports** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="944fe-228">Il gruppo specificato deve essere lo stesso gruppo usato per il parametro **ReportsReadOnlyAccessGroup** nel cmdlet **Enable-MbamReport** .</span><span class="sxs-lookup"><span data-stu-id="944fe-228">The specified group must be the same group that is used for the **ReportsReadOnlyAccessGroup** parameter in the **Enable-MbamReport** cmdlet.</span></span>

<span data-ttu-id="944fe-229">WebServiceApplicationPoolCredential</span><span class="sxs-lookup"><span data-stu-id="944fe-229">WebServiceApplicationPoolCredential</span></span>

<span data-ttu-id="944fe-230">Utente</span><span class="sxs-lookup"><span data-stu-id="944fe-230">User</span></span>

<span data-ttu-id="944fe-231">Specifica l'utente del dominio che deve essere usato dal pool di applicazioni per le applicazioni Web di MBAM.</span><span class="sxs-lookup"><span data-stu-id="944fe-231">Specifies the domain user to be used by the application pool for the MBAM web applications.</span></span> <span data-ttu-id="944fe-232">Deve essere lo stesso account utente di dominio specificato nel parametro **AccessAccount** del cmdlet **Enable-MbamDatabase** .</span><span class="sxs-lookup"><span data-stu-id="944fe-232">It must be the same domain user account that is specified in the **AccessAccount** parameter of the **Enable-MbamDatabase** cmdlet.</span></span> <span data-ttu-id="944fe-233">Se un gruppo di utenti di dominio è stato usato dal parametro **AccessAccount** durante l'uso del cmdlet **Enable-MbamDatabase** , l'utente del dominio specificato qui deve essere un membro del gruppo.</span><span class="sxs-lookup"><span data-stu-id="944fe-233">If a domain Users group was used by the **AccessAccount** parameter when running the **Enable-MbamDatabase** cmdlet, the domain user that is specified here must be a member of that group.</span></span> <span data-ttu-id="944fe-234">Se non specifichi le credenziali amministrative, vengono usate le credenziali amministrative specificate da qualsiasi applicazione Web abilitata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="944fe-234">If you do not specify the administrative credentials, the administrative credentials that were specified by any previously enabled web application are used.</span></span> <span data-ttu-id="944fe-235">Tutte le applicazioni Web usano la stessa identità del pool di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="944fe-235">All of the web applications use the same application pool identity.</span></span> <span data-ttu-id="944fe-236">Se viene specificato più volte, viene usato il valore specificato più di recente.</span><span class="sxs-lookup"><span data-stu-id="944fe-236">If it is specified multiple times, the most recently specified value is used.</span></span>

<span data-ttu-id="944fe-237">**Importante**  Per una maggiore sicurezza, imposta l'account specificato nelle credenziali amministrative per limitare i diritti utente.</span><span class="sxs-lookup"><span data-stu-id="944fe-237">**Important** For improved security, set the account that is specified in the administrative credentials to limited user rights.</span></span> <span data-ttu-id="944fe-238">Imposta inoltre la password dell'account su non scadono mai.</span><span class="sxs-lookup"><span data-stu-id="944fe-238">Also, set the password of the account to never expire.</span></span> <span data-ttu-id="944fe-239">Verificare che l'account predefinito IIS \ _IUSRS o l'account usato per il parametro **WebServiceApplicationPoolCredential** sia stato aggiunto al **client Impersonate dopo** l'impostazione di sicurezza locale di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="944fe-239">Ensure that either the built-in IIS\_IUSRS account or the account that is used for the **WebServiceApplicationPoolCredential** parameter has been added to the **Impersonate a client after authentication** local security setting.</span></span>

<span data-ttu-id="944fe-240">Per visualizzare l'impostazione di sicurezza locale, aprire l' **Editor criteri di sicurezza locali**, espandere il nodo **criteri locali** , selezionare il nodo **assegnazione diritti utente** e quindi fare doppio clic sul pulsante **rappresenta un client dopo l'autenticazione** e **accedere come** impostazioni di criteri di gruppo processo batch nel riquadro dei dettagli.</span><span class="sxs-lookup"><span data-stu-id="944fe-240">To view the local security setting, open the **Local Security Policy editor**, expand the **Local Policies** node, select the **User Rights Assignment** node, and then double-click the **Impersonate a client after authentication** and **Log on as a batch job** Group Policy settings in the details pane.</span></span>

 

 




## <span data-ttu-id="944fe-241">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="944fe-241">Related topics</span></span>


[<span data-ttu-id="944fe-242">Configurazione delle funzionalità server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="944fe-242">Configuring the MBAM 2.5 Server Features</span></span>](configuring-the-mbam-25-server-features.md)

[<span data-ttu-id="944fe-243">Convalida della configurazione delle funzionalità del server di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="944fe-243">Validating the MBAM 2.5 Server Feature Configuration</span></span>](validating-the-mbam-25-server-feature-configuration.md)

[<span data-ttu-id="944fe-244">Uso di Windows PowerShell per l'amministrazione di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="944fe-244">Using Windows PowerShell to Administer MBAM 2.5</span></span>](using-windows-powershell-to-administer-mbam-25.md)

 
## <span data-ttu-id="944fe-245">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="944fe-245">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="944fe-246">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="944fe-246">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="944fe-247">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="944fe-247">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





