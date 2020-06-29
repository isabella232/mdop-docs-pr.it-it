---
title: Informazioni di riferimento sui comandi di SFTMIME
description: Informazioni di riferimento sui comandi di SFTMIME
author: dansimp
ms.assetid: a4a69228-9dd3-4623-b773-899d03c0cf10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 47aac9110febaf3f349461d74fef840326b1c6e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815346"
---
# <span data-ttu-id="77fb5-103">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="77fb5-103">SFTMIME Command Reference</span></span>


<span data-ttu-id="77fb5-104">SFTMIME è un'interfaccia della riga di comando usata da Application Virtualization (App-V) che consente di gestire molti dettagli della configurazione del client.</span><span class="sxs-lookup"><span data-stu-id="77fb5-104">SFTMIME is a command-line interface used by Application Virtualization (App-V) that enables you to manage many client configuration details.</span></span> <span data-ttu-id="77fb5-105">Questa sezione contiene tutti i comandi e i relativi parametri, con una breve descrizione di ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="77fb5-105">This section contains all the commands and their parameters, with a brief description of each.</span></span>

**<span data-ttu-id="77fb5-106">Importante</span><span class="sxs-lookup"><span data-stu-id="77fb5-106">Important</span></span>**  
-   <span data-ttu-id="77fb5-107">Tutti i caratteri barra rovesciata devono essere sottolineati con una barra rovesciata precedente oppure il percorso non verrà analizzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="77fb5-107">All backslash characters must be escaped using a preceding backslash, or the path will not be parsed correctly.</span></span>

-   <span data-ttu-id="77fb5-108">Se si usa un programma chiamante per richiamare SFTMIME con **CreateProcess**, è necessario assicurarsi che il primo parametro sia il percorso per sftmime.exe.</span><span class="sxs-lookup"><span data-stu-id="77fb5-108">If you are using a calling program to invoke SFTMIME with **CreateProcess**, you must ensure that the first parameter is the path to sftmime.exe.</span></span>

-   <span data-ttu-id="77fb5-109">L'output del comando SFTMIME **query obj** non può essere inviato tramite pipe al comando **findstr** per cercare una stringa.</span><span class="sxs-lookup"><span data-stu-id="77fb5-109">The output of the SFTMIME **QUERY OBJ** command cannot be piped to the **findstr** command to search for a string.</span></span>

-   <span data-ttu-id="77fb5-110">L'uso dell'opzione **globale** richiede i diritti di amministratore locale.</span><span class="sxs-lookup"><span data-stu-id="77fb5-110">Use of the **GLOBAL** switch requires local administrator rights.</span></span>

-   <span data-ttu-id="77fb5-111">L'uso di percorsi brevi e percorsi relativi può determinare risultati imprevisti e deve essere evitato.</span><span class="sxs-lookup"><span data-stu-id="77fb5-111">Use of short paths and relative paths can lead to unexpected results and should be avoided.</span></span> <span data-ttu-id="77fb5-112">Usa sempre percorsi completi.</span><span class="sxs-lookup"><span data-stu-id="77fb5-112">Always use full paths.</span></span>

 

## <span data-ttu-id="77fb5-113">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="77fb5-113">In This Section</span></span>


[<span data-ttu-id="77fb5-114">ADD APP</span><span class="sxs-lookup"><span data-stu-id="77fb5-114">ADD APP</span></span>](add-app.md)

[<span data-ttu-id="77fb5-115">ADD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="77fb5-115">ADD PACKAGE</span></span>](add-package.md)

[<span data-ttu-id="77fb5-116">ADD SERVER</span><span class="sxs-lookup"><span data-stu-id="77fb5-116">ADD SERVER</span></span>](add-server.md)

[<span data-ttu-id="77fb5-117">ADD TYPE</span><span class="sxs-lookup"><span data-stu-id="77fb5-117">ADD TYPE</span></span>](add-type.md)

[<span data-ttu-id="77fb5-118">CLEAR APP</span><span class="sxs-lookup"><span data-stu-id="77fb5-118">CLEAR APP</span></span>](clear-app.md)

