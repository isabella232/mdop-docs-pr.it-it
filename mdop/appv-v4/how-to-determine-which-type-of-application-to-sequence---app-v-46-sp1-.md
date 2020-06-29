---
title: Come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)
description: Come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817486"
---
# <span data-ttu-id="9a646-103">Come determinare il tipo di applicazione da sequenziare (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="9a646-103">How to Determine Which Type of Application to Sequence (App-V 4.6 SP1)</span></span>


<span data-ttu-id="9a646-104">Puoi sequenziare tre tipi di applicazioni di base usando Microsoft Application Virtualization (App-V) Sequencer.</span><span class="sxs-lookup"><span data-stu-id="9a646-104">You can sequence three basic types of applications by using Microsoft Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="9a646-105">Per determinare il tipo di applicazione da sequenziare</span><span class="sxs-lookup"><span data-stu-id="9a646-105">To determine which type of application to sequence</span></span>


<span data-ttu-id="9a646-106">Usare la tabella seguente per determinare il tipo di applicazione che deve essere sequenziato e per ottenere altre informazioni su come sequenziare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9a646-106">Use the following table to determine which type of application you should sequence and to obtain more information about how to sequence the application.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a646-107">Tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="9a646-107">Application Type</span></span></th>
<th align="left"><span data-ttu-id="9a646-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a646-108">Description</span></span></th>
<th align="left"><span data-ttu-id="9a646-109">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="9a646-109">More Information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a646-110">Standard</span><span class="sxs-lookup"><span data-stu-id="9a646-110">Standard</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a646-111">Selezionare questa opzione per creare un pacchetto che contiene un'applicazione o una famiglia di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="9a646-111">Select this option to create a package that contains an application or a suite of applications.</span></span> <span data-ttu-id="9a646-112">È necessario selezionare questa opzione per la maggior parte delle applicazioni che si prevede di sequenziare.</span><span class="sxs-lookup"><span data-stu-id="9a646-112">You should select this option for most applications that you plan to sequence.</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)"><span data-ttu-id="9a646-113">Come sequenziare una nuova applicazione standard (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="9a646-113">How to Sequence a New Standard Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a646-114">Componente aggiuntivo o plug-in</span><span class="sxs-lookup"><span data-stu-id="9a646-114">Add-on or Plug-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a646-115">Selezionare questa opzione per creare un pacchetto che estende la funzionalità di un'applicazione standard, ad esempio un plug-in per Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9a646-115">Select this option to create a package that extends the functionality of a standard application, for example, a plug-in for Microsoft Excel.</span></span> <span data-ttu-id="9a646-116">È inoltre possibile usare i plug-in per le applicazioni installate nativamente o un altro pacchetto collegato tramite la composizione Dynamic Suite.</span><span class="sxs-lookup"><span data-stu-id="9a646-116">Additionally, you can use plug-ins for natively installed applications, or another package that is linked by using Dynamic Suite Composition.</span></span> <span data-ttu-id="9a646-117">Per altre informazioni sulla composizione della famiglia di prodotti dinamici, Vedi <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> come usare la composizione della famiglia dinamica </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</span><span class="sxs-lookup"><span data-stu-id="9a646-117">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)"><span data-ttu-id="9a646-118">Come sequenziare un nuovo componente aggiuntivo o applicazione plug-in (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="9a646-118">How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a646-119">Middleware</span><span class="sxs-lookup"><span data-stu-id="9a646-119">Middleware</span></span></p></td>
<td align="left"><p><span data-ttu-id="9a646-120">Selezionare questa opzione per creare un pacchetto richiesto da un'applicazione standard, ad esempio Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9a646-120">Select this option to create a package that is required by a standard application, for example, the Microsoft .NET Framework.</span></span> <span data-ttu-id="9a646-121">I pacchetti middleware vengono usati per il collegamento ad altri pacchetti tramite la composizione di suite dinamiche.</span><span class="sxs-lookup"><span data-stu-id="9a646-121">Middleware packages are used for linking to other packages by using Dynamic Suite Composition.</span></span> <span data-ttu-id="9a646-122">Per altre informazioni sulla composizione della famiglia di prodotti dinamici, Vedi <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> come usare la composizione della famiglia dinamica </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</span><span class="sxs-lookup"><span data-stu-id="9a646-122">For more information about Dynamic Suite Composition, see <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)">How To Use Dynamic Suite Composition</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804">https://go.microsoft.com/fwlink/?LinkId=203804</a>).</span></span></p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)"><span data-ttu-id="9a646-123">Come sequenziare una nuova applicazione middleware (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="9a646-123">How to Sequence a New Middleware Application (App-V 4.6 SP1)</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9a646-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9a646-124">Related topics</span></span>


[<span data-ttu-id="9a646-125">Attività per Application Virtualization Sequencer (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="9a646-125">Tasks for the Application Virtualization Sequencer (App-V 4.6 SP1)</span></span>](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





