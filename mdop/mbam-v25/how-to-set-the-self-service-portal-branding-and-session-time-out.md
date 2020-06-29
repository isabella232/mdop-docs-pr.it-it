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
# Come impostare il timeout della sessione e la personalizzazione del portale self-service


Dopo aver configurato il portale self-service, è possibile personalizzarlo con il nome della società, l'URL del supporto tecnico e il testo "nota". È anche possibile modificare l'impostazione di timeout della sessione per impostare la scadenza della sessione dell'utente finale dopo un periodo di inattività specificato.

**Nota**  
Puoi anche personalizzare il portale self-service usando il cmdlet di Windows PowerShell **Enable-MbamWebApplication** o la configurazione guidata del server mbam. Per istruzioni sull'uso della procedura guidata, vedere [come configurare le applicazioni Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).



**Nota**  
Nelle istruzioni seguenti, *selfservice* è il nome della directory virtuale predefinita per il portale self-service. Quando hai configurato il portale self-service, potresti aver usato un nome diverso.



**Per impostare il timeout della sessione e il branding per il portale self-service**

1.  Per impostare il periodo di timeout per la sessione dell'utente finale, avviare **Internet Information Services Manager**oppure eseguire **inetmgr.exe**.

2.  Passare a **siti** di &gt; **amministrazione e monitoraggio di Microsoft BitLocker** &gt; **selfservice** lo &gt; **ASP.NET** &gt; **stato sessione**di ASP.NET e modificare il valore di **timeout** in **Impostazioni cookie** per il numero di minuti dopo il quale scade la sessione del portale self-service dell'utente finale. Il valore predefinito è **5**. Per disabilitare l'impostazione in modo che non ci sia un timeout, imposta il valore su **0**.

3.  Per impostare gli elementi di personalizzazione per il portale self-service, avviare **Internet Information Services Manager** o eseguire **inetmgr.exe**.

4.  Individuare i **siti** di &gt; **amministrazione e monitoraggio** &gt; **SelfService** &gt; **delle impostazioni dell'applicazione**selfservice di Microsoft BitLocker.

5.  Nella colonna **nome** selezionare l'elemento che si vuole modificare e modificare il valore predefinito in modo che corrisponda al nome che si vuole usare. Nella tabella seguente sono elencati i valori che è possibile impostare.

    **Attenzione**  
    Non modificare il valore nella colonna nome (CompanyName \ *), perché il portale self-service non funzionerà più.



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





## Argomenti correlati


[Personalizzazione del portale self-service per l'organizzazione](customizing-the-self-service-portal-for-your-organization.md)



## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





