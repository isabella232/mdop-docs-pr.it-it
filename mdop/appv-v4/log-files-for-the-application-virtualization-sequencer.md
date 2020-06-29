---
title: File di registro per Application Virtualization Sequencer
description: File di registro per Application Virtualization Sequencer
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816216"
---
# <span data-ttu-id="9e74e-103">File di registro per Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="9e74e-103">Log Files for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="9e74e-104">I file di log per l'Application Virtualization (App-V) Sequencer contengono informazioni dettagliate sulla sequenziazione delle applicazioni e possono essere utili quando si verificano le funzionalità o quando si stanno risolvendo i problemi.</span><span class="sxs-lookup"><span data-stu-id="9e74e-104">The log files for the Application Virtualization (App-V) Sequencer provide detailed information about sequencing applications, and they can be helpful when you are verifying functionality or when you are troubleshooting issues.</span></span>

<span data-ttu-id="9e74e-105">La tabella seguente contiene informazioni sui file di log e sui relativi percorsi predefiniti, che vengono creati quando si usa Sequencer.</span><span class="sxs-lookup"><span data-stu-id="9e74e-105">The following table provides information about the log files and their default locations, which are created when using the Sequencer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9e74e-106">Nome file di log</span><span class="sxs-lookup"><span data-stu-id="9e74e-106">Log File Name</span></span></th>
<th align="left"><span data-ttu-id="9e74e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e74e-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9e74e-108">sft-seq-log.txt</span><span class="sxs-lookup"><span data-stu-id="9e74e-108">sft-seq-log.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e74e-109">Fornisce informazioni generali sulla sequenziazione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e74e-109">Provides general information about sequencing an application.</span></span> <span data-ttu-id="9e74e-110">Usare questo log come punto di partenza per la risoluzione dei problemi relativi agli errori del sequencer.</span><span class="sxs-lookup"><span data-stu-id="9e74e-110">Use this log as a starting point for troubleshooting Sequencer errors.</span></span></p>
<p><span data-ttu-id="9e74e-111">Percorso del file di log: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="9e74e-111">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="9e74e-112">[Valore token modello] Percorso del file di log App-V 4.6: <em> %windir%\Program Comuni\microsoft Application Virtualization Sequencer\Logs </em> [valore del token del modello]</span><span class="sxs-lookup"><span data-stu-id="9e74e-112">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="9e74e-113">sftbt.txt</span><span class="sxs-lookup"><span data-stu-id="9e74e-113">sftbt.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e74e-114">Fornisce informazioni sulle attività di riavvio del computer che si verificano durante il riavvio simulato del sequencer.</span><span class="sxs-lookup"><span data-stu-id="9e74e-114">Provides information about computer restart tasks that occur during the Sequencer’s simulated restart.</span></span></p>
<p><span data-ttu-id="9e74e-115">Percorso del file di log: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="9e74e-115">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="9e74e-116">[Valore token modello] Percorso del file di log App-V 4.6: <em> %windir%\Program Comuni\microsoft Application Virtualization Sequencer\Logs </em> [valore del token del modello]</span><span class="sxs-lookup"><span data-stu-id="9e74e-116">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="9e74e-117">SftCallBack.txt</span><span class="sxs-lookup"><span data-stu-id="9e74e-117">SftCallBack.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="9e74e-118">Fornisce informazioni generali sui processi usati durante la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="9e74e-118">Provides general information about processes used during sequencing.</span></span></p>
<p><span data-ttu-id="9e74e-119">Percorso del file di log: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="9e74e-119">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="9e74e-120">[Valore token modello] Percorso del file di log App-V 4.6: <em> %windir%\Program Comuni\microsoft Application Virtualization Sequencer\Logs </em> [valore del token del modello]</span><span class="sxs-lookup"><span data-stu-id="9e74e-120">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="9e74e-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9e74e-121">Related topics</span></span>


[<span data-ttu-id="9e74e-122">Riferimento per Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="9e74e-122">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

 

 





