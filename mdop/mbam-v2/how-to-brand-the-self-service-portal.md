---
title: Come personalizzare il portale self-service
description: Come personalizzare il portale self-service
author: dansimp
ms.assetid: 3ef9e951-7c42-4f7f-b131-3765d39b3207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe4f4efc5852042671711ba5780cc78055957ba8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825146"
---
# <span data-ttu-id="4e462-103">Come personalizzare il portale self-service</span><span class="sxs-lookup"><span data-stu-id="4e462-103">How to Brand the Self-Service Portal</span></span>


<span data-ttu-id="4e462-104">Dopo aver installato il portale self-service per l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM), è possibile personalizzare il portale self-service con il nome della società, l'URL del supporto tecnico e il testo "nota".</span><span class="sxs-lookup"><span data-stu-id="4e462-104">After you install the Microsoft BitLocker Administration and Monitoring (MBAM) Self-Service Portal, you can brand the Self-Service Portal with your company name, Help Desk URL, and “notice” text.</span></span> <span data-ttu-id="4e462-105">È anche possibile modificare l'impostazione di timeout della sessione per impostare la scadenza della sessione dell'utente finale dopo un periodo di inattività specificato.</span><span class="sxs-lookup"><span data-stu-id="4e462-105">You can also change the Session Timeout setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="4e462-106">Per impostare il timeout della sessione e il branding per il portale self-service</span><span class="sxs-lookup"><span data-stu-id="4e462-106">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="4e462-107">Per impostare il periodo di timeout per la sessione dell'utente finale, avviare **Internet Information Services Manager**oppure eseguire **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="4e462-107">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="4e462-108">Passare a **siti** di &gt; **amministrazione e monitoraggio di Microsoft BitLocker** &gt; **selfservice** &gt; **ASP.NET** lo &gt; **stato sessione**e modificare il valore di **timeout** in **Impostazioni cookie** per il numero di minuti dopo il quale scadrà la sessione del portale self-service dell'utente finale.</span><span class="sxs-lookup"><span data-stu-id="4e462-108">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session will expire.</span></span> <span data-ttu-id="4e462-109">L'impostazione predefinita è 5.</span><span class="sxs-lookup"><span data-stu-id="4e462-109">The default is 5.</span></span> <span data-ttu-id="4e462-110">Per disabilitare l'impostazione in modo che non ci sia un timeout, imposta il valore su **0**.</span><span class="sxs-lookup"><span data-stu-id="4e462-110">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="4e462-111">Per impostare gli elementi di personalizzazione per il portale self-service, avviare **Internet Information Services Manager**oppure eseguire **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="4e462-111">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="4e462-112">Individuare i **siti** di &gt; **amministrazione e monitoraggio** &gt; **SelfService** &gt; **delle impostazioni dell'applicazione**selfservice di Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4e462-112">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="4e462-113">Nella colonna **nome** selezionare l'elemento che si vuole modificare e cambiare il valore predefinito in modo che corrisponda al nome che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="4e462-113">From the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="4e462-114">Nella tabella seguente sono elencati i valori che è possibile impostare.</span><span class="sxs-lookup"><span data-stu-id="4e462-114">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="4e462-115">Attenzione</span><span class="sxs-lookup"><span data-stu-id="4e462-115">Caution</span></span>**  
    <span data-ttu-id="4e462-116">Non modificare il valore nella colonna Name (CompanyName \ \*), perché il portale self-service smetterà di funzionare.</span><span class="sxs-lookup"><span data-stu-id="4e462-116">Do not change the value in the Name column (CompanyName\*), as it will cause the Self-Service Portal to stop working.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CompanyName*</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText*</p></td>
<td align="left"><p>Contact Help Desk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl*</p></td>
<td align="left"><p>Http://www.microsoft.com</p></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.2.min.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MicrosoftAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/3.5/MicrosoftAjax.js</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftMvcAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/mvc/2.0/MicrosoftMvcValidation.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the Notice text either by using the IIS Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>
~~~



## <span data-ttu-id="4e462-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4e462-117">Related topics</span></span>


[<span data-ttu-id="4e462-118">Distribuzione dell'infrastruttura server di MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4e462-118">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









