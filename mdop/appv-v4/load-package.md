---
title: LOAD PACKAGE
description: LOAD PACKAGE
author: dansimp
ms.assetid: eb19116d-e5d0-445c-b2f0-3116a09384d7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 938aa92696c8530c91d9a7acaac42408de534edc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816236"
---
# <span data-ttu-id="b8567-103">LOAD PACKAGE</span><span class="sxs-lookup"><span data-stu-id="b8567-103">LOAD PACKAGE</span></span>


<span data-ttu-id="b8567-104">Carica il pacchetto specificato nella cache del file System.</span><span class="sxs-lookup"><span data-stu-id="b8567-104">Loads the specified package into the file system cache.</span></span>

`SFTMIME LOAD PACKAGE:package-name [/SFTPATH sft-pathname]                 [/LOG log-pathname | /CONSOLE | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b8567-105">Parametro</span><span class="sxs-lookup"><span data-stu-id="b8567-105">Parameter</span></span></th>
<th align="left"><span data-ttu-id="b8567-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8567-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8567-107">PACCHETTO: &lt; nome pacchetto&gt;</span><span class="sxs-lookup"><span data-stu-id="b8567-107">PACKAGE:&lt;package-name&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8567-108">Nome del pacchetto da caricare.</span><span class="sxs-lookup"><span data-stu-id="b8567-108">The name of the package to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8567-109">/SFTPATH &lt; SFT-PathName&gt;</span><span class="sxs-lookup"><span data-stu-id="b8567-109">/SFTPATH &lt;sft-pathname&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8567-110">Se specificato, il percorso di un file SFT da cui caricare.</span><span class="sxs-lookup"><span data-stu-id="b8567-110">If specified, the path to an SFT file to load from.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8567-111">/LOG</span><span class="sxs-lookup"><span data-stu-id="b8567-111">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8567-112">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="b8567-112">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b8567-113">/CONSOLE</span><span class="sxs-lookup"><span data-stu-id="b8567-113">/CONSOLE</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8567-114">Se specificato, l'output viene presentato nella finestra della console attiva (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="b8567-114">If specified, output is presented in the active console window (default).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8567-115">/GUI</span><span class="sxs-lookup"><span data-stu-id="b8567-115">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8567-116">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="b8567-116">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b8567-117">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="b8567-117">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b8567-118">/LOGU</span><span class="sxs-lookup"><span data-stu-id="b8567-118">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="b8567-119">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="b8567-119">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b8567-120">**Nota**  Se non viene specificato alcun SFTPATH, il client caricherà il pacchetto utilizzando il percorso configurato per l'uso, in base al file OSD, al valore della chiave del registro di sistema ApplicationSourceRoot o all'impostazione di OverrideURL.</span><span class="sxs-lookup"><span data-stu-id="b8567-120">**Note** If no SFTPATH is specified, the client will load the package by using the path it has been configured to use, based on the OSD file, the ApplicationSourceRoot registry key value, or the OverrideURL setting.</span></span>

<span data-ttu-id="b8567-121">Il comando **Carica pacchetto** esegue un caricamento sincrono e non sarà completo finché il pacchetto non viene caricato completamente o finché non incontra una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="b8567-121">The **LOAD PACKAGE** command performs a synchronous load and will not be complete until the package is fully loaded or until it encounters an error condition.</span></span>

 

## <span data-ttu-id="b8567-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8567-122">Related topics</span></span>


[<span data-ttu-id="b8567-123">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="b8567-123">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





