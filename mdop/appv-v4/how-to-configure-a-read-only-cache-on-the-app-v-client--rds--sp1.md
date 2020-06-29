---
title: Come configurare una cache di sola lettura sul client App-V (RDS)
description: Come configurare una cache di sola lettura sul client App-V (RDS)
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817946"
---
# <span data-ttu-id="62951-103">Come configurare una cache di sola lettura sul client App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="62951-103">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>


<span data-ttu-id="62951-104">**Importante**  Per usare questa procedura, è necessario che l'App-V 4,6, SP1 sia in uso.</span><span class="sxs-lookup"><span data-stu-id="62951-104">**Important** You must be running App-V 4.6, SP1 to use this procedure.</span></span>

 

<span data-ttu-id="62951-105">Puoi distribuire il client App-V usando una cache condivisa popolata con tutte le applicazioni necessarie per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="62951-105">You can deploy the App-V client by using a shared cache that is populated with all the applications required for all users.</span></span> <span data-ttu-id="62951-106">Quindi configuri i client Servizi Desktop remoto di App-V (RDS) per usare lo stesso file di cache.</span><span class="sxs-lookup"><span data-stu-id="62951-106">Then you configure the App-V Remote Desktop Services (RDS) Clients to use the same cache file.</span></span> <span data-ttu-id="62951-107">Agli utenti viene concesso l'accesso a specifiche applicazioni tramite il processo di pubblicazione App-V.</span><span class="sxs-lookup"><span data-stu-id="62951-107">Users are granted access to specific applications by using the App-V publishing process.</span></span> <span data-ttu-id="62951-108">Dato che la cache è già precaricata con tutte le applicazioni, nessun flusso si verifica quando un utente avvia un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62951-108">Because the cache is already preloaded with all applications, no streaming occurs when a user starts an application.</span></span> <span data-ttu-id="62951-109">Tuttavia, i pacchetti usati per prepopolare la cache devono essere inseriti in un server App-V che supporta il flusso RTSP (Real Time Streaming Protocol) e che concede le autorizzazioni di accesso ai client App-V.</span><span class="sxs-lookup"><span data-stu-id="62951-109">However, the packages used to prepopulate the cache must be put on an App-V server that supports Real Time Streaming Protocol (RTSP) streaming and that grants access permissions to the App-V Clients.</span></span> <span data-ttu-id="62951-110">Se pubblichi le applicazioni usando un server di gestione di App-V, puoi usarlo per ottenere questa funzione di flusso.</span><span class="sxs-lookup"><span data-stu-id="62951-110">If you publish the applications by using an App-V Management Server, you can use it to provide this streaming function.</span></span>

<span data-ttu-id="62951-111">**Nota**  I dettagli descritti in queste procedure sono intesi solo come esempi.</span><span class="sxs-lookup"><span data-stu-id="62951-111">**Note** The details outlined in these procedures are intended as examples only.</span></span> <span data-ttu-id="62951-112">Per completare il processo globale, è possibile usare metodi diversi.</span><span class="sxs-lookup"><span data-stu-id="62951-112">You might use different methods to complete the overall process.</span></span>

 

## <span data-ttu-id="62951-113">Distribuzione del client App-V in uno scenario RDS</span><span class="sxs-lookup"><span data-stu-id="62951-113">Deploying the App-V Client in an RDS Scenario</span></span>


<span data-ttu-id="62951-114">Il processo di distribuzione è costituito da quattro attività principali:</span><span class="sxs-lookup"><span data-stu-id="62951-114">The deployment process consists of four primary tasks:</span></span>

-   <span data-ttu-id="62951-115">Creazione e popolamento del file della cache condivisa Master</span><span class="sxs-lookup"><span data-stu-id="62951-115">Creating and populating the master shared cache file</span></span>

-   <span data-ttu-id="62951-116">Copia del file della cache condivisa nell'archiviazione del server</span><span class="sxs-lookup"><span data-stu-id="62951-116">Copying the shared cache file to the server storage</span></span>

-   <span data-ttu-id="62951-117">Configurazione del software client App-V</span><span class="sxs-lookup"><span data-stu-id="62951-117">Configuring the App-V client software</span></span>

-   <span data-ttu-id="62951-118">Gestione del ciclo di aggiornamento della distribuzione per il file della cache condivisa dopo la distribuzione iniziale</span><span class="sxs-lookup"><span data-stu-id="62951-118">Managing the update deployment cycle for the shared cache file after the initial deployment</span></span>

