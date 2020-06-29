---
title: Ripristino dei computer con DaRT 8.0
description: Ripristino dei computer con DaRT 8.0
author: dansimp
ms.assetid: 0caeb7d9-c1e6-4f32-bc27-157b91630989
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39bab02488252b53deb971d35bc6872c0a2df73b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824866"
---
# <span data-ttu-id="6ca54-103">Ripristino dei computer con DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="6ca54-103">Recovering Computers Using DaRT 8.0</span></span>


<span data-ttu-id="6ca54-104">Dopo la distribuzione dell'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0, puoi usare DaRT 8,0 per recuperare i computer.</span><span class="sxs-lookup"><span data-stu-id="6ca54-104">After deploying the Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0 recovery image, you can use DaRT 8.0 to recover computers.</span></span> <span data-ttu-id="6ca54-105">Le informazioni in questa sezione illustrano le attività di ripristino che è possibile eseguire.</span><span class="sxs-lookup"><span data-stu-id="6ca54-105">The information in this section describes the recovery tasks that you can perform.</span></span>

<span data-ttu-id="6ca54-106">Sono disponibili diversi metodi tra cui scegliere per l'avvio in dardo, a seconda di come si distribuisce l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="6ca54-106">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="6ca54-107">Inserire un CD, un DVD o un'unità flash USB nel computer problema e usarlo per avviare il computer.</span><span class="sxs-lookup"><span data-stu-id="6ca54-107">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="6ca54-108">Avviare il dardo da una partizione di ripristino nel computer del problema.</span><span class="sxs-lookup"><span data-stu-id="6ca54-108">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="6ca54-109">Avviare il dardo da una partizione remota nella rete.</span><span class="sxs-lookup"><span data-stu-id="6ca54-109">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="6ca54-110">Per informazioni sui vantaggi e gli svantaggi di ogni metodo, vedere Pianificazione della [procedura per salvare e distribuire l'immagine di ripristino di DaRT 8,0](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="6ca54-110">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 8.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).</span></span>

<span data-ttu-id="6ca54-111">Indipendentemente dal metodo usato per l'avvio in DaRT, devi abilitare il dispositivo di avvio nel BIOS per l'opzione di avvio o le opzioni che vuoi rendere disponibili all'utente finale.</span><span class="sxs-lookup"><span data-stu-id="6ca54-111">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="6ca54-112">**Nota**  La configurazione del BIOS è univoca, a seconda del tipo di unità disco rigido, schede di rete e altro hardware usato nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="6ca54-112">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

## <span data-ttu-id="6ca54-113">Recuperare un computer locale usando l'immagine di ripristino DaRT</span><span class="sxs-lookup"><span data-stu-id="6ca54-113">Recover a local computer by using the DaRT recovery image</span></span>


<span data-ttu-id="6ca54-114">Per recuperare un computer locale tramite dardo, è necessario essere fisicamente presenti nel computer dell'utente finale che sta riscontrando problemi che richiedono dardo.</span><span class="sxs-lookup"><span data-stu-id="6ca54-114">To recover a local computer by using DaRT, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

[<span data-ttu-id="6ca54-115">Come ripristinare i computer locali usando l'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="6ca54-115">How to Recover Local Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-8.md)

## <span data-ttu-id="6ca54-116">Recuperare un computer remoto usando l'immagine di ripristino DaRT</span><span class="sxs-lookup"><span data-stu-id="6ca54-116">Recover a remote computer by using the DaRT recovery image</span></span>


<span data-ttu-id="6ca54-117">La funzionalità di connessione remota in DaRT consente a un amministratore IT di eseguire gli strumenti DaRT in remoto in un computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="6ca54-117">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="6ca54-118">Dopo che alcune informazioni sono state fornite dall'utente finale (o da un Help Desk Professional che lavora nel computer dell'utente finale), l'amministratore IT o il lavoratore dell'help desk può prendere il controllo del computer dell'utente finale ed eseguire gli strumenti DaRT necessari in remoto.</span><span class="sxs-lookup"><span data-stu-id="6ca54-118">After certain information is provided by the end user (or by a help desk professional working on the end-user computer), the IT administrator or help desk worker can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="6ca54-119">**Importante**  I due computer che stabiliscono una connessione remota devono far parte della stessa rete.</span><span class="sxs-lookup"><span data-stu-id="6ca54-119">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="6ca54-120">La finestra del **set di strumenti di diagnostica e ripristino** include l'opzione per eseguire il comando Dart in un computer dell'utente finale da un computer amministratore.</span><span class="sxs-lookup"><span data-stu-id="6ca54-120">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="6ca54-121">L'utente finale apre gli strumenti DaRT nel computer problema e avvia la sessione remota facendo clic su **connessione remota**.</span><span class="sxs-lookup"><span data-stu-id="6ca54-121">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="6ca54-122">La funzionalità di connessione remota nel computer dell'utente finale crea le informazioni di connessione seguenti: un numero di biglietto, una porta e un elenco di tutti gli indirizzi IP disponibili.</span><span class="sxs-lookup"><span data-stu-id="6ca54-122">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="6ca54-123">Il numero di biglietto e la porta vengono generati in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="6ca54-123">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="6ca54-124">L'amministratore IT o il lavoratore dell'help desk immette queste informazioni nel **Visualizzatore di connessioni remote di Dart** per stabilire la connessione di Servizi terminal al computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="6ca54-124">The IT administrator or help desk worker enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="6ca54-125">La connessione di Servizi terminal che viene stabilita consente a un amministratore IT di interagire in remoto con gli strumenti DaRT nel computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="6ca54-125">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="6ca54-126">Il computer dell'utente finale elabora quindi le informazioni sulla connessione, condivide lo schermo e risponde alle istruzioni del computer dell'amministratore IT.</span><span class="sxs-lookup"><span data-stu-id="6ca54-126">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="6ca54-127">Come ripristinare i computer remoti con l'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="6ca54-127">How to Recover Remote Computers by Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-by-using-the-dart-recovery-image-dart-8.md)

## <span data-ttu-id="6ca54-128">Altre risorse per il recupero di computer con DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="6ca54-128">Other resources for recovering computers using DaRT 8.0</span></span>


[<span data-ttu-id="6ca54-129">Operazioni relative a DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="6ca54-129">Operations for DaRT 8.0</span></span>](operations-for-dart-80-dart-8.md)

 

 





