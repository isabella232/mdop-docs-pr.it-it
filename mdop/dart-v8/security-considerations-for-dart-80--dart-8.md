---
title: Considerazioni sulla sicurezza per DaRT 8.0
description: Considerazioni sulla sicurezza per DaRT 8.0
author: dansimp
ms.assetid: 45ef8164-fee7-41a1-9a36-de4e3264e7a8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 02d32d926c0def7d33bebd399cd380eed4e8385e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804420"
---
# <span data-ttu-id="a92de-103">Considerazioni sulla sicurezza per DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="a92de-103">Security Considerations for DaRT 8.0</span></span>


<span data-ttu-id="a92de-104">Questo argomento contiene una breve panoramica sugli account e i gruppi, i file di log e altre considerazioni relative alla sicurezza per Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.</span><span class="sxs-lookup"><span data-stu-id="a92de-104">This topic contains a brief overview about the accounts and groups, log files, and other security-related considerations for Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0.</span></span> <span data-ttu-id="a92de-105">Per altre informazioni, seguire i collegamenti contenuti in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="a92de-105">For more information, follow the links within this article.</span></span>

## <span data-ttu-id="a92de-106">Considerazioni generali sulla sicurezza</span><span class="sxs-lookup"><span data-stu-id="a92de-106">General security considerations</span></span>


<span data-ttu-id="a92de-107">**Comprendere i rischi per la sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="a92de-107">**Understand the security risks**.</span></span> <span data-ttu-id="a92de-108">DaRT 8,0 include funzionalità che consentono a un amministratore o a un lavoratore dell'help desk di eseguire gli strumenti DaRT in remoto per risolvere i problemi di un computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="a92de-108">DaRT 8.0 includes functionality that lets an administrator or a help desk worker run the DaRT tools remotely to resolve problems on an end-user computer.</span></span> <span data-ttu-id="a92de-109">È inoltre possibile salvare l'immagine ISO (International Organization for Standardizzation) in un'unità flash USB o inserire l'immagine ISO in una rete per includerne il contenuto come partizione di ripristino nel disco rigido di un computer.</span><span class="sxs-lookup"><span data-stu-id="a92de-109">In addition, you can save the International Organization for Standardization (ISO) image to a USB flash drive or put the ISO image on a network to include its contents as a recovery partition on a computer’s hard disk.</span></span> <span data-ttu-id="a92de-110">Queste funzionalità garantiscono flessibilità, ma creano anche potenziali rischi per la sicurezza da tenere in considerazione durante la configurazione di DaRT.</span><span class="sxs-lookup"><span data-stu-id="a92de-110">These capabilities provide flexibility, but also create potential security risks that you should consider when configuring DaRT.</span></span>

<span data-ttu-id="a92de-111">**Proteggere fisicamente i computer**.</span><span class="sxs-lookup"><span data-stu-id="a92de-111">**Physically secure your computers**.</span></span> <span data-ttu-id="a92de-112">Quando gli amministratori e i dipendenti dell'help desk non sono fisicamente al computer, dovrebbero bloccare i computer e usare uno screen saver protetto.</span><span class="sxs-lookup"><span data-stu-id="a92de-112">When administrators and help desk workers are not physically at their computers, they should lock their computers and use a secured screen saver.</span></span>

<span data-ttu-id="a92de-113">**Applicare gli aggiornamenti della sicurezza più recenti a tutti i computer**.</span><span class="sxs-lookup"><span data-stu-id="a92de-113">**Apply the most recent security updates to all computers**.</span></span> <span data-ttu-id="a92de-114">Rimanere informati sui nuovi aggiornamenti per i sistemi operativi iscrivendoti al servizio di notifica della sicurezza <https://go.microsoft.com/fwlink/?LinkId=28819> .</span><span class="sxs-lookup"><span data-stu-id="a92de-114">Stay informed about new updates for operating systems by subscribing to the Security Notification service (<https://go.microsoft.com/fwlink/?LinkId=28819>).</span></span>

## <span data-ttu-id="a92de-115">Limitare l'accesso degli utenti finali agli strumenti DaRT</span><span class="sxs-lookup"><span data-stu-id="a92de-115">Limit end-user access to DaRT tools</span></span>


<span data-ttu-id="a92de-116">Quando si crea l'immagine di ripristino delle freccette, è possibile selezionare gli strumenti da includere.</span><span class="sxs-lookup"><span data-stu-id="a92de-116">When you are creating the DaRT recovery image, you can select the tools that you want to include.</span></span> <span data-ttu-id="a92de-117">Per motivi di sicurezza, potresti voler limitare l'accesso degli utenti finali agli strumenti DaRT più potenti, come la cancellazione del disco e il fabbro.</span><span class="sxs-lookup"><span data-stu-id="a92de-117">For security reasons, you might want to restrict end-user access to the more powerful DaRT tools, such as Disk Wipe and Locksmith.</span></span> <span data-ttu-id="a92de-118">In DaRT 8,0 puoi disabilitare alcuni strumenti durante la configurazione e renderli ancora disponibili per aiutare gli operatori del servizio di assistenza quando l'utente finale avvia la funzionalità di connessione remota.</span><span class="sxs-lookup"><span data-stu-id="a92de-118">In DaRT 8.0, you can disable certain tools during configuration and still make them available to help desk workers when the end user starts the Remote Connection feature.</span></span>

