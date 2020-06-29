---
title: Migrazione dei pacchetti di impostazioni UE-V
description: Migrazione dei pacchetti di impostazioni UE-V
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823206"
---
# <span data-ttu-id="79029-103">Migrazione dei pacchetti di impostazioni UE-V</span><span class="sxs-lookup"><span data-stu-id="79029-103">Migrating UE-V Settings Packages</span></span>


<span data-ttu-id="79029-104">Nel ciclo di vita di una distribuzione di Microsoft User Experience Virtualization (UE-V), potrebbe essere necessario rilocare i pacchetti delle impostazioni utente quando si esegue la migrazione a un nuovo server o per scopi di backup.</span><span class="sxs-lookup"><span data-stu-id="79029-104">In the lifecycle of a Microsoft User Experience Virtualization (UE-V) deployment, you might need to relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span> <span data-ttu-id="79029-105">La migrazione dei pacchetti di impostazioni potrebbe essere necessaria negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="79029-105">Migration of settings packages might be needed in the following scenarios:</span></span>

-   <span data-ttu-id="79029-106">Aggiornamento dell'hardware del server esistente a un server più moderno.</span><span class="sxs-lookup"><span data-stu-id="79029-106">Upgrade of existing server hardware to a more modern server.</span></span>

-   <span data-ttu-id="79029-107">Migrazione di una condivisione della posizione di archiviazione delle impostazioni da un Lab a un server di produzione.</span><span class="sxs-lookup"><span data-stu-id="79029-107">Migration of a settings storage location share from a lab to a production server.</span></span>

<span data-ttu-id="79029-108">La semplice copia di file e cartelle non consentirà di mantenere le impostazioni e le autorizzazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="79029-108">Simply copying the files and folders will not preserve the security settings and permissions.</span></span> <span data-ttu-id="79029-109">La procedura descritta di seguito consente di copiare correttamente i file del pacchetto di impostazioni con le autorizzazioni NTFS per una nuova condivisione.</span><span class="sxs-lookup"><span data-stu-id="79029-109">The following described steps will properly copy the settings package files with their NTFS permissions to a new share.</span></span>

**<span data-ttu-id="79029-110">Come conservare i pacchetti di impostazioni UE-V quando si esegue la migrazione a un nuovo server</span><span class="sxs-lookup"><span data-stu-id="79029-110">How to preserve UE-V settings packages when migrating to a new server</span></span>**

1.  <span data-ttu-id="79029-111">In una nuova posizione in un server diverso creare una nuova cartella; ad esempio, impostazioni.</span><span class="sxs-lookup"><span data-stu-id="79029-111">In a new location on a different server, create a new folder; for example, MySettings.</span></span>

2.  <span data-ttu-id="79029-112">Disabilitare la condivisione per la condivisione della cartella precedente nel server precedente.</span><span class="sxs-lookup"><span data-stu-id="79029-112">Disable sharing for the old folder share on the old server.</span></span>

3.  <span data-ttu-id="79029-113">Trasferire i pacchetti di impostazioni esistenti nel nuovo server con Robocopy dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="79029-113">Move the existing settings packages to the new server with Robocopy from the command line.</span></span> <span data-ttu-id="79029-114">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="79029-114">For example:</span></span>

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    <span data-ttu-id="79029-115">**Nota**  Per monitorare lo stato di avanzamento della copia, aprire MySettings.txt con un lettore di file di log, ad esempio Trace32.</span><span class="sxs-lookup"><span data-stu-id="79029-115">**Note** To monitor the copy progress, open MySettings.txt with a log file reader such as Trace32.</span></span>

     

4.  <span data-ttu-id="79029-116">Concedere le autorizzazioni a livello di condivisione alla nuova condivisione.</span><span class="sxs-lookup"><span data-stu-id="79029-116">Grant share-level permissions to the new share.</span></span> <span data-ttu-id="79029-117">Abbandonare le autorizzazioni NTFS Man mano che erano impostate da Robocopy.</span><span class="sxs-lookup"><span data-stu-id="79029-117">Leave the NTFS permissions as they were set by Robocopy.</span></span>

    <span data-ttu-id="79029-118">Nei computer che eseguono l'agente UE-V aggiornare l'impostazione di configurazione SettingsStoragePath al percorso UNC della nuova condivisione.</span><span class="sxs-lookup"><span data-stu-id="79029-118">On computers that run the UE-V agent, update the SettingsStoragePath configuration setting to the UNC path of the new share.</span></span>

## <span data-ttu-id="79029-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79029-119">Related topics</span></span>


[<span data-ttu-id="79029-120">Amministrazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="79029-120">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="79029-121">Operazioni per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="79029-121">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





