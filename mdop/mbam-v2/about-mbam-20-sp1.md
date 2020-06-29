---
title: Informazioni su MBAM 2.0 SP1
description: Informazioni su MBAM 2.0 SP1
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823555"
---
# <span data-ttu-id="c0999-103">Informazioni su MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c0999-103">About MBAM 2.0 SP1</span></span>

<span data-ttu-id="c0999-104">In questo argomento vengono illustrate le modifiche apportate a Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c0999-104">This topic describes the changes in Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1).</span></span> <span data-ttu-id="c0999-105">Per una descrizione generale di MBAM, vedere [Introduzione a mbam 2,0](getting-started-with-mbam-20-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="c0999-105">For a general description of MBAM, see [Getting Started with MBAM 2.0](getting-started-with-mbam-20-mbam-2.md).</span></span>

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a><span data-ttu-id="c0999-106">Novità di MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c0999-106">What’s new in MBAM 2.0 SP1</span></span>

<span data-ttu-id="c0999-107">Questa versione di MBAM offre le nuove caratteristiche e funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="c0999-107">This version of MBAM provides the following new features and functionality.</span></span>

### <span data-ttu-id="c0999-108">Supporto per Windows 8,1, Windows Server 2012 R2 e gestione configurazione di System Center 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c0999-108">Support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager</span></span>

<span data-ttu-id="c0999-109">Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1) aggiunge il supporto per Windows 8,1, Windows Server 2012 R2 e System Center 2012 R2 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c0999-109">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Windows 8.1, Windows Server 2012 R2, and System Center 2012 R2 Configuration Manager.</span></span>

### <span data-ttu-id="c0999-110">Supporto per Microsoft SQL Server 2008 R2 SP2</span><span class="sxs-lookup"><span data-stu-id="c0999-110">Support for Microsoft SQL Server 2008 R2 SP2</span></span>

<span data-ttu-id="c0999-111">Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1) aggiunge il supporto per Microsoft SQL Server 2008 R2 SP2.</span><span class="sxs-lookup"><span data-stu-id="c0999-111">Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 Service Pack 1 (SP1) adds support for Microsoft SQL Server 2008 R2 SP2.</span></span> <span data-ttu-id="c0999-112">Se si esegue Microsoft System Center Configuration Manager 2007 R2, è necessario usare Microsoft SQL Server 2008 R2 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c0999-112">You must use Microsoft SQL Server 2008 R2 or higher if you are running Microsoft System Center Configuration Manager 2007 R2.</span></span>

### <span data-ttu-id="c0999-113">Rollup feedback dei clienti</span><span class="sxs-lookup"><span data-stu-id="c0999-113">Customer feedback rollup</span></span>

<span data-ttu-id="c0999-114">MBAM 2,0 SP1 include un rollup di correzioni per risolvere i problemi che sono stati trovati dopo la versione di amministrazione e monitoraggio di Microsoft BitLocker (MBAM) 2,0.</span><span class="sxs-lookup"><span data-stu-id="c0999-114">MBAM 2.0 SP1 includes a rollup of fixes to address issues that were found since the Microsoft BitLocker Administration and Monitoring (MBAM) 2.0 release.</span></span> <span data-ttu-id="c0999-115">Come parte di queste modifiche, il campo nome computer viene ora visualizzato nei report di conformità del computer e della conformità di BitLocker per i dettagli dell'organizzazione durante l'esecuzione di MBAM con Microsoft System Center Configuration Manager 2007.</span><span class="sxs-lookup"><span data-stu-id="c0999-115">As part of these changes, the Computer Name field now appears in the BitLocker Computer Compliance and BitLocker Enterprise Compliance Details reports when you run MBAM with Microsoft System Center Configuration Manager 2007.</span></span>

### <span data-ttu-id="c0999-116">L'eccezione del firewall deve essere impostata sulle porte per il portale self-service e il sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="c0999-116">Firewall exception must be set on ports for the Self-Service Portal and the Administration and Monitoring website</span></span>

<span data-ttu-id="c0999-117">Quando si configura il portale self-service e il sito Web di amministrazione e monitoraggio, è necessario impostare un'eccezione del firewall per consentire la comunicazione tramite le porte specificate.</span><span class="sxs-lookup"><span data-stu-id="c0999-117">When you configure the Self-Service Portal and the Administration and Monitoring website, you must set a firewall exception to enable communication through the specified ports.</span></span> <span data-ttu-id="c0999-118">In precedenza, l'installazione di MBAM server ha aperto le porte automaticamente in Windows Firewall.</span><span class="sxs-lookup"><span data-stu-id="c0999-118">Previously, the MBAM server installation opened the ports automatically in Windows Firewall.</span></span>

### <span data-ttu-id="c0999-119">La posizione dei report di MBAM è cambiata in Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c0999-119">Location of MBAM reports has changed in Configuration Manager</span></span>

<span data-ttu-id="c0999-120">I report di MBAM per la topologia integrata di Configuration Manager sono ora disponibili in sottocartelle all'interno del nodo MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0999-120">MBAM reports for the Configuration Manager integrated topology are now available under subfolders within the MBAM node.</span></span> <span data-ttu-id="c0999-121">I nomi delle sottocartelle rappresentano la lingua dei report all'interno della sottocartella.</span><span class="sxs-lookup"><span data-stu-id="c0999-121">The subfolder names represent the language of the reports within the subfolder.</span></span>

