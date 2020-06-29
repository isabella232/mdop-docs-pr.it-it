---
title: Generazione di report autonomi di MBAM 2.5
description: Generazione di report autonomi di MBAM 2.5
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823125"
---
# <span data-ttu-id="7f494-103">Generazione di report autonomi di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7f494-103">Generating MBAM 2.5 Stand-alone Reports</span></span>


<span data-ttu-id="7f494-104">Quando si configura l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) con la topologia autonoma, è possibile generare report per monitorare l'utilizzo e la conformità della crittografia unità BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7f494-104">When you configure Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate reports to monitor BitLocker drive encryption usage and compliance.</span></span> <span data-ttu-id="7f494-105">Questo argomento contiene le procedure seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f494-105">This topic contains the following procedures:</span></span>

-   [<span data-ttu-id="7f494-106">Per aprire il sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="7f494-106">To open the Administration and Monitoring Website</span></span>](#bkmk-openadmin)

-   [<span data-ttu-id="7f494-107">Per generare un report di conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="7f494-107">To generate an Enterprise Compliance Report</span></span>](#bkmk-enterprise)

-   [<span data-ttu-id="7f494-108">Per generare un report di conformità del computer</span><span class="sxs-lookup"><span data-stu-id="7f494-108">To generate a Computer Compliance Report</span></span>](#bkmk-computercomp)

-   [<span data-ttu-id="7f494-109">Per generare un report di controllo chiave di ripristino</span><span class="sxs-lookup"><span data-stu-id="7f494-109">To generate a Recovery Key Audit Report</span></span>](#bkmk-recoverykey)

<span data-ttu-id="7f494-110">Per le descrizioni dei report autonomi, vedere informazioni sui report autonomi di [MBAM 2,5](understanding-mbam-25-stand-alone-reports.md).</span><span class="sxs-lookup"><span data-stu-id="7f494-110">For descriptions of the Stand-alone reports, see [Understanding MBAM 2.5 Stand-alone Reports](understanding-mbam-25-stand-alone-reports.md).</span></span>

<span data-ttu-id="7f494-111">**Nota**  Per eseguire i report, è necessario essere un membro del gruppo di **utenti del report mbam** , che si configura in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7f494-111">**Note** To run the reports, you must be a member of the **MBAM Report Users** group, which you configure in Active Directory Domain Services.</span></span> <span data-ttu-id="7f494-112">Per altre informazioni, Vedi [pianificazione per i gruppi e gli account di MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="7f494-112">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md).</span></span>

 

<a href="" id="bkmk-openadmin"></a>**<span data-ttu-id="7f494-113">Per aprire il sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="7f494-113">To open the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="7f494-114">Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7f494-114">Open a web browser and navigate to the Administration and Monitoring Website.</span></span> <span data-ttu-id="7f494-115">L'URL predefinito per il sito Web di amministrazione e monitoraggio è:</span><span class="sxs-lookup"><span data-stu-id="7f494-115">The default URL for the Administration and Monitoring Website is:</span></span>

    *<span data-ttu-id="7f494-116">http (s):// &lt; MBAMAdministrationServerName &gt; : &lt; porta &gt; /helpdesk</span><span class="sxs-lookup"><span data-stu-id="7f494-116">http(s)://&lt;MBAMAdministrationServerName&gt;:&lt;port&gt;/Helpdesk</span></span>*

2.  <span data-ttu-id="7f494-117">Nel riquadro sinistro fare clic su **report**.</span><span class="sxs-lookup"><span data-stu-id="7f494-117">In the left pane, click **Reports**.</span></span> <span data-ttu-id="7f494-118">Nella barra dei menu superiore selezionare il report che si vuole eseguire.</span><span class="sxs-lookup"><span data-stu-id="7f494-118">From the top menu bar, select the report you want to run.</span></span>

    <span data-ttu-id="7f494-119">I dati del client MBAM vengono conservati nel database di conformità e controllo per riferimenti cronologici in caso di perdita o di furto di un computer.</span><span class="sxs-lookup"><span data-stu-id="7f494-119">MBAM client data is retained in the Compliance and Audit Database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="7f494-120">Durante l'esecuzione di report aziendali, è consigliabile usare le date di inizio e di fine appropriate per l'ambito dei tempi per i report da una a due settimane per aumentare la precisione dei dati di report.</span><span class="sxs-lookup"><span data-stu-id="7f494-120">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="7f494-121">Dopo aver generato un report, è possibile salvare i risultati in formati diversi, ad esempio HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="7f494-121">After you generate a report, you can save the results in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="7f494-122">**Nota**  Configurare SQL Server Reporting Services (SSRS) in modo da usare SSL (Secure Sockets Layer) prima di configurare il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7f494-122">**Note** Configure SQL Server Reporting Services (SSRS) to use Secure Sockets Layer (SSL) before configuring the Administration and Monitoring Website.</span></span> <span data-ttu-id="7f494-123">Se, per qualsiasi motivo, SSRS non è configurato per l'uso di SSL, l'URL per i report verrà impostato su HTTP anziché su HTTPS quando si configura il sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="7f494-123">If, for any reason, SSRS is not configured to use SSL, the URL for the Reports will be set to HTTP instead of to HTTPS when you configure the Administration and Monitoring Website.</span></span> <span data-ttu-id="7f494-124">Se si passa al sito Web amministrazione e monitoraggio e si seleziona un report, viene visualizzato il messaggio seguente: "viene visualizzato solo il contenuto protetto".</span><span class="sxs-lookup"><span data-stu-id="7f494-124">If you then go to the Administration and Monitoring Website and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="7f494-125">Per visualizzare il report, fare clic su **Mostra tutto il contenuto**.</span><span class="sxs-lookup"><span data-stu-id="7f494-125">To show the report, click **Show All Content**.</span></span>

     

<a href="" id="bkmk-enterprise"></a>**<span data-ttu-id="7f494-126">Per generare un report di conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="7f494-126">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="7f494-127">Nel sito Web amministrazione e monitoraggio selezionare il nodo **report** dal riquadro di spostamento sinistro, selezionare **report conformità aziendale**e selezionare i filtri da usare.</span><span class="sxs-lookup"><span data-stu-id="7f494-127">From the Administration and Monitoring Website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="7f494-128">I filtri disponibili per il report conformità aziendale sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f494-128">The available filters for the Enterprise Compliance Report are:</span></span>

    -   <span data-ttu-id="7f494-129">**Stato conformità**.</span><span class="sxs-lookup"><span data-stu-id="7f494-129">**Compliance Status**.</span></span> <span data-ttu-id="7f494-130">Usare questo filtro per specificare i tipi di stato di conformità del report, ad esempio conforme o non conformi.</span><span class="sxs-lookup"><span data-stu-id="7f494-130">Use this filter to specify the compliance status types of the report (for example, Compliant or Noncompliant).</span></span>

    -   <span data-ttu-id="7f494-131">**Stato errore**.</span><span class="sxs-lookup"><span data-stu-id="7f494-131">**Error State**.</span></span> <span data-ttu-id="7f494-132">Usare questo filtro per specificare i tipi di stato di errore del report, ad esempio nessun errore o errore.</span><span class="sxs-lookup"><span data-stu-id="7f494-132">Use this filter to specify the error state types of the report (for example, No Error or Error).</span></span>

2.  <span data-ttu-id="7f494-133">Fare clic su **Visualizza report** per visualizzare il report selezionato.</span><span class="sxs-lookup"><span data-stu-id="7f494-133">Click **View Report** to display the selected report.</span></span>

3.  <span data-ttu-id="7f494-134">Selezionare un nome di computer per visualizzare le informazioni sul computer nel report conformità computer.</span><span class="sxs-lookup"><span data-stu-id="7f494-134">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="7f494-135">Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.</span><span class="sxs-lookup"><span data-stu-id="7f494-135">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

<a href="" id="bkmk-computercomp"></a>**<span data-ttu-id="7f494-136">Per generare un report di conformità del computer</span><span class="sxs-lookup"><span data-stu-id="7f494-136">To generate a Computer Compliance Report</span></span>**

1.  <span data-ttu-id="7f494-137">Nel sito Web amministrazione e monitoraggio selezionare il nodo del **report** nel riquadro di spostamento sinistro e quindi selezionare **report conformità computer**.</span><span class="sxs-lookup"><span data-stu-id="7f494-137">From the Administration and Monitoring Website, select the **Report** node from the left navigation pane, and then select **Computer Compliance Report**.</span></span> <span data-ttu-id="7f494-138">Usare il report conformità computer per cercare il nome **utente** o il **nome del computer**.</span><span class="sxs-lookup"><span data-stu-id="7f494-138">Use the Computer Compliance Report to search for **User name** or **Computer name**.</span></span>

2.  <span data-ttu-id="7f494-139">Fare clic su **Visualizza report** per visualizzare il report conformità computer.</span><span class="sxs-lookup"><span data-stu-id="7f494-139">Click **View Report** to view the Computer Compliance Report.</span></span>

3.  <span data-ttu-id="7f494-140">Selezionare un nome di computer per visualizzare altre informazioni sul computer nel report conformità computer.</span><span class="sxs-lookup"><span data-stu-id="7f494-140">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="7f494-141">Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.</span><span class="sxs-lookup"><span data-stu-id="7f494-141">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="7f494-142">**Nota**  Un computer client di MBAM è considerato conforme se il computer corrisponde o supera i requisiti delle impostazioni dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="7f494-142">**Note** An MBAM client computer is considered compliant if the computer matches or exceeds the requirements of the MBAM Group Policy settings.</span></span>

<a href="" id="bkmk-recoverykey"></a>**<span data-ttu-id="7f494-143">Per generare un report di controllo chiave di ripristino</span><span class="sxs-lookup"><span data-stu-id="7f494-143">To generate a Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="7f494-144">Nel sito Web amministrazione e monitoraggio selezionare il nodo **report** nel riquadro di spostamento sinistro e quindi selezionare rapporto di **controllo ripristino**.</span><span class="sxs-lookup"><span data-stu-id="7f494-144">From the Administration and Monitoring Website, select the **Report** node in the left navigation pane, and then select **Recovery Audit Report**.</span></span> <span data-ttu-id="7f494-145">Selezionare i filtri per il report di controllo chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f494-145">Select the filters for your Recovery Key Audit Report.</span></span> <span data-ttu-id="7f494-146">I filtri disponibili per gli audit delle chiavi di ripristino sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f494-146">The available filters for recovery key audits are as follows:</span></span>

    -   <span data-ttu-id="7f494-147">**Utente helpdesk**.</span><span class="sxs-lookup"><span data-stu-id="7f494-147">**Helpdesk User**.</span></span> <span data-ttu-id="7f494-148">Questo filtro consente agli utenti di specificare il nome utente del richiedente.</span><span class="sxs-lookup"><span data-stu-id="7f494-148">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="7f494-149">Il richiedente è la persona nell'help desk che ha eseguito l'accesso alla chiave per conto di un utente finale.</span><span class="sxs-lookup"><span data-stu-id="7f494-149">The requester is the person in the Help Desk who accessed the key on behalf of an end user.</span></span>

    -   <span data-ttu-id="7f494-150">**Utente finale**.</span><span class="sxs-lookup"><span data-stu-id="7f494-150">**End User**.</span></span> <span data-ttu-id="7f494-151">Questo filtro consente agli utenti di specificare il nome utente del richiedente.</span><span class="sxs-lookup"><span data-stu-id="7f494-151">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="7f494-152">Il richiedente è l'utente finale che ha chiamato l'help desk per ottenere una chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7f494-152">The requestee is the end user who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="7f494-153">**Richiedi risultato**.</span><span class="sxs-lookup"><span data-stu-id="7f494-153">**Request Result**.</span></span> <span data-ttu-id="7f494-154">Questo filtro consente agli utenti di specificare i tipi di risultati della richiesta, ad esempio successo o non riuscito, su cui si vuole basare il report.</span><span class="sxs-lookup"><span data-stu-id="7f494-154">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="7f494-155">Ad esempio, gli utenti potrebbero voler visualizzare i tentativi di accesso tramite chiave non riusciti.</span><span class="sxs-lookup"><span data-stu-id="7f494-155">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="7f494-156">**Tipo di chiave**.</span><span class="sxs-lookup"><span data-stu-id="7f494-156">**Key Type**.</span></span> <span data-ttu-id="7f494-157">Questo filtro consente agli utenti di specificare il tipo di chiave, ad esempio la password del tasto di ripristino o l'hash della password del TPM, su cui si vuole basare il report.</span><span class="sxs-lookup"><span data-stu-id="7f494-157">This filter enables users to specify the key type (for example, Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="7f494-158">**Data di inizio**.</span><span class="sxs-lookup"><span data-stu-id="7f494-158">**Start Date**.</span></span> <span data-ttu-id="7f494-159">Questo filtro viene usato per definire la parte della data di inizio dell'intervallo di date a cui l'utente vuole segnalare.</span><span class="sxs-lookup"><span data-stu-id="7f494-159">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="7f494-160">**Data di fine**.</span><span class="sxs-lookup"><span data-stu-id="7f494-160">**End Date**.</span></span> <span data-ttu-id="7f494-161">Questo filtro viene usato per definire la parte relativa alla data di fine dell'intervallo di date a cui gli utenti vogliono segnalare.</span><span class="sxs-lookup"><span data-stu-id="7f494-161">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="7f494-162">Fare clic su **Visualizza report** per visualizzare il report.</span><span class="sxs-lookup"><span data-stu-id="7f494-162">Click **View Report** to view the report.</span></span>



## <span data-ttu-id="7f494-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7f494-163">Related topics</span></span>


[<span data-ttu-id="7f494-164">Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7f494-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.5</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[<span data-ttu-id="7f494-165">Informazioni sui report autonomi di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="7f494-165">Understanding MBAM 2.5 Stand-alone Reports</span></span>](understanding-mbam-25-stand-alone-reports.md)

 

## <span data-ttu-id="7f494-166">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="7f494-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="7f494-167">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="7f494-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="7f494-168">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="7f494-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





