---
title: Architettura di alto livello
description: Architettura di alto livello
author: dansimp
ms.assetid: a78e12ad-5aa6-40e0-ae8b-51acaf005712
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00df29c751653645ab4bee9762af57576a40092a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826205"
---
# <span data-ttu-id="4a37e-103">Architettura di alto livello</span><span class="sxs-lookup"><span data-stu-id="4a37e-103">High-Level Architecture</span></span>


<span data-ttu-id="4a37e-104">La soluzione MED-V include gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="4a37e-104">The MED-V solution comprises the following elements:</span></span>

-   <span data-ttu-id="4a37e-105">**Macchina virtuale definita dall'amministratore**: incapsula un ambiente desktop completo, tra cui un sistema operativo, le applicazioni e gli strumenti di gestione e sicurezza facoltativi.</span><span class="sxs-lookup"><span data-stu-id="4a37e-105">**Administrator-defined virtual machine**—Encapsulates a full desktop environment, including an operating system, applications, and optional management and security tools.</span></span>

-   <span data-ttu-id="4a37e-106">**Archivio immagini**: archivia tutte le immagini virtuali in un server IIS standard e consente la gestione delle versioni delle immagini virtuali, il recupero delle immagini autenticate dal client e il download efficiente (di una nuova immagine o aggiornamenti) tramite la tecnologia di trasferimento dei ritagli.</span><span class="sxs-lookup"><span data-stu-id="4a37e-106">**Image repository**—Stores all virtual images on a standard IIS server and enables virtual images version management, client-authenticated image retrieval, and efficient download (of a new image or updates) via Trim Transfer technology.</span></span>

-   <span data-ttu-id="4a37e-107">**Server di gestione**: associa le immagini virtuali del repository di immagini insieme ai criteri di utilizzo dell'amministratore a Active Directory® utenti o gruppi.</span><span class="sxs-lookup"><span data-stu-id="4a37e-107">**Management server**—Associates virtual images from the image repository along with administrator usage policies to Active Directory® users or groups.</span></span> <span data-ttu-id="4a37e-108">Il server di gestione aggrega inoltre gli eventi dei client e li archivia in un database esterno (Microsoft SQL Server®) per scopi di monitoraggio e creazione di report.</span><span class="sxs-lookup"><span data-stu-id="4a37e-108">The management server also aggregates clients' events and stores them in an external database (Microsoft SQL Server®) for monitoring and reporting purposes.</span></span>

-   <span data-ttu-id="4a37e-109">**Console di gestione**: consente agli amministratori di controllare il server di gestione e il repository di immagini.</span><span class="sxs-lookup"><span data-stu-id="4a37e-109">**Management console**—Enables administrators to control the management server and the image repository.</span></span>

-   **<span data-ttu-id="4a37e-110">Client per utenti finali</span><span class="sxs-lookup"><span data-stu-id="4a37e-110">End-user client</span></span>**

    1.  <span data-ttu-id="4a37e-111">Ciclo di vita dell'immagine virtuale: autenticazione, recupero delle immagini, applicazione dei criteri di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="4a37e-111">Virtual image life-cycle—Authentication, image retrieval, enforcement of usage policies.</span></span>

    2.  <span data-ttu-id="4a37e-112">Gestione sessioni della macchina virtuale: avviare, arrestare, bloccare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4a37e-112">Virtual machine session management—Start, stop, lock the virtual machine.</span></span>

    3.  <span data-ttu-id="4a37e-113">Esperienza desktop singola: le applicazioni installate nella macchina virtuale sono facilmente disponibili tramite il menu Start desktop standard e integrate con altre applicazioni sul desktop dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4a37e-113">Single desktop experience—Applications installed in the virtual machine seamlessly available through the standard desktop Start menu and integrated with other applications on the user desktop.</span></span>

<span data-ttu-id="4a37e-114">Tutte le comunicazioni tra il client e i server (server di gestione e archivio immagini) vengono effettuate sopra un canale HTTP o HTTPS standard.</span><span class="sxs-lookup"><span data-stu-id="4a37e-114">All communication between the client and the servers (management server and image repository) is carried on top of a standard HTTP or HTTPS channel.</span></span>

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 





