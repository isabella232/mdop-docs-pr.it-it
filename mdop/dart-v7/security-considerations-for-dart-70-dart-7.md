---
title: Considerazioni sulla sicurezza per DaRT 7.0
description: Considerazioni sulla sicurezza per DaRT 7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822735"
---
# <span data-ttu-id="cc10f-103">Considerazioni sulla sicurezza per DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="cc10f-103">Security Considerations for DaRT 7.0</span></span>


<span data-ttu-id="cc10f-104">Microsoft Diagnostics and Recovery Toolset (DaRT) 7 include funzionalità che consentono a un amministratore di eseguire gli strumenti DaRT in remoto per risolvere i problemi di un computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="cc10f-104">Microsoft Diagnostics and Recovery Toolset (DaRT)7 includes functionality that lets an administrator run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="cc10f-105">Nelle versioni precedenti di DaRT, un tecnico o un amministratore dell'help desk dovevano essere fisicamente in un computer per gli utenti finali ed eseguire il boot in DaRT usando il CD o il DVD che includeva l'immagine di ripristino DaRT.</span><span class="sxs-lookup"><span data-stu-id="cc10f-105">In earlier releases of DaRT, a help desk technician or administrator had to physically be at an end-user computer and boot into DaRT by using the CD or DVD that included the DaRT recovery image.</span></span> <span data-ttu-id="cc10f-106">A questo punto, il tecnico o l'amministratore dell'help desk può eseguire le stesse procedure in remoto.</span><span class="sxs-lookup"><span data-stu-id="cc10f-106">Now, the help desk technician or administrator can perform the same procedures remotely.</span></span>

<span data-ttu-id="cc10f-107">Anche in DaRT7, oltre alla masterizzazione di un CD o DVD, è ora possibile salvare l'immagine ISO (International Organization for Standardizzation) in un'unità flash USB.</span><span class="sxs-lookup"><span data-stu-id="cc10f-107">Also in DaRT7, in addition to burning a CD or DVD, you are now able to save the International Organization for Standardization (ISO) image to a USB flash drive.</span></span> <span data-ttu-id="cc10f-108">È anche possibile inserire l'immagine ISO in una rete o includerne il contenuto come partizione di ripristino in un disco rigido del computer.</span><span class="sxs-lookup"><span data-stu-id="cc10f-108">You can also put the ISO image on a network or include its contents as a recovery partition on a computer hard disk.</span></span>

<span data-ttu-id="cc10f-109">La caratteristica di **connessione remota** in DaRT7 consente agli utenti finali di accedere a Dart usando uno di questi nuovi metodi di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="cc10f-109">The **Remote Connection** feature in DaRT7 lets end users access DaRT by using one of these new deployment methods.</span></span> <span data-ttu-id="cc10f-110">Di conseguenza, possono avviare più facilmente le freccette e accedere agli strumenti DaRT.</span><span class="sxs-lookup"><span data-stu-id="cc10f-110">Therefore, they can more easily start DaRT and access the DaRT tools.</span></span>

<span data-ttu-id="cc10f-111">Le nuove funzionalità di DaRT7 garantiscono molto più flessibilità nel modo in cui usi dardo nell'azienda.</span><span class="sxs-lookup"><span data-stu-id="cc10f-111">The new functionalities in DaRT7 provide much more flexibility in how you use DaRT in your enterprise.</span></span> <span data-ttu-id="cc10f-112">Tuttavia, crea anche il proprio set di problemi di sicurezza che devono essere affrontati.</span><span class="sxs-lookup"><span data-stu-id="cc10f-112">However, they also create their own set of security issues that must be addressed.</span></span> <span data-ttu-id="cc10f-113">Quando si configura dardo, è consigliabile prendere in considerazione i seguenti suggerimenti per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="cc10f-113">We recommend that you consider the following security tips when you configure DaRT.</span></span>

## <span data-ttu-id="cc10f-114">Per mantenere la sicurezza quando si crea l'immagine di ripristino delle freccette</span><span class="sxs-lookup"><span data-stu-id="cc10f-114">To help maintain security when you create the DaRT recovery image</span></span>