### <span data-ttu-id="c0999-122">Possibilità di installare MBAM in un server del sito principale quando si installa MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c0999-122">Ability to install MBAM on a primary site server when you install MBAM with Configuration Manager</span></span>

<span data-ttu-id="c0999-123">È possibile installare MBAM in un server del sito principale o in un server del sito di amministrazione centrale quando si installa MBAM con la topologia integrata di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c0999-123">You can install MBAM on a primary site server or a central administration site server when you install MBAM with the Configuration Manager integrated topology.</span></span> <span data-ttu-id="c0999-124">In precedenza, era necessario installare MBAM in un server del sito di amministrazione centrale.</span><span class="sxs-lookup"><span data-stu-id="c0999-124">Previously, you were required to install MBAM on a central administration site server.</span></span>

**<span data-ttu-id="c0999-125">Importante</span><span class="sxs-lookup"><span data-stu-id="c0999-125">Important</span></span>**  
<span data-ttu-id="c0999-126">Il server in cui si installa MBAM deve essere il server di livello superiore della gerarchia.</span><span class="sxs-lookup"><span data-stu-id="c0999-126">The server on which you install MBAM must be the top-tier server in your hierarchy.</span></span>



<span data-ttu-id="c0999-127">L'installazione di MBAM funziona in modo diverso per Microsoft System Center Configuration Manager 2007 e Microsoft System Center 2012 Configuration Manager come segue:</span><span class="sxs-lookup"><span data-stu-id="c0999-127">The MBAM installation works differently for Microsoft System Center Configuration Manager 2007 and Microsoft System Center 2012 Configuration Manager as follows:</span></span>

-   <span data-ttu-id="c0999-128">**Configuration manager 2007** : se si installa mbam in un server del sito principale che fa parte di una gerarchia di Configuration Manager più grande e dispone di un server padre del sito centrale, mbam risolve il server padre del sito centrale ed esegue tutte le azioni di installazione in tale server padre.</span><span class="sxs-lookup"><span data-stu-id="c0999-128">**Configuration Manager 2007** : If you install MBAM on a primary site server that is part of a larger Configuration Manager hierarchy and has a central site parent server, MBAM resolves the central site parent server and performs all of the installation actions on that parent server.</span></span> <span data-ttu-id="c0999-129">Le azioni di installazione includono il controllo dei prerequisiti e l'installazione di oggetti e report di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c0999-129">The installation actions include checking prerequisites and installing the Configuration Manager objects and reports.</span></span> <span data-ttu-id="c0999-130">Ad esempio, se si installa MBAM in un server del sito principale che è un elemento figlio di un server padre del sito centrale, MBAM installa tutti gli oggetti e i report di Configuration Manager nel server padre.</span><span class="sxs-lookup"><span data-stu-id="c0999-130">For example, if you install MBAM on a primary site server that is a child of a central site parent server, MBAM installs all of the Configuration Manager objects and reports on the parent server.</span></span> <span data-ttu-id="c0999-131">Se si installa MBAM nel server padre, MBAM esegue tutte le operazioni di installazione in tale server padre.</span><span class="sxs-lookup"><span data-stu-id="c0999-131">If you install MBAM on the parent server, MBAM performs all of the installation actions on that parent server.</span></span>

-   <span data-ttu-id="c0999-132">**System Center 2012 Configuration Manager** : se si installa mbam in un server del sito principale o in un server di amministrazione centrale, mbam esegue tutte le operazioni di installazione nel server del sito.</span><span class="sxs-lookup"><span data-stu-id="c0999-132">**System Center 2012 Configuration Manager** : If you install MBAM on a primary site server or on a central administration server, MBAM performs all of the installation actions on that site server.</span></span>

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> <span data-ttu-id="c0999-133">La console di Configuration Manager deve essere installata nel computer in cui si installa il server MBAM</span><span class="sxs-lookup"><span data-stu-id="c0999-133">Configuration Manager Console must be installed on the computer on which you install the MBAM Server</span></span>

<span data-ttu-id="c0999-134">Quando si installa MBAM con la topologia integrata di Configuration Manager, è necessario installare la console di Configuration Manager nello stesso computer in cui verrà installato MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0999-134">When you install MBAM with the Configuration Manager integrated topology, you must install the Configuration Manager Console on the same computer on which MBAM will be installed.</span></span> <span data-ttu-id="c0999-135">Se si usa l'architettura consigliata, descritta in [Introduzione all'uso di mbam con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), è necessario installare Mbam nel server del sito primario di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c0999-135">If you use the recommended architecture, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), you would install MBAM on the Configuration Manager Primary Site Server.</span></span>

