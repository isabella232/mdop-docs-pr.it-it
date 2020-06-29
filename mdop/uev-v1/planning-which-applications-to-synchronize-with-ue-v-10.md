---
title: Pianificazione delle applicazioni da sincronizzare con UE-V 1.0
description: Pianificazione delle applicazioni da sincronizzare con UE-V 1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804210"
---
# <span data-ttu-id="7e6d1-103">Pianificazione delle applicazioni da sincronizzare con UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7e6d1-103">Planning Which Applications to Synchronize with UE-V 1.0</span></span>


<span data-ttu-id="7e6d1-104">Microsoft User Experience Virtualization (UE-V) USA i modelli di posizione delle impostazioni (file XML) che definiscono le impostazioni acquisite e applicate da UE-V.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="7e6d1-105">UE-V include un set di modelli di posizione predefiniti per le impostazioni e consente inoltre agli amministratori di creare modelli di posizione personalizzati per le applicazioni di terze parti o line-of-business usate nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-105">UE-V includes a set of predefined settings location templates and also allows administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="7e6d1-106">In qualità di amministratore, quando si considerano le applicazioni da includere nella soluzione UE-V, valutare quali impostazioni possono essere personalizzate dagli utenti e come e dove l'applicazione archivia le proprie impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-106">As an administrator, when you consider which applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="7e6d1-107">Non tutte le applicazioni hanno impostazioni che possono essere personalizzate o che sono personalizzate in routine dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-107">Not all applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="7e6d1-108">Inoltre, non tutte le impostazioni delle applicazioni possono spostarsi in modo sicuro in più computer o ambienti.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-108">In addition, not all applications settings can safely roam across multiple computers or environments.</span></span> <span data-ttu-id="7e6d1-109">Sincronizzare le impostazioni che soddisfano i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e6d1-109">Synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="7e6d1-110">Impostazioni archiviate in percorsi accessibili dall'utente.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-110">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="7e6d1-111">Ad esempio, non sincronizzare le impostazioni archiviate nella sezione system32 o outside HKCU del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-111">For example, do not synchronize settings that are stored in system32 or outside HKCU section of the registry.</span></span>

-   <span data-ttu-id="7e6d1-112">Impostazioni non specifiche per il computer specifico.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-112">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="7e6d1-113">Ad esempio, Escludi configurazioni di rete o hardware.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-113">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="7e6d1-114">Impostazioni che è possibile sincronizzare tra computer senza rischio di dati danneggiati.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-114">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="7e6d1-115">Ad esempio, non usare le impostazioni archiviate in un file di database.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-115">For example, do not use settings that are stored in a database file.</span></span>

## <span data-ttu-id="7e6d1-116">Modelli di posizione delle impostazioni inclusi in UE-V</span><span class="sxs-lookup"><span data-stu-id="7e6d1-116">Settings location templates that are included in UE-V</span></span>


**<span data-ttu-id="7e6d1-117">Modelli di posizione delle impostazioni dell'applicazione UE-V</span><span class="sxs-lookup"><span data-stu-id="7e6d1-117">UE-V application settings location templates</span></span>**

