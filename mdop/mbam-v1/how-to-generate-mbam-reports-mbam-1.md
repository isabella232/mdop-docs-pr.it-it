---
title: Come generare report di MBAM
description: Come generare report di MBAM
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824526"
---
# <span data-ttu-id="a20f9-103">Come generare report di MBAM</span><span class="sxs-lookup"><span data-stu-id="a20f9-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="a20f9-104">Microsoft BitLocker Administration and Monitoring (MBAM) genera diversi report per monitorare l'uso e la conformità della crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a20f9-104">Microsoft BitLocker Administration and Monitoring (MBAM) generates various reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="a20f9-105">Questo argomento descrive come aprire il sito Web di amministrazione di MBAM e come generare report di MBAM su conformità aziendali, singoli computer, compatibilità hardware e attività di recupero tasti.</span><span class="sxs-lookup"><span data-stu-id="a20f9-105">This topic describes how to open the MBAM administration website and how to generate MBAM reports on enterprise compliance, individual computers, hardware compatibility, and key recovery activity.</span></span> <span data-ttu-id="a20f9-106">Per altre informazioni sui report di MBAM, vedere informazioni sui [report di mbam](understanding-mbam-reports-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="a20f9-106">For more information about MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-1.md).</span></span>

<span data-ttu-id="a20f9-107">**Nota**  Per eseguire i report, è necessario essere membri del ruolo **report Users** nei computer in cui sono state installate le funzionalità di amministrazione e monitoraggio del server, il database di conformità e controllo e i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="a20f9-107">**Note** To run the reports, you must be a member of the **Report Users** role on the computers where you have installed the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports.</span></span>

 

**<span data-ttu-id="a20f9-108">Per aprire il sito Web di amministrazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="a20f9-108">To open the MBAM Administration website</span></span>**

1.  <span data-ttu-id="a20f9-109">Aprire un Web browser e passare al sito Web di MBAM.</span><span class="sxs-lookup"><span data-stu-id="a20f9-109">Open a web browser and navigate to the MBAM website.</span></span> <span data-ttu-id="a20f9-110">L'URL predefinito per il sito Web è \*http:// &lt; nomecomputer &gt; \* del server di amministrazione e monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a20f9-110">The default URL for the website is *http://&lt;computername&gt;* of the Microsoft BitLocker Administration and Monitoring server.</span></span>

    <span data-ttu-id="a20f9-111">**Nota**  Se il sito Web di MBAMadministration è stato installato in una porta diversa dalla porta 80, è necessario specificare il numero di porta nell'URL.</span><span class="sxs-lookup"><span data-stu-id="a20f9-111">**Note** If the MBAMadministration website was installed on a port other than port 80, you must specify that port number in the URL.</span></span> <span data-ttu-id="a20f9-112">Ad esempio, \*http:// &lt; nomecomputer &gt; : &lt; Port &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="a20f9-112">For example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="a20f9-113">Se è stato specificato un nome host per il sito Web MBAMadministration durante l'installazione, l'URL *sarebbe &lt; http:// &gt; hostname*.</span><span class="sxs-lookup"><span data-stu-id="a20f9-113">If you specified a Host Name for the MBAMadministration website during the installation, the URL would be *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="a20f9-114">Nel riquadro di spostamento fare clic su **report**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-114">In the navigation pane, click **Reports**.</span></span> <span data-ttu-id="a20f9-115">Nel riquadro principale fare clic sulla scheda relativa al tipo di report: **report conformità aziendale**, report **conformità computer**, **report controllo hardware**o **rapporto di controllo del ripristino**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-115">In the main pane, click the tab for your report type: **Enterprise Compliance Report**, **Computer Compliance Report**, **Hardware Audit Report**, or **Recovery Audit Report**.</span></span>

    <span data-ttu-id="a20f9-116">**Nota**  I dati del client MBAM storici vengono conservati nel database di conformità.</span><span class="sxs-lookup"><span data-stu-id="a20f9-116">**Note** Historical MBAM Client data is retained in the compliance database.</span></span> <span data-ttu-id="a20f9-117">I dati conservati potrebbero essere necessari in caso di perdita o di furto di un computer.</span><span class="sxs-lookup"><span data-stu-id="a20f9-117">This retained data may be needed in case a computer is lost or stolen.</span></span> <span data-ttu-id="a20f9-118">Durante l'esecuzione di report aziendali, è consigliabile usare le date di inizio e di fine appropriate per applicare l'ambito alle scadenze dei report da una a due settimane per aumentare l'accuratezza dei dati di report.</span><span class="sxs-lookup"><span data-stu-id="a20f9-118">When running enterprise reports, you should use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase the reporting data accuracy.</span></span>

     

