---
title: Modifica della frequenza delle attività pianificate di UE-V
description: Modifica della frequenza delle attività pianificate di UE-V
author: dansimp
ms.assetid: 33c2674e-0df4-4717-9c3d-820a90b16e19
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ced608608ffae82a29fb5ca84cfca281082b8127
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822686"
---
# <span data-ttu-id="cc186-103">Modifica della frequenza delle attività pianificate di UE-V</span><span class="sxs-lookup"><span data-stu-id="cc186-103">Changing the Frequency of UE-V Scheduled Tasks</span></span>


<span data-ttu-id="cc186-104">Il programma di installazione dell'agente Microsoft User Experience Virtualization (UE-V), AgentSetup.exe, crea due attività pianificate durante l'installazione di agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc186-104">The Microsoft User Experience Virtualization (UE-V) Agent installer, AgentSetup.exe, creates two scheduled tasks during the UE-V Agent installation.</span></span> <span data-ttu-id="cc186-105">Le due attività sono l'attività di **aggiornamento automatico del modello** e l'impostazione dell'attività di **stato della posizione di archiviazione** .</span><span class="sxs-lookup"><span data-stu-id="cc186-105">The two tasks are the **Template Auto Update** task and the **Setting Storage Location Status** task.</span></span> <span data-ttu-id="cc186-106">Queste attività pianificate non possono essere configurate con gli strumenti UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc186-106">These scheduled tasks are not configurable with the UE-V tools.</span></span> <span data-ttu-id="cc186-107">Gli amministratori che desiderano modificare l'attività pianificata per questi elementi possono creare uno script che usa le opzioni della riga di comando Schtasks.exe.</span><span class="sxs-lookup"><span data-stu-id="cc186-107">Administrators who wish to change the scheduled task for these items can create a script that uses the Schtasks.exe command-line options.</span></span>

