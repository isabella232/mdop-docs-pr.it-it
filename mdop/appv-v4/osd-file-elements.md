---
title: Elementi di file OSD
description: Elementi di file OSD
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816106"
---
# <span data-ttu-id="f0e83-103">Elementi di file OSD</span><span class="sxs-lookup"><span data-stu-id="f0e83-103">OSD File Elements</span></span>


<span data-ttu-id="f0e83-104">La directory di installazione di sequencer contiene un file di schema XML, **Softricity. xsd**, che definisce la struttura valida di un file OSD (Open Software Descriptor).</span><span class="sxs-lookup"><span data-stu-id="f0e83-104">The Sequencer installation directory contains an XML schema file, **Softricity.xsd**, which defines the valid structure of an Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="f0e83-105">Di seguito sono riportati alcuni degli elementi OSD più usati di frequente.</span><span class="sxs-lookup"><span data-stu-id="f0e83-105">Following are some of the more frequently used OSD elements.</span></span>

<a href="" id="softpkg"></a><span data-ttu-id="f0e83-106">SOFTPKG</span><span class="sxs-lookup"><span data-stu-id="f0e83-106">SOFTPKG</span></span>  
<span data-ttu-id="f0e83-107">Elemento radice del file OSD che contiene tutti gli elementi che definiscono il pacchetto software.</span><span class="sxs-lookup"><span data-stu-id="f0e83-107">The root element of the OSD file containing all elements defining the software package.</span></span>

<a href="" id="codebase"></a><span data-ttu-id="f0e83-108">CODEBASE</span><span class="sxs-lookup"><span data-stu-id="f0e83-108">CODEBASE</span></span>  
<span data-ttu-id="f0e83-109">Informazioni sul file SFT per il pacchetto, inclusi gli attributi HREF, FILENAME e GUID.</span><span class="sxs-lookup"><span data-stu-id="f0e83-109">Information about the .sft file for this package, including the HREF, FILENAME, and GUID attributes.</span></span> <span data-ttu-id="f0e83-110">Puoi modificare l'attributo HREF se modifichi il punto di distribuzione di questo particolare pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f0e83-110">You can edit the HREF attribute if you change the distribution point of this particular package.</span></span>

<a href="" id="os"></a><span data-ttu-id="f0e83-111">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f0e83-111">OS</span></span>  
<span data-ttu-id="f0e83-112">Definisce i sistemi operativi che questa applicazione può eseguire in base ai valori impostati inizialmente nella procedura guidata di sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="f0e83-112">Defines on what operating systems this application can run based on values that are initially set in the Sequencing Wizard.</span></span> <span data-ttu-id="f0e83-113">Questo valore può contenere solo i valori definiti in **Softricity. xsd**.</span><span class="sxs-lookup"><span data-stu-id="f0e83-113">This value can contain only the values defined in **Softricity.xsd**.</span></span>

<a href="" id="local-interaction-allowed"></a><span data-ttu-id="f0e83-114">LOCAL \ _INTERACTION \ _ALLOWED</span><span class="sxs-lookup"><span data-stu-id="f0e83-114">LOCAL\_INTERACTION\_ALLOWED</span></span>  
<span data-ttu-id="f0e83-115">Impostato su TRUE, questo consente di creare oggetti denominati (eventi, mutex, semafori, mapping di file e mailslot) e oggetti COM nello spazio dei nomi globale anziché isolati all'interno di un particolare ambiente virtuale, che consente alle applicazioni virtuali di interagire con le applicazioni del sistema operativo host.</span><span class="sxs-lookup"><span data-stu-id="f0e83-115">Set to TRUE, this enables creation of named objects (events, mutexes, semaphores, file mappings, and mailslots) and COM objects in the global namespace rather than isolated inside a particular virtual environment, which allows virtual applications to interact with the host operating system's applications.</span></span>

<span data-ttu-id="f0e83-116">Esempio: &lt; implementazione di SOFTPKG &gt; &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="f0e83-116">Example:&lt;SOFTPKG&gt;&lt;IMPLEMENTATION&gt;</span></span>

<span data-ttu-id="f0e83-117">&lt;&gt; &lt; criteri virtualenv&gt;</span><span class="sxs-lookup"><span data-stu-id="f0e83-117">&lt;VIRTUALENV&gt;&lt;POLICIES&gt;</span></span>

<span data-ttu-id="f0e83-118">&lt;LOCAL \ _INTERACTION \ _ALLOWED &gt; true</span><span class="sxs-lookup"><span data-stu-id="f0e83-118">&lt;LOCAL\_INTERACTION\_ALLOWED&gt;TRUE</span></span>

<span data-ttu-id="f0e83-119">&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;</span><span class="sxs-lookup"><span data-stu-id="f0e83-119">&lt;/LOCAL\_INTERACTION\_ALLOWED&gt;</span></span>

<span data-ttu-id="f0e83-120">&lt;/POLICIES &gt; &lt; /virtualenv&gt;</span><span class="sxs-lookup"><span data-stu-id="f0e83-120">&lt;/POLICIES&gt;&lt;/VIRTUALENV&gt;</span></span>

