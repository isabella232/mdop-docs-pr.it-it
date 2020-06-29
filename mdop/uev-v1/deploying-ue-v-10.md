---
title: Distribuzione di UE-V 1.0
description: Distribuzione di UE-V 1.0
author: dansimp
ms.assetid: 519598bb-8c81-4af7-bee7-357696bff880
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1a1c515f9be950d8ca7b0a199344d34f7852073d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827146"
---
# <span data-ttu-id="02587-103">Distribuzione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="02587-103">Deploying UE-V 1.0</span></span>


<span data-ttu-id="02587-104">È disponibile una serie di configurazioni di distribuzione diverse supportate da Microsoft User Experience Virtualization (UE-V).</span><span class="sxs-lookup"><span data-stu-id="02587-104">There are a number of different deployment configurations that Microsoft User Experience Virtualization (UE-V) supports.</span></span> <span data-ttu-id="02587-105">Questa sezione include informazioni generali e procedure dettagliate per consentire di eseguire correttamente le attività che è necessario completare in diverse fasi della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="02587-105">This section includes general information and step-by-step procedures to help you successfully perform the tasks that you must complete at different stages of your deployment.</span></span>

## <span data-ttu-id="02587-106">Informazioni sulla distribuzione per UE-V</span><span class="sxs-lookup"><span data-stu-id="02587-106">Deployment information for UE-V</span></span>


<span data-ttu-id="02587-107">Una distribuzione di UE-V richiede una posizione di archiviazione delle impostazioni in una condivisione di rete e un agente UE-V installato in tutti i computer che sincronizzano le impostazioni.</span><span class="sxs-lookup"><span data-stu-id="02587-107">A UE-V deployment requires a settings storage location on a network share and a UE-V agent installed on every computer that synchronizes settings.</span></span> <span data-ttu-id="02587-108">I modelli di criteri di gruppo UE-V possono essere usati per gestire le impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="02587-108">The UE-V Group Policy templates can be used to manage UE-V settings.</span></span> <span data-ttu-id="02587-109">Gli argomenti seguenti descrivono come distribuire queste funzionalità.</span><span class="sxs-lookup"><span data-stu-id="02587-109">The following topics describe how to deploy these features.</span></span>

