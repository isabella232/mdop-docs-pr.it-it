---
title: Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0
description: Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0
author: dansimp
ms.assetid: be76fc9a-31ca-4290-af11-7640dcb87d50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5d17f058bff452f88003ab4488daa7afa846f688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821195"
---
# <span data-ttu-id="fe74c-103">Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="fe74c-103">Planning for Custom Template Deployment for UE-V 1.0</span></span>


<span data-ttu-id="fe74c-104">Microsoft User Experience Virtualization (UE-V) USA i modelli di posizione delle impostazioni (file XML) che definiscono le impostazioni acquisite e applicate da UE-V.</span><span class="sxs-lookup"><span data-stu-id="fe74c-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="fe74c-105">Puoi usare il generatore UE-V per creare modelli di posizione delle impostazioni personalizzati che consentono agli utenti di eseguire il roaming delle impostazioni di applicazioni diverse da quelle incluse nei modelli di UE-V predefiniti.</span><span class="sxs-lookup"><span data-stu-id="fe74c-105">You can use the UE-V Generator to create custom settings location templates that let users roam the settings of applications other than those that are included in the default UE-V templates.</span></span> <span data-ttu-id="fe74c-106">Dopo aver testato il modello personalizzato per verificare che le impostazioni dell'applicazione vengano spostate correttamente in un ambiente di test, è possibile distribuire questi modelli di posizione nei computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="fe74c-106">After you test the custom template to ensure that the application settings roam correctly in a test environment, you can deploy these settings location templates to computers in the enterprise.</span></span>

<span data-ttu-id="fe74c-107">È possibile distribuire i modelli di posizione delle impostazioni personalizzate con un'infrastruttura di distribuzione esistente, ad esempio ESD (Enterprise Software Distribution), con le preferenze dei criteri di gruppo o configurando un catalogo di modelli di impostazioni UE-V.</span><span class="sxs-lookup"><span data-stu-id="fe74c-107">You can deploy your custom settings location templates with an existing deployment infrastructure, such as Enterprise Software Distribution (ESD), with Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="fe74c-108">I modelli distribuiti tramite ESD o criteri di gruppo devono essere registrati con WMI o PowerShell di UE-V.</span><span class="sxs-lookup"><span data-stu-id="fe74c-108">Templates that are deployed by using ESD or Group Policy must be registered with UE-V WMI or PowerShell.</span></span>

## <span data-ttu-id="fe74c-109">Catalogo di modelli di impostazioni</span><span class="sxs-lookup"><span data-stu-id="fe74c-109">Settings template catalog</span></span>


<span data-ttu-id="fe74c-110">Il catalogo dei modelli di impostazioni di virtualizzazione dell'esperienza utente è un percorso di cartella nei computer UE-V o in una condivisione di rete SMB (Server Message Block) in cui sono archiviati tutti i modello di posizione delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="fe74c-110">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="fe74c-111">L'agente UE-V recupera i modelli nuovi o aggiornati da questa posizione.</span><span class="sxs-lookup"><span data-stu-id="fe74c-111">The UE-V agent retrieves new or updated templates from this location.</span></span> <span data-ttu-id="fe74c-112">L'agente UE-V controlla la posizione una volta al giorno e aggiorna il comportamento di sincronizzazione in base ai modelli presenti nella cartella.</span><span class="sxs-lookup"><span data-stu-id="fe74c-112">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="fe74c-113">I modelli aggiunti o aggiornati in questa cartella dall'ultima volta che la cartella è stata selezionata vengono registrati dall'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="fe74c-113">Templates that were added or updated in this folder since the last time that the folder was checked are registered by the UE-V agent.</span></span> <span data-ttu-id="fe74c-114">L'agente UE-V Annulla la registrazione dei modelli rimossi dalla cartella.</span><span class="sxs-lookup"><span data-stu-id="fe74c-114">The UE-V agent deregisters templates that are removed from this folder.</span></span> <span data-ttu-id="fe74c-115">Per impostazione predefinita, i modelli sono registrati e non registrati una volta al giorno alle 3:30 A.M.</span><span class="sxs-lookup"><span data-stu-id="fe74c-115">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="fe74c-116">ora locale dall'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="fe74c-116">local time by the task scheduler.</span></span> <span data-ttu-id="fe74c-117">Per altre informazioni sulle attività di UE-V, vedere [modifica della frequenza delle attività pianificate di UE-v](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="fe74c-117">For more information about the UE-V tasks, see [Changing the Frequency of UE-V Scheduled Tasks](changing-the-frequency-of-ue-v-scheduled-tasks.md).</span></span>

<span data-ttu-id="fe74c-118">È possibile configurare il percorso del catalogo dei modelli di impostazioni usando le opzioni della riga di comando installa, criteri di gruppo, WMI o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe74c-118">You can configure the settings template catalog path by using the install command-line options, Group Policy, WMI, or PowerShell.</span></span> <span data-ttu-id="fe74c-119">I modelli archiviati nel percorso del catalogo dei modelli di impostazioni vengono registrati e annullati automaticamente da un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="fe74c-119">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span> <span data-ttu-id="fe74c-120">È possibile personalizzare l'attività pianificata in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="fe74c-120">You can customize this scheduled task as needed.</span></span>

## <span data-ttu-id="fe74c-121">Sostituire i modelli Microsoft predefiniti</span><span class="sxs-lookup"><span data-stu-id="fe74c-121">Replace the default Microsoft templates</span></span>


