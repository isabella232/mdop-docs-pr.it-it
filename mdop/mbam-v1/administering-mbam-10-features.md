---
title: Amministrazione delle funzionalità di MBAM 1.0
description: Amministrazione delle funzionalità di MBAM 1.0
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821225"
---
# <span data-ttu-id="5c8a6-103">Amministrazione delle funzionalità di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5c8a6-103">Administering MBAM 1.0 Features</span></span>


<span data-ttu-id="5c8a6-104">Dopo aver completato tutte le necessarie pianificazione e distribuzione di Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurare e usare MBAM per gestire la crittografia BitLocker aziendale.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-104">After you complete all necessary Microsoft BitLocker Administration and Monitoring (MBAM) planning and deployment, you can configure and use MBAM to manage enterprise BitLocker encryption.</span></span> <span data-ttu-id="5c8a6-105">Le informazioni in questa sezione illustrano le attività quotidiane di post-installazione di MBAM.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-105">The information in this section describes post-installation day-to-day MBAM feature operations tasks.</span></span>

## <span data-ttu-id="5c8a6-106">Gestire i ruoli di amministratore di MBAM</span><span class="sxs-lookup"><span data-stu-id="5c8a6-106">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="5c8a6-107">Dopo aver completato la configurazione di MBAM per tutte le funzionalità del server, agli utenti amministrativi deve essere concesso l'accesso a queste funzionalità del server.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-107">After MBAM Setup is complete for all server features, administrative users must be granted access to these server features.</span></span> <span data-ttu-id="5c8a6-108">Come procedura consigliata, gli amministratori che gestiscono o usano le caratteristiche di MBAM server devono essere assegnati a gruppi di sicurezza di Active Directory e quindi tali gruppi devono essere aggiunti al gruppo locale amministrativo di MBAM appropriato.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-108">As a best practice, administrators who will manage or use MBAM server features, should be assigned to Active Directory security groups and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="5c8a6-109">Come gestire i ruoli di amministrazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="5c8a6-109">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-1.md)

## <span data-ttu-id="5c8a6-110">Gestire la compatibilità hardware</span><span class="sxs-lookup"><span data-stu-id="5c8a6-110">Manage Hardware Compatibility</span></span>


<span data-ttu-id="5c8a6-111">La funzionalità di compatibilità hardware di MBAM può essere utile per verificare che solo l'hardware del computer specificato come supporto di BitLocker venga crittografato.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-111">The MBAM Hardware Compatibility feature can help you to ensure that only the computer hardware that you specify as supporting BitLocker will be encrypted.</span></span> <span data-ttu-id="5c8a6-112">Quando questa funzionalità è attivata, bit \ _admmontla Crittografa solo i computer contrassegnati come compatibili.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-112">When this feature is turned on, bit\_admmontla will encrypt only computers that are marked as Compatible.</span></span>

<span data-ttu-id="5c8a6-113">**Importante**  Quando questa caratteristica è disattivata, verranno crittografati tutti i computer in cui viene distribuito il criterio MBAM.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-113">**Important** When this feature is turned off, all computers where the MBAM policy is deployed will be encrypted.</span></span>

 

<span data-ttu-id="5c8a6-114">MBAM può raccogliere informazioni sia sulla creazione che sul modello di computer client se si distribuisce il criterio di gruppo "Consenti compatibilità hardware".</span><span class="sxs-lookup"><span data-stu-id="5c8a6-114">MBAM can collect information on both the make and model of client computers if you deploy the “Allow Hardware Compatibility Checking” Group Policy.</span></span> <span data-ttu-id="5c8a6-115">Se si configura questo criterio, l'agente di MBAM riporta il computer e le informazioni sul modello al server MBAM quando il client MBAM viene distribuito in un computer client.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-115">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

[<span data-ttu-id="5c8a6-116">Come gestire la compatibilità hardware</span><span class="sxs-lookup"><span data-stu-id="5c8a6-116">How to Manage Hardware Compatibility</span></span>](how-to-manage-hardware-compatibility-mbam-1.md)

[<span data-ttu-id="5c8a6-117">Come gestire le esenzioni della crittografia BitLocker dell'utente</span><span class="sxs-lookup"><span data-stu-id="5c8a6-117">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## <span data-ttu-id="5c8a6-118">Gestire le esenzioni crittografiche di BitLocker</span><span class="sxs-lookup"><span data-stu-id="5c8a6-118">Manage BitLocker encryption exemptions</span></span>


<span data-ttu-id="5c8a6-119">MBAM può concedere due forme di esenzione dalla crittografia BitLocker: esenzione dal computer e esenzione dall'utente.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-119">MBAM can grant two forms of exemption from BitLocker encryption: computer exemption and user exemption.</span></span> <span data-ttu-id="5c8a6-120">L'esenzione dal computer viene in genere usata quando una società dispone di computer che non devono essere crittografati, ad esempio i computer usati in sviluppo o test o i computer meno recenti che non supportano BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-120">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="5c8a6-121">In alcuni casi, la legge locale può anche richiedere che determinati computer non siano crittografati.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-121">In some cases, local law may also require that certain computers are not encrypted.</span></span> <span data-ttu-id="5c8a6-122">Si può anche scegliere di esonerare gli utenti che non hanno bisogno o vogliono che le unità vengano crittografate.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-122">You may also choose to exempt users who do not need or want their drives encrypted.</span></span>

[<span data-ttu-id="5c8a6-123">Come gestire le esenzioni della crittografia BitLocker del computer</span><span class="sxs-lookup"><span data-stu-id="5c8a6-123">How to Manage Computer BitLocker Encryption Exemptions</span></span>](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## <span data-ttu-id="5c8a6-124">Gestire le opzioni di crittografia di BitLocker client di MBAM tramite il pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="5c8a6-124">Manage MBAM Client BitLocker Encryption Options by using the Control Panel</span></span>


<span data-ttu-id="5c8a6-125">Se abilitata tramite un oggetto Criteri di gruppo, un pannello di controllo di MBAM personalizzato denominato opzioni di crittografia BitLocker sarà disponibile in **sistema e sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-125">If enabled through a Group Policy Objects (GPO), a custom MBAM control panel that is named BitLocker Encryption Options will be available under **System and Security**.</span></span> <span data-ttu-id="5c8a6-126">Questo pannello di controllo personalizzato sostituisce il pannello di controllo BitLocker predefinito di Windows.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-126">This customized control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="5c8a6-127">Il pannello di controllo di MBAM consente di sbloccare le unità crittografate (fisse e rimovibili) e consente anche di gestire il PIN o la password.</span><span class="sxs-lookup"><span data-stu-id="5c8a6-127">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span>

[<span data-ttu-id="5c8a6-128">Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="5c8a6-128">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## <span data-ttu-id="5c8a6-129">Altre risorse per l'amministrazione delle funzionalità di MBAM</span><span class="sxs-lookup"><span data-stu-id="5c8a6-129">Other resources for Administering MBAM features</span></span>


[<span data-ttu-id="5c8a6-130">Operazioni relative a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="5c8a6-130">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





