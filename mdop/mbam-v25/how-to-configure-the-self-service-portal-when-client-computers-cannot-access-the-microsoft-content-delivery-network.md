---
title: Come configurare il portale self-service quando i computer client non possono accedere alla rete di distribuzione dei contenuti Microsoft
description: Come configurare il portale self-service quando i computer client non possono accedere alla rete di distribuzione dei contenuti Microsoft
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824495"
---
# <span data-ttu-id="f2b83-103">Come configurare il portale self-service quando i computer client non possono accedere alla rete di distribuzione dei contenuti Microsoft</span><span class="sxs-lookup"><span data-stu-id="f2b83-103">How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network</span></span>


<span data-ttu-id="f2b83-104">Seguire queste istruzioni se i computer client dell'organizzazione non hanno accesso alla rete CDN (Microsoft AJAX Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="f2b83-104">Follow these instructions if the client computers in your organization do not have access to the Microsoft Ajax Content Delivery Network (CDN).</span></span>

**<span data-ttu-id="f2b83-105">Perché è necessario configurare questo:</span><span class="sxs-lookup"><span data-stu-id="f2b83-105">Why you need to configure this:</span></span>**

<span data-ttu-id="f2b83-106">I computer client devono accedere alla rete CDN, che fornisce al portale self-service l'accesso necessario a determinati file JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f2b83-106">Your client computers need access to the CDN, which gives the Self-Service Portal the required access to certain JavaScript files.</span></span> <span data-ttu-id="f2b83-107">Se non si configura il portale self-service quando i computer client non riescono ad accedere alla rete CDN, verranno visualizzati solo il nome della società e l'account in cui l'utente finale accede.</span><span class="sxs-lookup"><span data-stu-id="f2b83-107">If you don’t configure the Self-Service Portal when client computers cannot access CDN, only the company name and the account under which the end user logs in will be displayed.</span></span> <span data-ttu-id="f2b83-108">Nessun messaggio di errore verrà visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f2b83-108">No error message will be shown.</span></span>

<span data-ttu-id="f2b83-109">**Nota**  In MBAM 2,5 SP1 i file JavaScript sono inclusi nel prodotto e non è necessario seguire le istruzioni in questa sezione per configurare il provider di servizi condivisi per supportare i client che non possono accedere a Internet.</span><span class="sxs-lookup"><span data-stu-id="f2b83-109">**Note** In MBAM 2.5 SP1, the JavaScript files are included in the product, and you do not need to follow the instructions in this section to configure the SSP to support clients that cannot access the internet.</span></span>

 

**<span data-ttu-id="f2b83-110">Come configurare il portale self-service quando i computer client non riescono ad accedere alla rete CDN</span><span class="sxs-lookup"><span data-stu-id="f2b83-110">How to configure the Self-Service Portal when client computers cannot access the CDN</span></span>**