<span data-ttu-id="62951-119">Queste attività richiedono una pianificazione accurata.</span><span class="sxs-lookup"><span data-stu-id="62951-119">These tasks require careful planning.</span></span> <span data-ttu-id="62951-120">Ti consigliamo di preparare e documentare un processo metodico e riproducibile per l'organizzazione da seguire.</span><span class="sxs-lookup"><span data-stu-id="62951-120">We recommend that you prepare and document a methodical, reproducible process for your organization to follow.</span></span> <span data-ttu-id="62951-121">Questo aspetto è particolarmente importante per la preparazione e la distribuzione del file della cache condivisa master e per la gestione continua degli aggiornamenti delle applicazioni, ognuno dei quali richiede un aggiornamento della cache condivisa master.</span><span class="sxs-lookup"><span data-stu-id="62951-121">This is especially important for the preparation and deployment of the master shared cache file, and for the ongoing management of application updates, each of which require an update to the master shared cache.</span></span> <span data-ttu-id="62951-122">Per completare queste attività primarie, usare le procedure seguenti.</span><span class="sxs-lookup"><span data-stu-id="62951-122">Use the following procedures to complete these primary tasks.</span></span>

<span data-ttu-id="62951-123">**Nota**  Anche se è possibile pubblicare le applicazioni usando diversi metodi, le procedure seguenti si basano sull'uso di un'app-V Management Server per la pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="62951-123">**Note** Although you can publish the applications by using several different methods, the following procedures are based on your using an App-V Management Server for publishing.</span></span>

 

**<span data-ttu-id="62951-124">Per configurare la cache di sola lettura per la distribuzione iniziale</span><span class="sxs-lookup"><span data-stu-id="62951-124">To configure the read-only cache for initial deployment</span></span>**

1. <span data-ttu-id="62951-125">Impostare e configurare un server di gestione di App-V per consentire l'autenticazione utente e il supporto della pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="62951-125">Set up and configure an App-V Management Server to provide user authentication and publishing support.</span></span>

2. <span data-ttu-id="62951-126">Popolare la cartella contenuto di questo server di gestione con tutti i pacchetti di applicazioni necessari per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="62951-126">Populate the Content folder of this Management Server with all the application packages required for all users.</span></span>

3. <span data-ttu-id="62951-127">Configurare un computer di staging in cui è installato il client App-V.</span><span class="sxs-lookup"><span data-stu-id="62951-127">Set up a staging computer that has the App-V Client installed.</span></span> <span data-ttu-id="62951-128">Accedere al computer di staging usando un account che abbia accesso a tutte le applicazioni in modo che il set completo di applicazioni venga pubblicato nel computer e quindi eseguire il flusso delle applicazioni in cache in modo che siano completamente caricate.</span><span class="sxs-lookup"><span data-stu-id="62951-128">Log on to the staging computer by using an account that has access to all applications so that the complete set of applications are published to the computer, and then stream the applications to cache so that they are fully loaded.</span></span>

   **<span data-ttu-id="62951-129">Importante</span><span class="sxs-lookup"><span data-stu-id="62951-129">Important</span></span>**  
   <span data-ttu-id="62951-130">Il computer di staging deve usare lo stesso tipo di sistema operativo e l'architettura di sistema di quelle usate dalle VM in cui verrà eseguito il client App-V.</span><span class="sxs-lookup"><span data-stu-id="62951-130">The staging computer must use the same operating system type and system architecture as those used by the VMs on which the App-V Client will run.</span></span>

     

4. <span data-ttu-id="62951-131">Riavviare il computer di staging in modalità provvisoria per verificare che i driver non siano avviati, perché il file della cache verrà bloccato.</span><span class="sxs-lookup"><span data-stu-id="62951-131">Restart the staging computer in safe mode to make sure that the drivers are not started, because this would lock the cache file.</span></span>

   **<span data-ttu-id="62951-132">Nota</span><span class="sxs-lookup"><span data-stu-id="62951-132">Note</span></span>**  
   <span data-ttu-id="62951-133">In alternativa, è possibile arrestare e disabilitare il servizio di virtualizzazione dell'applicazione e quindi riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="62951-133">Or, you can stop and disable the Application Virtualization service, and then restart the computer.</span></span> <span data-ttu-id="62951-134">Dopo aver copiato il file, ricordarsi di abilitare e riavviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="62951-134">After the file is copied, remember to enable and start the service again.</span></span>

     

