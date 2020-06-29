---
title: Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 10
description: Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 10
author: dansimp
ms.assetid: 9a3e5413-2621-49ce-8bd2-992616691703
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bbaa8c4160970de90561f5ff8cedcefd08ca1dd7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822986"
---
# <span data-ttu-id="60a94-103">Pianificazione di come salvare e distribuire l'immagine di ripristino di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="60a94-103">Planning How to Save and Deploy the DaRT 10 Recovery Image</span></span>


<span data-ttu-id="60a94-104">È possibile salvare e distribuire l'immagine di ripristino di Microsoft Diagnostics and Recovery Toolset (DaRT) 10 usando i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="60a94-104">You can save and deploy the Microsoft Diagnostics and Recovery Toolset (DaRT) 10 recovery image by using the following methods.</span></span> <span data-ttu-id="60a94-105">Quando si determina il metodo che si vuole usare, valutare i vantaggi e gli svantaggi di ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="60a94-105">When you are determining the method that you will use, consider the advantages and disadvantages of each.</span></span> <span data-ttu-id="60a94-106">Dovresti anche prendere in considerazione l'infrastruttura e il personale di supporto.</span><span class="sxs-lookup"><span data-stu-id="60a94-106">You should also consider your infrastructure and support staff.</span></span> <span data-ttu-id="60a94-107">Se si dispone di una piccola infrastruttura, è consigliabile distribuire il dardo 10 usando elementi multimediali rimovibili, poiché l'immagine di ripristino sarà sempre disponibile se viene installata nel disco rigido locale.</span><span class="sxs-lookup"><span data-stu-id="60a94-107">If you have a small infrastructure, you might want to deploy DaRT 10 by using removable media, since the recovery image will always be available if you install it to the local hard drive.</span></span>

<span data-ttu-id="60a94-108">Se l'organizzazione usa servizi di dominio Active Directory, è consigliabile distribuire le immagini di ripristino come servizio di rete tramite Windows DS.</span><span class="sxs-lookup"><span data-stu-id="60a94-108">If your organization uses Active Directory Domain Services (AD DS), you may want to deploy recovery images as a network service by using Windows DS.</span></span> <span data-ttu-id="60a94-109">Le immagini di ripristino sono sempre disponibili per qualsiasi computer connesso.</span><span class="sxs-lookup"><span data-stu-id="60a94-109">Recovery images are always available to any connected computer.</span></span> <span data-ttu-id="60a94-110">È possibile distribuire più immagini da Windows DS e mantenerle tutte in un'unica posizione.</span><span class="sxs-lookup"><span data-stu-id="60a94-110">You can deploy multiple images from Windows DS and maintain them all in one place.</span></span>

<span data-ttu-id="60a94-111">**Nota**  È consigliabile usare più di un metodo nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="60a94-111">**Note** You may want to use more than one method in your organization.</span></span> <span data-ttu-id="60a94-112">Ad esempio, è possibile avviare il dardo da una partizione remota per la maggior parte delle situazioni e avere un'unità flash USB disponibile nel caso in cui il computer dell'utente finale non possa connettersi alla rete.</span><span class="sxs-lookup"><span data-stu-id="60a94-112">For example, you can boot into DaRT from a remote partition for most situations and have a USB flash drive available in case the end-user computer cannot connect to the network.</span></span>

 

