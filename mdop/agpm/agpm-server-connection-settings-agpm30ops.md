---
title: Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo
description: Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: 5f03e397-b868-4c49-9cbf-a5f5d0ddcc39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d9ee1e67eb2c565bcf833314d82cdf611e2caa85
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804641"
---
# <span data-ttu-id="f9826-103">Impostazioni di connessione del server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f9826-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="f9826-104">È possibile usare le impostazioni dei modelli amministrativi per la gestione avanzata dei criteri di gruppo per configurare centralmente le connessioni del server Advanced Group Policy Management per gli amministratori dei criteri di gruppo a cui viene applicato un oggetto Criteri di gruppo con queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f9826-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy Object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="f9826-105">Le impostazioni seguenti sono disponibili in utenti Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM durante la modifica di un oggetto Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f9826-105">The following settings are available under User Configuration\\Policies\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f9826-106">Impostazione</span><span class="sxs-lookup"><span data-stu-id="f9826-106">Setting</span></span></th>
<th align="left"><span data-ttu-id="f9826-107">Effetto</span><span class="sxs-lookup"><span data-stu-id="f9826-107">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="f9826-108">Advanced Group Policy Management: specificare il server Advanced Group Policy Management (tutti i domini)</span><span class="sxs-lookup"><span data-stu-id="f9826-108">AGPM: Specify default AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f9826-109">Questa impostazione dei criteri consente di specificare un server Advanced Group Policy Management per tutti i domini.</span><span class="sxs-lookup"><span data-stu-id="f9826-109">This policy setting allows you to specify a default AGPM Server for all domains.</span></span> <span data-ttu-id="f9826-110">Viene usato solo dai client Advanced Group Policy Management e limita gli amministratori dei criteri di gruppo a connettersi a un altro archivio.</span><span class="sxs-lookup"><span data-stu-id="f9826-110">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to another archive.</span></span> <span data-ttu-id="f9826-111">Puoi eseguire l'override di questo valore predefinito per singoli domini usando <strong> Advanced Group Policy Management: specificare l'impostazione dei server Advanced Group Policy </strong> .</span><span class="sxs-lookup"><span data-stu-id="f9826-111">You can override this default for individual domains using the <strong>AGPM: Specify AGPM Servers</strong> setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="f9826-112">Advanced Group Policy Management: specificare server Advanced Group Policy</span><span class="sxs-lookup"><span data-stu-id="f9826-112">AGPM: Specify AGPM Servers</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f9826-113">Questa impostazione dei criteri consente di specificare i server Advanced Group Policy Management per singoli domini.</span><span class="sxs-lookup"><span data-stu-id="f9826-113">This policy setting allows you to specify the AGPM Servers for individual domains.</span></span> <span data-ttu-id="f9826-114">Viene usato solo dai client Advanced Group Policy Management e limita gli amministratori dei criteri di gruppo a connettersi a un altro archivio per il dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="f9826-114">This is used only by AGPM Clients, and restricts Group Policy administrators from connecting to a different archive for the specified domain.</span></span> <span data-ttu-id="f9826-115">Per specificare un server Advanced Group Policy Management predefinito, usare <strong> Advanced Group Policy Management: specificare l'impostazione predefinita del server Advanced Group Policy Management (tutti i domini) </strong> e usare questa impostazione per ignorare il valore predefinito in base al dominio.</span><span class="sxs-lookup"><span data-stu-id="f9826-115">To specify a default AGPM Server, use the <strong>AGPM: Specify default AGPM Server (all domains)</strong> setting and use this policy setting to override the default on a per domain basis.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="f9826-116">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="f9826-116">Additional references</span></span>

-   [<span data-ttu-id="f9826-117">Cartella dei modelli amministrativi</span><span class="sxs-lookup"><span data-stu-id="f9826-117">Administrative Templates Folder</span></span>](administrative-templates-folder-agpm30ops.md)

-   [<span data-ttu-id="f9826-118">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f9826-118">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

 

 





