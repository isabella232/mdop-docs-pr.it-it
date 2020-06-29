---
title: Configurazione di UE-V con oggetti Criteri di gruppo
description: Configurazione di UE-V con oggetti Criteri di gruppo
author: dansimp
ms.assetid: 5c9be706-a05f-4397-9a38-e6b73ebff1e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7e479e6bef1a2b38cf822ffca19ed4220b0c59fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826696"
---
# <span data-ttu-id="04cce-103">Configurazione di UE-V con oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="04cce-103">Configuring UE-V with Group Policy Objects</span></span>


<span data-ttu-id="04cce-104">Alcune impostazioni di criteri di gruppo di Microsoft User Experience Virtualization (UE-V) possono essere definite per i computer e altre possono essere definite per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="04cce-104">Some Microsoft User Experience Virtualization (UE-V) Group Policy settings can be defined for computers and others can be defined for users.</span></span> <span data-ttu-id="04cce-105">Le impostazioni dei criteri di configurazione dell'agente UE-V possono essere definite per i computer o gli utenti.</span><span class="sxs-lookup"><span data-stu-id="04cce-105">UE-V agent configuration policy settings can be defined for computers or users.</span></span> <span data-ttu-id="04cce-106">Per informazioni su come installare i file ADMX di criteri di gruppo UE-V, vedere [installare i modelli ADMX di criteri di gruppo UE-v](installing-the-ue-v-group-policy-admx-templates.md).</span><span class="sxs-lookup"><span data-stu-id="04cce-106">For information about how to install UE-V Group Policy ADMX files, see [Installing the UE-V Group Policy ADMX Templates](installing-the-ue-v-group-policy-admx-templates.md).</span></span>

