---
title: Amministrazione di UE-V 2. x
description: Amministrazione di UE-V 2. x
author: dansimp
ms.assetid: 996e4797-8383-4627-b714-24a84c907798
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2674f6ace80672c1e89bb4f9c765b56f260c3bc0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825675"
---
# <span data-ttu-id="7aaf8-103">Amministrazione di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-103">Administering UE-V 2.x</span></span>


<span data-ttu-id="7aaf8-104">Dopo aver distribuito Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 o 2,1 SP1, è necessario essere in grado di eseguire varie attività amministrative in corso, ad esempio gestire la configurazione dell'agente UE-V e recuperare le impostazioni perse.</span><span class="sxs-lookup"><span data-stu-id="7aaf8-104">After you have deployed Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1, you must be able to perform various ongoing administrative tasks, such as managing the configuration of the UE-V Agent and recovering lost settings.</span></span> <span data-ttu-id="7aaf8-105">Queste attività di post-installazione sono descritte nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7aaf8-105">These post-installation tasks are described in the following sections.</span></span>

## <span data-ttu-id="7aaf8-106">Gestione delle configurazioni di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-106">Managing UE-V 2.x configurations</span></span>


<span data-ttu-id="7aaf8-107">Nel corso del ciclo di vita UE-V è necessario gestire la configurazione dell'agente UE-V e gestire anche i percorsi di archiviazione per le risorse, ad esempio i file di pacchetto delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7aaf8-107">In the course of the UE-V lifecycle, you have to manage the configuration of the UE-V Agent and also manage storage locations for resources such as settings package files.</span></span>

[<span data-ttu-id="7aaf8-108">Gestire le configurazioni per UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-108">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

## <span data-ttu-id="7aaf8-109">Uso dei modelli personalizzati UE-V e del generatore UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-109">Working with custom UE-V templates and the UE-V 2.x Generator</span></span>


<span data-ttu-id="7aaf8-110">Questo argomento fornisce istruzioni su come usare il generatore UE-V e gestire i modelli di posizione delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="7aaf8-110">This topic provides instructions for how to use the UE-V Generator and manage custom settings location templates.</span></span>

[<span data-ttu-id="7aaf8-111">Uso dei modelli Custom UE-V 2. x e del generatore UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-111">Working with Custom UE-V 2.x Templates and the UE-V 2.x Generator</span></span>](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

## <span data-ttu-id="7aaf8-112">Eseguire il backup e il ripristino delle impostazioni dell'applicazione e di Windows sincronizzate con UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-112">Backup and restore application and Windows settings that are synchronized with UE-V 2.x</span></span>


<span data-ttu-id="7aaf8-113">Le funzionalità di Strumentazione gestione Windows (WMI) e Windows PowerShell di UE-V consentono di ripristinare i pacchetti di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7aaf8-113">Windows Management Instrumentation (WMI) and Windows PowerShell features of UE-V provide the ability to restore settings packages.</span></span> <span data-ttu-id="7aaf8-114">Usando i comandi WMI e Windows PowerShell, puoi ripristinare lo stato originale delle impostazioni dell'applicazione e di Windows e ripristinare le impostazioni aggiuntive quando un utente adotta un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7aaf8-114">By using WMI and Windows PowerShell commands, you can restore application and Windows settings to their original state and restore additional settings when a user adopts a new device.</span></span>

[<span data-ttu-id="7aaf8-115">Gestire il backup e il ripristino amministrativi in UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-115">Manage Administrative Backup and Restore in UE-V 2.x</span></span>](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md)

## <span data-ttu-id="7aaf8-116">Modifica della frequenza delle attività pianificate di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-116">Changing the frequency of UE-V 2.x scheduled tasks</span></span>


<span data-ttu-id="7aaf8-117">È possibile configurare le attività pianificate che gestiscono quando la sezione UE-V Verifica la possibilità di impostazioni nuove o aggiornate o i modelli di posizione delle impostazioni personalizzate aggiornate nel catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="7aaf8-117">You can configure the scheduled tasks that manage when UE-V checks for new or updated settings or for updated custom settings location templates in the settings template catalog.</span></span>

[<span data-ttu-id="7aaf8-118">Modifica della frequenza delle attività pianificate di UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-118">Changing the Frequency of UE-V 2.x Scheduled Tasks</span></span>](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

## <span data-ttu-id="7aaf8-119">Migrazione dei pacchetti di impostazioni UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-119">Migrating UE-V 2.x settings packages</span></span>


<span data-ttu-id="7aaf8-120">È possibile rilocare i pacchetti delle impostazioni utente quando si esegue la migrazione a un nuovo server o a scopo di backup.</span><span class="sxs-lookup"><span data-stu-id="7aaf8-120">You can relocate the user settings packages either when they migrate to a new server or for backup purposes.</span></span>

[<span data-ttu-id="7aaf8-121">Migrazione dei pacchetti di impostazioni UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-121">Migrating UE-V 2.x Settings Packages</span></span>](migrating-ue-v-2x-settings-packages-both-uevv2.md)

## <span data-ttu-id="7aaf8-122">Uso di UE-V 2. x con applicazioni di virtualizzazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="7aaf8-122">Using UE-V 2.x with Application Virtualization applications</span></span>


<span data-ttu-id="7aaf8-123">È possibile usare UE-V con Microsoft Application Virtualization (App-V) per condividere le impostazioni tra le applicazioni virtuali e le applicazioni installate in più computer.</span><span class="sxs-lookup"><span data-stu-id="7aaf8-123">You can use UE-V with Microsoft Application Virtualization (App-V) to share settings between virtual applications and installed applications across multiple computers.</span></span>

[<span data-ttu-id="7aaf8-124">Uso di UE-V 2. x con applicazioni di virtualizzazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="7aaf8-124">Using UE-V 2.x with Application Virtualization Applications</span></span>](using-ue-v-2x-with-application-virtualization-applications-both-uevv2.md)

## <span data-ttu-id="7aaf8-125">Altre risorse per questo prodotto</span><span class="sxs-lookup"><span data-stu-id="7aaf8-125">Other resources for this product</span></span>


-   [<span data-ttu-id="7aaf8-126">Microsoft User Experience Virtualization (UE-V) 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-126">Microsoft User Experience Virtualization (UE-V) 2.x</span></span>](index.md)

-   [<span data-ttu-id="7aaf8-127">Introduzione a UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-127">Get Started with UE-V 2.x</span></span>](get-started-with-ue-v-2x-new-uevv2.md)

-   [<span data-ttu-id="7aaf8-128">Preparare una distribuzione UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-128">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [<span data-ttu-id="7aaf8-129">Risoluzione dei problemi relativi a UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-129">Troubleshooting UE-V 2.x</span></span>](troubleshooting-ue-v-2x-both-uevv2.md)

-   [<span data-ttu-id="7aaf8-130">Documentazione tecnica su UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="7aaf8-130">Technical Reference for UE-V 2.x</span></span>](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





