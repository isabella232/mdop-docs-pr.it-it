---
title: Come generare report di MBAM
description: Come generare report di MBAM
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824095"
---
# <span data-ttu-id="cf390-103">Come generare report di MBAM</span><span class="sxs-lookup"><span data-stu-id="cf390-103">How to Generate MBAM Reports</span></span>


<span data-ttu-id="cf390-104">Quando si installa Microsoft BitLocker Administration and Monitoring (MBAM) con la topologia autonoma, è possibile generare report diversi per monitorare l'uso e la conformità della crittografia BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cf390-104">When you install Microsoft BitLocker Administration and Monitoring (MBAM) with the Stand-alone topology, you can generate different reports to monitor BitLocker encryption usage and compliance.</span></span> <span data-ttu-id="cf390-105">Le procedure descritte in questo argomento illustrano come aprire il sito Web di amministrazione e monitoraggio e i passaggi necessari per generare i report di amministrazione e monitoraggio di Microsoft BitLocker in conformità aziendale, singoli computer e attività di ripristino delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="cf390-105">The procedures in this topic describe how to open the Administration and Monitoring website and the steps that are needed to generate Microsoft BitLocker Administration and Monitoring reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="cf390-106">Per informazioni dettagliate utili per comprendere i report di MBAM, vedere informazioni sui [report di mbam](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="cf390-106">For detailed information to help understand MBAM reports, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

<span data-ttu-id="cf390-107">**Nota**  Per eseguire i report, è necessario essere membri del **ruolo report Users** nei computer in cui sono installate le funzionalità di amministrazione e monitoraggio del server, la conformità e il database di controllo e i report di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="cf390-107">**Note** To run the reports, you must be a member of the **Report Users Role** on the computers where the Administration and Monitoring Server features, Compliance and Audit Database, and Compliance and Audit Reports are installed.</span></span>

 

**<span data-ttu-id="cf390-108">Per aprire il sito Web di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="cf390-108">To open the Administration and Monitoring website</span></span>**

1.  <span data-ttu-id="cf390-109">Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="cf390-109">Open a web browser and navigate to the Administration and Monitoring website.</span></span> <span data-ttu-id="cf390-110">L'URL predefinito per il sito Web di amministrazione e monitoraggio è \*http:// &lt; nomecomputer &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="cf390-110">The default URL for the Administration and Monitoring website is *http://&lt;computername&gt;*.</span></span>

    <span data-ttu-id="cf390-111">**Nota**  Se colponel e il sito Web di monitoraggio è stato installato in una porta diversa da 80, è necessario specificare la porta nell'URL, ad esempio \*http:// &lt; nomecomputer &gt; : &lt; porta &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="cf390-111">**Note** If theAdministration and Monitoring website was installed on a port other than 80, you have to specify the port in the URL (for example, *http://&lt;computername&gt;:&lt;port&gt;*.</span></span> <span data-ttu-id="cf390-112">Se è stato specificato un nome host per colponel e il sito Web di monitoraggio durante l'installazione, l'URL è \*http:// &lt; hostname &gt; \*.</span><span class="sxs-lookup"><span data-stu-id="cf390-112">If you specified a host name for theAdministration and Monitoring website during the installation, the URL is *http://&lt;hostname&gt;*.</span></span>

     

