---
title: LOAD APP
description: LOAD APP
author: dansimp
ms.assetid: 7b727d0c-5423-419d-92ef-7ebbc6343e79
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 02bd6e35da898f5b34f7efc21cbc01a72d555b8d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816246"
---
# <span data-ttu-id="66cd0-103">LOAD APP</span><span class="sxs-lookup"><span data-stu-id="66cd0-103">LOAD APP</span></span>


<span data-ttu-id="66cd0-104">Carica l'applicazione specificata e tutte le altre applicazioni nel pacchetto nella cache del file System.</span><span class="sxs-lookup"><span data-stu-id="66cd0-104">Loads the specified application and all other applications in the package into the file system cache.</span></span>

<span data-ttu-id="66cd0-105">**Nota**  Il comando **carica app** avvia il processo di caricamento e viene visualizzata una barra di stato nell'area di notifica desktop.</span><span class="sxs-lookup"><span data-stu-id="66cd0-105">**Note** The **LOAD APP** command starts the load process and a progress bar is displayed in the Desktop Notification Area.</span></span> <span data-ttu-id="66cd0-106">Il comando termina immediatamente dopo l'avvio di questo processo, in modo che gli eventuali errori di caricamento vengano visualizzati nella stessa posizione.</span><span class="sxs-lookup"><span data-stu-id="66cd0-106">The command exits immediately after starting this process, so any load errors are displayed in the same location.</span></span> <span data-ttu-id="66cd0-107">Usare il comando **Carica pacchetto** se si vuole avviare il processo di caricamento dalla riga di comando senza usare l'area di notifica desktop.</span><span class="sxs-lookup"><span data-stu-id="66cd0-107">Use the **LOAD PACKAGE** command if you want to start the load process from the command line without using the Desktop Notification Area.</span></span>

 

`SFTMIME LOAD APP:application [/LOG log-pathname | /GUI]`

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="66cd0-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="66cd0-108">Parameter</span></span></th>
<th align="left"><span data-ttu-id="66cd0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66cd0-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66cd0-110">APP: &lt; applicazione&gt;</span><span class="sxs-lookup"><span data-stu-id="66cd0-110">APP:&lt;application&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="66cd0-111">Nome e versione (facoltativa) dell'applicazione da caricare.</span><span class="sxs-lookup"><span data-stu-id="66cd0-111">The name and version (optional) of the application to load.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="66cd0-112">/LOG</span><span class="sxs-lookup"><span data-stu-id="66cd0-112">/LOG</span></span></p></td>
<td align="left"><p><span data-ttu-id="66cd0-113">Se specificato, l'output viene registrato nel nome del percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="66cd0-113">If specified, output is logged to the specified path name.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66cd0-114">/GUI</span><span class="sxs-lookup"><span data-stu-id="66cd0-114">/GUI</span></span></p></td>
<td align="left"><p><span data-ttu-id="66cd0-115">Se specificato, l'output viene presentato in una finestra di dialogo di Windows.</span><span class="sxs-lookup"><span data-stu-id="66cd0-115">If specified, output is presented in a Windows dialog box.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="66cd0-116">Per la versione 4.6 è stata aggiunta l'opzione seguente.</span><span class="sxs-lookup"><span data-stu-id="66cd0-116">For version4.6, the following option has been added.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="66cd0-117">/LOGU</span><span class="sxs-lookup"><span data-stu-id="66cd0-117">/LOGU</span></span></p></td>
<td align="left"><p><span data-ttu-id="66cd0-118">Se specificato, l'output viene registrato nel nome del percorso specificato in formato UNICODE.</span><span class="sxs-lookup"><span data-stu-id="66cd0-118">If specified, output is logged to the specified path name in UNICODE format.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="66cd0-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66cd0-119">Related topics</span></span>


[<span data-ttu-id="66cd0-120">Informazioni di riferimento sui comandi di SFTMIME</span><span class="sxs-lookup"><span data-stu-id="66cd0-120">SFTMIME Command Reference</span></span>](sftmime--command-reference.md)

 

 





