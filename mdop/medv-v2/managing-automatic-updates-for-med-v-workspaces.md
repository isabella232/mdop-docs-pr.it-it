---
title: Gestione degli aggiornamenti automatici per le aree di lavoro MED-V
description: Gestione degli aggiornamenti automatici per le aree di lavoro MED-V
author: dansimp
ms.assetid: 306f28a2-d653-480d-b737-4b8b3132de5d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: b22d3250db806e740c1d62da4fed98d5956b0eeb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825295"
---
# <span data-ttu-id="b9aeb-103">Gestione degli aggiornamenti automatici per le aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b9aeb-103">Managing Automatic Updates for MED-V Workspaces</span></span>


<span data-ttu-id="b9aeb-104">L'area di lavoro MED-V è una macchina virtuale che contiene un sistema operativo distinto, il cui processo di aggiornamento automatico del software deve essere gestito proprio come i computer fisici dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-104">The MED-V workspace is a virtual machine that contains a separate operating system, whose automatic software update process must be managed just like the physical computers in your enterprise.</span></span> <span data-ttu-id="b9aeb-105">Poiché il sistema operativo guest non è sempre necessariamente in uso quando il sistema operativo ospitante è in funzione, è necessario assicurarsi che la macchina virtuale MED-V sia configurata in modo che gli aggiornamenti software possano essere applicati al sistema operativo guest in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-105">Because the guest operating system is not always necessarily running when the host operating system is running, you must ensure that the MED-V virtual machine is configured in such a way that software updates can be applied to the guest operating system as required.</span></span> <span data-ttu-id="b9aeb-106">La soluzione Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 offre la funzionalità che consente di determinare il modo in cui vengono elaborati gli aggiornamenti software automatici in un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-106">The Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 solution provides the functionality that lets you determine how automatic software updates are processed in a MED-V workspace.</span></span>

## <span data-ttu-id="b9aeb-107">Gestione dei criteri di riattivazione dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b9aeb-107">Managing MED-V Workspace Wake-Up Policy</span></span>


<span data-ttu-id="b9aeb-108">Il criterio di riattivazione dell'area di lavoro MED-V garantisce che la macchina virtuale MED-V sia resa disponibile per gli aggiornamenti per l'ora specificata nelle impostazioni di configurazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-108">The MED-V workspace wake-up policy guarantees that the MED-V virtual machine is made available for updates for the time that you specify in your MED-V configuration settings.</span></span> <span data-ttu-id="b9aeb-109">Questo vale per entrambi gli aggiornamenti pubblicati da Microsoft tramite Windows Update e gli aggiornamenti distribuiti e controllati da soluzioni non Microsoft, come le applicazioni antivirus.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-109">This applies to both updates that are published from Microsoft through Windows Update and updates deployed and controlled by non-Microsoft solutions, such as antivirus applications.</span></span>

