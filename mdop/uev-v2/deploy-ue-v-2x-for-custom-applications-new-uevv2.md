---
title: Distribuire UE-V 2. x per le applicazioni personalizzate
description: Distribuire UE-V 2. x per le applicazioni personalizzate
author: dansimp
ms.assetid: f7cb089f-d764-4a93-82b6-926fe0385a23
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/19/2016
ms.openlocfilehash: 217f647d948df016c4a6b72736669c2b3305b705
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824405"
---
# <span data-ttu-id="de5d8-103">Distribuire UE-V 2. x per le applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="de5d8-103">Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="de5d8-104">Microsoft User Experience Virtualization (UE-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="de5d8-104">Microsoft User Experience Virtualization (UE-V) 2.0.</span></span> <span data-ttu-id="de5d8-105">2,1 e 2,1 SP1 usano i file XML denominati **modelli di posizione delle impostazioni** per monitorare e sincronizzare le impostazioni delle applicazioni desktop e le impostazioni desktop di Windows tra i computer degli utenti.</span><span class="sxs-lookup"><span data-stu-id="de5d8-105">2.1, and 2.1 SP1 use XML files called **settings location templates** to monitor and synchronize desktop application settings and Windows desktop settings between user computers.</span></span> <span data-ttu-id="de5d8-106">Per impostazione predefinita, alcuni modelli di percorsi impostazioni sono inclusi in UE-V.</span><span class="sxs-lookup"><span data-stu-id="de5d8-106">By default, some settings location templates are included in UE-V.</span></span> <span data-ttu-id="de5d8-107">Se invece si vogliono sincronizzare le impostazioni per le applicazioni desktop diverse da quelle incluse nei modelli predefiniti, è possibile creare modelli di posizione personalizzati con il generatore di impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="de5d8-107">But if you want to synchronize settings for desktop applications other than those included in the default templates, you can create your own custom settings location templates by using the UE-V Generator.</span></span>

<span data-ttu-id="de5d8-108">Dopo aver letto il materiale per la pianificazione in [preparare una distribuzione di UE-v 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md) e aver deciso di sincronizzare le impostazioni per le applicazioni personalizzate (di terze parti, line-of-business e così via), verranno distribuite le caratteristiche di UE-v come descritto in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="de5d8-108">Once you have read through the planning material in [Prepare a UE-V 2.x Deployment](prepare-a-ue-v-2x-deployment-new-uevv2.md) and have decided that you want to synchronize settings for custom applications (third-party, line-of-business, etc.), you will deploy the features of UE-V as described in this topic.</span></span> <span data-ttu-id="de5d8-109">Per iniziare, ecco i passaggi principali necessari per sincronizzare le impostazioni per le applicazioni personalizzate:</span><span class="sxs-lookup"><span data-stu-id="de5d8-109">To start, here are the main steps required to synchronize settings for custom applications:</span></span>

