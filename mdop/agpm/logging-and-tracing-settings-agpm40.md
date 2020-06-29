---
title: Impostazioni di registrazione e traccia
description: Impostazioni di registrazione e traccia
author: dansimp
ms.assetid: 66d03306-80d8-4132-bf71-2827157b1fc9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c58da00e7030c5e4cb3e4d5c4e5bbffa0c754233
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820596"
---
# <span data-ttu-id="c99a2-103">Impostazioni di registrazione e traccia</span><span class="sxs-lookup"><span data-stu-id="c99a2-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="c99a2-104">Le impostazioni del modello amministrativo per la gestione avanzata dei criteri di gruppo consentono di configurare in modo centralizzato le opzioni di registrazione e traccia per i server e i client di Advanced Group Policy in cui viene applicato un oggetto Criteri di gruppo con queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="c99a2-104">The Administrative template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="c99a2-105">L'impostazione seguente è disponibile in computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM durante la modifica di un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="c99a2-105">The following setting is available under Computer Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<span data-ttu-id="c99a2-106">**Percorsi dei file di traccia**:</span><span class="sxs-lookup"><span data-stu-id="c99a2-106">**Trace file locations**:</span></span>

-   <span data-ttu-id="c99a2-107">Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="c99a2-107">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="c99a2-108">Server:%ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="c99a2-108">Server: %ProgramData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c99a2-109">Impostazione</span><span class="sxs-lookup"><span data-stu-id="c99a2-109">Setting</span></span></th>
<th align="left"><span data-ttu-id="c99a2-110">Effetto</span><span class="sxs-lookup"><span data-stu-id="c99a2-110">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="c99a2-111">Advanced Group Policy Management: configurare la registrazione</span><span class="sxs-lookup"><span data-stu-id="c99a2-111">AGPM: Configure logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="c99a2-112">Questa impostazione consente di attivare e configurare la registrazione per Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c99a2-112">This policy setting allows you to turn on and configure logging for AGPM.</span></span> <span data-ttu-id="c99a2-113">Questa impostazione interessa sia i componenti client che quelli del server di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="c99a2-113">This setting affects both client and server components of AGPM.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="c99a2-114">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="c99a2-114">Additional references</span></span>

-   [<span data-ttu-id="c99a2-115">Cartella dei modelli amministrativi</span><span class="sxs-lookup"><span data-stu-id="c99a2-115">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm40.md)

 

 




