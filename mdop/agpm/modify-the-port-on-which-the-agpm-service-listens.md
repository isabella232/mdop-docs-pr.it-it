---
title: Modificare la porta su cui è in ascolto il servizio Gestione avanzata Criteri di gruppo
description: Modificare la porta su cui è in ascolto il servizio Gestione avanzata Criteri di gruppo
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820486"
---
# <span data-ttu-id="8625f-103">Modificare la porta su cui è in ascolto il servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8625f-103">Modify the Port on Which the AGPM Service Listens</span></span>


<span data-ttu-id="8625f-104">Il servizio Advanced Group Policy Management è un servizio Windows che funge da proxy di sicurezza, che consente di gestire l'accesso client agli oggetti Criteri di gruppo nell'ambiente di archiviazione e produzione.</span><span class="sxs-lookup"><span data-stu-id="8625f-104">The AGPM Service is a Windows service that acts as a security proxy, managing client access to Group Policy objects (GPOs) in the archive and production environment.</span></span> <span data-ttu-id="8625f-105">Per impostazione predefinita, il servizio Advanced Policy Management è in ascolto sulla porta 4600.</span><span class="sxs-lookup"><span data-stu-id="8625f-105">By default, the AGPM Service listens on port 4600.</span></span> <span data-ttu-id="8625f-106">È possibile modificare la porta modificando il file di indice dell'archivio di Advanced Group Policy Management (avanzata) per ogni archivio.</span><span class="sxs-lookup"><span data-stu-id="8625f-106">You can change this port by modifying the Advanced Group Policy Management (AGPM) archive index file for each archive.</span></span>

<span data-ttu-id="8625f-107">**Nota**  Prima di modificare la porta in cui è in ascolto il servizio Advanced Group Policy Management, è consigliabile eseguire il backup del file di indice dell'Archivio Advanced Group Policy Management (gpostate.xml).</span><span class="sxs-lookup"><span data-stu-id="8625f-107">**Note** Before modifying the port on which the AGPM Service listens, it is recommended that you back up the AGPM archive index file (gpostate.xml).</span></span> <span data-ttu-id="8625f-108">Questo file si trova nella cartella immessa come percorso di archiviazione durante l'installazione di Advanced Group Policy Management-Server.</span><span class="sxs-lookup"><span data-stu-id="8625f-108">This file is located in the folder entered as the archive path during the installation of Advanced Group Policy Management - Server.</span></span> <span data-ttu-id="8625f-109">Per impostazione predefinita, questa posizione di questo file è% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml nel server Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8625f-109">By default, this location of this file is %CommonAppData%\\Microsoft\\AGPM\\gpostate.xml on the AGPM Server.</span></span> <span data-ttu-id="8625f-110">Se non si conosce il computer che ospita l'archivio, è possibile seguire la procedura per modificare il percorso di archiviazione per visualizzare il percorso di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="8625f-110">If you do not know which computer hosts the archive, you can follow the procedure for modifying the archive path to display the current archive path.</span></span> <span data-ttu-id="8625f-111">Per altre informazioni, vedere [modificare il percorso di archiviazione](modify-the-archive-path.md).</span><span class="sxs-lookup"><span data-stu-id="8625f-111">For more information, see [Modify the Archive Path](modify-the-archive-path.md).</span></span>

 

<span data-ttu-id="8625f-112">Un account utente con accesso al server Advanced Group Policy Management (il computer in cui è installato il servizio Advanced Group Policy Management) e il file di indice di archivio è necessario per completare questa procedura.</span><span class="sxs-lookup"><span data-stu-id="8625f-112">A user account with access to the AGPM Server (the computer on which the AGPM Service is installed) and the archive index file is required to complete this procedure.</span></span>

**<span data-ttu-id="8625f-113">Per modificare la porta in cui è in ascolto il servizio Advanced Group Policy Management</span><span class="sxs-lookup"><span data-stu-id="8625f-113">To modify the port on which the AGPM Service listens</span></span>**

1.  <span data-ttu-id="8625f-114">Nel computer che ospita l'archivio aprire il file di indice di archivio (gpostate.xml) in un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="8625f-114">On the computer hosting the archive, open the archive index file (gpostate.xml) in a text editor.</span></span>

2.  <span data-ttu-id="8625f-115">Nel file cercare **Advanced Group Policy Management: Port = "4600"**.</span><span class="sxs-lookup"><span data-stu-id="8625f-115">In the file, search for **agpm:port="4600"**.</span></span>

3.  <span data-ttu-id="8625f-116">Sostituire **4600** con la porta in cui deve essere ascoltata il servizio Advanced Group Policy Management. quindi, Salva e Chiudi il file.</span><span class="sxs-lookup"><span data-stu-id="8625f-116">Replace **4600** with the port on which the AGPM Service should listen; then, save and close the file.</span></span>

4.  <span data-ttu-id="8625f-117">Nel server Advanced Group Policy Management riavviare il servizio Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8625f-117">On the AGPM Server, restart the AGPM Service.</span></span> <span data-ttu-id="8625f-118">Per altre informazioni, vedere [avviare e arrestare il servizio Advanced Group Policy Management](start-and-stop-the-agpm-service.md).</span><span class="sxs-lookup"><span data-stu-id="8625f-118">(For more information, see [Start and Stop the AGPM Service](start-and-stop-the-agpm-service.md).)</span></span>

5.  <span data-ttu-id="8625f-119">Modificare la porta nella connessione del server Advanced Group Policy Management per ogni amministratore di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="8625f-119">Modify the port in the AGPM Server connection for each Group Policy administrator.</span></span> <span data-ttu-id="8625f-120">Per altre informazioni, vedere [configurare la connessione al server Advanced Group Policy Management](configure-the-agpm-server-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8625f-120">(For more information, see [Configure the AGPM Server Connection](configure-the-agpm-server-connection.md).)</span></span>

6.  <span data-ttu-id="8625f-121">Ripetere la procedura per ogni server di archiviazione e Advanced Group Policy Management.</span><span class="sxs-lookup"><span data-stu-id="8625f-121">Repeat for each archive and AGPM Server.</span></span>

### <span data-ttu-id="8625f-122">Riferimenti aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="8625f-122">Additional references</span></span>

-   [<span data-ttu-id="8625f-123">Gestione del servizio Gestione avanzata Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="8625f-123">Managing the AGPM Service</span></span>](managing-the-agpm-service.md)

 

 





