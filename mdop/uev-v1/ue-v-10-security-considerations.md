---
title: Considerazioni sulla sicurezza di UE-V 1.0
description: Considerazioni sulla sicurezza di UE-V 1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823996"
---
# <span data-ttu-id="2cc16-103">Considerazioni sulla sicurezza di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc16-103">UE-V 1.0 Security Considerations</span></span>


<span data-ttu-id="2cc16-104">Questo argomento contiene una breve panoramica di account e gruppi, file di log e altre considerazioni relative alla sicurezza per Microsoft User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="2cc16-104">This topic contains a brief overview of accounts and groups, log files, and other security-related considerations for Microsoft User Experience Virtualization (UE-V).</span></span> <span data-ttu-id="2cc16-105">Per altre informazioni, seguire i collegamenti forniti qui.</span><span class="sxs-lookup"><span data-stu-id="2cc16-105">For more information, follow the links that are provided here.</span></span>

## <span data-ttu-id="2cc16-106">Considerazioni sulla sicurezza per la configurazione di UE-V</span><span class="sxs-lookup"><span data-stu-id="2cc16-106">Security considerations for UE-V configuration</span></span>


**<span data-ttu-id="2cc16-107">Quando si crea la condivisione di archiviazione delle impostazioni, limitare l'accesso alla condivisione agli utenti che hanno bisogno di Access.</span><span class="sxs-lookup"><span data-stu-id="2cc16-107">When you create the settings storage share, limit the share access to users that need access.</span></span>**

<span data-ttu-id="2cc16-108">Poiché i pacchetti di impostazioni possono contenere informazioni personali, è necessario prestare particolare attenzione per proteggerli nel modo migliore possibile.</span><span class="sxs-lookup"><span data-stu-id="2cc16-108">Because settings packages may contain personal information, you should take care to protect them as well as possible.</span></span> <span data-ttu-id="2cc16-109">In generale, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2cc16-109">In general, do the following:</span></span>

-   <span data-ttu-id="2cc16-110">Limita la condivisione solo agli utenti che hanno bisogno di Access.</span><span class="sxs-lookup"><span data-stu-id="2cc16-110">Restrict the share to only the users that need access.</span></span> <span data-ttu-id="2cc16-111">Creare un gruppo di sicurezza per gli utenti con cartelle reindirizzate in una particolare condivisione e limitare l'accesso solo agli utenti.</span><span class="sxs-lookup"><span data-stu-id="2cc16-111">Create a security group for users that have redirected folders on a particular share, and limit access to only those users.</span></span>

-   <span data-ttu-id="2cc16-112">Quando si crea la condivisione, nascondere la condivisione inserendo un $ dopo il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="2cc16-112">When you create the share, hide the share by putting a $ after the share name.</span></span> <span data-ttu-id="2cc16-113">In questo modo si nasconderà la condivisione da browser casual e la condivisione non sarà visibile nelle risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="2cc16-113">This will hide the share from casual browsers, and the share will not be visible in My Network Places.</span></span>

-   <span data-ttu-id="2cc16-114">Concedere agli utenti solo l'importo minimo delle autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="2cc16-114">Only give users the minimum amount of permissions needed.</span></span> <span data-ttu-id="2cc16-115">Le autorizzazioni necessarie sono illustrate nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="2cc16-115">The permissions needed are shown in the tables below.</span></span>

    1.  <span data-ttu-id="2cc16-116">Impostare le seguenti autorizzazioni SMB (share-level) per la cartella della posizione di archiviazione dell'impostazione:</span><span class="sxs-lookup"><span data-stu-id="2cc16-116">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><span data-ttu-id="2cc16-117">Account utente</span><span class="sxs-lookup"><span data-stu-id="2cc16-117">User account</span></span></th>
        <th align="left"><span data-ttu-id="2cc16-118">Autorizzazioni consigliate</span><span class="sxs-lookup"><span data-stu-id="2cc16-118">Recommended permissions</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="2cc16-119">Tutti</span><span class="sxs-lookup"><span data-stu-id="2cc16-119">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="2cc16-120">Nessuna autorizzazione</span><span class="sxs-lookup"><span data-stu-id="2cc16-120">No Permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="2cc16-121">Gruppo sicurezza di UE-V</span><span class="sxs-lookup"><span data-stu-id="2cc16-121">Security group of UE-V</span></span></p></td>
        <td align="left"><p><span data-ttu-id="2cc16-122">Controllo completo</span><span class="sxs-lookup"><span data-stu-id="2cc16-122">Full Control</span></span></p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### <span data-ttu-id="2cc16-123">Usare i server Windows Server 2003 o versione successiva per ospitare le condivisioni file reindirizzate</span><span class="sxs-lookup"><span data-stu-id="2cc16-123">Use Windows Server 2003 or later servers to host redirected file shares</span></span>