<span data-ttu-id="f0e83-121">&lt;/IMPLEMENTATION &gt; &lt; /SOFTPKG&gt;</span><span class="sxs-lookup"><span data-stu-id="f0e83-121">&lt;/IMPLEMENTATION&gt;&lt;/SOFTPKG&gt;</span></span>

<a href="" id="dependencies"></a><span data-ttu-id="f0e83-122">DIPENDENZE</span><span class="sxs-lookup"><span data-stu-id="f0e83-122">DEPENDENCIES</span></span>  
<span data-ttu-id="f0e83-123">Definisce la composizione della famiglia dinamica (dipendenze su altri pacchetti) usando un tag CODEBASE da un altro pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f0e83-123">Defines Dynamic Suite Composition (dependencies on other packages) by using a CODEBASE tag from another package.</span></span>

<span data-ttu-id="f0e83-124">Esempio: &lt; Dipendenze &gt; &lt; codebase href = "RTSPS://Server/package.SFT" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "pkg. 1 \ \ osguard. CP" size = "6572748" obbligatorio = "false"/ &gt; &lt; /Dependencies&gt;</span><span class="sxs-lookup"><span data-stu-id="f0e83-124">Example:&lt;DEPENDENCIES&gt;&lt;CODEBASE HREF="rtsps://server/package.sft" GUID="7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE="pkg.1\\osguard.cp" SIZE="6572748" MANDATORY="FALSE"/&gt;&lt;/DEPENDENCIES&gt;</span></span>

<a href="" id="package-name"></a><span data-ttu-id="f0e83-125">NOME PACCHETTO</span><span class="sxs-lookup"><span data-stu-id="f0e83-125">PACKAGE NAME</span></span>  
<span data-ttu-id="f0e83-126">Un nome comune per il pacchetto immesso nella pagina delle **informazioni del pacchetto** di sequenziazione guidata, che consente di specificare un singolo nome usato per un'applicazione sequenziata contenente più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f0e83-126">A common name for the package entered into the Sequencing Wizard **Package Information** page, which enables you to specify a single name used for a sequenced application containing multiple applications.</span></span>

<a href="" id="title"></a><span data-ttu-id="f0e83-127">TITOLO</span><span class="sxs-lookup"><span data-stu-id="f0e83-127">TITLE</span></span>  
<span data-ttu-id="f0e83-128">Nome descrittivo facoltativo dell'applicazione che si sta sequenziando.</span><span class="sxs-lookup"><span data-stu-id="f0e83-128">Optional descriptive name of the application you are sequencing.</span></span>

<a href="" id="abstract"></a><span data-ttu-id="f0e83-129">ASTRATTO</span><span class="sxs-lookup"><span data-stu-id="f0e83-129">ABSTRACT</span></span>  
<span data-ttu-id="f0e83-130">Breve descrizione del pacchetto software immesso nel campo **Commenti** nella pagina delle **informazioni del pacchetto** di sequenziazione guidata.</span><span class="sxs-lookup"><span data-stu-id="f0e83-130">Short description of the software package entered in the **Comments** field in the Sequencing Wizard **Package Information** page.</span></span> <span data-ttu-id="f0e83-131">Una procedura consigliata consiste nel specificare informazioni come il livello di sistema operativo e di Service Pack della workstation Sequencer, la versione sequencer e il nome dell'ingegnere della sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="f0e83-131">A best practice is to specify information such as the operating system and service-pack level of the Sequencer workstation, Sequencer version, and the sequencing engineer’s name.</span></span>

<a href="" id="script"></a><span data-ttu-id="f0e83-132">SCRIPT</span><span class="sxs-lookup"><span data-stu-id="f0e83-132">SCRIPT</span></span>  
<span data-ttu-id="f0e83-133">Definisce eventi di script specifici che si verificano durante l'avvio, l'arresto o lo streaming.</span><span class="sxs-lookup"><span data-stu-id="f0e83-133">Defines specific scripted events to occur during startup, shutdown, or streaming.</span></span>

<a href="" id="mgmt-shortcutlist"></a><span data-ttu-id="f0e83-134">MGMT \ _SHORTCUTLIST</span><span class="sxs-lookup"><span data-stu-id="f0e83-134">MGMT\_SHORTCUTLIST</span></span>  
<span data-ttu-id="f0e83-135">Elenco di tutti i collegamenti definiti nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="f0e83-135">List of all shortcuts defined in the wizard.</span></span>

<a href="" id="mgmt-fileassociations"></a><span data-ttu-id="f0e83-136">MGMT \ _FILEASSOCIATIONS</span><span class="sxs-lookup"><span data-stu-id="f0e83-136">MGMT\_FILEASSOCIATIONS</span></span>  
<span data-ttu-id="f0e83-137">Elenco dei tipi di file specificati nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="f0e83-137">List of the file types specified in the wizard.</span></span>

## <span data-ttu-id="f0e83-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f0e83-138">Related topics</span></span>


[<span data-ttu-id="f0e83-139">Informazioni sulla scheda OSD</span><span class="sxs-lookup"><span data-stu-id="f0e83-139">About the OSD Tab</span></span>](about-the-osd-tab.md)

 

 