<span data-ttu-id="a92de-119">È anche possibile configurare l'immagine del dardo in modo che l'opzione per avviare una sessione di connessione remota sia l'unico strumento disponibile per un utente finale.</span><span class="sxs-lookup"><span data-stu-id="a92de-119">You can even configure the DaRT image so that the option to start a remote connection session is the only tool available to an end user.</span></span>

<span data-ttu-id="a92de-120">**Importante**  Dopo aver stabilito la connessione remota, tutti gli strumenti inclusi nell'immagine di ripristino, inclusi quelli non disponibili per l'utente finale, saranno disponibili per qualsiasi lavoratore dell'help desk che sta lavorando al computer finale-utente.</span><span class="sxs-lookup"><span data-stu-id="a92de-120">**Important** After the remote connection is established, all the tools that you included in the recovery image, including those unavailable to the end user, will become available to any help desk worker who is working on the end–user computer.</span></span>

 

<span data-ttu-id="a92de-121">Per altre informazioni su come includere gli strumenti nell'immagine di ripristino delle freccette, vedere [Panoramica degli strumenti in dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="a92de-121">For more information about including tools in the DaRT recovery image, see [Overview of the Tools in DaRT 8.0](overview-of-the-tools-in-dart-80-dart-8.md).</span></span>

## <span data-ttu-id="a92de-122">Proteggere l'immagine di ripristino delle freccette</span><span class="sxs-lookup"><span data-stu-id="a92de-122">Secure the DaRT recovery image</span></span>


<span data-ttu-id="a92de-123">Se si distribuisce l'immagine di ripristino delle freccette salvarla in un'unità flash USB o creando una partizione remota o una partizione di ripristino, è possibile includere il metodo preferito della società per la crittografia dell'unità nell'ISO.</span><span class="sxs-lookup"><span data-stu-id="a92de-123">If you deploy the DaRT recovery image by saving it to a USB flash drive or by creating a remote partition or a recovery partition, you might want to include your company’s preferred method of drive encryption on the ISO.</span></span> <span data-ttu-id="a92de-124">La crittografia dell'ISO consente di garantire che gli utenti finali non possano usare le funzionalità DaRT se dovessero avere accesso all'immagine di ripristino e assicura che gli utenti non autorizzati non possano avviare il dardo in computer appartenenti a un altro utente.</span><span class="sxs-lookup"><span data-stu-id="a92de-124">Encrypting the ISO helps to ensure that end users cannot use DaRT functionality if they were to gain access to the recovery image, and it ensures that unauthorized users cannot boot into DaRT on computers that belong to someone else.</span></span> <span data-ttu-id="a92de-125">Se si usa un metodo di crittografia, assicurarsi di distribuirlo e abilitarlo in tutti i computer.</span><span class="sxs-lookup"><span data-stu-id="a92de-125">If you use an encryption method, be sure to deploy and enable it in all computers.</span></span>

<span data-ttu-id="a92de-126">**Nota**  DaRT 8,0 supporta BitLocker in modalità nativa.</span><span class="sxs-lookup"><span data-stu-id="a92de-126">**Note** DaRT 8.0 supports BitLocker natively.</span></span>

 

<span data-ttu-id="a92de-127">Per includere la crittografia unità, aggiungere i file della soluzione di crittografia quando si crea l'immagine di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a92de-127">To include drive encryption, add the encryption solution files when you create the recovery image.</span></span> <span data-ttu-id="a92de-128">La soluzione di crittografia deve essere in grado di essere eseguita su WinPE.</span><span class="sxs-lookup"><span data-stu-id="a92de-128">Your encryption solution must be able to run on WinPE.</span></span> <span data-ttu-id="a92de-129">Gli utenti finali che si avviano dall'ISO possono accedere alla soluzione di crittografia e sbloccare l'unità.</span><span class="sxs-lookup"><span data-stu-id="a92de-129">End users who boot from the ISO are then able to access that encryption solution and unblock the drive.</span></span>

## <span data-ttu-id="a92de-130">Mantenere la sicurezza tra due computer quando si usa la connessione remota</span><span class="sxs-lookup"><span data-stu-id="a92de-130">Maintain security between two computers when you use Remote Connection</span></span>


<span data-ttu-id="a92de-131">Per impostazione predefinita, la comunicazione tra due computer che hanno stabilito una sessione di **connessione remota** potrebbe non essere crittografata.</span><span class="sxs-lookup"><span data-stu-id="a92de-131">By default, the communication between two computers that have established a **Remote Connection** session may not be encrypted.</span></span> <span data-ttu-id="a92de-132">Pertanto, per semplificare la sicurezza tra i due computer, è consigliabile che entrambi i computer facciano parte della stessa rete.</span><span class="sxs-lookup"><span data-stu-id="a92de-132">Therefore, to help maintain security between the two computers, we recommend that both computers are a part of the same network.</span></span>

## <span data-ttu-id="a92de-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a92de-133">Related topics</span></span>


[<span data-ttu-id="a92de-134">Sicurezza e privacy per DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="a92de-134">Security and Privacy for DaRT 8.0</span></span>](security-and-privacy-for-dart-80-dart-8.md)

 

 





