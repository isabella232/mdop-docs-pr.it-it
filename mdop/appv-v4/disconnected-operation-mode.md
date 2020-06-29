---
title: Modalità di operazioni senza connessione
description: Modalità di operazioni senza connessione
author: dansimp
ms.assetid: 3f9849ea-ba53-4c68-85d3-87a4218f59c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e9534b93f23b17e5258ef5e2d548eb93213f2f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821625"
---
# <span data-ttu-id="f089d-103">Modalità di operazioni senza connessione</span><span class="sxs-lookup"><span data-stu-id="f089d-103">Disconnected Operation Mode</span></span>


<span data-ttu-id="f089d-104">Le impostazioni della modalità di operazione disconnessa, accessibile facendo clic con il pulsante destro del mouse sul nodo **Application Virtualization** , selezionando **Proprietà**e facendo clic sulla scheda **connettività** , consentono al client Desktop Application Virtualization o al client per Servizi Desktop remoto (in precedenza Servizi terminal) di eseguire applicazioni archiviate nella cache del file System del client quando il client non è in grado di connettersi al server Application Virtualization Management.</span><span class="sxs-lookup"><span data-stu-id="f089d-104">The disconnected operation mode settings—accessible by right-clicking the **Application Virtualization** node, selecting **Properties**, and clicking the **Connectivity** tab—enables the Application Virtualization Desktop Client or Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client is unable to connect to the Application Virtualization Management Server.</span></span>

<span data-ttu-id="f089d-105">Motivi per cui la mancata connessione al server include l'errore del server, l'interruzione della rete o la disconnessione dalla rete.</span><span class="sxs-lookup"><span data-stu-id="f089d-105">Reasons for failure to connect to the server include server failure, network outage, or disconnection from the network.</span></span> <span data-ttu-id="f089d-106">Se si verifica un errore, il client passerà automaticamente all'operazione disconnessa.</span><span class="sxs-lookup"><span data-stu-id="f089d-106">If any failure occurs, the client will automatically switch to disconnected operation.</span></span> <span data-ttu-id="f089d-107">Dopo la disconnessione, se il client necessita di dati aggiuntivi dal server per continuare a eseguire un'applicazione o se il timeout dell'operazione disconnessa scade, il client tenterà di riconnettersi al server.</span><span class="sxs-lookup"><span data-stu-id="f089d-107">After it is disconnected, if the client needs additional data from the server to continue to run an application or if the disconnected operation time-out expires, the client will attempt to reconnect to the server.</span></span> <span data-ttu-id="f089d-108">Se il tentativo di connessione non riesce, l'applicazione verrà chiusa.</span><span class="sxs-lookup"><span data-stu-id="f089d-108">If this connection attempt fails, the application will be shut down.</span></span>

<span data-ttu-id="f089d-109">Per impostazione predefinita, l'operazione disconnessa è abilitata e il timeout è impostato su 90 giorni.</span><span class="sxs-lookup"><span data-stu-id="f089d-109">By default, disconnected operation is enabled and the time-out is set to 90 days.</span></span> <span data-ttu-id="f089d-110">Il valore di timeout viene specificato come numero di giorni per cui si vuole limitare la modalità di operazione disconnessa ed è possibile immettere un valore da 1-999.</span><span class="sxs-lookup"><span data-stu-id="f089d-110">The time-out value is specified as the number of days you want to limit disconnected operation mode, and you can enter a value from 1–999.</span></span>

## <span data-ttu-id="f089d-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f089d-111">Related topics</span></span>


[<span data-ttu-id="f089d-112">Come disabilitare o modificare le impostazioni della modalità di operazioni senza connessione</span><span class="sxs-lookup"><span data-stu-id="f089d-112">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