### <span data-ttu-id="c0999-136">Nuovi parametri della riga di comando della configurazione per la topologia integrata di Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c0999-136">New setup command-line parameters for the Configuration Manager integrated topology</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c0999-137">Parametro della riga di comando</span><span class="sxs-lookup"><span data-stu-id="c0999-137">Command-Line Parameter</span></span></th>
<th align="left"><span data-ttu-id="c0999-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0999-138">Description</span></span></th>
<th align="left"><span data-ttu-id="c0999-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="c0999-139">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0999-140">CM_SSRS_REMOTE_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="c0999-140">CM_SSRS_REMOTE_SERVER_NAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0999-141">Consente di installare i report di Configuration Manager in un server SQL Server Reporting Services (SSRS) remoto che fa parte dello stesso sito di Configuration Manager in cui è installato MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0999-141">Enables you to install the Configuration Manager reports on a remote SQL Server Reporting Services (SSRS) server that is part of the same Configuration Manager site to which MBAM is installed.</span></span> <span data-ttu-id="c0999-142">Puoi impostare il valore sul nome di dominio completo del server dei ruoli del punto di SSRS remoto.</span><span class="sxs-lookup"><span data-stu-id="c0999-142">You can set the value to the fully qualified domain name of the remote SSRS point role server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0999-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</span><span class="sxs-lookup"><span data-stu-id="c0999-143">MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME=ssrsServer.Contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c0999-144">CM_REPORTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="c0999-144">CM_REPORTS_ONLY</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0999-145">Consente di installare solo i report di Configuration Manager, senza altri oggetti di Configuration Manager, ad esempio la linea di base, la raccolta e gli elementi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="c0999-145">Enables you to install only the Configuration Manager reports, without other Configuration Manager objects, such as the baseline, collection, and configuration items.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c0999-146">Nota</span><span class="sxs-lookup"><span data-stu-id="c0999-146">Note</span></span></strong><br/><p><span data-ttu-id="c0999-147">Devi combinare questo parametro con il parametro CM_REPORTS_COLLECTION_ID.</span><span class="sxs-lookup"><span data-stu-id="c0999-147">You must combine this parameter with the CM_REPORTS_COLLECTION_ID parameter.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="c0999-148">Valori di parametro validi:</span><span class="sxs-lookup"><span data-stu-id="c0999-148">Valid parameter values:</span></span></p>
<ul>
<li><p><span data-ttu-id="c0999-149">True</span><span class="sxs-lookup"><span data-stu-id="c0999-149">True</span></span></p></li>
<li><p><span data-ttu-id="c0999-150">False</span><span class="sxs-lookup"><span data-stu-id="c0999-150">False</span></span></p></li>
</ul>
<p><span data-ttu-id="c0999-151">Puoi combinare questo parametro con il parametro CM_SSRS_REMOTE_SERVER_NAME se vuoi installare i report solo su un server del ruolo del punto di SSRS remoto.</span><span class="sxs-lookup"><span data-stu-id="c0999-151">You can combine this parameter with the CM_SSRS_REMOTE_SERVER_NAME parameter if you want to install the reports only to a remote SSRS point role server.</span></span></p>
<p><span data-ttu-id="c0999-152">Se non si imposta il parametro o se lo si imposta su false, MBAM setup installa tutti gli oggetti di Configuration Manager, inclusi i report.</span><span class="sxs-lookup"><span data-stu-id="c0999-152">If you do not set the parameter or if you set it to False, MBAM Setup installs all of the Configuration Manager objects, including the reports.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0999-153">MbamSetup.exe CM_REPORTS_ONLY = true</span><span class="sxs-lookup"><span data-stu-id="c0999-153">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="c0999-154">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="c0999-154">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c0999-155">CM_REPORTS_COLLECTION_ID</span><span class="sxs-lookup"><span data-stu-id="c0999-155">CM_REPORTS_COLLECTION_ID</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0999-156">ID della raccolta esistente che identifica la raccolta per cui verranno visualizzati i dati di conformità per la creazione di report.</span><span class="sxs-lookup"><span data-stu-id="c0999-156">An existing collection ID that identifies the collection for which reporting compliance data will be displayed.</span></span> <span data-ttu-id="c0999-157">Puoi specificare qualsiasi ID raccolta.</span><span class="sxs-lookup"><span data-stu-id="c0999-157">You can specify any collection ID.</span></span> <span data-ttu-id="c0999-158">Non è necessario usare l'ID della raccolta "MBAM supported Computers".</span><span class="sxs-lookup"><span data-stu-id="c0999-158">You are not required to use the “MBAM Supported Computers” collection ID.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c0999-159">MbamSetup.exe CM_REPORTS_ONLY = true</span><span class="sxs-lookup"><span data-stu-id="c0999-159">MbamSetup.exe CM_REPORTS_ONLY=True</span></span></p>
<p><span data-ttu-id="c0999-160">CM_REPORTS_COLLECTION_ID = SMS00001</span><span class="sxs-lookup"><span data-stu-id="c0999-160">CM_REPORTS_COLLECTION_ID=SMS00001</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="c0999-161">Possibilità di attivare o disattivare il testo dell'avviso del portale self-service</span><span class="sxs-lookup"><span data-stu-id="c0999-161">Ability to turn Self-Service Portal notice text on or off</span></span>

<span data-ttu-id="c0999-162">MBAM 2,0 SP1 consente di disattivare il testo dell'avviso nel portale self-service.</span><span class="sxs-lookup"><span data-stu-id="c0999-162">MBAM 2.0 SP1 enables you to turn off the notice text on the Self-Service Portal.</span></span> <span data-ttu-id="c0999-163">In precedenza, il testo dell'avviso viene visualizzato per impostazione predefinita e non è stato possibile disattivarlo.</span><span class="sxs-lookup"><span data-stu-id="c0999-163">Previously, the notice text displayed by default, and you could not turn it off.</span></span>

**<span data-ttu-id="c0999-164">Per disattivare il testo dell'avviso</span><span class="sxs-lookup"><span data-stu-id="c0999-164">To turn off the notice text</span></span>**

