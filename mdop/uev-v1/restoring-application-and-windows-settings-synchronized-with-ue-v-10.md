---
title: Ripristino dell'applicazione e delle impostazioni di Windows sincronizzate con UE-V 1.0
description: Ripristino dell'applicazione e delle impostazioni di Windows sincronizzate con UE-V 1.0
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804180"
---
# <span data-ttu-id="d609d-103">Ripristino dell'applicazione e delle impostazioni di Windows sincronizzate con UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d609d-103">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>


<span data-ttu-id="d609d-104">Le funzionalità WMI e PowerShell di Microsoft User Experience Virtualization (UE-V) consentono di ripristinare i pacchetti di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="d609d-104">WMI and PowerShell features of Microsoft User Experience Virtualization (UE-V) provide the ability to restore settings packages.</span></span> <span data-ttu-id="d609d-105">I comandi WMI e PowerShell consentono di ripristinare le impostazioni dell'applicazione e di Windows nei valori delle impostazioni presenti nel computer la prima volta che l'applicazione è stata avviata dopo l'installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="d609d-105">WMI and PowerShell commands allow you to restore application and Windows settings to the settings values that were on the computer the first time the application launched after the UE-V Agent was installed.</span></span> <span data-ttu-id="d609d-106">Questa azione di ripristino viene eseguita in base alle impostazioni per applicazione o Windows.</span><span class="sxs-lookup"><span data-stu-id="d609d-106">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="d609d-107">Le impostazioni vengono ripristinate la volta successiva che l'applicazione viene eseguita o quando l'utente accede al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d609d-107">The settings are restored the next time that the application is run or when the user logs on to the operating system.</span></span>

**<span data-ttu-id="d609d-108">Per ripristinare le impostazioni dell'applicazione e le impostazioni di Windows con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d609d-108">To restore application settings and Windows settings with PowerShell</span></span>**

1.  <span data-ttu-id="d609d-109">Aprire la finestra di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d609d-109">Open the Windows PowerShell window.</span></span> <span data-ttu-id="d609d-110">Per importare il modulo Microsoft UE-V PowerShell, immettere il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="d609d-110">To import the Microsoft UE-V PowerShell module, enter the following command:</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="d609d-111">Immettere il cmdlet di PowerShell seguente per ripristinare le impostazioni dell'applicazione e le impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="d609d-111">Enter the following PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="d609d-112">Cmdlet di PowerShell</span><span class="sxs-lookup"><span data-stu-id="d609d-112">PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="d609d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d609d-113">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d609d-114">Ripristinare-UevUserSetting</span><span class="sxs-lookup"><span data-stu-id="d609d-114">Restore-UevUserSetting</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d609d-115">Ripristina le impostazioni utente per un'applicazione o ripristina un gruppo di impostazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="d609d-115">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="d609d-116">Per ripristinare le impostazioni delle applicazioni e le impostazioni di Windows con WMI</span><span class="sxs-lookup"><span data-stu-id="d609d-116">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="d609d-117">Aprire una finestra di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d609d-117">Open a PowerShell window.</span></span>

2.  <span data-ttu-id="d609d-118">Immettere il comando WMI seguente per ripristinare le impostazioni delle applicazioni e le impostazioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="d609d-118">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="d609d-119">Comando WMI</span><span class="sxs-lookup"><span data-stu-id="d609d-119">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="d609d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d609d-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="d609d-121">Invoke-WmiMethod-namespace root\Microsoft\UEV-Class UserSettings-Name RestoreByTemplateId-argument &lt; template_ID&gt;</span><span class="sxs-lookup"><span data-stu-id="d609d-121">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="d609d-122">Ripristina le impostazioni utente per un'applicazione o ripristina un gruppo di impostazioni di Windows</span><span class="sxs-lookup"><span data-stu-id="d609d-122">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="d609d-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d609d-123">Related topics</span></span>


[<span data-ttu-id="d609d-124">Amministrazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d609d-124">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="d609d-125">Operazioni per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="d609d-125">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





