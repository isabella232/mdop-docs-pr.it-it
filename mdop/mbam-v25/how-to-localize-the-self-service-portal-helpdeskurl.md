---
title: Come localizzare il portale self-service "HelpdeskURL"
description: Come localizzare il portale self-service "HelpdeskURL"
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826706"
---
# <span data-ttu-id="bfa2c-103">Come localizzare il portale self-service "HelpdeskURL"</span><span class="sxs-lookup"><span data-stu-id="bfa2c-103">How to Localize the Self-Service Portal “HelpdeskURL”</span></span>


<span data-ttu-id="bfa2c-104">Puoi configurare una versione localizzata dell'URL del portale self-service da visualizzare agli utenti finali per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-104">You can configure a localized version of the Self-Service Portal URL to display to end users by default.</span></span> <span data-ttu-id="bfa2c-105">L'URL del portale self-service è rappresentato dal parametro **HelpdeskURL**.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-105">The Self-Service Portal URL is represented by the parameter **HelpdeskURL**.</span></span>

<span data-ttu-id="bfa2c-106">Se si crea una versione localizzata, come descritto nelle istruzioni seguenti, Microsoft BitLocker Administration and Monitoring (MBAM) trova e visualizza la versione localizzata.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-106">If you create a localized version, as described in the following instructions, Microsoft BitLocker Administration and Monitoring (MBAM) finds and displays the localized version.</span></span> <span data-ttu-id="bfa2c-107">Se MBAM non trova una versione localizzata, Visualizza l'URL configurato per il parametro **HelpDeskURL**.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-107">If MBAM does not find a localized version, it displays the URL that is configured for the parameter **HelpDeskURL**.</span></span>

<span data-ttu-id="bfa2c-108">**Nota**  Nelle istruzioni seguenti, *selfservice* è il nome della directory virtuale predefinita per il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-108">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="bfa2c-109">Quando hai configurato il portale self-service, potresti aver usato un nome diverso.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-109">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="bfa2c-110">Per localizzare l'URL del portale self-service</span><span class="sxs-lookup"><span data-stu-id="bfa2c-110">To localize the Self-Service Portal URL</span></span>**

1.  <span data-ttu-id="bfa2c-111">Nel server in cui è stato configurato il portale self-service individuare i **siti** di &gt; **amministrazione e monitoraggio** &gt; **SelfService** &gt; **delle impostazioni delle applicazioni**di Microsoft BitLocker selfservice.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-111">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="bfa2c-112">Nel riquadro **azioni** fare clic su **Aggiungi** per aprire la finestra di dialogo **Aggiungi impostazioni applicazione** .</span><span class="sxs-lookup"><span data-stu-id="bfa2c-112">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="bfa2c-113">Nel campo **nome** Digitare **HelpdeskURL**\ _ &lt; *lingua* &gt; , dove &lt; *lingua* &gt; è il codice di lingua appropriato per l'URL.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-113">In the **Name** field, type **HelpdeskURL**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the URL.</span></span>

    <span data-ttu-id="bfa2c-114">Ad esempio, per creare una versione localizzata del `HelpdeskURL` valore in spagnolo, denominare il parametro **HelpdeskURL \ _es-es**.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-114">For example, to create a localized version of the `HelpdeskURL` value in Spanish, name the parameter **HelpdeskURL\_es-es**.</span></span>

    <span data-ttu-id="bfa2c-115">Il nome della cartella della lingua può essere anche il nome neutro della lingua **es** anziché **es-es**.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-115">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="bfa2c-116">Se il browser dell'utente finale è impostato su **es-es** e tale cartella non esiste, le impostazioni locali padre (come definito in .NET) vengono recuperate e controllate ricorsivamente, risolvendo &lt; la directory di installazione di mbam Self-Service &gt;\\SelfServiceWebsite\\es\\Notice.txt prima di diventare definitivamente il file di Notice.txt predefinito.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-116">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="bfa2c-117">Questo fallback ricorsivo simula le regole di caricamento delle risorse .NET.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-117">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="bfa2c-118">Per un elenco dei codici di lingua validi che è possibile usare, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="bfa2c-118">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="bfa2c-119">Nel campo **valore** Digitare la versione localizzata del `HelpdeskURL` valore che si desidera visualizzare per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="bfa2c-119">In the **Value** field, type the localized version of the `HelpdeskURL` value that you want to display to end users.</span></span>



## <span data-ttu-id="bfa2c-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bfa2c-120">Related topics</span></span>


[<span data-ttu-id="bfa2c-121">Personalizzazione del portale self-service per l'organizzazione</span><span class="sxs-lookup"><span data-stu-id="bfa2c-121">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 
## <span data-ttu-id="bfa2c-122">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="bfa2c-122">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="bfa2c-123">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="bfa2c-123">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="bfa2c-124">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="bfa2c-124">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