<span data-ttu-id="60a94-113">La tabella seguente mostra alcuni vantaggi e svantaggi di ogni metodo per l'uso di DaRT nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="60a94-113">The following table shows some advantages and disadvantages of each method of using DaRT in your organization.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="60a94-114">Metodo per l'avvio in dardo</span><span class="sxs-lookup"><span data-stu-id="60a94-114">Method to Boot into DaRT</span></span></th>
<th align="left"><span data-ttu-id="60a94-115">Vantaggi</span><span class="sxs-lookup"><span data-stu-id="60a94-115">Advantages</span></span></th>
<th align="left"><span data-ttu-id="60a94-116">Svantaggi</span><span class="sxs-lookup"><span data-stu-id="60a94-116">Disadvantages</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="60a94-117">Supporto rimovibile</span><span class="sxs-lookup"><span data-stu-id="60a94-117">Removable Media</span></span></strong></p>
<p><span data-ttu-id="60a94-118">L'immagine di ripristino viene scritta in un CD, un DVD o un'unità USB per consentire al personale di supporto di portare gli strumenti di ripristino al computer instabile.</span><span class="sxs-lookup"><span data-stu-id="60a94-118">The recovery image is written to a CD, DVD, or USB drive to enable support staff to take the recovery tools with them to the unstable computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="60a94-119">Supporta scenari in cui il record di avvio Master (MBR) è danneggiato e non è possibile accedere al disco rigido e supporta i casi in cui non è disponibile una connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="60a94-119">Supports scenarios in which the master boot record (MBR) is corrupted and you cannot access the hard disk and supports cases in which there is no network connection.</span></span></p>
<p><span data-ttu-id="60a94-120">Consente di creare più immagini di ripristino con strumenti diversi per ottenere livelli di supporto diversi.</span><span class="sxs-lookup"><span data-stu-id="60a94-120">Enables you to create multiple recovery images with different tools to provide different levels of support.</span></span></p>
<p><span data-ttu-id="60a94-121">Fornisce uno strumento predefinito per la masterizzazione di immagini di ripristino su supporti rimovibili.</span><span class="sxs-lookup"><span data-stu-id="60a94-121">Provides a built-in tool for burning recovery images to removable media.</span></span></p></td>
<td align="left"><p><span data-ttu-id="60a94-122">Richiede che il personale di supporto sia fisicamente al computer dell'utente finale per l'avvio in DaRT.</span><span class="sxs-lookup"><span data-stu-id="60a94-122">Requires that support staff are physically at the end-user computer to boot into DaRT.</span></span></p>
<p><span data-ttu-id="60a94-123">Richiede tempo e manutenzione per creare più elementi multimediali con configurazioni diverse per i computer a 32 bit e a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="60a94-123">Requires time and maintenance to create multiple media with different configurations for 32-bit and 64-bit computers.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="60a94-124">Da una partizione remota (rete)</span><span class="sxs-lookup"><span data-stu-id="60a94-124">From a remote (network) partition</span></span></strong></p>
<p><span data-ttu-id="60a94-125">L'immagine di ripristino è ospitata in un server di avvio di rete, ad esempio servizi di distribuzione Windows (Windows DS), che consente agli utenti o al personale di supporto di eseguire lo streaming su computer su richiesta.</span><span class="sxs-lookup"><span data-stu-id="60a94-125">The recovery image is hosted on a network boot server like Windows Deployment Services (Windows DS), which allows users or support staff to stream it to computers on demand.</span></span></p></td>
<td align="left"><p><span data-ttu-id="60a94-126">Disponibile per tutti i computer che hanno accesso al server di avvio di rete.</span><span class="sxs-lookup"><span data-stu-id="60a94-126">Available to all computers that have access to the network boot server.</span></span></p>
<p><span data-ttu-id="60a94-127">Le immagini di ripristino sono ospitate in un server centrale, che consente gli aggiornamenti centralizzati.</span><span class="sxs-lookup"><span data-stu-id="60a94-127">Recovery images are hosted on a central server, which enables centralized updates.</span></span></p>
<p><span data-ttu-id="60a94-128">Il personale dell'help desk centralizzato può fornire le riparazioni usando la connettività remota.</span><span class="sxs-lookup"><span data-stu-id="60a94-128">Centralized help desk staff can provide repairs by using remote connectivity.</span></span></p>
<p><span data-ttu-id="60a94-129">Nessun requisito di archiviazione locale per i client.</span><span class="sxs-lookup"><span data-stu-id="60a94-129">No local storage requirement on the clients.</span></span></p>
<p><span data-ttu-id="60a94-130">Possibilità di creare più immagini di ripristino con strumenti diversi per livelli di supporto specifici.</span><span class="sxs-lookup"><span data-stu-id="60a94-130">Ability to create multiple recovery images with different tools for specific support levels.</span></span></p></td>
<td align="left"><p><span data-ttu-id="60a94-131">La necessità di proteggere l'infrastruttura di Windows DS per garantire che gli utenti regolari possano avviare solo l'immagine di ripristino delle freccette e non il processo completo di imaging del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="60a94-131">The need to secure Windows DS infrastructure to ensure that regular users can start only the DaRT recovery image and not the full operating system imaging process.</span></span></p>
<p></p>
<p></p>
<p><span data-ttu-id="60a94-132">Richiede che il computer dell'utente finale sia connesso alla rete in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="60a94-132">Requires that the end-user computer is connected to the network at runtime.</span></span></p>
<p><span data-ttu-id="60a94-133">Richiede che l'immagine di ripristino venga portata in rete.</span><span class="sxs-lookup"><span data-stu-id="60a94-133">Requires that the recovery image is brought across the network.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="60a94-134">Da una partizione di ripristino nel disco rigido locale</span><span class="sxs-lookup"><span data-stu-id="60a94-134">From a recovery partition on the local hard drive</span></span></strong></p>
<p><span data-ttu-id="60a94-135">L'immagine di ripristino viene installata in un disco rigido locale manualmente o tramite sistemi elettronici di distribuzione del software, come System Center Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="60a94-135">The recovery image is installed on a local hard drive either manually or by using electronic software distribution systems like System Center Configuration Manager.</span></span></p></td>
<td align="left"><p><span data-ttu-id="60a94-136">L'immagine di ripristino è sempre disponibile perché è preimpostata nel computer.</span><span class="sxs-lookup"><span data-stu-id="60a94-136">The recovery image is always available because it is pre-staged on the computer.</span></span></p>
<p><span data-ttu-id="60a94-137">Il personale dell'help desk centralizzato può fornire supporto tramite la connessione remota.</span><span class="sxs-lookup"><span data-stu-id="60a94-137">Centralized help desk staff can provide support by using Remote Connection.</span></span></p>
<p><span data-ttu-id="60a94-138">L'immagine di ripristino è gestita centralmente e distribuita.</span><span class="sxs-lookup"><span data-stu-id="60a94-138">The recovery image is centrally managed and deployed.</span></span></p>
<p><span data-ttu-id="60a94-139">Le richieste di chiave di ripristino aggiuntive nei computer protetti da crittografia unità BitLocker di Windows vengono eliminate.</span><span class="sxs-lookup"><span data-stu-id="60a94-139">Additional recovery key requests on computers that are protected by Windows BitLocker drive encryption are eliminated.</span></span></p></td>
<td align="left"><p><span data-ttu-id="60a94-140">Lo spazio di archiviazione locale è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="60a94-140">Local storage is required.</span></span></p>
<p><span data-ttu-id="60a94-141">È consigliabile una partizione non crittografata dedicata per il posizionamento delle immagini di ripristino per ridurre il rischio di una partizione di avvio non riuscita.</span><span class="sxs-lookup"><span data-stu-id="60a94-141">A dedicated, unencrypted partition for recovery image placement is recommended to reduce the risk of a failed boot partition.</span></span></p>
<p><span data-ttu-id="60a94-142">Quando si aggiorna il dardo, è necessario aggiornare tutti i computer dell'organizzazione anziché una sola partizione (sulla rete) o un dispositivo rimovibile.</span><span class="sxs-lookup"><span data-stu-id="60a94-142">When updating DaRT, you must update all computers in your enterprise instead of just one partition (on the network) or removable device.</span></span></p>
<p><span data-ttu-id="60a94-143">Se si distribuisce l'immagine di ripristino dopo l'abilitazione di BitLocker, è necessario un ulteriore considerazione.</span><span class="sxs-lookup"><span data-stu-id="60a94-143">Additional consideration is required if you deploy the recovery image after BitLocker has been enabled.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="60a94-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60a94-144">Related topics</span></span>


[<span data-ttu-id="60a94-145">Pianificazione della distribuzione di DaRT 10</span><span class="sxs-lookup"><span data-stu-id="60a94-145">Planning to Deploy DaRT 10</span></span>](planning-to-deploy-dart-10.md)

 

 





