---
title: Elenco di controllo amministra il server e l'Archivio Advanced Group Policy
description: Elenco di controllo amministra il server e l'Archivio Advanced Group Policy
author: dansimp
ms.assetid: 0b2eb536-c3cc-462f-a42f-27a53f57bc55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f872a476a4a8ddd93546778c6278c175ec715850
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819155"
---
# <span data-ttu-id="8aa6f-103">Elenco di controllo: Amministrare l'archivio e il server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8aa6f-103">Checklist: Administer the AGPM Server and Archive</span></span>


<span data-ttu-id="8aa6f-104">In gestione avanzata Criteri di gruppo, sia il servizio Advanced Group Policy Management che l'archivio vengono gestiti da amministratori Advanced Group Policy (controllo completo).</span><span class="sxs-lookup"><span data-stu-id="8aa6f-104">In Advanced Group Policy Management (AGPM), both the AGPM Service and the archive are managed by AGPM Administrators (Full Control).</span></span> <span data-ttu-id="8aa6f-105">Di seguito sono riportate le attività tipiche di un amministratore Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-105">The following are typical tasks for an AGPM Administrator.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8aa6f-106">Attività frequente</span><span class="sxs-lookup"><span data-stu-id="8aa6f-106">Frequent Task</span></span></th>
<th align="left"><span data-ttu-id="8aa6f-107">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8aa6f-107">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8aa6f-108">Delegare l'accesso ad oggetti Criteri di gruppo nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-108">Delegate access to Group Policy Objects (GPOs) in the archive.</span></span></p></td>
<td align="left"><p><a href="delegate-domain-level-access-to-the-archive-agpm30ops.md" data-raw-source="[Delegate Domain-Level Access to the Archive](delegate-domain-level-access-to-the-archive-agpm30ops.md)"><span data-ttu-id="8aa6f-109">Delegare l'accesso a livello di dominio all'archivio</span><span class="sxs-lookup"><span data-stu-id="8aa6f-109">Delegate Domain-Level Access to the Archive</span></span></a></p>
<p><a href="delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md" data-raw-source="[Delegate Access to an Individual GPO in the Archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md)"><span data-ttu-id="8aa6f-110">Delegare l'accesso a un singolo oggetto Criteri di gruppo nell'archivio</span><span class="sxs-lookup"><span data-stu-id="8aa6f-110">Delegate Access to an Individual GPO in the Archive</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8aa6f-111">Eseguire il backup dell'archivio per abilitare il ripristino di emergenza.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-111">Back up the archive to enable disaster recovery.</span></span></p></td>
<td align="left"><p><a href="back-up-the-archive.md" data-raw-source="[Back Up the Archive](back-up-the-archive.md)"><span data-ttu-id="8aa6f-112">Eseguire il backup dell'archivio</span><span class="sxs-lookup"><span data-stu-id="8aa6f-112">Back Up the Archive</span></span></a></p></td>
</tr>
</tbody>
</table>

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8aa6f-113">Attività non frequenti</span><span class="sxs-lookup"><span data-stu-id="8aa6f-113">Infrequent Task</span></span></th>
<th align="left"><span data-ttu-id="8aa6f-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8aa6f-114">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8aa6f-115">Ripristinare l'archivio da un backup per recuperarlo da un disastro.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-115">Restore the archive from a backup to recover from a disaster.</span></span></p></td>
<td align="left"><p><a href="restore-the-archive-from-a-backup.md" data-raw-source="[Restore the Archive from a Backup](restore-the-archive-from-a-backup.md)"><span data-ttu-id="8aa6f-116">Ripristinare l'archivio da un backup</span><span class="sxs-lookup"><span data-stu-id="8aa6f-116">Restore the Archive from a Backup</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8aa6f-117">Trasferire il servizio Advanced Group Policy Management, l'archivio o entrambi in un server diverso.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-117">Move the AGPM Service, the archive, or both to a different server.</span></span></p></td>
<td align="left"><p><a href="move-the-agpm-server-and-the-archive.md" data-raw-source="[Move the AGPM Server and the Archive](move-the-agpm-server-and-the-archive.md)"><span data-ttu-id="8aa6f-118">Spostare l'archivio e il server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8aa6f-118">Move the AGPM Server and the Archive</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8aa6f-119">Modificare il percorso di archiviazione, l'account del servizio Advanced Group Policy Management o la porta in cui è in ascolto il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-119">Change the archive path, the AGPM Service Account, or the port on which the AGPM Service listens.</span></span></p></td>
<td align="left"><p><a href="modify-the-agpm-service-agpm30ops.md" data-raw-source="[Modify the AGPM Service](modify-the-agpm-service-agpm30ops.md)"><span data-ttu-id="8aa6f-120">Modificare il servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8aa6f-120">Modify the AGPM Service</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8aa6f-121">Risolvere i problemi comuni con il server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8aa6f-121">Troubleshoot common problems with the AGPM Server.</span></span></p></td>
<td align="left"><p><a href="troubleshooting-advanced-group-policy-management-agpm30ops.md" data-raw-source="[Troubleshooting Advanced Group Policy Management](troubleshooting-advanced-group-policy-management-agpm30ops.md)"><span data-ttu-id="8aa6f-122">Risoluzione dei problemi di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8aa6f-122">Troubleshooting Advanced Group Policy Management</span></span></a></p>
<p><a href="configure-logging-and-tracing-agpm30ops.md" data-raw-source="[Configure Logging and Tracing](configure-logging-and-tracing-agpm30ops.md)"><span data-ttu-id="8aa6f-123">Configurare registrazione e traccia</span><span class="sxs-lookup"><span data-stu-id="8aa6f-123">Configure Logging and Tracing</span></span></a></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="8aa6f-124">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="8aa6f-124">Additional references</span></span>

-   [<span data-ttu-id="8aa6f-125">Guida operativa per Gestione avanzata Criteri di gruppo Microsoft 3.0</span><span class="sxs-lookup"><span data-stu-id="8aa6f-125">Operations Guide for Microsoft Advanced Group Policy Management 3.0</span></span>](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





