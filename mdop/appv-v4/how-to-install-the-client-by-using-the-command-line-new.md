---
title: Come installare il client usando la riga di comando
description: Come installare il client usando la riga di comando
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817325"
---
# <span data-ttu-id="cbbca-103">Come installare il client usando la riga di comando</span><span class="sxs-lookup"><span data-stu-id="cbbca-103">How to Install the Client by Using the Command Line</span></span>


<span data-ttu-id="cbbca-104">Gli argomenti di questa sezione includono procedure per installare il client Desktop Application Virtualization (App-V) o il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal) usando setup.exe o setup.msi.</span><span class="sxs-lookup"><span data-stu-id="cbbca-104">The topics in this section include procedures to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span> <span data-ttu-id="cbbca-105">Per eseguire il programma di installazione è necessario disporre dei diritti amministrativi.</span><span class="sxs-lookup"><span data-stu-id="cbbca-105">Administrative rights are required to run either setup program.</span></span>

<span data-ttu-id="cbbca-106">Puoi usare i parametri facoltativi della riga di comando per applicare impostazioni di configurazione specifiche al client App-V durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="cbbca-106">You can use optional command-line parameters to apply specific configuration settings to the App-V client during the installation.</span></span> <span data-ttu-id="cbbca-107">Per altre informazioni sull'uso dei parametri, vedere [parametri della riga di comando di Application Virtualization Client Installer](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cbbca-107">For more information about using parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span> <span data-ttu-id="cbbca-108">Se sono state applicate le impostazioni del registro di sistema a un computer prima di distribuire un client, ad esempio tramite criteri di gruppo, queste impostazioni vengono mantenute e vengono applicati altri parametri della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="cbbca-108">If you have applied registry settings to a computer before deploying a client—for example, by using Group Policy—these settings are retained and any additional command line parameters are applied.</span></span> <span data-ttu-id="cbbca-109">I valori dei parametri della riga di comando sostituiscono qualsiasi valore esistente per la stessa impostazione.</span><span class="sxs-lookup"><span data-stu-id="cbbca-109">Command line parameter values will replace any existing value for the same setting.</span></span>

<span data-ttu-id="cbbca-110">**Nota**  Quando si installa il client App-V da usare con una cache di sola lettura, ad esempio con un'implementazione del server VDI, è necessario impostare il parametro *AUTOLOADTARGET* su None per impedire al client di provare ad aggiornare le applicazioni quando la cache è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="cbbca-110">**Note** When you install the App-V client to use with a read-only cache, for example with a VDI server implementation, you must set the *AUTOLOADTARGET* parameter to NONE to prevent the client from trying to update applications when the cache is read-only.</span></span>

 

