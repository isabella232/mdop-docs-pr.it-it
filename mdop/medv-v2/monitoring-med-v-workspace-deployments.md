---
title: Monitoraggio delle distribuzioni nell'area di lavoro MED-V
description: Monitoraggio delle distribuzioni nell'area di lavoro MED-V
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827215"
---
# <span data-ttu-id="63194-103">Monitoraggio delle distribuzioni nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="63194-103">Monitoring MED-V Workspace Deployments</span></span>


<span data-ttu-id="63194-104">La funzionalità di monitoraggio in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 consente di eseguire query su singole aree di lavoro MED-V per determinare se la configurazione per la prima volta è riuscita in tutta l'organizzazione dopo la distribuzione delle aree di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="63194-104">The monitoring feature in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 lets you run queries on individual MED-V workspaces to determine whether first time setup succeeded throughout your enterprise after the MED-V workspaces are deployed.</span></span> <span data-ttu-id="63194-105">Il monitoraggio dell'esito positivo della configurazione iniziale è importante perché MED-V non è in uno stato utilizzabile finché la configurazione iniziale non è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="63194-105">Monitoring the success of first time setup is important because MED-V is not in a usable state until first time setup has been completed successfully.</span></span>

<span data-ttu-id="63194-106">Questa sezione fornisce informazioni e istruzioni per aiutarti a monitorare l'esito positivo o negativo della configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="63194-106">This section provides information and instruction to assist you in monitoring the success or failure of first time setup.</span></span>

## <span data-ttu-id="63194-107">Per monitorare le distribuzioni dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="63194-107">To monitor MED-V workspace deployments</span></span>


<span data-ttu-id="63194-108">La funzionalità di monitoraggio è costituita da un provider di Strumentazione gestione Windows (WMI) in-process che è possibile eseguire una query usando la lingua di query WMI per individuare lo stato della configurazione iniziale per tutti gli utenti finali in un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="63194-108">The monitoring feature consists of a coupled in-process Windows Management Instrumentation (WMI) provider that you can query using WMI Query Language to discover the status of first time setup for all end users on a MED-V workspace.</span></span>

<span data-ttu-id="63194-109">Il provider WMI viene implementato tramite il Framework di estensione del provider WMI da Microsoft .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="63194-109">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span> <span data-ttu-id="63194-110">Il provider WMI viene eseguito nel contesto di LocalService e archivia la prima volta lo stato di installazione in modo sicuro in \\ProgramData.</span><span class="sxs-lookup"><span data-stu-id="63194-110">The WMI provider executes in the context of LocalService and stores the first time setup state securely under \\ProgramData.</span></span>

<span data-ttu-id="63194-111">Il provider WMI viene implementato nello spazio dei nomi **root\\microsoft\\medv** e implementa la classe **FTS \ _Status**, che espone il metodo **SetFtsState**.</span><span class="sxs-lookup"><span data-stu-id="63194-111">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **FTS\_Status**, which exposes the method **SetFtsState**.</span></span> <span data-ttu-id="63194-112">MED-V usa **SetFtsState** per impostare lo stato di configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="63194-112">MED-V uses **SetFtsState** to set the first time setup state.</span></span>

<span data-ttu-id="63194-113">La classe contiene le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="63194-113">The class contains the following properties.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="63194-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="63194-114">Property</span></span></th>
<th align="left"><span data-ttu-id="63194-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63194-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63194-116">Computer</span><span class="sxs-lookup"><span data-stu-id="63194-116">Machine</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="63194-117">Proprietà di sola lettura </strong> che contiene il nome della macchina virtuale Guest a cui è stato eseguito il provisioning per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="63194-117">Read Only</strong> property that contains the name of the guest virtual machine provisioned by first time setup.</span></span> <span data-ttu-id="63194-118">Questa chiave contiene il nome che l'ospite avrebbe avuto in caso di errore di configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="63194-118">This key contains the name that the guest would have had on first time setup failure.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63194-119">StatusCode</span><span class="sxs-lookup"><span data-stu-id="63194-119">StatusCode</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="63194-120"></strong>Proprietà di sola lettura che contiene zero se la configurazione per la prima volta è riuscita.</span><span class="sxs-lookup"><span data-stu-id="63194-120">Read Only</strong> property that contains zero if first time setup succeeded.</span></span> <span data-ttu-id="63194-121">Qualsiasi altro valore restituito è uguale all'ID evento dell'errore registrato.</span><span class="sxs-lookup"><span data-stu-id="63194-121">Any other value returned equals the event ID for the error that is logged.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="63194-122">Tempo</span><span class="sxs-lookup"><span data-stu-id="63194-122">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63194-123">Ora UTC che è stata completata la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="63194-123">The UTC time that first time setup completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="63194-124">Utente</span><span class="sxs-lookup"><span data-stu-id="63194-124">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="63194-125">L'utente per cui è stata eseguita la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="63194-125">The user for which first time setup was run.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="63194-126">Il codice seguente mostra il file MOF (Managed Object Format) che definisce la classe **FTS \ _Status** .</span><span class="sxs-lookup"><span data-stu-id="63194-126">The following code shows the Managed Object Format (MOF) file that defines the **FTS\_Status** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

<span data-ttu-id="63194-127">Poiché la preoccupazione principale è molto probabile che le aree di lavoro MED-V per cui la configurazione per la prima volta non è stata completata correttamente, è possibile scrivere la query in modo che restituiscano solo quelli non riusciti per la prima volta, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="63194-127">Because your main concern is most likely those MED-V workspaces for which first time setup was not completed successfully, you can write your query to only return those that failed first time setup, for example:</span></span>

``` syntax
Select * from FTS_Status where StatusCode != 0
```

<span data-ttu-id="63194-128">In questo caso, la caratteristica di monitoraggio restituisce un elenco delle aree di lavoro MED-V che non sono state eseguite per la prima volta, che è possibile usare per eseguire le azioni appropriate per risolvere l'errore.</span><span class="sxs-lookup"><span data-stu-id="63194-128">In this case, the monitoring feature returns a list of those MED-V workspaces that failed first time setup, which you can use to take the appropriate actions to resolve the failure.</span></span>

## <span data-ttu-id="63194-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63194-129">Related topics</span></span>


[<span data-ttu-id="63194-130">Monitorare le aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="63194-130">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="63194-131">Come verificare le impostazioni della prima configurazione</span><span class="sxs-lookup"><span data-stu-id="63194-131">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

 

 