**<span data-ttu-id="a20f9-119">Per generare un report di conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="a20f9-119">To generate an enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="a20f9-120">Nel sito Web di MBAMadministration fare clic su **report** nel riquadro di spostamento, quindi fare clic sulla scheda **report conformità aziendale** e selezionare i filtri appropriati per il report.</span><span class="sxs-lookup"><span data-stu-id="a20f9-120">On the MBAMadministration website, click **Reports** in the navigation pane, then click the **Enterprise Compliance Report** tab and select the appropriate filters for your report.</span></span> <span data-ttu-id="a20f9-121">Per il report conformità aziendale, è possibile impostare i filtri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a20f9-121">For the Enterprise Compliance Report, you can set the following filters.</span></span>

    -   <span data-ttu-id="a20f9-122">**Stato conformità**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-122">**Compliance Status**.</span></span> <span data-ttu-id="a20f9-123">Usare questo filtro per specificare i tipi di stato di conformità (ad esempio, conformi o non conforme) da includere nel report.</span><span class="sxs-lookup"><span data-stu-id="a20f9-123">Use this filter to specify the compliance status types (for example, Compliant or Noncompliant) to include in the report.</span></span>

    -   <span data-ttu-id="a20f9-124">**Stato errore**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-124">**Error State**.</span></span> <span data-ttu-id="a20f9-125">Usare questo filtro per specificare i tipi di stato di errore, ad esempio nessun errore o errore, da includere nel report.</span><span class="sxs-lookup"><span data-stu-id="a20f9-125">Use this filter to specify the Error State types, such as No Error or Error, to include in the report.</span></span>

2.  <span data-ttu-id="a20f9-126">Fare clic su **Visualizza report** per visualizzare il report specificato.</span><span class="sxs-lookup"><span data-stu-id="a20f9-126">Click **View Report** to display the specified report.</span></span>

    <span data-ttu-id="a20f9-127">I risultati del report possono essere salvati in uno dei diversi formati di file disponibili, ad esempio HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a20f9-127">The report results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="a20f9-128">**Nota**  Il report conformità aziendale viene generato da un processo SQL che viene eseguito ogni sei ore.</span><span class="sxs-lookup"><span data-stu-id="a20f9-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="a20f9-129">Di conseguenza, la prima volta che si prova a visualizzare il report, è possibile che siano presenti alcuni dati mancanti.</span><span class="sxs-lookup"><span data-stu-id="a20f9-129">Therefore, the first time you try to view the report you may find that some data is missing.</span></span>

     

3.  <span data-ttu-id="a20f9-130">Per visualizzare informazioni su un computer nel report conformità computer, selezionare il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="a20f9-130">To view information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="a20f9-131">Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.</span><span class="sxs-lookup"><span data-stu-id="a20f9-131">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="a20f9-132">Per generare il report di conformità del computer</span><span class="sxs-lookup"><span data-stu-id="a20f9-132">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="a20f9-133">Nel sito Web di MBAMadministration selezionare il nodo **report** nel riquadro di spostamento e quindi selezionare il **report conformità computer**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-133">In the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="a20f9-134">Usare il report conformità computer per cercare il nome **utente** o il **nome del computer**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-134">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="a20f9-135">Fare clic su **Visualizza report** per visualizzare il report computer.</span><span class="sxs-lookup"><span data-stu-id="a20f9-135">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="a20f9-136">I risultati possono essere salvati in uno dei diversi formati di file disponibili, ad esempio HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a20f9-136">Results can be saved in any of several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="a20f9-137">Per visualizzare altre informazioni su un computer nel report conformità computer, selezionare il nome del computer.</span><span class="sxs-lookup"><span data-stu-id="a20f9-137">To display more information about a computer in the Computer Compliance Report, select the computer name.</span></span>