<span data-ttu-id="04cce-107">Le impostazioni dei criteri seguenti possono essere configurate per UE-V:</span><span class="sxs-lookup"><span data-stu-id="04cce-107">The following policy settings can be configured for UE-V:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="04cce-108">Nome impostazione criterio</span><span class="sxs-lookup"><span data-stu-id="04cce-108">Policy setting name</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="04cce-109">Target</span><span class="sxs-lookup"><span data-stu-id="04cce-109">Target</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="04cce-110">Descrizione delle impostazioni dei criteri</span><span class="sxs-lookup"><span data-stu-id="04cce-110">Policy setting description</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="04cce-111">Opzioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="04cce-111">Configuration options</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04cce-112">Usare la virtualizzazione dell'esperienza utente (UE-V)</span><span class="sxs-lookup"><span data-stu-id="04cce-112">Use User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-113">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="04cce-113">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-114">Questa impostazione dei criteri consente di abilitare o disabilitare la virtualizzazione dell'esperienza utente (UE-V).</span><span class="sxs-lookup"><span data-stu-id="04cce-114">This policy setting allows you to enable or disable User Experience Virtualization (UE-V).</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-115">Abilitare o disabilitare questa impostazione per i criteri.</span><span class="sxs-lookup"><span data-stu-id="04cce-115">Enable or disable this policy setting.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04cce-116">Percorso di archiviazione delle impostazioni</span><span class="sxs-lookup"><span data-stu-id="04cce-116">Settings storage path</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-117">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="04cce-117">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-118">Questa impostazione dei criteri Configura la posizione in cui verranno archiviate le impostazioni utente.</span><span class="sxs-lookup"><span data-stu-id="04cce-118">This policy setting configures where the user settings will be stored.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-119">Specificare un percorso UNC (Universal Naming Convention) e variabili come \Server\SettingsShare%username%.</span><span class="sxs-lookup"><span data-stu-id="04cce-119">Provide a Universal Naming Convention (UNC) path and variables such as \Server\SettingsShare%username%.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04cce-120">Percorso catalogo di modelli di impostazioni</span><span class="sxs-lookup"><span data-stu-id="04cce-120">Settings template catalog path</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-121">Solo computer</span><span class="sxs-lookup"><span data-stu-id="04cce-121">Computers Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-122">Questa impostazione dei criteri Configura dove sono archiviati i modelli di posizione delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="04cce-122">This policy setting configures where custom settings location templates are stored.</span></span> <span data-ttu-id="04cce-123">Questa impostazione dei criteri Configura anche se il catalogo verrà usato per sostituire i modelli Microsoft predefiniti installati con l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="04cce-123">This policy setting also configures whether the catalog will be used to replace the default Microsoft templates that are installed with the UE-V agent.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-124">Specificare un percorso UNC (Universal Naming Convention), ad esempio \Server\TemplateShare, o un percorso di cartella nel computer.</span><span class="sxs-lookup"><span data-stu-id="04cce-124">Provide a Universal Naming Convention (UNC) path such as \Server\TemplateShare or a folder location on the computer.</span></span></p>
<p></p>
<p><span data-ttu-id="04cce-125">Selezionare la casella di controllo per sostituire i modelli Microsoft predefiniti.</span><span class="sxs-lookup"><span data-stu-id="04cce-125">Select the check box to replace the default Microsoft templates.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04cce-126">Non usare file offline</span><span class="sxs-lookup"><span data-stu-id="04cce-126">Do not use Offline Files</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-127">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="04cce-127">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-128">Questa impostazione dei criteri consente di configurare se UE-V utilizzerà la funzionalità file offline di Windows.</span><span class="sxs-lookup"><span data-stu-id="04cce-128">This policy setting allows you to configure whether UE-V will use the Windows Offline Files feature.</span></span> <span data-ttu-id="04cce-129">Questa impostazione dei criteri consente inoltre di abilitare la notifica quando l'importazione delle impostazioni utente viene ritardata.</span><span class="sxs-lookup"><span data-stu-id="04cce-129">This policy setting also allows you to enable notification to occur when the import of user settings is delayed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-130">Per configurare l'agente UE-V per non usare i file offline, abilitare questa impostazione.</span><span class="sxs-lookup"><span data-stu-id="04cce-130">To configure the UE-V Agent to not use offline files, enable this setting.</span></span></p>
<p></p>
<p><span data-ttu-id="04cce-131">Specificare se le notifiche devono essere fornite quando l'importazione delle impostazioni è ritardata.</span><span class="sxs-lookup"><span data-stu-id="04cce-131">Specify if notifications should be given when settings import is delayed.</span></span></p>
<p></p>
<p><span data-ttu-id="04cce-132">Specificare l'intervallo di tempo in secondi da attendere prima che venga visualizzata la notifica.</span><span class="sxs-lookup"><span data-stu-id="04cce-132">Specify the length of time in seconds to wait before the notification appears.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04cce-133">Timeout della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="04cce-133">Synchronization timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-134">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="04cce-134">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-135">Questa impostazione del criterio Configura il numero di millisecondi di attesa prima di un timeout durante il recupero delle impostazioni utente dalla posizione di impostazioni remote.</span><span class="sxs-lookup"><span data-stu-id="04cce-135">This policy setting configures the number of milliseconds that the computer waits before a timeout when retrieving user settings from the remote settings location.</span></span> <span data-ttu-id="04cce-136">Se la posizione di archiviazione remota non è disponibile, l'avvio dell'applicazione viene ritardato di molti millisecondi.</span><span class="sxs-lookup"><span data-stu-id="04cce-136">If the remote storage location is unavailable, the application launch is delayed by this many milliseconds.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-137">Specificare il timeout di sincronizzazione preferito in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="04cce-137">Specify the preferred synchronization timeout in milliseconds.</span></span> <span data-ttu-id="04cce-138">Il valore predefinito di 2000 millisecondi.</span><span class="sxs-lookup"><span data-stu-id="04cce-138">The default value of 2000 milliseconds.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04cce-139">Soglia di avviso dimensione pacchetto</span><span class="sxs-lookup"><span data-stu-id="04cce-139">Package size warning threshold</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-140">Computer e utenti</span><span class="sxs-lookup"><span data-stu-id="04cce-140">Computers and Users</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-141">Questa impostazione dei criteri consente di configurare l'agente UE-V per segnalare quando una dimensione del file del pacchetto di impostazioni raggiunge una soglia definita.</span><span class="sxs-lookup"><span data-stu-id="04cce-141">This policy setting allows you to configure the UE-V agent to report when a settings package file size reaches a defined threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-142">Specificata la soglia preferita per le dimensioni del pacchetto di impostazioni in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="04cce-142">Specified the preferred threshold for settings package sizes in kilobytes.</span></span></p>
<p><span data-ttu-id="04cce-143">Per impostazione predefinita, l'agente UE-V non ha una soglia di dimensione del file del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="04cce-143">By default, the UE-V agent does not have a package file size threshold.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="04cce-144">Impostazioni dell'applicazione roaming</span><span class="sxs-lookup"><span data-stu-id="04cce-144">Roaming Application settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-145">Solo utenti</span><span class="sxs-lookup"><span data-stu-id="04cce-145">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-146">Questa impostazione dei criteri Configura il roaming delle impostazioni utente delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="04cce-146">This policy setting configures the roaming of user settings of applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-147">Selezionare le impostazioni di Windows che andranno in roaming tra i computer.</span><span class="sxs-lookup"><span data-stu-id="04cce-147">Select which Windows settings will roam between computers.</span></span></p>
<p><span data-ttu-id="04cce-148">Per impostazione predefinita, le impostazioni utente delle applicazioni con il modello di impostazioni fornito da UE-V sono in roaming tra i computer.</span><span class="sxs-lookup"><span data-stu-id="04cce-148">By default, the user settings of applications with settings template provided by UE-V are roamed between computers.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="04cce-149">Impostazioni di Windows in roaming</span><span class="sxs-lookup"><span data-stu-id="04cce-149">Roaming Windows settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-150">Solo utenti</span><span class="sxs-lookup"><span data-stu-id="04cce-150">Users Only</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-151">Questa impostazione dei criteri Configura il roaming delle impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="04cce-151">This policy setting configures the roaming of Windows settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="04cce-152">Selezionare le applicazioni che andranno in roaming tra i computer.</span><span class="sxs-lookup"><span data-stu-id="04cce-152">Select which applications will roam between computers.</span></span></p>
<p><span data-ttu-id="04cce-153">Per impostazione predefinita, i temi di Windows vengono spostati tra i computer della stessa versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="04cce-153">By default, Windows themes are roamed between computers of the same operating system version.</span></span> <span data-ttu-id="04cce-154">Le impostazioni desktop di Windows e le impostazioni di accesso facilitato non sono in roaming.</span><span class="sxs-lookup"><span data-stu-id="04cce-154">Windows desktop settings and Ease of Access settings are not roamed.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="04cce-155">Per configurare i criteri di destinazione del computer</span><span class="sxs-lookup"><span data-stu-id="04cce-155">To configure computer-targeted policies</span></span>**