<span data-ttu-id="cc186-108">Per altre informazioni su Schtasks.exe, vedere [come usare schtasks, exe per pianificare le attività in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span><span class="sxs-lookup"><span data-stu-id="cc186-108">For more information about Schtasks.exe, see [How to use Schtasks,exe to Schedule Tasks in Windows Server 2003](https://go.microsoft.com/fwlink/?LinkID=264854).</span></span>

## <span data-ttu-id="cc186-109">Aggiornamento automatico del modello</span><span class="sxs-lookup"><span data-stu-id="cc186-109">Template Auto-Update</span></span>


<span data-ttu-id="cc186-110">L'attività di **aggiornamento automatico del modello** controlla il catalogo di modelli di impostazioni per nuovi, aggiornati o rimossi.</span><span class="sxs-lookup"><span data-stu-id="cc186-110">The **Template Auto Update** task checks the settings template catalog for new, updated, or removed templates.</span></span> <span data-ttu-id="cc186-111">Questa attività viene eseguita solo se il SettingsTemplateCatalog è configurato.</span><span class="sxs-lookup"><span data-stu-id="cc186-111">This task only runs if the SettingsTemplateCatalog is configured.</span></span> <span data-ttu-id="cc186-112">L'attività di **aggiornamento automatico del modello** esegue il file ApplySettingsCatalog.exe, che si trova nella directory di installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="cc186-112">The **Template Auto Update** task runs the ApplySettingsCatalog.exe file, which is located in the UE-V Agent install directory.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="cc186-113">Nome attività</span><span class="sxs-lookup"><span data-stu-id="cc186-113">Task name</span></span></th>
<th align="left"><span data-ttu-id="cc186-114">Trigger predefinito</span><span class="sxs-lookup"><span data-stu-id="cc186-114">Default trigger</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="cc186-115">Aggiornamento automatico di \Microsoft\UE-V\Template</span><span class="sxs-lookup"><span data-stu-id="cc186-115">\Microsoft\UE-V\Template Auto Update</span></span></p></td>
<td align="left"><p><span data-ttu-id="cc186-116">3:30 AM ogni giorno</span><span class="sxs-lookup"><span data-stu-id="cc186-116">3:30 AM every day</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="cc186-117">**Esempio:** Il comando seguente consente di configurare l'agente per controllare l'archivio di catalogo dei modelli di impostazioni ogni ora.</span><span class="sxs-lookup"><span data-stu-id="cc186-117">**Example:** The following command configures the agent to check the settings template catalog store every hour.</span></span>

``` syntax
schtasks /change /tn "Microsoft\UE-V\Template Auto Update" /ri 60
```

## <span data-ttu-id="cc186-118">Stato della posizione di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="cc186-118">Settings Storage Location Status</span></span>


<span data-ttu-id="cc186-119">L'attività per l' **impostazione dello stato della posizione di archiviazione** esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc186-119">The **Setting Storage Location Status** task performs the following actions:</span></span>

1.  <span data-ttu-id="cc186-120">Verifica che le cartelle UE-V siano ancora bloccate o registrate con la caratteristica file offline.</span><span class="sxs-lookup"><span data-stu-id="cc186-120">Checks to make sure the UE-V folders are still pinned or registered with the offline files feature.</span></span>

2.  <span data-ttu-id="cc186-121">Verifica se la posizione di archiviazione delle impostazioni è offline o online.</span><span class="sxs-lookup"><span data-stu-id="cc186-121">Checks whether the settings storage location is offline or online.</span></span>

3.  <span data-ttu-id="cc186-122">Impone una sincronizzazione nell'intervallo specificato anziché l'intervallo predefinito per i file offline.</span><span class="sxs-lookup"><span data-stu-id="cc186-122">Forces a synchronization on the specified interval instead of the default interval for offline files.</span></span>

4.  <span data-ttu-id="cc186-123">Sincronizza tutti i pacchetti di impostazioni configurati per essere precaricati.</span><span class="sxs-lookup"><span data-stu-id="cc186-123">Synchronizes any settings packages that are configured to be pre-fetched.</span></span>

5.  <span data-ttu-id="cc186-124">Verifica se il percorso della directory Home di Active Directory è cambiato.</span><span class="sxs-lookup"><span data-stu-id="cc186-124">Checks if the Active Directory home directory path has changed.</span></span>

6.  <span data-ttu-id="cc186-125">Scrive la configurazione dello spazio di archiviazione delle impostazioni corrente nella posizione seguente</span><span class="sxs-lookup"><span data-stu-id="cc186-125">Writes the current settings storage configuration under the following location</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="cc186-126">Nome attività</span><span class="sxs-lookup"><span data-stu-id="cc186-126">Task name</span></span></th>
    <th align="left"><span data-ttu-id="cc186-127">Trigger predefinito</span><span class="sxs-lookup"><span data-stu-id="cc186-127">Default trigger</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="cc186-128">Stato della posizione di archiviazione di \Microsoft\UE-V\Settings</span><span class="sxs-lookup"><span data-stu-id="cc186-128">\Microsoft\UE-V\Settings Storage Location Status</span></span></p></td>
    <td align="left"><p><span data-ttu-id="cc186-129">All'accesso di qualsiasi utente, dopo l'attivazione, ripetere ogni 30 minuti a tempo indeterminato.</span><span class="sxs-lookup"><span data-stu-id="cc186-129">At logon of any user – After triggered, repeat every 30 minutes indefinitely.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

<span data-ttu-id="cc186-130">**Esempio:** Il comando seguente configura l'agente per eseguire l'azione sopra ogni ora.</span><span class="sxs-lookup"><span data-stu-id="cc186-130">**Example:** The following command configures the agent to run the action above every hour.</span></span>

``` syntax
schtasks /change /tn "\Microsoft\UE-V\Settings Storage Location Status" /ri 60
```

## <span data-ttu-id="cc186-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc186-131">Related topics</span></span>


[<span data-ttu-id="cc186-132">Amministrazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="cc186-132">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="cc186-133">Operazioni per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="cc186-133">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





