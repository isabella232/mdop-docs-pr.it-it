---
title: Informazioni sulla risoluzione dei problemi per Application Virtualization Client
description: Informazioni sulla risoluzione dei problemi per Application Virtualization Client
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815195"
---
# <span data-ttu-id="5cf8f-103">Informazioni sulla risoluzione dei problemi per Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="5cf8f-103">Troubleshooting Information for the Application Virtualization Client</span></span>


<span data-ttu-id="5cf8f-104">Questo argomento include le informazioni che è possibile usare per risolvere diversi problemi relativi al client Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="5cf8f-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Client.</span></span>

## <span data-ttu-id="5cf8f-105">L'aggiornamento della pubblicazione è molto lento</span><span class="sxs-lookup"><span data-stu-id="5cf8f-105">Publishing Refresh Is Very Slow</span></span>


<span data-ttu-id="5cf8f-106">Se l'aggiornamento della pubblicazione in un computer specifico richiede molto più tempo del previsto e se il client è configurato per l'uso dell'impostazione **IconSourceRoot** , determinare se **IconSourceRoot** contiene un URL non valido.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-106">If publishing refresh on a specific computer takes much longer than expected and if the client is configured to use the **IconSourceRoot** setting, determine whether **IconSourceRoot** contains a nonvalid URL.</span></span> <span data-ttu-id="5cf8f-107">Un URL non valido causerà ritardi molto lunghi durante l'aggiornamento della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-107">A nonvalid URL will cause very long delays during publishing refresh.</span></span>

## <span data-ttu-id="5cf8f-108">Gli utenti non possono connettersi al server e accedere alla modalità operazioni disconnesse</span><span class="sxs-lookup"><span data-stu-id="5cf8f-108">Users Cannot Connect to the Server and Go into Disconnected Operations Mode</span></span>


<span data-ttu-id="5cf8f-109">Quando usi un server di gestione App-V configurato con il protocollo RTSPs, se gli utenti non riescono a connettersi e entrano in modalità operativa disconnessa, determina se il certificato usato nel server è valido.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-109">When you are using an App-V Management Server configured with the RTSPS protocol, if the users are unable to connect and they go into disconnected operations mode, determine whether the certificate that is being used on the server is valid.</span></span> <span data-ttu-id="5cf8f-110">Un certificato non valido impedirà agli utenti di connettersi e causerà la modalità operativa disconnessa.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-110">A nonvalid certificate will prevent users from connecting and will cause them to go into disconnected operations mode.</span></span>

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a><span data-ttu-id="5cf8f-111">Gli utenti avvertono prestazioni lente quando le applicazioni non vengono completamente memorizzate nella cache</span><span class="sxs-lookup"><span data-stu-id="5cf8f-111">Users Experience Slow Performance When Applications Are Not Fully Cached</span></span>


<span data-ttu-id="5cf8f-112">Quando le applicazioni non vengono completamente memorizzate nella cache, gli utenti potrebbero occasionalmente avere prestazioni temporanee lente o intermittenti quando avviano o usano l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-112">When applications are not fully cached, users might occasionally experience temporary slow or intermittent performance when they start or use the application.</span></span> <span data-ttu-id="5cf8f-113">È possibile che si verifichino diversi motivi, ad esempio quando il client App-V è in fase di caricamento automatico di un'applicazione o quando viene elaborata una richiesta fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-113">There are several possible reasons this can occur—for example, when the App-V Client is in the process of auto-loading an application or when an Out Of Sequence request is being processed.</span></span> <span data-ttu-id="5cf8f-114">Quando le applicazioni vengono completamente memorizzate nella cache, questi problemi non si verificheranno più.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-114">When the applications are fully cached, these problems will no longer occur.</span></span>

## <a href="" id="error-displayed-after-an-update-is-removed-"></a><span data-ttu-id="5cf8f-115">Errore visualizzato dopo la rimozione di un aggiornamento</span><span class="sxs-lookup"><span data-stu-id="5cf8f-115">Error Displayed After an Update Is Removed</span></span>


<span data-ttu-id="5cf8f-116">È necessario usare il formato di comando di Windows Installer 3,1 corretto per rimuovere un aggiornamento dal client App-V, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="5cf8f-116">You must use the correct Windows Installer 3.1 command format to remove an update from the App-V Client, as follows:</span></span>

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

