---
title: Gestione delle impostazioni dell'area di lavoro MED-V con un WMI
description: Gestione delle impostazioni dell'area di lavoro MED-V con un WMI
author: dansimp
ms.assetid: 05a665a3-2309-46c1-babb-a3e3bbb0b1f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e74e6fa4944ce0dacd5503baec73044b231abe83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826135"
---
# <span data-ttu-id="6f13c-103">Gestione delle impostazioni dell'area di lavoro MED-V con un WMI</span><span class="sxs-lookup"><span data-stu-id="6f13c-103">Managing MED-V Workspace Settings by Using a WMI</span></span>


<span data-ttu-id="6f13c-104">È possibile usare Strumentazione gestione Windows (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 per gestire le impostazioni di configurazione correnti.</span><span class="sxs-lookup"><span data-stu-id="6f13c-104">You can use Windows Management Instrumentation (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 to manage your current configuration settings.</span></span>

## <span data-ttu-id="6f13c-105">Per gestire le impostazioni dell'area di lavoro MED-V con un WMI</span><span class="sxs-lookup"><span data-stu-id="6f13c-105">To manage MED-V workspace settings with a WMI</span></span>


<span data-ttu-id="6f13c-106">Uno strumento di esplorazione WMI consente di visualizzare e modificare le impostazioni in un'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="6f13c-106">A WMI browsing tool lets you view and edit the settings in a MED-V workspace.</span></span> <span data-ttu-id="6f13c-107">Il provider WMI viene implementato tramite il Framework di estensione del provider WMI da Microsoft .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="6f13c-107">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span>

<span data-ttu-id="6f13c-108">Il provider WMI viene implementato nello spazio dei nomi **root\\microsoft\\medv** e implementa l' **impostazione**della classe.</span><span class="sxs-lookup"><span data-stu-id="6f13c-108">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **Setting**.</span></span> <span data-ttu-id="6f13c-109">L' **impostazione** della classe contiene proprietà che corrispondono alle impostazioni nel registro di sistema sotto la chiave del registro di HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv.</span><span class="sxs-lookup"><span data-stu-id="6f13c-109">The class **Setting** contains properties that correspond to the settings in the system registry under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv registry key.</span></span>

<span data-ttu-id="6f13c-110">**Attenzione**  Gli strumenti di esplorazione di WMI possono essere usati per eliminare o modificare classi e istanze.</span><span class="sxs-lookup"><span data-stu-id="6f13c-110">**Caution** WMI browsing tools can be used to delete or modify classes and instances.</span></span> <span data-ttu-id="6f13c-111">L'eliminazione o la modifica di determinate classi e istanze può comportare la perdita di dati importanti e causare una funzione di MED-V in modo imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="6f13c-111">Deleting or modifying certain classes and instances can result in the loss of valuable data and cause MED-V to function unpredictably.</span></span>

 

<span data-ttu-id="6f13c-112">È possibile usare lo strumento di esplorazione di WMI preferito per visualizzare e modificare le impostazioni di configurazione di MED-V seguendo questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="6f13c-112">You can use your preferred WMI browsing tool to view and edit MED-V configuration settings by following these steps.</span></span>

1.  <span data-ttu-id="6f13c-113">Aprire lo strumento di esplorazione di WMI preferito con le autorizzazioni di amministratore.</span><span class="sxs-lookup"><span data-stu-id="6f13c-113">Open your preferred WMI browsing tool with administrator permissions.</span></span>

2.  <span data-ttu-id="6f13c-114">Connettersi allo spazio dei nomi **root\\microsoft\\medv**.</span><span class="sxs-lookup"><span data-stu-id="6f13c-114">Connect to the namespace **root\\microsoft\\medv**.</span></span>

3.  <span data-ttu-id="6f13c-115">Enumerare le istanze per connettersi all'istanza in uso.</span><span class="sxs-lookup"><span data-stu-id="6f13c-115">Enumerate the instances to connect to the running instance.</span></span> <span data-ttu-id="6f13c-116">Si vuole connettersi all'istanza dell' **impostazione**della classe.</span><span class="sxs-lookup"><span data-stu-id="6f13c-116">You want to connect to the instance of the class **Setting**.</span></span>

    <span data-ttu-id="6f13c-117">Verrà visualizzata una finestra dell' **Editor oggetti** .</span><span class="sxs-lookup"><span data-stu-id="6f13c-117">An **Object Editor** window opens.</span></span> <span data-ttu-id="6f13c-118">Le impostazioni di configurazione di MED-V sono elencate come **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="6f13c-118">The MED-V configuration settings are listed as **Properties**.</span></span>

<span data-ttu-id="6f13c-119">Eseguire la procedura seguente per modificare un'impostazione di configurazione di MED-V in WMI.</span><span class="sxs-lookup"><span data-stu-id="6f13c-119">Perform the following steps to edit a MED-V configuration setting in the WMI.</span></span>

1.  <span data-ttu-id="6f13c-120">Nell'elenco delle **Proprietà** nella finestra **Editor oggetti** fare doppio clic sul nome dell'impostazione di configurazione che si vuole modificare.</span><span class="sxs-lookup"><span data-stu-id="6f13c-120">In the list of **Properties** on the **Object Editor** window, double-click the name of the configuration setting you want to edit.</span></span> <span data-ttu-id="6f13c-121">Ad esempio, per modificare le informazioni sul reindirizzamento degli URL di MED-V, fare doppio clic sulla proprietà **UxRedirectUrls**.</span><span class="sxs-lookup"><span data-stu-id="6f13c-121">For example, to edit MED-V URL redirection information, double-click the property **UxRedirectUrls**.</span></span>

    <span data-ttu-id="6f13c-122">Verrà visualizzata una finestra dell' **editor di proprietà** .</span><span class="sxs-lookup"><span data-stu-id="6f13c-122">A **Property Editor** window opens.</span></span>

2.  <span data-ttu-id="6f13c-123">Modificare il valore per aggiornare le informazioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="6f13c-123">Edit the value to update the configuration information.</span></span> <span data-ttu-id="6f13c-124">Ad esempio, per modificare le informazioni sul reindirizzamento degli URL di MED-V, aggiungere o rimuovere un indirizzo Web nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="6f13c-124">For example, to edit MED-V URL redirection information, add or remove a web address in the list.</span></span>

3.  <span data-ttu-id="6f13c-125">Salvare le impostazioni delle proprietà aggiornate.</span><span class="sxs-lookup"><span data-stu-id="6f13c-125">Save the updated property settings.</span></span>

<span data-ttu-id="6f13c-126">Dopo aver completato la visualizzazione o la modifica delle impostazioni di configurazione di MED-V, chiudere lo strumento di esplorazione di WMI.</span><span class="sxs-lookup"><span data-stu-id="6f13c-126">After you have finished viewing or editing MED-V configuration settings, close the WMI browsing tool.</span></span>

<span data-ttu-id="6f13c-127">**Importante**  In alcuni casi, è necessario riavviare l'area di lavoro MED-V per applicare le modifiche apportate alle impostazioni di configurazione di MED-V.</span><span class="sxs-lookup"><span data-stu-id="6f13c-127">**Important** In some cases, a restart of the MED-V workspace is required for changes to MED-V configuration settings to take effect.</span></span>

 

<span data-ttu-id="6f13c-128">Il codice seguente mostra il file MOF (Managed Object Format) che definisce la classe **Setting** .</span><span class="sxs-lookup"><span data-stu-id="6f13c-128">The following code shows the Managed Object Format (MOF) file that defines the **Setting** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

<span data-ttu-id="6f13c-129">La classe **Setting** eredita dalla classe **ConfigValueProvider** .</span><span class="sxs-lookup"><span data-stu-id="6f13c-129">The **Setting** class inherits from the **ConfigValueProvider** class.</span></span> <span data-ttu-id="6f13c-130">Il codice seguente mostra il file MOF (Managed Object Format) che definisce la classe **ConfigValueProvider** .</span><span class="sxs-lookup"><span data-stu-id="6f13c-130">The following code shows the Managed Object Format (MOF) file that defines the **ConfigValueProvider** class.</span></span>

``` syntax
[abstract]
class ConfigValueProvider
{
                [write] string DiagEventLogLevel;
                [write] boolean FtsAddUserToAdminGroupEnabled;
                [write] string FtsComputerNameMask;
                [write] sint32 FtsDeleteVMStateTimeout;
                [write] sint32 FtsDetachVfdTimeout;
                [write] string FtsDialogUrl;
                [write] sint32 FtsExplorerTimeout;
                [write] string FtsFailureDialogMsg;
                [write] string FtsLogFilePaths[];
                [write] sint32 FtsMaxPostponeTime;
                [write] sint32 FtsMaxRetryCount;
                [write] string FtsMode;
                [write] sint32 FtsNonInteractiveRetryTimeoutInc;
                [write] sint32 FtsNonInteractiveTimeout;
                [write] string FtsPostponeUtcDateTimeLimit;
                [write] string FtsRetryDialogMsg;
                [write] boolean FtsSetComputerNameEnabled;
                [write] boolean FtsSetJoinDomainEnabled;
                [write] boolean FtsSetMachineObjectOUEnabled;
                [write] boolean FtsSetRegionalSettingsEnabled;
                [write] boolean FtsSetUserDataEnabled;
                [write] string FtsStartDialogMsg;
                [write] sint32 FtsTaskCancelTimeout;
                [write] sint32 FtsTaskVMTurnOffTimeout;
                [write] sint32 FtsUpgradeTimeout;
                [write] boolean UxAppPublishingEnabled;
                [write] boolean UxAudioSharingEnabled;
                [write] boolean UxClipboardSharingEnabled;
                [write] boolean UxCredentialCacheEnabled;
                [write] sint32 UxDialogTimeout;
                [write] sint32 UxHideVmTimeout;
                [write] boolean UxLogonStartEnabled;
                [write] boolean UxPrinterSharingEnabled;
                [write] sint32 UxRebootAbsoluteDelayTimeout;
                [write] string UxRedirectUrls[];
                [write] boolean UxShowExit;
                [write] boolean UxSmartCardLogonEnabled;
                [write] boolean UxSmartCardSharingEnabled;
                [write] boolean UxUSBDeviceSharingEnabled;
                [write] string VmCloseAction;
                [write] sint32 VmGuestMemFromHostMem[];
                [write] sint32 VmGuestUpdateDuration;
                [write] string VmGuestUpdateTime;
                [write] sint32 VmHostMemToGuestMem[];
                [write] boolean VmHostMemToGuestMemCalcEnabled;
                [write] sint32 VmMemory;
                [write] boolean VmMultiUserEnabled;
                [write] string VmNetworkingMode;
                [write] sint32 VmTaskTimeout;
};
```

## <span data-ttu-id="6f13c-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f13c-131">Related topics</span></span>


[<span data-ttu-id="6f13c-132">Gestione delle impostazioni di configurazione dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="6f13c-132">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="6f13c-133">Gestire le impostazioni dell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="6f13c-133">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





