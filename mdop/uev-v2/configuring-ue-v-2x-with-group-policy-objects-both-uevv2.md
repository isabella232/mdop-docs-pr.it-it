---
title: Configurazione di UE-V 2. x con gli oggetti Criteri di gruppo
description: Configurazione di UE-V 2. x con gli oggetti Criteri di gruppo
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
ms.openlocfilehash: bdff63b948752b9bec83e77e275f1cb20a384463
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824425"
---
# <span data-ttu-id="6383a-103">Configurazione di UE-V 2. x con gli oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6383a-103">Configuring UE-V 2.x with Group Policy Objects</span></span>


<span data-ttu-id="6383a-104">Alcune impostazioni di criteri di gruppo di Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 e 2,1 SP1 possono essere definite per i computer e le altre impostazioni di criteri di gruppo possono essere definite per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="6383a-104">Some Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 Group Policy settings can be defined for computers, and other Group Policy settings can be defined for users.</span></span> <span data-ttu-id="6383a-105">Per informazioni su come installare i file ADMX di criteri di gruppo UE-V, vedere [installare i modelli ADMX di criteri di gruppo UE-v 2](https://technet.microsoft.com/library/dn458891.aspx#admx).</span><span class="sxs-lookup"><span data-stu-id="6383a-105">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V 2 Group Policy ADMX Templates](https://technet.microsoft.com/library/dn458891.aspx#admx).</span></span>

<span data-ttu-id="6383a-106">Le impostazioni dei criteri seguenti possono essere configurate per la versione UE-V.</span><span class="sxs-lookup"><span data-stu-id="6383a-106">The following policy settings can be configured for UE-V.</span></span>

**<span data-ttu-id="6383a-107">Impostazioni di Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6383a-107">Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6383a-108">Nome dell'impostazione di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6383a-108">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="6383a-109">Target</span><span class="sxs-lookup"><span data-stu-id="6383a-109">Target</span></span></th>
<th align="left"><span data-ttu-id="6383a-110">Descrizione dell'impostazione di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6383a-110">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="6383a-111">Opzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="6383a-111">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6383a-112">Contattare il testo del collegamento</span><span class="sxs-lookup"><span data-stu-id="6383a-112">Contact IT Link Text</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-113">Solo computer</span><span class="sxs-lookup"><span data-stu-id="6383a-113">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-114">Questa impostazione di criteri di gruppo specifica il testo del collegamento ipertestuale contatto URL nel centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="6383a-114">This Group Policy setting specifies the text of the Contact IT URL hyperlink in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-115">Se si abilita questa impostazione di criteri di gruppo, il centro impostazioni società Visualizza il testo specificato nel collegamento all'URL del contatto.</span><span class="sxs-lookup"><span data-stu-id="6383a-115">If you enable this Group Policy setting, the Company Settings Center displays the specified text in the link to the Contact IT URL.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6383a-116">URL contatti</span><span class="sxs-lookup"><span data-stu-id="6383a-116">Contact IT URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-117">Solo computer</span><span class="sxs-lookup"><span data-stu-id="6383a-117">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-118">Questa impostazione di criteri di gruppo specifica l'URL del collegamento contatto IT nel centro impostazioni società.</span><span class="sxs-lookup"><span data-stu-id="6383a-118">This Group Policy setting specifies the URL for the Contact IT link in the Company Settings Center.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-119">Se si abilita questa impostazione, il centro impostazioni società Contatta i collegamenti di testo all'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="6383a-119">If you enable this setting, the Company Settings Center Contact IT text links to the specified URL.</span></span> <span data-ttu-id="6383a-120">Il collegamento può essere di qualsiasi protocollo standard, ad esempio HTTP o mailto.</span><span class="sxs-lookup"><span data-stu-id="6383a-120">The link can be of any standard protocol, such as HTTP or mailto.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6383a-121">Non usare il provider di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="6383a-121">Do not use the sync provider</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-122">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="6383a-122">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-123">Usando questa impostazione di criteri di gruppo, è possibile specificare se la funzionalità provider di sincronizzazione viene usata da UE-V.</span><span class="sxs-lookup"><span data-stu-id="6383a-123">By using this Group Policy setting, you can configure whether UE-V uses the sync provider feature.</span></span> <span data-ttu-id="6383a-124">Questa impostazione dei criteri consente inoltre di attivare la notifica quando l'importazione delle impostazioni utente viene ritardata.</span><span class="sxs-lookup"><span data-stu-id="6383a-124">This policy setting also lets you enable notification to appear when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-125">Abilitare questa impostazione per configurare l'agente UE-V per non usare il provider di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6383a-125">Enable this setting to configure the UE-V Agent not to use the sync provider.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6383a-126">Notifica primo utilizzo</span><span class="sxs-lookup"><span data-stu-id="6383a-126">First Use Notification</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-127">Solo computer</span><span class="sxs-lookup"><span data-stu-id="6383a-127">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-128">Questa impostazione di criteri di gruppo Abilita una notifica nell'area di notifica visualizzata quando l'UE-V</span><span class="sxs-lookup"><span data-stu-id="6383a-128">This Group Policy setting enables a notification in the notification area that appears when the UE-V</span></span></p>
<p><span data-ttu-id="6383a-129">l'agente viene eseguito per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="6383a-129">agent runs for the first time.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-130">Il valore predefinito è Enabled.</span><span class="sxs-lookup"><span data-stu-id="6383a-130">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6383a-131">Impostazioni di Windows roaming</span><span class="sxs-lookup"><span data-stu-id="6383a-131">Roam Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-132">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="6383a-132">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-133">Questa impostazione di criteri di gruppo configura la sincronizzazione delle impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="6383a-133">This Group Policy setting configures the synchronization of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-134">Selezionare le impostazioni di Windows da sincronizzare tra i computer.</span><span class="sxs-lookup"><span data-stu-id="6383a-134">Select which Windows settings synchronize between computers.</span></span></p>
<p><span data-ttu-id="6383a-135">Per impostazione predefinita, i temi di Windows, le impostazioni desktop e le impostazioni di accesso facilitato sincronizzano le impostazioni tra i computer della stessa versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6383a-135">By default, Windows themes, desktop settings, and Ease of Access settings synchronize settings between computers of the same operating system version.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6383a-136">Soglia di avviso dimensioni pacchetto impostazioni</span><span class="sxs-lookup"><span data-stu-id="6383a-136">Settings package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-137">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="6383a-137">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-138">Questa impostazione di criteri di gruppo consente di configurare l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge una soglia definita.</span><span class="sxs-lookup"><span data-stu-id="6383a-138">This Group Policy setting lets you configure the UE-V Agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-139">Specificare la soglia preferita per le dimensioni del pacchetto di impostazioni in kilobyte (KB).</span><span class="sxs-lookup"><span data-stu-id="6383a-139">Specify the preferred threshold for settings package sizes in kilobytes (KB).</span></span></p>
<p><span data-ttu-id="6383a-140">Per impostazione predefinita, l'agente UE-V non ha una soglia di dimensione del file del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6383a-140">By default, the UE-V Agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6383a-141">Percorso di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="6383a-141">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-142">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="6383a-142">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-143">Questa impostazione di criteri di gruppo configura la posizione in cui devono essere archiviate le impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="6383a-143">This Group Policy setting configures where the user settings are to be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-144">Immettere un percorso UNC (Universal Naming Convention) e variabili come \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="6383a-144">Enter a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6383a-145">Percorso catalogo di modelli di impostazioni</span><span class="sxs-lookup"><span data-stu-id="6383a-145">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-146">Solo computer</span><span class="sxs-lookup"><span data-stu-id="6383a-146">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-147">Questa impostazione di criteri di gruppo Configura dove sono archiviati i modelli di posizione delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="6383a-147">This Group Policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="6383a-148">Questa impostazione dei criteri Configura anche se il catalogo deve essere usato per sostituire i modelli Microsoft predefiniti installati con l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="6383a-148">This policy setting also configures whether the catalog is to be used to replace the default Microsoft templates that are installed with the UE-V Agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-149">Immettere un percorso UNC (Universal Naming Convention), ad esempio \Server\TemplateShare, o una posizione di cartella nel computer.</span><span class="sxs-lookup"><span data-stu-id="6383a-149">Enter a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p><span data-ttu-id="6383a-150">Selezionare la casella di controllo per sostituire i modelli Microsoft predefiniti.</span><span class="sxs-lookup"><span data-stu-id="6383a-150">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6383a-151">Impostazioni di sincronizzazione tramite connessioni a consumo</span><span class="sxs-lookup"><span data-stu-id="6383a-151">Sync settings over metered connections</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-152">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="6383a-152">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-153">Questa impostazione di criteri di gruppo definisce se l'opzione UE-V sincronizza le impostazioni tramite connessioni a consumo.</span><span class="sxs-lookup"><span data-stu-id="6383a-153">This Group Policy setting defines whether UE-V synchronizes settings over metered connections.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-154">Per impostazione predefinita, l'agente UE-V non sincronizza le impostazioni tramite una connessione a consumo.</span><span class="sxs-lookup"><span data-stu-id="6383a-154">By default, the UE-V Agent does not synchronize settings over a metered connection.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6383a-155">Sincronizzare le impostazioni tramite connessioni a consumo anche in roaming</span><span class="sxs-lookup"><span data-stu-id="6383a-155">Sync settings over metered connections even when roaming</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-156">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="6383a-156">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-157">Questa impostazione di criteri di gruppo definisce se l'opzione UE-V sincronizza le impostazioni tramite connessioni a consumo all'esterno della rete del provider Home, ad esempio quando la connessione dati è in modalità roaming.</span><span class="sxs-lookup"><span data-stu-id="6383a-157">This Group Policy setting defines whether UE-V synchronizes settings over metered connections outside of the home provider network, for example, when the data connection is in roaming mode.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-158">Per impostazione predefinita, l'opzione UE-V non sincronizza le impostazioni tramite una connessione a consumo quando è in modalità roaming.</span><span class="sxs-lookup"><span data-stu-id="6383a-158">By default, UE-V does not synchronize settings over a metered connection when it is in roaming mode.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6383a-159">Timeout della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="6383a-159">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-160">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="6383a-160">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-161">Questa impostazione di criteri di gruppo Configura il numero di millisecondi che il computer attende prima di un timeout quando recupera le impostazioni utente dalla posizione di impostazioni remote.</span><span class="sxs-lookup"><span data-stu-id="6383a-161">This Group Policy setting configures the number of milliseconds that the computer waits before a time-out when it retrieves user settings from the remote settings location.</span></span> <span data-ttu-id="6383a-162">Se la posizione di archiviazione remota non è disponibile e l'utente non usa il provider di sincronizzazione, l'avvio dell'applicazione viene ritardato di molti millisecondi.</span><span class="sxs-lookup"><span data-stu-id="6383a-162">If the remote storage location is unavailable, and the user does not use the sync provider, the application start is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-163">Specificare il timeout di sincronizzazione preferito in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="6383a-163">Specify the preferred synchronization time-out in milliseconds.</span></span> <span data-ttu-id="6383a-164">Il valore predefinito è 2000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="6383a-164">The default value is 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6383a-165">Icona del vassoio</span><span class="sxs-lookup"><span data-stu-id="6383a-165">Tray Icon</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-166">Solo computer</span><span class="sxs-lookup"><span data-stu-id="6383a-166">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-167">Questa impostazione di criteri di gruppo consente l'icona della barra multifunzione di virtualizzazione (UE-V) dell'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="6383a-167">This Group Policy setting enables the User Experience Virtualization (UE-V) tray icon.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-168">Il valore predefinito è Enabled.</span><span class="sxs-lookup"><span data-stu-id="6383a-168">The default is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6383a-169">Usare la virtualizzazione dell'esperienza utente (UE-V)</span><span class="sxs-lookup"><span data-stu-id="6383a-169">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-170">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="6383a-170">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-171">Questa impostazione di criteri di gruppo consente di abilitare o disabilitare la virtualizzazione dell'esperienza utente (UE-V).</span><span class="sxs-lookup"><span data-stu-id="6383a-171">This Group Policy setting lets you enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-172">Abilitare o disabilitare questa impostazione di criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="6383a-172">Enable or disable this Group Policy setting.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6383a-173">**Nota**  Inoltre, le impostazioni dei criteri di gruppo sono disponibili per molte applicazioni desktop e app di Windows.</span><span class="sxs-lookup"><span data-stu-id="6383a-173">**Note** In addition, Group Policy settings are available for many desktop applications and Windows apps.</span></span> <span data-ttu-id="6383a-174">Puoi usare queste impostazioni per abilitare o disabilitare la sincronizzazione delle impostazioni per applicazioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="6383a-174">You can use these settings to enable or disable settings synchronization for specific applications.</span></span>

 

**<span data-ttu-id="6383a-175">Impostazioni dei criteri di gruppo delle app di Windows</span><span class="sxs-lookup"><span data-stu-id="6383a-175">Windows App Group Policy settings</span></span>**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6383a-176">Nome dell'impostazione di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6383a-176">Group Policy setting name</span></span></th>
<th align="left"><span data-ttu-id="6383a-177">Target</span><span class="sxs-lookup"><span data-stu-id="6383a-177">Target</span></span></th>
<th align="left"><span data-ttu-id="6383a-178">Descrizione dell'impostazione di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="6383a-178">Group Policy setting description</span></span></th>
<th align="left"><span data-ttu-id="6383a-179">Opzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="6383a-179">Configuration options</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6383a-180">Non sincronizzare le app di Windows</span><span class="sxs-lookup"><span data-stu-id="6383a-180">Do not synchronize Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-181">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="6383a-181">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-182">Questa impostazione di criteri di gruppo definisce se l'agente UE-V sincronizza le impostazioni per le app di Windows.</span><span class="sxs-lookup"><span data-stu-id="6383a-182">This Group Policy setting defines whether the UE-V Agent synchronizes settings for Windows apps.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-183">Il valore predefinito è la sincronizzazione delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="6383a-183">The default is to synchronize Windows apps.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6383a-184">Elenco delle app di Windows</span><span class="sxs-lookup"><span data-stu-id="6383a-184">Windows App List</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-185">Computer e utente</span><span class="sxs-lookup"><span data-stu-id="6383a-185">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-186">Questa impostazione elenca i nomi dei pacchetti familiari delle app di Windows e dichiara espressamente se l'opzione UE-V sincronizza le impostazioni dell'app.</span><span class="sxs-lookup"><span data-stu-id="6383a-186">This setting lists the family package names of the Windows apps and states expressly whether UE-V synchronizes that app’s settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-187">Puoi usare questa impostazione per specificare che le impostazioni di un'app non vengono mai sincronizzate da UE-V, anche se le impostazioni di tutte le altre app di Windows sono sincronizzate.</span><span class="sxs-lookup"><span data-stu-id="6383a-187">You can use this setting to specify that settings of an app are never synchronized by UE-V, even if the settings of all other Windows apps are synchronized.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6383a-188">Sincronizzare le app di Windows non in elenco</span><span class="sxs-lookup"><span data-stu-id="6383a-188">Sync Unlisted Windows Apps</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-189">Computer e utente</span><span class="sxs-lookup"><span data-stu-id="6383a-189">Computer and User</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-190">Questa impostazione di criteri di gruppo definisce il comportamento di sincronizzazione delle impostazioni predefinite dell'agente UE-V per le app di Windows che non sono elencate esplicitamente nell'elenco delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="6383a-190">This Group Policy setting defines the default settings sync behavior of the UE-V Agent for Windows apps that are not explicitly listed in the Windows app list.</span></span></p></td>
<td align="left"><p><span data-ttu-id="6383a-191">Per impostazione predefinita, l'agente UE-V Sincronizza solo le impostazioni delle app di Windows incluse nell'elenco delle app di Windows.</span><span class="sxs-lookup"><span data-stu-id="6383a-191">By default, the UE-V Agent only synchronizes settings of those Windows apps that are included in the Windows app list.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="6383a-192">Per altre informazioni sulla sincronizzazione delle app di Windows, Vedi [elenco delle app di Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span><span class="sxs-lookup"><span data-stu-id="6383a-192">For more information about synchronizing Windows apps, see [Windows App List](https://technet.microsoft.com/library/dn458925.aspx#win8applist).</span></span>

**<span data-ttu-id="6383a-193">Per configurare le impostazioni di criteri di gruppo mirate al computer</span><span class="sxs-lookup"><span data-stu-id="6383a-193">To configure computer-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="6383a-194">Usare la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo nel computer che funge da controller di dominio per gestire le impostazioni dei criteri di gruppo per i computer UE-V.</span><span class="sxs-lookup"><span data-stu-id="6383a-194">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the computer that acts as a domain controller to manage Group Policy settings for UE-V computers.</span></span> <span data-ttu-id="6383a-195">Passare alla **configurazione del computer**, selezionare i **criteri**, selezionare **modelli amministrativi**, fare clic su **componenti di Windows**e quindi selezionare **Microsoft User Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="6383a-195">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="6383a-196">Selezionare l'impostazione di criteri di gruppo da modificare.</span><span class="sxs-lookup"><span data-stu-id="6383a-196">Select the Group Policy setting to be edited.</span></span>

**<span data-ttu-id="6383a-197">Per configurare le impostazioni di criteri di gruppo mirate dall'utente</span><span class="sxs-lookup"><span data-stu-id="6383a-197">To configure user-targeted Group Policy settings</span></span>**

1.  <span data-ttu-id="6383a-198">Usare la console di gestione di criteri di gruppo o lo strumento Advanced Group Policy Management in Microsoft Desktop Optimization Pack (MDOP) nel computer del controller di dominio per gestire le impostazioni dei criteri di gruppo per UE-V.</span><span class="sxs-lookup"><span data-stu-id="6383a-198">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer to manage Group Policy settings for UE-V.</span></span> <span data-ttu-id="6383a-199">Passare alla **Configurazione utente**, selezionare i **criteri**, selezionare **modelli amministrativi**, fare clic su **componenti di Windows**e quindi selezionare **Microsoft User Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="6383a-199">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="6383a-200">Selezionare l'impostazione di criteri di gruppo modificata.</span><span class="sxs-lookup"><span data-stu-id="6383a-200">Select the edited Group Policy setting.</span></span>

<span data-ttu-id="6383a-201">L'agente UE-V usa l'ordine di precedenza seguente per determinare la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="6383a-201">The UE-V Agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="6383a-202">Ordine di precedenza per le impostazioni UE-V</span><span class="sxs-lookup"><span data-stu-id="6383a-202">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="6383a-203">Impostazioni di destinazione utente gestite da impostazioni di criteri di gruppo: queste impostazioni di configurazione sono archiviate nella chiave del registro di sistema in criteri di gruppo `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="6383a-203">User-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="6383a-204">Impostazioni di destinazione del computer gestite da impostazioni di criteri di gruppo: queste impostazioni di configurazione sono archiviate nella chiave del registro di sistema in criteri di gruppo `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="6383a-204">Computer-targeted settings that are managed by Group Policy settings - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="6383a-205">Impostazioni di configurazione definite dall'utente corrente tramite Windows PowerShell o Strumentazione gestione Windows (WMI)-queste impostazioni di configurazione sono archiviate dall'agente UE-V in questo percorso del registro di sistema: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="6383a-205">Configuration settings that are defined by the current user by using Windows PowerShell or Windows management Instrumentation (WMI) - These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="6383a-206">Impostazioni di configurazione definite per il computer tramite Windows PowerShell o WMI.</span><span class="sxs-lookup"><span data-stu-id="6383a-206">Configuration settings that are defined for the computer by using Windows PowerShell or WMI.</span></span> <span data-ttu-id="6383a-207">Queste impostazioni di configurazione sono archiviate dall'agente UE-V in questo percorso del registro di sistema: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="6383a-207">These configuration settings are stored by the UE-V Agent under this registry location: `HKEY_LOCAL_MACHINE\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

    <span data-ttu-id="6383a-208">**Hai un suggerimento per l'UE-V**?</span><span class="sxs-lookup"><span data-stu-id="6383a-208">**Got a suggestion for UE-V**?</span></span> <span data-ttu-id="6383a-209">Aggiungere o votare i suggerimenti [qui](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span><span class="sxs-lookup"><span data-stu-id="6383a-209">Add or vote on suggestions [here](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization).</span></span> <span data-ttu-id="6383a-210">**È stato ottenuto un problema UE-V**?</span><span class="sxs-lookup"><span data-stu-id="6383a-210">**Got a UE-V issue**?</span></span> <span data-ttu-id="6383a-211">Utilizzare il [forum TechNet di UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span><span class="sxs-lookup"><span data-stu-id="6383a-211">Use the [UE-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).</span></span>

## <span data-ttu-id="6383a-212">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6383a-212">Related topics</span></span>


[<span data-ttu-id="6383a-213">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="6383a-213">Administering UE-V 2.x</span></span>](administering-ue-v-2x-new-uevv2.md)

[<span data-ttu-id="6383a-214">Gestire le configurazioni per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="6383a-214">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





