---
title: Informazioni sulle fasi di sequenziazione
description: Informazioni sulle fasi di sequenziazione
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820005"
---
# <span data-ttu-id="837ba-103">Informazioni sulle fasi di sequenziazione</span><span class="sxs-lookup"><span data-stu-id="837ba-103">About Sequencing Phases</span></span>


<span data-ttu-id="837ba-104">La sequenziazione è il processo con cui crei un pacchetto di applicazione sequenziale usando Microsoft Application Virtualization (App-V) Sequencer.</span><span class="sxs-lookup"><span data-stu-id="837ba-104">Sequencing is the process by which you create a sequenced application package by using the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="837ba-105">Durante la sequenziazione, il sequencer monitora e registra tutti i processi di installazione e configurazione per un'applicazione e crea i file seguenti: ICO, OSD, SFT e SPRJ.</span><span class="sxs-lookup"><span data-stu-id="837ba-105">During sequencing, the Sequencer monitors and records all installation and setup processes for an application and creates the following files: ICO, OSD, SFT, and SPRJ.</span></span> <span data-ttu-id="837ba-106">Questi file contengono tutte le informazioni necessarie su un'applicazione e consentono l'esecuzione dell'applicazione in un ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="837ba-106">These files contain all the necessary information about an application, and they allow that application to run in a virtual environment.</span></span>

<span data-ttu-id="837ba-107">Le quattro fasi per la sequenziazione di un'applicazione e la creazione di un pacchetto di applicazione virtuale sono installazione, avvio, personalizzazione e salvataggio.</span><span class="sxs-lookup"><span data-stu-id="837ba-107">The four phases to sequencing an application and creating a virtual application package are installation, launch, customization, and save.</span></span> <span data-ttu-id="837ba-108">L'elenco seguente fornisce informazioni su ognuna delle fasi:</span><span class="sxs-lookup"><span data-stu-id="837ba-108">The following list provides information about each of the phases:</span></span>

1.  <span data-ttu-id="837ba-109">**Fase di installazione**: durante la fase di installazione, specificare il nome del pacchetto e un commento associato facoltativo che verrà associato al pacchetto.</span><span class="sxs-lookup"><span data-stu-id="837ba-109">**Installation phase**—During the installation phase, you specify the package name and an optional associated comment that will be associated with the package.</span></span> <span data-ttu-id="837ba-110">È anche possibile configurare le opzioni di monitoraggio avanzato durante questa fase.</span><span class="sxs-lookup"><span data-stu-id="837ba-110">You can also configure advanced monitoring options during this phase.</span></span> <span data-ttu-id="837ba-111">Le opzioni di monitoraggio avanzate includono la specifica della dimensione del blocco e se si installeranno gli aggiornamenti automatici durante il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="837ba-111">Advanced monitoring options include specifying the block size and whether you will install automatic updates during monitoring.</span></span> <span data-ttu-id="837ba-112">Il sequencer registra tutte le informazioni e le configurazioni necessarie per creare un pacchetto di applicazione virtuale e le impostazioni del file e del registro di sistema associate.</span><span class="sxs-lookup"><span data-stu-id="837ba-112">The sequencer records all necessary information and configurations required to create a virtual application package and the associated file and registry settings.</span></span>

    <span data-ttu-id="837ba-113">**Importante**  Per visualizzare le opzioni avanzate, selezionare **Mostra opzioni di monitoraggio avanzato** nella pagina **informazioni pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="837ba-113">**Important** To view the advanced options select **Show Advanced Monitoring Options** on the **Package Information** page.</span></span>

     

2.  <span data-ttu-id="837ba-114">**Fase di avvio**: durante la fase di avvio, è possibile specificare le associazioni di file e i descrittori di sicurezza necessari che devono essere configurati con il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="837ba-114">**Launch phase**—During the launch phase, you can specify any required file associations and security descriptors that should be configured with the package.</span></span> <span data-ttu-id="837ba-115">È necessario aprire l'applicazione tutte le volte necessarie per garantire la funzionalità e la stabilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="837ba-115">You should open the application as many times as necessary to ensure application functionality and stability.</span></span>

3.  <span data-ttu-id="837ba-116">**Fase di personalizzazione**: durante la fase di personalizzazione è possibile configurare il pacchetto usando i file OSD associati.</span><span class="sxs-lookup"><span data-stu-id="837ba-116">**Customization phase**—During the customization phase, you can configure your package by using the associated .osd files.</span></span> <span data-ttu-id="837ba-117">Puoi specificare se gli script associati devono essere eseguiti all'interno o all'esterno dell'ambiente virtuale, specificare altre azioni che devono essere eseguite, specificare la modalità di esecuzione degli script associati (in modo sincrono o asincrono) e specificare gli eventuali script aggiuntivi da eseguire nel contesto utente.</span><span class="sxs-lookup"><span data-stu-id="837ba-117">You can specify whether any associated scripts should run inside or outside of the virtual environment, specify additional actions that should be performed, specify how associated scripts run (synchronously or asynchronously), and specify any additional scripts that should be run under the user context.</span></span>

4.  <span data-ttu-id="837ba-118">**Fase di salvataggio**: durante la fase di salvataggio vengono creati tutti i file necessari per il pacchetto dell'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="837ba-118">**Save phase**—During the save phase, all required files for the virtual application package are created.</span></span> <span data-ttu-id="837ba-119">I file creati sono. sprj,. SFT,. OSD,. ico,. XML manifest e il file Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="837ba-119">The files created are .sprj, .sft, .osd, .ico, .xml manifest, and the Windows installer (.msi) file.</span></span>

## <span data-ttu-id="837ba-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="837ba-120">Related topics</span></span>


[<span data-ttu-id="837ba-121">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="837ba-121">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





