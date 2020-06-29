---
title: Come impostare il timeout della sessione e la personalizzazione del portale self-service
description: Come impostare il timeout della sessione e la personalizzazione del portale self-service
author: dansimp
ms.assetid: 031eedfc-fade-4d2f-8771-b329e1d38c0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e222880b2d5557ef15cd7a4efd6421b9972541f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804299"
---
# <span data-ttu-id="cb0bc-103">Come impostare il timeout della sessione e la personalizzazione del portale self-service</span><span class="sxs-lookup"><span data-stu-id="cb0bc-103">How to Set the Self-Service Portal Branding and Session Time-out</span></span>


<span data-ttu-id="cb0bc-104">Dopo aver configurato il portale self-service, è possibile personalizzarlo con il nome della società, l'URL del supporto tecnico e il testo "nota".</span><span class="sxs-lookup"><span data-stu-id="cb0bc-104">After you configure the Self-Service Portal, you can brand it with your company name, Help Desk URL, and "notice" text.</span></span> <span data-ttu-id="cb0bc-105">È anche possibile modificare l'impostazione di timeout della sessione per impostare la scadenza della sessione dell'utente finale dopo un periodo di inattività specificato.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-105">You can also change the Session Time-out setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="cb0bc-106">Nota</span><span class="sxs-lookup"><span data-stu-id="cb0bc-106">Note</span></span>**  
<span data-ttu-id="cb0bc-107">Puoi anche personalizzare il portale self-service usando il cmdlet di Windows PowerShell **Enable-MbamWebApplication** o la configurazione guidata del server mbam.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-107">You can also brand the Self-Service Portal by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="cb0bc-108">Per istruzioni sull'uso della procedura guidata, vedere [come configurare le applicazioni Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="cb0bc-108">For instructions on using the wizard, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>



**<span data-ttu-id="cb0bc-109">Nota</span><span class="sxs-lookup"><span data-stu-id="cb0bc-109">Note</span></span>**  
<span data-ttu-id="cb0bc-110">Nelle istruzioni seguenti, *selfservice* è il nome della directory virtuale predefinita per il portale self-service.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-110">In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="cb0bc-111">Quando hai configurato il portale self-service, potresti aver usato un nome diverso.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-111">You might have used a different name when you configured the Self-Service Portal.</span></span>



**<span data-ttu-id="cb0bc-112">Per impostare il timeout della sessione e il branding per il portale self-service</span><span class="sxs-lookup"><span data-stu-id="cb0bc-112">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="cb0bc-113">Per impostare il periodo di timeout per la sessione dell'utente finale, avviare **Internet Information Services Manager**oppure eseguire **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-113">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="cb0bc-114">Passare a **siti** di &gt; **amministrazione e monitoraggio di Microsoft BitLocker** &gt; **selfservice** lo &gt; **ASP.NET** &gt; **stato sessione**di ASP.NET e modificare il valore di **timeout** in **Impostazioni cookie** per il numero di minuti dopo il quale scade la sessione del portale self-service dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-114">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session expires.</span></span> <span data-ttu-id="cb0bc-115">Il valore predefinito è **5**.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-115">The default value is **5**.</span></span> <span data-ttu-id="cb0bc-116">Per disabilitare l'impostazione in modo che non ci sia un timeout, imposta il valore su **0**.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-116">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="cb0bc-117">Per impostare gli elementi di personalizzazione per il portale self-service, avviare **Internet Information Services Manager** o eseguire **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-117">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager** or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="cb0bc-118">Individuare i **siti** di &gt; **amministrazione e monitoraggio** &gt; **SelfService** &gt; **delle impostazioni dell'applicazione**selfservice di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-118">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="cb0bc-119">Nella colonna **nome** selezionare l'elemento che si vuole modificare e modificare il valore predefinito in modo che corrisponda al nome che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-119">In the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="cb0bc-120">Nella tabella seguente sono elencati i valori che è possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-120">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="cb0bc-121">Attenzione</span><span class="sxs-lookup"><span data-stu-id="cb0bc-121">Caution</span></span>**  
    <span data-ttu-id="cb0bc-122">Non modificare il valore nella colonna nome (CompanyName \ \*), perché il portale self-service non funzionerà più.</span><span class="sxs-lookup"><span data-stu-id="cb0bc-122">Do not change the value in the Name column (CompanyName\*), as it will cause Self-Service Portal to stop working.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ClientValidationEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>CompanyName</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DisplayNotice</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText</p></td>
<td align="left"><p>Contact Helpdesk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl</p></td>
<td align="left"><p>#</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, the HelpdeskUrl default value is empty.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390515](//go.microsoft.com/fwlink/?LinkID=390515)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery-1.10.2.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>jQueryValidatePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390516](//go.microsoft.com/fwlink/?LinkID=390516)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryValidateUnobtrusivePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390517](//go.microsoft.com/fwlink/?LinkID=390517)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.unobtrusive.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the notice text either by using the Internet Information Services (IIS) Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>UnobtrusiveJavaScriptEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
</tbody>
</table>
~~~





## <span data-ttu-id="cb0bc-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb0bc-123">Related topics</span></span>


[<span data-ttu-id="cb0bc-124">Personalizzazione del portale self-service per l'organizzazione</span><span class="sxs-lookup"><span data-stu-id="cb0bc-124">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)



## <span data-ttu-id="cb0bc-125">Hai un suggerimento per MBAM?</span><span class="sxs-lookup"><span data-stu-id="cb0bc-125">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="cb0bc-126">Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="cb0bc-126">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="cb0bc-127">Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="cb0bc-127">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