<span data-ttu-id="b9aeb-110">**Importante**  I criteri di riattivazione dell'area di lavoro MED-V sono ottimizzati per l'infrastruttura Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-110">**Important** The MED-V workspace wake-up policy is optimized for the Microsoft Update infrastructure.</span></span> <span data-ttu-id="b9aeb-111">Se si usa Microsoft System Center Configuration Manager per distribuire gli aggiornamenti non Microsoft, è consigliabile usare anche System Center Updates Publisher, che sfrutta la stessa infrastruttura di Microsoft Update e quindi beneficia dei criteri di riattivazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-111">If you are using Microsoft System Center Configuration Manager to deploy non-Microsoft updates, we recommend that you also use the System Center Updates Publisher, which takes advantage of the same infrastructure as Microsoft Update and therefore benefits from the MED-V workspace wake-up policy.</span></span> <span data-ttu-id="b9aeb-112">Per altre informazioni, vedere [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) ( https://go.microsoft.com/fwlink/?LinkId=200035) .</span><span class="sxs-lookup"><span data-stu-id="b9aeb-112">For more information, see [System Center Updates Publisher](https://go.microsoft.com/fwlink/?LinkId=200035) (https://go.microsoft.com/fwlink/?LinkId=200035).</span></span>

 

<span data-ttu-id="b9aeb-113">Quando è stato creato il pacchetto dell'area di lavoro MED-V, è stato configurato quando e come viene avviato, quando l'utente finale accede (**avvio veloce**) o quando l'utente finale apre per la prima volta un'applicazione pubblicata (**inizio normale**).</span><span class="sxs-lookup"><span data-stu-id="b9aeb-113">When you created your MED-V workspace package, you configured when and how it starts, either when the end user logs on (**Fast Start**) or when the end user first opens a published application (**Normal Start**).</span></span> <span data-ttu-id="b9aeb-114">Oppure imposta l'opzione per consentire all'utente finale di controllare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-114">Or you set the option to let the end user control this setting.</span></span>

<span data-ttu-id="b9aeb-115">In entrambi i casi, ogni volta che viene selezionata l'opzione **avvio veloce** , la macchina virtuale continua a essere eseguita purché l'host MED-V sia connesso come utente.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-115">Either way, whenever the **Fast Start** option is selected, the virtual machine continues to run as long as the MED-V host is logged on as User.</span></span> <span data-ttu-id="b9aeb-116">In questa configurazione, poiché MED-V è attivo quando l'host è attivo, gli aggiornamenti automatici vengono applicati senza richiedere ulteriori elaborazioni da MED-V.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-116">In this configuration, because MED-V is active when the host is active, automatic updates are applied without requiring any extra processing from MED-V.</span></span>

<span data-ttu-id="b9aeb-117">Tuttavia, per i casi in cui l' **avvio veloce** non viene specificato o la macchina virtuale viene sospesa o arrestata, Med-v garantisce attraverso i criteri di riattivazione dell'area di lavoro MED-v che il sistema operativo guest viene aggiornato regolarmente anche quando MED-V non viene usato regolarmente.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-117">However, for those cases in which **Fast Start** is not specified or the virtual machine hibernates or stops, MED-V guarantees through its MED-V workspace wake-up policy that the guest operating system is being regularly updated even when MED-V is not used regularly.</span></span> <span data-ttu-id="b9aeb-118">MED-V esegue questa funzione regolarmente riattivando la macchina virtuale in base alle impostazioni di configurazione specificate.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-118">MED-V performs this function by regularly waking up the virtual machine based on the configuration settings that you specify.</span></span> <span data-ttu-id="b9aeb-119">In questo modo i client di aggiornamento automatico della macchina virtuale verranno eseguiti in base alle loro configurazioni.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-119">This enables the automatic update clients in the virtual machine to execute based on their configurations.</span></span><span data-ttu-id="b9aeb-120">Una volta trascorso il periodo di tempo definito dall'impostazione di configurazione di MED-V, MED-V restituirà la macchina virtuale allo stato precedente.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-120">After the time period defined by the MED-V configuration setting elapses, MED-V returns the virtual machine to its previous state.</span></span>

<span data-ttu-id="b9aeb-121">**Nota**  Se l'utente finale apre un'applicazione pubblicata durante il periodo di aggiornamento, gli aggiornamenti richiesti vengono applicati, ma MED-V non viene automaticamente ibernato o arrestato al termine del periodo di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-121">**Note** If the end user opens a published application during the update period, the required updates are applied, but MED-V is not automatically hibernated or shut down after the update period ends.</span></span> <span data-ttu-id="b9aeb-122">Invece, MED-V continua a essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-122">Instead, MED-V continues running.</span></span>

 

<span data-ttu-id="b9aeb-123">I criteri di riattivazione dell'area di lavoro MED-V includono tre componenti principali:</span><span class="sxs-lookup"><span data-stu-id="b9aeb-123">The MED-V workspace wake-up policy includes three main components:</span></span>

**<span data-ttu-id="b9aeb-124">Guest Update Manager</span><span class="sxs-lookup"><span data-stu-id="b9aeb-124">Guest Update Manager</span></span>**

<span data-ttu-id="b9aeb-125">Questo programma eseguibile autonomo che risiede nell'host MED-V è responsabile del risveglio della macchina virtuale in base a una pianificazione predefinita configurabile.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-125">Residing on the MED-V host, this stand-alone executable program is responsible for waking up the virtual machine according to a predefined, configurable schedule.</span></span> <span data-ttu-id="b9aeb-126">Specificare le impostazioni di configurazione per indicare a che ora la macchina virtuale deve essere riattivata ogni giorno dall'Update Manager e per quanto tempo la macchina virtuale deve essere mantenuta (in minuti) per consentire l'applicazione degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-126">Specify the configuration settings to indicate at what time the update manager should wake up the virtual machine every day, and how long the virtual machine should be kept awake (in minutes) to allow for updates to be applied.</span></span> <span data-ttu-id="b9aeb-127">Dopo che è stato raggiunto il numero di minuti specificati, la gestione aggiornamento Guest inserisce la macchina virtuale in ibernazione, preparata per l'uso successivo.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-127">After the number of minutes specified has been reached, the guest update manager puts the virtual machine into hibernation, prepared for the next use.</span></span> <span data-ttu-id="b9aeb-128">Puoi programmare l'esecuzione di questo programma eseguibile tramite Windows Task Manager.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-128">You can schedule the execution of this executable program through the Windows Task Manager.</span></span>

**<span data-ttu-id="b9aeb-129">Servizio di gestione riavvio Guest</span><span class="sxs-lookup"><span data-stu-id="b9aeb-129">Guest Restart Management Service</span></span>**

<span data-ttu-id="b9aeb-130">Questo servizio, che risiede nell'host MED-V, ha tre responsabilità principali.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-130">Residing on the MED-V host, this service has three primary responsibilities.</span></span> <span data-ttu-id="b9aeb-131">Insieme a Guest Update Manager, gestisce il riavvio della macchina virtuale all'accesso dell'utente, se necessario.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-131">Along with the Guest Update Manager, it manages the restart of the virtual machine at user logon, if it is required.</span></span> <span data-ttu-id="b9aeb-132">Viene rilevato quando i riavvii della macchina virtuale sono necessari causati dagli aggiornamenti installati.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-132">It detects when virtual machine restarts are required caused by updates being installed.</span></span> <span data-ttu-id="b9aeb-133">E assicura che l'attività di gestione aggiornamento Guest sia sempre pianificata in base alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-133">And it ensures that the task for the Guest Update Manager is always scheduled according to configuration.</span></span>

**<span data-ttu-id="b9aeb-134">Servizio di aggiornamento Guest</span><span class="sxs-lookup"><span data-stu-id="b9aeb-134">Guest Update Service</span></span>**

<span data-ttu-id="b9aeb-135">Questo servizio Windows, che risiede nella macchina virtuale MED-V, è responsabile del monitoraggio quando gli aggiornamenti installati richiedono un riavvio.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-135">Residing on the MED-V virtual machine, this Windows service has the responsibility of monitoring when installed updates require a restart.</span></span> <span data-ttu-id="b9aeb-136">Dopo che il servizio viene a conoscenza della necessità di un riavvio, informa il servizio di gestione riavvio guest nell'host.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-136">After the service becomes aware of the need for a restart, it notifies the guest restart management service on the host.</span></span>

### <span data-ttu-id="b9aeb-137">Impostazioni di configurazione per i criteri di riattivazione dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b9aeb-137">Configuration Settings for MED-V Workspace Wake-Up Policy</span></span>

<span data-ttu-id="b9aeb-138">Puoi controllare quando e per quanto tempo la macchina virtuale si risveglia per ricevere gli aggiornamenti automatici definendo i due valori di configurazione seguenti nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-138">You control when and for how long the virtual machine awakens to receive automatic updates by defining the following two configuration values in the registry.</span></span> <span data-ttu-id="b9aeb-139">Entrambi questi valori si trovano sotto la chiave HKLM\\Software\\Microsoft\\MEDV\\v2\\VM.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-139">Both of these values are located under the HKLM\\Software\\Microsoft\\MEDV\\v2\\VM key.</span></span>

<span data-ttu-id="b9aeb-140">**GuestUpdateTime** -configura l'ora e il minuto ogni giorno quando MED-V deve riattivare la macchina virtuale per l'aggiornamento, in base allo standard di 24 ore.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-140">**GuestUpdateTime** – Configures the hour and minute each day when MED-V must wake up the virtual machine for updating, based on the 24-hour clock standard.</span></span> <span data-ttu-id="b9aeb-141">Specificare l'ora nel formato HH: MM.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-141">Specify the time in the format HH:MM.</span></span> <span data-ttu-id="b9aeb-142">Il valore predefinito è 00:00 (mezzanotte).</span><span class="sxs-lookup"><span data-stu-id="b9aeb-142">The default value is 00:00 (midnight).</span></span>

<span data-ttu-id="b9aeb-143">**GuestUpdateDuration** -configura il numero di minuti in cui MED-V deve conservare la macchina virtuale per l'aggiornamento, a partire dall'ora specificata nell'impostazione di configurazione di GuestUpdateTime.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-143">**GuestUpdateDuration** – Configures the number of minutes that MED-V must keep the virtual machine awake for updating, starting at the time specified in the GuestUpdateTime configuration setting.</span></span> <span data-ttu-id="b9aeb-144">Il valore predefinito è 240 (4 ore).</span><span class="sxs-lookup"><span data-stu-id="b9aeb-144">The default value is 240 (4 hours).</span></span> <span data-ttu-id="b9aeb-145">Impostando questo valore su zero (0) viene disabilitato il criterio di riattivazione dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-145">Setting this value to zero (0) disables the MED-V workspace wake-up policy.</span></span>

<span data-ttu-id="b9aeb-146">Per altre informazioni su come definire i valori di configurazione di MED-V, vedere [gestione delle impostazioni di configurazione dell'area di lavoro MED-v](managing-med-v-workspace-configuration-settings.md).</span><span class="sxs-lookup"><span data-stu-id="b9aeb-146">For more information about how to define your MED-V configuration values, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).</span></span>

<span data-ttu-id="b9aeb-147">**Nota**  Una procedura consigliata per MED-V consiste nell'impostare l'intervallo di riattivazione in modo che corrisponda al momento in cui le macchine virtuali MED-V sono pianificate per l'aggiornamento periodico.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-147">**Note** A MED-V best practice is to set your wake up interval to match the time when MED-V virtual machines are planned to be updated regularly.</span></span> <span data-ttu-id="b9aeb-148">Inoltre, ti consigliamo di configurare queste impostazioni per assomigliare al comportamento del computer host.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-148">In addition, we recommend that you configure these settings to resemble the host computer’s behavior.</span></span>

 

### <span data-ttu-id="b9aeb-149">Riavviare la notifica tramite il sistema ESD</span><span class="sxs-lookup"><span data-stu-id="b9aeb-149">Reboot Notification Using your ESD System</span></span>

<span data-ttu-id="b9aeb-150">Puoi configurare il sistema ESD per notificare a MED-V ogni volta che è necessario un riavvio per l'area di lavoro MED-V dopo l'applicazione degli aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-150">You can configure your ESD system to notify MED-V whenever a restart is required for the MED-V workspace after automatic updates have been applied.</span></span> <span data-ttu-id="b9aeb-151">Quando si applicano aggiornamenti automatici tramite il sistema ESD che si sa che richiedono un riavvio, è necessario scrivere uno script per segnalare l'evento globale seguente nell'area di lavoro MED-V:</span><span class="sxs-lookup"><span data-stu-id="b9aeb-151">When you apply automatic updates through your ESD system that you know require a restart, you should write a script to signal the following global event on the MED-V workspace:</span></span>

<span data-ttu-id="b9aeb-152">**Importante**  Per aprire l'evento è necessario modificare solo i diritti e quindi segnalarlo.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-152">**Important** You must open the event with Modify Only rights and then signal it.</span></span> <span data-ttu-id="b9aeb-153">Se non si apre con le autorizzazioni corrette, non funziona.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-153">If you do not open it with the correct permissions, it does not work.</span></span>

 

``` syntax
/// <summary>
/// The guest is required to be restarted due to an ESD update.
/// </summary>
public const string MedvGuestRebootRequiredEventName = @"Global\MedvGuestRebootRequiredEvent";
using (EventWaitHandle notificationEvent = 
EventWaitHandle.OpenExisting(eventName, EventWaitHandleRights.Modify))
{
notificationEvent.Set();
}
```

<span data-ttu-id="b9aeb-154">Quando segnali questo evento, MED-V la acquisisce e informa la macchina virtuale che è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="b9aeb-154">When you signal this event, MED-V captures it and informs the virtual machine that a restart is required.</span></span>

## <span data-ttu-id="b9aeb-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9aeb-155">Related topics</span></span>


[<span data-ttu-id="b9aeb-156">Gestione degli aggiornamenti software per le aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="b9aeb-156">Managing Software Updates for MED-V Workspaces</span></span>](managing-software-updates-for-med-v-workspaces.md)

 

 





