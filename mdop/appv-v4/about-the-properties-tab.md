---
title: Informazioni sulla scheda Proprietà
description: Informazioni sulla scheda Proprietà
author: dansimp
ms.assetid: a6cf6f51-3778-4c8d-9632-3af4005775d2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b2d6c3e01dde48fdd6701984f66610ea0333b74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819925"
---
# <span data-ttu-id="1d6ad-103">Informazioni sulla scheda Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d6ad-103">About the Properties Tab</span></span>


<span data-ttu-id="1d6ad-104">Usare la scheda **Proprietà** per visualizzare informazioni statistiche di base su un pacchetto di applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-104">Use the **Properties** tab to view basic statistical information about a sequenced application package.</span></span> <span data-ttu-id="1d6ad-105">Le informazioni vengono generate automaticamente, se non diversamente specificato.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-105">The information is automatically generated unless otherwise noted.</span></span> <span data-ttu-id="1d6ad-106">Questa scheda contiene gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-106">This tab contains the following elements.</span></span>

## <span data-ttu-id="1d6ad-107">Informazioni sul pacchetto</span><span class="sxs-lookup"><span data-stu-id="1d6ad-107">Package Information</span></span>


<a href="" id="package-name"></a>**<span data-ttu-id="1d6ad-108">Nome pacchetto</span><span class="sxs-lookup"><span data-stu-id="1d6ad-108">Package Name</span></span>**  
<span data-ttu-id="1d6ad-109">Il singolo nome usato per un pacchetto di applicazione sequenziale che potrebbe contenere una o più applicazioni, ad esempio Microsoft Office può essere usato per assegnare un'etichetta a un pacchetto di applicazione sequenziale che contiene le applicazioni Microsoft Word e Microsoft Excel eseguite nello stesso ambiente virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-109">The single name used for a sequenced application package that might contain one or more applications—for example, Microsoft Office could be used to label a sequenced application package that contains Microsoft Word and Microsoft Excel applications that run in the same virtual environment.</span></span>

<a href="" id="comments"></a>**<span data-ttu-id="1d6ad-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d6ad-110">Comments</span></span>**  
<span data-ttu-id="1d6ad-111">Visualizza una breve descrizione del pacchetto software che verrà visualizzato nell'elemento astratto del file OSD (Open Software Descriptor).</span><span class="sxs-lookup"><span data-stu-id="1d6ad-111">Displays a short description of the software package that will appear in the Open Software Descriptor (OSD) file ABSTRACT element.</span></span> <span data-ttu-id="1d6ad-112">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-112">This item is optional.</span></span>

<a href="" id="package-version"></a>**<span data-ttu-id="1d6ad-113">Versione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="1d6ad-113">Package Version</span></span>**  
<span data-ttu-id="1d6ad-114">Versione del pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-114">The sequenced application package version.</span></span>

<a href="" id="package-guid"></a>**<span data-ttu-id="1d6ad-115">GUID del pacchetto</span><span class="sxs-lookup"><span data-stu-id="1d6ad-115">Package GUID</span></span>**  
<span data-ttu-id="1d6ad-116">L'identificatore univoco globale (GUID) assegnato automaticamente al pacchetto dell'applicazione sequenziata per distinguerlo dagli altri pacchetti di applicazioni sequenziate che potrebbero essere in uso nel computer in cui è in streaming un pacchetto di applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-116">The globally unique identifier (GUID) automatically assigned to the sequenced application package to distinguish it from other sequenced application packages that might be running on the computer to which a sequenced application package is streamed.</span></span>

<a href="" id="package-version-guid"></a>**<span data-ttu-id="1d6ad-117">GUID versione pacchetto</span><span class="sxs-lookup"><span data-stu-id="1d6ad-117">Package Version GUID</span></span>**  
<span data-ttu-id="1d6ad-118">GUID della versione del pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-118">The sequenced application package version GUID.</span></span>

<a href="" id="root-directory"></a>**<span data-ttu-id="1d6ad-119">Directory radice</span><span class="sxs-lookup"><span data-stu-id="1d6ad-119">Root Directory</span></span>**  
<span data-ttu-id="1d6ad-120">Directory nel computer di sequenziazione in cui sono installati i file per il pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-120">The directory on the sequencing computer in which files for the sequenced application package are installed.</span></span> <span data-ttu-id="1d6ad-121">Questa directory viene creata anche nel computer in cui verrà trasmesso un pacchetto di applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-121">This directory is also created on the computer to which a sequenced application package will be streamed.</span></span> <span data-ttu-id="1d6ad-122">È consigliabile per la compatibilità con le versioni precedenti che si tratta di un nome di directory in formato 8,3 nella radice dell'unità Q, ad esempio Q:\\MyApp.1\\.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-122">It is recommended for backwards compatibility that this be an 8.3 format directory name at the root of the Q drive, such as Q:\\MyApp.1\\.</span></span>

