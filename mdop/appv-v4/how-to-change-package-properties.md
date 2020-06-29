---
title: Come modificare le proprietà del pacchetto
description: Come modificare le proprietà del pacchetto
author: dansimp
ms.assetid: 6050916a-d4fe-4dac-8f2a-47308dbbf481
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d2427a2651f3941f967c171ae7854facc62b4aa9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818045"
---
# <span data-ttu-id="5c00f-103">Come modificare le proprietà del pacchetto</span><span class="sxs-lookup"><span data-stu-id="5c00f-103">How to Change Package Properties</span></span>


<span data-ttu-id="5c00f-104">È possibile usare le procedure seguenti per modificare il nome di un pacchetto di virtualizzazione dell'applicazione e i commenti associati.</span><span class="sxs-lookup"><span data-stu-id="5c00f-104">You can use the following procedures to modify an Application Virtualization package name and its associated comments.</span></span>

<span data-ttu-id="5c00f-105">Se è la prima volta che il pacchetto è stato creato, è anche possibile modificare la dimensione del blocco dei parametri di sequenziazione, che determina la modalità di trasmissione di un pacchetto di applicazione sequenziata da un Application Virtualization Server a un client Desktop Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5c00f-105">If this is the first time the package has been created, you can also change the sequencing parameter block size, which determines how a sequenced application package is streamed from an Application Virtualization Server to an Application Virtualization Desktop Client.</span></span>

<span data-ttu-id="5c00f-106">**Nota**  Quando si seleziona una dimensione di blocco, prendere in considerazione le dimensioni del file SFT e la larghezza di banda della rete.</span><span class="sxs-lookup"><span data-stu-id="5c00f-106">**Note** When selecting a block size, consider the size of the SFT file and your network bandwidth.</span></span> <span data-ttu-id="5c00f-107">Un file con dimensioni di blocco più piccole richiede più tempo per eseguire il flusso sulla rete, ma è meno intensivo della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="5c00f-107">A file with a smaller block size takes longer to stream over the network, but it is less bandwidth intensive.</span></span> <span data-ttu-id="5c00f-108">I file con dimensioni di blocco più grandi potrebbero essere trasmessi più rapidamente, ma usano più larghezza di banda della rete.</span><span class="sxs-lookup"><span data-stu-id="5c00f-108">Files with larger block sizes might stream faster, but they use more network bandwidth.</span></span> <span data-ttu-id="5c00f-109">Grazie alla sperimentazione, è possibile individuare le dimensioni di blocco ottimali per le applicazioni di streaming della rete.</span><span class="sxs-lookup"><span data-stu-id="5c00f-109">Through experimentation, you can discover the optimum block size for streaming applications on your network.</span></span>

 

<span data-ttu-id="5c00f-110">La restante parte delle proprietà del pacchetto nella scheda **Proprietà** viene generata automaticamente e non può essere modificata in questa scheda.</span><span class="sxs-lookup"><span data-stu-id="5c00f-110">The remainder of the package properties on the **Properties** tab is automatically generated and cannot be modified on this tab.</span></span>

**<span data-ttu-id="5c00f-111">Per modificare il nome o i commenti del pacchetto</span><span class="sxs-lookup"><span data-stu-id="5c00f-111">To change the package name or comments</span></span>**

1.  <span data-ttu-id="5c00f-112">Fare clic sulla scheda **Proprietà** .</span><span class="sxs-lookup"><span data-stu-id="5c00f-112">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="5c00f-113">Nella casella di testo **nome pacchetto** immettere o modificare il singolo nome usato per il pacchetto, che può contenere più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5c00f-113">In the **Package Name** text box, enter or edit the single name used for the package, which can contain multiple applications.</span></span>

3.  <span data-ttu-id="5c00f-114">Nella casella di testo **Commenti** , facoltativamente, immettere o modificare i commenti.</span><span class="sxs-lookup"><span data-stu-id="5c00f-114">In the **Comments** text box, optionally enter or edit any comments.</span></span> <span data-ttu-id="5c00f-115">La procedura consigliata consigliata consiste nel creare informazioni dettagliate sul pacchetto e la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="5c00f-115">The suggested best practice is to provide detail information about the package and sequencing.</span></span>

4.  <span data-ttu-id="5c00f-116">Scegliere **Salva**dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="5c00f-116">From the **File** menu, select **Save**.</span></span>

**<span data-ttu-id="5c00f-117">Per modificare le dimensioni del blocco</span><span class="sxs-lookup"><span data-stu-id="5c00f-117">To change the block size</span></span>**

1.  <span data-ttu-id="5c00f-118">Fare clic sulla scheda **Proprietà** .</span><span class="sxs-lookup"><span data-stu-id="5c00f-118">Click the **Properties** tab.</span></span>

2.  <span data-ttu-id="5c00f-119">Nell'elenco a discesa **dimensione blocco** selezionare **4 KB**, **16 kb**, **32 KB**o **64 KB**.</span><span class="sxs-lookup"><span data-stu-id="5c00f-119">On the **Block Size** drop-down list, select **4 KB**, **16 KB**, **32 KB**, or **64 KB**.</span></span>

3.  <span data-ttu-id="5c00f-120">Scegliere **Salva**dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="5c00f-120">From the **File** menu, select **Save**.</span></span>

## <span data-ttu-id="5c00f-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c00f-121">Related topics</span></span>


[<span data-ttu-id="5c00f-122">Informazioni sulla scheda Proprietà</span><span class="sxs-lookup"><span data-stu-id="5c00f-122">About the Properties Tab</span></span>](about-the-properties-tab.md)

[<span data-ttu-id="5c00f-123">Console di Sequencer</span><span class="sxs-lookup"><span data-stu-id="5c00f-123">Sequencer Console</span></span>](sequencer-console.md)

 

 





