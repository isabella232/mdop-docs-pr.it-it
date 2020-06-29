---
title: Come modificare il livello di registrazione del server e i parametri del database
description: Come modificare il livello di registrazione del server e i parametri del database
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818035"
---
# <span data-ttu-id="16c42-103">Come modificare il livello di registrazione del server e i parametri del database</span><span class="sxs-lookup"><span data-stu-id="16c42-103">How to Change the Server Logging Level and the Database Parameters</span></span>


<span data-ttu-id="16c42-104">È possibile usare le procedure seguenti per modificare il livello di registrazione e i parametri del log del database dalla console di gestione di Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="16c42-104">You can use the following procedures to change the logging level and the database log parameters from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="16c42-105">Sono disponibili i livelli di registrazione seguenti:</span><span class="sxs-lookup"><span data-stu-id="16c42-105">The following logging levels are available:</span></span>

-   <span data-ttu-id="16c42-106">Solo transazione</span><span class="sxs-lookup"><span data-stu-id="16c42-106">Transaction Only</span></span>

-   <span data-ttu-id="16c42-107">Errori irreversibili</span><span class="sxs-lookup"><span data-stu-id="16c42-107">Fatal Errors</span></span>

-   <span data-ttu-id="16c42-108">Errori</span><span class="sxs-lookup"><span data-stu-id="16c42-108">Errors</span></span>

-   <span data-ttu-id="16c42-109">Avvisi/errori</span><span class="sxs-lookup"><span data-stu-id="16c42-109">Warnings/Errors</span></span>

-   <span data-ttu-id="16c42-110">Info/avvisi/errori</span><span class="sxs-lookup"><span data-stu-id="16c42-110">Info/Warnings/Errors</span></span>

-   <span data-ttu-id="16c42-111">Dettagliata</span><span class="sxs-lookup"><span data-stu-id="16c42-111">Verbose</span></span>

<span data-ttu-id="16c42-112">**Nota**  A causa delle dimensioni del file di log prodotto quando si usa la modalità **verbose** , si consiglia di non eseguire server di produzione con questo livello di set di registrazione.</span><span class="sxs-lookup"><span data-stu-id="16c42-112">**Note** Because of the size of the log file produced when you use **Verbose** mode, the recommendation is that you do not run production servers with this level of logging set.</span></span>

 

<span data-ttu-id="16c42-113">I parametri di registrazione del database determinano il tipo di driver di database, le credenziali di accesso e la posizione del database di registrazione.</span><span class="sxs-lookup"><span data-stu-id="16c42-113">The database logging parameters determine the database driver type, access credentials, and location of the logging database.</span></span>

**<span data-ttu-id="16c42-114">Per modificare il livello di registrazione per i server di gestione</span><span class="sxs-lookup"><span data-stu-id="16c42-114">To change the logging level for Management Servers</span></span>**

1.  <span data-ttu-id="16c42-115">Fare clic sul nodo **gruppi di server** per visualizzare i gruppi di server.</span><span class="sxs-lookup"><span data-stu-id="16c42-115">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="16c42-116">Fare clic con il pulsante destro del mouse sul gruppo Server e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="16c42-116">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="16c42-117">Nella finestra di dialogo **Proprietà** selezionare la scheda **registrazione** .</span><span class="sxs-lookup"><span data-stu-id="16c42-117">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="16c42-118">Nella finestra di dialogo **Proprietà gruppo Server** selezionare il server e quindi fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="16c42-118">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="16c42-119">Nella finestra di dialogo **Aggiungi/modifica modulo log** selezionare il livello di registrazione nell'elenco a discesa **tipo di evento** .</span><span class="sxs-lookup"><span data-stu-id="16c42-119">In the **Add/Edit Log Module** dialog box, select the logging level from the **Event Type** drop-down list.</span></span>

6.  <span data-ttu-id="16c42-120">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="16c42-120">Click **OK**.</span></span>

7.  <span data-ttu-id="16c42-121">Nella finestra di dialogo **Proprietà gruppo Server** fare clic su **OK** o su **applica**.</span><span class="sxs-lookup"><span data-stu-id="16c42-121">In the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

**<span data-ttu-id="16c42-122">Per modificare il livello di registrazione per i server di flusso</span><span class="sxs-lookup"><span data-stu-id="16c42-122">To change the logging level for Streaming Servers</span></span>**

1.  <span data-ttu-id="16c42-123">Modificare il valore della chiave del registro di sistema seguente per modificare il livello di registrazione:</span><span class="sxs-lookup"><span data-stu-id="16c42-123">Edit the following registry key value to change the logging level:</span></span>

    -   <span data-ttu-id="16c42-124">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span><span class="sxs-lookup"><span data-stu-id="16c42-124">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel</span></span>