<span data-ttu-id="2cc16-124">I file di pacchetto delle impostazioni utente contengono informazioni personali trasferite tra il computer client e il server in cui sono archiviati i pacchetti di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="2cc16-124">User settings package files contain personal information that is transferred between the client computer and the server that stores the settings packages.</span></span> <span data-ttu-id="2cc16-125">Per questo motivo, devi assicurarti che i dati siano protetti mentre viaggiano in rete.</span><span class="sxs-lookup"><span data-stu-id="2cc16-125">Because of this, you should ensure that the data is protected while it travels over the network.</span></span>

<span data-ttu-id="2cc16-126">I dati delle impostazioni utente sono vulnerabili a queste potenziali minacce: l'intercettazione dei dati durante l'attraversamento della rete; manomissione dei dati durante l'attraversamento della rete; e lo spoofing del server che ospita i dati.</span><span class="sxs-lookup"><span data-stu-id="2cc16-126">User settings data is vulnerable to these potential threats: interception of the data as it passes over the network; tampering with the data as it passes over the network; and spoofing of the server that hosts the data.</span></span>

<span data-ttu-id="2cc16-127">Diverse funzionalità di Windows Server 2003 e versioni successive consentono di proteggere i dati degli utenti:</span><span class="sxs-lookup"><span data-stu-id="2cc16-127">Several features of Windows Server 2003 and above can help to secure user data:</span></span>

-   <span data-ttu-id="2cc16-128">**Kerberos** -Kerberos è standard in tutte le versioni di Windows 2000 e windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="2cc16-128">**Kerberos** - Kerberos is standard on all versions of Windows 2000 and Windows Server 2003 and later.</span></span> <span data-ttu-id="2cc16-129">Kerberos garantisce il più alto livello di sicurezza per le risorse di rete.</span><span class="sxs-lookup"><span data-stu-id="2cc16-129">Kerberos ensures the highest level of security to network resources.</span></span> <span data-ttu-id="2cc16-130">NTLM autentica il client solo; Kerberos autentica il server e il client.</span><span class="sxs-lookup"><span data-stu-id="2cc16-130">NTLM authenticates the client only; Kerberos authenticates the server and the client.</span></span> <span data-ttu-id="2cc16-131">Quando si usa NTLM, il client non sa se il server è valido.</span><span class="sxs-lookup"><span data-stu-id="2cc16-131">When NTLM is used, the client does not know whether the server is valid.</span></span> <span data-ttu-id="2cc16-132">Questo è particolarmente importante se il client scambia i file personali con il server, come nel caso dei profili mobili.</span><span class="sxs-lookup"><span data-stu-id="2cc16-132">This is particularly important if the client is exchanging personal files with the server, as is the case with Roaming Profiles.</span></span> <span data-ttu-id="2cc16-133">Kerberos offre una sicurezza migliore rispetto a NTLM.</span><span class="sxs-lookup"><span data-stu-id="2cc16-133">Kerberos provides better security than NTLM.</span></span> <span data-ttu-id="2cc16-134">Kerberos non è disponibile nei sistemi operativi Windows NT versione 4,0 o versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="2cc16-134">Kerberos is not available on Windows NT version 4.0 or earlier operating systems.</span></span>

-   <span data-ttu-id="2cc16-135">**IPSec** : il protocollo IPSec (IP Security Protocol) offre l'autenticazione a livello di rete, l'integrità dei dati e la crittografia.</span><span class="sxs-lookup"><span data-stu-id="2cc16-135">**IPsec** - The IP Security Protocol (IPsec) provides network-level authentication, data integrity, and encryption.</span></span> <span data-ttu-id="2cc16-136">IPsec garantisce le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2cc16-136">IPsec ensures the following:</span></span>

    -   <span data-ttu-id="2cc16-137">I dati in roaming sono al sicuro dalla modifica dei dati durante la route.</span><span class="sxs-lookup"><span data-stu-id="2cc16-137">Roamed data is safe from data modification while en route.</span></span>

    -   <span data-ttu-id="2cc16-138">I dati in roaming sono sicuri dall'intercettazione, dalla visualizzazione o dalla copia.</span><span class="sxs-lookup"><span data-stu-id="2cc16-138">Roamed data is safe from interception, viewing, or copying.</span></span>

    -   <span data-ttu-id="2cc16-139">I dati in roaming sono sicuri per l'accesso da parte di parti non autenticate.</span><span class="sxs-lookup"><span data-stu-id="2cc16-139">Roamed data is safe from being accessed by unauthenticated parties.</span></span>

