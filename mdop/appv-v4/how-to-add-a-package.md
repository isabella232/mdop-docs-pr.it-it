---
title: Come aggiungere un pacchetto
description: Come aggiungere un pacchetto
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821396"
---
# <span data-ttu-id="67def-103">Come aggiungere un pacchetto</span><span class="sxs-lookup"><span data-stu-id="67def-103">How to Add a Package</span></span>


<span data-ttu-id="67def-104">È possibile aggiungere un pacchetto dalla console di gestione di Application Virtualization Server nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="67def-104">You can add a package from the Application Virtualization Server Management Console in the following ways:</span></span>

-   <span data-ttu-id="67def-105">Importa un'applicazione, che crea il pacchetto automaticamente nel processo.</span><span class="sxs-lookup"><span data-stu-id="67def-105">Import an application, which creates the package automatically in the process.</span></span>

-   <span data-ttu-id="67def-106">Aggiungere un pacchetto manualmente.</span><span class="sxs-lookup"><span data-stu-id="67def-106">Add a package manually.</span></span>

<span data-ttu-id="67def-107">È consigliabile importare le applicazioni invece di aggiungerle manualmente.</span><span class="sxs-lookup"><span data-stu-id="67def-107">It is recommended that you import applications instead of adding them manually.</span></span> <span data-ttu-id="67def-108">Per altre informazioni sull'importazione di applicazioni, vedere [come importare un'applicazione](how-to-import-an-applicationserver.md).</span><span class="sxs-lookup"><span data-stu-id="67def-108">For more information about importing applications, see [How to Import an Application](how-to-import-an-applicationserver.md).</span></span>

**<span data-ttu-id="67def-109">Per aggiungere un pacchetto manualmente</span><span class="sxs-lookup"><span data-stu-id="67def-109">To add a package manually</span></span>**

1.  <span data-ttu-id="67def-110">Nella console di gestione di Application Virtualization Server fare clic con il pulsante destro del mouse sul nodo **pacchetti** nel riquadro sinistro e scegliere **nuovo pacchetto**.</span><span class="sxs-lookup"><span data-stu-id="67def-110">In the Application Virtualization Server Management Console, right-click the **Packages** node in the left pane and choose **New Package**.</span></span>

2.  <span data-ttu-id="67def-111">Nella finestra di dialogo **nuovo pacchetto** Digitare un nome nel campo **nome pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="67def-111">In the **New Package** dialog box, type a name in the **Package Name** field.</span></span>

3.  <span data-ttu-id="67def-112">Cercare o digitare un nome di percorso nel campo **percorso completo per il file del pacchetto** .</span><span class="sxs-lookup"><span data-stu-id="67def-112">Browse for or type a path name in the **Full path for package file** field.</span></span> <span data-ttu-id="67def-113">Questo deve essere un file SFT.</span><span class="sxs-lookup"><span data-stu-id="67def-113">This must be an SFT file.</span></span>

    <span data-ttu-id="67def-114">**Nota**  Se si passa al file SFT, sostituire il percorso locale, ad esempio C:\\Programmi Files\\User\ _Apps \\Virtual\ _App \ _Server \\Content) con il nome host statico o l'indirizzo IP del server.</span><span class="sxs-lookup"><span data-stu-id="67def-114">**Note** If you browse to the SFT file, replace the local path (such as C:\\Program Files\\User\_Apps\\Virtual\_App\_Server\\content) with the server's static host name or IP address.</span></span> <span data-ttu-id="67def-115">L'uso della variabile *% sft \ _SOFTGRIDSERVER%* richiede la configurazione del computer per client.</span><span class="sxs-lookup"><span data-stu-id="67def-115">Using the variable *%SFT\_SOFTGRIDSERVER%* requires per-client computer configuration.</span></span>

    <span data-ttu-id="67def-116">Nelle finestre di dialogo che fanno riferimento a server delle applicazioni virtuali, è necessario usare un percorso di rete, ad esempio il nome host statico o l'indirizzo IP del server, a cui gli utenti possono accedere.</span><span class="sxs-lookup"><span data-stu-id="67def-116">In dialog boxes that refer to Virtual Application Servers, you must use a network location, such as the server's static host name or IP address, that your users can access.</span></span> <span data-ttu-id="67def-117">Il file OSD (Open Software Descriptor) dell'applicazione può sostituire la variabile segnaposto *% sft \ _SOFTGRIDSERER%* con il nome host statico del server o l'indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="67def-117">The application's Open Software Descriptor (OSD) file can replace the placeholder variable *%SFT\_SOFTGRIDSERER%* with the server's static host name or IP address.</span></span> <span data-ttu-id="67def-118">Se si lascia la variabile segnaposto, è necessario impostare questa variabile su ogni computer client che accederà al server.</span><span class="sxs-lookup"><span data-stu-id="67def-118">If you leave the placeholder variable, you must set this variable on each client computer that will access that server.</span></span> <span data-ttu-id="67def-119">Impostare un utente o una variabile di sistema in ogni computer per SFT \ _SOFTGRIDSERVER.</span><span class="sxs-lookup"><span data-stu-id="67def-119">Set a User or System variable on each computer for SFT\_SOFTGRIDSERVER.</span></span> <span data-ttu-id="67def-120">Il valore della variabile deve essere il nome host statico o l'indirizzo IP del server.</span><span class="sxs-lookup"><span data-stu-id="67def-120">The variable value must be the server's static host name or IP address.</span></span> <span data-ttu-id="67def-121">Se si imposta una variabile, si esce dalla sessione client, si disconnette e si torna in Microsoft Windows e quindi si riavvia la sessione in ogni computer in cui è stata eseguita una sessione ed è stata impostata la variabile.</span><span class="sxs-lookup"><span data-stu-id="67def-121">If you set a variable, exit the Client session, log out of and back into Microsoft Windows, and then restart the session on each computer that had a session running and had the variable set.</span></span>

     

4.  <span data-ttu-id="67def-122">Fai clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="67def-122">Click **Next**.</span></span>

5.  <span data-ttu-id="67def-123">La finestra di dialogo **Riepilogo** Mostra il percorso del file e chiede di copiare il file nella posizione se non è già stato fatto.</span><span class="sxs-lookup"><span data-stu-id="67def-123">The **Summary** dialog box shows the file location and prompts you to copy the file to the location if you have not already done so.</span></span> <span data-ttu-id="67def-124">Dopo aver verificato le informazioni, fare clic su **fine** .</span><span class="sxs-lookup"><span data-stu-id="67def-124">Click **Finish** after you have verified the information.</span></span>

    <span data-ttu-id="67def-125">**Nota**  Se si gestiscono applicazioni in un server remoto, nella finestra di dialogo successiva digitare solo il percorso del file relativo alla radice del contenuto del server.</span><span class="sxs-lookup"><span data-stu-id="67def-125">**Note** If you are managing applications on a remote server, in the next dialog box, type only the path of the file relative to the server's content root.</span></span>

     

## <span data-ttu-id="67def-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67def-126">Related topics</span></span>


[<span data-ttu-id="67def-127">Come importare un'applicazione</span><span class="sxs-lookup"><span data-stu-id="67def-127">How to Import an Application</span></span>](how-to-import-an-applicationserver.md)

[<span data-ttu-id="67def-128">Come gestire i pacchetti in Server Management Console</span><span class="sxs-lookup"><span data-stu-id="67def-128">How to Manage Packages in the Server Management Console</span></span>](how-to-manage-packages-in-the-server-management-console.md)

 

 





