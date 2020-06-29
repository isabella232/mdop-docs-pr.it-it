---
title: Come usare il file differenziale SFT
description: Come usare il file differenziale SFT
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816386"
---
# <span data-ttu-id="7fd7c-103">Come usare il file differenziale SFT</span><span class="sxs-lookup"><span data-stu-id="7fd7c-103">How to Use the Differential SFT File</span></span>


<span data-ttu-id="7fd7c-104">Durante la sequenziazione di un'applicazione, Microsoft Application Virtualization (App-V) Sequencer crea i file SFT (. SFT) per archiviare tutti i contenuti e le informazioni di configurazione dell'applicazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-104">When sequencing an application, the Microsoft Application Virtualization (App-V) Sequencer creates SFT files (.sft) to store all of the virtual application’s files content and configuration information.</span></span> <span data-ttu-id="7fd7c-105">Nella versione 4.5 di App-V è stato introdotto il file differenziale SFT (. dsft).</span><span class="sxs-lookup"><span data-stu-id="7fd7c-105">In version4.5 of App-V, the Differential SFT (.dsft) file has been introduced.</span></span> <span data-ttu-id="7fd7c-106">Dopo aver usato il sequencer per creare un aggiornamento per un pacchetto esistente, puoi scegliere di generare questo file per archiviare solo le differenze tra il pacchetto di applicazione sequenziata originale e la nuova versione.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-106">After using the Sequencer to create an upgrade for an existing package, you can choose to generate this file to store only the differences between the original sequenced application package and the new version.</span></span> <span data-ttu-id="7fd7c-107">È quindi molto più piccolo del file SFT completo per la nuova versione dell'applicazione e riduce l'impatto dell'invio di aggiornamenti del pacchetto sulle connessioni di rete a larghezza di banda ridotta.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-107">It is therefore much smaller than the full SFT file would be for the new version of the application and reduces the impact of sending package updates over low-bandwidth network connections.</span></span> <span data-ttu-id="7fd7c-108">Tuttavia, il suo uso è supportato solo in determinate situazioni limitate.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-108">However, its use is supported only in certain restricted situations.</span></span> <span data-ttu-id="7fd7c-109">Questa caratteristica è stata progettata per essere usata in modo specifico in cui si usa un sistema ESD (Electronic Software Distribution) per gestire un gruppo di utenti con un file server locale tramite una connessione a larghezza di banda ridotta e non si usa App-V Streaming Server.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-109">This feature was intended to be used specifically where you are using an electronic software distribution (ESD) system to manage a group of users with a local file server over a low-bandwidth connection and you are not using App-V streaming servers.</span></span>

<span data-ttu-id="7fd7c-110">Non è necessario usare il file differenziale SFT se si usa la configurazione di Manager2007 per gestire gli utenti, perché Configuration Manager supporta le distribuzioni con larghezza di banda ridotta già integrate.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-110">You do not need to use the Differential SFT file if you are using Configuration Manager2007 to manage the users, because Configuration Manager has support for low-bandwidth deployments already built in.</span></span> <span data-ttu-id="7fd7c-111">Non è inoltre necessario se si usa la gestione di Application Virtualization (App-V) o i server di flusso con aggiornamento attivo, perché il client recupererà solo le differenze tra le versioni precedenti e quelle nuove del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-111">It is also not required if you are using Application Virtualization (App-V) Management or Streaming Servers with Active Upgrade because the client will retrieve only the differences between the old and new package versions.</span></span>

<span data-ttu-id="7fd7c-112">La procedura seguente illustra come usare il mkdiffpkg.exe incluso nell'installazione di Sequencer per creare il file differenziale SFT, dopo aver completato l'aggiornamento del pacchetto di applicazione virtuale e per distribuire il file differenziale SFT.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-112">The following procedure shows how to use the mkdiffpkg.exe that is included in the Sequencer installation to create the Differential SFT file, after completing the upgrade of the virtual application package, and to deploy the Differential SFT file.</span></span> <span data-ttu-id="7fd7c-113">Il completamento di questa procedura consente di verificare che, se il pacchetto viene in qualche modo scaricato dal computer client, la volta successiva che l'utente prova a eseguire l'applicazione, il client ritornerà all'URL di override, che è impostato per trasmettere il pacchetto completo V2. sft dalla condivisione file locale.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-113">Completing this procedure helps ensure that if the package is somehow unloaded from the client computer, the next time the user tries to run the application, the client will fall back to the override URL, which is set to stream the full package V2.sft from the local file share.</span></span> <span data-ttu-id="7fd7c-114">In questo modo eviterai qualsiasi errore per l'utente durante l'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-114">This will avoid any failure for the user when starting the application.</span></span> <span data-ttu-id="7fd7c-115">Se l'intero client viene danneggiato o viene disinstallato, è consigliabile che il sistema ESD sia configurato per distribuire la versione completa del pacchetto aggiornato, V2. SFT, al client.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-115">If the entire client becomes corrupted or is uninstalled, it is recommended that the ESD system be configured to deploy the full version of the upgraded package, V2.sft, to the client.</span></span>