1.  <span data-ttu-id="c0999-165">Nel server in cui è stato installato il portale self-service aprire Internet Information Services (IIS) e individuare i **siti di &gt; amministrazione e monitoraggio &gt; &gt; delle impostazioni delle applicazioni di Microsoft BitLocker selfservice**.</span><span class="sxs-lookup"><span data-stu-id="c0999-165">On the server where you installed the Self-Service Portal, open Internet Information Services (IIS) and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="c0999-166">Nella colonna **nome** selezionare **DisplayNotice**e impostare il valore su **false**.</span><span class="sxs-lookup"><span data-stu-id="c0999-166">From the **Name** column, select **DisplayNotice**, and set the value to **false**.</span></span>

### <span data-ttu-id="c0999-167">Possibilità di localizzare l'istruzione HelpdeskText che punta gli utenti a più informazioni sul portale self-service</span><span class="sxs-lookup"><span data-stu-id="c0999-167">Ability to localize the HelpdeskText statement that points users to more Self-Service Portal information</span></span>

<span data-ttu-id="c0999-168">Puoi configurare una versione localizzata dell'istruzione Self-Service Portal "HelpdeskText", che indica agli utenti finali come ottenere assistenza aggiuntiva quando usano il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="c0999-168">You can configure a localized version of the Self-Service Portal “HelpdeskText” statement, which tells end users how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="c0999-169">Se si configura il testo localizzato per l'istruzione, come descritto nelle istruzioni seguenti, MBAM visualizzerà la versione localizzata.</span><span class="sxs-lookup"><span data-stu-id="c0999-169">If you configure localized text for the statement, as described in the following instructions, MBAM will display the localized version.</span></span> <span data-ttu-id="c0999-170">Se MBAM non trova la versione localizzata, Visualizza il valore che si trova nel parametro **HelpdeskText** .</span><span class="sxs-lookup"><span data-stu-id="c0999-170">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

**<span data-ttu-id="c0999-171">Per visualizzare una versione localizzata dell'istruzione HelpdeskText</span><span class="sxs-lookup"><span data-stu-id="c0999-171">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="c0999-172">Nel server in cui è stato installato il portale self-service aprire IIS e individuare \*\* &gt; &gt; &gt; le impostazioni dell'applicazione di amministrazione e monitoraggio di selfservice di Microsoft BitLocker\*\*.</span><span class="sxs-lookup"><span data-stu-id="c0999-172">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="c0999-173">Nel riquadro **azioni** fare clic su **Aggiungi** per aprire la finestra di dialogo **Aggiungi impostazioni applicazione** .</span><span class="sxs-lookup"><span data-stu-id="c0999-173">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="c0999-174">Nel campo **nome** Digitare **HelpdeskText**\ _ &lt; *lingua* &gt; , dove &lt; *lingua* &gt; è il codice di lingua appropriato per il testo.</span><span class="sxs-lookup"><span data-stu-id="c0999-174">In the **Name** field, type **HelpdeskText**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the text.</span></span> <span data-ttu-id="c0999-175">Ad esempio, per creare un'istruzione HelpdeskText localizzata in spagnolo, devi assegnare un nome al parametro HelpdeskText \ _es-es.</span><span class="sxs-lookup"><span data-stu-id="c0999-175">For example, to create a localized HelpdeskText statement in Spanish, you would name the parameter HelpdeskText\_es-es.</span></span> <span data-ttu-id="c0999-176">Per un elenco dei codici di lingua validi che è possibile usare, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="c0999-176">For a list of the valid language codes that you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="c0999-177">Nel campo **valore** Digitare il testo localizzato che si vuole visualizzare per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="c0999-177">In the **Value** field, type the localized text that you want to display to end users.</span></span>

### <span data-ttu-id="c0999-178">Possibilità di localizzare il portale self-service HelpdeskURL</span><span class="sxs-lookup"><span data-stu-id="c0999-178">Ability to localize the Self-Service Portal HelpdeskURL</span></span>

<span data-ttu-id="c0999-179">È possibile configurare una versione localizzata del portale self-service HelpdeskURL per la visualizzazione agli utenti finali per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c0999-179">You can configure a localized version of the Self-Service Portal HelpdeskURL to display to end users by default.</span></span> <span data-ttu-id="c0999-180">Se si crea una versione localizzata, come descritto nelle istruzioni seguenti, MBAM trova e visualizza la versione localizzata.</span><span class="sxs-lookup"><span data-stu-id="c0999-180">If you create a localized version, as described in the following instructions, MBAM finds and displays the localized version.</span></span> <span data-ttu-id="c0999-181">Se MBAM non trova una versione localizzata, Visualizza l'URL configurato per il parametro HelpDeskURL.</span><span class="sxs-lookup"><span data-stu-id="c0999-181">If MBAM does not find a localized version, it displays the URL that is configured for the HelpDeskURL parameter.</span></span>

**<span data-ttu-id="c0999-182">Per visualizzare un HelpdeskURL localizzato</span><span class="sxs-lookup"><span data-stu-id="c0999-182">To display a localized HelpdeskURL</span></span>**

1.  <span data-ttu-id="c0999-183">Nel server in cui è stato installato il portale self-service aprire IIS e individuare \*\* &gt; &gt; &gt; le impostazioni dell'applicazione di amministrazione e monitoraggio di selfservice di Microsoft BitLocker\*\*.</span><span class="sxs-lookup"><span data-stu-id="c0999-183">On the server where you installed the Self-Service Portal, open IIS and browse to **Sites &gt; Microsoft BitLocker Administration and Monitoring &gt; SelfService &gt; Application Settings**.</span></span>