<span data-ttu-id="7e6d1-118">Il software di installazione dell'agente UE-V installa l'agente e registra un gruppo predefinito di modelli di posizione delle impostazioni per le applicazioni Microsoft comuni.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-118">The UE-V agent installation software installs the agent and registers a default group of settings location templates for common Microsoft applications.</span></span> <span data-ttu-id="7e6d1-119">Questi modelli di posizione delle impostazioni acquisiscono i valori delle impostazioni per le applicazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e6d1-119">These settings location templates capture settings values for the following applications:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="7e6d1-120">Categoria applicazione</span><span class="sxs-lookup"><span data-stu-id="7e6d1-120">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="7e6d1-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e6d1-121">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e6d1-122">Applicazioni di Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-122">Microsoft Office 2010 applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-123">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-123">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="7e6d1-124">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-124">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="7e6d1-125">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-125">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="7e6d1-126">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-126">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="7e6d1-127">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-127">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="7e6d1-128">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-128">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="7e6d1-129">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-129">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="7e6d1-130">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-130">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="7e6d1-131">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-131">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="7e6d1-132">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-132">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="7e6d1-133">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-133">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="7e6d1-134">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="7e6d1-134">Microsoft OneNote 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7e6d1-135">Opzioni del browser (Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10)</span><span class="sxs-lookup"><span data-stu-id="7e6d1-135">Browser options (Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10)</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-136">Preferiti, Home page, schede e barre degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-136">Favorites, home page, tabs, and toolbars.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e6d1-137">Accessori per Windows</span><span class="sxs-lookup"><span data-stu-id="7e6d1-137">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-138">Calcolatrice, blocco note, WordPad.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-138">Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7e6d1-139">Le impostazioni dell'applicazione vengono applicate all'applicazione quando l'applicazione viene avviata.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-139">Application settings are applied to the application when the application is started.</span></span> <span data-ttu-id="7e6d1-140">Vengono salvati quando l'applicazione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-140">They are saved when the application closes.</span></span>

**<span data-ttu-id="7e6d1-141">Modelli di posizione delle impostazioni di Windows UE-V</span><span class="sxs-lookup"><span data-stu-id="7e6d1-141">UE-V Windows settings location templates</span></span>**

<span data-ttu-id="7e6d1-142">Esperienza utente la virtualizzazione include i modelli di posizione delle impostazioni che acquisiscono i valori delle impostazioni per le impostazioni di Windows seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e6d1-142">User Experience Virtualization includes settings location templates that capture settings values for the following Windows settings:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="7e6d1-143">impostazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="7e6d1-143">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="7e6d1-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e6d1-144">Description</span></span></th>
<th align="left"><span data-ttu-id="7e6d1-145">Applicare il</span><span class="sxs-lookup"><span data-stu-id="7e6d1-145">Apply on</span></span></th>
<th align="left"><span data-ttu-id="7e6d1-146">Stato predefinito</span><span class="sxs-lookup"><span data-stu-id="7e6d1-146">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e6d1-147">Sfondo del desktop</span><span class="sxs-lookup"><span data-stu-id="7e6d1-147">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-148">Sfondo del desktop attualmente attivo.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-148">Currently active desktop background.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-149">Accesso, sblocco, connessione remota.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-149">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-150">Abilitato</span><span class="sxs-lookup"><span data-stu-id="7e6d1-150">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="7e6d1-151">Accessibilità</span><span class="sxs-lookup"><span data-stu-id="7e6d1-151">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-152">Impostazioni di accessibilità e input, lente di ingrandimento, Assistente vocale e tastiera su schermo.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-152">Accessibility and input settings, magnifier, Narrator, and on-Screen keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-153">Accesso, sblocco, connessione remota.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-153">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-154">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="7e6d1-154">Disabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="7e6d1-155">Impostazioni desktop</span><span class="sxs-lookup"><span data-stu-id="7e6d1-155">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-156">Menu Start e impostazioni della barra delle applicazioni, Opzioni cartella, icone desktop predefinite, clock aggiuntivi e impostazioni area geografica e lingua.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-156">Start menu and Taskbar settings, Folder options, default desktop icons, additional clocks, and region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-157">Solo accesso.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-157">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="7e6d1-158">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="7e6d1-158">Disabled</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="7e6d1-159">Lo sfondo del desktop di Windows e le impostazioni di accessibilità vengono applicati quando l'utente effettua l'accesso, quando il computer viene sbloccato o dopo la connessione remota a un altro computer.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-159">The Windows desktop background and Ease of Access settings are applied when the user logs on, when the computer is unlocked, or upon remote connection to another computer.</span></span> <span data-ttu-id="7e6d1-160">L'agente Salva queste impostazioni quando l'utente si disconnette, quando il computer è bloccato o quando una connessione remota è disconnessa.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-160">The agent saves these settings when the user logs off, when the computer is locked, or when a remote connection is disconnected.</span></span> <span data-ttu-id="7e6d1-161">Per impostazione predefinita, le impostazioni in background di Windows desktop sono in roaming tra i computer della stessa versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-161">By default, Windows desktop background settings are roamed between computers of the same operating system version.</span></span>