<span data-ttu-id="cbbca-111">Per altre informazioni sull'impostazione di questi valori di parametro dopo l'installazione, vedere [come configurare le impostazioni del registro di sistema client App-v usando la riga di comando](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) nella Guida alle operazioni di Application Virtualization (app-v).</span><span class="sxs-lookup"><span data-stu-id="cbbca-111">For more information about setting these parameter values after installation, see [How to Configure the App-V Client Registry Settings by Using the Command Line](https://go.microsoft.com/fwlink/?LinkId=169355) (https://go.microsoft.com/fwlink/?LinkId=169355) in the Application Virtualization (App-V) Operations Guide.</span></span>

<span data-ttu-id="cbbca-112">**Nota**  Se un'impostazione di configurazione nel computer dell'utente dipende dal percorso di installazione del client, tenere presente che il client Application Virtualization (App-V) 4.5 copia i file di installazione in una cartella diversa rispetto alle versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="cbbca-112">**Note** If a configuration setting on the user’s computer depends on the client installation path, note that the Application Virtualization (App-V)4.5 client copies its installation files to a different folder than previous versions did.</span></span> <span data-ttu-id="cbbca-113">Per impostazione predefinita, una nuova installazione del client App-V 4.5 copierà i file di installazione nella cartella cartella \\Programmi\\microsoft Application Virtualization Client.</span><span class="sxs-lookup"><span data-stu-id="cbbca-113">By default, a new installation of the App-V4.5 client will copy its installation files to the \\Program Files\\Microsoft Application Virtualization Client folder.</span></span> <span data-ttu-id="cbbca-114">Se una versione precedente del client è già installata, l'esecuzione del programma di installazione client App-V 4,5 eseguirà un aggiornamento del client esistente usando la cartella di installazione esistente.</span><span class="sxs-lookup"><span data-stu-id="cbbca-114">If an earlier version of the client is already installed, running the App-V 4.5 client installer will perform an upgrade of the existing client using the existing installation folder.</span></span>

 

<span data-ttu-id="cbbca-115">\ [Valore token modello \]</span><span class="sxs-lookup"><span data-stu-id="cbbca-115">\[Template Token Value\]</span></span>

<span data-ttu-id="cbbca-116">**Nota**  Per App-V versione 4.6 e successive, quando è installato App-V client, SFTLDR.DLL viene copiato nella directory Windows\\system32.</span><span class="sxs-lookup"><span data-stu-id="cbbca-116">**Note** For App-V version4.6 and later, when the App-V client is installed, SFTLDR.DLL is copied to the Windows\\system32 directory.</span></span> <span data-ttu-id="cbbca-117">Se l'App-V client è installata in un sistema a 64 bit, SFTLDR\_WOW64.DLL viene copiato nella directory Windows\\SysWOW64.</span><span class="sxs-lookup"><span data-stu-id="cbbca-117">If the App-V client is installed on a 64-bit system, SFTLDR\_WOW64.DLL is copied to the Windows\\SysWOW64 directory.</span></span>

 

<span data-ttu-id="cbbca-118">\ [Valore token modello \]</span><span class="sxs-lookup"><span data-stu-id="cbbca-118">\[Template Token Value\]</span></span>

## <span data-ttu-id="cbbca-119">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="cbbca-119">In This Section</span></span>


<span data-ttu-id="cbbca-120">Gli argomenti seguenti descrivono come installare il client Desktop Application Virtualization (App-V) o il client App-V per Servizi Desktop remoto (in precedenza Servizi terminal) usando setup.exe o setup.msi.</span><span class="sxs-lookup"><span data-stu-id="cbbca-120">The following topics describe how to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[<span data-ttu-id="cbbca-121">Come installare il client App-V con Setup.exe</span><span class="sxs-lookup"><span data-stu-id="cbbca-121">How to Install the App-V Client by Using Setup.exe</span></span>](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
<span data-ttu-id="cbbca-122">Fornisce una procedura dettagliata per l'installazione del client App-V tramite il programma setup.exe.</span><span class="sxs-lookup"><span data-stu-id="cbbca-122">Provides a step-by-step procedure for installing the App-V client by using the setup.exe program.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[<span data-ttu-id="cbbca-123">Come installare il client App-V con Setup.msi</span><span class="sxs-lookup"><span data-stu-id="cbbca-123">How to Install the App-V Client by Using Setup.msi</span></span>](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
<span data-ttu-id="cbbca-124">Fornisce procedure dettagliate per l'installazione di qualsiasi software prerequisito e anche per il client App-V tramite il programma setup.msi.</span><span class="sxs-lookup"><span data-stu-id="cbbca-124">Provides step-by-step procedures for installing any prerequisite software and also the App-V client by using the setup.msi program.</span></span>

## <span data-ttu-id="cbbca-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cbbca-125">Related topics</span></span>


[<span data-ttu-id="cbbca-126">Parametri della riga di comando del programma di installazione di Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="cbbca-126">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="cbbca-127">Come installare manualmente Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="cbbca-127">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="cbbca-128">Come pubblicare un'applicazione virtuale nel client</span><span class="sxs-lookup"><span data-stu-id="cbbca-128">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="cbbca-129">Come disinstallare il client App-V</span><span class="sxs-lookup"><span data-stu-id="cbbca-129">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





