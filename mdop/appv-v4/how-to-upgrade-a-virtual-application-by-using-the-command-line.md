---
title: Come eseguire l'aggiornamento di un'applicazione virtuale con la riga di comando
description: Come eseguire l'aggiornamento di un'applicazione virtuale con la riga di comando
author: dansimp
ms.assetid: 83c97767-6ea1-42aa-b411-ccc9fa61cf81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8612deb31a1692dd85cfee88ca4b18cbc5ac2ab2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816465"
---
# <span data-ttu-id="6614d-103">Come eseguire l'aggiornamento di un'applicazione virtuale con la riga di comando</span><span class="sxs-lookup"><span data-stu-id="6614d-103">How to Upgrade a Virtual Application by Using the Command Line</span></span>


<span data-ttu-id="6614d-104">Usare la procedura seguente per aggiornare un'applicazione virtuale tramite una riga di comando.</span><span class="sxs-lookup"><span data-stu-id="6614d-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span>

**<span data-ttu-id="6614d-105">Per aggiornare un'applicazione virtuale</span><span class="sxs-lookup"><span data-stu-id="6614d-105">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="6614d-106">Nel computer in cui è in esecuzione Application Virtualization (App-V) Sequencer, per aprire il prompt dei comandi, selezionare **Start**, **Esegui**e digitare **cmd**.</span><span class="sxs-lookup"><span data-stu-id="6614d-106">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="6614d-107">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="6614d-107">Click **OK**.</span></span>

2.  <span data-ttu-id="6614d-108">Al prompt dei comandi specificare il percorso in cui è installato App-V Sequencer.</span><span class="sxs-lookup"><span data-stu-id="6614d-108">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="6614d-109">Ad esempio, al prompt dei comandi digitare quanto segue: **CD C:\\Programmi \\Programmi\\microsoft Application Virtualization Sequencer**.</span><span class="sxs-lookup"><span data-stu-id="6614d-109">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="6614d-110">Al prompt dei comandi digitare il comando seguente, sostituendo il testo tra virgolette con i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6614d-110">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="6614d-111">Nota</span><span class="sxs-lookup"><span data-stu-id="6614d-111">Note</span></span>**  
    <span data-ttu-id="6614d-112">Puoi specificare parametri aggiuntivi usando la riga di comando, a seconda della complessità dell'applicazione che stai aggiornando.</span><span class="sxs-lookup"><span data-stu-id="6614d-112">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="6614d-113">Per un elenco completo dei parametri disponibili per l'uso con l'App-V Sequencer, Vedi [parametri della riga di comando sequencer](sequencer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6614d-113">For a complete list of parameters that are available for use with the App-V Sequencer, see [Sequencer Command-Line Parameters](sequencer-command-line-parameters.md).</span></span>



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



4. <span data-ttu-id="6614d-114">Premere **invio**.</span><span class="sxs-lookup"><span data-stu-id="6614d-114">Press **Enter**.</span></span>

## <span data-ttu-id="6614d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6614d-115">Related topics</span></span>


[<span data-ttu-id="6614d-116">Come creare o aggiornare le applicazioni virtuali tramite App-V Sequencer</span><span class="sxs-lookup"><span data-stu-id="6614d-116">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[<span data-ttu-id="6614d-117">Codici di errore della riga di comando di Sequencer</span><span class="sxs-lookup"><span data-stu-id="6614d-117">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

[<span data-ttu-id="6614d-118">Parametri della riga di comando di Sequencer</span><span class="sxs-lookup"><span data-stu-id="6614d-118">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)









