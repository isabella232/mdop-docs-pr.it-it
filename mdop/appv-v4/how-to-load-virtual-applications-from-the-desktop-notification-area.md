---
title: Come caricare le applicazioni virtuali dall'area di notifica del desktop
description: Come caricare le applicazioni virtuali dall'area di notifica del desktop
author: dansimp
ms.assetid: f52758eb-8b81-4b3c-9bc3-adcf7c00c238
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d7004f9e0031dfeeedc8b6a916e2f3488f1d31e1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817216"
---
# <span data-ttu-id="3cf72-103">Come caricare le applicazioni virtuali dall'area di notifica del desktop</span><span class="sxs-lookup"><span data-stu-id="3cf72-103">How to Load Virtual Applications from the Desktop Notification Area</span></span>


<span data-ttu-id="3cf72-104">Se si è un utente per dispositivi mobili, è consigliabile caricare completamente le applicazioni nella cache per usarle durante l'operazione disconnessa o la modalità offline.</span><span class="sxs-lookup"><span data-stu-id="3cf72-104">If you are a mobile user, you might want to fully load your applications in the cache to use them during disconnected operation or offline mode.</span></span> <span data-ttu-id="3cf72-105">Per eseguire il flusso delle applicazioni dal server Application Virtualization (App-V) o dall'Application Virtualization (App-V) streaming server, è necessario essere connessi a un server per caricare le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3cf72-105">To stream applications from the Application Virtualization (App-V) Server or the Application Virtualization (App-V) Streaming Server, you must be connected to a server to load applications.</span></span> <span data-ttu-id="3cf72-106">Se non si è connessi al server quando si tenta di caricare le applicazioni, il sistema genererà un messaggio di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="3cf72-106">If you are not connected to the server when you attempt to load applications, your system will generate an appropriate error message.</span></span> <span data-ttu-id="3cf72-107">È anche possibile eseguire il flusso di applicazioni nel client da un file o un disco.</span><span class="sxs-lookup"><span data-stu-id="3cf72-107">You can also stream applications to the client from a file or disk.</span></span>

<span data-ttu-id="3cf72-108">Le applicazioni vengono caricate un'applicazione alla volta.</span><span class="sxs-lookup"><span data-stu-id="3cf72-108">The applications are loaded one application at a time.</span></span> <span data-ttu-id="3cf72-109">La barra di stato Mostra il nome dell'applicazione, la percentuale di applicazione caricata e il numero di applicazioni già elaborate rispetto al numero totale delle applicazioni accodate.</span><span class="sxs-lookup"><span data-stu-id="3cf72-109">The progress bar shows you the application name, the percentage of application loaded, and the number of applications already processed compared to the total number of the applications queued.</span></span> <span data-ttu-id="3cf72-110">È possibile ignorare qualsiasi applicazione in corso prima che venga caricata 100%.</span><span class="sxs-lookup"><span data-stu-id="3cf72-110">You can skip any application in progress before it is 100% loaded.</span></span> <span data-ttu-id="3cf72-111">È anche possibile ignorare il caricamento di tutte le applicazioni rimanenti.</span><span class="sxs-lookup"><span data-stu-id="3cf72-111">You can skip the loading of all remaining applications as well.</span></span>

<span data-ttu-id="3cf72-112">**Nota**  Se il sistema rileva un errore durante il caricamento di un'applicazione, segnala l'errore.</span><span class="sxs-lookup"><span data-stu-id="3cf72-112">**Note** If your system encounters an error while loading an application, it reports the error to you.</span></span> <span data-ttu-id="3cf72-113">È necessario chiudere la finestra di dialogo di errore prima che venga caricata l'applicazione successiva.</span><span class="sxs-lookup"><span data-stu-id="3cf72-113">You must dismiss the error dialog before it will load the next application.</span></span>

 

**<span data-ttu-id="3cf72-114">Per caricare tutte le applicazioni</span><span class="sxs-lookup"><span data-stu-id="3cf72-114">To load all applications</span></span>**

1.  <span data-ttu-id="3cf72-115">Fare clic con il pulsante destro del mouse sull'icona Application Virtualization System nell'area di notifica.</span><span class="sxs-lookup"><span data-stu-id="3cf72-115">Right-click the Application Virtualization System icon in the notification area.</span></span>

2.  <span data-ttu-id="3cf72-116">Selezionare **Carica applicazioni** dal menu a comparsa.</span><span class="sxs-lookup"><span data-stu-id="3cf72-116">Select **Load Applications** from the pop-up menu.</span></span>

**<span data-ttu-id="3cf72-117">Per ignorare le applicazioni</span><span class="sxs-lookup"><span data-stu-id="3cf72-117">To skip applications</span></span>**

1.  <span data-ttu-id="3cf72-118">Fare clic sulla barra di stato per visualizzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="3cf72-118">Click the progress bar to display the dialog box.</span></span>

2.  <span data-ttu-id="3cf72-119">Selezionare uno dei pulsanti seguenti per ottenere i risultati desiderati:</span><span class="sxs-lookup"><span data-stu-id="3cf72-119">Select one of the following buttons to achieve the desired results:</span></span>

    1.  <span data-ttu-id="3cf72-120">**Skip**-per ignorare l'applicazione attualmente caricata.</span><span class="sxs-lookup"><span data-stu-id="3cf72-120">**Skip**—To skip the currently loading application.</span></span>

    2.  <span data-ttu-id="3cf72-121">**Ignora tutto**: per ignorare tutte le applicazioni rimanenti.</span><span class="sxs-lookup"><span data-stu-id="3cf72-121">**Skip All**—To skip all remaining applications.</span></span>

    3.  <span data-ttu-id="3cf72-122">**Continua**: per annullare la finestra di dialogo e continuare a caricare le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3cf72-122">**Continue**—To cancel the dialog box and continue loading applications.</span></span>

## <span data-ttu-id="3cf72-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3cf72-123">Related topics</span></span>


[<span data-ttu-id="3cf72-124">Come usare l'area di notifica del desktop per Application Virtualization Client Management</span><span class="sxs-lookup"><span data-stu-id="3cf72-124">How to Use the Desktop Notification Area for Application Virtualization Client Management</span></span>](how-to-use-the-desktop-notification-area-for-application-virtualization-client-management.md)

 

 





