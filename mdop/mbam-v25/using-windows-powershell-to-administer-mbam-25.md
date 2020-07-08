---
title: Uso di Windows PowerShell per l'amministrazione di MBAM 2.5
description: Uso di Windows PowerShell per l'amministrazione di MBAM 2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804450"
---
# Uso di Windows PowerShell per l'amministrazione di MBAM 2.5


Questo argomento descrive i cmdlet di Windows PowerShell per l'amministrazione e il monitoraggio di Microsoft BitLocker (MBAM) correlati al recupero di computer o unità quando gli utenti vengono bloccati.

Per i cmdlet che si usano per configurare le caratteristiche di MBAM server, vedere [configurazione delle caratteristiche del server mbam 2,5 tramite Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a>Cmdlet per il recupero di computer o unità gestite da MBAM


Usare i cmdlet di Windows PowerShell seguenti per recuperare i computer o le unità gestite da MBAM.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nome</th>
<th align="left">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Richiede una chiave di ripristino MBAM che consente agli utenti di sbloccare un computer o un'unità crittografata.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Fornisce agli utenti una password del proprietario del TPM che possono usare per sbloccare un TPM (Trusted Platform Module) quando il TPM li ha bloccati e non accetterà più il PIN.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> Guida per i cmdlet di MBAM


La Guida di Windows PowerShell per i cmdlet MBAM è disponibile nei formati seguenti:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato della Guida di Windows PowerShell</th>
<th align="left">Altre informazioni</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>In un prompt dei comandi di Windows PowerShell digitare <strong> Get-Help </strong> &lt; <em> cmdlet</em>&gt;</p></td>
<td align="left"><p>Per caricare i più recenti cmdlet di Windows PowerShell, seguire le istruzioni visualizzate nella pagina <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> configurazione delle caratteristiche del server MBAM 2,5 tramite Windows PowerShell</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>In TechNet come pagine Web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nell'area download come file di Word. docx</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Nell'area download come file PDF</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## Argomenti correlati


[Amministrazione delle funzionalità di MBAM 2.5](administering-mbam-25-features.md)

[Configurazione delle funzionalità del server di MBAM 2.5 con Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## Hai un suggerimento per MBAM?
- Aggiungere o votare i suggerimenti [qui](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Per i problemi di MBAM, usa il [Forum di mbam TechNet](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