<span data-ttu-id="cc10f-115">Quando si crea l'immagine di ripristino delle freccette, è possibile selezionare gli strumenti da includere.</span><span class="sxs-lookup"><span data-stu-id="cc10f-115">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="cc10f-116">Per motivi di sicurezza, potresti voler limitare l'accesso degli utenti finali agli strumenti DaRT più potenti, come la cancellazione del disco e il fabbro.</span><span class="sxs-lookup"><span data-stu-id="cc10f-116">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="cc10f-117">In DaRT7 è possibile disabilitare determinati strumenti durante la configurazione e renderli ancora disponibili per gli agenti dell'helpdesk quando l'utente finale avvia la funzionalità di connessione remota.</span><span class="sxs-lookup"><span data-stu-id="cc10f-117">In DaRT7, you can disable certain tools during configuration and still make them available to helpdesk agents when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="cc10f-118">È anche possibile configurare l'immagine del dardo in modo che l'opzione per avviare una sessione di connessione remota sia l'unico strumento disponibile per un utente finale.</span><span class="sxs-lookup"><span data-stu-id="cc10f-118">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="cc10f-119">**Importante**  Dopo aver stabilito la connessione remota, tutti gli strumenti inclusi nell'immagine di ripristino, inclusi quelli non disponibili per l'utente finale, saranno disponibili per l'agente helpdesk che lavora al computer finale-utente.</span><span class="sxs-lookup"><span data-stu-id="cc10f-119">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to the helpdesk agent working on the end–user computer.</span></span>

 

<span data-ttu-id="cc10f-120">Per altre informazioni su come includere gli strumenti nell'immagine di ripristino delle freccette, vedere [come usare la creazione guidata immagine di ripristino di freccette per creare l'immagine di ripristino](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span><span class="sxs-lookup"><span data-stu-id="cc10f-120">For more information about including tools in the DaRT recovery image, see [How to Use the DaRT Recovery Image Wizard to Create the Recovery Image](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).</span></span>

## <span data-ttu-id="cc10f-121">Per semplificare la sicurezza, crittografando l'immagine di ripristino delle freccette</span><span class="sxs-lookup"><span data-stu-id="cc10f-121">To help maintain security by encrypting the DaRT recovery image</span></span>


<span data-ttu-id="cc10f-122">Se si usa una delle opzioni di distribuzione nuove in DaRT7, ad esempio il salvataggio in un'unità flash USB o la creazione di una partizione remota o di una partizione di ripristino, è possibile includere il metodo preferito della società per la crittografia dell'unità nell'ISO.</span><span class="sxs-lookup"><span data-stu-id="cc10f-122">If you use one of the deployment options new in DaRT7, for example, saving to a USB flash drive or creating a remote partition or a recovery partition, you can include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="cc10f-123">Ciò consentirà di verificare che un utente finale non possa usare la funzionalità di DaRT per ottenere l'accesso all'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="cc10f-123">This will help make sure that an end user cannot use the functionality of DaRT should they gain access to the recovery image.</span></span> <span data-ttu-id="cc10f-124">E farà anche in modo che gli utenti non autorizzati non possano avviare il dardo in computer appartenenti a un altro utente.</span><span class="sxs-lookup"><span data-stu-id="cc10f-124">And it will also make sure that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span>

<span data-ttu-id="cc10f-125">Il metodo di crittografia deve essere distribuito e abilitato in tutti i computer.</span><span class="sxs-lookup"><span data-stu-id="cc10f-125">Your encryption method should be deployed and enabled in all computers.</span></span>

<span data-ttu-id="cc10f-126">**Nota**  DaRT7 supporta BitLocker nativamente.</span><span class="sxs-lookup"><span data-stu-id="cc10f-126">**Note** DaRT7 supports BitLocker natively.</span></span>

 

## <span data-ttu-id="cc10f-127">Per semplificare la sicurezza tra due computer durante la connessione remota</span><span class="sxs-lookup"><span data-stu-id="cc10f-127">To help maintain security between two computers during Remote Connection</span></span>


<span data-ttu-id="cc10f-128">Per impostazione predefinita, la comunicazione tra due computer che hanno stabilito una sessione di **connessione remota** potrebbe non essere crittografata.</span><span class="sxs-lookup"><span data-stu-id="cc10f-128">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="cc10f-129">Pertanto, per semplificare la sicurezza tra i due computer, è consigliabile che entrambi i computer facciano parte della stessa rete.</span><span class="sxs-lookup"><span data-stu-id="cc10f-129">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="cc10f-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc10f-130">Related topics</span></span>


[<span data-ttu-id="cc10f-131">Operazioni relative a DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="cc10f-131">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





