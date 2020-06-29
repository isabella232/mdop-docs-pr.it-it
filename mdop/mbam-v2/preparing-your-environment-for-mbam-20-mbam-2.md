---
title: Preparazione dell'ambiente per MBAM 2.0
description: Preparazione dell'ambiente per MBAM 2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825606"
---
# <span data-ttu-id="0912f-103">Preparazione dell'ambiente per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0912f-103">Preparing your Environment for MBAM 2.0</span></span>


<span data-ttu-id="0912f-104">Prima di iniziare l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM), verificare di avere soddisfatto i prerequisiti per installare il prodotto.</span><span class="sxs-lookup"><span data-stu-id="0912f-104">Before beginning Microsoft BitLocker Administration and Monitoring (MBAM) Setup, you should make sure that you have met the prerequisites to install the product.</span></span> <span data-ttu-id="0912f-105">Quando si sa quali sono i prerequisiti in anticipo, è possibile distribuire il prodotto in modo efficiente e abilitarne le funzionalità per consentire il supporto più efficace degli obiettivi aziendali dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="0912f-105">When you know what the prerequisites are ahead of time, you can efficiently deploy the product and enable its features so that it most effectively supports your organization’s business objectives.</span></span>

<span data-ttu-id="0912f-106">Se si distribuisce l'amministrazione e il monitoraggio di Microsoft BitLocker con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager, vedere [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="0912f-106">If you are deploying Microsoft BitLocker Administration and Monitoring with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager, see [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

## <span data-ttu-id="0912f-107">Verificare i prerequisiti di distribuzione di MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="0912f-107">Review MBAM 2.0 Deployment Prerequisites</span></span>


<span data-ttu-id="0912f-108">Il client MBAM e ognuna delle funzionalità di MBAM server presentano prerequisiti specifici che devono essere soddisfatti prima che possano essere installati correttamente.</span><span class="sxs-lookup"><span data-stu-id="0912f-108">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="0912f-109">Per garantire l'installazione di successo di MBAM client e le caratteristiche del server MBAM, assicurarsi che i computer specificati per MBAM client o MBAM Server funzionalità di installazione sono adeguatamente preparati per la configurazione MBAM.</span><span class="sxs-lookup"><span data-stu-id="0912f-109">To ensure successful installation of MBAM Clients and MBAM Server features, ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="0912f-110">**Nota**  La configurazione di MBAM controlla che tutti i prerequisiti vengano soddisfatti prima dell'avvio dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="0912f-110">**Note** MBAM Setup checks that all prerequisites are met before installation starts.</span></span> <span data-ttu-id="0912f-111">Se non sono soddisfatti tutti i prerequisiti, il programma di installazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0912f-111">If all prerequisites are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="0912f-112">Prerequisiti per la distribuzione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0912f-112">MBAM 2.0 Deployment Prerequisites</span></span>](mbam-20-deployment-prerequisites-mbam-2.md)

## <span data-ttu-id="0912f-113">Pianificare i requisiti di criteri di gruppo di MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="0912f-113">Plan for MBAM 2.0 Group Policy Requirements</span></span>


<span data-ttu-id="0912f-114">Prima che MBAM possa gestire i client nell'organizzazione, è necessario definire criteri di gruppo per i requisiti di crittografia dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="0912f-114">Before MBAM can manage clients in the enterprise, you must define Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="0912f-115">**Importante**  MBAM non funziona con i criteri per la crittografia unità BitLocker autonoma.</span><span class="sxs-lookup"><span data-stu-id="0912f-115">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="0912f-116">Le impostazioni dei criteri di gruppo devono essere definite per MBAM o la crittografia e l'imposizione di BitLocker non avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0912f-116">Group Policy settings must be defined for MBAM, or BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="0912f-117">Pianificazione dei requisiti di Criteri di gruppo per MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0912f-117">Planning for MBAM 2.0 Group Policy Requirements</span></span>](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## <span data-ttu-id="0912f-118">Pianificare i ruoli di amministratore di MBAM 2,0</span><span class="sxs-lookup"><span data-stu-id="0912f-118">Plan for MBAM 2.0 Administrator Roles</span></span>


<span data-ttu-id="0912f-119">I ruoli di amministratore di MBAM sono gestiti da gruppi locali creati dalla configurazione di MBAM quando si installa il server di amministrazione e monitoraggio di BitLocker, la caratteristica rapporti di conformità e controllo e il database di stato di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="0912f-119">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="0912f-120">L'appartenenza ai ruoli di amministrazione e monitoraggio di Microsoft BitLocker può essere gestita in modo ottimale tramite la creazione di gruppi di sicurezza in ActiveDirectoryDomainServices, l'aggiunta degli account di amministratore appropriati a tali gruppi e quindi l'aggiunta di tali gruppi di sicurezza ai gruppi locali di amministrazione e monitoraggio di BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0912f-120">The membership of Microsoft BitLocker Administration and Monitoring roles can best be managed by creating security groups in ActiveDirectoryDomainServices, adding the appropriate administrator accounts to those groups, and then adding those security groups to the BitLocker Administration and Monitoring local groups.</span></span> <span data-ttu-id="0912f-121">Per altre informazioni, Vedi [come gestire i ruoli di amministratore di mbam](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="0912f-121">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

## <span data-ttu-id="0912f-122">Altre risorse per la pianificazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="0912f-122">Other Resources for MBAM Planning</span></span>


[<span data-ttu-id="0912f-123">Pianificazione di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0912f-123">Planning for MBAM 2.0</span></span>](planning-for-mbam-20-mbam-2.md)

[<span data-ttu-id="0912f-124">Configurazioni supportate di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="0912f-124">MBAM 2.0 Supported Configurations</span></span>](mbam-20-supported-configurations-mbam-2.md)

 

 