[<span data-ttu-id="77fb5-119">CLEAR OBJ</span><span class="sxs-lookup"><span data-stu-id="77fb5-119">CLEAR OBJ</span></span>](clear-obj.md)

[<span data-ttu-id="77fb5-120">CONFIGURE APP</span><span class="sxs-lookup"><span data-stu-id="77fb5-120">CONFIGURE APP</span></span>](configure-app.md)

[<span data-ttu-id="77fb5-121">CONFIGURE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="77fb5-121">CONFIGURE PACKAGE</span></span>](configure-package.md)

[<span data-ttu-id="77fb5-122">CONFIGURE SERVER</span><span class="sxs-lookup"><span data-stu-id="77fb5-122">CONFIGURE SERVER</span></span>](configure-server.md)

[<span data-ttu-id="77fb5-123">CONFIGURE TYPE</span><span class="sxs-lookup"><span data-stu-id="77fb5-123">CONFIGURE TYPE</span></span>](configure-type.md)

[<span data-ttu-id="77fb5-124">DELETE APP</span><span class="sxs-lookup"><span data-stu-id="77fb5-124">DELETE APP</span></span>](delete-app.md)

[<span data-ttu-id="77fb5-125">DELETE OBJ</span><span class="sxs-lookup"><span data-stu-id="77fb5-125">DELETE OBJ</span></span>](delete-obj.md)

[<span data-ttu-id="77fb5-126">DELETE PACKAGE</span><span class="sxs-lookup"><span data-stu-id="77fb5-126">DELETE PACKAGE</span></span>](delete-package.md)

[<span data-ttu-id="77fb5-127">DELETE SERVER</span><span class="sxs-lookup"><span data-stu-id="77fb5-127">DELETE SERVER</span></span>](delete-server.md)

[<span data-ttu-id="77fb5-128">DELETE TYPE</span><span class="sxs-lookup"><span data-stu-id="77fb5-128">DELETE TYPE</span></span>](delete-type.md)

[<span data-ttu-id="77fb5-129">HELP</span><span class="sxs-lookup"><span data-stu-id="77fb5-129">HELP</span></span>](help.md)

[<span data-ttu-id="77fb5-130">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="77fb5-130">LOAD APP</span></span>](load-app.md)

[<span data-ttu-id="77fb5-131">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="77fb5-131">LOAD PACKAGE</span></span>](load-package.md)

[<span data-ttu-id="77fb5-132">LOCK APP</span><span class="sxs-lookup"><span data-stu-id="77fb5-132">LOCK APP</span></span>](lock-app.md)

[<span data-ttu-id="77fb5-133">PUBLISH APP</span><span class="sxs-lookup"><span data-stu-id="77fb5-133">PUBLISH APP</span></span>](publish-app.md)

[<span data-ttu-id="77fb5-134">PUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="77fb5-134">PUBLISH PACKAGE</span></span>](publish-package.md)

[<span data-ttu-id="77fb5-135">QUERY OBJ</span><span class="sxs-lookup"><span data-stu-id="77fb5-135">QUERY OBJ</span></span>](query-obj.md)

[<span data-ttu-id="77fb5-136">REFRESH SERVER</span><span class="sxs-lookup"><span data-stu-id="77fb5-136">REFRESH SERVER</span></span>](refresh-server.md)

[<span data-ttu-id="77fb5-137">REPAIR APP</span><span class="sxs-lookup"><span data-stu-id="77fb5-137">REPAIR APP</span></span>](repair-app.md)

[<span data-ttu-id="77fb5-138">UNLOAD APP</span><span class="sxs-lookup"><span data-stu-id="77fb5-138">UNLOAD APP</span></span>](unload-app.md)

[<span data-ttu-id="77fb5-139">UNLOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="77fb5-139">UNLOAD PACKAGE</span></span>](unload-package.md)

[<span data-ttu-id="77fb5-140">UNLOCK APP</span><span class="sxs-lookup"><span data-stu-id="77fb5-140">UNLOCK APP</span></span>](unlock-app.md)

[<span data-ttu-id="77fb5-141">UNPUBLISH PACKAGE</span><span class="sxs-lookup"><span data-stu-id="77fb5-141">UNPUBLISH PACKAGE</span></span>](unpublish-package.md)

 

 





