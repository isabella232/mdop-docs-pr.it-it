---
title: Pianificazione per i metodi di configurazione di UE-V
description: Pianificazione per i metodi di configurazione di UE-V
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827095"
---
# <span data-ttu-id="17c0f-103">Pianificazione per i metodi di configurazione di UE-V</span><span class="sxs-lookup"><span data-stu-id="17c0f-103">Planning for UE-V Configuration Methods</span></span>


<span data-ttu-id="17c0f-104">Le configurazioni Microsoft User Experience Virtualization (UE-V) determinano la sincronizzazione delle impostazioni in tutta l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="17c0f-104">Microsoft User Experience Virtualization (UE-V) configurations determine how settings are synchronized throughout the enterprise.</span></span> <span data-ttu-id="17c0f-105">Questo argomento descrive come vengono create le configurazioni UE-V per facilitare la formulazione di un piano di configurazione che soddisfi meglio i requisiti aziendali.</span><span class="sxs-lookup"><span data-stu-id="17c0f-105">This topic describes how UE-V configurations are created to help you formulate a configuration plan that best meets your business requirements.</span></span>

## <span data-ttu-id="17c0f-106">Metodi di configurazione per UE-V</span><span class="sxs-lookup"><span data-stu-id="17c0f-106">Configuration methods for UE-V</span></span>


<span data-ttu-id="17c0f-107">Puoi configurare la versione UE-V prima, durante o dopo l'installazione dell'agente, a seconda del metodo di configurazione che usi.</span><span class="sxs-lookup"><span data-stu-id="17c0f-107">You can configure UE-V before, during, or after agent installation, depending on the configuration method that you use.</span></span>

<span data-ttu-id="17c0f-108">**Criteri di gruppo:** l'infrastruttura di criteri di gruppo esistente può essere usata per configurare la versione UE-v prima o dopo la distribuzione di agenti UE-v.</span><span class="sxs-lookup"><span data-stu-id="17c0f-108">**Group Policy:** existing Group Policy infrastructure can be used to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="17c0f-109">Il modello ADMX UE-V consente la gestione centralizzata delle opzioni di configurazione dell'agente UE-V comuni e include le impostazioni per la configurazione della sincronizzazione UE-V.</span><span class="sxs-lookup"><span data-stu-id="17c0f-109">The UE-V ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span> <span data-ttu-id="17c0f-110">Gli ambienti di rete che usano criteri di gruppo possono preconfigurare UE-V in previsione della distribuzione dell'agente.</span><span class="sxs-lookup"><span data-stu-id="17c0f-110">Network environments that use Group Policy can preconfigure UE-V in anticipation of agent deployment.</span></span>

[<span data-ttu-id="17c0f-111">Configurazione di UE-V con oggetti Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="17c0f-111">Configuring UE-V with Group Policy Objects</span></span>](configuring-ue-v-with-group-policy-objects.md)

