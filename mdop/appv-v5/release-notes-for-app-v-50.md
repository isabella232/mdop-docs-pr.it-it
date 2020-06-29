---
title: Note sulla versione per App-V 5.0
description: Note sulla versione per App-V 5.0
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804888"
---
# <span data-ttu-id="a3508-103">Note sulla versione per App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a3508-103">Release Notes for App-V 5.0</span></span>


**<span data-ttu-id="a3508-104">Per cercare un problema specifico in queste note sulla versione, premere CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="a3508-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="a3508-105">Leggere accuratamente queste note sulla versione prima di installare App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a3508-105">Read these release notes thoroughly before you install App-V 5.0.</span></span>

<span data-ttu-id="a3508-106">Queste note sulla versione contengono informazioni necessarie per installare correttamente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a3508-106">These release notes contain information that is required to successfully install App-V 5.0.</span></span> <span data-ttu-id="a3508-107">Le note sulla versione contengono anche informazioni che non sono disponibili nella documentazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="a3508-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="a3508-108">Se c'è una differenza tra queste note sulla versione e altre documentazioni di App-V 5,0, l'ultima modifica deve essere considerata autorevole.</span><span class="sxs-lookup"><span data-stu-id="a3508-108">If there is a difference between these release notes and other App-V 5.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="a3508-109">Queste note sulla versione sostituiscono il contenuto incluso in questo prodotto.</span><span class="sxs-lookup"><span data-stu-id="a3508-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="a3508-110">Informazioni sulla documentazione del prodotto</span><span class="sxs-lookup"><span data-stu-id="a3508-110">About the Product Documentation</span></span>


<span data-ttu-id="a3508-111">Per informazioni sulla documentazione di App-V 5,0, vedere la Home page di App-V 5,0 in Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="a3508-111">For information about App-V 5.0 documentation, see the App-V 5.0 home page on Microsoft TechNet.</span></span>

## <span data-ttu-id="a3508-112">Inviare commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="a3508-112">Provide Feedback</span></span>


<span data-ttu-id="a3508-113">Siamo interessati a ricevere commenti e suggerimenti su App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a3508-113">We are interested in your feedback on App-V 5.0.</span></span> <span data-ttu-id="a3508-114">È possibile inviare il proprio feedback <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="a3508-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="a3508-115">**Nota**  Questo indirizzo di posta elettronica non è un canale di supporto, ma il feedback ci aiuterà a pianificare le modifiche future nella documentazione e nei rilasci del prodotto.</span><span class="sxs-lookup"><span data-stu-id="a3508-115">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="a3508-116">Per le informazioni più aggiornate su MDOP e sulle risorse di formazione aggiuntive, vedere la pagina relativa all' [esperienza di MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="a3508-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="a3508-117">Per altre informazioni sui nuovi aggiornamenti o per inviare commenti e suggerimenti, seguici su [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="a3508-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="a3508-118">Problemi noti di App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="a3508-118">Known Issues with App-V 5.0</span></span>


<span data-ttu-id="a3508-119">Questa sezione contiene note sulla versione sui problemi noti di App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a3508-119">This section contains release notes about the known issues with App-V 5.0.</span></span>

### <span data-ttu-id="a3508-120">Non è possibile terminare l'aggiunta di pacchetti quando si usano i cmdlet di PowerShell per server</span><span class="sxs-lookup"><span data-stu-id="a3508-120">Unable to terminate adding packages when using server PowerShell cmdlets</span></span>

<span data-ttu-id="a3508-121">Quando si aggiunge un pacchetto con PowerShell, non esiste alcun metodo per uscire dall'aggiunta di nuovi pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a3508-121">When you add a package using PowerShell, there is no method to exit adding new packages.</span></span>

<span data-ttu-id="a3508-122">SOLUZIONE alternativa: per interrompere l'aggiunta di pacchetti, premere **invio** dopo aver aggiunto il pacchetto finale.</span><span class="sxs-lookup"><span data-stu-id="a3508-122">WORKAROUND: To stop adding packages, press **enter** after you have added the final package.</span></span>

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> <span data-ttu-id="a3508-123">Il client App-V 5,0 rifiuta i pacchetti dai server il cui certificato SSL è stato revocato</span><span class="sxs-lookup"><span data-stu-id="a3508-123">App-V 5.0 client rejects packages from servers whose SSL certificate has been revoked</span></span>

<span data-ttu-id="a3508-124">Quando si usa il protocollo HTTPS, per impostazione predefinita il client App-V 5,0 rifiuterà i pacchetti da server il cui certificato SSL è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="a3508-124">When using the HTTPS protocol, the App-V 5.0 client will by default reject packages from servers whose SSL certificate has been revoked.</span></span> <span data-ttu-id="a3508-125">Questo comportamento può essere disattivato tramite la configurazione modificando l'impostazione **VerifyCertificateRevocationList** .</span><span class="sxs-lookup"><span data-stu-id="a3508-125">This behavior can be turned off through configuration by modifying the **VerifyCertificateRevocationList** setting.</span></span> <span data-ttu-id="a3508-126">L'applicazione di una nuova configurazione per questa impostazione non avrà effetto finché non viene riavviato il servizio App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a3508-126">Applying new configuration for this setting will not take effect until the App-V 5.0 service is restarted.</span></span>

<span data-ttu-id="a3508-127">SOLUZIONE alternativa: riavviare il servizio App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="a3508-127">WORKAROUND: Restart the App-V 5.0 service.</span></span>

## <span data-ttu-id="a3508-128">Informazioni sul copyright delle note sulla versione</span><span class="sxs-lookup"><span data-stu-id="a3508-128">Release Notes Copyright Information</span></span>


<span data-ttu-id="a3508-129">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune e WindowsPowerShell sono marchi di fabbrica del gruppo Microsoft di società.</span><span class="sxs-lookup"><span data-stu-id="a3508-129">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="a3508-130">Tutti gli altri marchi sono proprietà dei rispettivi proprietari.</span><span class="sxs-lookup"><span data-stu-id="a3508-130">All other trademarks are property of their respective owners.</span></span>








## <span data-ttu-id="a3508-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3508-131">Related topics</span></span>


[<span data-ttu-id="a3508-132">Informazioni su App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="a3508-132">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





