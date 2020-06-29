---
title: Distribuzione del percorso dell'archivio impostazioni per UE-v 1.0
description: Distribuzione del percorso dell'archivio impostazioni per UE-v 1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826636"
---
# <span data-ttu-id="a303d-103">Distribuzione del percorso dell'archivio impostazioni per UE-v 1.0</span><span class="sxs-lookup"><span data-stu-id="a303d-103">Deploying the Settings Storage Location for UE-V 1.0</span></span>


<span data-ttu-id="a303d-104">La distribuzione di Microsoft User Experience Virtualization (UE-V) richiede una posizione di archiviazione delle impostazioni in cui le impostazioni utente sono archiviate in un file di pacchetto di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a303d-104">Microsoft User Experience Virtualization (UE-V) deployment requires a settings storage location where the user settings are stored in a settings package file.</span></span> <span data-ttu-id="a303d-105">La posizione di archiviazione delle impostazioni può essere configurata in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="a303d-105">The settings storage location can be configured in one of the following two ways:</span></span>

-   <span data-ttu-id="a303d-106">**Directory Home di Active Directory** : se è definita una directory Home per l'utente in Active Directory, l'agente UE-V utilizzerà questa posizione per archiviare i pacchetti della posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a303d-106">**Active Directory home directory** – if a home directory is defined for the user in Active Directory, the UE-V agent will use this location to store settings location packages.</span></span> <span data-ttu-id="a303d-107">L'agente UE-V crea dinamicamente la cartella di archiviazione specifica dell'utente sotto la radice della Home Directory.</span><span class="sxs-lookup"><span data-stu-id="a303d-107">The UE-V agent dynamically creates the user-specific storage folder below the root of the home directory.</span></span> <span data-ttu-id="a303d-108">L'agente usa solo la home directory di Active Directory se una posizione di archiviazione delle impostazioni non è definita.</span><span class="sxs-lookup"><span data-stu-id="a303d-108">The agent only uses the home directory of the Active Directory if a settings storage location is not defined.</span></span>

-   <span data-ttu-id="a303d-109">**Creare una condivisione di archiviazione delle impostazioni** : la condivisione di archiviazione delle impostazioni è una condivisione di rete standard accessibile dagli utenti di UE-V.</span><span class="sxs-lookup"><span data-stu-id="a303d-109">**Create a settings storage share** – the settings storage share is a standard network share that is accessible by UE-V users.</span></span>

## <span data-ttu-id="a303d-110">Distribuire una condivisione di archiviazione delle impostazioni di UE-V</span><span class="sxs-lookup"><span data-stu-id="a303d-110">Deploy a UE-V settings storage share</span></span>


<span data-ttu-id="a303d-111">Quando si crea la condivisione di archiviazione delle impostazioni, è consigliabile limitare l'accesso solo agli utenti che hanno bisogno di Access.</span><span class="sxs-lookup"><span data-stu-id="a303d-111">When you create the settings storage share, you should limit access only to users that need access.</span></span> <span data-ttu-id="a303d-112">Le autorizzazioni necessarie sono visualizzate nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="a303d-112">The necessary permissions are shown in the tables below.</span></span>

**<span data-ttu-id="a303d-113">Per distribuire la condivisione di rete UE-V</span><span class="sxs-lookup"><span data-stu-id="a303d-113">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="a303d-114">Creare un nuovo gruppo di sicurezza per gli utenti di UE-V.</span><span class="sxs-lookup"><span data-stu-id="a303d-114">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="a303d-115">Creare una nuova cartella nel computer situato in posizione centrale in cui verranno archiviati i pacchetti di impostazioni di UE-V e quindi concedere agli utenti di UE-V le autorizzazioni di gruppo per la cartella.</span><span class="sxs-lookup"><span data-stu-id="a303d-115">Create a new folder on the centrally located computer that will store the UE-V settings packages, and then grant the UE-V users with group permissions to the folder.</span></span> <span data-ttu-id="a303d-116">L'amministratore che supporta la versione UE-V dovrà disporre delle autorizzazioni per questa cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="a303d-116">The administrator supporting UE-V will need permissions to this shared folder.</span></span>

