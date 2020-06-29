---
title: Amministrazione di UE-V 1.0
description: Amministrazione di UE-V 1.0
author: dansimp
ms.assetid: c399ae8d-c839-4f84-9bfc-adacd8f89f34
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4dcafd1949dcedd195569dabb7540ce55a2f1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822696"
---
# <span data-ttu-id="52ea7-103">Amministrazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="52ea7-103">Administering UE-V 1.0</span></span>


<span data-ttu-id="52ea7-104">Dopo aver distribuito Microsoft User Experience Virtualization (UE-V), è necessario essere in grado di eseguire varie attività amministrative in corso.</span><span class="sxs-lookup"><span data-stu-id="52ea7-104">After you have deployed Microsoft User Experience Virtualization (UE-V), you must be able to perform various ongoing administrative tasks.</span></span> <span data-ttu-id="52ea7-105">Queste attività di post-installazione sono descritte nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="52ea7-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="52ea7-106">Gestione delle risorse di UE-V</span><span class="sxs-lookup"><span data-stu-id="52ea7-106">Managing UE-V resources</span></span>


<span data-ttu-id="52ea7-107">Nel corso del ciclo di vita UE-V è necessario gestire la configurazione dell'agente UE-V e gestire anche i percorsi di archiviazione per le risorse, ad esempio i pacchetti di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="52ea7-107">In the course of the UE-V lifecycle, you will need to manage the configuration of the UE-V agent and also manage storage locations for resources such as settings packages.</span></span> <span data-ttu-id="52ea7-108">Potrebbe essere necessario eseguire altre attività, ad esempio per ripristinare lo stato originale delle impostazioni di un utente da prima dell'installazione di UE-V in modo da recuperare le impostazioni perse.</span><span class="sxs-lookup"><span data-stu-id="52ea7-108">You might need to perform other tasks such as to restore a user’s settings to their original state from before UE-V was installed in order to recover lost settings.</span></span> <span data-ttu-id="52ea7-109">Gli argomenti seguenti includono indicazioni per la gestione delle risorse UE-V.</span><span class="sxs-lookup"><span data-stu-id="52ea7-109">The following topics provide guidance for managing UE-V resources.</span></span>

### <span data-ttu-id="52ea7-110">Modifica della frequenza delle attività pianificate di UE-V</span><span class="sxs-lookup"><span data-stu-id="52ea7-110">Changing the Frequency of UE-V Scheduled Tasks</span></span>

<span data-ttu-id="52ea7-111">È possibile configurare le attività pianificate che gestiscono quando UE-V controlla i modelli di posizione personalizzati nuovi, aggiornati o rimossi nel catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="52ea7-111">You can configure the scheduled tasks that manage when UE-V checks for new, updated, or removed custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="52ea7-112">Modifica della frequenza delle attività pianificate di UE-V</span><span class="sxs-lookup"><span data-stu-id="52ea7-112">Changing the Frequency of UE-V Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-scheduled-tasks.md)

### <a href="" id="sharing-settings-location-templates-with-the-ue-v-template-gallery-"></a><span data-ttu-id="52ea7-113">Condivisione dei modelli percorsi impostazioni con la raccolta di modelli UE-V</span><span class="sxs-lookup"><span data-stu-id="52ea7-113">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>

<span data-ttu-id="52ea7-114">La raccolta modelli UE-V semplifica la condivisione dei modelli di posizione delle impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="52ea7-114">The UE-V template gallery facilitates the sharing of UE-V settings location templates.</span></span> <span data-ttu-id="52ea7-115">La raccolta consente di caricare i modelli di posizione delle impostazioni da condividere con altri utenti e di scaricare i modelli creati da altri utenti.</span><span class="sxs-lookup"><span data-stu-id="52ea7-115">The gallery enables you to upload your settings location templates to share with other people and to download templates that other people have created.</span></span>

[<span data-ttu-id="52ea7-116">Condivisione dei modelli percorsi impostazioni con la raccolta di modelli UE-V</span><span class="sxs-lookup"><span data-stu-id="52ea7-116">Sharing Settings Location Templates with the UE-V Template Gallery</span></span>](sharing-settings-location-templates-with-the-ue-v-template-gallery.md)

### <span data-ttu-id="52ea7-117">Ripristinare le impostazioni di applicazione e Windows sincronizzate con UE-V 1,0</span><span class="sxs-lookup"><span data-stu-id="52ea7-117">Restoring application and Windows settings synchronized with UE-V 1.0</span></span>

<span data-ttu-id="52ea7-118">Le funzionalità WMI e PowerShell di UE-V consentono di ripristinare i pacchetti di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="52ea7-118">WMI and PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="52ea7-119">I comandi WMI e PowerShell consentono di ripristinare le impostazioni delle applicazioni e le impostazioni di Windows per i valori delle impostazioni presenti nel computer la prima volta che l'applicazione è stata avviata dopo l'avvio dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="52ea7-119">WMI and PowerShell commands allow you to restore application settings and Windows settings to the settings values that were on the computer the first time the application was started after the UE-V agent was launched.</span></span>

[<span data-ttu-id="52ea7-120">Ripristino dell'applicazione e delle impostazioni di Windows sincronizzate con UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="52ea7-120">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md)

### <span data-ttu-id="52ea7-121">Configurazione di UE-V con oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="52ea7-121">Configuring UE-V with Group Policy Objects</span></span>

<span data-ttu-id="52ea7-122">È possibile usare criteri di gruppo per modificare le impostazioni che definiscono la modalità di sincronizzazione delle impostazioni di UE-V nei computer.</span><span class="sxs-lookup"><span data-stu-id="52ea7-122">You can use Group Policy to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="52ea7-123">Configurazione di UE-V con oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="52ea7-123">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

### <span data-ttu-id="52ea7-124">Amministrazione di UE-V con PowerShell e WMI</span><span class="sxs-lookup"><span data-stu-id="52ea7-124">Administering UE-V with PowerShell and WMI</span></span>

<span data-ttu-id="52ea7-125">È possibile usare PowerShell e WMI per modificare le impostazioni che definiscono la modalità di sincronizzazione delle impostazioni di UE-V nei computer.</span><span class="sxs-lookup"><span data-stu-id="52ea7-125">You can use PowerShell and WMI to modify the settings that define how UE-V synchronizes settings on computers.</span></span>

[<span data-ttu-id="52ea7-126">Gestione dei pacchetti e dell'agente di UE-V 1.0 con PowerShell e WMI</span><span class="sxs-lookup"><span data-stu-id="52ea7-126">Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI</span></span>](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md)

### <span data-ttu-id="52ea7-127">Migrazione dei pacchetti di impostazioni UE-V</span><span class="sxs-lookup"><span data-stu-id="52ea7-127">Migrating UE-V Settings Packages</span></span>

<span data-ttu-id="52ea7-128">È possibile spostare i pacchetti delle impostazioni utente quando si esegue la migrazione a un nuovo server o per scopi di backup.</span><span class="sxs-lookup"><span data-stu-id="52ea7-128">You can relocate the user settings packages either when migrating to a new server or for backup purposes.</span></span>

[<span data-ttu-id="52ea7-129">Migrazione dei pacchetti di impostazioni UE-V</span><span class="sxs-lookup"><span data-stu-id="52ea7-129">Migrating UE-V Settings Packages</span></span>](migrating-ue-v-settings-packages.md)

## <span data-ttu-id="52ea7-130">Altre risorse per questo prodotto</span><span class="sxs-lookup"><span data-stu-id="52ea7-130">Other resources for this product</span></span>


[<span data-ttu-id="52ea7-131">Operazioni per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="52ea7-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