5. <span data-ttu-id="62951-135">Copiare il file della cache Sftfs. fsd in una SAN in cui tutti i server RDS possono accedervi, ad esempio in una cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="62951-135">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="62951-136">Imposta le autorizzazioni di accesso alle cartelle per la sola lettura per il gruppo Everyone e per il controllo completo per gli amministratori che gestiscono gli aggiornamenti dei file della cache.</span><span class="sxs-lookup"><span data-stu-id="62951-136">Set the folder access permissions to Read-only for the group Everyone and to Full Control for administrators who will manage the cache file updates.</span></span> <span data-ttu-id="62951-137">La posizione del file di cache può essere ottenuta dal registro di sistema AppFS\\FileName.</span><span class="sxs-lookup"><span data-stu-id="62951-137">The location of the cache file can be obtained from the registry AppFS\\FileName.</span></span>

   **<span data-ttu-id="62951-138">Importante</span><span class="sxs-lookup"><span data-stu-id="62951-138">Important</span></span>**  
   <span data-ttu-id="62951-139">È necessario inserire il file FSD in una posizione che disponga della capacità di risposta e affidabilità pari alle prestazioni di archiviazione associate localmente, ad esempio una SAN.</span><span class="sxs-lookup"><span data-stu-id="62951-139">You must put the FSD file in a location that has the responsiveness and reliability equal to locally attached storage performance, for example, a SAN.</span></span>

     

6. <span data-ttu-id="62951-140">Installare il client App-V RDS in ogni server RDS e quindi configurarlo per l'uso della cache di sola lettura aggiungendo i valori della chiave del registro di sistema seguenti alla chiave AppFS nel client.</span><span class="sxs-lookup"><span data-stu-id="62951-140">Install the App-V RDS Client on each RDS server, and then configure it to use the read-only cache by adding the following registry key values to the AppFS key on the client.</span></span> <span data-ttu-id="62951-141">La chiave AppFS si trova in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS per i computer a 32 bit e in HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS per i computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="62951-141">The AppFS key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\]Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 32-bit computers and at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 64-bit computers.</span></span>

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="62951-142">Chiave</span><span class="sxs-lookup"><span data-stu-id="62951-142">Key</span></span></th>
   <th align="left"><span data-ttu-id="62951-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="62951-143">Type</span></span></th>
   <th align="left"><span data-ttu-id="62951-144">Value</span><span class="sxs-lookup"><span data-stu-id="62951-144">Value</span></span></th>
   <th align="left"><span data-ttu-id="62951-145">Scopo</span><span class="sxs-lookup"><span data-stu-id="62951-145">Purpose</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="62951-146">FileName</span><span class="sxs-lookup"><span data-stu-id="62951-146">FileName</span></span></p></td>
   <td align="left"><p><span data-ttu-id="62951-147">String</span><span class="sxs-lookup"><span data-stu-id="62951-147">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="62951-148">percorso di FSD</span><span class="sxs-lookup"><span data-stu-id="62951-148">path of FSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="62951-149">Specifica il percorso del file della cache condivisa, ad esempio \RDSServername\Sharefolder\SFTFS. FSD (obbligatorio).</span><span class="sxs-lookup"><span data-stu-id="62951-149">Specifies the path of the shared cache file, for example, \RDSServername\Sharefolder\SFTFS.FSD (Required).</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="62951-150">ReadOnlyFSD</span><span class="sxs-lookup"><span data-stu-id="62951-150">ReadOnlyFSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="62951-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="62951-151">DWORD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="62951-152">1</span><span class="sxs-lookup"><span data-stu-id="62951-152">1</span></span></p></td>
   <td align="left"><p><span data-ttu-id="62951-153">Configura il client per l'uso in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="62951-153">Configures the client to operate in Read-Only mode.</span></span> <span data-ttu-id="62951-154">In questo modo, il client non tenterà di eseguire lo streaming degli aggiornamenti nella cache del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="62951-154">This ensures that the client will not try to stream updates to the package cache.</span></span> <span data-ttu-id="62951-155">(obbligatorio).</span><span class="sxs-lookup"><span data-stu-id="62951-155">(Required)</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="62951-156">ErrorLogLocation</span><span class="sxs-lookup"><span data-stu-id="62951-156">ErrorLogLocation</span></span></p></td>
   <td align="left"><p><span data-ttu-id="62951-157">String</span><span class="sxs-lookup"><span data-stu-id="62951-157">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="62951-158">percorso del file di log degli errori (ETL)</span><span class="sxs-lookup"><span data-stu-id="62951-158">path of error log (.etl) file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="62951-159">Voce usata per specificare il percorso del log degli errori.</span><span class="sxs-lookup"><span data-stu-id="62951-159">Entry used to specify the path of the error log.</span></span> <span data-ttu-id="62951-160">Consigliato.</span><span class="sxs-lookup"><span data-stu-id="62951-160">(Recommended.</span></span> <span data-ttu-id="62951-161">Usare un percorso locale come C:\Logs\Sftfs.etl).</span><span class="sxs-lookup"><span data-stu-id="62951-161">Use a local path such as C:\Logs\Sftfs.etl).</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="62951-162">Configurare ogni server RDS nella farm per usare il server di pubblicazione e per usare l'aggiornamento della pubblicazione quando gli utenti accedono.</span><span class="sxs-lookup"><span data-stu-id="62951-162">Configure each RDS server in the farm to use the publishing server and to use publishing update when users log on.</span></span> <span data-ttu-id="62951-163">Quando gli utenti accedono ai server RDS, si verifica un ciclo di aggiornamento della pubblicazione e pubblica tutte le applicazioni per cui è autorizzato il proprio account.</span><span class="sxs-lookup"><span data-stu-id="62951-163">As users log on to the RDS servers, a publishing update cycle occurs and publishes all the applications for which their account is authorized.</span></span> <span data-ttu-id="62951-164">Queste applicazioni vengono eseguite dalla cache condivisa.</span><span class="sxs-lookup"><span data-stu-id="62951-164">These applications are run from the shared cache.</span></span>

