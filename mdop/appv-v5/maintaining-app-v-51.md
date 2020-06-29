---
title: Manutenzione di App-V 5.1
description: Manutenzione di App-V 5.1
author: dansimp
ms.assetid: 5abd17d3-e8af-4261-b914-741ae116b0e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 431ad65507a5699358159c73eaf9f3cf0dee33b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805109"
---
# <span data-ttu-id="757c2-103">Manutenzione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="757c2-103">Maintaining App-V 5.1</span></span>


<span data-ttu-id="757c2-104">Dopo aver completato tutte le pianificazioni necessarie e quindi la distribuzione di App-V 5,1, è possibile usare le informazioni seguenti per gestire l'infrastruttura di App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="757c2-104">After you have completed all the necessary planning, and then deployment of App-V 5.1, you can use the following information to maintain the App-V 5.1 infrastructure.</span></span>

## <a href="" id="move-the-app-v-5-1-server-"></a><span data-ttu-id="757c2-105">Trasferire il server App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="757c2-105">Move the App-V 5.1 Server</span></span>


<span data-ttu-id="757c2-106">Il server App-V 5,1 si connette al database App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="757c2-106">The App-V 5.1 server connects to the App-V 5.1 database.</span></span> <span data-ttu-id="757c2-107">È quindi possibile installare il componente di gestione in qualsiasi computer della rete e quindi connetterlo al database App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="757c2-107">Therefore you can install the management component to any computer on the network and then connect it to the App-V 5.1 database.</span></span>

[<span data-ttu-id="757c2-108">Come spostare il server App-V in un altro computer</span><span class="sxs-lookup"><span data-stu-id="757c2-108">How to Move the App-V Server to Another Computer</span></span>](how-to-move-the-app-v-server-to-another-computer51.md)

## <a href="" id="determine-if-an-app-v-5-1-application-is-running-virtualized-"></a><span data-ttu-id="757c2-109">Determinare se un'applicazione App-V 5,1 è in uso virtualizzata</span><span class="sxs-lookup"><span data-stu-id="757c2-109">Determine if an App-V 5.1 Application is Running Virtualized</span></span>


<span data-ttu-id="757c2-110">I fornitori di software indipendenti che desiderano determinare se un'applicazione è in uso virtualizzato con App-V 5,1 o superiore, dovrebbero aprire un oggetto denominato denominato \*\*AppVVirtual- &lt; PID &gt; \*\* nello spazio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="757c2-110">Independent software vendors (ISV) who want to determine if an application is running virtualized with App-V 5.1 or above, should open a named object called **AppVVirtual-&lt;PID&gt;** in the default namespace.</span></span> <span data-ttu-id="757c2-111">Ad esempio, l'API di Windows **GetCurrentProcessId ()** può essere usata per ottenere l'ID del processo corrente, ad esempio 4052, e quindi se un oggetto evento denominato denominato **AppVVirtual-4052** può essere aperto correttamente usando **OpenEvent ()** nello spazio dei nomi predefinito per l'accesso in lettura, l'applicazione è virtuale.</span><span class="sxs-lookup"><span data-stu-id="757c2-111">For example, Windows API **GetCurrentProcessId()** can be used to obtain the current process's ID, for example 4052, and then if a named Event object called **AppVVirtual-4052** can be successfully opened using **OpenEvent()** in the default namespace for read access, then the application is virtual.</span></span> <span data-ttu-id="757c2-112">Se la chiamata a **OpenEvent ()** non riesce, l'applicazione non è virtuale.</span><span class="sxs-lookup"><span data-stu-id="757c2-112">If the **OpenEvent()** call fails, the application is not virtual.</span></span>

<span data-ttu-id="757c2-113">Inoltre, gli ISV che vogliono virtualizzare in modo esplicito o meno le chiamate su API specifiche con App-V 5,1 e versioni successive, possono usare le funzioni **VirtualizeCurrentThread ()** e **CurrentThreadIsVirtualized ()** implementate nel modulo AppEntSubsystems32.dll.</span><span class="sxs-lookup"><span data-stu-id="757c2-113">Additionally, ISV’s who want to explicitly virtualize or not virtualize calls on specific API’s with App-V 5.1 and above, can use the **VirtualizeCurrentThread()** and **CurrentThreadIsVirtualized()** functions implemented in the AppEntSubsystems32.dll module.</span></span> <span data-ttu-id="757c2-114">Questi consentono di accennare a un componente downstream che la chiamata deve o non deve essere virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="757c2-114">These provide a way of hinting at a downstream component that the call should or should not be virtualized.</span></span>






## <span data-ttu-id="757c2-115">Altre risorse per la gestione dell'App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="757c2-115">Other resources for maintaining App-V 5.1</span></span>


[<span data-ttu-id="757c2-116">Operazioni per App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="757c2-116">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