2.  <span data-ttu-id="c0999-184">Nel riquadro **azioni** fare clic su **Aggiungi** per aprire la finestra di dialogo **Aggiungi impostazioni applicazione** .</span><span class="sxs-lookup"><span data-stu-id="c0999-184">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="c0999-185">Nel campo **nome** Digitare **HelpdeskURL**\ _ &lt; *lingua* &gt; , dove &lt; *lingua* &gt; è il codice di lingua appropriato per l'URL.</span><span class="sxs-lookup"><span data-stu-id="c0999-185">In the **Name** field, type **HelpdeskURL**\_&lt;*language*&gt;, where &lt;*language*&gt; is the appropriate language code for the URL.</span></span> <span data-ttu-id="c0999-186">Ad esempio, per creare un HelpdeskURL localizzato in spagnolo, devi assegnare un nome al parametro HelpdeskURL \ _es-es.</span><span class="sxs-lookup"><span data-stu-id="c0999-186">For example, to create a localized HelpdeskURL in Spanish, you would name the parameter HelpdeskURL\_es-es.</span></span> <span data-ttu-id="c0999-187">Per un elenco dei codici di lingua validi che è possibile usare, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="c0999-187">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="c0999-188">Nel campo **valore** Digitare il HelpdeskURL localizzato che si vuole visualizzare per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="c0999-188">In the **Value** field, type the localized HelpdeskURL that you want to display to end users.</span></span>

### <span data-ttu-id="c0999-189">Possibilità di localizzare il testo dell'avviso del portale self-service</span><span class="sxs-lookup"><span data-stu-id="c0999-189">Ability to localize the Self-Service Portal notice text</span></span>

<span data-ttu-id="c0999-190">È possibile configurare il testo dell'avviso localizzato per la visualizzazione agli utenti finali per impostazione predefinita nel portale self-service.</span><span class="sxs-lookup"><span data-stu-id="c0999-190">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="c0999-191">Il file notice.txt, che Visualizza il testo dell'avviso, si trova nella directory radice seguente:</span><span class="sxs-lookup"><span data-stu-id="c0999-191">The notice.txt file, which displays the notice text, is located in the following root directory:</span></span>

<span data-ttu-id="c0999-192">&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self</span><span class="sxs-lookup"><span data-stu-id="c0999-192">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="c0999-193">Per visualizzare il testo dell'avviso localizzato, è possibile creare un file notice.txt localizzato e salvarlo in una specifica cartella della lingua nella directory seguente:</span><span class="sxs-lookup"><span data-stu-id="c0999-193">To display localized notice text, you create a localized notice.txt file and save it under a specific language folder in the following directory:</span></span>

<span data-ttu-id="c0999-194">&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self</span><span class="sxs-lookup"><span data-stu-id="c0999-194">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="c0999-195">MBAM Visualizza il testo dell'avviso in base alle regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0999-195">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="c0999-196">Se crei un file notice.txt localizzato nella cartella della lingua appropriata, MBAM visualizzerà il testo dell'avviso localizzato.</span><span class="sxs-lookup"><span data-stu-id="c0999-196">If you create a localized notice.txt file in the appropriate language folder, MBAM displays the localized notice text.</span></span>

-   <span data-ttu-id="c0999-197">Se MBAM non trova una versione localizzata del file notice.txt, Visualizza il testo nel file notice.txt predefinito.</span><span class="sxs-lookup"><span data-stu-id="c0999-197">If MBAM does not find a localized version of the notice.txt file, it displays the text in the default notice.txt file.</span></span>

-   <span data-ttu-id="c0999-198">Se MBAM non trova un file di notice.txt predefinito, Visualizza il testo predefinito nel portale self-service.</span><span class="sxs-lookup"><span data-stu-id="c0999-198">If MBAM does not find a default notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

**<span data-ttu-id="c0999-199">Nota</span><span class="sxs-lookup"><span data-stu-id="c0999-199">Note</span></span>**  
<span data-ttu-id="c0999-200">Se il browser di un utente finale è impostato su una lingua che non ha una sottocartella o notice.txt di lingua corrispondente, viene visualizzato il testo presente nel file notice.txt nella directory radice seguente:</span><span class="sxs-lookup"><span data-stu-id="c0999-200">If an end user’s browser is set to a language that does not have a corresponding language subfolder or notice.txt, the text that is in the notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="c0999-201">&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self</span><span class="sxs-lookup"><span data-stu-id="c0999-201">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>



**<span data-ttu-id="c0999-202">Per creare un file notice.txt localizzato</span><span class="sxs-lookup"><span data-stu-id="c0999-202">To create a localized notice.txt file</span></span>**

1.  <span data-ttu-id="c0999-203">Nel server in cui è stato installato il portale self-service creare una &lt; cartella della *lingua* &gt; nella directory seguente, dove &lt; *lingua* &gt; rappresenta il nome della lingua localizzata:</span><span class="sxs-lookup"><span data-stu-id="c0999-203">On the server where you installed the Self-Service Portal, create a &lt;*language*&gt; folder in the following directory, where &lt;*language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="c0999-204">&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self</span><span class="sxs-lookup"><span data-stu-id="c0999-204">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

    **<span data-ttu-id="c0999-205">Nota</span><span class="sxs-lookup"><span data-stu-id="c0999-205">Note</span></span>**  
    <span data-ttu-id="c0999-206">Alcune cartelle di lingua esistono già, quindi potrebbe non essere necessario crearne una.</span><span class="sxs-lookup"><span data-stu-id="c0999-206">Some language folders already exist, so you may not have to create one.</span></span> <span data-ttu-id="c0999-207">Se è necessario creare una cartella della lingua, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947) per un elenco dei nomi validi che è possibile usare per la cartella della &lt; *lingua* &gt; .</span><span class="sxs-lookup"><span data-stu-id="c0999-207">If you do need to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*language*&gt; folder.</span></span>



