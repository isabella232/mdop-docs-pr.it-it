---
title: Amministrazione delle funzionalità di MBAM 2.0
description: Amministrazione delle funzionalità di MBAM 2.0
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823506"
---
# <span data-ttu-id="33784-103">Amministrazione delle funzionalità di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="33784-103">Administering MBAM 2.0 Features</span></span>


<span data-ttu-id="33784-104">Dopo aver completato tutte le pianificazioni necessarie e aver poi distribuito Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurarlo e usarlo per gestire la crittografia BitLocker nell'organizzazione le informazioni in questa sezione descrivono le attività di amministrazione e monitoraggio di Microsoft BitLocker per la gestione quotidiana delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="33784-104">After completing all necessary planning and then deploying Microsoft BitLocker Administration and Monitoring (MBAM), you can configure and use it to manage BitLocker encryption across the enterprise The information in this section describes post-installation day-to-day Microsoft BitLocker Administration and Monitoring feature operations tasks.</span></span>

## <span data-ttu-id="33784-105">Gestire i ruoli di amministratore di MBAM</span><span class="sxs-lookup"><span data-stu-id="33784-105">Manage MBAM Administrator Roles</span></span>


<span data-ttu-id="33784-106">Dopo aver completato la configurazione di MBAM per tutte le funzionalità del server, agli utenti amministrativi deve essere concesso l'accesso.</span><span class="sxs-lookup"><span data-stu-id="33784-106">After MBAM Setup is complete for all server features, administrative users have to be granted access to them.</span></span> <span data-ttu-id="33784-107">Come procedura consigliata, gli amministratori che gestiscono o usano le caratteristiche di MBAM server devono essere assegnati ai gruppi di sicurezza di Active Directory Domain Services e quindi tali gruppi devono essere aggiunti al gruppo locale amministrativo di MBAM appropriato.</span><span class="sxs-lookup"><span data-stu-id="33784-107">As a best practice, administrators who will manage or use MBAM server features should be assigned to Active Directory Domain Services security groups, and then those groups should be added to the appropriate MBAM administrative local group.</span></span>

[<span data-ttu-id="33784-108">Come gestire i ruoli di amministrazione di MBAM</span><span class="sxs-lookup"><span data-stu-id="33784-108">How to Manage MBAM Administrator Roles</span></span>](how-to-manage-mbam-administrator-roles-mbam-2.md)

## <span data-ttu-id="33784-109">Gestire le esenzioni crittografiche di BitLocker</span><span class="sxs-lookup"><span data-stu-id="33784-109">Manage BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="33784-110">MBAM consente di concedere esenzioni di crittografia a utenti specifici che non hanno bisogno o vogliono crittografare le unità.</span><span class="sxs-lookup"><span data-stu-id="33784-110">MBAM lets you grant encryption exemptions to specific users who do not need or want their drives encrypted.</span></span> <span data-ttu-id="33784-111">L'esenzione dal computer viene in genere usata quando una società dispone di computer che non devono essere crittografati, ad esempio i computer usati in sviluppo o test o i computer meno recenti che non supportano BitLocker.</span><span class="sxs-lookup"><span data-stu-id="33784-111">Computer exemption is typically used when a company has computers that do not have to be encrypted, such as computers that are used in development or testing, or older computers that do not support BitLocker.</span></span> <span data-ttu-id="33784-112">In alcuni casi, la legge locale può anche richiedere che determinati computer non siano crittografati.</span><span class="sxs-lookup"><span data-stu-id="33784-112">In some cases, local law may also require that certain computers are not encrypted.</span></span>

[<span data-ttu-id="33784-113">Come gestire le esenzioni della crittografia BitLocker dell'utente</span><span class="sxs-lookup"><span data-stu-id="33784-113">How to Manage User BitLocker Encryption Exemptions</span></span>](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## <span data-ttu-id="33784-114">Gestire le opzioni di crittografia di BitLocker client di MBAM tramite il pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="33784-114">Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="33784-115">MBAM fornisce un pannello di controllo personalizzato, denominato opzioni di crittografia BitLocker, che verrà visualizzato in **sistema e sicurezza**.</span><span class="sxs-lookup"><span data-stu-id="33784-115">MBAM provides a custom control panel, called BitLocker Encryption Options, that will appear under **System and Security**.</span></span> <span data-ttu-id="33784-116">Il pannello di controllo di MBAM può essere usato per sbloccare le unità fisse e rimovibili crittografate e gestire anche il PIN o la password.</span><span class="sxs-lookup"><span data-stu-id="33784-116">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span>

<span data-ttu-id="33784-117">**Nota**  Questo pannello di controllo personalizzato non sostituisce il pannello di controllo BitLocker predefinito di Windows.</span><span class="sxs-lookup"><span data-stu-id="33784-117">**Note** This customized control panel does not replace the default Windows BitLocker control panel.</span></span>

 

[<span data-ttu-id="33784-118">Come gestire le opzioni di crittografia BitLocker del client MBAM usando il Pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="33784-118">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## <span data-ttu-id="33784-119">Altre risorse per l'amministrazione delle funzionalità di MBAM</span><span class="sxs-lookup"><span data-stu-id="33784-119">Other Resources for Administering MBAM Features</span></span>


[<span data-ttu-id="33784-120">Operazioni relative a MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="33784-120">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





