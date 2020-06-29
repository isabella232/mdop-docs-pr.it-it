---
title: Miglioramento della sicurezza durante la sequenza di App-V
description: Miglioramento della sicurezza durante la sequenza di App-V
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816356"
---
# <span data-ttu-id="48578-103">Miglioramento della sicurezza durante la sequenza di App-V</span><span class="sxs-lookup"><span data-stu-id="48578-103">Improving Security During App-V Sequencing</span></span>


<span data-ttu-id="48578-104">Le applicazioni di creazione di pacchetti per la sequenziazione sono l'attività in corso più grande in un'infrastruttura di App-V.</span><span class="sxs-lookup"><span data-stu-id="48578-104">Packaging applications for sequencing is the largest ongoing task in an App-V infrastructure.</span></span> <span data-ttu-id="48578-105">Poiché questa attività è in corso, è consigliabile valutare attentamente la creazione di criteri e procedure da seguire durante la sequenziazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="48578-105">Because this task is ongoing, you should carefully consider creating policies and procedures to follow when sequencing applications.</span></span> <span data-ttu-id="48578-106">In App-V 4.5, durante la sequenziazione, è possibile acquisire gli elenchi di controllo di accesso (ACL) negli asset di file dell'applicazione virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="48578-106">In App-V4.5, during sequencing, you can capture Access Control Lists (ACLs) on the file assets of the virtualized application.</span></span>

## <span data-ttu-id="48578-107">Ricerca di virus nel sequencer</span><span class="sxs-lookup"><span data-stu-id="48578-107">Virus Scanning on the Sequencer</span></span>


<span data-ttu-id="48578-108">È consigliabile installare il software di analisi nel computer di sequenziazione e quindi analizzare il computer per ottenere virus e malware.</span><span class="sxs-lookup"><span data-stu-id="48578-108">It is a best practice to install the scanning software on the sequencing computer and then scan the computer for viruses and malware.</span></span> <span data-ttu-id="48578-109">Quando il computer di sequenziazione viene digitalizzato e privo di virus o malware, disattivare il software di analisi, inclusi tutti i software di rilevamento antivirus e malware, nel computer di sequenziazione prima di sequenziare qualsiasi applicazione.</span><span class="sxs-lookup"><span data-stu-id="48578-109">After the sequencing computer is scanned and free of any viruses or malware, disable the scanning software, including all antivirus and malware detection software, on the sequencing computer before sequencing any applications.</span></span> <span data-ttu-id="48578-110">Questo accelera il processo di sequenziazione e impedisce che i componenti software di analisi vengano rilevati durante la sequenziazione e inclusi nel pacchetto di applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="48578-110">This speeds the sequencing process and prevents the scanning software components from being detected during sequencing and included in the virtual application package.</span></span>

## <span data-ttu-id="48578-111">Acquisizione di ACL nei file (NTFS)</span><span class="sxs-lookup"><span data-stu-id="48578-111">Capturing ACLs on Files (NTFS)</span></span>


<span data-ttu-id="48578-112">Il sequencer acquisisce le autorizzazioni NTFS (ACL) per i file monitorati durante la fase di installazione sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="48578-112">The Sequencer captures NTFS permissions (the ACLs) for the files that are monitored during the sequencing installation phase.</span></span> <span data-ttu-id="48578-113">Prima del rilascio di App-V 4.5, gli ACL non sono stati acquisiti come parte del processo di sequenziazione. Questa nuova funzionalità consente l'esecuzione di alcune applicazioni per gli utenti con un basso livello di autorizzazione che in genere richiedono privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="48578-113">(Before the release of App-V4.5, ACLs were not captured as part of the sequencing process.) This new feature enables certain applications to run for users with a low level of permission that would normally require Administrative privileges.</span></span>

<span data-ttu-id="48578-114">Questa funzionalità consente inoltre all'ingegnere sequenziazione di acquisire le impostazioni di sicurezza identificate dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="48578-114">This feature also enables the sequencing engineer to capture the security settings identified by the vendor.</span></span> <span data-ttu-id="48578-115">Se non si applicano le impostazioni consigliate dal fornitore, l'applicazione può essere aperta a un attacco o un uso improprio da parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="48578-115">Failing to apply the settings recommended by the vendor could leave the application open to attack or misuse by users.</span></span> <span data-ttu-id="48578-116">Per informazioni sul fatto che sia necessario distribuire o meno un'applicazione con ACL aperti, vedere il gruppo di supporto dell'applicazione o il fornitore del software.</span><span class="sxs-lookup"><span data-stu-id="48578-116">For information about whether or not you should deploy an application with open ACLs, refer to your application support group or the software vendor.</span></span>

<span data-ttu-id="48578-117">**Importante**  Anche se il sequencer acquisisce gli ACL NTFS durante il monitoraggio della fase di installazione della sequenziazione, non acquisisce gli ACL per il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="48578-117">**Important** Although the sequencer captures the NTFS ACLs while monitoring the installation phase of sequencing, it does not capture the ACLs for the registry.</span></span> <span data-ttu-id="48578-118">Gli utenti hanno accesso completo a tutte le chiavi del registro di sistema per le applicazioni virtuali eccetto i servizi.</span><span class="sxs-lookup"><span data-stu-id="48578-118">Users have full access to all registry keys for virtual applications except for services.</span></span> <span data-ttu-id="48578-119">Tuttavia, se un utente modifica il registro di sistema di un'applicazione virtuale, tale modifica viene archiviata in una posizione specifica ( `uservol_sftfs_v1.pkg` ) e non influisce su altri utenti.</span><span class="sxs-lookup"><span data-stu-id="48578-119">However, if a user modifies the registry of a virtual application, that change is stored in a specific location (`uservol_sftfs_v1.pkg`) and won’t affect other users.</span></span>

 

<span data-ttu-id="48578-120">Durante la fase di installazione, un ingegnere della sequenziazione può modificare le autorizzazioni predefinite dei file, se necessario.</span><span class="sxs-lookup"><span data-stu-id="48578-120">During the installation phase, a sequencing engineer can modify the default permissions of the files if necessary.</span></span> <span data-ttu-id="48578-121">Dopo aver completato il processo di sequenziazione, ma prima di salvare il pacchetto, l'ingegnere della sequenziazione può quindi scegliere di applicare i descrittori di sicurezza acquisiti durante la fase di installazione.</span><span class="sxs-lookup"><span data-stu-id="48578-121">After the sequencing process is complete, but before saving the package, the sequencing engineer can then choose to enforce security descriptors that were captured during the installation phase.</span></span> <span data-ttu-id="48578-122">Si tratta di una procedura consigliata per applicare i descrittori di sicurezza se nessun'altra soluzione consente l'esecuzione corretta dell'applicazione una volta virtualizzata.</span><span class="sxs-lookup"><span data-stu-id="48578-122">It is a best practice to enforce security descriptors if no other solution allows the application to run properly once virtualized.</span></span>

 

 





