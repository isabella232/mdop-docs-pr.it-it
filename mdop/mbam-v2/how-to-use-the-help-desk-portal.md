---
title: Come usare il portale del supporto tecnico
description: Come usare il portale del supporto tecnico
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826326"
---
# <span data-ttu-id="df3af-103">Come usare il portale del supporto tecnico</span><span class="sxs-lookup"><span data-stu-id="df3af-103">How to Use the Help Desk Portal</span></span>


<span data-ttu-id="df3af-104">Il sito Web di amministrazione e monitoraggio di MBAM, denominato anche portale help desk, è un'interfaccia amministrativa per la crittografia unità BitLocker installata come parte dell'infrastruttura del server di amministrazione e monitoraggio di Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="df3af-104">The MBAM Administration and Monitoring website, also referred to as the Help Desk Portal, is an administrative interface to BitLocker drive encryption that is installed as part of the Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure.</span></span> <span data-ttu-id="df3af-105">Nelle sezioni seguenti viene descritto come usare questo sito Web per esaminare i report, recuperare le unità degli utenti finali e gestire i TPMs degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="df3af-105">The following sections describe how you can use this website to review reports, recover end users’ drives, and manage end users’ TPMs.</span></span>

## <a href="" id="bkmk-reports"></a><span data-ttu-id="df3af-106">Rapporti</span><span class="sxs-lookup"><span data-stu-id="df3af-106">Reports</span></span>


<span data-ttu-id="df3af-107">MBAM raccoglie informazioni da Active Directory e computer client, che consente di eseguire report diversi per monitorare l'uso e la conformità di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="df3af-107">MBAM collects information from Active Directory and client computers, which enables you to run different reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="df3af-108">Usando la sezione **report** del sito Web amministrazione e monitoraggio, è possibile generare report sulla conformità aziendale, sui singoli computer e sulle attività di ripristino delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="df3af-108">Using the **Reports** section of the Administration and Monitoring website, you can generate reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="df3af-109">Per una descrizione di ogni report, vedere [informazioni sui report di mbam](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="df3af-109">For a description of each report, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

**<span data-ttu-id="df3af-110">Per accedere ai report</span><span class="sxs-lookup"><span data-stu-id="df3af-110">To access reports</span></span>**

1.  <span data-ttu-id="df3af-111">Aprire un Web browser e passare al sito Web di amministrazione e monitoraggio di MBAM.</span><span class="sxs-lookup"><span data-stu-id="df3af-111">Open a web browser and navigate to the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="df3af-112">Selezionare **report** nel riquadro sinistro.</span><span class="sxs-lookup"><span data-stu-id="df3af-112">Select **Reports** in the left pane.</span></span>

3.  <span data-ttu-id="df3af-113">Nella barra dei menu superiore selezionare il tipo di report che si vuole generare.</span><span class="sxs-lookup"><span data-stu-id="df3af-113">From the top menu bar, select the report type you want to generate.</span></span> <span data-ttu-id="df3af-114">Per salvare i report, fare clic sul pulsante **Esporta** nella barra dei menu report.</span><span class="sxs-lookup"><span data-stu-id="df3af-114">To save reports, click the **Export** button on the Reports menu bar.</span></span>

