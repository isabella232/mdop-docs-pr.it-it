---
title: Risoluzione dei problemi di Application Virtualization Sequencer
description: Risoluzione dei problemi di Application Virtualization Sequencer
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815245"
---
# <span data-ttu-id="8ec33-103">Risoluzione dei problemi di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="8ec33-103">Troubleshooting Application Virtualization Sequencer Issues</span></span>


<span data-ttu-id="8ec33-104">Questo argomento include informazioni che è possibile usare per risolvere i problemi generali di Application Virtualization (App-V) Sequencer.</span><span class="sxs-lookup"><span data-stu-id="8ec33-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="8ec33-105">La creazione di un file SFTD tramite App-V Sequencer aumenta il numero di versione in modo imprevisto</span><span class="sxs-lookup"><span data-stu-id="8ec33-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="8ec33-106">Usare la riga di comando per generare un nuovo file SFT.</span><span class="sxs-lookup"><span data-stu-id="8ec33-106">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="8ec33-107">Per creare il file SFT usando la riga di comando, immettere quanto segue al prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="8ec33-107">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="8ec33-108">mkdiffpkg.exe &lt; base SFT nome file &gt; &lt; diff SFT nome file&gt;</span><span class="sxs-lookup"><span data-stu-id="8ec33-108">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="8ec33-109">Il nome file nel file OSD non è corretto dopo l'aggiornamento del pacchetto</span><span class="sxs-lookup"><span data-stu-id="8ec33-109">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="8ec33-110">Quando si apre un pacchetto per l'aggiornamento, è necessario specificare l'unità root Q:\\ come percorso di output per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="8ec33-110">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="8ec33-111">Non specificare un nome file associato con la posizione di output.</span><span class="sxs-lookup"><span data-stu-id="8ec33-111">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="8ec33-112">L'installazione predefinita di Microsoft Word2003 genera un errore quando viene trasmesso a un client</span><span class="sxs-lookup"><span data-stu-id="8ec33-112">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="8ec33-113">Quando si esegue lo streaming di Microsoft Word2003 in un client, viene restituito un errore, ma Microsoft Word continua a essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ec33-113">When you stream Microsoft Word2003 to a client, an error is returned, but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="8ec33-114">Soluzione</span><span class="sxs-lookup"><span data-stu-id="8ec33-114">Solution</span></span>**

<span data-ttu-id="8ec33-115">Risequenziare il pacchetto dell'applicazione virtuale e selezionare **installazione completa**.</span><span class="sxs-lookup"><span data-stu-id="8ec33-115">Resequence the virtual application package and select **Full Install**.</span></span>

## <span data-ttu-id="8ec33-116">L'aggiornamento attivo non funziona quando si crea un pacchetto dipendente</span><span class="sxs-lookup"><span data-stu-id="8ec33-116">Active Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="8ec33-117">Quando si crea un pacchetto dipendente con l'aggiornamento attivo e si aggiungono nuove voci del registro di sistema, il funzionamento viene eseguito correttamente, ma le voci del registro di sistema aggiornate non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="8ec33-117">When you create a dependent package by using active upgrade and add new registry entries, it appears to function correctly, but the updated registry entries are not available.</span></span>

**<span data-ttu-id="8ec33-118">Soluzione</span><span class="sxs-lookup"><span data-stu-id="8ec33-118">Solution</span></span>**

<span data-ttu-id="8ec33-119">Le impostazioni del registro di sistema vengono sempre archiviate con la versione originale del pacchetto, quindi gli aggiornamenti al pacchetto non saranno disponibili, a meno che non si ripari il pacchetto originale.</span><span class="sxs-lookup"><span data-stu-id="8ec33-119">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="8ec33-120">Le informazioni dettagliate non sono visibili per i documenti di Microsoft office2007 tramite la pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="8ec33-120">Detailed information is not visible for Microsoft Office2007 documents by using the properties page</span></span>


<span data-ttu-id="8ec33-121">Quando si prova a visualizzare informazioni dettagliate associate a un documento di Microsoft office2007 tramite la pagina delle proprietà, le informazioni dettagliate non sono visibili.</span><span class="sxs-lookup"><span data-stu-id="8ec33-121">When you try to view detailed information associated with a Microsoft Office2007 document by using the properties page, the detailed information is not visible.</span></span>

**<span data-ttu-id="8ec33-122">Soluzione</span><span class="sxs-lookup"><span data-stu-id="8ec33-122">Solution</span></span>**

<span data-ttu-id="8ec33-123">App-V non supporta le estensioni di Shell necessarie per queste pagine delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="8ec33-123">App-V does not support the required shell extensions for these property pages.</span></span>

## <span data-ttu-id="8ec33-124">Alcune chiavi del registro di sistema non vengono acquisite quando si sequenziano le applicazioni a 16 bit</span><span class="sxs-lookup"><span data-stu-id="8ec33-124">Some registry keys are not captured when you sequence 16-bit applications</span></span>


<span data-ttu-id="8ec33-125">In App-V 4,5 l'aggancio del registro di sistema è stato spostato dalla modalità kernel alla modalità utente.</span><span class="sxs-lookup"><span data-stu-id="8ec33-125">In App-V 4.5, registry hooking has been moved from kernel mode to user mode.</span></span> <span data-ttu-id="8ec33-126">Se si vuole sequenziare un'applicazione a 16 bit o un'applicazione che usa un programma di installazione a 16 bit, è necessario prima di tutto configurare il computer sequencer in modo che il processo venga eseguito in una copia di Windows NT Virtual DOS Machine (NTVDM).</span><span class="sxs-lookup"><span data-stu-id="8ec33-126">If you want to sequence a 16-bit application or an application that uses a 16-bit installer, you must first configure the sequencer computer so that the process runs in its own copy of the Windows NT Virtual DOS Machine (NTVDM).</span></span>

**<span data-ttu-id="8ec33-127">Soluzione</span><span class="sxs-lookup"><span data-stu-id="8ec33-127">Solution</span></span>**

<span data-ttu-id="8ec33-128">Prima di sequenziare l'applicazione, imposta il valore della chiave del registro di sistema REGSZ globale seguente su "Yes" nel computer di sequenziazione:</span><span class="sxs-lookup"><span data-stu-id="8ec33-128">Before you sequence the application, set the following global REGSZ registry key value to "yes" on the sequencing computer:</span></span>

<span data-ttu-id="8ec33-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span><span class="sxs-lookup"><span data-stu-id="8ec33-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span></span>

<span data-ttu-id="8ec33-130">È necessario riavviare il computer prima che questa operazione abbia effetto.</span><span class="sxs-lookup"><span data-stu-id="8ec33-130">You must restart the computer before this takes effect.</span></span>

## <span data-ttu-id="8ec33-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8ec33-131">Related topics</span></span>


[<span data-ttu-id="8ec33-132">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="8ec33-132">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





