---
title: Risoluzione dei problemi di Application Virtualization Sequencer
description: Risoluzione dei problemi di Application Virtualization Sequencer
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815185"
---
# <span data-ttu-id="08bd4-103">Risoluzione dei problemi di Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="08bd4-103">Troubleshooting the Application Virtualization Sequencer</span></span>


<span data-ttu-id="08bd4-104">Questo argomento include informazioni che è possibile usare per risolvere i problemi generali di Application Virtualization (App-V) Sequencer.</span><span class="sxs-lookup"><span data-stu-id="08bd4-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="08bd4-105">La creazione di un file SFTD tramite App-V Sequencer aumenta il numero di versione in modo imprevisto</span><span class="sxs-lookup"><span data-stu-id="08bd4-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="08bd4-106">Il numero di versione associato a un file SFTD aumenta in modo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="08bd4-106">The version number associated with an SFTD file increases unexpectedly.</span></span>

**<span data-ttu-id="08bd4-107">Soluzione</span><span class="sxs-lookup"><span data-stu-id="08bd4-107">Solution</span></span>**

<span data-ttu-id="08bd4-108">Usare la riga di comando per generare un nuovo file SFT.</span><span class="sxs-lookup"><span data-stu-id="08bd4-108">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="08bd4-109">Per creare il file SFT usando la riga di comando, immettere quanto segue al prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="08bd4-109">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="08bd4-110">mkdiffpkg.exe &lt; base SFT nome file &gt; &lt; diff SFT nome file&gt;</span><span class="sxs-lookup"><span data-stu-id="08bd4-110">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="08bd4-111">Il nome file nel file OSD non è corretto dopo l'aggiornamento del pacchetto</span><span class="sxs-lookup"><span data-stu-id="08bd4-111">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="08bd4-112">Dopo l'aggiornamento di un pacchetto esistente, il nome del file non è corretto.</span><span class="sxs-lookup"><span data-stu-id="08bd4-112">After you upgrade an existing package, the file name is not correct.</span></span>

**<span data-ttu-id="08bd4-113">Soluzione</span><span class="sxs-lookup"><span data-stu-id="08bd4-113">Solution</span></span>**

<span data-ttu-id="08bd4-114">Quando si apre un pacchetto per l'aggiornamento, è necessario specificare l'unità root Q:\\ come percorso di output per il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="08bd4-114">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="08bd4-115">Non specificare un nome file associato con la posizione di output.</span><span class="sxs-lookup"><span data-stu-id="08bd4-115">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="08bd4-116">L'installazione predefinita di Microsoft Word2003 genera un errore quando viene trasmesso a un client</span><span class="sxs-lookup"><span data-stu-id="08bd4-116">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="08bd4-117">Quando si esegue lo streaming di Microsoft Word2003 in un client, viene restituito un errore, ma Microsoft Word continua a essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="08bd4-117">When you stream Microsoft Word2003 to a client, an error is returned but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="08bd4-118">Soluzione</span><span class="sxs-lookup"><span data-stu-id="08bd4-118">Solution</span></span>**

<span data-ttu-id="08bd4-119">Risequenziare il pacchetto dell'applicazione virtuale e selezionare **installazione completa**.</span><span class="sxs-lookup"><span data-stu-id="08bd4-119">Resequence the virtual application package, and select **Full Install**.</span></span>

## <span data-ttu-id="08bd4-120">L'aggiornamento del pacchetto non funziona quando si crea un pacchetto dipendente</span><span class="sxs-lookup"><span data-stu-id="08bd4-120">Package Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="08bd4-121">Quando si crea un pacchetto dipendente con l'aggiornamento del pacchetto e si aggiungono nuove voci del registro di sistema, la funzione viene visualizzata correttamente, ma le voci del registro di sistema aggiornate non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="08bd4-121">When you create a dependent package by using package upgrade and add new registry entries, it appears to function correctly but the updated registry entries are not available.</span></span>

**<span data-ttu-id="08bd4-122">Soluzione</span><span class="sxs-lookup"><span data-stu-id="08bd4-122">Solution</span></span>**

<span data-ttu-id="08bd4-123">Le impostazioni del registro di sistema vengono sempre archiviate con la versione originale del pacchetto, quindi gli aggiornamenti al pacchetto non saranno disponibili, a meno che non si ripari il pacchetto originale.</span><span class="sxs-lookup"><span data-stu-id="08bd4-123">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="08bd4-124">Errore durante il tentativo di sequenziazione. NET 2.0</span><span class="sxs-lookup"><span data-stu-id="08bd4-124">Error When Trying to Sequence .NET2.0</span></span>


<span data-ttu-id="08bd4-125">Quando si sequenzia un pacchetto che richiede. NET 2.0 viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="08bd4-125">When you sequence a package that requires .NET2.0, you get an error.</span></span>

**<span data-ttu-id="08bd4-126">Soluzione</span><span class="sxs-lookup"><span data-stu-id="08bd4-126">Solution</span></span>**

<span data-ttu-id="08bd4-127">Sequenziazione di pacchetti che richiedono. NET 2.0 non è supportato.</span><span class="sxs-lookup"><span data-stu-id="08bd4-127">Sequencing packages that require .NET2.0 is not supported.</span></span>

## <span data-ttu-id="08bd4-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08bd4-128">Related topics</span></span>


[<span data-ttu-id="08bd4-129">Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="08bd4-129">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





