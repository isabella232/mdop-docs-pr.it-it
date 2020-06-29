---
title: Risoluzione dei problemi relativi alle operazioni
description: Risoluzione dei problemi relativi alle operazioni
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804455"
---
# <span data-ttu-id="f03ca-103">Risoluzione dei problemi relativi alle operazioni</span><span class="sxs-lookup"><span data-stu-id="f03ca-103">Operations Troubleshooting</span></span>


<span data-ttu-id="f03ca-104">Questo argomento include le informazioni che è possibile usare per risolvere i problemi di funzionamento generali in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="f03ca-104">This topic includes information that you can use to help troubleshoot general operational issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="f03ca-105">Risoluzione dei problemi nelle operazioni MED-V</span><span class="sxs-lookup"><span data-stu-id="f03ca-105">Troubleshooting Issues in MED-V Operations</span></span>


<span data-ttu-id="f03ca-106">Di seguito sono riportati alcuni problemi che gli utenti finali potrebbero incontrare durante l'esecuzione di MED-V e soluzioni per risolvere i problemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f03ca-106">The following are some issues end users might encounter when they run MED-V and solutions to help troubleshoot these issues:</span></span>

<span data-ttu-id="f03ca-107">Il **Reindirizzamento della documentazione non riesce**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-107">**Documentation Redirection Fails**.</span></span> <span data-ttu-id="f03ca-108">Questo problema si verifica in genere quando la cartella documenti di un utente finale punta a un percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="f03ca-108">This issue typically occurs when an end user’s My Documents folder points to a network location.</span></span> <span data-ttu-id="f03ca-109">Windows non supporta la creazione di una condivisione da un'altra cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="f03ca-109">Windows does not support creating a share from another shared folder.</span></span> <span data-ttu-id="f03ca-110">Quando un'unità o una cartella viene reindirizzata al Guest, RDP\\Windows Virtual PC crea una condivisione per tale cartella.</span><span class="sxs-lookup"><span data-stu-id="f03ca-110">When a drive or folder is redirected to the guest, RDP\\Windows Virtual PC creates a share for that folder.</span></span> <span data-ttu-id="f03ca-111">Pertanto, se la cartella documenti nell'host fa già riferimento a una condivisione, RDP\\Windows Virtual PC non può creare una condivisione di una condivisione.</span><span class="sxs-lookup"><span data-stu-id="f03ca-111">Therefore, if the My Documents folder on the host is already pointing to a share, RDP\\Windows Virtual PC cannot create a share of a share.</span></span>

<span data-ttu-id="f03ca-112">Un'altra possibile causa di questo problema è che le credenziali necessarie per connettersi alla risorsa di rete potrebbero essere diverse dalle credenziali di dominio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f03ca-112">Another possible cause of this issue is that the credentials that are required to connect to the network resource might differ from the user’s domain credentials.</span></span> <span data-ttu-id="f03ca-113">MED-V potrebbe rilevare che i documenti vengono reindirizzati nell'host, inviare tali informazioni al Guest e quindi provare a riconnettere la risorsa di rete.</span><span class="sxs-lookup"><span data-stu-id="f03ca-113">MED-V might be detecting that documents are redirected on the host, send that information to the guest, and then try to reconnect the network resource.</span></span> <span data-ttu-id="f03ca-114">Se le credenziali dell'utente non eseguono l'autenticazione, MED-V potrebbe smettere di provare a eseguire l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="f03ca-114">If the user’s credentials do not authenticate, MED-V might stop trying to authenticate.</span></span>

**<span data-ttu-id="f03ca-115">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-115">Solution</span></span>**

<span data-ttu-id="f03ca-116">Per risolvere il problema, provare a eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f03ca-116">Try one of the following to resolve this issue:</span></span>

-   <span data-ttu-id="f03ca-117">Impostare la directory radice dell'utente all'interno di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f03ca-117">Set the user’s root directory inside Active Directory.</span></span> <span data-ttu-id="f03ca-118">Il Guest e l'host devono quindi connettersi alla stessa risorsa di rete.</span><span class="sxs-lookup"><span data-stu-id="f03ca-118">The guest and host should then connect to the same network resource.</span></span>

