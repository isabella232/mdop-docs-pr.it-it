---
title: Come eliminare tutte le applicazioni virtuali usando la riga di comando
description: Come eliminare tutte le applicazioni virtuali usando la riga di comando
author: dansimp
ms.assetid: bfe13b5c-825a-4eb1-a979-6c4b8d8b2a9c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 55c809df31fa5c19f2f1a56c143d492b092156c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817536"
---
# <span data-ttu-id="3edfe-103">Come eliminare tutte le applicazioni virtuali usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="3edfe-103">How to Delete All Virtual Applications by Using the Command Line</span></span>


<span data-ttu-id="3edfe-104">Per eliminare tutte le applicazioni virtuali da un computer specifico, è possibile usare la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="3edfe-104">You can use the following procedure to delete all virtual applications from a specific computer.</span></span>

<span data-ttu-id="3edfe-105">**Nota**  Quando tutte le applicazioni vengono eliminate da un pacchetto, il client di Application Virtualization (App-V) Elimina anche il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3edfe-105">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

 

**<span data-ttu-id="3edfe-106">Per eliminare tutte le applicazioni</span><span class="sxs-lookup"><span data-stu-id="3edfe-106">To delete all applications</span></span>**

-   <span data-ttu-id="3edfe-107">Eseguire il comando seguente per eliminare tutte le applicazioni per l'account utente in cui viene eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="3edfe-107">Run the following command to delete all applications for the user account under which the command is run.</span></span> <span data-ttu-id="3edfe-108">Se si esegue il comando con l'opzione/GLOBAL facoltativa, usando un account con diritti amministrativi, tutte le applicazioni vengono eliminate per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="3edfe-108">If you run the command with the optional /GLOBAL switch, using an account with administrative rights, all applications are deleted for all users.</span></span>

    `SFTMIME DELETE OBJ:APP [/GLOBAL]`

    <span data-ttu-id="3edfe-109">**Nota**  Quando tutte le applicazioni vengono eliminate da un pacchetto, il client di Application Virtualization (App-V) Elimina anche il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="3edfe-109">**Note** When all applications are deleted from a package, the Application Virtualization (App-V) Client also deletes the package.</span></span>

     

## <span data-ttu-id="3edfe-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3edfe-110">Related topics</span></span>


[<span data-ttu-id="3edfe-111">Come aggiungere un pacchetto con la riga di comando</span><span class="sxs-lookup"><span data-stu-id="3edfe-111">How to Add a Package by Using the Command Line</span></span>](how-to-add-a-package-by-using-the-command-line.md)

[<span data-ttu-id="3edfe-112">Come rimuovere un pacchetto con la riga di comando</span><span class="sxs-lookup"><span data-stu-id="3edfe-112">How to Remove a Package by Using the Command Line</span></span>](how-to-remove-a-package-by-using-the-command-line.md)

 

 





