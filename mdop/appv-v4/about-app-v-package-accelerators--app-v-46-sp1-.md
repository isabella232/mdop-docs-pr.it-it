---
title: Informazioni sugli acceleratori pacchetto di App-V (App-V 4.6 SP1)
description: Informazioni sugli acceleratori pacchetto di App-V (App-V 4.6 SP1)
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820095"
---
# <span data-ttu-id="fcaf9-103">Informazioni sugli acceleratori pacchetto di App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="fcaf9-103">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="fcaf9-104">Puoi usare gli acceleratori del pacchetto App-V per sequenziare automaticamente le applicazioni di grandi dimensioni e complesse.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-104">You can use App-V Package Accelerators to automatically sequence large, complex applications.</span></span> <span data-ttu-id="fcaf9-105">Inoltre, quando applichi un Acceleratore pacchetto App-V, non devi sempre installare manualmente un'applicazione per creare il pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-105">Additionally, when you apply an App-V Package Accelerator, you are not always required to manually install an application to create the virtual application package.</span></span>

<span data-ttu-id="fcaf9-106">**Nota**  In alcuni casi viene richiesto di installare un'applicazione localmente nel computer che esegue App-V Sequencer prima di poter usare l'Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-106">**Note** In some cases, you are prompted to install an application locally to the computer running the App-V Sequencer before you can use the Package Accelerator.</span></span> <span data-ttu-id="fcaf9-107">Per installare un'applicazione, è necessario installare l'applicazione nella posizione predefinita dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-107">If you have to install an application, you must install the application to the application’s default location.</span></span> <span data-ttu-id="fcaf9-108">Questa installazione non viene monitorata da App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-108">This installation is not monitored by App-V Sequencer.</span></span> <span data-ttu-id="fcaf9-109">Quando viene creato l'Acceleratore pacchetto App-V, l'autore dell'acceleratore del pacchetto determina se installare un'applicazione localmente è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-109">When the App-V Package Accelerator is created, the author of the Package Accelerator determines whether to install an application locally is required.</span></span>

 

<span data-ttu-id="fcaf9-110">App-V Sequencer estrae i file necessari dall'acceleratore del pacchetto App-V e dal supporto di installazione associato per creare un pacchetto virtuale senza dover monitorare l'installazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-110">App-V Sequencer extracts the required files from the App-V Package Accelerator and associated installation media to create a virtual package without having to monitor the installation of the application.</span></span>

<span data-ttu-id="fcaf9-111">**Importante**  Dichiarazione di non responsabilità: Microsoft Application Virtualization Sequencer non offre alcun diritto di licenza per l'applicazione software in uso per creare un Acceleratore pacchetto.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-111">**Important** Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="fcaf9-112">È necessario rispettare tutte le condizioni di licenza per l'utente finale per tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-112">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="fcaf9-113">È tua responsabilità assicurarti che le condizioni di licenza dell'applicazione software ti consentano di creare un Acceleratore pacchetto usando Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-113">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>

 

<span data-ttu-id="fcaf9-114">Gli acceleratori del pacchetto App-V e i modelli di progetto sono diversi tra loro.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-114">App-V Package Accelerators and project templates differ from each other.</span></span> <span data-ttu-id="fcaf9-115">Gli acceleratori pacchetto sono specifici dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-115">Package Accelerators are application-specific.</span></span> <span data-ttu-id="fcaf9-116">I modelli di progetto consentono agli utenti di salvare le impostazioni di uso comune specifiche di un'organizzazione e di applicarle a più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-116">Project templates enable users to save commonly used settings specific to an organization and apply them to multiple applications.</span></span> <span data-ttu-id="fcaf9-117">È anche possibile creare modelli di progetto al prompt dei comandi, mentre al contrario è necessario usare la console App-V Sequencer per creare acceleratori di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-117">You can also create project templates at the command prompt, while in contrast, you must use the App-V Sequencer console to create Package Accelerators.</span></span> <span data-ttu-id="fcaf9-118">Inoltre, la creazione di un pacchetto tramite un Acceleratore pacchetto e l'applicazione di un modello di progetto non è supportata.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-118">Additionally, creating a package by using a Package Accelerator and applying a project template is not supported.</span></span>

## <span data-ttu-id="fcaf9-119">Condivisione di acceleratori pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="fcaf9-119">Sharing App-V Package Accelerators</span></span>


