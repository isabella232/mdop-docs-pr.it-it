---
title: Come aggiungere o rimuovere le informazioni sul reindirizzamento URL in un'area di lavoro MED-V distribuita
description: Come aggiungere o rimuovere le informazioni sul reindirizzamento URL in un'area di lavoro MED-V distribuita
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826445"
---
# <span data-ttu-id="37c49-103">Come aggiungere o rimuovere le informazioni sul reindirizzamento URL in un'area di lavoro MED-V distribuita</span><span class="sxs-lookup"><span data-stu-id="37c49-103">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>


<span data-ttu-id="37c49-104">Per modificare le informazioni di reindirizzamento degli URL in un'area di lavoro MED-V distribuita, è consigliabile aggiornare il registro di sistema tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="37c49-104">To edit URL redirection information in a deployed MED-V workspace, we recommend that you update the system registry by using Group Policy.</span></span> <span data-ttu-id="37c49-105">Anche se non è consigliabile, è anche possibile ricostruire e ridistribuire l'area di lavoro MED-V con le informazioni aggiornate sul reindirizzamento degli URL.</span><span class="sxs-lookup"><span data-stu-id="37c49-105">Although we do not recommend it, you can also rebuild and redeploy the MED-V workspace with the updated URL redirection information.</span></span>

<span data-ttu-id="37c49-106">La chiave del registro di sistema si trova in genere in:</span><span class="sxs-lookup"><span data-stu-id="37c49-106">The registry key is usually located at:</span></span>

<span data-ttu-id="37c49-107">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="37c49-107">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="37c49-108">Deve essere presente il valore multistringa seguente:</span><span class="sxs-lookup"><span data-stu-id="37c49-108">The following multi-string value must be present:</span></span> `RedirectUrls`

<span data-ttu-id="37c49-109">I dati del valore per `RedirectUrls` sono un elenco di tutti gli URL specificati per il reindirizzamento quando è stato compilato il pacchetto dell'area di lavoro MED-v tramite **Packager area di lavoro MED-v**.</span><span class="sxs-lookup"><span data-stu-id="37c49-109">The value data for `RedirectUrls` is a list of all of the URLs that you specified for redirection when you built the MED-V workspace package by using the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="37c49-110">Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="37c49-110">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="37c49-111">È possibile aggiungere e rimuovere informazioni sul reindirizzamento degli URL eseguendo una delle attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="37c49-111">You can add and remove URL redirection information by performing one of the following tasks:</span></span>

-   [<span data-ttu-id="37c49-112">Modificare la chiave del registro di sistema di reindirizzamento URL e distribuire tramite criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="37c49-112">Edit the URL Redirection Registry Key and Deploy Using Group Policy</span></span>](#bkmk-editreg)

-   [<span data-ttu-id="37c49-113">Modificare il file di testo del reindirizzamento degli URL e ricostruire l'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="37c49-113">Edit the URL Redirection Text File and Rebuild the MED-V Workspace</span></span>](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**<span data-ttu-id="37c49-114">Per aggiornare le informazioni sul reindirizzamento degli URL tramite criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="37c49-114">To update URL Redirection information by using Group Policy</span></span>**

1.  <span data-ttu-id="37c49-115">Modificare il valore multistringa della chiave del registro di sistema denominato `RedirectUrls` .</span><span class="sxs-lookup"><span data-stu-id="37c49-115">Edit the registry key multi-string value that is named `RedirectUrls`.</span></span> <span data-ttu-id="37c49-116">Questo valore si trova in genere in:</span><span class="sxs-lookup"><span data-stu-id="37c49-116">This value is typically located at:</span></span>

    <span data-ttu-id="37c49-117">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="37c49-117">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

    <span data-ttu-id="37c49-118">Se si aggiungono URL alla chiave del registro di sistema, immetterli uno per riga, come richiesto quando si è compilato il pacchetto dell'area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="37c49-118">If you are adding URLs to the registry key, enter them one per line, as was required when you built the MED-V workspace package.</span></span> <span data-ttu-id="37c49-119">Per altre informazioni, vedere [creare un pacchetto di area di lavoro MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="37c49-119">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

2.  <span data-ttu-id="37c49-120">Distribuire la chiave del registro di sistema aggiornata usando criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="37c49-120">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="37c49-121">Per altre informazioni sull'uso dei criteri di gruppo, vedere [installazione del software criteri di gruppo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="37c49-121">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

<span data-ttu-id="37c49-122">**Nota**  Questo metodo per modificare le informazioni sul reindirizzamento degli URL è una procedura consigliata per MED-V.</span><span class="sxs-lookup"><span data-stu-id="37c49-122">**Note** This method of editing URL redirection information is a MED-V best practice.</span></span>

 

<a href="" id="bkmk-edittext"></a>**<span data-ttu-id="37c49-123">Per ricompilare l'area di lavoro MED-V usando un file di testo URL aggiornato</span><span class="sxs-lookup"><span data-stu-id="37c49-123">To rebuild the MED-V workspace by using an updated URL text file</span></span>**

-   <span data-ttu-id="37c49-124">Un altro metodo per l'aggiunta e la rimozione di URL dall'elenco di reindirizzamento consiste nell'aggiornare il file di testo del reindirizzamento degli URL e quindi usarlo per creare una nuova area di lavoro MED-V.</span><span class="sxs-lookup"><span data-stu-id="37c49-124">Another method of adding and removing URLs from the redirection list is to update the URL redirection text file and then use it to build a new MED-V workspace.</span></span> <span data-ttu-id="37c49-125">Puoi quindi ridistribuire l'area di lavoro MED-V come prima, usando il processo standard di distribuzione, ad esempio un sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="37c49-125">You can then redeploy the MED-V workspace as before, by using your standard process of deployment, such as an ESD system.</span></span>

    <span data-ttu-id="37c49-126">**Importante**  Non è consigliabile questo metodo per modificare le informazioni di reindirizzamento degli URL.</span><span class="sxs-lookup"><span data-stu-id="37c49-126">**Important** We do not recommend this method of editing URL redirection information.</span></span> <span data-ttu-id="37c49-127">Inoltre, ogni volta che si ridistribuisce l'area di lavoro MED-V nell'organizzazione, è necessario eseguire di nuovo la configurazione per la prima volta e tutti i dati salvati nella macchina virtuale andranno perduti.</span><span class="sxs-lookup"><span data-stu-id="37c49-127">In addition, any time that you redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="37c49-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37c49-128">Related topics</span></span>


[<span data-ttu-id="37c49-129">Come verificare il reindirizzamento URL</span><span class="sxs-lookup"><span data-stu-id="37c49-129">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="37c49-130">Gestione delle applicazioni distribuite in aree di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="37c49-130">Managing Applications Deployed to MED-V Workspaces</span></span>](managing-applications-deployed-to-med-v-workspaces.md)

[<span data-ttu-id="37c49-131">Creare un pacchetto nell'area di lavoro MED-V</span><span class="sxs-lookup"><span data-stu-id="37c49-131">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

 

 