<a href="" id="created"></a>**<span data-ttu-id="1d6ad-123">Creato</span><span class="sxs-lookup"><span data-stu-id="1d6ad-123">Created</span></span>**  
<span data-ttu-id="1d6ad-124">Data e ora in cui è stato creato il pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-124">The date and time the sequenced application package was created.</span></span>

<a href="" id="modified"></a>**<span data-ttu-id="1d6ad-125">Modificato</span><span class="sxs-lookup"><span data-stu-id="1d6ad-125">Modified</span></span>**  
<span data-ttu-id="1d6ad-126">Data e ora dell'Ultima modifica del pacchetto dell'applicazione sequenziata.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-126">The date and time the sequenced application package was last modified.</span></span>

<a href="" id="package-size"></a>**<span data-ttu-id="1d6ad-127">Dimensioni del pacchetto</span><span class="sxs-lookup"><span data-stu-id="1d6ad-127">Package Size</span></span>**  
<span data-ttu-id="1d6ad-128">Dimensioni del pacchetto in megabyte.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-128">The size of the package in megabytes.</span></span>

<a href="" id="launch-size"></a>**<span data-ttu-id="1d6ad-129">Dimensioni di avvio</span><span class="sxs-lookup"><span data-stu-id="1d6ad-129">Launch Size</span></span>**  
<span data-ttu-id="1d6ad-130">Dimensioni in megabyte della parte del file SFT necessaria per avviare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-130">The size in megabytes of the portion of the SFT file that is required to start the application.</span></span>

## <span data-ttu-id="1d6ad-131">Parametri di sequenziazione</span><span class="sxs-lookup"><span data-stu-id="1d6ad-131">Sequencing Parameters</span></span>


<a href="" id="block-size"></a>**<span data-ttu-id="1d6ad-132">Dimensione blocco</span><span class="sxs-lookup"><span data-stu-id="1d6ad-132">Block Size</span></span>**  
<span data-ttu-id="1d6ad-133">Specifica le dimensioni dei blocchi di funzionalità primari e secondari in cui il file SFT è diviso per lo streaming in una rete.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-133">Specifies the size of the primary and secondary feature blocks into which the SFT file is divided for streaming across a network.</span></span> <span data-ttu-id="1d6ad-134">Tutti i blocchi equivalgono alle dimensioni specificate; l'ultimo blocco potrebbe tuttavia essere più piccolo di quello specificato.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-134">All blocks equal the specified size; however, the last block might be smaller than specified.</span></span> <span data-ttu-id="1d6ad-135">Verrà visualizzato uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1d6ad-135">You will see one of the following values:</span></span>

-   <span data-ttu-id="1d6ad-136">4 KB</span><span class="sxs-lookup"><span data-stu-id="1d6ad-136">4 KB</span></span>

-   <span data-ttu-id="1d6ad-137">16 KB</span><span class="sxs-lookup"><span data-stu-id="1d6ad-137">16 KB</span></span>

-   <span data-ttu-id="1d6ad-138">32 KB</span><span class="sxs-lookup"><span data-stu-id="1d6ad-138">32 KB</span></span>

-   <span data-ttu-id="1d6ad-139">64 KB</span><span class="sxs-lookup"><span data-stu-id="1d6ad-139">64 KB</span></span>

<span data-ttu-id="1d6ad-140">**Nota**  Dopo aver creato il pacchetto iniziale, il valore della dimensione del blocco non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="1d6ad-140">**Note** After the initial package has been created, the block size value is not changeable.</span></span>

 

## <span data-ttu-id="1d6ad-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d6ad-141">Related topics</span></span>


[<span data-ttu-id="1d6ad-142">Come modificare le proprietà del pacchetto</span><span class="sxs-lookup"><span data-stu-id="1d6ad-142">How to Change Package Properties</span></span>](how-to-change-package-properties.md)

[<span data-ttu-id="1d6ad-143">Console di Sequencer</span><span class="sxs-lookup"><span data-stu-id="1d6ad-143">Sequencer Console</span></span>](sequencer-console.md)

 

 