-   <span data-ttu-id="2cc16-140">**SMB signing** -il protocollo di autenticazione SMB (Server Message Block) supporta l'autenticazione dei messaggi che impedisce gli attacchi di tipo Active Message e "Man-in-the-Middle".</span><span class="sxs-lookup"><span data-stu-id="2cc16-140">**SMB Signing** - The Server Message Block (SMB) authentication protocol supports message authentication which prevents active message and "man-in-the-middle" attacks.</span></span> <span data-ttu-id="2cc16-141">La firma SMB fornisce questa autenticazione inserendo una firma digitale in ogni SMB.</span><span class="sxs-lookup"><span data-stu-id="2cc16-141">SMB signing provides this authentication by placing a digital signature into each SMB.</span></span> <span data-ttu-id="2cc16-142">La firma digitale viene quindi verificata sia dal client che dal server.</span><span class="sxs-lookup"><span data-stu-id="2cc16-142">The digital signature is then verified by both the client and the server.</span></span> <span data-ttu-id="2cc16-143">Per usare la firma SMB, è prima necessario abilitarla o richiederla sia nel client SMB che nel server SMB.</span><span class="sxs-lookup"><span data-stu-id="2cc16-143">In order to use SMB signing, you must first either enable it or require it on both the SMB client and the SMB server.</span></span> <span data-ttu-id="2cc16-144">Tieni presente che la firma SMB impone una penalizzazione delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2cc16-144">Note that the SMB signing imposes a performance penalty.</span></span> <span data-ttu-id="2cc16-145">Non utilizza più larghezza di banda della rete, ma usa più cicli di CPU sul lato client e server.</span><span class="sxs-lookup"><span data-stu-id="2cc16-145">It does not consume any more network bandwidth, but it uses more CPU cycles on the client and server side.</span></span>

### <span data-ttu-id="2cc16-146">Usare sempre il file system NTFS per i volumi che tengono i dati degli utenti</span><span class="sxs-lookup"><span data-stu-id="2cc16-146">Always use the NTFS File system for volumes holding users data</span></span>

<span data-ttu-id="2cc16-147">Per la configurazione più sicura, configurare i server che ospitano i file delle impostazioni UE-V per usare il file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="2cc16-147">For the most secure configuration, configure servers that host the UE-V settings files to use the NTFS File System.</span></span> <span data-ttu-id="2cc16-148">Diversamente da FAT, NTFS supporta gli elenchi di controllo di accesso discrezionale (DACL) e gli elenchi di controllo di accesso di sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="2cc16-148">Unlike FAT, NTFS supports Discretionary access control lists (DACLs) and system access control lists (SACLs).</span></span> <span data-ttu-id="2cc16-149">Gli elenchi DACL e SACL controllano chi può eseguire operazioni su un file e quali eventi attiverà la registrazione delle azioni eseguite in un file.</span><span class="sxs-lookup"><span data-stu-id="2cc16-149">DACLs and SACLs control who can perform operations on a file and what events will trigger the logging of actions performed on a file.</span></span>

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a><span data-ttu-id="2cc16-150">Non affidarsi a EFS per crittografare i file degli utenti quando vengono trasmessi tramite la rete</span><span class="sxs-lookup"><span data-stu-id="2cc16-150">Do not rely on EFS to encrypt users’ files when transmitted over the network</span></span>

<span data-ttu-id="2cc16-151">Quando si usa crittografia file System (EFS) per crittografare i file in un server remoto, i dati crittografati non vengono crittografati durante il transito sulla rete; Viene crittografato solo quando è archiviato su disco.</span><span class="sxs-lookup"><span data-stu-id="2cc16-151">When you use Encrypting File System (EFS) to encrypt files on a remote server, the encrypted data is not encrypted during transit over the network; It only becomes encrypted when stored on disk.</span></span>

<span data-ttu-id="2cc16-152">Le eccezioni a questo problema si verificano quando il sistema include IPsec (Internet Protocol Security) o WebDAV (Web Distributed Authoring and Versioning).</span><span class="sxs-lookup"><span data-stu-id="2cc16-152">The exceptions to this are when your system includes Internet Protocol security (IPsec) or Web Distributed Authoring and Versioning (WebDAV).</span></span> <span data-ttu-id="2cc16-153">IPsec crittografa i dati mentre viene trasportato su una rete TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2cc16-153">IPsec encrypts data while it is transported over a TCP/IP network.</span></span> <span data-ttu-id="2cc16-154">Se il file viene crittografato prima di essere copiato o spostato in una cartella WebDAV in un server, resterà crittografato durante la trasmissione e mentre viene archiviato nel server.</span><span class="sxs-lookup"><span data-stu-id="2cc16-154">If the file is encrypted before being copied or moved to a WebDAV folder on a server, it will remain encrypted during the transmission and while it is stored on the server.</span></span>