<span data-ttu-id="7e6d1-162">Il desktop di Windows e le impostazioni di accesso facilitato vengono applicati all'accesso prima che il desktop venga presentato all'utente.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-162">Windows desktop and Ease of Access settings are applied at logon before the desktop is presented to the user.</span></span> <span data-ttu-id="7e6d1-163">Per ottimizzare l'esperienza di accesso, queste impostazioni non sono in roaming per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-163">To optimize the logon experience, these settings are not roamed by default.</span></span> <span data-ttu-id="7e6d1-164">Le impostazioni desktop e di accesso facilitato possono essere abilitate tramite criteri di gruppo, PowerShell e WMI.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-164">Desktop and Ease of Access settings can be enabled by using Group Policy, PowerShell, and WMI.</span></span>

<span data-ttu-id="7e6d1-165">UE-V non supporta il roaming delle impostazioni tra sistemi operativi con lingue diverse.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-165">UE-V does not support the roaming of settings between operating systems with different languages.</span></span> <span data-ttu-id="7e6d1-166">La sincronizzazione tra l'inglese e il tedesco, ad esempio, non è supportata.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-166">For example, synchronization between English and German is not supported.</span></span> <span data-ttu-id="7e6d1-167">La lingua di tutti i computer a cui è necessario eseguire il roaming delle impostazioni utente in UE-V deve corrispondere.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-167">The language of all computers to which UE-V roams the user settings must match.</span></span>

<span data-ttu-id="7e6d1-168">**Nota**  Se si modificano i modelli di posizione delle impostazioni forniti da Microsoft, la virtualizzazione dell'esperienza utente potrebbe non funzionare correttamente per l'applicazione designata o per il gruppo impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-168">**Note** If you change the settings location templates that are provided by Microsoft, User Experience Virtualization might not work properly for the designated application or Windows settings group.</span></span>

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a><span data-ttu-id="7e6d1-169">Impedire la configurazione delle impostazioni utente non intenzionale</span><span class="sxs-lookup"><span data-stu-id="7e6d1-169">Prevent unintentional user Settings configuration</span></span>


<span data-ttu-id="7e6d1-170">L'esperienza utente verifica la virtualizzazione delle nuove informazioni sulle impostazioni utente e Scarica le informazioni di conseguenza da una posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-170">User Experience Virtualization checks for new user settings information, and downloads that information accordingly from a settings storage location.</span></span> <span data-ttu-id="7e6d1-171">Applica quindi le impostazioni al computer locale nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7e6d1-171">Then, it applies the settings to the local computer in the following cases:</span></span>

-   <span data-ttu-id="7e6d1-172">Ogni volta che viene avviata un'applicazione con un modello UE-V registrato.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-172">Every time an application is launched that has a registered UE-V template.</span></span>

-   <span data-ttu-id="7e6d1-173">Quando un utente accede al proprio computer.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-173">When a user logs on to their computer.</span></span>

-   <span data-ttu-id="7e6d1-174">Quando un utente sblocca il computer.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-174">When a user unlocks their computer.</span></span>

-   <span data-ttu-id="7e6d1-175">Quando viene effettuata una connessione a un computer desktop remoto in cui è installata la versione UE-V.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-175">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

