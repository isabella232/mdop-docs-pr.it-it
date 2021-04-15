---
title: Configurazione di UE-V 2.x con oggetti Criteri di gruppo
description: Configurazione di UE-V 2.x con oggetti Criteri di gruppo
author: dansimp
ms.assetid: 2bb55834-26ee-4f19-9860-dfdf3c797143
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b6c9636df36a53cbf65bf1904965f2809484b99c
ms.sourcegitcommit: bdc377477a8cc9e973fbcdd67c2f07b882c5d61e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "11494061"
---
# <a name="configuring-ue-v-2x-with-group-policy-objects"></a><span data-ttu-id="0ec7f-103">Configurazione di UE-V 2.x con oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0ec7f-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="0ec7f-104">Alcune impostazioni di Criteri di gruppo di Microsoft User Experience Virtualization (UE-V) 2.0, 2.1 e 2.1 SP1 possono essere definite per i computer e altre impostazioni di Criteri di gruppo possono essere definite per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="0ec7f-105">Per informazioni su come installare i file ADMX di Criteri di gruppo UE-V, vedere [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span><span class="sxs-lookup"><span data-stu-id="0ec7f-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="0ec7f-106">Le impostazioni dei criteri seguenti possono essere configurate per UE-V.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="0ec7f-107">Impostazioni di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0ec7f-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0ec7f-108">Nome dell'impostazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0ec7f-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="0ec7f-109">Target</span><span class="sxs-lookup"><span data-stu-id="0ec7f-109">Target</span></span></th>
<th align="left"><span data-ttu-id="0ec7f-110">Descrizione dell'impostazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0ec7f-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="0ec7f-111">Opzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="0ec7f-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ec7f-112">Configure Sync, metodo</span><span class="sxs-lookup"><span data-stu-id="0ec7f-112">Configure Sync Method</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-113">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-114">Utilizzando questa impostazione di Criteri di gruppo, è possibile configurare se User Experience Virtualization (UE-V) usa la funzionalità del provider di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-114">By using this Group Policy setting, you can configure whether User Experience Virtualization (UE-V) uses the sync provider feature.</span></span> <span data-ttu-id="0ec7f-115">Questa impostazione dei criteri consente inoltre di abilitare la visualizzazione di una notifica quando l'importazione delle impostazioni utente viene ritardata.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-115">This policy setting also lets you enable a notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-116">Abilitare questa impostazione per configurare l'agente UE-V in modo che non utilizzi il provider di sincronizzazione o che utilizzi il motore di sincronizzazione esterno.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-116">Enable this setting to configure the UE-V agent not to use the sync provider, or to use the external synchronization engine.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ec7f-117">Testo collegamento IT contatto</span><span class="sxs-lookup"><span data-stu-id="0ec7f-117">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-118">Solo computer</span><span class="sxs-lookup"><span data-stu-id="0ec7f-118">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-119">Questa impostazione di Criteri di gruppo consente di specificare il testo del collegamento ipertestuale URL IT contatto nel Centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-119">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-120">Se si abilita questa impostazione di Criteri di gruppo, nel Centro impostazioni società verrà visualizzato il testo specificato nel collegamento all'URL IT contatto.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-120">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ec7f-121">CONTATTA L'URL IT</span><span class="sxs-lookup"><span data-stu-id="0ec7f-121">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-122">Solo computer</span><span class="sxs-lookup"><span data-stu-id="0ec7f-122">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-123">Questa impostazione di Criteri di gruppo consente di specificare l'URL per il collegamento IT Contatto nel Centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-123">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-124">Se si abilita questa impostazione, il Centro impostazioni società collega il testo IT all'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-124">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="0ec7f-125">Il collegamento può essere di qualsiasi protocollo standard, ad esempio HTTP o mailto.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-125">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ec7f-126">Notifica di primo utilizzo</span><span class="sxs-lookup"><span data-stu-id="0ec7f-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-127">Solo computer</span><span class="sxs-lookup"><span data-stu-id="0ec7f-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-128">Questa impostazione di Criteri di gruppo abilita una notifica nell'area di notifica visualizzata quando ue-V</span><span class="sxs-lookup"><span data-stu-id="0ec7f-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="0ec7f-129">l'agente viene eseguito per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-130">Il valore predefinito è abilitato.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ec7f-131">Eseguire il ping del percorso di archiviazione delle impostazioni prima della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="0ec7f-131">Ping the settings storage location before sync</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-132">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-133">Questa impostazione dei criteri consente alla configurazione del provider di sincronizzazione UE-V di eseguire il ping del percorso di archiviazione delle impostazioni prima di tentare di sincronizzare le impostazioni per verificare la connessione.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-133">This policy setting allows configuration of the UE-V sync provider to ping the settings storage path before attempting to sync settings in order to verify the connection.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-134">Abilita o disabilita questa impostazione di Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-134">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ec7f-135">Soglia di avviso dimensioni pacchetto impostazioni</span><span class="sxs-lookup"><span data-stu-id="0ec7f-135">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-136">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-136">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-137">Questa impostazione di Criteri di gruppo consente di configurare l'agente UE-V per segnalare quando le dimensioni del file di un pacchetto di impostazioni raggiungono una soglia definita.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-137">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-138">Specificare la soglia preferita per le dimensioni dei pacchetti di impostazioni in kilobyte (KB).</span><span class="sxs-lookup"><span data-stu-id="0ec7f-138">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="0ec7f-139">Per impostazione predefinita, l'agente UE-V non ha una soglia per le dimensioni del file del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-139">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ec7f-140">Percorso di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="0ec7f-140">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-141">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-141">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-142">Questa impostazione di Criteri di gruppo consente di configurare la posizione in cui devono essere archiviate le impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-142">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-143">Immettere un percorso UNC (Universal Naming Convention) e variabili quali \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-143">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ec7f-144">Percorso del catalogo dei modelli di impostazioni</span><span class="sxs-lookup"><span data-stu-id="0ec7f-144">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-145">Solo computer</span><span class="sxs-lookup"><span data-stu-id="0ec7f-145">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-146">Questa impostazione di Criteri di gruppo consente di configurare la posizione in cui vengono archiviati i modelli di percorso delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-146">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="0ec7f-147">Questa impostazione dei criteri consente inoltre di configurare se il catalogo deve essere utilizzato per sostituire i modelli Microsoft predefiniti installati con l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-147">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-148">Immettere un percorso UNC (Universal Naming Convention), ad esempio \Server\Condivisione Template o un percorso di cartella nel computer.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-148">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="0ec7f-149">Selezionare la casella di controllo per sostituire i modelli Microsoft predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-149">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ec7f-150">Sincronizzazione delle impostazioni su connessioni a consumo</span><span class="sxs-lookup"><span data-stu-id="0ec7f-150">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-151">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-151">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-152">Questa impostazione di Criteri di gruppo definisce se UE-V sincronizza le impostazioni su connessioni a consumo.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-152">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-153">Per impostazione predefinita, l'agente UE-V non sincronizza le impostazioni su una connessione a consumo.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-153">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ec7f-154">Sincronizzare le impostazioni su connessioni a consumo anche quando si esegue il roaming</span><span class="sxs-lookup"><span data-stu-id="0ec7f-154">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-155">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-155">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-156">Questa impostazione di Criteri di gruppo definisce se UE-V sincronizza le impostazioni su connessioni a consumo esterne alla rete del provider principale, ad esempio quando la connessione dati è in modalità roaming.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-156">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-157">Per impostazione predefinita, UE-V non sincronizza le impostazioni su una connessione a consumo quando è in modalità roaming.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-157">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ec7f-158">Timeout sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="0ec7f-158">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-159">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-159">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-160">Questa impostazione di Criteri di gruppo configura il numero di millisecondi che il computer attende prima di un timeout quando recupera le impostazioni utente dalla posizione delle impostazioni remote.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-160">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="0ec7f-161">Se il percorso di archiviazione remota non è disponibile e l'utente non utilizza il provider di sincronizzazione, l'avvio dell'applicazione viene ritardato di questo numero di millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-161">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-162">Specificare il timeout di sincronizzazione preferito in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-162">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="0ec7f-163">Il valore predefinito è 2000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-163">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ec7f-164">Sincronizzare le impostazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="0ec7f-164">Synchronize Windows settings</span></span> </p></td>
<td align="left"><p><span data-ttu-id="0ec7f-165">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-165">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-166">Questa impostazione di Criteri di gruppo configura la sincronizzazione delle impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-166">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-167">Selezionare le impostazioni di Windows da sincronizzare tra i computer.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-167">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="0ec7f-168">Per impostazione predefinita, i temi di Windows, le impostazioni del desktop e le impostazioni di Accessibilità sincronizzano le impostazioni tra i computer della stessa versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-168">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ec7f-169">Icona Cassetto</span><span class="sxs-lookup"><span data-stu-id="0ec7f-169">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-170">Solo computer</span><span class="sxs-lookup"><span data-stu-id="0ec7f-170">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-171">Questa impostazione di Criteri di gruppo abilita l'icona cassetto UE-V.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-171">This Group Policy setting enables the UE-V tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-172">Il valore predefinito è abilitato.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-172">The default is enabled.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ec7f-173">Usare User Experience Virtualization (UE-V)</span><span class="sxs-lookup"><span data-stu-id="0ec7f-173">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-174">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-174">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-175">Questa impostazione di Criteri di gruppo consente di abilitare o disabilitare UE-V.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-175">This Group Policy setting lets you enable or disable UE-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-176">Abilita o disabilita questa impostazione di Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-176">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ec7f-177">Configurazione VDI</span><span class="sxs-lookup"><span data-stu-id="0ec7f-177">VDI Configuration</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-178">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-178">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-179">Questa impostazione dei criteri configura la sincronizzazione delle informazioni di rollback UE-V per i computer in esecuzione in un ambiente VDI in pool.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-179">This policy setting configures the synchronization of UE-V rollback information for computers running in a pooled VDI environment.</span></span> <span data-ttu-id="0ec7f-180">Se questo criterio è abilitato, lo stato di rollback di UE-V viene copiato nel percorso di archiviazione delle impostazioni al logout e ripristinato all'accesso.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-180">If this policy is enabled, the UE-V rollback state is copied to the settings storage location on logout and restored on login.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-181">Abilita o disabilita questa impostazione di Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-181">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="0ec7f-182">Nota</span><span class="sxs-lookup"><span data-stu-id="0ec7f-182">Note</span></span>**  
<span data-ttu-id="0ec7f-183">Inoltre, le impostazioni di Criteri di gruppo sono disponibili per molte applicazioni desktop e app di Windows.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-183">In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="0ec7f-184">È possibile utilizzare queste impostazioni per abilitare o disabilitare la sincronizzazione delle impostazioni per applicazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-184">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="0ec7f-185">Impostazioni di Criteri di gruppo per le app di Windows</span><span class="sxs-lookup"><span data-stu-id="0ec7f-185">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="0ec7f-186">Nome dell'impostazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0ec7f-186">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="0ec7f-187">Target</span><span class="sxs-lookup"><span data-stu-id="0ec7f-187">Target</span></span></th>
<th align="left"><span data-ttu-id="0ec7f-188">Descrizione dell'impostazione di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="0ec7f-188">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="0ec7f-189">Opzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="0ec7f-189">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ec7f-190">Non sincronizzare le app di Windows</span><span class="sxs-lookup"><span data-stu-id="0ec7f-190">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-191">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="0ec7f-191">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-192">Questa impostazione di Criteri di gruppo definisce se l'agente UE-V sincronizza le impostazioni per le app di Windows.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-192">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-193">L'impostazione predefinita è la sincronizzazione delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-193">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="0ec7f-194">Elenco app di Windows</span><span class="sxs-lookup"><span data-stu-id="0ec7f-194">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-195">Computer e utente</span><span class="sxs-lookup"><span data-stu-id="0ec7f-195">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-196">Questa impostazione elenca i nomi dei pacchetti di famiglia delle app di Windows e indica espressamente se UE-V sincronizza le impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-196">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-197">Puoi usare questa impostazione per specificare che le impostazioni di un'app non vengono mai sincronizzate da UE-V, anche se le impostazioni di tutte le altre app di Windows sono sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-197">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="0ec7f-198">Sincronizza app di Windows non in elenco</span><span class="sxs-lookup"><span data-stu-id="0ec7f-198">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-199">Computer e utente</span><span class="sxs-lookup"><span data-stu-id="0ec7f-199">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-200">Questa impostazione di Criteri di gruppo definisce il comportamento di sincronizzazione delle impostazioni predefinite dell'agente UE-V per le app di Windows che non sono esplicitamente elencate nell'elenco delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-200">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="0ec7f-201">Per impostazione predefinita, l'agente UE-V sincronizza solo le impostazioni delle app di Windows incluse nell'elenco delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-201">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="0ec7f-202">Per altre informazioni sulla sincronizzazione delle app di Windows, vedi [Elenco app di Windows.](https://technet.microsoft.com/library/dn458925.aspx#win8applist)</span><span class="sxs-lookup"><span data-stu-id="0ec7f-202">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="0ec7f-203">Per configurare le impostazioni di Criteri di gruppo di destinazione del computer</span><span class="sxs-lookup"><span data-stu-id="0ec7f-203">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="0ec7f-204">Utilizzare console Gestione Criteri di gruppo (GPMC) o Gestione avanzata Criteri di gruppo (AGPM) nel computer che funge da controller di dominio per gestire le impostazioni di Criteri di gruppo per i computer UE-V.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-204">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="0ec7f-205">Passare a **Configurazione computer,** selezionare **Criteri,** **modelli**amministrativi, fare clic su Componenti di **Windows**e quindi selezionare Microsoft User **Experience Virtualization.**</span><span class="sxs-lookup"><span data-stu-id="0ec7f-205">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="0ec7f-206">Selezionare l'impostazione di Criteri di gruppo da modificare.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-206">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="0ec7f-207">Per configurare le impostazioni di Criteri di gruppo mirate all'utente</span><span class="sxs-lookup"><span data-stu-id="0ec7f-207">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="0ec7f-208">Utilizzare la Console Gestione Criteri di gruppo (GPMC) o lo strumento Gestione avanzata Criteri di gruppo (AGPM) in Microsoft Desktop Optimization Pack (MDOP) nel computer controller di dominio per gestire le impostazioni di Criteri di gruppo per UE-V.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-208">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="0ec7f-209">Passare a **Configurazione utente,** selezionare **Criteri,** **modelli**amministrativi, fare clic su Componenti di **Windows**e quindi selezionare Microsoft User **Experience Virtualization.**</span><span class="sxs-lookup"><span data-stu-id="0ec7f-209">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="0ec7f-210">Selezionare l'impostazione di Criteri di gruppo modificata.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-210">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="0ec7f-211">L'agente UE-V usa il seguente ordine di precedenza per determinare la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-211">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="0ec7f-212">Ordine di precedenza per le impostazioni UE-V</span><span class="sxs-lookup"><span data-stu-id="0ec7f-212">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="0ec7f-213">Impostazioni di destinazione dell'utente gestite dalle impostazioni di Criteri di gruppo- Queste impostazioni di configurazione vengono archiviate nella chiave del Registro di sistema da Criteri di gruppo in `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="0ec7f-213">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="0ec7f-214">Impostazioni di destinazione del computer gestite dalle impostazioni di Criteri di gruppo - Queste impostazioni di configurazione vengono archiviate nella chiave del Registro di sistema da Criteri di gruppo in `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="0ec7f-214">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="0ec7f-215">Impostazioni di configurazione definite dall'utente corrente tramite Windows PowerShell o Strumentazione gestione Windows (WMI): queste impostazioni di configurazione vengono archiviate dall'agente UE-V in questo percorso del Registro di sistema: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="0ec7f-215">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="0ec7f-216">Impostazioni di configurazione definite per il computer tramite Windows PowerShell o WMI.</span><span class="sxs-lookup"><span data-stu-id="0ec7f-216">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="0ec7f-217">Queste impostazioni di configurazione vengono archiviate dall'agente UE-V in questo percorso del Registro di sistema: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="0ec7f-217">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="0ec7f-218">**Hai un suggerimento per UE-V**?</span><span class="sxs-lookup"><span data-stu-id="0ec7f-218">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="0ec7f-219">Aggiungere o votare i suggerimenti [qui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="0ec7f-219">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="0ec7f-220">**Hai un problema di UE-V?**</span><span class="sxs-lookup"><span data-stu-id="0ec7f-220">**Got a UE-V issue**?</span></span> <span data-ttu-id="0ec7f-221">Usa il [forum TechNet UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="0ec7f-221">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ec7f-222">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ec7f-222">Related topics</span></span>


[<span data-ttu-id="0ec7f-223">Amministrazione di UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="0ec7f-223">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="0ec7f-224">Gestire le configurazioni per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="0ec7f-224">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 