### <span data-ttu-id="2cc16-155">Crittografare la cache dei file offline</span><span class="sxs-lookup"><span data-stu-id="2cc16-155">Encrypt the Offline Files cache</span></span>

<span data-ttu-id="2cc16-156">Per impostazione predefinita, la cache dei file offline è protetta dalle partizioni NTFS tramite ACL, ma la crittografia della cache migliora ulteriormente la sicurezza in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="2cc16-156">By default, the Offline Files cache is protected on NTFS partitions by ACLs, but encrypting the cache further enhances security on a local computer.</span></span> <span data-ttu-id="2cc16-157">Per impostazione predefinita, la cache nel computer locale non è crittografata, quindi qualsiasi file crittografato memorizzato nella cache dalla rete non verrà crittografato nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="2cc16-157">By default, the cache on the local computer is not encrypted, so any encrypted files cached from the network will not be encrypted on the local computer.</span></span> <span data-ttu-id="2cc16-158">Questo potrebbe rappresentare un rischio per la sicurezza in alcuni ambienti.</span><span class="sxs-lookup"><span data-stu-id="2cc16-158">This may pose a security risk in some environments.</span></span>

<span data-ttu-id="2cc16-159">Quando la crittografia è abilitata, tutti i file della cache dei file offline vengono crittografati.</span><span class="sxs-lookup"><span data-stu-id="2cc16-159">When encryption is enabled, all files in the Offline Files cache are encrypted.</span></span> <span data-ttu-id="2cc16-160">Questo include la crittografia dei file esistenti e i file che verranno aggiunti in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="2cc16-160">This includes encrypting existing files as well as files that are added later.</span></span> <span data-ttu-id="2cc16-161">La copia memorizzata nella cache nel computer locale è interessata, ma la copia di rete associata non è.</span><span class="sxs-lookup"><span data-stu-id="2cc16-161">The cached copy on the local computer is affected, but the associated network copy is not.</span></span>

<span data-ttu-id="2cc16-162">La cache può essere crittografata in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2cc16-162">The cache can be encrypted in one of two ways:</span></span>

1.  <span data-ttu-id="2cc16-163">Tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="2cc16-163">Via Group Policy.</span></span> <span data-ttu-id="2cc16-164">-Abilitare l'impostazione **Crittografa la cache dei file offline** , disponibile nel computer Configuration\\Administrative Templates\\Network\\Offline file, nell'Editor criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="2cc16-164">- Enable the **Encrypt the Offline Files Cache** setting, located at Computer Configuration\\Administrative Templates\\Network\\Offline Files, in the Group Policy editor.</span></span>

2.  <span data-ttu-id="2cc16-165">Manualmente.</span><span class="sxs-lookup"><span data-stu-id="2cc16-165">Manually.</span></span> <span data-ttu-id="2cc16-166">-Selezionare strumenti e quindi Opzioni cartella nel menu di comando di Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="2cc16-166">- Select Tools and then Folder Options in the command menu of Windows Explorer.</span></span> <span data-ttu-id="2cc16-167">Selezionare la scheda file offline e quindi selezionare la casella **di controllo Crittografa i file offline per i dati protetti** .</span><span class="sxs-lookup"><span data-stu-id="2cc16-167">Select the Offline Files tab, and then select the **Encrypt offline files to secure data** check box.</span></span>

### <span data-ttu-id="2cc16-168">Consentire all'agente UE-V di creare cartelle per ogni utente</span><span class="sxs-lookup"><span data-stu-id="2cc16-168">Let the UE-V Agent create folders for each user</span></span>

<span data-ttu-id="2cc16-169">Per assicurarsi che UE-V funzioni in modo ottimale, creare solo la condivisione radice sul server e consentire all'agente UE-V di creare le cartelle per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="2cc16-169">To ensure that UE-V works optimally, create only the root share on the server, and let the UE-V Agent create the folders for each user.</span></span> <span data-ttu-id="2cc16-170">UE-V creerà queste cartelle utente con la sicurezza appropriata.</span><span class="sxs-lookup"><span data-stu-id="2cc16-170">UE-V will create these user folders with the appropriate security.</span></span>