<span data-ttu-id="7e6d1-176">Se UE-V è installato nel computer A e nel computer B e le impostazioni desiderate per l'applicazione si trovano nel computer A, il computer A deve aprire e chiudere prima l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-176">If UE-V is installed on computer A and computer B, and the desired settings for the application are on computer A, then computer A must open and close the application first.</span></span> <span data-ttu-id="7e6d1-177">Se un'applicazione viene aperta e chiusa prima del computer B, le impostazioni dell'applicazione nel computer A verranno configurate in modo che siano le stesse delle impostazioni dell'applicazione nel computer B.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-177">If an application is opened and closed on computer B first, then the application settings on computer A will be configured to be the same as the application settings on computer B.</span></span>

<span data-ttu-id="7e6d1-178">Questo scenario si applica anche alle impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-178">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="7e6d1-179">Se le impostazioni di Windows nel computer B devono essere le stesse delle impostazioni di Windows nel computer A, l'utente deve innanzitutto accedere al computer e disconnessione.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-179">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should logon and logoff computer A first.</span></span>

<span data-ttu-id="7e6d1-180">Se le impostazioni utente desiderate vengono applicate nell'ordine errato, possono essere recuperate eseguendo un'operazione di ripristino per l'applicazione specifica o la configurazione di Windows nel computer in cui sono state sovrascritte le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-180">If the desired user settings are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="7e6d1-181">Per altre informazioni, vedere [ripristino delle impostazioni di applicazione e Windows sincronizzate con UE-V 1,0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="7e6d1-181">For more information, see [Restoring Application and Windows Settings Synchronized with UE-V 1.0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span></span>

## <span data-ttu-id="7e6d1-182">Modelli di posizione delle impostazioni UE-V personalizzati</span><span class="sxs-lookup"><span data-stu-id="7e6d1-182">Custom UE-V settings location templates</span></span>


<span data-ttu-id="7e6d1-183">Puoi creare modelli di posizione delle impostazioni personalizzati usando il generatore UE-V.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-183">You can create custom settings location templates by using the UE-V Generator.</span></span> <span data-ttu-id="7e6d1-184">Dopo aver creato e testato un modello di posizione delle impostazioni personalizzato in un ambiente di test, è possibile distribuire i modelli di posizione delle impostazioni ai computer nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-184">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span> <span data-ttu-id="7e6d1-185">I modelli di posizione delle impostazioni personalizzate devono essere distribuiti con un'infrastruttura di distribuzione esistente, ad esempio il metodo ESD (Enterprise Software Distribution), con le preferenze o configurando un catalogo di modelli di impostazioni UE-V.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-185">Custom settings location templates must be deployed with an existing deployment infrastructure, such as enterprise software distribution (ESD) method, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="7e6d1-186">I modelli distribuiti con ESD o criteri di gruppo devono essere registrati usando WMI o PowerShell di UE-V.</span><span class="sxs-lookup"><span data-stu-id="7e6d1-186">Templates that are deployed with ESD or Group Policy must be registered by using UE-V WMI or PowerShell.</span></span> <span data-ttu-id="7e6d1-187">Per altre informazioni sui modelli di posizione delle impostazioni personalizzate, vedere [pianificazione della distribuzione di modelli personalizzati per la versione UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="7e6d1-187">For more information about custom settings location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

<span data-ttu-id="7e6d1-188">Per informazioni sull'eventuale sincronizzazione di un'applicazione line-of-business, vedere [elenco di controllo per la valutazione delle applicazioni line-of-business per UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="7e6d1-188">For guidance on whether a line-of-business application should be synchronized, see [Checklist for Evaluating Line-of-Business Applications for UE-V 1.0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span></span>

## <span data-ttu-id="7e6d1-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e6d1-189">Related topics</span></span>


[<span data-ttu-id="7e6d1-190">Pianificazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7e6d1-190">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="7e6d1-191">Pianificazione della distribuzione dei modelli personalizzati per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7e6d1-191">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

[<span data-ttu-id="7e6d1-192">Distribuzione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="7e6d1-192">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

 

 