1.  <span data-ttu-id="04cce-156">Usare la console Gestione criteri di gruppo o la gestione avanzata Criteri di gruppo nel computer controller di dominio che gestisce i criteri di gruppo per i computer UE-V.</span><span class="sxs-lookup"><span data-stu-id="04cce-156">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) on the domain controller computer that manages Group Policy for UE-V computers.</span></span> <span data-ttu-id="04cce-157">Passare alla **configurazione del computer**, selezionare i **criteri**, selezionare **modelli amministrativi**, fare clic su **componenti di Windows**e quindi selezionare **Microsoft User Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="04cce-157">Navigate to **Computer configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="04cce-158">Selezionare l'impostazione del criterio da modificare.</span><span class="sxs-lookup"><span data-stu-id="04cce-158">Select the policy setting to be edited.</span></span>

**<span data-ttu-id="04cce-159">Per configurare i criteri di destinazione dell'utente</span><span class="sxs-lookup"><span data-stu-id="04cce-159">To configure user-targeted policies</span></span>**

1.  <span data-ttu-id="04cce-160">Usare la console di gestione di criteri di gruppo o lo strumento Advanced Group Policy Management in Microsoft Desktop Optimization Pack (MDOP) nel computer controller di dominio che gestisce i criteri di gruppo per UE-V.</span><span class="sxs-lookup"><span data-stu-id="04cce-160">Use the Group Policy Management Console (GPMC) or the Advanced Group Policy Management (AGPM) tool in Microsoft Desktop Optimization Pack (MDOP) on the domain controller computer that manages Group Policy for UE-V.</span></span> <span data-ttu-id="04cce-161">Passare alla **Configurazione utente**, selezionare i **criteri**, selezionare **modelli amministrativi**, fare clic su **componenti di Windows**e quindi selezionare **Microsoft User Experience Virtualization**.</span><span class="sxs-lookup"><span data-stu-id="04cce-161">Navigate to **User configuration**, select **Policies**, select **Administrative Templates**, click **Windows Components**, and then select **Microsoft User Experience Virtualization**.</span></span>

