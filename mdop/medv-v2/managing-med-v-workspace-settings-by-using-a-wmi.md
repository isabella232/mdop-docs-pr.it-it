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
# Gestione delle impostazioni dell'area di lavoro MED-V con un WMI


È possibile usare Strumentazione gestione Windows (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 per gestire le impostazioni di configurazione correnti.

## Per gestire le impostazioni dell'area di lavoro MED-V con un WMI


Uno strumento di esplorazione WMI consente di visualizzare e modificare le impostazioni in un'area di lavoro MED-V. Il provider WMI viene implementato tramite il Framework di estensione del provider WMI da Microsoft .NET Framework 3,5.

Il provider WMI viene implementato nello spazio dei nomi **root\\microsoft\\medv** e implementa l' **impostazione**della classe. L' **impostazione** della classe contiene proprietà che corrispondono alle impostazioni nel registro di sistema sotto la chiave del registro di HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv.

**Attenzione**  Gli strumenti di esplorazione di WMI possono essere usati per eliminare o modificare classi e istanze. L'eliminazione o la modifica di determinate classi e istanze può comportare la perdita di dati importanti e causare una funzione di MED-V in modo imprevedibile.

 

È possibile usare lo strumento di esplorazione di WMI preferito per visualizzare e modificare le impostazioni di configurazione di MED-V seguendo questi passaggi.

1.  Aprire lo strumento di esplorazione di WMI preferito con le autorizzazioni di amministratore.

2.  Connettersi allo spazio dei nomi **root\\microsoft\\medv**.

3.  Enumerare le istanze per connettersi all'istanza in uso. Si vuole connettersi all'istanza dell' **impostazione**della classe.

    Verrà visualizzata una finestra dell' **Editor oggetti** . Le impostazioni di configurazione di MED-V sono elencate come **Proprietà**.

Eseguire la procedura seguente per modificare un'impostazione di configurazione di MED-V in WMI.

1.  Nell'elenco delle **Proprietà** nella finestra **Editor oggetti** fare doppio clic sul nome dell'impostazione di configurazione che si vuole modificare. Ad esempio, per modificare le informazioni sul reindirizzamento degli URL di MED-V, fare doppio clic sulla proprietà **UxRedirectUrls**.

    Verrà visualizzata una finestra dell' **editor di proprietà** .

2.  Modificare il valore per aggiornare le informazioni di configurazione. Ad esempio, per modificare le informazioni sul reindirizzamento degli URL di MED-V, aggiungere o rimuovere un indirizzo Web nell'elenco.

3.  Salvare le impostazioni delle proprietà aggiornate.

Dopo aver completato la visualizzazione o la modifica delle impostazioni di configurazione di MED-V, chiudere lo strumento di esplorazione di WMI.

**Importante**  In alcuni casi, è necessario riavviare l'area di lavoro MED-V per applicare le modifiche apportate alle impostazioni di configurazione di MED-V.

 

Il codice seguente mostra il file MOF (Managed Object Format) che definisce la classe **Setting** .

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

La classe **Setting** eredita dalla classe **ConfigValueProvider** . Il codice seguente mostra il file MOF (Managed Object Format) che definisce la classe **ConfigValueProvider** .

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

## Argomenti correlati


[Gestione delle impostazioni di configurazione dell'area di lavoro MED-V](managing-med-v-workspace-configuration-settings.md)

[Gestire le impostazioni dell'area di lavoro MED-V](manage-med-v-workspace-settings.md)

 

 





