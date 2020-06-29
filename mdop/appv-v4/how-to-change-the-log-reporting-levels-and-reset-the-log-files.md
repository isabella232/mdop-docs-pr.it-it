---
title: Come modificare i livelli del report di registro e azzerare i file di registro
description: Come modificare i livelli del report di registro e azzerare i file di registro
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818046"
---
# <span data-ttu-id="33c02-103">Come modificare i livelli del report di registro e azzerare i file di registro</span><span class="sxs-lookup"><span data-stu-id="33c02-103">How to Change the Log Reporting Levels and Reset the Log Files</span></span>


<span data-ttu-id="33c02-104">È possibile usare la procedura seguente per modificare il livello di report del log dal nodo **Application Virtualization** in Application Virtualization Management Console.</span><span class="sxs-lookup"><span data-stu-id="33c02-104">You can use the following procedure to change the log reporting level from the **Application Virtualization** node in the Application Virtualization Management Console.</span></span> <span data-ttu-id="33c02-105">Quando il file di log raggiunge la dimensione massima (il valore predefinito è 256 MB), viene forzata una reimpostazione quando si verifica la successiva scrittura nel log.</span><span class="sxs-lookup"><span data-stu-id="33c02-105">When the log file reaches the maximum size (default is 256 MB), a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="33c02-106">Un reset causa la creazione di un nuovo file di log e il vecchio file viene rinominato come backup.</span><span class="sxs-lookup"><span data-stu-id="33c02-106">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span>

**<span data-ttu-id="33c02-107">Per modificare il livello di report del log</span><span class="sxs-lookup"><span data-stu-id="33c02-107">To change the log reporting level</span></span>**

1.  <span data-ttu-id="33c02-108">Fare clic con il pulsante destro del mouse sul nodo **Application Virtualization** e scegliere **Proprietà** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="33c02-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="33c02-109">Nella scheda **generale** della finestra di dialogo **Proprietà** Selezionare il livello di log desiderato nell'elenco a discesa **livello log** .</span><span class="sxs-lookup"><span data-stu-id="33c02-109">On the **General** tab in the **Properties** dialog box, from the **Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="33c02-110">**Nota**  Se si sceglie **verbose** come livello di registrazione, i file di log si svilupperanno in modo molto rapido.</span><span class="sxs-lookup"><span data-stu-id="33c02-110">**Note** If you choose **Verbose** as the logging level, the log files will grow large very quickly.</span></span> <span data-ttu-id="33c02-111">Ciò potrebbe inibire le prestazioni del client, quindi è consigliabile usare questo livello di log solo per la diagnosi di problemi specifici.</span><span class="sxs-lookup"><span data-stu-id="33c02-111">This might inhibit client performance, so best practice is to use this log level only for diagnosing specific problems.</span></span>

     

3.  <span data-ttu-id="33c02-112">Nella scheda **generale** della finestra di dialogo **Proprietà** Selezionare il livello di log desiderato nell'elenco a discesa **livello registro di sistema** .</span><span class="sxs-lookup"><span data-stu-id="33c02-112">On the **General** tab in the **Properties** dialog box, from the **System Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="33c02-113">**Nota**  L'impostazione **livello registro di sistema** controlla il livello di messaggi inviati al log eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="33c02-113">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="33c02-114">I messaggi registrati sono identici ai messaggi che vengono registrati nel log eventi del client, ma archiviati in una posizione diversa.</span><span class="sxs-lookup"><span data-stu-id="33c02-114">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location.</span></span>

     

4.  <span data-ttu-id="33c02-115">Fare clic su **OK** o su **applica** per modificare l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="33c02-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="33c02-116">Per reimpostare il file di log</span><span class="sxs-lookup"><span data-stu-id="33c02-116">To reset the log file</span></span>**

1.  <span data-ttu-id="33c02-117">Fare clic con il pulsante destro del mouse sul nodo **Application Virtualization** e scegliere **Proprietà** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="33c02-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="33c02-118">Nella scheda **generale** della finestra di dialogo **Proprietà** fare clic su **Reimposta log** per eseguire il backup del file di log corrente e avviare immediatamente un nuovo file di log.</span><span class="sxs-lookup"><span data-stu-id="33c02-118">On the **General** tab in the **Properties** dialog box, click **Reset Log** to back up the current log file and immediately start a new log file.</span></span> <span data-ttu-id="33c02-119">I file di log di backup sono archiviati nella stessa cartella.</span><span class="sxs-lookup"><span data-stu-id="33c02-119">The backup log files are stored in the same folder.</span></span>

3.  <span data-ttu-id="33c02-120">Fare clic su **OK** o su **applica** per modificare l'impostazione.</span><span class="sxs-lookup"><span data-stu-id="33c02-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="33c02-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="33c02-121">Related topics</span></span>


[<span data-ttu-id="33c02-122">Come configurare il client in Application Virtualization Client Management Console</span><span class="sxs-lookup"><span data-stu-id="33c02-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[<span data-ttu-id="33c02-123">Autorizzazioni di accesso utente in Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="33c02-123">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





