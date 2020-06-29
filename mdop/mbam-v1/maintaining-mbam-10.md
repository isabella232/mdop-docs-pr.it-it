---
title: Manutenzione di MBAM 1.0
description: Manutenzione di MBAM 1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825775"
---
# <span data-ttu-id="31da3-103">Manutenzione di MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="31da3-103">Maintaining MBAM 1.0</span></span>


<span data-ttu-id="31da3-104">Dopo aver completato tutte le pianificazioni necessarie e quindi distribuito Microsoft BitLocker Administration and Monitoring (MBAM), è possibile configurare MBAM per l'esecuzione in modo altamente disponibile durante l'uso per gestire le operazioni di crittografia di BitLocker aziendali.</span><span class="sxs-lookup"><span data-stu-id="31da3-104">After you complete all the necessary planning and then deploy Microsoft BitLocker Administration and Monitoring (MBAM), you can configure MBAM to run in a highly available fashion while using it to manage enterprise BitLocker encryption operations.</span></span> <span data-ttu-id="31da3-105">Le informazioni in questa sezione descrive le opzioni di disponibilità elevata per MBAM, nonché come trasferire le funzionalità del server MBAM, se necessario.</span><span class="sxs-lookup"><span data-stu-id="31da3-105">The information in this section describes high availability options for MBAM, as well as how to move MBAM Server features if necessary.</span></span>

## <span data-ttu-id="31da3-106">MBAM Management Pack</span><span class="sxs-lookup"><span data-stu-id="31da3-106">MBAM Management Pack</span></span>


<span data-ttu-id="31da3-107">Il Management Pack di MicrosoftSystemCenterOperationsManager per MBAM è disponibile per il download dall'area download Microsoft.</span><span class="sxs-lookup"><span data-stu-id="31da3-107">The MicrosoftSystemCenterOperationsManager Management Pack for MBAM is available for download from the Microsoft Download Center.</span></span>

<span data-ttu-id="31da3-108">Questo Management Pack monitora le interazioni critiche nell'infrastruttura lato server, ad esempio le connessioni tra i servizi Web e i database e le chiamate operative tra i siti Web e il servizio Web di supporto.</span><span class="sxs-lookup"><span data-stu-id="31da3-108">This management pack monitors the critical interactions in the server-side infrastructure, such as the connections between the web services and databases and the operational calls between websites and their supportive web service.</span></span> <span data-ttu-id="31da3-109">Carica inoltre le richieste tra client desktop e i rispettivi endpoint di servizio Web di ricezione.</span><span class="sxs-lookup"><span data-stu-id="31da3-109">It also uploads the requests between desktop clients and their respective receiving web service endpoints.</span></span>

[<span data-ttu-id="31da3-110">Amministrazione e monitoraggio di Microsoft BitLocker Management Pack</span><span class="sxs-lookup"><span data-stu-id="31da3-110">Microsoft BitLocker Administration And Monitoring Management Pack</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## <span data-ttu-id="31da3-111">Garantire la disponibilità elevata per MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="31da3-111">Ensure high availability for MBAM 1.0</span></span>


<span data-ttu-id="31da3-112">MBAM è progettato per essere a tolleranza d'errore.</span><span class="sxs-lookup"><span data-stu-id="31da3-112">MBAM is designed to be fault-tolerant.</span></span> <span data-ttu-id="31da3-113">Se un server diventa non disponibile, gli utenti non devono essere colpiti negativamente.</span><span class="sxs-lookup"><span data-stu-id="31da3-113">If a server becomes unavailable, the users should not be negatively affected.</span></span> <span data-ttu-id="31da3-114">Le informazioni in questa sezione possono essere usate per configurare un'installazione di MBAM a elevata disponibilità.</span><span class="sxs-lookup"><span data-stu-id="31da3-114">The information in this section can be used to configure a highly available MBAM installation.</span></span>

[<span data-ttu-id="31da3-115">Disponibilità elevata per MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="31da3-115">High Availability for MBAM 1.0</span></span>](high-availability-for-mbam-10.md)

## <span data-ttu-id="31da3-116">Trasferire le caratteristiche di MBAM 1,0 a un altro server</span><span class="sxs-lookup"><span data-stu-id="31da3-116">Move MBAM 1.0 features to another server</span></span>


<span data-ttu-id="31da3-117">Quando è necessario trasferire una caratteristica di un server MBAM da un computer server a un altro, esiste un ordine specifico e i passaggi necessari per evitare perdite di produttività o dati.</span><span class="sxs-lookup"><span data-stu-id="31da3-117">When you need to move an MBAM Server feature from one server computer to another, there is a specific order and required steps that you should follow to avoid loss of productivity or data.</span></span> <span data-ttu-id="31da3-118">Questa sezione descrive i passaggi da eseguire per trasferire una o più funzionalità di MBAM server in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="31da3-118">This section describes the steps that you should take to move one or more MBAM Server features to a different computer.</span></span>

[<span data-ttu-id="31da3-119">Come spostare le funzionalità di MBAM 1.0 in un altro computer</span><span class="sxs-lookup"><span data-stu-id="31da3-119">How to Move MBAM 1.0 Features to Another Computer</span></span>](how-to-move-mbam-10-features-to-another-computer.md)

## <span data-ttu-id="31da3-120">Altre risorse per la manutenzione di MBAM</span><span class="sxs-lookup"><span data-stu-id="31da3-120">Other resources for maintaining MBAM</span></span>


[<span data-ttu-id="31da3-121">Operazioni relative a MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="31da3-121">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





