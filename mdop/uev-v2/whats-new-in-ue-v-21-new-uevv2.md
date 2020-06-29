---
title: Novità in UE-V 2.1
description: Novità in UE-V 2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826265"
---
# <span data-ttu-id="b91fb-103">Novità in UE-V 2.1</span><span class="sxs-lookup"><span data-stu-id="b91fb-103">What's New in UE-V 2.1</span></span>


<span data-ttu-id="b91fb-104">User Experience Virtualization 2,1 offre queste nuove funzionalità e funzionalità rispetto a UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="b91fb-104">User Experience Virtualization 2.1 provides these new features and functionality compared to UE-V 2.0.</span></span> <span data-ttu-id="b91fb-105">Le [Note sulla versione di Microsoft User Experience Virtualization (UE-v) 2,1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) contengono ulteriori informazioni sulla versione UE-v 2,1.</span><span class="sxs-lookup"><span data-stu-id="b91fb-105">The [Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) provide more information about the UE-V 2.1 release.</span></span>

## <span data-ttu-id="b91fb-106">Modello di posizione delle impostazioni di Office 2013</span><span class="sxs-lookup"><span data-stu-id="b91fb-106">Office 2013 Settings Location Template</span></span>


<span data-ttu-id="b91fb-107">UE-V 2,1 include il modello di posizione delle impostazioni di Microsoft Office 2013 con il supporto per la firma di Outlook migliorato.</span><span class="sxs-lookup"><span data-stu-id="b91fb-107">UE-V 2.1 includes the Microsoft Office 2013 settings location template with improved Outlook signature support.</span></span> <span data-ttu-id="b91fb-108">In UE-V 2,1 i dati della firma vengono sincronizzati tra i dispositivi utente.</span><span class="sxs-lookup"><span data-stu-id="b91fb-108">In UE-V 2.1, the signature data synchronizes between user devices.</span></span> <span data-ttu-id="b91fb-109">È stata aggiunta la sincronizzazione delle impostazioni predefinite della firma per i messaggi di posta elettronica nuovi, di risposta e inoltrati.</span><span class="sxs-lookup"><span data-stu-id="b91fb-109">We’ve added synchronization of default signature settings for new, reply, and forwarded emails.</span></span> <span data-ttu-id="b91fb-110">I clienti non devono più scegliere le impostazioni predefinite della firma.</span><span class="sxs-lookup"><span data-stu-id="b91fb-110">Customers no longer have to choose the default signature settings.</span></span>

<span data-ttu-id="b91fb-111">**Nota**  È necessario creare un profilo di Outlook per qualsiasi dispositivo in cui un utente vuole sincronizzare la firma di Outlook.</span><span class="sxs-lookup"><span data-stu-id="b91fb-111">**Note** An Outlook profile must be created for any device on which a user wants to sync their Outlook signature.</span></span> <span data-ttu-id="b91fb-112">Se il profilo non è già stato creato, l'utente può crearne uno e quindi riavviare Outlook in tale dispositivo per abilitare la sincronizzazione della firma.</span><span class="sxs-lookup"><span data-stu-id="b91fb-112">If the profile is not already created, the user can create one and then restart Outlook on that device to enable signature synchronization.</span></span>

 

<span data-ttu-id="b91fb-113">In precedenza la versione UE-V includeva i modelli di posizione delle impostazioni di Microsoft Office 2010 distribuiti automaticamente e registrati con l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="b91fb-113">Previously UE-V included Microsoft Office 2010 settings location templates that were automatically distributed and registered with the UE-V Agent.</span></span> <span data-ttu-id="b91fb-114">UE-V 2,1 funziona con Office 365 per determinare se le impostazioni di Office 2013 sono in roaming da Office 365.</span><span class="sxs-lookup"><span data-stu-id="b91fb-114">UE-V 2.1 works with Office 365 to determine whether Office 2013 settings are roamed by Office 365.</span></span> <span data-ttu-id="b91fb-115">Se le impostazioni sono in roaming con Office 365, non vengono spostate in roaming da UE-V.</span><span class="sxs-lookup"><span data-stu-id="b91fb-115">If settings are roamed by Office 365 they are not roamed by UE-V.</span></span> <span data-ttu-id="b91fb-116">[Panoramica delle impostazioni utente e roaming per Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) offre ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="b91fb-116">[Overview of user and roaming settings for Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) provides more information.</span></span>