-   [<span data-ttu-id="de5d8-110">Installare il generatore di UEV</span><span class="sxs-lookup"><span data-stu-id="de5d8-110">Install the UEV Generator</span></span>](#uevgen)

    <span data-ttu-id="de5d8-111">Usa il generatore UEV per creare modelli di posizione delle impostazioni XML personalizzati.</span><span class="sxs-lookup"><span data-stu-id="de5d8-111">Use the UEV Generator to create custom XML settings location templates.</span></span>

-   [<span data-ttu-id="de5d8-112">Configurare un catalogo di modelli di impostazioni UE-V</span><span class="sxs-lookup"><span data-stu-id="de5d8-112">Configure a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="de5d8-113">Puoi definire questo percorso in cui vengono archiviati i modelli di posizione delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="de5d8-113">You can define this path where custom settings location templates are stored.</span></span>

-   [<span data-ttu-id="de5d8-114">Creare modelli di posizione delle impostazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="de5d8-114">Create custom settings location templates</span></span>](#createcustomtemplates)

    <span data-ttu-id="de5d8-115">Questi modelli personalizzati consentono agli utenti di sincronizzare le impostazioni per le applicazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="de5d8-115">These custom templates let users sync settings for custom applications.</span></span>

-   [<span data-ttu-id="de5d8-116">Distribuire i modelli di posizione delle impostazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="de5d8-116">Deploy the custom settings location templates</span></span>](#deploycustomtemplates)

    <span data-ttu-id="de5d8-117">Dopo aver testato il modello personalizzato per verificare che le impostazioni vengano sincronizzate correttamente, è possibile distribuire questi modelli in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="de5d8-117">After you test the custom template to ensure that settings are synced correctly, you can deploy these templates in one of these ways:</span></span>

    -   <span data-ttu-id="de5d8-118">Tramite l'infrastruttura di distribuzione esistente, ad esempio Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="de5d8-118">Through your existing deployment infrastructure, such as Configuration Manager</span></span>

    -   <span data-ttu-id="de5d8-119">Usando le preferenze di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="de5d8-119">By using Group Policy preferences</span></span>

    -   [<span data-ttu-id="de5d8-120">Distribuire un catalogo di modelli di impostazioni UE-V</span><span class="sxs-lookup"><span data-stu-id="de5d8-120">Deploy a UE-V settings template catalog</span></span>](#deploycatalogue)

    <span data-ttu-id="de5d8-121">**Nota**  I modelli distribuiti tramite ESD o criteri di gruppo devono essere registrati con Strumentazione gestione Windows (WMI) di UE-V o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de5d8-121">**Note** Templates that are deployed by using ESD or Group Policy must be registered with UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span>

     

## <span data-ttu-id="de5d8-122">Preparare la distribuzione di UE-V 2. x per le applicazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="de5d8-122">Prepare to Deploy UE-V 2.x for Custom Applications</span></span>


<span data-ttu-id="de5d8-123">Prima di iniziare a distribuire le funzionalità UE-V che gestiscono le applicazioni personalizzate, è possibile esaminare solo un paio di elementi.</span><span class="sxs-lookup"><span data-stu-id="de5d8-123">Before you start deploying the UE-V features that handle custom applications, there are just a couple things to review.</span></span>

### <span data-ttu-id="de5d8-124">Generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="de5d8-124">The UE-V Generator</span></span>

<span data-ttu-id="de5d8-125">Il generatore di UE-V monitora un'applicazione per individuare e acquisire le posizioni in cui vengono archiviate le impostazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-125">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="de5d8-126">L'applicazione monitorata deve essere un'applicazione tradizionale.</span><span class="sxs-lookup"><span data-stu-id="de5d8-126">The application that is monitored must be a traditional application.</span></span> <span data-ttu-id="de5d8-127">Si usa il generatore UE-V per creare modelli di posizione delle impostazioni, ma non è possibile creare un modello di posizione delle impostazioni da questi tipi di applicazione:</span><span class="sxs-lookup"><span data-stu-id="de5d8-127">You use the UE-V Generator to create settings location templates, but it cannot create a settings location template from these application types:</span></span>

-   <span data-ttu-id="de5d8-128">Applicazioni virtualizzate</span><span class="sxs-lookup"><span data-stu-id="de5d8-128">Virtualized applications</span></span>

-   <span data-ttu-id="de5d8-129">Applicazioni offerte tramite Servizi terminal</span><span class="sxs-lookup"><span data-stu-id="de5d8-129">Applications that are offered through Terminal Services</span></span>

-   <span data-ttu-id="de5d8-130">Applicazioni Java</span><span class="sxs-lookup"><span data-stu-id="de5d8-130">Java applications</span></span>

-   <span data-ttu-id="de5d8-131">App di Windows  </span><span class="sxs-lookup"><span data-stu-id="de5d8-131">Windows apps</span></span>

<span data-ttu-id="de5d8-132">**Nota**  Non è possibile creare modelli di posizione delle impostazioni di UE-V da applicazioni virtualizzate o Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="de5d8-132">**Note** UE-V settings location templates cannot be created from virtualized applications or Terminal Services applications.</span></span> <span data-ttu-id="de5d8-133">Tuttavia, le impostazioni sincronizzate con i modelli possono essere applicate a tali applicazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-133">However, settings that are synchronized by using the templates can be applied to those applications.</span></span> <span data-ttu-id="de5d8-134">Per creare modelli che supportano le applicazioni VDI (Virtual Desktop Infrastructure) e Servizi terminal, aprire una versione del pacchetto di Windows Installer (con estensione msi) dell'applicazione usando il generatore UE-V.</span><span class="sxs-lookup"><span data-stu-id="de5d8-134">To create templates that support Virtual Desktop Infrastructure (VDI) and Terminal Services applications, open a version of the Windows Installer (.msi) package of the application by using the UE-V Generator.</span></span> <span data-ttu-id="de5d8-135">Per altre informazioni sulla sincronizzazione delle impostazioni per le applicazioni virtuali, vedere [uso di UE-V 2. x con applicazioni di virtualizzazione dell'applicazione](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="de5d8-135">For more information about synchronizing settings for virtual applications, see [Using UE-V 2.x with Application Virtualization Applications](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md).</span></span>

 

<span data-ttu-id="de5d8-136">**Percorsi esclusi:** Il processo di individuazione esclude le posizioni che in genere archiviano i file software dell'applicazione che non sincronizzano correttamente le impostazioni tra i computer degli utenti o gli ambienti di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-136">**Excluded Locations:** The discovery process excludes locations that commonly store application software files that do not synchronize settings well between user computers or computing environments.</span></span> <span data-ttu-id="de5d8-137">Per impostazione predefinita, questi sono esclusi:</span><span class="sxs-lookup"><span data-stu-id="de5d8-137">By default, these are excluded:</span></span>

-   <span data-ttu-id="de5d8-138">HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file a cui l'utente connesso non può scrivere valori</span><span class="sxs-lookup"><span data-stu-id="de5d8-138">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="de5d8-139">HKEY \ _CURRENT \ _USER le chiavi del registro di sistema e i file associati alle funzionalità di base di Windows</span><span class="sxs-lookup"><span data-stu-id="de5d8-139">HKEY\_CURRENT\_USER registry keys and files that are associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="de5d8-140">Tutte le chiavi del registro di sistema che si trovano nell'HKEY \ _LOCAL \ _MACHINE hive</span><span class="sxs-lookup"><span data-stu-id="de5d8-140">All registry keys that are located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="de5d8-141">File che si trovano nelle directory dei file di programma</span><span class="sxs-lookup"><span data-stu-id="de5d8-141">Files that are located in Program Files directories</span></span>

-   <span data-ttu-id="de5d8-142">File che si trovano in utenti \ \ \ [nome utente \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="de5d8-142">Files that are located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="de5d8-143">File di sistema operativo Windows che si trovano in% SystemRoot%</span><span class="sxs-lookup"><span data-stu-id="de5d8-143">Windows operating system files that are located in %Systemroot%</span></span>

<span data-ttu-id="de5d8-144">Se le chiavi del registro di sistema e i file archiviati in percorsi esclusi sono necessari per sincronizzare le impostazioni dell'applicazione, è possibile aggiungere manualmente le posizioni al modello di percorso delle impostazioni durante il processo di creazione del modello.</span><span class="sxs-lookup"><span data-stu-id="de5d8-144">If registry keys and files that are stored in excluded locations are required to synchronize application settings, you can manually add the locations to the settings location template during the template creation process.</span></span>
<span data-ttu-id="de5d8-145">Tuttavia, solo le modifiche apportate all'HKEY \ _CURRENT \ _USER hive verranno sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="de5d8-145">However, only changes to the HKEY\_CURRENT\_USER hive will be sync-ed.</span></span>

### <span data-ttu-id="de5d8-146">Sostituire i modelli Microsoft predefiniti</span><span class="sxs-lookup"><span data-stu-id="de5d8-146">Replace the default Microsoft templates</span></span>

<span data-ttu-id="de5d8-147">L'agente UE-V installa un gruppo predefinito di modelli di posizione delle impostazioni per le comuni applicazioni Microsoft e le impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="de5d8-147">The UE-V Agent installs a default group of settings location templates for common Microsoft applications and Windows settings.</span></span> <span data-ttu-id="de5d8-148">Se si personalizzano questi modelli o si creano modelli di posizione delle impostazioni per la sincronizzazione delle impostazioni per le applicazioni personalizzate, l'agente UE-V può essere configurato per l'uso di un catalogo di modelli di impostazioni per l'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-148">If you customize these templates, or create settings location templates to synchronize settings for custom applications, the UE-V Agent can be configured to use a settings template catalog to store the templates.</span></span> <span data-ttu-id="de5d8-149">In questo caso dovrai includere i modelli predefiniti insieme ai modelli personalizzati nel catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-149">In this case, you will need to include the default templates along with the custom templates in the settings template catalog.</span></span>

<span data-ttu-id="de5d8-150">Quando si [distribuisce un agente UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent), è possibile usare il parametro della riga `RegisterMSTemplates` di comando per disabilitare la registrazione dei modelli Microsoft predefiniti.</span><span class="sxs-lookup"><span data-stu-id="de5d8-150">When you [Deploy a UE-V Agent](https://technet.microsoft.com/library/dn458891.aspx#agent), you can use the command-line parameter `RegisterMSTemplates` to disable the registration of the default Microsoft templates.</span></span>

<span data-ttu-id="de5d8-151">Quando si usano criteri di gruppo per configurare il percorso del catalogo dei modelli di impostazioni, è possibile scegliere di sostituire i modelli Microsoft predefiniti.</span><span class="sxs-lookup"><span data-stu-id="de5d8-151">When you use Group Policy to configure the settings template catalog path, you can choose to replace the default Microsoft templates.</span></span> <span data-ttu-id="de5d8-152">Se si configurano le impostazioni dei criteri per sostituire i modelli Microsoft predefiniti, tutti i modelli Microsoft predefiniti installati dall'agente UE-V vengono eliminati e vengono usati solo i modelli presenti nel catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-152">If you configure the policy settings to replace the default Microsoft templates, all of the default Microsoft templates that are installed by the UE-V Agent are deleted and only the templates that are located in the settings template catalog are used.</span></span> <span data-ttu-id="de5d8-153">Il parametro dell'impostazione di configurazione dell'agente UE-V `RegisterMSTemplates` deve essere impostato su *true* per eseguire l'override del modello Microsoft predefinito.</span><span class="sxs-lookup"><span data-stu-id="de5d8-153">The UE-V Agent configuration setting parameter `RegisterMSTemplates` must be set to *true* in order to override the default Microsoft template.</span></span>

<span data-ttu-id="de5d8-154">**Nota**  Se si disabilita questa impostazione dei criteri dopo che è stata abilitata, l'agente UE-V non ripristinerà i modelli Microsoft predefiniti.</span><span class="sxs-lookup"><span data-stu-id="de5d8-154">**Note** If you disable this policy setting after it has been enabled, the UE-V Agent does not restore the default Microsoft templates.</span></span>

 

<span data-ttu-id="de5d8-155">Se sono presenti modelli personalizzati nel catalogo di modelli di impostazioni che usano lo stesso ID dei modelli Microsoft predefiniti e l'agente UE-V non è configurato per sostituire i modelli Microsoft predefiniti, i modelli Microsoft vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="de5d8-155">If there are customized templates in the settings template catalog that use the same ID as the default Microsoft templates, and the UE-V Agent is not configured to replace the default Microsoft templates, the Microsoft templates are ignored.</span></span>

<span data-ttu-id="de5d8-156">È anche possibile sostituire i modelli predefiniti usando le caratteristiche di Windows PowerShell di UE-V.</span><span class="sxs-lookup"><span data-stu-id="de5d8-156">You can also replace the default templates by using the UE-V Windows PowerShell features.</span></span> <span data-ttu-id="de5d8-157">Per sostituire il modello Microsoft predefinito con Windows PowerShell, annullare la registrazione di tutti i modelli Microsoft predefiniti e quindi registrare i modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="de5d8-157">To replace the default Microsoft template with Windows PowerShell, unregister all of the default Microsoft templates, and then register the customized templates.</span></span>

<span data-ttu-id="de5d8-158">**Nota**  I pacchetti di impostazioni precedenti rimangono nella posizione di archiviazione delle impostazioni anche se si distribuiscono i nuovi modelli di posizione delle impostazioni per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-158">**Note** Old settings packages remain in the settings storage location even if you deploy new settings location templates for an application.</span></span> <span data-ttu-id="de5d8-159">Questi pacchetti non vengono letti dall'agente, ma non vengono eliminati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="de5d8-159">These packages are not read by the agent, but neither are they automatically deleted.</span></span>

 

## <a href="" id="uevgen"></a><span data-ttu-id="de5d8-160">Installare il generatore UEV 2. x</span><span class="sxs-lookup"><span data-stu-id="de5d8-160">Install the UEV 2.x Generator</span></span>


<span data-ttu-id="de5d8-161">Installare il generatore di Microsoft User Experience Virtualization (UE-V) 2,0 in un computer che può essere usato per creare un modello di posizione delle impostazioni personalizzato.</span><span class="sxs-lookup"><span data-stu-id="de5d8-161">Install the Microsoft User Experience Virtualization (UE-V) 2.0 Generator on a computer that you can then use to create a custom settings location template.</span></span> <span data-ttu-id="de5d8-162">Questo computer dovrebbe avere le applicazioni installate per cui devono essere generati i modelli di posizione delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="de5d8-162">This computer should have the applications installed for which custom settings location templates are to be generated.</span></span>

**<span data-ttu-id="de5d8-163">Per installare il generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="de5d8-163">To install the UE-V Generator</span></span>**

1.  <span data-ttu-id="de5d8-164">Come utente con diritti di amministratore locale, individuare il file di installazione del generatore di UE-V **ToolSetup.exe** fornito con il software UE-v.</span><span class="sxs-lookup"><span data-stu-id="de5d8-164">As a user with local administrator rights, locate the UE-V Generator installation file **ToolSetup.exe** provided with the UE-V software.</span></span> <span data-ttu-id="de5d8-165">In alternativa, se si conosce l'architettura del computer, è possibile eseguire il file di Windows Installer (MSI) appropriato, **ToolsSetupx64.msi** o **ToolsSetupx86.msi**.</span><span class="sxs-lookup"><span data-stu-id="de5d8-165">Or, if you know the computer architecture, you can run the appropriate Windows Installer (.msi) file, **ToolsSetupx64.msi** or **ToolsSetupx86.msi**.</span></span>

2.  <span data-ttu-id="de5d8-166">Fare doppio clic sul file di installazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-166">Double-click the installation file.</span></span> <span data-ttu-id="de5d8-167">Verrà visualizzata la configurazione guidata generatore di virtualizzazione dell'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="de5d8-167">The User Experience Virtualization Generator Setup wizard opens.</span></span> <span data-ttu-id="de5d8-168">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="de5d8-168">Click **Next** to continue.</span></span>

3.  <span data-ttu-id="de5d8-169">Accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="de5d8-169">Accept the Microsoft Software License Terms, and then click **Next**.</span></span>

4.  <span data-ttu-id="de5d8-170">Fare clic sulle opzioni per gli aggiornamenti Microsoft e sul programma Analisi utilizzo software.</span><span class="sxs-lookup"><span data-stu-id="de5d8-170">Click the options for Microsoft Updates and the Customer Experience Improvement Program.</span></span>

5.  <span data-ttu-id="de5d8-171">Selezionare la cartella di destinazione in cui installare il generatore UE-V e quindi fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="de5d8-171">Select the destination folder in which to install the UE-V Generator, and then click **Next**.</span></span>

6.  <span data-ttu-id="de5d8-172">Fare clic su **Installa** per avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-172">Click **Install** to begin the installation.</span></span>

    <span data-ttu-id="de5d8-173">**Nota**  Prima dell'installazione dell'applicazione viene visualizzato un prompt per il **controllo dell'account utente** .</span><span class="sxs-lookup"><span data-stu-id="de5d8-173">**Note** A prompt for **User Account Control** appears before the application is installed.</span></span> <span data-ttu-id="de5d8-174">Per installare il generatore UE-V è necessaria l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-174">Permission is required to install the UE-V Generator.</span></span>

     

7.  <span data-ttu-id="de5d8-175">Fare clic su **fine** per chiudere la procedura guidata al termine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-175">Click **Finish** to close the wizard after the installation is finished.</span></span> <span data-ttu-id="de5d8-176">È necessario riavviare il computer prima di poter eseguire il generatore di UE-V.</span><span class="sxs-lookup"><span data-stu-id="de5d8-176">You must restart your computer before you can run the UE-V Generator.</span></span>

    <span data-ttu-id="de5d8-177">Per verificare che l'installazione sia stata eseguita correttamente, fare clic sul pulsante **Start**, scegliere **tutti i programmi**, **Microsoft User Experience Virtualization**e quindi fare clic su **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="de5d8-177">To verify that the installation was successful, click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

    <span data-ttu-id="de5d8-178">**Nota**  Il generatore UE-V 2 può essere usato solo per creare modelli per gli agenti UE-V 2.</span><span class="sxs-lookup"><span data-stu-id="de5d8-178">**Note** The UE-V 2 Generator can only be used to create templates for UE-V 2 Agents.</span></span> <span data-ttu-id="de5d8-179">In una distribuzione mista di agenti UE-V 1,0 e di agenti UE-V 2, è necessario continuare a usare il generatore UE-V 1,0 fino a quando non sono stati aggiornati tutti gli agenti di UE-v.</span><span class="sxs-lookup"><span data-stu-id="de5d8-179">In a mixed deployment of UE-V 1.0 Agents and UE-V 2 Agents, you should continue to use the UE-V 1.0 Generator until you have upgraded all UE-V Agents.</span></span>

     

## <a href="" id="deploycatalogue"></a><span data-ttu-id="de5d8-180">Distribuire un catalogo di modelli di impostazioni</span><span class="sxs-lookup"><span data-stu-id="de5d8-180">Deploy a Settings Template Catalog</span></span>


<span data-ttu-id="de5d8-181">Il catalogo dei modelli di impostazioni di virtualizzazione dell'esperienza utente è un percorso di cartella nei computer UE-V o in una condivisione di rete SMB (Server Message Block) in cui sono archiviati tutti i modello di posizione delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="de5d8-181">The User Experience Virtualization settings template catalog is a folder path on UE-V computers or a Server Message Block (SMB) network share that stores all the custom settings location templates.</span></span> <span data-ttu-id="de5d8-182">Un'attività pianificata nell'agente UE-V controlla questa posizione una volta al giorno e aggiorna il comportamento di sincronizzazione, in base ai modelli in questa cartella.</span><span class="sxs-lookup"><span data-stu-id="de5d8-182">A scheduled task in the UE-V Agent checks this location one time each day and updates its synchronization behavior, based on the templates in this folder.</span></span>

<span data-ttu-id="de5d8-183">L'agente UE-V registra i modelli che sono stati aggiunti o aggiornati in questa cartella dopo l'ultima volta che la cartella è stata selezionata e Annulla la registrazione dei modelli rimossi.</span><span class="sxs-lookup"><span data-stu-id="de5d8-183">The UE-V Agent registers templates that were added or updated in this folder after the last time that the folder was checked and unregisters templates that are removed.</span></span> <span data-ttu-id="de5d8-184">Per impostazione predefinita, i modelli sono registrati e non registrati una volta al giorno alle 3:30 A.M.</span><span class="sxs-lookup"><span data-stu-id="de5d8-184">By default, templates are registered and unregistered one time per day at 3:30 A.M.</span></span> <span data-ttu-id="de5d8-185">ora locale dall'utilità di pianificazione e dall'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="de5d8-185">local time by the Task Scheduler and at system startup.</span></span> <span data-ttu-id="de5d8-186">Per personalizzare la frequenza di questa attività pianificata, vedere [modifica della frequenza delle attività pianificate di UE-V 2. x](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span><span class="sxs-lookup"><span data-stu-id="de5d8-186">To customize the frequency of this scheduled task, see [Changing the Frequency of UE-V 2.x Scheduled Tasks](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).</span></span>

<span data-ttu-id="de5d8-187">È possibile configurare il percorso del catalogo dei modelli di impostazioni usando le opzioni della riga di comando per l'installazione, criteri di gruppo, WMI o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de5d8-187">You can configure the settings template catalog path by using the installation command-line options, Group Policy, WMI, or Windows PowerShell.</span></span> <span data-ttu-id="de5d8-188">I modelli archiviati nel percorso del catalogo dei modelli di impostazioni vengono registrati e annullati automaticamente da un'attività pianificata.</span><span class="sxs-lookup"><span data-stu-id="de5d8-188">Templates that are stored at the settings template catalog path are automatically registered and unregistered by a scheduled task.</span></span>

**<span data-ttu-id="de5d8-189">Per configurare il catalogo dei modelli di impostazioni per UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="de5d8-189">To configure the settings template catalog for UE-V 2.x</span></span>**

1.  <span data-ttu-id="de5d8-190">Creare una nuova cartella nel computer in cui è archiviato il catalogo dei modelli di impostazioni UE-V.</span><span class="sxs-lookup"><span data-stu-id="de5d8-190">Create a new folder on the computer that stores the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="de5d8-191">Impostare le seguenti autorizzazioni SMB per la cartella del catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-191">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="de5d8-192">Account utente</span><span class="sxs-lookup"><span data-stu-id="de5d8-192">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="de5d8-193">Autorizzazioni consigliate</span><span class="sxs-lookup"><span data-stu-id="de5d8-193">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="de5d8-194">Tutti</span><span class="sxs-lookup"><span data-stu-id="de5d8-194">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-195">Nessuna autorizzazione</span><span class="sxs-lookup"><span data-stu-id="de5d8-195">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="de5d8-196">Computer di dominio</span><span class="sxs-lookup"><span data-stu-id="de5d8-196">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-197">Livelli di autorizzazione di lettura</span><span class="sxs-lookup"><span data-stu-id="de5d8-197">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="de5d8-198">Administrators</span><span class="sxs-lookup"><span data-stu-id="de5d8-198">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-199">Livelli di autorizzazione di lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="de5d8-199">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="de5d8-200">Impostare le autorizzazioni di file system NTFS seguenti per la cartella del catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-200">Set the following NTFS file system permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="de5d8-201">Account utente</span><span class="sxs-lookup"><span data-stu-id="de5d8-201">User account</span></span></th>
    <th align="left"><span data-ttu-id="de5d8-202">Autorizzazioni consigliate</span><span class="sxs-lookup"><span data-stu-id="de5d8-202">Recommended permissions</span></span></th>
    <th align="left"><span data-ttu-id="de5d8-203">Applica a</span><span class="sxs-lookup"><span data-stu-id="de5d8-203">Apply to</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="de5d8-204">Creatore/proprietario</span><span class="sxs-lookup"><span data-stu-id="de5d8-204">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-205">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="de5d8-205">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-206">Questa cartella, le sottocartelle e i file</span><span class="sxs-lookup"><span data-stu-id="de5d8-206">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="de5d8-207">Computer di dominio</span><span class="sxs-lookup"><span data-stu-id="de5d8-207">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-208">Contenuto della cartella di elenco e lettura</span><span class="sxs-lookup"><span data-stu-id="de5d8-208">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-209">Questa cartella, le sottocartelle e i file</span><span class="sxs-lookup"><span data-stu-id="de5d8-209">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="de5d8-210">Tutti</span><span class="sxs-lookup"><span data-stu-id="de5d8-210">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-211">Nessuna autorizzazione</span><span class="sxs-lookup"><span data-stu-id="de5d8-211">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-212">Nessuna autorizzazione</span><span class="sxs-lookup"><span data-stu-id="de5d8-212">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="de5d8-213">Administrators</span><span class="sxs-lookup"><span data-stu-id="de5d8-213">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-214">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="de5d8-214">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="de5d8-215">Questa cartella, le sottocartelle e i file</span><span class="sxs-lookup"><span data-stu-id="de5d8-215">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="de5d8-216">Fare clic su **OK** per chiudere le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="de5d8-216">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="de5d8-217">La condivisione di rete deve almeno concedere le autorizzazioni per il gruppo Domain Computers.</span><span class="sxs-lookup"><span data-stu-id="de5d8-217">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="de5d8-218">Concedere inoltre le autorizzazioni di accesso per la cartella di condivisione di rete agli amministratori che gestiscono i modelli archiviati.</span><span class="sxs-lookup"><span data-stu-id="de5d8-218">In addition, grant access permissions for the network share folder to administrators who are to manage the stored templates.</span></span>

## <a href="" id="createcustomtemplates"></a><span data-ttu-id="de5d8-219">Creare modelli di posizione delle impostazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="de5d8-219">Create Custom Settings Location Templates</span></span>


<span data-ttu-id="de5d8-220">Usa il generatore UE-V per creare modelli di posizione delle impostazioni per le applicazioni line-of-business o altre applicazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="de5d8-220">Use the UE-V Generator to create settings location templates for line-of-business applications or other custom applications.</span></span> <span data-ttu-id="de5d8-221">Dopo aver creato il modello per un'applicazione, è possibile distribuirlo nei computer in modo che le impostazioni vengano sincronizzate per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-221">After the template for an application is created, you can deploy it to computers so that settings are synchronized for that application.</span></span>

**<span data-ttu-id="de5d8-222">Per creare un modello di posizione delle impostazioni di UE-V con il generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="de5d8-222">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="de5d8-223">Fare clic sul pulsante **Start**, scegliere **tutti i programmi**, fare clic su **Microsoft User Experience Virtualization**e quindi su **Microsoft User Experience Virtualization Generator**.</span><span class="sxs-lookup"><span data-stu-id="de5d8-223">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="de5d8-224">Fare clic su **Crea modello posizione impostazioni**.</span><span class="sxs-lookup"><span data-stu-id="de5d8-224">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="de5d8-225">Specifica l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-225">Specify the application.</span></span> <span data-ttu-id="de5d8-226">Individuare il percorso del file dell'applicazione (con estensione exe) o il collegamento all'applicazione (con estensione lnk) per cui si vuole creare un modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-226">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="de5d8-227">Specificare gli argomenti della riga di comando, se presenti, e la directory di lavoro, se presenti.</span><span class="sxs-lookup"><span data-stu-id="de5d8-227">Specify the command-line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="de5d8-228">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="de5d8-228">Click **Next** to continue.</span></span>

    <span data-ttu-id="de5d8-229">**Nota**  Prima che l'applicazione venga avviata, il sistema Visualizza un prompt per il **controllo dell'account utente**.</span><span class="sxs-lookup"><span data-stu-id="de5d8-229">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="de5d8-230">È necessaria l'autorizzazione per monitorare il registro di sistema e i percorsi dei file usati dall'applicazione per archiviare le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-230">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="de5d8-231">Dopo l'avvio dell'applicazione, chiudere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-231">After the application starts, close the application.</span></span> <span data-ttu-id="de5d8-232">Il generatore UE-V registra le posizioni in cui vengono archiviate le impostazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-232">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="de5d8-233">Al termine del processo, fare clic su **Avanti** per continuare.</span><span class="sxs-lookup"><span data-stu-id="de5d8-233">After the process is completed, click **Next** to continue.</span></span>

6.  <span data-ttu-id="de5d8-234">Esaminare e selezionare le caselle di controllo accanto alle posizioni appropriate per la sincronizzazione delle impostazioni del registro di sistema e dei file di impostazioni da sincronizzare per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-234">Review and select the check boxes that are next to the appropriate registry settings locations and settings file locations to synchronize for this application.</span></span> <span data-ttu-id="de5d8-235">L'elenco include le due categorie seguenti per i percorsi delle impostazioni:</span><span class="sxs-lookup"><span data-stu-id="de5d8-235">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="de5d8-236">**Standard**: impostazioni dell'applicazione archiviate nel registro di sistema in HKEY \ _CURRENT \ _USER i tasti o nelle cartelle file in \ \ **Users** \ \ \ [nome utente \] \ \ **AppData**  \\  **roaming**.</span><span class="sxs-lookup"><span data-stu-id="de5d8-236">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="de5d8-237">Il generatore UE-V include queste impostazioni per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="de5d8-237">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="de5d8-238">Non **standard**: le impostazioni dell'applicazione archiviate all'esterno delle posizioni vengono specificate nelle procedure consigliate per l'archiviazione dei dati delle impostazioni (facoltativo).</span><span class="sxs-lookup"><span data-stu-id="de5d8-238">**Nonstandard**: Application settings that are stored outside the locations are specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="de5d8-239">Questi includono file e cartelle in **utenti** \ \ \ [nome utente \] \ \ **AppData**  \\  **local**.</span><span class="sxs-lookup"><span data-stu-id="de5d8-239">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="de5d8-240">Esaminare queste posizioni per determinare se includerle nel modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-240">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="de5d8-241">Selezionare le caselle di controllo percorsi per includerle.</span><span class="sxs-lookup"><span data-stu-id="de5d8-241">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="de5d8-242">Fai clic su **Next** per continuare.</span><span class="sxs-lookup"><span data-stu-id="de5d8-242">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="de5d8-243">Rivedere e modificare le **Proprietà**, le posizioni **del registro di sistema** e i percorsi dei **file** per il modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-243">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="de5d8-244">Modificare le proprietà seguenti nella scheda **Proprietà** :</span><span class="sxs-lookup"><span data-stu-id="de5d8-244">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="de5d8-245">**Nome applicazione**: il nome dell'applicazione scritto nella descrizione delle proprietà dei file di programma.</span><span class="sxs-lookup"><span data-stu-id="de5d8-245">**Application Name**: The application name that is written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="de5d8-246">**Nome programma**: il nome del programma che viene ricavato dalle proprietà del file di programma.</span><span class="sxs-lookup"><span data-stu-id="de5d8-246">**Program name**: The name of the program that is taken from the program file properties.</span></span> <span data-ttu-id="de5d8-247">Il nome in genere ha l'estensione exe.</span><span class="sxs-lookup"><span data-stu-id="de5d8-247">This name usually has the .exe file name extension.</span></span>

        -   <span data-ttu-id="de5d8-248">**Versione del prodotto**: il numero di versione del prodotto del file exe dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-248">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="de5d8-249">Questa proprietà, insieme alla versione del **file**, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-249">This property, in conjunction with the **File version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="de5d8-250">Questa proprietà accetta un numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="de5d8-250">This property accepts a major version number.</span></span> <span data-ttu-id="de5d8-251">Se questa proprietà è vuota, il modello di posizione delle impostazioni si applica a tutte le versioni del prodotto.</span><span class="sxs-lookup"><span data-stu-id="de5d8-251">If this property is empty, the settings location template applies to all versions of the product.</span></span>

        -   <span data-ttu-id="de5d8-252">**Versione file**: il numero di versione del file exe dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-252">**File version**: The file version number of the .exe file of the application.</span></span> <span data-ttu-id="de5d8-253">Questa proprietà, insieme alla versione del **prodotto**, consente di determinare quali applicazioni sono destinate al modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-253">This property, in conjunction with the **Product version**, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="de5d8-254">Questa proprietà accetta un numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="de5d8-254">This property accepts a major version number.</span></span> <span data-ttu-id="de5d8-255">Se questa proprietà è vuota, il modello di posizione delle impostazioni si applica a tutte le versioni del programma.</span><span class="sxs-lookup"><span data-stu-id="de5d8-255">If this property is empty, the settings location template applies to all versions of the program.</span></span>

        -   <span data-ttu-id="de5d8-256">**Nome autore modello** (facoltativo): nome dell'autore del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-256">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="de5d8-257">**Autore** di un modello (facoltativo): l'indirizzo di posta elettronica dell'autore del modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-257">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="de5d8-258">La scheda **Registro di sistema** elenca la **chiave** e l' **ambito** delle posizioni del registro di sistema incluse nel modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-258">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="de5d8-259">Modificare i percorsi del registro di sistema usando il menu a discesa **attività** .</span><span class="sxs-lookup"><span data-stu-id="de5d8-259">Edit the registry locations by using the **Tasks** drop-down menu.</span></span> <span data-ttu-id="de5d8-260">Le attività consentono di aggiungere nuove chiavi, modificare il nome o l'ambito delle chiavi esistenti, eliminare le chiavi e passare al registro di sistema in cui si trovano le chiavi.</span><span class="sxs-lookup"><span data-stu-id="de5d8-260">Tasks enable you to add new keys, edit the name or scope of existing keys, delete keys, and browse the registry where the keys are located.</span></span> <span data-ttu-id="de5d8-261">Usare l'ambito **tutte le impostazioni** per includere tutte le impostazioni del registro di sistema sotto la chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="de5d8-261">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="de5d8-262">Usare **tutte le impostazioni e le sottochiavi** per includere tutte le impostazioni del registro di sistema sotto la chiave, le sottochiavi e le impostazioni della sottochiave specificati.</span><span class="sxs-lookup"><span data-stu-id="de5d8-262">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="de5d8-263">Nella scheda **file** sono elencati il percorso del file e la maschera di file delle posizioni di file incluse nel modello di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-263">The **Files** tab lists the file path and file mask of the file locations that are included in the settings location template.</span></span> <span data-ttu-id="de5d8-264">Modificare i percorsi dei file usando il menu a discesa **attività** .</span><span class="sxs-lookup"><span data-stu-id="de5d8-264">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="de5d8-265">Le attività per i percorsi dei file consentono di aggiungere nuovi file o posizioni delle cartelle, modificare l'ambito di file o cartelle esistenti, eliminare file o cartelle e aprire la posizione selezionata in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="de5d8-265">Tasks for file locations enable you to add new files or folder locations, edit the scope of existing files or folders, delete files or folders, and open the selected location in Windows Explorer.</span></span> <span data-ttu-id="de5d8-266">Lascia vuota la maschera di file per includere tutti i file nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="de5d8-266">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="de5d8-267">Fare clic su **Crea**e quindi su **Salva** per salvare il modello posizione impostazioni nel computer.</span><span class="sxs-lookup"><span data-stu-id="de5d8-267">Click **Create**, and then click **Save** to save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="de5d8-268">Fare clic su **Chiudi** per chiudere la procedura guidata modello di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-268">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="de5d8-269">Uscire dall'applicazione Generator UE-V.</span><span class="sxs-lookup"><span data-stu-id="de5d8-269">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="de5d8-270">Dopo aver creato il modello di posizione delle impostazioni per un'applicazione, è consigliabile testare il modello.</span><span class="sxs-lookup"><span data-stu-id="de5d8-270">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="de5d8-271">Distribuire il modello in un ambiente lab prima di inserirlo nella produzione aziendale.</span><span class="sxs-lookup"><span data-stu-id="de5d8-271">Deploy the template in a lab environment before you put it into production in the enterprise.</span></span>

<span data-ttu-id="de5d8-272">Guida di [riferimento allo schema del modello di applicazione per la direttiva UE-v](https://technet.microsoft.com/library/dn763947.aspx) descrive la struttura XML del modello di posizione delle impostazioni di UE-v e fornisce indicazioni per la modifica di questi file.</span><span class="sxs-lookup"><span data-stu-id="de5d8-272">[Application Template Schema Reference for UE-V](https://technet.microsoft.com/library/dn763947.aspx) details the XML structure of the UE-V settings location template and provides guidance for editing these files.</span></span>

## <a href="" id="deploycustomtemplates"></a><span data-ttu-id="de5d8-273">Distribuire i modelli di posizione delle impostazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="de5d8-273">Deploy the Custom Settings Location Templates</span></span>


<span data-ttu-id="de5d8-274">Dopo aver creato un modello di posizione delle impostazioni con il generatore UE-V, è consigliabile testarlo per verificare che le impostazioni dell'applicazione vengano sincronizzate correttamente.</span><span class="sxs-lookup"><span data-stu-id="de5d8-274">After you create a settings location template with the UE-V Generator, you should test it to ensure that the application settings are synchronized correctly.</span></span> <span data-ttu-id="de5d8-275">Puoi quindi distribuire il modello di posizione delle impostazioni in modo sicuro ai computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="de5d8-275">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="de5d8-276">I modelli di posizione delle impostazioni possono essere distribuiti usando uno di questi metodi:</span><span class="sxs-lookup"><span data-stu-id="de5d8-276">Settings location templates can be deployed by using one of these methods:</span></span>

-   <span data-ttu-id="de5d8-277">Sistema ESD (Enterprise Software Distribution), ad esempio System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="de5d8-277">An enterprise software distribution (ESD) system such as System Center Configuration Manager</span></span>

-   <span data-ttu-id="de5d8-278">Preferenze di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="de5d8-278">Group Policy preferences</span></span>

-   <span data-ttu-id="de5d8-279">Catalogo di modelli di impostazioni UE-V</span><span class="sxs-lookup"><span data-stu-id="de5d8-279">A UE-V settings template catalog</span></span>

<span data-ttu-id="de5d8-280">I modelli distribuiti tramite un sistema ESD o gli oggetti Criteri di gruppo devono essere registrati tramite Strumentazione gestione Windows (WMI) di UE-V o Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="de5d8-280">Templates that are deployed by using an ESD system or Group Policy Objects must be registered through UE-V Windows Management Instrumentation (WMI) or Windows PowerShell.</span></span> <span data-ttu-id="de5d8-281">I modelli archiviati nella posizione del catalogo dei modelli di impostazioni vengono automaticamente registrati dall'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="de5d8-281">Templates that are stored in the settings template catalog location are automatically registered by the UE-V Agent.</span></span>

**<span data-ttu-id="de5d8-282">Per usare il percorso del catalogo di modelli di impostazioni per distribuire i modelli di posizione delle impostazioni di UE-V</span><span class="sxs-lookup"><span data-stu-id="de5d8-282">To use the settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="de5d8-283">Passare alla cartella della condivisione di rete definita come catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-283">Browse to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="de5d8-284">Aggiungere, rimuovere o aggiornare i modelli di posizione delle impostazioni nel catalogo dei modelli di impostazioni per riflettere la configurazione del modello di agente UE-V desiderata per i computer UE-V.</span><span class="sxs-lookup"><span data-stu-id="de5d8-284">Add, remove, or update settings location templates in the settings template catalog to reflect the UE-V Agent template configuration that you want for UE-V computers.</span></span>

    <span data-ttu-id="de5d8-285">**Nota**  I modelli nei computer vengono aggiornati giornalmente.</span><span class="sxs-lookup"><span data-stu-id="de5d8-285">**Note** Templates on computers are updated daily.</span></span> <span data-ttu-id="de5d8-286">L'aggiornamento si basa sulle modifiche apportate al catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="de5d8-286">The update is based on changes to the settings template catalog.</span></span>

     

3.  <span data-ttu-id="de5d8-287">Per aggiornare manualmente i modelli in un computer che esegue l'agente UE-V, aprire un prompt dei comandi con privilegi elevati e passare a \*\*% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 o x64 &gt; \*\*, quindi eseguire **ApplySettingsTemplateCatalog.exe**.</span><span class="sxs-lookup"><span data-stu-id="de5d8-287">To manually update templates on a computer that runs the UE-V Agent, open an elevated command prompt, and browse to **%Program Files%\\Microsoft User Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe**.</span></span>

    <span data-ttu-id="de5d8-288">**Nota**  Questo programma viene eseguito automaticamente durante l'avvio del computer e ogni giorno in 3:30 a. M.</span><span class="sxs-lookup"><span data-stu-id="de5d8-288">**Note** This program runs automatically during computer startup and daily at 3:30 A. M.</span></span> <span data-ttu-id="de5d8-289">per raccogliere tutti i nuovi modelli aggiunti di recente al catalogo.</span><span class="sxs-lookup"><span data-stu-id="de5d8-289">to gather any new templates that were recently added to the catalog.</span></span>

     






## <span data-ttu-id="de5d8-290">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de5d8-290">Related topics</span></span>


[<span data-ttu-id="de5d8-291">Preparare una distribuzione UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="de5d8-291">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="de5d8-292">Distribuire le funzionalità necessarie per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="de5d8-292">Deploy Required Features for UE-V 2.x</span></span>](deploy-required-features-for-ue-v-2x-new-uevv2.md)

 

 





