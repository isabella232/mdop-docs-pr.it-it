---
title: Preparazione dell'ambiente per MBAM 1.0
description: Preparazione dell'ambiente per MBAM 1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823195"
---
# <span data-ttu-id="31801-103">Preparazione dell'ambiente per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="31801-103">Preparing your Environment for MBAM 1.0</span></span>


<span data-ttu-id="31801-104">Prima di iniziare l'installazione di Microsoft BitLocker Administration and Monitoring (MBAM), verificare di avere soddisfatto i prerequisiti necessari per installare il prodotto.</span><span class="sxs-lookup"><span data-stu-id="31801-104">Before you begin the Microsoft BitLocker Administration and Monitoring (MBAM) Setup, make sure that you have met the necessary prerequisites to install the product.</span></span> <span data-ttu-id="31801-105">Se si conoscono i prerequisiti in anticipo, è possibile distribuire il prodotto in modo efficiente e abilitarne le caratteristiche, in grado di supportare più efficacemente gli obiettivi aziendali dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="31801-105">If you know the prerequisites in advance, you can efficiently deploy the product and enable its features, which can support the business objectives of your organization more effectively.</span></span>

## <span data-ttu-id="31801-106">Verificare i prerequisiti di distribuzione di MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="31801-106">Review MBAM 1.0 deployment prerequisites</span></span>


<span data-ttu-id="31801-107">Il client MBAM e ognuna delle funzionalità di MBAM server presentano prerequisiti specifici che devono essere soddisfatti prima che possano essere installati correttamente.</span><span class="sxs-lookup"><span data-stu-id="31801-107">The MBAM Client and each of the MBAM Server features have specific prerequisites that must be met before they can be successfully installed.</span></span>

<span data-ttu-id="31801-108">Per garantire l'installazione di successo di MBAM client e le caratteristiche del server MBAM, si dovrebbe pianificare per garantire che i computer specificati per MBAM client o MBAM Server funzionalità di installazione sono adeguatamente preparati per la configurazione MBAM.</span><span class="sxs-lookup"><span data-stu-id="31801-108">To ensure successful installation of MBAM Clients and MBAM Server features, you should plan to ensure that computers specified for MBAM Client or MBAM Server feature installation are properly prepared for MBAM Setup.</span></span>

<span data-ttu-id="31801-109">**Nota**  MBAM setup verifica se tutti i prerequisiti vengono soddisfatti prima dell'avvio dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="31801-109">**Note** MBAM Setup verifies if all prerequisites are met before installation starts.</span></span> <span data-ttu-id="31801-110">Se non sono soddisfatte, il programma di installazione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="31801-110">If they are not met, Setup will fail.</span></span>

 

[<span data-ttu-id="31801-111">Prerequisiti per la distribuzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="31801-111">MBAM 1.0 Deployment Prerequisites</span></span>](mbam-10-deployment-prerequisites.md)

## <span data-ttu-id="31801-112">Pianificare i requisiti di criteri di gruppo di MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="31801-112">Plan for MBAM 1.0 Group Policy requirements</span></span>


<span data-ttu-id="31801-113">Prima che MBAM possa gestire i client nell'organizzazione, è necessario definire i criteri di gruppo per i requisiti di crittografia dell'ambiente.</span><span class="sxs-lookup"><span data-stu-id="31801-113">Before MBAM can manage clients in the enterprise, you must define the Group Policy for the encryption requirements of your environment.</span></span>

<span data-ttu-id="31801-114">**Importante**  MBAM non funziona con i criteri per la crittografia unità BitLocker autonoma.</span><span class="sxs-lookup"><span data-stu-id="31801-114">**Important** MBAM will not work with policies for stand-alone BitLocker drive encryption.</span></span> <span data-ttu-id="31801-115">I criteri di gruppo devono essere definiti per MBAM; in caso contrario, la crittografia e l'imposizione di BitLocker avranno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="31801-115">Group Policy must be defined for MBAM; otherwise, the BitLocker encryption and enforcement will fail.</span></span>

 

[<span data-ttu-id="31801-116">Pianificazione dei requisiti di Criteri di gruppo per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="31801-116">Planning for MBAM 1.0 Group Policy Requirements</span></span>](planning-for-mbam-10-group-policy-requirements.md)

## <span data-ttu-id="31801-117">Pianificare i ruoli di amministratore di MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="31801-117">Plan for MBAM 1.0 administrator roles</span></span>


<span data-ttu-id="31801-118">I ruoli di amministratore di MBAM sono gestiti da gruppi locali creati tramite MBAM setup quando si installano le operazioni seguenti: server di amministrazione e monitoraggio di BitLocker, la caratteristica conformità e report di controllo e il database di stato di conformità e controllo.</span><span class="sxs-lookup"><span data-stu-id="31801-118">MBAM administrator roles are managed by local groups that are created by MBAM Setup when you install the following: BitLocker Administration and Monitoring Server, the Compliance and Audit Reports feature, and the Compliance and Audit Status Database.</span></span>

<span data-ttu-id="31801-119">L'appartenenza ai ruoli di MBAM può essere gestita in modo più efficace se si creano gruppi di sicurezza in ActiveDirectoryDomainServices, si aggiungono gli account di amministratore appropriati a tali gruppi e quindi si aggiungono tali gruppi di sicurezza ai gruppi locali di MBAM.</span><span class="sxs-lookup"><span data-stu-id="31801-119">The membership of MBAM roles can be managed more effectively if you create security groups in ActiveDirectoryDomainServices, add the appropriate administrator accounts to those groups, and then add those security groups to the MBAM local groups.</span></span> <span data-ttu-id="31801-120">Per altre informazioni, Vedi [come gestire i ruoli di amministratore di mbam](how-to-manage-mbam-administrator-roles-mbam-1.md).</span><span class="sxs-lookup"><span data-stu-id="31801-120">For more information, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-1.md).</span></span>

[<span data-ttu-id="31801-121">Pianificazione dei ruoli di amministrazione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="31801-121">Planning for MBAM 1.0 Administrator Roles</span></span>](planning-for-mbam-10-administrator-roles.md)

## <span data-ttu-id="31801-122">Altre risorse per la pianificazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="31801-122">Other resources for MBAM planning</span></span>


[<span data-ttu-id="31801-123">Pianificazione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="31801-123">Planning for MBAM 1.0</span></span>](planning-for-mbam-10.md)

 

 





