---
title: Come modificare le dimensioni della cache del server
description: Come modificare le dimensioni della cache del server
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818026"
---
# <span data-ttu-id="525f4-103">Come modificare le dimensioni della cache del server</span><span class="sxs-lookup"><span data-stu-id="525f4-103">How to Change the Server Cache Size</span></span>


<span data-ttu-id="525f4-104">È possibile usare la procedura seguente per modificare le dimensioni della cache per qualsiasi server direttamente dalla console di gestione di Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="525f4-104">You can use the following procedure to change the cache size for any server directly from the Application Virtualization Server Management Console.</span></span>

<span data-ttu-id="525f4-105">**Nota**  Anche se è possibile modificare le dimensioni della cache, a meno che la configurazione non richieda specificamente la modifica delle dimensioni, è consigliabile abbandonare la dimensione della cache impostata sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="525f4-105">**Note** Although you can change the cache size, unless your configuration specifically requires you to change the size, it is recommended that you leave the cache size set to the default values.</span></span>

 

**<span data-ttu-id="525f4-106">Per modificare le dimensioni della cache del server</span><span class="sxs-lookup"><span data-stu-id="525f4-106">To change the server cache size</span></span>**

1.  <span data-ttu-id="525f4-107">Fare clic sul nodo **gruppi di server** nel riquadro sinistro per espandere l'elenco di gruppi di server.</span><span class="sxs-lookup"><span data-stu-id="525f4-107">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="525f4-108">Nel riquadro **risultati** fare doppio clic sul gruppo di server desiderato per visualizzare l'elenco dei server nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="525f4-108">In the **Results** pane, double-click the desired server group to display the list of servers in the group.</span></span>

3.  <span data-ttu-id="525f4-109">Nel riquadro **risultati** fare clic con il pulsante destro del mouse sul server desiderato e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="525f4-109">In the **Results** pane, right-click the desired server and select **Properties**.</span></span>

4.  <span data-ttu-id="525f4-110">Selezionare la scheda **Avanzate** .</span><span class="sxs-lookup"><span data-stu-id="525f4-110">Select the **Advanced** tab.</span></span>

5.  <span data-ttu-id="525f4-111">Immettere un valore nel campo **massimo allocazione della memoria** per la cache del server e immettere un valore per il livello di avviso soglia nel campo **allocazione della memoria** di avviso.</span><span class="sxs-lookup"><span data-stu-id="525f4-111">Enter a value in the **Maximum Memory Allocation** field for the server cache, and enter a value for the threshold warning level in the **Warn Memory Allocation** field.</span></span>

6.  <span data-ttu-id="525f4-112">Immettere un valore nel campo **dimensione blocco massimo** .</span><span class="sxs-lookup"><span data-stu-id="525f4-112">Enter a value in the **Maximum Block Size** field.</span></span> <span data-ttu-id="525f4-113">Questo numero deve essere maggiore o uguale alla dimensione massima del blocco del pacchetto più grande che verrà trasmesso dal server.</span><span class="sxs-lookup"><span data-stu-id="525f4-113">This number must be greater than or equal to the maximum block size of the largest package that will be streamed from the server.</span></span>

7.  <span data-ttu-id="525f4-114">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="525f4-114">Click **OK**.</span></span>

## <span data-ttu-id="525f4-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="525f4-115">Related topics</span></span>


[<span data-ttu-id="525f4-116">Come modificare la porta del server</span><span class="sxs-lookup"><span data-stu-id="525f4-116">How to Change the Server Port</span></span>](how-to-change-the-server-port.md)

[<span data-ttu-id="525f4-117">Come gestire i server in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="525f4-117">How to Manage Servers in the Server Management Console</span></span>](how-to-manage-servers-in-the-server-management-console.md)

 

 