<span data-ttu-id="5cf8f-117">L'uso del formato di comando precedente `msiexec /package <GUID> /uninstall <GUID>` causerà l'errore 6003 "Application Virtualization Client non è stato possibile avviare".</span><span class="sxs-lookup"><span data-stu-id="5cf8f-117">Using the older command format `msiexec /package <GUID> /uninstall <GUID>` will cause error 6003 "Application Virtualization client could not be started".</span></span>

## <span data-ttu-id="5cf8f-118">Codice di errore 0A-0000E01E si verifica quando si tenta di avviare un'applicazione</span><span class="sxs-lookup"><span data-stu-id="5cf8f-118">Error Code 0A-0000E01E Occurs When You Try to Start an Application</span></span>


<span data-ttu-id="5cf8f-119">Codice di errore 0A-0000E01E indica che il pacchetto dell'applicazione sequenziata potrebbe essere danneggiato.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-119">Error code 0A-0000E01E indicates that the sequenced application package might be corrupt.</span></span> <span data-ttu-id="5cf8f-120">La soluzione consiste nel risequenziare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-120">The solution is to resequence the package.</span></span>

## <span data-ttu-id="5cf8f-121">Gli utenti non possono accedere ai file creati nell'unità Q:</span><span class="sxs-lookup"><span data-stu-id="5cf8f-121">Users Cannot Access Files They Have Created on the Q: Drive</span></span>


<span data-ttu-id="5cf8f-122">Se gli utenti salvano i file nell'unità **Q:** non possono recuperarli perché non hanno diritti di lettura per l'unità.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-122">If users save files to the **Q:** drive, they cannot retrieve them because they do not have read rights to the drive.</span></span> <span data-ttu-id="5cf8f-123">Gli utenti non devono salvare i file nell'unità **Q:** .</span><span class="sxs-lookup"><span data-stu-id="5cf8f-123">Users should not save files to the **Q:** drive.</span></span>

## <span data-ttu-id="5cf8f-124">All'utente viene richiesto un errore 1D1</span><span class="sxs-lookup"><span data-stu-id="5cf8f-124">User Is Prompted with a 1D1 Error</span></span>


<span data-ttu-id="5cf8f-125">Quando l'URL del flusso di file non viene impostato correttamente nel file OSD (Open Software Descriptor), il client App-V restituisce un errore 1d1 anziché un errore "file non trovato".</span><span class="sxs-lookup"><span data-stu-id="5cf8f-125">When the file streaming URL is incorrectly set in the Open Software Descriptor (OSD) file, the App-V Client returns a 1d1 error instead of a “file not found” error.</span></span> <span data-ttu-id="5cf8f-126">Questo errore indica che l'avvio dell'applicazione non è riuscito e che l'utente è stato costretto alla modalità operativa disconnessa.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-126">This error indicates that the application start failed and the user has been forced into disconnected operations mode.</span></span> <span data-ttu-id="5cf8f-127">Correggere l'URL di flusso di file.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-127">Correct the file streaming URL.</span></span>

## <span data-ttu-id="5cf8f-128">Icone non corrette associate ad alcune applicazioni</span><span class="sxs-lookup"><span data-stu-id="5cf8f-128">Incorrect Icons Associated with Some Applications</span></span>


<span data-ttu-id="5cf8f-129">Quando un'icona deve essere usata in un'operazione di pubblicazione, il client App-V determina prima di tutto se ha già una copia memorizzata nella cache dell'icona, cercando nella cache delle icone di un elemento il cui percorso di origine originale corrisponde al percorso dell'icona assegnato all'operazione di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-129">When an icon is to be used in a publishing operation, the App-V Client first determines whether it already has a cached copy of the icon, by looking in the icon cache for an item whose original source path matches the path of the icon given to the publishing operation.</span></span> <span data-ttu-id="5cf8f-130">Se il client App-V trova una corrispondenza, utilizzerà l'icona già memorizzata nella cache; in caso contrario, la nuova icona verrà scaricata nella cache.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-130">If the App-V Client finds a match, it will use the already-cached icon; otherwise, it will download the new icon into the cache.</span></span> <span data-ttu-id="5cf8f-131">Se il percorso dell'icona è una directory di Scratch o se viene riutilizzata per nuove icone o pacchetti, la ricerca nella cache potrebbe selezionare l'icona sbagliata da un'operazione precedente.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-131">If the path to the icon is a scratch directory or if it gets reused for new icons or packages, the lookup in the cache might pick the wrong icon from a previous operation.</span></span>