3.  <span data-ttu-id="a303d-117">Impostare le seguenti autorizzazioni SMB (share-level) per la cartella della posizione di archiviazione dell'impostazione:</span><span class="sxs-lookup"><span data-stu-id="a303d-117">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="a303d-118">Account utente</span><span class="sxs-lookup"><span data-stu-id="a303d-118">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="a303d-119">Autorizzazioni consigliate</span><span class="sxs-lookup"><span data-stu-id="a303d-119">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a303d-120">Tutti</span><span class="sxs-lookup"><span data-stu-id="a303d-120">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a303d-121">Nessuna autorizzazione</span><span class="sxs-lookup"><span data-stu-id="a303d-121">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a303d-122">Gruppo di sicurezza degli utenti di UE-V</span><span class="sxs-lookup"><span data-stu-id="a303d-122">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a303d-123">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="a303d-123">Full Control</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="a303d-124">Impostare le autorizzazioni NTFS seguenti per la cartella della posizione di archiviazione delle impostazioni:</span><span class="sxs-lookup"><span data-stu-id="a303d-124">Set the following NTFS permissions for the settings storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="a303d-125">Account utente</span><span class="sxs-lookup"><span data-stu-id="a303d-125">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="a303d-126">Autorizzazioni consigliate</span><span class="sxs-lookup"><span data-stu-id="a303d-126">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="a303d-127">Cartella</span><span class="sxs-lookup"><span data-stu-id="a303d-127">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="a303d-128">Creatore/proprietario</span><span class="sxs-lookup"><span data-stu-id="a303d-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a303d-129">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="a303d-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a303d-130">Solo sottocartelle e file</span><span class="sxs-lookup"><span data-stu-id="a303d-130">Subfolders and Files Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="a303d-131">Gruppo di sicurezza degli utenti di UE-V</span><span class="sxs-lookup"><span data-stu-id="a303d-131">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a303d-132">Cartella di elenco/dati letti, creare cartelle/accodare dati</span><span class="sxs-lookup"><span data-stu-id="a303d-132">List Folder/Read Data, Create Folders/Append Data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="a303d-133">Solo questa cartella</span><span class="sxs-lookup"><span data-stu-id="a303d-133">This Folder Only</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

5.  <span data-ttu-id="a303d-134">Fare clic su **OK** per chiudere le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a303d-134">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="a303d-135">Questa configurazione delle autorizzazioni consente agli utenti di creare cartelle per l'archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a303d-135">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="a303d-136">L'agente UE-V crea e protegge una `settingspackage` cartella durante l'esecuzione nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a303d-136">The UE-V agent creates and secures a `settingspackage` folder while running in the context of the user.</span></span> <span data-ttu-id="a303d-137">L'utente riceve il controllo completo nella `settingspackage` cartella.</span><span class="sxs-lookup"><span data-stu-id="a303d-137">The user receives full control to their `settingspackage` folder.</span></span> <span data-ttu-id="a303d-138">Altri utenti non ereditano l'accesso alla cartella.</span><span class="sxs-lookup"><span data-stu-id="a303d-138">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="a303d-139">Non è necessario creare e proteggere singole directory utente, perché questa operazione verrà eseguita automaticamente dall'agente che viene eseguito nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a303d-139">You do not need to create and secure individual user directories, because this will be done automatically by the agent that runs in the context of the user.</span></span>

<span data-ttu-id="a303d-140">**Nota**  La sicurezza aggiuntiva può essere configurata quando viene usato un server Windows per la condivisione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a303d-140">**Note** Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="a303d-141">L'opzione UE-V può essere configurata per verificare che il gruppo di amministratori locali o l'utente corrente sia il proprietario della cartella in cui sono archiviati i pacchetti di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="a303d-141">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="a303d-142">Per abilitare la sicurezza aggiuntiva, completare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a303d-142">To enable additional security complete the following:</span></span>

1.  <span data-ttu-id="a303d-143">Aggiungere una chiave del registro di sistema **reg \ _DWORD** denominata "RepositoryOwnerCheckEnabled" a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**</span><span class="sxs-lookup"><span data-stu-id="a303d-143">Add a **REG\_DWORD** registry key named "RepositoryOwnerCheckEnabled" to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration.**</span></span>

2.  <span data-ttu-id="a303d-144">Impostare il valore della chiave del registro di sistema su 1.</span><span class="sxs-lookup"><span data-stu-id="a303d-144">Set registry key value to 1.</span></span>

 

## <span data-ttu-id="a303d-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a303d-145">Related topics</span></span>


[<span data-ttu-id="a303d-146">Distribuzione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="a303d-146">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="a303d-147">Configurazioni supportate per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="a303d-147">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

<span data-ttu-id="a303d-148">Distribuire lo spazio di archiviazione centrale per i modelli di impostazioni e le impostazioni di virtualizzazione dell'esperienza utente [installazione del generatore UE-V](installing-the-ue-v-generator.md)</span><span class="sxs-lookup"><span data-stu-id="a303d-148">Deploy the Central Storage for User Experience Virtualization Settings Templates and Settings Packages [Installing the UE-V Generator](installing-the-ue-v-generator.md)</span></span>

[<span data-ttu-id="a303d-149">Distribuzione dell'agente di UE-V</span><span class="sxs-lookup"><span data-stu-id="a303d-149">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

 

 