-   <span data-ttu-id="f03ca-119">Invece di reindirizzare la cartella documenti in un percorso UNC, mapparla a una lettera di unità (nell'host, eseguire il mapping di un'unità che punta alla risorsa di rete).</span><span class="sxs-lookup"><span data-stu-id="f03ca-119">Instead of redirecting the My Documents folder to a UNC path, map it to a drive letter (on the host, map a drive that points to the network resource).</span></span> <span data-ttu-id="f03ca-120">La cartella documenti può quindi essere impostata per usare la lettera dell'unità invece del percorso UNC.</span><span class="sxs-lookup"><span data-stu-id="f03ca-120">The My Documents folder can then be set to use the drive letter instead of the UNC path.</span></span> <span data-ttu-id="f03ca-121">Il Guest verrà quindi reindirizzato alla stessa unità mappata come previsto.</span><span class="sxs-lookup"><span data-stu-id="f03ca-121">The guest will then redirect to that same mapped drive as expected.</span></span>

-   <span data-ttu-id="f03ca-122">Creare uno script di avvio nel guest che reindirizza la cartella documenti alla risorsa di rete e fornisca le credenziali aggiuntive in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="f03ca-122">Create a startup script in the guest that redirects the My Documents folder to the network resource and provides additional credentials as needed.</span></span>

<span data-ttu-id="f03ca-123">Il **Reindirizzamento degli URL non riesce**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-123">**URL Redirection Fails**.</span></span> <span data-ttu-id="f03ca-124">Un URL specificato per il reindirizzamento dall'host al Guest non viene reindirizzato come previsto o sta restituendo un messaggio di errore che indica che il sito Web non esiste.</span><span class="sxs-lookup"><span data-stu-id="f03ca-124">A URL that you have specified for redirection from the host to the guest is not redirecting as intended or is returning an error message that indicates that the website does not exist.</span></span>

**<span data-ttu-id="f03ca-125">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-125">Solution</span></span>**

<span data-ttu-id="f03ca-126">Questo errore può verificarsi quando si verifica un errore di ortografia o un uso errato di caratteri, ad esempio Asterisk (\ \*), nelle informazioni sul reindirizzamento degli URL.</span><span class="sxs-lookup"><span data-stu-id="f03ca-126">This error can occur when there is a misspelling or incorrect use of characters, such as asterisk (\*), in the URL redirection information.</span></span> <span data-ttu-id="f03ca-127">Controllare il valore del registro di sistema per il reindirizzamento degli URL e correggere eventuali errori.</span><span class="sxs-lookup"><span data-stu-id="f03ca-127">Check the registry value for URL redirection and correct any mistakes.</span></span>

<span data-ttu-id="f03ca-128">La chiave del registro di sistema viene chiamata `RedirectUrls` e si trova in genere in:</span><span class="sxs-lookup"><span data-stu-id="f03ca-128">The registry key is called `RedirectUrls` and is typically located at:</span></span>

<span data-ttu-id="f03ca-129">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="f03ca-129">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="f03ca-130">**Icona nella barra delle applicazioni ingannevole**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-130">**Icon in Taskbar Misleading**.</span></span> <span data-ttu-id="f03ca-131">Per impostazione predefinita, l'icona visualizzata nella barra delle applicazioni di un utente finale per l'applicazione pubblica e gli URL reindirizzati è l'icona per Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="f03ca-131">By default, the icon that appears in an end user’s taskbar for published applications and redirected URLs is the icon for Windows Virtual PC.</span></span> <span data-ttu-id="f03ca-132">Se un utente finale non è a conoscenza di questo comportamento predefinito, possono essere confusi quando si guarda la barra delle applicazioni per individuare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f03ca-132">If an end user is not aware of this default behavior, they can become confused when looking at the taskbar to locate their application.</span></span>

**<span data-ttu-id="f03ca-133">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-133">Solution</span></span>**

