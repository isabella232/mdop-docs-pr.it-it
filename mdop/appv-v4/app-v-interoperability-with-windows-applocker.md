---
title: Interoperabilità di App-V con Windows AppLocker
description: Interoperabilità di App-V con Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822315"
---
# <span data-ttu-id="2317f-103">Interoperabilità di App-V con Windows AppLocker</span><span class="sxs-lookup"><span data-stu-id="2317f-103">App-V Interoperability with Windows AppLocker</span></span>


<span data-ttu-id="2317f-104">La versione 4,5 SP1 di Microsoft Application Virtualization (App-V) client supporta la funzionalità AppLocker di Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2317f-104">Version 4.5 SP1 of the Microsoft Application Virtualization (App-V) client supports the AppLocker feature of Windows 7.</span></span> <span data-ttu-id="2317f-105">La funzionalità AppLocker consente agli amministratori IT di specificare quali applicazioni sono limitate dall'uso in computer.</span><span class="sxs-lookup"><span data-stu-id="2317f-105">The AppLocker feature enables IT administrators to specify which applications are restricted from running on computers.</span></span> <span data-ttu-id="2317f-106">Questo documento descrive come configurare le regole di AppLocker per l'utilizzo con l'ambiente virtuale App-V e le applicazioni virtualizzate.</span><span class="sxs-lookup"><span data-stu-id="2317f-106">This document describes how to configure the AppLocker rules to work with the App-V virtual environment and virtualized applications.</span></span>

<span data-ttu-id="2317f-107">**Nota**  Windows AppLocker deve prima essere abilitato prima di configurare le regole di Windows AppLocker per le applicazioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="2317f-107">**Note** Windows AppLocker must first be enabled before configuring Windows AppLocker rules for virtual applications.</span></span> <span data-ttu-id="2317f-108">Per altre informazioni sull'abilitazione di Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .</span><span class="sxs-lookup"><span data-stu-id="2317f-108">For more information about enabling Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) (https://go.microsoft.com/fwlink/?LinkId=156732).</span></span>

 

## <span data-ttu-id="2317f-109">Configurazione delle regole di Windows AppLocker per le applicazioni virtuali</span><span class="sxs-lookup"><span data-stu-id="2317f-109">Configuring Windows AppLocker Rules for Virtual Applications</span></span>


<span data-ttu-id="2317f-110">Gli amministratori locali possono creare regole di Windows AppLocker che limitano l'uso di file eseguibili di programmi (file exe), file di Windows Installer (file con estensione msi e msp) e script (con estensione PS, bat, cmd e js).</span><span class="sxs-lookup"><span data-stu-id="2317f-110">Local administrators can create Windows AppLocker rules that restrict the running of program executables (.exe files), Windows Installer files (.msi and .msp files), and scripts (.ps, .bat, .cmd, .vbs and .js files).</span></span> <span data-ttu-id="2317f-111">L'amministratore esegue questa operazione usando un computer di riferimento in cui è installato il client App-V e che contiene tutte le applicazioni virtuali rilevanti in streaming nella cache del client.</span><span class="sxs-lookup"><span data-stu-id="2317f-111">The administrator does this by using a reference computer that has the App-V client installed and that has all the relevant virtual applications streamed to the client cache.</span></span> <span data-ttu-id="2317f-112">L'amministratore usa quindi la sezione Windows AppLocker dello snap-in Microsoft Management Console (MMC) dei criteri di sicurezza locali nel computer di riferimento per creare le regole.</span><span class="sxs-lookup"><span data-stu-id="2317f-112">The administrator then uses the Windows AppLocker section of the Local Security Policy Microsoft Management Console (MMC) snap-in on the reference computer to create the rules.</span></span>

<span data-ttu-id="2317f-113">Quando si cerca un percorso di directory o un file specifico per cui si vuole creare una regola, è possibile accedere all'unità App-V usando il percorso della condivisione nascosta.</span><span class="sxs-lookup"><span data-stu-id="2317f-113">When you browse to find a directory path or specific file for which you want to create a rule, you can access the App-V drive by using the path to the hidden share.</span></span> <span data-ttu-id="2317f-114">Ad esempio, puoi passare a \\\\localhost\\Q $, dove l'App-V Drive è drive Q. Tuttavia, per creare la regola, devi modificare il percorso per rimuovere il riferimento a \\\\localhost\\Q $ e usare Q:\\.</span><span class="sxs-lookup"><span data-stu-id="2317f-114">For example, you can browse to \\\\localhost\\Q$, where the App-V drive is drive Q. However, to create the rule, you must edit the path to remove the reference to \\\\localhost\\Q$ and use Q:\\ instead.</span></span> <span data-ttu-id="2317f-115">È necessario avviare ogni applicazione nel computer di riferimento per accedere ai file dell'applicazione e sono necessari i diritti amministrativi per passare a \\\\localhost\\Q $.</span><span class="sxs-lookup"><span data-stu-id="2317f-115">You must start each application on the reference computer to access the application’s files, and administrative rights are required to browse to \\\\localhost\\Q$.</span></span>

 

 