2.  <span data-ttu-id="c0999-208">Creare un file di notice.txt contenente il testo dell'avviso localizzato.</span><span class="sxs-lookup"><span data-stu-id="c0999-208">Create a notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="c0999-209">Salvare il file notice.txt nella cartella della &lt; *lingua* &gt; .</span><span class="sxs-lookup"><span data-stu-id="c0999-209">Save the notice.txt file in the &lt;*language*&gt; folder.</span></span> <span data-ttu-id="c0999-210">Per creare un file di notice.txt localizzato in spagnolo, ad esempio, è necessario salvare il file notice.txt localizzato nella cartella seguente:</span><span class="sxs-lookup"><span data-stu-id="c0999-210">For example, to create a localized notice.txt file in Spanish, you would save the localized notice.txt file in the following folder:</span></span>

    <span data-ttu-id="c0999-211">&lt;Directory di installazione *di mbam self-service* &gt; Website\\es-es servizio \\Self</span><span class="sxs-lookup"><span data-stu-id="c0999-211">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\es-es</span></span>

## <span data-ttu-id="c0999-212">Aggiornamento a MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c0999-212">Upgrading to MBAM 2.0 SP1</span></span>


<span data-ttu-id="c0999-213">È possibile eseguire l'aggiornamento a MBAM 2,0 SP1 da qualsiasi versione precedente di MBAM.</span><span class="sxs-lookup"><span data-stu-id="c0999-213">You can upgrade to MBAM 2.0 SP1 from any previous version of MBAM.</span></span>

### <span data-ttu-id="c0999-214">Aggiornamento dell'infrastruttura MBAM</span><span class="sxs-lookup"><span data-stu-id="c0999-214">Upgrading the MBAM infrastructure</span></span>

<span data-ttu-id="c0999-215">È possibile aggiornare l'infrastruttura del server MBAM per MBAM 2,0 SP1 come segue:</span><span class="sxs-lookup"><span data-stu-id="c0999-215">You can upgrade the MBAM Server infrastructure to MBAM 2.0 SP1 as follows:</span></span>

<span data-ttu-id="c0999-216">**Sostituzione del server sul posto manuale**: è necessario disinstallare manualmente l'infrastruttura di mbam server esistente e quindi installare l'infrastruttura del server MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c0999-216">**Manual in-place server replacement**: You must manually uninstall the existing MBAM Server infrastructure, and then install the MBAM 2.0 SP1 Server infrastructure.</span></span> <span data-ttu-id="c0999-217">Non è necessario rimuovere i database per eseguire l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="c0999-217">You do not have to remove the databases to do the upgrade.</span></span> <span data-ttu-id="c0999-218">Devi invece selezionare i database esistenti, che la versione precedente di MBAM ha creato.</span><span class="sxs-lookup"><span data-stu-id="c0999-218">Instead, you select the existing databases, which the previous version of MBAM created.</span></span> <span data-ttu-id="c0999-219">L'installazione di aggiornamento di MBAM 2,0 SP1 esegue quindi la migrazione dei database esistenti in MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c0999-219">The MBAM 2.0 SP1 upgrade installation then migrates the existing databases to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="c0999-220">**Aggiornamento client distribuito**: se si usa la topologia di mbam autonoma, è possibile aggiornare gradualmente i client mbam dopo l'installazione dell'infrastruttura del Server MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c0999-220">**Distributed client upgrade**: If you are using the Stand-alone MBAM topology, you can upgrade the MBAM Clients gradually after you install the MBAM 2.0 SP1 Server infrastructure.</span></span>

<span data-ttu-id="c0999-221">Dopo aver aggiornato l'infrastruttura di MBAM server, i client MBAM 1,0 o 2,0 verranno segnalati al server MBAM 2,0 SP1 con successo e memorizzerà i dati di ripristino, ma la conformità sarà basata sui criteri disponibili per la versione client di MBAM attualmente installata.</span><span class="sxs-lookup"><span data-stu-id="c0999-221">After you upgrade the MBAM Server infrastructure, MBAM 1.0 or 2.0 Clients will report to the MBAM 2.0 SP1 Server successfully and will store the recovery data, but compliance will be based on the policies available for the MBAM Client version that is currently installed.</span></span> <span data-ttu-id="c0999-222">Per abilitare la creazione di report con i criteri di MBAM 2,0 SP1, è necessario aggiornare i computer client a MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c0999-222">To enable reporting against MBAM 2.0 SP1 policies, you must upgrade client computers to MBAM 2.0 SP1.</span></span> <span data-ttu-id="c0999-223">È possibile aggiornare i computer client al client MBAM 2,0 SP1 senza disinstallare il client precedente e il client inizierà ad applicarsi e a segnalare, in base ai criteri di MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c0999-223">You can upgrade the client computers to the MBAM 2.0 SP1 Client without uninstalling the previous Client, and the Client will start to apply and report, based on the MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="c0999-224">Per altre informazioni sull'aggiornamento dei server MBAM, vedere [aggiornamento dalle versioni precedenti di mbam](upgrading-from-previous-versions-of-mbam.md).</span><span class="sxs-lookup"><span data-stu-id="c0999-224">For more information about upgrading the MBAM servers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