2.  <span data-ttu-id="cf390-113">Nel riquadro sinistro fare clic su **report** e quindi selezionare il report che si vuole eseguire dalla barra dei menu superiore.</span><span class="sxs-lookup"><span data-stu-id="cf390-113">In the left pane, click **Reports** and then select the report you want to run from the top menu bar.</span></span>

    <span data-ttu-id="cf390-114">I dati del client MBAM storici vengono conservati nel database di conformità per riferimenti cronologici nel caso in cui un computer venga smarrito o rubato.</span><span class="sxs-lookup"><span data-stu-id="cf390-114">Historical MBAM client data is retained in the compliance database for historical reference in case a computer is lost or stolen.</span></span> <span data-ttu-id="cf390-115">Durante l'esecuzione di report aziendali, è consigliabile usare le date di inizio e di fine appropriate per l'ambito dei tempi per i report da una a due settimane per aumentare la precisione dei dati di report.</span><span class="sxs-lookup"><span data-stu-id="cf390-115">When running enterprise reports, we recommend that you use appropriate start and end dates to scope the time frames for the reports from one to two weeks to increase reporting data accuracy.</span></span>

    <span data-ttu-id="cf390-116">**Nota**  Se SSRS non è stato configurato per l'uso di Secure Socket Layer, l'URL per i report verrà impostato su HTTP anziché su HTTPS quando si installa il server MBAM.</span><span class="sxs-lookup"><span data-stu-id="cf390-116">**Note** If SSRS was not configured to use Secure Socket Layer, the URL for the reports will be set to HTTP instead of to HTTPS when you install the MBAM Server.</span></span> <span data-ttu-id="cf390-117">Se si passa al portale help desk e si seleziona un report, viene visualizzato il messaggio seguente: "viene visualizzato solo il contenuto protetto".</span><span class="sxs-lookup"><span data-stu-id="cf390-117">If you then go to the Help Desk portal and select a report, the following message displays: “Only Secure Content is Displayed.”</span></span> <span data-ttu-id="cf390-118">Per visualizzare il report, fare clic su **Mostra tutto il contenuto**.</span><span class="sxs-lookup"><span data-stu-id="cf390-118">To show the report, click **Show All Content**.</span></span>

     

**<span data-ttu-id="cf390-119">Per generare un report di conformità aziendale</span><span class="sxs-lookup"><span data-stu-id="cf390-119">To generate an Enterprise Compliance Report</span></span>**

1.  <span data-ttu-id="cf390-120">Nel sito Web amministrazione e monitoraggio selezionare il nodo **report** dal riquadro di spostamento sinistro, selezionare **report conformità aziendale**e selezionare i filtri da usare.</span><span class="sxs-lookup"><span data-stu-id="cf390-120">From the Administration and Monitoring website, select the **Reports** node from the left navigation pane, select **Enterprise Compliance Report**, and select the filters that you want to use.</span></span> <span data-ttu-id="cf390-121">I filtri disponibili per il report conformità aziendale sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf390-121">The available filters for the Enterprise Compliance Report are the following:</span></span>

    -   <span data-ttu-id="cf390-122">**Stato conformità**.</span><span class="sxs-lookup"><span data-stu-id="cf390-122">**Compliance Status**.</span></span> <span data-ttu-id="cf390-123">Usare questo filtro per specificare i tipi di stato di conformità (ad esempio, conforme o non conformi) del report.</span><span class="sxs-lookup"><span data-stu-id="cf390-123">Use this filter to specify the compliance status types (for example, Compliant, or Noncompliant) of the report.</span></span>

    -   <span data-ttu-id="cf390-124">**Stato errore**.</span><span class="sxs-lookup"><span data-stu-id="cf390-124">**Error State**.</span></span> <span data-ttu-id="cf390-125">Usare questo filtro per specificare i tipi di stato di errore (ad esempio, nessun errore o errore) del report.</span><span class="sxs-lookup"><span data-stu-id="cf390-125">Use this filter to specify the error state types (for example, No Error, or Error) of the report.</span></span>

2.  <span data-ttu-id="cf390-126">Fare clic su **Visualizza report** per visualizzare il report selezionato.</span><span class="sxs-lookup"><span data-stu-id="cf390-126">Click **View Report** to display the selected report.</span></span>

    <span data-ttu-id="cf390-127">I risultati possono essere salvati in diversi formati, ad esempio HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="cf390-127">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

    <span data-ttu-id="cf390-128">**Nota**  Il report conformità aziendale viene generato da un processo SQL che viene eseguito ogni sei ore.</span><span class="sxs-lookup"><span data-stu-id="cf390-128">**Note** The Enterprise Compliance report is generated by a SQL job that runs every six hours.</span></span> <span data-ttu-id="cf390-129">Di conseguenza, la prima volta che si Visualizza il report, è possibile che siano presenti alcuni dati mancanti.</span><span class="sxs-lookup"><span data-stu-id="cf390-129">Therefore, the first time you view the report, you may find that some data is missing.</span></span> <span data-ttu-id="cf390-130">È possibile generare manualmente i dati del report aggiornati tramite SQL Management Studio.</span><span class="sxs-lookup"><span data-stu-id="cf390-130">You can generate updated report data manually by using SQL Management Studio.</span></span> <span data-ttu-id="cf390-131">Nella finestra **Esplora oggetti** espandere **SQL Server Agent**, espandere **processi**, fare clic con il pulsante destro del mouse sul processo **CreateCache** e scegliere **Avvia processo al passaggio.**</span><span class="sxs-lookup"><span data-stu-id="cf390-131">From the **Object Explorer** window, expand **SQL Server Agent**, expand **Jobs**, right-click the **CreateCache** job, and select **Start Job at Step….**</span></span>

     

