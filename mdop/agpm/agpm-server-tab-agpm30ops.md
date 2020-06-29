---
title: Scheda Server di Gestione avanzata Criteri di gruppo
description: Scheda Server di Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: fb3b0265-53ed-4bf6-88a4-c409f5f1bed4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 335cad07691f914884583636cef01be8dbaa0266
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819286"
---
# <span data-ttu-id="90a8b-103">Scheda Server di Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="90a8b-103">AGPM Server Tab</span></span>


<span data-ttu-id="90a8b-104">La scheda **server Advanced Group Policy Management** nel riquadro **Cambia controllo** consente di selezionare un server Advanced Group Policy Management immettendo un nome di computer completo e una porta e per eliminare le versioni precedenti degli oggetti Criteri di gruppo dall'archivio per risparmiare spazio su disco nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="90a8b-104">The **AGPM Server** tab on the **Change Control** pane enables you to select an AGPM Server by entering a fully-qualified computer name and port, and to delete older versions of Group Policy Objects (GPOs) from the archive to conserve disk space on the AGPM Server.</span></span>

## <span data-ttu-id="90a8b-105">Specifica del server Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="90a8b-105">Specifying the AGPM Server</span></span>


<span data-ttu-id="90a8b-106">Il server Advanced Group Policy Management selezionato determina quale archivio viene visualizzato nella scheda **contenuto** e in quale posizione vengono applicate le impostazioni di **delega del dominio** .</span><span class="sxs-lookup"><span data-stu-id="90a8b-106">The AGPM Server selected determines which archive is displayed for you on the **Contents** tab and to which location the **Domain Delegation** settings are applied.</span></span> <span data-ttu-id="90a8b-107">La porta predefinita per Advanced Group Policy Management è la porta 4600.</span><span class="sxs-lookup"><span data-stu-id="90a8b-107">The default port for Advanced Group Policy Management (AGPM) is port 4600.</span></span>

<span data-ttu-id="90a8b-108">Se la connessione del server Advanced Group Policy Management è configurata in modo centralizzato usando le impostazioni dei modelli amministrativi, le opzioni disponibili in questa scheda per la configurazione della connessione non sono</span><span class="sxs-lookup"><span data-stu-id="90a8b-108">If the AGPM Server connection is centrally configured using Administrative template settings, the options on this tab for configuring the connection are unavailable.</span></span> <span data-ttu-id="90a8b-109">Per altre informazioni, vedere [configurare le connessioni del server Advanced Group Policy Management](configure-agpm-server-connections-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="90a8b-109">For more information, see [Configure AGPM Server Connections](configure-agpm-server-connections-agpm30ops.md).</span></span>

## <span data-ttu-id="90a8b-110">Eliminazione delle versioni precedenti degli oggetti Criteri di stato</span><span class="sxs-lookup"><span data-stu-id="90a8b-110">Deleting old GPO versions</span></span>


<span data-ttu-id="90a8b-111">Per impostazione predefinita, tutte le versioni di ogni GPO controllato vengono mantenute nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="90a8b-111">By default, all versions of every controlled GPO are retained in the archive.</span></span> <span data-ttu-id="90a8b-112">Tuttavia, puoi configurare il servizio Advanced Group Policy Management per limitare il numero di versioni conservate per ogni GPO ed eliminare automaticamente la versione meno recente quando tale limite viene superato.</span><span class="sxs-lookup"><span data-stu-id="90a8b-112">However, you can configure the AGPM Service to limit the number of versions retained for each GPO and automatically delete the oldest version when that limit is exceeded.</span></span> <span data-ttu-id="90a8b-113">Solo le versioni di GPO visualizzate nella scheda **versioni univoche** del conteggio della finestra **cronologia** verso il limite.</span><span class="sxs-lookup"><span data-stu-id="90a8b-113">Only GPO versions displayed on the **Unique Versions** tab of the **History** window count toward the limit.</span></span>

<span data-ttu-id="90a8b-114">**Nota**  Il numero massimo di versioni univoche da archiviare per ogni GPO non include la versione corrente, quindi l'immissione di 0 mantiene solo la versione corrente.</span><span class="sxs-lookup"><span data-stu-id="90a8b-114">**Note** The maximum number of unique versions to store for each GPO does not include the current version, so entering 0 retains only the current version.</span></span> <span data-ttu-id="90a8b-115">Il limite non deve essere superiore alle versioni di 999.</span><span class="sxs-lookup"><span data-stu-id="90a8b-115">The limit must be no greater than 999 versions.</span></span>

<span data-ttu-id="90a8b-116">Quando viene eliminata una versione di un GPO, un record di tale versione rimane nella cronologia dell'oggetto Criteri di controllo, ma la versione del GPO viene eliminata dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="90a8b-116">When a GPO version is deleted, a record of that version remains in the history of the GPO, but the GPO version itself is deleted from the archive.</span></span> <span data-ttu-id="90a8b-117">Puoi impedire l'eliminazione di una versione di un GPO contrassegnando la cronologia come non cancellabile.</span><span class="sxs-lookup"><span data-stu-id="90a8b-117">You can prevent a GPO version from being deleted by marking it in the history as not deletable.</span></span>

 

### <span data-ttu-id="90a8b-118">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="90a8b-118">Additional references</span></span>

-   [<span data-ttu-id="90a8b-119">Interfaccia utente: Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="90a8b-119">User Interface: Advanced Group Policy Management</span></span>](user-interface-advanced-group-policy-management-agpm30ops.md)

-   [<span data-ttu-id="90a8b-120">Attività di amministrazione per Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="90a8b-120">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks-agpm30ops.md)

-   [<span data-ttu-id="90a8b-121">Attività del revisore</span><span class="sxs-lookup"><span data-stu-id="90a8b-121">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks-agpm30ops.md)

 

 





