---
title: Come modificare le proprietà di distribuzione
description: Come modificare le proprietà di distribuzione
author: dansimp
ms.assetid: 0a214a7a-cc83-4d04-89f9-5727153be918
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dfb42962d41159479db61da9c3beb3771ef35502
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818065"
---
# <span data-ttu-id="247f4-103">Come modificare le proprietà di distribuzione</span><span class="sxs-lookup"><span data-stu-id="247f4-103">How to Change Deployment Properties</span></span>


<span data-ttu-id="247f4-104">Puoi usare le procedure seguenti per modificare le informazioni sulla scheda **distribuzione** per un'applicazione che stai sequenziando, incluso l'URL del server di virtualizzazione dell'applicazione, i sistemi operativi richiesti dalle applicazioni virtualizzate e le opzioni di output per l'applicazione virtuale da installare.</span><span class="sxs-lookup"><span data-stu-id="247f4-104">You can use the following procedures to change the **Deployment** tab information for an application you are sequencing, including the Application Virtualization server URL, the operating systems required by the virtualized applications, and the output options for the virtual application to be installed.</span></span>

**<span data-ttu-id="247f4-105">Per modificare l'URL del server</span><span class="sxs-lookup"><span data-stu-id="247f4-105">To change the server URL</span></span>**

1.  <span data-ttu-id="247f4-106">Selezionare il protocollo di flusso dalla casella di riepilogo a discesa.</span><span class="sxs-lookup"><span data-stu-id="247f4-106">Select the streaming protocol from the drop-down list box.</span></span>

2.  <span data-ttu-id="247f4-107">Immettere il nome host del server delle applicazioni virtuali o del bilanciamento del carico del gruppo Server.</span><span class="sxs-lookup"><span data-stu-id="247f4-107">Enter the host name of the virtual application server or the server group's load balancer.</span></span> <span data-ttu-id="247f4-108">È possibile usare il nome host o l'indirizzo IP effettivo.</span><span class="sxs-lookup"><span data-stu-id="247f4-108">You can use the actual host name or IP address.</span></span>

3.  <span data-ttu-id="247f4-109">Specifica il numero di porta in cui il server delle applicazioni virtuali o il bilanciamento del carico ascolteranno una richiesta client Desktop Application Virtualization per l'applicazione in streaming.</span><span class="sxs-lookup"><span data-stu-id="247f4-109">Specify the port number on which the virtual application server or load balancer will listen for an Application Virtualization Desktop Client request for the streamed application.</span></span>

4.  <span data-ttu-id="247f4-110">Specificare il percorso relativo nel server delle applicazioni virtuali in cui è archiviato il pacchetto software.</span><span class="sxs-lookup"><span data-stu-id="247f4-110">Specify the relative path on the virtual application server where the software package is stored.</span></span>

**<span data-ttu-id="247f4-111">Per modificare i requisiti dei sistemi operativi dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="247f4-111">To change the application operating systems requirements</span></span>**

1.  <span data-ttu-id="247f4-112">Per aggiungere il sistema operativo o i sistemi operativi necessari, selezionarlo nell'elenco **disponibile** e fare clic sul pulsante freccia che punta al controllo elenco dei sistemi operativi **selezionati** .</span><span class="sxs-lookup"><span data-stu-id="247f4-112">To add the required operating system(s), select it in the **Available** list and click the arrow button pointing to the **Selected** operating systems list control.</span></span>

2.  <span data-ttu-id="247f4-113">Per rimuovere un sistema operativo, selezionarlo nel controllo elenco **selezionato** e fare clic sul pulsante freccia che punta al controllo elenco sistemi operativi **disponibili** .</span><span class="sxs-lookup"><span data-stu-id="247f4-113">To remove an operating system, select it in the **Selected** list control, and click the arrow button pointing to the **Available** operating systems list control.</span></span>

**<span data-ttu-id="247f4-114">Per modificare le opzioni di output dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="247f4-114">To change the application output options</span></span>**

1.  <span data-ttu-id="247f4-115">Nell'elenco a discesa **algoritmo di compressione** selezionare il metodo di compressione da usare quando si esegue il flusso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="247f4-115">From the **Compression Algorithm** drop-down list, select the compression method to use when streaming the application.</span></span>

2.  <span data-ttu-id="247f4-116">Selezionare la casella di controllo **applica descrittori di sicurezza** per verificare che i descrittori di sicurezza delle applicazioni con pacchetto vengano applicati durante la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="247f4-116">Select the **Enforce Security Descriptors** check box to ensure security descriptors of the packaged applications are enforced when deployed.</span></span>

3.  <span data-ttu-id="247f4-117">Seleziona **genera file Difference** per generare un file Difference per l'applicazione dalla versione sequenziata precedente.</span><span class="sxs-lookup"><span data-stu-id="247f4-117">Select **Generate Difference File** to generate a difference file for the application from the previous sequenced version.</span></span>

4.  <span data-ttu-id="247f4-118">Selezionare **Genera pacchetto di Microsoft Windows Installer (MSI)** per creare un pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="247f4-118">Select **Generate Microsoft Windows Installer (MSI) Package** to create an installer package.</span></span>

## <span data-ttu-id="247f4-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="247f4-119">Related topics</span></span>


[<span data-ttu-id="247f4-120">Informazioni sulla scheda Distribuzione</span><span class="sxs-lookup"><span data-stu-id="247f4-120">About the Deployment Tab</span></span>](about-the-deployment-tab.md)

[<span data-ttu-id="247f4-121">Console di Sequencer</span><span class="sxs-lookup"><span data-stu-id="247f4-121">Sequencer Console</span></span>](sequencer-console.md)

 

 





