---
title: Distribuzione del catalogo dei modelli di impostazioni per UE-v 1.0
description: Distribuzione del catalogo dei modelli di impostazioni per UE-v 1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826635"
---
# <span data-ttu-id="72cfa-103">Distribuzione del catalogo dei modelli di impostazioni per UE-v 1.0</span><span class="sxs-lookup"><span data-stu-id="72cfa-103">Deploying the Settings Template Catalog for UE-V 1.0</span></span>


<span data-ttu-id="72cfa-104">I modelli di posizione delle impostazioni personalizzate possono essere archiviati in un percorso di cartella nei computer Microsoft User Experience Virtualization (UE-V) o in una condivisione di rete SMB (Server Message Block).</span><span class="sxs-lookup"><span data-stu-id="72cfa-104">Custom settings location templates can be stored on a folder path on Microsoft User Experience Virtualization (UE-V) computers or on a Server Message Block (SMB) network share.</span></span> <span data-ttu-id="72cfa-105">Un'attività pianificata nel computer verifica la ricerca di modelli nuovi o aggiornati da questa posizione.</span><span class="sxs-lookup"><span data-stu-id="72cfa-105">A scheduled task on the computer checks for new or updated templates from this location.</span></span> <span data-ttu-id="72cfa-106">L'attività controlla questa posizione una volta al giorno e aggiorna il comportamento di sincronizzazione in base ai modelli presenti nella cartella.</span><span class="sxs-lookup"><span data-stu-id="72cfa-106">The task checks this location once each day and updates its synchronization behavior based on the templates in this folder.</span></span> <span data-ttu-id="72cfa-107">I modelli aggiunti o aggiornati in questa cartella dall'ultimo controllo vengono registrati dall'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="72cfa-107">Templates that are added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="72cfa-108">L'agente UE-V Annulla la registrazione dei modelli rimossi dalla cartella.</span><span class="sxs-lookup"><span data-stu-id="72cfa-108">The UE-V agent deregisters templates that were removed from this folder.</span></span> <span data-ttu-id="72cfa-109">L'attività pianificata viene eseguita come SYSTEM.</span><span class="sxs-lookup"><span data-stu-id="72cfa-109">The scheduled task runs as SYSTEM.</span></span> <span data-ttu-id="72cfa-110">La condivisione di rete deve almeno concedere le autorizzazioni per il gruppo Domain Computers.</span><span class="sxs-lookup"><span data-stu-id="72cfa-110">At a minimum, the network share must grant permissions for the Domain Computers group.</span></span> <span data-ttu-id="72cfa-111">Concedere inoltre le autorizzazioni di accesso per la cartella di condivisione di rete agli amministratori che gestiscono i modelli archiviati.</span><span class="sxs-lookup"><span data-stu-id="72cfa-111">In addition, grant access permissions for the network share folder to administrators who will manage the stored templates.</span></span> <span data-ttu-id="72cfa-112">Per altre informazioni sui modelli di posizione delle impostazioni personalizzate, vedere [pianificazione della distribuzione di modelli personalizzati per la versione UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="72cfa-112">For more information about custom setting location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

**<span data-ttu-id="72cfa-113">Per configurare il catalogo dei modelli di impostazioni per UE-V</span><span class="sxs-lookup"><span data-stu-id="72cfa-113">To configure the settings template catalog for UE-V</span></span>**

1.  <span data-ttu-id="72cfa-114">Creare una nuova cartella nel computer in cui verrà memorizzato il catalogo dei modelli di impostazioni UE-V.</span><span class="sxs-lookup"><span data-stu-id="72cfa-114">Create a new folder on the computer that will store the UE-V settings template catalog.</span></span>

2.  <span data-ttu-id="72cfa-115">Impostare le seguenti autorizzazioni SMB per la cartella del catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="72cfa-115">Set the following share-level (SMB) permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="72cfa-116">Account utente</span><span class="sxs-lookup"><span data-stu-id="72cfa-116">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="72cfa-117">Consigliare le autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="72cfa-117">Recommend permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="72cfa-118">Tutti</span><span class="sxs-lookup"><span data-stu-id="72cfa-118">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-119">Nessuna autorizzazione</span><span class="sxs-lookup"><span data-stu-id="72cfa-119">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="72cfa-120">Computer di dominio</span><span class="sxs-lookup"><span data-stu-id="72cfa-120">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-121">Livelli di autorizzazione di lettura</span><span class="sxs-lookup"><span data-stu-id="72cfa-121">Read Permission Levels</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="72cfa-122">Administrators</span><span class="sxs-lookup"><span data-stu-id="72cfa-122">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-123">Livelli di autorizzazione di lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="72cfa-123">Read/Write Permission Levels</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

3.  <span data-ttu-id="72cfa-124">Impostare le autorizzazioni NTFS seguenti per la cartella del catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="72cfa-124">Set the following NTFS permissions for the settings template catalog folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="72cfa-125">Account utente</span><span class="sxs-lookup"><span data-stu-id="72cfa-125">User Account</span></span></th>
    <th align="left"><span data-ttu-id="72cfa-126">Autorizzazioni consigliate</span><span class="sxs-lookup"><span data-stu-id="72cfa-126">Recommended Permissions</span></span></th>
    <th align="left"><span data-ttu-id="72cfa-127">Applica a</span><span class="sxs-lookup"><span data-stu-id="72cfa-127">Apply To</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="72cfa-128">Creatore/proprietario</span><span class="sxs-lookup"><span data-stu-id="72cfa-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-129">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="72cfa-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-130">Questa cartella, le sottocartelle e i file</span><span class="sxs-lookup"><span data-stu-id="72cfa-130">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="72cfa-131">Computer di dominio</span><span class="sxs-lookup"><span data-stu-id="72cfa-131">Domain Computers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-132">Contenuto della cartella di elenco e lettura</span><span class="sxs-lookup"><span data-stu-id="72cfa-132">List Folder Contents and Read</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-133">Questa cartella, le sottocartelle e i file</span><span class="sxs-lookup"><span data-stu-id="72cfa-133">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="72cfa-134">Tutti</span><span class="sxs-lookup"><span data-stu-id="72cfa-134">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-135">Nessuna autorizzazione</span><span class="sxs-lookup"><span data-stu-id="72cfa-135">No Permissions</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-136">Nessuna autorizzazione</span><span class="sxs-lookup"><span data-stu-id="72cfa-136">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="72cfa-137">Administrators</span><span class="sxs-lookup"><span data-stu-id="72cfa-137">Administrators</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-138">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="72cfa-138">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="72cfa-139">Questa cartella, le sottocartelle e i file</span><span class="sxs-lookup"><span data-stu-id="72cfa-139">This Folder, Subfolders and Files</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="72cfa-140">Fare clic su **OK** per chiudere le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="72cfa-140">Click **OK** to close the dialog boxes.</span></span>

## <span data-ttu-id="72cfa-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72cfa-141">Related topics</span></span>


[<span data-ttu-id="72cfa-142">Distribuzione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="72cfa-142">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="72cfa-143">Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="72cfa-143">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





