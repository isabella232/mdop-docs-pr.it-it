---
title: Come aprire un'applicazione sequenziata usando la riga di comando
description: Come aprire un'applicazione sequenziata usando la riga di comando
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816916"
---
# <span data-ttu-id="26f5b-103">Come aprire un'applicazione sequenziata usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="26f5b-103">How to Open a Sequenced Application Using the Command Line</span></span>


<span data-ttu-id="26f5b-104">È possibile aprire pacchetti di applicazioni virtuali tramite la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="26f5b-104">You can open virtual application packages using the command line.</span></span> <span data-ttu-id="26f5b-105">È necessario eseguire il prompt **cmd** come amministratore.</span><span class="sxs-lookup"><span data-stu-id="26f5b-105">You must run the **cmd** prompt as an administrator.</span></span>

<span data-ttu-id="26f5b-106">Usare la procedura seguente per aprire i pacchetti di applicazioni sequenziate tramite la riga di comando</span><span class="sxs-lookup"><span data-stu-id="26f5b-106">Use the following procedure to open sequenced application packages using the command line</span></span>

**<span data-ttu-id="26f5b-107">Per aprire un'applicazione sequenziata tramite la riga di comando</span><span class="sxs-lookup"><span data-stu-id="26f5b-107">To open a sequenced application using the command line</span></span>**

1.  <span data-ttu-id="26f5b-108">Per aprire il prompt dei comandi, fare clic sul pulsante **Start**e scegliere **Esegui**, digitare **cmd**e quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="26f5b-108">To open the command prompt, click **Start**, and select **Run**, type **cmd**, and click **OK**.</span></span>

2.  <span data-ttu-id="26f5b-109">Al prompt dei comandi digitare **cd\\** e specificare il percorso della directory in cui è installato Sequencer e quindi premere **INVIO.**</span><span class="sxs-lookup"><span data-stu-id="26f5b-109">At a command prompt, type **cd\\** and specify the path to the directory where the Sequencer is installed and then press **Enter.**</span></span>

3.  <span data-ttu-id="26f5b-110">Al prompt dei comandi digitare il comando seguente, sostituendo il testo in corsivo con i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="26f5b-110">At the command prompt, type the following command, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="26f5b-111">SFTSequencer/OPEN:*"specifica il file con estensione SPRJ da aprire"*</span><span class="sxs-lookup"><span data-stu-id="26f5b-111">SFTSequencer /OPEN:*”specifies the .sprj file to open"*</span></span>

    <span data-ttu-id="26f5b-112">Premere **invio**.</span><span class="sxs-lookup"><span data-stu-id="26f5b-112">Press **Enter**.</span></span>

4.  <span data-ttu-id="26f5b-113">È anche possibile specificare i parametri facoltativi seguenti.</span><span class="sxs-lookup"><span data-stu-id="26f5b-113">You can also specify the following optional parameters.</span></span> <span data-ttu-id="26f5b-114">Al prompt dei comandi digitare i comandi seguenti, sostituendo il testo in corsivo con i valori:</span><span class="sxs-lookup"><span data-stu-id="26f5b-114">At the command prompt, type the following commands, replacing the italicized text with your values:</span></span>

    <span data-ttu-id="26f5b-115">/PACKAGENAME: "*specifica il nome del pacchetto"*</span><span class="sxs-lookup"><span data-stu-id="26f5b-115">/PACKAGENAME:"*specifies the package name"*</span></span>

    <span data-ttu-id="26f5b-116">/MSI-specifica la generazione di un programma di installazione di Microsoft Windows associato.</span><span class="sxs-lookup"><span data-stu-id="26f5b-116">/MSI - specifies generating an associated Microsoft Windows Installer.</span></span>

    <span data-ttu-id="26f5b-117">/COMPRESS: specifica se il pacchetto verrà compresso.</span><span class="sxs-lookup"><span data-stu-id="26f5b-117">/COMPRESS – specifies if the package will be compressed.</span></span> <span data-ttu-id="26f5b-118">Per impostazione predefinita, i pacchetti non vengono compressi.</span><span class="sxs-lookup"><span data-stu-id="26f5b-118">By default, packages are not compressed.</span></span>

    <span data-ttu-id="26f5b-119">Premere **invio**.</span><span class="sxs-lookup"><span data-stu-id="26f5b-119">Press **Enter**.</span></span>

    <span data-ttu-id="26f5b-120">**Nota**  Se il pacchetto di installazione o di Windows Installer ha un'interfaccia utente grafica, verrà visualizzato dopo aver specificato i parametri della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="26f5b-120">**Note** If the installer or Windows Installer package has a graphical user interface, it will be displayed after you specify the command-line parameters.</span></span>

     

## <span data-ttu-id="26f5b-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26f5b-121">Related topics</span></span>


[<span data-ttu-id="26f5b-122">Come gestire le applicazioni virtuali usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="26f5b-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





