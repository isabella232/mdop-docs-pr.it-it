---
title: Come modificare i sistemi operativi associati a un file di Windows Installer esistente
description: Come modificare i sistemi operativi associati a un file di Windows Installer esistente
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816955"
---
# <span data-ttu-id="ae509-103">Come modificare i sistemi operativi associati a un file di Windows Installer esistente</span><span class="sxs-lookup"><span data-stu-id="ae509-103">How to Modify the Operating Systems Associated With an Existing Windows Installer File</span></span>


<span data-ttu-id="ae509-104">Usare la procedura seguente per modificare le versioni del sistema operativo associate a un file di Windows Installer (**MSI**) esistente creato tramite App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="ae509-104">Use the following procedure to modify the operating system versions associated with an existing Windows Installer (**MSI**) file that was created by using the App-V Sequencer.</span></span>

**<span data-ttu-id="ae509-105">Per modificare i sistemi operativi di un file di Windows Installer esistente</span><span class="sxs-lookup"><span data-stu-id="ae509-105">To modify the operating systems of an existing Windows Installer file</span></span>**

1.  <span data-ttu-id="ae509-106">Installare App-V Sequencer in un computer nell'ambiente in cui è installato solo il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ae509-106">Install the App-V Sequencer on a computer in your environment that has only the operating system installed.</span></span> <span data-ttu-id="ae509-107">In alternativa, è possibile installare il sequencer in un computer che gestisce un ambiente virtuale, ad esempio Microsoft Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="ae509-107">Alternatively, you can install the Sequencer on a computer running a virtual environment—for example, Microsoft Virtual PC.</span></span> <span data-ttu-id="ae509-108">Questo metodo è utile perché è più semplice mantenere un ambiente di sequenziazione pulito che è possibile riutilizzare con una configurazione aggiuntiva minima.</span><span class="sxs-lookup"><span data-stu-id="ae509-108">This method is useful because it is easier to maintain a clean sequencing environment that you can reuse with minimal additional configuration.</span></span> <span data-ttu-id="ae509-109">Per altre informazioni sull'installazione di App-V Sequencer, vedere [come installare Sequencer](how-to-install-the-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="ae509-109">For more information about installing the App-V Sequencer, see [How to Install the Sequencer](how-to-install-the-sequencer.md).</span></span>

2.  <span data-ttu-id="ae509-110">Copiare l'intero pacchetto di applicazione virtuale che contiene il file di Windows Installer che si vuole modificare nel computer in cui è in uso il sequencer.</span><span class="sxs-lookup"><span data-stu-id="ae509-110">Copy the entire virtual application package that contains the Windows Installer file you want to modify to the computer running the Sequencer.</span></span>

3.  <span data-ttu-id="ae509-111">Per modificare il file di Windows Installer, aprire la console sequencer, selezionare **pacchetto**  /  **aperto**e quindi passare al percorso in cui è stato salvato il pacchetto di applicazione virtuale associato al file di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ae509-111">To modify the Windows Installer file, open the Sequencer console, select **Package** / **Open**, and then browse to the location where the virtual application package associated with the Windows Installer file is saved.</span></span>

4.  <span data-ttu-id="ae509-112">Per aggiungere o rimuovere sistemi operativi, selezionare la scheda **distribuzione** nella console Sequencer.</span><span class="sxs-lookup"><span data-stu-id="ae509-112">To add or remove operating systems, select the **Deployment** tab in the Sequencer console.</span></span> <span data-ttu-id="ae509-113">Per specificare altri sistemi operativi che verranno associati al file di Windows Installer, selezionare il sistema operativo desiderato e quindi fare clic sulla freccia che punta al controllo elenco del sistema operativo **selezionato** .</span><span class="sxs-lookup"><span data-stu-id="ae509-113">To specify additional operating systems that will be associated with the Windows Installer file, select the desired operating system, and then click the arrow that points to the **Selected** operating system list control.</span></span>

    <span data-ttu-id="ae509-114">Per rimuovere un'associazione di sistema operativo, selezionare il sistema operativo che si vuole rimuovere e quindi fare clic sulla freccia che punta al controllo elenco sistema operativo **disponibile** .</span><span class="sxs-lookup"><span data-stu-id="ae509-114">To remove an operating system association, select the operating system you want to remove, and then click the arrow that points to the **Available** operating system list control.</span></span>

5.  <span data-ttu-id="ae509-115">Per creare un nuovo Windows Installer che verrà associato al pacchetto di applicazione virtuale, selezionare **Genera pacchetto di Microsoft Windows Installer (MSI)**.</span><span class="sxs-lookup"><span data-stu-id="ae509-115">To create a new Windows Installer that will be associated with the virtual application package, select **Generate Microsoft Windows Installer (MSI) Package**.</span></span> <span data-ttu-id="ae509-116">In alternativa, è possibile selezionare **strumenti**per  /  **creare MSI**.</span><span class="sxs-lookup"><span data-stu-id="ae509-116">Alternatively, you can select **Tools** / **Create MSI**.</span></span>

    <span data-ttu-id="ae509-117">**Nota**  Se si seleziona **strumenti** / **Crea MSI** per creare un nuovo file di Windows Installer, è possibile ignorare il **passaggio 6** di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="ae509-117">**Note** If you select **Tools** / **Create MSI** to create a new Windows Installer file, you can skip **Step 6** of this procedure.</span></span>

     

6.  <span data-ttu-id="ae509-118">Per salvare il pacchetto di applicazione virtuale, **Package**selezionare  /  **Salva**pacchetto.</span><span class="sxs-lookup"><span data-stu-id="ae509-118">To save the virtual application package, select **Package** / **Save**.</span></span>

## <span data-ttu-id="ae509-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ae509-119">Related topics</span></span>


[<span data-ttu-id="ae509-120">Attività per Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="ae509-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)

 

 