<span data-ttu-id="df3af-115">Per altre informazioni su come eseguire i report di MBAM, vedere [come generare report di mbam](how-to-generate-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="df3af-115">For additional information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

## <a href="" id="bkmk-drirec"></a><span data-ttu-id="df3af-116">Ripristino unità</span><span class="sxs-lookup"><span data-stu-id="df3af-116">Drive Recovery</span></span>


<span data-ttu-id="df3af-117">La funzionalità di **recupero unità** del sito Web amministrazione e monitoraggio consente agli utenti con ruoli di amministratore specifici, ad esempio gli utenti del supporto tecnico, di accedere ai dati chiave di ripristino raccolti dal client mbam.</span><span class="sxs-lookup"><span data-stu-id="df3af-117">The **Drive Recovery** feature of the Administration and Monitoring website allows users with specific administrator roles (for example, Help Desk Users) to access recovery key data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="df3af-118">Questi dati possono essere usati per accedere a un'unità protetta da BitLocker quando BitLocker entra in modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="df3af-118">This data can be used to access a BitLocker-protected drive when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="df3af-119">Per istruzioni su come recuperare un'unità in modalità di ripristino, vedere [come recuperare un'unità in modalità di ripristino](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="df3af-119">For instructions on how to recover a drive that is in recovery mode, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span></span>

<span data-ttu-id="df3af-120">È anche possibile recuperare le unità che sono state spostate o danneggiate:</span><span class="sxs-lookup"><span data-stu-id="df3af-120">You can also recover drives that have been moved or that are corrupted:</span></span>

-   [<span data-ttu-id="df3af-121">Come recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="df3af-121">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="df3af-122">Come recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="df3af-122">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

<span data-ttu-id="df3af-123">Per altre informazioni su come recuperare un'unità protetta da BitLocker, vedere [eseguire la gestione di BitLocker con mbam](performing-bitlocker-management-with-mbam-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="df3af-123">For additional information about how to recover a BitLocker-protected drive, see [Performing BitLocker Management with MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span></span>

## <a href="" id="bkmk-manatpm"></a><span data-ttu-id="df3af-124">Gestisci TPM</span><span class="sxs-lookup"><span data-stu-id="df3af-124">Manage TPM</span></span>


<span data-ttu-id="df3af-125">La funzionalità Gestisci TPM del sito Web di amministrazione e monitoraggio offre agli utenti determinati ruoli di amministratore, ad esempio gli utenti di "MBAM helpdesk", accedono ai dati del TPM raccolti dal client MBAM.</span><span class="sxs-lookup"><span data-stu-id="df3af-125">The Manage TPM feature of the Administration and Monitoring website gives users with certain administrator roles (for example, “MBAM Helpdesk Users”) access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="df3af-126">In un blocco TPM un amministratore può usare il sito Web di amministrazione e monitoraggio per recuperare il file di password necessario per sbloccare il TPM.</span><span class="sxs-lookup"><span data-stu-id="df3af-126">In a TPM lockout, an administrator can use the Administration and Monitoring website to retrieve the necessary password file to unlock the TPM.</span></span> <span data-ttu-id="df3af-127">Per istruzioni su come reimpostare un TPM dopo un blocco TPM, vedere [come reimpostare un blocco TPM](how-to-reset-a-tpm-lockout-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="df3af-127">For instructions on how to reset a TPM after a TPM lockout, see [How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-2.md).</span></span>

## <a href="" id="bkmk-helpdesk"></a> <span data-ttu-id="df3af-128">MBAM help desk attività</span><span class="sxs-lookup"><span data-stu-id="df3af-128">MBAM Help Desk Tasks</span></span>


<span data-ttu-id="df3af-129">È possibile usare il sito Web di amministrazione e monitoraggio per molte attività amministrative, ad esempio la gestione dell'hardware protetto da BitLocker, il recupero delle unità e l'uso di report.</span><span class="sxs-lookup"><span data-stu-id="df3af-129">You can use the Administration and Monitoring website for many administrative tasks, such as managing BitLocker-protected hardware, recovering drives, and running reports.</span></span> <span data-ttu-id="df3af-130">Per impostazione predefinita, l'URL del sito Web di amministrazione e monitoraggio è http:// &lt; *MBAMAdministrationServername* &gt; , anche se è possibile personalizzarlo durante il processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="df3af-130">By default, the URL for the Administration and Monitoring website is http://&lt;*MBAMAdministrationServername*&gt;, although you can customize it during the installation process.</span></span>

<span data-ttu-id="df3af-131">**Nota**  Per accedere alle varie funzionalità offerte dal sito Web di amministrazione e monitoraggio, è necessario disporre dei ruoli appropriati associati al proprio account utente.</span><span class="sxs-lookup"><span data-stu-id="df3af-131">**Note** To access the various features offered by the Administration and Monitoring website, you must have the appropriate roles associated with your user account.</span></span> <span data-ttu-id="df3af-132">Per altre informazioni sulla comprensione dei ruoli utente, vedere [come gestire i ruoli di amministratore di mbam](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="df3af-132">For more information about understanding user roles, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

 

<span data-ttu-id="df3af-133">Usare i collegamenti seguenti per trovare informazioni sulle attività che è possibile eseguire tramite il sito Web amministrazione e monitoraggio:</span><span class="sxs-lookup"><span data-stu-id="df3af-133">Use the following links to find information about the tasks that you can perform by using the Administration and Monitoring website:</span></span>

-   [<span data-ttu-id="df3af-134">Come ripristinare un blocco del TPM</span><span class="sxs-lookup"><span data-stu-id="df3af-134">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [<span data-ttu-id="df3af-135">Come recuperare un'unità in modalità di ripristino</span><span class="sxs-lookup"><span data-stu-id="df3af-135">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [<span data-ttu-id="df3af-136">Come recuperare un'unità spostata</span><span class="sxs-lookup"><span data-stu-id="df3af-136">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="df3af-137">Come recuperare un'unità danneggiata</span><span class="sxs-lookup"><span data-stu-id="df3af-137">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [<span data-ttu-id="df3af-138">Come determinare lo stato della crittografia BitLocker nei computer smarriti</span><span class="sxs-lookup"><span data-stu-id="df3af-138">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





