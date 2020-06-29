---
title: Gestione degli aggiornamenti software per le aree di lavoro MED-V
description: Gestione degli aggiornamenti software per le aree di lavoro MED-V
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824815"
---
# <span data-ttu-id="1a76b-103">Gestione degli aggiornamenti software per le aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1a76b-103">Managing Software Updates for MED-V Workspaces</span></span>


<span data-ttu-id="1a76b-104">Sono disponibili diverse opzioni per fornire gli aggiornamenti software per le applicazioni nell'area di lavoro MED-V distribuita.</span><span class="sxs-lookup"><span data-stu-id="1a76b-104">You have several different options available to you for providing software updates for the applications in the deployed MED-V workspace.</span></span>

<span data-ttu-id="1a76b-105">**Nota**  Per informazioni su come specificare le impostazioni di configurazione che definiscono la modalità di ricezione degli aggiornamenti automatici in MED-V, vedere [gestione degli aggiornamenti automatici per le aree di lavoro MED-v](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="1a76b-105">**Note** For information about how to specify the configuration settings that define how MED-V receives automatic updates, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

 

**<span data-ttu-id="1a76b-106">Aggiornamento del software in un'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1a76b-106">Updating Software in a MED-V Workspace</span></span>**

1.  **<span data-ttu-id="1a76b-107">Uso di un sistema elettronico di distribuzione del software</span><span class="sxs-lookup"><span data-stu-id="1a76b-107">Using an Electronic Software Distribution System</span></span>**

    <span data-ttu-id="1a76b-108">Se l'organizzazione usa un sistema ESD (Electronic Software Distribution System) per distribuire il software, è possibile usarlo per ottenere gli aggiornamenti software per le applicazioni nelle aree di lavoro MED-V così come vengono forniti gli aggiornamenti per le applicazioni nei computer fisici.</span><span class="sxs-lookup"><span data-stu-id="1a76b-108">If your organization uses an Electronic Software Distribution System (ESD) system to deploy software, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

2.  **<span data-ttu-id="1a76b-109">Uso di criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="1a76b-109">Using Group Policy</span></span>**

    <span data-ttu-id="1a76b-110">Se l'organizzazione distribuisce il software tramite criteri di gruppo, è possibile usarlo per ottenere gli aggiornamenti software per le applicazioni nelle aree di lavoro MED-V così come vengono forniti gli aggiornamenti per le applicazioni nei computer fisici.</span><span class="sxs-lookup"><span data-stu-id="1a76b-110">If your organization deploys software by using Group Policy, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

3.  **<span data-ttu-id="1a76b-111">Uso della virtualizzazione delle applicazioni (APP-V)</span><span class="sxs-lookup"><span data-stu-id="1a76b-111">Using Application Virtualization (APP-V)</span></span>**

    <span data-ttu-id="1a76b-112">Se si usa MED-V insieme a App-V, è possibile specificare gli aggiornamenti software per le applicazioni nell'area di lavoro MED-V seguendo i passaggi richiesti da App-V per l'aggiornamento del software.</span><span class="sxs-lookup"><span data-stu-id="1a76b-112">If you use MED-V together with App-V, you can provide software updates to applications in the MED-V workspace by following the steps that are required by App-V for updating software.</span></span> <span data-ttu-id="1a76b-113">Per altre informazioni, Vedi [virtualizzazione delle applicazioni](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="1a76b-113">For more information, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

4.  **<span data-ttu-id="1a76b-114">Aggiornamento del software nell'immagine principale</span><span class="sxs-lookup"><span data-stu-id="1a76b-114">Updating Software in the Core Image</span></span>**

    <span data-ttu-id="1a76b-115">Anche se non è considerata una procedura consigliata per MED-V, è possibile installare gli aggiornamenti software per le applicazioni nell'immagine principale.</span><span class="sxs-lookup"><span data-stu-id="1a76b-115">Although not considered a MED-V best practice, you can install software updates to applications on the core image.</span></span> <span data-ttu-id="1a76b-116">Dopo aver installato gli aggiornamenti, è possibile ridistribuire l'area di lavoro MED-V all'organizzazione come è stata distribuita in origine.</span><span class="sxs-lookup"><span data-stu-id="1a76b-116">After you have installed the updates, you can then redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

    <span data-ttu-id="1a76b-117">**Importante**  Questo metodo di gestione degli aggiornamenti software non è consigliabile.</span><span class="sxs-lookup"><span data-stu-id="1a76b-117">**Important** We do not recommend this method of managing software updates.</span></span> <span data-ttu-id="1a76b-118">Inoltre, se aggiorni il software nell'immagine principale e Ridistribuisci l'area di lavoro MED-V all'interno dell'organizzazione, la prima volta che la configurazione deve essere eseguita di nuovo e tutti i dati salvati nella macchina virtuale andranno perduti.</span><span class="sxs-lookup"><span data-stu-id="1a76b-118">In addition, if you update software in the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="1a76b-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a76b-119">Related topics</span></span>


[<span data-ttu-id="1a76b-120">Gestione degli aggiornamenti automatici per le aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1a76b-120">Managing Automatic Updates for MED-V Workspaces</span></span>](managing-automatic-updates-for-med-v-workspaces.md)

[<span data-ttu-id="1a76b-121">Come verificare la pubblicazione delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="1a76b-121">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="1a76b-122">Come pubblicare e annullare la pubblicazione di un'applicazione nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="1a76b-122">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





