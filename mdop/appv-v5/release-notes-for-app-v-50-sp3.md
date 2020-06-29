---
title: Note sulla versione di App-V 5.0 SP3
description: Note sulla versione di App-V 5.0 SP3
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804893"
---
# <span data-ttu-id="6666d-103">Note sulla versione di App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6666d-103">Release Notes for App-V 5.0 SP3</span></span>


<span data-ttu-id="6666d-104">Di seguito sono riportati i problemi noti di Microsoft Application Virtualization (App-V) 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="6666d-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.0 SP3.</span></span>

## <span data-ttu-id="6666d-105">I file del server non vengono eliminati dopo una nuova installazione di App-V 5,0 SP3 server</span><span class="sxs-lookup"><span data-stu-id="6666d-105">Server files fail to get deleted after a new App-V 5.0 SP3 Server installation</span></span>


<span data-ttu-id="6666d-106">Se si disinstalla il server App-V 5,0 SP1 e quindi si installa il server App-V 5,0 SP3, l'installazione non riesce e viene installata la versione errata del server di gestione.</span><span class="sxs-lookup"><span data-stu-id="6666d-106">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.0 SP3 Server, the installation fails and the wrong version of the Management server is installed.</span></span> <span data-ttu-id="6666d-107">Vengono visualizzati gli errori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6666d-107">The following errors are displayed:</span></span>

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

<span data-ttu-id="6666d-108">Il problema si verifica perché i file del server non vengono eliminati quando si disinstalla l'App-V 5,0 SP1, quindi il processo di installazione di App-V 5,0 SP3 esegue erroneamente un aggiornamento anziché una nuova installazione.</span><span class="sxs-lookup"><span data-stu-id="6666d-108">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the App-V 5.0 SP3 installation process erroneously does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="6666d-109">**Soluzione alternativa**: eliminare la chiave del registro di sistema seguente prima di iniziare l'installazione di App-V 5,0 SP3:</span><span class="sxs-lookup"><span data-stu-id="6666d-109">**Workaround**: Delete the following registry key before you start installing App-V 5.0 SP3:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## <span data-ttu-id="6666d-110">L'esecuzione di query su servizi di dominio Active Directory può causare un funzionamento non corretto delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="6666d-110">Querying AD DS can cause some applications to work incorrectly</span></span>


<span data-ttu-id="6666d-111">Quando si ricevono pacchetti aggiornati eseguendo una query su servizi di dominio Active Directory per le appartenenze ai gruppi aggiornati, può causare un funzionamento non corretto delle applicazioni se le applicazioni dipendono dal token di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6666d-111">When you receive updated packages by querying Active Directory Domain Services for updated group memberships, it can cause some applications to work incorrectly if the applications depend on the user’s access token.</span></span> <span data-ttu-id="6666d-112">Inoltre, le frequenti query di appartenenza ai gruppi possono causare l'overload del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="6666d-112">In addition, frequent group membership queries can cause the domain controller to overload.</span></span> <span data-ttu-id="6666d-113">Per altre informazioni sui token di accesso degli utenti, vedere [token di accesso](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).</span><span class="sxs-lookup"><span data-stu-id="6666d-113">For more information about user access tokens, see [Access Tokens](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).</span></span>

<span data-ttu-id="6666d-114">**Soluzione alternativa**: attendere che l'utente si disconnetta e quindi rieseguire l'accesso prima di eseguire una query per le appartenenze ai gruppi aggiornate.</span><span class="sxs-lookup"><span data-stu-id="6666d-114">**Workaround**: Wait until the user logs off and then logs back on before you query for updated group memberships.</span></span> <span data-ttu-id="6666d-115">Non usare la chiave del registro di sistema, descritta nel [pacchetto hotfix 2 per Microsoft Application Virtualization 5,0 Service Pack 1](https://support.microsoft.com/kb/2897087), per eseguire query per le appartenenze ai gruppi aggiornate.</span><span class="sxs-lookup"><span data-stu-id="6666d-115">Do not use the registry key, described in [Hotfix Package 2 for Microsoft Application Virtualization 5.0 Service Pack 1](https://support.microsoft.com/kb/2897087), to query for updated group memberships.</span></span>






## <span data-ttu-id="6666d-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6666d-116">Related topics</span></span>


[<span data-ttu-id="6666d-117">Informazioni su App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="6666d-117">About App-V 5.0 SP3</span></span>](about-app-v-50-sp3.md)

 

 