### <span data-ttu-id="c0999-225">Aggiornamento del client MBAM per MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c0999-225">Upgrading the MBAM Client to MBAM 2.0 SP1</span></span>

<span data-ttu-id="c0999-226">Per aggiornare i computer degli utenti finali al client MBAM 2,0 SP1, eseguire **MbamClientSetup.exe** in ogni computer client.</span><span class="sxs-lookup"><span data-stu-id="c0999-226">To upgrade end-user computers to the MBAM 2.0 SP1 Client, run **MbamClientSetup.exe** on each client computer.</span></span> <span data-ttu-id="c0999-227">Il programma di installazione aggiorna automaticamente il client al client MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c0999-227">The installer automatically updates the Client to the MBAM 2.0 SP1 Client.</span></span> <span data-ttu-id="c0999-228">Dopo l'installazione, i computer client non devono essere riavviati e il client MBAM 2,0 SP1 inizia ad applicarsi e a segnalare i criteri di MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c0999-228">After the installation, client computers do not have to be rebooted, and the MBAM 2.0 SP1 Client starts to apply and report against MBAM 2.0 SP1 policies.</span></span>

<span data-ttu-id="c0999-229">Se si usa MBAM con Configuration Manager, è necessario aggiornare i computer client MBAM per MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c0999-229">If you are using MBAM with Configuration Manager, you must upgrade the MBAM client computers to MBAM 2.0 SP1.</span></span>

<span data-ttu-id="c0999-230">Per altre informazioni sull'aggiornamento dei computer client MBAM, vedere [aggiornamento dalle versioni precedenti di mbam](upgrading-from-previous-versions-of-mbam.md).</span><span class="sxs-lookup"><span data-stu-id="c0999-230">For more information about upgrading the MBAM client computers, see [Upgrading from Previous Versions of MBAM](upgrading-from-previous-versions-of-mbam.md).</span></span>

## <span data-ttu-id="c0999-231">Installazione o aggiornamento di MBAM 2,0 SP1 con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c0999-231">Installing or upgrading to MBAM 2.0 SP1 with Configuration Manager</span></span>


<span data-ttu-id="c0999-232">Questa sezione descrive i requisiti durante l'installazione di MBAM 2,0 SP1 come nuova installazione o come aggiornamento a un'installazione precedente di MBAM 2,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="c0999-232">This section describes the requirements when you are installing MBAM 2.0 SP1 as a new installation or as an upgrade to a previous MBAM 2.0 SP1 installation.</span></span>

### <span data-ttu-id="c0999-233">File necessari per l'installazione di MBAM 2,0 SP1 se si usa MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="c0999-233">Required files for installing MBAM 2.0 SP1 if you are using MBAM with Configuration Manager</span></span>

<span data-ttu-id="c0999-234">Se si sta installando MBAM per la prima volta e si usa MBAM 2,0 SP1 con System Center Configuration Manager, è necessario creare o modificare i file MOF per consentire a MBAM di funzionare correttamente con Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c0999-234">If you are installing MBAM for the first time and you are using MBAM 2.0 SP1 with System Center Configuration Manager, you must create or edit mof files to enable MBAM to work correctly with Configuration Manager.</span></span>

-   **<span data-ttu-id="c0999-235">file MOF di Configuration</span><span class="sxs-lookup"><span data-stu-id="c0999-235">configuration.mof file</span></span>**

    -   <span data-ttu-id="c0999-236">Se si usa Configuration Manager 2007, è necessario modificare il file Configuration. mof completando il passaggio 3 dall'elemento **aggiornare il file Configuration. mof se si esegue l'aggiornamento a mbam 2,0 SP1 e si usa mbam con Configuration Manager 2007**, che segue questo elemento.</span><span class="sxs-lookup"><span data-stu-id="c0999-236">If you are using Configuration Manager 2007, you must edit the configuration.mof file by completing step 3 from the item **Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007**, which follows this item.</span></span>

    -   <span data-ttu-id="c0999-237">Se si usa System Center 2012 Configuration Manager, modificare il file Configuration. mof seguendo le istruzioni in [modificare il file Configuration. mof](edit-the-configurationmof-file.md).</span><span class="sxs-lookup"><span data-stu-id="c0999-237">If you are using System Center 2012 Configuration Manager, edit the configuration.mof file by following the instructions in [Edit the Configuration.mof File](edit-the-configurationmof-file.md).</span></span>

-   <span data-ttu-id="c0999-238">**SMS \ _def file MOF** : seguire le istruzioni in [creare o modificare il file SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md).</span><span class="sxs-lookup"><span data-stu-id="c0999-238">**sms\_def.mof file** – follow the instructions in [Create or Edit the Sms\_def.mof File](create-or-edit-the-sms-defmof-file.md).</span></span>

### <span data-ttu-id="c0999-239">Aggiornare il file Configuration. mof se si esegue l'aggiornamento a MBAM 2,0 SP1 e si usa MBAM con Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="c0999-239">Update the configuration.mof file if you upgrade to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007</span></span>

<span data-ttu-id="c0999-240">Se si esegue l'aggiornamento a MBAM 2,0 SP1 e si usa MBAM con Configuration Manager 2007, è necessario aggiornare il file Configuration. mof per verificare che MBAM 2,0 SP1 funzioni correttamente.</span><span class="sxs-lookup"><span data-stu-id="c0999-240">If you are upgrading to MBAM 2.0 SP1 and you are using MBAM with Configuration Manager 2007, you must update the configuration.mof file to ensure that MBAM 2.0 SP1 works correctly.</span></span>

