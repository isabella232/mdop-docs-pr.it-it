---
title: Note sulla versione di MED-V 1.0
description: Note sulla versione di MED-V 1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826595"
---
# <span data-ttu-id="5cf1b-103">Note sulla versione di MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="5cf1b-103">MED-V 1.0 Release Notes</span></span>


## <span data-ttu-id="5cf1b-104">Problemi noti di MED-V</span><span class="sxs-lookup"><span data-stu-id="5cf1b-104">Known Issues with MED-V</span></span>


<span data-ttu-id="5cf1b-105">Questa sezione fornisce le informazioni più aggiornate sui problemi generali della piattaforma Microsoft Enterprise Desktop Virtualization (MED-V).</span><span class="sxs-lookup"><span data-stu-id="5cf1b-105">This section provides the most up-to-date information about general issues with the Microsoft Enterprise Desktop Virtualization (MED-V) platform.</span></span> <span data-ttu-id="5cf1b-106">Questi problemi non vengono visualizzati nella documentazione del prodotto e in alcuni casi potrebbe essere contraddetta la documentazione del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-106">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="5cf1b-107">Quando possibile, questi problemi verranno risolti in versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-107">Whenever possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="5cf1b-108">I download di file non seguono le regole di reindirizzamento Web</span><span class="sxs-lookup"><span data-stu-id="5cf1b-108">File downloads do not follow Web redirection rules</span></span>

<span data-ttu-id="5cf1b-109">I download di file non seguono le regole di reindirizzamento Web impostate in un criterio di area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-109">File downloads do not follow Web redirection rules set in a MED-V workspace policy.</span></span>

### <span data-ttu-id="5cf1b-110">Quando si espande una finestra dell'applicazione console-pubblicata a schermo intero, scompare</span><span class="sxs-lookup"><span data-stu-id="5cf1b-110">When expanding a console-published application window to full screen, it disappears</span></span>

<span data-ttu-id="5cf1b-111">Se si espande un'applicazione pubblicata da console (ad esempio cmd.exe) a schermo intero all'interno di un'area di lavoro MED-V configurata in modalità di integrazione perfetta, la finestra dell'applicazione potrebbe scomparire o non rispondere.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-111">If you expand a console-published application (such as cmd.exe) window to full screen inside a MED-V workspace configured in seamless integration mode, the application window might disappear or not respond.</span></span>

### <span data-ttu-id="5cf1b-112">Quando si lavora in modalità desktop completo, le posizioni delle icone sul desktop non vengono salvate</span><span class="sxs-lookup"><span data-stu-id="5cf1b-112">When working in full desktop mode, icon locations on the desktop are not saved</span></span>

<span data-ttu-id="5cf1b-113">Quando si lavora in modalità desktop completo, le modifiche della posizione manuale delle icone sul desktop non vengono salvate tra le sessioni dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-113">When working in full desktop mode, manual location changes of icons on the desktop are not saved between MED-V workspace sessions.</span></span>

### <span data-ttu-id="5cf1b-114">Un'immagine locale e un'immagine di test con lo stesso nome non possono esistere nello stesso dominio</span><span class="sxs-lookup"><span data-stu-id="5cf1b-114">A local image and a test image with the same name cannot exist in the same domain</span></span>

<span data-ttu-id="5cf1b-115">Se un'immagine locale viene unita al dominio e l'amministratore crea una nuova versione della stessa immagine con lo stesso nome del computer di un'immagine di test, quando l'immagine di test si unisce al dominio, l'azione di join Domain non riesce o riesce e l'immagine locale viene rimossa dal dominio.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-115">If a local image is joined to the domain and the administrator creates a new version of the same image with the same computer name as a test image, when the test image joins the domain, either the join domain action fails or it succeeds and the local image is removed from the domain.</span></span>

### <span data-ttu-id="5cf1b-116">MED-V non supporta le funzionalità di Windows Aero</span><span class="sxs-lookup"><span data-stu-id="5cf1b-116">MED-V does not support Windows Aero features</span></span>

<span data-ttu-id="5cf1b-117">MED-V non supporta le funzionalità Windows Aero, ad esempio Aero Flip 3D.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-117">MED-V does not support Windows Aero features (such as Aero Flip 3D).</span></span>

### <span data-ttu-id="5cf1b-118">La console di gestione può essere usata da un solo utente Windows per computer</span><span class="sxs-lookup"><span data-stu-id="5cf1b-118">The management console can be used by only one Windows user per computer</span></span>

<span data-ttu-id="5cf1b-119">La console di gestione MED-V può essere usata solo dagli amministratori e dall'utente Windows che ha installato l'applicazione di gestione.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-119">The MED-V management console can be used only by administrators and the Windows user who installed the management application.</span></span>

### <span data-ttu-id="5cf1b-120">L'utilità di configurazione del server MED-V Verifica la connettività di Microsoft SQL Server in contesto utente anziché in contesto del servizio MED-V Server</span><span class="sxs-lookup"><span data-stu-id="5cf1b-120">The MED-V Server configuration utility tests Microsoft SQL Server connectivity under user context rather than under MED-V Server service context</span></span>

<span data-ttu-id="5cf1b-121">MED-V usa il contesto del servizio MED-V Server per raccogliere report dal database di report di Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-121">MED-V uses MED-V Server service context to collect reports from the Microsoft SQL Server reports database.</span></span> <span data-ttu-id="5cf1b-122">L'utilità di configurazione del server MED-V Verifica il database e verifica la stringa di connessione del database.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-122">The MED-V Server configuration utility verifies the database and tests the database connection string.</span></span> <span data-ttu-id="5cf1b-123">Non convalidare l'accesso del servizio MED-V Server al database.</span><span class="sxs-lookup"><span data-stu-id="5cf1b-123">It does not validate the access of MED-V Server service to the database.</span></span>

 

 





