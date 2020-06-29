---
title: Amministrazione di MBAM 1.0 con PowerShell
description: Amministrazione di MBAM 1.0 con PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825136"
---
# Amministrazione di MBAM 1.0 con PowerShell


Microsoft BitLocker Administration and Monitoring (MBAM) fornisce il seguente set di cmdlet di Windows PowerShell. Gli amministratori possono usare questi cmdlet di PowerShell per eseguire varie attività di MBAM server dal prompt dei comandi invece che dal sito Web di amministrazione di MBAM.

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
<td align="left"><p>Add-MbamHardwareType</p></td>
<td align="left"><p>Aggiunge un nuovo modello hardware all'inventario hardware di MBAM. Questo cmdlet può anche specificare se l'hardware è supportato o non supporta la crittografia unità BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Richiede una chiave di ripristino MBAM che consentirà a un utente di sbloccare un computer o un'unità crittografata.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamHardwareType</p></td>
<td align="left"><p>Ottiene un inventario hardware master che contiene dati che indicano se i modelli hardware sono compatibili o non sono compatibili con la crittografia unità BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Fornisce una password del proprietario del TPM per un utente per gestire l'accesso al TPM (Trusted Platform Module). Consente agli utenti quando il TPM li ha bloccati e non accetterà più il PIN.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Installare-Mbam</p></td>
<td align="left"><p>Installa le caratteristiche di MBAM che includono strumenti avanzati per criteri di gruppo, crittografia, recupero di chiavi e report di conformità.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Remove-MbamHardwareType</p></td>
<td align="left"><p>Rimuove i modelli hardware dall'inventario hardware.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Set-MbamHardwareType</p></td>
<td align="left"><p>Consente la gestione di un inventario hardware master per indicare se i modelli hardware sono in grado o non possono eseguire la crittografia BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Disinstallare-mbam</p></td>
<td align="left"><p>Rimuove le caratteristiche di MBAM installate in precedenza che includono strumenti avanzati per i criteri, la crittografia, il recupero delle chiavi e i report di conformità.</p></td>
</tr>
</tbody>
</table>

 

## Argomenti correlati


[Operazioni relative a MBAM 1.0](operations-for-mbam-10.md)

 

 