**<span data-ttu-id="c0999-241">Per aggiornare il file Configuration. mof:</span><span class="sxs-lookup"><span data-stu-id="c0999-241">To update the configuration.mof file:</span></span>**

1.  <span data-ttu-id="c0999-242">Nel server Configuration Manager passare al percorso del file Configuration. mof:</span><span class="sxs-lookup"><span data-stu-id="c0999-242">On the Configuration Manager Server, browse to the location of the Configuration.mof file:</span></span>

    <span data-ttu-id="c0999-243">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="c0999-243">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="c0999-244">In un'installazione predefinita, il percorso di installazione è%systemdrive%\\Program Files (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="c0999-244">On a default installation, the installation location is %systemdrive%\\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="c0999-245">Esaminare il blocco di codice aggiunto al file Configuration. MOF ed eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="c0999-245">Review the block of code that you appended to the configuration.mof file, and delete it.</span></span> <span data-ttu-id="c0999-246">Il blocco di codice sarà simile a quello mostrato nel passaggio seguente.</span><span class="sxs-lookup"><span data-stu-id="c0999-246">The block of code will be similar to the one shown in the following step.</span></span>

3.  <span data-ttu-id="c0999-247">Copiare il blocco di codice seguente e quindi accodarlo al file Configuration. mof per aggiungere al file le classi di MBAM necessarie seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0999-247">Copy the following block of code, and then append it to the configuration.mof file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### <span data-ttu-id="c0999-248">Traduzione di MBAM 2,0 SP1</span><span class="sxs-lookup"><span data-stu-id="c0999-248">Translation of MBAM 2.0 SP1</span></span>

<span data-ttu-id="c0999-249">MBAM 2,0 SP1 è ora disponibile nelle lingue seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0999-249">MBAM 2.0 SP1 is now available in the following languages:</span></span>

-   <span data-ttu-id="c0999-250">Inglese (Stati Uniti) en-US</span><span class="sxs-lookup"><span data-stu-id="c0999-250">English (United States) en-US</span></span>
-   <span data-ttu-id="c0999-251">Francese (Francia) fr-FR</span><span class="sxs-lookup"><span data-stu-id="c0999-251">French (France) fr-FR</span></span>
-   <span data-ttu-id="c0999-252">Italiano (Italia) it-IT</span><span class="sxs-lookup"><span data-stu-id="c0999-252">Italian (Italy) it-IT</span></span>
-   <span data-ttu-id="c0999-253">Tedesco (Germania) de-DE</span><span class="sxs-lookup"><span data-stu-id="c0999-253">German (Germany) de-DE</span></span>
-   <span data-ttu-id="c0999-254">Spagnolo, ordinamento internazionale (Spagna) es-ES</span><span class="sxs-lookup"><span data-stu-id="c0999-254">Spanish, International Sort (Spain) es-ES</span></span>
-   <span data-ttu-id="c0999-255">Coreano (Corea) ko-KR</span><span class="sxs-lookup"><span data-stu-id="c0999-255">Korean (Korea) ko-KR</span></span>
-   <span data-ttu-id="c0999-256">Giapponese (Giappone) ja-JP</span><span class="sxs-lookup"><span data-stu-id="c0999-256">Japanese (Japan) ja-JP</span></span>
-   <span data-ttu-id="c0999-257">Portoghese (Brasile) PT-BR</span><span class="sxs-lookup"><span data-stu-id="c0999-257">Portuguese (Brazil) pt-BR</span></span>
-   <span data-ttu-id="c0999-258">Russo (Russia) ru-RU</span><span class="sxs-lookup"><span data-stu-id="c0999-258">Russian (Russia) ru-RU</span></span>
-   <span data-ttu-id="c0999-259">Zh-TW tradizionale cinese</span><span class="sxs-lookup"><span data-stu-id="c0999-259">Chinese Traditional zh-TW</span></span>
-   <span data-ttu-id="c0999-260">Zh-CN semplificato in cinese</span><span class="sxs-lookup"><span data-stu-id="c0999-260">Chinese Simplified zh-CN</span></span>

## <span data-ttu-id="c0999-261">Come ottenere le tecnologie MDOP</span><span class="sxs-lookup"><span data-stu-id="c0999-261">How to Get MDOP Technologies</span></span>

<span data-ttu-id="c0999-262">MBAM 2,0 SP1 fa parte di Microsoft Desktop Optimization Pack (MDOP).</span><span class="sxs-lookup"><span data-stu-id="c0999-262">MBAM 2.0 SP1 is a part of the Microsoft Desktop Optimization Pack (MDOP).</span></span> <span data-ttu-id="c0999-263">MDOP fa parte di Microsoft Software Assurance.</span><span class="sxs-lookup"><span data-stu-id="c0999-263">MDOP is part of Microsoft Software Assurance.</span></span> <span data-ttu-id="c0999-264">Per altre informazioni su Microsoft Software Assurance e sull'acquisizione di MDOP, vedere [come si ottiene MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .</span><span class="sxs-lookup"><span data-stu-id="c0999-264">For more information about Microsoft Software Assurance and acquiring MDOP, see [How Do I Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) (https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="c0999-265">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0999-265">Related topics</span></span>

[<span data-ttu-id="c0999-266">Note sulla versione di MBAM 2.0 SP1</span><span class="sxs-lookup"><span data-stu-id="c0999-266">Release Notes for MBAM 2.0 SP1</span></span>](release-notes-for-mbam-20-sp1.md)