<span data-ttu-id="f03ca-134">L'unico modo per evitare questo comportamento predefinito consiste nel modificare le impostazioni utente per le proprietà della barra delle applicazioni come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f03ca-134">The only way to avoid this default behavior is to change the user settings for the taskbar properties as follows:</span></span>

1.  <span data-ttu-id="f03ca-135">Fare clic con il pulsante destro del mouse sulla barra delle applicazioni e quindi scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-135">Right-click the taskbar and then click **Properties**.</span></span>

2.  <span data-ttu-id="f03ca-136">Nella finestra di dialogo **delle proprietà del menu Start e della barra** delle applicazioni fare clic sulla scheda della **barra delle applicazioni** .</span><span class="sxs-lookup"><span data-stu-id="f03ca-136">In the **Taskbar and Start Menu Properties** dialog box, click the **Taskbar** tab.</span></span>

3.  <span data-ttu-id="f03ca-137">Nella barra a discesa della finestra di dialogo **pulsanti della barra delle applicazioni** selezionare **non combinare mai**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-137">In the drop-down bar for the **Taskbar buttons** box, select **Never combine**.</span></span>

4.  <span data-ttu-id="f03ca-138">Fai clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-138">Click **OK**.</span></span>

<span data-ttu-id="f03ca-139">Vengono visualizzate le icone previste per le applicazioni pubblicate e gli URL reindirizzati.</span><span class="sxs-lookup"><span data-stu-id="f03ca-139">The expected icons for published applications and redirected URLs are displayed.</span></span>

<span data-ttu-id="f03ca-140">**Avviso emesso se il secondo utente tenta di accedere o se la macchina virtuale è in uso**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-140">**Warning Issued if Second User Attempts Log on or if Virtual Machine is in Use**.</span></span> <span data-ttu-id="f03ca-141">Viene emesso un messaggio di avviso quando un secondo utente accede a un'area di lavoro MED-V mentre un primo utente esegue ancora MED-V.</span><span class="sxs-lookup"><span data-stu-id="f03ca-141">A warning message is issued when a second user logs on to a MED-V workspace while a first user is still running MED-V.</span></span> <span data-ttu-id="f03ca-142">L'avviso viene emesso anche se MED-V viene avviato durante l'uso della macchina virtuale, ad esempio se la macchina virtuale è stata avviata tramite Windows Virtual PC nel menu **Start** .</span><span class="sxs-lookup"><span data-stu-id="f03ca-142">The warning is also issued if MED-V is started while the virtual machine is being used, for example, if the virtual machine was started through Windows Virtual PC on the **Start** menu.</span></span> <span data-ttu-id="f03ca-143">Quando l'utente finale accetta il messaggio di avviso, viene arrestato MED-V.</span><span class="sxs-lookup"><span data-stu-id="f03ca-143">When the end user accepts the warning message, MED-V shuts down.</span></span>

**<span data-ttu-id="f03ca-144">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-144">Solution</span></span>**

<span data-ttu-id="f03ca-145">Un utente finale deve verificare che tutti gli altri utenti abbiano eseguito la disconnessione da MED-V prima di provare a eseguire l'accesso.</span><span class="sxs-lookup"><span data-stu-id="f03ca-145">An end user must verify that all other users are logged off MED-V before they try to log on.</span></span> <span data-ttu-id="f03ca-146">In questo modo si garantisce che non sia in corso nessun'altra istanza di MED-V e che Windows Virtual PC non sia in controllo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f03ca-146">This ensures that no other instance of MED-V is running and that Windows Virtual PC is not in control of the virtual machine.</span></span>

<span data-ttu-id="f03ca-147">**Bip sentiti durante la configurazione per la prima volta**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-147">**Beeps Heard During First Time Setup**.</span></span> <span data-ttu-id="f03ca-148">Occasionalmente viene emesso un segnale acustico mentre MED-V esegue la configurazione per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="f03ca-148">Occasionally, beeps are heard while MED-V is running first time setup.</span></span> <span data-ttu-id="f03ca-149">Questo può creare confusione per un utente finale.</span><span class="sxs-lookup"><span data-stu-id="f03ca-149">This can be confusing to an end user.</span></span> <span data-ttu-id="f03ca-150">I segnali acustici provengono dalla macchina virtuale quando eseguono determinate azioni, ad esempio l'arresto.</span><span class="sxs-lookup"><span data-stu-id="f03ca-150">The beeps are originating from the virtual machine when it performs certain actions, such as shutting down.</span></span>

