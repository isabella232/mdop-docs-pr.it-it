---
title: Informazioni sul chip TPM del computer
description: Informazioni sul chip TPM del computer
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823535"
---
# <span data-ttu-id="a1216-103">Informazioni sul chip TPM del computer</span><span class="sxs-lookup"><span data-stu-id="a1216-103">About the Computer TPM Chip</span></span>


<span data-ttu-id="a1216-104">BitLocker offre ulteriore protezione quando viene usato con un chip TPM (Trusted Platform Module).</span><span class="sxs-lookup"><span data-stu-id="a1216-104">BitLocker provides additional protection when it is used with a Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="a1216-105">Il chip TPM è un componente hardware installato in molti computer più recenti dai produttori di computer.</span><span class="sxs-lookup"><span data-stu-id="a1216-105">The TPM chip is a hardware component that is installed in many newer computers by the computer manufacturers.</span></span> <span data-ttu-id="a1216-106">Microsoft BitLocker Administration and Monitoring (MBAM) USA BitLocker, oltre al chip TPM, per fornire ulteriore protezione dei dati e per assicurarsi che il computer non sia stato manomesso.</span><span class="sxs-lookup"><span data-stu-id="a1216-106">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker, in addition to the TPM chip, to help provide additional protection of your data and to make sure that your computer has not been tampered with.</span></span>

## <span data-ttu-id="a1216-107">Come configurare il TPM</span><span class="sxs-lookup"><span data-stu-id="a1216-107">How to Set Up Your TPM</span></span>


<span data-ttu-id="a1216-108">Quando si avvia la crittografia guidata unità BitLocker nel computer, BitLocker verifica se l'organizzazione ha configurato BitLocker per l'uso di un chip TPM.</span><span class="sxs-lookup"><span data-stu-id="a1216-108">When you start the BitLocker Drive Encryption wizard on your computer, BitLocker checks for a TPM chip if your organization has configured BitLocker to use a TPM chip.</span></span> <span data-ttu-id="a1216-109">Se BitLocker trova un chip TPM compatibile, potrebbe essere richiesto di riavviare il computer per abilitare il chip TPM per l'uso.</span><span class="sxs-lookup"><span data-stu-id="a1216-109">If BitLocker finds a compatible TPM chip, you may be prompted to restart your computer to enable the TPM chip for use.</span></span> <span data-ttu-id="a1216-110">Non appena il computer viene riavviato, seguire le istruzioni per configurare il chip TPM nel BIOS (il BIOS è un livello pre-Windows del software del computer).</span><span class="sxs-lookup"><span data-stu-id="a1216-110">As soon as your computer has restarted, follow the instructions to configure the TPM chip in the BIOS (the BIOS is a pre-Windows layer of your computer software).</span></span>

<span data-ttu-id="a1216-111">Dopo la configurazione di BitLocker, è possibile accedere ad altre informazioni sul chip TPM aprendo lo strumento di opzioni di crittografia BitLocker nel pannello di controllo di Windows e quindi selezionando **Amministrazione TPM**.</span><span class="sxs-lookup"><span data-stu-id="a1216-111">After BitLocker is configured, you can access additional information about the TPM chip by opening the BitLocker Encryption Options tool in the Windows Control Panel, and then selecting **TPM Administration**.</span></span>

<span data-ttu-id="a1216-112">**Nota**  Per accedere a questo strumento, è necessario disporre delle credenziali amministrative nel computer.</span><span class="sxs-lookup"><span data-stu-id="a1216-112">**Note** You must have administrative credentials on your computer to access this tool.</span></span>

 

<span data-ttu-id="a1216-113">In un errore del TPM, una modifica del BIOS o alcuni aggiornamenti di Windows, BitLocker bloccherà il computer e richiederà di contattare il supporto tecnico per sbloccarlo.</span><span class="sxs-lookup"><span data-stu-id="a1216-113">In a TPM failure, a change in the BIOS, or certain Windows Updates, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="a1216-114">È necessario specificare il nome del computer e il dominio del computer.</span><span class="sxs-lookup"><span data-stu-id="a1216-114">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="a1216-115">Help desk può fornire un file di password che può essere usato per sbloccare il computer.</span><span class="sxs-lookup"><span data-stu-id="a1216-115">Help Desk can give you a password file that can be used to unlock your computer.</span></span>

## <span data-ttu-id="a1216-116">Risoluzione dei problemi relativi al TPM</span><span class="sxs-lookup"><span data-stu-id="a1216-116">Troubleshooting TPM Issues</span></span>


<span data-ttu-id="a1216-117">Se si verifica un errore di TPM, la modifica nel BIOS o alcuni aggiornamenti di Windows, BitLocker bloccherà il computer e richiederà di contattare il supporto tecnico per sbloccarlo.</span><span class="sxs-lookup"><span data-stu-id="a1216-117">If a TPM failure, change in the BIOS, or certain Windows Updates occur, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="a1216-118">È necessario specificare il nome del computer e il dominio del computer.</span><span class="sxs-lookup"><span data-stu-id="a1216-118">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="a1216-119">Il supporto tecnico può fornire un file di password che può essere usato per sbloccare il computer.</span><span class="sxs-lookup"><span data-stu-id="a1216-119">The Help Desk can give you a password file that you can use to unlock your computer.</span></span>

## <span data-ttu-id="a1216-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a1216-120">Related topics</span></span>


[<span data-ttu-id="a1216-121">Aiutare gli utenti finali a gestire BitLocker</span><span class="sxs-lookup"><span data-stu-id="a1216-121">Helping End Users Manage BitLocker</span></span>](helping-end-users-manage-bitlocker.md)

[<span data-ttu-id="a1216-122">Uso di PIN o password</span><span class="sxs-lookup"><span data-stu-id="a1216-122">Using Your PIN or Password</span></span>](using-your-pin-or-password.md)

 

 





