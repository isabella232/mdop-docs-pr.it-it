---
title: Attività iniziali di MBAM 1.0
description: Attività iniziali di MBAM 1.0
author: dansimp
ms.assetid: 4fab4e4a-d25e-4661-b235-2b45bf5ac3e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0bbbcabfb25cfc8b24cbb4cbc3d344d4e7f209b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825275"
---
# <span data-ttu-id="97e7e-103">Attività iniziali di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97e7e-103">Getting Started with MBAM 1.0</span></span>

> <span data-ttu-id="97e7e-104">**Importante** MBAM 1,0 raggiungerà la fine del supporto il 14 settembre 2021.</span><span class="sxs-lookup"><span data-stu-id="97e7e-104">**IMPORTANT** MBAM 1.0 will reach end of support on September 14, 2021.</span></span> 
> <span data-ttu-id="97e7e-105">Per altre informazioni, vedere la [pagina ciclo](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) di vita.</span><span class="sxs-lookup"><span data-stu-id="97e7e-105">See our [lifecycle page](https://support.microsoft.com/lifecycle/search?alpha=Microsoft%20BitLocker%20Administration%20and%20Monitoring%201.0) for more information.</span></span> <span data-ttu-id="97e7e-106">È consigliabile [eseguire la migrazione a mbam 2,5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) o a un'altra versione supportata di mbam oppure eseguire la migrazione della gestione di BitLocker a [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span><span class="sxs-lookup"><span data-stu-id="97e7e-106">We recommend [migrating to MBAM 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/upgrading-to-mbam-25-or-mbam-25-sp1-from-previous-versions) or another supported version of MBAM, or migrating your BitLocker management to [Microsoft Endpoint Manager](https://www.microsoft.com/microsoft-365/microsoft-endpoint-manager).</span></span>


<span data-ttu-id="97e7e-107">Microsoft BitLocker Administration and Monitoring (MBAM) richiede una pianificazione completa prima di distribuirla o utilizzarne le caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="97e7e-107">Microsoft BitLocker Administration and Monitoring (MBAM) requires thorough planning before you deploy it or use its features.</span></span> <span data-ttu-id="97e7e-108">Poiché questo prodotto può influire su tutti i computer dell'organizzazione, è possibile che l'intera rete venga interrotta se non si prevede di pianificare la distribuzione con attenzione.</span><span class="sxs-lookup"><span data-stu-id="97e7e-108">Because this product can affect every computer in your organization, you might disrupt your entire network if you do not plan your deployment carefully.</span></span> <span data-ttu-id="97e7e-109">Tuttavia, se pianifichi la distribuzione con attenzione e la Gestisci in modo che soddisfi le esigenze aziendali, MBAM può contribuire a ridurre il sovraccarico amministrativo e il costo totale della proprietà.</span><span class="sxs-lookup"><span data-stu-id="97e7e-109">However, if you plan your deployment carefully and manage it so that it meets your business needs, MBAM can help reduce your administrative overhead and total cost of ownership.</span></span>

<span data-ttu-id="97e7e-110">Se si è nuovi a questo prodotto, è consigliabile leggere accuratamente la documentazione.</span><span class="sxs-lookup"><span data-stu-id="97e7e-110">If you are new to this product, we recommend that you read the documentation thoroughly.</span></span> <span data-ttu-id="97e7e-111">Prima di distribuirla in un ambiente di produzione, è consigliabile convalidare il piano di distribuzione in un ambiente di rete di test.</span><span class="sxs-lookup"><span data-stu-id="97e7e-111">Before you deploy it to a production environment, we also recommend that you validate your deployment plan in a test network environment.</span></span> <span data-ttu-id="97e7e-112">Potresti anche prendere in considerazione l'assunzione di una classe sulle tecnologie rilevanti.</span><span class="sxs-lookup"><span data-stu-id="97e7e-112">You might also consider taking a class about relevant technologies.</span></span> <span data-ttu-id="97e7e-113">Per altre informazioni sulle opportunità di formazione per Microsoft, vedere Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347> .</span><span class="sxs-lookup"><span data-stu-id="97e7e-113">For more information about Microsoft training opportunities, see the Microsoft Training Overview at <https://go.microsoft.com/fwlink/p/?LinkId=80347>.</span></span>

<span data-ttu-id="97e7e-114">**Nota**  È possibile trovare una versione scaricabile di questa documentazione e la guida alla valutazione di MBAM <https://go.microsoft.com/fwlink/p/?LinkId=225356> .</span><span class="sxs-lookup"><span data-stu-id="97e7e-114">**Note** You can find a downloadable version of this documentation and the MBAM Evaluation Guide at <https://go.microsoft.com/fwlink/p/?LinkId=225356>.</span></span>

 

<span data-ttu-id="97e7e-115">Questa sezione della Guida di MBAM Administrator include informazioni di alto livello su MBAM per offrirti una conoscenza di base del prodotto prima di iniziare la pianificazione della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="97e7e-115">This section of the MBAM Administrator’s Guide includes high-level information about MBAM to provide you with a basic understanding of the product before you begin the deployment planning.</span></span> <span data-ttu-id="97e7e-116">Ulteriore documentazione di MBAM può essere trovata nella pagina di download della documentazione di MBAM Resources <https://go.microsoft.com/fwlink/p/?LinkId=258391> .</span><span class="sxs-lookup"><span data-stu-id="97e7e-116">Additional MBAM documentation can be found on the MBAM Documentation Resources Download page at <https://go.microsoft.com/fwlink/p/?LinkId=258391>.</span></span>

## <span data-ttu-id="97e7e-117">Guida introduttiva a MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="97e7e-117">Getting started with MBAM 1.0</span></span>


-   [<span data-ttu-id="97e7e-118">Informazioni su MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97e7e-118">About MBAM 1.0</span></span>](about-mbam-10.md)

    <span data-ttu-id="97e7e-119">Offre una panoramica di alto livello su MBAM e su come può essere usata nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="97e7e-119">Provides a high-level overview of MBAM and how it can be used in your organization.</span></span>

-   [<span data-ttu-id="97e7e-120">Valutazione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97e7e-120">Evaluating MBAM 1.0</span></span>](evaluating-mbam-10.md)

    <span data-ttu-id="97e7e-121">Fornisce informazioni su come è possibile valutare meglio MBAM per l'uso nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="97e7e-121">Provides information about how you can best evaluate MBAM for use in your organization.</span></span>

-   [<span data-ttu-id="97e7e-122">Architettura di alto livello per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97e7e-122">High Level Architecture for MBAM 1.0</span></span>](high-level-architecture-for-mbam-10.md)

    <span data-ttu-id="97e7e-123">Fornisce una descrizione delle caratteristiche di MBAM e del modo in cui collaborano.</span><span class="sxs-lookup"><span data-stu-id="97e7e-123">Provides a description of the MBAM features and how they work together.</span></span>

-   [<span data-ttu-id="97e7e-124">Accessibilità per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97e7e-124">Accessibility for MBAM 1.0</span></span>](accessibility-for-mbam-10.md)

    <span data-ttu-id="97e7e-125">Fornisce informazioni sulle caratteristiche e i servizi che rendono questo prodotto e la relativa documentazione più accessibile per gli utenti con disabilità.</span><span class="sxs-lookup"><span data-stu-id="97e7e-125">Provides information about features and services that make this product and its corresponding documentation more accessible for people with disabilities.</span></span>

## <a href="" id="other-resources-for-this-product-"></a><span data-ttu-id="97e7e-126">Altre risorse per questo prodotto</span><span class="sxs-lookup"><span data-stu-id="97e7e-126">Other resources for this product</span></span>


-   [<span data-ttu-id="97e7e-127">Guida per l'amministrazione e il monitoraggio di Microsoft BitLocker 1</span><span class="sxs-lookup"><span data-stu-id="97e7e-127">Microsoft BitLocker Administration and Monitoring 1 Administrator's Guide</span></span>](index.md)

-   [<span data-ttu-id="97e7e-128">Pianificazione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97e7e-128">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

-   [<span data-ttu-id="97e7e-129">Distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97e7e-129">Deploying MBAM 1.0</span></span>](deploying-mbam-10.md)

-   [<span data-ttu-id="97e7e-130">Operazioni relative a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97e7e-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

-   [<span data-ttu-id="97e7e-131">Risoluzione dei problemi relativi a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="97e7e-131">Troubleshooting MBAM 1.0</span></span>](troubleshooting-mbam-10.md)

 

 