## <span data-ttu-id="5cf8f-132">Quando si avvia un'applicazione agli utenti vengono richieste le credenziali</span><span class="sxs-lookup"><span data-stu-id="5cf8f-132">Users Are Prompted for Credentials When Starting an Application</span></span>


<span data-ttu-id="5cf8f-133">Se un utente tenta di avviare un'applicazione virtuale a cui l'amministratore di sistema ha accesso limitato, è possibile che venga chiesto di immettere le credenziali per l'utente.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-133">If a user attempts to start a virtual application to which the system administrator has restricted access, the user might be prompted to enter credentials.</span></span> <span data-ttu-id="5cf8f-134">L'utente deve digitare il nome utente e la password per un account che disponga delle autorizzazioni per avviare l'applicazione e quindi premere INVIO.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-134">The user should type the user name and password for an account that has permission to launch the application and then press ENTER.</span></span>

## <span data-ttu-id="5cf8f-135">L'aggiornamento della pubblicazione non riesce dopo l'aggiornamento del client App-V alla versione 4,5</span><span class="sxs-lookup"><span data-stu-id="5cf8f-135">Publishing Refresh Fails After Upgrading the App-V Client to Version 4.5</span></span>


<span data-ttu-id="5cf8f-136">Se la directory dei dati utente è stata precedentemente inserita in una posizione non standard (%*ALLUSERSPROFILE*%\\Documents\\SoftGrid Client\\Users\\%*nomeutente*%), gli utenti che non hanno privilegi di amministratore nel computer troveranno che l'aggiornamento della pubblicazione non riesce dopo l'aggiornamento del client App-V.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-136">If the user data directory was previously placed in a non-standard location (%*AllUsersProfile*%\\Documents\\SoftGrid Client\\Users\\%*username*%), users who do not have administrator privileges on the computer will find that publishing refresh fails after the App-V Client is upgraded.</span></span> <span data-ttu-id="5cf8f-137">Durante l'aggiornamento, la directory di dati globali di App-V client e tutte le relative sottodirectory sono configurate con diritti di accesso limitato solo per gli amministratori.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-137">During the upgrade, the App-V Client global data directory and all its subdirectories are configured with restricted access rights for administrators only.</span></span> <span data-ttu-id="5cf8f-138">Per evitare questo problema, è possibile modificare la directory dei dati utente prima di eseguire l'aggiornamento in modo che non sia una sottodirectory della directory globale dei dati.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-138">You can avoid this problem by changing the user data directory before upgrading so that it is not a subdirectory of the global data directory.</span></span>

## <span data-ttu-id="5cf8f-139">Riavvio necessario dopo l'installazione non riuscita</span><span class="sxs-lookup"><span data-stu-id="5cf8f-139">Reboot Required After Install Failure</span></span>


<span data-ttu-id="5cf8f-140">Se l'installazione del client non riesce per qualsiasi motivo e se i successivi tentativi di installazione del client non riescono, controllare il log di Windows Installer per verificare se viene visualizzato un errore "sftplay non riuscito, errore = 1072".</span><span class="sxs-lookup"><span data-stu-id="5cf8f-140">If the client install fails for any reason and if subsequent attempts to install the client also fail, check the Windows Installer log to see whether it shows an error “sftplay failed, error=1072”.</span></span> <span data-ttu-id="5cf8f-141">In questo caso, riavviare il computer prima di provare a installare di nuovo il client.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-141">If so, restart the computer before trying to install the client again.</span></span>

## <span data-ttu-id="5cf8f-142">Ripristino di un'applicazione virtuale danneggiata</span><span class="sxs-lookup"><span data-stu-id="5cf8f-142">Repairing a Corrupted Virtual Application</span></span>


<span data-ttu-id="5cf8f-143">Se per qualsiasi motivo un pacchetto di applicazione virtuale installato con un file di pacchetto di Windows Installer (MSI) viene danneggiato, reinstallare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-143">If for any reason a virtual application package installed using a Windows Installer Package (MSI) file becomes corrupted, reinstall the package.</span></span> <span data-ttu-id="5cf8f-144">La funzione di ripristino disponibile in Windows Installer non aggiornerà i volumi degli utenti.</span><span class="sxs-lookup"><span data-stu-id="5cf8f-144">The Repair function available in the Windows Installer will not update the user volumes.</span></span>

## <span data-ttu-id="5cf8f-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5cf8f-145">Related topics</span></span>


[<span data-ttu-id="5cf8f-146">Riferimento per Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="5cf8f-146">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)

 

 