**<span data-ttu-id="f03ca-151">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-151">Solution</span></span>**

<span data-ttu-id="f03ca-152">È possibile arrestare il servizio bip specificando il comando "net stop beep" all'inizio di ogni sequenza di inizio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f03ca-152">You can stop the beep service by specifying the "net stop beep" command at the beginning of each virtual machine start sequence.</span></span> <span data-ttu-id="f03ca-153">In alternativa, è possibile disabilitare il servizio bip specificando il comando "sc config beep start = disabled".</span><span class="sxs-lookup"><span data-stu-id="f03ca-153">Or you can disable the beep service by specifying the “sc config beep start= disabled" command.</span></span> <span data-ttu-id="f03ca-154">Puoi specificare questi comandi prima di chiudere l'immagine o come parte di Sysprep.</span><span class="sxs-lookup"><span data-stu-id="f03ca-154">You can specify these commands either before you seal the image or as part of Sysprep.</span></span>

<span data-ttu-id="f03ca-155">**Più connessioni di rete create per le aree di lavoro MED-V in modalità Bridged**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-155">**Multiple Network Connections Created for MED-V Workspaces in BRIDGED Mode**.</span></span> <span data-ttu-id="f03ca-156">Se la configurazione per la prima volta crea un'area di lavoro MED-V configurata per la modalità NAT, crea solo una singola connessione di rete in Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="f03ca-156">If first time setup is creating a MED-V workspace that is configured for NAT mode, it only creates a single network connection in Windows Virtual PC.</span></span> <span data-ttu-id="f03ca-157">Tuttavia, se la configurazione per la prima volta crea un'area di lavoro MED-V configurata per la modalità a BRIDGE, crea una connessione di rete separata per ogni scheda di rete installata nel computer, perché MED-V non può determinare la scheda di rete attiva.</span><span class="sxs-lookup"><span data-stu-id="f03ca-157">However, if first time setup is creating a MED-V workspace that is configured for BRIDGED mode, it creates a separate network connection for each network adapter that is installed in the computer, because MED-V cannot determine which network adapter is active.</span></span> <span data-ttu-id="f03ca-158">Questo assicura inoltre che gli utenti mobili abbiano sempre una scheda di rete disponibile per le connessioni cablate e wireless.</span><span class="sxs-lookup"><span data-stu-id="f03ca-158">This also ensures that roaming users always have a network adapter available for wired and wireless connections.</span></span>

**<span data-ttu-id="f03ca-159">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-159">Solution</span></span>**

<span data-ttu-id="f03ca-160">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="f03ca-160">None.</span></span>

<span data-ttu-id="f03ca-161">L' **applicazione MED-V non risponde troppo a lungo quando si chiude**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-161">**MED-V Application is Unresponsive for Too Long when Closing**.</span></span> <span data-ttu-id="f03ca-162">In alcuni casi, un'applicazione MED-V smette di rispondere quando sta provando a chiudersi.</span><span class="sxs-lookup"><span data-stu-id="f03ca-162">In some instances, a MED-V application stops responding when it is trying to close.</span></span>

**<span data-ttu-id="f03ca-163">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-163">Solution</span></span>**

