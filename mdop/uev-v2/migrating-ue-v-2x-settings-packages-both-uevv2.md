---
title: Migrazione dei pacchetti di impostazioni UE-V 2. x
description: Migrazione dei pacchetti di impostazioni UE-V 2. x
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825516"
---
# <span data-ttu-id="732c4-103">Migrazione dei pacchetti di impostazioni UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="732c4-103">Migrating UE-V 2.x Settings Packages</span></span>


<span data-ttu-id="732c4-104">Nel ciclo di vita di una distribuzione di Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1, potrebbe essere necessario rilocare i pacchetti delle impostazioni utente quando si esegue la migrazione a un nuovo server o quando si eseguono i backup.</span><span class="sxs-lookup"><span data-stu-id="732c4-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 deployment, you might have to relocate the user settings packages either when you migrate to a new server or when you perform backups.</span></span> <span data-ttu-id="732c4-105">Potrebbe essere necessario eseguire la migrazione dei pacchetti di impostazioni negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="732c4-105">Settings packages might have to be migrated in the following scenarios:</span></span>

-   <span data-ttu-id="732c4-106">Aggiornamento dell'hardware del server esistente a un server più moderno.</span><span class="sxs-lookup"><span data-stu-id="732c4-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="732c4-107">Migrazione di una condivisione della posizione di archiviazione delle impostazioni da un server di prova a un server di produzione.</span><span class="sxs-lookup"><span data-stu-id="732c4-107">Migration of a settings storage location share from a test server to a production server.</span></span>

<span data-ttu-id="732c4-108">La semplice copia di file e cartelle non consente di mantenere le impostazioni e le autorizzazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="732c4-108">Simply copying the files and folders does not preserve the security settings and permissions.</span></span> <span data-ttu-id="732c4-109">La procedura seguente descrive come copiare correttamente il pacchetto di impostazioni insieme alle autorizzazioni di file system NTFS per una nuova condivisione.</span><span class="sxs-lookup"><span data-stu-id="732c4-109">The following steps describe how to correctly copy the settings package along with their NTFS file system permissions to a new share.</span></span>

**<span data-ttu-id="732c4-110">Per conservare i pacchetti di impostazioni di UE-V 2 quando si esegue la migrazione a un nuovo server</span><span class="sxs-lookup"><span data-stu-id="732c4-110">To preserve UE-V 2 settings packages when you migrate to a new server</span></span>**

1.  <span data-ttu-id="732c4-111">In una nuova posizione in un server diverso creare una nuova cartella, ad esempio impostazioni.</span><span class="sxs-lookup"><span data-stu-id="732c4-111">In a new location on a different server, create a new folder, for example, MySettings.</span></span>

2.  <span data-ttu-id="732c4-112">Disabilitare la condivisione per la condivisione della cartella precedente nel server precedente.</span><span class="sxs-lookup"><span data-stu-id="732c4-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="732c4-113">Per copiare i pacchetti di impostazioni esistenti nel nuovo server con Robocopy</span><span class="sxs-lookup"><span data-stu-id="732c4-113">To copy the existing settings packages to the new server with Robocopy</span></span>

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="732c4-114">**Nota**  Per monitorare lo stato di avanzamento della copia, aprire MySettings.txt con un visualizzatore log, ad esempio Trace32.</span><span class="sxs-lookup"><span data-stu-id="732c4-114">**Note** To monitor the copy progress, open MySettings.txt with a log viewer such as Trace32.</span></span>

     

4.  <span data-ttu-id="732c4-115">Concedere le autorizzazioni a livello di condivisione alla nuova condivisione.</span><span class="sxs-lookup"><span data-stu-id="732c4-115">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="732c4-116">Abbandonare le autorizzazioni di file system NTFS Man mano che erano impostate da Robocopy.</span><span class="sxs-lookup"><span data-stu-id="732c4-116">Leave the NTFS file system permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="732c4-117">Nei computer che eseguono l'agente UE-V aggiornare l'impostazione di configurazione **SettingsStoragePath** al percorso UNC (Universal Naming Convention) della nuova condivisione.</span><span class="sxs-lookup"><span data-stu-id="732c4-117">On computers that run the UE-V Agent, update the **SettingsStoragePath** configuration setting to the Universal Naming Convention (UNC) path of the new share.</span></span>

    <span data-ttu-id="732c4-118">**Hai un suggerimento per l'UE-V**?</span><span class="sxs-lookup"><span data-stu-id="732c4-118">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="732c4-119">Aggiungere o votare i suggerimenti [qui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="732c4-119">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="732c4-120">**È stato ottenuto un problema UE-V**?</span><span class="sxs-lookup"><span data-stu-id="732c4-120">**Got a UE-V issue**?</span></span> <span data-ttu-id="732c4-121">Utilizzare il [forum TechNet di UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="732c4-121">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="732c4-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="732c4-122">Related topics</span></span>


[<span data-ttu-id="732c4-123">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="732c4-123">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

 

 