<span data-ttu-id="7fd7c-116">Per altre informazioni sull'aggiornamento di un pacchetto, vedere "come aggiornare un'applicazione virtuale esistente" in App-V 4.5 Operations Guide at</span><span class="sxs-lookup"><span data-stu-id="7fd7c-116">For more information about upgrading a package, see “How to Upgrade an Existing Virtual Application” in the App-V4.5 Operations Guide at</span></span> <https://go.microsoft.com/fwlink/?LinkId=133129>

<span data-ttu-id="7fd7c-117">**Nota**  Come prerequisito, tutti i computer degli utenti a cui viene assegnato l'ESD devono avere il file v1. SFT completamente caricato nella cache locale e il flusso di file deve essere abilitato in tutti i computer.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-117">**Note** As a prerequisite, all user computers being targeted by the ESD must have the V1.sft file fully loaded into their local cache, and file streaming must be enabled on all computers.</span></span>

 

**<span data-ttu-id="7fd7c-118">Per usare il file differenziale SFT</span><span class="sxs-lookup"><span data-stu-id="7fd7c-118">To use the Differential SFT file</span></span>**

1.  <span data-ttu-id="7fd7c-119">Accedere al computer sequencer usando un account con diritti di amministratore.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-119">Log on to the Sequencer computer by using an account with administrator rights.</span></span> <span data-ttu-id="7fd7c-120">Aprire il pacchetto originale (V1) per l'aggiornamento nel sequencer e quindi aggiornare il pacchetto alla nuova versione (v2) e salvarlo come nuovo V2. SFT.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-120">Open the original package (V1) for upgrade in the Sequencer, and then upgrade the package to the new version (V2) and save it as a new V2.sft.</span></span>

2.  <span data-ttu-id="7fd7c-121">Aprire una finestra di comando nella cartella di installazione dell'App-V 4.5 Sequencer ed eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="7fd7c-121">Open a command window in the App-V4.5 Sequencer installation folder, and run the following command:</span></span>

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  <span data-ttu-id="7fd7c-122">Usando il sistema ESD o un altro processo di copia di file, copiare il file di contenuto del pacchetto V2 completo, V2. SFT, in una condivisione di file locale accessibile ai computer degli utenti in una connessione di rete ben collegata.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-122">Using the ESD system or other file copy process, copy the full V2 package content file, V2.sft, to a local file share that is accessible to the user computers on a well-connected network connection.</span></span>

4.  <span data-ttu-id="7fd7c-123">Usando il sistema ESD, inserire una copia del file differenziale SFT, V2. dsft, in ogni computer utente.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-123">Using the ESD system, place a copy of the Differential SFT file, V2.dsft, on each user computer.</span></span>

5.  <span data-ttu-id="7fd7c-124">Per importare il file V2. dsft, eseguire il comando SFTMIME seguente in ogni computer utente:</span><span class="sxs-lookup"><span data-stu-id="7fd7c-124">To import the V2.dsft file, run the following SFTMIME command on each user computer:</span></span>

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  <span data-ttu-id="7fd7c-125">Eseguire il comando SFTMIME seguente in ogni computer utente per impostare l'URL di override in punto del file V2. SFT:</span><span class="sxs-lookup"><span data-stu-id="7fd7c-125">Run the following SFTMIME command on each user computer to set the override URL to point to the V2.sft file:</span></span>

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**<span data-ttu-id="7fd7c-126">Nota</span><span class="sxs-lookup"><span data-stu-id="7fd7c-126">Note</span></span>**  
-   <span data-ttu-id="7fd7c-127">I file differenziali SFT devono essere applicati ai client nell'ordine corretto.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-127">Differential SFT files must be applied to clients in the correct order.</span></span> <span data-ttu-id="7fd7c-128">Ad esempio, V2. dsft deve essere applicato a un'applicazione V1 prima di applicare V3. dsft.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-128">For example, V2.dsft must be applied to a V1 application before V3.dsft is applied.</span></span>

-   <span data-ttu-id="7fd7c-129">La funzionalità **Genera pacchetto di Microsoft Windows Installer (MSI)** nel sequencer non può essere usata con il file differenziale SFT.</span><span class="sxs-lookup"><span data-stu-id="7fd7c-129">The **Generate Microsoft Windows Installer (MSI) Package** capability in the Sequencer cannot be used with the Differential SFT file.</span></span>

 

## <span data-ttu-id="7fd7c-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fd7c-130">Related topics</span></span>


[<span data-ttu-id="7fd7c-131">Come creare o aggiornare le applicazioni virtuali tramite App-V Sequencer</span><span class="sxs-lookup"><span data-stu-id="7fd7c-131">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