**<span data-ttu-id="62951-165">Per configurare il client RDS per l'aggiornamento del pacchetto</span><span class="sxs-lookup"><span data-stu-id="62951-165">To configure the RDS client for package upgrade</span></span>**

1.  <span data-ttu-id="62951-166">Completare l'aggiornamento e il test del pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="62951-166">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="62951-167">Aggiornare il pacchetto nel server App-V.</span><span class="sxs-lookup"><span data-stu-id="62951-167">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="62951-168">Quindi, pubblica e trasmetti la nuova versione delle applicazioni al client nel computer di staging in modo che siano completamente caricati nella cache.</span><span class="sxs-lookup"><span data-stu-id="62951-168">Then, publish and stream the new version of the applications to the client on the staging computer so that they are fully loaded into cache.</span></span>

3.  <span data-ttu-id="62951-169">Riavviare il computer di staging in modalità provvisoria per verificare che i driver non siano avviati.</span><span class="sxs-lookup"><span data-stu-id="62951-169">Restart the staging computer in safe mode to ensure the drivers are not started.</span></span>

    <span data-ttu-id="62951-170">**Nota**  In alternativa, è possibile prima arrestare e quindi disabilitare il servizio di virtualizzazione dell'applicazione in Services. msc e riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="62951-170">**Note** Or, you can first stop and then disable the Application Virtualization service in the Services.msc, and restart the computer.</span></span> <span data-ttu-id="62951-171">Dopo aver copiato il file, ricordarsi di abilitare e riavviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="62951-171">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="62951-172">Copiare il file della cache Sftfs. fsd in una SAN in cui tutti i server RDS possono accedervi, ad esempio in una cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="62951-172">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="62951-173">È possibile usare un nome file diverso, ad esempio SFTFS \ _V2. FSD per distinguere la nuova versione.</span><span class="sxs-lookup"><span data-stu-id="62951-173">You can use a different file name, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="62951-174">Per configurare il client App-V RDS in ogni server RDS della farm per usare il file della cache condivisa aggiornato, cambiare il valore del nome del file della chiave del registro di sistema AppFS in punto nella posizione in cui è stato aggiornato, ad esempio \\\\RDSServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="62951-174">To configure the App-V RDS Client on each RDS server in the farm to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\RDSServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="62951-175">Questo garantisce che ogni server RDS riceva la copia aggiornata della cache quando i driver dell'app-VClient vengono riavviati.</span><span class="sxs-lookup"><span data-stu-id="62951-175">This guarantees that each RDS server receives the updated copy of the cache when the App-Vclient drivers restart.</span></span>

    <span data-ttu-id="62951-176">**Importante**  Per usare il file della cache condivisa aggiornata, è necessario riavviare i server RDS.</span><span class="sxs-lookup"><span data-stu-id="62951-176">**Important** You must restart the RDS servers in order to use the updated shared cache file.</span></span>

     

