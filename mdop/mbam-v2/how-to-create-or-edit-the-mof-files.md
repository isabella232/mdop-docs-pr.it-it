---
title: Come creare o modificare i file MOF
description: Come creare o modificare i file MOF
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825325"
---
# <span data-ttu-id="53743-103">Come creare o modificare i file MOF</span><span class="sxs-lookup"><span data-stu-id="53743-103">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="53743-104">Prima di installare Microsoft BitLocker Administration and Monitoring (MBAM) con Configuration Manager, è necessario modificare il file Configuration. mof.</span><span class="sxs-lookup"><span data-stu-id="53743-104">Before you install Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, you need to edit the Configuration.mof file.</span></span> <span data-ttu-id="53743-105">È inoltre necessario modificare o creare il file SMS \ _def. mof, a seconda della versione di Configuration Manager in uso.</span><span class="sxs-lookup"><span data-stu-id="53743-105">You also need to either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

## <span data-ttu-id="53743-106">Modificare il file Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="53743-106">Edit the Configuration.mof File</span></span>


<span data-ttu-id="53743-107">Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker tramite i report di MBAM Configuration Manager, è necessario modificare il file Configuration. mof per Microsoft System Center Configuration Manager 2007 e SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="53743-107">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file for Microsoft System Center Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span>

[<span data-ttu-id="53743-108">Modificare il file Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="53743-108">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="53743-109">Creare o modificare il file SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="53743-109">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="53743-110">Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker nei report di MBAM Configuration Manager, è necessario creare o modificare il file SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="53743-110">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="53743-111">In Configuration Manager 2007 il file esiste già, quindi è necessario modificare, ma non sovrascrivere, il file esistente.</span><span class="sxs-lookup"><span data-stu-id="53743-111">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span> <span data-ttu-id="53743-112">Se si usa il ConfigurationManager di SystemCenter2012, è necessario creare il file.</span><span class="sxs-lookup"><span data-stu-id="53743-112">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span>

[<span data-ttu-id="53743-113">Creare o modificare il file SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="53743-113">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file.md)

## <span data-ttu-id="53743-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53743-114">Related topics</span></span>


[<span data-ttu-id="53743-115">Distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="53743-115">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