3.  <span data-ttu-id="cf390-132">Selezionare un nome di computer per visualizzare le informazioni sul computer nel report conformità computer.</span><span class="sxs-lookup"><span data-stu-id="cf390-132">Select a computer name to view information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="cf390-133">Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.</span><span class="sxs-lookup"><span data-stu-id="cf390-133">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

**<span data-ttu-id="cf390-134">Per generare il report di conformità del computer</span><span class="sxs-lookup"><span data-stu-id="cf390-134">To generate the Computer Compliance Report</span></span>**

1.  <span data-ttu-id="cf390-135">Nel sito Web amministrazione e monitoraggio selezionare il nodo **report** nel riquadro di spostamento sinistro e quindi selezionare il **report conformità computer**.</span><span class="sxs-lookup"><span data-stu-id="cf390-135">In the Administration and Monitoring website, select the **Report** node from the left navigation pane, and then select the **Computer Compliance Report**.</span></span> <span data-ttu-id="cf390-136">Usare il report conformità computer per cercare il nome **utente** o il **nome del computer**.</span><span class="sxs-lookup"><span data-stu-id="cf390-136">Use the Computer Compliance report to search for **user name** or **computer name**.</span></span>

2.  <span data-ttu-id="cf390-137">Fare clic su **Visualizza report** per visualizzare il report computer.</span><span class="sxs-lookup"><span data-stu-id="cf390-137">Click **View Report** to view the computer report.</span></span>

    <span data-ttu-id="cf390-138">I risultati possono essere salvati in diversi formati, ad esempio HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="cf390-138">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

3.  <span data-ttu-id="cf390-139">Selezionare un nome di computer per visualizzare altre informazioni sul computer nel report conformità computer.</span><span class="sxs-lookup"><span data-stu-id="cf390-139">Select a computer name to display more information about the computer in the Computer Compliance Report.</span></span>

4.  <span data-ttu-id="cf390-140">Selezionare il segno più (+) accanto al nome del computer per visualizzare le informazioni sui volumi nel computer.</span><span class="sxs-lookup"><span data-stu-id="cf390-140">Select the plus sign (+) next to the computer name to view information about the volumes on the computer.</span></span>

    <span data-ttu-id="cf390-141">**Nota**  Un computer client di MBAM è considerato conforme se il computer soddisfa i requisiti delle impostazioni dei criteri di MBAM.</span><span class="sxs-lookup"><span data-stu-id="cf390-141">**Note** An MBAM client computer is considered compliant if the computer matches the requirements of the MBAM policy settings.</span></span>

     

**<span data-ttu-id="cf390-142">Per generare il report di controllo chiave di ripristino</span><span class="sxs-lookup"><span data-stu-id="cf390-142">To generate the Recovery Key Audit Report</span></span>**

