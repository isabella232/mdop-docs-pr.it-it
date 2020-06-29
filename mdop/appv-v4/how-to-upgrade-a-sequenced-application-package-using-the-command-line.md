---
title: Come aggiornare un pacchetto di applicazione sequenziata usando la riga di comando
description: Come aggiornare un pacchetto di applicazione sequenziata usando la riga di comando
author: dansimp
ms.assetid: 682fac46-c71d-4731-831b-81bfd5032764
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eade2ced43852419176f635918f0a6b7c3444aee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816486"
---
# <span data-ttu-id="96f0e-103">Come aggiornare un pacchetto di applicazione sequenziata usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="96f0e-103">How to Upgrade a Sequenced Application Package Using the Command Line</span></span>


<span data-ttu-id="96f0e-104">Usare la procedura seguente per aggiornare un'applicazione virtuale tramite una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="96f0e-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span> <span data-ttu-id="96f0e-105">Quando si aggiorna un pacchetto di applicazione virtuale esistente tramite la riga di comando, la versione originale del file SFT viene eliminata.</span><span class="sxs-lookup"><span data-stu-id="96f0e-105">When you upgrade an existing virtual application package by using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="96f0e-106">È consigliabile eseguire il backup del file SFT associato prima di aggiornare il pacchetto tramite la riga di comando.</span><span class="sxs-lookup"><span data-stu-id="96f0e-106">You should back up the associated .sft file before upgrading the package by using the command line.</span></span>

**<span data-ttu-id="96f0e-107">Per aggiornare un'applicazione virtuale</span><span class="sxs-lookup"><span data-stu-id="96f0e-107">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="96f0e-108">Nel computer in cui è in esecuzione Application Virtualization (App-V) Sequencer, per aprire il prompt dei comandi, selezionare **Start**, **Esegui**e digitare **cmd**.</span><span class="sxs-lookup"><span data-stu-id="96f0e-108">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="96f0e-109">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="96f0e-109">Click **OK**.</span></span>

2.  <span data-ttu-id="96f0e-110">Al prompt dei comandi specificare il percorso in cui è installato App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="96f0e-110">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="96f0e-111">Ad esempio, al prompt dei comandi digitare quanto segue: **CD C:\\Programmi \\Programmi\\microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="96f0e-111">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="96f0e-112">Al prompt dei comandi digitare il comando seguente, sostituendo il testo tra virgolette con i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="96f0e-112">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="96f0e-113">Nota</span><span class="sxs-lookup"><span data-stu-id="96f0e-113">Note</span></span>**  
    <span data-ttu-id="96f0e-114">Puoi specificare parametri aggiuntivi usando la riga di comando, a seconda della complessità dell'applicazione che stai aggiornando.</span><span class="sxs-lookup"><span data-stu-id="96f0e-114">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="96f0e-115">Per un elenco completo dei parametri disponibili per l'uso con l'App-V Sequencer, Vedi [parametri della riga di comando](command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="96f0e-115">For a complete list of parameters that are available for use with the App-V Sequencer, see [Command-Line Parameters](command-line-parameters.md).</span></span>



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="96f0e-116">Premere **invio**.</span><span class="sxs-lookup"><span data-stu-id="96f0e-116">Press **Enter**.</span></span>

## <span data-ttu-id="96f0e-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96f0e-117">Related topics</span></span>


[<span data-ttu-id="96f0e-118">Come gestire le applicazioni virtuali usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="96f0e-118">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









