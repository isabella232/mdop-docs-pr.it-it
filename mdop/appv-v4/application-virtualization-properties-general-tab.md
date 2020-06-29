---
title: Scheda generale delle proprietà di Application Virtualization
description: Scheda generale delle proprietà di Application Virtualization
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819686"
---
# <span data-ttu-id="08bb0-103">Proprietà Application Virtualization: Scheda Generale</span><span class="sxs-lookup"><span data-stu-id="08bb0-103">Application Virtualization Properties: General Tab</span></span>


<span data-ttu-id="08bb0-104">Usare la scheda **generale** della finestra di dialogo **Proprietà Application Virtualization** per modificare le impostazioni del log e le posizioni dei dati.</span><span class="sxs-lookup"><span data-stu-id="08bb0-104">Use the **General** tab of the **Application Virtualization Properties** dialog box to modify log settings and data locations.</span></span>

<span data-ttu-id="08bb0-105">Questa scheda contiene gli elementi seguenti.</span><span class="sxs-lookup"><span data-stu-id="08bb0-105">This tab contains the following elements.</span></span>

<a href="" id="log-level"></a>**<span data-ttu-id="08bb0-106">Livello di log</span><span class="sxs-lookup"><span data-stu-id="08bb0-106">Log Level</span></span>**  
<span data-ttu-id="08bb0-107">Selezionare il livello nell'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="08bb0-107">Select the level from the drop-down list.</span></span> <span data-ttu-id="08bb0-108">Il livello predefinito è le **informazioni**.</span><span class="sxs-lookup"><span data-stu-id="08bb0-108">The default level is **Information**.</span></span>

<a href="" id="reset-log"></a>**<span data-ttu-id="08bb0-109">Reimposta log</span><span class="sxs-lookup"><span data-stu-id="08bb0-109">Reset Log</span></span>**  
<span data-ttu-id="08bb0-110">Fare clic su questo pulsante per eseguire il backup del file di log corrente e avviare immediatamente un nuovo file di log.</span><span class="sxs-lookup"><span data-stu-id="08bb0-110">Click this button to back up the current log file and immediately start a new log file.</span></span>

<a href="" id="location"></a>**<span data-ttu-id="08bb0-111">Posizione</span><span class="sxs-lookup"><span data-stu-id="08bb0-111">Location</span></span>**  
<span data-ttu-id="08bb0-112">Immettere o passare al percorso in cui si vuole salvare il file di log sftlog.txt.</span><span class="sxs-lookup"><span data-stu-id="08bb0-112">Enter or browse to the location where you want to save the log file sftlog.txt.</span></span> <span data-ttu-id="08bb0-113">I percorsi predefiniti sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="08bb0-113">The default locations are as follows:</span></span>

-   <span data-ttu-id="08bb0-114">Per WindowsXP, Windows Server2003 —*c:\\Documents and e Settings\\All Users\\Application Data\\Microsoft\\Application client di virtualizzazione*</span><span class="sxs-lookup"><span data-stu-id="08bb0-114">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="08bb0-115">Per Windows Vista, Windows 7, Windows Server2008 —*client di virtualizzazione C:\\ProgramData\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="08bb0-115">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="system-log-level"></a>**<span data-ttu-id="08bb0-116">Livello di registro di sistema</span><span class="sxs-lookup"><span data-stu-id="08bb0-116">System Log Level</span></span>**  
<span data-ttu-id="08bb0-117">Selezionare il livello nell'elenco a discesa.</span><span class="sxs-lookup"><span data-stu-id="08bb0-117">Select the level from the drop-down list.</span></span> <span data-ttu-id="08bb0-118">Il livello predefinito è **warning**.</span><span class="sxs-lookup"><span data-stu-id="08bb0-118">The default level is **Warning**.</span></span>

<span data-ttu-id="08bb0-119">**Nota**  L'impostazione **livello registro di sistema** controlla il livello di messaggi inviati al log eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="08bb0-119">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="08bb0-120">I messaggi registrati sono identici ai messaggi che vengono registrati nel log eventi del client, ma archiviati in una posizione diversa che non ha le limitazioni di spazio del log eventi del client.</span><span class="sxs-lookup"><span data-stu-id="08bb0-120">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location that does not have the space limitations of the client event log.</span></span> <span data-ttu-id="08bb0-121">Poiché il log eventi di sistema non ha limitazioni di spazio, è ideale per le situazioni in cui è necessaria la registrazione dettagliata.</span><span class="sxs-lookup"><span data-stu-id="08bb0-121">Because the system event log does not have space limitations, it is ideally suited for situations where verbose logging is necessary.</span></span>

 

<a href="" id="global-data-directory"></a>**<span data-ttu-id="08bb0-122">Directory dati globale</span><span class="sxs-lookup"><span data-stu-id="08bb0-122">Global Data Directory</span></span>**  
<span data-ttu-id="08bb0-123">Immettere o passare al percorso della directory del file di log.</span><span class="sxs-lookup"><span data-stu-id="08bb0-123">Enter or browse to the location of the directory of the log file.</span></span> <span data-ttu-id="08bb0-124">I percorsi predefiniti sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="08bb0-124">The default locations are as follows:</span></span>

-   <span data-ttu-id="08bb0-125">Per WindowsXP, Windows Server2003 —*c:\\Documents and e Settings\\All Users\\Application Data\\Microsoft\\Application client di virtualizzazione*</span><span class="sxs-lookup"><span data-stu-id="08bb0-125">For WindowsXP, Windows Server2003—*C:\\Documents and Settings\\All Users\\Application Data\\Microsoft\\Application Virtualization Client*</span></span>

-   <span data-ttu-id="08bb0-126">Per Windows Vista, Windows 7, Windows Server2008 —*client di virtualizzazione C:\\ProgramData\\Microsoft\\Application*</span><span class="sxs-lookup"><span data-stu-id="08bb0-126">For Windows Vista, Windows 7, Windows Server2008—*C:\\ProgramData\\Microsoft\\Application Virtualization Client*</span></span>

<a href="" id="user-data-directory"></a>**<span data-ttu-id="08bb0-127">Directory dati utente</span><span class="sxs-lookup"><span data-stu-id="08bb0-127">User Data Directory</span></span>**  
<span data-ttu-id="08bb0-128">Immettere o passare al percorso della directory in cui sono archiviati i dati specifici dell'utente.</span><span class="sxs-lookup"><span data-stu-id="08bb0-128">Enter or browse to the location of the directory where user-specific data is stored.</span></span> <span data-ttu-id="08bb0-129">Il valore predefinito è% APPDATA%.</span><span class="sxs-lookup"><span data-stu-id="08bb0-129">The default is %APPDATA%.</span></span> <span data-ttu-id="08bb0-130">Questo percorso deve essere una variabile di ambiente valida nel computer client.</span><span class="sxs-lookup"><span data-stu-id="08bb0-130">This path must be a valid environment variable on the client computer.</span></span>

## <span data-ttu-id="08bb0-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08bb0-131">Related topics</span></span>


[<span data-ttu-id="08bb0-132">Client Management Console: Proprietà Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="08bb0-132">Client Management Console: Application Virtualization Properties</span></span>](client-management-console-application-virtualization-properties.md)

 

 





