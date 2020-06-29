---
title: Panoramica dello scenario di recapito autonomo
description: Panoramica dello scenario di recapito autonomo
author: dansimp
ms.assetid: b109f309-f3c1-43af-996f-2a9b138dd171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9f29b1c8d1c9ae97f7a21498369647f31f552839
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815306"
---
# <span data-ttu-id="14e95-103">Panoramica dello scenario di recapito autonomo</span><span class="sxs-lookup"><span data-stu-id="14e95-103">Stand-Alone Delivery Scenario Overview</span></span>


<span data-ttu-id="14e95-104">Lo scenario di recapito autonomo è una soluzione ideale per la virtualizzazione dell'applicazione per ambienti in cui una connettività a larghezza di banda ridotta o nessuna connettività limita la capacità del client Desktop Application Virtualization di eseguire lo streaming delle applicazioni da server centralizzati.</span><span class="sxs-lookup"><span data-stu-id="14e95-104">The stand-alone delivery scenario is an ideal application virtualization solution for environments where either low bandwidth connectivity or no connectivity limits the ability of the Application Virtualization Desktop Client to stream applications from centralized servers.</span></span> <span data-ttu-id="14e95-105">In questi ambienti gli utenti lavorano spesso in remoto e i proprietari di dispositivi installano le applicazioni usando i file di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="14e95-105">In these environments, users often work remotely and device owners install applications by using Windows Installer files.</span></span>

<span data-ttu-id="14e95-106">Puoi usare Application Virtualization Sequencer per creare applicazioni sequenziate che includono file di Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="14e95-106">You can use the Application Virtualization Sequencer to create sequenced applications that include Windows Installer files.</span></span> <span data-ttu-id="14e95-107">Questi pacchetti includono le applicazioni virtualizzate, le informazioni sulla pubblicazione e le routine di installazione necessarie per l'installazione dei pacchetti nei sistemi client.</span><span class="sxs-lookup"><span data-stu-id="14e95-107">These packages include the virtualized applications, publication information, and the necessary installer routines for installing the packages on the client systems.</span></span> <span data-ttu-id="14e95-108">Il programma di installazione aggiunge il pacchetto dell'applicazione virtuale al client desktop Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="14e95-108">The installer adds the virtual application package to the Microsoft Application Virtualization Desktop Client.</span></span> <span data-ttu-id="14e95-109">Le informazioni sulla pubblicazione sono configurate per caricare le applicazioni da una posizione locale invece che tramite una WAN.</span><span class="sxs-lookup"><span data-stu-id="14e95-109">The publication information is configured to load applications from a local location rather than stream them across a WAN.</span></span> <span data-ttu-id="14e95-110">Gli utenti possono connettersi temporaneamente a una rete per recuperare i file di Windows Installer o eseguirli da un DVD.</span><span class="sxs-lookup"><span data-stu-id="14e95-110">Users can temporarily connect to a network to retrieve the Windows Installer files or can run them from a DVD.</span></span>

<span data-ttu-id="14e95-111">Lo scenario di recapito autonomo offre agli utenti i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="14e95-111">The stand-alone delivery scenario provides users the following benefits:</span></span>

-   <span data-ttu-id="14e95-112">Operazione di distribuzione semplice.</span><span class="sxs-lookup"><span data-stu-id="14e95-112">Simple deployment operation.</span></span>

-   <span data-ttu-id="14e95-113">La rete e i server non sono necessari in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="14e95-113">Network and servers not needed at runtime.</span></span>

-   <span data-ttu-id="14e95-114">Applicazioni pre-memorizzate nella cache e disponibili per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="14e95-114">Applications pre-cached and available to all users.</span></span>

<span data-ttu-id="14e95-115">Lo scenario di recapito autonomo presenta le limitazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="14e95-115">The stand-alone delivery scenario has the following limitations:</span></span>

-   <span data-ttu-id="14e95-116">Il reporting automatizzato incorporato non è disponibile. i report devono essere generati con strumenti per la creazione di report esterni.</span><span class="sxs-lookup"><span data-stu-id="14e95-116">Built-in, automated reporting is unavailable; reports must be generated with external reporting tools.</span></span>

-   <span data-ttu-id="14e95-117">Le applicazioni devono essere recapitate manualmente al client, ad esempio i file di Windows Installer originali.</span><span class="sxs-lookup"><span data-stu-id="14e95-117">Applications must be delivered to the client manually like the original Windows Installer files.</span></span>

## <span data-ttu-id="14e95-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="14e95-118">Related topics</span></span>


[<span data-ttu-id="14e95-119">Come installare manualmente Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="14e95-119">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="14e95-120">Come pubblicare un'applicazione virtuale nel client</span><span class="sxs-lookup"><span data-stu-id="14e95-120">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

 

 





