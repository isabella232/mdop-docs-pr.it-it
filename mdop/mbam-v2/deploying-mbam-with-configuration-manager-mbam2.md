---
title: Distribuzione di MBAM con Configuration Manager
description: Distribuzione di MBAM con Configuration Manager
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823455"
---
# <span data-ttu-id="ecd71-103">Distribuzione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ecd71-103">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="ecd71-104">Le procedure seguenti descrivono come distribuire Microsoft BitLocker Administration and Monitoring (MBAM) con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager tramite la configurazione consigliata di usingthe, descritta in [Introduzione all'uso di mbam con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="ecd71-104">The following procedures describe how to deploy Microsoft BitLocker Administration and Monitoring (MBAM) with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager by usingthe recommended configuration, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="ecd71-105">La configurazione consigliata consiste nell'installare le funzionalità di amministrazione e monitoraggio in uno o più server di amministrazione e monitoraggio di Microsoft BitLocker e installare Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager in un server separato.</span><span class="sxs-lookup"><span data-stu-id="ecd71-105">The recommended configuration is to install the Administration and Monitoring features on one or more Microsoft BitLocker Administration and Monitoring servers, and install Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager on a separate server.</span></span>

<span data-ttu-id="ecd71-106">Prima di avviare l'installazione, verificare di avere soddisfatto i prerequisiti e i requisiti hardware e software per l'installazione di MBAM con Configuration Manager, rivedendo la [pianificazione della distribuzione di mbam con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="ecd71-106">Before you start the installation, ensure that you have met the prerequisites and hardware and software requirements for installing MBAM with Configuration Manager by reviewing [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="ecd71-107">Se è necessario reinstallare MBAM con la topologia di Configuration Manager, sarà necessario rimuovere prima alcuni oggetti di Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ecd71-107">If you ever have to reinstall MBAM with the Configuration Manager topology, you will need to remove certain Configuration Manager objects first.</span></span> <span data-ttu-id="ecd71-108">Per altre informazioni, leggere l' [articolo della Knowledge base](https://go.microsoft.com/fwlink/?LinkId=286306) .</span><span class="sxs-lookup"><span data-stu-id="ecd71-108">Read the [Knowledge Base article](https://go.microsoft.com/fwlink/?LinkId=286306) for more information.</span></span>

<span data-ttu-id="ecd71-109">I passaggi per installare MBAM con Configuration Manager sono raggruppati nelle categorie seguenti.</span><span class="sxs-lookup"><span data-stu-id="ecd71-109">The steps to install MBAM with Configuration Manager are grouped into the following categories.</span></span> <span data-ttu-id="ecd71-110">Completare la procedura per ogni categoria per completare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ecd71-110">Complete the steps for each category to complete the installation.</span></span>

## <span data-ttu-id="ecd71-111">Come creare o modificare i file MOF</span><span class="sxs-lookup"><span data-stu-id="ecd71-111">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="ecd71-112">Per consentire ai computer client di segnalare i dettagli di conformità di BitLocker tramite i report di MBAM Configuration Manager, è necessario modificare il file **Configuration. mof** e modificare o creare il file Sms \ _def. mof, a seconda della versione di Configuration Manager in uso.</span><span class="sxs-lookup"><span data-stu-id="ecd71-112">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the **Configuration.mof** file, and either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

[<span data-ttu-id="ecd71-113">Come creare o modificare i file MOF</span><span class="sxs-lookup"><span data-stu-id="ecd71-113">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

## <span data-ttu-id="ecd71-114">Come installare MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ecd71-114">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="ecd71-115">Questa sezione illustra come installare le operazioni seguenti: MBAM nel server Configuration Manager; Database di ripristino e controllo nel server di database; e le funzionalità di amministrazione e monitoraggio del server nel server di amministrazione e monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="ecd71-115">This section provides steps about how to install the following: MBAM on the Configuration Manager Server; the Recovery and Audit Databases on the Database Server; and the Administration and Monitoring Server features on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="ecd71-116">Come installare MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ecd71-116">How to Install MBAM with Configuration Manager</span></span>](how-to-install-mbam-with-configuration-manager.md)

## <span data-ttu-id="ecd71-117">Come convalidare l'installazione di funzionalità di MBAM server nel server Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ecd71-117">How to Validate the MBAM Server Feature Installation on the Configuration Manager Server</span></span>


<span data-ttu-id="ecd71-118">Dopo aver completato l'installazione di amministrazione e monitoraggio di Microsoft BitLocker, verificare che l'installazione abbia configurato correttamente tutte le funzionalità necessarie per MBAM per il Server Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="ecd71-118">When the Microsoft BitLocker Administration and Monitoring installation is complete, validate that the installation has successfully set up all the necessary MBAM features required for the Configuration Manager Server.</span></span>

[<span data-ttu-id="ecd71-119">Come convalidare l'installazione di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ecd71-119">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## <span data-ttu-id="ecd71-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ecd71-120">Related topics</span></span>


[<span data-ttu-id="ecd71-121">Uso di MBAM con Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ecd71-121">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