2.  <span data-ttu-id="04cce-162">Selezionare l'impostazione dei criteri modificata.</span><span class="sxs-lookup"><span data-stu-id="04cce-162">Select the policy setting edited.</span></span>

<span data-ttu-id="04cce-163">L'agente UE-V usa l'ordine di precedenza seguente per determinare la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="04cce-163">The UE-V agent uses the following order of precedence to determine synchronization.</span></span>

**<span data-ttu-id="04cce-164">Ordine di precedenza per le impostazioni UE-V</span><span class="sxs-lookup"><span data-stu-id="04cce-164">Order of precedence for UE-V settings</span></span>**

1.  <span data-ttu-id="04cce-165">Impostazioni di destinazione utente gestite da criteri di gruppo: queste impostazioni di configurazione sono archiviate nella chiave del registro di sistema in criteri di gruppo `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="04cce-165">User-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_CURRENT_USER\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="04cce-166">Impostazioni di destinazione del computer gestite da criteri di gruppo: queste impostazioni di configurazione sono archiviate nella chiave del registro di sistema in criteri di gruppo `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="04cce-166">Computer-targeted settings managed by Group Policy - These configuration settings are stored in the registry key by Group Policy under `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Uev\Agent\Configuration`.</span></span>

3.  <span data-ttu-id="04cce-167">Impostazioni di configurazione definite dall'utente corrente tramite PowerShell o WMI-queste impostazioni di configurazione sono archiviate dall'agente UE-V in questo percorso del registro di sistema: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="04cce-167">Configuration settings defined by the current user using PowerShell or WMI - These configuration settings are stored by the UE-V agent under this registry location: `HKEY_CURRENT_USER\Software\Microsoft\Uev\Agent\Configuration`.</span></span>

4.  <span data-ttu-id="04cce-168">Impostazioni di configurazione definite per il computer con PowerShell o WMI.</span><span class="sxs-lookup"><span data-stu-id="04cce-168">Configuration settings defined for the computer using PowerShell or WMI.</span></span> <span data-ttu-id="04cce-169">Queste impostazioni di configurazione sono archiviate dall'agente UE-V in `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="04cce-169">These configuration settings are stored by the UE-V agent under the `HKEY_LOCAL_MACHINE \Software\Microsoft\Uev\Agent\Configuration`.</span></span>

## <span data-ttu-id="04cce-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="04cce-170">Related topics</span></span>


[<span data-ttu-id="04cce-171">Amministrazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="04cce-171">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="04cce-172">Operazioni per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="04cce-172">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