## <span data-ttu-id="62951-177">Come usare i collegamenti simbolici durante l'aggiornamento della cache</span><span class="sxs-lookup"><span data-stu-id="62951-177">How to Use Symbolic Links when Upgrading the Cache</span></span>


<span data-ttu-id="62951-178">Invece di cambiare il valore FILENAME della chiave AppFS ogni volta che viene distribuito un nuovo file di cache che contiene pacchetti nuovi o aggiornati, è possibile usare un collegamento simbolico nei sistemi operativi seguenti: Windows Vista, Windows 7 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="62951-178">Instead of changing the AppFS key FILENAME value every time that a new cache file is deployed that contains new or upgraded packages, you can use a symbolic link in the following operating systems: Windows Vista, Windows 7, and Windows Server 2008.</span></span> <span data-ttu-id="62951-179">Per altre informazioni sui collegamenti simbolici, vedere [collegamenti simbolici](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) .</span><span class="sxs-lookup"><span data-stu-id="62951-179">For more information about symbolic links, see [Symbolic Links](https://go.microsoft.com/fwlink/?LinkId=157626) (https://go.microsoft.com/fwlink/?LinkId=157626).</span></span> <span data-ttu-id="62951-180">Al contrario, Windows XP non supporta l'uso di collegamenti simbolici ed è invece necessario usare i punti di giunzione.</span><span class="sxs-lookup"><span data-stu-id="62951-180">In contrast, Windows XP does not support the use of symbolic links, and you must use junction points instead.</span></span> <span data-ttu-id="62951-181">Per altre informazioni sulle giunzioni, vedere l' [articolo 205524](https://go.microsoft.com/fwlink/?LinkId=182553) della Microsoft Knowledge base ( https://go.microsoft.com/fwlink/?LinkId=182553) e anche lo strumento [Junction v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ( https://go.microsoft.com/fwlink/?LinkId=182554) .</span><span class="sxs-lookup"><span data-stu-id="62951-181">For more information about junctions, see [article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=182553), and also the tool [Junction v1.05](https://go.microsoft.com/fwlink/?LinkId=182554) (https://go.microsoft.com/fwlink/?LinkId=182554).</span></span>

**<span data-ttu-id="62951-182">Per configurare un collegamento simbolico per fare riferimento alla cache</span><span class="sxs-lookup"><span data-stu-id="62951-182">To configure a symbolic link to reference the cache</span></span>**

1.  <span data-ttu-id="62951-183">Durante la fase di distribuzione iniziale aprire una finestra del prompt dei comandi come amministratore locale nel sistema operativo host del server RDS.</span><span class="sxs-lookup"><span data-stu-id="62951-183">During the initial deployment stage, open a Command Prompt window as a local administrator on the RDS server host operating system.</span></span>

2.  <span data-ttu-id="62951-184">Creare un collegamento simbolico usando il comando MKLINK e quindi configurarlo in punti al file Sftfs. FSD.</span><span class="sxs-lookup"><span data-stu-id="62951-184">Create a symbolic link by using the MKLINK command, and then configure it to point to the Sftfs.fsd file.</span></span>

    **     <span data-ttu-id="62951-185">MKLINK symlinkname \\\\rdshostserver\\sharefolder\\sftfs.FSD</span><span class="sxs-lookup"><span data-stu-id="62951-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span></span>**

3.  <span data-ttu-id="62951-186">Nell'immagine VDI Master VM aprire una finestra del prompt dei comandi usando l'opzione **Esegui come amministratore** e concedere le autorizzazioni di collegamento remoto in modo che la VM possa accedere al collegamento simbolico nel sistema operativo host VDI.</span><span class="sxs-lookup"><span data-stu-id="62951-186">On the VDI Master VM Image, open a Command Prompt window by using the **Run as administrator** option and grant remote link permissions so that the VM can access the symbolic link on the VDI Host operating system.</span></span> <span data-ttu-id="62951-187">Per impostazione predefinita, le autorizzazioni di collegamento remoto sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="62951-187">By default, remote link permissions are disabled.</span></span>

    **<span data-ttu-id="62951-188">fsutil behavior set SymlinkEvaluation R2R: 1</span><span class="sxs-lookup"><span data-stu-id="62951-188">fsutil behavior set SymlinkEvaluation R2R:1</span></span>**

    <span data-ttu-id="62951-189">**Nota**  Nel server di archiviazione è necessario abilitare le autorizzazioni appropriate per i collegamenti.</span><span class="sxs-lookup"><span data-stu-id="62951-189">**Note** On the storage server, appropriate link permissions must be enabled.</span></span> <span data-ttu-id="62951-190">A seconda della posizione del collegamento e del file Sftfs. FSD, le autorizzazioni sono **L2L: 1** o **L2R: 1** o **R2L: 1** o **R2R: 1**.</span><span class="sxs-lookup"><span data-stu-id="62951-190">Depending on the location of link and the Sftfs.fsd file, the permissions are **L2L:1** or **L2R:1** or **R2L:1** or **R2R:1**.</span></span>

     

4.  <span data-ttu-id="62951-191">Quando si configura il client App-V RDS, impostare il valore FILENAME della chiave AppFS uguale al percorso UNC del file FSD che usa il collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="62951-191">When you configure the App-V RDS Client, set the AppFS key FILENAME value equal to the UNC path of the FSD file that is using the symbolic link.</span></span> <span data-ttu-id="62951-192">Ad esempio, imposta il nome del file su \\\\VDIHostserver\\Symlinkname.</span><span class="sxs-lookup"><span data-stu-id="62951-192">For example, set the file name to \\\\VDIHostserver\\Symlinkname.</span></span> <span data-ttu-id="62951-193">Quando l'App-V client accede prima alla cache, il collegamento simbolico passa al client un handle per il file della cache.</span><span class="sxs-lookup"><span data-stu-id="62951-193">When the App-V client first accesses the cache, the symbolic link passes to the client a handle to the cache file.</span></span> <span data-ttu-id="62951-194">Il client continua a usare tale handle purché il client sia in funzione.</span><span class="sxs-lookup"><span data-stu-id="62951-194">The client continues to use that handle as long as the client is running.</span></span> <span data-ttu-id="62951-195">Il valore del collegamento simbolico può essere aggiornato in modo sicuro anche se i client esistenti hanno aperto la cache condivisa precedente.</span><span class="sxs-lookup"><span data-stu-id="62951-195">The value of the symbolic link can safely be updated even if existing clients have the old shared cache open.</span></span>

5.  <span data-ttu-id="62951-196">Quando è necessario aggiornare un pacchetto o aggiungere un nuovo pacchetto alla cache, seguire i passaggi da 1 a 4 della procedura di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="62951-196">When you must upgrade a package or to add a new package to the cache, follow steps 1 through 4 of the upgrade procedure.</span></span> <span data-ttu-id="62951-197">Eliminare quindi il collegamento simbolico e ricrearlo in maniera che punti alla nuova versione del file della cache condivisa.</span><span class="sxs-lookup"><span data-stu-id="62951-197">Then, delete the symbolic link and re-create it to point to the new version of the shared cache file.</span></span> <span data-ttu-id="62951-198">Questo garantisce che ogni server RDS riceva la copia aggiornata della cache quando i driver di App-V client vengono riavviati.</span><span class="sxs-lookup"><span data-stu-id="62951-198">This guarantees that each RDS server receives the updated copy of the cache when the App-V client drivers restart.</span></span> <span data-ttu-id="62951-199">Quando il server RDS viene riavviato, il client App-V riceve un handle per la copia aggiornata della cache perché il client usa il percorso che contiene il collegamento simbolico aggiornato.</span><span class="sxs-lookup"><span data-stu-id="62951-199">When the RDS server is restarted, the App-V client receives a handle to the updated copy of the cache because the client uses the path that contains the updated symbolic link.</span></span> <span data-ttu-id="62951-200">Gli utenti hanno quindi accesso alle applicazioni nuove e aggiornate.</span><span class="sxs-lookup"><span data-stu-id="62951-200">Then, the users have access to the new and updated applications.</span></span>

## <span data-ttu-id="62951-201">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62951-201">Related topics</span></span>


[<span data-ttu-id="62951-202">Come installare il server di gestione di Application Virtualization</span><span class="sxs-lookup"><span data-stu-id="62951-202">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

[<span data-ttu-id="62951-203">Come installare manualmente Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="62951-203">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="62951-204">Come installare il client usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="62951-204">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





