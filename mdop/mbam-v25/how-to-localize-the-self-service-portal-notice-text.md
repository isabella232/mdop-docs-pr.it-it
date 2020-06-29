---
title: Come localizzare il testo dell'avviso nel portale self-service
description: Come localizzare il testo dell'avviso nel portale self-service
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826715"
---
# <span data-ttu-id="8e1ac-103">Come localizzare il testo dell'avviso nel portale self-service</span><span class="sxs-lookup"><span data-stu-id="8e1ac-103">How to Localize the Self-Service Portal Notice Text</span></span>


<span data-ttu-id="8e1ac-104">È possibile configurare il testo dell'avviso localizzato per la visualizzazione agli utenti finali per impostazione predefinita nel portale self-service.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-104">You can configure localized notice text to display to end users by default in the Self-Service Portal.</span></span> <span data-ttu-id="8e1ac-105">Il file Notice.txt che Visualizza il testo dell'avviso si trova nella directory radice seguente:</span><span class="sxs-lookup"><span data-stu-id="8e1ac-105">The Notice.txt file that displays the notice text is in the following root directory:</span></span>

<span data-ttu-id="8e1ac-106">&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self</span><span class="sxs-lookup"><span data-stu-id="8e1ac-106">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="8e1ac-107">Per visualizzare il testo dell'avviso localizzato, è possibile creare un file Notice.txt localizzato e salvarlo in una specifica cartella della lingua nella directory di esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="8e1ac-107">To display localized notice text, you create a localized Notice.txt file, and then save it under a specific language folder in the following example directory:</span></span>

<span data-ttu-id="8e1ac-108">&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self</span><span class="sxs-lookup"><span data-stu-id="8e1ac-108">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

<span data-ttu-id="8e1ac-109">**Nota**  Puoi configurare il percorso usando l'elemento **NoticeTextPath** nelle **impostazioni dell'applicazione**.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-109">**Note** You can configure the path by using the **NoticeTextPath** item in **Application Settings**.</span></span>

 

<span data-ttu-id="8e1ac-110">MBAM Visualizza il testo dell'avviso in base alle regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="8e1ac-110">MBAM displays the notice text, based on the following rules:</span></span>

-   <span data-ttu-id="8e1ac-111">Se crei un file **Notice.txt** localizzato nella cartella della lingua appropriata, mbam visualizzerà il testo dell'avviso localizzato se il file di **Notice.txt** predefinito esiste.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-111">If you create a localized **Notice.txt** file in the appropriate language folder, MBAM displays the localized notice text if the default **Notice.txt** file exists.</span></span> <span data-ttu-id="8e1ac-112">Se manca il file **Notice.txt** predefinito, viene visualizzato un messaggio che indica che il file predefinito non è presente.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-112">If the default **Notice.txt** file is missing, a message displays indicating that the default file is missing.</span></span>

-   <span data-ttu-id="8e1ac-113">Se MBAM non trova una versione localizzata del file Notice.txt, Visualizza il testo nel file Notice.txt predefinito.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-113">If MBAM does not find a localized version of the Notice.txt file, it displays the text in the default Notice.txt file.</span></span>

-   <span data-ttu-id="8e1ac-114">Se MBAM non trova un file di Notice.txt predefinito, Visualizza il testo predefinito nel portale self-service.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-114">If MBAM does not find a default Notice.txt file, it displays the default text in the Self-Service Portal.</span></span>

<span data-ttu-id="8e1ac-115">**Nota**  Se il browser di un utente finale è impostato su una lingua che non ha una sottocartella o Notice.txt di lingua corrispondente, viene visualizzato il testo nel file Notice.txt nella directory radice seguente:</span><span class="sxs-lookup"><span data-stu-id="8e1ac-115">**Note** If an end user’s browser is set to a language that does not have a corresponding language subfolder or Notice.txt, the text in the Notice.txt file in the following root directory is displayed:</span></span>

<span data-ttu-id="8e1ac-116">&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self</span><span class="sxs-lookup"><span data-stu-id="8e1ac-116">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

 