4.  <span data-ttu-id="a20f9-138">Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.</span><span class="sxs-lookup"><span data-stu-id="a20f9-138">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="a20f9-139">**Nota**  Un computer client di MBAM è considerato conforme se il computer soddisfa i requisiti delle impostazioni dei criteri di MBAM o il modello hardware del computer è impostato su incompatibile.</span><span class="sxs-lookup"><span data-stu-id="a20f9-139">**Note** An MBAM Client computer is considered compliant if the computer matches the requirements of the MBAM policy settings or the computer’s hardware model is set to incompatible.</span></span> <span data-ttu-id="a20f9-140">Di conseguenza, quando si visualizzano informazioni dettagliate sui volumi del disco associati al computer, i computer esenti da crittografia BitLocker a causa della compatibilità hardware possono essere visualizzati come conformi anche se lo stato di crittografia del volume dell'unità viene visualizzato come non conforme.</span><span class="sxs-lookup"><span data-stu-id="a20f9-140">Therefore, when you are viewing detailed information about the disk volumes associated with the computer, computers that are exempt from BitLocker encryption due to hardware compatibility can be displayed as compliant even though their drive volume encryption status is displayed as noncompliant.</span></span>

     

**<span data-ttu-id="a20f9-141">Per generare il report di controllo compatibilità hardware</span><span class="sxs-lookup"><span data-stu-id="a20f9-141">To generate the Hardware Compatibility Audit Report</span></span>**

1.  <span data-ttu-id="a20f9-142">Dal sito Web di MBAMadministration selezionare il nodo del **report** nel riquadro di spostamento e quindi selezionare il **report di controllo hardware**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-142">From the MBAMadministration website, select the **Report** node from the navigation pane, and then select the **Hardware Audit Report**.</span></span> <span data-ttu-id="a20f9-143">Selezionare i filtri appropriati per il report di controllo hardware.</span><span class="sxs-lookup"><span data-stu-id="a20f9-143">Select the appropriate filters for your Hardware Audit report.</span></span> <span data-ttu-id="a20f9-144">Il report di controllo hardware offre i seguenti filtri disponibili:</span><span class="sxs-lookup"><span data-stu-id="a20f9-144">The Hardware Audit report offers the following available filters:</span></span>

    -   <span data-ttu-id="a20f9-145">**Utente (dominio\\utente)**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-145">**User (Domain\\User)**.</span></span> <span data-ttu-id="a20f9-146">Specifica il nome dell'utente che ha apportato una modifica.</span><span class="sxs-lookup"><span data-stu-id="a20f9-146">Specifies the name of the user who made a change.</span></span>

    -   <span data-ttu-id="a20f9-147">**Modificare il tipo**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-147">**Change Type**.</span></span> <span data-ttu-id="a20f9-148">Specifica il tipo di modifiche da cercare.</span><span class="sxs-lookup"><span data-stu-id="a20f9-148">Specifies the type of changes you are looking for.</span></span>

    -   <span data-ttu-id="a20f9-149">**Data di inizio**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-149">**Start Date**.</span></span> <span data-ttu-id="a20f9-150">Specifica la parte della data di inizio dell'intervallo di date in cui si vuole creare un report.</span><span class="sxs-lookup"><span data-stu-id="a20f9-150">Specifies the Start Date part of the date range that you want to report on.</span></span>

    -   <span data-ttu-id="a20f9-151">**Data di fine**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-151">**End Date**.</span></span> <span data-ttu-id="a20f9-152">Specifica la parte relativa alla data di fine dell'intervallo di date in cui si vuole creare un report.</span><span class="sxs-lookup"><span data-stu-id="a20f9-152">Specifies the End Date part of the date range that you want to report on.</span></span>

