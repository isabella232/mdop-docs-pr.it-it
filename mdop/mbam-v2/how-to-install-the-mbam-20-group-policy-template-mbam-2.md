---
title: Come installare il modello Criteri di gruppo di MBAM 2.0
description: Come installare il modello Criteri di gruppo di MBAM 2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826255"
---
# <span data-ttu-id="2f3cc-103">Come installare il modello Criteri di gruppo di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2f3cc-103">How to Install the MBAM 2.0 Group Policy Template</span></span>


<span data-ttu-id="2f3cc-104">Oltre alle caratteristiche di amministrazione e monitoraggio Microsoft BitLocker correlate al server, l'applicazione di configurazione del server include un modello di criteri di gruppo per l'amministrazione e il monitoraggio di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-104">In addition to the server-related Microsoft BitLocker Administration and Monitoring (MBAM) features, the server setup application includes an Microsoft BitLocker Administration and Monitoring Group Policy template.</span></span> <span data-ttu-id="2f3cc-105">Questo modello può essere installato in qualsiasi computer in grado di eseguire la console Gestione criteri di gruppo o gestione avanzata Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-105">This template can be installed on any computer capable of running the Group Policy Management Console (GPMC) or Advanced Group Policy Management (AGPM).</span></span>

<span data-ttu-id="2f3cc-106">I passaggi seguenti descrivono come installare il modello dei criteri di gruppo di MBAM.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-106">The following steps describe how to install the MBAM Group Policy template.</span></span>

<span data-ttu-id="2f3cc-107">**Nota**  Verificare di usare la configurazione a 32 bit nei server a 32 bit e la configurazione a 64 bit nei server a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-107">**Note** Make sure that you use the 32-bit setup on 32-bit servers and the 64-bit setup on 64-bit servers.</span></span>

 

**<span data-ttu-id="2f3cc-108">Per installare il modello dei criteri di gruppo di MBAM</span><span class="sxs-lookup"><span data-stu-id="2f3cc-108">To install the MBAM Group Policy template</span></span>**

1.  <span data-ttu-id="2f3cc-109">Nel server in cui si vuole installare MBAM eseguire **MBAMSetup.exe** per avviare l'installazione guidata di mbam.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-109">On the server where you want to install MBAM, run **MBAMSetup.exe** to start the MBAM installation wizard.</span></span>

2.  <span data-ttu-id="2f3cc-110">Nella pagina di **benvenuto** selezionare facoltativamente il **programma Analisi utilizzo software**e quindi fare clic su **Avvia**.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-110">On the **Welcome** page, optionally select the **Customer Experience Improvement Program**, and then click **Start**.</span></span>

3.  <span data-ttu-id="2f3cc-111">Leggere e accettare le condizioni di licenza software Microsoft e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-111">Read and accept the Microsoft Software License Terms, and then click **Next** to continue the installation.</span></span>

4.  <span data-ttu-id="2f3cc-112">Per impostazione predefinita, tutte le funzionalità di amministrazione e monitoraggio di Microsoft BitLocker sono selezionate per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-112">By default, all Microsoft BitLocker Administration and Monitoring features are selected for installation.</span></span> <span data-ttu-id="2f3cc-113">Deselezionare tutte le opzioni di funzionalità tranne il **modello di criteri**e quindi fare clic su **Avanti** per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-113">Clear all feature options except for **Policy Template**, and then click **Next** to continue the installation.</span></span>

    <span data-ttu-id="2f3cc-114">**Nota**  La procedura guidata di installazione controlla i prerequisiti per l'installazione e Visualizza i prerequisiti mancanti.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-114">**Note** The installation wizard checks the prerequisites for your installation and displays prerequisites that are missing.</span></span> <span data-ttu-id="2f3cc-115">Se tutti i prerequisiti sono soddisfatti, l'installazione continua.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-115">If all the prerequisites are met, the installation continues.</span></span> <span data-ttu-id="2f3cc-116">Se viene rilevato un prerequisito mancante, è necessario risolvere i prerequisiti mancanti e quindi fare di nuovo clic su **Controlla prerequisiti**.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-116">If a missing prerequisite is detected, you have to resolve the missing prerequisites, and then click **Check prerequisites again**.</span></span> <span data-ttu-id="2f3cc-117">Dopo aver soddisfatto tutti i prerequisiti, l'installazione verrà ripresa.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-117">Once all prerequisites are met, the installation will resume.</span></span>

     

5.  <span data-ttu-id="2f3cc-118">Per istruzioni specifiche su come e dove installare i modelli, vedere [come scaricare e distribuire i modelli di criteri di gruppo di MDOP (con estensione ADMX)](https://technet.microsoft.com/library/dn659707.aspx).</span><span class="sxs-lookup"><span data-stu-id="2f3cc-118">For specific steps about how and where to install the templates, see [How to Download and Deploy MDOP Group Policy (.admx) Templates](https://technet.microsoft.com/library/dn659707.aspx).</span></span>

6.  <span data-ttu-id="2f3cc-119">Dopo aver visualizzato la configurazione guidata amministrazione e monitoraggio di Microsoft BitLocker per le caratteristiche selezionate, fare clic su **fine** per chiudere la configurazione di mbam.</span><span class="sxs-lookup"><span data-stu-id="2f3cc-119">After the Microsoft BitLocker Administration and Monitoring Setup wizard displays installation pages for the selected features, click **Finish** to close MBAM Setup.</span></span>

## <span data-ttu-id="2f3cc-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f3cc-120">Related topics</span></span>


[<span data-ttu-id="2f3cc-121">Distribuzione degli oggetti Criteri di gruppo di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="2f3cc-121">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





