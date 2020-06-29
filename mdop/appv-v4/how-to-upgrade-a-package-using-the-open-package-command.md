---
title: Come aggiornare un pacchetto usando il comando Apri pacchetto
description: Come aggiornare un pacchetto usando il comando Apri pacchetto
author: dansimp
ms.assetid: 67c10440-de8a-4547-a34b-f83206d0cc3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cca438fe90373e8f934d1d790246544cdf46fa18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816516"
---
# <span data-ttu-id="b996e-103">Come aggiornare un pacchetto usando il comando Apri pacchetto</span><span class="sxs-lookup"><span data-stu-id="b996e-103">How to Upgrade a Package Using the Open Package Command</span></span>


<span data-ttu-id="b996e-104">Usare il comando Apri pacchetto per aggiornare o applicare un aggiornamento a un pacchetto di applicazione sequenziale.</span><span class="sxs-lookup"><span data-stu-id="b996e-104">Use the Open Package command to upgrade or apply an update to a sequenced application package.</span></span> <span data-ttu-id="b996e-105">Quando si aggiorna un pacchetto di applicazione virtuale esistente tramite la riga di comando, la versione originale del file SFT viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="b996e-105">When you upgrade an existing virtual application package using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="b996e-106">È consigliabile eseguire il backup del file SFT associato prima di aggiornare il pacchetto tramite la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b996e-106">You should backup the associated .sft file before upgrading the package using the command line.</span></span>

**<span data-ttu-id="b996e-107">Per aggiornare un pacchetto tramite il comando Apri pacchetto</span><span class="sxs-lookup"><span data-stu-id="b996e-107">To upgrade a package using the Open Package command</span></span>**

1.  <span data-ttu-id="b996e-108">Per aprire il pacchetto che verrà aggiornato, nella console di Application Virtualization (App-V) selezionare **file**, **aprire il pacchetto per l'aggiornamento**.</span><span class="sxs-lookup"><span data-stu-id="b996e-108">To open the package that will be upgraded, in the Application Virtualization (App-V) console select **File**, **Open Package for Upgrade**.</span></span> <span data-ttu-id="b996e-109">Nella finestra di dialogo **Apri** selezionare il pacchetto che verrà aggiornato.</span><span class="sxs-lookup"><span data-stu-id="b996e-109">In the **Open** dialog box, select the package that will be upgraded.</span></span>

2.  <span data-ttu-id="b996e-110">Per avviare la **sequenziazione** guidata, selezionare **strumenti**, **sequenziazione guidata**.</span><span class="sxs-lookup"><span data-stu-id="b996e-110">To start the **Sequencing** wizard, select **Tools**, **Sequencing Wizard**.</span></span> <span data-ttu-id="b996e-111">Completare la procedura guidata applicando le modifiche alla configurazione, per salvare la nuova applicazione sequenziata, selezionare **file**, **Salva**.</span><span class="sxs-lookup"><span data-stu-id="b996e-111">Complete the wizard applying the configuration changes, to save the new sequenced application, select **File**, **Save**.</span></span>

3.  <span data-ttu-id="b996e-112">Per aggiungere il numero di versione al nome del pacchetto, nella console sequencer selezionare **strumenti**, **Opzioni**.</span><span class="sxs-lookup"><span data-stu-id="b996e-112">To append the version number to the package name, in the Sequencer console, select **Tools**, **Options**.</span></span> <span data-ttu-id="b996e-113">Selezionare **Accoda versione pacchetto a nomefile**.</span><span class="sxs-lookup"><span data-stu-id="b996e-113">Select **Append Package Version to Filename**.</span></span> <span data-ttu-id="b996e-114">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="b996e-114">Click **OK**.</span></span>

    <span data-ttu-id="b996e-115">**Importante**  L'aggiornamento del nome file con la versione del pacchetto è essenziale per completare correttamente l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b996e-115">**Important** Updating the file name with the package version is essential to successfully completing the upgrade.</span></span>

     

## <span data-ttu-id="b996e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b996e-116">Related topics</span></span>


[<span data-ttu-id="b996e-117">Come gestire le applicazioni virtuali usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="b996e-117">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





