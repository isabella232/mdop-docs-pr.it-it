---
title: Come aggiungere una versione del pacchetto
description: Come aggiungere una versione del pacchetto
author: dansimp
ms.assetid: dbb829c1-e5cb-4a2f-bc17-9a9bb50c671c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a60252e8b43af61ad548df30a93d8fbc9bae0cb7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821405"
---
# <span data-ttu-id="49f22-103">Come aggiungere una versione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="49f22-103">How to Add a Package Version</span></span>


<span data-ttu-id="49f22-104">Quando si risequenzia un pacchetto in Application Virtualization Server Management Console, è possibile usare la procedura seguente per aggiungere la nuova versione ai server per lo streaming.</span><span class="sxs-lookup"><span data-stu-id="49f22-104">In the Application Virtualization Server Management Console, when you resequence a package, you can use the following procedure to add the new version to your servers for streaming.</span></span>

<span data-ttu-id="49f22-105">**Nota**  Quando si aggiorna un pacchetto con una nuova versione, è possibile abbandonare la versione esistente o eliminarla e lasciarla solo quella più recente.</span><span class="sxs-lookup"><span data-stu-id="49f22-105">**Note** When you upgrade a package with a new version, you can leave the existing version in place or delete it and leave only the newest one.</span></span> <span data-ttu-id="49f22-106">Potrebbe essere necessario abbandonare la versione precedente per la compatibilità con i documenti legacy o in modo da poter testare la nuova versione prima di renderla disponibile per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="49f22-106">You might want to leave the old version in place for compatibility with legacy documents or so that you can test the new version before making it available to all users.</span></span>

 

**<span data-ttu-id="49f22-107">Per aggiungere una versione del pacchetto</span><span class="sxs-lookup"><span data-stu-id="49f22-107">To add a package version</span></span>**

1.  <span data-ttu-id="49f22-108">Copiare il nuovo file SFT nella cartella contenuto del server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="49f22-108">Copy the new SFT file to the application server's content folder.</span></span> <span data-ttu-id="49f22-109">Se la risequenziazione non è stata aggiunta alle modifiche apportate ai file OSD (Open Software Descriptor), Icon (ICO) o Sequencer Project (SPRJ), non è necessario copiarli.</span><span class="sxs-lookup"><span data-stu-id="49f22-109">If resequencing did not add changes to the Open Software Descriptor (OSD), icon (ICO), or Sequencer Project (SPRJ) files, you do not need to copy those.</span></span> <span data-ttu-id="49f22-110">Puoi includere questi file se vuoi che tutti i file visualizzino la stessa data.</span><span class="sxs-lookup"><span data-stu-id="49f22-110">You can include those files if you want all the files to display the same date.</span></span>

2.  <span data-ttu-id="49f22-111">Nel riquadro sinistro della console di gestione di Application Virtualization Server espandere il nodo **pacchetti** .</span><span class="sxs-lookup"><span data-stu-id="49f22-111">In left pane of the Application Virtualization Server Management Console, expand the **Packages** node.</span></span>

3.  <span data-ttu-id="49f22-112">Fare clic con il pulsante destro del mouse sul pacchetto che si vuole aggiornare e scegliere **Aggiungi versione**.</span><span class="sxs-lookup"><span data-stu-id="49f22-112">Right-click the package you want to upgrade, and choose **Add Version**.</span></span>

4.  <span data-ttu-id="49f22-113">Nella finestra di dialogo **Aggiungi versione pacchetto** cercare o digitare il nome del percorso per il nuovo file dell'applicazione nel campo **percorso completo per il file del pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="49f22-113">In the **Add Package Version** dialog box, browse for or type the path name for the new application file in the **Full path for package file** field.</span></span> <span data-ttu-id="49f22-114">Questo deve essere un file SFT.</span><span class="sxs-lookup"><span data-stu-id="49f22-114">This must be an SFT file.</span></span>

5.  <span data-ttu-id="49f22-115">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="49f22-115">Click **Next**.</span></span>

6.  <span data-ttu-id="49f22-116">La finestra di dialogo **Riepilogo** Mostra il percorso del file e chiede di copiare il file se non è già stato fatto.</span><span class="sxs-lookup"><span data-stu-id="49f22-116">The **Summary** dialog box shows the file location and prompts you to copy the file there if you have not already done so.</span></span> <span data-ttu-id="49f22-117">Dopo aver verificato le informazioni, fare clic su **fine** .</span><span class="sxs-lookup"><span data-stu-id="49f22-117">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="49f22-118">La nuova versione è ora completa e pronta per il flusso.</span><span class="sxs-lookup"><span data-stu-id="49f22-118">The new version is now complete and ready to stream.</span></span>

## <span data-ttu-id="49f22-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49f22-119">Related topics</span></span>


[<span data-ttu-id="49f22-120">Come eliminare un pacchetto</span><span class="sxs-lookup"><span data-stu-id="49f22-120">How to Delete a Package</span></span>](how-to-delete-a-packageserver.md)

[<span data-ttu-id="49f22-121">Come gestire i pacchetti in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="49f22-121">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





