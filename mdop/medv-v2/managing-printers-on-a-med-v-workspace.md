---
title: Gestione delle stampanti in un'area di lavoro MED-V
description: Gestione delle stampanti in un'area di lavoro MED-V
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826116"
---
# <span data-ttu-id="2956d-103">Gestione delle stampanti in un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="2956d-103">Managing Printers on a MED-V Workspace</span></span>


<span data-ttu-id="2956d-104">In Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, il reindirizzamento della stampante offre agli utenti finali un'esperienza di stampa coerente tra la macchina virtuale MED-V e il computer host.</span><span class="sxs-lookup"><span data-stu-id="2956d-104">In Microsoft Enterprise Desktop Virtualization (MED-V) 2.0, printer redirection provides end users with a consistent printing experience between the MED-V virtual machine and the host computer.</span></span>

<span data-ttu-id="2956d-105">In questo argomento vengono fornite informazioni su come gestire la stampa in un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2956d-105">This topic provides information about how to manage printing in a MED-V workspace.</span></span>

## <span data-ttu-id="2956d-106">Gestione delle stampanti nelle aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="2956d-106">Managing Printers in MED-V Workspaces</span></span>


<span data-ttu-id="2956d-107">Nella maggior parte dei casi, MED-V gestisce automaticamente il reindirizzamento della stampante.</span><span class="sxs-lookup"><span data-stu-id="2956d-107">In most cases, MED-V handles printer redirection automatically.</span></span> <span data-ttu-id="2956d-108">Al termine della configurazione per la prima volta, MED-V identifica tutte le stampanti di rete installate nell'host, recupera i driver corrispondenti dal server di stampa della rete e, se disponibile, installa i driver rilevanti nell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2956d-108">After first time setup finishes, MED-V identifies all network printers installed on the host, retrieves the corresponding drivers from the network print server, and if found, installs the relevant drivers in the MED-V workspace.</span></span> <span data-ttu-id="2956d-109">Dopo aver trovato e installato tutti i driver, MED-V riavvia l'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="2956d-109">After all drivers are found and installed, MED-V reboots the MED-V workspace.</span></span> <span data-ttu-id="2956d-110">Solo dopo il riavvio dell'area di lavoro MED-V, le stampanti host sono presenti e disponibili nel guest, in genere in pochi minuti.</span><span class="sxs-lookup"><span data-stu-id="2956d-110">Only after the MED-V workspace restarts, the host printers are present and available on the guest, typically in a few minutes.</span></span>

<span data-ttu-id="2956d-111">**Nota**  Se le applicazioni sono in uso nell'area di lavoro MED-V, viene chiesto all'utente finale di consentire al riavvio di continuare o di rinviarlo fino a un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="2956d-111">**Note** If applications are running on the MED-V workspace, the end user is prompted to let the restart continue or postpone it until later.</span></span> <span data-ttu-id="2956d-112">Se non sono in uso applicazioni, il riavvio è automatico e non viene visualizzato per l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="2956d-112">If no applications are running, the restart is automatic and not shown to the end user.</span></span>

 

<span data-ttu-id="2956d-113">Ogni volta che MED-V viene riavviato, controlla se le nuove stampanti sono installate nell'host e, se presenti, recupera i driver corrispondenti dal server di stampa della rete e li installa nel guest.</span><span class="sxs-lookup"><span data-stu-id="2956d-113">Every time MED-V is re-started, it checks whether any new printers are installed on the host and, if found, retrieves the corresponding drivers from the network print server and installs them on the guest.</span></span> <span data-ttu-id="2956d-114">MED-V riavvia quindi l'area di lavoro MED-V proprio come al termine della configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="2956d-114">MED-V then restarts the MED-V workspace just as when first time setup was completed.</span></span>

<span data-ttu-id="2956d-115">**Importante**  Dopo aver installato i driver rilevanti per l'ospite, le stampanti diventano visibili solo dopo che il riavvio si è verificato.</span><span class="sxs-lookup"><span data-stu-id="2956d-115">**Important** After the relevant drivers are installed on the guest, the printers only become visible on the guest after the restart occurs.</span></span>

 

<span data-ttu-id="2956d-116">Se in qualsiasi momento non è possibile localizzare o installare un driver, è necessario che sia installato manualmente nel guest per consentire alla stampante di rete di essere disponibile per l'utente finale.</span><span class="sxs-lookup"><span data-stu-id="2956d-116">If at any time a driver cannot be located or installed, it must be manually installed on the guest for the network printer to be available to the end user.</span></span>

<span data-ttu-id="2956d-117">L'elenco seguente offre alcune indicazioni aggiuntive:</span><span class="sxs-lookup"><span data-stu-id="2956d-117">The following list offers some additional guidance:</span></span>

<span data-ttu-id="2956d-118">**MED-V gestisce solo le stampanti di rete**.</span><span class="sxs-lookup"><span data-stu-id="2956d-118">**MED-V only manages network printers**.</span></span> <span data-ttu-id="2956d-119">I driver per le stampanti installate localmente nell'host non vengono installati automaticamente nell'ospite.</span><span class="sxs-lookup"><span data-stu-id="2956d-119">Drivers for printers that are installed locally on the host are not automatically installed on the guest.</span></span>

<span data-ttu-id="2956d-120">**MED-V installa solo i driver della stampante se presenti nel server di stampa**.</span><span class="sxs-lookup"><span data-stu-id="2956d-120">**MED-V only installs printer drivers if found on the print server**.</span></span> <span data-ttu-id="2956d-121">Se non viene trovato, i driver della stampante devono essere installati manualmente.</span><span class="sxs-lookup"><span data-stu-id="2956d-121">If not found, printer drivers must be manually installed.</span></span>

<span data-ttu-id="2956d-122">**Le stampanti installate manualmente nel guest non sono accessibili all'host**.</span><span class="sxs-lookup"><span data-stu-id="2956d-122">**Printers manually installed on the guest are not accessible to the host**.</span></span> <span data-ttu-id="2956d-123">Per impostazione predefinita, MED-V supporta solo il reindirizzamento della stampante dall'ospite all'host.</span><span class="sxs-lookup"><span data-stu-id="2956d-123">By default, MED-V only supports printer redirection from the guest to the host.</span></span>

<span data-ttu-id="2956d-124">**Avviso**  Se una stampante è installata manualmente nel guest e la stessa stampante viene installata in seguito nell'host, il risultato è che la stampante viene installata due volte nel guest.</span><span class="sxs-lookup"><span data-stu-id="2956d-124">**Warning** If a printer is manually installed on the guest, and the same printer is later installed on the host, the result is that the printer is installed two times in the guest.</span></span> <span data-ttu-id="2956d-125">Per evitare questa situazione, una procedura consigliata per MED-V consiste nel gestire il reindirizzamento della stampante in un solo modo: disabilitare il reindirizzamento e installare le stampanti manualmente nell'ospite o abilitare il reindirizzamento e non installare le stampanti manualmente nell'ospite.</span><span class="sxs-lookup"><span data-stu-id="2956d-125">To avoid this situation, a MED-V best practice is to manage printer redirection in one manner only: either disable redirection and install printers manually on the guest, or enable redirection and do not install printers manually on the guest.</span></span>

 

## <span data-ttu-id="2956d-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2956d-126">Related topics</span></span>


[<span data-ttu-id="2956d-127">Gestire le impostazioni dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="2956d-127">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





