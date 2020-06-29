---
title: Impostazioni di registrazione e traccia
description: Impostazioni di registrazione e traccia
author: dansimp
ms.assetid: db6b43c7-fdde-4d11-b5ab-a81346e56940
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bef0f8367647aad688c2aec7586ecdaae2e22143
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820586"
---
# <span data-ttu-id="3f986-103">Impostazioni di registrazione e traccia</span><span class="sxs-lookup"><span data-stu-id="3f986-103">Logging and Tracing Settings</span></span>


<span data-ttu-id="3f986-104">Le impostazioni del modello amministrativo per la gestione avanzata dei criteri di gruppo consentono di configurare in modo centralizzato le opzioni di registrazione e traccia per i server e i client di Advanced Group Policy in cui viene applicato un oggetto Criteri di gruppo con queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="3f986-104">The Administrative Template settings for Advanced Group Policy Management (AGPM) enable you to centrally configure logging and tracing options for AGPM Servers and clients to which a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="3f986-105">L'impostazione seguente è disponibile in computer Configuration\\Administrative Templates\\Windows Components\\AGPM nell' **Editor oggetti Criteri di gruppo** per la modifica di un oggetto Criteri di gruppo in console Gestione criteri di Group (GPMC).</span><span class="sxs-lookup"><span data-stu-id="3f986-105">The following setting is available under Computer Configuration\\Administrative Templates\\Windows Components\\AGPM in the **Group Policy Object Editor** when editing a GPO in the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="3f986-106">Se il percorso non è visibile, fare clic con il pulsante destro del mouse su **modelli amministrativi**e quindi aggiungere il modello Advanced Group Policy Management. admx o Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="3f986-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<span data-ttu-id="3f986-107">**Percorsi dei file di traccia**:</span><span class="sxs-lookup"><span data-stu-id="3f986-107">**Trace file locations**:</span></span>

-   <span data-ttu-id="3f986-108">Client:%LocalAppData%\\Microsoft\\AGPM\\agpm.log</span><span class="sxs-lookup"><span data-stu-id="3f986-108">Client: %LocalAppData%\\Microsoft\\AGPM\\agpm.log</span></span>

-   <span data-ttu-id="3f986-109">Server:%CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span><span class="sxs-lookup"><span data-stu-id="3f986-109">Server: %CommonAppData%\\Microsoft\\AGPM\\agpmserv.log</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="3f986-110">Impostazione</span><span class="sxs-lookup"><span data-stu-id="3f986-110">Setting</span></span></th>
<th align="left"><span data-ttu-id="3f986-111">Effetto</span><span class="sxs-lookup"><span data-stu-id="3f986-111">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="3f986-112">Registrazione Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="3f986-112">AGPM Logging</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="3f986-113">Se abilitata, questa impostazione Configura se la traccia è attivata e il livello di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="3f986-113">If enabled, this setting configures whether tracing is turned on and the level of detail.</span></span> <span data-ttu-id="3f986-114">Questa impostazione interessa sia i componenti client che quelli del server di Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="3f986-114">This setting affects both client and server components of AGPM.</span></span></p>
<p><span data-ttu-id="3f986-115">Se disabilitata o non configurata, questa impostazione non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="3f986-115">If disabled or not configured, this setting has no effect.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="3f986-116">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="3f986-116">Additional references</span></span>

-   [<span data-ttu-id="3f986-117">Impostazioni del modello amministrativo</span><span class="sxs-lookup"><span data-stu-id="3f986-117">Administrative Template Settings</span></span>](administrative-template-settings.md)

 

 