2.  <span data-ttu-id="a20f9-153">Fare clic su **Visualizza report** per visualizzare il report.</span><span class="sxs-lookup"><span data-stu-id="a20f9-153">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="a20f9-154">I risultati possono essere salvati in diversi formati di file disponibili, ad esempio HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a20f9-154">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

**<span data-ttu-id="a20f9-155">Per generare il report di controllo chiave di ripristino</span><span class="sxs-lookup"><span data-stu-id="a20f9-155">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="a20f9-156">Nel sito Web MBAMadministration selezionare il nodo **report** nel riquadro di spostamento e quindi selezionare il rapporto di **controllo del ripristino**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-156">From the MBAMadministration website, select the **Report** node in the navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="a20f9-157">Selezionare i filtri per il report di controllo chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a20f9-157">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="a20f9-158">I filtri disponibili per gli audit delle chiavi di ripristino sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a20f9-158">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="a20f9-159">**Richiedente**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-159">**Requestor**.</span></span> <span data-ttu-id="a20f9-160">Specifica il nome utente del richiedente.</span><span class="sxs-lookup"><span data-stu-id="a20f9-160">Specifies the user name of the requestor.</span></span> <span data-ttu-id="a20f9-161">Il richiedente è la persona nell'help desk che ha eseguito l'accesso alla chiave per conto di un utente.</span><span class="sxs-lookup"><span data-stu-id="a20f9-161">The requestor is the person in the help desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="a20f9-162">**Richiedente**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-162">**Requestee**.</span></span> <span data-ttu-id="a20f9-163">Specifica il nome utente del richiedente.</span><span class="sxs-lookup"><span data-stu-id="a20f9-163">Specifies the user name of the requestee.</span></span> <span data-ttu-id="a20f9-164">Il richiedente è la persona che ha chiamato l'help desk per ottenere una chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a20f9-164">The requestee is the person who called the help desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="a20f9-165">**Risultato della richiesta** Specifica i tipi di risultati della richiesta, ad esempio: successo o non riuscito.</span><span class="sxs-lookup"><span data-stu-id="a20f9-165">**Request Result** Specifies the request result types, such as: Success or Failed.</span></span> <span data-ttu-id="a20f9-166">Ad esempio, potresti voler visualizzare i tentativi di accesso tramite chiave non riusciti.</span><span class="sxs-lookup"><span data-stu-id="a20f9-166">For example, you may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="a20f9-167">**Tipo di chiave**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-167">**Key Type**.</span></span> <span data-ttu-id="a20f9-168">Specifica il tipo di chiave, ad esempio: password chiave di ripristino o hash della password del TPM.</span><span class="sxs-lookup"><span data-stu-id="a20f9-168">Specifies the Key Type, such as: Recovery Key Password or TPM Password Hash.</span></span>

    -   <span data-ttu-id="a20f9-169">**Data di inizio**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-169">**Start Date**.</span></span> <span data-ttu-id="a20f9-170">Specifica la parte della data di inizio dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="a20f9-170">Specifies the Start Date part of the date range.</span></span>

    -   <span data-ttu-id="a20f9-171">**Data di fine**.</span><span class="sxs-lookup"><span data-stu-id="a20f9-171">**End Date**.</span></span> <span data-ttu-id="a20f9-172">Specifica la parte relativa alla data di fine dell'intervallo di date.</span><span class="sxs-lookup"><span data-stu-id="a20f9-172">Specifies the End Date part of the date range.</span></span>

2.  <span data-ttu-id="a20f9-173">Fare clic su **Visualizza report** per visualizzare il report.</span><span class="sxs-lookup"><span data-stu-id="a20f9-173">Click **View Report** to display the report.</span></span>

    <span data-ttu-id="a20f9-174">I risultati possono essere salvati in diversi formati di file disponibili, ad esempio HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a20f9-174">Results can be saved in several available file formats such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="a20f9-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a20f9-175">Related topics</span></span>


[<span data-ttu-id="a20f9-176">Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a20f9-176">Monitoring and Reporting BitLocker Compliance with MBAM 1.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





