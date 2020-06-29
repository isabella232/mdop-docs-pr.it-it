---
ms.reviewer: ''
title: Come usare un'applicazione App-V 4,6 da un'applicazione App-V 5,0
description: Come usare un'applicazione App-V 4,6 da un'applicazione App-V 5,0
ms.assetid: 4e78cb32-9c8b-478e-ae8b-c474a7e42487
author: msfttracyp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8b29e861b97d18e427f6a8247a1f731be2dc0889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805133"
---
# <span data-ttu-id="ee4f5-103">Come usare un'applicazione App-V 4,6 da un'applicazione App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="ee4f5-103">How to Use an App-V 4.6 Application From an App-V 5.0 Application</span></span>

<span data-ttu-id="ee4f5-104">*Nota:*\* App-V 4,6 è uscito dal supporto mainstream.</span><span class="sxs-lookup"><span data-stu-id="ee4f5-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="ee4f5-105">La procedura seguente si applica a un pacchetto App-V 4,6 SP3.</span><span class="sxs-lookup"><span data-stu-id="ee4f5-105">The following applies to an App-V 4.6 SP3 package.</span></span>

<span data-ttu-id="ee4f5-106">Usare la procedura seguente per eseguire un'applicazione App-V 4.6 con le applicazioni App-V 5,0 in un client autonomo.</span><span class="sxs-lookup"><span data-stu-id="ee4f5-106">Use the following procedure to run an App-V4.6 application with App-V 5.0 applications on a standalone client.</span></span>

**<span data-ttu-id="ee4f5-107">Per eseguire applicazioni in un client autonomo</span><span class="sxs-lookup"><span data-stu-id="ee4f5-107">To run applications on a standalone client</span></span>**

1.  <span data-ttu-id="ee4f5-108">Selezionare due applicazioni nell'ambiente che possono essere aperte l'una dall'altra.</span><span class="sxs-lookup"><span data-stu-id="ee4f5-108">Select two applications in your environment that can be opened from one another.</span></span> <span data-ttu-id="ee4f5-109">Ad esempio, Microsoft Outlook e Adobe Acrobat Reader.</span><span class="sxs-lookup"><span data-stu-id="ee4f5-109">For example, Microsoft Outlook and Adobe Acrobat Reader.</span></span> <span data-ttu-id="ee4f5-110">È possibile accedere a un allegato di posta elettronica creato con Adobe Acrobat.</span><span class="sxs-lookup"><span data-stu-id="ee4f5-110">You can access an email attachment created using Adobe Acrobat.</span></span>

2.  <span data-ttu-id="ee4f5-111">Converti i pacchetti o crea un nuovo pacchetto per una delle applicazioni che usano il formato App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ee4f5-111">Convert the packages, or create a new package for either of the applications using the App-V 5.0 format.</span></span> <span data-ttu-id="ee4f5-112">Per altre informazioni sulla conversione di pacchetti, vedere [come eseguire la migrazione di punti di estensione da un pacchetto App-v 4,6 a un pacchetto di App-v 5,0 convertito per tutti gli utenti in un computer specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) o [come eseguire la migrazione di punti di estensione da un pacchetto app-v 4,6 a app-v 5,0 per un utente specifico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="ee4f5-112">For more information about converting packages see, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) or [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span></span>

3.  <span data-ttu-id="ee4f5-113">Aggiungere e eseguire il provisioning del pacchetto usando la console di gestione di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="ee4f5-113">Add and provision the package using the App-V 5.0 management console.</span></span> <span data-ttu-id="ee4f5-114">Per altre informazioni sull'aggiunta e il provisioning di pacchetti, vedere [come aggiungere o aggiornare pacchetti tramite la console di gestione](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) e [come configurare l'accesso ai pacchetti tramite la console di gestione](how-to-configure-access-to-packages-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="ee4f5-114">For more information adding and provisioning packages see, [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Configure Access to Packages by Using the Management Console](how-to-configure-access-to-packages-by-using-the-management-console-50.md).</span></span>

4.  <span data-ttu-id="ee4f5-115">L'applicazione convertita viene ora eseguita tramite App-V 5,0 ed è possibile aprire un'applicazione dall'altra.</span><span class="sxs-lookup"><span data-stu-id="ee4f5-115">The converted application now runs using App-V 5.0 and you can open one application from the other.</span></span> <span data-ttu-id="ee4f5-116">Ad esempio, se hai convertito un pacchetto di Microsoft Office in un pacchetto di App-V 5,0 e Adobe Acrobat è ancora in corso come pacchetto App-V 4.6, puoi aprire un allegato di Adobe Acrobat Reader con Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="ee4f5-116">For example, if you converted a Microsoft Office package to an App-V 5.0 package and Adobe Acrobat is still running as an App-V4.6 package, you can open an Adobe Acrobat Reader attachment using Microsoft Outlook.</span></span>

    <span data-ttu-id="ee4f5-117">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="ee4f5-117">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="ee4f5-118">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="ee4f5-118">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="ee4f5-119">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="ee4f5-119">Got an App-V issue?</span></span>** <span data-ttu-id="ee4f5-120">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="ee4f5-120">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="ee4f5-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee4f5-121">Related topics</span></span>


[<span data-ttu-id="ee4f5-122">Operazioni per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="ee4f5-122">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 