[<span data-ttu-id="17c0f-112">Installazione di modelli ADMX di Criteri di gruppo di UE-V</span><span class="sxs-lookup"><span data-stu-id="17c0f-112">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="17c0f-113">**Installazione in una riga di comando o in batch script:** i parametri usati con la distribuzione dell'agente UE-v consentono la configurazione di molte impostazioni UE-v.</span><span class="sxs-lookup"><span data-stu-id="17c0f-113">**Command-line or Batch Script Installation:** parameters that are used with the deployment of the UE-V Agent allow the configuration of many UE-V settings.</span></span> <span data-ttu-id="17c0f-114">I sistemi di distribuzione elettronica del software, ad esempio System Center Configuration Manager, usano questi parametri per configurare i client durante la distribuzione e l'installazione del software dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="17c0f-114">Electronic software distribution systems, such as System Center Configuration Manager, use these parameters to configure their clients when deploying and installing the UE-V Agent software.</span></span> <span data-ttu-id="17c0f-115">Per un elenco dei parametri di installazione e degli script di installazione di esempio, vedere [distribuzione dell'agente UE-V](deploying-the-ue-v-agent.md).</span><span class="sxs-lookup"><span data-stu-id="17c0f-115">For a list of installation parameters and sample installation scripts, see [Deploying the UE-V Agent](deploying-the-ue-v-agent.md).</span></span>

<span data-ttu-id="17c0f-116">**PowerShell e WMI:** i comandi con script che usano PowerShell o WMI possono essere usati per modificare le configurazioni dopo l'installazione dell'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="17c0f-116">**PowerShell and WMI:** scripted commands using PowerShell or WMI can be used to modify configurations after the UE-V Agent has been installed.</span></span> <span data-ttu-id="17c0f-117">Per un elenco di comandi di PowerShell e WMI, vedere [gestione dell'agente e dei pacchetti UE-V 1,0 con PowerShell e WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="17c0f-117">For a list of PowerShell and WMI commands, see [Managing the UE-V 1.0 Agent and Packages with PowerShell and WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).</span></span>

<span data-ttu-id="17c0f-118">**Modificare le impostazioni del registro di sistema:** Le impostazioni di UE-V sono archiviate nel registro di sistema e possono essere modificate usando qualsiasi strumento che può modificare le impostazioni del registro di sistema, ad esempio RegEdit.</span><span class="sxs-lookup"><span data-stu-id="17c0f-118">**Edit Registry Settings:** UE-V settings are stored in the registry and can be modified by using any tool that can modify registry settings, such as RegEdit.</span></span>

<span data-ttu-id="17c0f-119">**Nota**  La modifica del registro di sistema può causare la perdita di dati o il computer diventa inattivo.</span><span class="sxs-lookup"><span data-stu-id="17c0f-119">**Note** Registry modification can result in data loss or the computer becoming unresponsive.</span></span> <span data-ttu-id="17c0f-120">Ti consigliamo di usare altri metodi di configurazione.</span><span class="sxs-lookup"><span data-stu-id="17c0f-120">We recommend that you use other configuration methods.</span></span>

 

### <span data-ttu-id="17c0f-121">Impostazioni di configurazione di UE-V</span><span class="sxs-lookup"><span data-stu-id="17c0f-121">UE-V configuration settings</span></span>

<span data-ttu-id="17c0f-122">Di seguito sono riportati alcuni esempi di impostazioni di configurazione di UE-V:</span><span class="sxs-lookup"><span data-stu-id="17c0f-122">The following are examples of UE-V configuration settings:</span></span>

-   <span data-ttu-id="17c0f-123">**Impostazione del percorso di archiviazione:** specifica la posizione della condivisione file in cui sono archiviate le impostazioni UE-V.</span><span class="sxs-lookup"><span data-stu-id="17c0f-123">**Setting Storage Path:** specifies the location of the file share that stores the UE-V settings.</span></span>

-   <span data-ttu-id="17c0f-124">**Percorso catalogo di modelli di impostazioni:** specifica il percorso UNC (Universal Naming Convention) che definisce la posizione selezionata per i nuovi modelli di posizione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="17c0f-124">**Settings Template Catalog Path:** specifies the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span>

-   <span data-ttu-id="17c0f-125">**Registrare i modelli Microsoft:** specifica se i modelli Microsoft predefiniti devono essere registrati durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="17c0f-125">**Register Microsoft Templates:** specifies whether the default Microsoft templates should be registered during installation.</span></span>

-   <span data-ttu-id="17c0f-126">**Metodo di sincronizzazione:** specifica se la caratteristica file offline di Windows viene usata per il supporto offline.</span><span class="sxs-lookup"><span data-stu-id="17c0f-126">**Synchronization Method:** specifies whether the Windows Offline Files feature is used for offline support.</span></span>

-   <span data-ttu-id="17c0f-127">**Timeout sincronizzazione:** specifica il numero di millisecondi che il computer attende prima del timeout durante il recupero delle impostazioni utente dalla posizione di archiviazione delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="17c0f-127">**Synchronization Timeout:** specifies the number of milliseconds that the computer waits before timeout when retrieving the user settings from the settings storage location.</span></span>

-   <span data-ttu-id="17c0f-128">**Enable sincronizzazione:** specifica se la sincronizzazione delle impostazioni UE-V è abilitata o disabilitata.</span><span class="sxs-lookup"><span data-stu-id="17c0f-128">**Synchronization Enable:** specifies whether the UE-V settings synchronization is enabled or disabled.</span></span>

-   <span data-ttu-id="17c0f-129">**Dimensioni massime del pacchetto:** specifica una dimensione della soglia dei file del pacchetto di impostazioni in byte in cui l'agente UE-V segnala un avviso.</span><span class="sxs-lookup"><span data-stu-id="17c0f-129">**Maximum Package Size:** specifies a settings package file threshold size in bytes at which the UE-V Agent reports a warning.</span></span>

## <span data-ttu-id="17c0f-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="17c0f-130">Related topics</span></span>


[<span data-ttu-id="17c0f-131">Pianificazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="17c0f-131">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="17c0f-132">Pianificazione per la configurazione di UE-V</span><span class="sxs-lookup"><span data-stu-id="17c0f-132">Planning for UE-V Configuration</span></span>](planning-for-ue-v-configuration.md)

 

 





