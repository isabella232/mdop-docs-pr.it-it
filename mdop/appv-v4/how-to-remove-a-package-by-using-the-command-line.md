---
title: Come rimuovere un pacchetto con la riga di comando
description: Come rimuovere un pacchetto con la riga di comando
author: dansimp
ms.assetid: 47697ec7-20e5-4258-8865-a0a710d41d5a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b282830802f34bfb0670ddfdb8e2852d3559e3f7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816825"
---
# <span data-ttu-id="d8de8-103">Come rimuovere un pacchetto con la riga di comando</span><span class="sxs-lookup"><span data-stu-id="d8de8-103">How to Remove a Package by Using the Command Line</span></span>


<span data-ttu-id="d8de8-104">È possibile usare le procedure della riga di comando seguenti per eliminare un pacchetto di applicazione virtuale dal client Application Virtualization (App-V) in un computer specifico.</span><span class="sxs-lookup"><span data-stu-id="d8de8-104">You can use the following command-line procedures to delete a virtual application package from the Application Virtualization (App-V) Client on a specific computer.</span></span>

**<span data-ttu-id="d8de8-105">Per eliminare un pacchetto di applicazione virtuale per tutti gli utenti</span><span class="sxs-lookup"><span data-stu-id="d8de8-105">To delete a virtual application package for all users</span></span>**

-   <span data-ttu-id="d8de8-106">Se il pacchetto è stato aggiunto in precedenza per tutti gli utenti usando l'opzione/GLOBAL, usare il comando seguente per eliminare il pacchetto e i tipi di file e i tasti di scelta rapida globali.</span><span class="sxs-lookup"><span data-stu-id="d8de8-106">If the package was previously added for all users by using the /GLOBAL switch, use the following command to delete the package and the global file types and shortcuts.</span></span> <span data-ttu-id="d8de8-107">Sono necessari i diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="d8de8-107">Administrator rights are required.</span></span> <span data-ttu-id="d8de8-108">L'opzione/GLOBAL non è necessaria in questo caso perché il comando esegue sempre un'eliminazione globale del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d8de8-108">The /GLOBAL switch is not needed in this case because the command always performs a global deletion of the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

**<span data-ttu-id="d8de8-109">Per eliminare un pacchetto aggiunto in precedenza per singoli utenti</span><span class="sxs-lookup"><span data-stu-id="d8de8-109">To delete a package previously added for individual users</span></span>**

1.  <span data-ttu-id="d8de8-110">Se il pacchetto è stato aggiunto in precedenza per singoli utenti, sono disponibili diverse opzioni.</span><span class="sxs-lookup"><span data-stu-id="d8de8-110">If the package was previously added for individual users, you have several options.</span></span>

    <span data-ttu-id="d8de8-111">Eseguire il comando seguente una volta sotto l'account utente di ogni persona a cui è stato pubblicato il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d8de8-111">Run the following command once under the user account of each person the package was published to.</span></span> <span data-ttu-id="d8de8-112">In questo caso l'accesso dell'utente alle applicazioni viene negato se si spostano in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="d8de8-112">This denies the user access to the applications if they roam to another computer.</span></span> <span data-ttu-id="d8de8-113">Elimina le impostazioni, i collegamenti e i tipi di file specifici dell'utente dal profilo e arresta i carichi in background nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d8de8-113">It deletes the specific user’s settings, shortcuts, and file types from the profile, and it stops background loads under the user’s context.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

2.  <span data-ttu-id="d8de8-114">In alternativa, eseguire il comando seguente sotto l'account utente di ogni persona a cui è stato pubblicato il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d8de8-114">Alternatively, run the following command under the user account of each person the package was published to.</span></span>

    `SFTMIME UNPUBLISH PACKAGE:”name”`

    <span data-ttu-id="d8de8-115">Esegui quindi questo comando per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="d8de8-115">Then run this command for the package.</span></span>

    `SFTMIME DELETE PACKAGE:”name”`

    <span data-ttu-id="d8de8-116">Questo rimuove completamente il pacchetto e Elimina tutte le impostazioni utente, i tasti di scelta rapida e i tipi di file dai relativi profili.</span><span class="sxs-lookup"><span data-stu-id="d8de8-116">This completely removes the package, and it deletes all user settings, shortcuts, and file types from their profiles.</span></span> <span data-ttu-id="d8de8-117">Se il pacchetto viene successivamente aggiunto nuovamente, gli utenti dovranno specificare di nuovo le relative impostazioni.</span><span class="sxs-lookup"><span data-stu-id="d8de8-117">If the package is subsequently re-added, the users will have to specify their settings again.</span></span> <span data-ttu-id="d8de8-118">Per eseguire questo comando è necessaria solo l'autorizzazione "Elimina applicazioni" (**Deleteapp**).</span><span class="sxs-lookup"><span data-stu-id="d8de8-118">Only “Delete applications” (**DeleteApp**) permission is needed to run this command.</span></span>

3.  <span data-ttu-id="d8de8-119">Come terza alternativa, è possibile eseguire semplicemente il comando **Elimina pacchetto** senza usare il comando Annulla **pubblicazione pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="d8de8-119">As a third alternative, you can simply run the **DELETE PACKAGE** command without using the **UNPUBLISH PACKAGE** command.</span></span> <span data-ttu-id="d8de8-120">In questo caso, i tipi di file e i tasti di scelta rapida per ogni utente sono nascosti anziché eliminati e le impostazioni utente vengono mantenute.</span><span class="sxs-lookup"><span data-stu-id="d8de8-120">In this case, file types and shortcuts for each user are hidden rather than deleted, and the user settings are retained.</span></span> <span data-ttu-id="d8de8-121">Questo significa che se il pacchetto viene successivamente aggiunto di nuovo per l'utente, i tipi di file e i collegamenti vengono ripristinati e le impostazioni utente vengono riapplicate.</span><span class="sxs-lookup"><span data-stu-id="d8de8-121">This means that if the package is subsequently re-added for the user, the file types and shortcuts are restored, and the user settings are reapplied.</span></span>

## <span data-ttu-id="d8de8-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8de8-122">Related topics</span></span>


[<span data-ttu-id="d8de8-123">Come aggiungere un pacchetto con la riga di comando</span><span class="sxs-lookup"><span data-stu-id="d8de8-123">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="d8de8-124">Come eliminare tutte le applicazioni virtuali usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="d8de8-124">How to Delete All Virtual Applications by Using the Command Line</span></span>](how-to-delete-all-virtual-applications-by-using-the-command-line.md)

 

 