<span data-ttu-id="fcaf9-120">In questa sezione vengono fornite informazioni sulle procedure consigliate su come condividere gli acceleratori di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-120">This section provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="fcaf9-121">Se si prevede di condividere gli acceleratori di pacchetto, le informazioni come i nomi di computer, le informazioni sugli account utente e le informazioni sulle applicazioni associate potrebbero essere incluse negli acceleratori del pacchetto. l'elenco seguente descrive i metodi da tenere in considerazione durante la creazione di acceleratori di pacchetti:</span><span class="sxs-lookup"><span data-stu-id="fcaf9-121">If you plan to share Package Accelerators, information such as computer names, user account information, and information about the associated applications might be included in the Package Accelerators.The following list describes methods you should consider when creating Package Accelerators:</span></span>

-   <span data-ttu-id="fcaf9-122">**Nome utente**.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-122">**User name**.</span></span> <span data-ttu-id="fcaf9-123">Quando si accede al computer in cui è in uso App-V Sequencer, è necessario usare un account utente generico, ad esempio l'account di **amministratore** predefinito per l'amministrazione del computer o del dominio.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-123">When you log on to the computer running App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account for administering the computer / domain.</span></span> <span data-ttu-id="fcaf9-124">Non usare un account basato su un nome utente esistente.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-124">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="fcaf9-125">**Nome computer**.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-125">**Computer Name**.</span></span> <span data-ttu-id="fcaf9-126">Specificare un nome generale non Identificativo per il computer che ha eseguito il sequencer.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-126">Specify a general, non-identifying name for the computer running the Sequencer.</span></span>

-   <span data-ttu-id="fcaf9-127">**URL del server**.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-127">**Server URL**.</span></span> <span data-ttu-id="fcaf9-128">Nella scheda **distribuzione** della console sequencer usare le impostazioni predefinite per le informazioni di configurazione dell'URL del server.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-128">In the Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="fcaf9-129">**Applicazioni**.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-129">**Applications**.</span></span> <span data-ttu-id="fcaf9-130">Se non si vuole condividere l'elenco delle applicazioni installate nel computer che esegue il sequencer quando è stato creato l'acceleratore del pacchetto, è necessario eliminare il file **appv\_manifest.xml** .</span><span class="sxs-lookup"><span data-stu-id="fcaf9-130">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="fcaf9-131">Questo file si trova nella directory radice del pacchetto del pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-131">This file is located in the package root directory of the virtual application package.</span></span>

<span data-ttu-id="fcaf9-132">Dovresti anche rivedere le impostazioni o i file di configurazione associati al pacchetto di applicazione virtuale per assicurarti che le applicazioni non contengano informazioni personali.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-132">You should also review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.</span></span>

## <span data-ttu-id="fcaf9-133">Protezione degli acceleratori del pacchetto App-V</span><span class="sxs-lookup"><span data-stu-id="fcaf9-133">Securing App-V Package Accelerators</span></span>


<span data-ttu-id="fcaf9-134">Salva sempre gli acceleratori del pacchetto App-V e tutti i supporti di installazione associati in un percorso sicuro della rete per proteggere gli acceleratori del pacchetto App-V e i file di installazione da manomessi o danneggiati.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-134">Always save App-V Package Accelerators and any associated installation media in a secure location on the network to protect the App-V Package Accelerators and the installation files from being tampered with or becoming corrupted.</span></span> <span data-ttu-id="fcaf9-135">Dato che gli acceleratori pacchetto possono anche contenere password e informazioni specifiche dell'utente, è necessario salvare gli acceleratori del pacchetto App-V in una posizione sicura ed è necessario firmare digitalmente l'acceleratore del pacchetto dopo averlo creato in modo che il Publisher possa essere verificato quando viene applicato l'acceleratore del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="fcaf9-135">Because Package Accelerators can also contain password and user-specific information, you must save App-V Package Accelerators in a secure location, and you must digitally sign the Package Accelerator after you create it so that the publisher can be verified when the Package Accelerator is applied.</span></span> <span data-ttu-id="fcaf9-136">Per altre informazioni sulle firme digitali, vedere [linee guida per le procedure per la firma digitale per la sicurezza dei criteri comuni](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .</span><span class="sxs-lookup"><span data-stu-id="fcaf9-136">For more information about digital signatures, see [Application Guidelines on Digital Signature Practices for Common Criteria Security](https://go.microsoft.com/fwlink/?LinkId=204705) (https://go.microsoft.com/fwlink/?LinkId=204705).</span></span>

## <span data-ttu-id="fcaf9-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fcaf9-137">Related topics</span></span>


[<span data-ttu-id="fcaf9-138">Come creare acceleratori pacchetto di App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="fcaf9-138">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[<span data-ttu-id="fcaf9-139">Come applicare un Acceleratore pacchetto per creare un pacchetto di applicazione virtuale (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="fcaf9-139">How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)</span></span>](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 