1.  <span data-ttu-id="cf390-143">Nel sito Web amministrazione e monitoraggio selezionare il nodo **report** nel riquadro di spostamento sinistro e quindi selezionare il rapporto di **controllo del ripristino**.</span><span class="sxs-lookup"><span data-stu-id="cf390-143">From the Administration and Monitoring website, select the **Report** node in the left navigation pane, and then select the **Recovery Audit Report**.</span></span> <span data-ttu-id="cf390-144">Selezionare i filtri per il report di controllo chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="cf390-144">Select the filters for your Recovery Key Audit report.</span></span> <span data-ttu-id="cf390-145">I filtri disponibili per gli audit delle chiavi di ripristino sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf390-145">The available filters for Recovery Key audits are as follows:</span></span>

    -   <span data-ttu-id="cf390-146">**Richiedente**.</span><span class="sxs-lookup"><span data-stu-id="cf390-146">**Requestor**.</span></span> <span data-ttu-id="cf390-147">Questo filtro consente agli utenti di specificare il nome utente del richiedente.</span><span class="sxs-lookup"><span data-stu-id="cf390-147">This filter enables users to specify the user name of the requester.</span></span> <span data-ttu-id="cf390-148">Il richiedente è la persona nell'help desk che ha eseguito l'accesso alla chiave per conto di un utente.</span><span class="sxs-lookup"><span data-stu-id="cf390-148">The requester is the person in the Help Desk who accessed the key on behalf of a user.</span></span>

    -   <span data-ttu-id="cf390-149">**Richiedente**.</span><span class="sxs-lookup"><span data-stu-id="cf390-149">**Requestee**.</span></span> <span data-ttu-id="cf390-150">Questo filtro consente agli utenti di specificare il nome utente del richiedente.</span><span class="sxs-lookup"><span data-stu-id="cf390-150">This filter enables users to specify the user name of the requestee.</span></span> <span data-ttu-id="cf390-151">Il richiedente è la persona che ha chiamato l'help desk per ottenere una chiave di ripristino.</span><span class="sxs-lookup"><span data-stu-id="cf390-151">The requestee is the person who called the Help Desk to obtain a recovery key.</span></span>

    -   <span data-ttu-id="cf390-152">**Richiedi risultato**.</span><span class="sxs-lookup"><span data-stu-id="cf390-152">**Request Result**.</span></span> <span data-ttu-id="cf390-153">Questo filtro consente agli utenti di specificare i tipi di risultati della richiesta, ad esempio successo o non riuscito, su cui si vuole basare il report.</span><span class="sxs-lookup"><span data-stu-id="cf390-153">This filter enables users to specify the request result types (for example, Success or Failed) that they want to base the report on.</span></span> <span data-ttu-id="cf390-154">Ad esempio, gli utenti potrebbero voler visualizzare i tentativi di accesso tramite chiave non riusciti.</span><span class="sxs-lookup"><span data-stu-id="cf390-154">For example, users may want to view failed key access attempts.</span></span>

    -   <span data-ttu-id="cf390-155">**Tipo di chiave**.</span><span class="sxs-lookup"><span data-stu-id="cf390-155">**Key Type**.</span></span> <span data-ttu-id="cf390-156">Questo filtro consente agli utenti di specificare il tipo di chiave, ad esempio la password del tasto di ripristino o l'hash della password del TPM, su cui si vuole basare il report.</span><span class="sxs-lookup"><span data-stu-id="cf390-156">This filter enables users to specify the Key Type (for example: Recovery Key Password or TPM Password Hash) that they want to base the report on.</span></span>

    -   <span data-ttu-id="cf390-157">**Data di inizio**.</span><span class="sxs-lookup"><span data-stu-id="cf390-157">**Start Date**.</span></span> <span data-ttu-id="cf390-158">Questo filtro viene usato per definire la parte della data di inizio dell'intervallo di date a cui l'utente vuole segnalare.</span><span class="sxs-lookup"><span data-stu-id="cf390-158">This filter is used to define the Start Date part of the date range that the user wants to report on.</span></span>

    -   <span data-ttu-id="cf390-159">**Data di fine**.</span><span class="sxs-lookup"><span data-stu-id="cf390-159">**End Date**.</span></span> <span data-ttu-id="cf390-160">Questo filtro viene usato per definire la parte relativa alla data di fine dell'intervallo di date a cui gli utenti vogliono segnalare.</span><span class="sxs-lookup"><span data-stu-id="cf390-160">This filter is used to define the End Date part of the date range that the users want to report on.</span></span>

2.  <span data-ttu-id="cf390-161">Fare clic su **Visualizza report** per visualizzare il report.</span><span class="sxs-lookup"><span data-stu-id="cf390-161">Click **View Report** to view the report.</span></span>

    <span data-ttu-id="cf390-162">I risultati possono essere salvati in diversi formati, ad esempio HTML, Microsoft Word e Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="cf390-162">Results can be saved in different formats, such as HTML, Microsoft Word, and Microsoft Excel.</span></span>

## <span data-ttu-id="cf390-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cf390-163">Related topics</span></span>


[<span data-ttu-id="cf390-164">Monitoraggio e creazione di report sulla conformità di BitLocker con MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="cf390-164">Monitoring and Reporting BitLocker Compliance with MBAM 2.0</span></span>](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