1. <span data-ttu-id="f2b83-111">Scaricare i seguenti file JavaScript dalla rete CDN:</span><span class="sxs-lookup"><span data-stu-id="f2b83-111">Download the following JavaScript files from the CDN:</span></span>

   -   [<span data-ttu-id="f2b83-112">jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="f2b83-112">jQuery-1.10.2.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [<span data-ttu-id="f2b83-113">jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="f2b83-113">jQuery.validate.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [<span data-ttu-id="f2b83-114">jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="f2b83-114">jQuery.validate.unobtrusive.min.js</span></span>](https://go.microsoft.com/fwlink/?LinkID=390517)

2. <span data-ttu-id="f2b83-115">Copiare i file JavaScript nella directory **Scripts** del portale self-service.</span><span class="sxs-lookup"><span data-stu-id="f2b83-115">Copy the JavaScript files to the **Scripts** directory of the Self-Service Portal.</span></span> <span data-ttu-id="f2b83-116">Questa directory si trova in <em> &lt; mbam self-service install directory &gt; \\ </em> self service Website\\Scripts.</span><span class="sxs-lookup"><span data-stu-id="f2b83-116">This directory is located in <em>&lt;MBAM Self-Service Install Directory&gt;\\</em>Self Service Website\\Scripts.</span></span>

3. <span data-ttu-id="f2b83-117">Aprire Gestione Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="f2b83-117">Open Internet Information Services (IIS) Manager.</span></span>

4. <span data-ttu-id="f2b83-118">Espandere i **siti** &gt; **di amministrazione e monitoraggio di Microsoft BitLocker**ed evidenziare **selfservice**.</span><span class="sxs-lookup"><span data-stu-id="f2b83-118">Expand **Sites** &gt; **Microsoft BitLocker Administration and Monitoring**, and highlight **SelfService**.</span></span>

   **<span data-ttu-id="f2b83-119">Nota</span><span class="sxs-lookup"><span data-stu-id="f2b83-119">Note</span></span>**  
   <span data-ttu-id="f2b83-120">*Selfservice* è il nome della directory virtuale predefinita.</span><span class="sxs-lookup"><span data-stu-id="f2b83-120">*SelfService* is the default virtual directory name.</span></span> <span data-ttu-id="f2b83-121">Se si è scelto un nome diverso per questa directory durante la configurazione, ricordarsi di sostituire *selfservice* in queste istruzioni con il nome scelto.</span><span class="sxs-lookup"><span data-stu-id="f2b83-121">If you chose a different name for this directory during the configuration, remember to replace *SelfService* in these instructions with the name you chose.</span></span>

     

5. <span data-ttu-id="f2b83-122">Nel riquadro centrale fare doppio clic su **Impostazioni applicazione**.</span><span class="sxs-lookup"><span data-stu-id="f2b83-122">In the middle pane, double-click **Application Settings**.</span></span>

6. <span data-ttu-id="f2b83-123">Per ogni elemento dell'elenco seguente modificare le impostazioni dell'applicazione per fare riferimento alla nuova posizione sostituendo/ &lt; *directory virtuale* &gt; /con/selfservice/(o qualunque nome scelto durante la configurazione).</span><span class="sxs-lookup"><span data-stu-id="f2b83-123">For each item in the following list, edit the application settings to reference the new location by replacing /&lt;*virtual directory*&gt;/ with /SelfService/ (or whatever name you chose during configuration).</span></span> <span data-ttu-id="f2b83-124">Il percorso della directory virtuale, ad esempio, sarà simile a/selfservice/Scripts/jQuery-1.10.2.min.js.</span><span class="sxs-lookup"><span data-stu-id="f2b83-124">For example, the virtual directory path will be similar to /selfservice/Scripts/ jQuery-1.10.2.min.js.</span></span>

   -   <span data-ttu-id="f2b83-125">jQueryPath:/ &lt; *directory virtuale* &gt; /script/jQuery-1.10.2.min.js</span><span class="sxs-lookup"><span data-stu-id="f2b83-125">jQueryPath: /&lt;*virtual directory*&gt;/Scripts/jQuery-1.10.2.min.js</span></span>

   -   <span data-ttu-id="f2b83-126">jQueryValidatePath:/ &lt; *directory virtuale* &gt; /script/jQuery.validate.min.js</span><span class="sxs-lookup"><span data-stu-id="f2b83-126">jQueryValidatePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.min.js</span></span>

   -   <span data-ttu-id="f2b83-127">jQueryValidateUnobtrusivePath:/ &lt; *directory virtuale* &gt; /script/jQuery.validate.unobtrusive.min.js</span><span class="sxs-lookup"><span data-stu-id="f2b83-127">jQueryValidateUnobtrusivePath: /&lt;*virtual directory*&gt;/Scripts/jQuery.validate.unobtrusive.min.js</span></span>



## <span data-ttu-id="f2b83-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f2b83-128">Related topics</span></span>


[<span data-ttu-id="f2b83-129">Come configurare le applicazioni Web di MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f2b83-129">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

 

## <span data-ttu-id="f2b83-130">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="f2b83-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f2b83-131">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f2b83-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f2b83-132">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f2b83-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





