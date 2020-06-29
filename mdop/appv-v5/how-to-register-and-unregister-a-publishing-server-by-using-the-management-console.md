---
title: Come registrare e annullare la registrazione di un server di pubblicazione tramite la console di gestione
description: Come registrare e annullare la registrazione di un server di pubblicazione tramite la console di gestione
author: dansimp
ms.assetid: c24f3b43-4888-41a9-9a39-973657f2b917
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5241af748029b7976c49b6474e5ef7c050699dd7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805223"
---
# <span data-ttu-id="59a88-103">Come registrare e annullare la registrazione di un server di pubblicazione tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="59a88-103">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>


<span data-ttu-id="59a88-104">È possibile registrare e annullare la registrazione dei server di pubblicazione che verranno sincronizzati con il server di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="59a88-104">You can register and unregister publishing servers that will synchronize with the App-V 5.0 management server.</span></span> <span data-ttu-id="59a88-105">È anche possibile vedere l'ultimo tentativo che il server di pubblicazione ha eseguito per sincronizzare le informazioni con il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="59a88-105">You can also see the last attempt that the publishing server made to synchronize the information with the management server.</span></span>

<span data-ttu-id="59a88-106">Usare la procedura seguente per registrare o annullare la registrazione di un server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="59a88-106">Use the following procedure to register or unregister a publishing server.</span></span>

**<span data-ttu-id="59a88-107">Per registrare un server di pubblicazione tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="59a88-107">To register a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="59a88-108">Connettersi alla console di gestione e selezionare **Server**.</span><span class="sxs-lookup"><span data-stu-id="59a88-108">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="59a88-109">Per altre informazioni su come connettersi alla console di gestione, vedere [come connettersi alla console di gestione](how-to-connect-to-the-management-console-beta.md).</span><span class="sxs-lookup"><span data-stu-id="59a88-109">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-beta.md).</span></span>

2.  <span data-ttu-id="59a88-110">Viene visualizzato un elenco dei server di pubblicazione già sincronizzati con il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="59a88-110">A list of publishing servers that already synchronize with the management server is displayed.</span></span> <span data-ttu-id="59a88-111">Fare clic su Registra nuovo server per registrare un nuovo server.</span><span class="sxs-lookup"><span data-stu-id="59a88-111">Click Register New Server to register a new server.</span></span>

3.  <span data-ttu-id="59a88-112">Digitare il nome di un computer di un computer collegato alla riga del **nome del server** per specificare un nome per il server.</span><span class="sxs-lookup"><span data-stu-id="59a88-112">Type a computer name of a domain joined computer on the **Server Name** line, to specify a name for the server.</span></span> <span data-ttu-id="59a88-113">Dovresti anche includere un nome di dominio, ad esempio **MyDomain\\TestServer**.</span><span class="sxs-lookup"><span data-stu-id="59a88-113">You should also include a domain name, for example, **MyDomain\\TestServer**.</span></span> <span data-ttu-id="59a88-114">Fare clic su **Controlla**.</span><span class="sxs-lookup"><span data-stu-id="59a88-114">Click **Check**.</span></span>

4.  <span data-ttu-id="59a88-115">Selezionare il computer e fare clic su **Aggiungi** per aggiungere il computer all'elenco dei server.</span><span class="sxs-lookup"><span data-stu-id="59a88-115">Select the computer and click **Add** to add the computer to the list of servers.</span></span> <span data-ttu-id="59a88-116">Il nuovo server verrà visualizzato nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="59a88-116">The new server will be displayed in the list.</span></span>

**<span data-ttu-id="59a88-117">Per annullare la registrazione di un server di pubblicazione tramite la console di gestione</span><span class="sxs-lookup"><span data-stu-id="59a88-117">To unregister a publishing server using the Management Console</span></span>**

1.  <span data-ttu-id="59a88-118">Connettersi alla console di gestione e selezionare **Server**.</span><span class="sxs-lookup"><span data-stu-id="59a88-118">Connect to the Management Console and select **Servers**.</span></span> <span data-ttu-id="59a88-119">Per altre informazioni su come connettersi alla console di gestione, vedere [come connettersi alla console di gestione](how-to-connect-to-the-management-console-beta.md).</span><span class="sxs-lookup"><span data-stu-id="59a88-119">For more information about how to connect to the Management Console, see [How to Connect to the Management Console](how-to-connect-to-the-management-console-beta.md).</span></span>

2.  <span data-ttu-id="59a88-120">Viene visualizzato un elenco dei server di pubblicazione che vengono sincronizzati con il server di gestione.</span><span class="sxs-lookup"><span data-stu-id="59a88-120">A list of publishing servers that synchronize with the management server is displayed.</span></span>

3.  <span data-ttu-id="59a88-121">Per annullare la registrazione del server, fare clic con il pulsante destro del mouse sul nome del computer e selezionare il nome del computer e scegliere **Annulla registrazione server**.</span><span class="sxs-lookup"><span data-stu-id="59a88-121">To unregister the server, right-click the computer name and select the computer name and select **unregister server**.</span></span>

    <span data-ttu-id="59a88-122">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="59a88-122">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="59a88-123">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="59a88-123">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="59a88-124">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="59a88-124">Got an App-V issue?</span></span>** <span data-ttu-id="59a88-125">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="59a88-125">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="59a88-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59a88-126">Related topics</span></span>


[<span data-ttu-id="59a88-127">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="59a88-127">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 




