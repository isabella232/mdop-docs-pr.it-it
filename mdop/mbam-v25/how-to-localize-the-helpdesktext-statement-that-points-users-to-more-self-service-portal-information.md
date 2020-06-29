---
title: Come localizzare l'istruzione "HelpdeskText" che indirizza gli utenti verso altre informazioni nel portale self-service
description: Come localizzare l'istruzione "HelpdeskText" che indirizza gli utenti verso altre informazioni nel portale self-service
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823425"
---
# <span data-ttu-id="c8ee7-103">Come localizzare l'istruzione "HelpdeskText" che indirizza gli utenti verso altre informazioni nel portale self-service</span><span class="sxs-lookup"><span data-stu-id="c8ee7-103">How to Localize the “HelpdeskText” Statement that Points Users to More Self-Service Portal Information</span></span>


<span data-ttu-id="c8ee7-104">È possibile configurare una versione localizzata dell'istruzione Self-Service Portal "HelpdeskText", che informa gli utenti finali su come ottenere assistenza aggiuntiva quando usano il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-104">You can configure a localized version of the Self-Service Portal "HelpdeskText" statement, which informs end users about how to get additional help when they are using the Self-Service Portal.</span></span> <span data-ttu-id="c8ee7-105">Se si configura il testo localizzato per l'istruzione, come descritto nelle istruzioni seguenti, MBAM Visualizza la versione localizzata.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-105">If you configure localized text for the statement, as described in the following instructions, MBAM displays the localized version.</span></span> <span data-ttu-id="c8ee7-106">Se MBAM non trova la versione localizzata, Visualizza il valore che si trova nel parametro **HelpdeskText** .</span><span class="sxs-lookup"><span data-stu-id="c8ee7-106">If MBAM does not find the localized version, it displays the value that is in the **HelpdeskText** parameter.</span></span>

<span data-ttu-id="c8ee7-107">**Nota**  Nelle istruzioni seguenti, *selfservice* è il nome della directory virtuale predefinita per il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-107">**Note** In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="c8ee7-108">Quando hai configurato il portale self-service, potresti aver usato un nome diverso.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-108">You might have used a different name when you configured the Self-Service Portal.</span></span>

 

**<span data-ttu-id="c8ee7-109">Per visualizzare una versione localizzata dell'istruzione HelpdeskText</span><span class="sxs-lookup"><span data-stu-id="c8ee7-109">To display a localized version of the HelpdeskText statement</span></span>**

1.  <span data-ttu-id="c8ee7-110">Nel server in cui è stato configurato il portale self-service individuare i **siti** di &gt; **amministrazione e monitoraggio** &gt; **SelfService** &gt; **delle impostazioni delle applicazioni**di Microsoft BitLocker selfservice.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-110">On the server where you configured the Self-Service Portal, browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

2.  <span data-ttu-id="c8ee7-111">Nel riquadro **azioni** fare clic su **Aggiungi** per aprire la finestra di dialogo **Aggiungi impostazioni applicazione** .</span><span class="sxs-lookup"><span data-stu-id="c8ee7-111">In the **Actions** pane, click **Add** to open the **Add Application Setting** dialog box.</span></span>

3.  <span data-ttu-id="c8ee7-112">Nel campo **nome** Digitare **HelpdeskText**\ _ &lt; *lingua* &gt; , dove &lt; *lingua* &gt; è il codice di lingua appropriato per il testo.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-112">In the **Name** field, type **HelpdeskText**\_&lt;*Language*&gt;, where &lt;*Language*&gt; is the appropriate language code for the text.</span></span>

    <span data-ttu-id="c8ee7-113">Ad esempio, per creare un'istruzione HelpdeskText localizzata in spagnolo, denominare il parametro **HelpdeskText \ _es-es**.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-113">For example, to create a localized HelpdeskText statement in Spanish, name the parameter **HelpdeskText\_es-es**.</span></span>

    <span data-ttu-id="c8ee7-114">Il nome della cartella della lingua può essere anche il nome neutro della lingua **es** anziché **es-es**.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-114">The name of the Language folder can also be the language neutral name **es** instead of **es-es**.</span></span> <span data-ttu-id="c8ee7-115">Se il browser dell'utente finale è impostato su **es-es** e tale cartella non esiste, le impostazioni locali padre (come definito in .NET) vengono recuperate e controllate ricorsivamente, risolvendo &lt; la directory di installazione di mbam Self-Service &gt;\\SelfServiceWebsite\\es\\Notice.txt prima di diventare definitivamente il file di Notice.txt predefinito.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-115">If the end user’s browser is set to **es-es** and that folder does not exist, the parent locale (as defined in .NET) is recursively retrieved and checked, resolving to &lt;MBAM Self-Service Install Directory&gt;\\SelfServiceWebsite\\es\\Notice.txt before finally becoming the default Notice.txt file.</span></span> <span data-ttu-id="c8ee7-116">Questo fallback ricorsivo simula le regole di caricamento delle risorse .NET.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-116">This recursive fallback mimics the .NET resource loading rules.</span></span>

    <span data-ttu-id="c8ee7-117">Per un elenco dei codici di lingua validi che è possibile usare, vedere informazioni di [riferimento sulle API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).</span><span class="sxs-lookup"><span data-stu-id="c8ee7-117">For a list of the valid language codes you can use, see [National Language Support (NLS) API Reference](https://go.microsoft.com/fwlink/?LinkId=317947).</span></span>

4.  <span data-ttu-id="c8ee7-118">Nel campo **valore** Digitare il testo localizzato che si vuole visualizzare per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="c8ee7-118">In the **Value** field, type the localized text that you want to display to end users.</span></span>



## <span data-ttu-id="c8ee7-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8ee7-119">Related topics</span></span>


[<span data-ttu-id="c8ee7-120">Personalizzazione del portale self-service per l'organizzazione</span><span class="sxs-lookup"><span data-stu-id="c8ee7-120">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)

 

 

## <span data-ttu-id="c8ee7-121">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="c8ee7-121">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="c8ee7-122">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="c8ee7-122">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="c8ee7-123">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="c8ee7-123">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



