---
title: Ripristino dei computer con DaRT 7.0
description: Ripristino dei computer con DaRT 7.0
author: dansimp
ms.assetid: bcded7ca-237b-4971-ac34-4394b05cbc50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 44dd48146155294bd8013b4b5a9bf23ffb3e8316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822766"
---
# <span data-ttu-id="908aa-103">Ripristino dei computer con DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="908aa-103">Recovering Computers Using DaRT 7.0</span></span>


<span data-ttu-id="908aa-104">Esistono due metodi disponibili per recuperare i computer usando Microsoft Diagnostics and Recovery Toolset (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="908aa-104">There are two methods available to recover computers using Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span> <span data-ttu-id="908aa-105">È possibile eseguire l'immagine di ripristino DaRT7 localmente o usare la funzionalità di connessione remota disponibile in DaRT7 per recuperare un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="908aa-105">You can either run the DaRT7 recovery image locally or use The Remote Connection feature available in DaRT7 to recover a remote computer.</span></span> <span data-ttu-id="908aa-106">In questa sezione vengono descritti in modo più dettagliato entrambi i metodi.</span><span class="sxs-lookup"><span data-stu-id="908aa-106">Both methods are described in more detail in this section.</span></span>

## <span data-ttu-id="908aa-107">Recuperare i computer locali usando l'immagine di ripristino DaRT</span><span class="sxs-lookup"><span data-stu-id="908aa-107">Recover Local Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="908aa-108">Per recuperare un computer locale usando DaRT7, è necessario essere fisicamente presenti nel computer dell'utente finale che sta riscontrando problemi che richiedono dardo.</span><span class="sxs-lookup"><span data-stu-id="908aa-108">To recover a local computer by using DaRT7, you must be physically present at the end-user computer that is experiencing problems that require DaRT.</span></span>

<span data-ttu-id="908aa-109">Sono disponibili diversi metodi tra cui scegliere per l'avvio in dardo, a seconda di come si distribuisce l'immagine di ripristino delle freccette.</span><span class="sxs-lookup"><span data-stu-id="908aa-109">You have several different methods to choose from to boot into DaRT, depending on how you deploy the DaRT recovery image.</span></span>

-   <span data-ttu-id="908aa-110">Inserire un CD, un DVD o un'unità flash USB nel computer problema e usarlo per avviare il computer.</span><span class="sxs-lookup"><span data-stu-id="908aa-110">Insert a DaRT recovery image CD, DVD, or USB flash drive into the problem computer and use it to boot into the computer.</span></span>

-   <span data-ttu-id="908aa-111">Avviare il dardo da una partizione di ripristino nel computer del problema.</span><span class="sxs-lookup"><span data-stu-id="908aa-111">Boot into DaRT from a recovery partition on the problem computer.</span></span>

-   <span data-ttu-id="908aa-112">Avviare il dardo da una partizione remota nella rete.</span><span class="sxs-lookup"><span data-stu-id="908aa-112">Boot into DaRT from a remote partition on the network.</span></span>

<span data-ttu-id="908aa-113">Per informazioni sui vantaggi e gli svantaggi di ogni metodo, vedere Pianificazione della [procedura per salvare e distribuire l'immagine di ripristino di DaRT 7,0](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span><span class="sxs-lookup"><span data-stu-id="908aa-113">For information about the advantages and disadvantages of each method, see [Planning How to Save and Deploy the DaRT 7.0 Recovery Image](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).</span></span>

<span data-ttu-id="908aa-114">Indipendentemente dal metodo usato per l'avvio in DaRT, devi abilitare il dispositivo di avvio nel BIOS per l'opzione di avvio o le opzioni che vuoi rendere disponibili all'utente finale.</span><span class="sxs-lookup"><span data-stu-id="908aa-114">Whichever method that you use to boot into DaRT, you must enable the boot device in the BIOS for the boot option or options that you want to make available to the end user.</span></span>

<span data-ttu-id="908aa-115">**Nota**  La configurazione del BIOS è univoca, a seconda del tipo di unità disco rigido, schede di rete e altro hardware usato nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="908aa-115">**Note** Configuring the BIOS is unique, depending on the kind of hard disk drive, network adapters, and other hardware that is used in your organization.</span></span>

 

[<span data-ttu-id="908aa-116">Come ripristinare i computer locali usando l'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="908aa-116">How to Recover Local Computers Using the DaRT Recovery Image</span></span>](how-to-recover-local-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="908aa-117">Recuperare computer remoti usando l'immagine di ripristino DaRT</span><span class="sxs-lookup"><span data-stu-id="908aa-117">Recover Remote Computers by Using the DaRT Recovery Image</span></span>


<span data-ttu-id="908aa-118">La funzionalità di connessione remota in DaRT consente a un amministratore IT di eseguire gli strumenti DaRT in remoto in un computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="908aa-118">The Remote Connection feature in DaRT lets an IT administrator run the DaRT tools remotely on an end-user computer.</span></span> <span data-ttu-id="908aa-119">Dopo che alcune informazioni sono state fornite dall'utente finale (o da un helpdesk professionale che lavora nel computer dell'utente finale), l'amministratore IT o l'agente dell'helpdesk può prendere il controllo del computer dell'utente finale ed eseguire gli strumenti DaRT necessari in remoto.</span><span class="sxs-lookup"><span data-stu-id="908aa-119">After certain information is provided by the end user (or by a helpdesk professional working on the end-user computer), the IT administrator or helpdesk agent can take control of the end user's computer and run the necessary DaRT tools remotely.</span></span>

<span data-ttu-id="908aa-120">**Importante**  I due computer che stabiliscono una connessione remota devono far parte della stessa rete.</span><span class="sxs-lookup"><span data-stu-id="908aa-120">**Important** The two computers establishing a remote connection must be part of the same network.</span></span>

 

<span data-ttu-id="908aa-121">La finestra del **set di strumenti di diagnostica e ripristino** include l'opzione per eseguire il comando Dart in un computer dell'utente finale da un computer amministratore.</span><span class="sxs-lookup"><span data-stu-id="908aa-121">The **Diagnostics and Recovery Toolset** window includes the option to run DaRT on an end-user computer remotely from an administrator computer.</span></span> <span data-ttu-id="908aa-122">L'utente finale apre gli strumenti DaRT nel computer problema e avvia la sessione remota facendo clic su **connessione remota**.</span><span class="sxs-lookup"><span data-stu-id="908aa-122">The end user opens the DaRT tools on the problem computer and starts the remote session by clicking **Remote Connection**.</span></span>

<span data-ttu-id="908aa-123">La funzionalità di connessione remota nel computer dell'utente finale crea le informazioni di connessione seguenti: un numero di biglietto, una porta e un elenco di tutti gli indirizzi IP disponibili.</span><span class="sxs-lookup"><span data-stu-id="908aa-123">The Remote Connection feature on the end-user computer creates the following connection information: a ticket number, a port, and a list of all available IP addresses.</span></span> <span data-ttu-id="908aa-124">Il numero di biglietto e la porta vengono generati in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="908aa-124">The ticket number and port are generated randomly.</span></span>

<span data-ttu-id="908aa-125">L'amministratore IT o l'agente dell'helpdesk immette queste informazioni nel **Visualizzatore di connessione remota Dart** per stabilire la connessione ai Servizi terminal per il computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="908aa-125">The IT administrator or helpdesk agent enters this information into the **DaRT Remote Connection Viewer** to establish the terminal services connection to the end-user computer.</span></span> <span data-ttu-id="908aa-126">La connessione di Servizi terminal che viene stabilita consente a un amministratore IT di interagire in remoto con gli strumenti DaRT nel computer dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="908aa-126">The terminal services connection that is established lets an IT administrator remotely interact with the DaRT tools on the end-user computer.</span></span> <span data-ttu-id="908aa-127">Il computer dell'utente finale elabora quindi le informazioni sulla connessione, condivide lo schermo e risponde alle istruzioni del computer dell'amministratore IT.</span><span class="sxs-lookup"><span data-stu-id="908aa-127">The end-user computer then processes the connection information, shares its screen, and responds to instructions from the IT administrator computer.</span></span>

[<span data-ttu-id="908aa-128">Come ripristinare i computer remoti con l'immagine di ripristino di DaRT</span><span class="sxs-lookup"><span data-stu-id="908aa-128">How to Recover Remote Computers Using the DaRT Recovery Image</span></span>](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md)

## <span data-ttu-id="908aa-129">Altre risorse per il recupero di computer con DaRT7</span><span class="sxs-lookup"><span data-stu-id="908aa-129">Other resources for recovering computers using DaRT7</span></span>


[<span data-ttu-id="908aa-130">Operazioni relative a DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="908aa-130">Operations for DaRT 7.0</span></span>](operations-for-dart-70-new-ia.md)

 

 





