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
# Come personalizzare il portale self-service


Dopo aver installato il portale self-service per l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM), è possibile personalizzare il portale self-service con il nome della società, l'URL del supporto tecnico e il testo "nota". È anche possibile modificare l'impostazione di timeout della sessione per impostare la scadenza della sessione dell'utente finale dopo un periodo di inattività specificato.

**Per impostare il timeout della sessione e il branding per il portale self-service**

1.  Per impostare il periodo di timeout per la sessione dell'utente finale, avviare **Internet Information Services Manager**oppure eseguire **inetmgr.exe**.

2.  Passare a **siti** di &gt; **amministrazione e monitoraggio di Microsoft BitLocker** &gt; **selfservice** &gt; **ASP.NET** lo &gt; **stato sessione**e modificare il valore di **timeout** in **Impostazioni cookie** per il numero di minuti dopo il quale scadrà la sessione del portale self-service dell'utente finale. L'impostazione predefinita è 5. Per disabilitare l'impostazione in modo che non ci sia un timeout, imposta il valore su **0**.

3.  Per impostare gli elementi di personalizzazione per il portale self-service, avviare **Internet Information Services Manager**oppure eseguire **inetmgr.exe**.

4.  Individuare i **siti** di &gt; **amministrazione e monitoraggio** &gt; **SelfService** &gt; **delle impostazioni dell'applicazione**selfservice di Microsoft BitLocker.

5.  Nella colonna **nome** selezionare l'elemento che si vuole modificare e cambiare il valore predefinito in modo che corrisponda al nome che si vuole usare. Nella tabella seguente sono elencati i valori che è possibile impostare.

    **Attenzione**  
    Non modificare il valore nella colonna Name (CompanyName \ *), perché il portale self-service smetterà di funzionare.



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



## Argomenti correlati


[Distribuzione dell'infrastruttura server di MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