<span data-ttu-id="2cc16-171">Questa configurazione delle autorizzazioni consente agli utenti di creare cartelle per l'archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="2cc16-171">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="2cc16-172">L'agente UE-V crea e protegge una cartella settingspackage durante l'esecuzione nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2cc16-172">The UE-V agent creates and secures a settingspackage folder while running in the context of the user.</span></span> <span data-ttu-id="2cc16-173">L'utente riceve il controllo completo nella propria cartella settingspackage.</span><span class="sxs-lookup"><span data-stu-id="2cc16-173">The user receives full control to their settingspackage folder.</span></span> <span data-ttu-id="2cc16-174">Altri utenti non ereditano l'accesso alla cartella.</span><span class="sxs-lookup"><span data-stu-id="2cc16-174">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="2cc16-175">Non è necessario creare e proteggere le singole directory utente.</span><span class="sxs-lookup"><span data-stu-id="2cc16-175">You do not need to create and secure individual user directories.</span></span> <span data-ttu-id="2cc16-176">Questa operazione verrà eseguita automaticamente dall'agente che viene eseguito nel contesto dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2cc16-176">This will be done automatically by the agent that runs in the context of the user.</span></span>

**<span data-ttu-id="2cc16-177">Nota</span><span class="sxs-lookup"><span data-stu-id="2cc16-177">Note</span></span>**  
<span data-ttu-id="2cc16-178">La sicurezza aggiuntiva può essere configurata quando viene usato un server Windows per la condivisione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="2cc16-178">Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="2cc16-179">L'opzione UE-V può essere configurata per verificare che il gruppo di amministratori locali o l'utente corrente sia il proprietario della cartella in cui sono archiviati i pacchetti di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="2cc16-179">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="2cc16-180">Per abilitare la sicurezza aggiuntiva, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="2cc16-180">To enable additional security use the following command:</span></span>

1.  <span data-ttu-id="2cc16-181">Aggiungere una chiave del registro di sistema REG \ _DWORD denominata "RepositoryOwnerCheckEnabled" `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="2cc16-181">Add a REG\_DWORD registry key named "RepositoryOwnerCheckEnabled" to `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="2cc16-182">Impostare il valore della chiave del registro di sistema su 1.</span><span class="sxs-lookup"><span data-stu-id="2cc16-182">Set registry key value to 1.</span></span>

<span data-ttu-id="2cc16-183">Quando questa impostazione di configurazione è in posizione, l'agente UE-V Verifica che il gruppo o l'utente corrente dell'amministratore locale sia il proprietario della cartella settingspackage.</span><span class="sxs-lookup"><span data-stu-id="2cc16-183">When this configuration setting is in place, the UE-V agent verifies that the local administrator’s group or current user is the owner of the settingspackage folder.</span></span> <span data-ttu-id="2cc16-184">In caso contrario, l'agente UE-V non consentirà l'accesso alla cartella.</span><span class="sxs-lookup"><span data-stu-id="2cc16-184">If not, then the UE-V agent will not allow access to the folder.</span></span>



<span data-ttu-id="2cc16-185">Se è necessario creare cartelle per gli utenti e verificare di avere impostato le autorizzazioni corrette.</span><span class="sxs-lookup"><span data-stu-id="2cc16-185">If you must create folders for the users and ensure that you have the correct permissions set.</span></span>

<span data-ttu-id="2cc16-186">Ti consigliamo vivamente di non creare cartelle precreative e, invece, puoi consentire all'agente UE-V di creare la cartella per l'utente.</span><span class="sxs-lookup"><span data-stu-id="2cc16-186">We strongly recommend that you do not precreate folders and that instead, you allow the UE-V agent to create the folder for the user.</span></span>

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a><span data-ttu-id="2cc16-187">Verificare che le autorizzazioni corrette vengano impostate durante l'archiviazione delle impostazioni di UE-V nella home directory di un utente</span><span class="sxs-lookup"><span data-stu-id="2cc16-187">Ensure that correct permissions are set when storing UE-V settings in a user’s home directory</span></span>

<span data-ttu-id="2cc16-188">Se si reindirizza le impostazioni di UE-V nella home directory di un utente, assicurarsi che le autorizzazioni nella directory Home dell'utente siano impostate in modo appropriato per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="2cc16-188">If you redirect UE-V settings to a user’s home directory, be sure that the permissions on the user's home directory are set appropriately for your organization.</span></span>

## <span data-ttu-id="2cc16-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2cc16-189">Related topics</span></span>


[<span data-ttu-id="2cc16-190">Sicurezza e privacy per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2cc16-190">Security and Privacy for UE-V 1.0</span></span>](security-and-privacy-for-ue-v-10.md)