[<span data-ttu-id="02587-110">Distribuzione del percorso dell'archivio impostazioni per UE-v 1.0</span><span class="sxs-lookup"><span data-stu-id="02587-110">Deploying the Settings Storage Location for UE-V 1.0</span></span>](deploying-the-settings-storage-location-for-ue-v-10.md)

<span data-ttu-id="02587-111">Tutte le distribuzioni di UE-V richiedono una posizione di archiviazione delle impostazioni in cui si trovano i pacchetti di impostazioni che contengono i valori di impostazione sincronizzati.</span><span class="sxs-lookup"><span data-stu-id="02587-111">All UE-V deployments require a settings storage location where the settings packages that contain the synchronized setting values are located.</span></span>

[<span data-ttu-id="02587-112">Distribuzione dell'agente di UE-V</span><span class="sxs-lookup"><span data-stu-id="02587-112">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

<span data-ttu-id="02587-113">Per sincronizzare le impostazioni tramite UE-V, un computer deve avere l'agente UE-V installato ed eseguito.</span><span class="sxs-lookup"><span data-stu-id="02587-113">To synchronize settings by using UE-V, a computer must have the UE-V Agent installed and running.</span></span>

[<span data-ttu-id="02587-114">Installazione di modelli ADMX di Criteri di gruppo di UE-V</span><span class="sxs-lookup"><span data-stu-id="02587-114">Installing the UE-V Group Policy ADMX Templates</span></span>](installing-the-ue-v-group-policy-admx-templates.md)

<span data-ttu-id="02587-115">È possibile usare criteri di gruppo per preconfigurare le impostazioni di UE-V prima di distribuire l'agente UE-V e la configurazione standard di UE-V.</span><span class="sxs-lookup"><span data-stu-id="02587-115">You can use Group Policy to preconfigure UE-V settings before you deploy the UE-V Agent as well as standard UE-V configuration.</span></span>

## <span data-ttu-id="02587-116">Informazioni sulla distribuzione per la distribuzione di modelli personalizzati</span><span class="sxs-lookup"><span data-stu-id="02587-116">Deployment information for custom template deployment</span></span>


<span data-ttu-id="02587-117">Se si prevede di creare modelli di posizione personalizzati per le applicazioni diverse dalle applicazioni Microsoft incluse in UE-V, ad esempio applicazioni line-of-business, è possibile distribuire un catalogo di modelli di impostazioni ed è necessario installare il generatore UE-V per creare questi modelli.</span><span class="sxs-lookup"><span data-stu-id="02587-117">If you plan to create custom settings location templates for applications other than the Microsoft applications that are included in UE-V, such as line-of-business applications, then you can deploy a settings template catalog and you must install the UE-V Generator to create those templates.</span></span> <span data-ttu-id="02587-118">Per altre informazioni, vedere [pianificazione della distribuzione di modelli personalizzati per la versione UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="02587-118">For more information, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

[<span data-ttu-id="02587-119">Installazione di Generatore UE-V</span><span class="sxs-lookup"><span data-stu-id="02587-119">Installing the UE-V Generator</span></span>](installing-the-ue-v-generator.md)

<span data-ttu-id="02587-120">Usa il generatore UE-V per creare, modificare e convalidare modelli di posizione personalizzati che consentono di sincronizzare le impostazioni delle applicazioni diverse dalle applicazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="02587-120">Use the UE-V Generator to create, edit, and validate custom settings location templates that help synchronize settings of applications other than the default applications.</span></span>

[<span data-ttu-id="02587-121">Distribuzione del catalogo dei modelli di impostazioni per UE-v 1.0</span><span class="sxs-lookup"><span data-stu-id="02587-121">Deploying the Settings Template Catalog for UE-V 1.0</span></span>](deploying-the-settings-template-catalog-for-ue-v-10.md)

<span data-ttu-id="02587-122">Se è necessario distribuire modelli di posizione delle impostazioni personalizzate per supportare applicazioni diverse dalle applicazioni predefinite nell'agente UE-V, è necessario configurare un catalogo di modelli di impostazioni per archiviarli.</span><span class="sxs-lookup"><span data-stu-id="02587-122">If you need to deploy custom settings location templates to support applications other than the default applications in the UE-V Agent, you must configure a settings template catalog to store them.</span></span>

[<span data-ttu-id="02587-123">Distribuzione dei modelli percorsi impostazioni UE-V per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="02587-123">Deploying UE-V Settings Location Templates for UE-V 1.0</span></span>](deploying-ue-v-settings-location-templates-for-ue-v-10.md)

<span data-ttu-id="02587-124">Se è necessario sincronizzare applicazioni diverse dalle applicazioni predefinite nell'agente UE-V, i modelli di posizione di impostazione personalizzati creati con il generatore UE-V possono essere distribuiti nel catalogo dei modelli di impostazioni di UE-V.</span><span class="sxs-lookup"><span data-stu-id="02587-124">If you need to synchronize applications other than the default applications in the UE-V Agent, the custom setting location templates that are created with UE-V Generator can be distributed to the UE-V settings template catalog.</span></span>

<span data-ttu-id="02587-125">**Nota**  La distribuzione di modelli personalizzati richiede un catalogo di modelli di impostazioni.</span><span class="sxs-lookup"><span data-stu-id="02587-125">**Note** Deploying custom templates requires a settings template catalog.</span></span> <span data-ttu-id="02587-126">I modelli di applicazione Microsoft predefiniti vengono distribuiti con l'agente UE-V.</span><span class="sxs-lookup"><span data-stu-id="02587-126">The default Microsoft application templates are deployed with the UE-V Agent.</span></span>

 

## <span data-ttu-id="02587-127">Argomenti per questo prodotto</span><span class="sxs-lookup"><span data-stu-id="02587-127">Topics for this product</span></span>


[<span data-ttu-id="02587-128">Microsoft User Experience Virtualization (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="02587-128">Microsoft User Experience Virtualization (UE-V) 1.0</span></span>](index.md)

[<span data-ttu-id="02587-129">Attività iniziali di User Experience Virtualization 1.0</span><span class="sxs-lookup"><span data-stu-id="02587-129">Getting Started With User Experience Virtualization 1.0</span></span>](getting-started-with-user-experience-virtualization-10.md)

[<span data-ttu-id="02587-130">Pianificazione di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="02587-130">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="02587-131">Operazioni per UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="02587-131">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

[<span data-ttu-id="02587-132">Risoluzione dei problemi di UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="02587-132">Troubleshooting UE-V 1.0</span></span>](troubleshooting-ue-v-10.md)

 

 





