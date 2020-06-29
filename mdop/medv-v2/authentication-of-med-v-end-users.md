---
title: Autenticazione degli utenti finali MED-V
description: Autenticazione degli utenti finali MED-V
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824886"
---
# <span data-ttu-id="7ac5f-103">Autenticazione degli utenti finali MED-V</span><span class="sxs-lookup"><span data-stu-id="7ac5f-103">Authentication of MED-V End Users</span></span>


<span data-ttu-id="7ac5f-104">L'autenticazione degli utenti finali di Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 è un problema di sicurezza molto importante.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-104">The authentication of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 end users is a very important security issue.</span></span> <span data-ttu-id="7ac5f-105">In questo contesto, l'autenticazione fa riferimento alla verifica dell'identità dell'utente finale MED-V.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-105">In this context, authentication refers to verifying the identity of the MED-V end user.</span></span>

<span data-ttu-id="7ac5f-106">La sezione seguente contiene informazioni e indicazioni sull'autenticazione degli utenti finali in MED-V.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-106">The following section provides information and guidance about end-user authentication in MED-V.</span></span>

## <span data-ttu-id="7ac5f-107">Autenticazione utente in MED-V</span><span class="sxs-lookup"><span data-stu-id="7ac5f-107">User Authentication in MED-V</span></span>


<span data-ttu-id="7ac5f-108">L'autenticazione in MED-V si verifica in genere a due livelli: quando un utente accede prima a MED-V e ogni volta che cambia la password.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-108">Authentication in MED-V generally occurs at two levels: when a user first accesses MED-V and every time that they change their password.</span></span>

<span data-ttu-id="7ac5f-109">A seconda di come sono state configurate le impostazioni di MED-V per l'autenticazione, l'utente finale viene in genere richiesto ad un certo punto per immettere la propria password, ovvero la prima volta che viene avviato MED-V o la prima volta che provano ad aprire un'applicazione pubblicata.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-109">Depending on how you have configured MED-V settings for authentication, the end user is typically prompted at some point to enter their password, either the first time MED-V is started or the first time that they try to open a published application.</span></span>

<span data-ttu-id="7ac5f-110">Esistono diversi aspetti dell'autenticazione dell'utente finale che è possibile controllare, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ac5f-110">There are several aspects of end-user authentication that you can control, including the following:</span></span>

<span data-ttu-id="7ac5f-111">Se le credenziali immessi dall'utente finale sono archiviate in Gestione credenziali</span><span class="sxs-lookup"><span data-stu-id="7ac5f-111">Whether the credentials the end user enters are stored in Credential Manager</span></span>

<span data-ttu-id="7ac5f-112">In che modo viene presentato l'utente finale con l'opzione di immissione e salvataggio della password</span><span class="sxs-lookup"><span data-stu-id="7ac5f-112">In what manner the end user is presented with the option of entering and saving their password</span></span>

<span data-ttu-id="7ac5f-113">In base al processo preferito della società per la gestione dell'autenticazione degli utenti finali, è possibile specificare se si verifica la memorizzazione delle credenziali per una specifica area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-113">Depending on your company’s preferred process for managing end-user authentication, you can specify whether credential caching occurs for a particular MED-V workspace.</span></span> <span data-ttu-id="7ac5f-114">La memorizzazione nella cache delle credenziali di un utente finale è utile perché viene richiesto solo una volta per la password.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-114">Caching the credentials of an end user is helpful because they are only prompted one time for their password.</span></span> <span data-ttu-id="7ac5f-115">Se l'utente finale non è autorizzato a salvare la password o decide di non farlo, ogni volta che avvia una nuova sessione MED-V, deve immetterla di nuovo.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-115">If the end user is not allowed to save their password or they decide not to, every time that they start a new MED-V session, they must enter it again.</span></span> <span data-ttu-id="7ac5f-116">Ad esempio, se MED-V è configurato per l'avvio quando l'utente finale accede all'host ma l'autenticazione è disabilitata, l'utente finale viene richiesto solo una volta durante l'accesso.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-116">For example, if MED-V is configured to start when the end user logs on to the host but Authentication is disabled, the end user is only prompted one time during logon.</span></span> <span data-ttu-id="7ac5f-117">In questo caso, le credenziali sono valide finché l'utente finale non si disconnette dall'host.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-117">In this case, credentials are valid until the end user logs off from the host.</span></span>

<span data-ttu-id="7ac5f-118">Se necessario, è possibile usare Gestione credenziali per rimuovere eventuali credenziali degli utenti finali archiviate.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-118">If it is necessary, you can use Credential Manager to remove any stored end-user credentials.</span></span>

