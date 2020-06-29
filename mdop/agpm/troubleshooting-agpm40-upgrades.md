---
title: Risoluzione dei problemi relativi agli aggiornamenti Advanced Group Policy
description: Risoluzione dei problemi relativi agli aggiornamenti Advanced Group Policy
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818246"
---
# <span data-ttu-id="72ce1-103">Risoluzione dei problemi relativi agli aggiornamenti Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="72ce1-103">Troubleshooting AGPM Upgrades</span></span>

<span data-ttu-id="72ce1-104">In questa sezione vengono elencati i problemi comuni che possono verificarsi quando si aggiorna il server Advanced Group Policy Management in una versione più recente, ad esempio Advanced Group Policy Manager 4,0, in Advanced Group Management 4,3.</span><span class="sxs-lookup"><span data-stu-id="72ce1-104">This section lists common issues that you may encounter when you upgrade your Advanced Group Policy Management (AGPM) server to a newer version (e.g. AGPM 4.0 to AGPM 4.3).</span></span> <span data-ttu-id="72ce1-105">Per diagnosticare i problemi non elencati in questo articolo, potrebbe essere utile visualizzare la [risoluzione dei problemi di Advanced Group Policy Management](troubleshooting-agpm-agpm40.md) o per un amministratore della gestione avanzata Criteri di amministrazione (controllo completo) per usare la registrazione e la traccia.</span><span class="sxs-lookup"><span data-stu-id="72ce1-105">To diagnose issues not listed here, it may be helpful to view the [Troubleshooting AGPM](troubleshooting-agpm-agpm40.md) or for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="72ce1-106">Per altre informazioni, vedere [configurare la registrazione e la traccia](configure-logging-and-tracing-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="72ce1-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md).</span></span>

## <span data-ttu-id="72ce1-107">Quali problemi si verificano?</span><span class="sxs-lookup"><span data-stu-id="72ce1-107">What problems are you having?</span></span>

-   [<span data-ttu-id="72ce1-108">Non è possibile generare un report di differenza GPO HTML (codice di errore 80004003)</span><span class="sxs-lookup"><span data-stu-id="72ce1-108">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a><span data-ttu-id="72ce1-109">Non è possibile generare un report di differenza GPO HTML (codice di errore 80004003)</span><span class="sxs-lookup"><span data-stu-id="72ce1-109">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>

-   <span data-ttu-id="72ce1-110">**Causa**: il pacchetto di aggiornamento della Advanced Group Policy è stato installato con un account errato.</span><span class="sxs-lookup"><span data-stu-id="72ce1-110">**Cause**: You have installed the AGPM upgrade package with an incorrect account.</span></span>

-   <span data-ttu-id="72ce1-111">**Soluzione**: è necessario essere un amministratore della Advanced Group Policy Management per risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="72ce1-111">**Solution**: You will need to be an AGPM administrator in order to fix this issue.</span></span>
    
    -   <span data-ttu-id="72ce1-112">Verificare di conoscere il nome utente & la password dell' **account del servizio Advanced Group Policy Management**.</span><span class="sxs-lookup"><span data-stu-id="72ce1-112">Ensure you know the username & password of your **AGPM service account**.</span></span>

    -   <span data-ttu-id="72ce1-113">Accedere in modo interattivo al server Advanced Group Policy Management come account del servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="72ce1-113">Log onto your AGPM server interactively as your AGPM service account.</span></span>
        
        -   <span data-ttu-id="72ce1-114">Questa operazione è di importanza cruciale, perché l'installazione non riesce se si usa un account diverso.</span><span class="sxs-lookup"><span data-stu-id="72ce1-114">This is critically important, as the install will fail if you use a different account.</span></span>

    -   <span data-ttu-id="72ce1-115">Arrestare il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="72ce1-115">Shutdown the AGPM service.</span></span>
    
    -   <span data-ttu-id="72ce1-116">Installare l'hotfix necessario.</span><span class="sxs-lookup"><span data-stu-id="72ce1-116">Install the required hotfix.</span></span>
    
    -   <span data-ttu-id="72ce1-117">Connettersi a Advanced Group Policy Management usando un client Advanced Group Policy Management per verificare che i report delle differenze funzionino.</span><span class="sxs-lookup"><span data-stu-id="72ce1-117">Connect to AGPM using an AGPM client to test that your difference reports are now functioning.</span></span>
    
## <span data-ttu-id="72ce1-118">Installare il pacchetto hotfix 1 per Microsoft Advanced Group Policy Management 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="72ce1-118">Install Hotfix Package 1 for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>
    
<span data-ttu-id="72ce1-119">**Problema risolto in questo hotfix**: Advanced Group Policy Management non può generare report di differenza quando controlla o gestisce nuovi oggetti Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="72ce1-119">**Issue fixed in this hotfix**: AGPM can't generate difference reports when it controls or manages new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="72ce1-120">**Come ottenere questo aggiornamento**: installare l'ultima versione di Microsoft Desktop Optimization Pack ([versione di manutenzione di 2017 marzo](https://www.microsoft.com/download/details.aspx?id=54967)).</span><span class="sxs-lookup"><span data-stu-id="72ce1-120">**How to get this update**: Install the latest version of Microsoft Desktop Optimization Pack ([March 2017 Servicing Release](https://www.microsoft.com/download/details.aspx?id=54967)).</span></span> <span data-ttu-id="72ce1-121">Per altre informazioni, vedere [KB 4014009](https://support.microsoft.com/help/4014009/) .</span><span class="sxs-lookup"><span data-stu-id="72ce1-121">See [KB 4014009](https://support.microsoft.com/help/4014009/) for more information.</span></span>

<span data-ttu-id="72ce1-122">In particolare, è possibile scegliere di scaricare solo il primo file, `AGPM4.0SP1_Server_X64_KB4014009.exe` dall'elenco presentato dopo aver premuto il pulsante download.</span><span class="sxs-lookup"><span data-stu-id="72ce1-122">More specifically, you can choose to download only the first file, `AGPM4.0SP1_Server_X64_KB4014009.exe`, from the list presented after pressing the download button.</span></span>
      
<span data-ttu-id="72ce1-123">Il collegamento per il download al Microsoft Desktop Optimization Pack (versione di manutenzione di marzo 2017) può essere trovato [qui](https://www.microsoft.com/download/details.aspx?id=54967).</span><span class="sxs-lookup"><span data-stu-id="72ce1-123">The download link to the Microsoft Desktop Optimization Pack (March 2017 Servicing Release) can be found [here](https://www.microsoft.com/download/details.aspx?id=54967).</span></span>
      
      
## <span data-ttu-id="72ce1-124">Collegamento di riferimento</span><span class="sxs-lookup"><span data-stu-id="72ce1-124">Reference link</span></span>
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
