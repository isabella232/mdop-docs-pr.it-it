---
title: Come configurare il client per la modalità di operazioni senza connessione
description: Come configurare il client per la modalità di operazioni senza connessione
author: dansimp
ms.assetid: 3b48464a-b8b4-494b-93e3-9a6d9bd74652
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1c917d87996a26b330551deb04b1828c31fd3c73
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817816"
---
# <span data-ttu-id="68a07-103">Come configurare il client per la modalità di operazioni senza connessione</span><span class="sxs-lookup"><span data-stu-id="68a07-103">How to Configure the Client for Disconnected Operation Mode</span></span>


<span data-ttu-id="68a07-104">La modalità operativa disconnessa consente al client Desktop Application Virtualization (App-V) o al client Application Virtualization (App-V) per Servizi Desktop remoto (in precedenza Servizi terminal) di eseguire applicazioni archiviate nella cache del file System del client quando il client non riesce a connettersi al server di gestione di App-V.</span><span class="sxs-lookup"><span data-stu-id="68a07-104">The disconnected operation mode enables the Application Virtualization (App-V) Desktop Client or the Application Virtualization (App-V) Client for Remote Desktop Services (formerly Terminal Services) to run applications that are stored in the file system cache of the client when the client cannot connect to the App-V Management Server.</span></span>

<span data-ttu-id="68a07-105">**Importante**  In un'organizzazione di grandi dimensioni in cui più server Host sessione Desktop remoto (in precedenza Terminal Server) sono collegati in una farm per supportare molti utenti, l'uso di un'unica App-V Management Server per supportare la farm rappresenta un singolo punto di errore.</span><span class="sxs-lookup"><span data-stu-id="68a07-105">**Important** In a large organization where multiple Remote Desktop Session Host (RD°Session Host) servers (formerly Terminal Servers) are linked in a farm to support many users, using a single App-V Management Server to support the farm represents a single point of failure.</span></span> <span data-ttu-id="68a07-106">Per ottenere una disponibilità elevata per supportare la farm host di RDSession, è consigliabile collegare due o più server di gestione di App-V per usare lo stesso database.</span><span class="sxs-lookup"><span data-stu-id="68a07-106">To provide high availability to support the RDSession Host farm, consider linking two or more App-V Management Servers to use the same database.</span></span>

 

**<span data-ttu-id="68a07-107">Per abilitare la modalità di operazione disconnessa</span><span class="sxs-lookup"><span data-stu-id="68a07-107">To enable disconnected operation mode</span></span>**

-   <span data-ttu-id="68a07-108">Impostare il valore della chiave del registro di sistema seguente uguale a 1 per abilitare la modalità di operazione disconnessa:</span><span class="sxs-lookup"><span data-stu-id="68a07-108">Set the following registry key value equal to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="68a07-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="68a07-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

**<span data-ttu-id="68a07-110">Per impostare un limite di tempo per l'uso della modalità di operazione disconnessa</span><span class="sxs-lookup"><span data-stu-id="68a07-110">To set a time limit on disconnected operation mode use</span></span>**

1.  <span data-ttu-id="68a07-111">Impostare il valore della chiave del registro di sistema seguente su 1:</span><span class="sxs-lookup"><span data-stu-id="68a07-111">Set the following registry key value to 1:</span></span>

    <span data-ttu-id="68a07-112">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="68a07-112">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

2.  <span data-ttu-id="68a07-113">Impostare il valore della chiave del registro di sistema seguente sul numero di minuti per cui si vuole limitare la modalità di operazione disconnessa.</span><span class="sxs-lookup"><span data-stu-id="68a07-113">Set the following registry key value to the number of minutes you want to limit disconnected operation mode.</span></span> <span data-ttu-id="68a07-114">L'intervallo di valori valido è 1-999999.</span><span class="sxs-lookup"><span data-stu-id="68a07-114">The valid range of values is 1–999999.</span></span> <span data-ttu-id="68a07-115">Il valore predefinito è 90 giorni o 129.600 minuti.</span><span class="sxs-lookup"><span data-stu-id="68a07-115">The default value is 90 days or 129,600 minutes.</span></span>

    <span data-ttu-id="68a07-116">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span><span class="sxs-lookup"><span data-stu-id="68a07-116">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\DOTimeoutMinutes</span></span>

**<span data-ttu-id="68a07-117">Per configurare il client per Servizi Desktop remoto per la modalità di operazione disconnessa</span><span class="sxs-lookup"><span data-stu-id="68a07-117">To configure the Client for Remote Desktop Services for disconnected operation mode</span></span>**

1.  <span data-ttu-id="68a07-118">Impostare il valore della chiave del registro di sistema seguente su 1 per abilitare la modalità di operazione disconnessa:</span><span class="sxs-lookup"><span data-stu-id="68a07-118">Set the following registry key value to 1 to enable disconnected operation mode:</span></span>

    <span data-ttu-id="68a07-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="68a07-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\AllowDisconnectedOperation</span></span>

2.  <span data-ttu-id="68a07-120">Impostare il valore della chiave del registro di sistema seguente su 0 (zero) per consentire l'utilizzo illimitato della modalità di operazione disconnessa:</span><span class="sxs-lookup"><span data-stu-id="68a07-120">Set the following registry key value to 0 (zero) to allow unlimited use of disconnected operation mode:</span></span>

    <span data-ttu-id="68a07-121">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span><span class="sxs-lookup"><span data-stu-id="68a07-121">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\LimitDisconnectedOperation</span></span>

3.  <span data-ttu-id="68a07-122">Assicurarsi che tutti i pacchetti vengano precaricati nella cache per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="68a07-122">Ensure that all packages are preloaded into the cache to improve performance.</span></span>

## <span data-ttu-id="68a07-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68a07-123">Related topics</span></span>


[<span data-ttu-id="68a07-124">Modalità di operazioni senza connessione</span><span class="sxs-lookup"><span data-stu-id="68a07-124">Disconnected Operation Mode</span></span>](disconnected-operation-mode.md)

[<span data-ttu-id="68a07-125">Come configurare le impostazioni dei file di registro dei client App-V usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="68a07-125">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