<span data-ttu-id="f03ca-164">Puoi specificare il periodo di tempo in cui MED-V attende di chiudere le applicazioni che non rispondono impostando la chiave del registro di sistema WaitToKillAppTimeout nella macchina virtuale guest.</span><span class="sxs-lookup"><span data-stu-id="f03ca-164">You can specify the length of time that MED-V waits to close unresponsive applications by setting the WaitToKillAppTimeout registry key in the guest virtual machine.</span></span> <span data-ttu-id="f03ca-165">Per altre informazioni, vedere [come aumentare il tempo di arresto in modo che i processi possano uscire correttamente in Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .</span><span class="sxs-lookup"><span data-stu-id="f03ca-165">For more information, see [How To Increase Shutdown Time So That Processes Can Quit Properly in Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) (https://go.microsoft.com/fwlink/?LinkId=206819).</span></span>

<span data-ttu-id="f03ca-166">La **ridenominazione di un collegamento a un'applicazione pubblicata nella macchina virtuale guest non modifica il nome pubblicato nell'host**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-166">**Renaming a Published Application Shortcut in the Guest Virtual Machine does not Change the Published Name in the Host**.</span></span> <span data-ttu-id="f03ca-167">Quando si pubblica un'applicazione creando un collegamento e quindi rinominando il collegamento nella macchina virtuale Guest, il nome dell'applicazione originale rimane nel menu **Start** dell'host.</span><span class="sxs-lookup"><span data-stu-id="f03ca-167">When you publish an application by creating a shortcut and then rename the shortcut in the guest virtual machine, the original application name remains in the host **Start** menu.</span></span> <span data-ttu-id="f03ca-168">Il programma continuerà a essere eseguito come previsto, ma il programma manterrà sempre il nome originale.</span><span class="sxs-lookup"><span data-stu-id="f03ca-168">The program continues to run as expected, however the program will always retain the original name.</span></span>

**<span data-ttu-id="f03ca-169">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-169">Solution</span></span>**

<span data-ttu-id="f03ca-170">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="f03ca-170">None.</span></span> <span data-ttu-id="f03ca-171">Si tratta di un comportamento noto di Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="f03ca-171">This is a known behavior of Windows Virtual PC.</span></span>

<span data-ttu-id="f03ca-172">Lo **spostamento di un collegamento nella macchina virtuale guest non consente di aggiornare la posizione nel menu Start del computer host**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-172">**Moving a Shortcut in the Guest Virtual Machine does not Update the Location on the Host Computer Start Menu**.</span></span> <span data-ttu-id="f03ca-173">I tasti di scelta rapida dell'applicazione MED-V pubblicati nel menu **Start** del computer host sono catalogati nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f03ca-173">MED-V application shortcuts that are published to the host computer **Start** menu are cataloged in the registry.</span></span> <span data-ttu-id="f03ca-174">Se sposti un collegamento a un'applicazione in una sottocartella, il registro di sistema non viene aggiornato per riflettere la modifica.</span><span class="sxs-lookup"><span data-stu-id="f03ca-174">If you move an application shortcut into a subfolder, the registry is not updated to reflect the change.</span></span>

**<span data-ttu-id="f03ca-175">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-175">Solution</span></span>**

<span data-ttu-id="f03ca-176">Seguire questa procedura per modificare la posizione di un collegamento a un'applicazione MED-V:</span><span class="sxs-lookup"><span data-stu-id="f03ca-176">Follow these steps to change the location of a MED-V application shortcut:</span></span>

1.  <span data-ttu-id="f03ca-177">Quando è in corso l'installazione di MED-V, aprire Esplora risorse nella macchina virtuale guest MED-V.</span><span class="sxs-lookup"><span data-stu-id="f03ca-177">When MED-V is running, open up Windows Explorer on the MED-V guest virtual machine.</span></span>

2.  <span data-ttu-id="f03ca-178">Passare alla directory "%ALLUSERSPROFILE%\\Start Menu\\Programs".</span><span class="sxs-lookup"><span data-stu-id="f03ca-178">Browse to the "%ALLUSERSPROFILE%\\Start Menu\\Programs" directory.</span></span>

3.  <span data-ttu-id="f03ca-179">Rimuovere le scelte rapide dall'applicazione dalle cartelle di StartMenu o Programs.</span><span class="sxs-lookup"><span data-stu-id="f03ca-179">Move the application shortcuts out of the startmenu or programs folders.</span></span>

4.  <span data-ttu-id="f03ca-180">Dopo circa 30 secondi, verificare che i tasti di scelta rapida vengano rimossi dal menu **Start** del computer host.</span><span class="sxs-lookup"><span data-stu-id="f03ca-180">After about 30 seconds, validate that the shortcuts are removed from the host computer **Start** menu.</span></span>

5.  <span data-ttu-id="f03ca-181">Riportare i tasti di scelta rapida delle applicazioni nelle nuove cartelle programmi nella directory Start Menu\\Programs.</span><span class="sxs-lookup"><span data-stu-id="f03ca-181">Move the application shortcuts back in to the new program folders under the Start Menu\\Programs directory.</span></span>

6.  <span data-ttu-id="f03ca-182">Dopo circa 30 secondi, verificare che i tasti di scelta rapida vengano aggiornati nel menu **Start** del computer host.</span><span class="sxs-lookup"><span data-stu-id="f03ca-182">After about 30 seconds, validate that the shortcuts are updated in the host computer **Start** Menu.</span></span>

<span data-ttu-id="f03ca-183">**Le applicazioni pubblicate possono essere disattivate dopo il soggiorno**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-183">**Published Applications can Time Out after Sitting Idle**.</span></span> <span data-ttu-id="f03ca-184">In alcuni casi, le applicazioni pubblicate verranno disattivate per un periodo di tempo inattivo.</span><span class="sxs-lookup"><span data-stu-id="f03ca-184">In some cases, published applications will time out if they have sat idle for some time.</span></span> <span data-ttu-id="f03ca-185">Questa situazione si verifica solo se IPsec è abilitato e l'area di lavoro MED-V è configurata per la modalità NAT.</span><span class="sxs-lookup"><span data-stu-id="f03ca-185">This situation only occurs if IPsec is enabled and the MED-V workspace is configured for NAT mode.</span></span> <span data-ttu-id="f03ca-186">Questa situazione non si verifica se l'operazione viene eseguita in modalità BRIDGEd.</span><span class="sxs-lookup"><span data-stu-id="f03ca-186">This situation does not occur if running in BRIDGED mode.</span></span>

**<span data-ttu-id="f03ca-187">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-187">Solution</span></span>**

<span data-ttu-id="f03ca-188">Disabilitare IPsec quando si esegue l'area di lavoro MED-V in modalità NAT.</span><span class="sxs-lookup"><span data-stu-id="f03ca-188">Disable IPsec when you are running the MED-V workspace in NAT mode.</span></span>

<span data-ttu-id="f03ca-189">**L'aggiunta di un'applicazione pubblicata alla barra delle applicazioni consente di ignorare MED-V**.</span><span class="sxs-lookup"><span data-stu-id="f03ca-189">**Pinning a Published Application to the Taskbar Bypasses MED-V**.</span></span> <span data-ttu-id="f03ca-190">Se un utente finale aggiunge un'applicazione pubblicata alla barra delle applicazioni e quindi chiude l'applicazione, MED-V viene ignorato la volta successiva che l'applicazione viene aperta dall'icona della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f03ca-190">If an end user pins a published application to the taskbar and then closes the application, MED-V is bypassed the next time that the application is opened from the taskbar icon.</span></span> <span data-ttu-id="f03ca-191">L'applicazione viene invece aperta direttamente in una finestra di VMSAL.</span><span class="sxs-lookup"><span data-stu-id="f03ca-191">Instead, the application opens directly in a VMSAL window.</span></span>

**<span data-ttu-id="f03ca-192">Soluzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-192">Solution</span></span>**

<span data-ttu-id="f03ca-193">Non aggiungere le applicazioni pubblicate in MED-V alla barra delle domande.</span><span class="sxs-lookup"><span data-stu-id="f03ca-193">Do not pin the applications published in MED-V to the taskbar.</span></span>

## <span data-ttu-id="f03ca-194">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f03ca-194">Related topics</span></span>


[<span data-ttu-id="f03ca-195">Procedure consigliate per le operazioni MED-V</span><span class="sxs-lookup"><span data-stu-id="f03ca-195">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)

[<span data-ttu-id="f03ca-196">Risoluzione dei problemi relativi alla distribuzione</span><span class="sxs-lookup"><span data-stu-id="f03ca-196">Deployment Troubleshooting</span></span>](deployment-troubleshooting.md)

 

 





