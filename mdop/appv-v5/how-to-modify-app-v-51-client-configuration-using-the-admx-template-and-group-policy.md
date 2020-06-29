---
title: Come modificare la configurazione del client App-V 5.1 usando il modello ADMX e Criteri di gruppo
description: Come modificare la configurazione del client App-V 5.1 usando il modello ADMX e Criteri di gruppo
author: dansimp
ms.assetid: 0d9cf13a-b29c-4c87-a776-15fea34027dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 18363b4fb904d995862ac30634be1350c972d918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805266"
---
# <span data-ttu-id="2419d-103">Come modificare la configurazione del client App-V 5.1 usando il modello ADMX e Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2419d-103">How to Modify App-V 5.1 Client Configuration Using the ADMX Template and Group Policy</span></span>


<span data-ttu-id="2419d-104">Usare il modello ADMX di Microsoft Application Virtualization (App-V) 5,1 per configurare le impostazioni del client App-V 5,1 tramite il modello ADMX e i criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="2419d-104">Use the Microsoft Application Virtualization (App-V) 5.1 ADMX template to configure App-V 5.1 client settings using the ADMX Template and Group Policy.</span></span>

**<span data-ttu-id="2419d-105">Per modificare la configurazione client di App-V 5,1 con criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="2419d-105">To modify App-V 5.1 client configuration using Group Policy</span></span>**

1.  <span data-ttu-id="2419d-106">Per modificare la configurazione del client App-V 5,1, individuare i file di **ADMXTemplate** disponibili in App-v 5,1.</span><span class="sxs-lookup"><span data-stu-id="2419d-106">To modify the App-V 5.1 client configuration, locate the **ADMXTemplate** files that are available with App-V 5.1.</span></span>

    <span data-ttu-id="2419d-107">**Nota**  Usare il collegamento seguente per scaricare i **modelli di ADMX**App-V 5,1: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .</span><span class="sxs-lookup"><span data-stu-id="2419d-107">**Note** Use the following link to download the App-V 5.1 **ADMX Templates**: <https://go.microsoft.com/fwlink/p/?LinkId=393941>.</span></span>

     

2.  <span data-ttu-id="2419d-108">Nel computer in cui vengono gestiti i criteri di gruppo, in genere il controller di dominio, copiare il file con estensione **ADMX** modello nella directory seguente: \*\* &lt; unità di installazione &gt; \ \ Windows \ \ PolicyDefinitions\*\*.</span><span class="sxs-lookup"><span data-stu-id="2419d-108">On the computer where you manage group Policy, typically the domain controller, copy the template **.admx** file to the following directory: **&lt;Installation Drive&gt; \\ Windows \\ PolicyDefinitions**.</span></span>

    <span data-ttu-id="2419d-109">Nello stesso computer copiare quindi il file con estensione **ADML** nella directory seguente: \*\* &lt; InstallationDrive &gt; \ \ Windows \ \ POLICYDEFINITIONS \ \ en-US\*\*.</span><span class="sxs-lookup"><span data-stu-id="2419d-109">Next, on the same computer, copy the **.adml** file to the following directory: **&lt;InstallationDrive&gt; \\ Windows \\ PolicyDefinitions \\ en-US**.</span></span>

3.  <span data-ttu-id="2419d-110">Dopo aver copiato i file, aprire la console di gestione di criteri di gruppo per modificare i criteri associati ai client App-v 5,1 individuare i criteri di **configurazione dei computer**  /  **Policies**  /  **modelli amministrativi**  /  **System**  /  **App-v**.</span><span class="sxs-lookup"><span data-stu-id="2419d-110">After you have copied the files open the Group Policy Management Console, to modify the policies associated with your App-V 5.1 clients browse to **Computer Configuration** / **Policies** / **Administrative Templates** / **System** / **App-V**.</span></span>

    <span data-ttu-id="2419d-111">**Hai un suggerimento per App-V**?</span><span class="sxs-lookup"><span data-stu-id="2419d-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="2419d-112">Aggiungere o votare i suggerimenti [qui](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="2419d-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="2419d-113">Hai un problema con l'App-V?</span><span class="sxs-lookup"><span data-stu-id="2419d-113">Got an App-V issue?</span></span>** <span data-ttu-id="2419d-114">Usare l' [App-V Forum TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="2419d-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="2419d-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2419d-115">Related topics</span></span>


[<span data-ttu-id="2419d-116">Distribuzione di App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="2419d-116">Deploying App-V 5.1</span></span>](deploying-app-v-51.md)

[<span data-ttu-id="2419d-117">Informazioni sulle impostazioni di configurazione client</span><span class="sxs-lookup"><span data-stu-id="2419d-117">About Client Configuration Settings</span></span>](about-client-configuration-settings51.md)

 

 





