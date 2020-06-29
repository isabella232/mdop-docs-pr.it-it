---
title: Pianificazione della distribuzione di DaRT 7.0
description: Pianificazione della distribuzione di DaRT 7.0
author: dansimp
ms.assetid: 05e97cdb-a8c2-46e4-9c75-a7d12fe26fe8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 09725e994a95f4f93ae655402e7577e137e33f18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821316"
---
# <span data-ttu-id="7c1c6-103">Pianificazione della distribuzione di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7c1c6-103">Planning to Deploy DaRT 7.0</span></span>


<span data-ttu-id="7c1c6-104">Prima di creare il piano di distribuzione, è necessario prendere in considerazione diverse configurazioni e prerequisiti di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-104">There are a number of different deployment configurations and prerequisites that you must consider before you create your deployment plan.</span></span> <span data-ttu-id="7c1c6-105">Questa sezione include informazioni che consentono di raccogliere le informazioni necessarie per formulare un piano di distribuzione che soddisfi meglio i requisiti aziendali.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-105">This section includes information that can help you gather the information that you must have to formulate a deployment plan that best meets your business requirements.</span></span>

<span data-ttu-id="7c1c6-106">Quando si pianifica l'installazione di Microsoft Diagnostics and Recovery Toolset (DaRT) 7, tenere presente quanto segue:</span><span class="sxs-lookup"><span data-stu-id="7c1c6-106">Consider the following when you plan your Microsoft Diagnostics and Recovery Toolset (DaRT)7 installation:</span></span>

-   <span data-ttu-id="7c1c6-107">Quando si installa DaRT, è possibile installare tutte le funzionalità in un computer dell'amministratore IT in cui verranno eseguite tutte le attività associate al dardo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-107">When you install DaRT, you can either install all functionality on an IT administrator computer where you will perform all the tasks associated with running DaRT.</span></span> <span data-ttu-id="7c1c6-108">In alternativa, è possibile installare solo la funzionalità DaRT che crea l'immagine di ripristino nel computer dell'amministratore IT.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-108">Or you can install only the DaRT functionality that creates the recovery image on the IT administrator computer.</span></span> <span data-ttu-id="7c1c6-109">Installare quindi la funzionalità usata per eseguire le freccette, ad esempio il **Visualizzatore di connessioni remote Dart** e l' **analizzatore di crash**, in un computer dell'agente helpdesk.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-109">Then, install the functionality used to run DaRT, such as the **DaRT Remote Connection Viewer** and **Crash Analyzer**, on a helpdesk agent computer.</span></span>

-   <span data-ttu-id="7c1c6-110">Per poter eseguire le freccette in remoto, verificare che il computer dell'agente helpdesk e tutti i computer a cui si sta risolvendo la risoluzione remota si trovino nella stessa rete.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-110">To be able to run DaRT remotely, make sure that the helpdesk agent computer and all computers that you might be troubleshooting remotely are on the same network.</span></span>

-   <span data-ttu-id="7c1c6-111">Prima di distribuire il dardo in produzione, è possibile creare prima di tutto un ambiente lab per i test.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-111">Before you roll out DaRT into production, you can first build a lab environment for testing.</span></span> <span data-ttu-id="7c1c6-112">Un laboratorio di test deve includere almeno due computer, uno per fungere da amministratore IT/computer dell'agente helpdesk e uno per fungere da computer per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-112">A test lab should include a minimum of two computers, one to act as the IT administrator/helpdesk agent computer and one to act as an end-user computer.</span></span> <span data-ttu-id="7c1c6-113">In alternativa, è possibile usare tre computer in laboratorio per separare le responsabilità dell'amministratore IT da quelle dell'agente helpdesk.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-113">Or, you can use three computers in your lab if you want to separate the IT administrator responsibilities from those of the helpdesk agent.</span></span>

## <span data-ttu-id="7c1c6-114">Rivedere le configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="7c1c6-114">Review the supported configurations</span></span>


