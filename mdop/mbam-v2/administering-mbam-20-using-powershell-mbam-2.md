---
title: Amministrazione di MBAM 2.0 con PowerShell
description: Amministrazione di MBAM 2.0 con PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823505"
---
# Amministrazione di MBAM 2.0 con PowerShell


Microsoft BitLocker Administration and Monitoring (MBAM) fornisce il seguente set di cmdlet di Windows PowerShell. Gli amministratori possono usare questi cmdlet di PowerShell per eseguire varie attività di amministrazione e monitoraggio di Microsoft BitLocker dalla riga di comando invece che dal sito Web di amministrazione di MBAM.

## Come amministrare MBAM usando PowerShell


Usare i cmdlet di PowerShell descritti qui per amministrare MBAM.

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
<td align="left"><p>Installare-Mbam</p></td>
<td align="left"><p>Installa le caratteristiche di MBAM che includono criteri avanzati, crittografia, ripristino delle chiavi e report di conformità.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Disinstallare-mbam</p></td>
<td align="left"><p>Rimuove le caratteristiche di MBAM che consentono di usare criteri avanzati, crittografia, recupero chiavi e strumenti per la creazione di report di conformità.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Richiede una chiave di ripristino MBAM che consentirà agli utenti di sbloccare un computer o un'unità crittografata.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Fornisce agli utenti una password del proprietario del TPM che possono usare per sbloccare un TPM (Trusted Platform Module) quando il TPM li ha bloccati e non accetterà più il PIN.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Operazioni relative a MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