<span data-ttu-id="7ac5f-119">Per impostazione predefinita, l'archiviazione delle credenziali è disabilitata, ma è possibile modificare questa impostazione con uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ac5f-119">By default, credential storing is disabled, but you can change this setting through one of the following methods:</span></span>

<span data-ttu-id="7ac5f-120">**Durante la creazione del pacchetto area di lavoro MED-V**.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-120">**While you are creating the MED-V workspace package**.</span></span> <span data-ttu-id="7ac5f-121">Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="7ac5f-121">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="7ac5f-122">**Dopo aver distribuito l'area di lavoro MED-V**.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-122">**After you have deployed the MED-V workspace**.</span></span> <span data-ttu-id="7ac5f-123">Modificare il parametro UxCredentialCacheEnabled del cmdlet MED-V per impostare la chiave del registro di sistema Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-123">Edit the MED-V cmdlet parameter UxCredentialCacheEnabled to set the Terminal Services registry key.</span></span> <span data-ttu-id="7ac5f-124">Per altre informazioni, vedere Guida di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-124">For more information, see Windows PowerShell Help.</span></span>

<span data-ttu-id="7ac5f-125">Dopo la distribuzione dell'area di lavoro MED-V, è possibile impostare la preferenza per l'autenticazione dell'utente finale modificando il criterio Servizi terminal denominato DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-125">After MED-V workspace deployment, you can set your preference for end-user authentication by modifying the Terminal Services policy named DisablePasswordSaving.</span></span> <span data-ttu-id="7ac5f-126">DisablePasswordSaving controlla se la casella di controllo salvataggio password viene visualizzata nella finestra di dialogo client RDP e se viene visualizzata la richiesta di credenziale MED-V.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-126">DisablePasswordSaving controls whether the password saving check box appears on the RDP client dialog window and whether the MED-V credential prompt is displayed.</span></span>

<span data-ttu-id="7ac5f-127">Di seguito è riportato il percorso dei criteri per il criterio Servizi terminal denominato DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-127">Following is the policy path for the Terminal Services policy named DisablePasswordSaving.</span></span>

**<span data-ttu-id="7ac5f-128">Regedit</span><span class="sxs-lookup"><span data-stu-id="7ac5f-128">Regedit:</span></span>**

<span data-ttu-id="7ac5f-129">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="7ac5f-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span></span>

**<span data-ttu-id="7ac5f-130">Nota</span><span class="sxs-lookup"><span data-stu-id="7ac5f-130">Note</span></span>**  
<span data-ttu-id="7ac5f-131">Le modifiche apportate a DisablePasswordSaving influenzano solo il prompt RDP in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-131">The changes that you make to DisablePasswordSaving only affect the RDP prompt to a virtual machine.</span></span>



