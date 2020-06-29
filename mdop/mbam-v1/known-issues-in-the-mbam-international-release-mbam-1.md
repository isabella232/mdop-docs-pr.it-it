---
title: Problemi noti nella versione internazionale di MBAM
description: Problemi noti nella versione internazionale di MBAM
author: dansimp
ms.assetid: bbf888dc-93c1-4323-b43c-0ded098e9b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af32551135ff297d25930f94b40bf04c0fcaaafe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825786"
---
# <span data-ttu-id="1cff7-103">Problemi noti nella versione internazionale di MBAM</span><span class="sxs-lookup"><span data-stu-id="1cff7-103">Known Issues in the MBAM International Release</span></span>

<span data-ttu-id="1cff7-104">Questa sezione contiene problemi noti per il rilascio di Microsoft BitLocker Administration and Monitoring (MBAM) International release.</span><span class="sxs-lookup"><span data-stu-id="1cff7-104">This section contains known issues for Microsoft BitLocker Administration and Monitoring (MBAM) International Release.</span></span>

## <span data-ttu-id="1cff7-105">Problemi noti nella versione internazionale di MBAM</span><span class="sxs-lookup"><span data-stu-id="1cff7-105">Known Issues in the MBAM International Release</span></span>

### <span data-ttu-id="1cff7-106">Il processo di installazione non specifica l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="1cff7-106">The Installation Process Does Not Specify Update</span></span>

<span data-ttu-id="1cff7-107">Dopo aver aggiornato il server o i server di amministrazione e monitoraggio di Microsoft BitLocker, il programma di installazione non dichiara che è in corso l'installazione di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1cff7-107">Upon updating the Microsoft BitLocker Administration and Monitoring server or servers, the Setup program does not state that an update is being installed.</span></span>

<span data-ttu-id="1cff7-108">**Soluzione alternativa**: None.</span><span class="sxs-lookup"><span data-stu-id="1cff7-108">**Workaround**: None.</span></span>

### <span data-ttu-id="1cff7-109">Certificati usati per il ruolo del server di amministrazione e monitoraggio</span><span class="sxs-lookup"><span data-stu-id="1cff7-109">Certificates Used for the Administration and Monitoring Server Role</span></span>

<span data-ttu-id="1cff7-110">Se si usa un certificato per l'autenticazione tra i server MBAM, dopo aver aggiornato l'amministrazione e il server di monitoraggio di MBAM è necessario assicurarsi che il certificato sia valido e non revocato o scaduto.</span><span class="sxs-lookup"><span data-stu-id="1cff7-110">If you are using a certificate for authentication between MBAM servers, after updating the MBAM Administration and Monitoring server you must ensure that the certificate is valid and not revoked or expired.</span></span>

<span data-ttu-id="1cff7-111">**Soluzione alternativa**: None.</span><span class="sxs-lookup"><span data-stu-id="1cff7-111">**Workaround**: None.</span></span>

### <span data-ttu-id="1cff7-112">MBAM svclog spazio su disco di riempimento file</span><span class="sxs-lookup"><span data-stu-id="1cff7-112">MBAM Svclog File Filling Disk Space</span></span>

<span data-ttu-id="1cff7-113">Se è stato seguito l' [articolo 2668170 della Knowledge base](https://go.microsoft.com/fwlink/?LinkID=247277), potrebbe essere necessario ripetere i passaggi della KB dopo l'installazione di questo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1cff7-113">If you have followed [Knowledge Base article 2668170](https://go.microsoft.com/fwlink/?LinkID=247277), you might have to repeat the KB steps after you install this update.</span></span>

<span data-ttu-id="1cff7-114">**Soluzione alternativa**: None.</span><span class="sxs-lookup"><span data-stu-id="1cff7-114">**Workaround**: None.</span></span>

## <span data-ttu-id="1cff7-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1cff7-115">Related topics</span></span>

[<span data-ttu-id="1cff7-116">Distribuzione dell'aggiornamento della versione localizzata di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="1cff7-116">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





