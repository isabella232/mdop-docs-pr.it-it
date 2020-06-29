---
title: Come configurare il server di distribuzione Web di immagini
description: Come configurare il server di distribuzione Web di immagini
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825156"
---
# <span data-ttu-id="e3476-103">Come configurare il server di distribuzione Web di immagini</span><span class="sxs-lookup"><span data-stu-id="e3476-103">How to Configure the Image Web Distribution Server</span></span>


<span data-ttu-id="e3476-104">Un repository di immagini è un server facoltativo usato per la distribuzione delle immagini (dove gli amministratori caricano le nuove immagini e i computer client controllano il server ogni 15 minuti e ne aggiornano l'immagine se ne è disponibile uno nuovo).</span><span class="sxs-lookup"><span data-stu-id="e3476-104">An image repository is an optional server that is used for image distribution (where administrators upload new images and client computers check the server every 15 minutes and update their image if a new one is available).</span></span>

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


<span data-ttu-id="e3476-105">Un server di distribuzione delle immagini richiede le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3476-105">An image distribution server requires the following:</span></span>

-   <span data-ttu-id="e3476-106">Internet Information Services (IIS): per informazioni, vedere [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).</span><span class="sxs-lookup"><span data-stu-id="e3476-106">Internet Information Services (IIS)—For information, see [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).</span></span>

    <span data-ttu-id="e3476-107">Durante l'aggiunta di servizi ruolo durante l'installazione di IIS, selezionare i metodi di autenticazione supportati seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3476-107">During the IIS installation, when adding role services, select the following supported authentication methods:</span></span>

    -   **<span data-ttu-id="e3476-108">Autenticazione di base</span><span class="sxs-lookup"><span data-stu-id="e3476-108">Basic Authentication</span></span>**

    -   **<span data-ttu-id="e3476-109">Autenticazione di Windows</span><span class="sxs-lookup"><span data-stu-id="e3476-109">Windows Authentication</span></span>**

    -   **<span data-ttu-id="e3476-110">Autenticazione del mapping dei certificati client</span><span class="sxs-lookup"><span data-stu-id="e3476-110">Client Certificate Mapping Authentication</span></span>**

    <span data-ttu-id="e3476-111">Per la configurazione di IIS, includere i seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="e3476-111">When configuring IIS, include the following:</span></span>

    -   <span data-ttu-id="e3476-112">Aggiungere una directory virtuale con l'alias denominato **MEDVImages**.</span><span class="sxs-lookup"><span data-stu-id="e3476-112">Add a virtual directory, with the alias named **MEDVImages**.</span></span> <span data-ttu-id="e3476-113">Il percorso fisico deve puntare alla posizione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="e3476-113">The physical path should point to the location of the images.</span></span>

    -   <span data-ttu-id="e3476-114">Abilitare BITS.</span><span class="sxs-lookup"><span data-stu-id="e3476-114">Enable BITS.</span></span>

    -   <span data-ttu-id="e3476-115">Aggiungere i tipi MIME seguenti:</span><span class="sxs-lookup"><span data-stu-id="e3476-115">Add the following MIME types:</span></span>

        -   **<span data-ttu-id="e3476-116">. CKM (applicazione/ottetto-Stream)</span><span class="sxs-lookup"><span data-stu-id="e3476-116">.ckm (application/octet-stream)</span></span>**

        -   <span data-ttu-id="e3476-117">**. index (applicazione/ottetto-Stream**)</span><span class="sxs-lookup"><span data-stu-id="e3476-117">**.index (application/octet-stream**)</span></span>

    -   <span data-ttu-id="e3476-118">Nel sito MED-V aggiungere le autorizzazioni di lettura per **tutti gli utenti**.</span><span class="sxs-lookup"><span data-stu-id="e3476-118">On the MED-V site, add read permissions to **Everyone**.</span></span>

    -   <span data-ttu-id="e3476-119">Riavviare IIS.</span><span class="sxs-lookup"><span data-stu-id="e3476-119">Restart IIS.</span></span>

-   <span data-ttu-id="e3476-120">Estensioni del server BITS per IIS: per informazioni, vedere [installare le estensioni del server BITS](https://go.microsoft.com/fwlink/?LinkId=142996).</span><span class="sxs-lookup"><span data-stu-id="e3476-120">BITS Server Extensions for IIS—For information, see [Install BITS Server Extensions](https://go.microsoft.com/fwlink/?LinkId=142996).</span></span>

## <span data-ttu-id="e3476-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3476-121">Related topics</span></span>


[<span data-ttu-id="e3476-122">Configurazioni supportate</span><span class="sxs-lookup"><span data-stu-id="e3476-122">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="e3476-123">Progettare i repository delle immagini MED-V</span><span class="sxs-lookup"><span data-stu-id="e3476-123">Design the MED-V Image Repositories</span></span>](design-the-med-v-image-repositories.md)

 

 





