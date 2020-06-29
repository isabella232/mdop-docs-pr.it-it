---
title: Come eseguire l'aggiornamento di un pacchetto
description: Come eseguire l'aggiornamento di un pacchetto
author: dansimp
ms.assetid: 831c7556-6f6c-4b3a-aefb-26889094dc1a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0a9b3eca2c996337d79e551784818a421f495316
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816505"
---
# <span data-ttu-id="abd54-103">Come eseguire l'aggiornamento di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="abd54-103">How to Upgrade a Package</span></span>


<span data-ttu-id="abd54-104">Il processo di aggiornamento automatico è uguale a quello per l'aggiunta di una versione del pacchetto nella console di gestione di Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="abd54-104">The process for an automatic upgrade is the same as for adding a package version in the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="abd54-105">Viene eseguito un aggiornamento automatico quando si risequenzia l'applicazione in un pacchetto esistente.</span><span class="sxs-lookup"><span data-stu-id="abd54-105">An automatic upgrade is performed when you resequence the application in an existing package.</span></span> <span data-ttu-id="abd54-106">È quindi possibile aggiungere la nuova versione ai server per lo streaming.</span><span class="sxs-lookup"><span data-stu-id="abd54-106">Then you can add this new version to your servers for streaming.</span></span>

<span data-ttu-id="abd54-107">Quando si aggiorna un pacchetto con una nuova versione, è possibile abbandonare la versione esistente o eliminarla e lasciarla solo quella più recente.</span><span class="sxs-lookup"><span data-stu-id="abd54-107">When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="abd54-108">Potrebbe essere necessario abbandonare la versione precedente per la compatibilità con i documenti legacy o in modo da poter testare la nuova versione prima di renderla disponibile per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="abd54-108">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

**<span data-ttu-id="abd54-109">Per aggiornare automaticamente un pacchetto</span><span class="sxs-lookup"><span data-stu-id="abd54-109">To upgrade a package automatically</span></span>**

1.  <span data-ttu-id="abd54-110">Copiare il nuovo file SFT nella cartella contenuto del server Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="abd54-110">Copy the new SFT file to the Application Virtualization Server's content folder.</span></span>

    <span data-ttu-id="abd54-111">**Nota**  Se la risequenziazione non aggiunge caratteristiche che hanno modificato i file OSD (Open Software Descriptor), Icon (ICO) o Sequencer Project (SPRJ), non è necessario copiarli.</span><span class="sxs-lookup"><span data-stu-id="abd54-111">**Note** If resequencing did not add features that changed the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="abd54-112">Puoi includere questi file se vuoi che tutti questi file visualizzino la stessa data.</span><span class="sxs-lookup"><span data-stu-id="abd54-112">You can include these files if you want all these files to display the same date.</span></span>

     

2.  <span data-ttu-id="abd54-113">Nel riquadro sinistro della console di gestione di Application Virtualization Server espandere **pacchetti**.</span><span class="sxs-lookup"><span data-stu-id="abd54-113">In left pane of the Application Virtualization Server Management Console, expand **Packages**.</span></span>

3.  <span data-ttu-id="abd54-114">Fare clic con il pulsante destro del mouse sul pacchetto che si vuole aggiornare e scegliere **Aggiungi versione**.</span><span class="sxs-lookup"><span data-stu-id="abd54-114">Right-click the package you want to upgrade, and select **Add Version**.</span></span>

4.  <span data-ttu-id="abd54-115">Nella finestra di dialogo **Aggiungi versione pacchetto** cercare o digitare il nome del percorso completo per la nuova versione dell'applicazione nel **percorso completo per il campo file** .</span><span class="sxs-lookup"><span data-stu-id="abd54-115">In the **Add Package Version** dialog box, browse for or type the full path name for the new application version in the **Full Path for the file** field.</span></span> <span data-ttu-id="abd54-116">Questo deve essere un file SFT.</span><span class="sxs-lookup"><span data-stu-id="abd54-116">This must be an SFT file.</span></span>

5.  <span data-ttu-id="abd54-117">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="abd54-117">Click **Next**.</span></span>

6.  <span data-ttu-id="abd54-118">La finestra di dialogo **Riepilogo** Mostra il percorso del file e chiede di copiare il file se non è già stato fatto.</span><span class="sxs-lookup"><span data-stu-id="abd54-118">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="abd54-119">Dopo aver verificato le informazioni, fare clic su **fine** .</span><span class="sxs-lookup"><span data-stu-id="abd54-119">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="abd54-120">La nuova versione è ora completa e pronta per il flusso.</span><span class="sxs-lookup"><span data-stu-id="abd54-120">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="abd54-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="abd54-121">Related topics</span></span>


[<span data-ttu-id="abd54-122">Come gestire i pacchetti in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="abd54-122">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





