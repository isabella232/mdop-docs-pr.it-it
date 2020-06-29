---
title: Come configurare o disabilitare le dimensioni dei database
description: Come configurare o disabilitare le dimensioni dei database
author: dansimp
ms.assetid: 4abaf349-132d-4186-8873-a0e515593b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cbb041920e2680d51b01926f144eba595fe28d05
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816565"
---
# <span data-ttu-id="0b770-103">Come configurare o disabilitare le dimensioni dei database</span><span class="sxs-lookup"><span data-stu-id="0b770-103">How to Set Up or Disable Database Size</span></span>


<span data-ttu-id="0b770-104">È possibile usare le procedure seguenti nella console di gestione di Application Virtualization Server per specificare le dimensioni (in MB) dell'utilizzo del sistema di virtualizzazione delle applicazioni che si desidera archiviare nel database.</span><span class="sxs-lookup"><span data-stu-id="0b770-104">You can use the following procedures in the Application Virtualization Server Management Console to specify the size (in MB) of Application Virtualization System usage that you want to store in the database.</span></span>

<span data-ttu-id="0b770-105">Quando la dimensione dei dati archiviati raggiunge il 95% (la filigrana alta) del limite specificato, il sistema eliminerà il 10% dei dati di utilizzo, lasciando il 85% dei dati.</span><span class="sxs-lookup"><span data-stu-id="0b770-105">When the size of the stored data reaches 95% (the high watermark) of the specified limit, the system will delete 10% of the usage data, leaving 85% of the data.</span></span> <span data-ttu-id="0b770-106">I dati di utilizzo del pacchetto e dell'applicazione verranno eliminati.</span><span class="sxs-lookup"><span data-stu-id="0b770-106">Package and application usage data will be deleted.</span></span> <span data-ttu-id="0b770-107">Quando il database diventa abbastanza grande e si avvicina alla filigrana elevata, viene inviato un messaggio di avviso al log di SQL Server per comunicare che è stato raggiunto il limite.</span><span class="sxs-lookup"><span data-stu-id="0b770-107">When the database grows large enough and approaches the high watermark, a warning message is sent to the SQL Server log to inform you that this limit has been reached.</span></span> <span data-ttu-id="0b770-108">Questo avviso è necessario perché l'azione di pulitura può influire sull'output dei report.</span><span class="sxs-lookup"><span data-stu-id="0b770-108">This warning is necessary because the cleanup action can affect the output of the reports.</span></span> <span data-ttu-id="0b770-109">Consente inoltre di decidere se è necessario aumentare le dimensioni massime del database, ridurre il numero di mesi di dati di utilizzo da mantenere oppure abbassare il livello di registrazione.</span><span class="sxs-lookup"><span data-stu-id="0b770-109">It will also help you decide whether you need to increase the maximum database size, reduce the number of months of usage data to be kept, or turn down the logging level.</span></span>

<span data-ttu-id="0b770-110">**Nota**  Sono disponibili le opzioni **Nessun limite di dimensioni** e **Mantieni tutto l'utilizzo** per disabilitare la creazione di report di utilizzo e la pulizia del database.</span><span class="sxs-lookup"><span data-stu-id="0b770-110">**Note** The **No Size Limit** and **Keep All Usage** options are provided so that you can disable usage reporting and database cleanup.</span></span> <span data-ttu-id="0b770-111">La selezione di questi elementi consente di pulire anche il log delle transazioni del database.</span><span class="sxs-lookup"><span data-stu-id="0b770-111">Selecting these items will clean up the database transaction log as well.</span></span> <span data-ttu-id="0b770-112">Tutte le transazioni di Microsoft SQL Server salvate verranno rimosse dal log del database.</span><span class="sxs-lookup"><span data-stu-id="0b770-112">(All committed Microsoft SQL Server transactions will be removed from the database log.)</span></span>

 

**<span data-ttu-id="0b770-113">Per impostare le dimensioni del database</span><span class="sxs-lookup"><span data-stu-id="0b770-113">To set up database size</span></span>**

1.  <span data-ttu-id="0b770-114">Fare clic con il pulsante destro del mouse sul nodo Application Virtualization System nel riquadro sinistro e scegliere **Opzioni di sistema**.</span><span class="sxs-lookup"><span data-stu-id="0b770-114">Right-click the Application Virtualization System node in the left pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="0b770-115">Selezionare la scheda **database** .</span><span class="sxs-lookup"><span data-stu-id="0b770-115">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="0b770-116">Selezionare il pulsante di opzione **dimensione massima del database (MB)** o **Nessun limite di dimensione** .</span><span class="sxs-lookup"><span data-stu-id="0b770-116">Select the **Maximum Database Size (MB)** or **No Size Limit** radio button.</span></span>

4.  <span data-ttu-id="0b770-117">Se si sceglie di specificare le dimensioni di un database, è consigliabile immettere un numero compreso tra 512 e 4096 MB.</span><span class="sxs-lookup"><span data-stu-id="0b770-117">If you choose to specify a database size, best practices recommend that you enter a number between 512 and 4096 MB.</span></span> <span data-ttu-id="0b770-118">La dimensione predefinita è 1024 MB e se è necessario aumentare le dimensioni del database, il valore massimo che è possibile immettere è 2.147.483.647.</span><span class="sxs-lookup"><span data-stu-id="0b770-118">The default size is 1024 MB and if you need to increase the database size, the maximum value you can enter is 2,147,483,647.</span></span> <span data-ttu-id="0b770-119">Se si seleziona **Nessun limite di dimensione**, il database si svilupperà fino a raggiungere il limite di dimensioni del disco.</span><span class="sxs-lookup"><span data-stu-id="0b770-119">If you select **No Size Limit**, the database will grow until it reaches the disk size limit.</span></span>

5.  <span data-ttu-id="0b770-120">Fare clic su **applica** o **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b770-120">Click **Apply** or **OK**.</span></span>

**<span data-ttu-id="0b770-121">Per disabilitare i limiti delle dimensioni del database</span><span class="sxs-lookup"><span data-stu-id="0b770-121">To disable database size limits</span></span>**

1.  <span data-ttu-id="0b770-122">Fare clic con il pulsante destro del mouse sul nodo Application Virtualization System nel riquadro **ambito** e scegliere **Opzioni di sistema**.</span><span class="sxs-lookup"><span data-stu-id="0b770-122">Right-click the Application Virtualization System node in the **Scope** pane, and select **System Options**.</span></span>

2.  <span data-ttu-id="0b770-123">Selezionare la scheda **database** .</span><span class="sxs-lookup"><span data-stu-id="0b770-123">Select the **Database** tab.</span></span>

3.  <span data-ttu-id="0b770-124">Selezionare il **limite nessuna dimensione** e **Mantieni tutti i** pulsanti di opzione utilizzo.</span><span class="sxs-lookup"><span data-stu-id="0b770-124">Select the **No Size Limit** and **Keep All Usage** radio buttons.</span></span>

4.  <span data-ttu-id="0b770-125">Fare clic su **applica** o **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b770-125">Click **Apply** or **OK**.</span></span>

## <span data-ttu-id="0b770-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0b770-126">Related topics</span></span>


[<span data-ttu-id="0b770-127">Come personalizzare un sistema di Application Virtualization in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="0b770-127">How to Customize an Application Virtualization System in the Server Management Console</span></span>](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[<span data-ttu-id="0b770-128">Come configurare o disabilitare la creazione di report di utilizzo</span><span class="sxs-lookup"><span data-stu-id="0b770-128">How to Set Up or Disable Usage Reporting</span></span>](how-to-set-up-or-disable-usage-reporting.md)

 

 