2.  <span data-ttu-id="16c42-125">Selezionare uno dei valori seguenti per impostare il livello di registrazione.</span><span class="sxs-lookup"><span data-stu-id="16c42-125">Select one of the following values to set the logging level.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="16c42-126">Value</span><span class="sxs-lookup"><span data-stu-id="16c42-126">Value</span></span></th>
    <th align="left"><span data-ttu-id="16c42-127">Livello di registrazione</span><span class="sxs-lookup"><span data-stu-id="16c42-127">Logging Level</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="16c42-128">0</span><span class="sxs-lookup"><span data-stu-id="16c42-128">0</span></span></p></td>
    <td align="left"><p><span data-ttu-id="16c42-129">Solo transazioni</span><span class="sxs-lookup"><span data-stu-id="16c42-129">Transactions Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="16c42-130">1</span><span class="sxs-lookup"><span data-stu-id="16c42-130">1</span></span></p></td>
    <td align="left"><p><span data-ttu-id="16c42-131">Errori irreversibili</span><span class="sxs-lookup"><span data-stu-id="16c42-131">Fatal Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="16c42-132">2</span><span class="sxs-lookup"><span data-stu-id="16c42-132">2</span></span></p></td>
    <td align="left"><p><span data-ttu-id="16c42-133">Errori</span><span class="sxs-lookup"><span data-stu-id="16c42-133">Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="16c42-134">3</span><span class="sxs-lookup"><span data-stu-id="16c42-134">3</span></span></p></td>
    <td align="left"><p><span data-ttu-id="16c42-135">Avvisi/errori</span><span class="sxs-lookup"><span data-stu-id="16c42-135">Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="16c42-136">4</span><span class="sxs-lookup"><span data-stu-id="16c42-136">4</span></span></p></td>
    <td align="left"><p><span data-ttu-id="16c42-137">Informazioni/avvisi/errori</span><span class="sxs-lookup"><span data-stu-id="16c42-137">Information/ Warnings/Errors</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="16c42-138">5</span><span class="sxs-lookup"><span data-stu-id="16c42-138">5</span></span></p></td>
    <td align="left"><p><span data-ttu-id="16c42-139">Dettagliata</span><span class="sxs-lookup"><span data-stu-id="16c42-139">Verbose</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="16c42-140">Per modificare i parametri del log del database</span><span class="sxs-lookup"><span data-stu-id="16c42-140">To change database log parameters</span></span>**

1.  <span data-ttu-id="16c42-141">Fare clic sul nodo **gruppi di server** per visualizzare i gruppi di server.</span><span class="sxs-lookup"><span data-stu-id="16c42-141">Click the **Server Groups** node to display the server groups.</span></span>

2.  <span data-ttu-id="16c42-142">Fare clic con il pulsante destro del mouse sul gruppo Server e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="16c42-142">Right-click the server group, and select **Properties**.</span></span>

3.  <span data-ttu-id="16c42-143">Nella finestra di dialogo **Proprietà** selezionare la scheda **registrazione** .</span><span class="sxs-lookup"><span data-stu-id="16c42-143">In the **Properties** dialog box, select the **Logging** tab.</span></span>

4.  <span data-ttu-id="16c42-144">Nella finestra di dialogo **Proprietà gruppo Server** selezionare il server e quindi fare clic su **modifica**.</span><span class="sxs-lookup"><span data-stu-id="16c42-144">In the **Server Group Properties** dialog box, select the server and then click **Edit**.</span></span>

5.  <span data-ttu-id="16c42-145">Nella finestra di dialogo **Aggiungi/modifica modulo log** selezionare un driver di database dall'elenco a discesa **driver del database** .</span><span class="sxs-lookup"><span data-stu-id="16c42-145">In the **Add/Edit Log Module** dialog box, select a database driver from the **Database Driver** drop-down list.</span></span>

6.  <span data-ttu-id="16c42-146">Immettere un **nome host DNS**.</span><span class="sxs-lookup"><span data-stu-id="16c42-146">Enter a **DNS Host Name**.</span></span>

7.  <span data-ttu-id="16c42-147">Fare clic sulla casella di controllo **determina dinamicamente la porta** o immettere un numero di porta nel campo della **porta** .</span><span class="sxs-lookup"><span data-stu-id="16c42-147">Click the **Dynamically Determine Port** check box, or enter a port number in the **Port** field.</span></span>

8.  <span data-ttu-id="16c42-148">Immettere il **nome** di un servizio nel campo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="16c42-148">Enter a **Service Name** in the corresponding field.</span></span>

9.  <span data-ttu-id="16c42-149">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="16c42-149">Click **OK**.</span></span>

10. <span data-ttu-id="16c42-150">Nella finestra di dialogo **Proprietà gruppo Server** fare clic su **OK** o su **applica**.</span><span class="sxs-lookup"><span data-stu-id="16c42-150">On the **Server Group Properties** dialog box, click **OK** or **Apply**.</span></span>

## <span data-ttu-id="16c42-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16c42-151">Related topics</span></span>


[<span data-ttu-id="16c42-152">Come personalizzare un sistema di Application Virtualization in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="16c42-152">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