<span data-ttu-id="7ac5f-132">La tabella seguente elenca i diversi modi in cui è possibile configurare le impostazioni per l'archiviazione delle credenziali e gli effetti delle diverse configurazioni:</span><span class="sxs-lookup"><span data-stu-id="7ac5f-132">The following table lists the different ways you can configure your settings for credential storing and the effects of the different configurations:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7ac5f-133">Value</span><span class="sxs-lookup"><span data-stu-id="7ac5f-133">Value</span></span></th>
<th align="left"><span data-ttu-id="7ac5f-134">Configurazione</span><span class="sxs-lookup"><span data-stu-id="7ac5f-134">Configuration</span></span></th>
<th align="left"><span data-ttu-id="7ac5f-135">Risultato</span><span class="sxs-lookup"><span data-stu-id="7ac5f-135">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ac5f-136">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="7ac5f-136">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="7ac5f-137">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="7ac5f-137">Disabled</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="7ac5f-138">Viene presentato il prompt di MED-V e una casella di controllo accetta è disponibile e deselezionata.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-138">The MED-V prompt is presented and a check box to accept is available and cleared.</span></span> <span data-ttu-id="7ac5f-139">Se l'utente finale seleziona la casella di controllo, le credenziali vengono memorizzate nella cache per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-139">If the end user selects the check box, credentials are cached for subsequent use.</span></span> <span data-ttu-id="7ac5f-140">L'utente finale ha anche il vantaggio di essere richiesto solo quando la password scade.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-140">The end user also has the benefit of only being prompted when the password expires.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="7ac5f-141">Se l'utente finale non seleziona la casella di controllo, viene visualizzata la richiesta client di connessione Desktop remoto (RDC) al posto del prompt di MED-V e la casella di controllo accetta è deselezionata.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-141">If the end user does not select the check box, the Remote Desktop Connection (RDC) Client prompt is presented instead of the MED-V prompt, and the check box to accept is cleared.</span></span> <span data-ttu-id="7ac5f-142">Se l'utente finale seleziona la casella di controllo, la credenziale del client RDC viene archiviata per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-142">If the end user selects the check box, the RDC Client credential is stored for later use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="7ac5f-143">Importante</span><span class="sxs-lookup"><span data-stu-id="7ac5f-143">Important</span></span></strong><br/><p><span data-ttu-id="7ac5f-144">RDC non convalida le credenziali quando l'utente finale li immette.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-144">RDC does not validate credentials when the end user enters them.</span></span> <span data-ttu-id="7ac5f-145">Se l'utente finale memorizza nella cache le credenziali tramite il prompt della tecnologia RDC, esiste il rischio che vengano archiviate credenziali non corrette.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-145">If the end user caches the credentials through the RDC prompt, there is a risk that incorrect credentials might be stored.</span></span> <span data-ttu-id="7ac5f-146">In questo caso, le credenziali non corrette devono essere eliminate in Gestione credenziali di Windows.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-146">In this case, the incorrect credentials must be deleted in the Windows Credential Manager.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7ac5f-147">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="7ac5f-147">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="7ac5f-148">Abilitato</span><span class="sxs-lookup"><span data-stu-id="7ac5f-148">Enabled</span></span></strong></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="7ac5f-149">Nota</span><span class="sxs-lookup"><span data-stu-id="7ac5f-149">Note</span></span></strong><br/><p><span data-ttu-id="7ac5f-150">Questa configurazione è più sicura perché non consente la memorizzazione nella cache delle credenziali degli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-150">This configuration is more secure because it does not allow end user credentials to be cached.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7ac5f-151">Per impostazione predefinita, l'installazione di MED-V imposta una chiave del registro di sistema nel guest per eliminare il prompt "password che sta per scadere".</span><span class="sxs-lookup"><span data-stu-id="7ac5f-151">By default, the MED-V installation sets a registry key in the guest to suppress the "password about to expire" prompt.</span></span> <span data-ttu-id="7ac5f-152">L'utente finale viene richiesto solo per la modifica di una password nell'host.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-152">The end user is only prompted for a password change on the host.</span></span> <span data-ttu-id="7ac5f-153">Le credenziali aggiornate nell'host vengono passate al Guest.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-153">Credentials that are updated on the host are passed to the guest.</span></span>

**<span data-ttu-id="7ac5f-154">Attenzione</span><span class="sxs-lookup"><span data-stu-id="7ac5f-154">Caution</span></span>**  
<span data-ttu-id="7ac5f-155">Se si usano criteri di gruppo nell'ambiente, verificare che sia possibile eseguire l'override della chiave del registro di sistema causando la ricomparsa delle richieste di password da parte del Guest.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-155">If you use Group Policy in your environment, know that it can override the registry key causing the password prompts from the guest to reappear.</span></span>



### <span data-ttu-id="7ac5f-156">Problemi di sicurezza con l'autenticazione</span><span class="sxs-lookup"><span data-stu-id="7ac5f-156">Security Concerns with Authentication</span></span>

<span data-ttu-id="7ac5f-157">Anche se la memorizzazione nella cache delle credenziali dell'utente finale offre la migliore esperienza utente, è necessario essere consapevoli dei rischi.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-157">Even though caching the end user’s credentials provides the best user experience, you must be aware of the risks involved.</span></span>

<span data-ttu-id="7ac5f-158">Quando la cache delle credenziali è abilitata, le credenziali di dominio dell'utente finale vengono archiviate in un formato reversibile all'interno di Windows Credential Manager.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-158">When credential caching is enabled, the end user’s domain credential is stored in a reversible format within the Windows Credential Manager.</span></span> <span data-ttu-id="7ac5f-159">Di conseguenza, un utente malintenzionato potrebbe scrivere uno strumento che viene eseguito sia come processo a livello di sistema che come processo utente finale e che recupera le credenziali dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-159">As a result, an attacker could write a tool that runs as either a system level process or an end user process and that retrieves the end user's credentials.</span></span> <span data-ttu-id="7ac5f-160">Puoi ridurre questo rischio solo impostando DisablePasswordSaving su **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-160">You can only lessen this risk by setting DisablePasswordSaving to **Enabled**.</span></span>

<span data-ttu-id="7ac5f-161">Questa stessa preoccupazione esiste quando l'autenticazione MED-V è disabilitata, ma l'impostazione dei criteri Servizi terminal è abilitata.</span><span class="sxs-lookup"><span data-stu-id="7ac5f-161">This same concern exists when MED-V authentication is disabled but the Terminal Services policy setting is enabled.</span></span>

## <span data-ttu-id="7ac5f-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ac5f-162">Related topics</span></span>


[<span data-ttu-id="7ac5f-163">Procedure consigliate per le operazioni MED-V</span><span class="sxs-lookup"><span data-stu-id="7ac5f-163">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)









