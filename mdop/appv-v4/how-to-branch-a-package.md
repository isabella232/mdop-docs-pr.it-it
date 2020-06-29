---
title: Come creare una diramazione di un pacchetto
description: Come creare una diramazione di un pacchetto
author: dansimp
ms.assetid: bfe46a8a-f0ee-4a71-9e9c-64ac08aac9c1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2de36fae1a09aeae4d1b7b21ebe00f683e3b3693
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818126"
---
# <span data-ttu-id="34bf1-103">Come creare una diramazione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="34bf1-103">How to Branch a Package</span></span>


<span data-ttu-id="34bf1-104">Usare questa procedura per modificare un pacchetto di applicazione sequenziale esistente in modo da poterlo eseguire affiancato al pacchetto di applicazione sequenziata originale.</span><span class="sxs-lookup"><span data-stu-id="34bf1-104">Use this procedure to modify an existing sequenced application package so you can run it side-by-side with the original sequenced application package.</span></span> <span data-ttu-id="34bf1-105">Questo processo è denominato branching.</span><span class="sxs-lookup"><span data-stu-id="34bf1-105">This process is called branching.</span></span> <span data-ttu-id="34bf1-106">Quando si dirama un pacchetto di applicazione virtuale, è possibile eseguire due versioni dello stesso pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34bf1-106">When you branch a virtual application package you are able to run two versions of the same package.</span></span> <span data-ttu-id="34bf1-107">Ad esempio, puoi applicare un Service Pack a un pacchetto esistente ed eseguirlo affiancato con il pacchetto di applicazione virtuale sequenziato originale.</span><span class="sxs-lookup"><span data-stu-id="34bf1-107">For example, you can apply a service pack to an existing package, and run it side-by-side with the original sequenced virtual application package.</span></span>

<span data-ttu-id="34bf1-108">Usare la procedura seguente per creare un branching di un pacchetto di applicazione virtuale sequenziato.</span><span class="sxs-lookup"><span data-stu-id="34bf1-108">Use the following procedure to branch a sequenced virtual application package.</span></span>

**<span data-ttu-id="34bf1-109">Per creare una succursale di un pacchetto di applicazione virtuale sequenziato</span><span class="sxs-lookup"><span data-stu-id="34bf1-109">To branch a sequenced virtual application package</span></span>**

1.  <span data-ttu-id="34bf1-110">Aprire il sequencer di Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="34bf1-110">Open the Microsoft Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="34bf1-111">Per specificare la directory di destinazione che contiene il pacchetto (con estensione SPRJ) che si vuole diramare selezionare **file**, **aprire**.</span><span class="sxs-lookup"><span data-stu-id="34bf1-111">To specify the destination directory that contains the package (.sprj) you want to branch select **File**, **Open**.</span></span>

2.  <span data-ttu-id="34bf1-112">Passare alla directory che contiene l'applicazione sequenziata che si prevede di diramazione e fare clic su **Apri**.</span><span class="sxs-lookup"><span data-stu-id="34bf1-112">Navigate to the directory that contains the sequenced application you plan to branch and click **Open**.</span></span>

3.  <span data-ttu-id="34bf1-113">Per salvare una copia del pacchetto, in App-V Sequencer selezionare **file**, **Salva con nome**.</span><span class="sxs-lookup"><span data-stu-id="34bf1-113">To save a copy of the package, in the App-V Sequencer, select **File**, **Save As**.</span></span> <span data-ttu-id="34bf1-114">Specifica un nuovo nome univoco e specifica una nuova directory radice del pacchetto univoco per la copia del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34bf1-114">Specify a new, unique name, and specify a new unique package root directory for the copy of the package.</span></span> <span data-ttu-id="34bf1-115">Fare clic su **Save**.</span><span class="sxs-lookup"><span data-stu-id="34bf1-115">Click **Save**.</span></span>

    **<span data-ttu-id="34bf1-116">Importante</span><span class="sxs-lookup"><span data-stu-id="34bf1-116">Important</span></span>**  
    <span data-ttu-id="34bf1-117">Devi specificare un nuovo nome di pacchetto o sovrascrivere la versione esistente del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="34bf1-117">You must specify a new package name or you will overwrite the existing version of the package.</span></span>



~~~
The sequencer will automatically generate new GUID files for the new package. The version number associated with the package will also be automatically appended to the OSD file name.
~~~

4. <span data-ttu-id="34bf1-118">Dopo aver salvato la nuova versione, è possibile applicare le modifiche necessarie alla configurazione e salvare i file ICO, OSD, SFT e SPRJ associati per correggere la posizione nel server Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="34bf1-118">After you save the new version you can apply the required configuration changes and save the associated ICO, OSD, SFT, and SPRJ files to correct location on the Application Virtualization (App-V) server.</span></span>

## <span data-ttu-id="34bf1-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="34bf1-119">Related topics</span></span>


[<span data-ttu-id="34bf1-120">Attività per Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="34bf1-120">Tasks for the Application Virtualization Sequencer</span></span>](tasks-for-the-application-virtualization-sequencer.md)