<span data-ttu-id="b91fb-117">Per abilitare la sincronizzazione delle impostazioni tramite UE-V 2,1, eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b91fb-117">To enable settings synchronization using UE-V 2.1, do one of the following:</span></span>

-   <span data-ttu-id="b91fb-118">Usare criteri di gruppo per disabilitare la sincronizzazione di Office 365</span><span class="sxs-lookup"><span data-stu-id="b91fb-118">Use Group Policy to disable Office 365 synchronization</span></span>

-   <span data-ttu-id="b91fb-119">Non abilitare l'esperienza di sincronizzazione di Office 365 durante l'installazione di Office 2013</span><span class="sxs-lookup"><span data-stu-id="b91fb-119">Do not enable the Office 365 synchronization experience during Office 2013 installation</span></span>

<span data-ttu-id="b91fb-120">UE-V 2,1 include i [modelli di office 2013 e office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span><span class="sxs-lookup"><span data-stu-id="b91fb-120">UE-V 2.1 ships [Office 2013 and Office 2010 templates](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).</span></span> <span data-ttu-id="b91fb-121">Questa versione rimuove i modelli di Office 2007.</span><span class="sxs-lookup"><span data-stu-id="b91fb-121">This release removes the Office 2007 templates.</span></span> <span data-ttu-id="b91fb-122">Gli utenti possono ancora usare i modelli di Office 2007 da UE-V 2,0 o versioni precedenti e possono ancora ottenere i modelli dalla raccolta modelli di UE-V che si trova [qui](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span><span class="sxs-lookup"><span data-stu-id="b91fb-122">Users can still use Office 2007 templates from UE-V 2.0 or earlier and can still get the templates from the UE-V template gallery located [here](https://go.microsoft.com/fwlink/p/?LinkID=246589).</span></span>

## <span data-ttu-id="b91fb-123">Correzione per gli utenti dello spazio dei nomi Distributed file System</span><span class="sxs-lookup"><span data-stu-id="b91fb-123">Fix for Distributed File System Namespace Users</span></span>


<span data-ttu-id="b91fb-124">In UE-V è stato migliorato il supporto dello spazio dei nomi Distributed file System (DFSN) aggiungendo una configurazione UE-V denominata SyncProviderPingEnabled.</span><span class="sxs-lookup"><span data-stu-id="b91fb-124">UE-V has improved Distributed File System Namespace (DFSN) support by adding a UE-V configuration called SyncProviderPingEnabled.</span></span> <span data-ttu-id="b91fb-125">La disattivazione di questa configurazione tramite PowerShell o WMI consente agli utenti di disabilitare il ping di UE-V.</span><span class="sxs-lookup"><span data-stu-id="b91fb-125">Disabling this configuration using PowerShell or WMI allows users to disable the UE-V ping.</span></span> <span data-ttu-id="b91fb-126">Il ping di UE-V causa un errore quando si usano i server di DFSN perché questi server non rispondono ai ping.</span><span class="sxs-lookup"><span data-stu-id="b91fb-126">The UE-V ping causes an error when using DFSN servers because these servers do not respond to pings.</span></span> <span data-ttu-id="b91fb-127">La mancata risposta impedisce la sincronizzazione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="b91fb-127">The non-response prevents UE-V from synchronizing settings.</span></span> <span data-ttu-id="b91fb-128">La disabilitazione del ping UE-V consente la sincronizzazione di UE-V in modo che funzioni normalmente.</span><span class="sxs-lookup"><span data-stu-id="b91fb-128">Disabling the UE-V ping allows UE-V synchronization to work normally.</span></span>

<span data-ttu-id="b91fb-129">Per disabilitare il ping di UE-V, usare questo cmdlet di PowerShell:</span><span class="sxs-lookup"><span data-stu-id="b91fb-129">To disable UE-V ping, use this PowerShell cmdlet:</span></span>

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## <span data-ttu-id="b91fb-130">Sincronizzazione per le credenziali</span><span class="sxs-lookup"><span data-stu-id="b91fb-130">Synchronization for Credentials</span></span>


<span data-ttu-id="b91fb-131">UE-V 2,1 offre ai clienti la possibilità di sincronizzare credenziali e certificati archiviati in Gestione credenziali di Windows.</span><span class="sxs-lookup"><span data-stu-id="b91fb-131">UE-V 2.1 gives customers the ability to synchronize credentials and certificates stored in the Windows Credential Manager.</span></span> <span data-ttu-id="b91fb-132">Questo componente è disabilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b91fb-132">This component is disabled by default.</span></span> <span data-ttu-id="b91fb-133">L'attivazione di questo componente consente agli utenti di conservare le credenziali di dominio e i certificati in sincronia. Gli utenti possono eseguire l'accesso una sola volta su un dispositivo e queste credenziali verranno spostate per l'utente in tutti i dispositivi abilitati per l'UE-V.</span><span class="sxs-lookup"><span data-stu-id="b91fb-133">Enabling this component lets users keep their domain credentials and certificates in sync. Users can sign in one time on a device, and these credentials will roam for that user across all of their UE-V enabled devices.</span></span> <span data-ttu-id="b91fb-134">[Gestisci le credenziali con UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) offre ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="b91fb-134">[Manage Credentials with UE-V 2.1](https://technet.microsoft.com/library/dn458932.aspx#creds) provides more information.</span></span>

<span data-ttu-id="b91fb-135">**Nota**  In Windows 8 e versioni successive, gestione credenziali contiene le credenziali Web.</span><span class="sxs-lookup"><span data-stu-id="b91fb-135">**Note** In Windows 8 and later, Credential Manager contains web credentials.</span></span> <span data-ttu-id="b91fb-136">Queste credenziali non vengono sincronizzate tra i dispositivi degli utenti.</span><span class="sxs-lookup"><span data-stu-id="b91fb-136">These credentials are not synchronized between users’ devices.</span></span>

 

## <span data-ttu-id="b91fb-137">Sincronizzazione dell'account UE-V e Microsoft</span><span class="sxs-lookup"><span data-stu-id="b91fb-137">UE-V and Microsoft Account Synchronization</span></span>


<span data-ttu-id="b91fb-138">UE-V rileva se "impostazioni di sincronizzazione con OneDrive", nota anche come sincronizzazione dell'account Microsoft, è attivata.</span><span class="sxs-lookup"><span data-stu-id="b91fb-138">UE-V detects if “Sync settings with OneDrive”, also known as Microsoft Account synchronization, is on.</span></span> <span data-ttu-id="b91fb-139">Se l'account Microsoft non è configurato per la sincronizzazione delle impostazioni, UE-V sincronizza le app di Windows, i pacchetti AppX e le impostazioni desktop di Windows tra i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="b91fb-139">If the Microsoft Account is not configured to synchronize settings, UE-V synchronizes Windows apps, AppX packages, and Windows desktop settings between devices.</span></span> <span data-ttu-id="b91fb-140">Ciò consente agli utenti di accedere alle app dello Store, alla musica, alle immagini e ad altre applicazioni Microsoft per l'account, senza eseguire la sincronizzazione all'esterno del firewall aziendale.</span><span class="sxs-lookup"><span data-stu-id="b91fb-140">This lets users access their Store apps, music, pictures and other Microsoft Account-enabled applications without syncing outside of the enterprise firewall.</span></span> <span data-ttu-id="b91fb-141">UE-V controlla se i criteri di gruppo interrompono la sincronizzazione delle impostazioni con OneDrive o se l'utente disabilita la **sincronizzazione delle impostazioni di questo computer** nei controlli utente.</span><span class="sxs-lookup"><span data-stu-id="b91fb-141">UE-V checks whether Group Policy will stop synchronizing settings with OneDrive or if the user disables **Sync your settings on this computer** in the user controls.</span></span>

## <span data-ttu-id="b91fb-142">Supporto per il SyncMethod External</span><span class="sxs-lookup"><span data-stu-id="b91fb-142">Support for the SyncMethod External</span></span>


<span data-ttu-id="b91fb-143">Una nuova [configurazione di SyncMethod](https://technet.microsoft.com/library/dn554321.aspx) denominata **External** specifica che se le impostazioni di UE-V vengono scritte in una cartella locale nel computer utente, è possibile usare qualsiasi motore di sincronizzazione esterno, ad esempio OneDrive for business, cartelle di lavoro, SharePoint o Dropbox, per applicare queste impostazioni ai diversi computer a cui gli utenti accedono.</span><span class="sxs-lookup"><span data-stu-id="b91fb-143">A new [SyncMethod configuration](https://technet.microsoft.com/library/dn554321.aspx) called **External** specifies that if UE-V settings are written to a local folder on the user computer, then any external sync engine (such as OneDrive for Business, Work Folders, Sharepoint, or Dropbox) can be used to apply these settings to the different computers that users access.</span></span>

## <span data-ttu-id="b91fb-144">Supporto avanzato per la modalità VDI</span><span class="sxs-lookup"><span data-stu-id="b91fb-144">Enhanced Support for VDI Mode</span></span>


<span data-ttu-id="b91fb-145">UE-V 2,1 include il [supporto per le sessioni VDI](https://technet.microsoft.com/library/dn458932.aspx#vdi) condivise tra gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="b91fb-145">UE-V 2.1 includes [support for VDI sessions](https://technet.microsoft.com/library/dn458932.aspx#vdi) that are shared among end users.</span></span> <span data-ttu-id="b91fb-146">Come amministratore, puoi registrare e configurare uno speciale modello VDI, garantendo che UE-V mantenga intatte tutte le sue funzionalità per le sessioni VDI non persistenti.</span><span class="sxs-lookup"><span data-stu-id="b91fb-146">As an administrator, you can register and configure a special VDI template, which ensures that UE-V keeps all of its functionality intact for non-persistent VDI sessions.</span></span>

<span data-ttu-id="b91fb-147">**Nota**  Se non si Abilita la modalità VDI per le sessioni VDI non persistenti, alcune caratteristiche non funzionano, ad esempio backup/ripristino e LKG.</span><span class="sxs-lookup"><span data-stu-id="b91fb-147">**Note** If you do not enable VDI mode for non-persistent VDI sessions, certain features do not work, such as back-up/restore and LKG.</span></span>

 

## <span data-ttu-id="b91fb-148">Backup e ripristino amministrativi</span><span class="sxs-lookup"><span data-stu-id="b91fb-148">Administrative Backup and Restore</span></span>


<span data-ttu-id="b91fb-149">Puoi ripristinare altre impostazioni quando un utente adotta un nuovo dispositivo inserendo un modello di posizione di impostazioni nel profilo di **backup** o **roaming (impostazione predefinita)** usando il cmdlet Set-UevTemplateProfile di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b91fb-149">You can restore additional settings when a user adopts a new device by putting a settings location template in **backup** or **roam (default)** profile using the Set-UevTemplateProfile PowerShell cmdlet.</span></span> <span data-ttu-id="b91fb-150">In questo modo, le impostazioni del computer vengono sincronizzate con il nuovo computer, oltre alle impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="b91fb-150">This lets computer settings sync to the new computer, in addition to user settings.</span></span> <span data-ttu-id="b91fb-151">I modelli assegnati al profilo di backup vengono backup per il dispositivo e configurati in base al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b91fb-151">Templates assigned to the backup profile are backed up for that device and configured on a per-device basis.</span></span> <span data-ttu-id="b91fb-152">[Gestire il backup e il ripristino amministrativi in UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) offre ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="b91fb-152">[Manage Administrative Backup and Restore in UE-V 2.x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) provides more information.</span></span>

## <span data-ttu-id="b91fb-153">Sincronizzazione per altre impostazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="b91fb-153">Synchronization for Additional Windows Settings</span></span>


<span data-ttu-id="b91fb-154">UE-V Sincronizza ora la personalizzazione della tastiera virtuale, il dizionario ortografico e consente l'attivazione dell'app per le app recenti e le impostazioni del bordo dello schermo per la sincronizzazione tra dispositivi Windows 8 e Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="b91fb-154">UE-V now synchronizes touch keyboard personalization, the spelling dictionary, and enables the App Switching for recent apps and screen edge settings to synchronize between Windows 8 and Windows 8.1 devices.</span></span>






## <span data-ttu-id="b91fb-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b91fb-155">Related topics</span></span>


[<span data-ttu-id="b91fb-156">Introduzione a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="b91fb-156">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="b91fb-157">Preparare una distribuzione UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="b91fb-157">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="b91fb-158">Note sulla versione di Microsoft User Experience Virtualization (UE-V) 2.1</span><span class="sxs-lookup"><span data-stu-id="b91fb-158">Microsoft User Experience Virtualization (UE-V) 2.1 Release Notes</span></span>](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