<span data-ttu-id="7c1c6-115">Per verificare che i computer selezionati per l'installazione di client o funzionalità soddisfino i requisiti minimi per l'hardware e il sistema operativo, è consigliabile esaminare le informazioni sulle configurazioni di Microsoft Diagnostics and Recovery (DaRT) 7 supportate.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-115">You should review the Microsoft Diagnostics and Recovery Toolset (DaRT)7 Supported Configurations information to confirm that the computers you have selected for client or feature installation meet the minimum hardware and operating system requirements.</span></span>

[<span data-ttu-id="7c1c6-116">Configurazioni supportate di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7c1c6-116">DaRT 7.0 Supported Configurations</span></span>](dart-70-supported-configurations-dart-7.md)

## <span data-ttu-id="7c1c6-117">Pianificare la creazione dell'immagine di ripristino delle freccette</span><span class="sxs-lookup"><span data-stu-id="7c1c6-117">Plan for creating the DaRT recovery image</span></span>


<span data-ttu-id="7c1c6-118">Quando si crea l'immagine di ripristino delle freccette, è necessario decidere gli strumenti da includere nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-118">When you create the DaRT recovery image, you have to decide which tools to include on the image.</span></span> <span data-ttu-id="7c1c6-119">Quando si decide, tenere presente che gli utenti finali potrebbero avere accesso occasionalmente ai vari strumenti DaRT.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-119">When you make that decision, remember that end users might have access occasionally to the various DaRT tools.</span></span> <span data-ttu-id="7c1c6-120">Quando si crea l'immagine di ripristino, verrà specificato anche se si desidera includere altri driver o file.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-120">When you create the recovery image, you will also specify whether you want to include additional drivers or files.</span></span> <span data-ttu-id="7c1c6-121">Determinare le posizioni di eventuali altri driver o file che si desidera includere nell'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-121">Determine the locations of any additional drivers or files that you want to include on the DaRT recovery image.</span></span>

<span data-ttu-id="7c1c6-122">È necessario tenere presenti i prerequisiti e altri suggerimenti per la pianificazione aggiuntivi per la creazione dell'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-122">You should be aware of the prerequisites and other additional planning recommendations for creating the DaRT recovery image.</span></span>

[<span data-ttu-id="7c1c6-123">Pianificazione per la creazione dell'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7c1c6-123">Planning to Create the DaRT 7.0 Recovery Image</span></span>](planning-to-create-the-dart-70-recovery-image.md)

## <span data-ttu-id="7c1c6-124">Pianificare il salvataggio e la distribuzione dell'immagine di ripristino delle freccette</span><span class="sxs-lookup"><span data-stu-id="7c1c6-124">Plan for saving and deploying the DaRT recovery image</span></span>


<span data-ttu-id="7c1c6-125">Diversi metodi possono essere usati per salvare e distribuire l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-125">Several methods can be used to save and deploy the DaRT recovery image.</span></span> <span data-ttu-id="7c1c6-126">Quando si determina il metodo che si vuole usare, valutare i vantaggi e gli svantaggi di ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-126">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="7c1c6-127">Considera inoltre come vuoi usare il dardo nell'azienda.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-127">Also, consider how you want to use DaRT in your enterprise.</span></span>

<span data-ttu-id="7c1c6-128">**Nota**  Potresti voler usare più di un metodo nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-128">**Note** You might want to use more than one method in your organization.</span></span> <span data-ttu-id="7c1c6-129">Ad esempio, è possibile avviare il dardo da una partizione remota per la maggior parte delle situazioni e avere un'unità flash USB disponibile nel caso in cui il computer dell'utente finale non possa connettersi alla rete.</span><span class="sxs-lookup"><span data-stu-id="7c1c6-129">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

[<span data-ttu-id="7c1c6-130">Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7c1c6-130">Planning How to Save and Deploy the DaRT 7.0 Recovery Image</span></span>](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md)

## <span data-ttu-id="7c1c6-131">Altre risorse per la pianificazione della distribuzione di DaRT</span><span class="sxs-lookup"><span data-stu-id="7c1c6-131">Other resources for Planning to Deploy DaRT</span></span>


[<span data-ttu-id="7c1c6-132">Pianificazione di DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="7c1c6-132">Planning for DaRT 7.0</span></span>](planning-for-dart-70-new-ia.md)

 

 





