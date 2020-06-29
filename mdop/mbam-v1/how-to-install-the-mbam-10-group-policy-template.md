---
title: Come installare il modello Criteri di gruppo di MBAM 1.0
description: Come installare il modello Criteri di gruppo di MBAM 1.0
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825336"
---
# <span data-ttu-id="0da50-103">Come installare il modello Criteri di gruppo di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0da50-103">How to Install the MBAM 1.0 Group Policy Template</span></span>


<span data-ttu-id="0da50-104">Oltre alle funzionalità relative al server di Microsoft BitLocker Administration and Monitoring (MBAM), l'applicazione di configurazione del server include un modello di criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="0da50-104">In addition to the server-related features of Microsoft BitLocker Administration and Monitoring (MBAM), the server setup application includes an MBAM Group Policy template.</span></span> <span data-ttu-id="0da50-105">Questo modello può essere installato in qualsiasi computer in grado di eseguire la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0da50-105">You can install this template on any computer that is capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="0da50-106">I passaggi seguenti descrivono come installare il modello dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="0da50-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="0da50-107">**Nota**  Verificare di usare la configurazione a 32 bit nei server a 32 bit e la configurazione a 64 bit nei server a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="0da50-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="0da50-108">Per installare il modello dei criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="0da50-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="0da50-109">Avviare l'installazione guidata di MBAM; Fare quindi clic su **Installa** nella pagina di benvenuto.</span><span class="sxs-lookup"><span data-stu-id="0da50-109">Start the MBAM installation wizard; then, click **Install** on the Welcome page.</span></span>

2.  <span data-ttu-id="0da50-110">Leggere e accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="0da50-110">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

3.  <span data-ttu-id="0da50-111">Per impostazione predefinita, tutte le caratteristiche di MBAM sono selezionate per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="0da50-111">By default, all MBAM features are selected for installation.</span></span> <span data-ttu-id="0da50-112">Deselezionare tutte le opzioni di funzionalità tranne il **modello di criteri**e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="0da50-112">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="0da50-113">**Nota**  La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti.</span><span class="sxs-lookup"><span data-stu-id="0da50-113">**Note** The installation wizard checks the prerequisites for your installation and displays the prerequisites that are missing.</span></span> <span data-ttu-id="0da50-114">Se tutti i prerequisiti sono soddisfatti, l'installazione continua.</span><span class="sxs-lookup"><span data-stu-id="0da50-114">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="0da50-115">Se viene rilevato un prerequisito mancante, è necessario risolvere il presupposto mancante e quindi fare di nuovo clic su **Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="0da50-115">If a missing prerequisite is detected, you must resolve the missing prerequisite and then click **Check prerequisites again**.</span></span> <span data-ttu-id="0da50-116">Dopo aver soddisfatto tutti i prerequisiti, l'installazione verrà ripresa.</span><span class="sxs-lookup"><span data-stu-id="0da50-116">Once all prerequisites are met, the installation will resume.</span></span>

     

4.  <span data-ttu-id="0da50-117">Dopo la configurazione guidata MBAM Visualizza le pagine di installazione per le caratteristiche selezionate, fare clic su **fine** per chiudere la configurazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="0da50-117">After the MBAM Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="0da50-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0da50-118">Related topics</span></span>


[<span data-ttu-id="0da50-119">Distribuzione degli oggetti Criteri di gruppo di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0da50-119">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