**<span data-ttu-id="8e1ac-117">Per creare un file Notice.txt localizzato</span><span class="sxs-lookup"><span data-stu-id="8e1ac-117">To create a localized Notice.txt file</span></span>**

1.  <span data-ttu-id="8e1ac-118">Nel server in cui è stato configurato il portale self-service creare una &lt; cartella della *lingua* &gt; nella directory di esempio seguente, dove &lt; *lingua* &gt; rappresenta il nome della lingua localizzata:</span><span class="sxs-lookup"><span data-stu-id="8e1ac-118">On the server where you configured the Self-Service Portal, create a &lt;*Language*&gt; folder in the following example directory, where &lt;*Language*&gt; represents the name of the localized language:</span></span>

    <span data-ttu-id="8e1ac-119">&lt;Directory di installazione *di mbam self-service* &gt; Website\\ servizio \\Self</span><span class="sxs-lookup"><span data-stu-id="8e1ac-119">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\</span></span>

    <span data-ttu-id="8e1ac-120">**Nota**  Alcune cartelle di lingua esistono già, quindi potrebbe non essere necessario creare una cartella.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-120">**Note** Some language folders already exist, so you might not have to create a folder.</span></span> <span data-ttu-id="8e1ac-121">Se è necessario creare una cartella della lingua, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947) per un elenco dei nomi validi che è possibile usare per la cartella della &lt; *lingua* &gt; .</span><span class="sxs-lookup"><span data-stu-id="8e1ac-121">If you do have to create a language folder, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947) for a list of the valid names that you can use for the &lt;*Language*&gt; folder.</span></span>

     

2.  <span data-ttu-id="8e1ac-122">Creare un file di Notice.txt contenente il testo dell'avviso localizzato.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-122">Create a Notice.txt file that contains the localized notice text.</span></span>

3.  <span data-ttu-id="8e1ac-123">Salvare il file Notice.txt nella cartella della &lt; *lingua* &gt; .</span><span class="sxs-lookup"><span data-stu-id="8e1ac-123">Save the Notice.txt file in the &lt;*Language*&gt; folder.</span></span> <span data-ttu-id="8e1ac-124">Ad esempio, per creare un file di Notice.txt localizzato in spagnolo, salvare il file Notice.txt localizzato nella directory di esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="8e1ac-124">For example, to create a localized Notice.txt file in Spanish, save the localized Notice.txt file in the following example directory:</span></span>

    <span data-ttu-id="8e1ac-125">&lt;Directory di installazione *di mbam self-service* &gt; Website\\Es-es servizio \\Self</span><span class="sxs-lookup"><span data-stu-id="8e1ac-125">&lt;*MBAM Self-Service Install Directory*&gt;\\Self Service Website\\Es-es</span></span>

    <span data-ttu-id="8e1ac-126">Il nome della cartella della lingua può essere anche il nome neutro della lingua **es** anziché **es-es**.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-126">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="8e1ac-127">Se il browser dell'utente finale è impostato su **es-es** e tale cartella non esiste, le impostazioni locali padre (come definito in .NET) vengono recuperate e controllate ricorsivamente, risolvendo &lt; la directory di installazione di mbam Self-Service &gt;\\SelfServiceWebsite\\es\\Notice.txt prima di diventare definitivamente il file di Notice.txt predefinito.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-127">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="8e1ac-128">Questo fallback ricorsivo simula le regole di caricamento delle risorse .NET.</span><span class="sxs-lookup"><span data-stu-id="8e1ac-128">This recursive fallback mimics the .NET resource loading rules.</span></span>



## <span data-ttu-id="8e1ac-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8e1ac-129">Related topics</span></span>


[<span data-ttu-id="8e1ac-130">Personalizzazione del portale self-service per l'organizzazione</span><span class="sxs-lookup"><span data-stu-id="8e1ac-130">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

## <span data-ttu-id="8e1ac-131">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="8e1ac-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8e1ac-132">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="8e1ac-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="8e1ac-133">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8e1ac-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