<span data-ttu-id="fe74c-122">L'agente UE-V installa un gruppo predefinito di modelli di posizione delle impostazioni per le comuni applicazioni Microsoft e le impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="fe74c-122">The UE-V agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="fe74c-123">Se l'organizzazione richiede versioni personalizzate di questi modelli, l'agente UE-V può essere configurato per l'uso di un catalogo di modelli di impostazioni e quindi sostituire i modelli Microsoft predefiniti.</span><span class="sxs-lookup"><span data-stu-id="fe74c-123">If your enterprise needs customized versions of these templates, the UE-V agent can be configured to use a settings template catalog and you should then replace the default Microsoft templates.</span></span>

<span data-ttu-id="fe74c-124">Durante l'installazione dell'agente UE-V, il parametro della riga di comando `RegisterMSTemplates` può essere usato per disabilitare la registrazione dei modelli Microsoft predefiniti.</span><span class="sxs-lookup"><span data-stu-id="fe74c-124">During the installation of the UE-V agent, the command-line parameter, `RegisterMSTemplates`, can be used to disable the registration of the default Microsoft templates.</span></span> <span data-ttu-id="fe74c-125">Per altre informazioni su come impostare i parametri UE-V, vedere [pianificazione dei metodi di configurazione di UE-v](planning-for-ue-v-configuration-methods.md).</span><span class="sxs-lookup"><span data-stu-id="fe74c-125">For more information about how to set the UE-V parameters, see [Planning for UE-V Configuration Methods](planning-for-ue-v-configuration-methods.md).</span></span>

<span data-ttu-id="fe74c-126">Quando si usano criteri di gruppo per configurare il percorso del catalogo dei modelli di impostazioni, è possibile scegliere di sostituire i modelli Microsoft predefiniti.</span><span class="sxs-lookup"><span data-stu-id="fe74c-126">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="fe74c-127">Se si configurano le impostazioni dei criteri per sostituire i modelli Microsoft predefiniti, tutti i modelli Microsoft predefiniti installati dall'agente UE-V verranno eliminati dal computer e verranno usati solo i modelli presenti nel catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="fe74c-127">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V agent will be deleted from the computer, and only the templates that are located in the settings template catalog will be used.</span></span> <span data-ttu-id="fe74c-128">L'impostazione di configurazione dell'agente UE-V `RegisterMSTemplates` deve essere impostata su true per eseguire l'override del modello Microsoft predefinito.</span><span class="sxs-lookup"><span data-stu-id="fe74c-128">The UE-V Agent configuration setting `RegisterMSTemplates` must be set to true in order to override the default Microsoft template.</span></span>

<span data-ttu-id="fe74c-129">**Nota**  Se si disattiva l'impostazione di questo criterio dopo che è stata abilitata, l'agente UE-V non ripristinerà i modelli Microsoft predefiniti.</span><span class="sxs-lookup"><span data-stu-id="fe74c-129">**Note** If you disable this policy setting after it has been enabled, the UE-V agent will not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="fe74c-130">Se sono presenti modelli personalizzati nel catalogo di modelli di impostazioni che usano lo stesso ID dei modelli Microsoft predefiniti e l'agente UE-V non è configurato per sostituire i modelli Microsoft predefiniti, i modelli Microsoft nel catalogo verranno ignorati.</span><span class="sxs-lookup"><span data-stu-id="fe74c-130">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V agent is not configured to replace the default Microsoft templates, the Microsoft templates in the catalog will be ignored.</span></span>

<span data-ttu-id="fe74c-131">È anche possibile sostituire i modelli predefiniti usando le caratteristiche di PowerShell di UE-V.</span><span class="sxs-lookup"><span data-stu-id="fe74c-131">You can also replace the default templates by using the UE-V PowerShell features.</span></span> <span data-ttu-id="fe74c-132">Per sostituire il modello Microsoft predefinito con PowerShell, annullare la registrazione di tutti i modelli Microsoft predefiniti e quindi registrare i modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="fe74c-132">To replace the default Microsoft Template with PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="fe74c-133">**Nota**  I pacchetti di impostazioni precedenti rimangono nella posizione di archiviazione delle impostazioni anche se vengono distribuiti nuovi modelli di impostazioni per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fe74c-133">**Note** Old settings packages remain in the settings storage location even if new settings templates are deployed for an application.</span></span> <span data-ttu-id="fe74c-134">Questi pacchetti non vengono letti dall'agente, ma non vengono eliminati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fe74c-134">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <span data-ttu-id="fe74c-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe74c-135">Related topics</span></span>


[<span data-ttu-id="fe74c-136">Pianificazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="fe74c-136">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="fe74c-137">Pianificazione delle applicazioni da sincronizzare con UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="fe74c-137">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

[<span data-ttu-id="fe74c-138">Pianificazione per i metodi di configurazione di UE-V</span><span class="sxs-lookup"><span data-stu-id="fe74c-138">Planning for UE-V Configuration Methods</span></span>](planning-for-ue-v-configuration-methods.md)

<span data-ttu-id="fe74c-139">Pianificazione della distribuzione di modelli personalizzati</span><span class="sxs-lookup"><span data-stu-id="fe74c-139">Planning for Custom Template Deployment</span></span>
 

 





