---
title: Distribuzione dei modelli percorsi impostazioni UE-V per UE-V 1.0
description: Distribuzione dei modelli percorsi impostazioni UE-V per UE-V 1.0
author: dansimp
ms.assetid: 7e0cc553-14f7-40fa-828a-281c8d2d1934
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b276fb9d6c0b3749f9818483869dfe98bbc147c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827125"
---
# <span data-ttu-id="f120e-103">Distribuzione dei modelli percorsi impostazioni UE-V per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f120e-103">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>


<span data-ttu-id="f120e-104">Microsoft User Experience Virtualization (UE-V) USA i modelli di posizione delle impostazioni (file XML) che definiscono le impostazioni acquisite e applicate dalla virtualizzazione dell'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="f120e-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by User Experience Virtualization.</span></span> <span data-ttu-id="f120e-105">UE-V include un set di modelli standard, oltre a uno strumento, il generatore UE-V, che consente di creare modelli di posizione delle impostazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="f120e-105">UE-V includes a set of standard templates, as well as a tool, the UE-V Generator, which allows you to create custom settings location templates.</span></span> <span data-ttu-id="f120e-106">Dopo aver creato un modello di posizione delle impostazioni, è consigliabile testarlo per verificare che le impostazioni dell'applicazione scorrano correttamente in un ambiente di test.</span><span class="sxs-lookup"><span data-stu-id="f120e-106">After you create a settings location template, you should test it to ensure that the application settings roam correctly in a test environment.</span></span> <span data-ttu-id="f120e-107">Puoi quindi distribuire il modello di posizione delle impostazioni in modo sicuro ai computer dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="f120e-107">You can then safely deploy the settings location template to computers in the enterprise.</span></span>

<span data-ttu-id="f120e-108">I modelli di posizione delle impostazioni possono essere distribuiti tramite ESD (Enterprise Software Distribution), preferenze di criteri di gruppo o configurando un catalogo di modelli di impostazioni UE-V.</span><span class="sxs-lookup"><span data-stu-id="f120e-108">Settings location templates can be deployed by using enterprise software distribution (ESD), Group Policy preferences, or by configuring a UE-V settings template catalog.</span></span> <span data-ttu-id="f120e-109">I modelli distribuiti tramite ESD o criteri di gruppo devono essere registrati tramite WMI o PowerShell di UE-V.</span><span class="sxs-lookup"><span data-stu-id="f120e-109">Templates that are deployed by using an ESD or Group Policy must be registered through UE-V WMI or PowerShell.</span></span> <span data-ttu-id="f120e-110">I modelli archiviati nella posizione del catalogo dei modelli di impostazioni vengono automaticamente registrati dall'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f120e-110">Templates that are stored in the settings template catalog location are automatically registered by the UE-V agent.</span></span>

## <span data-ttu-id="f120e-111">Distribuire i modelli di posizione delle impostazioni con un percorso catalogo di modelli di impostazioni</span><span class="sxs-lookup"><span data-stu-id="f120e-111">Deploy the settings location templates with a settings template catalog path</span></span>


<span data-ttu-id="f120e-112">Il percorso del catalogo dei modelli della posizione delle impostazioni di UE-V può essere definito usando i metodi seguenti: criteri di gruppo, l'installazione dell'agente parametri della riga di comando, WMI o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f120e-112">The UE-V settings location template catalog path can be defined by using the following methods: Group Policy, the agent install command-line parameters, WMI, or PowerShell.</span></span> <span data-ttu-id="f120e-113">Dopo aver definito il percorso del catalogo dei modelli, l'agente UE-V recupera i modelli nuovi o aggiornati da questa posizione.</span><span class="sxs-lookup"><span data-stu-id="f120e-113">After the template catalog path has been defined, the UE-V agent retrieves the new or updated templates from this location.</span></span> <span data-ttu-id="f120e-114">L'agente UE-V controlla la posizione una volta al giorno e aggiorna il comportamento di sincronizzazione in base ai modelli presenti nella cartella.</span><span class="sxs-lookup"><span data-stu-id="f120e-114">The UE-V agent checks this location once each day and updates its synchronization behavior based on the templates found in this folder.</span></span> <span data-ttu-id="f120e-115">I modelli che sono stati aggiunti o aggiornati in questa cartella dall'ultimo controllo vengono registrati dall'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f120e-115">Templates that have been added or updated in this folder since the last check are registered by the UE-V agent.</span></span> <span data-ttu-id="f120e-116">L'agente UE-V annulla anche la registrazione dei modelli rimossi dalla cartella.</span><span class="sxs-lookup"><span data-stu-id="f120e-116">The UE-V agent also unregisters templates that have been removed from this folder.</span></span> <span data-ttu-id="f120e-117">I modelli sono registrati e non registrati una volta al giorno dall'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="f120e-117">Templates are registered and unregistered one time per day by the task scheduler.</span></span>

**<span data-ttu-id="f120e-118">Per usare il percorso del catalogo delle impostazioni per distribuire i modelli di posizione delle impostazioni di UE-V</span><span class="sxs-lookup"><span data-stu-id="f120e-118">To use settings template catalog path to deploy UE-V settings location templates</span></span>**

1.  <span data-ttu-id="f120e-119">Passare alla cartella della condivisione di rete definita come catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f120e-119">Navigate to the network share folder that is defined as the settings template catalog.</span></span>

2.  <span data-ttu-id="f120e-120">Aggiungere, rimuovere o aggiornare i modelli di posizione delle impostazioni nel catalogo dei modelli di impostazioni per riflettere la configurazione del modello di agente UE-V desiderata per i computer UE-V.</span><span class="sxs-lookup"><span data-stu-id="f120e-120">Add, remove, or update settings location templates in the settings template catalog to reflect the desired UE-V agent template configuration for UE-V computers.</span></span>

3.  <span data-ttu-id="f120e-121">I modelli nei computer vengono aggiornati giornalmente in base alle modifiche apportate al catalogo dei modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="f120e-121">Templates on computers are updated daily based on changes to the settings template catalog.</span></span>

4.  <span data-ttu-id="f120e-122">Aprire un prompt dei comandi con privilegi elevati e passare a \*\*% Program Files%\\Microsoft User Experience Virtualization \ \ Agent \ \ &lt; x86 o x64 &gt; \*\*, quindi eseguire **ApplySettingsTemplateCatalog.exe** per aggiornare manualmente i modelli in un computer che esegue l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="f120e-122">Open an elevated command prompt and navigate to **%program files%\\Microsoft user Experience Virtualization \\ Agent \\ &lt;x86 or x64 &gt;**, and then run **ApplySettingsTemplateCatalog.exe** to manually update templates on a computer that runs the UE-V agent.</span></span>

## <span data-ttu-id="f120e-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f120e-123">Related topics</span></span>


[<span data-ttu-id="f120e-124">Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="f120e-124">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="f120e-125">Distribuzione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f120e-125">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="f120e-126">Pianificazione delle applicazioni da sincronizzare con UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="f120e-126">Planning Which Applications to Synchronize with UE-V 1.0</span></span>](planning-which-applications-to-synchronize-with-ue-v-10.md)

 

 





